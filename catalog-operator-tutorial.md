---

copyright:
  years: 2021
lastupdated: "2021-08-31"

keywords: onboard software, operator, validate, test, Red Hat OpenShift cluster, sample Node-RED Operator, CSV file, CSV, operator bundle, TGZ file

subcollection: account

content-type: tutorial
services: Registry
account-plan: paid
completion-time: 45m 

---

{:shortdesc: .shortdesc}
{:screen: .screen}  
{:codeblock: .codeblock}  
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:beta: .beta}
{:important: .important}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'} 

# Onboarding an Operator from a GitHub repository
{: #catalog-operator-gh}
{: toc-content-type="tutorial"} 
{: toc-services="Registry"}
{: toc-completion-time="45m"} 

This tutorial walks you through how to onboard a sample Operator from a GitHub repository to your account. You can onboard an Operator bundle using a TGZ file or an Operator using a CSV file. By completing this tutorial, you learn how to create a private catalog, import your CSV or TGZ file, validate that it can be installed on a Red Hat OpenShift cluster, and make the Operator available to users who have access to your account. 
{: shortdesc}

## Before you begin
{: #catalog-operator-prereqs}

1. [Upload your Operator and application images to {{site.data.keyword.registrylong}}](/docs/Registry?topic=Registry-getting-started).
1. [Create your Red Hat OpenShift cluster](/docs/openshift?topic=openshift-getting-started). 
1. Upload your source code to your GitHub repository. 

   Use the [latest release of the sample Node-RED Operator](https://github.com/IBM-Cloud/operator-bundle-sample/releases){: external} as an example of how to set up your directory structure. 
   {: tip} 
  
1. Make sure you're assigned the {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) editor role on the catalog management service. See [Assigning access to account management services](/docs/account?topic=account-account-services) for more information. 

1. For Operator bundles, you also need the following {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) roles. 
   * Administrator on all account management services and all IAM services
   * Editor on the software instance service
   * Editor on the {{site.data.keyword.registrylong_notm}} service
   * Administrator on the {{site.data.keyword.redhat_notm}} {{site.data.keyword.openshiftshort}} cluster

Make sure that you use the same account to access {{site.data.keyword.registrylong_notm}} and to create the {{site.data.keyword.redhat_notm}} {{site.data.keyword.openshiftshort}} cluster.
{: important}

## Create a private catalog
{: #catalog-operator-private}
{: step}

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud_notm}} console, and click **Create a catalog**. 
1. Select **Product default** as the catalog type. 
1. Enter the name of your catalog, for example, `Sample Operator`.
1. Select **No products** to exclude all products in the {{site.data.keyword.cloud}} catalog from your catalog. For more information about how this affects which products are visible in the catalog, see [Managing catalog settings](/docs/account?topic=account-filter-account&interface=ui).
1. Click **Create**.

## Import your Operator 
{: #catalog-operator-import}
{: step}

1. On the Private products page, click **Add**.
1. Select **Operator from GitHub repository** as your deployment method. 
1. Confirm that **Public repository** is selected as the repository type.
1. Enter `https://github.com/IBM-Cloud/operator-bundle-sample/archive/refs/tags/v0.0.3.tar.gz` as your source URL. 
1. Enter the software version in the format of major version, minor version, and revision, for example, `1.0.0`.

   Enter the version of your software and not the version of your Operator. For example, you might be using Operator version 1.3.0 to install software version 3.1.1. 
   {: important}
1. Click **Add product**.

## Review the version details
{: #catalog-operator-review-version}
{: step}

From the Configure product tab, you can review your version details. There are no actions that you need to take. When you are ready to move on, click **Next**.

## Set an image pull secret
{: #catalog-operator-secret}
{: step}

When you create your {{site.data.keyword.openshiftlong}} cluster, the cluster includes an IAM service ID that is given reader access to {{site.data.keyword.registrylong_notm}}. The service ID credentials are authenticated in a non-expiring service ID API key that is stored in image pull secrets in your cluster. As part of configuring the deployment details, you set a pull secret that's used to access and pull your images from the private {{site.data.keyword.registrylong_notm}} repository. 

1. From the Set an image pull secret section, click **Add image pull secret**.
1. Enter the name and value of the image pull secret. 
1. Click **Update**.
1. From the **Image pull secret name** list, select the image pull secret that you just added. 
1. Click **Next**.

## Set the license requirements
{: #catalog-operator-license}
{: step}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement, provide the URL to each agreement. Or, if users can bring their own licenses, you can provide that URL as well.  

1. Click **Add license agreements** > **Add**. 
2. Enter the name and URL, and click **Update**.
3. After entering all additional license agreements, click **Next**.

## Review your readme file 
{: #catalog-operator-readme}
{: step}

When users access your Operator from your account, they can view installation instructions from the Readme tab of Operator's details page in your private catalog. The readme information is automatically generated from the details in your TGZ or CSV file. 

1. From the Edit readme tab, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
2. Preview how the information in the readme file will be displayed to users when they are installing the Operator.
3. If you need to make changes, edit the information in your source and import the updated software to your private catalog. 
4. Click **Next**.  

## Validate the Operator
{: #catalog-operator-validate}
{: step}

To publish the Operator to your account, you're required to validate that it can be successfully installed on the target Red Hat OpenShift cluster.  

1. From the Validate product tab, select the target cluster and project, and click **Next**. 
1. Enter the name of your Schematics workspace, select a resource group, and click **Next**. 

   In the **Tags** field, you can enter a name of a specific tag to attach to your Operator. Tags provide a way to organize, track usage costs, and manage access to the resources in your account.
   {: tip}
  
1. Click **Validate**.


## Next steps
{: #catalog-operator-next}

After you onboard and validate your Operator, you're ready to publish it to your account. From the **Actions** menu, select **Publish to account**. As a result, the Operator is available only to users who have access to the `Sample Operator` private catalog in your account.
