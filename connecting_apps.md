---

copyright:
  years: 2017, 2021
lastupdated: "2021-09-22"

keywords: create connection, connect a service, bind, alias

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Managing connections
{: #connect_app}

You can connect a service to an existing or new {{site.data.keyword.Bluemix}} application from the Connections tab on your service dashboard. You can add more connections or delete connections from the Connections tab.
{: shortdesc}

However, when you connect a service instance that is managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) to an application, an alias of the service that is managed by IAM is automatically created in the corresponding space with the connection information that you specified. This alias is represented as a service instance of your IAM-managed service.

## What is an alias?
{: #what_is_alias}

An alias is a connection between your IAM-managed service within a resource group and an application within an org or a space. In the {{site.data.keyword.Bluemix_notm}} console, the connection (alias) is represented as a service instance. You can manage your alias by modifying the service instance that represents your connection.

Aliases are like symlinks that hold references to remote resources and enable interoperability and reuse of an instance across the platform. For example, you can create an instance of a service in a resource group and then reuse it from any available region by creating an alias in an org or space in those regions.

The following rules apply to aliases:

* There's no extra charge for an alias, but each alias counts against your quota in your organization.
* You can create only one alias per space in the {{site.data.keyword.Bluemix_notm}} console. However, more than one alias per space can be created by using the {{site.data.keyword.Bluemix_notm}} CLI. For more information, see [Working with resources and resource groups](/docs/cli?topic=cli-ibmcloud_commands_resource).
* You can create multiple connections between your IAM-managed service and any application in any space, organization, and region in the same account if you have permission.
* Multiple connections that are made in the same space to different apps from an IAM-managed service instance use the same alias.
* Unbinding an IAM-managed service instance *doesn't* delete the service instance that represents the alias.
* Deleting the application that your IAM-managed service instance is connected to *doesn't* delete the instance that represents the alias.
* Deleting an IAM-managed service instance *deletes* the service instance that represents the alias.

## Creating a connection (alias) between an IAM-managed service and an app
{: #creating_alias}
{: ui}

To connect your IAM-managed service instance to an application:

1. Go to your dashboard.

2. Click the name of your app to open the app details view.

3. Click **Connect existing** and choose from your existing app. Or click **Create connection** to create an app to connect to.

4. Specify the **Access Role for connection**. This value sets the IAM service access role. For more information, see [IAM access](/docs/account?topic=account-userroles).

5. Optionally, you can provide a **Service ID for connection** by either allowing IAM to generate a unique value for you, or by providing an existing service ID. For more information, see [Creating and working with service IDs](/docs/account?topic=account-serviceids).

6. Click **Create**.

## Creating a connection (alias) between an IAM-managed service and an app by using the API
{: #creating_alias-api}
{: api}

To create a new alias and connect your IAM-managed service instance to an application, call the [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller#create-resource-alias){: external} as shown in the following example: 

```bash
curl -X POST https://resource-controller.cloud.ibm.com/v2/resource_aliases -H 'Authorization: Bearer <IAM_TOKEN>' -H 'Content-Type: application/json' -d '{
    "name": "my-instance-alias-1",
    "source": "8d7af921-b136-4078-9666-081bd8470d94",
    "target": "crn:v1:cf:public:cf:eu-gb:o/e242c7f0-9eb7-4541-ad3e-b5f5a45a1498::cf-space:f5038ca8-9d28-42a1-9e57-9b9fdd66bf8e"
  }'
```
{: codeblock}
{: curl}

```java
CreateResourceAliasOptions createResourceAliasOptions = new CreateResourceAliasOptions.Builder()
  .name(aliasName)
  .source(instanceGuid)
  .target(aliasTargetCRN)
  .build();

Response<ResourceAlias> response = service.createResourceAlias(createResourceAliasOptions).execute();
ResourceAlias resourceAlias = response.getResult();

System.out.printf("createResourceAlias() response:\n%s\n", resourceAlias.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  name: aliasName,
  source: instanceGuid,
  target: aliasTargetCRN,
};

resourceControllerService.createResourceAlias(params)
  .then(res => {
    aliasGuid = res.result.guid;
    console.log('createResourceAlias() response:\n' + JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
resource_alias = resource_controller_service.create_resource_alias(
    name=alias_name,
    source=instance_guid,
    target=alias_target_crn
).get_result()

print('\ncreate_resource_alias() response:\n',
      json.dumps(resource_alias, indent=2))
```
{: codeblock}
{: python}

```go
createResourceAliasOptions := resourceControllerService.NewCreateResourceAliasOptions(
  aliasName,
  instanceGUID,
  aliasTargetCRN,
)

resourceAlias, response, err := resourceControllerService.CreateResourceAlias(createResourceAliasOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(resourceAlias, "", "  ")
fmt.Printf("\nCreateResourceAlias() response:\n%s\n", string(b))
```
{: codeblock}
{: go}


## Viewing an alias
{: #view_alias}
{: ui}

After you create a connection between an IAM-managed service and an app, the alias is displayed on the Connections tab of the connected app. Additionally, the alias is displayed as a running service instance on your resource list, and contains a Connections tab only when you open it.

1. Go to the your resource list.
2. From the **Application Services** table, click the name of the service instance to open the service details view. If it has a Connections tab only, it's an alias.

## Viewing an alias by using the API
{: #view_alias-api}
{: api}

After you create a connection between an IAM-managed service and an app, you can view the alias by getting a list of all resource aliases for an instance or you can retrieve a resource alias by ID. 

### Get a list of all resource aliases for an instance
{: #list-rsc-alias-instance-api}

To get a list of all resource aliases for the instance, call the [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller?code=node#list-resource-aliases-for-instance){: external} as shown in the following example: 

```bash
curl -X GET https://resource-controller.cloud.ibm.com/v2/resource_instances/8d7af921-b136-4078-9666-081bd8470d94/resource_aliases -H 'Authorization: Bearer <IAM_TOKEN>'
```
{: codeblock}
{: curl}

```java
ListResourceAliasesForInstanceOptions listResourceAliasesForInstanceOptions = new ListResourceAliasesForInstanceOptions.Builder()
  .id(instanceGuid)
  .build();

Response<ResourceAliasesList> response = service.listResourceAliasesForInstance(listResourceAliasesForInstanceOptions).execute();
ResourceAliasesList resourceAliasesList = response.getResult();

System.out.printf("listResourceAliasesForInstance() response:\n%s\n", resourceAliasesList.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  id: instanceGuid,
};

resourceControllerService.listResourceAliasesForInstance(params)
  .then(res => {
    console.log('listResourceAliasesForInstance() response:\n' + JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
resource_aliases_list = resource_controller_service.list_resource_aliases_for_instance(
    id=instance_guid
).get_result()

print('\nlist_resource_aliases_for_instance() response:\n',
      json.dumps(resource_aliases_list, indent=2))
```
{: codeblock}
{: python}

```go
listResourceAliasesForInstanceOptions := resourceControllerService.NewListResourceAliasesForInstanceOptions(
  instanceGUID,
)

resourceAliasesList, response, err := resourceControllerService.ListResourceAliasesForInstance(listResourceAliasesForInstanceOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(resourceAliasesList, "", "  ")
fmt.Printf("\nListResourceAliasesForInstance() response:\n%s\n", string(b))
```
{: codeblock}
{: go}

### Retrieve a resource alias by ID
{: #get-rsc-alias-api}

To retrieve a resource alias by ID, call the [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller?code=go#get-resource-alias){: external} as shown in the following example:

```bash
curl -X GET https://resource-controller.cloud.ibm.com/v2/resource_aliases/267bf377-7fa2-43f6-94ec-09103a8e89d4 -H 'Authorization: Bearer <IAM_TOKEN>' \
```
{: codeblock}
{: curl}

```java
GetResourceAliasOptions getResourceAliasOptions = new GetResourceAliasOptions.Builder()
  .id(aliasGuid)
  .build();

Response<ResourceAlias> response = service.getResourceAlias(getResourceAliasOptions).execute();
ResourceAlias resourceAlias = response.getResult();

System.out.printf("getResourceAlias() response:\n%s\n", resourceAlias.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  id: aliasGuid,
};

resourceControllerService.getResourceAlias(params)
  .then(res => {
    console.log('getResourceAlias() response:\n' + JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
resource_alias = resource_controller_service.get_resource_alias(
    id=alias_guid
).get_result()

print('\nget_resource_alias() response:\n',
      json.dumps(resource_alias, indent=2))
```
{: codeblock}
{: python}

```go
getResourceAliasOptions := resourceControllerService.NewGetResourceAliasOptions(
  aliasGUID,
)

resourceAlias, response, err := resourceControllerService.GetResourceAlias(getResourceAliasOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(resourceAlias, "", "  ")
fmt.Printf("\nGetResourceAlias() response:\n%s\n", string(b))
```
{: codeblock}
{: go}

## Deleting an alias
{: #delete_alias}
{: ui}

The easiest way to delete the alias is to delete the IAM-managed service instance. However, you can maintain your IAM-managed service instance and instead delete the alias directly.

1. Go to the your resource list.
2. From the **Application Services** table, click the name of the service instance to open the service details view. If it has a Connections tab only, it's an alias.
3. Delete the instance.

## Deleting an alias by using the API
{: #delete_alias-api}
{: api}

To delete an alias directly, call the [Resource Contoller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller?code=go#delete-resource-alias){: external} as shown in the following example: 

```bash
curl -X DELETE https://resource-controller.cloud.ibm.com/v2/resource_aliases/267bf377-7fa2-43f6-94ec-09103a8e89d4 -H 'Authorization: Bearer <IAM_TOKEN>' \
```
{: codeblock}
{: curl}

```java
DeleteResourceAliasOptions deleteResourceAliasOptions = new DeleteResourceAliasOptions.Builder()
  .id(aliasGuid)
  .build();

Response<Void> response = service.deleteResourceAlias(deleteResourceAliasOptions).execute();

System.out.printf("deleteResourceAlias() response status code: %d\n", response.getStatusCode());
```
{: codeblock}
{: java}

```javascript
const params = {
  id: aliasGuid,
};

resourceControllerService.deleteResourceAlias(params)
  .then(res => {
    console.log('deleteResourceAlias() response status code: ' + res.status);
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
response = resource_controller_service.delete_resource_alias(
    id=alias_guid
)
print('\ndelete_resource_alias() response status code: ',
      response.get_status_code())
```
{: codeblock}
{: python}

```go
deleteResourceAliasOptions := resourceControllerService.NewDeleteResourceAliasOptions(
  aliasGUID,
)

response, err := resourceControllerService.DeleteResourceAlias(deleteResourceAliasOptions)
if err != nil {
  panic(err)
}
fmt.Printf("\nDeleteResourceAlias() response status code: %d\n", response.StatusCode)
```
{: codeblock}
{: go}

## Creating a connection between multiple services
{: #multiple_services}

For more information, see [Connecting services to a Cloud Foundry app](/docs/account?topic=account-s2s_binding).
