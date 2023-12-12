---

copyright:
  years: 2023
lastupdated: "2023-12-08"

keywords: MFA, MFA status, fulfill MFA, multifactor authentication, MFA requirement, MFA report

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Identifying a user's MFA status
{: #id-user-mfa}

The first time that users log in to your account after you [enable multifactor authentication (MFA)](/docs/account?topic=account-enablemfa), they must set up their authentication factors. Otherwise, your account is subject to security vulnerabilities and attacks. You can identify the users in your account who don't meet your MFA requirements by generating an MFA status report.
{: shortdesc}

You must have the Administrator role on the IAM Identity Service to view and update the report. The following actions are included in this role.
- The action `iam-identity.mfa-status.get` is required to view the report.
- The action `iam-identity.report.create` is required to generate a new report.

## Viewing the MFA status of users in the console
{: #view-user-mfa-status}

To view the MFA status of users in the console, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **MFA status**.
1. Click **Update report** to view the most recent report in your account.

   Only the most recent report is available. When you generate a new report, any reports older than a day are deleted.
   {: note}

1. View the Satisfies MFA column to determine if the user is enrolled for the required MFA method. The following values are possible:
   - Yes: The user either does not need to provide any additional authentication factor, or they are already enrolled for the required authentication factor. Any time this user tries to log in to IBM Cloud, they are prompted to complete the required MFA method.
   - No: The user has not yet enrolled for the required authentication factor. The next time the user logs in to IBM Cloud, they are prompted to enroll.
   - Not all accounts: The user belongs to at least one other IBM Cloud account that requires a stronger MFA method, but the user is not enrolled yet for that method.

   ID-based MFA is the current and most secure type of MFA. Account-based MFA is deprecated. Factors vary between both types of MFA. For more information, see the current [MFA options](/docs/account?topic=account-types#mfa-options) and [Deprecated legacy account-based MFA](/docs/account?topic=account-legacy-mfa).
   {: tip}

1. Contact the users in your account who don't satisfy the MFA requirements. Ask them to comply by logging in and setting up the required factors. For more information, see [Managing your authentication factors](/docs/account?topic=account-verification-authentication#auth-factors).
