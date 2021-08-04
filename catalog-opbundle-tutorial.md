---

copyright:
  years: 2021
lastupdated: "2021-07-30"

keywords: private catalog, software, onboard, operator, validate, test, Red Hat OpenShift operator, operator bundle

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
{:important: .important}
{:beta: .beta}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'} 

# Onboarding a Certified Operator from a {{site.data.keyword.redhat_notm}} registry 
{: #catalog-opbundle-tutorial}
{: toc-content-type="tutorial"} 
{: toc-services="Registry"}
{: toc-completion-time="45m"} 

This tutorial walks you through how to onboard a sample Operator bundle from a {{site.data.keyword.redhat_full}} registry to your account. By completing this tutorial, you learn how to create a private catalog in your account, import the Operator bundle, and validate that it can be installed on a {{site.data.keyword.redhat_notm}} {{site.data.keyword.openshiftshort}} cluster.
{: shortdesc}

## Before you begin
{: #catalog-opbundle-prereqs}

1. Go to the {{site.data.keyword.redhat_notm}} OperatorHub to confirm that your Operator bundle exists in the {{site.data.keyword.redhat_notm}} Certified registry.
1. [Create your {{site.data.keyword.redhat_notm}} {{site.data.keyword.openshiftshort}} cluster](/docs/openshift?topic=openshift-getting-started). 
1. [Upload your Operator bundle and application images to {{site.data.keyword.registrylong_notm}}](/docs/Registry?topic=Registry-getting-started).
1. Verify that you're assigned the following {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM). See [Assigning access to account management services](/docs/account?topic=account-account-services) and [Managing access to resources](/docs/account?topic=account-assign-access-resources) for more information.
   * Administrator on all account management services and all IAM services
   * Editor on the catalog management service
   * Editor on the software instance service
   * Editor on the {{site.data.keyword.registrylong_notm}} service
   * Administrator on the {{site.data.keyword.redhat_notm}} {{site.data.keyword.openshiftshort}} cluster

Make sure that you use the same account to access {{site.data.keyword.registrylong_notm}} and to create the {{site.data.keyword.redhat_notm}} {{site.data.keyword.openshiftshort}} cluster.
{: important}

## Create a private catalog
{: #catalog-opbundle-private}
{: step}

Private catalogs provide a way for you to make your own products available to users in your account. 

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud_notm}} console, and click **Create a catalog**. 
1. Select **Product default** as the catalog type. 
1. Enter the name of your catalog, for example, `Sample Operator Bundle`.
1. Select **No products** to exclude all products in the {{site.data.keyword.cloud}} catalog from your catalog.
1. Click **Create**.

## Import your Operator bundle
{: #catalog-opbundle-import}
{: step}

1. On the Private products page, click **Add**.
1. Select **Operator from {{site.data.keyword.redhat_notm}} registry** as your deployment method. 
1. Select **Certified** as your {{site.data.keyword.redhat_notm}} repository. 
1. Select your Operator bundle. For example, for the purposes of this tutorial, you can select **Akka Cluster Operator** as your Operator.
1. Select the Operator bundle version that you would like to import.
1. Enter the software version that the Operator bundle installs in the format of major version, minor version, and revision. For example, you can use Operator version `1.0.0` to install software version `2.0.0`. 
1. Click **Add version**.

## Add end user license agreements
{: #catalog-opbundle-license}
{: step}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement, provide the URL to each agreement.   

1. In the Version list table, click the row that contains your Operator bundle. 
1. Click **Add license agreements** > **Add**. 
1. Enter the name and URL of the license agreement, and click **Update**.
1. After entering all additional license agreements, click **Next**.

## Review your readme file 
{: #catalog-opbundle-readme}
{: step}

Users can view installation instructions from the Readme tab of the Operator bundle details page in your private catalog. 

1. From the Edit readme tab, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
2. Preview how the information in the readme file will be displayed to users when they are installing the Operator bundle.
3. If you need to make changes, edit the information in the source file and import the updated Operator bundle to your private catalog. 
4. Click **Next**.

## Validate your Operator bundle
{: #catalog-opbundle-validate}
{: step}

Validate that the Operator bundle can be successfully installed on the target {{site.data.keyword.redhat_notm}} {{site.data.keyword.openshiftshort}} cluster.  

1. Click **Validate product**
1. Select the Update channel to receive version updates from. 
1. Select whether you want the updates to be applied automatically or manually. 
1. Select the target cluster and project, and click **Next**.
1. Enter the name of your Schematics workspace, select a resource group, and click **Next**.  

  In the **Tags** field, you can enter a name of a specific tag to attach to your Operator. Tags provide a way to organize, track usage costs, and manage access to the resources in your account.
  {: tip}

1. Click **Validate**. 

## Next steps
{: #catalog-opbundle-next}

After you onboard and validate your Operator bundle, you're ready to publish it to your account. From the **Actions** menu, select **Publish to account**. As a result, the Operator bundle is available only to users who have access to the `Sample Operator Bundle` private catalog in your account.
