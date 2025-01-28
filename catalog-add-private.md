---

copyright:

  years: 2019, 2025
lastupdated: "2025-01-28"

keywords: catalog, catalogs, private catalogs, account catalogs, catalog visibility, software visibility, import software

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Onboarding software to your account
{: #create-private-catalog}

The process to onboard software to your account includes importing a version to a private catalog, validating that the version can be successfully installed on the target infrastructure that you require, and publishing the software to your account. The software is then available to users in your account.
{: shortdesc}

## Before you begin
{: #prereq-create}

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.

1. Review the list of software that you can onboard:

   * Helm charts on Kubernetes and {{site.data.keyword.openshiftshort}} clusters
   * Terraform templates
   * OVA images that are deployed on VMware Solutions Dedicated - vCenter Server
   * Virtual server images with Terraform deployed on VPC infrastructure or {{site.data.keyword.powerSys_notm}}
   * Virtual server images for VPC

    Onboarding Virtual Server Images for VPC with {{site.data.keyword.IBMz}} deployment support is available in private catalogs. The onboarding experience for {{site.data.keyword.IBMz_notm}}-supported Virtual Server Images is the same as how you onboard other Virtual Server Images in your private catalog.
    {: note}

   * Operators with TGZ file from GitHub or GitLab repositories
   * Operator bundles from Red Hat OpenShift registries

1. There is no requirement to upload your source code to a release on your GitHub or GitLab repository if you are deploying VSI on VPC. Instead, ensure you have a custom image ready and available in your account. See [Importing and validating custom images into VPC](/docs/vpc?topic=vpc-importing-custom-images-vpc&interface=ui). 

1. Make sure you are assigned the following [IAM access](/docs/account?topic=account-groups):

   * Manager role on the Schematics service
   * Editor role on the catalog management service
   * Viewer role on all resource groups in your account. You need access to at least one resource group to run the validation 
   * Writer role on the {{site.data.keyword.secrets-manager_short}} service. This role is not required if you are using VSI on VPC

1. Install the {{site.data.keyword.cloud_notm}} CLI and the {{site.data.keyword.bplong_notm}} plug-in. See [Setting up the CLI](/docs/schematics?topic=schematics-setup-cli) for more information.

For containerized apps, complete the following prerequisites:

   1. Create your [Kubernetes cluster](/docs/containers?topic=containers-getting-started) or [Red Hat OpenShift cluster](/docs/openshift?topic=openshift-getting-started).
   2. For deployments to {{site.data.keyword.cloud_notm}} Kubernetes Service, [set up your Helm chart](/docs/containers?topic=containers-helm).
   3. For deployments to Red Hat OpenShift, set up your [Helm chart](/docs/openshift?topic=openshift-helm) or [Operator](/docs/openshift?topic=openshift-operators).

For virtual server images, complete the following prerequisites:

   1. Review the list of [supported images](/docs/vpc?topic=vpc-about-images).
   2. If required, create your [Terraform template](/docs/schematics?topic=schematics-create-tf-config). Virtual server image for VPC does not require a Terraform template.
   3. Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and add your image to a bucket.

Before you can onboard software to your account by using Terraform, make sure that you have completed the following:
{: terraform}

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://developer.hashicorp.com/terraform/language){: external}.
{: terraform}

To share software with other accounts, your software must be approved in Partner Center. For more information, see [Getting set up to sell software](/docs/sell?topic=sell-sw-getting-started).
{: important}






## Creating a private catalog
{: #create-catalog-ui}
{: ui}

Private catalogs provide a way for you to manage access to products for users in your account.

1. Go to **Manage** > **Catalogs** in the {{site.data.keyword.cloud_notm}} console, and click **Create a catalog**.
1. Enter a name and description of your catalog.
1. Select to exclude or include all products in the {{site.data.keyword.cloud_notm}} catalog in your private catalog. For more information about how this affects visibility in the catalog, see [Managing catalog settings](/docs/account?topic=account-filter-account&interface=ui).
1. Click **Create**.

## Importing software to your private catalog
{: #add-public-repo-ui}
{: ui}

Complete the following steps to import software to your private catalog:

1. From the Private products page, click **Add**.
1. Select your deployment method.
1. Select whether you are adding your product from a private or public repository. Or, if you're onboarding an Operator from a Red Hat registry, select your Red Hat repository type: **Certified**, **Marketplace**, **Community**.

   If you're adding your product from a private repository, you can provide a personal access token or you can use a secret. Instead of giving users a personal access token, you can give them access to a secret, add the token to a secret, and centrally manage all tokens and access the secret allows.

   * If you're using a personal access token, select **No** to indicate that you aren't using a secret and provide your personal access token.
   * If you're using a secret, select **Yes** and click **Select from Secrets Manager**. Select your service instance, secret group, and secret. If you don't see your secret, make sure you're using the correct secret group and service instance.

    The message `No service instance available` might be displayed if you haven't created a secret or if you don't have the correct access to use secrets, even if you have service instances that are created.
    {: note}

1. Enter your source URL. You can review the following list of supported formats per software type:

   * Helm chart: `https://raw.githubusercontent.com/IBM/charts/master/repo/ibm-helm`
   * Node-RED Operator: `https://github.com/IBM-Cloud/operator-bundle-sample/archive/refs/tags/v0.0.3.tar.gz`
   * Operator bundle from a {{site.data.keyword.openshiftshort}} registry: For an example, select the `Akka Cluster Operator` from the list of available Operators in the Certified repository.
   * OVA image: `https://github.com/gcatalog/OVA-sample/blob/main/ova-sample.yaml`
   * Terraform template: `https://github.com/IBM-Cloud/terraform-sample/releases/tag/v1.0.0`
   * Virtual server image with Terraform: `https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/releases/download/v1.0/isv-vsi-product-deploy-sample.tar.gz`
   * Virtual server image for VPC: Select an image from the list of available images that were imported into your VPC, or import a new image to your account.

    A virtual server image for VPC can only be added to one product within one private catalog at a time. If the virtual server image you want to import is already imported into another product, you must remove the image from that product or delete the product before you add the virtual server image to a new product.
    {: note}

1. If applicable, enter the version of the software in the format of major version, minor version, and revision. For example, enter version 1.1.2.
1. Select a catalog category for the product. Categories are used to organize products in the {{site.data.keyword.cloud_notm}} catalog based on function, use, or common solutions.
1. Click **Add product**.

## Adding catalog entry details
{: #catalog-tile}
{: ui}

When you publish your product to the catalog for users with access to your private catalog, they see a tile with the product name and other details that add during onboarding. In addition to the category that you set when you import your software, you can add other filters that are related to industry, compliance, technologies it works with, and more. Each of these filters is used in the catalog for users to find software that fits their needs. In the catalog entry details section, you can also evaluate and make updates to the short descriptions, documentation URL, and even keywords to help user search and find your product quickly.

1. From the Catalog entry details section, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit").
2. Review the information that was imported with your product, and make edits as needed.
3. Review the filters and industry options to select catalog filters that apply. You can select up to five industry filters.
4. Check your catalog entry preview to see how your catalog tile displays to users who are evaluating your software in the catalog.
5. Click **Save** when you're happy with your changes.

For more information, see [Defining your product details](/docs/account?topic=account-cm-catalog-details&interface=ui).

## Configuring the software
{: #catalog-configure-details}
{: ui}

### Helm chart
{: #catalog-config-helm}
{: ui}

1. From the version list that's displayed on the product details page, click the row that contains your software.
1. Review the version details, and click **Next**.
1. Configure the preinstallation, and click **Next**.
1. Configure the deployment details by setting the access that's required to run the installation script and setting the deployment values, and click **Next**.

### Terraform
{: #catalog-config-tf}
{: ui}

1. From the version list that's displayed on the product details page, click the row that contains your software.
1. Review the version details, and click **Next**.
1. Configure the deployment values.
1. If applicable, edit the output value descriptions, and click **Next**.
1. Define the required IAM access, and click **Next**.

### Operator from GitHub repository
{: #catalog-config-opgh}
{: ui}

1. From the version list that's displayed on the product details page, click the row that contains your software.
1. Review the version details, and click **Next**.



### Operator from Red Hat registry
{: #catalog-config-oprh}
{: ui}

1. From the version list that's displayed on the product details page, click the row that contains your software.
1. Review the version details, and click **Next**.

### OVA image
{: #catalog-config-ova}
{: ui}

1. From the version list that's displayed on the product details page, click the row that contains your software.
1. Review the version details, and click **Next**.

### Virtual server image with Terraform
{: #catalog-config-vsi}
{: ui}

1. From the version list that's displayed on the product details page, click the row that contains your software.
1. Review the version details, and click **Next**.
1. Configure the deployment values.
1. If applicable, edit the output value descriptions, and click **Next**.
1. Define the required IAM access, and click **Next**.

### Virtual server image for VPC
{: #catalog-config-vsivpc}
{: ui}

1. From the version list that's displayed on the product details page, click the row that contains your software.
1. Review the list of images, and click **Next**.
1. Review the version details, and click **Next**.

## Adding license agreements
{: #catalog-add-license}
{: ui}

Provide the URLs to the license agreements that users are required to accept when they install the product. The license agreements are in addition to the {{site.data.keyword.cloud_notm}} Services Agreement.

1. Click **Add license agreements** > **Add license**.
1. Enter the name and URL, and click **Update** > **Next**.

## Editing your readme file
{: #catalog-readme-edit}
{: ui}

When users install the software, they can select the link to your readme file to view product information. The information in the Readme link is generated from the readme file that you uploaded to your source repository.

1. From the Edit readme tab, preview how the information in the readme file will be displayed to users when they install the software.
1. To make updates, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") next to the Readme section title.
1. Click **Save**.
1. Click **Next**.

If you are importing a virtual server image for VPC, the readme file is not automatically generated. Copy and paste the contents of the [readme file template](/media/docs/downloads/software/sw-readme-tab-template.md){: external} and make updates as needed.
{: note}

## Validating the software
{: #catalog-validate-product}
{: ui}

When you validate your software, you're confirming that the current version can be successfully installed on the deployment target. The validation steps vary based on your deployment method.

To monitor the progress of the validation process, click **View logs**.
{: tip}

### Helm chart
{: #catalog-validate-helm}
{: ui}

1. From the Validate product tab, select your cluster.
1. If the deployment target is a Kubernetes cluster, select a namespace or create a new one. If the deployment target is a Red Hat OpenShift cluster, select a project or create a new one.
1. Click **Next**.
1. Configure your {{site.data.keyword.bplong_notm}} workspace.
1. Click **Next**.
1. If applicable, review the license agreements, and select **I have read and agree to the following license agreements:**.
1. Click **Validate**.

### Terraform
{: #catalog-validate-tf}
{: ui}

1. From the Validate product tab, configure your {{site.data.keyword.bplong_notm}} workspace.
1. Click **Next**.
1. If applicable, review the license agreements, and select **I have read and agree to the following license agreements:**.
1. Click **Validate**.

### Operator from GitHub repository
{: #catalog-validate-opgh}
{: ui}

1. From the Validate product tab, select your Red Hat OpenShift cluster.
1. Select a project or create a new one. A project is similar to a Kubernetes cluster namespace, and the list is populated from your Red Hat OpenShift environment.
1. Click **Next**.
1. Configure your {{site.data.keyword.bplong_notm}} workspace.
1. Click **Next**.
1. If applicable, review the license agreements, and select **I have read and agree to the following license agreements:**.
1. Click **Validate**.

### Operator from Red Hat registry
{: #catalog-validate-oprh}
{: ui}

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
{: ui}

1. From the Validate product tab, review the license agreements, and select **I have read and agree to the following license agreements:**.
1. Click **Validate**.

### Virtual server image with Terraform
{: #catalog-validate-vsi}
{: ui}

1. From the Validate product tab, configure your {{site.data.keyword.bplong_notm}} workspace.
1. Click **Next**.
1. If applicable, review the license agreements, and select **I have read and agree to the following license agreements:**.
1. Click **Validate**.

### Virtual server image for VPC
{: #catalog-validate-vsivpc}
{: ui}

1. From the validate version tab, configure the validation target, and click **Next**.
1. Optionally, configure your Schematics workspace, and click **Next**.
1. If applicable, review the license agreements, and select **I have read and agree to the following license agreements:**.
1. Click **Validate**.

## Manage compliance
{: #catalog-manage-controls}
{: ui}

You can add profiles and controls to your software to prove that it meets security and compliance requirements. You must use {{site.data.keyword.compliance_short}} to scan the resources created during validation.

Only profiles and controls that are supported by the {{site.data.keyword.compliance_short}} and validated by {{site.data.keyword.compliance_short}} scans appear in the catalog.

### Run a Security and Compliance Center scan
{: #catalog-run-scc-scans}
{: ui}

When you claim profiles and controls, you must evaluate the resources that were created during validation to ensure compliance. To run a scan, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) **> Security and Compliance** to access {{site.data.keyword.compliance_short}}.
2. In the navigation, click **Profile**.
3. Click the **Overflow** menu in the row of the profile that you want to evaluate and select **Run scan**.
3. Click **Run scan**.

After your scan completes, you can return to your private catalog to continue the onboarding process.

### Adding compliance controls
{: #catalog-add-controls}
{: ui}

Add the profiles and controls that you want to claim.

1. In the Manage compliance section of your product, select **Add claims**.
1. Select the profile that you want to add.
1. Choose to add the entire profile or a subset of controls.
1. If you choose an entire profile, continue to the next step. If you choose to add a subset of controls, select the controls that you want to add.
1. Click **Add**.

### Applying {{site.data.keyword.compliance_short}} scans
{: #catalog-add-scc-scans}
{: ui}

Add the scans that you previously ran in the {{site.data.keyword.compliance_short}}. {{site.data.keyword.compliance_short}} scans determine adherence to regulatory controls. For more information, see [Running a scan on demand](/docs/security-compliance?topic=security-compliance-attachments#scan-ondemand).

1. Click **Add scan**.
1. Select the profile that you used for the evaluation.
1. Select the {{site.data.keyword.compliance_short}} scan.
1. Click **Apply scan**.
1. Click **Next**.

## Review requirements
{: #catalog-manage-review-reqs}

You must complete validation and any other requirements to share to your account. When you're ready to make your product available to all users who have access to your private catalog, click **Ready to share**.

## Sharing the software
{: #validating-software}
{: ui}

If you want to share your product to your account or enterprise, click the name of the product in the navigation to go to the product details page. From the **Actions** menu, click **Share**. Select where you want to share your product, and click **Share**.


## Onboarding software to your catalog by using the CLI
{: #create-cicd-product}
{: cli}


Complete the following steps to add your software by using the CLI. You can use this task in a CI/CD process. To add software from a private repository, you must include a personal access token.

1. Run the [ibmcloud catalog create](/docs/cli?topic=cli-manage-catalogs-plugin#create-catalog) command to create a private catalog. Private catalogs provide a way for you to manage access to products for users in your account.
    ```bash
    ibmcloud catalog create --name CATALOG [--catalog-description "DESCRIPTION"]
    ```
    {: codeblock}

1. Run the [ibmcloud catalog offering create](/docs/cli?topic=cli-manage-catalogs-plugin#create-offering) command to add software to your private catalog.
    ```bash
    ibmcloud catalog offering create [--catalog CATALOG-NAME] [--zipurl URL]
    ```
    {: codeblock}

    If you want to import software from a private repository, you can use a personal access token by adding [--token TOKEN] to your command.
    {: important}

1. Run the [ibmcloud catalog offering add-category](/docs/cli?topic=cli-manage-catalogs-plugin#add-category-offering) command to add a category to your product. By default, the **Developer tools** category is added to your product.
    ```bash
    ibmcloud catalog offering add-category --catalog CATALOG_NAME [--offering OFFERING] [--category CATEGORY]
    ```
    {: codeblock}

1. Run the [ibmcloud catalog offering import-version](/docs/cli?topic=cli-manage-catalogs-plugin#import-offering-version) command to import the software version that you want in your catalog.
    ```bash
    ibmcloud catalog offering import-version --catalog CATALOG --offering OFFERING_NAME --zipurl URL
    ```
    {: codeblock}

    The following shows the list of supported formats per software type:

    * Helm chart: `https://raw.githubusercontent.com/IBM/charts/master/repo/ibm-helm`
    * Node-RED Operator: `https://github.com/IBM-Cloud/operator-bundle-sample/archive/refs/tags/v0.0.3.tar.gz`
    * Operator bundle from a {{site.data.keyword.openshiftshort}} registry: For an example, select the `Akka Cluster Operator` from the list of available Operators in the Certified repository.
    * OVA image: `https://github.com/gcatalog/OVA-sample/blob/main/ova-sample.yaml`
    * Terraform template: `https://github.com/IBM-Cloud/terraform-sample/releases/tag/v1.0.0`
    * Virtual server image with Terraform: `https://github.com/IBM-Cloud/isv-vsi-product-deploy-sample/releases/download/v1.0/isv-vsi-product-deploy-sample.tar.gz`
    * Virtual server image for VPC: Select an image from the list of images that were imported into your VPC, or import a new image to your account.

1. Run the [ibmcloud catalog offering version validate](/docs/cli?topic=cli-manage-catalogs-plugin#validate-offering) command to validate the software.
    ```bash
    ibmcloud catalog offering version validate --version-locator VERSION_NUMBER --cluster CLUSTER_ID --namespace NAME [--timeout TIMEOUT] [--wait WAIT]
    ```
    {: codeblock}

    Deploying the software can take a few minutes. Run the [ibmcloud catalog offering version validate-status](/docs/cli?topic=cli-manage-catalogs-plugin#validate-status-offering) to check the validation status by querying the product validation state.
    ```bash
   ibmcloud catalog offering version validate-status --version-locator VERSION_NUMBER [--output FORMAT]

    ```
    {: codeblock}

1. Run the [ibmcloud catalog offering publish account](/docs/cli?topic=cli-manage-catalogs-plugin#publish-offering-to-account) to publish your software to users in your account.
    ```bash
    ibmcloud catalog offering publish account [--catalog CATALOG][--offering OFFERING]
    ```
    {: codeblock}



## Creating a private catalog by using the API
{: #create-catalog-api}
{: api}

Private catalogs provide a way for you to manage access to products for users in your account. You can programmatically create a private catalog by calling the Catalog Management API as shown in the following sample request. For more information, see the [Catalog Management API](/apidocs/resource-catalog/private-catalog?code=java#create-catalog) for creating a catalog.

```java
String label = "{label}";
String shortDesc = "{shortDesc}";
CreateCatalogOptions createOptions = new CreateCatalogOptions.Builder().label(label).shortDescription(shortDesc).build();
Response<Catalog> response = service.createCatalog(createOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
label = "{label}";
shortDesc = "{shortDesc}";
response = await service.createCatalog({ 'label': label, 'shortDescription': shortDesc });
console.log(response);
```
{: codeblock}
{: javascript}

```python
label = "{label}"
shortDesc = "{shortDesc}"
response = self.service.create_catalog(label=label, short_description=shortDesc)
print(response)
```
{: codeblock}
{: python}

```go
label := "{label}"
shortDesc := "{shortDesc}"
createOptions := service.NewCreateCatalogOptions()
createOptions.SetLabel(label)
createOptions.SetShortDescription(shortDesc)
_, response, _ := service.CreateCatalog(createOptions)
fmt.Println(response)
```
{: codeblock}
{: go}

## Importing software to your private catalog by using the API
{: #import-product-api}
{: api}

You can programmatically import software to your catalog by calling the Catalog Management API as shown in the following sample request. This API creates the software and imports it as well. For detailed information about the API, see [Catalog Management API](/apidocs/resource-catalog/private-catalog?code=go#import-offering).

```java
id = "{id}";
offeringURL = "{offeringURL}";
ImportOfferingOptions offeringOptions = new ImportOfferingOptions.Builder().catalogIdentifier(id).zipurl(offeringURL).build();
Response<Offering> response = service.importOffering(offeringOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
id = "{id}";
offeringURL = "{offeringURL}";
response = await service.importOffering({ 'catalogIdentifier': id, 'zipurl': offeringURL });
console.log(response);
```
{: codeblock}
{: javascript}

```python
id = "{id}"
offeringURL = "{offeringURL}"
response = self.service.import_offering(catalog_identifier=id, zipurl=offeringURL)
print(response)
```
{: codeblock}
{: python}

```go
id := "{id}"
offeringURL := "{offeringURL}"
offeringOptions := service.NewImportOfferingOptions(id, offeringURL)
_, response, _ := service.ImportOffering(offeringOptions)
fmt.Println(response)
```
{: codeblock}
{: go}

## Validating your software by using the API
{: #validate-product-api}
{: api}

You can programmatically validate your product to by calling the Catalog Management API as shown in the following sample request. This process can take several minutes. For detailed information about the API, see [Catalog Management API](/apidocs/resource-catalog/private-catalog?code=java#validate-install).

```java
String authRefreshToken = "{authRefreshToken}";
String versionLocator = "{versionLocator}";
ValidationInstallOptions installOptions = new ValidationInstallOptions.Builder().xAuthRefreshToken(authRefreshToken).versionLocId(versionLocator).build();
Response<Void> response = service.validationInstall(installOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
versionLocator = "{versionLocator}";
authRefreshToken = "{authRefreshToken}";
response = await service.validationInstall({ 'versionLocatorId': versionLocator, 'xAuthRefreshToken': authRefreshToken });
console.log(response);
```
{: codeblock}
{: javascript}

```python
authRefreshToken="{authRefreshToken}"
versionLocator = "{versionLocator}"
response = self.service.validation_install(version_locator_id=versionLocator, x_auth_refresh_token=authRefreshToken)
print(response)
```
{: codeblock}
{: python}

```go
versionLocator := "{versionLocator}"
authRefreshToken := "{authRefreshToken}"
installOptions := service.NewValidationInstallOptions(versionLocator, authRefreshToken)
response, _ := service.ValidationInstall(installOptions)
fmt.Println(response)
```
{: codeblock}
{: go}

## Publishing your software to your account by using the API
{: #publish-product-api}
{: api}

You can programmatically publish your software to your account by calling the Catalog Management API as shown in the following sample request.

```java
String versionLocator = "{versionLocator}";
AccountPublishVersionOptions publishOption = new AccountPublishVersionOptions.Builder().versionLocId(versionLocator).build();
Response<Void> response = service.accountPublishVersion(publishOption).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
versionLocator = "{versionLocator}";
response = await service.accountPublishVersion({ 'versionLocId': versionLocator});
console.log(response);
```
{: codeblock}
{: javascript}

```python
versionLocator = "{versionLocator}"
response = self.service.account_publish_version(version_loc_id=versionLocator)
print(response)
```
{: codeblock}
{: python}

```go
versionLocator := "{versionLocator}"
publishOptions := service.NewAccountPublishVersionOptions(versionLocator)
response, _ := service.AccountPublishVersion(publishOptions)
fmt.Println(response)
```
{: codeblock}
{: go}

## Creating a private catalog by using Terraform
{: #create-catalog-terraform}
{: terraform}

Use the following steps to create a private catalog by using Terraform.

1. Add your argument to your `main.tf` file. The following example creates a private catalog by using the `ibm_cm_catalog` resource, where `label` is a display name to identify the catalog.

   ```terraform
   resource "ibm_cm_catalog" "cm_catalog" {
   label = "label"
   short_description = "short_description"
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Catalog Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_catalog){: external} page.

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

## Importing a product to your catalog by using Terraform
{: #create-cicd-product-terraform}
{: terraform}

Use the following steps to import a product to your private catalog by using Terraform.

1. Add your argument to your `main.tf` file. The following example adds your product by using the `ibm_cm_offering` resource, where `label` is a display name to identify the product.

   ```terraform
   resource "ibm_cm_offering" "cm_offering" {
   catalog_id = "catalog_id"
   label = "label"
   tags = [ "tags" ]
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Catalog Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_offering){: external} page.

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

## Importing a version of your software by using Terraform
{: #create-cicd-version-terraform}
{: terraform}

After you add your product, use the following steps to add a version of your software by using Terraform.

1. Add your argument to your `main.tf` file. The following example accesses the software version by using the `cm_version` resource, where `offering_id` identifies the software.

   ```terraform
   resource "cm_version" "cm_version" {
   catalog_identifier = "catalog_identifier"
   offering_id = "offering_id"
   zipurl = "zipurl"
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Catalog Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/cm_version){: external} page.

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
