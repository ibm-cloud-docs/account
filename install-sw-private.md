---

copyright:
  years: 2020
lastupdated: "2020-02-04"

keywords: catalog, catalogs, private catalogs, install software, software offering 

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Installing a private software offering
{: #install-sw}

In this tutorial, you install the apache-two-instances offering that was previously added to the My first catalog catalog. 
{: shortdesc} 

This feature is available only in a closed beta. If you’re interested in participating, contact kala.nenkova@ibm.com.
{: note}

## Before you begin
{: #prereq-installsw}

To complete this tutorial, you need to be assigned the following roles:

* Viewer on the private catalog service or a specific private catalog
* Administrator and manager roles on the Kubernetes cluster service
* Manager role on the Schematics service
* Viewer role on all resource groups

If you don't see what you're expecting in the console based on your permissions, try refreshing your session by going to https://cloud.ibm.com/login.
{: tip}

## Install a private software offering in the console
{: #installsw-console}

1. Click **Catalog** in the console menu bar.
2. Select **My first catalog** from the list of catalogs. 
1. Click the Private tab, and select **apache-two-instances**.
1. Select a Kubernetes cluster, and enter a namespace value.
1. Click **Install** to install the Apache Helm chart.

### Success criteria
{: #create-success-offering}

You successfully completed this tutorial if the following items are true:

1. The Private tab is displayed in the {{site.data.keyword.cloud_notm}} catalog. 
1. You can click the Private tab, and view the apache-two-instances offering.
2. You can install the apache-two-instances offering offering.

## Next steps
{: next-update}

A user with access to your private catalog updates the apache-two-instances offering. See [Updating a software offering in your private catalog](/docs/account?topic=account-update-private) for more information.



