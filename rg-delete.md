---



copyright:

  years: 2020
lastupdated: "2020-07-08"

keywords: delete resource group, resource group, manage resource groups

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Deleting a resource group 
{: #delete_rgs}

You can't delete the default resource group that's added to your account. Besides the default one, you can delete any resource group only if it doesn't contain any resources. 
{: shortdesc}

## Deleting a resource group in the console
{: #delete-rg-console}

To delete a resource group that is empty and not your default resource group, complete the following steps:

1. In the console, go to **Manage** > **Account** > **Account resources** > **Resource groups**.
2. Click the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu, and select **Delete**.

## Deleting a resource group by using the CLI
{: #delete-cli}

Run the [`ibmcloud resource group-delete`](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_group_delete) command to delete  a resource group. For example, delete resource group `example-group`:

```
ibmcloud resource group-delete example-group -f
```
