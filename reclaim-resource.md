---



copyright:

  years: 2020
lastupdated: "2020-07-08"

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
ibmcloud resource reclamations [--instance-id INSTANCE_ID | --instance-name INSTANCE_NAME] [--output FORMAT]
```
{: codeblock}

Enter the following command options:
  * **--instance-id**: The ID of the resource instance. 
  * **--instance-name**: The name of the resource instance.
  * **--output**: Specify output format. Only JSON is supported.

The following example shows how to list the resource reclamation for the service instance that's named `test-cloudant`:

```
ibmcloud resource reclamations --instance-name "test-cloudant"
```

## Deleting a reclaimed resource 
{: #delete-reclaimed}

To delete a reclaimed resource by using the CLI, run the following command: 

```
ibmcloud resource reclamation-delete --id RECLAMATION_ID [--comment COMMENT] [--f, --force] [--output FORMAT]
```
{: codeblock}

Enter the following command options:
  * **--instance-id**: The ID of the resource reclamation (required). 
  * **--comment**: Comments about the action.
  * **-f, --force**: Force deletion without confirmation.
  * **--output**: Specify output format. Only JSON is supported.

The following example shows how to delete a resource reclamation with ID `d9fendfwlw`:

```
ibmcloud resource reclamation-delete --id "d9fendfwlw"
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
ibmcloud resource reclamation-restore --id RECLAMATION_ID [--comment COMMENT] [--output FORMAT]
```
{: codeblock}

Enter the following command options:
  * **ID**: The ID of the resource reclamation. (Required)
  * **--comment**: Comments about the action.  
  * **--output**: Specify the output format. Only `JSON` is supported. 

The following example shows how to restore a resource with the `d9fendfwlw` ID:

```
ibmcloud resource reclamation-restore --id "d9fendfwlw"
```
