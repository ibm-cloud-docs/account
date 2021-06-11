---



copyright:

  years: 2020, 2021
lastupdated: "2021-06-11"

keywords: account resources, delete resource, delete instance

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:ruby: .ph data-hd-programlang='ruby'}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}

# Deleting resources 
{: #delete-resource}

When you don't need a resource in your account anymore, or if a user in your account created a resource that you don't want them to use, you can delete the instance from your account.
{: shortdesc}

## Deleting resources in the console
{: #delete-resource-console}
{: ui}

You can delete a resource in the console by using the following steps:

1. From your dashboard, click **View resources** in the Resources summary widget.
2. Expand the sections to locate the service instance that you want to delete.
3. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) > **Delete** for the row.

## Deleting resources by using the CLI
{: #delete-resource-cli}
{: cli}

You can delete a resource by using the {{site.data.keyword.Bluemix}} Command Line Interface. For detailed information about managing IBM Cloud resources, see [Working with resources and resource groups](/docs/cli?topic=cli-ibmcloud_commands_resource).

1. Log in, and select the account.

  ```
  ibmcloud login
  ```
  {:codeblock}
2. Delete a service instance by running the [`ibmcloud resource service-instance-delete`](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_service_instance_delete) command, where `NAME` is the name of the service instance, exclusive with ID, and `ID` is the ID of the service instance, exclusive with NAME.

  ```
  ibmcloud resource service-instance-delete (NAME|ID) [-f, --force] [--recursive]
  ```
  {:codeblock}

  For example, the following command deletes a resource service-instance named `my-service-instance`:

  ```
  ibmcloud resource service-instance-delete my-service-instance
  ```
  {:codeblock}

## Deleting resource instances by using the API
{: #delete-resource-instance-api}
{: api}

You can programmatically delete a resource instance by calling the Resource Controller API as shown in the following sample request. For detailed information about the API, see [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller#delete-resource-instance){: external}.

```bash
curl -X DELETE \
https://resource-controller.cloud.ibm.com/v2/resource_instances/8d7af921-b136-4078-9666-081bd8470d94 \
  -H 'Authorization: Bearer <>'
```
{: pre}
{: curl}

```java
DeleteResourceInstanceOptions deleteResourceInstanceOptions = new DeleteResourceInstanceOptions.Builder()
  .id(instanceGuid)
  .recursive(false)
  .build();

Response<Void> response = service.deleteResourceInstance(deleteResourceInstanceOptions).execute();

System.out.printf("deleteResourceInstance() response status code: %d\n", response.getStatusCode());
```
{: codeblock}
{: java}

```javascript
const params = {
  id: instanceGuid,
  recursive: false,
};

resourceControllerService.deleteResourceInstance(params)
  .then(res => {
    console.log('deleteResourceInstance() response status code: ' + res.status);
  })
  .catch(err => {
    console.warn(err)
  });
  ```
{: codeblock}
{: javascript}

```python
response = resource_controller_service.delete_resource_instance(
    id=instance_guid,
    recursive=False
)

print('\ndelete_resource_instance() response status code: ',
      response.get_status_code())
```
{: codeblock}
{: python}

```go
deleteResourceInstanceOptions := resourceControllerService.NewDeleteResourceInstanceOptions(
  instanceGUID,
)
deleteResourceInstanceOptions.SetRecursive(false)

response, err := resourceControllerService.DeleteResourceInstance(deleteResourceInstanceOptions)
if err != nil {
  panic(err)
}
fmt.Printf("\nDeleteResourceInstance() response status code: %d\n", response.StatusCode)
```
{: codeblock}
{: go}

