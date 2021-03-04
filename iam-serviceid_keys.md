---

copyright:

  years: 2015, 2021
lastupdated: "2021-03-03"

keywords: service ID, service ID API key, lock service ID API key, delete service ID API key

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


# Managing service ID API keys
{: #serviceidapikeys}

Service IDs are created to enable access to your {{site.data.keyword.Bluemix}} services by applications hosted both inside and outside of {{site.data.keyword.Bluemix_notm}}. API keys are used by an application to authenticate as a particular service ID and are granted the access that is associated with that specific service ID.
{:shortdesc}

After you create a service ID, you can start creating API keys and assigning service policies. Each policy specifies the level of access that is allowed when the API key is used to authenticate with your services. For more information about creating a service ID and assigning policies, see [Creating and working with service IDs](/docs/account?topic=account-serviceids). For more information about the CLI commands that are used to manage service ID API keys, see [Managing IAM access, API keys, service IDs, and access groups](/docs/cli?topic=cli-ibmcloud_commands_iam).

Each API key that is associated with a service ID inherits the policy that is assigned to the service ID. For example, if you want one application to view resources within a service, you need to use an API key that is associated with a service ID that has a policy that is assigned with the Viewer role. If you want another application to be able to have full access within a service, then you need to use an API key that is associated with a second service ID that has a policy that is assigned with the Administrator role.

For more information, see [Examples of how to use a service ID](/docs/account?topic=account-serviceids#examples_serviceid).

## Required access for managing service ID API keys
{: #required-access-serviceid-keys}

All users can create service IDs in an account, and they are the administrator for those IDs and can create the associated API key and access policies. However, account owners and users assigned the Administrator role on the IAM Identity service can manage the API keys for all service IDs in an account. Users can also be given access to a single service ID only, if the ID is specified when the administrator assigns the access.

If you are a user with the required access, you can view, update, and delete API keys for any service ID in the account. Go to the **API keys** page, and select the **All service ID API keys** option in the **View** menu to find an API key that you want to view details for, update, or delete.
{: ui}


## Creating an API key for a service ID
{: #create_service_key}
{: ui}

Create an API key to associate with a service ID in the console:

1. In the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** &gt; **Access (IAM)**, and select **Service IDs**.
2. If you don't have a service ID created, create the service ID.
3. From the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu, click **Manage service ID**.
4. Click **API keys**.
5. Click **Create**.
6. Add a name and description to easily identify the API key.
7. Click **Create**.
8. Save your API key by copying or downloading it to secure location.

For security reasons, the API key is only available to be copied or downloaded at the time of creation. If the API key is lost, you must create a new API key.
{: note}


## Updating an API key for a service ID
{: #update_service_key}
{: ui}

You can update an API key by editing the name or description that is used to identify the key in the UI.

1. In the console, go to **Manage** &gt; **Access (IAM)**, and select **Service IDs**.
2. From the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu, click **Manage service ID**.
3. Click **API keys**.
4. From the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu, click **Edit name & description**.

If you didn't create the service ID, but you are the account owner or an administrator for the IAM Identity service, you can update API keys for any service ID in the account. Go to the **API keys** page, and select the **All service ID API keys** option in the **View** menu to find the API key that you want to work with.
{: tip}


## Updating an API key for a service ID
{: #update_service_key-cli}
{: cli}

To update an API key for a service ID by using the CLI, you can use the [ibmcloud iam service-api-key-update](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_service_api_key_update) command.

```
ibmcloud iam service-api-key-update NAME SERVICE_ID [-n, --name NEW_sNAME] [-d, --description DESCRIPTION] [-v, --version VERSION] [-f, --force]
```
{: codeblock}


## Locking a service ID's API key
{: #lockkey}

For API keys that represent the identity of the service ID, you can prevent the API key from being deleted by locking it. A locked API key is indicated by the ![Locked icon](images/locked.svg "Locked") icon in the UI.

1. In the console, click **Manage** &gt; **Access (IAM)**, and select **Service IDs**.
2. Identify the row of the service ID that you want to select an API key for, and select the name of the service ID.
3. Click **API keys**.
4. Hover on the row of the API key that you want to lock, and click the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu to open a list of options.
5. Click **Lock API key**.

You can unlock your API key at any time to update, delete, or add an access policy, or to remove the API key.
{: tip}

## Locking or unlocking a service ID API key with the CLI
{: #lock_unlock_cli}
{: cli}

For API keys that represent the identity of the service ID, you can prevent the API key from being deleted by locking it. A locked API key is indicated by the ![Locked icon](images/locked.svg "Locked") icon in the UI. To lock a service ID API key, use the following command:

```
ibmcloud iam service-api-key-lock (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID) [-f, --force]
```

<strong>Prerequisites</strong>: Endpoint, Login, Target

<strong>Command Options</strong>:
<dl>
  <dt>APIKEY_NAME (required)</dt>
  <dd>Name of the API key, exclusive with APIKEY_UUID</dd>
  <dt>APIKEY_UUID (required)</dt>
  <dd>UUID of the API key, exclusive with APIKEY_NAME</dd>
  <dt>SERVICE_ID_NAME (required)</dt>
  <dd>Name of the service ID, exclusive with SERVICE_ID_UUID</dd>
  <dt>SERVICE_ID_UUID (required)</dt>
  <dd>UUID of the service ID, exclusive with SERVICE_ID_NAME</dd>
  <dt>-f, --force</dt>
  <dd>Lock without confirmation</dd>
</dl>

<strong>Examples</strong>:

Lock service API key `sample-key` of service ID `sample-service`:

```
ibmcloud iam service-api-key-lock sample-key sample-service
```

To unlock a service ID API key, use the following command:

```
ibmcloud iam service-api-key-unlock (APIKEY_NAME|APIKEY_UUID) (SERVICE_ID_NAME|SERVICE_ID_UUID) [-f, --force]
```


## Deleting an API key for a service ID
{: #delete_service_key}
{: ui}

You can delete an API key that is associated with a service ID. However, deleting an API key that is used by an application removes the ability for that application to authenticate with your services.

1. In the console, go to **Manage** &gt; **Access (IAM)**, and select **Service IDs**.
2. If you don't have a service ID created, create the service ID.
3. From the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu, click **Manage service ID**.
4. Click **API keys**.
5. From the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu, click **Delete**.

If you didn't create the service ID, but you are the account owner or an administrator for the IAM Identity service, you can delete API keys for any service ID in the account. Go to the **API keys** page, and select the **All service ID API keys** option in the **View** menu to find the API key that you want to work with.
{: tip}


## Deleting an API key for a service ID using the CLI
{: #delete_service_key-cli}
{: cli}

You can delete an API key that is associated with a service ID. However, deleting an API key that is used by an application removes the ability for that application to authenticate with your services. To delete an API key for a service ID by using the CLI, you can use the [ibmcloud iam service-api-key-delete](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_service_api_key_delete) command.

```
ibmcloud iam service-api-key-delete NAME SERVICE_ID [-f, --force]
```
{: codeblock}
