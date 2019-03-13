---

copyright:
  years: 2015, 2019
lastupdated: "2019-03-13"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account, subscription, service bundle

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Account types
{: #accounts}

{{site.data.keyword.Bluemix_notm}} has three different account types: Lite, Pay-As-You-Go, and Subscription. You get a free Lite account as soon as you sign up. Pay-As-You-Go and Subscription are our billable account options, each offering different features. Compare each account and choose the one that best suits your needs.
{:shortdesc}


## Comparing accounts
{: #compare}

The following table provides a comparison of Lite, Pay-As-You-Go, and Subscription accounts. For more details about each account, see the sections that follow.

|                                         | Lite               | Pay-As-You-Go      | Subscription       |
|-----------------------------------------|--------------------|--------------------|--------------------|
| **Access to free Cloud Foundry memory** | 256 MB             | 512 MB             | 512 MB             |
| **Access to [Lite service plans ![External link icon](../icons/launch-glyph.svg "External link icon")](https://{DomainName}/catalog/?search=label:lite){: new_window}** | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Access to all free plans**            |                    | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Access to the full {{site.data.keyword.Bluemix_notm}} catalog** |  | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Access to multiple Cloud Foundry regions** |               | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **No time restrictions** | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| **Guaranteed zero cost**                | ![Feature available](../icons/icon_enabled.svg) |  |         |
| **Discounted pricing**                  |                    |                    | ![Feature available](../icons/icon_enabled.svg) |
| **Best for learning or building proof of concepts** | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |  |
| **Fit for production use cases**        |                    | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
{: caption="Table 1. Comparison of {{site.data.keyword.Bluemix_notm}} accounts" caption-side="top"}


## Lite account
{: #liteaccount}

Sign up for a Lite account to start building your apps and exploring services with select free Lite plans, which are displayed with a Lite tag ![Lite tag](../icons/Lite.svg) in the {{site.data.keyword.Bluemix_notm}} console. Your Lite account doesn't expire and your credit card isn't required.

You have access to a single resource group that's created for you and named `Default`. All of your service's instances that are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) are automatically added to this resource group. You can update the name of this resource group at any time. See [Renaming a resource group](/docs/resources?topic=resources-rgs#rename_rgs) for the detailed steps.

Each resource group is free. When you create a connection between a service that is managed by IAM and a Cloud Foundry app, you create an alias, which is a service instance, that counts toward your quota. See [Managing connections](/docs/resources?topic=resources-connect_app).
{: tip}

### What's available?
{: #lite-account-features}

Check out the following list of key features that are available in a Lite account:

   * The account is free - no credit card required.
   * The account never expires.
   * You can use one org in one {{site.data.keyword.Bluemix_notm}} region.
   * Basic {{site.data.keyword.Bluemix_notm}} support for free. Basic support is provided for non-production environments or workloads where traditional severities are not used and specific response times are not stipulated.
   * You receive email notifications about your account status and quota limits.
   * Your Cloud Foundry apps can access up to 256 MB of free, instantaneous runtime memory.
   * You can provision one instance of any service in the [{{site.data.keyword.Bluemix_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} that has a Lite plan.
   * After 10 days of no development activity, your apps go to sleep. You can wake up your apps by continuing to work on them.
   * After 30 days of no development activity, your service instances with Lite plans are deleted.

### Upgrading your Lite account
{: #upgrade-lite-account}

You can upgrade to a Pay-As-You-Go account or Subscription account. For more information, see [How do I upgrade or convert my account type?](/docs/account?topic=account-changeacct).

You get a promotional credit of $200 after you upgrade to a Pay-As-You-Go account, and the credit is automatically applied to your account. Your $200 credit is valid for 30 days and is automatically applied to your invoice. The credit cannot be used with third-party offerings.

## Pay-As-You-Go account
{: #paygo}

With a Pay-As-You-Go account, you can create multiple resource groups to easily manage quota and view billing usage for a set of resources. Your charges are based on your use of {{site.data.keyword.Bluemix_notm}} computing and services. You're eligible for free runtime and service allowances. If you use more than the free allowance, you receive a monthly {{site.data.keyword.Bluemix_notm}} invoice. The invoice is in United States dollars (USD) and provides details about your resource charges.

Also, with a Pay-As-You-Go account, you can order optional items such as advanced or premium support options. Contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) for more information.


### Upgrading your Pay-As-You-Go account
{: #upgrade-to-subscription}

To upgrade your Pay-As-You-Go account to a Subscription account, contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon").

## Subscription account
{: #subscription-account}

With a Subscription account, you can create multiple resource groups to easily manage quota and view billing usage for a set of resources. You commit to a combined a minimum spending amount each month and receive a subscription discount that is applied to that minimum charge. You're charged the non-discounted rate for any usage that exceeds your total subscription amount. To view your subscription, go to **Manage > Billing and usage**, and select **Subscriptions**.

If you have a subscription account, you can create most of the services that are available from the [{{site.data.keyword.Bluemix_notm}} catalog](https://cloud.ibm.com/catalog/){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon"). However, some services use a specific pricing plan that requires you to purchase it separately.

### Service bundle subscriptions
{: #service-bundles}

Service bundle subscriptions give you access and credit towards a set of services within a particular domain that are targeted for popular use cases. You can choose from service bundles that span AI, analytics, {{site.data.keyword.blockchainfull_notm}}, Internet of Things (IoT), and cloud-native services. If your needs cross multiple domains, you can purchase multiple service bundle subscriptions.

You can add services bundles to any type of existing account, including Lite accounts. For the first 90 days, you're limited to using the services within the bundle. After the initial 90 days, you can access the full catalog.

Service bundle subscriptions aren't available through the {{site.data.keyword.Bluemix_notm}} console. To learn more and purchase a service bundle, contact [{{site.data.keyword.Bluemix_notm}} Sales ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}.
{:tip}

After you purchase a service bundle subscription, you'll receive an email with a feature code that you apply to add the bundle to your account. For more information about how to apply feature codes, see [Applying feature codes](/docs/account?topic=account-codes). When your service bundle expires or you use all of the credit, you can continue to use any of the services, with usage charged at the Pay-As-You Go rate.


### {{site.data.keyword.Bluemix_dedicated_notm}} account
With {{site.data.keyword.Bluemix_dedicated_notm}}, you must sign up for a one year minimum term that includes:

   * VPN connectivity back to your infrastructure
   * Fully redundant environment in a {{site.data.keyword.BluSoftlayer_notm}} data center
   * All supported runtimes ({{site.data.keyword.runtime_liberty_short}}, {{site.data.keyword.runtime_nodejs_short}}, and built-in open source runtimes)
   * All dedicated services that you selected and all public {{site.data.keyword.Bluemix_notm}} services
   * Standard {{site.data.keyword.Bluemix_notm}} support

You can also order optional items such as {{site.data.keyword.BluDirectLink}} or advanced or premium support options. Contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) for more information.

What you pay each month during that term is based on the dedicated services that you want, plus a Subscription account that gives you access to all public services. Usage charges of the services in {{site.data.keyword.Bluemix_notm}} Public are calculated based on your Subscription account agreement. You receive an invoice for any services that you use beyond that subscription agreement. Contact your IBM designated account representative or [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) to get started on your agreement.
