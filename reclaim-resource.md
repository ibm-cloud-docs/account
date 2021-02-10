---



copyright:

  years: 2020, 2021
lastupdated: "2021-02-10"

keywords: account resources, reclaim resource, restore resource

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Using resource reclamations 
{: #resource-reclamation}

You can use the {{site.data.keyword.cloud}} CLI to manage the reclamation process of specific resources. 
{: shortdesc}

## Listing reclaimed resources 
{: #list-reclaimed}

To list reclaimed resources that can be restored or deleted by using the CLI, run the following command: 

```
ibmcloud resource reclamations [--resource-instance-id INSTANCE_ID]
```
{: codeblock}

Enter the following command option:
  * **--resource-instance-id**: The globally unique ID (GUID) of the resource instance.

The following example shows how to list the reclamations of a particular service instance:

```
ibmcloud resource reclamations --resource-instance-id abcd1234-ef56-486e-b293-22d6c7eb6699
```

## Deleting a reclaimed resource 
{: #delete-reclaimed}

To delete a reclaimed resource by using the CLI, run the following command: 

```
ibmcloud resource reclamation-delete ID [--comment COMMENT] [--f, --force]
```
{: codeblock}

Enter the following command options:
  * **ID**: The ID of the resource reclamation (required).
  * **--comment**: Comments about the action.
  * **-f, --force**: Force deletion without confirmation.

The following example shows how to delete a resource reclamation with ID `d9fendfwlw`:

```
ibmcloud resource reclamation-delete "d9fendfwlw"
```

The following example shows how to delete a resource reclamation with ID `d9fendfwlw` and leave a comment of "no longer needed" without confirmation:

```
ibmcloud resource reclamation-delete --id "d9fendfwlw" --comment "no longer needed" -f
```

## Restoring a resource
{: #restore-resource}

You can restore a resource within 7 days after you delete it. 

Not all resources can be restored. You can run the **`ibmcloud resource reclamations`** command to check the resources that you can restore.
{: important}

To restore a resource by using the CLI, run the following command:

```
ibmcloud resource reclamation-restore ID [--comment COMMENT]
```
{: codeblock}

Enter the following command options:
  * **ID**: The ID of the resource reclamation. (Required)
  * **--comment**: Comments about the action.  

The following example shows how to restore a resource with the `d9fendfwlw` ID:

```
ibmcloud resource reclamation-restore "d9fendfwlw"
```

For more information, see the [`ibmcloud resource reclamations` command reference](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_reclamations).
