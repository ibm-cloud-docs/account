---

copyright:

  years: 2021, 2022

lastupdated: "2022-08-05"

keywords: remove restrictions, delete restrictions, delete network access, delete context based restrictions, remove network access, rule, context, network access rule, network zone

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Removing context-based restrictions
{: #context-restrictions-remove}

By removing context-based restrictions, you delete restrictions that are defined by the contexts in a rule. Deleting rules removes context-based restrictions from the given resource, and requests from any context are allowed if the user has the correct permissions.
{: shortdesc}

## Removing a rule
{: #context-restrictions-remove-rules}

You can remove a rule on your cloud resources by completing the following steps: 
1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Context-based restrictions**, and select **Rules**.
2. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") in the row that contains the rule, and click **Remove**.

## Removing a network zone
{: #network-zones-remove}

Removing a network zone removes the set of allowed network locations from which an access request is created. If a network zone is added to a rule, you first have to remove the zone from the rule. See [Updating context-based restrictions](/docs/account?topic=account-context-restrictions-update) for more information about removing a zone from a rule. Then, complete the following steps: 

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Context-based restrictions**, and select **Network zones**.
2. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") in the row that contains the network zone, and click **Remove**.
