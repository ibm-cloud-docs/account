---

copyright:

  years: 2020, 2026
lastupdated: "2026-04-17"

keywords: troubleshoot account, dashboard role, permission, view dashboard, dashboard

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I view all the resources on the dashboard that are shared?
{: #ts_dash-access}
{: troubleshoot}

You're unable to view all resources on the shared dashboard because you lack the required IAM access or are blocked by context-based restrictions.
{: shortdesc}

The view of the scoped dashboard that was shared with you is different than the view for other users in the account.
{: tsSymptoms}

You don't have the required IAM access on the individual resource, or a context-based restriction is blocking your access to the resource.
{: tsCauses}

The account owner can update your access to any resource in the account, or you can contact any user who is assigned to the administrator role on the service or service instance. For more information, see [IAM access](/docs/iam?topic=iam-userroles).
{: tsResolve}

The account owner or any user assigned the administrator role on all account management services can check the context-based restrictions on a resource.

To check the context-based restrictions on a resource, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Context-based restrictions**, and select **Rules**.
1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") on the rule for your service.
1. Click **Details**.
1. Take note of the contexts for the rule. Access is granted by a rule only when at least one of the rule's contexts are satisfied by the user.

For more information, see [Layered security with context-based restrictions](/docs/iam?topic=iam-context-restrictions-whatis).
