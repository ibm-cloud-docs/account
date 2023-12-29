---

copyright:
  years: 2015, 2023
lastupdated: "2023-12-29"

keywords: update orgs, update spaces, quotas, Cloud Foundry orgs, domains

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Updating orgs and spaces
{: #orgupdates}

As an {{site.data.keyword.Bluemix}} account owner or Cloud Foundry organization manager, you can perform management tasks at the org level and the space level. These tasks include renaming an org or space, assigning or updating Cloud Foundry users' roles, managing domains, and viewing org quota details.
{: shortdesc}

IBM Cloud Foundry Public is deprecated with an end-of-support date of 1 June 2023. For more information, see [Deprecation of IBM Cloud Foundry](/docs/cloud-foundry-public?topic=cloud-foundry-public-deprecation).
{: deprecated}

## Updating orgs and spaces in the console
{: #orgupdates-console}
{: ui}

Go to **Manage** > **Account** in the {{site.data.keyword.cloud_notm}} console, and select **Cloud Foundry orgs**.

You can view the resources of only one org at a time. If you are a member of multiple orgs, you can switch orgs from the user account preferences link in the console menu bar.
{: tip}

* To rename an org, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions") for the org you want to rename, and select **Rename**.
{: #orgrename}

    Any changes that you make apply to all users in the org.

* To delete a space, select the org in which the space is assigned. Then, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Delete**. When you delete a space, all included resources and users are also deleted.

    You can delete spaces but not orgs.
    {: note}

* To repurpose an org, delete all spaces within the org and then rename it. Although you cannot delete orgs, you can simplify the list on the Cloud Foundry Orgs page by clearing and then re-using obsolete orgs rather than creating new ones.

* To edit user roles at the org level, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Users**.
{: #listmembers}

   Depending on how you want to modify the user permissions, select or clear the checkbox for a specific role. The roles that you can assign at the organization level are Manager, Billing manager, and Auditor. For more information, see [Cloud Foundry roles](/docs/account?topic=account-mngcf#cfroles).

* To edit user roles for a specific space, click the org in which the space is assigned. Then, click the name of the space.

   Depending on how you want to modify the user permissions, select or clear the checkbox for a specific role. The roles that you can assign at the space level are Manager, Developer, and Auditor. For more information, see [Cloud Foundry roles](/docs/account?topic=account-mngcf#cfroles).

* To manage your domains, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions") for the respective org, and select **Domains**.
{: #managedomains}

   As an account owner or organization manager, you can view the system domain and add custom domains for applications that are built within an org and its spaces. If you're a space manager, this page displays read-only list of the domains that are assigned to the space.

   If you add a custom domain, you must configure your DNS server to resolve your custom domain to point to the {{site.data.keyword.Bluemix_notm}} system domain. In this way, when {{site.data.keyword.Bluemix_notm}} receives a request for your custom domain, it's properly routed to your app. The system domain is always available to a space, and custom domains might also be allocated to a space. Apps that are created in a space might use any of the domains that are listed for that space. For more information about creating and by using custom domains, see [Managing your domains](/docs/cloud-foundry-public?topic=cloud-foundry-public-custom-domains).

* To manage the allocated quota for an org, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions") for the respective org, and select **Quotas**.
{: #managequota}

   From here, you can view the quota details for the number of apps, amount of memory, number of services, and plan details. The quota represents the resource limits for the org, which is assigned when the organization is created. The resources that are available to an org vary depending on whether you have a free account or a billable account. Any application or service that is included in a space within the org contributes to the usage of the allocated quota.

   To change the quota that is allocated to an org, you must create a support case. For more information, see [Working with support cases](/docs/get-support?topic=get-support-open-case).

   To view the quota details at the space level for each location, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions") for the respective org, and select **Quotas**. Then, expand each row accordingly.

## Updating orgs and spaces by using the CLI
{: #orgupdates-cli}
{: cli}

### Renaming orgs
{: #rename-org-cli}
{: cli}

1. Log in, and select the account.

   ```bash
   ibmcloud login
   ```
   {: codeblock}

2. Rename an organization by running the [`ibmcloud account org-rename`](/docs/cli?topic=cli-ibmcloud_commands_account#ibmcloud_account_org_rename) command, where `OLD_ORG_NAME` is the old name of the org that is to be renamed, `NEW_ORG_NAME` is the new name of the org that is to be renamed, and `-r, --region REGION` is the region name.

   ```bash
   ibmcloud account org-rename OLD_ORG_NAME NEW_ORG_NAME [-r, --region REGION]
   ```
   {: codeblock}


This operation can be done only by an org manager.
{: note}

### Deleting spaces
{: #delete-space-cli}
{: cli}

1. Log in, and select the account.

   ```bash
   ibmcloud login
   ```
   {: codeblock}

2. Delete a space by using the [`ibmcloud account space-delete`](/docs/cli?topic=cli-ibmcloud_commands_account#ibmcloud_account_space_delete) command, where `-f` is forcing deletion without confirmation, and `-o` is deleting space within specified org.

   ```bash
   ibmcloud account space-delete SPACE [-o ORG] [-f]
   ```
   {: codeblock}

For more information on managing accounts, users in an account by using the CLI, and the org, space, and roles of public Cloud Foundry environments, visit [Managing accounts, users, and Cloud Foundry orgs](https://cloud.ibm.com/docs/cli?topic=cli-ibmcloud_commands_account).

## Updating orgs and spaces by using the Cloud Foundry API
{: #orgupdates-api}
{: api}

### Updating organizations
{: #update-org-api}
{: api}

You can update organizations by calling the Cloud Foundry API. For detailed information about how to use it, see [Update an Organization](http://v3-apidocs.cloudfoundry.org/version/3.97.0/index.html#update-an-organization){: external}. Check the following sample request:

```curl
curl "https://api.example.org/v3/organizations/[guid]" \
  -X PATCH \
  -H "Authorization: bearer [token]" \
  -H "Content-Type: application/json" \
  -d '{ "name": "my-organization" }'
```
{: codeblock}
{: curl}

### Deleting spaces
{: #delete-space-api}
{: api}

You can delete spaces by calling the Cloud Foundry API. For detailed information about how to use it, see [Delete a space](http://v3-apidocs.cloudfoundry.org/version/3.97.0/index.html#delete-a-space){: external}. Check the following sample request:

```curl
curl "https://api.example.org/v3/spaces/[guid]" \
  -X DELETE \
  -H "Authorization: bearer [token]"
```
{: codeblock}
{: curl}
