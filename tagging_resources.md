---

copyright:

  years: 2018, 2021
lastupdated: "2021-02-25"

keywords: tags, user tags, access management tags, attach tags, detach tags, full list of tags, how to use tags

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}


# Working with tags
{: #tag}

Use tags to organize, track usage costs, and even manage access to your resources. You can tag related resources and view them throughout your account by filtering by tags from your resource list.  
{: shortdesc}

To see a full list of tags in your account, go to **Manage** > **Account** in the {{site.data.keyword.cloud}} console, and select **Tags**.

You can apply **user tags** to organize your resources and easily find them later or help you with identifying specific team usage or cost allocation.
By clicking **Access management tags**, you can create tags to control access to your resources without requiring updates to your IAM policies.

## Tagging rules
{: #limits}

Tags are not case-sensitive, and the maximum length of a tag is 128 characters. The permitted characters are A-Z, 0-9, spaces, underscore, hyphen, period, and colon. The use of a colon formats the tag into a string that isolates two logical parts, like a `key:value` pair. A comma separates multiple tags and can't be used within the tag name itself.

The only supported format for access management tags is `key:value`.
{: note}

### Sample tags and syntax
{: #sample-and-syntax}

You can apply tags to help you organize and manage your resources and access policies. Consider writing tags as `key:value` pairs to help coordinate your development environments, projects, compliance, and optimization throughout your organization. See the following table for some examples of tags that you might want to use.

| Tag | Description |
|----------|---------|
| `env:dev`, `env:test`, `env:stage`, `env:prod` | Use to identify or even manage access to your development environment|
| `project:lw-wizard`, `app:poc-app` | Use to identify or even manage access to a project |
| `dataresidency:germany`, `compliance:hipaa`, `compliance:pii` | Use to define compliance requirements |
| `schedule:24x7`, `maxruntime:12days` | Use to help you automate optimization |
{:caption="Table 1. Tag syntax" caption-side="top"}

Because tags are visible account-wide, avoid using personal information, such as your name, address, phone number, email address, or other identifying or proprietary information.
{: note}

## Creating tags
{: #create}

### Creating user tags
{: #create-user-tags}

You don't need to create user tags to attach them to resources. Go to the [Attaching and detaching tags on a resource](#attach-detach) for the following steps.

### Creating access management tags in the console
{: #create-access-console}

Before you can attach your access management tags to individual resources, you need to create them first. To create access management tags, you need to have administrator role on either the Tagging Service that is listed under the Account management services or on all Account management services.

{{site.data.keyword.cloud}} allows up to 30 access management tags per account.
{: note}

1. Go to **Manage** > **Account** in the {{site.data.keyword.cloud}} console, and select **Tags**.
2. Click **Access management tags**.
3. Type the names of your tags, and click **Create Tags**. These tags are now ready to be attached to resources and to be written to access policies.

### Creating access management tags by using the CLI
{: #create-access-cli}

1. Log in to {{site.data.keyword.cloud}} CLI. If you have multiple accounts, you are prompted to select which account to use. If you do not specify a region with the `-r` flag, you must also select a region.
    ```
    ibmcloud login
    ```
    {: codeblock}

    If your credentials are rejected, you might be using a federated ID. To log in with a federated ID, use the `--sso` flag. See [Logging in with a federated ID](/docs/account?topic=account-federated_id) for more details.
    {: tip}
    
    If it's your first time using the {{site.data.keyword.cloud_notm}} CLI, check out the [getting started tutorial](/docs/cli?topic=cli-getting-started).

2. Enter the `ibmcloud resource tag-create` command to create an access management tag in your account. This example creates a tag that is called `project:myproject`: 
    ```
    ibmcloud resource tag-create --tag-names project:myproject
    ```
    {: codeblock} 
 

For more information, see the [`ibmcloud resource` command reference](/docs/cli?topic=cli-ibmcloud_commands_resource).


### Creating access management tags by using the API
{: #create-access-api}

You can programmatically create access management tags by calling the [Global Search and Tagging - Tagging API](https://{DomainName}/apidocs/tagging){: external} as shown in the following sample request. The example creates a tag that is called `project:myproject`.
```
curl -X POST -H "Authorization: {iam_token}" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-d '{ "tag_names": ["project:myproject"] }' \
"{base_url}/v3/tags?tag_type=access"
```
{: codeblock}

## Attaching and detaching tags on a resource
{: #attach-detach}

### In the console
1. From the {{site.data.keyword.cloud}} console, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) > **Resource list** to view your list of resources.
2. Expand the resource type twistie that contains the resource you want to tag. For example, if you want to tag an instance of {{site.data.keyword.cos_full_notm}}, expand **Storage**.  
3. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) to attach or update a tag for the resource.
    * To attach tags, click the **Actions** menu ![Actions icon](../icons/action-menu-icon.svg) and select **Add Tags**.
    * To update your tags, you can either select Edit tags from the **Actions** menu ![Actions icon](../icons/action-menu-icon.svg), or click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg) next to the displayed tags in the resource list.
    * Type a name for your user or access management tag. Press Enter to continue adding tags.
4. To remove a tag, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg). Then, click the **Remove** icon ![Remove icon](../icons/close-tagging.svg) next to the tag.

To attach or detach an access management tag, appropriate permission is required. For more information, see [Granting users access to tag resources](/docs/account?topic=account-access).

When you detach an access management tag from a resource, any associated access policies are also detached from that resource.
{: note}

### By using the CLI
{: #attach-detach-cli}

Log in to [{{site.data.keyword.cloud}} CLI](/docs/cli?topic=cli-getting-started) and select your account to run the appropriate CLI command:
* To attach a tag to a resource, use the `ibmcloud resource tag-attach` command.
    The following example shows how to attach a user tag called `MyTag` to a resource named `MyResource`:
    ```
    ibmcloud resource tag-attach --tag-name MyTag --resource-name  'MyResource'
    ```
    {: codeblock}
    
    An example for attaching an access management tag called `project:myproject` to a resource named `MyResource`:
    ```
    ibmcloud resource tag-attach --tag-names MyTag --resource-name  'MyResource' --tag-type access 
    ```
    {: codeblock}    

    The allowed values for `tag-type` are `user` for user tags and `access` for access management tags. The default value is `user`.
* To detach a tag from a resource, use the `ibmcloud resource tag-detach` command.
    An example to detach a user tag called `MyTag` from a resource named `MyResource`:
    ```
    ibmcloud resource tag-detach --tag-names MyTag —resource-name 'MyResource'
    ```
    {: codeblock}
    
    An example to detach an access management tag called `MyTag` from a resource named `MyResource`:
    ```
    ibmcloud resource tag-detach --tag-names project:myproject —resource-name 'MyResource' --tag-type access
    ```
    {: codeblock}
 
For more information, see the [`ibmcloud resource` command reference](/docs/cli?topic=cli-ibmcloud_commands_resource). 

### By using the API
{: #attach-detach-api}

You can programmatically attach or detach tags by calling the [Global Search and Tagging - Tagging API](https://{DomainName}/apidocs/tagging){: external} as shown in the following sample requests. The allowed values for the `tag_type` query parameter are: `user` for user tags and `access` for access management tags.
* Attaching an access management tag called `project:myproject` to a service instance:
    ```
    curl -X POST -H "Authorization: {iam_token}" \
    -H "Accept: application/json" \
    -H "Content-Type: application/json" \
    -d '{ "resources": [{ "resource_id": "crn:v1:bluemix:public:cloud-object-storage:global:a/59bcbfa6ea2f006b4ed7094c1a08dcdd:1a0ec336-f391-4091-a6fb-5e084a4c56f4::" }], "tag_names": ["project:myproject"] }' \
    "{base_url}/v3/tags/attach?tag_type=access"
    ```
    {: codeblock}
* Detaching the same access management tag from the service instance:
    ```
    curl -X POST -H "Authorization: {iam_token}" \
    -H "Accept: application/json" \
    -H "Content-Type: application/json" \
    -d '{ "resources": [{ "resource_id": "crn:v1:bluemix:public:cloud-object-storage:global:a/59bcbfa6ea2f006b4ed7094c1a08dcdd:1a0ec336-f391-4091-a6fb-5e084a4c56f4::" }], "tag_names": ["project:myproject"] }' \
    "{base_url}/v3/tags/detach?tag_type=access"
    ```
    {: codeblock}

## Searching for tags
{: #search-tags}

You can search for tags by using any of the following methods:

  * Try the search bar that is located in the {{site.data.keyword.cloud}} console menu bar.
  * You can filter your resource list by the tag you are searching for.
  * From the application detail page, you can locate the tags that are associated with that resource.

The same tag can be attached to multiple resources by different users in the same billing account, and not all users have visibility on all resources on the account.
{: note}

## Tagging for resellers
{: #resell}

All tags are visible to all members of an account. To view the policy of an access management tag, the user is required to have at least a viewer role on the tagged resource. If your account is associated with different organizations, if you're a reseller for example, you might want to recommend your customers not to store sensitive information in tags.

To control tag visibility, circulate tagging guidelines and let users know that tags are visible account-wide.

Use codes rather than names for clients and accounts and avoid placing sensitive information in tags.
{: tip}

## Deleting unused tags from the account
{: #delete}

Before you can delete a tag, you must remove it from all resources. If you still can't delete it, the tag might be attached to a resource that you don't have permission to view or was reclaimed. The same tag can be attached to several resources by different users in the same billing account.

If a reclaimed resource is blocking tag deletion, you can either completely delete that reclaimed resource or restore it within 7 days after you delete it. Not all resources can be restored. You can use the {{site.data.keyword.Bluemix}} CLI to manage the reclamation process of specific resources. For more information, see [Using resource reclamations](/docs/account?topic=account-resource-reclamation).

When you delete an access management tag from the account, any associated IAM policies are also deleted with it.
{: note}

1. To see the full list of tags in your account, go to **Manage** > **Account** in the {{site.data.keyword.cloud}} console, and select **Tags**.
2. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) next to the unused tag and select **Delete**.

### By using the CLI
{: #delete-cli}

Log in to [{{site.data.keyword.cloud}} CLI](/docs/cli?topic=cli-getting-started) and select your account to run the `ibmcloud resource tag-delete` command for deleting only one or all of the unused tags.
* The following example deletes the `MyTag` user tag:
  ```
  ibmcloud resource tag-delete --tag-names MyTag
  ```  
  {: codeblock}

### By using the API
{: #delete-api}

You can delete tags by calling the [Global Search and Tagging - Tagging API](https://{DomainName}/apidocs/tagging){: external} as shown in the following sample requests. The allowed values for the `tag_type` query parameter are: `user` for user tags and `access` for access management tags.
* Deleting an access management tag called `project:myproject` from the account:
    ```
    curl -X DELETE -H "Authorization: {iam_token}" \
    -H "Accept: application/json" \
    "{base_url}/v3/tags/project:myproject?tag_type=access"
    ```
    {: codeblock}
    
* Deleting all unused access management tags from the account:
    ```
    curl -X DELETE -H "Authorization: {iam_token}" \
    -H "Accept: application/json" \
    "{base_url}/v3/tags?tag_type=access"
    ```
    {: codeblock}
