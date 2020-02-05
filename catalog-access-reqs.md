---

copyright:
  years: 2020
lastupdated: "2020-02-05"

keywords: catalog, private catalogs, IAM access, roles, private catalog service

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Assigning users access
{: #catalog-access}

As the account owner, you assign users specific access depending on what tasks they are performing. To streamline the process of assigning access, you can use access groups to organize a set of users into a single entity. That way, you can assign a single policy to the group one time, and then add or remove users from the group as needed. 
{: shortdesc}

For more details about access management, see [Managing access in {{site.data.keyword.cloud_notm}}](/docs/iam?topic=iam-cloudaccess).

This feature is available only in a closed beta program. If you’re interested in participating, contact kala.nenkova@ibm.com.
{: note}

## Set up your access groups
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
7. Select **IAM services**.
8. From the What type of access do you want to assign section, select **Private Catalog** and confirm that the **Account** option is selected.
9. In the Platform access section, select the **Administrator** role.
10. Click **Add** > **Assign**.

### Editor access
{: #catalog-access-editor}

Editor access is required for creating private catalogs, setting filters at the private catalog level, adding your software to your private catalog, and updating, deprecating, and restoring your software.    

1. Go to **Access groups**, and click **Create**.
2. Enter `private-catalog-editors` as the group name, and click **Create**.
6. Click **Access policies** > **Assign access**.
7. Select **IAM services**.
8. From the What type of access do you want to assign section, select **Private Catalog** and confirm that the **Account** option is selected.
9. In the Platform access section, select the **Editor** role.
10. Click **Add** > **Assign**.

### Viewer access
{: #catalog-access-viewer}

Viewer access is required for viewing private catalogs, the filtered {{site.data.keyword.cloud_notm}} catalog, and the filter settings.   

1. Go to **Access groups**, and click **Create**.
2. Enter `private-catalog-viewers` as the group name, and click **Create**.
6. Click **Access policies** > **Assign access**.
7. Select **IAM services**.
8. From the What type of access do you want to assign section, select **Private Catalog** and confirm that the **Account** option is selected.
9. In the Platform access section, select the **Viewer** role.
10. Click **Add** > **Assign**.

## Add users to your access groups
{: #catalog-access-users}

1. Go to **Users**, and click **Invite users**.
2. Specify the email addresses of the users. If you are inviting more than one user with a single invitation, they are all assigned the same access.
3. Select one of the three access groups you previously created, and click **Add** > **Invite**.
4. Repeat the steps to add users to your other access groups. 














