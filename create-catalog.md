---

copyright:
  years: 2019, 2020
lastupdated: "2020-02-06"

keywords: catalog, catalogs, private catalogs, account catalogs, catalog visibility, offering visibility, import software

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Adding your software to a private catalog
{: #create-private-catalog}

This tutorial walks you through the steps for creating a private catalog and adding your own software offering. The software offering is available to all users with access to the private catalog.
{: shortdesc} 

This feature is available only in a closed beta program. If you’re interested in participating, contact kala.nenkova@ibm.com.
{: note}

## Before you begin
{: #prereq-create}

To complete this tutorial, you need to be assigned the following roles:

* Editor role on the private catalog service
* Administrator and manager roles on the Kubernetes cluster service
* Manager role on the Schematics service
* Viewer role on all resource groups

For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
{: tip}

### Set up the required resources 
{: #create-resources-editor}

You must have a Kubernetes cluster to validate an Apache Helm chart on the cluster. If you don't have one already, complete the following steps to create a Kubernetes cluster with the minimal resources needed to complete the tutorials. You are charged for your usage. 

1. Go to the [Kubernetes landing page](https://cloud.ibm.com/kubernetes/landing) in the {{site.data.keyword.cloud_notm}} console.
1. Click **Create cluster**.
1. Select **Classic infrastructure**.
1. Enter your cluster name, and select the resource group that you want to assign it to.
1. In the Location section, select **Single zone**.
1. Select the worker zones.
1. In the Default worker pool section, select a minimum flavor of 2vCPUs with 4GB RAM.
1. Select 1 worker node.
1. Click **Create cluster**.  

Creating a cluster can take a few minutes. When the status on the Overview page is updated to Normal, the cluster is ready and you can proceed with the steps for adding your software to a private catalog.

## Add your software offering in the console
{: #create-editor-offering}

Complete the following steps to add an Apache Helm chart from Bitnami with a few custom configurations to your private catalog. 

1. Go to [Manage > Catalogs](https://cloud.ibm.com/content-mgmt/catalogs). If you created a private catalog in the previous tutorials, you can skip the next 3 steps.
1. Click **Create** to start creating a new private catalog.
1. Enter `My first catalog` as the catalog name, select the resource group that you want to assign it to, and click **Create**.
1. Select **My first catalog** from the list of private catalogs.
1. Click **Add offering**.  
1. Enter the repository URL or TGZ archive location for your software offering, and click **Add**. For testing purposes use the Bitnami Apache offering: https://charts.bitnami.com/ibm/apache-6.0.2.tgz. This creates Apache version 2.4.39 from chart version 6.0.2.
1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg), update the offering name to `apache-two-instances`, and set at least one category for your offering, for example, Developer Tools. This category can be used by users later to filter for the offering.
2. Click **Update** to apply your changes. 
1. Scroll to the Configure deployment details section, and click **Add deployment values**.
1. Select **replicaCount**, and click **Add deployment values**.
1. In the Deployment values section, click the replicaCount parameter.
1. Update the default value from `1` to `2`, and click **Update**.
1. Click **Update**.
1. Click the Validate offering tab.
1. In the Configure the validation target section, select your cluster from the **Cluster** list, and enter `apache-test-deployment` as the namespace.
1. Click **Validate** to ensure that your offering can be installed successfully. This step is required before you can make it available for users in your account. This action can take several minutes. In the Validation summary section, the status is displayed as Validated when the deployment is complete. 
2. Make sure the deployment is successful by checking the Schematics workspace and the Kubernetes cluster:
    1. Click **View logs** in the Validation summary section. You're directed to your workspace details.
    2. Confirm that the recent activity shows that the plan is applied.
    3. Open the log file for the workspace by clicking **View log**.
    4. Scroll to the end of the log file, and confirm that the text `Command finished successfully.` is displayed.
    5. Return to the Validate offering tab, and click the name of the cluster in the Validation summary section. You're directed to your cluster details.
    1. Click **Kubernetes dashboard**. 
    1. Click **Namespaces** > the name of your namespace. 
    1. Click **Services** in the navigation. 
    1. Click the external endpoint link with port 80, and verify a page with the text `It works!` is displayed. 
1. Return to the Validate offering tab, click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Publish to account** to make the offering available to all users in your account through your private catalog.

## Add your software offering by using CLI
{: #create-cicd-offering}

First clean up your resources and the Apache deployment on your cluster by deleting your workspace that was created during the validation process in the previous steps.

1. Click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) > **Schematics**.
2. Click **Workspaces**.
3. In the row for your workspace instance, click the **Actions** ![Actions icon](../icons/actions-icon-vertical.svg) icon, and select delete.
<br>

Complete the following steps to add your software offering by using the CLI. You can use this task in a CI/CD process.

1. Delete the software offering that you previously installed to start fresh.
    ```
    ibmcloud catalog offering delete  --catalog "My first catalog" --offering "apache-two-instances"
    ```
    {: codeblock}
    
1. Add a new software offering to your private catalog.  
    ```
    ibmcloud catalog offering create --catalog "My first catalog" --zipurl https://charts.bitnami.com/ibm/apache-6.0.2.tgz
    ```
    {: codeblock}
    
1. Add the **Developer Tools** category to the offering.  
    ```
    ibmcloud catalog offering add-category --catalog "My first catalog" --offering "apache-two-instances" --category "Developer Tools"
    ```
    {: codeblock}
    
1. Validate the offering.  
    
    You need the version locator for your offering. To find it, run the `ibmcloud catalog offering list --catalog "My first catalog"` command, and search for the particular version of your offering. Also, use the cluster that you created when you set up the required resources. 
    {: important}
    
    ```
    ibmcloud catalog offering validate --version-locator <LOCATOR> --cluster <CLUSTER> --namespace "apache-test-deployment"
    ```
    {: codeblock}
    
    Deploying the offering can take a few minutes. You can check the validation status by querying the offering validation state. The validation is complete when the state is Valid. 
    ```
    ibmcloud catalog offering validate-status --version-locator <LOCATOR>
    ```
    {: codeblock}
    
1. Publish the offering to the account. This step adds a tile in the {{site.data.keyword.cloud_notm}} catalog on the Private tab only for users with access to the private catalog.
    ```
    ibmcloud catalog offering publish-to-account --version-locator <LOCATOR>
    ```
    {: codeblock}
    
## Next steps
{: #install-sw-next}

A user installs the apache-two-instances offering from your private catalog. See [Installing a private software offering](/docs/account?topic=account-install-sw) for more information.

### Providing feedback
{: #survey-addsw}

We put together a [survey](https://airtable.com/shr6Fornt8WwtAKPZ){: external} specifically about this tutorial. We'd love to know what you think!
