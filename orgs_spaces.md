---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-18"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Adding orgs and spaces
{: #orgsspacesusers}

As an {{site.data.keyword.Bluemix}} account owner, you can add orgs and spaces to your account. If you're an organization manager, you can manage the orgs in the account. Go to **Manage** > **Account**, and select **Cloud Foundry orgs**.
{:shortdesc}

You can use orgs to enable collaboration among users and to facilitate the logical grouping of project resources in the following ways:

   * You can group a set of spaces, apps, services, domains, routes, and users together in orgs. 
   * You can manage the user access to the orgs and spaces on an individual basis. 

## Adding orgs
{: #createorg}

Orgs can span multiple regions, and they are defined by the following items:

<dl>
<dt>Users</dt>
<dd>The role with basic permission in orgs and spaces. You must be assigned to an org before you can be granted other permissions to the spaces within the org. For more details, see [Users and roles](/docs/iam/users_roles.html#userrolesinfo).</dd>
<dt>Domains</dt>
<dd>Provide the route on the internet that is allocated to the org. A route has a subdomain and a domain. A subdomain is typically the application name. A domain might be a system domain or a custom domain that you registered for your application. See [Managing custom domains](/docs/account/manageorg.html#managedomains).<br/>
<p>If you add a custom domain, you must configure your DNS server to resolve your custom domain to point to the {{site.data.keyword.Bluemix_notm}} system domain. In this way, when {{site.data.keyword.Bluemix_notm}} receives a request for your custom domain, it can properly route it to your application.</p></dd>
<dt>Quota</dt>
<dd>Represents the resources that are available to an org, including the number of services and the amount of memory that can be allocated for use by the org. Quotas are assigned when orgs are created. Any application or service in a space within an  org contributes to the usage of the quota. With Pay-As-You-Go or Subscription accounts, you can adjust your quota for Cloud Foundry applications and containers as the needs of your org change. See [Managing quota](/docs/account/manageorg.html#managequota).</dd>
</dl>

In a Subscription account, the quota is a user-defined limit that initiates spending notifications.
{: tip}

When you add an org, the name must be unique in {{site.data.keyword.Bluemix_notm}}. If the org name is already in use by another {{site.data.keyword.Bluemix_notm}} Public, Dedicated, or Local user, you must specify a new name. After you add the org, you're automatically assigned the Organization Manager permission, so you can edit the org name, add users, and create or delete spaces in the org. If you have a billable account, you can add as many orgs as you need. However, in a Lite account, you can have only one org. 

The following [user roles](/docs/iam/users_roles.html#userrolesinfo) can be assigned to users in an org. All users who are invited to the account are assigned the auditor role by default.

   * Organization manager
   * Organization billing manager
   * Organization auditor

Complete the following steps to add an org:

  1. Click **Add an organization**.
  2. Enter the org name.  
  3. Click **Add**.

<!-- Add info on Manage infrastructure option under a space -->

## Adding spaces
{: #spaceinfo}

Within an organization, you can use spaces to group a set of applications, services, and users. Spaces are tied to a specific region in {{site.data.keyword.Bluemix_notm}}. You can create spaces in an org based on the delivery lifecycle. For example, you can create a `dev` space as a development environment, a `test` space as a testing environment, and a `production` space as a production environment. Then, you can associate your apps with spaces.

After you add users to an org, you can grant them permissions to the spaces. Similar to orgs, spaces also have a set of [Cloud Foundry roles](/docs/iam/cfaccess.html#cfroles) with specific permissions that are assigned to team members:

  * Space manager
  * Space developer
  * Space auditor

A user must be assigned at least one of the permissions in the space.
{: tip}

Complete the following steps to add a space:

  1. Click the name of the org that you want to add a space to.
  2. Click **Add a space**.
  3. Select a region and enter a name.
  4. Click **Save**.
