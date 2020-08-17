---

copyright:
  years: 2020
lastupdated: "2020-08-17"

keywords: catalog, catalogs, private catalogs, install software, software product, deployment target

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Installing software from a private catalog
{: #install-sw}

You can install software that's been added to a private catalog if you're the catalog owner or you have the required access to it. 
{: shortdesc} 

## Before you begin
{: #prereq-installsw}

To complete this task, you need to be assigned the following roles:

* Viewer role on the catalog management service
* Administrator and manager roles on the cluster
* Viewer role on all resource groups

For more information, see [Assigning catalog management access](/docs/account?topic=account-catalog-access).

## Installing software by using the console
{: #installsw-console}

1. Click **Catalog** in the console menu bar.
2. Select the name of the catalog from the list of catalogs. 
1. Click **Private** > the software type that you want to install.
1. Select a cluster, and enter one of the following values:

   * A namespace if your deployment target is IBM Kubernetes Service. 
   * A project name if your deployment target is Red Hat OpenShift. 
   
  You can install software to clusters that are deployed to classic {{site.data.keyword.cloud}} infrastructure. Installing software to clusters that are deployed to {{site.data.keyword.cloud_notm}} Virtual Private Cloud is currently not supported.
  {: note}
  
1. Click **Install**.



