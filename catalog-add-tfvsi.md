---

copyright:
  years: 2019, 2023
lastupdated: "2023-03-02"

keywords: catalog, catalogs, private catalogs, account catalogs, catalog visibility, software visibility, import software

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Adding products that use Terraform templates with virtual server images
{: #addtfvsi}

The process to onboard software to your account includes importing a version to a private catalog, validating that the version can be successfully installed on the target infrastructure that you require, and publishing the software to your account. The software is then available to users in your account.
{: shortdesc}

## Before you begin
{: #addtfvsi-prereq}

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.

1. Review the list of software that you can onboard:

   * Helm charts on Kubernetes and {{site.data.keyword.openshiftshort}} clusters
   * Terraform templates
   * OVA images deployed on VMware Solutions Dedicated - vCenter Server
   * Virtual server images with Terraform deployed on VPC infrastructure
   * Operators with TGZ file from GitHub or GitLab repositories
   * Operator bundles from Red Hat OpenShift registries

1. Upload your source code to a release in your GitHub or GitLab repository. See [Setting up your source code repository](/docs/sell?topic=sell-source-repo-setup).
1. Make sure you're assigned the following [IAM access](/docs/account?topic=account-groups):

   * Editor role on the catalog management service
   * Viewer role on all resource groups in your account
   * Writer role on the {{site.data.keyword.secrets-manager_short}} service

1. Install the {{site.data.keyword.cloud_notm}} CLI and the {{site.data.keyword.bplong_notm}} plug-in. See [Setting up the CLI](/docs/schematics?topic=schematics-setup-cli) for more information.

For containerized apps, complete the following prerequisites:

   1. Create your [Kubernetes cluster](/docs/containers?topic=containers-getting-started) or [Red Hat OpenShift cluster](/docs/openshift?topic=openshift-getting-started).
   2. For deployments to {{site.data.keyword.cloud_notm}} Kubernetes Service, [set up your Helm chart](/docs/containers?topic=containers-helm).
   3. For deployments to Red Hat OpenShift, set up your [Helm chart](/docs/openshift?topic=openshift-helm) or [Operator](/docs/openshift?topic=openshift-operators).

For virtual server images, complete the following prerequisites:

   1. Review the list of [supported images](/docs/vpc?topic=vpc-about-images).
   2. Create your [Terraform template](/docs/schematics?topic=schematics-create-tf-config).
   3. Create an instance of [{{site.data.keyword.cloud_notm}} Object Storage](/docs/cloud-object-storage?topic=cloud-object-storage-getting-started-cloud-object-storage) and add your image to a bucket.







## Importing software to your private catalog
{: #addtfvsi-import}
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

1. If applicable, enter the version of the software in the format of major version, minor version, and revision. For example. enter version 1.1.2.
1. Select a catalog category for the product. Categories are used to organize products in the {{site.data.keyword.cloud_notm}} catalog based on function, use, or common solutions.
1. Click **Add version**.

## Defining your product details
{: #addtfvsi-details}
