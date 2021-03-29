---

copyright:

  years: 2021
lastupdated: "2021-03-29"

keywords: tags, user tags, access management tags, attach tags, detach tags, attach tags ui, attach tags cli, attach tags api, detach tags ui, detach tags api, detach tags cli

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}

# Attaching and detaching tags on a resource

You can attach and detach tags on a resource through the console, CLI, or API. To attach or detach a tag on a resource, appropriate permission is required. For more information, see [Granting users access to tag resources](/docs/account?topic=account-access).

## Attaching and detaching tags on a resource in the console 
{: #attach-detach-console}
{: ui}

1. From the {{site.data.keyword.cloud}} console, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) > **Resource list** to view your list of resources.
2. Expand the resource type twistie that contains the resource you want to tag. For example, if you want to tag an instance of {{site.data.keyword.cos_full_notm}}, expand **Storage**.  
3. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) to attach or update a tag for the resource.
    * To attach tags, click the **Actions** menu ![Actions icon](../icons/action-menu-icon.svg) and select **Add Tags**.
    * To update your tags, you can either select Edit tags from the **Actions** menu ![Actions icon](../icons/action-menu-icon.svg), or click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg) next to the displayed tags in the resource list.
    * Type a name for your user or access management tag. Press Enter to continue adding tags.
4. To remove a tag, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg). Then, click the **Remove** icon ![Remove icon](../icons/close-tagging.svg) next to the tag.

When you detach an access management tag from a resource, any associated access policies are also detached from that resource.
{: note}

## Attaching tags to a resource by using the CLI
{: #attach-cli}
{: cli}

Log in to [{{site.data.keyword.cloud}} CLI](/docs/cli?topic=cli-getting-started) and select your account to run the appropriate CLI command.

To attach a tag to a resource, use the [**`ibmcloud resource tag-attach`**](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_tag_attach) command. The allowed values for `tag-type` are `user` for user tags and `access` for access management tags. The default value is `user`. The following example shows how to attach a user tag called `MyTag` to a resource named `MyResource`:

```
ibmcloud resource tag-attach --tag-name MyTag --resource-name  'MyResource'
```
{: codeblock}

An example for attaching an access management tag called `project:myproject` to a resource named `MyResource`:

```
ibmcloud resource tag-attach --tag-names project:myproject --resource-name  'MyResource' --tag-type access 
```
{: codeblock}    
    
## Detaching tags from a resource by using the CLI
{: #detach-cli}
{: cli}

To detach a tag from a resource, use the [**`ibmcloud resource tag-detach`**](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_tag_detach) command. An example to detach a user tag called `MyTag` from a resource named `MyResource`:

```
ibmcloud resource tag-detach --tag-names MyTag —resource-name 'MyResource'
```
{: codeblock}

An example to detach an access management tag called `project:myproject` from a resource named `MyResource`:

```
ibmcloud resource tag-detach --tag-names project:myproject —resource-name 'MyResource' --tag-type access
```
{: codeblock}

For more information, see the [`ibmcloud resource` command reference](/docs/cli?topic=cli-ibmcloud_commands_resource).

When you detach an access management tag from a resource, any associated access policies are also detached from that resource.
{: note} 

## Attaching tags to a resource by using the API
{: #attach-api}
{: api}

You can programmatically attach tags by calling the [Global Search and Tagging - Tagging API](https://{DomainName}/apidocs/tagging#attach-tag){: external} as shown in the following sample requests. The allowed values for the `tag_type` query parameter are: `user` for user tags and `access` for access management tags. The following example shows how to attach an access management tag called `project:myproject` to a service instance:

```
curl -X POST -H "Authorization: {iam_token}" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-d '{ "resources": [{ "resource_id": "crn:v1:bluemix:public:cloud-object-storage:global:a/59bcbfa6ea2f006b4ed7094c1a08dcdd:1a0ec336-f391-4091-a6fb-5e084a4c56f4::" }], "tag_names": ["project:myproject"] }' \
"{base_url}/v3/tags/attach?tag_type=access"
```
{: codeblock}

## Detaching tags from a resource by using the API
{: #detach-api}
{: api}

You can programmatically detach tags by calling the [Global Search and Tagging - Tagging API](https://{DomainName}/apidocs/tagging#detach-tag){: external} as shown in the following sample requests. The allowed values for the `tag_type` query parameter are: `user` for user tags and `access` for access management tags. The following example shows how to detach an access management tag called `project:myproject` from a service instance:

```
curl -X POST -H "Authorization: {iam_token}" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-d '{ "resources": [{ "resource_id": "crn:v1:bluemix:public:cloud-object-storage:global:a/59bcbfa6ea2f006b4ed7094c1a08dcdd:1a0ec336-f391-4091-a6fb-5e084a4c56f4::" }], "tag_names": ["project:myproject"] }' \
"{base_url}/v3/tags/detach?tag_type=access"
```
{: codeblock}

When you detach an access management tag from a resource, any associated access policies are also detached from that resource.
{: note}
