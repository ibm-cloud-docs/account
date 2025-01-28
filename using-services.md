---

copyright:

  years: 2018, 2025
lastupdated: lastupdated: "2025-01-28"

keywords: classic infrastructure assets, application development, services that work with classic infrastructure

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Using services with classic infrastructure assets
{: #api-services-infrastructure}

You can easily use API-based public {{site.data.keyword.Bluemix}} services with your classic infrastructure assets. All APIs are secure and encrypted so that your data is protected.

You can gain insights and cognitive knowledge by calling Watson APIs from your apps to make them more personalized. Or, use data and analytics services to tap into high-performance analytics for your apps. Or, choose database-as-a-service where you can leave the management to {{site.data.keyword.Bluemix_notm}}.

Modernize your application development by using containers with services like {{site.data.keyword.activedeployshort}} and {{site.data.keyword.deliverypipeline}}. You can then use the {{site.data.keyword.vpn_short}} service to communicate and connect your container in a private network to the classic infrastructure private network. All of the usage charges of the compute resources and services are reflected in your {{site.data.keyword.Bluemix_notm}} invoice.

## Add a service to classic infrastructure assets
{: #add-service-classic-ui}
{: ui}

For example, do you want to add cognitive capabilities from Watson to your apps that are running on classic infrastructure bare metal servers? You can add a service such as {{site.data.keyword.personalityinsightsshort}} to help understand your app's user by completing the following steps:

1. In the {{site.data.keyword.Bluemix_notm}} console, search for the service in the catalog.
2. Create an instance of the service with just a few clicks.
3. Set up the service to run with your existing code by copying the service credentials and adding them to your application.
4. After the update to the app, deploy the new version to your classic infrastructure assets.

## Add a service to classic infrastructure assets by using the API
{: #add-service-classic-api}
{: api}

For example, do you want to add cognitive capabilities from Watson to your apps that are running on classic infrastructure bare metal servers? You can add a service such as {{site.data.keyword.personalityinsightsshort}} to help understand your app's user by completing the following steps:

1. Create an instance of the service by calling [Resource Controller API](/apidocs/resource-controller/resource-controller?code=go#create-resource-instance){: external} as shown in the following example request: 

   ```bash
   curl -X POST https://resource-controller.cloud.ibm.com/v2/resource_instances -H 'Authorization: Bearer <>' -H 'Content-Type: application/json' -d '{
      "name": "my-instance",
      "target": "bluemix-global",
      "resource_group": "5g9f447903254bb58972a2f3f5a4c711",
      "resource_plan_id": "0be5ad401ae913d8ff665d92680664ed",
      "tags": [
        "my-tag"
      ]
    }'
   ```
   {: codeblock}
   {: curl}

   ```java
   CreateResourceInstanceOptions createResourceInstanceOptions = new CreateResourceInstanceOptions.Builder()
    .name(resourceInstanceName)
    .target(targetRegion)
    .resourceGroup(resourceGroup)
    .resourcePlanId(resourcePlanId)
    .build();

   Response<ResourceInstance> response = service.createResourceInstance(createResourceInstanceOptions).execute();
   ResourceInstance resourceInstance = response.getResult();

   System.out.printf("createResourceInstance() response:\n%s\n", resourceInstance.toString());
   ```
   {: codeblock}
   {: java}

   ```javascript
   const params = {
    name: resourceInstanceName,
    target: targetRegion,
    resourceGroup: resourceGroupGuid,
    resourcePlanId: resourcePlanId,
   };

   resourceControllerService.createResourceInstance(params)
    .then(res => {
      instanceGuid = res.result.guid;
      console.log('createResourceInstance() response:\n' + JSON.stringify(res.result, null, 2));
    })
    .catch(err => {
      console.warn(err)
    });
   ```
   {: codeblock}
   {: javascript}

   ```python
   resource_instance = resource_controller_service.create_resource_instance(
      name=resource_instance_name,
      target=target_region,
      resource_group=resource_group,
      resource_plan_id=resource_plan_id
   ).get_result()

   print('\ncreate_resource_instance() response:\n',
        json.dumps(resource_instance, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   createResourceInstanceOptions := resourceControllerService.NewCreateResourceInstanceOptions(
    resourceInstanceName,
    targetRegion,
    resourceGroup,
    resourcePlanID,
   )

   resourceInstance, response, err := resourceControllerService.CreateResourceInstance(createResourceInstanceOptions)
   if err != nil {
    panic(err)
   }

   b, _ := json.MarshalIndent(resourceInstance, "", "  ")
   fmt.Printf("\nCreateResourceInstance() response:\n%s\n", string(b))
   ```
   {: codeblock}
   {: go}

1. Retrieve the credentials (resource key). Call the [Resource Controller API](/apidocs/resource-controller/resource-controller#get-resource-key){: external} as shown in the following example request and pass the ID associated with the instance.

   ```bash
   curl -X GET https://resource-controller.cloud.ibm.com/v2/resource_keys/23693f48-aaa2-4079-b0c7-334846eff8d0 -H 'Authorization: Bearer <IAM_TOKEN>'
   ```
   {: codeblock}
   {: curl}

   ```java
   GetResourceKeyOptions getResourceKeyOptions = new GetResourceKeyOptions.Builder()
    .id(instanceKeyGuid)
    .build();

   Response<ResourceKey> response = service.getResourceKey(getResourceKeyOptions).execute();
   ResourceKey resourceKey = response.getResult();

   System.out.printf("getResourceKey() response:\n%s\n", resourceKey.toString());
   ```
   {: codeblock}
   {: java}

   ```javascript
   const params = {
    id: instanceKeyGuid,
   };

   resourceControllerService.getResourceKey(params)
    .then(res => {
      console.log('getResourceKey() response:\n' + JSON.stringify(res.result, null, 2));
    })
    .catch(err => {
      console.warn(err)
    });
   ```
   {: codeblock}
   {: javascript}

   ```python
   resource_key = resource_controller_service.get_resource_key(
      id=instance_key_guid
   ).get_result()

   print('\nget_resource_key() response:\n',
        json.dumps(resource_key, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   getResourceKeyOptions := resourceControllerService.NewGetResourceKeyOptions(
    instanceKeyGUID,
   )

   resourceKey, response, err := resourceControllerService.GetResourceKey(getResourceKeyOptions)
   if err != nil {
    panic(err)
   }
   b, _ := json.MarshalIndent(resourceKey, "", "  ")
   fmt.Printf("\nGetResourceKey() response:\n%s\n", string(b))
   ```
   {: codeblock}
   {: go}

1. Copy the service credentials and add them to your application. 
1. After the update to the app, deploy the new version to your classic infrastructure assets. 
