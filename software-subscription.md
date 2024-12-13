---

copyright:
  years: 2024
lastupdated: "2024-12-13"

keywords: IBM Cloud billing, software subscription, SaaS subscription

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Managing SaaS subscriptions
{: #software-subscription}

You must have a paid account type for your SaaS subscription: Subscription, Pay-As-You-Go, or Enterprise Saving Plan. For more information, see [Account types](/docs/account?topic=account-accounts).
{: shortdesc}

To view your account type, go to **Manage > Account**, and select **Account settings** in the {{site.data.keyword.Bluemix_notm}} console. Details about your account type are listed in the Account Type section.
{: tip}

Work with an [{{site.data.keyword.Bluemix_notm}} Cloud Sales](https://www.ibm.com/cloud?contactmodule){: external} representative to create a quote based on your software needs and the spending amount for the period that you want to subscribe.

## Before you begin
{: #before-software}

- You can have multiple SaaS subscriptions for different services active at the same time.
- You cannot have SaaS subscriptions for {{site.data.keyword.IBM_notm}} Partner Programs accounts or root enterprise accounts.
- You can apply a SaaS subscription to a child account in an enterprise.
- Make sure that the country and currency on your account matches the country and currency in your SaaS subscription order. To check your country and currency, export your CSV usage report and look in the Country Code and Currency Code headers. For more information, see [Understanding your account summary report](/docs/account?topic=account-exporting-your-usage&interface=ui#account-summary-csv-version-1-2).

## Adding your SaaS subscription to an account
{: #slc-software}

After you purchase a SaaS subscription, you receive an email to add the subscription to your account.

If you don't have a paid account when you receive an email with the subject `Action required: Add your SaaS subscription to an account`, you might need to:
- Create an account by contacting an [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external} representative.
- Upgrade to a paid account by contacting an [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external} representative.
- Activate your platform subscription, which converts your account to a paid Subscription account. To activate a platform subscription, look for an email with the subject `Action required: Add your platform subscription to an account` and follow the instructions in the email.

To add your SaaS subscription to an account, complete the following steps:
1. Open the email with the subject `Action required: Add your SaaS subscription to an account` and click **Add subscription**.
1. Select the account where you want to assign the subscription.
1. Select a resource group.
1. Review your selections.
1. Click **Assign** and continue.

## Managing your software instances
{: #sofware-instance}

After you add your SaaS subscription to an account, you can view it in your resource list. From there, you can create resource instances.

1. From the {{site.data.keyword.cloud_notm}} console, click the Navigation Menu icon  ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list** to view your list of resources.
1. Click the name of the subscription instance to view details.

   The subscription instance has a `Global` location. The software instances that you create can have a regional location.
   {: note}

1. Click **Instances > Create resource**. Location and Plan are selected for you based on your subscription.

   If you create an instance from the catalog, you must select the plan that corresponds with your SaaS subscription. The subscription ID populates when you click the correct corresponding plan.
   {: exception}

1. Configure the resource. For example, select a resource group or [add user tags](/docs/account?topic=account-tag&interface=ui#tag-types) to organize, track, and manage costs for related resources. The resource group that you select can be different than the resource group that you selected for the subscription itself.
1. Click **I agree > Create**.
1. View the resource in the resource list.

## Viewing your SaaS subscription billing
{: #software-sub-cost}

To view your SaaS subscription, go to the [Service commitments](/billing/service-commits){: external} page.

To view and pay your SaaS subscription bill, check your email for an email from {{site.data.keyword.IBM}} or contact your [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external} representative.

SaaS subscriptions are not included in your usage reports.
{: note}
