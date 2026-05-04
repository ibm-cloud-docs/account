---

copyright:
  years: 2023, 2026
lastupdated: "2026-04-30"

keywords: apptio, cost benefit analysis

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Exporting your usage data for continual insights
{: #exporting-your-usage}

You can export your account's usage data to a Cloud Object Storage (COS) bucket for continual visibility, optimization, governance, and more across cloud environments. For example, if you are an account administrator and want to learn more about your account's usage and get cost optimization analysis, you can integrate your account with a third-party provider to gain insights about your accounts usage.
{: shortdesc}

When you set up your account to export usage report to an {{site.data.keyword.cos_full_notm}} bucket, you are enabling your account to continually export that data. To export data on a one time basis, see [Exporting your usage details to a CSV file](/docs/account?topic=account-viewingusage&interface=ui#export-csv).

To enable your account to share usage data, you need to grant permissions to the Billing service to access usage details and export it to a COS bucket. Because the report includes usage data for the entire account, child account usage and information about services and instances, the service ID used by the Billing service needs administrator access to export usage details. After this setup is complete, a CSV formatted cost and usage report is automatically exported to your COS bucket daily.

## Enabling your account to export usage data
{: #enable-export-usage}
{: ui}

Before you can enable your account to export usage data, you need to have Administrator or editor role on the Billing account management service. For more information, see [IAM access](/docs/iam?topic=iam-userroles).

When you enable your account to export usage data, the COS bucket can collect data from as far back as a year. So, if its June 2024, you can only view usage as early as June 2023, but you'll always be able to view data from that far back. Meaning that if you enabled this feature in June 2023, and it is now June 2024, you can view usage data from June 2022 to June 2024.
{: note}

To enable your account to export usage data, use the following steps:

1. From the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Billing and usage**, and select **Settings**.
1. Click **Connect**.
1. Select a Cloud Object Storage instance and Bucket. By selecting these, you are choosing which bucket will store your usage reports.
   1. Optional: If you don't want to select an existing instance, you can click **Select an instance** > **Create new**.
   1. Optional: You can select a bucket or create a new bucket by clicking **Create new bucket** in the Bucket dropdown. For more information about buckets, see [Getting started with IBM Cloud Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage). After you create your bucket
1. For service to service authorizations, click **Authorize**. For the required access, select **Object Writer** and **Content Reader**. Click **Review** and then **Assign**.
1. Click **Connect** after you review your folder details.

If you convert your account to an enterprise account, you need to follow these steps again to enable the enterprise account to export usage data. You can keep this feature on your original account or you can remove it by [disconnecting your account from sharing usage](/docs/account?topic=account-exporting-your-usage&interface=ui#disconnect-exporting-your-usage).
{: note}

## Requesting access to historical data
{: #access-historical-data}

When you enable your account to export usage data, the COS bucket, by default, collects data from the current month as provided by the automatic daily export from the Billing service, but it can contain data from as far back as a year if you request historical data. So, if its June 2024, you can only view usage as early as June 2023, but you'll always be able to view data from that far back. Meaning that if you enabled this feature in June 2023, and it is now June 2024, you can view usage data from June 2022 to June 2024. To get historical data, you need to create a support case.

To request access to historical data, use the following steps:

1. From the {{site.data.keyword.cloud_notm}} console menu bar, click the **Help** icon ![Help icon](../icons/help.svg "Help") > **Support center**.
1. From the Contact support section, click **Create a case**.
1. For the category, select **Billing and usage**.
1. For the topic, select **Billing and usage**, and for the subtopic, select **Exporting your usage details to a .csv file**.
1. Complete the required fields. For the description of the support case, you need to mention the months that you want the data from.

   To maintain security, do not include any personal information, sensitive data, or device or service credentials in case responses. For example, don't include passwords, API keys, secrets, or credit card information.
   {: important}

1. Click **Next**, review your case summary, and click **Submit case**. After you receive email verification for the case, follow the instructions for further communication on the issue.

After your support case is created, you can follow its progress on the [Manage cases page](/unifiedsupport/cases).
{: tip}

## Enabling your account to export usage data by using Terraform
{: #enabling-account-terraform}
{: terraform}

Before you can attach enable your account to export usage data by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://developer.hashicorp.com/terraform/language){: external}.

To enable your account to export usage data, you need to authorize a policy between two instances and provision `billing_report_snaptshot` for a resource instance. For more information, see the terraform documentation for [ibm_billing_report_snapshot](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/billing_report_snapshot){: external}. Use the following steps to create an authorization policy and provision `billing_report_snaptshot` for a resource instance by using Terraform:

Credentials need to be provided by setting the environment variable `IC_API_KEY` that corresponds to the API key of the respective account to run the billing snapshot configuration. For more information, see [IBM Cloud Provider terraform documentation](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs){: external}.

1. The following example creates an authorization policy between two specific instances.

   ```terraform
   provider "ibm" {
   }
   resource "ibm_iam_authorization_policy" "policy" {
   source_service_name         = "billing"
   target_service_name         = "cloud-object-storage"
   target_resource_instance_id = var.cos_instance_id
   roles                       = ["Object Writer", "Content Reader"]
   }
   ```
   {: codeblock}

1. The following example provisions `billing_report_snaptshot` for a resource instance.

   ```terraform
      provider "ibm" {
   }
   resource "ibm_billing_report_snapshot" "billing_report_snapshot_instance" {
   interval = var.billing_report_snapshot_interval
   versioning = var.billing_report_snapshot_versioning
   report_types = var.billing_report_snapshot_report_types
   cos_reports_folder = var.billing_report_snapshot_cos_reports_folder
   cos_bucket = var.billing_report_snapshot_cos_bucket
   cos_location = var.billing_report_snapshot_cos_location
   depends_on = [ ibm_iam_authorization_policy.policy ]
   }
   ```
   {: codeblock}

1. After you finish building your configuration file, initialize the Terraform CLI. For more information, see [Initializing Working Directories](https://developer.hashicorp.com/terraform/cli/init){: external}.

   ```terraform
   terraform init
   ```
   {: pre}

1. Provision the resources from the `main.tf` file. For more information, see [Provisioning Infrastructure with Terraform](https://developer.hashicorp.com/terraform/cli/run){: external}.

   1. Run `terraform plan` to generate a Terraform execution plan to preview the proposed actions.

      ```terraform
      terraform plan
      ```
      {: pre}

   1. Run `terraform apply` to create the resources that are defined in the plan.

      ```terraform
      terraform apply
      ```
      {: pre}

If a service-to-service authentication already exists, the `depends_on` constraint can be removed for creation of billing_report_snapshot_instance.
{: note}

### Bucket requirements
{: #enable-export-usage-bucket-requirements}

The bucket that you use to store your results does not require any particular settings or naming format. All the traffic between the Billing service and Cloud Object Storage is done over a private network. The retrieval of data for display purposes in the console does not cost you anything. However, if you choose to download the data directly from Cloud Object Storage after it is stored, you do incur a data transfer cost. See [Cloud Object Storage pricing](/docs/cloud-object-storage?topic=cloud-object-storage-billing) for more information.

## Disconnecting your account from sharing usage
{: #disconnect-exporting-your-usage}
{: ui}

If you've set up your account to export usage data, you can disconnect your chosen bucket so that you are no longer exporting data.

To disconnect, use the following steps:

1. From the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Billing and usage**, and select **Settings**.
1. Click **Disconnect**.
1. Enter the name of your bucket.
1. Click **Disconnect**.


## Know how your usage data is stored and used
{: #storing-usage-data}


Your data that is shared by using billing report snapshots and by going through the steps to enable your account to export usage data, you are setting up the snapshots.

Snapshots of the billing reports are stored based on the configuration setup. Depending on the configuration, older snapshots are either deleted or retained. Each snapshot would have a manifest file describing the details of the snapshot such as the files included as part of the snapshot. The manifest of the latest snapshot for that billing month would be stored at each billing month folder as well.


The following is an example of the folder structure of the snapshots in the COS bucket.

```sh
<cos_reports_folder>/
<cos_reports_folder>/<billing-month>/
<cos_reports_folder>/<billing-month>/manifest.json
<cos_reports_folder>/<billing-month>/<snaphot-id>
<cos_reports_folder>/<billing-month>/<snaphot-id>/manifest.json
<cos_reports_folder>/<billing-month>/<snaphot-id>/*.gz
```
{: codeblock}

cos_reports_folder
:   The billing reports root folder customer has configured as part of the biling-reports-snapshots setup.
:   Defaults to IBMCloud-Billing-Reports

billing-month
:   The billing month for corresponding to the snapshot.
:   Format is `YYYY-MM`. For example, `2023-03`.

snapshot-id
:   ID of the snapshot.
:   Alphanumeric value. For example, `1678234269105`.

manifest.json
:   Metadata file describing the details of the snapshot, such as the customer account id, csv files corresponding to the snapshot, report types 
:   The manifest file at the billing-month contains the latest snapshot taken

*.gz
:   List of files mentioned in the manifest.json

For more information about the usage of snapshot API, see [Setup the snapshot configuration](/apidocs/metering-reporting#create-reports-snapshot-config){: external}.
