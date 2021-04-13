---



copyright:

  years: 2020, 2021
lastupdated: "2021-04-13"

keywords: account resources, reclaim resource, restore resource

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
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Using resource reclamations 
{: #resource-reclamation}

You can use the {{site.data.keyword.cloud}} CLI or the [{{site.data.keyword.cloud}} Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller?code=go#run-reclamation-action) to manage the reclamation process of specific resources. 
{: shortdesc}

## Listing reclaimed resources by using the CLI
{: #list-reclaimed-cli}
{: cli}

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

## Listing reclaimed resources by using the API
{: #list-reclaimed-api}
{: api}

To list reclaimed resources that can be restored or deleted, call the [{{site.data.keyword.cloud}} Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller#list-reclamations) as shown in the following example:

Use the `ListReclamationsOptions.Builder` to create a `ListReclamationsOptions` object that contains the parameter values for the `listReclamations` method.
{: java}

Instantiate the `ListReclamationsOptions` struct and set the fields to provide parameter values for the `ListReclamations` method.
{: go}

```bash
curl -X GET https://resource-controller.cloud.ibm.com/v1/reclamations?account_id=b80a8b513ae24e178438b7a18bd8d609 -H 'Authorization: Bearer <IAM_TOKEN>'
```
{: codeblock}
{: curl}

```java
ListReclamationsOptions listReclamationsOptions = new ListReclamationsOptions.Builder()
  .accountId(accountId)
  .build();

Response<ReclamationsList> response = service.listReclamations(listReclamationsOptions).execute();
ReclamationsList reclamationsList = response.getResult();

System.out.printf("listReclamations() response:\n%s\n", reclamationsList.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  accountId: accountId,
};

resourceControllerService.listReclamations(params)
  .then(res => {
    var resources = res.result.resources;
    resources.forEach(reclaim => {
      if (reclaim.resource_instance_id.toString() === instanceGuid) {
        reclamationId = reclaim.id;
      }
    });
    console.log('listReclamations() response:\n' + JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
reclamations_list = resource_controller_service.list_reclamations(
    account_id=account_id
).get_result()

print('\nlist_reclamations() response:\n',
      json.dumps(reclamations_list, indent=2))
```
{: codeblock}
{: python}

```go
listReclamationsOptions := resourceControllerService.NewListReclamationsOptions()
listReclamationsOptions = listReclamationsOptions.SetAccountID(accountID)
reclamationsList, response, err := resourceControllerService.ListReclamations(listReclamationsOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(reclamationsList, "", "  ")
fmt.Printf("\nListReclamations() response:\n%s\n", string(b))
```
{: codeblock}
{: go}


## Deleting a reclaimed resource by using the CLI
{: #delete-reclaimed-cli}
{: cli}

To delete a reclaimed resource by using the CLI, run the following command: 

```
ibmcloud resource reclamation-delete ID [--comment COMMENT] [--f, --force]
```
{: codeblock}

Enter the following command options:
  * **ID**: The ID of the resource reclamation. This is the reclamation ID and not the resource instance ID. (Required).
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

## Deleting resource by using the API
{: #delete-reclaimed-api}
{: api}

To reclaim (provisionally delete) a resource, call the [{{site.data.keyword.cloud}} Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller?code=go#run-reclamation-action) as shown in the following example. Specify `reclaim` to delete a resource. `id` is the reclamation ID and not the resource instance ID. 

```bash
curl -X POST https://resource-controller.cloud.ibm.com/v1/reclamations/0114be9024c6eede47d08a85ac0c5c43/actions/reclaim -H 'Authorization: Bearer <IAM_TOKEN>' -H 'Content-Type: application/json' -d '{
    "request_by": "bar",
    "comment": "reclaim resource instance 614fc866-1d4f-4c9e-973e-637f1089a6a1"
  }'
```
{: codeblock}
{: curl}

```java
RunReclamationActionOptions runReclamationActionOptions = new RunReclamationActionOptions.Builder()
  .id(reclamationId)
  .actionName("reclaim")
  .build();

Response<Reclamation> response = service.runReclamationAction(runReclamationActionOptions).execute();
Reclamation reclamation = response.getResult();

System.out.printf("runReclamationAction() response:\n%s\n", reclamation.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  id: reclamationId,
  actionName: 'reclaim',
};

resourceControllerService.runReclamationAction(params)
  .then(res => {
    console.log('runReclamationAction() response:\n' + JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
reclamation = resource_controller_service.run_reclamation_action(
    id=reclamation_id,
    action_name='reclaim'
).get_result()

print('\nrun_reclamation_action() response:\n',
      json.dumps(reclamation, indent=2))
```
{: codeblock}
{: python}

```go
runReclamationActionOptions := resourceControllerService.NewRunReclamationActionOptions(
  reclamationID,
  "reclaim",
)

reclamation, response, err := resourceControllerService.RunReclamationAction(runReclamationActionOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(reclamation, "", "  ")
fmt.Printf("\nRunReclamationAction() response:\n%s\n", string(b))
```
{: codeblock}
{: go}

## Restoring a resource by using the CLI
{: #restore-resource-cli}
{: cli}

You can restore a resource within 7 days after you delete it. 

Not all resources can be restored. You can run the **`ibmcloud resource reclamations`** command to check the resources that you can restore.
{: important}

To restore a resource by using the CLI, run the following command:

```
ibmcloud resource reclamation-restore ID [--comment COMMENT]
```
{: codeblock}

Enter the following command options:
  * **ID**: The ID of the resource reclamation. This is the reclamation ID and not the resource instance ID.  (Required) 
  * **--comment**: Comments about the action.  

The following example shows how to restore a resource with the `d9fendfwlw` ID:

```
ibmcloud resource reclamation-restore "d9fendfwlw"
```

For more information, see the [`ibmcloud resource reclamations` command reference](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_reclamations).

## Restoring a resource by using the API
{: #restore-resource-api}
{: api}

You can restore a resource within 7 days after you delete it.

Not all resources can be restored. [Get a list of all reclaimations](https://cloud.ibm.com/apidocs/resource-controller/resource-controller?code=go#list-reclamations) to check the resources that you can restore.
{: important}

To restore a resource by using the API, call the [{{site.data.keyword.cloud}} Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller?code=go#run-reclamation-action) as shown in the following example. Specify `restore` to restore a resource. `id` is the reclamation ID and not the resource instance ID. 

```bash
curl -X POST https://resource-controller.cloud.ibm.com/v1/reclamations/0114be9024c6eede47d08a85ac0c5c43/actions/restore -H 'Authorization: Bearer <IAM_TOKEN>' -H 'Content-Type: application/json' -d '{
    "request_by": "bar",
    "comment": "restore resource instance 614fc866-1d4f-4c9e-973e-637f1089a6a1"
  }'
```
{: codeblock}
{: curl}

```java
RunReclamationActionOptions runReclamationActionOptions = new RunReclamationActionOptions.Builder()
  .id(reclamationId)
  .actionName("restore")
  .build();

Response<Reclamation> response = service.runReclamationAction(runReclamationActionOptions).execute();
Reclamation reclamation = response.getResult();

System.out.printf("runReclamationAction() response:\n%s\n", reclamation.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  id: reclamationId,
  actionName: 'restore',
};

resourceControllerService.runReclamationAction(params)
  .then(res => {
    console.log('runReclamationAction() response:\n' + JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
reclamation = resource_controller_service.run_reclamation_action(
    id=reclamation_id,
    action_name='restore'
).get_result()

print('\nrun_reclamation_action() response:\n',
      json.dumps(reclamation, indent=2))
```
{: codeblock}
{: python}

```go
runReclamationActionOptions := resourceControllerService.NewRunReclamationActionOptions(
  reclamationID,
  "restore",
)

reclamation, response, err := resourceControllerService.RunReclamationAction(runReclamationActionOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(reclamation, "", "  ")
fmt.Printf("\nRunReclamationAction() response:\n%s\n", string(b))
```
{: codeblock}
{: go}
