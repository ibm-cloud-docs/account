---

copyright:

  years: 2017, 2021

lastupdated: "2021-04-13"

keywords: service ID, create service ID, lock service ID, service ID example

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Creating and working with service IDs
{: #serviceids}

A service ID identifies a service or application similar to how a user ID identifies a user. A service ID that you create can be used to enable an application outside of {{site.data.keyword.Bluemix_notm}} access to your {{site.data.keyword.Bluemix_notm}} services. You can assign specific access policies to the service ID that restrict permissions for using specific services, or even combine permissions for accessing different services. Since service IDs are not tied to a specific user, if a user happens to leave an organization and is deleted from the account, the service ID remains ensuring that your application or service stays up and running.
{:shortdesc}

When you create a service ID, you create a unique name and description that is easy for you to identify and work with in the UI. After you create your service ID, you can [create API keys](/docs/account?topic=account-serviceidapikeys#create_service_key) specific to each service ID that your application can use to authenticate with your {{site.data.keyword.Bluemix_notm}} services. The API key can be set for one-time use or unlimited use. To ensure that your application has the appropriate access for authenticating with your {{site.data.keyword.Bluemix_notm}} services, you use access policies that are assigned to each service ID that you create.

The access policies that are associated with a service ID enable specific actions that can be taken when that service ID is used to access a specific service. A single service ID can have multiple policies assigned that define the level of access that is allowed when accessing multiple Identity and access-enabled services, and even different instances of a single service. For example, you have two services with two service instances each. For example, you might assign the Viewer role for all available instances of one service and assign the Editor role for only one instance of a second service. This way you can customize access to multiple services, but use a single API key for authentication to all.

All users have access to create a service ID in an account to which they are a member. However, to allow a user in an account access to view or manage a service ID that they did not personally create, they are required to have access with a role on the IAM identity service account management service. For more information, see [IAM identity service](/docs/account?topic=account-account-services#identity-service-account-management).


If the Restrict service ID creation IAM account setting is enabled, then everyone in the account, including account owners, is blocked from creating service IDs unless they are assigned explicit access. For more information, see [Restricting users from creating service IDs](/docs/account?topic=account-restrict-service-id-create).
{: important}

## Creating a service ID
{: #create_serviceid}
{: ui}

To create a service ID, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** &gt; **Access (IAM)**, and select **Service IDs**.
2. Click **Create**.
3. Follow the process to create a name and description for your service ID.
4. Click **Create**.

Then, hover on the row of a service ID to use the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu to manage your service ID. You can start by assigning a policy and creating API keys. For more information about working with API keys, see [Managing service ID API keys](/docs/account?topic=account-serviceidapikeys).

## Creating a service ID by using the API
{: #create_serviceid-api}
{: api}

To create a service ID, call the [IAM Identity Services API](https://cloud.ibm.com/apidocs/iam-identity-token-api#create-service-id) as shown in the following example:

```bash
curl -X POST 'https://iam.cloud.ibm.com/v1/serviceids' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json' -d '{
  "name": "My-serviceID",
  "description": "my special service ID",
  "account_id": "ACCOUNT_ID"
}'
```
{: codeblock}
{: curl}

```java
CreateServiceIdOptions createServiceIdOptions = new CreateServiceIdOptions.Builder()
    .accountId(accountId)
    .name(serviceIdName)
    .description("Example ServiceId")
    .build();

Response<ServiceId> response = service.createServiceId(createServiceIdOptions).execute();
ServiceId serviceId = response.getResult();
svcId = serviceId.getId();
System.out.println(serviceId.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  accountId: accountId,
  name: serviceIdName,
  description: 'Example ServiceId',
};

iamIdentityService.createServiceId(params)
  .then(res => {
    svcId = res.result.id;
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err);
  });
```
{: codeblock}
{: javascript}

```python
service_id = iam_identity_service.create_service_id(
  account_id=account_id,
  name=serviceid_name,
  description='Example ServiceId'
).get_result()

svc_id = service_id['id']

print(json.dumps(service_id, indent=2))
```
{: codeblock}
{: python}

```go
createServiceIDOptions := iamIdentityService.NewCreateServiceIDOptions(accountID, serviceIDName)
createServiceIDOptions.SetDescription("Example ServiceId")

serviceID, response, err := iamIdentityService.CreateServiceID(createServiceIDOptions)
if err != nil {
  panic(err)
}
svcID = *serviceID.ID
b, _ := json.MarshalIndent(serviceID, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

For more informatiion, see the [IAM Identity Services API](https://cloud.ibm.com/apidocs/iam-identity-token-api#create-service-id).

## Updating a service ID
{: #update_serviceid}
{: ui}

You can update a service ID by changing the name and description at any time. You can also delete and create new API keys as needed or update the assigned access policies. Hover on the row of a service ID to use the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu to manage your service ID.

Any changes that you make to an existing service ID, such as changing the assigned policies or deleting an API key that is used, might cause service interruptions to applications that use that service ID.

## Updating a service ID by using the API
{: #update_serviceid-api}
{: api}

To update a service ID, call the [IAM Identity Services API](https://cloud.ibm.com/apidocs/iam-identity-token-api#update-service-id) as shown in the following example:

```bash
curl -X PUT 'https://iam.cloud.ibm.com/v1/serviceids/SERVICE_ID_UNIQUE_ID' -H 'Authorization: Bearer TOKEN' -H 'If-Match: <value of etag header from GET request>' -H 'Content-Type: application/json' -d '{
  "name": "My-super-secret-serviceid",
  "description": "super secret service ID"
}'
```
{: codeblock}
{: curl}

```java
UpdateServiceIdOptions updateServiceIdOptions = new UpdateServiceIdOptions.Builder()
    .id(svcId)
    .ifMatch(svcIdEtag)
    .description("This is an updated description")
    .build();

Response<ServiceId> response = service.updateServiceId(updateServiceIdOptions).execute();
ServiceId serviceId = response.getResult();
System.out.println(serviceId.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  id: svcId,
  ifMatch: svcIdEtag,
  description: 'This is an updated description',
};

iamIdentityService.updateServiceId(params)
  .then(res => {
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err);
  });
```
{: codeblock}
{: javascript}

```python
service_id = iam_identity_service.update_service_id(
  id=svc_id,
  if_match=svc_id_etag,
  description='This is an updated description'
).get_result()

print(json.dumps(service_id, indent=2))
```
{: codeblock}
{: python}

```go
updateServiceIDOptions := iamIdentityService.NewUpdateServiceIDOptions(svcID, svcIDEtag)
updateServiceIDOptions.SetDescription("This is an updated description")

serviceID, response, err := iamIdentityService.UpdateServiceID(updateServiceIDOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(serviceID, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

For more information, see the [IAM Identity Services API](https://cloud.ibm.com/apidocs/iam-identity-token-api#update-service-id).

## Locking a service ID
{: #lock_serviceid}

To avoid a situation where your service ID is deleted causing an outage or disruption for the users of your service, you have the option to lock your service ID by using the UI or CLI. Locking a service ID also prevents any policies from being changed, deleted, or assigned. In addition to the ability to lock a service ID, you can [lock individual API keys](/docs/account?topic=account-serviceidapikeys#lockkey) that are associated with each service ID that you create in your account.

While locked service IDs cannot be deleted from the account and the access policies can't be updated, locked service IDs can still be removed from any access group that they are added to. This means that any access that is assigned to the ID by its membership in an access group is removed when the service ID is removed from the access group.
{: note}

### Providing user access for locking service IDs
{: #access_lock_serviceid}

In order for a user to have access to lock and unlock service IDs and API keys that are associated with service IDs, they must be assigned a specific access policy. Two types of access policies can grant the proper access: access to all service IDs in the account or access to a specific service ID in the account

To assign access to all service IDs in the account, set an access policy for account management services with the following details:

* Editor or Administrator role
* IAM Identity Service

To assign access to a specific service ID in the account, set an access policy for account management services with the following details:

* Editor or Administrator role
* IAM Identity Service
* Specify "serviceid" in the Resource type field
* Specify the service ID identifier in the Resource ID field

To get the identifier of a specific service ID, go to **Manage** > **Access (IAM)**, and select **Service IDs**. Select the service ID that you want to view details for, and copy the ID value.
{: ui}


### Locking a service ID from the UI
{: #lock_serviceid_ui}
{: ui}

A locked service ID is indicated by the ![Locked icon](images/locked.svg "Locked") icon.

1. In the console, click **Manage** &gt; **Access (IAM)** and then select **Service IDs**.
2. Identify the row of the service ID that you want to lock, and select **Lock service ID** from the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu.

To unlock a service ID, select the service ID from the table that you want to unlock and select **Unlock service ID** from the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu. You must have the appropriate level of access to unlock a service ID.
{: tip}


### Locking and unlocking a service ID by using the CLI
{: #lock_serviceid_cli}
{: cli}

To lock a service ID, use the following command:

```
ibmcloud iam service-id-lock (NAME|UUID) [-f, --force]
```

Command Options:

<dl>
  <dt>NAME (required)</dt>
  <dd>Name of the service, exclusive with UUID</dd>
  <dt>UUID (required)</dt>
  <dd>UUID of the service, exclusive with NAME</dd>
  <dt>-f, --force</dt>
  <dd>Lock without confirmation</dd>
</dl>

<strong>Examples</strong>:

Lock service ID `sample-test` without confirmation

```
ibmcloud iam service-id-lock sample-test -f
```

Lock service ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976`

```
ibmcloud iam service-id-lock ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

To unlock a service ID, use the following command:

 ```
ibmcloud iam service-id-unlock (NAME|UUID) [-f, --force]
```

Command Options:

<dl>
  <dt>NAME (required)</dt>
  <dd>Name of the service, exclusive with UUID</dd>
  <dt>UUID (required)</dt>
  <dd>UUID of the service, exclusive with NAME</dd>
  <dt>-f, --force</dt>
  <dd>Unlock without confirmation</dd>
</dl>

<strong>Examples</strong>:

Unlock service ID `sample-test` without confirmation

```
ibmcloud iam service-id-unlock sample-test -f
```

Unlock service ID `ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976`

```
ibmcloud iam service-id-unlock ServiceId-cb258cb9-8de3-4ac0-9aec-b2b2d27ac976
```

### Locking a service ID by using the API
{: #lock_serviceid_api}
{: api}

To lock a service ID, call the [IAM Identity Services API](https://cloud.ibm.com/apidocs/iam-identity-token-api#lock-service-id) as shown in the following example:

```bash
curl -X POST 'https://iam.cloud.ibm.com/v1/serviceids/SERVICE_ID_UNIQUE_ID/lock' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json'
```
{: codeblock}
{: curl}

```java
LockServiceIdOptions lockServiceIdOptions = new LockServiceIdOptions.Builder()
    .id(svcId)
    .build();

service.lockServiceId(lockServiceIdOptions).execute();
```
{: codeblock}
{: java}

```javascript
const params = {
  id: svcId,
};

iamIdentityService.lockServiceId(params)
  .then(res => {
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err);
  });
```
{: codeblock}
{: javascript}

```python
response = iam_identity_service.lock_service_id(id=svc_id)

print(response)
```
{: codeblock}
{: python}

```go
lockServiceIDOptions := iamIdentityService.NewLockServiceIDOptions(svcID)

response, err := iamIdentityService.LockServiceID(lockServiceIDOptions)
if err != nil {
  panic(err)
}
```
{: codeblock}
{: go}

For more information, see the [IAM Identity Services API](https://cloud.ibm.com/apidocs/iam-identity-token-api#lock-service-id).

### Unlocking a service ID by using the API
{: #unlock_serviceid_api}
{: api}

To unlock a service ID, call the [IAM Identity Services API](https://cloud.ibm.com/apidocs/iam-identity-token-api#unlock-service-id) as shown in the following example:

```bash
curl -X DELETE 'https://iam.cloud.ibm.com/v1/serviceids/SERVICE_ID_UNIQUE_ID/lock' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json'
```
{: codeblock}
{: curl}

```java
UnlockServiceIdOptions unlockServiceIdOptions = new UnlockServiceIdOptions.Builder()
    .id(svcId)
    .build();

service.unlockServiceId(unlockServiceIdOptions).execute();
```
{: codeblock}
{: java}

```javascript
const params = {
  id: svcId,
};

iamIdentityService.unlockServiceId(params)
  .then(res => {
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err);
    done(err);
  });
```
{: codeblock}
{: javascript}

```python
response = iam_identity_service.unlock_service_id(id=svc_id)

print(response)
```
{: codeblock}
{: python}

```go
unlockServiceIDOptions := iamIdentityService.NewUnlockServiceIDOptions(svcID)

response, err := iamIdentityService.UnlockServiceID(unlockServiceIDOptions)
if err != nil {
  panic(err)
}
```
{: codeblock}
{: go}

For more information, see the [IAM Identity Services API](https://cloud.ibm.com/apidocs/iam-identity-token-api#unlock-service-id).

## Examples of how to use a service ID
{: #examples_serviceid}

The following are examples of how a Service ID is used with the {{site.data.keyword.objectstorageshort}} and Cloud SQL Query services.

- {{site.data.keyword.objectstorageshort}} - [Use the {{site.data.keyword.Bluemix_notm}} CLI](/docs/cloud-object-storage?topic=cloud-object-storage-uhc-hmac-credentials-main).
- Cloud SQL Query - [How to use the SQL Query REST API](https://www.youtube.com/watch?v=jDZKF0CnUvU){: external}.
