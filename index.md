---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-15"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account, subscription, service bundle

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:row-headers: .row-headers}

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
{: row-headers}
{: class="comparison-table"}
{: caption="Table 1. Comparison of {{site.data.keyword.Bluemix_notm}} accounts" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the feature. The column headers identify the account type. To understand which features apply to the account types, navigate to the row, and find the feature that you're interested in."}

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
   * Your Cloud Foundry apps can access up to 256 MB of free, instantaneous runtime memory per month.
   * You can provision one instance of any service in the [{{site.data.keyword.Bluemix_notm}} catalog ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} that has a Lite plan.
   * After 10 days of no development activity, your apps go to sleep. You can wake up your apps by continuing to work on them.
   * After 30 days of no development activity, your service instances with Lite plans are deleted.

## Pay-As-You-Go account
{: #paygo}

With a Pay-As-You-Go account, you can access the full {{site.data.keyword.Bluemix_notm}} catalog, including all free plans, and you get double the free runtime memory at 512 MB per month. You'll pay only for billable services that you use, with no long-term contracts or commitments.

You can create multiple resource groups to easily manage quota and view billing usage for a set of resources. Your charges are based on your use of {{site.data.keyword.Bluemix_notm}} computing and services. If you use more than the free runtime and service allowances, you receive a monthly invoice that provides details about your resource charges.

Also, with a Pay-As-You-Go account, you can order advanced or premium support plans to get extra help with your production workloads. Learn more in [Support plans](/docs/get-support?topic=get-support-support-plans).

## Subscription account
{: #subscription-account}

With a Subscription account, you can create multiple resource groups to easily manage quota and view billing usage for a set of resources. You commit to a minimum spending amount each month and receive a subscription discount that is applied to that minimum charge.

For example, if you commit to spend $100 a month for 6 months, you can get a 10% discount. During the subscription term, you get $600 of usage but pay only $540 for it. The longer the subscription term, the better the discount.

Your usage is deducted from your total subscription amount. Even if your usage varies from month to month, you get predictable, consistent billing. If your usage exceeds your total subscription amount, you're charged the non-discounted rate for the overage.

As with Pay-As-You-Go accounts, your Subscription account enables you to order advanced or premium support plans to get extra help if you need it. Learn more in [Support plans](/docs/get-support?topic=get-support-support-plans).

If you have a Subscription account, you can create most of the services that are available from the [{{site.data.keyword.Bluemix_notm}} catalog](https://{DomainName}/catalog){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon"). However, some services use a specific pricing plan that requires you to purchase it separately.

### Service bundle subscriptions
{: #service-subscriptions}

Service bundle subscriptions give you access and credit towards a set of services within a particular domain that are targeted for popular use cases. You can choose from service bundles that span AI, analytics, {{site.data.keyword.blockchainfull_notm}}, Internet of Things (IoT), and cloud-native services. If your needs cross multiple domains, you can purchase multiple service bundle subscriptions.

You can add services bundles to any type of existing account, including Lite accounts. For the first 90 days, you're limited to using the services within the bundle. After the initial 90 days, you can access the full catalog. Service bundle subscriptions are subject to the [{{site.data.keyword.Bluemix_notm}} Service Description](/docs/overview/terms-of-use?topic=overview-terms) terms.

Service bundle subscriptions aren't available through the {{site.data.keyword.Bluemix_notm}} console. To learn more and purchase a service bundle, contact [{{site.data.keyword.Bluemix_notm}} Sales ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}.
{:tip}

After you purchase a service bundle subscription, you'll receive an email with a subscription code that you apply to add the bundle to your account. For more information about how to apply subscription codes, see [Managing subscriptions](/docs/billing-usage?topic=billing-usage-subscriptions). When your service bundle expires or you use all of the credit, you can continue to use any of the services, with usage charged at the Pay-As-You Go rate.

## Upgrading your account
{: #upgrade-lite-account}

When you're ready to take your account to the next level, you can [upgrade your Lite account](/docs/account?topic=account-upgrading-account) to a Pay-As-You-Go account or Subscription account. Upgrading your account unlocks the full {{site.data.keyword.Bluemix_notm}} catalog, gives you extra free resources, and more.

After you upgrade your Lite account to a Pay-As-You-Go account, you get a promotional credit of $200 that is automatically applied to your account. Your $200 credit is valid for 30 days, and your usage is automatically deducted from the credit amount. The credit cannot be used with third-party offerings, and the credit might not be available for all accounts.

If you already have a Pay-As-You-Go or Subscription account, you can also convert your account to a different type. For more information, see [Upgrading your account](/docs/account?topic=account-upgrading-account).
