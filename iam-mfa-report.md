---

copyright:
  years: 2023
lastupdated: "2023-03-22"

keywords: MFA, MFA status, fulfill MFA, multifactor authentication, MFA requirement, MFA report

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Identifying a user's MFA status
{: #id-user-mfa}

The first time that a user logs in to your account after you [enable multifactor authentication (MFA)](/docs/account?topic=account-enablemfa), they need to set up their authentication factors. Users that don't log in and follow this process leave your account vulnerable to attacks. Identify the users in your account that don't satisfy your MFA requirements by generating an MFA status report.
{: shortdesc}

You must have the Administrator role on the IAM Identity Service to view and update the report. The following actions are included in this role.
- The action `iam-identity.mfa-status.get` is required to view the report.
- The action `iam-identity.report.create` is required to generate a new report.

## Viewing the MFA status of users in the console
{: #view-user-mfa-status}

To view the MFA status of users in the console, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **MFA status**.
2. Click **Update report** to view the most recent report in your account.

   Only the most recent report is available. Reports older than a day are deleted when you generate a new report.
   {: note}

3. Contact the users in your account that don't satisfy their MFA requirement. Ask them to comply by logging in and setting up factors. For more information, see [Managing your authentication factors](/docs/account?topic=account-verification-authentication#auth-factors).
