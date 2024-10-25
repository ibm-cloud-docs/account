---

copyright:
  years: 2021, 2024
lastupdated: "2024-01-18"

keywords: vulnerabilities, scanning, scans, images, software, catalog

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Scanning software for vulnerabilities
{: #scans}

Before you install instances of software from the {{site.data.keyword.cloud}} catalog, you might want to complete a vulnerability assessment on the contents of the software and its associated images. By doing so, you can reduce the probability of security threats and unauthorized access of systems.
{: shortdesc}

## Before you begin
{: #scans-prereqs}

You need to install the {{site.data.keyword.cloud_notm}} CLI. For more information, see [Getting started with the {{site.data.keyword.cloud_notm}} CLI](/docs/cli?topic=cli-getting-started).

## Scanning software for vulnerabilities
{: #scan-vulnerabilities}

To scan for software vulnerabilities, you need to use the {{site.data.keyword.cloud_notm}} CLI after you select your software from the catalog.

1. From the [{{site.data.keyword.cloud_notm}} catalog](https://cloud.ibm.com/catalog){: external}, select the software.
1. Click **View details** on the software's product page.
1. Copy the Catalog source URL.
1. Run the `ibmcloud login` command to log in to the CLI:

   ```sh
   ibmcloud login
   ```
   {: pre}

   If you're logging in with a federated ID, run the `ibmcloud login --sso` command. For more information, see [Logging in with a federated ID](/docs/account?topic=account-federated_id&interface=cli).
   {: note}

1. Run the `ibmcloud oath-tokens` command to retrieve your access token. If you're working with OVA images, you can skip this step.

   ```sh
   ibmcloud iam oauth-tokens
   ```
   {: pre}

   The following truncated example shows a retrieved token.

   ```sh
   IAM token:  Bearer eyJraWQiOiIyM...
   ```
   {: screen}

1. Copy the access token.

1. Run the curl command with the software's source URL and your access token to download the source package. The `filename` is what you want to name the file on your computer.

   ```bash
   curl --location --request GET '<source URL>' --header 'Authorization: bearer <token>' -o <filename>
   ```
   {: pre}

1. Use a vulnerability scanning tool of your choice to scan the downloaded contents of the software and associated images for any issues.

After you run the scan and address any reported issues, you can return to the console and install the software.
