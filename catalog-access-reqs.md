---

copyright:
  years: 2020
lastupdated: "2020-08-14"

keywords: catalog, private catalogs, IAM access, roles, private catalog service, access groups, permissions

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Assigning catalog management access
{: #catalog-access}

As the account owner, you assign users specific catalog management access depending on what tasks they are performing. To streamline the process of assigning access, you can use access groups to organize a set of users into a single entity. That way, you can assign a single policy to the group one time, and then add or remove users from the group as needed. 
{: shortdesc}

For more details, see [Managing access in {{site.data.keyword.cloud_notm}}](/docs/account?topic=account-cloudaccess).

## Setting up your access groups
{: #catalog-access-groups}

See the following sections for details about creating your access groups and assigning specific IAM policies to each one.

### Administrator access
{: #catalog-access-admin}

Administrator access is required for setting account-level filters to the {{site.data.keyword.cloud_notm}} catalog.   

1. Log in to your {{site.data.keyword.cloud_notm}} account.
2. Go to **Manage** > **Access (IAM)** > **Access groups**.
4. Click **Create**.
5. Enter `private-catalog-admins` as the group name, and click **Create**.
6. Click **Access policies** > **Assign access**.
7. Select **Account management**.
8. Select **Catalog Management** from the **What type of access do you want to assign?** list.
9. Select the catalog that you want users to access.
9. In the Platform access section, select the **Administrator** role.
10. Click **Add** > **Assign**.

### Editor access
{: #catalog-access-editor}

Editor access is required for creating private catalogs, setting filters at the private catalog level, adding your software to your private catalog, and updating, deprecating, and restoring your software.    

1. Go to **Access groups**, and click **Create**.
2. Enter `private-catalog-editors` as the group name, and click **Create**.
6. Click **Access policies** > **Assign access**.
7. Select **Account management**.
8. Select **Catalog Management** from the **What type of access do you want to assign?** list.
9. Select the catalog that you want users to access.
9. In the Platform access section, select the **Editor** role.
10. Click **Add**.
11. Select **IAM services** > **Kubernetes Service**.
12. Select your cluster, and then select the **Administrator** and **Manager** roles.
13. Click **Add**.
14. Select **IAM services** > **Schematics**.
15. Select the **Manager** role.
16. Click **Add** > **Assign**.

### Viewer access
{: #catalog-access-viewer}

Viewer access is required for viewing private catalogs, the filtered {{site.data.keyword.cloud_notm}} catalog, and the filter settings.  

1. Go to **Access groups**, and click **Create**.
2. Enter `private-catalog-viewers` as the group name, and click **Create**.
6. Click **Access policies** > **Assign access**.
7. Select **Account management**.
8. Select **Catalog Management** from the **What type of access do you want to assign?** list.
9. Select the catalog that you want users to access.
9. In the Platform access section, select the **Viewer** role.
10. Click **Add** > **Assign**.

You also need to have viewer access on the resource group to which your private catalog is assigned. You can assign your private catalog to a resource group when you complete the steps for creating your private catalog. For more information, see [Customizing the IBM Cloud catalog for all account users](/docs/account?topic=account-filter-account). 

To assign viewer access to your private catalog's resource group, use the following steps:

1. Go to **Users** and select the user. 
1. Select **Access policies** > **Assign access**. 
1. From the **Assign users additional access** section, select **IAM services**.  
1. Select **All Identity and Access enabled services** and your private catalogs resource group from the **What type of access do you want to assign?** list.
1. In the Platform access section, select the **Viewer** role.
1. Click **Add** > **Assign**.

## Add users to your access groups
{: #catalog-access-users}

1. Go to **Users**, and click **Invite users**.
2. Specify the email addresses of the users. If you are inviting more than one user with a single invitation, they are all assigned the same access.
3. Select one of the three access groups you previously created, and click **Add** > **Invite**.
4. Repeat the steps to add users to your other access groups. 














