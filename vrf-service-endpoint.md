---

copyright:
  years: 2019, 2024
lastupdated: "2024-05-07"

keywords: VRF, virtual routing and forwarding, service endpoint, private network, account networking, direct network, services that support service endpoints, service endpoint support, using service endpoints

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Enabling VRF and service endpoints
{: #vrf-service-endpoint}

When using the classic infrastructure, you connect to resources in your account over the {{site.data.keyword.cloud}} public network by default. You can enable virtual routing and forwarding (VRF) to move IP routing for your account and all of its resources into a separate routing table. If VRF is enabled, you can then enable {{site.data.keyword.cloud_notm}} service endpoints to connect directly to resources without using the public network.
{: shortdesc}

Virtual Private Clouds (VPCs) are automatically enabled for virtual routing and forwarding (VRF). To enable service endpoints for your VPC, continue to [Enabling service endpoints](#service-endpoint).
{: note}

By default, classic accounts that were established before 30 November 2023, are included in the {{site.data.keyword.cloud_notm}} general routing table. Previously, if you wanted to convert a classic account to a VRF-style account, you were required to open a support case with {{site.data.keyword.IBM}} Support. Beginning 30 November 2023, any new classic account or any existing classic account that is "empty" (for example, without any provisioned VLANs), will be automatically converted to a VRF-style account the next time that account initiates a private network connection. For more information, see [FAQs about VRF account migration](/docs/account?topic=account-vrf-faqs).
{: attention}

## Before you begin
{: #before-service-endpoint-enablement}

Before you begin, ensure that you meet the following criteria:

* You need a billable account to enable virtual routing and forwarding and {{site.data.keyword.cloud_notm}} service endpoints.
* You must have access to {{site.data.keyword.cloud_notm}} infrastructure in your account. Go to the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Classic Infrastructure** to verify that you have access.

## Enabling VRF in the console
{: #vrf}
{: ui}

VRF allows multiple instances of a routing table to exist in a router and to work simultaneously. When you enable VRF, a separate routing table is created for your account, and connections to and from your account's resources are routed separately on the {{site.data.keyword.cloud_notm}} network. VRF is enabled at the account level, so all resources are affected by this networking change. For more information about VRF technology and how it affects your account's network routing, see [Virtual routing and forwarding on {{site.data.keyword.cloud_notm}}](/docs/dl?topic=dl-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud).

Enabling VRF permanently alters the networking for your account. Be sure that you understand the impact to your account and resources. After you enable VRF, it cannot be disabled.
{: important}

To enable VRF:

1. In the console, go to **Manage > Account**, then click **Account settings**.
2. Go to **Virtual routing and forwarding**, and click **On**. 

For most accounts, this action immediately converts the private network to VRF. For a select few accounts, coordination with {{site.data.keyword.cloud_notm}} support might be required. To create the support case, complete the following steps:

1. Click **Create case**. You must have a Pay-As-You-Go or Subscription account.
2. In the case description, enter your classic infrastructure account number.
3. Click the **Submit** button.

   Don't change the rest of the populated support case information. The information is tailored to ensure that your request is handled as quickly as possible.
   {: tip}

The {{site.data.keyword.cloud_notm}} network engineering team will contact the case owner to schedule a time for your account's networking to be converted to VRF. During the conversion process, connections to resources in your account might be unstable due to packet loss. The conversion takes roughly 15 - 30 minutes, depending on the complexity of your account. If your account has legacy {{site.data.keyword.BluDirectLink}} connections, it might take more time.

Changing an empty account to VRF modifies the behavior of the future resources with no interruption. A short intermittent connectivity loss can occur between your *existing* servers on the private network during the migration process, which is scheduled at a convenient time for you.

The migration does not make any changes to the public network configuration of your VLANs or subnetworks. However, if you have any web or application servers that provide a public-facing service that relies on a private network connection to reach a database, application, or other type of server, be aware that the public-facing service might be disrupted.

VRF is not compatible with IPSec VPN services and limits SSL VPN connections to the resources in the data center of the connection. Alternatively, you can purchase {{site.data.keyword.BluDirectLink}} products for management of your servers, or run your own VPN solution that can be configured with different types of VPNs.

## Enabling service endpoints
{: #service-endpoint}

When {{site.data.keyword.cloud_notm}} service endpoints are enabled in your account, you can choose to expose a private network endpoint when you create a resource. You can then connect directly to this endpoint over the {{site.data.keyword.cloud_notm}} private network rather than the public network. Because resources that use private network endpoints don't have an internet-routable IP address, connections to these resources are more secure. For more information, see [Secure access to services using service endpoints](/docs/account?topic=account-service-endpoints-overview).

Before you can enable service endpoints, VRF must be enabled for your account. Virtual Private Clouds (VPCs) are automatically enabled for VRF.
{: note}

### Enabling service endpoints in the console
{: #service-endpoint-console}
{: ui}

1. In the console, go to **Manage > Account**, then click **Account settings**.
1. From the Service endpoints section, click **On**.

   If you can't click **On**, VRF might not be enabled for your account. Verify that it's enabled by checking the virtual routing and forwarding section.
   
1. Review the impacts to your account, and click **On**.

It might take a few minutes for this change to take effect.

### Enabling service endpoints in the CLI
{: #service-endpoint-cli}
{: cli}

To enable service endpoints from the [{{site.data.keyword.cloud_notm}} CLI](/docs/cli?topic=cli-getting-started), you need version 0.13 or later.

1.  Check whether service endpoints are already enabled in your account.

    ```bash
    ibmcloud account show
    ```
    {: codeblock}

    If `Service Endpoint Enabled` is `false` as shown in the following example, service endpoints are not enabled.

    ```bash
    Retrieving account Mia Example's Account of m.example@example.com...
    OK

    Account ID:                   abc123d0bc2edefthyufffc9b5ca318
    Currently Targeted Account:   true
    Linked Softlayer Account:     0123456
    Service Endpoint Enabled:     false
    ```
    {: screen}

1. Enable service endpoints by running the following command.

   ```bash
   ibmcloud account update --service-endpoint-enable true
   ```
   {: codeblock}

   It might take a few minutes for this change to take effect. After the command completes, you can run the `ibmcloud account show` command again to verify.

    If VRF isn't enabled for your account, running this command prompts you to create a case to enable it. Enter `y` to create the support case. After VRF is enabled in the account, run the command again to enable service endpoint connectivity in your account.

    ```bash
    Service Endpoint is not available in linked Softlayer Account 1008967.
    Enable VRF(Virtual Routing and Forwarding) first to proceed.
    Learn more about VRF here - https://cloud.ibm.com/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html.

    Do you want to open a ticket to enable it?[y/N]> y
    Ticket 70729615 was opened successfully. Follow the link https://control.softlayer.com/support/tickets/70729876 to check the details and track the status of the ticket. You will be required to login to view this ticket.
    Account ID:    1008967
    Ticket:        Private Network Question
    ```
    {: screen}


After service endpoints are enabled, you can create resources that connect over the {{site.data.keyword.cloud_notm}} private network. For a list of services that support service endpoints and more information, see [Enabling VRF and service endpoints](/docs/account?topic=account-vrf-service-endpoint).

## Using service endpoints
{: #use-service-endpoint}

After you enable the VRF and service endpoint account settings, you can create resources from the catalog that support service endpoints. The following table lists the services that support using service endpoints.

To find the endpoints for each service, refer to the Endpoint URLs section of the API documentation for the specific service.
{: tip}

| Service | Documentation |
|-------------------|-------------------------------|
| {{site.data.keyword.appconfig_short}} | [Regions and endpoints](/docs/app-configuration?topic=app-configuration-ac-regions-endpoints) |
| {{site.data.keyword.cloudcerts_short}} | [Regions and endpoints](/docs/secrets-manager?topic=secrets-manager-endpoints) |
| {{site.data.keyword.registryshort_notm}} | {{site.data.keyword.containershort}} clusters with [private service endpoints only](/docs/containers?topic=containers-plan_basics#workeruser-master) pull container images by using the [{{site.data.keyword.registryshort_notm}}](/docs/Registry?topic=Registry-registry_overview) service endpoint. |
| {{site.data.keyword.contdelivery_short}} | [Regions and endpoints](/docs/ContinuousDelivery?topic=ContinuousDelivery-regions#service-endpoints) |
| {{site.data.keyword.databases-for-elasticsearch}} | [{{site.data.keyword.databases-for-elasticsearch}} service endpoints integration](/docs/cloud-databases?topic=cloud-databases-service-endpoints&interface=ui) |
| {{site.data.keyword.databases-for-etcd}} | [{{site.data.keyword.databases-for-etcd}} service endpoints integration](/docs/databases-for-etcd?topic=databases-for-etcd-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [{{site.data.keyword.databases-for-mongodb}} service endpoints integration](/docs/databases-for-mongodb?topic=databases-for-mongodb-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [{{site.data.keyword.databases-for-postgresql}} service endpoints integration](/docs/databases-for-postgresql?topic=databases-for-postgresql-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [{{site.data.keyword.databases-for-redis}} service endpoints integration](/docs/databases-for-redis?topic=databases-for-redis-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [Connectivity options](/docs/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [Connecting to a private endpoint](/docs/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
| {{site.data.keyword.en_short}} | [Regions and endpoints](/docs/event-notifications?topic=event-notifications-en-regions-endpoints) |
|{{site.data.keyword.messagehub}} | [Restricting network access using the Enterprise plan](/docs/EventStreams?topic=EventStreams-restrict_access) |
| {{site.data.keyword.hscrypto}} | [{{site.data.keyword.hscrypto}} service endpoints integration](/docs/services/hs-crypto?hs-crypto-private-endpoints=hs-crypto-private-endpoints)|
| {{site.data.keyword.ihsdbaas_mongodb_full}} | [Securing your connection to {{site.data.keyword.ihsdbaas_mongodb_full}}](/docs/databases-for-mongodb?topic=databases-for-mongodb-service-endpoints&interface=ui) |
| {{site.data.keyword.ihsdbaas_postgresql_full}} | [Securing your connection to {{site.data.keyword.ihsdbaas_postgresql_full}}](/docs/databases-for-postgresql?topic=databases-for-postgresql-service-endpoints&interface=ui) |
| {{site.data.keyword.cloudant}}  |  [Available for all dedicated hardware plans deployed after 1 January 2019](/docs/Cloudant?topic=Cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.keymanagementserviceshort}} | [Connecting to {{site.data.keyword.keymanagementserviceshort}} on the {{site.data.keyword.cloud_notm}} private network](/docs/key-protect?topic=key-protect-private-endpoints) |
| KMIP for VMware on {{site.data.keyword.cloud_notm}} | [KMIP for VMware on {{site.data.keyword.cloud_notm}} documentation](/docs/vmwaresolutions?topic=vmwaresolutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [Public and private service endpoints for {{site.data.keyword.containershort_notm}}](/docs/containers?topic=containers-plan_basics#workeruser-master) |
| {{site.data.keyword.la_full}} | [{{site.data.keyword.la_full_notm}} service endpoints integration](/docs/log-analysis?topic=log-analysis-endpoints)|
| {{site.data.keyword.messages-for-rabbitmq}} | [{{site.data.keyword.messages-for-rabbitmq}} service endpoints integration](/docs/messages-for-rabbitmq?topic=messages-for-rabbitmq-vpes&interface=ui)|
| {{site.data.keyword.mon_full_notm}} | [{{site.data.keyword.mon_full_notm}} service endpoints integration](/docs/monitoring?topic=monitoring-endpoints#endpoints_ingestion)|
| {{site.data.keyword.cos_short}} | [{{site.data.keyword.cos_short}} endpoints and storage locations](/docs/cloud-object-storage?topic=cloud-object-storage-endpoints) |
| {{site.data.keyword.bpshort}} | [Using private endpoints](/docs/schematics?topic=schematics-private-endpoints) |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.wh-acd_short}} | [Public and private network endpoints](/docs/watson?topic=watson-public-private-endpoints) with {{site.data.keyword.wh-acd_short}} |
| {{site.data.keyword.conversationshort}} | [Securing your assistant](/docs/watson-assistant?topic=watson-assistant-admin-securing#security-private-endpoints) with {{site.data.keyword.conversationshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.discoveryshort}} | [Public and private network endpoints](/docs/watson?topic=watson-public-private-endpoints) with {{site.data.keyword.discoveryshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.knowledgestudioshort}} | [Public and private network endpoints](/docs/watson-knowledge-studio?topic=watson-public-private-endpoints) with {{site.data.keyword.knowledgestudioshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.languagetranslatorshort}} | [Public and private network endpoints](/docs/language-translator?topic=language-translator-public-private-endpoints) with {{site.data.keyword.languagetranslatorshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.pm_short}} | [Public and private network endpoints](https://dataplatform.cloud.ibm.com/docs/content/wsj/analyze-data/ml-service-endpoint.html?audience=wdp){: external} with {{site.data.keyword.pm_short}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.nlushort}} | [Public and private network endpoints](/docs/natural-language-understanding?topic=watson-public-private-endpoints#requirements-endpoints) with {{site.data.keyword.nlushort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.speechtotextshort}} | [Public and private network endpoints](/docs/speech-to-text?topic=speech-to-text-public-private-endpoints) with {{site.data.keyword.speechtotextshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.texttospeechshort}} | [Public and private network endpoints](/docs/text-to-speech?topic=text-to-speech-public-private-endpoints ) with {{site.data.keyword.texttospeechshort}} |
{: caption="Table 1. Services that support using service endpoints" caption-side="top"}
