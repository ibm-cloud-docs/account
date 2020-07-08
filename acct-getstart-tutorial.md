---

copyright:
  years: 2020
lastupdated: "2020-07-07"

keywords: getting started, account, Subscription, Pay-As-You-Go, enterprise, catalog, upgrade account, IAM, access groups, invite users, notifications, email preferences, account settings

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}

# Setting up your {{site.data.keyword.cloud_notm}} account
{: #account-getting-started}

This tutorial walks you through the steps for setting up an account in {{site.data.keyword.cloud}}. By completing this tutorial, you learn how to set up account authentication, manage your account settings, effectively organize resources in your account, and control access to resources.
{:shortdesc}

This tutorial focuses on how to set up a Pay-As-You-Go account. If you're looking for details about how to set up accounts in an enterprise hierarchy, see [Getting started with an enterprise](/docs/account?topic=account-enterprise-tutorial).
{: tip}

## Step 1. Create your account
{: #account-gs-createlite}

First, create a Lite account by using your existing IBMid or a new IBMid. If your company is registered to use a federated ID for single sign-on (SSO), you can use your federated ID instead to create your account.

| Login ID | Details |    
|-----------------|---------|
|Existing IBMid   | If you already have an IBMid, sign up for {{site.data.keyword.Bluemix_notm}} with your existing credentials that you use for other {{site.data.keyword.IBM}} products and services. |
|New IBMid        | If you don't yet have an IBMid, you'll create one when you sign up. With an IBMid, you can use one username to log in to all {{site.data.keyword.IBM_notm}} products and services, including {{site.data.keyword.Bluemix_notm}}. |
|Federated ID     | If your company already requested to register the user credentials from your company's domain with {{site.data.keyword.IBM_notm}}, you can sign up for {{site.data.keyword.Bluemix_notm}} by using the credentials that you already use for your company's login. You must enter a phone number when you sign up. |
{:caption="Table 1. ID options for creating a Lite account" caption-side="top"}

### Using your IBMid
{: #signup-ibmid}

If you're not a part of a company that uses a federated ID, use your IBMid to create your Lite account.

1. Go to the [{{site.data.keyword.Bluemix_notm}} login page](https://cloud.ibm.com/){: external} ![External link icon](../icons/launch-glyph.svg "External link icon"), and click **Create an {{site.data.keyword.Bluemix_notm}} account**.
1. Enter your IBMid email address. If you don't have an existing IBMid, an ID is created based on the email that you enter.
1. Complete the remaining fields with your information, and click **Create account**.
1. Confirm your account by clicking the link in the confirmation email that's sent to your provided email address.

### Using a federated ID
{: #signup-federated}

A federated ID is an ID within a company's domain that is registered with {{site.data.keyword.IBM_notm}} so that the domain and user credentials can be used to access {{site.data.keyword.IBM_notm}} web applications. You can sign up for {{site.data.keyword.Bluemix_notm}} with a federated ID only if your company is already registered with {{site.data.keyword.IBM_notm}}. Registering a company's domain with {{site.data.keyword.IBM_notm}} enables users to log in to {{site.data.keyword.IBM_notm}} products and services by using their existing company user credentials. Authentication is then handled by your company's identity provider through single sign-on (SSO).

{{site.data.keyword.IBM_notm}} uses the Security Assertion Markup Language 2.0 (SAML 2.0) for this identity federation. SAML 2.0 is a standard version for exchanging authentication data between security domains. It's an XML-based protocol that uses a security token that contains assertions to pass information between the organizations "Identity Provider", and the "{{site.data.keyword.IBM_notm}} Rely Party (RP)", otherwise known as the Service Provider.

For information about how to register your company for a federated ID, see the [IBMid Enterprise Federation Adoption Guide ![External link icon](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: external}. An {{site.data.keyword.IBM_notm}} sponsor, such as an offering advocate or client advocate, is required when you request to register federated IDs.

## Step 2. Upgrade to a Pay-As-You-Go account
{: #account-gs-upgrade}

Upgrade your Lite account to a Pay-As-You-Go account to access the full {{site.data.keyword.cloud_notm}} catalog. 

1. Click **Manage > Account**.
2. Select **Account settings**, and click **Add credit card**.
1. Enter your credit card information.

## Step 3. Set up account authentication
{: #account-gs-mfa}

An the account owner, you can set up  multifactor authentication (MFA) for users in your account.  

Complete the following steps to enable MFA:

1. Go to **Manage** > **Access (IAM)** > **Settings**.
2. Click **Edit** for the Account login setting.
3. Select **None**, **Non-federated users only**, or **All users** depending on which type of authentication you want to require.
4. If you select the non-federated users only option, confirm that you understand the impact of requiring MFA.
5. Click **Update**.


After you enable MFA for your account, complete the following steps to set up a time-based one-time passcode (TOTP) with an authenticator app that you'll use the next time that you log in. All users in your account must also set up the one-time passcode at their next login.

1. Log in with your IBMid and password.

  It might take up to 5 minutes for you to be able to log in after MFA is enabled.
  {: note}

2. Select **Verify** on the **Verification is required** screen to set up MFA with an authenticator app.
3. Select **Setup your authenticator app** to get a one-time code sent to your email to continue setting up the authenticator app.
4. Select **Verify**.
5. Scan the bar code with your app, or click **Can't scan the bar code?** to enter a provided key.
6. Click **Continue** to enter your code.
7. Enter your code and select **Verify**.

## Step 4. Estimate your costs
{: #account-gs-estimate}

Complete the following steps to get an estimate of how much your usage might cost:

1. Go to the [catalog](https://cloud.ibm.com/catalog){: external}, and select **Services**.
2. Select a service that you're interested in.
3. Select a pricing plan, enter other configuration details if needed, and click **Add to estimate**.

  By default, the estimator shows the pricing and billing currency for your location. Pricing can vary by region. If you're estimating costs for a different location, select the correct region to view accurate pricing.
  
4. Add the calculated cost to your estimate by clicking **Save**. 
5. When you're done adding products to your estimate, click **Review estimate** to a detailed view of your estimate. 

  You can download a PDF of the estimate by clicking **Download PDF**.
  {: tip}

## Step 5. Manage your invoices and payment methods
{: #account-gs-invoicepayment}

Before you start working with resources in your account, familiarize yourself with where you can manage your payment method and access your invoices.

### Managing your payment method
{: #account-gs-paymentdetails}

* To manage your payment method for an account that's billed in USD currency, go to **Manage > Billing and usage**, and select **Payments**.
* To manage your payment method for an account that's billed in non-USD currency, go to [IBM Billing](https://myibm.ibm.com/billing/){: external}.

### Accessing your invoices
{: #account-gs-invoicedetails}

* To access an invoice for an account that's billed in USD currency, go to **Manage** > **Billing and usage**, and select **Invoices**. 
* To access an invoice for an account that's billed in non-USD currency, go to **Manage** > **Billing and usage**, and select **Invoices**. Then, click **{{site.data.keyword.IBM_notm}} Invoices**. 

## Step 6. Set preferences for receiving notifications
{: #account-gs-notifications}

Complete the following steps to set your preferences for receiving various types of notifications: 

1. To receive notifications about unplanned events, planned maintenance, announcements, go to the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg)
 > **Profile and settings** > **Notifications**.
   * Platform notifications are associated with the {{site.data.keyword.cloud_notm}} platform and don't apply to events related to {{site.data.keyword.cloud_notm}} services. By default, all platform notifications are turned off. 
   * Infrastructure notifications apply only to the account in which the preferences are set. By default, all infrastructure notifications are turned on. 
2. To receive spending notifications, go to **Manage** > **Billing and usage** > **Spending notifications**. You receive notifications when you reach 80%, 90%, and 100% of the spending thresholds that you specify. 

## Step 7. Create your resource groups
{: #account-gs-resourcegroups}

Resource groups provide a way for you to easily manage access to multiple resources and to view billage usage for a set of resources. With your Pay-As-You-Go account, you can create more resource groups in addition to the default resource group that's included when you first created your Lite account. 

1. Go to **Manage** > **Account** > **Account resources** > **Resource groups**.
2. Click **Create**.
3. Enter a name for your resource group, and click **Add**.

See [What makes a good resource group strategy?](/docs/account?topic=account-account_setup#resource-group-strategy) for details about how to optimally organize resources in your resource groups. 

## Step 8. Set up access
{: #account-gs-accessgroups}

IAM access groups provide a way for you to quickly and easily assign access to multiple resources in your account at one time. 

1. Create an access group.

  1. Go to **Manage** > **Access (IAM)** > **Access Groups**.
  2. Click **Create**.
  3. Enter a name for your group, and click **Create**. For example, if you know multiple users in your account will need to be able to apply subscription codes, track usage, or perform other billed-related tasks, you might name your group `Billing-Editor-Access`. 

2. Assign access to the group. 

  1. Click **Access policies** > **Assign access**.
  2. Select the type of access to assign: 
    
    * **IAM services**: Assigns access to IAM-enabled services, which are services that are managed by using IAM access control and assigned to a resource group.
    * **Account management services**: Assigns access to manage platform services, such as billing, license and entitlements, and enterprises.

  3. Select all roles that apply.
  4. Click **Add** > **Assign**.
  
See [What is a good access group strategy?](/docs/account?topic=account-account_setup#resource-group-strategy) for details about how to best set up your access groups. 
  
## Step 9. Invite users to your account
{: #account-gs-inviteusers}

You're ready to invite users to your account and grant them access based on the resources they will work with and the tasks they'll perform. If you want users to create resources from the catalog and assign the resources to a resource group, the following access is required:

  * Viewer role or higher on the resource group.
  * Editor or administrator role on the service. 

Complete the following steps:

1. Go to **Manage** > **Access (IAM)** > **Users**.
2. Click **Invite users**.
3. Specify the email address of the user. If you are inviting more than one user, they are all assigned the same access.
4. Add the user to one or more of the access groups that you created in the previous step. 
5. Click **Invite**. 

## Step 10. Explore your support options
{: #account-gs-supportcenter}

You can use the Support Center to get help with any issues that you might encounter. To access the Support Center, click **Support** in the console menu bar. 

* The "Help just for you" section features links to common tasks, troubleshooting, and FAQs specific to the resources in your account.
* The "Featured FAQs" section provides FAQs related to platform tasks, for example, resetting your password, IAM, and upgrading your account.
* The "Contact support" section provides the options for getting in touch with a support representative: start a live chat, contact by phone, or create a support case.













