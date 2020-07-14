---

copyright:

  years: 2018, 2020
lastupdated: "2020-06-09"

keywords: MFA, multifactor authentication, IBMid MFA, two-factor authentication, account MFA, time-based one-time passcode, TOTP

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}
{:external: target="_blank" .external}
{:tip: .tip}
{:note: .note}

# Requiring MFA for users in your account
{: #enablemfa}

As an {{site.data.keyword.Bluemix}} account owner or administrator for the billing service, you can choose to require multifactor authentication (MFA) for every user in the account or just users with non-federated IDs who do not use single sign-on (SSO). All users with an IBMid use a time-based one-time passcode (TOTP) MFA method, and any users with a different type of ID must be enabled to use the TOTP, security questions, or external authentication method separately.  
{:shortdesc}

## Before you begin
{: #considerations}

Review the following considerations before you enable IBMid MFA for your account to ensure that you know how it affects all users in your account:

* When you enable MFA for your account, users must complete the MFA process the next time they log in.
* API keys for users and service IDs continue to work after MFA is enabled.
* If you require the use of CLI or UI login into Cloud Foundry, you must use API keys or SSO after MFA is enabled for the account.
* MFA for your account applies to a user's login, but does not apply to API calls. If a user has permission to make API calls to resources in your account, the user can do so without completing MFA. If the user belongs to other accounts, the user can make API calls to resources in your account by using an API key from an account that did not require MFA.
* If you require MFA for your account and you have users in your account that do not have an IBMid, you must enable one of the other MFA options for that user from the User details page in the {{site.data.keyword.Bluemix_notm}} console. For more information, see [Types of multifactor authentication](/docs/account?topic=account-types).
* Plan a communication and support strategy for users in your account:
  * Choose a date and time that you plan to enable MFA that results in the least impact to your business.
  * Notify your account users after you enable MFA with information on how to [get set up](/docs/account?topic=account-enablemfa#setupapp).

When the multifactor authentication account setting is enabled, all IBMid users in your account are prompted for IBMid MFA authentication upon login. If you have other MFA methods set up for any IBMid users in your account, they are no longer prompted for those MFA methods. For example, if you previously enabled 2FA in the customer portal for your classic infrastructure resources, the MFA account setting overrides the 2FA option. 
{: tip}

## Enabling MFA for all users in your account
{: #enabling}
{: help}
{: support}

To enable MFA, you must be the account owner or an administrator for the billing account management service. Enabling MFA does not affect users that are already logged in, as the enforcement of MFA on the account takes effect only at new logins. Make sure that you notify your account users that MFA is enabled, and describe the impact to users at their next login.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and then select **Settings**.
2. Click **Edit** for the Account login setting.
3. Select **None**, **Non-federated users only**, or **All users** depending on which type of authentication you want to require.
4. Select the checkbox to confirm that you understand the impact of requiring MFA for users in your account, if you select the non-federated users only option.
5. Click **Update**.

## Setting up your TOTP
{: #setupapp}

After you enable MFA for your account, you must set up the one-time passcode with an authenticator app the next time that you log in. All users in your account must also set up the one-time passcode at their next login.

Complete the following steps to set up your one-time passcode with an authenticator app for the first time:

1. Log in with your IBMid and password.

  It might take up to 5 minutes for you to be able to log back in with MFA.
  {: note}

2. Select **Verify** on the **Verification is required** screen to set up MFA with an authenticator app.
3. Select **Setup your authenticator app** to get a one-time code sent to your email to continue setting up the authenticator app.
4. Select **Verify**.
5. Scan the bar code with your app, or click **Can't scan the bar code?** to enter a provided key.
6. Click **Continue** to enter your code.
7. Enter your code and select **Verify**.

If you encounter an error message that states that you've already set up authentication, but your verification code is not working or you do not have your verification code to enter, you must contact the [Help desk](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: external} to reset your MFA enrollment.
{: note}
{: #mfahelp}

## Disabling required MFA for all users in your account
{: #disablemfa}

To disable MFA, you must be the account owner or an administrator for the account management billing service. Disabling MFA does not affect users that are already logged in. The action takes effect at all new logins.

1. From the console, click **Manage** &gt; **Access (IAM)**, and then select **Settings**.
2. Select **Edit** for the Account login setting.
3. Select **None**.
4. Click **Save**.

