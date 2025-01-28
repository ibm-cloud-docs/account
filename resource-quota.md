---

copyright:

  years: 2024, 2025
lastupdated: "2025-01-28"

keywords: resources, resource quota, quota, service limit

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Viewing resource quotas and service limits
{: #view-resource-quota}

The centralized {{site.data.keyword.cloud}} [Resource quotas and service limits](/account/resource-quotas){: external} page provides a way for you to view and manage quotas and limits for infrastructure services, account management, and {{site.data.keyword.IBM_notm}} {{site.data.keyword.iamshort}} (IAM). Quotas are the maximum limit for resources in your account. If the default limit of resources is not suitable for your business needs, you can request the increase of your resource quota values. By viewing and managing resource quotas and limits, you can help ensure efficient resource optimization and prevent overconsumption.
{: shortdesc}

## Viewing your resource quotas
{: #view-quota-resource}

Check the resource quotas in your account to make sure that you optimize your resource usage and maintain resource performance. To view your resource quotas, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage > Account > Account resources > Resource quotas**.
1. In the **Resource quotas and service limits** page, select the category that your resource is associated with. You can filter the resources by regions, and by whether the resource quotas are adjustable.
1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") of a specific resource and select **View quota details**. You can find more details on the **Resource quota details** side panel, including the default quota metric, quota type, default quota limit, current quota limit, current utilization, and whether the resource quota is adjustable.

If your resource associated with the infrastructure service is at capacity and you reached the default quota limit, you can create a support case in the [Support Center](/unifiedsupport/cases/add){: external} to adjust the quota limit. For more information, see [Increasing account limits](/docs/account?topic=account-account-limits).

You can't adjust the quota limit for resources that are associated with IAM. For more information on the maximum limits for IAM resources, see [{{site.data.keyword.cloud_notm}} IAM limits](/docs/account?topic=account-known-issues#access-tag-limits).
{: note}
