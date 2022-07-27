---

copyright:
  years: 2015, 2021
lastupdated: "2022-03-03"

keywords: service keys, api keys, using services outside IBM cloud, external apps

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Connecting services to external apps
{: #externalapp}

You might have applications that were created and run outside of {{site.data.keyword.Bluemix}}, or you might use third-party tools. If {{site.data.keyword.Bluemix_notm}} services provide service keys that are accessible from the internet, you can use those services with your local apps or third-party tools.
{: shortdesc}

To enable an external app or third-party tool to use an {{site.data.keyword.Bluemix_notm}} service, complete the following steps:

Most services don't require extra parameters, and for services that do, each service defines its own unique list of parameters. For a list of supported configuration parameters, see the documentation for the particular service.
{: tip}

## Connect a service to an external app in the console
{: #externalapp-ui}
{: ui}

1. Create an instance of the service.
    1. Click **Catalog**.
    2. From the catalog, select the service that you want by clicking the service tile. 
    3. Select the location and org and space or resource group, and then click **Create**.
2. From the service details page, select **Service Credentials** to view or add credentials in JSON format. 
    * To create new credentials, select **New credential** and optionally add configuration parameters manually or import a file in JSON format, then click **Add**. Select **View credentials** to save the credentials to connect to your external app.
    * Select a set of credentials and click **View credentials** in the Actions column if they already exist. 
3. Use the API key that is displayed as the credentials to connect to the service instance.

Your application that runs outside of {{site.data.keyword.Bluemix_notm}} can now access the {{site.data.keyword.Bluemix_notm}} service.

If you want to delete service instances or check the billing information, you must go back to the Resource list page in the user interface to manage the service instances.
{: tip}

## Connect a service to an external app by using the API
{: #externalapp-api}
{: api}

1. Create an instance of the service by calling [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller?code=go#create-resource-instance){: external} as shown in the following example request: 

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

2. Retrieve or create credentials (resource key).
   * To create new credentials, call the [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller#create-resource-key) as shown in the following example.

   ```bash
   curl -X POST https://resource-controller.cloud.ibm.com/v2/resource_keys -H 'Authorization: Bearer <IAM_TOKEN>' -H 'Content-Type: application/json' -d '{
    "name": "my-instance-key-1",
    "source": "267bf377-7fa2-43f6-94ec-09103a8e89d4",
    "role": "Writer"
   }'
   ```
   {: codeblock}
   {: curl}

   ```java
   ResourceKeyPostParameters parameters = new ResourceKeyPostParameters.Builder()
    .add("exampleParameter", "exampleValue")
    .build();
   CreateResourceKeyOptions createResourceKeyOptions = new CreateResourceKeyOptions.Builder()
    .name(keyName)
    .source(instanceGuid)
    .parameters(parameters)
    .build();

   Response<ResourceKey> response = service.createResourceKey(createResourceKeyOptions).execute();
   ResourceKey resourceKey = response.getResult();

   System.out.printf("createResourceKey() response:\n%s\n", resourceKey.toString());
   ```
   {: codeblock}
   {: java}

   ```javascript
   const parameters = {
    'exampleParameter': 'exampleValue'
   };

   const params = {
    name: keyName,
    source: instanceGuid,
    parameters: parameters,
   };

   resourceControllerService.createResourceKey(params)
    .then(res => {
      instanceKeyGuid = res.result.guid;
      console.log('createResourceKey() response:\n' + JSON.stringify(res.result, null, 2));
    })
    .catch(err => {
      console.warn(err)
    });
   ```
   {: codeblock}
   {: javascript}

   ```python
   parameters = {
      'exampleParameter': 'exampleValue'
   }
   resource_key = resource_controller_service.create_resource_key(
      name=key_name,
      source=instance_guid,
      parameters=parameters
   ).get_result()

   print('\ncreate_resource_key() response:\n',
        json.dumps(resource_key, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   createResourceKeyOptions := resourceControllerService.NewCreateResourceKeyOptions(
    keyName,
    instanceGUID,
   )

   parameters := &resourcecontrollerv2.ResourceKeyPostParameters{}
   parameters.SetProperty("exampleParameter", "exampleValue")
   createResourceKeyOptions.SetParameters(parameters)

   resourceKey, response, err := resourceControllerService.CreateResourceKey(createResourceKeyOptions)
   if err != nil {
    panic(err)
   }
   b, _ := json.MarshalIndent(resourceKey, "", "  ")
   fmt.Printf("\nCreateResourceKey() response:\n%s\n", string(b))
   ```
   {: codeblock}
   {: go}

   * To retrieve service credentials, call the [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller#get-resource-key) as shown in the following example request and pass the ID associated with the instance.

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

3. Use the API key that is displayed as the credentials to connect to the service instance.

## Services with service keys
{: #service_keys}

The following services provide service keys for you to use externally:

* {{site.data.keyword.alertnotificationshort}} 
* {{site.data.keyword.sparks}} 
* {{site.data.keyword.blockchain}} 
* {{site.data.keyword.discoveryshort}} 
* {{site.data.keyword.messagehub}} 
* {{site.data.keyword.geospatialshort_Geospatial}} 
* {{site.data.keyword.GlobalizationPipeline_short}} 
* {{site.data.keyword.appconserviceshort}} 
* {{site.data.keyword.cloudant}} 
* {{site.data.keyword.languagetranslatorshort}} 
* {{site.data.keyword.dwl_short}} 
* {{site.data.keyword.nlclassifiershort}} 
* {{site.data.keyword.objectstorageshort}} 
* {{site.data.keyword.personalityinsightsshort}}
* {{site.data.keyword.mobilepush}} 
* {{site.data.keyword.speechtotextshort}} 
* {{site.data.keyword.streaminganalyticsshort}} 
* {{site.data.keyword.texttospeechshort}} 
* {{site.data.keyword.toneanalyzershort}} 
* {{site.data.keyword.conversationshort}} 
* {{site.data.keyword.workloadscheduler}} 

