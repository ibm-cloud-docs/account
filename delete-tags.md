---

copyright:

  years: 2021, 2024
lastupdated: "2024-02-19"

keywords: tags, delete tags, unused tags, delete tags in  the console, delete  tags cli, delete tags api

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Deleting unused tags from the account
{: #delete}

Before you can delete a tag, you must remove it from all resources and service IDs. If you still can't delete it, the tag might be attached to a resource that you don't have permission to view or was reclaimed. The same tag can be attached to several resources and service IDs by different users in the same billing account.

If a reclaimed resource is blocking tag deletion, you can either completely delete that reclaimed resource or restore it within 7 days after you delete it. Not all resources can be restored. You can use the {{site.data.keyword.Bluemix}} CLI to manage the reclamation process of specific resources. For more information, see [Using resource reclamations](/docs/account?topic=account-resource-reclamation).

When you delete an access management tag from the account, any associated IAM policies are also deleted with it.
{: note}

## Deleting unused tags in the console
{: #delete-tag-console}
{: ui}

1. To see the full list of tags in your account, go to **Manage** > **Account** in the {{site.data.keyword.cloud}} console, and select **Tags**.
1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Delete** next to the unused tag.

## Deleting unused tags by using the CLI
{: #delete-tag-cli}
{: cli}

Log in to [{{site.data.keyword.cloud}} CLI](/docs/cli?topic=cli-getting-started) and select your account to run the **`ibmcloud resource tag-delete`** command for deleting only one or all of the unused tags.

The following example deletes the `MyTag` user tag:

   ```bash
   ibmcloud resource tag-delete --tag-name MyTag
   ```
   {: codeblock}

## Deleting unused tags by using the API
{: #delete-tag-api}
{: api}

You can delete tags by calling the [Global Search and Tagging - Tagging API](/apidocs/tagging#delete-tag-all){: external} as shown in the following sample requests. The allowed values for the `tag_type` query parameter are: `user` for user tags and `access` for access management tags.

### Deleting a tag
{: #delete-a-tag-api}

Deleting an access management tag called `project:myproject` from the account:
```bash
curl -X DELETE -H "Authorization: {iam_token}" \
-H "Accept: application/json" \
"https://tags.global-search-tagging.cloud.ibm.com/v3/tags/project:myproject?tag_type=access"
```
{: codeblock}
{: curl}

```java
DeleteTagOptions deleteTagOptions = new DeleteTagOptions.Builder()
    .tagName("env:example-access-tag")
    .tagType("access")
    .build();

Response<DeleteTagResults> response = service.deleteTag(deleteTagOptions).execute();
DeleteTagResults deleteTagResults = response.getResult();
System.out.println(deleteTagResults.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  tagName: 'env:example-access-tag',
  tagType: 'access',
};

globalTaggingService.deleteTag(params)
  .then(res => {
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
delete_tag_results = global_tagging_service.delete_tag(
  tag_name='env:example-access-tag',
  tag_type='access').get_result()

print(json.dumps(delete_tag_results, indent=2))
```
{: codeblock}
{: python}

```go
deleteTagOptions := globalTaggingService.NewDeleteTagOptions("env:example-access-tag")
deleteTagOptions.SetTagType("access")

deleteTagResults, response, err := globalTaggingService.DeleteTag(deleteTagOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(deleteTagResults, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

### Deleting all unused tags
{: #delete-all-tags-api}

Deleting all unused access management tags from the account:
```bash
curl -X DELETE -H "Authorization: {iam_token}" \
-H "Accept: application/json" \
"https://tags.global-search-tagging.cloud.ibm.com//v3/tags?tag_type=access"
```
{: codeblock}
{: curl}

```java
DeleteTagAllOptions deleteTagAllOptions = new DeleteTagAllOptions.Builder()
    .tagType("user")
    .build();

Response<DeleteTagsResult> response = service.deleteTagAll(deleteTagAllOptions).execute();
DeleteTagsResult deleteTagsResult = response.getResult();

System.out.println(deleteTagsResult.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  tagType: 'access',
};

globalTaggingService.deleteTagAll(params)
  .then(res => {
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
delete_tags_result = global_tagging_service.delete_tag_all(
  tag_type='user').get_result()

print(json.dumps(delete_tags_result, indent=2))
```
{: codeblock}
{: python}

```go
deleteTagAllOptions := globalTaggingService.NewDeleteTagAllOptions()
deleteTagAllOptions.SetTagType("user")

deleteTagsResult, response, err := globalTaggingService.DeleteTagAll(deleteTagAllOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(deleteTagsResult, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}


## Deleting tags by using Terraform
{: #delete-terraform}
{: terraform}

Before you can delete tags by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://developer.hashicorp.com/terraform/language){: external}.

Use the following steps to delete tags from your account:

1. Create an argument in your `main.tf` file. The following example deletes the `ibm_tag` from the resource `ibm`, which is attached to resource ID `ibm_satellite_location.location.crn`.

   ```terraform
   resource "ibm_resource" "ibm" {
   resource_id = ibm_satellite_location.location.crn
   tags        = [ "ibm_tag" ]
   }
   ```
   {: codeblock}

1. After you finish building your configuration file, initialize the Terraform CLI. For more information, see [Initializing Working Directories](https://developer.hashicorp.com/terraform/cli/init){: external}.

   ```terraform
   terraform init
   ```
   {: pre}

1. Provision the resources from the `main.tf` file. For more information, see [Provisioning Infrastructure with Terraform](https://developer.hashicorp.com/terraform/cli/run){: external}.

   1. Run `terraform plan` to generate a Terraform execution plan to preview the proposed actions.

      ```terraform
      terraform plan
      ```
      {: pre}

   1. Run `terraform apply` to create the resources that are defined in the plan.

      ```terraform
      terraform apply
      ```
      {: pre}

1. Delete the tags.

   ```terraform
   terraform destroy
   ```
   {: pre}
