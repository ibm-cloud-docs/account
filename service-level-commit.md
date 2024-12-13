---

copyright:
  years: 2024
lastupdated: "2024-12-13"

keywords: IBM Cloud billing, commitment model, using commitments, pay as you go with committed use, enterprise savings plan

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Managing service commitments
{: #service-comit}

Service commitments include a service or bundle of services, a term, discount, and total commitment amount. You might also have a monthly or yearly minimum spend if applicable. A term might be multiple months or years. For example, you might have a commitment with the following provisions:
- 3-year term
- 30% discount on {{site.data.keyword.powerSys_notm}}
- $360,000 total commitment
- $1,000 committed usage per month

Depending on the service, your commitment might be in terms of dollars or metric units.

| Commitment    | Description | Overage                | Example |
|---------------|-------------|------------------------|---------|
| **Dollars**   | You commit to a certain amount of usage in a dollar amount. | Any usage that surpasses your monthly committed dollar amount is charged at the same committed rate. | You commit to $5,000/month of {{site.data.keyword.powerSysFull}} Private Cloud usage for 3 years. If you spend more than $5,000 on {{site.data.keyword.powerSysFull}} usage, the extra usage is charged at the same rate. If your total usage adds up to only $3,000, you are still charged the committed amount of $5,000. |
| **Metric units**  | You commit to pay for a certain amount of usage in units, like storage capacity, compute hours, or licenses. | Any usage that surpasses the committed capacity is counted as overage and might be charged at a different rate. | You commit to 50 TB/hour of storage for 6 months. For one hour of the month, you use 100 TB of storage. The extra 50 TB is charged as overage, which might be a different rate than the first 50 TB. Each month, you are charged the amount for your committed capacity plus any overage. |
{: caption="Comparing service commitments that are based in dollars and metric units." caption-side="top"}

## Before you begin
{: #before-service-commit}

- You can have commitments for services that are deployed on-premises in a stand-alone account or an enterprise account.
- With a service commitment at the enterprise level, usage from child accounts contributes to your committed spend.
- A service commitment cannot be shared across multiple stand-alone accounts.
- The discount that you receive with a service commitment does not combine with other discounts, such as account-level discounts from an Enterprise Savings Plan or a platform Subscription. Your usage counts toward only one commitment at a time, and a service commitment supersedes an account-level discount.

## Signing up for a commitment
{: #signup-slc}

Most account types can order a service commitment. Work with [{{site.data.keyword.Bluemix_notm}} Cloud Sales](https://www.ibm.com/cloud?contactmodule){: external} to create a commitment quote based on your hardware, software, or service needs and the spending amount for the period that you want to commit to.

You can have multiple commitments for different services active at the same time.
{: note}

When the contract term ends, service commitments are automatically converted to Pay-As-You-Go and you're charged on-demand pricing for those services.

### Purchasing services deployed on-premises
{: #slc-on-prem}

Hybrid cloud services that can be deployed on-premises, like {{site.data.keyword.powerSysFull}} Private Cloud, often require a service commitment to order and deploy hardware at your site. With this commitment, you receive a discount on the standard metered rates for the service or bundle of services that you select.

Your on-premises usage data is sent to {{site.data.keyword.Bluemix_notm}} when your service commitment is activated, which allows you to monitor hardware usage alongside your cloud-based usage. Gain a complete view of your resource usage trends across both on-premises and cloud environments to help you make informed decisions.

Workloads that you deploy to your on-premises or edge environment are enabled through {{site.data.keyword.satellitelong}}. For more information, see [Getting started with {{site.data.keyword.satellitelong}}](/docs/satellite?topic=satellite-getting-started).

#### Ordering managed hardware
{: #ordering-slc}

Managed hardware is physical hardware like servers, storage, and networking equipment, which {{site.data.keyword.IBM_notm}} provides and maintains based on the capacity and performance requirements in your order. To order your on-premises private cloud service, discuss your requirements with [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external} or your IBM Business Partner.

After you accept the commitment quote and sign the commitment contract, you receive an email to confirm that your payment information is processed, that the commitment is added to your account, and your hardware order is placed. Your commitment start date begins when the hardware is delivered and set up in your data center. When the hardware is deployed, the commitment is active and you can begin monitoring your hardware usage, service charges, and any additional costs within the {{site.data.keyword.Bluemix_notm}} console.

Learn about the shared responsibilities for using {{site.data.keyword.cloud_notm}} products by reviewing [IBM Hybrid Cloud](/docs/overview?topic=overview-shared-responsibilities#hybrid-responsibilities).

## Committed spending
{: #spending-min-slc}

Multi-year commitments might be broken up into year-long terms. All commitments have a monthly committed spending amount. If your usage doesn't meet the monthly or yearly committed amount, you are charged up to the remaining committed amount. To view how your commitment is progressing, go to the Service commitments page and click a commitment. Here you can view a detailed breakdown of your spending.

Set a spending notification to make sure that your usage is on track to fulfill your commitment. For more information, see [Setting spending notifications](/docs/account?topic=account-spending).
{: tip}

## Viewing your commitment usage
{: #slc-services}

To view your service commitment usage, go to **Manage > Billing and usage > Commitments** and click **Service commitments**. To access this information, you need an access policy with the viewer role or higher on the billing account management service.

For more details, download your usage report by [Exporting your account usage details to a CSV file](/docs/account?topic=account-viewingusage&interface=ui#export-csv) or [Exporting your enterprise usage details to a .csv file](/docs/enterprise-management?topic=enterprise-management-enterprise-usage&interface=ui#export-enterprise-csv).

In the usage report, **Credit Pool Type** and **Category** help you identify a service commitment.

| Credit Pool Type | Category               | Commitment |
|-------------------|------------------------|------------|
| `PLATFORM`       | `SERVICE_SUBSCRIPTION` | Service commitment |
{: caption="Identify a service commitment in your usage .csv" caption-side="top"}

To view usage for an on-premises resource, like {{site.data.keyword.powerSys_notm}} Private Cloud, complete the following steps:
1. Go to the **Pricing region** column and filter to the {{site.data.keyword.satelliteshort}} location associated with your pod.
1. Go to the **Service name** column and filter to {{site.data.keyword.powerSys_notm}}. The sum of the **Cost** column gives you this month's usage toward a service commitment, which matches the value in the **Used credits** column.

To map commitment usage in your enterprise back to child accounts, complete the following steps:
1. Go to the **Entity ID** column and filter on an account ID.
1. Go to the **Cost** column. The sum of the **Cost** column gives you this month's usage toward a service commitment in a specific account.

## Getting support
{: #support-slc}

You can get Advanced or Premium support with your service commitment. The level of support that you select determines the severity that you can assign to support cases and your level of access to the tools available in the Support Center. To get support, contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external}.

For more information about {{site.data.keyword.Bluemix_notm}} support plans, see [Basic, Advanced, and Premium Support plans](/docs/account?topic=account-support-plans).
