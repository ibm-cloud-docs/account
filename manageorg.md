---

copyright:

  years: 2015, 2018
lastupdated: "2018-05-21"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Updating orgs and spaces
{: #orgupdates}

As an account owner or organization manager, you can perform management tasks at the organization level and the space level. These tasks include renaming an organization or space, assigning or updating Cloud Foundry users roles, managing domains, and viewing organization quota details. 
{:shortdesc}

To manage your orgs from the {{site.data.keyword.Bluemix}} console, click **Manage > Account > Cloud Foundry Orgs**. You can view resources of only one org at a time. If you are a member of multiple orgs, you can switch orgs from the user account preferences link in the console menu bar.

## Renaming orgs
{: #orgrename}

Complete the following steps to rename your org. Note any changes you make apply to all users in the org.

1. Click **Manage** > **Account** > **Cloud Foundry Orgs**.
2. Click the Actions icon for the org you want to rename, and select **Rename**.  
3. Enter the new name, and click **Save**.

## Deleting orgs and spaces
{: #deleteorgs}

### Deleting an org

To delete an org, contact [Support](/docs/get-support/howtogetsupport.html). When an org is deleted, all the spaces and resources within the org are also deleted. Be sure to note that delete operations cannot be reversed. 

### Deleting a space

When you delete a space, all included resources and users are also deleted. Complete the following steps to delete a space:

1. Click **Manage** > **Account** > **Cloud Foundry Orgs**.
2. Click the org in which the space is assigned.
3. Click the Actions icon, and select **Delete**.
4. Confirm you want to delete the space by typing the space name in the field, and click **Delete**.

## Editing user roles
{: #listmembers}

The roles you can assign at the organization level are Manager, Billing manager, and Auditor. The roles you can assign at the space level are Manager, Developer, and Auditor. For the detailed role descriptions, see [Cloud Foundry roles](/docs/iam/cfaccess.html#cfroles).

### Editing user roles at the organization level

Complete the following steps to edit the user roles for a specific org:

1. Click **Manage** > **Account** > **Cloud Foundry Orgs**.
2. Click the Actions icon, and select **Users**.
3. Depending on how you want to modify the user permissions, select or clear the check box for a specific role.
4. Confirm your changes by clicking **Save**. 

### Editing user roles at the space level

Complete the following steps to edit the user roles for a specific space:

1. Click **Manage** > **Account** > **Cloud Foundry Orgs**.
2. Click the org in which the space is assigned.
3. Click the name of the space.
4. Depending on how you want to modify the user permissions, select or clear the check box for a specific role.
5. Confirm your changes by clicking **Save**.

## Managing domains
{: #managedomains}

As an account owner or organization manager, you can view the system domain and add custom domains for applications that are built within an org and its spaces. As a space manager, the **Domains** tab is a read-only list of the domains that are assigned to the space.

1. Click **Manage** &gt; **Account** &gt; **Cloud Foundry Orgs**.
2. Click the Actions icon for the org, and select **Domains**.

If you add a custom domain, you must configure your DNS server to resolve your custom domain to point to the {{site.data.keyword.Bluemix_notm}} system domain. In this way, when {{site.data.keyword.Bluemix_notm}} receives a request for your custom domain, it's properly routed to your app. The system domain is always available to a space, and custom domains might also be allocated to a space. Apps created in a space might use any of the domains listed for that space. For more information about creating and using custom domains, see [Using a custom domain](/docs/apps/updapps.html#domain).

## Managing quota
{: #managequota}

You can view the used and allocated quota for an org. The quota represents the resource limits for the org, which is assigned when the organization is created. The resources that are available to an org vary depending on whether you have a free account or a billable account. Any application or service included in a space within the org contributes to the usage of the allocated quota.

To view the used and allocated quota for an org, complete the following steps:

1. Click **Manage** &gt; **Account** &gt; **Cloud Foundry Orgs**.
2. Click the Actions icon for the specific org, and select **Quotas**.

   By default, the **Cloud Foundry** quota page is displayed. From here, you can view the quota details for the following resources:
 
   * The number of apps
   * The amount of memory 
   * The number of services 
   * Plan details 

3. Expand the row to view the quota at the space level for each region.  

To change the quota that is allocated to an org, you must open a support ticket. For more information, see [Getting customer support](/docs/get-support/howtogetsupport.html#getting-customer-support). 

