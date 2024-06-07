---

copyright:
  years: 2021, 2022
lastupdated: "2022-12-06"

subcollection: account

keywords: objects, private catalog, onboarding, vpe objects, view vpe objects, vpe

---

{{site.data.keyword.attribute-definition-list}}


# Managing objects
{: #managing-object}

You can view details about a specific object in your private catalog or you can view a list of all objects in your private catalog.
{: shortdesc}

## Viewing an object's details by using the CLI
{: #viewing-object-details-cli}
{: cli}

To view the details of a specific object, use the following steps.

1. View your object.
   ```bash
   ibmcloud catalog object get [--catalog CATALOG] [--name NAME]
   ```
   {: codeblock}

   For more information about this command, enter
   ```bash
   ibmcloud catalog object help get
   ```
   {: codeblock}

## Viewing all objects in a private catalog by using the CLI
{: #viewing-object-cli}
{: cli}

Use the following steps to view your objects:

1. View your objects.
   ```bash
   ibmcloud catalog object list [--catalog CATALOG]
   ```
   {: codeblock}

   For more information about this command, enter
   ```bash
   ibmcloud catalog object help list
   ```
   {: codeblock}

## Searching for objects
{: #searching-object-cli}
{: cli}

Use the following steps to search for objects.

1. Search for objects.
    ```bash
    ibmcloud catalog object search [--query QUERY]
    ```
    {: codeblock}

If needed, you can add an output value `[--output OUTPUT]` to the command. Currently, JSON is the only supported format.

## Updating objects
{: #updating-object-cli}
{: cli}

Use the following steps to update your object.

1. Update object.
    ```bash
    ibmcloud catalog object update vpe [--catalog CATALOG] [--name NAME]
    ```
    {: codeblock}

The following fields are optional. Only include the fields that you would like to update.

- `[--crn CRN]`
   - Service CRN
- `[--endpoint-type TYPE]`
   - VPE endpoint type
- `[--fqdn FQDN]`
   - List of fully qualified domain names separated by a comma
- `[--region REGION]`
   - Region for the VPE endpoint

## Managing the access list for your object
{: #access-list-object-cli}
{: cli}

You can use the cli to retrieve an object's access list, add accounts to the access list, and remove accounts from the access list.

### Getting an object's access list
{: #access-get-object-cli}
{: cli}

Use the following command to retrieve your object's access list.

```bash
ibmcloud catalog object access-list get [--catalog CATALOG] [--name NAME]
```
{: codeblock}

If needed, you can add an output value `[--output OUTPUT]` to the command. Currently, JSON is the only supported format.

### Adding accounts to an object's access list
{: #access-add-object-cli}
{: cli}

Use the following command to add accounts to an object's access list.

```bash
ibmcloud catalog object access-list add [--account-id ID] [--catalog CATALOG] [--name NAME]
```
{: codeblock}

To add multiple accounts at once, list the account ids separated by a comma in the account ID field. For example, `[--account-id account1, account2]`.

### Removing accounts to an object's access list
{: #access-remove-object-cli}
{: cli}

Use the following command to remove accounts from an object's access list.

```bash
ibmcloud catalog object access-list rm [--account-id ID] [--catalog CATALOG] [--name NAME]
```
{: codeblock}

To remove multiple accounts at once, list the account ids separated by a comma in the account ID field. For example, `[--account-id account1, account2]`.
