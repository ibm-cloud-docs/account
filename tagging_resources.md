---

copyright:

  years: 2018, 2024

lastupdated: "2024-09-17"

keywords: tags, user tags, access management tags, attach tags, detach tags, full list of tags, how to use tags

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Working with tags
{: #tag}

Use tags to organize, track usage costs, and even manage access to your resources and service IDs. You can tag related resources and view them throughout your account by filtering by tags from your resource list.
{: shortdesc}

To see a full list of tags in your account, go to **Manage** > **Account** in the {{site.data.keyword.cloud}} console, and select **Tags**.
{: ui}

You can apply **user tags** to organize your resources and service IDs and easily find them later. User tags can also help you with identifying specific team usage or cost allocation. By creating **access management tags**, you can control access to your resources and service IDs without requiring updates to your IAM policies.

## Tag types
{: #tag-types}

There are three types of tags: service, user, and access management.

User tags
:   User tags are added to resources or service IDs by an authorized user in the account.  Add user tags to your resources to organize, track, and manage costs for related resources. When you use a consistent tagging schema to identify which resources are tied to specific teams, you can group and filter by those tags when you analyze costs within your exported usage report.

Consider using a project to organize and track resources across accounts. Resources that are created by deploying a project automatically have service tags attached with the project ID and configuration ID. This way, you don't have to manage tagging related resources maually.
{: tip}

Service tags
:   Service tags are attached by services. No users are authorized to attach or detach service tags on a resource, even if they have access to manage tags on the resource.

Resources that are created by deploying a project are automatically tagged with the project ID and configuration ID, which is available on your usage report. Use projects to help you track spending for projects. For more information, see [Tracking usage and spend for projects](/docs/enterprise-management?topic=enterprise-management-project-usage-spend).
{: note}

Access management tags
:   Access management tags are used to manage access to resources. They can be created in advance for use in access policies, which grant access to the resources where access management tags are attached. Only the account administrator can create access management tags, and they can delete them only when the tags aren't attached to any resources in the account. Only the resource administrator can attach and detach access management tags on the resource itself.

## Tagging rules
{: #limits}

Tags are not case-sensitive, any uppercase characters are converted to lowercase, and the maximum length of a tag is 128 characters. The permitted characters are A-Z, 0-9, spaces, underscore, hyphen, period, and colon. The only supported format for access management tags is `key:value`. The use of a colon formats the tag into a string that isolates two logical parts, like a `env:dev` pair. A comma separates multiple tags and can't be used within the tag name itself.

Tags are visible account-wide and can be replicated across geographic regions. Since tags are not regulated information, avoid creating tags that use personal information, such as your name, address, phone number, email address, or other identifying or proprietary information.
{: important}

### Sample tags and syntax
{: #sample-and-syntax}

You can apply tags to help you organize and manage your resources, service IDs, and access policies. Consider writing tags as `key:value` pairs to help coordinate your development environments, projects, compliance, and optimization throughout your organization. See the following table for some examples of tags that you might want to use.

| Tag | Description |
|----------|---------|
| `env:dev`, `env:test`, `env:stage`, `env:prod` | Use to identify or even manage access to your development environment|
| `project:lw-wizard`, `app:poc-app` | Use to identify or even manage access to a project |
| `dataresidency:germany`, `compliance:hipaa`, `compliance:pii` | Use to define compliance requirements |
| `schedule:24x7`, `maxruntime:12days` | Use to help you automate optimization |
{: caption="Tag syntax" caption-side="top"}


## Creating tags
{: #create}

### Creating user tags
{: #create-user-tags}

You don't need to create user tags to attach them to resources or service IDs. For more information, see [Attaching and detaching tags](/docs/account?topic=account-attaching-and-detaching-tags-on-a-resource).

### Creating access management tags in the console
{: #create-access-console}
{: ui}

Before you can attach your access management tags to individual resources or service IDs, you need to create them first. To create access management tags, you must have the administrator role on either the **Tagging Service** or on **All Account management services**.

{{site.data.keyword.cloud}} allows up to 250 access management tags per account.
{: note}

1. Go to **Manage** > **Account** in the {{site.data.keyword.cloud}} console, and select **Tags**.
2. Click **Access management tags**.
3. Type the names of your tags, and click **Create Tags**. These tags are now ready to be attached to resources or service IDs, and to scope access policies.

Next, see [Attaching and detaching tags](/docs/account?topic=account-attaching-and-detaching-tags-on-a-resource). For a full tutorial, see [Controlling access to resources by using tags](/docs/account?topic=account-access-tags-tutorial).

### Creating access management tags by using the CLI
{: #create-access-cli}
{: cli}

Before you can attach your access management tags to individual resources or service IDs, you need to create them first. To create access management tags, you need to have administrator role on either the Tagging Service that is listed under the Account management services or on all Account management services.

{{site.data.keyword.cloud}} allows up to 250 access management tags per account.
{: note}

1. Log in to {{site.data.keyword.Bluemix_notm}} CLI. If you have multiple accounts, you are prompted to select which account to use. If you do not specify a region with the `-r` flag, you must also select a region.

    ```bash
    ibmcloud login
    ```
    {: codeblock}

    If your credentials are rejected, you might be using a federated ID. To log in with a federated ID, use the `--sso` flag. See [Logging in with a federated ID](/docs/account?topic=account-federated_id) for more details.
    {: tip}

    If it's your first time using the {{site.data.keyword.cloud_notm}} CLI, check out the [getting started tutorial](/docs/cli?topic=cli-getting-started).

1. Enter the **`ibmcloud resource tag-create`** command to create an access management tag in your account. This example creates a tag that is called `project:myproject`:

    ```bash
    ibmcloud resource tag-create --tag-names project:myproject
    ```
    {: codeblock}

For more information, see the [`ibmcloud resource` command reference](/docs/cli?topic=cli-ibmcloud_commands_resource).

Next, see [Attaching and detaching tags](/docs/account?topic=account-attaching-and-detaching-tags-on-a-resource&interface=cli#attach-cli).

### Creating access management tags by using the API
{: #create-access-api}
{: api}

Before you can attach your access management tags to individual resources or service IDs, you need to create them first. To create access management tags, you need to have administrator role on either the Tagging Service that is listed under the Account management services or on all Account management services.

{{site.data.keyword.cloud}} allows up to 250 access management tags per account.
{: note}

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

Next, see [Attaching and detaching tags](/docs/account?topic=account-attaching-and-detaching-tags-on-a-resource&interface=api#attach-api).

### Creating access management tags by using Terraform
{: #create-access-terraform}
{: terraform}

Before you can create access management tags by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://developer.hashicorp.com/terraform/language){: external}.
- Before you can attach your access management tags to individual resources or service IDs, you need to create them first. To create access management tags, you need to have administrator role on either the Tagging Service that is listed under the Account management services or on all Account management services.

{{site.data.keyword.cloud}} allows up to 250 access management tags per account.
{: note}

Use the following steps to create access management tags by using Terraform:

1. Create an argument in your `main.tf` file. The following example creates the access management tag `ibm_tag` to the `ibm` resource for the resource ID `ibm_satellite_location.location.crn`.

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

## Searching for tags in the console
{: #search-tags}
{: ui}

You can search for tags and tag related resources by using any of the following methods:

* Try the search bar that is located in the {{site.data.keyword.cloud}} console menu bar.
* You can filter your resource list by the tag you are searching for.
* From the application detail page, you can locate the tags that are associated with that resource.

The same tag can be attached to multiple resources and service IDs by different users in the same billing account, and not all users have visibility on all resources on the account.
{: note}

## Searching for tags by using the CLI
{: #search-tags-cli-link}
{: cli}

To search for tags by using the CLI, see [Searching for resources](/docs/account?topic=account-searching-for-resources#searching-cl).

## Searching for tags by using the API
{: #search-tags-api-link}
{: api}

To search for tags by using the API, see [Searching for resources](/docs/account?topic=account-searching-for-resources#searching-api).

A common use case for searching for tags by using the API is retrieving the tags that are attached to a resource. There are a couple of options for doing that.

The preferred option is the [Search API](/apidocs/search){: external}, as shown in the following example.

```bash
curl -s -H'Content-type:application/json' -H'Accept:application/json' -H"Authorization:Bearer $IAM_TOKEN" \
-X POST 'https://api.global-search-tagging.cloud.ibm.com/v3/resources/search' \
-d'{"query":"crn:\"crn:v1:bluemix:public:codeengine:us-south:a/aabbccddeeff00112233445566778899:aabbccdd-1234-4321-aaaa-001122334455::\"", \
"fields":["crn","name","tags", "access_tags", "service_tags"]}'
```
{: codeblock}

If the resource with the given CRN exists and you can read it, then you get the following example output, which includes all of the tag types attached to the resource:

```JSON
{
  "items": [
    {
      "name": "my-codeengine-instance",
      "crn": "crn:v1:bluemix:public:codeengine:us-south:a/aabbccddeeff00112233445566778899:aabbccdd-1234-4321-aaaa-001122334455::",
      "tags": ["one", "two"],
      "access_tags": ["atag:one", "another-tag:two"],
       "service_tags": ["service-tag:one", "service-tag:two"]
     }
  ],
  "limit": 10,
  "search_cursor": "..."
}
```
{: codeblock}

You can also use the [Get tags](https://cloud.ibm.com/apidocs/tagging#list-tags) API with the `attached_to` query parameter to obtain the same result. However, the Get tags API is strictly rate limited and doesn't return all of the tag types in a single call as the `/v3/resources/search` does which is the reason it's not the suggested method.

If you need to accomplish the task by using the `ibmcloud` command line, then use the `resource search` command. By default, it outputs all of the tags that are attached to the resources.

For example, if you use the command `ibmcloud resource search name:my-codeengine-instance`, you get the following output:

```bash
Name:                my-codeengine-instance
Location:            us-south
Family:              resource_controller
Resource Type:       resource-instance
Resource Group ID:   a58ebff30cab4b30bc67de9fec9cfda5
CRN:                 crn:v1:staging:public:codeengine:us-south:a/aa00ffbccdb34a6fbe7a6499ce091aaa:0a01030b-1234-1234-aaaa-002245318e88::
Tags:                one,two
Service Tags:        service-tag:one,service-tag:two
Access Tags:         atag:one,another-tag:two
```
{: codeblock}

## Tagging for resellers
{: #resell}

All tags are visible to all members of an account. To view the policy of an access management tag, the user must be assigned at least a viewer role on the tagged resource. If your account is associated with different organizations, if you're a reseller for example, you might want to recommend your customers not to store sensitive information in tags.

To control tag visibility, circulate tagging guidelines and let users know that tags are visible account-wide.

Use codes rather than names for clients and accounts and avoid placing sensitive information in tags.
{: tip}
