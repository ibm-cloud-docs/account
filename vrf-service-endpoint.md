---

copyright:
  years: 2019, 2020
lastupdated: "2020-08-12"

keywords: VRF, virtual routing and forwarding, service endpoint, private network, account networking, direct network, services that support service endpoints, service endpoint support, using service endpoints

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Enabling VRF and service endpoints
{: #vrf-service-endpoint}

When using the classic infrastructure, you connect to resources in your account over the {{site.data.keyword.Bluemix}} public network by default. You can enable virtual routing and forwarding (VRF) to move IP routing for your account and all of its resources into a separate routing table. If VRF is enabled, you can then enable {{site.data.keyword.Bluemix_notm}} service endpoints to connect directly to resources without using the public network.
{:shortdesc}

Virtual Private Clouds (VPCs) are automatically enabled for virtual routing and forwarding (VRF). To enable service endpoints for your VPC, continue to [Enabling service endpoints](#service-endpoint).
{: note}

## Before you begin
{: #before-service-endpoint-enablement}

Before you begin, ensure that you meet the following criteria:

* You need a billable account to enable virtual routing and forwarding and {{site.data.keyword.Bluemix_notm}} service endpoints.
* You must have access to {{site.data.keyword.cloud_notm}} infrastructure in your account. Go to the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) > **Classic Infrastructure** to verify that you have access.

## Enabling VRF
{: #vrf}

VRF allows multiple instances of a routing table to exist in a router and to work simultaneously. When you enable VRF, a separate routing table is created for your account, and connections to and from your account's resources are routed separately on the {{site.data.keyword.Bluemix_notm}} network. VRF is enabled at the account level, so all resources are affected by this networking change. For more information about VRF technology and how it affects your account's network routing, see [Virtual routing and forwarding on {{site.data.keyword.Bluemix_notm}}](/docs/dl?topic=dl-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud).

Enabling VRF permanently alters networking for your account. Be sure that you understand the impact to your account and resources. After you enable VRF, it cannot be disabled.
{: important}

To enable VRF, create a support case with your request.

1. In the console, go to **Manage > Account**, then click **Account settings**.
1. In the Virtual routing and forwarding section, click **Create case**.
1. In the case description, enter your classic infrastructure account number, and click **Submit**.

   Don't change the rest of the prefilled support case information. The information is tailored to make sure that your request is handled as quickly as possible.
   {: tip}

The {{site.data.keyword.Bluemix_notm}} network engineering team will reach out to the case owner to schedule a time for your account's networking to be converted to VRF. During the conversion process, connections to resources in your account might be unstable due to packet loss. The conversion takes roughly 15 - 30 minutes, depending on the complexity of your account. If your account has legacy {{site.data.keyword.BluDirectLink}} connections, it might take more time.


## Enabling service endpoints
{: #service-endpoint}

When {{site.data.keyword.Bluemix_notm}} service endpoints are enabled in your account, you can choose to expose a private network endpoint when you create a resource. You can then connect directly to this endpoint over the {{site.data.keyword.Bluemix_notm}} private network rather than the public network. Because resources that use private network endpoints don't have an internet-routable IP address, connections to these resources are more secure. For more information, see [Service endpoints for private network connections](/docs/account?topic=account-service-endpoints-overview).

Before you can enable service endpoints, VRF must be enabled for your account. Virtual Private Clouds (VPCs) are automatically enabled for VRF.
{: note}

### From the console
{: #service-endpoint-console}

1. In the console, go to **Manage > Account**, then click **Account settings**.
1. In the Service endpoints section, click **On**.

   If you can't click the button, VRF might not be enabled for your account. Verify that it's enabled by checking the virtual routing and forwarding section, which is the preceding section in your account settings.
1. Review the impacts to your account, and click **On**.

It might take a few minutes for this change to take effect.

### From the CLI
{: #service-endpoint-cli}

To enable service endpoints from the [{{site.data.keyword.Bluemix_notm}} CLI](/docs/cli?topic=cli-getting-started), you need version 0.13 or later.

1.  Check whether service endpoints are already enabled in your account.

    ```
    ibmcloud account show
    ```
    {: codeblock}

    If `Service Endpoint Enabled` is `false` as shown in the following example, service endpoints are not enabled.

    ```
    Retrieving account Mia Example's Account of m.example@example.com...
    OK

    Account ID:                   abc123d0bc2edefthyufffc9b5ca318   
    Currently Targeted Account:   true   
    Linked Softlayer Account:     0123456   
    Service Endpoint Enabled:     false  
    ```
    {: screen}
1. Enable service endpoints by running the following command.

   ```
   ibmcloud account update --service-endpoint-enable true
   ```
   {: codeblock}

   It might take a few minutes for this change to take affect. After the command completes, you can run the `ibmcloud account show` command again to verify.
   
    If VRF isn't enabled for your account, running this command prompts you to create a case to enable it. Enter `y` to create the support case. After VRF is enabled in the account, run the command again to enable service endpoint connectivity in your account. 
    
    ```
    Service Endpoint is not available in linked Softlayer Account 1008967.
    Enable VRF(Virtual Routing and Forwarding) first to proceed.
    Learn more about VRF here - https://cloud.ibm.com/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html.

    Do you want to open a ticket to enable it?[y/N]> y
    Ticket 70729615 was opened successfully. Follow the link https://control.softlayer.com/support/tickets/70729876 to check the details and track the status of the ticket. You will be required to login to view this ticket.
    Account ID:    1008967
    Ticket:        Private Network Question
    ```
    {: screen}
  

After service endpoints are enabled, you can create resources that connect over the {{site.data.keyword.Bluemix_notm}} private network. For a list of services that support service endpoints and more information, see [Setting up private network endpoints](/docs/account?topic=account-vrf-service-endpoint).

## Using service endpoints
{: #use-service-endpoint}

After you enable the VRF and service endpoint account settings, you can create resources from the catalog that support service endpoints. The following table lists the services that support using service endpoints.

Refer to the documentation for the specific service for more information about using service endpoints.
{: tip}

| Service | Documentation |
|-------------------|-------------------------------|
| {{site.data.keyword.iae_short}} | [{{site.data.keyword.iae_short}} cloud service endpoints integration](/docs/services/AnalyticsEngine?topic=AnalyticsEngine-service-endpoint-integration) |
| {{site.data.keyword.databases-for-elasticsearch}} | [{{site.data.keyword.databases-for-elasticsearch}} service endpoints integration](/docs/services/databases-for-elasticsearch?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-etcd}} | [{{site.data.keyword.databases-for-etcd}} service endpoints integration](/docs/services/databases-for-etcd?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-mongodb}} | [{{site.data.keyword.databases-for-mongodb}} service endpoints integration](/docs/services/databases-for-mongodb?topic=cloud-databases-service-endpoints) |
| {{site.data.keyword.databases-for-postgresql}} | [{{site.data.keyword.databases-for-postgresql}} service endpoints integration](/docs/services/databases-for-postgresql?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.databases-for-redis}} | [{{site.data.keyword.databases-for-redis}} service endpoints integration](/docs/services/databases-for-redis?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.Db2_on_Cloud_short}} | [Connectivity options](/docs/services/Db2onCloud?topic=Db2onCloud-connect_options) |
| {{site.data.keyword.dashdbshort}} | [Connecting to a private endpoint](/docs/services/Db2whc?topic=Db2whc-connect_options#priv_endpt) |
|{{site.data.keyword.messagehub}} | [Restricting network access using the Enterprise plan](/docs/EventStreams?topic=EventStreams-restrict_access) |
| {{site.data.keyword.hscrypto}} | [{{site.data.keyword.hscrypto}} service endpoints integration](/docs/services/hs-crypto?topic=hs-crypto-private-endpoints)|
| {{site.data.keyword.ihsdbaas_mongodb_full}} | [Securing your connection to {{site.data.keyword.ihsdbaas_mongodb_full}}](/docs/hyper-protect-dbaas-for-mongodb?topic=hyper-protect-dbaas-for-mongodb-service-connection) |
| {{site.data.keyword.ihsdbaas_postgresql_full}} | [Securing your connection to {{site.data.keyword.ihsdbaas_postgresql_full}}](/docs/hyper-protect-dbaas-for-postgresql?topic=hyper-protect-dbaas-for-postgresql-service-connection) |
| {{site.data.keyword.cloudant}}  |  [Available for all dedicated hardware plans deployed after 1 January 2019](//docs/Cloudant?topic=Cloudant-ibm-cloud-public#dedicated-hardware-plan) |
| {{site.data.keyword.registryshort_notm}} | {{site.data.keyword.containershort}} clusters with [private service endpoints only](/docs/containers?topic=containers-plan_clusters#workeruser-master) pull container images by using the [{{site.data.keyword.registryshort_notm}}](/docs/Registry?topic=Registry-registry_overview) service endpoint. |
| {{site.data.keyword.cfee_full}} | [{{site.data.keyword.cfee_full_notm}} service endpoints integration](/docs/cloud-foundry?topic=cloud-foundry-isolated-network#private-access)|
| {{site.data.keyword.streaminganalyticsfull}} |  [Managing service endpoints for {{site.data.keyword.streaminganalyticsshort}}](/docs/services/StreamingAnalytics?topic=StreamingAnalytics-manage_endpoints#manage_endpoints) |
| {{site.data.keyword.keymanagementserviceshort}} | [Connecting to {{site.data.keyword.keymanagementserviceshort}} on the {{site.data.keyword.cloud_notm}} private network](/docs/services/key-protect?topic=key-protect-private-endpoints) |
| KMIP for VMware on {{site.data.keyword.cloud_notm}} | [KMIP for VMware on {{site.data.keyword.cloud_notm}} documentation](/docs/vmwaresolutions?topic=vmwaresolutions-kmip_standalone_considerations#kmip_standalone_considerations-install)|
| {{site.data.keyword.containershort}} | [Public and private service endpoints for {{site.data.keyword.containershort_notm}}](/docs/containers?topic=containers-plan_clusters#workeruser-master) |
| {{site.data.keyword.messages-for-rabbitmq}} | [{{site.data.keyword.messages-for-rabbitmq}} service endpoints integration](/docs/services/messages-for-rabbitmq?topic=cloud-databases-service-endpoints)|
| {{site.data.keyword.cos_short}} | [{{site.data.keyword.cos_short}} endpoints and storage locations](/docs/cloud-object-storage-infrastructure?topic=cloud-object-storage-infrastructure-endpoints-iaas) |
| {{site.data.keyword.la_full}} | [{{site.data.keyword.la_full_notm}} service endpoints integration](/docs/Log-Analysis-with-LogDNA?topic=Log-Analysis-with-LogDNA-endpoints)|
| {{site.data.keyword.mon_full_notm}} | [{{site.data.keyword.mon_full_notm}} service endpoints integration](/docs/Monitoring-with-Sysdig?topic=Monitoring-with-Sysdig-endpoints#endpoints_ingestion)|
| {{site.data.keyword.bpshort}} | [Using private endpoints](/docs/schematics?topic=schematics-private-endpoints) |
| {{site.data.keyword.conversationshort}} | [Protecting sensitive information](/docs/assistant?topic=assistant-security) with {{site.data.keyword.conversationshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.cncshort}} | [Public and private network endpoints](/docs/compare-comply?topic=watson-public-private-endpoints) with {{site.data.keyword.cncshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.discoveryshort}} | [Public and private network endpoints](/docs/discovery?topic=watson-public-private-endpoints) with {{site.data.keyword.discoveryshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.wh-iml_short}} | [Public and private network endpoints](/docs/wh-iml?topic=watson-public-private-endpoints) with {{site.data.keyword.wh-iml_short}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.knowledgestudioshort}} | [Public and private network endpoints](/docs/services/watson-knowledge-studio?topic=watson-public-private-endpoints) with {{site.data.keyword.knowledgestudioshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.languagetranslatorshort}} | [Public and private network endpoints](/docs/services/language-translator?topic=watson-public-private-endpoints) with {{site.data.keyword.languagetranslatorshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.nlushort}} | [Public and private network endpoints](/docs/services/natural-language-understanding?topic=watson-public-private-endpoints) with {{site.data.keyword.nlushort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.personalityinsightsshort}} | [Public and private network endpoints](/docs/services/personality-insights?topic=watson-public-private-endpoints) with {{site.data.keyword.personalityinsightsshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.speechtotextshort}} | [Public and private network endpoints](/docs/services/speech-to-text?topic=watson-public-private-endpoints) with {{site.data.keyword.speechtotextshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.texttospeechshort}} | [Public and private network endpoints](/docs/services/text-to-speech?topic=watson-public-private-endpoints) with {{site.data.keyword.texttospeechshort}} |
| {{site.data.keyword.ibmwatson_notm}} {{site.data.keyword.toneanalyzershort}} | [Public and private network endpoints](/docs/services/tone-analyzer?topic=watson-public-private-endpoints) with {{site.data.keyword.toneanalyzershort}} |
{: caption="Table 1. Services that support using service endpoints" caption-side="top"}


