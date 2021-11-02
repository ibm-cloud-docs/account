---

copyright:
  years: 2021
lastupdated: "2021-11-02"

keywords: vulnerabilities, scanning, scans, images, software, catalog

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:beta: .beta}
{:important: .important}
{:download: .download}

# Testing software for vulnerabilities
{: #scans}

Before you install instances of software from the {{site.data.keyword.cloud}} catalog, you might want to complete a vulnerability assessment on the software. By doing so, you can reduce the probability of security threats and unauthorized access of systems. 
{: shortdesc}

1. Select the software from the catalog in the {{site.data.keyword.cloud_notm}} console. 
1. Copy the URL that's displayed in the Source URL section on the Create tab. 
1. Generate an IAM access token. If you're working with OVA images, you can skip this step. 

   To generate an access token by using the {{site.data.keyword.cloud_notm}} CLI, complete the following steps:
   1. Log in to the CLI:

   ```sh
   ibmcloud login
   ```
   {: pre}

   If you're logging in with a federated ID, run the `ibmcloud login --sso` command. For more information, see [Logging in with a federated ID](/docs/account?topic=account-federated_id&interface=cli).
   {: note}

   2. Specify the region and resource group in which to create an instance of the software:

   ```sh
   ibmcloud target -r <region_name> -g <resource_group_name>
   ```
   {: pre}

   3. Retrieve your access token:

   ```sh
   ibmcloud iam oauth-tokens
   ```
   {: pre}

   The following truncated example shows a retrieved token.

   ```sh
   IAM token:  Bearer eyJraWQiOiIyM...
   ```
   {: screen}

   To generate an access token by using an API, complete the following steps:
   1. Log in to the {{site.data.keyword.cloud_notm}} CLI:

   ```sh
   ibmcloud login
   ```
   {: pre}

   If you're logging in with a federated ID, run the `ibmcloud login --sso` command. For more information, see [Logging in with a federated ID](/docs/account?topic=account-federated_id&interface=cli).
   {: note}

   2. Specify the region and resource group in which to create an instance of the software:

   ```sh
   ibmcloud target -r <region_name> -g <resource_group_name>
   ```
   {: pre}

   3. Create an API key:

   ```sh
   ibmcloud iam api-key-create <API_key_name>
       [-d, --description <description>]
       [--file <API_key_file_name>]
   ```
   {: pre}

   4. Retrieve your access token:

   ```bash
   curl --location --request GET '<source URL>' \ 
   -- header 'Authorization: bearer <token>' -o <filename> 
   ```
   {: pre}


1. Enter the source URL that you copied in the previous step in the GET request. If you're working with OVA images, you can skip this step. 
1. Press Enter to download the source package. 
1. Use a vulnerability scanning tool of your choice to validate the software. 

After you run the scan and address any issues, you can return to the console and install the software. 
