---

copyright:

  years: 2021, 2022

lastupdated: "2022-06-24"

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
2. Select the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") on the rule you want to update, and select **Edit**.
3. Provide a new description for your rule. Click **Apply** to update the description, or click **Continue**.
5. To update the scope of resources for the restriction, you can select **All resources** or **Specific resources** based on the available attributes, such as resource group or location. Then, click **Apply** or **Continue**.
6. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") in the the summary panel to update an existing context.
7. Click the **Remove** icon ![Remove icon](../icons/delete.svg "Remove") in the summary panel to remove network zones.
8. Configure a new context by selecting all endpoints or a specific endpoint, and by selecting your network zones. Then, click **Add**. 
9. Click **Apply** to finish.

## Updating network zones
{: #network-zones-update}

You can modify the list of allowed locations where an access request can originate. A set of one or more network locations can be specified by IP addresses (individual addresses, ranges, or subnets), VPCs, or service references. You can update a network zone that is used in a rule, or integrate the new updated network zones into your rules later.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Context-based restrictions**, and select **Network zones**.
1. Select the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") on the network zone you want to update, and select **Edit**.
1. You can update your zone name and description.
1. You can edit the list of allowed IP addresses where an access request can originate. Include exceptions in the deny list, if necessary.
1. You can add or remove allowed VPCs. 
1. You can add or remove service references. Select a service to associate its IP addresses with your network zone.
1. Click **Next** to review your new configuration.
1. To apply changes, click **Update**.
