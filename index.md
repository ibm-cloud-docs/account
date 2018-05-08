---

copyright:

  years: 2015, 2018
lastupdated: "2018-05-08"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Account types
{: #accounts}

You can start building on {{site.data.keyword.Bluemix}} for free. We have three different account types that you can choose from: Lite, Pay-As-You-Go, and Subscription. You can use any of the account types to get started in {{site.data.keyword.Bluemix_notm}} - simply choose the one that best suits your needs.
{:shortdesc}

## Account comparison
{: #compare}

The following table provides a comparison of Lite, Pay-As-You-Go, and Subscription accounts. For more details about each account, see the sections that follow.

|  | Lite  | Pay-As-You-Go | Subscription |
|--------------------|--------------------|--------------------|--------------------|
| **Access to free Cloud Foundry memory** | 256 MB | 512 MB | 512 MB |
| **Access to [Lite service plans ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/?search=label:lite){: new_window}** | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Access to all free plans** |  | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Access to the full catalog** |  | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Access to multiple Cloud Foundry regions** |  | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **No time restrictions** | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Guaranteed zero cost** | ![Feature available](../icons/icon_enabled.svg) |  |  |
| **Discounted pricing** |  |  | ![Feature available](../icons/icon_enabled.svg) |
| **Best for learning or building proof of concepts** | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |  |
| **Fit for production use cases** |  | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
{: caption="Table 1. Comparison of {{site.data.keyword.Bluemix_notm}} accounts" caption-side="top"}

## Lite account
{: #liteaccount}

Sign up for a free Lite account to build apps and explore services with select free plans that are named Lite and displayed with a Lite tag ![Lite tag](../icons/Lite.svg) in the {{site.data.keyword.Bluemix_notm}} console. Your Lite account doesn't expire and your credit card isn't required.

You have access to a single resource group that's created for you and named `Default`. All of your services instances that are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) are automatically added to this resource group. You can update the name of this resource group at any time. See [Renaming a resource group](/docs/account/resourcegroups.html#renaming-a-resource-group) for the detailed steps.

Each resource group is free. When you create a connection between a service managed by IAM and a Cloud Foundry app, you create an alias, which is a service instance, that counts toward your quota. See [What is an alias?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

### What's available?

You might be wondering what's offered in a Lite account. Check out the following list of key features:

   * The account is free - no credit card required.
   * The account never expires.
   * You can use one org in one {{site.data.keyword.Bluemix_notm}} region.
   * Basic {{site.data.keyword.Bluemix_notm}} support for free. Basic support is provided for non-production environments or workloads where traditional severities are not used and specific response times are not stipulated.
   * You receive email notifications about your account status and quota limits.
   * Your Cloud Foundry apps can access up to 256 MB of free, instantaneous runtime memory.
   * You can provision one instance of any service in the [{{site.data.keyword.Bluemix_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window} that has a Lite plan.
   * After 10 days of no development activity, your apps go to sleep. You can start working on new apps without having to worry about hitting memory quota limits.
   * After 30 days of no development activity, your service instances with Lite plans are deleted. This way, you don't have to manage deleting inactive instances before you create new ones.

### Upgrading your account

When you are ready to grow, upgrade to a Pay-As-You-Go account and pay for only what you use beyond the free allowances. After you upgrade, you can continue using any instances you created with your Lite account. Go to **Manage** > **Billing and Usage** > **Billing** in the console, and click **Add Credit Card**. 

## Billable accounts
{: #billableacts}

The following table lists the different account types and their charging methods.

|Account type |	How am I charged? |
|------------------|-----------------------|
|Pay-As-You-Go |	Charges are based on your use of {{site.data.keyword.Bluemix_notm}} compute and services |
|Subscription | You can get a monthly discount based on a minimum monthly spending commitment |
| {{site.data.keyword.Bluemix_dedicated_notm}} | Annual contract |
|{{site.data.keyword.Bluemix_local_notm}} |	Annual contract |
{:caption="Table 2. {{site.data.keyword.Bluemix_notm}} billable accounts and charges" caption-side="top"}

If you link your {{site.data.keyword.Bluemix_notm}} billable account with a SoftLayer account, starting on the first of the next month, your combined charges are included on your {{site.data.keyword.Bluemix_notm}} invoice. For more information, see [Viewing credits](/docs/billing-usage/viewing_usage.html#credits).
{: tip}

### Pay-As-You-Go account

With a Pay-As-You-Go account, you can create multiple resource groups to easily manage quota and view billing usage for a set of resources. You're eligible for free runtime and service allowances. If you use more than the free allowance, you'll receive a monthly {{site.data.keyword.Bluemix_notm}} invoice. The invoice will be in United States dollars (USD) and will detail your resource charges.

In many countries and regions, you can sign up for a Pay-As-You-Go account from the {{site.data.keyword.Bluemix_notm}} console. After you provide your billing and credit card information, accept the terms and conditions, and submit your account request. Then, your credit card will be validated. You'll also receive a confirmation email regarding the account information. A few minutes after you receive the confirmation email, you can return to the console to continue building your apps. 

If your online request can't be processed for your country or region, contact [{{site.data.keyword.Bluemix_notm}} Support](https://ibm.biz/bluemixsupport){: new_window} ![External link icon](../icons/launch-glyph.svg). After you log in to the {{site.data.keyword.Bluemix_notm}} Service Portal, click **contact support** and select the **Billing, Account or Login** option.

You can convert your Pay-As-You-Go account to a Subscription account at any time. Contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) for more details.
{: tip}

### Subscription account

With a Subscription account, you can create multiple resource groups to easily manage quota and view billing usage for a set of resources.

You commit to a minimum spending amount each month and receive a subscription discount that is applied to that minimum charge. You also pay for any usage that exceeds the minimum spending amount.

To sign up for a Subscription account, and for more information about subscription rates and discounts, you must contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg)

### {{site.data.keyword.Bluemix_dedicated_notm}} account

With {{site.data.keyword.Bluemix_dedicated_notm}}, you must sign up for a one year minimum term that includes:

   * VPN connectivity back to your infrastructure
   * Fully redundant environment in a {{site.data.keyword.BluSoftLayer_notm}} data center
   * All supported runtimes (IBM Java Liberty, Node.js, and built-in open source runtimes)
   * All dedicated services that you have selected and all public {{site.data.keyword.Bluemix_notm}} services
   * Standard {{site.data.keyword.Bluemix_notm}} support

You can also order optional items such as SoftLayer DirectLink or premium support options. Contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) for more information.

What you pay each month during that term is based on the dedicated services that you want, plus a Subscription account that gives you access to all public services. Usage charges of the services in {{site.data.keyword.Bluemix_notm}} Public are calculated based on your Subscription account agreement. You receive an invoice for any services that you use beyond that subscription agreement. Contact your IBM designated account representative or [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) to get started on your agreement.

### {{site.data.keyword.Bluemix_local_notm}} account

With {{site.data.keyword.Bluemix_local_notm}}, you must sign up for a one year minimum term that includes:

   * A delivery capability called relay that enables IBM to connect to your local deployment and automatically and consistently deliver updates
   * All supported runtimes (IBM Java Liberty, Node.js, and built-in open source runtimes)
   * All local services that you have selected and access to all public {{site.data.keyword.Bluemix_notm}} services
   * Standard {{site.data.keyword.Bluemix_notm}} support

What you pay each month during that term is based on the local services that you want, plus a Subscription account that gives you access to all public services. Usage charges of the services in {{site.data.keyword.Bluemix_notm}} Public are calculated based on your Subscription account agreement. You receive an invoice for any services that you use beyond that subscription agreement. Contact your IBM designated account representative or [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) to get started on your agreement.

## Trial account
{: #trial}

Trial accounts are available in all regions. With a free 30-day trial, you can jump right in and start building your apps and exploring services in {{site.data.keyword.Bluemix_notm}}.

When you sign up for a free trial with your {{site.data.keyword.Bluemix_notm}} ID, your account is provided with the following resources free of charge:

  * Maximum 2 GB memory
  * 10 services
  * 1 SSL certificate

You also have access to a single resource group that's created for you and named `Default`. All of your IAM-managed service instances are automatically added to this resource group. You can update the name of this resource group at any time. See [Renaming a resource group](/docs/account/resourcegroups.html#renaming-a-resource-group) for the detailed steps.

Each resource group is free. When you create a connection between a service managed by IAM and a Cloud Foundry app, you create an alias, which is a service instance, that counts toward your quota. See [What is an alias?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

### What happens when my free trial ends?
{: #trialend}

When your free trial expires 30 days after you sign up, the apps in your account are stopped. You can't sign up for another {{site.data.keyword.Bluemix_notm}} account, but you can still access your account and any accounts that you are invited to.

To restart your apps, convert your account to a billable account by either providing your credit card information for a Pay-As-You-Go account or creating a Subscription account. You can then continue to use free compute and service allowances. You pay only for the usage of services, containers, and runtimes that's not included in your free monthly allowance.

  * To upgrade to a Pay-As-You-Go account, go to **Manage** > **Billing and Usage** > **Billing** in the console, and click **Add Credit Card**.
  * To sign up for a Subscription account, contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg).

If you don't convert your account after your free trial expires, your apps and services are removed after 30 days. However, your account is not deleted and you can log in and upgrade to a billable account at any time. Also, you receive email notifications to remind you to create a billable account and avoid losing your app settings and service configurations. If you prefer not to receive notifications from {{site.data.keyword.Bluemix_notm}}, you can unsubscribe at any time.

If you convert your account, your free allowances are limited to allowances normally provided by each service. The allowances are no longer unlimited use allowances that are offered by many of the IBM services during the free trial.

