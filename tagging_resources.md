---

copyright:

  years: 2018, 2022
lastupdated: "2022-01-20"

keywords: tags, user tags, access management tags, attach tags, detach tags, full list of tags, how to use tags

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Working with tags
{: #tag}

Use tags to organize, track usage costs, and even manage access to your resources. You can tag related resources and view them throughout your account by filtering by tags from your resource list.  
{: shortdesc}

To see a full list of tags in your account, go to **Manage** > **Account** in the {{site.data.keyword.cloud}} console, and select **Tags**.
{: ui}

You can apply **user tags** to organize your resources and easily find them later or help you with identifying specific team usage or cost allocation.
By creating **access management tags**, you can control access to your resources without requiring updates to your IAM policies.

## Tagging rules
{: #limits}

Tags are not case-sensitive, and the maximum length of a tag is 128 characters. The permitted characters are A-Z, 0-9, spaces, underscore, hyphen, period, and colon. The only supported format for access management tags is `key:value`. The use of a colon formats the tag into a string that isolates two logical parts, like a `env:dev` pair. A comma separates multiple tags and can't be used within the tag name itself.

Tags are visible account-wide and can be replicated across geographic regions. Since tags are not regulated information, avoid creating tags that use personal information, such as your name, address, phone number, email address, or other identifying or proprietary information.
{: important}

### Sample tags and syntax
{: #sample-and-syntax}

You can apply tags to help you organize and manage your resources and access policies. Consider writing tags as `key:value` pairs to help coordinate your development environments, projects, compliance, and optimization throughout your organization. See the following table for some examples of tags that you might want to use.

| Tag | Description |
|----------|---------|
| `env:dev`, `env:test`, `env:stage`, `env:prod` | Use to identify or even manage access to your development environment|
| `project:lw-wizard`, `app:poc-app` | Use to identify or even manage access to a project |
| `dataresidency:germany`, `compliance:hipaa`, `compliance:pii` | Use to define compliance requirements |
| `schedule:24x7`, `maxruntime:12days` | Use to help you automate optimization |
{: caption="Table 1. Tag syntax" caption-side="top"}


## Creating tags
{: #create}

### Creating user tags
{: #create-user-tags}

You don't need to create user tags to attach them to resources. Go to the [Attaching and detaching tags on a resource](/docs/account?topic=account-attaching-and-detaching-tags-on-a-resource) for the following steps.

### Creating access management tags in the console
{: #create-access-console}
{: ui}

Before you can attach your access management tags to individual resources, you need to create them first. To create access management tags, you need to have administrator role on either the Tagging Service that is listed under the Account management services or on all Account management services.

{{site.data.keyword.cloud}} allows up to 250 access management tags per account.
{: note}

1. Go to **Manage** > **Account** in the {{site.data.keyword.cloud}} console, and select **Tags**.
2. Click **Access management tags**.
3. Type the names of your tags, and click **Create Tags**. These tags are now ready to be attached to resources and to be written to access policies.

For a full tutorial, see [Controlling access to resources by using tags](/docs/account?topic=account-access-tags-tutorial).

### Creating access management tags by using the CLI
{: #create-access-cli}
{: cli}

1. Log in to {{site.data.keyword.Bluemix_notm}} CLI. If you have multiple accounts, you are prompted to select which account to use. If you do not specify a region with the `-r` flag, you must also select a region.

    ```bash
    ibmcloud login
    ```
    {: codeblock}

    If your credentials are rejected, you might be using a federated ID. To log in with a federated ID, use the `--sso` flag. See [Logging in with a federated ID](/docs/account?topic=account-federated_id) for more details.
    {: tip}
    
    If it's your first time using the {{site.data.keyword.cloud_notm}} CLI, check out the [getting started tutorial](/docs/cli?topic=cli-getting-started).

2. Enter the **`ibmcloud resource tag-create`** command to create an access management tag in your account. This example creates a tag that is called `project:myproject`: 

    ```bash
    ibmcloud resource tag-create --tag-names project:myproject
    ```
    {: codeblock} 
 

For more information, see the [`ibmcloud resource` command reference](/docs/cli?topic=cli-ibmcloud_commands_resource).

### Creating access management tags by using the API
{: #create-access-api}
{: api}

You can programmatically create access management tags by calling the [Global Search and Tagging - Tagging API](/apidocs/tagging#create-tag){: external} as shown in the following sample request. The example creates a tag that is called `project:myproject`.

```bash
curl -X POST -H "Authorization: {iam_token}" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-d '{ "tag_names": ["project:myproject"] }' \
"tags.global-search-tagging.cloud.ibm.com/v3/tags?tag_type=access"
```
{: pre}
{: curl}

```java
CreateTagOptions createTagOptions = new CreateTagOptions.Builder()
    .addTagNames("project:myproject")
    .tagType("access")
    .build();

Response<CreateTagResults> response = service.createTag(createTagOptions).execute();
CreateTagResults createTagResults = response.getResult();
System.out.println(createTagResults);
```
{: codeblock}
{: java}

```javascript
const params = {
  tagNames: ['project:myproject'],
  tagType: 'access',
};

globalTaggingService.createTag(params)
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
create_tag_results = global_tagging_service.create_tag(
  tag_names=['project:myproject'],
  tag_type='access').get_result()

print(json.dumps(create_tag_results, indent=2))
```
{: codeblock}
{: python}

```go
createTagOptions := globalTaggingService.NewCreateTagOptions(
  []string{"project:myproject"},
)
createTagOptions.SetTagType("access")

createTagResults, response, err := globalTaggingService.CreateTag(createTagOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(createTagResults, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

### Creating access management tags by using Terraform
{: #create-access-terraform}
{: terraform}

You can create access management tags by using Terraform. 

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
1. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to create access management tags by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}. The following example creates the access management tag `ibm_tag` to the `ibm` resource for the resource ID `ibm_satellite_location.location.crn`. 
    
   ```terraform
   resource "ibm_resource" "ibm" {
   resource_id = ibm_satellite_location.location.crn
   tags        = [ "ibm_tag" ]
   }
   ```
    {: codeblock}

1. Initialize the Terraform CLI.
   
   ```terraform
   terraform init
   ```
   {: pre}

1. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to create access management tags.
   
   ```terraform
   terraform plan
   ```
   {: pre}

1. Create the access management tags.

   ```terraform
   terraform apply
   ```
   {: pre}

## Searching for tags in the console 
{: #search-tags}
{: ui}

You can search for tags by using any of the following methods:

* Try the search bar that is located in the {{site.data.keyword.cloud}} console menu bar.
* You can filter your resource list by the tag you are searching for.
* From the application detail page, you can locate the tags that are associated with that resource.

The same tag can be attached to multiple resources by different users in the same billing account, and not all users have visibility on all resources on the account.
{: note}

## Searching for tags by using the CLI 
{: #search-tags-cli-link}
{: cli}

To search for tags by using the CLI, see [Searching for resources](/docs/account?topic=account-searching-for-resources#searching-cl). 

## Searching for tags by using the API 
{: #search-tags-api-link}
{: api}

To search for tags by using the API, see [Searching for resources](/docs/account?topic=account-searching-for-resources#searching-api). 


## Tagging for resellers
{: #resell}

All tags are visible to all members of an account. To view the policy of an access management tag, the user is required to have at least a viewer role on the tagged resource. If your account is associated with different organizations, if you're a reseller for example, you might want to recommend your customers not to store sensitive information in tags.

To control tag visibility, circulate tagging guidelines and let users know that tags are visible account-wide.

Use codes rather than names for clients and accounts and avoid placing sensitive information in tags.
{: tip}
