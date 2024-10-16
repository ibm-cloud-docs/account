---

copyright:

  years: 2020, [{CURRENT_YEAR}]

lastupdated: "[{LAST_UPDATED_DATE}]"


keywords: getting started, account, Subscription, Pay-As-You-Go, catalog, upgrade account, IAM, access groups, invite users, notifications, email preferences, account settings, authentication, MFA, TOTP, U2F, FIDO U2F, security key, google login, Google ID, Google sign up

subcollection: account

content-type: tutorial
completion-time: 60m

---

{{site.data.keyword.attribute-definition-list}}

# Setting up your {{site.data.keyword.cloud_notm}} account
{: #account-getting-started}
{: toc-content-type="tutorial"}
{: toc-completion-time="60m"}

This tutorial walks you through the steps for setting up a Pay-As-You-Go account in {{site.data.keyword.cloud}}. By completing this tutorial, you learn how to set up account authentication, manage your account settings, effectively organize resources in your account, and control access to resources.
{: shortdesc}

## Create your account
{: #account-gs-create}
{: step}

First, create an account by using your existing IBMid or a new IBMid. If your company is registered to use a federated ID for single sign-on (SSO), you can use your federated ID instead.

| Login ID | Details |
|-----------------|---------|
|Existing IBMid   | If you already have an IBMid, sign up for {{site.data.keyword.Bluemix_notm}} with your existing credentials that you use for other {{site.data.keyword.IBM}} products and services. |
|New IBMid        | If you don't yet have an IBMid, you can create one when you sign up. With an IBMid, you can use one username to log in to all {{site.data.keyword.IBM_notm}} products and services, including {{site.data.keyword.Bluemix_notm}}. |
|Federated ID     | If your company already requested to register the user credentials from your company's domain with {{site.data.keyword.IBM_notm}}, you can sign up for {{site.data.keyword.Bluemix_notm}} by using the credentials that you already use for your company's login. You must enter a phone number when you sign up. |
|Google ID | If you already have a Google account, you can use the credentials for Google to sign-up or log in to {{site.data.keyword.IBM_notm}}. |
{: caption="ID options for creating an account" caption-side="top"}

### Using your IBMid
{: #signup-ibmid}

If you're not a part of a company that uses a federated ID, use your IBMid to create your account.

1. Go to the [{{site.data.keyword.Bluemix_notm}} login page](https://cloud.ibm.com/){: external}, and click **Create an {{site.data.keyword.Bluemix_notm}} account**.
1. Enter your IBMid email address. If you don't have an existing IBMid, an ID is created based on the email that you enter.
1. Complete the remaining fields with your information.

   You are prompted for your credit card information to verify your identity and secure your account. You can [try out {{site.data.keyword.Bluemix_notm}} for free](/docs/overview?topic=overview-tutorial-try-for-free) and pay only for the billable services that you choose to use, with no long-term contracts or commitments.
   {: note}

1. Click **Create account**.
1. Confirm your account by clicking the link in the confirmation email that's sent to your provided email address.

See [Account types](/docs/account?topic=account-accounts) to compare and choose an account type.

### Personal use availability
{: #signup-personalaccts}

The following table shows the countries where personal use of our platform that is not related to business, trade, craft, or professional purposes are not supported

| Country |
|---------|
| Algeria |
| Cameroon |
| Canary Islands |
| Egypt |
| Ghana |
| Ivory Coast |
| Kenya |
| Mauritania |
| Nigeria |
| Seychelles |
| Tanzania |
| Uganda |
{: caption="Countries in Africa that are not supported" caption-side="bottom"}
{: #Africa}
{: tab-title="Africa"}
{: tab-group="not-supported-countries"}
{: class="simple-tab-table"}

| Country |
|---------|
| Armenia |
| Bahrain |
| Kazakstan |
| Kingdom of Saudi Arabia |
| Taiwan |
| Turkey |
| United Arab Emirates |
| Uzbekistan|
| Vietnam |
{: caption="Countries in Asia that are not supported" caption-side="bottom"}
{: #Asia}
{: tab-title="Asia"}
{: tab-group="not-supported-countries"}
{: class="simple-tab-table"}

| Country |
|---------|
| Albania|
| Belarus |
| Moldova |
| Norway |
| Serbia |
| Switzerland |
| Ukraine|
{: caption="Countries in Europe that are not supported" caption-side="bottom"}
{: #Europe}
{: tab-title="Europe"}
{: tab-group="not-supported-countries"}
{: class="simple-tab-table"}

{{site.data.keyword.IBM}} Norway and {{site.data.keyword.IBM}} Switzerland are able to contract with local customers to offer personal use accounts.
{: note}

To work with a local Business Partner, go to the [IBM Business Partner Directory](https://www.ibm.com/partnerplus/directory){: external}. Customers are not required to have a VAT ID to work with a local Business Partner.

### Using a federated ID
{: #signup-federated}

A federated ID is an ID within a company's domain that is registered with {{site.data.keyword.IBM_notm}} so that the domain and user credentials can be used to access {{site.data.keyword.IBM_notm}} web applications. You can sign up for {{site.data.keyword.Bluemix_notm}} with a federated ID only if your company is already registered with {{site.data.keyword.IBM_notm}}. Registering a company's domain with {{site.data.keyword.IBM_notm}} enables users to log in to {{site.data.keyword.IBM_notm}} products and services by using their existing company user credentials. Authentication is then handled by your company's identity provider (IdP) through single sign-on (SSO).

{{site.data.keyword.IBM_notm}} uses the Security Assertion Markup Language 2.0 (SAML 2.0) for this identity federation. SAML 2.0 is a standard version for exchanging authentication data between security domains. It’s an XML-based protocol that uses a security token that contains assertions to pass information between the organization's IdP, and the {{site.data.keyword.IBM_notm}} Rely Party (RP), otherwise known as the Service Provider.

For information about how to register your company for a federated ID, see the [IBMid Enterprise Federation Adoption Guide](https://www.ibm.com/docs/en/ief){: external}. An {{site.data.keyword.IBM_notm}} sponsor, such as an product advocate or client advocate, is required when you request to register federated IDs.


### Using a Google ID 
{: #signup-google}

Your Google credentials can be used to sign-up for a new {{site.data.keyword.Bluemix_notm}} account, or can be used to log in to an existing {{site.data.keyword.Bluemix_notm}} account. Users that log in with Google are treated like non-federated users, and multifactor authentication (MFA) is enabled for all users to add an extra layer of security.

This functionality is only available for newly registered IBMids on any eligible domain and existing IBMids on the gmail.com and googlemail.com domains. Logging in with Google credentials is not available for IBMids that are federated with a corporate identity provider through SAML.
{: note}

You can log in with your Google from the [{{site.data.keyword.Bluemix_notm}} login page](https://cloud.ibm.com/){: external} by clicking **Continue with Google** and entering your Google credentials. 

To sign-up with your Google credentials, complete the following steps: 
1. Go to the [{{site.data.keyword.Bluemix_notm}} login page](https://cloud.ibm.com/){: external}, and click **Create an {{site.data.keyword.Bluemix_notm}} account**.
1. Click **Continue with Google**. 
1. Review the IBMid account privacy notice, and click **Proceed**. 
1. Select your country, and click **Next**. 
1. Review the terms and conditions. 
1. Click **Continue**.

## Set up account MFA settings
{: #account-gs-mfa}
{: step}

By default, users in your account verify themselves by logging in with a username and password. To require users to use more secure authentication factors, complete the following steps to set up multifactor authentication (MFA).

Setting up MFA in your account affects all members of the account. This means that if users of your account are members of multiple {{site.data.keyword.cloud_notm}} accounts, they must enroll for MFA at their next login even if they don't intend to use resources in the secured account.
{: important}

1. Go to **Manage** > **Access (IAM)** > **Settings** in the {{site.data.keyword.cloud_notm}} console.
1. Update the current authentication setting by clicking **Edit** in the Authentication section.
1. Select the type of MFA to enable in your account.
   * **MFA for users with an IBMid**: Require users to authenticate by using an IBMid, password, and time-based one-time passcode (TOTP). You can enable this option for all users or non-federated users.
   * **MFA for all users (IBMid & supported IdPs)**: Require users to authenticate by using one of the following MFA factors. This option applies to users who are using either an IBMid or an external IdP.
      * **Email-based MFA**: Users authenticate by using a security passcode that's sent by email.
      * **TOTP MFA**: Users authenticate by using a time-based one-time passcode (TOTP) with an authenticator app, such as {{site.data.keyword.IBM_notm}} Security Verify or Google Authenticator.
      * **U2F MFA**: Users authenticate by using a hardware security key. This factor offers the highest level of security.
1. Click **Update**.

The first time that you log in to your account after updating your MFA settings, you need to verify your identity by using two different verification methods. Methods for verification include email, text, or phone call, and you can use any combination of those options to verify your identity. After you verify your identity, you set up and provide details for your authentication factor.
{: note}


## Estimate your costs
{: #account-gs-estimate}
{: step}

Complete the following steps to get an estimate of how much your usage might cost:

1. Go to the [catalog](https://cloud.ibm.com/catalog){: external}, and select **Services**.
2. Select a service that you're interested in.
3. Select a pricing plan, enter other configuration details if needed, and click **Add to estimate**.

   By default, the estimator shows the pricing and billing currency for your location. Pricing can vary by region. If you're estimating costs for a different location, select the correct region to view accurate pricing.

1. Add the calculated cost to your estimate by clicking **Save**.
1. When you're done adding products to your estimate, click **Review estimate** to a detailed view of your estimate.

   You can download a CSV, XSLX, or PDF of the estimate by clicking **Download**.
   {: tip}

## Manage your invoices and payment methods
{: #account-gs-invoicepayment}
{: step}

Before you start working with resources in your account, familiarize yourself with where you can manage your payment method and access your invoices.

### Managing your payment method
{: #account-gs-paymentdetails}

* To manage your payment method for an account that's billed in USD currency, go to **Manage** > **Billing and usage** in the {{site.data.keyword.cloud_notm}} console, and select **Payments**.
* To manage your payment method for an account that's billed in non-USD currency, go to [{{site.data.keyword.IBM_notm}} Billing](https://myibm.ibm.com/billing/){: external}.

### Accessing your invoices
{: #account-gs-invoicedetails}

* To access an invoice for an account that's billed in USD currency, go to **Manage** > **Billing and usage** in the {{site.data.keyword.cloud_notm}} console, and select **Invoices**.
* To access an invoice for an account that's billed in non-USD currency, go to **Manage** > **Billing and usage** in the {{site.data.keyword.cloud_notm}} console, and select **Invoices**. Then, click **{{site.data.keyword.IBM_notm}} Invoices**.

## Set preferences for receiving notifications
{: #account-gs-notifications}
{: step}

Complete the following steps to set your preferences for receiving various types of notifications:

1. To receive notifications about {{site.data.keyword.cloud_notm}} platform-related, or resource-related items, go to the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar")
   **Profile** > **Notification preferences**.
   * When you set {{site.data.keyword.cloud_notm}} platform notifications, you receive email notifications that are associated with only the platform. You do not receive notifications about events that are associated with {{site.data.keyword.cloud_notm}} services. By default, all platform notifications are turned off.
   *  If you update your preferences on resource activity, such as incidents, maintenance, security bulletins, or infrastructure service updates, the notifications are for only the services you use or the devices that you created. By default, all infrastructure notifications are turned off.

1. To receive spending notifications, go to **Manage** > **Billing and usage** > **Spending notifications** in the {{site.data.keyword.cloud_notm}} console. Or, you can access it directly from the [Notification preferences](/user/notifications) page by clicking **Manage** in the **Billing and Usage** section.

   You receive notifications when you reach 80%, 90%, and 100% of the spending thresholds that you specify. Enter the dollar amount to set a spending threshold when set up your spending notification. For more information, see [Setting spending notifications](/docs/billing-usage?topic=billing-usage-spending).


## Create your resource groups
{: #account-gs-resourcegroups}
{: step}

Resource groups provide a way for you to easily manage access to multiple resources and to view billing usage for a set of resources. With your Pay-As-You-Go account, you can create more resource groups in addition to the default resource group that's created for you.

1. Go to **Manage** > **Account** > **Account resources** > **Resource groups** in the {{site.data.keyword.cloud_notm}} console.
1. Click **Create**.
1. Enter a name for your resource group, and click **Add**.

See [What makes a good resource group strategy?](/docs/account?topic=account-account_setup#resource-group-strategy) for details about how to optimally organize resources in your resource groups.

## Set up access
{: #account-gs-accessgroups}
{: step}

IAM access groups provide a way for you to quickly and easily assign access to multiple resources in your account at one time.

1. Create an access group.

   1. Go to **Manage** > **Access (IAM)** > **Access Groups** in the {{site.data.keyword.cloud_notm}} console.
   1. Click **Create**.
   1. Enter a name for your group, and click **Create**. For example, if you know multiple users in your account need to be able to apply subscription codes, track usage, or perform other billed-related tasks, you might name your group `Billing-Editor-Access`.

1. Assign access to the group.

   1. Click **Access** > **Assign access**.
   1. Select a single service or a group of services:

      * **All Identity and Access enabled services**: Assigns access to all catalog services that use IAM for access management.
      * **All Account Management services**: Assigns access to manage platform services, such as billing, and license and entitlements. For more information, see [Assigning access to account management services](https://cloud.ibm.com/docs/account?topic=account-account-services&interface=ui#account-management-actions-roles).
      * **All IAM Account Management services**: Assigns access to a subset of account management services that includes the IAM platform services IAM Identity, IAM Access Management, IAM User Management, IAM Groups, and future IAM services.

   1. Click **Next**.
   1. Select all roles that apply, then click **Next**.
   1. Click **Add** and repeat as needed.
   1. Click **Assign**.

See [What makes a good access group strategy?](/docs/account?topic=account-account_setup#resource-group-strategy) for details about how to best set-up your access groups.

## Invite users to your account
{: #account-gs-inviteusers}
{: step}

You're ready to invite users to your account and grant them access based on the resources they work with and the tasks they perform. If you want users to create resources from the catalog and assign the resources to a resource group, the following access is required:

* Viewer role or higher on the resource group.
* Editor or administrator role on the service.

Complete the following steps:

1. Go to **Manage** > **Access (IAM)** > **Users** in the {{site.data.keyword.cloud_notm}} console.
1. Click **Invite users**.
1. Specify the email address of the user. If you are inviting more than one user, they are all assigned the same access.
1. Add the user to one or more of the access groups that you created in the previous step.
1. Click **Invite**.

To learn more about the invitation flow and how users can accept invitations, see [Inviting users to an account](/docs/account?topic=account-iamuserinv).

You can also give users access to your account by using trusted profiles. For more information, see [What makes a good trusted profiles strategy?](/docs/account?topic=account-account_setup#trustedprofiles_strategy).

## Explore your support options
{: #account-gs-supportcenter}
{: step}

You can use the Support Center to get help with any issues that you might encounter. To access the Support Center, click the **Help** icon ![Help icon](../icons/help.svg "Help") > **Support center** from the console menu bar.

* The Help just for you section features links to common tasks, troubleshooting, and FAQs specific to the resources in your account.
* The Featured FAQs section provides FAQs related to platform tasks, for example, resetting your password, IAM, and upgrading your account.
* The Contact support section provides the options for getting in touch with a support representative: start a live chat, contact by phone, or create a support case.
