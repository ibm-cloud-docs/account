---

copyright:
  years: 2019, 2021
lastupdated: "2021-06-07"

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

You can build and onboard software solutions to a private catalog to then share them with your organization.
{: shortdesc} 

## Before you begin
{: #prereq-create}

1. Review the list of supported software that you can onboard:

  * Helm charts
  * Terraform templates
  * OVA images deployed on VMware vCenter Server
  * Virtual server images with Terraform deployed on VPC infrastructure
  * Operators deployed on Red Hat OpenShift
  
1. Upload your soure code in a GitHub repository. For more information, see [Managing releases in a repository](https://docs.github.com/en/github/administering-a-repository/managing-releases-in-a-repository){: external}.
1. Make sure you're assigned the following IAM access:

  * Editor role on the catalog management service
  * Viewer role on all resource groups in your account
  * Writer role on the {{site.data.keyword.secrets-manager_short}} service

1. Install the IBM Cloud CLI and the IBM Cloud Schematics plug-in. See [Setting up the CLI](/docs/schematics?topic=schematics-setup-cli) for more information.

For containerized apps, complete the following prerequisites:

  1. Create your [Kubernetes cluster](/docs/containers?topic=containers-getting-started) or [Red Hat OpenShift cluster](/docs/openshift?topic=openshift-getting-started).
  2. For deployments to {{site.data.keyword.cloud_notm}} Kubernetes Service, [set up your Helm chart](/docs/containers?topic=containers-helm). 
  3. For deployments to Red Hat OpenShift, set up your [Helm chart](/docs/openshift?topic=openshift-helm) or [operator](/docs/openshift?topic=openshift-operators).

For virtual server images, complete the following prerequisites:

  1. Review the list of [supported images](/docs/vpc?topic=vpc-about-images).
  2. Create your [Terraform template](/docs/schematics?topic=schematics-getting-started).
  3. Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and add your image to a bucket.
 

## Creating your private catalog
{: #create-catalog}
{: ui}

1. Go to **Manage** > **Catalogs**, and select **Private catalogs**. 
2. Click **Create**.
3. Select **Product default** as the catalog type. 
4. Enter a name and description of your catalog.
5. Select whether to exclude all products in the {{site.data.keyword.cloud}} catalog from your catalog.
6. Click **Create**.

## Adding a product to your catalog in the console
{: #add-public-repo}
{: ui}

Complete the following steps to add a product to your catalog:

1. Click **Private catalogs**, and select your private catalog from the list.
1. Click **Private products** > **Add**.
1. Select whether you are adding your product from a private or public repository. 
1. Enter your repository's URL or TGZ archive. 
1. If you're adding your product from a private repository, you can choose to provide a personal access token or you can use a secret. Instead of giving users a personal access token, you can give them access to a secret and add the token to a secret and centrally manage all tokens and access the secret allows.

  * If you're using a personal access token, select **No** to indicate you aren't using a secret and provide your personal access token.
  * If you're using a secret, select **Yes** and click **Select from Secrets Manager**. Select your service instance, secret group, and secret. If you don't see your secret, make sure you're using the correct secret group and service instance. 
    
    The message `No service instance available` might be displayed if you haven't created a secret or if you don't have the correct access to use secrets, even if you have service instances that are created. 
    {: note}

1. Select a category and your deployment target.
1. Click **Add**. 

## Publishing your product in the console
{: #validating-software}
{: ui}

After you add your product to your catalog, you're ready to publish it to your account. Complete the following steps to validate and publish your product:

1. Review the product details by selecting **Configure product**, **Add license**, and **Edit readme**. 
1. Select **Validate product**. 
1. Select a cluster. 
1. Click **Validate** to ensure that your product can be installed successfully. This step is required before you can make it available for users in your account, and the validation can take several minutes. In the Validation summary section, the status is displayed as Validated when the deployment is complete. 
1. Click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg), and select **Publish to account** to make your product available to all users in your account through your private catalog.


## Adding a product to your catalog by using the CLI
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

## Adding a product to your catalog by using the API
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
