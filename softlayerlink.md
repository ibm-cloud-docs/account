---

copyright:
  years: 2016, 2019
lastupdated: "2019-01-28"

keywords: SoftLayer account, link account, complete account, IBM Cloud account, IBMid, Bluemix account, Bluemix

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Switching to IBMid and linking accounts
{: #unifyingaccounts}

An IBMid is a single ID that you use to log in to your {{site.data.keyword.Bluemix}} account to access and purchase infrastructure, services, and application features. All new accounts automatically receive an IBMid and existing SoftLayer accounts, except SAML federated accounts, are enabled to switch to IBMid authentication.
{:shortdesc}

## Switching to IBMid
{: #switchtoIBMid}

When you begin the process to switch to an IBMid, you can always cancel the switch before you complete the process. However, each time that you log in, the prompt to switch to an IBMid is displayed. Each SoftLayer account that you plan to link to an {{site.data.keyword.Bluemix_notm}} account must be owned by a unique IBMid with a unique email address.

To switch your existing SoftLayer account to an IBMid, you create an IBMid and then use your registration code to confirm it.

### Requesting an IBMid and registration code
{: #reqIBMidandregcode}

1. Log in to your SoftLayer account, and click **OK** when the prompt to switch to an IBMid is displayed.

   If you are a master user and a prompt to switch to an IBMid is not displayed in the customer portal, contact IBM support for help. See [Getting support](/docs/get-support?topic=get-support-getting-customer-support) for more information about contacting support.

   If you previously logged in and you clicked **Later** in the prompt, but you want to switch to IBMid authentication in the current session, go to the Edit User Profile page and click **Switch to IBMid**.

2. Follow the wizard prompts to create your IBMid.

   Enter an email address that is not currently in use by any IBMid. This email address is used as the user name for the new IBMid, and it's where your registration code is sent after the IBMid is created. You can update the email address that is associated with the IBMid later on, but you can't change the user name.

### Confirming your IBMid with the registration code
{: #confIBMiduseregcode}

1. When you receive your registration code, click the link in the email or copy the URL into a browser and enter your registration code. The registration code is valid for seven days and you can use it only once.

2. After you submit your registration code, use your IBMid to log in to the customer portal.

   At the Account Login prompt, go to the **IBMid Account Login** section and click **Log in with IBMid**. Do not use the **Username** and **Password** fields that you used previously with your SoftLayer ID.

If you are a new customer, you're asked for your existing IBMid or to create a new IBMid when you check out your order.
  * To use an existing IBMid, enter the user name or the email address of the IBMid if it is not shared across multiple IBMids.
  * To create a new IBMid, enter an email address that is not currently in use by any IBMid. This email address is the user name for the IBMid, and it's where your registration code is sent after the IBMid is created. You can update the email address that's associated with the IBMid later on, but you can't change the user name.

To resolve any problems with logging in with your IBMid, see [Troubleshooting for accessing {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-accessing).


## Linking IBMid accounts
{: #link_accounts}

After accounts are switched to IBMid accounts, you can link SoftLayer accounts and {{site.data.keyword.Bluemix_notm}} accounts to use combined infrastructure as a service (IaaS) and platform as a service (PaaS) resources. Then, you can access IaaS resources and PaaS resources from a single login. Linking your accounts also provides you with a single bill for all of the PaaS and IaaS resources that you use. You can link your own account or, if you are a master user, you can link your user accounts.

### Linking your IBMid account
{: #link_user_account}

If you are a classic infrastructure customer, and you also have PaaS accounts in {{site.data.keyword.Bluemix_notm}} or create them, you can link IaaS and PaaS for a single view of your accounts. To link your accounts, use the following steps:
1. Log in to your SoftLayer account.
2. From the Account Summary page, click **New! Link a Bluemix Account**.
3. Review the terms of use and click to acknowledge your acceptance.
4. Complete one of the following final steps, depending on how your account is set up:
  * If your IBMid has an associated {{site.data.keyword.Bluemix_notm}} account you’ll be directed to an authorization page, then back to the final confirmation step.
  * If you don’t have an associated {{site.data.keyword.Bluemix_notm}} account, you are prompted to create a new one.

To see common questions and answers about linking your account, check out the [FAQs](/docs/account?topic=account-al_login).

### Linking IBMid user accounts
{: #link_customer_accounts}

After your user accounts switch to IBMid authentication, resellers and distributors can link their users accounts. To link customer accounts, you must be a SoftLayer master user. The IBMid that is the master user of the account must be the owner of the {{site.data.keyword.Bluemix_notm}} platform account that you're linking to.

After you link your accounts, they can't be unlinked.
{: note}

Be sure to review the following important notes about linking accounts:

  * The master user of the SoftLayer account that's being linked must have an IBMid.
  * Each user account that you link to an {{site.data.keyword.Bluemix_notm}} account must be owned by a unique IBMid with a unique email address. Even though a single IBMid can own multiple SoftLayer accounts, you must change the master user to be a unique IBMid for each account. Contact support to change the master user of a SoftLayer account. See [Getting support for {{site.data.keyword.Bluemix_notm}} infrastructure](/docs/customer-portal?topic=customer-portal-customerportal_support) for more information.
  * When you add new users to a linked account, you must add them to both the SoftLayer account and the {{site.data.keyword.Bluemix_notm}} account so that they can access all the capabilities of the unified console.
  * If you have a brand account, you use the Brand Agent Portal (BAP), and you need support when linking your account, contact the Revenue Services team by emailing softlayer_revenue_services_team@wwpdl.vnet.ibm.com.

Complete the following steps to link each SoftLayer account to an existing {{site.data.keyword.Bluemix_notm}} platform account or to create a new one:

   1. Log in to the customer portal with your master user account IBMid.
   2. From the customer portal, click **Link a Bluemix Account**.
   3. Read and accept the terms for linking SoftLayer and {{site.data.keyword.Bluemix_notm}} accounts.
   4. Follow the wizard prompts, including adding the users in the SoftLayer account to the {{site.data.keyword.Bluemix_notm}} account.
   5. When you are prompted, do one of the following actions:
     * If you already have an {{site.data.keyword.Bluemix_notm}} account, provide the email address that is associated with that account to link the accounts.
     * If you don't have an {{site.data.keyword.Bluemix_notm}} account, provide the email address that you want to use and follow the instructions to be invited to {{site.data.keyword.Bluemix_notm}} and create an account.
   6. After you link the account, inform the end user of each account to migrate to IBMid by following the procedure described in the preceding [Switching to IBMid](#switchtoIBMid) section.

      Migrate only end user accounts to IBMid. Do not migrate brand accounts, which are parent accounts for end user accounts and do not contain any resources. Brand account users that migrate to IBMid lose the ability to log in to the Brand Agent Portal (BAP).
      {: important}

Note the following changes after your accounts are linked:

  * You now log in to the [{{site.data.keyword.Bluemix}} console ![External link icon](../icons/launch-glyph.svg)](https://cloud.ibm.com){: new_window}.
  * You must use your IBMid credentials to access both your SoftLayer and your {{site.data.keyword.Bluemix_notm}} accounts.
  * Any existing SoftLayer discounts are applied across {{site.data.keyword.Bluemix_notm}} charges.
  * You receive one invoice in United States dollars (USD). If you have an existing {{site.data.keyword.Bluemix_notm}} account, the billing through {{site.data.keyword.Bluemix_notm}} for infrastructure resources takes effect for the new billing cycle that starts after the accounts are linked. For more information, see [Consolidated billing for linked accounts](/docs/customer-portal?topic=customer-portal-unifybillaccounts).
  * You can monitor the usage of your classic infrastructure resources in the {{site.data.keyword.Bluemix_notm}} console.

## Multi-factor authentication usage in linked accounts
{: #2fa}

If you have a linked account, you can use the {{site.data.keyword.Bluemix_notm}} IAM **Settings** page to enable multi-factor authentication (MFA) for your account. This is also commonly known as two-factor authentication (2FA), and it adds a layer of security for accessing your account beyond the standard required IBMid and password. MFA for your account applies to all resources in your linked {{site.data.keyword.Bluemix_notm}} account. When it is enabled for your account, it also applies to all users who have been added to your account.

Other multi-factor authentication methods are not per IBMid. It is per account. When an IBMid is associated with multiple accounts, and you switch between accounts, you must confirm your identity every time you switch to a different account that requires two-factor authentication. This is true even if the prior account and the new account are both configured with the same two-factor authentication mechanism.

If you previously enabled [2FA in the customer portal](/docs/customer-portal?topic=customer-portal-customerportal_2fa) for your classic infrastructure resources, and then you enable the {{site.data.keyword.Bluemix_notm}} account MFA setting, the MFA account setting overrides the 2FA that you set up in the customer portal. This means you can disable the 2FA that you purchased in the customer portal in favor of the account MFA setting.
