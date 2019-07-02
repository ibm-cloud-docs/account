---

copyright:
  years: 2019
lastupdated: "2019-07-01"

keywords: VRF, virtual routing and forwarding, service endpoint, private network

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Enabling VRF and service endpoints
{: #vrf-service-endpoint}

By default, you connect to resources in your account over the {{site.data.keyword.Bluemix}} public network. You can enable virtual routing and forwarding (VRF) to move IP routing for your account and all of its resources into a separate routing table. If VRF is enabled, you can then enable {{site.data.keyword.Bluemix_notm}} service endpoints to connect directly to resources without using the public network.
{:shortdesc}

To enable virtual routing and forwarding and {{site.data.keyword.Bluemix_notm}} service endpoint, you need a billable account.

## Enabling VRF
{: #vrf}

VRF allows multiple instances of a routing table to exist in a router and to work simultaneously. When you enable VRF, a separate routing table is created for your account, and connections to and from your account's resources are routed separately on the {{site.data.keyword.Bluemix_notm}} network. VRF is enabled at the account level, so all resources are affected by this networking change. For more information about VRF technology and how it affects your account's network routing, see [Virtual routing and forwarding on {{site.data.keyword.Bluemix_notm}}](/docs/resources?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud).

Enabling VRF permanently alters networking for your account. Be sure that you understand the impact to your account and resources. After you enable VRF, it cannot be disabled.
{: important}

To enable VRF, create a support case with your request.

1. In the console, go to **Support** and click **Create a case**.
1. Select **Account and access** as the support type.
1. In the **Subject** field, enter `Private networking question`.
1. In the **Description** field, enter the following message, replacing _enter your account number_ with your {{site.data.keyword.Bluemix_notm}} account number.

   `We are requesting that account *enter your account number* is moved to its own VRF. We understand the risks and approve the change. Please reply back with the scheduled window(s) of time where this change will be made so we can prepare for the migration.`

The {{site.data.keyword.Bluemix_notm}} network engineering team will reach out to the case owner to schedule a time for your account's networking to be converted to VRF. During the conversion process, connections to resources in your account might be unstable due to packet loss. The conversion takes roughly 15-30 minutes, depending on the complexity of your account. If your account has legacy {{site.data.keyword.BluDirectLink}} connections, it might take more time.


## Enabling service endpoints
{: #service-endpoint}

When {{site.data.keyword.Bluemix_notm}} service endpoints are enabled in your account, you can choose to expose a private network endpoint when you create a resource. You can then connect directly to this endpoint over the {{site.data.keyword.Bluemix_notm}} private network rather than the public network. Because resources that use private network endpoints don't have an internet-routable IP address, connections to these resources are more secure. For more information, see [Service endpoints for private network connections](/docs/resources?topic=resources-service-endpoints).

Before you can enable service endpoints, VRF must be enabled for your account.
{: note}

To enable service endpoints from the CLI, you need version 0.13 or later of the [{{site.data.keyword.Bluemix_notm}} CLI](/docs/cli?topic=cloud-cli-getting-started).

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


After service endpoints are enabled, you can create resources that connect over the {{site.data.keyword.Bluemix_notm}} private network. For a list of services that support service endpoints and more information, see [Setting up private network endpoints](/docs/resources?topic=resources-private-network-endpoints).
