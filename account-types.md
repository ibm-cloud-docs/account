---

copyright:

  years: 2015, 2018
lastupdated: "2017-11-29"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Account types
{: #accounts}

You can start building on {{site.data.keyword.Bluemix}} for free. When you are ready to grow, upgrade and pay only for what you use beyond free allowances. We have four different account types that you can choose from: Lite, Pay-As-You-Go, Subscription, and Promo. You can use any of the account types to get started in {{site.data.keyword.Bluemix_notm}} - simply choose the one that best suits your needs. 
{:shortdesc}

## Account comparison
{: #compare}

The following table provides a comparison of Lite, Pay-As-You-Go, and Subscription accounts. For more details about each account, see the sections that follow.

|  | Lite  | Pay-As-You-Go | Subscription | 
|--------------------|--------------------|--------------------|--------------------|
| **Access to free Cloud Foundry memory** | 256 MB | 512 MB | 512 MB | 
| **Access to [Lite service plans ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window}** | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Access to all free plans** |  | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Access to the full catalog** |  | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **No time restrictions** | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Guaranteed zero cost** | ![Feature available](../icons/icon_enabled.svg) |  |  |
| **Negotiated pricing** |  |  | ![Feature available](../icons/icon_enabled.svg) | 
| **Best for learning or building POCs** | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |  | 
| **Fit for production use cases** |  | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) | 
{: caption="Table 1. Comparison of {{site.data.keyword.Bluemix_notm}} accounts" caption-side="top"}

## Lite account
{: #liteaccount}

Sign up for a free Lite account to build apps and explore services with select free plans that are named Lite and displayed with a Lite tag ![Lite tag](../icons/Lite.svg) in the {{site.data.keyword.Bluemix_notm}} console. Your Lite account doesn't expire and your credit card isn't required. 

You have access to a single resource group that's created for you and named `Default`. All of your services instances that are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) are automatically added to this resource group. You can update the name of this resource group at any time. See [Renaming a resource group](/docs/admin/resourcegroups.html#renaming-a-resource-group) for the detailed steps. 

Each resource group is free. When you create a connection between a service managed by IAM and a Cloud Foundry app, you create an alias, which is a service instance, that counts toward your quota. See [What is an alias?](/docs/manageapps/connecting_apps.html#what_is_alias).
{: tip}

### What's available?

You might be wondering what's offered in a Lite account. Check out the following list of key features:

   * The account is free - no credit card required.
   * The account never expires.
   * You can use one org in one {{site.data.keyword.Bluemix_notm}} region.
   * Free {{site.data.keyword.Bluemix_notm}} support.
   * You receive email notifications about your account status and quota limits.
   * Your Cloud Foundry apps can access up to 256 MB of free, instantaneous runtime memory. 
   * You can work with a Kubernetes cluster with 2 CPU and 4 GB RAM.
   * You can provision one instance of any service in the [{{site.data.keyword.Bluemix_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window} that has a Lite plan.
   * After 10 days of no development activity, your apps go to sleep. You can start working on new apps without having to worry about hitting memory quota limits.
   * After 30 days of no development activity, your service instances with Lite plans are deleted. This way, you don't have to manage deleting inactive instances before you create new ones.

## Billable accounts
{: #billableacts}

When you sign up for a {{site.data.keyword.Bluemix_notm}} billable plan or request an upgrade to your account, you can select from four different {{site.data.keyword.Bluemix_notm}} accounts. The following table lists the different account types and their charging methods.

|Account type |	How am I charged? |
|------------------|-----------------------|
|Pay-As-You-Go |	Charges are based on your use of {{site.data.keyword.Bluemix_notm}} compute and services |
|Subscription | You can get a monthly discount based on a minimum monthly spending commitment |
| {{site.data.keyword.Bluemix_dedicated_notm}} | Annual contract |
|{{site.data.keyword.Bluemix_local_notm}} |	Annual contract |
{:caption="Table 2. {{site.data.keyword.Bluemix_notm}} billable accounts and charges" caption-side="top"}

If you link your {{site.data.keyword.Bluemix_notm}} billable account with a SoftLayer account, starting on the first of the next month, your combined charges are included on your {{site.data.keyword.Bluemix_notm}} invoice. For more information, see [Viewing credits](/docs/pricing/viewing_usage.html#credits).
{: tip}

### Pay-As-You-Go account

With a Pay-As-You-Go account, you can create multiple resource groups to easily manage quota and view billing usage for a set of resources.

You're eligible for free runtime and service allowances. If you use more than the free allowance, you'll receive a monthly {{site.data.keyword.Bluemix_notm}} invoice. The invoice will be in United States dollars (USD) and will detail your resource charges. 

In many countries and regions, you can sign up for a Pay-As-You-Go account from the {{site.data.keyword.Bluemix_notm}} console. After you provide your billing and credit card information, accept the terms and conditions, and submit your account request. Then, your credit card will be validated. A confirmation email of the account information is also sent. A few minutes after you receive the confirmation email, you can return to the console to continue building your apps.

If your online request can't be processed for your country or region, contact {{site.data.keyword.Bluemix_notm}} Sales by using the link listed on the
[{{site.data.keyword.Bluemix_notm}} Support ![External link icon](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} page.

You can convert your Pay-As-You-Go account to a Subscription account at any time. Contact {{site.data.keyword.Bluemix_notm}} Sales by using the link listed on the
[{{site.data.keyword.Bluemix_notm}} Support ![External link icon](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} page.

### Subscription account

With a Subscription account, you can create multiple resource groups to easily manage quota and view billing usage for a set of resources.

You commit to a minimum spending amount each month and receive a subscription discount that is applied to that minimum charge. You also pay for any usage that exceeds the minimum spending amount.

To sign up for a Subscription account, and for more information about subscription rates and discounts, you must contact {{site.data.keyword.Bluemix_notm}} Sales by using the link listed on the [{{site.data.keyword.Bluemix_notm}} Support ![External link icon](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} page.

### {{site.data.keyword.Bluemix_dedicated_notm}} account

With {{site.data.keyword.Bluemix_dedicated_notm}}, you must sign up for a one year minimum term that includes:

   * VPN connectivity back to your infrastructure
   * Fully redundant environment in a {{site.data.keyword.BluSoftLayer_notm}} data center
   * All supported runtimes (IBM Java Liberty, Node.js, and built-in open source runtimes)
   * All dedicated services that you have selected and all public {{site.data.keyword.Bluemix_notm}} services
   * Standard {{site.data.keyword.Bluemix_notm}} support

You can also order optional items such as SoftLayer DirectLink or premium support options. Contact [{{site.data.keyword.Bluemix_notm}} Sales ![External link icon](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} for more information.

What you pay each month during that term is based on the dedicated services that you want, plus a Subscription account that gives you access to all public services. Usage charges of the services in {{site.data.keyword.Bluemix_notm}} Public are calculated based on your Subscription account agreement. You receive an invoice for any services that you use beyond that subscription agreement. Contact your IBM designated account representative or contact [{{site.data.keyword.Bluemix_notm}} Sales ![External link icon](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} to get started on your agreement.

### {{site.data.keyword.Bluemix_local_notm}} account

With {{site.data.keyword.Bluemix_local_notm}}, you must sign up for a one year minimum term that includes:

   * A delivery capability called relay that enables IBM to connect to your local deployment and automatically and consistently deliver updates
   * All supported runtimes (IBM Java Liberty, Node.js, and built-in open source runtimes)
   * All local services that you have selected and access to all public {{site.data.keyword.Bluemix_notm}} services
   * Standard {{site.data.keyword.Bluemix_notm}} support

What you pay each month during that term is based on the local services that you want, plus a Subscription account that gives you access to all public services. Usage charges of the services in {{site.data.keyword.Bluemix_notm}} Public are calculated based on your Subscription account agreement. You receive an invoice for any services that you use beyond that subscription agreement. Contact your IBM designated account representative or contact [{{site.data.keyword.Bluemix_notm}} Sales ![External link icon](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} to get started on your agreement.

## Promo account
{: #promo}

Promo accounts, occasionally offered as part of special promotions, are free timeboxed trials with access to most of the {{site.data.keyword.Bluemix_notm}} catalog. This account type is available through the use of a promo code only. The time period of validity for the account varies by promotion. 
   
With a Promo account, you have access to a single resource group that's created for you and named `Default`. All of your IAM-managed service instances are automatically added to this resource group. You can update the name of this resource group at any time. See [Renaming a resource group](/docs/admin/resource-groups.html#renaming-a-resource-group) for the detailed steps. 

Each resource group is free. When you create a connection between a service managed by IAM and a Cloud Foundry app, you create an alias, which is a service instance, that counts toward your quota. See [What is an alias?](/docs/manageapps/connecting_apps.html#what_is_alias).
{: tip}

### What happens when my Promo account expires?
{: #trialend}

When your Promo account expires, the apps in your account are stopped. You can't sign up for another {{site.data.keyword.Bluemix_notm}} account, but you can still access your account and any accounts that you are invited to.

To restart your apps, convert your account to a billable account by either providing your credit card information for a Pay-As-You-Go account or creating a Subscription account. You can then continue to use free compute and service allowances. You pay only for the usage of services, containers, and runtimes that's not included in your free monthly allowance.

If you don't convert your account after your Promo account expires, your apps and services are removed after 30 days. However, your account is not deleted and you can log in and upgrade to a billable account at any time. Also, you receive email notifications to remind you to create a billable account and avoid losing your app settings and service configurations. If you prefer not to receive notifications from {{site.data.keyword.Bluemix_notm}}, you can unsubscribe at any time.

If you convert your account, your free allowances are limited to allowances normally provided by each service. The allowances are no longer unlimited use allowances that are offered by many of the IBM services during the free trial.
