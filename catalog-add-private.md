---

copyright:
  years: 2019, 2021
lastupdated: "2021-07-19"

keywords: catalog, catalogs, private catalogs, account catalogs, catalog visibility, software visibility, import software

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:external: target="_blank" .external}
{:beta: .beta}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Onboarding software to your account
{: #create-private-catalog}

The process to onboard software to your account includes importing a version to a private catalog, and validating that the version can be successfully installed on the deployment target. The software is then available to users in your account. 
{: shortdesc} 

## Before you begin
{: #prereq-create}

1. Review the list of software that you can onboard:

  * Helm charts
  * Terraform templates
  * OVA images deployed on VMware vCenter Server
  * Virtual server images with Terraform deployed on VPC infrastructure
  * Operators from GitHub repositories deployed on Red Hat OpenShift
  * Operator bundles from Red Hat OpenShift registries
  
1. Upload your soure code in a GitHub repository. For more information, see [Managing releases in a repository](https://docs.github.com/en/github/administering-a-repository/managing-releases-in-a-repository){: external}.
1. Make sure you're assigned the following [IAM access](/docs/account?topic=account-groups):

  * Editor role on the catalog management service
  * Viewer role on all resource groups in your account
  * Writer role on the {{site.data.keyword.secrets-manager_short}} service

1. Install the {{site.data.keyword.cloud_notm}} CLI and the {{site.data.keyword.bplong_notm}} plug-in. See [Setting up the CLI](/docs/schematics?topic=schematics-setup-cli) for more information.

For containerized apps, complete the following prerequisites:

  1. Create your [Kubernetes cluster](/docs/containers?topic=containers-getting-started) or [Red Hat OpenShift cluster](/docs/openshift?topic=openshift-getting-started).
  2. For deployments to {{site.data.keyword.cloud_notm}} Kubernetes Service, [set up your Helm chart](/docs/containers?topic=containers-helm). 
  3. For deployments to Red Hat OpenShift, set up your [Helm chart](/docs/openshift?topic=openshift-helm) or [operator](/docs/openshift?topic=openshift-operators).

For virtual server images, complete the following prerequisites:

  1. Review the list of [supported images](/docs/vpc?topic=vpc-about-images).
  2. Create your [Terraform template](/docs/schematics?topic=schematics-getting-started).
  3. Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and add your image to a bucket.
 

## Creating a private catalog
{: #create-catalog}
{: ui}

Private catalogs provide a way for you to manage access to products for users in your account. 

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud_notm}} console, and click **Create a catalog**. 
1. Enter a name and description of your catalog.
1. Select to exclude or include all products in the {{site.data.keyword.cloud_notm}} catalog in your private catalog.
1. Click **Create**.

## Importing software to your private catalog
{: #add-public-repo}
{: ui}

Complete the following steps to import software to your private catalog:

1. From the Private products page, click **Add**.
1. Select your deployment method. 
1. Select whether you are adding your product from a private or public repository. Or, if you're onboarding an Operator from a Red Hat registry, select your Red Hat repository type: **Certified**, **Marketplace**, **Community**.

  If you're adding your product from a private repository, you can provide a personal access token or you can use a secret. Instead of giving users a personal access token, you can give them access to a secret, add the token to a secret, and centrally manage all tokens and access the secret allows.

  * If you're using a personal access token, select **No** to indicate you aren't using a secret and provide your personal access token.
  * If you're using a secret, select **Yes** and click **Select from Secrets Manager**. Select your service instance, secret group, and secret. If you don't see your secret, make sure you're using the correct secret group and service instance. 
    
    The message `No service instance available` might be displayed if you haven't created a secret or if you don't have the correct access to use secrets, even if you have service instances that are created. 
    {: note}

1. Enter your source URL. If you're importing a version from a public repository, you can review the following list of supported formats per software type:

  * Helm chart: `https://charts.bitnami.com/ibm/apache-8.3.2.tgz`
  * Node-RED Operator: `https://github.com/IBM-Cloud/isv-operator-product-deploy-sample/blob/main/bundle/1.0.0/manifests/node-red-operator.v1.0.0.clusterserviceversion.yaml`
  * OVA image: `https://github.com/gcatalog/OVA-sample/blob/main/ova-sample.yaml`
  * Terraform template: `https://github.com/Cloud-Schematics/2-zone-vpc/releases/download/v1.0.9/terraform-2-zone-vpc-1.0.9.tgz`
  * Virtual server image with Terraform: `https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/releases/download/v1.0/isv-vsi-product-deploy-sample.tar.gz`

1. If applicable, enter the version of the software in the format of major version, minor version, and revision.   
1. Select a catalog category for the product. Categories are used to organize products in the {{site.data.keyword.cloud_notm}} catalog based on function, use, or common solutions.
1. Click **Add version**. 

## Configuring the software
{: #catalog-configure-details}

1. From the version list that's displayed on the product details page, click the row that contains your software. 
1. Review the version details, and click **Next**.
1. Depending on the deployment method that you previously selected, the additional configuration steps vary.

  * Helm chart: Configure the preinstallation and deployment details. 
  * Terraform: Configure the deployment details.
  * Operator from GitHub repository: Set an image pull secret, which is used to access and pull the image from a private container registry. An image pull secret is not required if the image is in a public container registry.
  * Virtual server image with Terraform: Configure the deployment details. 

1. Click **Next**. 

## Adding license agreements
{: #catalog-add-license}

If users are required to accept any license agreements beyond the {{site.data.keyword.cloud_notm}} Services Agreement when they install the software, provide the URL to each agreement. 

1. Click **Add license agreements** > **Add license**. 
1. Enter the name and URL, and click **Update**.
1. After you enter all additional license agreements, click **Next**.

## Editing your readme file
{: #catalog-readme-edit}

When users install the software, they can view installation instructions from the Readme tab of your product's catalog details page. The information on the Readme tab is generated from the readme file that you uploaded to your GitHub repository. 

1. From the Edit readme tab, preview how the information in the readme file will be displayed to users when they install the software.
1. To make updates, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") next to the Readme section title.
1. Click **Next**.

## Validating the software 
{: #catalog-validate-product}

When you validate your software, you're confirming that the current version can be successfully installed on the deployment target. The validation steps vary based on your deployment method. 

To monitor the progress of the validation process, click **View logs**.
{: tip}

### Helm chart
{: #catalog-validate-helm}

1. From the Validate product tab, select your cluster.
1. If the deployment target is a Kubernetes cluster, select a namespace or create a new one. If the deployment target is a Red Hat OpenShift cluster, select a project or create a new one. 
1. Click **Next**.
1. Configure your {{site.data.keyword.bplong_notm}} workspace.
1. Click **Next**.
1. If applicable, review the license agreements, and select **I have read and agree to the following license agreements:**. 
1. Click **Validate**.

### Cloud Pak
{: #catalog-validate-pak}

1. From the Validate product tab, select your Red Hat OpenShift cluster.
1. Select a project or create a new one. A project is similar to a Kubernetes cluster namespace, and the list is populated from your Red Hat OpenShift environment.
1. Click **Next**.
1. Run the preinstallation script. 
1. Click **Next**.
1. Configure your {{site.data.keyword.bplong_notm}} workspace.
1. Click **Next**.
1. If applicable, review the license agreements, and select **I have read and agree to the following license agreements:**. 
1. Click **Validate**.

### Terraform
{: #catalog-validate-tf}

1. From the Validate product tab, configure your {{site.data.keyword.bplong_notm}} workspace.
1. Click **Next**.
1. If applicable, review the license agreements, and select **I have read and agree to the following license agreements:**. 
1. Click **Validate**.

### Operator from GitHub repository
{: #catalog-validate-opgh}

1. From the Validate product tab, select your Red Hat OpenShift cluster.
1. Select a project or create a new one. A project is similar to a Kubernetes cluster namespace, and the list is populated from your Red Hat OpenShift environment.
1. Click **Next**.
1. Configure your {{site.data.keyword.bplong_notm}} workspace.
1. Click **Next**.
1. If applicable, review the license agreements, and select **I have read and agree to the following license agreements:**. 
1. Click **Validate**.

### Operator from Red Hat registry
{: #catalog-validate-oprh}

1. From the Validate product tab, select an update channel.
1. Select an approval strategy. 
1. Select your Red Hat OpenShift cluster.
1. Select a project or create a new one. A project is similar to a Kubernetes cluster namespace, and the list is populated from your Red Hat OpenShift environment.
1. Click **Next**.
1. Configure your {{site.data.keyword.bplong_notm}} workspace.
1. Click **Next**.
1. If applicable, review the license agreements, and select **I have read and agree to the following license agreements:**. 
1. Click **Validate**.

### OVA image
{: #catalog-validate-ova}

1. From the Validate product tab, review the license agreements, and select **I have read and agree to the following license agreements:**.
1. Click **Validate**. 

### Virtual server image with Terraform
{: #catalog-validate-vsi}

1. From the Validate product tab, configure your {{site.data.keyword.bplong_notm}} workspace.
1. Click **Next**.
1. If applicable, review the license agreements, and select **I have read and agree to the following license agreements:**. 
1. Click **Validate**.

## Publishing the software
{: #validating-software}
{: ui}

After you validate your software, you're ready to make it available to all users who have access to your private catalog. Open the **Actions** menu, and select **Publish to account**.


## Importing software to your private catalog
{: #create-cicd-product}
{: cli}

Complete the following steps to add your software by using the CLI. You can use this task in a CI/CD process.
    
1. Add software to your private catalog. For more information, see the [cli documentation](/docs/cli?topic=cli-manage-catalogs-plugin#create-offering) for adding software to your private catalog. 
    ```
    ibmcloud catalog offering create --catalog "Name of catalog" --zipurl https://software.url.com.tgz
    ```
    {: codeblock}
    
1. Add the **Developer Tools** category. For more information, see the [cli documentation](/docs/cli?topic=cli-manage-catalogs-plugin#add-category-offering) for adding a category. 
    ```
    ibmcloud catalog offering add-category --catalog "Name of catalog" --offering "software-offering" --category "Developer Tools"
    ```
    {: codeblock}
    
1. Validate the software. For more information, see the [cli documentation](/docs/cli?topic=cli-manage-catalogs-plugin#validate-offering) for validating the software.
    
    You need the version locator for your software. To find it, run the **`ibmcloud catalog offering list --catalog "Name of catalog"`** command, and search for the particular version of your software. Also, use the cluster that you created when you set up the required resources. 
    {: important}
    
    ```
    ibmcloud catalog offering validate --version-locator <LOCATOR> --cluster <CLUSTER> --namespace "software-offering"
    ```
    {: codeblock}
    
    Deploying the software can take a few minutes. You can check the validation status by querying the product validation state. The validation is complete when the state is Valid. For more information, see the [cli documentation](/docs/cli?topic=cli-manage-catalogs-plugin#validate-status-offering) for validation status.
    ```
    ibmcloud catalog offering validate-status --version-locator <LOCATOR>
    ```
    {: codeblock}
    
1. Publish your software to make it available to users in your account. For more information, see the [cli documentation](/docs/cli?topic=cli-manage-catalogs-plugin#publish-offering-to-account) for publishing to your account.
    ```
    ibmcloud catalog offering publish-to-account --version-locator <LOCATOR>
    ```
    {: codeblock}

## Importing software to your private catalog
{: create-product-api}
{: api}

You can programmatically add an offering to your catalog by calling the Catalog Management API as shown in the following sample request. For detailed information about the API, see [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=java#create-offering).

```java
String id = "{id}";
String name = "{name}";
String label = "{label}";
CreateOfferingOptions offeringOptions = new CreateOfferingOptions.Builder().catalogIdentifier(id).name(name).label(label).build();
Response<Offering> response = service.createOffering(offeringOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
id = "{id}";
name = "{name}";
label = "{label}";
response = await service.createOffering({ 'catalogIdentifier': id, 'id': id, 'name': name, 'label': label });
console.log(response);
```
{: codeblock}
{: javascript}

```python
id = "{id}"
name = "{name}"
label = "{label}"
response = self.service.create_offering(catalog_identifier=id, name=name, label=label)
print(response)

```
{: codeblock}
{: python}

```go 
id := "{id}"
name := "{name}"
label := "{label}"
offeringOptions := service.NewCreateOfferingOptions(id)
offeringOptions.SetName(name)
offeringOptions.SetLabel(label)
_, response, _ := service.CreateOffering(offeringOptions)
fmt.Println(response)
```
{: codeblock}
{: go}
