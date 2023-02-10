---

copyright:

  years: 2022, 2023

lastupdated: "2023-02-10"

keywords: private catalog, software, onboard, Terraform, terraform template, cli

subcollection: account

content-type: tutorial
services: Terraform
account-plan: paid
completion-time: 20m

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding a Terraform template by using the CLI
{: #catalog-terraform-template-cli}
{: toc-content-type="tutorial"}
{: toc-services="Terraform"}
{: toc-completion-time="20m"}

This tutorial walks you through how to onboard a Terraform template to your account by using the CLI. By completing this tutorial, you learn how to create a private catalog and import the template. After that, you can validate that the template can create resources, or run a script, and you can make it available to users who have access to your account.
{: shortdesc}


## Before you begin
{: #prereq-tutorial-terraform-template-cli}

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.
1. Upload your source code to a release in your GitHub or public GitLab repository. See [Setting up your source code repository](/docs/sell?topic=sell-source-repo-setup).
1. Make sure you're assigned the following [IAM access](/docs/account?topic=account-groups):

   * Editor role on the catalog management service
   * Viewer role on all resource groups in your account
   * Writer role on the {{site.data.keyword.secrets-manager_short}} service

1. Install the {{site.data.keyword.cloud_notm}} CLI and the {{site.data.keyword.bplong_notm}} plug-in. See [Setting up the CLI](/docs/schematics?topic=schematics-setup-cli) for more information.
1. Create your [Terraform template](/docs/schematics?topic=schematics-create-tf-config).

   1. Review the list of [supported images](/docs/vpc?topic=vpc-about-images).
   1. Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and add your image to a bucket.

To share software with other accounts, your software must be approved in Partner Center. For more information, see [Getting set up to sell software](/docs/sell?topic=sell-sw-getting-started).
{: important}


## Create a private catalog
{: #tutorial-terraform-template-cli-catalog}
{: step}

Complete the following steps to add your software by using the CLI. You can use this task in a CI/CD process.

Create a private catalog. Private catalogs provide a way for you to manage access to products for users in your account. For more information, see the [cli documentation](/docs/account?topic=cli-manage-catalogs-plugin#create-catalog) for creating a private catalog.

```bash
ibmcloud catalog create --name CATALOG [--catalog-description "DESCRIPTION"]
```
{: codeblock}

## Add the Terraform template to your catalog
{: #tutorial-terraform-template-cli-catalog-add}
{: step}

Add software to your private catalog. For more information, see the [cli documentation](/docs/cli?topic=cli-manage-catalogs-plugin#create-offering) for adding software to your private catalog.

```bash
ibmcloud catalog offering create --catalog "Name of catalog" --zipurl https://software.url.com.tgz
```
{: codeblock}

If you want to import software from a private repository, you can use a personal access token by adding [--token TOKEN] to your command. Private GitLab repositories are not supported.
{: important}

## Add a category tag to your Terraform template
{: #tutorial-terraform-template-cli-catalog-category}
{: step}

Add a category. By default, the **Developer tools** category is added to your product. For more information, see the [cli documentation](/docs/cli?topic=cli-manage-catalogs-plugin#add-category-offering) for adding a category.

```bash
ibmcloud catalog offering add-category --catalog "Name of catalog" --offering "software-offering" --category "category"
```
{: codeblock}

## Update your Terraform template
{: #tutorial-terraform-template-cli-catalog-update}
{: step}

To update a product in your private catalog, you first need get the product and then you can update. For more information, see the [cli documentation](/docs/cli?topic=cli-manage-catalogs-plugin#add-category-offering) for updating your product.

Run the `offering get` command. For more information, see [ibmcloud catalog offering get](#get-offering).

```bash
ibmcloud catalog offering get -c <CATALOGID> -o <OFFERINGID> --output json
```
{: codeblock}

Run the `offering update` command.

```bash
ibmcloud catalog offering update -c <CATALOGID> -o <OFFERINGID> --updated-offering <UPDATED_OFFERING.json>
```
{: codeblock}


## Import a version of your Terraform template
{: #tutorial-terraform-template-cli-catalog-import}
{: step}

Import the software version that you want in your catalog.

```bash
ibmcloud catalog offering import-version -c <CATALOGID> -o <OFFERINGID> --zipurl <TGZ> --target-version <VERSION>
```
{: codeblock}


## Validate your Terraform template
{: #tutorial-terraform-template-cli-catalog-validate}
{: step}

Validate the software. For more information, see the [cli documentation](/docs/cli?topic=cli-manage-catalogs-plugin#validate-offering) for validating the software.

```bash
ibmcloud catalog offering version validate --version-locator VERSION_NUMBER --cluster CLUSTER_ID --namespace NAME [--timeout TIMEOUT] [--wait WAIT] [--override-values VALUES|FILENAME]
```
{: codeblock}

Deploying the software can take a few minutes. You can check the validation status by querying the product validation state. The validation is complete when the state is Valid. For more information, see the [cli documentation](/docs/cli?topic=cli-manage-catalogs-plugin#validate-status-offering) for validation status.

```bash
ibmcloud catalog offering version validate-status --version-locator VERSION_NUMBER [--output FORMAT]
```
{: codeblock}

## Mark a version as ready
{: #mark-version-ready}
{: step}

When a product is published, all versions marked as ready within it have the same visibility. If your product is approved to publish, you can use the following commands to manage sharing your versions and products.

```bash
ibmcloud catalog offering ready --vl <VERSION_LOCATOR>
```
{: codeblock}

## Publish your Terraform template
{: #tutorial-terraform-template-cli-catalog-publish}
{: step}

Publish your software to make it available to users in your account. For more information, see the [cli documentation](/docs/cli?topic=cli-manage-catalogs-plugin#publish-offering-to-account) for publishing to your account.

```bash
ibmcloud catalog offering publish account [--catalog CATALOG][--offering OFFERING]
```
{: codeblock}
