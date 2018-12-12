---

copyright:

  years: 2018
lastupdated: "2018-11-14"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:notes: .note}


# Enabling access for Cloud Foundry resources
{: #tagging-CF}

You can tag related resources and view them throughout your account by filtering by a tag in your resource list. Tags can help you organize and find the resources that are important to you and help you monitor costs. To see a full list of tags on your account, go to **Manage > Account**, and select **Tags**. 
{: shortdesc}


## Tagging permissions
{: #tagging-permissions}

Anyone on the account can see the tags on resources and they can use the tags to organize resources in the account. But to attach or remove a tag from a resource, you must have a role on that resource. Cloud Foundry resources include Cloud Foundry apps and service instances. To attach and remove tags, you must have a space `developer` role within that specific resource. Developers can create and manage Cloud Foundry apps and services, view logs and reports for a space, and they are the only users with access to take tagging actions on resources.  


## Granting access
{: #access}

For users on account to add tags to a resource, they be assigned the appropriate access. Access to services that belong to a Cloud Foundry org and space are managed by Cloud Foundry org and space roles. 

To provide access to tag Cloud Foundry services, complete the following steps:
1. Click **Manage > Access (IAM)**, and select **Users**.
2. Select the name for the user that you want to provide access to.
3. Click the **Cloud Foundry access** tab. 
4. Click **Assign Organization**.
5. Expand and select the `Organization` with the service instance that you want to provide the user access to. 
6. Select the `Region`. 
7. Select the `Developer` space role.
8. Click **Save role**.

If the user isn't already assigned to an organization, click **Assign organization**. From there, you can select the org and spaces that the user needs to be added to with the necessary roles assigned. 
{: tip} 

