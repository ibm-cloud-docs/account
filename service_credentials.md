---

copyright:

  years: 2015, 2021
lastupdated: "2022-05-04"

keywords: service key, api key, bind, credential

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Adding and viewing credentials
{: #service_credentials}

You can generate a new set of credentials for times when you want to manually connect an app or external consumer to an {{site.data.keyword.Bluemix}} service. For example, if you're trying to bind an AWS app to a Watson service, you need to generate a new credential that can be used to bind them together. After your credential is created, you can [manually add](/docs/apps?topic=apps-credentials_overview) it to your {{site.data.keyword.Bluemix_notm}} app or other [external consumer](/docs/account?topic=account-externalapp) to connect your service.
{: shortdesc}

To manually add credentials to your apps, refer to the documentation for the type of app or compute option that you are using.
{: tip}

## Adding a credential when binding an IAM-enabled service
{: #IAM_credential-ui}
{: ui}

Services that are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) can generate a resource key, also known as a credential. Credentials are service-specific and vary based on how each service defines the credentials they need to generate. A credential might contain a user name, password, host name, port, and a URL.

However, while the contents of each credential is unique to the service that generates it, all services managed by IAM require that new credentials include an IAM Service access role. Some services might generate more data that requires parameters to be passed in. For example, a service might require you to input a language parameter to set the default language that is returned in the resource key that is generated.

Complete the following steps to add a credential to a service that is managed by IAM:

1. From the Resource list page, select the name of the service to open the service details page. Then, select the Credentials tab, and click **New Credential**.
2. From the Add New Credential dialog, provide a **Name**.
3. Specify the role. This value sets the IAM service access role. For more information, see [IAM Access](/docs/account?topic=account-userroles).
4. Optionally, you can provide a Service ID by either allowing IAM to generate a unique value for you, or by providing an existing Service ID. For more information, see [Creating and working with service IDs](/docs/account?topic=account-serviceids).
5. Optionally, you can provide more parameters as a valid JSON object that contains service-specific configuration parameters, provided either inline or in a file.

   Most services don't require extra parameters, and for services that do, each service defines its own unique list of parameters. For a list of supported configuration parameters, see the documentation for the particular service offering.
   {: note}

6. Click **Add** to generate the new service credential.

## Adding a credential when binding an IAM-enabled service by using the API
{: #IAM_credential-api}
{: api}

Services that are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) can generate a resource key, also known as a credential. Credentials are service-specific and vary based on how each service defines the credentials they need to generate. A credential might contain a user name, password, host name, port, and a URL.

However, while the contents of each credential is unique to the service that generates it, all services managed by IAM require that new credentials include an IAM Service access role. Some services might generate more data that requires parameters to be passed in. For example, a service might require you to input a language parameter to set the default language that is returned in the resource key that is generated.

To create a resource key, call the [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller#create-resource-key) as shown in the following example:

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

## Adding a credential when binding an IAM-enabled service by using Terraform
{: #iam-credential-terraform}
{: terraform}

You can add credentials for an IAM-enabled service by using Terraform. 

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to add a credential by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

   The following example creates credentials for a resource without a service ID by using the `ibm_resource_instance` resource, where `name` is a unique name to identify the credential. 
   
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
  
3. Initialize the Terraform CLI.

   ```terraform
   terraform init
   ```
   {: pre}
   
4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to create the credentials.

   ```terraform
   terraform plan
   ```
   {: pre}

5. Create the credentials.

   ```terraform
   terraform apply
   ```
   {: pre}

## Adding a credential when binding a Cloud Foundry service
{: #cf_credential-ui}
{: ui}

Cloud Foundry services can generate a service key, also known as a credential. Credentials are service-specific and vary based on how each service defines the credentials they need to generate. A service credential might contain a user name, password, host name, port, and a URL.

However, the contents of each credential is unique to the service that generates it. Some services might generate extra data that requires parameters to be passed in. For example, a service might require you to input a language parameter to set the default language that is returned in the service key that is generated.

Complete the following steps to add a Cloud Foundry credential:

1. From the service details page, select the Credentials tab, and click **New Credential**.
2. From the Add New Credential dialog, provide a **Name**.
3. Optionally, you can provide more parameters as a valid JSON object that contains service-specific configuration parameters, provided either inline or in a file.

   Most services don't require extra parameters, and for services that do, each service defines its own unique list of parameters. For a list of supported configuration parameters, see the documentation for the particular service offering.
   {: note}
   
4. Click **Add** to generate the new service credential.

## Adding a credential when binding a Cloud Foundry service by using the API
{: #cf_credential-api}
{: api}

Service credential bindings are used to make the details of the connection to a service instance available to an app or a developer. Service credential bindings can be of type `app` or `key`.

A service credential binding is of type `app` when it is a binding between a [service instance](http://v3-apidocs.cloudfoundry.org/version/3.99.0/index.html#service-instances){}: external} and an [application](http://v3-apidocs.cloudfoundry.org/version/3.99.0/index.html#apps){: external}. Not all services support this binding, as some services deliver value to users directly without integration with an application. Field `broker_catalog.features.bindable` from [service plan](http://v3-apidocs.cloudfoundry.org/version/3.99.0/index.html#the-service-plan-object){: external} of the service instance can be used to determine if it is bindable.

A service credential binding is of type `key` when it retrieves only the details of the service instance and makes them available to the developer.

To create a service credential binding, call the [Cloud Foundry API](http://v3-apidocs.cloudfoundry.org/version/3.99.0/index.html#create-a-service-credential-binding){: external} as shown in the following examples.

### Example request to create an app credential binding
{: #app-cred-binding-api}

```bash
curl "https://api.example.org/v3/service_credential_bindings" \
  -X POST \
  -H "Authorization: bearer [token]" \
  -H "Content-type: application/json" \
  -d '{
    "type": "app",
    "name": "some-binding-name",
    "relationships": {
      "service_instance": {
        "data": {
          "guid": "7304bc3c-7010-11ea-8840-48bf6bec2d78"
        }
      },
      "app": {
        "data": {
          "guid": "e0e4417c-74ee-11ea-a604-48bf6bec2d78"
        }
      }
    },
    "parameters": {
      "key1": "value1",
      "key2": "value2"
    },
    "metadata": {
      "labels": {
        "foo": "bar"
      },
      "annotations": {
        "baz": "qux"
      }
    }
  }'
```
{: codeblock}

### Example request to create a key credential binding
{: #key-cred-binding-api}

```bash 
curl "https://api.example.org/v3/service_credential_bindings" \
  -X POST \
  -H "Authorization: bearer [token]" \
  -H "Content-type: application/json" \
  -d '{
    "type": "key",
    "name": "some-binding-name",
    "relationships": {
      "service_instance": {
        "data": {
          "guid": "7304bc3c-7010-11ea-8840-48bf6bec2d78"
        }
      }
    },
    "parameters": {
      "key1": "value1",
      "key2": "value2"
    },
    "metadata": {
      "labels": {
        "foo": "bar"
      },
      "annotations": {
        "baz": "qux"
      }
    }
  }'
```
{: codeblock}

## Viewing a credential
{: #viewing-credentials-ui}
{: ui}

After a credential is created for a service, it can be viewed at any time for users that need the API key value. However, all users must have the correct level of access to see the details of a credential that includes the API key value. 

To view an existing service credential for a service, complete the following steps:

1. From the Resource list page, select the name of the service to open the service details page. 
2. Click **Service credentials**
3. Expand **View credentials** on the row for an existing credential.

### Credential level access
{: #access-credentials-ui}
{: ui}

The access of the user must be equal to or greater than the access of the service credential. For example, if the credential has the IAM service role `Writer`, then the user trying to view the credential must have the IAM service role `Writer` or `Manager` for that particular service assigned. When a user doesn't have the correct access, details such as the API key value are redacted:

```text
    "credentials": {
        "REDACTED": "REDACTED"
    },
```

### IAM level access
{: #iam-access-credentials-ui}
{: ui}

When the credential level access can't be determined by comparing the access of the user and the credential, the credential is redacted: 

```text
    "credentials": {
        "REDACTED": "REDACTED_EXPLICIT"
    },
```

To view the credential, the user must have the IAM level access action `resource-controller.credential.retrieve_all`. This action is given with the Administrator role, and overrides any credential level access enabling the user to view the credential.

## Viewing a credential by using the API
{: #viewing-credentials-api}
{: api}

After a credential is created for a service, it can be viewed at any time for users that need the API key value. However, all users must have the correct level of access to see the details of a credential including the API key value. The access of the user must be equal to or greater than that of the service credential. For example, if the credential has the IAM service role `Writer`, then the user trying to view the credential must have the IAM service role `Writer` or `Manager` for that particular service assigned.

To get a list of all of the resource keys, call the [Resource Controller API](https://cloud.ibm.com/apidocs/resource-controller/resource-controller#list-resource-keys) as shown in the following example: 

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

### Credential level access
{: #access-credentials-api}
{: api}

The access of the user must be equal to or greater than the access of the service credential. For example, if the credential has the IAM service role `Writer`, then the user that is trying to view the credential must have the IAM service role `Writer` or `Manager` for that particular service assigned. When a user doesn't have the correct access, details such as the API key value are redacted:

```text
    "credentials": {
        "REDACTED": "REDACTED"
    },
```

### IAM level access
{: #iam-access-credentials-api}
{: api}

When the credential level access can't be determined by comparing the access of the user and the credential, the credential is redacted: 

```text
    "credentials": {
        "REDACTED": "REDACTED_EXPLICIT"
    },
```

To view the credential, the user must have the IAM level access action `resource-controller.credential.retrieve_all`. This action is given with the Administrator role, and overrides any credential level access enabling the user to view the credential.
