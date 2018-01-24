---

copyright:

  years: 2015, 2018
lastupdated: "2018-01-23"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Working with organizations
As an account owner or an organization manager, you can perform org management tasks, including renaming your org, deleting an org or space, updating org or space roles, and managing quota and domains.
{:shortdesc}

To manage your orgs from the {{site.data.keyword.Bluemix}} console, click **Manage > Account > Cloud Foundry Orgs**. You can view resources of only one organization at a time. If you are a member of multiple organizations, you can switch organizations from the user account preferences link in the console menu bar.

## Renaming orgs
{: #orgrename}

Complete the following steps to rename your organization:
1. Click **Manage** > **Account** > **Cloud Foundry Orgs**.
2. Determine which org you want to rename, and click **View Details**.
3. Click **Edit Cloud Foundry Org**.
4. Click **Edit** next to the name of the org.
5. Type the new org name, and click **Save**.

## Deleting orgs and spaces
{: #deleteorgs}

### Deleting an org

When you delete an organization, all the spaces, applications, and services within the organization are deleted. Be sure to note that deleting operations cannot be reversed. 

### Deleting a space

Complete the following steps to delete a space:

1. Click **Manage** > **Account** > **Cloud Foundry Orgs**.
2. Select the org that you want to edit, and click **View Details**.
3. Determine which space to delete, and click **Edit Space**.
4. Click **Delete Cloud Foundry Space**.

## Editing user roles
{: #listmembers}

### Editing user roles for a specific org 

Complete the following steps to edit the users roles for a specific org:

1. Click **Manage** > **Account** > **Cloud Foundry Orgs**.
2. Determine which organization you want to edit, and click **View Details** then **Edit Org**.
4. You can see the members of your organization and their roles in the **USERS** tab.

### Editing user roles for a specific space

Complete the following steps to edit the user roles for a specific space:

1. Click **Manage** > **Account** > **Cloud Foundry Orgs**.
2. Select the organization that you want to view the members for, and click **View Details**.
3. Determine which space you want to edit, and click **Edit Space**.
4. You can see the members of your space and their roles in the **USERS** tab.

## Managing quota
{: #managequota}

As an {{site.data.keyword.Bluemix_notm}} account owner or organization manager, you can view the used and allocated quota for an organization. The quota represents the resource limits for the organization, which is assigned when the organization is created. The resources that are available to an organization vary depending on whether you have a free account or a billable account. Any application or service in a space within the organization contributes to the usage of the allocated quota.

To view the used and allocated quota for an org, complete the following steps:

1. Click **Manage** &gt; **Account** &gt; **Cloud Foundry Orgs**.
2. Identify the organization that you want to view the quota for, and click **View Details**.
3. Click **Edit Org**.
4. If you have spaces defined in more than one region, select the specific region that you want to view.
5. Click **QUOTA**. 
6. By default, the **Cloud Foundry** quota page opens. You can view the quota details for the following resources:
 * MEMORY
 * SERVICES
 * PLAN
 * PRICE
7. Click **Containers** to view the used and available container quota allocation. The container allocation varies depending on your pricing plan. You can view the quota details for the following resources:
 * MEMORY
 * PUBLIC IP
 * FILE SHARES
8. Click **Virtual Servers** to view the virtual machines.

Containers are not available in the {{site.data.keyword.Bluemix_notm}} Sydney region. 
{: tip}

For more information about containers, see [Quota](/docs/containers/container_planning.html#container_planning_quota) in the Containers documentation.
To change the quota that is allocated to an organization, you must open a support ticket. For more information about opening a support ticket, see [Getting customer support](/docs/get-support/howtogetsupport.html#getting-customer-support). 

## Managing domains
{: #managedomains}

As an {{site.data.keyword.Bluemix_notm}} account owner or organization manager, you can view the system domain and add custom domains for applications that are built within an organization and its spaces. As a space manager, the **Domains** tab for a space is a read-only list of the domains that are assigned to the space.

1. Click **Manage** &gt; **Account** &gt; **Cloud Foundry Orgs**.
2. Identify the organization that you want to view or edits domains for.
3. Select **View Details** for that org.
4. Click **Edit Org**.
5. Click **DOMAINS**.

If you add a custom domain, you must configure your DNS server to resolve your custom domain to point to the {{site.data.keyword.Bluemix_notm}} system domain. In this way, when {{site.data.keyword.Bluemix_notm}} receives a request for your custom domain, it can properly route it to your app. The system domain is always available to a space, and custom domains might also be allocated to a space. Apps created in a space might use any of domains listed for that space. For more information about creating and using custom domains, see [Using a custom domain](/docs/apps/updapps.html#domain).
