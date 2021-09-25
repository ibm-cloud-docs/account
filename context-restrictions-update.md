---

copyright:

  years: 2021

lastupdated: "2021-09-23"

keywords: update network access, network access rule, network zone

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:pre: .pre}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Updating context-based restrictions
{: #context-restrictions-update}

You can update context rules at any time by providing a new description, which helps identifying the purpose of the rule, or selecting a new list of resources and network environments.
{: shortdesc}

To update a context rule, you must be assigned the appropriate access.

## Updating context-based restrictions
{: #context-restrictions-update-rules}

You can edit the network-level access to your cloud resources by the following steps.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Context-based restrictions**, and select **Rules**.
2. Select the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") next to the access rule you want to update, and select **Edit**.
3. You can provide a new description for your rule, then click **Continue**.
4. To define new access, select all resources or specific resources of the selected service based on attributes such as resource groups or location, then click **Continue**.
5. You can edit or remove network environments by using the summary panel.
    * Allow access from all or specific service endpoint types, which can be the combination of public, private, and direct endpoints.
    * Select, remove, or create network zones for your access rule.
    * By clicking **Add**, you can define multiple contexts.
6. Click **Apply** to finish.

## Updating network zones
{: #network-zones-update}

You can modify the list of allowed locations where an access request can originate. A set of one or more network locations can be specified by IP addresses (individual addresses, ranges, or subnets), VPC, or service reference. You can update a network zone that is used in a rule, or integrate the new predefined network zones into your rules later.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Context-based restrictions**, and select **Network zones**.
1. Select the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") next to the network zone you want to update, and select **Edit**.
1. You can reconfigure your zone by providing a better name and a description.
1. Edit allowed client IP addresses from which an access request can originate. Include exceptions in the deny list, if necessary.
1. Edit allowed VPCs. 
1. Reference a service. Select a service to associate its IP addresses with your network zone.
1. Click **Next step** to review your new configuration.
1. To apply changes, click **Update zone**.
