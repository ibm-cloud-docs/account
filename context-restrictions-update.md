---

copyright:

  years: 2021, 2022

lastupdated: "2022-04-01"

keywords: update network access, network access rule, network zone

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Updating context-based restrictions
{: #context-restrictions-update}

You can update context rules at any time by providing a new description, which helps identifying the purpose of the rule, or selecting a new list of resources and network environments.
{: shortdesc}

To update a context-based restrictions rule, you must be assigned the administrator role on the account management service.

## Updating rules
{: #context-restrictions-update-rules}

To edit the context-based restrictions on your cloud resources, complete the following steps.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Context-based restrictions**, and select **Rules**.
2. Select the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") next to the rule you want to update, and select **Edit**.
3. Provide a new description for your rule. Click **Apply** to simply update the description, or click **Continue**.
4. To update the scope of the service you want to restrict, you can select all resources or specific resources based on the available attributes, such as resource groups or location. Then, click **Apply** or **Continue**.
5. You can edit or remove network zones by using the summary panel.
    * Allow access from all or specific service endpoint types, which can be the combination of public, private, and direct endpoints.
    * Select, remove, or create network zones for your access rule.
    * By clicking **Add**, you can define multiple contexts.
6. Click **Apply** to finish.

## Updating network zones
{: #network-zones-update}

You can modify the list of allowed locations where an access request can originate. A set of one or more network locations can be specified by IP addresses (individual addresses, ranges, or subnets), VPCs, or service references. You can update a network zone that is used in a rule, or integrate the new updated network zones into your rules later.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Context-based restrictions**, and select **Network zones**.
1. Select the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") next to the network zone you want to update, and select **Edit**.
1. You can update your zone with a better name and a description.
1. You can edit the list of allowed IP addresses where an access request can originate. Include exceptions in the deny list, if necessary.
1. You can add or remove allowed VPCs. 
1. You can add or remove service references. Select a service to associate its IP addresses with your network zone.
1. Click **Next** to review your new configuration.
1. To apply changes, click **Update**.
