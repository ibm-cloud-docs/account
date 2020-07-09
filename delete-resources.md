---



copyright:

  years: 2020
lastupdated: "2020-07-08"

keywords: account resources, delete resource, delete instance

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Deleting resources 
{: #delete-resource}

When you don't need a resource in your account anymore, or if a user in your account created a resource that you don't want them to use, you can delete the instance from your account.
{: shortdesc}

## Deleting resources in the console
{: #delete-resource-console}

You can delete a resource in the console by using the following steps:

1. From your dashboard, click **View resources** in the Resources summary widget.
2. Expand the sections to locate the service instance that you want to delete.
3. Select the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu for the row, and click **Delete**.

## Deleting resources by using the CLI
{: #delete-resource-cli}

To delete a resource by using the CLI, run the following command:

```
ibmcloud resource service-instance-delete (NAME|ID) [-f, --force] [--recursive]
```
{: codeblock}

Enter the following command options:
  * **Name**: The name of the service instance, exclusive with ID. (Required)
  * **ID**: The ID of the service instance, exclusive with NAME. (Required)
  * **-f, --force**: Force deletion without confirmation. 
  * **--recursive**: Delete all belonging resources. 

The following example shows how to delete a resource service-instance that's named `my-service-instance`:

```
ibmcloud resource service-instance-delete my-service-instance
```
