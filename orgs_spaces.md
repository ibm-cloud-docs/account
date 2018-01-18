---

copyright:

  years: 2015, 2018
lastupdated: "2018-01-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Creating organizations and spaces
{: #orgsspacesusers}

As an account owner, you can manage your organizations and spaces from the Manage Organizations page in the {{site.data.keyword.Bluemix}} console. Organization managers can also use the Manage Organizations page to manage any organizations where they are set as the manager.
{:shortdesc}

To manage organizations and spaces, click **Manage** &gt; **Account** &gt; **Cloud Foundry Orgs**. 


## Creating organizations
{: #createorg}

Organizations can span multiple regions, and they are defined by the following items:

<dl>
<dt>Users</dt>
<dd>The role with basic permission in organizations and spaces. You must be assigned to an organization before you can be granted other permissions to the spaces within the organization. For detailed information, see [Users and roles](/docs/iam/users_roles.html#userrolesinfo).</dd>
<dt>Domains</dt>
<dd>Provide the route on the internet that is allocated to the organization. A route has a sub-domain and a domain. A sub-domain is typically the application name. A domain might be a system domain, or a custom domain that you registered for your application. See [Managing custom domains](/docs/account/manageorg.html#managedomains).<br/>
<p>**Note:** If you add a custom domain, you must configure your DNS server to resolve your custom domain to point to the {{site.data.keyword.Bluemix_notm}} system domain. In this way, when {{site.data.keyword.Bluemix_notm}} receives a request for your custom domain, it can properly route it to your application.</p></dd>
<dt>Quota</dt>
<dd>Represents the resources that are available to an organization, including the number of services and the amount of memory that can be allocated for use by the organization. Quotas are assigned when organizations are created. Any application or service in a space within an  organization contributes to the usage of the quota. With the Pay-As-You-Go or Subscription accounts, you can adjust your quota for Cloud Foundry applications and containers as the needs of your organization change. See [Managing quota](/docs/account/manageorg.html#managequota).</dd>
</dl>

In a Subscription account, quota is a user defined limit that triggers spending notifications.
{: tip}

In {{site.data.keyword.Bluemix_notm}}, you can use organizations to enable collaboration among users and to facilitate the logical grouping of project resources in the following ways:

   * You can group a set of spaces, apps, services, domains, routes, and users together in organizations. 
   * You can manage the access to the spaces and organizations on a per-user basis. 

When you create an organization, the name must be unique in {{site.data.keyword.Bluemix_notm}}. If the organization name is already in use by another {{site.data.keyword.Bluemix_notm}} Public, Dedicated, or Local user, you must specify a new name. After you create the organization, you're automatically assigned the *Organization Manager* permission, which enables you to edit the organization name, add users, and create or delete spaces in the organization.

You can use the [`bx iam org-delete`](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_iam_org_delete) command to delete organizations. When you delete an organization, all the spaces, applications, and services within the organization are deleted.

The following [user roles](/docs/iam/users_roles.html#userrolesinfo) can be assigned to users in an organization. All users invited to the account are assigned the auditor role by default.

   * Organization manager
   * Organization billing manager
   * Organization auditor

You can create an organization by completing the following steps:

1. Click **Manage** &gt; **Account** &gt; **Cloud Foundry Orgs**.
2. Click **Add a New Cloud Foundry Org**.
3. Enter the org name.
4. Click **Add**.

<!-- Add info on Manage infrastructure option under a space -->

## Creating spaces
{: #spaceinfo}

Within an organization, you can use spaces to group a set of applications, services, and users. Spaces are tied to a specific region in {{site.data.keyword.Bluemix_notm}}.

After you add users to an organization, you can grant them permissions to the spaces. Similar to organizations, spaces also have a set of [user roles](/docs/iam/users_roles.html#userrolesinfo) with specific permissions that are assigned to team members:

  * Space manager
  * Space developer
  * Space auditor

A user must be assigned at least one of the permissions in the space.
{: tip}

You can create spaces in your organization; for example, a *dev* space as a development environment, a *test* space as a testing environment, and a *production* space as a production environment. Then, you can associate your apps with spaces. Complete the following steps to create a space:

1. Click **Manage** &gt; **Account** &gt; **Cloud Foundry Orgs**.
2. Determine the organization that you want to add a space to and select **View Details**.
4. Click **Add a Cloud Foundry Space**.
5. Enter the space name.
6. Click **Add**.
