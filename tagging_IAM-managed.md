---

copyright:

  years: 2018
lastupdated: "2018-11-12"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:notes: .note}


# Enabling access for IAM-managed resources
{: #tagging-IAM}

You can tag related resources and view them throughout your account by filtering by a tag in your resource list. Tags can help you organize and find the resources that are important to you and help you monitor costs. To see a full list of tags on your account, go to **Manage > Account**, and select **Tags**. 
{: shortdesc}


## Tagging permissions
{: #tagging-permissions}

Anyone on the account can see the tags on resources and they can use the tags to organize resources in the account. But to attach or remove a tag from a resource, you must have a role on that resource. For IAM-managed resources like a resource controller-managed service or a Kubernetes Cluster, a user must be an `Editor` or an `Administrator` on the resource to attach a tag. Additionally, anyone on the account can delete a tag.   
When a tag is removed from a resource, it still might be attached to another resource. To must remove a tag from all resources to delete it.
{: note}


## Granting access
{: #access}

For users to add tags to a resource, they must be assigned the appropriate access. Access to services that belong to a resource group are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) access policies. 

To provide access to tag IAM-enabled services, complete the following steps:
1. Click **Manage > Access (IAM)**, and select **Users**.
2. Select the name for the user that you want to provide access to.
3. Click the **Access policies** tab.
4. Click **Assign access**.
5. Select the **Assign access to resources** option.
6. Select a specific service or **All Identity and Access enabled services**.
7. Select the **Editor** platform access role.
8. Click **Assign**.

