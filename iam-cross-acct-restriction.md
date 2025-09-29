---

copyright:

   years: 2021, 2025
lastupdated: "2025-05-12"

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

1. Set up {{site.data.keyword.atracker_full_notm}} to view IAM audit events. For more information, see [Viewing activity tracking events for IAM](/docs/account?topic=account-at_events_iam#at-viewing-iam)
1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)** > **Settings** > **Resources**.
1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
1. Select **Report-only**.
1. Add accounts to the allowlist (Optional).
    1. Enter the account IDs for the accounts that you want to allow.
    1. Click **Add**.

    If you want users to generate API keys in only your account, don't add any accounts to the allowlist. An empty allowlist restricts all users from accessing resources in your account if they are using API keys that are created in other accounts.
    {: tip}

1. Click **Save**.
1. Next, view your [{{site.data.keyword.atracker_full_notm}} reports](/docs/account?topic=account-cross-acct#view-cross-acct-report).

After you monitor the results from report-only mode for at least 30 days, update the setting to **Limited**.

## Viewing your reports
{: #view-cross-acct-report}

{{site.data.keyword.atracker_full_notm}} events are generated when the restriction is set to  **Report-only** or **Limited**. In **Report-only** mode, both permitted and requests that would be denied are reported. In **Limited** mode, only denied requests are reported.

To view {{site.data.keyword.atracker_full_notm}} events, you must configure an {{site.data.keyword.logs_full_notm}} instance as the target. For more information, see [Configuring an {{site.data.keyword.logs_full_notm}} instance as a target](/docs/atracker?topic=atracker-getting-started-target-cloud-logs).
{: tip}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)** > **Settings** > **Resources**.
1. Click **Edit > Open {{site.data.keyword.atracker_full_notm}}**.
1. Click **Explore Logs**  to compose a query.
1. Search the logs for the event action: `iam-access-management.account-settings.eval`

### Identifying potential access disruptions
{: #identify-disruptions}

When using **Report-only** mode, your primary focus should be on identifying cross-account access that would be blocked when switching to **Limited** mode:

1. Filter for `responseData.isEnforced:"false" AND responseData.decision:"Deny"`
   
   **This is the most critical analysis** you should perform. This query reveals all cross-account access attempts that would be blocked when enforcement is enabled. These results show which identities are currently accessing resources across account boundaries that would be denied access when you switch to **Limited** mode.

2. For each "deny" result, you must determine if this cross-account flow needs to be preserved or if it should be blocked:
   - If the flow should be preserved: Preferably, contact the user and adjust the work flow to ensure the token used is scoped to the correct account, or if that isn't possible, add the external account to your allowlist. To validate, please see   [ validating allowlist changes section](/docs/account?topic=account-cross-acct#validate-allowlist). 
   - If the flow should be blocked: No action needed, as it will be automatically blocked when the switch is made to **Limited** mode

### Validating allowlist changes
{: #validate-allowlist}

After deciding to preserve specific external identity interaction flows by adding accounts to your allowlist, you can verify these changes are working as expected:

1. Filter for `responseData.isEnforced:"false" AND responseData.decision:"Permit"`
   
   This query shows requests that passed the restriction, including those that were previously denied but are now permitted due to your allowlist changes.

2. Look specifically for permits from accounts you recently added to your allowlist to confirm your changes are working correctly. This validation step is valuable when you've made allowlist changes and want to ensure that the previously blocked cross-account access is now permitted.

### Monitoring Limited mode
{: #monitor-limited}

When the restriction is set to **Limited**, you can monitor blocked requests:

- Filter for `responseData.isEnforced:"true" AND responseData.decision:"Deny"`
  
  This shows all requests that were blocked because they came from accounts not on your allowlist.

You can add or remove accounts from the allowlist at any time to meet your security requirements. For a list of the actions that generate an event, see [Activity tracking events for IAM](/docs/account?topic=account-at_events_iam).
