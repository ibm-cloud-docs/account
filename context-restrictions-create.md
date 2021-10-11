---

copyright:

  years: 2021

lastupdated: "2021-10-10"

keywords: create network access, network access rule, network zone

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:pre: .pre}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}


# Creating context-based restrictions
{: #context-restrictions-create}

Context-based restrictions allow you to manage user and service access to specific cloud resources. You can define restrictions to the resources based on contexts, such as network zones and endpoint types. For more information, see [What are context-based restrictions](/docs/account?topic=account-context-restrictions-whatis&interface=ui).
{: shortdesc}

User and account level IP address restrictions can also affect users' ability to access resources. To view account level IP address restrictions, go to [Settings](/iam/settings). To view individual user settings, go to [Users](/iam/users) and view each user's IP address restrictions in the details tab. 
{: note}

## Before you begin
{: #context-prereq}

To set up context-based restrictions, you must be the account owner or have an access policy with the administrator role on all account management services. For more information, see [Assigning access to account management services](/docs/account?topic=account-account-services).

## Creating network zones
{: #network-zones-create}

By creating network zones, you can create a list of allowed locations where an access request originates. A set of one or more network locations can be specified by IP addresses such as individual addresses, ranges or subnets, and VPC IDs. After you create a network zone, you can add it to a rule. 

To create a network zone, complete the following steps. 
1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Context-based restrictions**, and select **Network zones**.
1. Click **Create**. 

    Instead of creating a zone by using UI inputs, you can use the JSON code form to directly enter JSON to create a zone by clicking **Enter as JSON code**.
    {: note}

1. Enter a unique name and a description.
1. Enter the allowed IP addresses where an access request can originate. Include IP address exceptions in the deny list, if necessary.
1. Enter the allowed VPCs. 
1. Reference a service. Select a service and click **Add** to associate its IP addresses with your network zone.
1. Click **Next** to review your network zone.
1. Click **Create**.

You can continue by creating more network zones, or by creating rules.
{: tip}

## Creating rules
{: #context-restrictions-create-rules}

Define restrictions to your cloud resources by creating rules.

To create a rule, complete the following steps. 
1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Context-based restrictions**, and select **Rules**.
2. Click **Create**.  
3. Provide a unique description, then click **Continue**. 
4. Select the resources that you want to target in your rule. Select all resources or select resources based on attributes such as location or resource groups, then click **Continue**.
    1. Select **Account management** to restrict access to services like user management and policy management. 

    When you create context-based restriction for the IAM Access Groups service, users who don't satisfy the rule will not be able to view any groups in the account, including the public access group. 
    {: note}

5. Next, add one or more contexts. Select endpoint types and network zones, and click **Add**. 
    * You can allow access from all service supported or specific service endpoint types. If the toggle is set to Yes, all service supported endpoint types are added to the rule. 
    * You can add existing network zones to your rule or create new zones to add to your rule. For more information, [Creating network zones](/docs/account?topic=network-zones-create).
6. Click **Create**.

If you create a context-based restriction for the **IAM Access Groups** or **IAM Users** services, the rule must allow the two services to still communicate. To do this, create a network zone with a service reference to the other service. For example, if you create a context-based restriction around the IAM Access Groups service, create a network zone with a service reference to the IAM Users service. Then, add this network zone to the rule you create around the IAM Access Groups service. This way, the IP addresses associated with the IAM Users service is included in the rule’s allowed context. If you don't do this, the services might produce unexpected behavior.
{: tip}
