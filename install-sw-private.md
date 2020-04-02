---

copyright:
  years: 2020
lastupdated: "2020-04-02"

keywords: catalog, catalogs, private catalogs, install software, software product 

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Installing software from your private catalog
{: #install-sw}

In this tutorial, you install the apache-two-instances product that was previously added to the My first catalog catalog. 
{: shortdesc} 

## Before you begin
{: #prereq-installsw}

To complete this tutorial, you need to be assigned the following roles:

* Viewer role on the catalog management service
* Administrator and manager roles on the Kubernetes cluster service
* Manager role on the Schematics service
* Viewer role on all resource groups

For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
{: tip}

## Install the software by using the console
{: #installsw-console}

1. Click **Catalog** in the console menu bar.
2. Select **My first catalog** from the list of catalogs. 
1. Click **Private** > **apache-two-instances**.
1. Select a Kubernetes cluster, and enter a namespace value.
1. Click **Install** to install the Apache Helm chart.

### Success criteria
{: #create-success-offering}

You successfully completed this tutorial if the following items are true:

1. You can navigate to the Private tab and view the apache-two-instances product.
2. You can install the software.

## Next steps
{: next-update}

A user with access to your private catalog updates the software. See [Updating software in your private catalog](/docs/account?topic=account-update-private) for more information.



