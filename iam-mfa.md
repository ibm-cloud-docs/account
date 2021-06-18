---

copyright:

  years: 2018, 2021
lastupdated: "2021-06-18"

keywords: MFA, multifactor authentication, IBMid MFA, two-factor authentication, account MFA, time-based one-time passcode, TOTP, FIDO U2F, U2F, universal 2nd factor authentication, security key

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

# Enabling MFA for your account
{: #enablemfa}

As an {{site.data.keyword.Bluemix}} account owner or administrator for the billing service, you can choose to require multifactor authentication (MFA) for every user in the account or just users with IBMids who do not use single sign-on (SSO).
{:shortdesc}

## Before you begin
{: #considerations}

Review the following considerations before you enable IBMid MFA for your account to ensure that you know how it affects all users in your account:

* Enabling MFA in your account affects all members of the account. This means that if users of your account are members of multiple {{site.data.keyword.cloud_notm}} accounts, they must enroll for MFA at their next login even if they don't intend to use resources in the secured account. 
* API keys for users and service IDs continue to work after MFA is enabled.
* If you require the use of CLI or UI login into Cloud Foundry, you must use API keys or SSO after MFA is enabled for the account.
* MFA for your account applies to a user's login, but does not apply to API calls. If a user has permission to make API calls to resources in your account, the user can do so without completing MFA. If the user belongs to other accounts, the user can make API calls to resources in your account by using an API key from an account that did not require MFA.
* Plan a communication and support strategy for users in your account:
  * Choose a date and time that you plan to enable MFA that results in the least impact to your business.
  * Notify your account users after you enable MFA with information on how to get set up.

When the MFA setting is enabled, all IBMid users in your account are prompted for IBMid MFA authentication upon login. If you have other MFA factors set up for any IBMid users in your account, they are no longer prompted for those MFA factors. For example, if you previously enabled 2FA in the customer portal for your classic infrastructure resources, the MFA account setting overrides the 2FA option. 
{: tip}

## Enabling MFA 
{: #enabling}
{: help}
{: support}

To enable MFA, you must be the account owner or an administrator for the billing account management service. Enabling MFA does not affect users that are already logged in, as the enforcement of MFA on the account takes effect only at new logins. Make sure that you notify your account users that MFA is enabled, and describe the impact to users at their next login.

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)** > **Settings**.
2. Click **Edit** in the Authentication section.
3. Select the type of MFA to enable in your account.

 * **MFA for users with an IBMid**: Require users to authenticate by using an IBMid, password, and time-based one-time passcode (TOTP). You can enable this option for all users or  non-federated users. 
 * **MFA for all users (IBMid & supported IdPs)**: Require users to authenticate by using one of the following MFA factors. This option applies to users who are using either an IBMid or an external identity provider (IdP). 
     * **Email-based MFA**: Users authenticate by using a security passcode that's sent in an email. 
     * **TOTP MFA**: Users authenticate by using a TOTP. 
     * **U2F MFA**: Users authenticate by using a physical hardware-based security key that generates a six-digit numerical code. Based on the FIDO U2F standard, this factor offers the highest level of security.

4. Click **Update**.

### Setting up your TOTP
{: #setupapp}

After you set up MFA in your account, create a time-based one-time passcode (TOTP) with an authenticator app, such as {{site.data.keyword.IBM_notm}} Security Verify or Google Authenticator, that you use the next time you log in. All users in your account must also create a TOTP with an authenticator app before they can log in again. 

1. Log in with your IBMid and password.

  It might take up to 5 minutes for you to be able to log in after MFA is enabled.
  {: note}

2. Click **Verify** on the Verification is required screen to create a TOTP with an authenticator app.
3. Click **Setup your authenticator app**.
4. Use your app to scan the bar code, or select **Can't scan the bar code?** to enter the provided key.

If you encounter an error message that states that you've already set up authentication, but your verification code is not working or you do not have a verification code to enter, contact the [{{site.data.keyword.IBM_notm}} Help desk](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: external}) to reset your MFA enrollment.
{: note}
{: #mfahelp}

## Disabling MFA
{: #disablemfa}

To disable MFA, you must be the account owner or an administrator for the account management billing service. Disabling MFA does not affect users that are already logged in. The action takes effect at all new logins.

1. Go to **Manage** > **Access (IAM)** > **Settings**.
2. Click **Edit** in the Authentication section.
3. Select **None**.
4. Click **Update**.

