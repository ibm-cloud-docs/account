---

copyright:

  years: 2019, 2021

lastupdated: "2021-09-22"

keywords: account management, access, access policy, account administrator, user management, account management services, use account management services to grant users in the account access to invite users to the account, billing service, support center service, identity service, global catalog service, enterprise service, license service, entitlement service, license and entitlement service, role management service, catalog management service, cloud shell service, software instance service

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

# Assigning access to account management services
{: #account-services}

As the account owner or the administrator of an account management service, you can grant users access to invite users to the account, track billing and usage, and work with support cases. Users with account management access policies can also manage service IDs, access policies, catalog entries, and access groups.
{: shortdesc}

## Creating policies for account management service access
{: #account-management-access}

### Assigning access in the console
{: #console-acct-mgmt}
{: ui}

To assign access to one or all account management services, complete the following steps:

1. In the {{site.data.keyword.cloud}} console, click **Manage** > **Access (IAM)**, and then select **Users**.
2. From the row for the user that you want to assign access, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) > **Assign access**.
3. Select **Assign users additional access**, and select **Account Management**.
4. For the access, select **All Account Management Services** or select a specific account management service.
5. Select any combination of roles or permissions to define the scope of access, and click **Add**.
6. Click **Assign**. 

To grant another user full access to the account for the purposes of managing user access and all IAM-enabled account resources, you must assign two policies. To create the first policy, use the **IAM services** option, and select **All Identity and Access enabled services** in **Account** with the Administrator platform role and Manager service role. To create the second policy, use the **Account Management** option, and select **All Account Management Services** with the Administrator role assigned.
{: tip}

### Assigning access by using the CLI
{: cli}

To assign access, run the `user-policy-create` command. For more information, see [ibmcloud iam user-policy-create](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_user_policy_create). The following example command assigns a policy with the Administrator role for the Access groups account management service.

```
ibmcloud iam user-policy-create USER_NAME --roles administrator --service-name iam-groups
```

For service names to use in the CLI command for each account management service, see the following table. However, for a policy on all account management services in the CLI, use `--account-management` instead of `--service-name SERVICE_NAME`.
{: tip}

### Assigning access by using the API
{: #api-acct-mgmt}
{: api}

If you're using the [Policy management API](https://cloud.ibm.com/apidocs/iam-policy-management#create-a-policy), the account management services use the following attributes and values:

| Account management service         | Attribute and value   |
|---------------|---------------------------------|
| Billing | serviceName=billing |
| Catalog management | serviceName=globalcatalog-collection |
| Enterprise | serviceName=enterprise |
| Global catalog | serviceName=globalcatalog |
| IAM Access groups service | serviceName=iam-groups |
| IAM Identity service | serviceName=iam-identity |
| {{site.data.keyword.cloud-shell_notm}} | serviceName=cloudshell |
| License and entitlement | serviceName=entitlement | 
| Role management | serviceName=iam-access-management |
| Support center| serviceName=support |
| User management | serviceName=user-management |
| All account management services | serviceType=platform_service (don't include a serviceName attribute)  | 
{: caption="Table 1. Account management service names for API calls" caption-side="top"}

The following example assigns a policy with the Administrator role on the IAM Access groups account management service.

```bash
curl -X POST \
'https://iam.cloud.ibm.com/v1/policies' \
-H 'Authorization: $TOKEN'\
-H 'Content-Type: application/json'\
-d '{
  "type": "access",
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
      "role_id": "crn:v1:bluemix:public:iam::::role:Administrator"
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
          "value": "iam-groups"
        }
      ]
    }
  ]
}'
```
{: curl}
{: codeblock}

```java
SubjectAttribute subjectAttribute = new SubjectAttribute.Builder()
        .name("iam_id")
        .value(EXAMPLE_USER_ID)
        .build();

PolicySubject policySubjects = new PolicySubject.Builder()
        .addAttributes(subjectAttribute)
        .build();

PolicyRole policyRoles = new PolicyRole.Builder()
        .roleId("crn:v1:bluemix:public:iam::::role:Administrator")
        .build();

ResourceAttribute accountIdResourceAttribute = new ResourceAttribute.Builder()
        .name("accountId")
        .value(exampleAccountId)
        .operator("stringEquals")
        .build();

ResourceAttribute serviceNameResourceAttribute = new ResourceAttribute.Builder()
        .name("serviceName")
        .value("iam-groups")
        .operator("stringEquals")
        .build();

PolicyResource policyResources = new PolicyResource.Builder()
        .addAttributes(accountIdResourceAttribute)
        .addAttributes(serviceNameResourceAttribute)
        .build();

CreatePolicyOptions options = new CreatePolicyOptions.Builder()
        .type("access")
        .subjects(Arrays.asList(policySubjects))
        .roles(Arrays.asList(policyRoles))
        .resources(Arrays.asList(policyResources))
        .build();

Response<Policy> response = service.createPolicy(options).execute();
Policy policy = response.getResult();

System.out.println(policy);
```
{: java}
{: codeblock}

```javascript
const policySubjects = [
  {
    attributes: [
      {
        name: 'iam_id',
        value: exampleUserId,
      },
    ],
  },
];
const policyRoles = [
  {
    role_id: 'crn:v1:bluemix:public:iam::::role:Administrator',
  },
];
const accountIdResourceAttribute = {
  name: 'accountId',
  value: exampleAccountId,
  operator: 'stringEquals',
};
const serviceNameResourceAttribute = {
  name: 'serviceName',
  value: 'iam-groups',
  operator: 'stringEquals',
};
const policyResources = [
  {
    attributes: [accountIdResourceAttribute, serviceNameResourceAttribute]
  },
];
const params = {
  type: 'access',
  subjects: policySubjects,
  roles: policyRoles,
  resources: policyResources,
};

iamPolicyManagementService.createPolicy(params)
  .then(res => {
    examplePolicyId = res.result.id;
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: javascript}
{: codeblock}

```python
policy_subjects = PolicySubject(
  attributes=[SubjectAttribute(name='iam_id', value=example_user_id)])
policy_roles = PolicyRole(
  role_id='crn:v1:bluemix:public:iam::::role:Administrator')
account_id_resource_attribute = ResourceAttribute(
  name='accountId', value=example_account_id)
service_name_resource_attribute = ResourceAttribute(
  name='serviceName', value='iam-groups')
policy_resources = PolicyResource(
  attributes=[account_id_resource_attribute,
        service_name_resource_attribute])

policy = iam_policy_management_service.create_policy(
  type='access',
  subjects=[policy_subjects],
  roles=[policy_roles],
  resources=[policy_resources]
).get_result()

print(json.dumps(policy, indent=2))
```
{: python}
{: codeblock}

```go
subjectAttribute := &iampolicymanagementv1.SubjectAttribute{
  Name:  core.StringPtr("iam_id"),
  Value: &exampleUserID,
}
policySubjects := &iampolicymanagementv1.PolicySubject{
  Attributes: []iampolicymanagementv1.SubjectAttribute{*subjectAttribute},
}
policyRoles := &iampolicymanagementv1.PolicyRole{
  RoleID: core.StringPtr("crn:v1:bluemix:public:iam::::role:Administrator"),
}
accountIDResourceAttribute := &iampolicymanagementv1.ResourceAttribute{
  Name:     core.StringPtr("accountId"),
  Value:    core.StringPtr(exampleAccountID),
  Operator: core.StringPtr("stringEquals"),
}
serviceNameResourceAttribute := &iampolicymanagementv1.ResourceAttribute{
  Name:     core.StringPtr("serviceName"),
  Value:    core.StringPtr("iam-groups"),
  Operator: core.StringPtr("stringEquals"),
}
policyResources := &iampolicymanagementv1.PolicyResource{
  Attributes: []iampolicymanagementv1.ResourceAttribute{
    *accountIDResourceAttribute, *serviceNameResourceAttribute},
}

options := iamPolicyManagementService.NewCreatePolicyOptions(
  "access",
  []iampolicymanagementv1.PolicySubject{*policySubjects},
  []iampolicymanagementv1.PolicyRole{*policyRoles},
  []iampolicymanagementv1.PolicyResource{*policyResources},
)

policy, response, err := iamPolicyManagementService.CreatePolicy(options)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(policy, "", "  ")
fmt.Println(string(b))
```
{: go}
{: codeblock}

## Actions and roles for account management services
{: #account-management-actions-roles}

The following tables outline the actions that users can take when they are assigned a specific role for each account management service. Review the information to ensure that you are assigning the correct level of access to your users. 

### All account management services option
{: #all-account-management}

To quickly give users a wide-ranging set of account management access, you can assign a policy on the all account management services option. Depending on the role that is selected, all applicable actions per the selected role for each account management service can be completed by the subject of the policy.


| Roles         | Actions                                                                                                      |
|---------------|--------------------------------------------------------------------------------------------------------------|
| Viewer        | All viewer role actions for the account management services                                                  |
| Operator      | All operator role actions for the account management services                                                |
| Editor        | All editor role actions for the account management services and the ability to create resource groups        |
| Administrator | All administrator role actions for the account management services and the ability to create resource groups |
{: caption="Table 1. Roles and example actions for a policy on all identity and access services" caption-side="top"}

### Billing
{: #billing-acct-mgmt}

You can give users access to update account settings, view subscriptions, view offers, apply subscription and feature codes, update spending limits, and track usage by using the billing service.

| Roles         | Actions                                                                                                    |
|---------------|------------------------------------------------------------------------------------------------------------|
| Viewer        | View account feature settings \n  \n View subscriptions in account \n  \n View account name \n  \n View subscription balances and track usage           |
| Operator      | View account feature settings \n  \n View subscriptions in account \n  \n View and change account name |
| Editor        | View and update account feature settings \n  \n View subscriptions in account \n  \n View offers in account \n  \n View and apply subscription and feature codes \n  \n View and change account name \n  \n View and update spending limits \n  \n Set spending notifications \n  \n View subscription balances and track usage |
| Administrator | View and update account feature settings \n  \n View subscriptions in account \n  \n View offers in account \n  \n View and apply subscription and feature codes \n  \n View and change account name \n  \n View and update spending limits \n  \n Set spending notifications \n  \n View subscription balances and track usage \n  \n Create an enterprise |
{: caption="Table 2. Roles and example actions for the Billing service" caption-side="top"}

It's possible to view subscription balances and usage from the Account settings page, but you can't view the Account settings page with the Viewer or Operator roles. To access the Account settings page and your subscription information from that page, you need the Editor role or higher. 
{: note}

### Catalog management
{: #catalog-management-account-management}

You can give users access to view private catalogs and catalog filters, create private catalogs, add software to private catalogs, and set catalog filters. 

| Roles         | Actions                                                                                                |
|---------------|--------------------------------------------------------------------------------------------------------|
| Viewer        | View account-level filters set for the {{site.data.keyword.cloud_notm}} catalog \n  \n View private catalogs                                          |
| Operator      | Create private catalogs \n  \n Set filters for private catalogs \n  \n Add and update software \n  \n View account-level filters    |
| Editor        | Create private catalogs \n  \n Set filters for private catalogs \n  \n Add and update software \n  \n View account-level filters |
| Administrator | Set account-level filters for the {{site.data.keyword.cloud_notm}} catalog \n  \n Create, update, and delete private catalogs \n  \n Publish {{site.data.keyword.IBM_notm}}-approved products \n  \n Assign access policies |
| Publisher     | Publish products that are approved by {{site.data.keyword.IBM_notm}} from a private catalog |
{: caption="Table 3. Roles and example actions for the catalog management service" caption-side="top"}

### Enterprise
{: #enterprise-account-management}

You can use the enterprise service to assign users access to manage an enterprise by creating accounts within the enterprise, assigning accounts to account groups, naming account groups, and more. This type of policy works only if it is assigned within the enterprise account. 

| Roles               | Actions                                                                                                                                    |
|---------------------|--------------------------------------------------------------------------------------------------------------------------------------------|
| Viewer              | View the enterprise, account groups, and accounts                                                                                          |
| Operator            | View the enterprise, account groups, and accounts                                                                                          |
| Editor              | View and update the enterprise name and domain, create accounts and account groups, view usage reports, and import accounts. |
| Administrator       | View and update the enterprise name and domain, create accounts and account groups, move accounts between account groups, import existing accounts, and view usage reports |
| Usage report viewer | View the enterprise, accounts, and account groups and view usage reports for all accounts in the enterprise.                               |
{: caption="Table 4. Roles and example actions for the Enterprise service" caption-side="top"}

### Global catalog
{: #global-catalog-account-management}

You can give users access to view private services in the catalog or change the visibility for others users for private services by using the global catalog service.

| Roles         | Actions                                                                                                |
|---------------|--------------------------------------------------------------------------------------------------------|
| Viewer        | View private services                                                                                  |
| Operator      | Not applicable                                                                                         |
| Editor        | Change object metadata but can't change visibility for private services                                |
| Administrator | Change object metadata or visibility for private services, and restrict visibility of a public service |
{: caption="Table 5. Roles and example actions for the Global Catalog service" caption-side="top"}

### IAM access groups service
{: #access-groups-account-management}

You can give users access to view, create, edit, and delete access groups in the account by using the access groups account management service.

| Roles         | Actions                                                                                                                                                    |
|---------------|------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Viewer        | View access groups and members                                                                                                                             |
| Operator      | Not applicable                                                                                                                                             |
| Editor        | View, create, edit, and delete groups \n  \n Add or remove users from groups                                                                             |
| Administrator | View, create, edit, and delete groups \n  \n Add or remove users \n  \n Assign access to a group \n  \n Manage access for working with access groups \n  \n Enable or disable public access to resources at the account level |
{: caption="Table 6. Roles and example actions for the IAM access groups service" caption-side="top"}

### IAM identity service
{: #identity-service-account-management}

You can give users access to manage service IDs and identity providers (IdPs) by using the IAM identity service. For the IAM identity service, these actions apply to service IDs and IdPs within the account that the user didn't create. All users can create service IDs. They are the administrator for those IDs, and they can create the associated API key and access policies, but only users with the Operator and Administrator role can create IdPs. This account management service applies to the ability to view, update, delete, and assign access to service IDs in the account created by other users.

| Roles         | Actions                                                                                           |
|---------------|----------------------------------------------------------------------------------------------------|
| Viewer        | View IDs              |
| Operator      | Create and delete IDs and API keys \n  \n View, create, update, and delete IdPs \n  \n Update IAM account setting for service IDs and user API key creation         |
| Editor        | Create, update, and delete IDs and API keys \n  \n View and update IdPs \n  \n Update IAM account setting for service IDs and user API key creation      |
| Administrator | Create, update, and delete IDs and API keys \n  \n Assign access policies to IDs \n  \n View, create, update, and delete IdPs \n  \n Update IAM account setting for service IDs and user API key creation |
| User API key creator | Can create API keys when the account setting to restrict API key creation is enabled. |
| Service ID creator | Can create service IDs when the account setting to restrict service ID creation is enabled. |
{: caption="Table 7. Roles and example actions for the IAM Identity service" caption-side="top"}
{: #identity-service-acct-mgmt}

### {{site.data.keyword.cloud-shell_notm}} settings
{: #shell-service-account-management}

You can assign users access to view and update {{site.data.keyword.cloud-shell_notm}} settings for the account. Only the account owner or a user with the {{site.data.keyword.cloud-shell_notm}} administrator role can view and update the settings.

| Roles         | Actions                                                                                           |
|---------------|----------------------------------------------------------------------------------------------------|
| Viewer        | Not applicable        |
| Operator      | Not applicable        |
| Editor        | Not applicable        |
| Administrator | View and update {{site.data.keyword.cloud-shell_notm}} settings |
| Cloud Operator | Create {{site.data.keyword.cloud-shell_short}} environments to manage {{site.data.keyword.cloud_notm}} resources. |
| Cloud Developer | Create {{site.data.keyword.cloud-shell_short}} environments to manage {{site.data.keyword.cloud_notm}} resources and develop applications for {{site.data.keyword.cloud_notm}} (Web Preview enabled). |
| File Manager | Create {{site.data.keyword.cloud-shell_short}} environments to manage {{site.data.keyword.cloud_notm}}resources and manage files in your workspace (File Upload and File Download enabled). |
{: caption="Table 8. Roles and example actions for the {{site.data.keyword.cloud-shell_notm}} service" caption-side="top"}
{: #shell-service-acct-mgmt}

### License and entitlement 
{: #license-entitlement-management}

You can use the license and entitlement service to assign users access to manage licenses and entitlements within an account. Any member of an account can view and use an account’s entitlement.  
 
| Roles         | Actions                                                                                                    |
|---------------|------------------------------------------------------------------------------------------------------------|
| Viewer        |  Not applicable                                                                                            |
| Operator      |  Not applicable                                                                                            |
| Editor        |  Editors can create entitlements and view, update, bind, or delete only the entitlements they acquired.    |
| Administrator |  Administrators can create entitlements and view, update, bind, or delete any entitlements in the account. |
{: caption="Table 9. Roles and example actions for the license and entitlement service" caption-side="top"}

### Role management
{: #custom-roles-account-management}

You can give users access to create, update, and delete custom roles for services in the account. 

| Roles         | Actions                        |
|---------------|------------------------------------|
| Viewer        | Not applicable         |
| Operator      | Not applicable             |
| Editor        | Edit and update custom roles in an account          |
| Administrator | Create, edit, update, and delete custom roles in an account  |
{: caption="Table 10. Roles and example actions for the Role management service" caption-side="top"}

### Software instance
{: #sw-instance-account-management}

You can give users access to create, delete, or update a software instance. And, you can give users access to view the details page and the logs for the software instance. 

| Roles         | Actions                            |
|---------------|------------------------------------|
| Viewer        | View the software instance details page |
| Operator      | Update a software instance \n  \n View the details page for the software instance |
| Editor        | Create, delete, update a software instance \n  \n View the details page for the software instance |
| Administrator | Create, delete, update a software instance \n  \n View the details page for the software instance \n  \n View the logs for the software instance \n  \n Assign IAM permissions |
{: caption="Table 11. Roles and example actions for the Software instance service" caption-side="top"}

### Support center
{: #support-center-account-management}

You can give users access to manage support cases by using the support center service.

| Roles         | Actions                                                                       |
|---------------|-------------------------------------------------------------------------------|
| Viewer        |  View cases \n  \n Search cases                                             |
| Operator      |  Not applicable                                                               |
| Editor        |  View cases \n  \n Search cases \n  \n Update cases \n  \n Create cases |
| Administrator |  View cases \n  \n Search cases \n  \n Update cases \n  \n Create cases |
{: caption="Table 12. Roles and example actions for the Support Center service" caption-side="top"}

Assign users the viewer role on the user management service in addition to a support center access policy so the user can see all cases in the account regardless of user list visibility settings. If the user list visibility is set to restricted, this can limit a user's ability to view, search, and manage support cases in an account that they didn't open themselves.
{: tip}

### User management
{: #user-management-account-management}

You can give users access to view users in an account, invite and remove users, and view and update user profile settings with the user management account management service. 

| Roles         | Actions                                                                                                |
|---------------|--------------------------------------------------------------------------------------------------------|
| Viewer        | View users in the account \n  \n View user profile settings                                          |
| Operator      | View users in the account \n  \n View user profile settings                                          |
| Editor        | View, invite, remove, and update users from the account \n  \n View and update user profile settings |
| Administrator | View, invite, remove, and update users from the account \n  \n View and update user profile settings |
{: caption="Table 13. Roles and example actions for the User Management service" caption-side="top"}

The viewer role on the user management service is a role that is commonly assigned for users assigned a role to view or manage support cases. If an account owner restricts the visibility of the user list in the IAM settings, users can't see support cases that are opened by other users in the account. However, if they are assigned the viewer role for the user management service, the user list visibility setting doesn't affect the ability to view cases in the account.
{: tip}




