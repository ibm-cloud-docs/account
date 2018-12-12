---

copyright:

  years: 2018
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:notes: .note}


# Enabling access for classic infrastructure resources
{: #tagging-classic-infra}

You can tag related resources and view them throughout your account by filtering by a tag in your resource list. Tags can help you organize and find the resources that are important to you and help you monitor costs. To see a full list of tags on your account, go to **Manage > Account**, and select **Tags**. 
{: shortdesc}


## Tagging permissions
{: #tagging-permissions}

Anyone on the account can see the tags on resources and they can use the tags to organize resources in the account. But to attach or remove a tag from a resource, you must have a role on that resource. To attach or remove tags on one of these resources, you must have `view hardware details` or `view virtual server details` permissions and device access to servers. To enable the tagging capability on storage devices like Cloud Object Storage, you must have the `Manager` service access role.


## Granting access
{: #access}

For users on account to add tags to a resource, they be assigned the appropriate access. To provide access to tag classic infrastructure services, complete the following steps: 
1. Click **Manage > Access (IAM)**, and select **Users**.
2. Select the name for the user that you want to provide access to.
3. Click the **Classic infrastructure** tab.
4. From the **Permissions** tab, click the arrow in the Devices category to expand the list of permissions. 
4. Check the boxes for `View Hardware Details` and `View Virtual Server Details`.  
8. Click **Save**.


