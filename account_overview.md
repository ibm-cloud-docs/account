---

copyright:

  years: 2018
lastupdated: "2018-07-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Account hierarchy
{: #overview}

Your {{site.data.keyword.Bluemix}} account includes many interacting components and systems. The following diagram and explanation for each component are intended to help you understand how certain components are interrelated, or connected, and how access works across the account. 

![{{site.data.keyword.Bluemix_notm}} account diagram](images/account_diagram.svg "{{site.data.keyword.Bluemix_notm}} account diagram")

For a larger view of the diagram, [click here](https://console.stage1.bluemix.net/docs/api/content/account/images/account_diagram.svg).

Within the diagram, there are two main concepts for the components in the account hierarchy that are important to understand. The use of the solid lines and the dotted lines help illustrate that some components are contained within others, for example, users are added to access groups or Cloud Foundry orgs. However, some components interact with others for the purpose of providing access instead of membership. For example, users are given access to resource groups but are not members of a resource group the same way they are for access groups. These concepts are also explained in the following sections.

<dl>
<dt>Users</dt>
<dd>Users are invited to the account and given access to the different resources within the account.</dd>
<dt>Service IDs</dt>
<dd>A service ID identifies a service or application similar to how a user ID identifies a user. You can use a service ID that you create to enable an application outside of {{site.data.keyword.Bluemix_notm}} access to your {{site.data.keyword.Bluemix_notm}} services. You can assign specific access policies to the service ID that restrict permissions for using specific services, or even combine permissions for accessing different services. Since service IDs are not tied to a specific user, if a user happens to leave an organization and is deleted from the account, the service ID remains ensuring that your application or service stays up and running. FOr more information, see [Creating and working with service IDs](/docs/iam/serviceid.html#serviceids).</dd>
<dt>Service instances or resources</dt>
<dd>Services in {{site.data.keyword.Bluemix_notm}} are resource group or Cloud Foundry-based. Service instances that can be added to a resource group and managed by using {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) are called resources. Service instances that are added to Cloud Foundry orgs and spaces have a separate access management system by using Cloud Foundry roles. For more information, see [What is a resource?](/docs/resources/acct_resources.html#resource)</dd>
<dt>API keys</dt>
<dd>An application programming interface key (API key) is a unique code that is passed in to an application programming interface (API) to identify the calling application or user. There are Platform API keys that are associated with user identities and there are API keys that can be created for service IDs. For more information, see [Working with API keys](/docs/iam/apikeys.html#manapikey).</dd>
<dt>Access groups</dt>
<dd>You can create an access group to organize a set of users and service IDs into a single entity and easily assign permissions. You can assign a single policy to the group instead of assigning the same access multiple times per individual user or service ID. For more information, see [Setting up access groups](/docs/iam/groups.html#groups).</dd>
<dt>Resource groups</dt>
<dd>A resource group is a way for you to organize your account resources in customizable groupings so that you can quickly assign users access to more than one resource at a time. Any account resource that is managed by using IAM access control belongs to a resource group within your account. Users are not added to resource groups, but users are provided access to the resources within or can manage the resource group. Users given access to manage the resource group can create new instances within the group, manage other user's access to work with the group, or edit the group name based on the assigned IAM role. For more information, see [Managing resource groups](/docs/resources/resourcegroups.html#rgs) and [Best practices for organizing resources in resource groups](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).</dd>
<dt>Cloud Foundry orgs</dt>
<dd>As an account owner or organization manager, you can add orgs and spaces from the Cloud Foundry Organizations page in the console. Services that support the use of Cloud Foundry orgs and spaces are added to an org and space when you create them from the catalog. Orgs contain users, domains, and quotas. Within each org, spaces are added, which contain the service instances. For more information, see [Adding orgs and spaces](/docs/account/orgs_spaces.html#orgsspacesusers).</dd>
<dt>Cloud Foundry spaces</dt>
<dd>Within an organization, you can use spaces to group a set of applications, services, and users. Spaces are tied to a specific region in {{site.data.keyword.Bluemix_notm}}. You can create spaces in an org based on the delivery lifecycle. For example, you can create a dev space as a development environment, a test space as a testing environment, and a production space as a production environment. Then, you can associate your apps with spaces. For more information, see [Adding orgs and spaces](/docs/account/orgs_spaces.html#orgsspacesusers).</dd>
</dl>

Another important aspect of the diagram is the depiction of the three types of access management systems that you can use to provide account users access to resources within the account. 

* IAM [access roles](/docs/iam/users_roles.html#iamusermanrol) are used to provide users access to all resources that belong to a resource group. These access roles are also used to give users access to manage resource groups and create new service instances that get assigned to a resource group.
* Cloud Foundry [organization and space roles](/docs/iam/cfaccess.html#cfroles) are used to provide users access to any service instances that reside in a Cloud Foundry space.
* The infrastructure [customer portal](/docs/customer-portal/cpwhatis.html#customerportal_whatisCP) permissions are available for granting users granular [permissions](/docs/iam/infrastructureaccess.html#infrapermission) for customer portal access and the features within it such as invoices, billing, configuration of IaaS, monitoring of IaaS, purchasing of IaaS, and support. Device access is separate and handled from the device itself.
