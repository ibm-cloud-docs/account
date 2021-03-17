---

copyright:

  years: 2021
lastupdated: "2021-03-12"

keywords: tags, delete tags, unused tags, delete tags in  the console, delete  tags cli, delete tags api

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

# Deleting unused tags from the account
{: #delete}

Before you can delete a tag, you must remove it from all resources. If you still can't delete it, the tag might be attached to a resource that you don't have permission to view or was reclaimed. The same tag can be attached to several resources by different users in the same billing account.

If a reclaimed resource is blocking tag deletion, you can either completely delete that reclaimed resource or restore it within 7 days after you delete it. Not all resources can be restored. You can use the {{site.data.keyword.Bluemix}} CLI to manage the reclamation process of specific resources. For more information, see [Using resource reclamations](/docs/account?topic=account-resource-reclamation).

When you delete an access management tag from the account, any associated IAM policies are also deleted with it.
{: note}

## Deleting unused tags in the console
{: #delete-tag-console}
{: ui}

1. To see the full list of tags in your account, go to **Manage** > **Account** in the {{site.data.keyword.cloud}} console, and select **Tags**.
2. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) next to the unused tag and select **Delete**.

## Deleting unused tags by using the CLI
{: #delete-tag-cli}
{: cli}

Log in to [{{site.data.keyword.cloud}} CLI](/docs/cli?topic=cli-getting-started) and select your account to run the **`ibmcloud resource tag-delete`** command for deleting only one or all of the unused tags.
* The following example deletes the `MyTag` user tag:
  ```
  ibmcloud resource tag-delete --tag-names MyTag
  ```  
  {: codeblock}

## Deleting unused tags by using the API
{: #delete-tag-api}
{: api}

You can delete tags by calling the [Global Search and Tagging - Tagging API](https://{DomainName}/apidocs/tagging#delete-tag-all){: external} as shown in the following sample requests. The allowed values for the `tag_type` query parameter are: `user` for user tags and `access` for access management tags.

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
