---

copyright:

  years: 2015, 2025
lastupdated: "2025-07-02"

keywords: service key, api key, credential, connect resources to apps, multi-cloud

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Connecting services to apps
{: #service_credentials}

Connect your apps or third-party tools to {{site.data.keyword.cloud_notm}} services by generating a new set of service credentials. These credentials act as the bridge between your app, whether it’s hosted on {{site.data.keyword.Bluemix}} or an external platform like AWS, and the {{site.data.keyword.Bluemix}} service that you want to use. For example, if you’re integrating an AWS-hosted app with {{site.data.keyword.conversationshort}}, you generate a service credential that provides the necessary access. Then, you can add it to your app’s configuration to establish the connection.

To add credentials to your apps, refer to the documentation for the type of app or compute option that you are using.
{: tip}

## Creating a service credential
{: #IAM_credential-ui}
{: ui}

Credentials that you create after 04 August 2025 are one-time view by default, so make sure that you save them securely. The one-time view property on existing credentials is not affected. For more information, see [One-time credentials](/docs/account?topic=account-service_credentials&interface=ui#onetime-credentials).
{: important}

Services that are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) can generate a resource key, also known as a credential. Credentials are service-specific and vary based on how each service defines the credentials they need to generate. A credential might contain a username, password, hostname, port, and a URL, however the contents of each credential is unique to the service that generates it.

Some services might generate more data that requires parameters to be passed in. For example, a service might require you to input a language parameter to set the default language that is returned in the resource key that is generated.

To add credentials to your service:

Complete the following steps to add a credential to a service:

1. From the **Resource list**, select the name of the service to open the service details page.
1. Click **Service credentials**.
1. Check the **One-time view** setting, which determines whether you can retrieve the resource key values later.
   1. Set to **On** or **Off** depending on your use case. Users with the Administrator role on the resource instance can manage this setting by using the [Resource Controller API](/apidocs/resource-controller/resource-controller#update-resource-instance).

      Set to On to help ensure compliance with security best practices and regulations, such as [PCI DSS](https://www.ibm.com/cloud/compliance/pci){: external}, by preventing shared access to credentials.
      {: tip}

1. Click **Create credential**.
1. Enter a **Name**.
1. Assign an IAM service access role. For more information about roles, see [IBM Cloud IAM roles](/docs/account?topic=account-userroles).
   1. Specify `None` to assign no role to the new credential if you want to manage access by associating a new or existing service ID with the service credential.
1. (Optional) Select an existing service ID or **Create New Service ID** to associate with the credential. This way, you can manage access directly within IAM by going to **Manage > Access (IAM) > Service IDs**. For more information, see [Creating and working with service IDs](/docs/account?topic=account-serviceids).

      For services that have finer grain resource access, you might want to use a service ID to grant access only to a subresource, such as a {{site.data.keyword.cos_short}} bucket.
      {: tip}

1. Click **Advanced options** to provide more parameters as a valid JSON object that contains service-specific configuration parameters, provided either inline or in a file.

      Most services don't require extra parameters, and for services that do, each service defines its own unique list of parameters. For a list of supported configuration parameters, see the documentation for the particular service.
      {: note}

1. Click **Create** to generate the new service credential.

   The service credentials is read only. The user can either copy or download the credentials.
   {: note}

1. If the credential is set to one-time view, it cannot be viewed again.
1. Expand the details of your new service credential. Copy the credential properties that your app or external consumer needs. For example, the API key or password and URL.

## Creating a service credential by using the API
{: #IAM_credential-api}
{: api}

Credentials that you create after 04 August 2025 are one-time view by default, so make sure that you save them securely. The one-time view property on existing credentials is not affected. For more information, see [One-time credentials](/docs/account?topic=account-service_credentials&interface=ui#onetime-credentials).
{: important}

{{site.data.keyword.cloud_notm}} services can generate a resource key, also known as a credential. Credentials are service-specific and vary based on how each service defines the credentials they need to generate. A credential might contain a username, password, hostname, port, and a URL, however the contents of each credential is unique to the service that generates it.

Some services might generate more data that requires parameters to be passed in. For example, a service might require you to input a language parameter to set the default language that is returned in the resource key that is generated.

You can assign an IAM service access role to new credentials that you generate for an {{site.data.keyword.cloud_notm}} service. This role grants access to the entire service instance, not a specific resource. For services that have finer grain resource access, you might want to grant access only to a subresource, such as a {{site.data.keyword.cos_short}} bucket. In this case, assign no role to the new credential. This way, you can manage fine grain access by associating the credential with a service ID and create an IAM policy that you scope to a specific resource, like a bucket. To do so, go to **Manage > Access (IAM) > Service IDs**. Select the service ID with the same name as the service credential key, and click **Assign access**.
{: tip}

To create a resource key, call the [Resource Controller API](/apidocs/resource-controller/resource-controller#create-resource-key) as shown in the following example:

```bash
curl -X POST https://resource-controller.cloud.ibm.com/v2/resource_keys -H 'Authorization: Bearer <IAM_TOKEN>' -H 'Content-Type: application/json' -d '{
  "name": "my-instance-key-1",
  "source": "267bf377-7fa2-43f6-94ec-09103a8e89d4",
  "role": "Writer"
}'
```
{: codeblock}
{: curl}

```java
ResourceKeyPostParameters parameters = new ResourceKeyPostParameters.Builder()
  .add("exampleParameter", "exampleValue")
  .build();
CreateResourceKeyOptions createResourceKeyOptions = new CreateResourceKeyOptions.Builder()
  .name(keyName)
  .source(instanceGuid)
  .parameters(parameters)
  .build();

Response<ResourceKey> response = service.createResourceKey(createResourceKeyOptions).execute();
ResourceKey resourceKey = response.getResult();

System.out.printf("createResourceKey() response:\n%s\n", resourceKey.toString());
```
{: codeblock}
{: java}

```javascript
const parameters = {
  'exampleParameter': 'exampleValue'
};

const params = {
  name: keyName,
  source: instanceGuid,
  parameters: parameters,
};

resourceControllerService.createResourceKey(params)
  .then(res => {
    instanceKeyGuid = res.result.guid;
    console.log('createResourceKey() response:\n' + JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
parameters = {
    'exampleParameter': 'exampleValue'
}
resource_key = resource_controller_service.create_resource_key(
    name=key_name,
    source=instance_guid,
    parameters=parameters
).get_result()

print('\ncreate_resource_key() response:\n',
      json.dumps(resource_key, indent=2))
```
{: codeblock}
{: python}

```go
createResourceKeyOptions := resourceControllerService.NewCreateResourceKeyOptions(
  keyName,
  instanceGUID,
)

parameters := &resourcecontrollerv2.ResourceKeyPostParameters{}
parameters.SetProperty("exampleParameter", "exampleValue")
createResourceKeyOptions.SetParameters(parameters)

resourceKey, response, err := resourceControllerService.CreateResourceKey(createResourceKeyOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(resourceKey, "", "  ")
fmt.Printf("\nCreateResourceKey() response:\n%s\n", string(b))
```
{: codeblock}
{: go}

Use the API key or other credential properties to connect the service instance to your app or other external consumer.

## Creating a service credential by using Terraform
{: #iam-credential-terraform}
{: terraform}

Credentials that you create after 04 August 2025 are one-time view by default, so make sure that you save them securely. The one-time view property on existing credentials is not affected. For more information, see [One-time credentials](/docs/account?topic=account-service_credentials&interface=ui#onetime-credentials).
{: important}

A credential might contain a username, password, hostname, port, and a URL, however the contents of each credential is unique to the service that generates it.Before you can create a credential to connect your app or external consumer to an {{site.data.keyword.cloud_notm}} service by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://developer.hashicorp.com/terraform/language){: external}.

Use the following steps to create a credential for connecting your app or external consumer to an {{site.data.keyword.cloud_notm}} service:

1. Create an argument in your `main.tf` file. The following example creates credentials for a resource without a service ID by using the `ibm_resource_instance` resource, where `name` is a unique name to identify the credential.

   ```terraform
   data "ibm_resource_instance" "resource_instance" {
    name = "myobjectsotrage"
   }

   resource "ibm_resource_key" "resourceKey" {
    name                 = "myobjectkey"
    role                 = "Viewer"
    resource_instance_id = data.ibm_resource_instance.resource_instance.id

    //User can increase timeouts
    timeouts {
      create = "15m"
     delete = "15m"
    }
   }
   ```
   {: codeblock}

   By default, the `ibm_resource_key` resource creates service credentials that use the public service endpoint of a service
   {: note}

   You can specify `tags` associated with the resource group instance. For more information, see the argument reference details on the [Terraform Resource Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/resource_key){: external} page.

1. After you finish building your configuration file, initialize the Terraform CLI. For more information, see [Initializing Working Directories](https://developer.hashicorp.com/terraform/cli/init){: external}.

   ```terraform
   terraform init
   ```
   {: pre}

1. Provision the resources from the `main.tf` file. For more information, see [Provisioning Infrastructure with Terraform](https://developer.hashicorp.com/terraform/cli/run){: external}.

   1. Run `terraform plan` to generate a Terraform execution plan to preview the proposed actions.

      ```terraform
      terraform plan
      ```
      {: pre}

   1. Run `terraform apply` to create the resources that are defined in the plan.

      ```terraform
      terraform apply
      ```
      {: pre}

Use the API key or other credential properties to connect the service instance to your app or other external consumer.

## Viewing a credential by using Terraform
{: #viewing-credentials-terra}
{: terraform}

You can retrieve a credentail after creation only if `onetime_credentials` is `false` for that credential. Users with the following access on the resource instance can view service key values for credentials that have `onetime_credentials` configured to `false`.
- Users with access to the service instance that is equal to or greater than the access of the service credential. For more information, see [Credential level access](/docs/account?topic=account-service_credentials).
- Users with the Administrator role on the service instance
- Users with the IAM action `resource-controller.credential.retrieve_all`. This action is given with the Administrator role.

To view an existing service credential for a service, complete the following steps:

1. Create an argument in your `main.tf` file. The following example retrieves an existing credential for a resource. For more information, see [ibm_resource_key Terraform documentation](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/resource_key).

    ```terraform
    data "ibm_resource_key" "resourceKeydata" {
      name                  = "myobjectKey"
      resource_instance_id  = ibm_resource_instance.resource.id
    }
    ```
    {: pre}

1. After you finish building your configuration file, initialize the Terraform CLI. For more information, see [Initializing Working Directories](https://developer.hashicorp.com/terraform/cli/init){: external}.

   ```terraform
   terraform init
   ```
   {: pre}

1. Provision the resources from the `main.tf` file. For more information, see [Provisioning Infrastructure with Terraform](https://developer.hashicorp.com/terraform/cli/run){: external}.

   1. Run `terraform plan` to generate a Terraform execution plan to preview the proposed actions.

      ```terraform
      terraform plan
      ```
      {: pre}

   1. Run `terraform apply` to create the resources that are defined in the plan.

      ```terraform
      terraform apply
      ```
      {: pre}

### One-time credentials
{: #onetime-credentials-terra}
{: terraform}

A resource instance has a `onetime_credentials` property that determines whether credentials that you create for that instance are one-time view. The instance setting at the time of creation determines how the property is set for each credential and cannot be changed later.
- If this property is set to `false`, the credential can be retrieved at any time by users with access. For more information about retrieving a credential, see the [ibm_resource_key Terraform documentation](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/data-sources/resource_key).
- If this property is set to `true`, you can view the credential only at creation

   Save one-time view credentials securely by using a secrets manager, password manager, or secure storage, like {{site.data.keyword.cos_short}}, in your application to prevent loss.
   {: tip}

Enable one-time view on service instances to align with the least privilege model and avoid shared access to credentials. Shared keys can make it difficult to audit how identities in your account access resources.

#### Managing the one-time view setting for a resource instance
{: #manage-otv-terra}

Users with the Administrator role or IAM action `resource-controller.instance.update_onetime_credential_off` on the service instance can manage the one-time view setting for a resource instance.

```curl
 {
      "displayName": {
        "default": "Resource Instance Update Onetime Credential Off"
      },
      "description": {
        "default": "The ability to change onetime_credential from On to Off for existing instances."
      },
      "id": "resource-controller.instance.update_onetime_credential_off",
      "roles": [
        "crn:v1:bluemix:public:iam::::role:Administrator"
      ],
      "apiTypes": [
        "crn:v1:bluemix:public:context-based-restrictions::::platform-api-type:resource-management"
      ]
    }
```
{: codeblock}

For more information, see the [ibm_resource_instance Terraform documentation](/apidocs/resource-controller/resource-controller#update-resource-instance) to update the `onetime_credentials` property. When you change the setting for an instance, existing credentials retain the setting that they have at the time of creation.

### Credential level access
{: #access-credentials-terraform}
{: terraform}

The access of the user must be equal to or greater than the access of the service credential. For example, if the credential has the IAM service role `Writer`, then the user that is trying to view the credential must have the IAM service role `Writer` or `Manager` for that particular service assigned. When a user doesn't have the correct access, details such as the API key value are redacted:

```bash
    "credentials": {
        "REDACTED": "REDACTED"
    },
```

### IAM level access
{: #iam-access-credentials-terraform}
{: terraform}

When the credential level access can't be determined by comparing the access of the user and the credential, the credential is redacted:

```bash
    "credentials": {
        "REDACTED": "REDACTED_EXPLICIT"
    },
```

## Viewing a credential
{: #viewing-credentials-ui}
{: ui}

After a credential is created for a service that has `onetime_credentials` configured to `false`, it can be viewed at any time for users that need the credential values. However, all users must have the correct level of access to see the details of a credential that includes the API key value. You can retrieve a credentail after creation only if one-time view is off for that credential. Users with the following access on the resource instance can view service key values for credentials with one-time view turned off.

- Users with access to the service instance that is equal to or greater than the access of the service credential. For more information, see [Credential level access](/docs/account?topic=account-service_credentials).
- Users with the Administrator role on the service instance.
- Users with the IAM action `resource-controller.credential.retrieve_all`. This action is given with the Administrator role.

To view an existing service credential for a service, complete the following steps:

1. From the Resource list page, select the name of the service to open the service details page.
2. Click **Service credentials**.
3. Expand **View credentials** on the row for an existing credential.

### One-time credentials
{: #onetime-credentials}
{: ui}

The credential has a `onetime_credentials` property that determines whether you can retrieve and view the credential after its initial creation. If the property is `false`, users with access can view the credential values at any time. A resource instance has a "One-time view" setting that determines whether credentials that you create for that instance are one-time view. One-time view credentials can be viewed and saved only at the time of creation. The instance setting at the time of creation determines how the property is set for each credential and cannot be changed later.
- If one-time view is "Off", the credential can be retrieved at any time by users with access.
- If one-time view is "On", you can view the credential only at creation.

   Save one-time view credentials securely by using a secrets manager, password manager, or secure storage, like {{site.data.keyword.cos_short}}, in your application to prevent loss.
   {: tip}

Enable one-time view on service instances to align with the least privilege model and avoid shared access to credentials. Shared keys can make it difficult to audit how identities in your account access resources.

#### Managing the one-time view setting for a resource instance
{: #manage-otv-ui}

Users with the Administrator role or IAM action `resource-controller.instance.update_onetime_credential_off` on a service instance can manage the one-time view setting for that instance.

```curl
 {
      "displayName": {
        "default": "Resource Instance Update Onetime Credential Off"
      },
      "description": {
        "default": "The ability to change onetime_credential from On to Off for existing instances."
      },
      "id": "resource-controller.instance.update_onetime_credential_off",
      "roles": [
        "crn:v1:bluemix:public:iam::::role:Administrator"
      ],
      "apiTypes": [
        "crn:v1:bluemix:public:context-based-restrictions::::platform-api-type:resource-management"
      ]
    }
```
{: codeblock}

For more information, see the [Resource Controller API](/apidocs/resource-controller/resource-controller#update-resource-instance) to update the `onetime_credentials` property on an instance. When you change the setting for an instance, existing credentials retain the setting that they have at the time of creation.

Existing credentials created before this property change are not affected.
{: note}

### Credential level access
{: #access-credentials-ui}
{: ui}

The access of the user must be equal to or greater than the access of the service credential. For example, if the credential has the IAM service role `Writer`, then the user trying to view the credential must have the IAM service role `Writer` or `Manager` for that particular service assigned. When a user doesn't have the correct access, details such as the API key value are redacted:

```bash
    "credentials": {
        "REDACTED": "REDACTED"
    },
```

### IAM level access
{: #iam-access-credentials-ui}
{: ui}

When the credential level access can't be determined by comparing the access of the user and the credential, the credential is redacted:

```bash
    "credentials": {
        "REDACTED": "REDACTED_EXPLICIT"
    },
```

To view the credential, the user must have the IAM level access action `resource-controller.credential.retrieve_all`. This action is given with the Administrator role, and overrides any credential level access enabling the user to view the credential.

## Viewing a credential by using the API
{: #viewing-credentials-api}
{: api}

After a credential is created for a service that has `onetime_credentials` configured to `false`, it can be viewed at any time for users that need the credential values. However, all users must have the correct level of access to see the details of a credential that includes the API key value. The access of the user must be equal to or greater than that of the service credential. For example, if the credential has the IAM service role `Writer`, then the user that is trying to view the credential must have the IAM service role `Writer` or `Manager` for that particular service assigned. You can retrieve a credentail after creation only if `onetime_credentials` is `false` for that credential. Users with the following access on the resource instance can view service key values for credentials that have `onetime_credentials` configured to `false`.

- Users with access to the service instance that is equal to or greater than the access of the service credential. For more information, see [Credential level access](/docs/account?topic=account-service_credentials).
- Users with the Administrator role on the service instance.
- Users with the IAM action `resource-controller.credential.retrieve_all`. This action is given with the Administrator role.

To get a list of all of the resource keys, call the [Resource Controller API](/apidocs/resource-controller/resource-controller#list-resource-keys) as shown in the following example:

```bash
curl -X GET https://resource-controller.cloud.ibm.com/v2/resource_keys -H 'Authorization: Bearer <IAM_TOKEN>'
```
{: codeblock}
{: curl}

```java
ListResourceKeysOptions listResourceKeysOptions = new ListResourceKeysOptions.Builder()
  .name(keyName)
  .build();

Response<ResourceKeysList> response = service.listResourceKeys(listResourceKeysOptions).execute();
ResourceKeysList resourceKeysList = response.getResult();

System.out.printf("listResourceKeys() response:\n%s\n", resourceKeysList.toString());
```
{: codeblock}
{: java}

```javascript
const params = {
  name: keyName,
};

resourceControllerService.listResourceKeys(params)
  .then(res => {
    console.log('listResourceKeys() response:\n' + JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
resource_keys_list = resource_controller_service.list_resource_keys(
    name=key_name
).get_result()

print('\nlist_resource_keys() response:\n',
      json.dumps(resource_keys_list, indent=2))
```
{: codeblock}
{: python}

```go
listResourceKeysOptions := resourceControllerService.NewListResourceKeysOptions()
listResourceKeysOptions = listResourceKeysOptions.SetName(keyName)

resourceKeysList, response, err := resourceControllerService.ListResourceKeys(listResourceKeysOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(resourceKeysList, "", "  ")
fmt.Printf("\nListResourceKeys() response:\n%s\n", string(b))
```
{: codeblock}
{: go}

Example response:

```bash
{
  "rows_count": 1,
  "next_url": null,
  "resources": [
    {
      "id": "crn:v1:bluemix:public:cloud-object-storage:global:a/4329073d16d2f3663f74bfa955259139:8d7af921-b136-4078-9666-081bd8470d94:resource-key:23693f48-aaa2-4079-b0c7-334846eff8d0",
      "guid": "23693f48-aaa2-4079-b0c7-334846eff8d0",
      "url": "/v2/resource_keys/23693f48-aaa2-4079-b0c7-334846eff8d0",
      "created_at": "2018-07-02T22:03:43.837979455Z",
      "updated_at": "2018-07-02T22:03:43.837979455Z",
      "deleted_at": null,
      "created_by": "IBMid-5500093BHN",
      "updated_by": "IBMid-5500093BHN",
      "deleted_by": "",
      "source_crn": "crn:v1:bluemix:public:cloud-object-storage:global:a/4329073d16d2f3663f74bfa955259139:8d7af921-b136-4078-9666-081bd8470d94::",
      "role": "crn:v1:bluemix:public:iam::::serviceRole:Writer",
      "name": "my-instance-key-1",
      "parameters": {
        "role_crn": "crn:v1:bluemix:public:iam::::serviceRole:Writer"
      },
      "crn": "crn:v1:bluemix:public:cloud-object-storage:global:a/4329073d16d2f3663f74bfa955259139:8d7af921-b136-4078-9666-081bd8470d94:resource-key:23693f48-aaa2-4079-b0c7-334846eff8d0",
      "state": "active",
      "account_id": "4329073d16d2f3663f74bfa955259139",
      "resource_group_id": "0be5ad401ae913d8ff665d92680664ed",
      "resource_id": "dff97f5c-bc5e-4455-b470-411c3edbe49c",
      "onetime_credentials": false,
      "credentials": {
        "apikey": "XXXX-YYYY-ZZZZ\"",
        "endpoints": "https://cos-service-armada-s.us-south.containers.mybluemix.net/endpoints",
        "iam_apikey_description": "Auto generated apikey during resource-key operation for Instance - crn:v1:bluemix:public:cloud-object-storage:global:a/4329073d16d2f3663f74bfa955259139:8d7af921-b136-4078-9666-081bd8470d94::",
        "iam_apikey_name": "auto-generated-apikey-23693f48-aaa2-4079-b0c7-334846eff8d0",
        "iam_role_crn": "crn:v1:bluemix:public:iam::::serviceRole:Writer",
        "iam_serviceid_crn": "crn:v1:bluemix:public:iam-identity::a/4329073d16d2f3663f74bfa955259139::serviceid:ServiceId-64c29e4f-422d-468c-a11b-1a8f671b5c89",
        "resource_instance_id": "crn:v1:bluemix:public:cloud-object-storage:global:a/4329073d16d2f3663f74bfa955259139:8d7af921-b136-4078-9666-081bd8470d94::"
      },
      "iam_compatible": true,
      "migrated": false,
      "resource_instance_url": "/v2/resource_instances/8d7af921-b136-4078-9666-081bd8470d94",
      "resource_alias_url": null
    }
  ]
}
```
{: codeblock}

### One-time credentials
{: #onetime-credentials-api}
{: api}

A resource instance has a `onetime_credentials` property that determines whether credentials that you create for that instance are one-time view. The instance setting at the time of creation determines how the property is set for each credential and cannot be changed later.
- If this property is set to `false`, the credential can be retrieved at any time by users with access. For more information about retrieving a credential, see the [Get resource key](/apidocs/resource-controller/resource-controller#get-resource-key) operation.
- If this property is set to `true`, you can view the credential only at creation, so make sure that you save it securely.

   Save one-time view credentials securely by using a secrets manager, password manager, or secure storage, like {{site.data.keyword.cos_short}}, in your application to prevent loss.
   {: tip}

Enable one-time view on service instances to align with the least privilege model and avoid shared access to credentials. Shared keys can make it difficult to audit how identities in your account access resources.

#### Managing the one-time view setting for a resource instance
{: #manage-otv-terra-instance}

Users with the Administrator role or IAM action `resource-controller.instance.update_onetime_credential_off` on a service instance can manage the one-time view setting for that instance.

```curl
 {
      "displayName": {
        "default": "Resource Instance Update Onetime Credential Off"
      },
      "description": {
        "default": "The ability to change onetime_credential from On to Off for existing instances."
      },
      "id": "resource-controller.instance.update_onetime_credential_off",
      "roles": [
        "crn:v1:bluemix:public:iam::::role:Administrator"
      ],
      "apiTypes": [
        "crn:v1:bluemix:public:context-based-restrictions::::platform-api-type:resource-management"
      ]
    }
```
{: codeblock}

For more information, see the [Resource Controller API](/apidocs/resource-controller/resource-controller#update-resource-instance) to update the `onetime_credentials` property on an instance. When you change the setting for an instance, existing credentials retain the setting that they have at the time of creation.

### Credential level access
{: #access-credentials-api}
{: api}

The access of the user must be equal to or greater than the access of the service credential. For example, if the credential has the IAM service role `Writer`, then the user that is trying to view the credential must have the IAM service role `Writer` or `Manager` for that particular service assigned. When a user doesn't have the correct access, details such as the API key value are redacted:

```bash
    "credentials": {
        "REDACTED": "REDACTED"
    },
```

### IAM level access
{: #iam-access-credentials-api}
{: api}

When the credential level access can't be determined by comparing the access of the user and the credential, the credential is redacted:

```bash
    "credentials": {
        "REDACTED": "REDACTED_EXPLICIT"
    },
```

To view the credential, the user must have the IAM level access action `resource-controller.credential.retrieve_all`. This action is given with the Administrator role, and overrides any credential level access enabling the user to view the credential.
