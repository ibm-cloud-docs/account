---

copyright:
  years: 2019, 2023
lastupdated: "2023-03-02"

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
{:terraform: .ph data-hd-interface='terraform'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Publishing products that use Helm charts
{: #publishhelm}

The process to onboard software to your account includes importing a version to a private catalog, validating that the version can be successfully installed on the target infrastructure that you require, and publishing the software to your account. The software is then available to users in your account.
{: shortdesc}

## Before you begin
{: #publishhelm-prereq}

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









## Configuring the software
{: #publishhelm-cfg}
{: ui}

### Helm chart
{: #catalog-config-helm}
{: ui}

1. From the version list that's displayed on the product details page, click the row that contains your software.
1. Review the version details, and click **Next**.
1. Configure the preinstallation, and click **Next**.
1. Configure the deployment details by setting the access that's required to run the installation script and setting the deployment values, and click **Next**.

## Adding license agreements
{: #publishhelm-eula}
{: ui}

Provide the URLs to the license agreements that users are required to accept when they install the product. The license agreements are in addition to the {{site.data.keyword.cloud_notm}} Services Agreement.

1. Click **Add license agreements** > **Add license**.
1. Enter the name and URL, and click **Update**.
1. After you enter all additional license agreements, click **Next**.

## Editing your readme file
{: #publishhelm-readme}
{: ui}

When users install the software, they can select the link to your readme file to view product information. The information in the Readme link is generated from the readme file that you uploaded to your source repository.

1. From the Edit readme tab, preview how the information in the readme file will be displayed to users when they install the software.
1. To make updates, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") next to the Readme section title.
1. Click **Save**.
1. Click **Next**.

## Validating the software
{: #publishhelm-validate}
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

## Publishing the software
{: #publishhelm-pub}
{: ui}

After you validate your software, you're ready to make it available to all users who have access to your private catalog. Open the **Actions** menu, and select **Publish to account**.
