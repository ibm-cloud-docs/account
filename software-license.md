---


copyright:
  years: 2020
lastupdated: "2020-04-13"

keywords: license, entitlement, software, passport advantage, cloud pak, binding a license, PPA, part number

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}

# Assigning software licenses to your account
{: #software-license}

To install software products, such as Cloud Paks, in {{site.data.keyword.cloud}}, you must have a license assigned to your account. You're entitled to install a specific version of the software for a specific period of time, for example, one year. Licenses, which are also referred to as entitlements, are purchased and acquired through {{site.data.keyword.IBM}} Passport Advantage. 
{: shortdesc}

## Acquiring a license 
{: #acquire-license}

In most cases, someone in a procurement or financial role in your organization works with an {{site.data.keyword.cloud_notm}} sales representative to purchase the license through [{{site.data.keyword.IBM_notm}} Passport Advantage](https://www.ibm.com/software/passportadvantage/index.html). A part number is associated with the license for the software product to be used in {{site.data.keyword.cloud_notm}}. The person acquiring the license is not the same person who typically installs the software in the {{site.data.keyword.cloud_notm}} account. After a sales representative acquires the license through the Software Quote Order tool, it must be assigned to each account that requires entitlement for use of the software in {{site.data.keyword.cloud_notm}}. 

## Assigning a license to an account
{: #assign-license}

If the procurement focal is not the owner of the account to which this license must be assigned, they must have an IAM access policy on the [License and entitlement account management service](/docs/iam?topic=iam-account-services#license-entitlement-management). 

As an administrator, you can create entitlements by assigning it, and you can view, update, or delete any entitlements in the account.
{: tip}

Complete the following steps to assign a license to an account:
1. Log in to the console, and go to the Catalog page.
1. Search for the software product that you have a license for, and select it. 
1. On the Create page, the available entitlements for the software in the account are displayed in the Assign a license section. Select the one you want to use.
1. Click **Assign**. 

  If the **Assign** button is disabled, you don't have the correct access to assign the license to this account. Contact the account owner to update your access.
  {: note}

Check the summary details to confirm that the license is assigned to the account. A license can't be removed after it's assigned. 

## Installing software 
{: #install-software}

After the license is assigned to an account, all users can install the software depending on their access. The license is automatically available for the software after a user selects it from the catalog. To verify that the license is available, check the Summary section on the Create page for the software. All assigned licenses in the account are listed. 

Any user that is a member of the account can install the software if the following requirements are met:

   * A user is assigned the viewer role or higher on the software and a resource group in the account
   * A user is assigned the administrator and manager roles on the cluster
   * A user is assigned the manager role on the Schematics service

For specific details about the deployment values and the minimum required configuration options, review the Readme tab or the documentation linked from the product in the catalog.
{: note}

Complete the following steps to install the software:
1. Select a cluster and provide any required information to configure your installation.
1. Click **Install**.
