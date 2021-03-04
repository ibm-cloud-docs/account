---

copyright:

  years: 2017, 2021

lastupdated: "2021-03-04"

keywords: resource access, assign access, IAM access policy, access to resource groups, edit access, remove access 

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:help: data-hd-content-type='help'}
{:support: data-reuse='support'}
{:tip: .tip}
{:note: .note}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}

# Managing access to resources
{: #assign-access-resources}

To manage access for users or service IDs by using IAM policies, you must be the account owner or have the correct access assigned. To assign user's access to resources you must be an administrator on all services in the account, or the assigned administrator for the particular service or service instance. To assign access to a service ID, you must be administrator on the identity service or the specific service ID.
{:shortdesc}

## Assigning access to resources
{: #assign-new-access}
{: help}
{: support}

You can assign access to resources by using two types of policies:

* Access to resources in the account, including the option for just one type or all types
* Access to resources within a resource group, including the option for just one resource or all

If you delete or edit an existing policy for a service ID currently being used, it might cause service interruption.
{: note}

If you want to enable a user full administrator access to complete [account management tasks](/docs/account?topic=account-account-services#account-services), such as inviting and removing users, viewing billing and usage, managing service IDs, managing access groups, managing user access, and access to all account resources, you must assign a user the following access:
* A policy for **All Identity and Access enabled services** within the **Account** with the Administrator and Manager roles.
* A policy with Administrator role on **All Account Management Services**.

### Assigning access to resources in the console
{: #access-resources-console}
{: ui}

To assign access to an individual resource in the account or access to all resources in the account, complete the following steps:

1. In the console, click **Manage** > **Access (IAM)**, and select **Users** or **Manage** > **Access (IAM)**, and select **Service IDs**, depending on which identity you want to assign access.
2. From the row for the user or service ID that you want to assign access, select the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu > **Assign access**.
3. Add the user or service ID to an access group. Click **Add** for the access group that you want the user or service ID to belong to.
4. (Optional) Manually assign users access.
  1. Expand the Assign additional access section, and click **IAM services**.
  2. Select the option for all services or just a specific service.
  3. Select any combination of roles to assign the user or service ID, and click **Add** > **Assign**.

If a user doesn't have a role on the resource group that contains the resources, they can see the resources, but can't access the resources by going to the Resource list page in the account to start working with them. Assign the Viewer role or higher on the resource group itself to ensure that a user can access the resource.
{: note}

### Assigning access to resources by using the CLI
{: #access-resources-cli}
{: cli}

1. Log in to {{site.data.keyword.cloud}} CLI. If you have multiple accounts, you are prompted to select which account to use. If you do not specify a region with the `-r` flag, you must also select a region.
    ```
    ibmcloud login
    ```
    {: codeblock}

    If your credentials are rejected, you might be using a federated ID. To log in with a federated ID, use the `--sso` flag. See [Logging in with a federated ID](/docs/account?topic=account-federated_id) for more details.
    {: tip}
    
    If it's your first time using the {{site.data.keyword.cloud_notm}} CLI, check out the [getting started tutorial](/docs/cli?topic=cli-getting-started).

2. Create an access policy and assign it to a user or a service ID.

 * To assign access to an individual resource in the account or access to all resources in the account, enter the [**`ibmcloud iam user-policy-create`**](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_user_policy_create) command. This example gives `name@example.com` `Administrator` role for all instances of `sample-service` service:
    ```
    ibmcloud iam user-policy-create name@example.com --roles Administrator --service-name sample-service
    ```
    {: codeblock}
 * To assign access to a service ID or to more services in the account, enter the [**`ibmcloud iam service-policy-create`**](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_service_policy_create) command. This example grants service `test` the `Administrator` role for all account management services:
    ```
    ibmcloud iam service-policy-create test --roles Administrator --account-management
    ```
    {: codeblock}

### Assigning access to resources by using the API
{: #access-resources-api}
{: api}

You can assign access to an individual resource in the account or access to a list of resources in the account by calling the [{{site.data.keyword.iamlong}} (IAM) Policy Management API](https://{DomainName}/apidocs/iam-policy-management){: external} as shown in the following sample request. The sample request gives `Editor` role access for an instance of a service:

   ```
    curl -X POST 'https://iam.cloud.ibm.com/v1/policies' -H 'Authorization: Bearer $TOKEN' \
    -H 'Content-Type: application/json' -d '{
      "type": "access",
      "description": "Editor role for SERVICE_NAME's RESOURCE_NAME",
      "subjects": [
        {
          "attributes": [
            {
              "name": "iam_id",
              "value": "IBMid-123453user"
            }
          ]
        }'
      ],
      "roles":[
        {
          "role_id": "crn:v1:bluemix:public:iam::::role:Editor"
        }
      ],
      "resources":[
        {
          "attributes": [
            {
              "name": "accountId",
              "value": "$ACCOUNT_ID"
            },
            {
              "name": "serviceName",
              "value": "$SERVICE_NAME"
            },
            {
              "name": "resource",
              "value": "$RESOURCE_NAME",
              "operator": "stringEquals"
            }
          ]
        }
      ]
    }'
   ```
   {: codeblock}

### Assigning access within a resource group in the console
{: #access-to-resources-console}
{: ui}

To assign access to all resources in a resource group or to just one service within a resource group, complete the following steps:

1. In the console, click **Manage** > **Access (IAM)**, and select **Users** or **Manage** > **Access (IAM)**, and select **Service IDs**, depending on which identity you want to assign access.
2. From the row for the user or service ID that you want to assign access, select the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu, and click **Assign access**.
3. Add the user or service ID to an access group. Click **Add** for the access group that you want the user or service ID to belong to.
4. (Optional) Manually assign additional access.
  1. Expand the Assign additional access section, and click **IAM services**.
  2. Select the option for all services or just a specific service, and then specify if the access is in the **Account**, which means the user or service ID doesn't get access to the resource group that contains the resource, or select a specific resource group. By selecting a resource group, you can select roles for access to manage the resource group as well.
  3. Select any combination of roles to assign, and click **Add** > **Assign**.

### Assigning access within a resource group by using the CLI
{: #access-resourcegroups-cli}
{: cli}

Enter the [**`ibmcloud user-policy-create`**](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_user_policy_create) command to assign access to all resources in a resource group or to just one service within a resource group. This example gives `name@example.com` `Operator` role for resource group with ID `dda27e49d2a1efca58083a01dfde18f6`:

  ```
  ibmcloud iam user-policy-create name@example.com --roles Operator --resource-type resource-group --resource dda27e49d2a1efca58083a01dfde18f6
  ```
  {: codeblock}

Enter the [**`ibmcloud iam service-policy-create`**](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_service_policy_create) command to assign access to all resources in a resource group or to just one service within a resource group. This example gives service `test` `Administrator` role for resource group called `sample-resource-group`:

  ```
  ibmcloud iam service-policy-create test --roles Administrator --resource-group-name sample-resource-group
  ```
  {: codeblock}

## Removing access in the console
{: #removing-access-console}
{: ui}

Removing access for a user or service ID can take up to 10 minutes to take effect.

1. In the console, click **Manage** > **Access (IAM)**, and select **Users** or **Manage** > **Access (IAM)**, and select **Service IDs**, depending on which identity you want to assign access.
2. Select the user's name or service ID that you want to remove access for.
3. From the **Access policies** tab, select the **Actions** ![List of actions icon](../icons/action-menu-icon.svg) menu on the row for the policy you want to remove, and click **Remove**.  
4. Review the policy details that you're about to remove, and confirm by clicking **Remove**.

You can also remove users and service IDs from access groups by selecting the checkbox for the user or service ID that you want to remove, and click **Remove**. Then, click **Remove** again to approve the process. 
{: tip}

## Removing access by using the CLI
{: #removing-access-cli}
{: cli}

To remove a user policy by using the CLI, you can use the [**`ibmcloud iam user-policy-delete`**](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_user_policy_delete) command.

  ```
  ibmcloud iam user-policy-delete USER_ID POLICY_ID [-f, --force]
  ```
  {: codeblock}

To remove a service ID policy by using the CLI, you can use the [**`ibmcloud iam service-policy-delete`**](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_service_policy_delete) command.

  ```
  ibmcloud iam service-policy-delete SERVICE_ID POLICY_ID [-f, --force]
  ```
  {: codeblock}

## Removing access by using the API
{: #remove-access-api}
{: api}

Delete a policy by providing a policy ID and calling the [{{site.data.keyword.iamlong}} (IAM) Policy Management API](https://{DomainName}/apidocs/iam-policy-management){: external} as shown in the following sample request:

  ```
  curl -X DELETE 'https://iam.cloud.ibm.com/v1/policies/$POLICY_ID' \
  -H 'Authorization: Bearer $TOKEN' \
  -H 'Content-Type: application/json'
  ```
  {: codeblock}

A policy cannot be deleted if the subject ID contains a locked service ID.
{: note}

## Reviewing assigned access in the console
{: #review-your-access-console}
{: ui}

If you need to review your assigned access in an account that you've been added to, complete the following steps:

1. In the console, click **Manage** > **Access (IAM)**, and select **Users** or **Service IDs**, depending on which identity you want to review.
2. Select your name or the service ID.
3. Review the assigned access in the **Access policies** section.

If you need more access, you must contact the account owner to update your access or contact the administrator for the service or service instance to update the access policy.
{: tip}

## Reviewing assigned access by using the CLI
{: #review-your-access-cli}
{: cli}

If you need to review your assigned access in an account that you've been added to, you can use the [**`ibmcloud iam user-policies`**](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_user_policies) command. This example lists policies of user `name@example.com`:

  ```
  ibmcloud iam user-policies name@example.com
  ```
  {: codeblock} 

## Reviewing assigned access by using the API
{: #review-your-access-api}
{: api}

By using the API, you can only retrieve all policies in the account and filter by attribute values. You can check your assigned access in an account by going to **Manage** > **Users** > **your_name** > **Access policies** in the console. To retrieve policies, call the [{{site.data.keyword.iamlong}} (IAM) Policy Management API](https://{DomainName}/apidocs/iam-policy-management){: external} as shown in the following sample request:

   ```
   curl -X GET 'https://iam.cloud.ibm.com/v1/policies?account_id=$ACCOUNT_ID' \
   -H 'Authorization: Bearer $TOKEN' \
   -H 'Content-Type: application/json'
   ```
   {: codeblock} 
