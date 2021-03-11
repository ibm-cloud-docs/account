---



copyright:

  years: 2020, 2021
lastupdated: "2021-03-11"

keywords: account resources, delete resource, delete instance

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
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
3. Select the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu for the row, and click **Delete**.

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
```
curl -X DELETE \
https://resource-controller.cloud.ibm.com/v2/resource_instances/8d7af921-b136-4078-9666-081bd8470d94 \
  -H 'Authorization: Bearer <>'
```
{: codeblock}
