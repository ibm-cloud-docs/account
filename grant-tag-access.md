---

copyright:

  years: 2018-2020
lastupdated: "2020-07-30"

keywords: tagging, enabling others to tag, tagging permissions

subcollection: account

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}


# Granting users access to tag resources
{: #access}

As the account owner, you might want to delegate some of the responsibility of tagging resources. For users to add tags to a resource, you must grant them the appropriate access. Use {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) access policies to grant users access to resources in a resource group. Use Cloud Foundry roles to grant users access to resources in a Cloud Foundry org and space.
{: shortdesc}

## Tagging permissions
{: #tagging-permissions}

Any user in an account can view tags. When a resource is tagged, all users who have read access to the resource can view the tag. To add or remove a tag from a resource, certain access roles or permissions are required depending on the resource type. See the following table to understand what role is required for each resource type.


| Resource Type | Role |
|--------|---------------|
| IAM-enabled | Editor or administrator on the resource |
| Cloud Foundry | Developer on the space that the resource belongs to  |
| Bare metal on classic infrastructure| View hardware details and access to a specific set of services or all bare metal servers |
| Dedicated Hosts on classic infrastructure | View virtual dedicated host details and access to a specific set of services or all dedicated hosts |
| Virtual Server on classic infrastructure | View virtual server details and access to a specific set of services or all virtual servers |
| Cloud Object Storage S3 on classic infrastructure | Storage manage permission |
| File Storage on classic infrastructure | Storage manage permission |
| Evault backup on classic infrastructure | Storage manage permission |
| Content Delivery Network on classic infrastructure | Manage CDN account permission |
| Direct Link on classic infrastructure | Account member |
| Hardware Firewall | Manage Firewalls |
| FortiGate Security Appliance | Manage Firewalls |
| IBM Cloud Load Balancer | Manage Load Balancers |
| Gateway Appliance | Manage Network Gateways |
{: caption="Table 1. Required roles for adding and removing tags" caption-side="top"}
{: summary="This is a simple data table."}


## Granting users access to tag IAM-enabled resources
{: #iam-managed}

Complete the following steps to assign the editor role for a user to tag IAM-enabled resources: 

  1. From the {{site.data.keyword.Bluemix_notm}} console, click **Manage > Access (IAM)**, and select **Access groups**.
  2. Click **Create**.
  3. Enter a group name and description, and click **Create**.
  4. Add users to the access group by clicking **Add users**, selecting one or more users from the table, and clicking **Add to group**.
  5. Click **Access policies** > **Assign access**.
  6. Select **All Identity and Access enabled services** or a specific service as the type of access to assign.
  7. Select a specific region or accept the default **All regions** option. 
  8. Select **Editor** from the list of platform access roles, and click **Add**.
  9. Review your access summary, and click **Assign**. 

## Granting users access to tag Cloud Foundry resources
{: #cf_tag_access}

Complete the following steps to assign the developer space role for a user to tag Cloud Foundry resources:

1. Click **Manage > Access (IAM)**, and select **Users**.
2. Click the user's name from the table.
3. Click **Cloud Foundry access** > **Assign organization**.
5. Select the organization that contains the service instance you want to provide the user access to.
6. Select a specific region or accept the default **All current regions** option. 
7. Select **Developer** as the space role.
8. Click **Save role**.

## Granting users access to tag classic infrastructure resources
{: #classic-infra}

The taggable resources for classic infrastructure are Virtual Guest, Virtual Dedicated Host, Network Application Delivery Controller, Gateway Member, Subnet, VLAN, and VLAN Firewall (Dedicated). Complete the following steps to assign the Manager service access role for a user to tag classic infrastructure services:

  1. Click **Manage > Access (IAM)**, and select **Users**.
  2. Click the user's name from the table.
  3. Click **Classic infrastructure**
  4. From the **Permissions** tab, expand the **Devices** category.
  5. Select **View Hardware Details** and **View Virtual Server Details**. If you need to assign access to Cloud Object Storage S3, File Storage, or Evault Backup, assign the **Storage manage** permission. If you need to assign access to Content Delivery network, assign the **Manage CDN Account** permission.
  6. Click **Save**.
  7. Click the **Devices** tab.
  8. Select **All bare metal servers** or **All virtual servers** depending on the resource that you want the user to be able to tag.
