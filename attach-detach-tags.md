---

copyright:

  years: 2021, 2024
lastupdated: "2024-06-11"

keywords: tags, user tags, access management tags, attach tags, detach tags, attach tags ui, attach tags cli, attach tags api, detach tags ui, detach tags api, detach tags cli

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Attaching and detaching tags
{: #attaching-and-detaching-tags-on-a-resource}

You can attach and detach tags on a resource or service ID through the console, CLI, or API. To attach or detach a tag on a resource or service ID, users must be assigned the appropriate permission. For more information, see [Granting users access to tag resources](/docs/account?topic=account-access).
{: shortdesc}

A resource can have a maximum of 1000 user tags, 1000 service tags, and 250 access tags.
{: note}

## Attaching and detaching tags on a resource in the console
{: #attach-detach-console}
{: ui}

1. From the {{site.data.keyword.cloud}} console, click the Navigation Menu icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list** to view your list of resources.
1. Locate the specific resource in the list.
1. To attach a tag to the resource, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions")  > **Add tags**.
1. Enter the name of the tag, and click **Save**.
1. To detach the tag from the resource, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") next to the tag in your resource list.

   When you detach an access management tag from a resource, any associated access policies are also detached from that resource.
   {: note}

## Attaching tags to a resource by using the CLI
{: #attach-cli}
{: cli}

Log in to [{{site.data.keyword.cloud}} CLI](/docs/cli?topic=cli-getting-started) and select your account to run the appropriate CLI command.

To attach a tag to a resource, use the [**`ibmcloud resource tag-attach`**](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_tag_attach) command. The allowed values for `tag-type` are `user` for user tags and `access` for access management tags. The default value is `user`. The following example shows how to attach a user tag that is called `MyTag` to a resource named `MyResource`:

```bash
ibmcloud resource tag-attach --tag-names MyTag --resource-name  'MyResource'
```
{: codeblock}

An example for attaching an access management tag called `project:myproject` to a resource named `MyResource`:

```bash
ibmcloud resource tag-attach --tag-names project:myproject --resource-name  'MyResource' --tag-type access 
```
{: codeblock}

## Updating key:value tags of a resource by using the CLI
{: #update-key-value-cli}
{: cli}

Log in to [{{site.data.keyword.cloud}} CLI](/docs/cli?topic=cli-getting-started) and select your account to run the appropriate CLI command.

If you manage tags in the format `key:value`, you can update the `value` atomically,
without first detach the `key:old-value` and attach the new `key:new-value`.

To update the value of a tag in the format `key:value`, use the [**`ibmcloud resource tag-attach`**](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_tag_attach) command with the `--update` option. The allowed values for `tag-type` are `user` for user tags and `access` for access management tags. The default value is `user`. The following example shows how to update to `production` the value of the `env` user tag on a resource named `MyResource`:

```bash
ibmcloud resource tag-attach --tag-names 'env:production' --resource-name 'MyResource' --update
```
{: codeblock}

Add the `tag-type` option to the previous command to update an access management tag:

```bash
ibmcloud resource tag-attach --tag-names 'env:production' --resource-name 'MyResource' --update --tag-type access 
```
{: codeblock}

## Replacing all tags of a resource with a new set of tags by using the CLI
{: #update-key-value-cli}
{: cli}

Log in to [{{site.data.keyword.cloud}} CLI](/docs/cli?topic=cli-getting-started) and select your account to run the appropriate CLI command.

The attach operation results in adding tags to a resource in addition to what it might already have. There are cases where you need to replace the existing tags that are attached to a resource with a new set.

To replace all resource's tags with a new set of tags, use the [**`ibmcloud resource tag-attach`**](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_tag_attach) command with the `--replace` option. The allowed values for `tag-type` are `user` for user tags and `access` for access management tags. The default value is `user`. The following example shows how to set the tags `tag1`, `tag2`, and `tag3` on a resource that is named `MyResource`, and remove all of those that it might already have:

```bash
ibmcloud resource tag-attach --tag-names 'tag1,tag2,tag3' --resource-name 'MyResource' --replace
```
{: codeblock}

Add the `tag-type` option to the previous command to set access management tags. For example, to replace all access management tags with the `compliance:hipaa`:

```bash
ibmcloud resource tag-attach --tag-names 'compliance:hipaa' --resource-name 'MyResource' --replace --tag-type access 
```
{: codeblock}

## Detaching tags from a resource by using the CLI
{: #detach-cli}
{: cli}

To detach a tag from a resource, use the [**`ibmcloud resource tag-detach`**](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_tag_detach) command. The following is an example to detach a user tag called `MyTag` from a resource named `MyResource`:

```bash
ibmcloud resource tag-detach --tag-names MyTag —resource-name 'MyResource'
```
{: codeblock}

You can use the `*` wildcard to detach tags, which is useful to detach tags in the format `key:value`, and to detach all tags. For example, if you want to detach the `env` tag from `MyResource`, regardless of its value, you can run the following command:

```bash
ibmcloud resource tag-detach --tag-names 'env:*' —resource-name 'MyResource'
```
{: codeblock}

To detach all tags from `MyResource`, you can use the following command:

```bash
ibmcloud resource tag-detach --tag-names '*' —resource-name 'MyResource'
```
{: codeblock}

The following is an example to detach an access management tag called `project:myproject` from a resource named `MyResource`:

```bash
ibmcloud resource tag-detach --tag-names project:myproject —resource-name 'MyResource' --tag-type access
```
{: codeblock}

For more information, see the [`ibmcloud resource` command reference](/docs/cli?topic=cli-ibmcloud_commands_resource).

When you detach an access management tag from a resource, any associated access policies are also detached from that resource.
{: note}

## Attaching tags to a resource by using the API
{: #attach-api}
{: api}

You can programmatically attach tags by calling the [Global Search and Tagging - Tagging API](/apidocs/tagging#attach-tag){: external} as shown in the following sample requests. The allowed values for the `tag_type` query parameter are: `user` for user tags and `access` for access management tags. The following example shows how to attach an access management tag that is called `project:myproject` to a service instance.

1. Find the unique identifier for your resource by calling the following command:

   ```bash
   curl -v -X POST -k --header 'Content-Type: application/json'
   --header 'Accept: application/json'
   --header 'Authorization: bearer  <your IAM token>'
   -d '{"query": "name:myresource"}' 'https://api.global-search-tagging.cloud.ibm.com/v3/resources/search'
   ```
   {: codeblock}
   {: curl}

   ```java
   SearchOptions searchOptions = new SearchOptions.Builder()
    .query("GST-sdk-*")
    .fields(new java.util.ArrayList<String>(java.util.Arrays.asList("crn")))
    .searchCursor(searchCursor)
    .build();

   Response<ScanResult> response = service.search(searchOptions).execute();
   ScanResult scanResult = response.getResult();

   System.out.println(scanResult);
   ```
   {: codeblock}
   {: java}

   ```javascript
   const params = {
   query: 'GST-sdk-*',
   fields: ['crn'],
   searchCursor: searchCursor,
   };

   globalSearchService.search(params)
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
   response = global_search_service.search(query='GST-sdk-*',
                      fields=['crn'])
   scan_result = response.get_result()

   print(json.dumps(scan_result, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   searchOptions := globalSearchService.NewSearchOptions()
   searchOptions.SetLimit(10)
   searchOptions.SetQuery("GST-sdk-*")
   searchOptions.SetFields([]string{"crn"})

   scanResult, response, err := globalSearchService.Search(searchOptions)
   if err != nil {
    panic(err)
   }
   b, _ := json.MarshalIndent(scanResult, "", "  ")
   fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}

2. Extract the value of the CRN field from the response.

   ```bash
      {
      "items": [
        {
          "crn": "crn:v1:bluemix:public:cf:au-syd:a/000af2ea12345aabb1234567801fffab::cf-organization:aaaf4100-0011-2233-1111-11aaffee0011"
        }
      ],
      "limit": 1,
      "search_cursor": "e34535305339jg0rntt39nt3nu5tt9yn3u5ntt329nutt92u4ntt92u4t9u5gt2u5gt92u4n5g982458hg2t45hg9u42rg9t2u49gh285ght28h5t2835th85ht318h4tg9138h4tg91u3hgt931hg45918h34tg18h43hgt31hgt3rng0fnefvodnfvpojdpbojarfdbpojeafrbeafbjeqpnrqngrpqgrhbHNlIiwiY2FuVGFnIjoiZmFsc2UiLCJsdfshfksdhfkshfdkshfdkhkhewrkfehrkhkwhfkwrhkfhrgk3h5k3h45k3hk45hgk3hgk3hfk3h4k3hfkrfh3rkgh3krghk3rgh3kghk3hgk3hgk3rhgdWJsaWM6Y2Y6YXUtwriretoeiroteito4i5ot4i5oyti45ito4tio45ito45io5ogno5iogn5oin5oingoi5o5ngogo4ngo4ngro3jrong3gor3g3gno3jrgo3jrngo3ngro3g32ODQiXX0t"
    }
   ```
   {: codeblock}

3. Call the following command:

   ```bash
   curl -X POST -H "Authorization: {iam_token}" \
   -H "Accept: application/json" \
   -H "Content-Type: application/json" \
   -d '{ "resources": [{ "resource_id": "crn:v1:bluemix:public:cloud-object-storage:global:a/59bcbfa6ea2f006b4ed7094c1a08dcdd:1a0ec336-f391-4091-a6fb-5e084a4c56f4::" }], "tag_names": ["project:myproject"] }' \
   "https://tags.global-search-tagging.cloud.ibm.com/v3/tags/attach?tag_type=access"
   ```
   {: codeblock}
   {: curl}

   ```java
   Resource resourceModel = new Resource.Builder().resourceId(resourceCRN).build();
   AttachTagOptions attachTagOptions = new AttachTagOptions.Builder()
   .addResources(resourceModel)
   .addTagNames("project:myproject")
   .tagType("access")
   .build();

   Response<TagResults> response = service.attachTag(attachTagOptions).execute();
   TagResults tagResults = response.getResult();
   System.out.println(tagResults.toString());
   ```
   {: codeblock}
   {: java}

   ```javascript
   const resourceModel = {
   resource_id: resourceCrn,
   };

   const params = {
   resources: [resourceModel],
   tagNames: ["project:myproject"],
   tagType: 'access',
   };

   globalTaggingService.attachTag(params)
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
   resource_model = {'resource_id': resource_crn}

   tag_results = global_tagging_service.attach_tag(
   resources=[resource_model],
   tag_names=['project:myproject'],
   tag_type='access').get_result()


   print(json.dumps(tag_results, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   resourceModel := &globaltaggingv1.Resource{
   ResourceID: &resourceCRN,
   }

   attachTagOptions := globalTaggingService.NewAttachTagOptions(
   []globaltaggingv1.Resource{*resourceModel},
   )
   attachTagOptions.SetTagNames([]string{"project:myproject"})
   attachTagOptions.SetTagType("access")

   tagResults, response, err := globalTaggingService.AttachTag(attachTagOptions)
   if err != nil {
   panic(err)
   }
   b, _ := json.MarshalIndent(tagResults, "", "  ")
   fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}

## Detaching tags from a resource by using the API
{: #detach-api}
{: api}

You can programmatically detach tags by calling the [Global Search and Tagging - Tagging API](/apidocs/tagging#detach-tag){: external} as shown in the following sample requests. The allowed values for the `tag_type` query parameter are: `user` for user tags and `access` for access management tags. The following example shows how to detach an access management tag that is called `project:myproject` from a service instance:

1. Find the unique identifier for your resource by calling the following command:

   ```bash
   curl -v -X POST -k --header 'Content-Type: application/json'
   --header 'Accept: application/json'
   --header 'Authorization: bearer  <your IAM token>'
   -d '{"query": "name:myresource"}' 'https://api.global-search-tagging.cloud.ibm.com/v3/resources/search'
   ```
   {: codeblock}
   {: curl}

   ```java
   SearchOptions searchOptions = new SearchOptions.Builder()
    .query("GST-sdk-*")
    .fields(new java.util.ArrayList<String>(java.util.Arrays.asList("crn")))
    .searchCursor(searchCursor)
    .build();

   Response<ScanResult> response = service.search(searchOptions).execute();
   ScanResult scanResult = response.getResult();

   System.out.println(scanResult);
   ```
   {: codeblock}
   {: java}

   ```javascript
   const params = {
   query: 'GST-sdk-*',
   fields: ['crn'],
   searchCursor: searchCursor,
   };

   globalSearchService.search(params)
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
   response = global_search_service.search(query='GST-sdk-*',
                      fields=['crn'])
   scan_result = response.get_result()

   print(json.dumps(scan_result, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   searchOptions := globalSearchService.NewSearchOptions()
   searchOptions.SetLimit(10)
   searchOptions.SetQuery("GST-sdk-*")
   searchOptions.SetFields([]string{"crn"})

   scanResult, response, err := globalSearchService.Search(searchOptions)
   if err != nil {
    panic(err)
   }
   b, _ := json.MarshalIndent(scanResult, "", "  ")
   fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}

2. Extract the value of the CRN field from the response.

   ```bash
      {
      "items": [
        {
          "crn": "crn:v1:bluemix:public:cf:au-syd:a/000af2ea12345aabb1234567801fffab::cf-organization:aaaf4100-0011-2233-1111-11aaffee0011"
        }
      ],
      "limit": 1,
      "search_cursor": "e34535305339jg0rntt39nt3nu5tt9yn3u5ntt329nutt92u4ntt92u4t9u5gt2u5gt92u4n5g982458hg2t45hg9u42rg9t2u49gh285ght28h5t2835th85ht318h4tg9138h4tg91u3hgt931hg45918h34tg18h43hgt31hgt3rng0fnefvodnfvpojdpbojarfdbpojeafrbeafbjeqpnrqngrpqgrhbHNlIiwiY2FuVGFnIjoiZmFsc2UiLCJsdfshfksdhfkshfdkshfdkhkhewrkfehrkhkwhfkwrhkfhrgk3h5k3h45k3hk45hgk3hgk3hfk3h4k3hfkrfh3rkgh3krghk3rgh3kghk3hgk3hgk3rhgdWJsaWM6Y2Y6YXUtwriretoeiroteito4i5ot4i5oyti45ito4tio45ito45io5ogno5iogn5oin5oingoi5o5ngogo4ngo4ngro3jrong3gor3g3gno3jrgo3jrngo3ngro3g32ODQiXX0t"
    }
   ```
   {: codeblock}

3. Call the following command:

   ```bash
   curl -X POST -H "Authorization: {iam_token}" \
   -H "Accept: application/json" \
   -H "Content-Type: application/json" \
   -d '{ "resources": [{ "resource_id": "crn:v1:bluemix:public:cloud-object-storage:global:a/59bcbfa6ea2f006b4ed7094c1a08dcdd:1a0ec336-f391-4091-a6fb-5e084a4c56f4::" }], "tag_names": ["project:myproject"] }' \
   "https://tags.global-search-tagging.cloud.ibm.com/v3/tags/detach?tag_type=access"
   ```
   {: codeblock}
   {: curl}

   ```java
   Resource resourceModel = new Resource.Builder().resourceId(resourceCRN).build();
   DetachTagOptions detachTagOptions = new DetachTagOptions.Builder()
   .addResources(resourceModel)
   .addTagNames("project:myproject")
   .tagType("access")
   .build();

   Response<TagResults> response = service.detachTag(detachTagOptions).execute();
   TagResults tagResults = response.getResult();
   System.out.println(tagResults.toString());
   ```
   {: codeblock}
   {: java}

   ```javascript
   const resourceModel = {
   resource_id: resourceCrn,
   };

   const params = {
   resources: [resourceModel],
   tagNames: ["project:myproject"],
   tagType: 'access',
   };

   globalTaggingService.detachTag(params)
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
   resource_model = {'resource_id': resource_crn}

   tag_results = global_tagging_service.detach_tag(
   resources=[resource_model],
   tag_names=['project:myproject'],
   tag_type='access').get_result()

   print(json.dumps(tag_results, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   resourceModel := &globaltaggingv1.Resource{
   ResourceID: &resourceCRN,
   }

   detachTagOptions := globalTaggingService.NewDetachTagOptions(
   []globaltaggingv1.Resource{*resourceModel},
   )
   detachTagOptions.SetTagNames([]string{"project:myproject"})
   detachTagOptions.SetTagType("access")

   tagResults, response, err := globalTaggingService.DetachTag(detachTagOptions)
   if err != nil {
   panic(err)
   }
   b, _ := json.MarshalIndent(tagResults, "", "  ")
   fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}

   When you detach an access management tag from a resource, any associated access policies are also detached from that resource.
   {: note}

## Attaching tags to a resource by using Terraform
{: #attach-terraform}
{: terraform}

Before you can attach tags to a resource by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://developer.hashicorp.com/terraform/language){: external}.

Use the following steps to attach tags to a resource by using Terraform:

1. The following example attaches the `imb_tag` tag to the `ibm` resource for the resource ID `ibm_satellite_location.location.crn`.

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


## Attaching tags to a service ID in the console
{: #am-tags-serviceid-ui}
{: ui}

To add a tag to a service ID, complete the following steps:

1. Choose to attach an access management tag or a user tag.
   - If you want to attach an access management tag, you must first create the tag. For more information, see [Creating tags](/docs/account?topic=account-tag&interface=ui#create).
   - If you want to attach a user tag, you don't need to create the user tag to attach it to resources or service IDs. Attaching the tag also creates it.
1. Go to **Manage** > **Access (IAM)** > **Service IDs**.
1. Select the service ID that you want to tag.
1. Click **Add tag** ![Edit icon](../icons/edit-tagging.svg "Edit").
1. Enter the name of the tag, and press Enter.
1. Click **Save**.

When you tag a service ID, all policies that have resources that are scoped to your access management tag include access to this service ID.
{: note}

## Attaching tags to a service ID by using the CLI
{: #am-tags-serviceid-cli}
{: cli}

The allowed values for the `tag_type` query parameter are: `user` for user tags and `access` for access management tags. The following example shows how to attach an access management tag that is called project:myproject to a service ID.

To add a tag to a service ID, complete the following steps:

1. Choose to attach an access management tag or a user tag.
   - If you want to attach an access management tag, you must first create the tag. For more information, see [Creating tags](/docs/account?topic=account-tag&interface=cli#create).
   - If you want to attach a user tag, you don't need to create the user tag to attach it to resources or service IDs. Attaching the tag also creates it.
1. To attach the tag to your service ID, use the `tag-attach` command. For more information, see the [CLI command reference](/docs/cli?topic=cli-ibmcloud_commands_resource).

    ```bash
    ibmcloud resource tag-attach --tag-names project:myproject --resource-name 'ServiceIdName' --tag-type access
    ```
    {: codeblock}

When you tag a service ID, all policies that have resources that are scoped to your access management tag include access to this service ID.
{: note}

## Attaching tags to a service ID by using the API
{: #am-tags-serviceid-api}
{: api}

To add a tag to a service ID, complete the following steps:

1. Choose to attach an access management tag or a user tag.
   - If you want to attach an access management tag, you must first create the tag. For more information, see [Creating tags](/docs/account?topic=account-tag&interface=cli#create).
   - If you want to attach a user tag, you don't need to create the user tag to attach it to resources or service IDs. Attaching the tag also creates it.
1. Find the unique identifier for your service ID by calling the [IAM Identity Services](/apidocs/iam-identity-token-api#list-service-ids) with the following command:

   ```bash
   curl -X GET 'https://iam.cloud.ibm.com/v1/serviceids?account_id=ACCOUNT_ID&name=My-serviceID' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json'
   ```
   {: codeblock}
   {: curl}

   ```java
   ListServiceIdsOptions listServiceIdsOptions = new ListServiceIdsOptions.Builder()
      .accountId(accountId)
      .name(serviceIdName)
      .build();

   Response<ServiceIdList> response = service.listServiceIds(listServiceIdsOptions).execute();
   ServiceIdList serviceIdList = response.getResult();

   System.out.println(serviceIdList);
   ```
   {: codeblock}
   {: java}

   ```javascript
   const params = {
   accountId: accountId,
   name: serviceIdName,
   };

   try {
   const res = await iamIdentityService.listServiceIds(params)
   console.log(JSON.stringify(res.result, null, 2));
   } catch (err) {
   console.warn(err);
   }
   ```
   {: codeblock}
   {: javascript}

   ```python
   service_id_list = iam_identity_service.list_service_ids(
   account_id=account_id,
   name=serviceid_name
   ).get_result()

   print(json.dumps(service_id_list, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   listServiceIdsOptions := iamIdentityService.NewListServiceIdsOptions()
   listServiceIdsOptions.SetAccountID(accountID)
   listServiceIdsOptions.SetName(serviceIDName)

   serviceIDList, response, err := iamIdentityService.ListServiceIds(listServiceIdsOptions)
   if err != nil {
   panic(err)
   }
   b, _ := json.MarshalIndent(serviceIDList, "", "  ")
   fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}

1. Extract the value of the `crn` field from the response.

   ```bash
      {
   "offset": 0,
   "limit": 1,
   "first": {
      "href": "https://iam.cloud.ibm.com/v1/serviceids?account_id=accountId"
   },
   "next": {
      "href": "https://iam.cloud.ibm.com/v1/serviceids?pagetoken=pageToken"
   },
   "serviceids": {
      "id": "ServiceId-ee1103f8-e03b-4d02-a977-e540ebdffb16",
      "iam_id": "iam-ServiceId-ee1103f8-e03b-4d02-a977-e540ebdffb16",
      "entity_tag": "3-c46d2fd21b701adf7eb67cfd1a498fde",
      "crn": "crn:v1:bluemix:public:iam-identity::a/100abcde100a41abc100aza678abc0zz::serviceid:ServiceId-ee1103f8-e03b-4d02-a977-e540ebdffb16",
      "locked": false,
      "created_at": "2020-10-16T10:36+0000",
      "modified_at": "2020-10-16T10:36+0000",
      "account_id": "100abcde100a41abc100aza678abc0zz",
      "name": "serviceId-test",
      "description": "serviceId-test",
      "unique_instance_crns": []
   }
   }
   ```
   {: codeblock}

1. To attach the tag to your service ID, call the [Global Search and Tagging - Tagging API](/apidocs/tagging#detach-tag){: external} with the following command.

   Replace `{SERVICEID_CRN}` with the value that you extracted in the previous step.
   {: curl}

   Replace `(serviceidCRN)` with the value that you extracted in the previous step.
   {: java}

   Replace `serviceidCrn` with the value that you extracted in the previous step.
   {: javascript}

   Replace `serviceid_crn` with the value that you extracted in the previous step.
   {: python}

   Replace `&serviceidCRN` with the value that you extracted in the previous step.
   {: go}

   ```bash
   curl -X POST --header "Authorization: Bearer {iam_token}" --header "Accept: application/json" --header "Content-Type: application/json" -d '{ "resources": [{ "resource_id": "{SERVICEID_CRN}" }], "tag_names": ["tag_test_1", "tag_test_2"] }' "{base_url}/v3/tags/attach?tag_type=user"
   ```
   {: codeblock}
   {: curl}

   ```java
   Resource resourceModel = new Resource.Builder().resourceId(serviceidCRN).build();
   AttachTagOptions attachTagOptions = new AttachTagOptions.Builder()
      .addResources(resourceModel)
      .addTagNames("tag_test_1")
      .addTagNames("tag_test_2")
      .build();

   Response<TagResults> response = service.attachTag(attachTagOptions).execute();
   TagResults tagResults = response.getResult();
   System.out.println(tagResults.toString());
   ```
   {: codeblock}
   {: java}

   ```javascript
   const resourceModel = {
   resource_id: serviceidCrn,
   };

   const params = {
   resources: [resourceModel],
   tagNames: ["tag_test_1", "tag_test_2"],
   tagType: 'user',
   };

   globalTaggingService.attachTag(params)
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
   resource_model = {'resource_id': serviceid_crn}

   tag_results = global_tagging_service.attach_tag(
   resources=[resource_model],
   tag_names=['tag_test_1', 'tag_test_2'],
   tag_type='user').get_result()

   print(json.dumps(tag_results, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   resourceModel := &globaltaggingv1.Resource{
   ResourceID: &serviceidCRN,
   }

   attachTagOptions := globalTaggingService.NewAttachTagOptions(
   []globaltaggingv1.Resource{*resourceModel},
   )
   attachTagOptions.SetTagNames([]string{"tag_test_1", "tag_test_2"})
   attachTagOptions.SetTagType("user")

   tagResults, response, err := globalTaggingService.AttachTag(attachTagOptions)
   if err != nil {
   panic(err)
   }
   b, _ := json.MarshalIndent(tagResults, "", "  ")
   fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}


When you tag a service ID, all policies that have resources that are scoped to your access management tag include access to this service ID.
{: note}

## Detaching tags on a service ID in the console
{: #detach-tag-service-id-ui}
{: ui}

To detach a tag from a service ID, complete the following steps:

1. Go to **Manage** > **Access (IAM)** > **Service IDs**.
1. Click the  **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") in the Tags column.
1. Click the **Remove** icon ![Remove icon](../icons/delete.svg "Remove") on the tag that you want to detach from the service ID.
1. Click **Save**.

When you detach an access management tag from a service ID, any policies that are scoped to that tag no longer includes access to the service ID.
{: note}

## Detaching tags on a service ID by using the CLI
{: #detach-tag-service-id-cli}
{: cli}

To detach a tag on your service ID, use the `tag-detach` command. For more information, see the [CLI command reference](/docs/cli?topic=cli-ibmcloud_commands_resource).

```bash
ibmcloud resource tag-detach --tag-names project:myproject --resource-id  'ServiceIdName' --tag-type access
```
{: codeblock}

When you detach an access management tag from a service ID, any policies that are scoped that that tag no longer includes access the service ID.
{: note}

## Detaching tags on a service ID by using the API
{: #detach-tag-service-id-api}
{: api}

To detach a tag from a service ID, complete the following steps:

1. Find the unique identifier for your service ID by calling the [IAM Identity Services](/apidocs/iam-identity-token-api#list-service-ids) with the following command:

   ```bash
   curl -X GET 'https://iam.cloud.ibm.com/v1/serviceids?account_id=ACCOUNT_ID&name=My-serviceID' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json'
   ```
   {: codeblock}
   {: curl}

   ```java
   ListServiceIdsOptions listServiceIdsOptions = new ListServiceIdsOptions.Builder()
      .accountId(accountId)
      .name(serviceIdName)
      .build();

   Response<ServiceIdList> response = service.listServiceIds(listServiceIdsOptions).execute();
   ServiceIdList serviceIdList = response.getResult();

   System.out.println(serviceIdList);
   ```
   {: codeblock}
   {: java}

   ```javascript
   const params = {
   accountId: accountId,
   name: serviceIdName,
   };

   try {
   const res = await iamIdentityService.listServiceIds(params)
   console.log(JSON.stringify(res.result, null, 2));
   } catch (err) {
   console.warn(err);
   }
   ```
   {: codeblock}
   {: javascript}

   ```python
   service_id_list = iam_identity_service.list_service_ids(
   account_id=account_id,
   name=serviceid_name
   ).get_result()

   print(json.dumps(service_id_list, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   listServiceIdsOptions := iamIdentityService.NewListServiceIdsOptions()
   listServiceIdsOptions.SetAccountID(accountID)
   listServiceIdsOptions.SetName(serviceIDName)

   serviceIDList, response, err := iamIdentityService.ListServiceIds(listServiceIdsOptions)
   if err != nil {
   panic(err)
   }
   b, _ := json.MarshalIndent(serviceIDList, "", "  ")
   fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}

1. Extract the value of the `crn` field from the response.

   ```bash
      {
   "offset": 0,
   "limit": 1,
   "first": {
      "href": "https://iam.cloud.ibm.com/v1/serviceids?account_id=accountId"
   },
   "next": {
      "href": "https://iam.cloud.ibm.com/v1/serviceids?pagetoken=pageToken"
   },
   "serviceids": {
      "id": "ServiceId-ee1103f8-e03b-4d02-a977-e540ebdffb16",
      "iam_id": "iam-ServiceId-ee1103f8-e03b-4d02-a977-e540ebdffb16",
      "entity_tag": "3-c46d2fd21b701adf7eb67cfd1a498fde",
      "crn": "crn:v1:bluemix:public:iam-identity::a/100abcde100a41abc100aza678abc0zz::serviceid:ServiceId-ee1103f8-e03b-4d02-a977-e540ebdffb16",
      "locked": false,
      "created_at": "2020-10-16T10:36+0000",
      "modified_at": "2020-10-16T10:36+0000",
      "account_id": "100abcde100a41abc100aza678abc0zz",
      "name": "serviceId-test",
      "description": "serviceId-test",
      "unique_instance_crns": []
   }
   }
   ```
   {: codeblock}

1. To detach the tag on your service ID, call the [Global Search and Tagging - Tagging API](/apidocs/tagging#detach-tag){: external} with the following command.

   Replace `{SERVICEID_CRN}` with the value that you extracted in the previous step.
   {: curl}

   Replace `(serviceidCRN)` with the value that you extracted in the previous step.
   {: java}

   Replace `serviceidCrn` with the value that you extracted in the previous step.
   {: javascript}

   Replace `serviceid_crn` with the value that you extracted in the previous step.
   {: python}

   Replace `&serviceidCRN` with the value that you extracted in the previous step.
   {: go}

   ```bash
   curl -X POST --header "Authorization: Bearer {iam_token}" --header "Accept: application/json" --header "Content-Type: application/json" -d '{ "resources": [{ "resource_id": "{SERVICEID_CRN}" }], "tag_names": ["tag_test_1", "tag_test_2"] }' "{base_url}/v3/tags/detach?tag_type=user"
   ```
   {: codeblock}
   {: curl}

   ```java
   Resource resourceModel = new Resource.Builder().resourceId(serviceidCRN).build();
   DetachTagOptions detachTagOptions = new DetachTagOptions.Builder()
      .addResources(resourceModel)
      .addTagNames("tag_test_1")
      .addTagNames("tag_test_2")
      .tagType("user")
      .build();

   Response<TagResults> response = service.detachTag(detachTagOptions).execute();
   TagResults tagResults = response.getResult();
   System.out.println(tagResults.toString());
   ```
   {: codeblock}
   {: java}

   ```javascript
   const resourceModel = {
   resource_id: serviceidCrn,
   };

   const params = {
   resources: [resourceModel],
   tagNames: ["tag_test_1", "tag_test_2"],
   tagType: 'user',
   };

   globalTaggingService.detachTag(params)
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
   resource_model = {'resource_id': serviceid_crn}

   tag_results = global_tagging_service.detach_tag(
   resources=[resource_model],
   tag_names=['tag_test_1', 'tag_test_2'],
   tag_type='user').get_result()

   print(json.dumps(tag_results, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   resourceModel := &globaltaggingv1.Resource{
   ResourceID: &serviceidCRN,
   }

   detachTagOptions := globalTaggingService.NewDetachTagOptions(
   []globaltaggingv1.Resource{*resourceModel},
   )
   detachTagOptions.SetTagNames([]string{"tag_test_1", "tag_test_2"})
   detachTagOptions.SetTagType("user")

   tagResults, response, err := globalTaggingService.DetachTag(detachTagOptions)
   if err != nil {
   panic(err)
   }
   b, _ := json.MarshalIndent(tagResults, "", "  ")
   fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}

When you detach an access management tag from a service ID, any policies that are scoped to that tag no longer includes access to the service ID.
{: note}
