---



copyright:

  years: 2020, 2021
lastupdated: "2021-03-11"

keywords: delete resource group, resource group, manage resource groups

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

# Deleting a resource group 
{: #delete_rgs}

You can't delete the default resource group that's added to your account. Besides the default one, you can only delete a resource group if it doesn't contain any resources. 
{: shortdesc}

## Deleting a resource group in the console
{: #delete-rg-console}
{: ui}

To delete a resource group that doesn't contain resources and is not your default, complete the following steps:

1. In the console, go to **Manage** > **Account** > **Account resources** > **Resource groups**.
2. Click the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu, and select **Delete**.

## Deleting a resource group by using the CLI
{: #delete-cli}
{: cli}

To delete a resource group that doesn't contain resources and is not your default, run the [`ibmcloud resource group-delete`](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_group_delete). For example, delete resource group `example-group`:

```
ibmcloud resource group-delete example-group -f
```

## Deleting a resource group by using the API
{: #delete-api}
{: api}

You can programmatically delete a resource group by calling the Resource Manager API as shown in the following sample request. For detailed information about the API, see [Resource Manager API](/apidocs/resource-controller/resource-manager#delete-resource-group){: external}.

```
curl -X DELETE \
  https://resource-controller.cloud.ibm.com/v2/resource_groups/09f8c1c0742c493f80baaf7835212345 \
  -H 'Authorization: Bearer <IAM_TOKEN>'
  -H 'Content-Type: application/json'
```
{: codeblock}


