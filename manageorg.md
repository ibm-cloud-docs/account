---

copyright:
  years: 2015, 2020
lastupdated: "2020-01-08"

keywords: update orgs, update spaces, quotas, Cloud Foundry orgs, domains

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# Updating orgs and spaces
{: #orgupdates}

As an {{site.data.keyword.Bluemix}} account owner or Cloud Foundry organization manager, you can perform management tasks at the org level and the space level. These tasks include renaming an org or space, assigning or updating Cloud Foundry users' roles, managing domains, and viewing org quota details.
{:shortdesc}

Go to **Manage > Account**, and select **Cloud Foundry orgs**.

You can view the resources of only one org at a time. If you are a member of multiple orgs, you can switch orgs from the user account preferences link in the console menu bar.
{: tip}

  * To rename an org, click the Actions icon ![Action icon](../icons/action-menu-icon.svg) for the org you want to rename, and select **Rename**.
    {: #orgrename}

    Any changes that you make apply to all users in the org.

  * To delete a space, select the org in which the space is assigned. Then, click the Actions icon ![Action icon](../icons/action-menu-icon.svg), and select **Delete**.

    When you delete a space, all included resources and users are also deleted. You can delete spaces but not orgs.

  * To edit user roles at the org level, click the Actions icon ![Action icon](../icons/action-menu-icon.svg), and select **Users**.
    {: #listmembers}

    Depending on how you want to modify the user permissions, select or clear the checkbox for a specific role. The roles that you can assign at the organization level are Manager, Billing manager, and Auditor. For more information, see [Cloud Foundry roles](/docs/iam?topic=iam-cfaccess#cfroles).

  * To edit user roles for a specific space, click the org in which the space is assigned. Then, click the name of the space.

    Depending on how you want to modify the user permissions, select or clear the checkbox for a specific role. The roles that you can assign at the space level are Manager, Developer, and Auditor. For more information, see [Cloud Foundry roles](/docs/iam?topic=iam-cfaccess#cfroles).

  * To manage your domains, click the Actions icon ![Action icon](../icons/action-menu-icon.svg) for the respective org, and select **Domains**.
    {: #managedomains}

    As an account owner or organization manager, you can view the system domain and add custom domains for applications that are built within an org and its spaces. If you're a space manager, this page displays read-only list of the domains that are assigned to the space.

    If you add a custom domain, you must configure your DNS server to resolve your custom domain to point to the {{site.data.keyword.Bluemix_notm}} system domain. In this way, when {{site.data.keyword.Bluemix_notm}} receives a request for your custom domain, it's properly routed to your app. The system domain is always available to a space, and custom domains might also be allocated to a space. Apps that are created in a space might use any of the domains that are listed for that space. For more information about creating and by using custom domains, see [Managing your domains](/docs/apps?topic=creating-apps-update-domain).

  * To manage the allocated quota for an org, click the Actions icon ![Action icon](../icons/action-menu-icon.svg) for the respective org, and select **Quotas**.
    {: #managequota}

    From here, you can view the quota details for the number of apps, amount of memory, number of services, and plan details. The quota represents the resource limits for the org, which is assigned when the organization is created. The resources that are available to an org vary depending on whether you have a free account or a billable account. Any application or service that is included in a space within the org contributes to the usage of the allocated quota.

    To change the quota that is allocated to an org, you must create a support case. For more information, see [Working with support cases](/docs/get-support?topic=get-support-open-case).

    To view the quota details at the space level for each location, click the Actions icon ![Action icon](../icons/action-menu-icon.svg) for the respective org, and select **Quotas**. Then, expand each row accordingly.

