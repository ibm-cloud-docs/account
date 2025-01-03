---

copyright:
  years: 2021, 2024

lastupdated: "2024-05-21"

keywords: cross-account restriction, cross-account resource, resource sharing across account, cross-account, cross account

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Managing external identity interactions
{: #cross-acct}

By default, users with an IAM access policy on resources in an account can access those resources from any account, not just the one that owns the resource. A user's API key can be used to generate a token and access resources that the user has access to outside of the account where the API key was created. User API keys contain the identity's permissions across all accounts that they are a member of. You can require users to access resources in your account only when authenticated in your account or accounts that you specify.
{: shortdesc}

You can monitor how limiting access to resources in your account affects users without enforcing it by using report-only mode. This way, you can identify gaps in your access policies and make sure that users have the access they need. For the best experience, turn on report-only mode for at least 30 days before you limit access to resources in your account.

If you want to know which identities in your account access a specific resource, see [Auditing access to resources](/docs/account?topic=account-access-report&interface=ui).

Anticipating the name and number of users who are impacted by limiting identity interactions can be difficult. To turn on report-only mode and observe the potential impact of limiting access to resources in your account, complete the following steps:

1. Create an instance of {{site.data.keyword.at_full_notm}} in the [catalog](/catalog/services/ibm-cloud-activity-tracker){: external}. For more information, see [Getting started with {{site.data.keyword.cloud_notm}} Activity Tracker](/docs/activity-tracker?topic=activity-tracker-getting-started).

   You must create an instance of the Activity Tracker service in the `eu-de` region to start tracking events.
   {: important}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)** > **Settings** > **Resources**.
1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
1. Select **Report-only**.
1. Add accounts to the allowlist (Optional).
    1. Enter the account IDs for the accounts that you want to allow.
    1. Click **Add**.

    If you want users to generate API keys in only your account, don't add any accounts to the allowlist. An empty allowlist restricts all users from accessing resources in your account if they are using API keys that are created in other accounts.
    {: tip}

1. Click **Save**.
1. Next, view your [{{site.data.keyword.at_full_notm}} reports](/docs/account?topic=account-cross-acct#view-cross-acct-report).

After you monitor the results from report-only mode for at least 30 days, update the setting to **Limited**.

## Viewing your reports
{: #view-cross-acct-report}

Only denied or potentially denied access attempts are reported in {{site.data.keyword.at_full_notm}}.

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)** > **Settings** > **Resources**.
1. Click **Edit > View Activity Tracker**.
1. Review the report.
    1. If the state of the restriction is **Report-only**, the query shows only potentially denied access attempts.
    1. If the state of the restriction is **Limited**, the query shows only denied access attempts.

You can add or remove accounts from the allowlist at any time to meet your security requirements. For a list of the actions that generate an event, see [Auditing events for IAM](/docs/activity-tracker?topic=activity-tracker-at_events_iam).
