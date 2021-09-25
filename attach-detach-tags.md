---

copyright:

  years: 2021
lastupdated: "2021-09-24"

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
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}
{:terraform: .ph data-hd-interface='terraform'}

# Attaching and detaching tags on a resource

You can attach and detach tags on a resource through the console, CLI, or API. To attach or detach a tag on a resource, appropriate permission is required. For more information, see [Granting users access to tag resources](/docs/account?topic=account-access).

## Attaching and detaching tags on a resource in the console 
{: #attach-detach-console}
{: ui}

1. From the {{site.data.keyword.cloud}} console, click the Menu icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list** to view your list of resources.
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

To attach a tag to a resource, use the [**`ibmcloud resource tag-attach`**](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_tag_attach) command. The allowed values for `tag-type` are `user` for user tags and `access` for access management tags. The default value is `user`. The following example shows how to attach a user tag called `MyTag` to a resource named `MyResource`:

```bash
ibmcloud resource tag-attach --tag-name MyTag --resource-name  'MyResource'
```
{: codeblock}

An example for attaching an access management tag called `project:myproject` to a resource named `MyResource`:

```bash
ibmcloud resource tag-attach --tag-names project:myproject --resource-name  'MyResource' --tag-type access 
```
{: codeblock}    
    
## Detaching tags from a resource by using the CLI
{: #detach-cli}
{: cli}

To detach a tag from a resource, use the [**`ibmcloud resource tag-detach`**](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_tag_detach) command. An example to detach a user tag called `MyTag` from a resource named `MyResource`:

```bash
ibmcloud resource tag-detach --tag-names MyTag —resource-name 'MyResource'
```
{: codeblock}

An example to detach an access management tag called `project:myproject` from a resource named `MyResource`:

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

You can programmatically attach tags by calling the [Global Search and Tagging - Tagging API](/apidocs/tagging#attach-tag){: external} as shown in the following sample requests. The allowed values for the `tag_type` query parameter are: `user` for user tags and `access` for access management tags. The following example shows how to attach an access management tag called `project:myproject` to a service instance. 

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

3. Call the following:
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

You can programmatically detach tags by calling the [Global Search and Tagging - Tagging API](/apidocs/tagging#detach-tag){: external} as shown in the following sample requests. The allowed values for the `tag_type` query parameter are: `user` for user tags and `access` for access management tags. The following example shows how to detach an access management tag called `project:myproject` from a service instance.

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

3. Call the following:
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

You can attach tags by using Terraform. 

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
1. Attach a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to attach access management tags by by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}. The following example attaches the `imb_tag` tag to the `ibm` resource for the resource ID `ibm_satellite_location.location.crn`.

   ```terraform
   data "ibm_satellite_location" "location" {
   location  = var.location
   }
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

1. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to attach tags.

   ```terraform
   terraform plan
   ```
   {: pre}

1. Attach the tags.

   ```terraform
   terraform apply
   ```
   {: pre}
   
