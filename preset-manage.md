---

copyright:
  years: 2022
lastupdated: "2022-12-06"

subcollection: account

keywords: objects, private catalog, onboarding, preset configurations, view preset configurations, preset

---

{{site.data.keyword.attribute-definition-list}}


# Managing preset configurations
{: #managing-preset}

You can view details about a specific preset configuration in your private catalog or you can view a list of all preset configurations in your private catalog.
{: shortdesc}

## Viewing a preset configuration's details by using the CLI
{: #viewing-preset-details-cli}
{: cli}

To view the details of a specific preset configuration, use the following steps.

1. View your preset configuration.
   ```bash
   ibmcloud catalog object get [--catalog CATALOG] [--name NAME]
   ```
   {: codeblock}

   For more information about this command, enter
   ```bash
   ibmcloud catalog object help get
   ```
   {: codeblock}

## Viewing all preset configurations in a private catalog by using the CLI
{: #viewing-preset-cli}
{: cli}

Use the following steps to view your preset configurations:

1. View your preset configurations.
   ```bash
   ibmcloud catalog object list [--catalog CATALOG]
   ```
   {: codeblock}

   For more information about this command, enter
   ```bash
   ibmcloud catalog object help list
   ```
   {: codeblock}

## Searching for preset configurations
{: #searching-preset-cli}
{: cli}

Use the following steps to search for preset configurations.

1. Search for preset configurations.
    ```bash
    ibmcloud catalog object search [--query QUERY]
    ```
    {: codeblock}

If needed, you can add an output value `[--output OUTPUT]` to the command. Currently, JSON is the only supported format.

## Updating preset configurations
{: #updating-preset-cli}
{: cli}

Use the following steps to update your preset configuration.

1. Update preset configuration.
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

## Managing the access list for your preset configuration
{: #access-list-preset-cli}
{: cli}

You can use the cli to retrieve an preset configuration's access list, add accounts to the access list, and remove accounts from the access list.

### Getting a preset configuration's access list
{: #access-get-preset-cli}
{: cli}

Use the following command to retrieve your preset configuration's access list.

```bash
ibmcloud catalog object access-list get [--catalog CATALOG] [--name NAME]
```
{: codeblock}

If needed, you can add an output value `[--output OUTPUT]` to the command. Currently, JSON is the only supported format.

### Adding accounts to a preset configuration's access list
{: #access-add-preset-cli}
{: cli}

Use the following command to add accounts to a preset configuration's access list.

```bash
ibmcloud catalog object access-list add [--account-id ID] [--catalog CATALOG] [--name NAME]
```
{: codeblock}

To add multiple accounts at once, list the account ids separated by a comma in the account ID field. For example, `[--account-id account1, account2]`.

### Removing accounts to a preset configuration's access list
{: #access-remove-preset-cli}
{: cli}

Use the following command to remove accounts from a preset configuration's access list.

```bash
ibmcloud catalog object access-list rm [--account-id ID] [--catalog CATALOG] [--name NAME]
```
{: codeblock}

To remove multiple accounts at once, list the account ids separated by a comma in the account ID field. For example, `[--account-id account1, account2]`.
