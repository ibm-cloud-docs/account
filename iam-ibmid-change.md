---

copyright:

  years: 2021, 2023
lastupdated: "2023-07-20"

keywords: IBMid change, credentials, ID, new ID

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Changing a user's IBMid
{: #change-ibm-id}


As an account owner, you can update a user's IBMid. The new IBMid that you use to replace the current IBMid must already exist.
{: shortdesc}

The IBMid you're replacing is removed from the account. If you need the existing IBMid to continue to be a member of the account, you must invite the user again and reestablish their access.

Account owners can't change their own IBMid.
{: note}

## Before you begin
{: #id-update-prereq}

To change an IBMid, the replacement ID must already exist. If you're not sure if the new IBMid exists, users can go to [My IBM](https://myibm.ibm.com) and click **Create an IBMid**. If you enter an email address that corresponds to a federated identity provider (IdP) domain, IBMid redirects you to that IdP's login page. First-time logins to {{site.data.keyword.IBM}} using a federated IdP triggers the creation of a new IBMid. Otherwise, follow the steps to create the ID. The email address that is used becomes the user's new replacement IBMid.

After the user ensures that the new IBMid exists, complete the following steps:

1. Go to **Manage** > **Access (IAM)** > **Users** in the {{site.data.keyword.cloud}} console, and select the user whose IBMid you want to update.
2. In the **Details** section, click **Update IBMid**.
3. Enter the new IBMid, and click **Update**. 

The user can now log in to ibm.com with their new IMBid and continue working in the {{site.data.keyword.Bluemix_notm}} account with the access assigned to their previously used IBMid.
