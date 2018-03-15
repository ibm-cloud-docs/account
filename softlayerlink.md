---

copyright:

  years: 2016, 2018

lastupdated: "2018-03-05"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Switching to IBMid and linking accounts
{: #unifyingaccounts}

Authentication in SoftLayer now uses an IBMid to provide a single login for all of {{site.data.keyword.Bluemix}}. An IBMid is a single ID that you use to log into your {{site.data.keyword.Bluemix_notm}} account to access and purchase infrastructure, services, and application features. All new accounts automatically receive an IBMid and existing SoftLayer accounts, except SAML federated accounts, are enabled to switch to IBMid authentication.
{:shortdesc}

## Switching to IBMid
{: #switchtoIBMid}

When you begin the process to switch to an IBMid, you can always cancel the switch before you complete the process. However, each time that you log in, the prompt to switch to an IBMid is displayed. Each SoftLayer account that you plan to link to a {{site.data.keyword.Bluemix_notm}} account must be owned by a unique IBMid with a unique email address.

To switch your existing SoftLayer account to an IBMid, you create an IBMid and then use your registration code to confirm it.

### Requesting an IBMid and registration code
{: #reqIBMidandregcode}

1. Log in to your SoftLayer account, and click **OK** when the prompt to switch to an IBMid is displayed.

   If you are a master user and a prompt to switch to an IBMid is not displayed in the {{site.data.keyword.BluSoftlayer_full}} infrastructure customer portal, contact IBM support for help. See [IBM support](/docs/get-support/howtogetsupport.html#getting-customer-support) for more information about contacting support.

   If you previously logged in and you clicked **Later** in the prompt, but you want to switch to IBMid authentication in the current session, go to the Edit User Profile page and click **Switch to IBMid**.

2. Follow the wizard prompts to create your IBMid.

   Enter an email address that is not currently in use by any IBMid. This email address is used as the user name for the new IBMid, and it's where your registration code is sent after the IBMid is created. You can update the email address that is associated with the IBMid later on, but you can't change the user name.

### Confirming your IBMid with the registration code
{: #confIBMiduseregcode}

1. When you receive your registration code, click the link in the email or copy the URL into a browser and enter your registration code.

   The registration code is valid for seven days and you can use it only once.

2. After you submit your registration code, use your IBMid to log in to the customer portal.

   At the Account Login prompt, go to the **IBMid Account Login** section and click **Log in with IBMid**. Do not use the **Username** and **Password** fields that you used previously with your SoftLayer ID.

If you are a new customer, you're asked for your existing IBMid or to create a new IBMid when you check out your order.
  * To use an existing IBMid, enter the user name or the email address of the IBMid if it is unique (that is, it's not shared across multiple IBMids).
  * To create a new IBMid, enter an email address that is not currently in use by any IBMid. This email address is the user name for the IBMid, and it's where your registration code is sent after the IBMid is created. You can update the email address that's associated with the IBMid later on, but you can't change the user name.

To resolve any problems with logging in with your IBMid, see [Troubleshooting for accessing {{site.data.keyword.Bluemix_notm}}](/docs/troubleshoot/ts_accessing.html#accessing).

## Linking IBMid user accounts
{: #link_user_accounts}

After your user accounts switch to IBMid authentication, resellers and distributors can link SoftLayer accounts and {{site.data.keyword.Bluemix_notm}} accounts to make use of combined infrastructure as a service (IaaS) and platform as a service (PaaS) resources. You can then access IaaS resources from the {{site.data.keyword.BluSoftlayer_full}} infrastructure customer portal and PaaS resources from the  {{site.data.keyword.Bluemix_notm}} console all from a single log in. Linking your accounts also provides you with a single bill for all of the PaaS and IaaS resources that you use.

To link accounts, you must be a SoftLayer master user. The IBMid that is the master user of the account must be the owner of the {{site.data.keyword.Bluemix_notm}} platform account that you're linking to. Be sure to review the following important notes to link accounts:

  * The master user of the SoftLayer account that's being linked must have an IBMid.
  * Each user account that you link to an {{site.data.keyword.Bluemix_notm}} account must be owned by a unique IBMid with a unique email address. Even though a single IBMid can own multiple SoftLayer accounts, you must change the master user to be a unique IBMid for each account. Contact support to change the master user of a SoftLayer account. See [Getting support for {{site.data.keyword.Bluemix_notm}} infrastructure](/docs/customer-portal/cpsupport.html) for more information.
  * When you add new users to a linked account, you must add them to both the SoftLayer account and the {{site.data.keyword.Bluemix_notm}} account so that they can access all the capabilities of the unified console.
  * If you have a brand account, you use the Brand Agent Portal (BAP), and you need support when linking your account, contact the Revenue Services team by emailing softlayer_revenue_services_team@wwpdl.vnet.ibm.com.
  * All linked accounts in {{site.data.keyword.Bluemix_notm}} must be Pay-As-You-Go accounts. You can create a new Pay-As-You-Go account, link an existing Pay-As-You-Go account, or link an existing trial account, which is then upgraded to a Pay-As-You-Go account. You cannot link to {{site.data.keyword.Bluemix_notm}} subscription accounts.

Complete the following steps to link each SoftLayer account to an existing {{site.data.keyword.Bluemix_notm}} platform account or to create a new one:

   1. Log in to the {{site.data.keyword.BluSoftlayer_full}} infrastructure customer portal with your master user account IBMid.
   2. From the {{site.data.keyword.Bluemix_notm}} infrastructure customer portal, click **Link a Bluemix Account**.
   3. Read and accept the terms for linking SoftLayer and {{site.data.keyword.Bluemix_notm}} accounts.
   4. Follow the wizard prompts, including adding the users in the SoftLayer account to the {{site.data.keyword.Bluemix_notm}} account.
   5. When you are prompted, do one of the following actions:
     * If you already have an {{site.data.keyword.Bluemix_notm}} account, provide the email address that is associated with that account to link the accounts.
     * If you don't have an {{site.data.keyword.Bluemix_notm}} account, provide the email address that you want to use and follow the instructions to be invited to {{site.data.keyword.Bluemix_notm}} and create an account.
   6. After you link the account, inform the end user of each account to migrate to IBMid by following the procedure described in the preceding [Switching to IBMid](/docs/account/softlayerlink.html#switchtoIBMid) section.

Migrate only end user accounts to IBMid. Do not migrate brand accounts, which are parent accounts for end user accounts and do not contain any resources. Brand account users that migrate to IBMid lose the ability to log in to the Brand Agent Portal (BAP).
{: tip}

Linked accounts log in to the [{{site.data.keyword.Bluemix}} console ![External link icon](../icons/launch-glyph.svg)](https://console.bluemix.net){: new_window}.

Also, note the following changes after your accounts are linked:
  * You must use your IBMid credentials to access both your SoftLayer and your {{site.data.keyword.Bluemix_notm}} accounts.
  * Any existing SoftLayer discounts are applied across {{site.data.keyword.Bluemix_notm}} charges.
  * You will receive one invoice in United States dollars (USD). If you have an existing {{site.data.keyword.Bluemix_notm}} account, the billing through {{site.data.keyword.Bluemix_notm}} for infrastructure resources takes effect for the new billing cycle that starts after the accounts are linked.
  * You can monitor the usage of your infrastructure resources in the {{site.data.keyword.Bluemix_notm}} console.

After you link your accounts, they cannot be unlinked.
{: tip}

## Multi-factor authentication usage in linked accounts
{: #2fa}

If you have a linked account, you can use the Identity and Access **Settings** page to enable multi-factor authentication for your account. This is also commonly known as two-factor authentication (2FA), and it adds a layer of security for accessing your account beyond the standard required IBMid and password. Multi-factor authentication for your account applies to all resources in your linked {{site.data.keyword.Bluemix_notm}} account. When it is enabled for your account, it also applies to all users who have been added to your account.

Multi-factor authentication is not per IBMid. It is still per account. When an IBMid is associated with multiple accounts, and you switch between accounts, you must confirm your identity every time you switch to a different account that requires two-factor authentication. This is true even if the prior account and the new account are both configured with the same two-factor authentication mechanism.
