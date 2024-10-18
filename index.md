---

copyright:
  years: 2015, 2024
lastupdated: "2024-09-19"

keywords: account types, Lite, paid account, buy account, account difference, compare account, subscription, savings plan, enterprise savings plan

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Account types
{: #accounts}

When you register with {{site.data.keyword.cloud}}, you are set up with a Pay-As-You-Go account. Even though you provide your credit card information for account security and identity verification purposes, you can still use {{site.data.keyword.cloud_notm}} for free by selecting products in the catalog that offer Free and Lite pricing plans. Another account type, called a Subscription account, is also available. With a Subscription account, you get many of the same features of a Pay-As-You-Go account, plus discounts for platform services and support with a more consistent billing structure that uses subscriptions.
{: shortdesc}

By default, classic accounts that were established before 30 November 2023, are included in the {{site.data.keyword.cloud_notm}} general routing table. Previously, if you wanted to convert a classic account to a VRF-style account, you were required to open a support case with {{site.data.keyword.IBM}} Support. Beginning 30 November 2023, any new classic account or any existing classic account that is "empty" (for example, without any provisioned VLANs), will be automatically converted to a VRF-style account the next time that account initiates a private network connection. For more information, see [FAQs about VRF account migration](/docs/account?topic=account-vrf-faqs).
{: attention}

## Comparing accounts
{: #compare}

The following table provides a comparison of Trial, Pay-As-You-Go, and Subscription accounts. For more details about each account, see the sections that follow.

| Feature | Trial              | Pay-As-You-Go      | Subscription       |
|-----------------------------------------|--------------------|--------------------|--------------------|
| Access to [Lite service plans](/catalog?search=label%3Alite){: external} | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| Access to all Free plans           | ![Feature available](../icons/icon_enabled.svg) |   ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| Access to the full {{site.data.keyword.cloud_notm}} catalog |        | ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg) |
| Fit for production use cases      |        |     ![Feature available](../icons/icon_enabled.svg) | ![Feature available](../icons/icon_enabled.svg)|
| Available for enterprise account hierarchy        |        |    ![Feature available](../icons/icon_enabled.svg) [^tabletext]   | ![Feature available](../icons/icon_enabled.svg) |
| Invoiced on monthly consumption       |        |     ![Feature available](../icons/icon_enabled.svg) |                     |
{: row-headers}
{: class="comparison-table"}
{: caption="Comparison of {{site.data.keyword.cloud_notm}} accounts" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the feature. The column headers identify the account type. To understand which features apply to the account types, navigate to the row, and find the feature that you're interested in."}

[^tabletext]: Pay-As-You-Go accounts that sign up with a credit card on cloud.ibm.com can create an enterprise. Pay-As-You-Go accounts that sign up through IBM Cloud Sales or Softlayer can't create an enterprise.

## Trial account
{: #trial}

Trial accounts offer timed access to a limited range of service plans and allow you to test out the platform without a financial commitment. You can access Lite service plans and Free plans for a limited time with a trial account. To qualify for a trial account, go to [Harness the Power of IBM](https://ibm.biz/academic){: external} and validate your institution credentials or reach out to your educational program or course leader. If you don't have an account, select **Register with a Code** during {{site.data.keyword.cloud_notm}} registration to apply a code. If you have an account, go to the [Account settings](/account/settings) page in the console to apply the code.

If you upgrade your trial account to a Pay-As-You-Go account by entering a credit card, it can't be converted back to a trial account. {{site.data.keyword.cloud_notm}} trial accounts are available for faculty and students at accredited academic institutions. Trial accounts expire after 30 days. Your account is deactivated when the trial period ends. To reactivate your account, log in to your account and upgrade it to a Pay-As-You-Go account.

If you import a trial account into an enterprise, it's automatically upgraded to a [Pay-As-You-Go account](/docs/account?topic=account-accounts).
{: note}

Support for a trial account is limited to nontechnical support issues that are related to account access and billing. Users with trial accounts can view the [{{site.data.keyword.cloud_notm}} documentation](/docs/account?topic=account-using-avatar), Chat with Watson, and use [Stack Overflow](https://stackoverflow.com/questions/tagged/ibm-cloud){: external}.

## Pay-As-You-Go account
{: #paygo}

With a Pay-As-You-Go account, you can access the full {{site.data.keyword.cloud_notm}} catalog, including all Free and Lite plans. You pay only for billable services that you use and monthly commitments, with no long-term contracts or commitments. When you register with {{site.data.keyword.cloud_notm}}, you get a Pay-As-You-Go account, and you receive a [$200 credit](/docs/account?topic=account-upgrading-account) to help get you started. You can use the $200 credit on {{site.data.keyword.cloud_notm}} products.

Your resource usage consists of recurring and fluctuating costs. If you purchase classic infrastructure services, you're billed on an hourly or monthly recurring basis in advance of use, like a rent bill. If you purchase platform services, your invoice fluctuates as your resource usage fluctuates, similar to a utility bill. You will receive invoices for recurring resources in your account until you cancel them. Turning a resource "off" does not cancel the resource in your account. See [Cancelling your billing items](/docs/account?topic=account-cancel-billing-items) for more information.

You can create multiple resource groups to easily manage quota and view billing usage for a set of resources. Your charges are based on your use of {{site.data.keyword.cloud_notm}} computing and services. If you use more than the free runtime and service allowances, you receive a monthly invoice that provides details about your resource charges. You can [set up spending notifications](/docs/account?topic=account-spending) to get notified when your account or a particular service reaches a specific spending threshold that you set.

Basic support is included with your {{site.data.keyword.cloud_notm}} Pay-As-You-Go. It is provided for nonproduction environments or workloads where traditional severities are not used and specific response times are not stipulated. Also, with a Pay-As-You-Go account, you can order Advanced or Premium support plans to get extra help with your production workloads. For more information, see [Basic, Advanced, and Premium Support plans](/docs/account?topic=account-support-plans).

## Subscription account
{: #subscription-account}

Subscription accounts offer many of the same benefits as Pay-As-You-Go accounts, including access to the full {{site.data.keyword.cloud_notm}} catalog and the ability to create multiple resource groups. In addition, Subscription accounts provide discounts for platform services and support and more consistent billing through subscriptions. You can also [set up spending notifications](/docs/account?topic=account-spending) to get notified when your account or a particular service reaches a specific spending threshold that you set.

When you purchase a subscription, you commit to a minimum spending amount for a certain period of time and receive a discount on the overall cost. For example, if you commit to spend $1,000 a month for 6 months, you might get a 5% discount. For the duration of the subscription, you get $6,000 of usage but pay only $5,700 for it. The larger the subscription, the better the discount.

Large organizations and other users with large cloud workloads can benefit from the savings and predictable billing that are provided by subscriptions. {{site.data.keyword.cloud_notm}} offers multiple types of subscriptions to fit your usage needs.

### Platform subscriptions
{: #platform-subscriptions}

When you purchase a subscription for the {{site.data.keyword.cloud_notm}} platform, you get discounted credit that pays for services and other resources that you create from the [{{site.data.keyword.cloud_notm}} catalog](/catalog){: external}.

Your resource usage is deducted from your total subscription amount. Even if your usage varies from month to month, you get predictable, consistent billing. If your usage exceeds your total subscription amount, you're charged the nondiscounted rate for the overage. For more information about tracking your subscription usage, see [Managing subscriptions](/docs/account?topic=account-subscriptions).

Your subscription applies to most services in the catalog. However, some services use a specific pricing plan that requires you to purchase it separately.

### Support subscriptions
{: #support-subscriptions}

Basic support is included with your Subscription account. If you want to enhance your support experience for production-critical resources, contact [{{site.data.keyword.cloud_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external} to purchase a support subscription for an Advanced or Premium support plan. With a support subscription, you commit to a monthly spending amount that goes toward your support costs.

Support subscription credit is separate from any platform or service subscription credit in your account and can't be spent on resource usage. For more information, see [How subscription credit is spent](/docs/account?topic=account-subscriptions#subscription-basics).

### Service bundle subscriptions
{: #service-subscriptions}

Service bundle subscriptions give you access and credit toward a set of services within a particular domain that are targeted for popular use cases. You can choose from service bundles that span AI, analytics, {{site.data.keyword.blockchainfull_notm}}, Internet of Things (IoT), and cloud-native services. If your needs cross multiple domains, you can purchase multiple service bundle subscriptions.

You can add services bundles to any type of existing account, including Lite accounts. Service bundle subscriptions are subject to the [{{site.data.keyword.cloud_notm}} Terms of Use](/docs/overview?topic=overview-terms).

Service bundle subscriptions aren't available through the {{site.data.keyword.cloud_notm}} console. To learn more and purchase a service bundle, contact [{{site.data.keyword.cloud_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external}.
{: tip}

After you purchase a service bundle subscription, you'll receive an email with a subscription code that you apply to add the bundle to your account. For more information about how to apply subscription codes, see [Subscription credit](/docs/account?topic=account-subscriptions#subscription-codes). When your service bundle expires or you use all of the credit, you can continue to use any of the services, with usage charged at the Pay-As-You Go rate.

### Expiring subscriptions
{: #expiring-subscription-account}

When your subscription is about to expire, you are notified by email 60, 30, 14, and 1 day before the expiration date of the last subscription on the account. After your subscription expires, your account is converted to a Pay-As-You-Go account, which means you pay only for billable services that you use with no contracts or commitments. In addition, the discounts that are associated with your subscription account won't apply to the Pay-As-You-Go account. Go to the [Subscriptions](/billing/subscriptions) page to check whether any of your subscriptions are approaching their expiration date.

You can work with [{{site.data.keyword.cloud_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external} to renew your subscription account.

## Lite account
{: #liteaccount}

If you created a Lite account before 25 October 2021, your account doesn't expire and you can work in {{site.data.keyword.cloud_notm}} for free by accessing services with select Lite plans, which are displayed with a **Lite** tag ![Lite tag](../icons/Lite.svg "Lite") in the catalog. To gain access to all Free plans, you can go ahead and [upgrade to a Pay-As-You-Go account](/docs/account?topic=account-accountfaqs#changeacct) by adding your credit card information.

Starting 25 October 2021, all new accounts are created as Pay-As-You-Go based on an update to our account registration process. As part of this update, you're asked to provide credit card information for identity verification. You have full access to the catalog, including all Free and Lite plans, and you get a $200 credit that you can apply in your first 30 days. You pay only for billable services that you use, with no long-term contracts or commitments.
{: note}

Lite accounts have access to a single resource group that is created for you with the name `Default`. All of your service's instances are automatically added to this resource group. You can update the name of this resource group at any time. See [Renaming a resource group](/docs/account?topic=account-rgs#rename_rgs) for the detailed steps.

### What's available in a lite account?
{: #lite-account-features}

Check out the following list of key features that are available in a Lite account:

* The account is free - no credit card required.
* The account never expires.
* You receive email notifications about your account status and quota limits.
* You can create one instance of any service in the [{{site.data.keyword.cloud_notm}} catalog](/catalog?search=label%3Alite){: external} that has a Lite plan.
* After 10 days of no development activity, your apps go to sleep. You can wake up your apps by continuing to work on them.
* After 30 days of no development activity, your service instances with Lite plans are deleted.

Only Lite accounts created before 12 August 2021 can use 186 GBH of free buildpacks per month.
{: note}
