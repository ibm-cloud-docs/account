---

copyright:

  years: 2018, 2023

lastupdated: "2023-01-18"


keywords: access groups, access group, create group, assign access to group, administrator, administrator role

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Setting up access groups
{: #groups}

An access group can be created to organize a set of users, service IDs, and trusted profiles into a single entity that makes it easy for you to assign access. You can assign a single policy to the group instead of assigning the same access multiple times for an individual user or service ID.
{: shortdesc}

Access groups are assigned policies that grant roles and permissions to the members of that group. Members of an access group can include multiple identity types, like users, service IDs, and trusted profiles. The members inherit the policies, roles, and permissions that are assigned to the access group, and also keep the roles that they are assigned individually.

For example, if a user is assigned the `viewer` role on the billing service and they are added to an access group that has the `publisher` role on the catalog management service, they keep their `viewer` role even though that isn't part of the access group permissions.

To make assigning and managing access even easier, you can set up resource groups to organize a set of resources that you want a group of users to have access to. When your resource group is set up, you can assign a policy that gives access to all resources within that group instead of creating access policies for individual service instances within your account.
{: tip}

## Watch and learn
{: #watch-accessgroups}

![Setting up an access group](https://www.kaltura.com/p/1773841/sp/177384100/embedIframeJs/uiconf_id/27941801/partner_id/1773841?iframeembed=true&entry_id=1_2vfzfco0){: video output="iframe" data-script="#groups-transcript" id="mediacenterplayer" frameborder="0" width="560" height="315" allowfullscreen webkitallowfullscreen mozAllowFullScreen}

### Video transcript
{: #groups-transcript}
{: notoc}

Welcome back to another installment of the IBM Cloud Console Guide. In this video, we will be showing you how to set up an access group.

Assigning access to users in IBM Cloud individually can be time consuming, especially if you have a large organization. That’s where access groups come in to play.

Access groups allow you to assign a minimal number of policies by giving the same access to all users and service IDs that belong to the same access group. In other words, instead of assigning the same access multiple times to multiple users or service IDs, you can create a group and assign a single policy to that group. This helps save time and keep access permissions organized.

The best practice for setting up access groups is to create one access group per wanted level of access. Then, you can map each access group to the previously created resource groups. For example, you might create Auditor, Developer, and Admin groups, then assign access to these groups based upon the individual’s role.

Now that you know what access groups are and why they’re important, let’s go over how to create an access group.

In the IBM Cloud console, click “Manage” and then “Access (IAM).” Then, select “Access Groups” and click “Create.”

Here you will enter the name and description for the group. Then, click “Create.

After you create an access group, you can then add users and service IDs to the group (clicks Users and Service ID tabs within the UI for managing the created access group).

Before we dive into how to assign access to the access groups, you need to understand how IAM access policies provide access. A policy consists of a subject, target, and role (clicks Access policies tab). The subject is the access group. The target will be what you want the subject to access. This could be a set of resources, a service instance, all services in the account, or all instances of a service.

Access policies can only be set for IAM-enabled services and account management services (clicks "Assign access" button on the Access policies tab for the created access group, then highlights two tiles for IAM-enabled services and Account management services). Cloud Foundry and Classic Infrastructure are separate.

The role defines the level of access granted to a user (Starts creating a policy by selecting All identity and access enabled services, then scrolling the available roles that display). The most commonly used roles are viewer, editor, and administrator. The viewer role provides the least amount of access for viewing instances and resource groups. The editor role allows more access to create, edit, delete, and bind service instances. While the administrator includes everything for working with a service instance and can also assign access to others.

To make assigning access as easy as possible, you can organize resources into a resource group and users and service IDs into an access group. After you set up each one, you can then create access policies for the access groups to give users access to the resources you’ve created.

To get started, click “Manage” in the IBM Cloud console, then click “Access (IAM)” and select “Access Groups.”

Then, select the name of the access group that you want to assign access.

Select the “Access policies” tab, and then click “Assign access.”

Now you will select the type of access that you want to assign (clicks IAM services, selects All identity and access-enabled services, selects Administrator platform role, selects Reader service role). Then, click “Add” and “Assign.” (Then, clicks "Invite" button.)

Inviting users to the access group is easy. You can add users directly to each access group by clicking on “Users” and the blue “Invite Users” button.

Thank you for watching this installment of the IBM Cloud Console Guide.

## Before you begin
{: #prereq-create-groups}

To manage or create new access groups, you must have the following type of access:

* Account owner
* Administrator or editor on the IAM Access Groups account management service in the account
* Administrator or editor for the All Account Management services

Additionally, an administrator or editor can be assigned access to manage an individual group by creating an access policy where the resource is the Access group ID. For more information about access policies and roles for the IAM Access Groups service, see [IAM access](/docs/account?topic=account-userroles#userroles).

## Before you begin
{: #prereq-create-groups-tf}
{: terraform}

Before you can set up access groups by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to create an authorization between services by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

## Creating an access group in the console
{: #create_ag}
{: ui}

A unique name is required to differentiate access groups in the account. To create an access group, complete the following steps:

1. In the {{site.data.keyword.cloud}} console, click **Manage** > **Access (IAM)**, and select **Access Groups**.
1. Click **Create**.
1. Enter a unique name to identify your access group, an optional description, and click **Create**.

Next, continue to set up your groups by adding users, service IDs, or trusted profiles. You can add users manually or by [creating dynamic rules](/docs/account?topic=account-rules&interface=ui). Or, you can start assigning the group access, and decide who you want to add to the access group later.

You can delete a group by selecting the **Remove group** option. When you remove a group from the account, you are removing all users and service IDs from the group and all access that is assigned to the group.
{: note}

## Creating an access group by using the CLI
{: #create_ag_cli}
{: cli}

To create an access group by using the CLI, you can use the [ibmcloud iam access-group-create](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_access_group_policy_create) command.

```bash
ibmcloud iam access-group-create GROUP_NAME [-d, --description DESCRIPTION]
```
{: codeblock}

A unique name is required to differentiate access groups in the account.
{: note}

## Creating an access group by using the API
{: #create_ag_api}
{: api}

You can programmatically create access groups by calling the [{{site.data.keyword.iamlong}} (IAM) Access Groups API](/apidocs/iam-access-groups#create-access-group){: external} as shown in the following sample request. The example creates an access group for managers in the account:

```bash
curl -X POST -H "Authorization: {iam_token}" \
-H "Accept: application/json" \
-H "Content-Type: application/json" \
-d '{ "name": "Managers", "description": "Group for managers" }' \
"{base_url}/groups?account_id={account_id}"
```
{: curl}
{: codeblock}

```java
CreateAccessGroupOptions createAccessGroupOptions = new CreateAccessGroupOptions.Builder()
  .accountId(testAccountId)
  .name("Managers")
  .description("Group for managers")
  .build();

Response<Group> response = service.createAccessGroup(createAccessGroupOptions).execute();
Group group = response.getResult();

System.out.println(group);
```
{: java}
{: codeblock}

```javascript
const params = {
  accountId: testAccountId,
  name: 'Managers',
  description: 'Group for managers'
};

iamAccessGroupsService.createAccessGroup(params)
  .then(res => {
    testGroupId = res.result.id;
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: javascript}
{: codeblock}

```python
group = iam_access_groups_service.create_access_group(
  account_id=test_account_id,
  name='Managers',
  description='Group for managers'
).get_result()

print(json.dumps(group, indent=2))
```
{: python}
{: codeblock}

```go
createAccessGroupOptions := iamAccessGroupsService.NewCreateAccessGroupOptions(testAccountID, "Managers")
createAccessGroupOptions.SetDescription("Group for managers")
group, response, err := iamAccessGroupsService.CreateAccessGroup(createAccessGroupOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(group, "", "  ")
fmt.Println(string(b))
```
{: go}
{: codeblock}

A unique name is required to differentiate access groups in the account.
{: note}

## Creating an access group by using Terraform
{: #create-ag-terraform}
{: terraform}

Use the following steps to create access groups by using Terraform:

1. Create an argument in your `main.tf` file. The following example creates an access group by using the `ibm_iam_access_group` resource, where `name` is a unique name to identify the access group.

   ```terraform
   resource "ibm_iam_access_group" "accgrp" {
    name        = "test"
    description = "New access group"
   }
   ```
   {: codeblock}

   You can also specify the description of the access group on the `description` option. For more information, see the argument reference details on the [Terraform Identity and Access Management (IAM)](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_access_group){: external} page.

1. After you finish building your configuration file, initialize the Terraform CLI. For more information, see [Initializing Working Directories](https://www.terraform.io/cli/init){: external}.

   ```terraform
   terraform init
   ```
   {: pre}

1. Provision the resources from the `main.tf` file. For more information, see [Provisioning Infrastructure with Terraform](https://www.terraform.io/cli/run){: external}.

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

## Assigning access to a group in the console
{: #access_ag}
{: ui}

After you set up your group with users and service IDs, you can assign a common access policy to the group. Remember, any policy that you set for the group applies to all entities within the group.

Assigning an access group Administrator access on **All Identity and Access enabled services** and **All Account Management services** includes the ability to revoke access for other users with the administrator role by removing them from the group.
{: important}

Use the following steps to assign access to a group in the console:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Access Groups**.
1. For the group that you want to assign access, select the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions"), and click **Assign access**.
1. You can assign access to only resources that you manage. You must assign at least one access option. For any access options that you don't add and configure, the default value of **No access** is assigned. Depending on the options that you are authorized to manage, you can assign the following types of access:

     * A group of services, like **All Identity and Access enabled services**, **All Account Management services**, or **All IAM Account Management services**.
     * A specific service

1. Next, you can scope the access to all resources or specific resources based on selected resource attributes like access management tags, location, or resource group.
1. Select all roles that apply. To view what actions are mapped to each role, click the numbers listed next to each role. Some services support the use of advanced operators to grant access to resources that satisfy specific naming conventions. See [Assigning access by using wildcard policies](/docs/account?topic=account-wildcard) for more information.
1. Click **Review**.
1. Click **Add** to add your policy configuration to your policy summary.
1. Click **Assign**.

You can also assign access by using access management tags. For more information, see [Controlling access to resources by using tags](/docs/account?topic=account-access-tags-tutorial).
{: tip}

## Assigning access to a group by using the CLI
{: #access_ag_cli}
{: cli}

To create an access group policy by using the CLI, you can use the [ibmcloud iam access-group-policy-create](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_access_group_policy_create) command.

```bash
ibmcloud iam access-group-policy-create GROUP_NAME {-f, --file @JSON_FILE | --roles ROLE_NAME1,ROLE_NAME2... [--service-name SERVICE_NAME] [--service-instance SERVICE_INSTANCE] [--region REGION] [--resource-type RESOURCE_TYPE] [--resource RESOURCE] [--resource-group-name RESOURCE_GROUP_NAME] [--resource-group-id RESOURCE_GROUP_ID]}
```
{: codeblock}

## Assigning access to a group by using the API
{: #access_ag_api}
{: api}

You can programmatically assign access to a group by calling the [{{site.data.keyword.iamlong}} (IAM) Policy Management API](/apidocs/iam-policy-management#create-policy){: external} as shown in the following sample request. The example assigns an access group `Editor` role for an instance of a service:

```bash
curl -X POST 'https://iam.cloud.ibm.com/v1/policies' \
-H 'Authorization: Bearer $TOKEN' \
-H 'Content-Type: application/json' \
-d '{
  "type": "access",
  "description": "Editor role for SERVICE_NAME's RESOURCE_NAME",
  "subjects": [
    {
      "attributes": [
        {
          "name": "access_group_id",
          "value": "exampleAccessGroupId"
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
{: curl}
{: codeblock}

```java
SubjectAttribute subjectAttribute = new SubjectAttribute.Builder()
        .name("access_group_id")
        .value(exampleAccessGroupId)
        .build();

PolicySubject policySubjects = new PolicySubject.Builder()
        .addAttributes(subjectAttribute)
        .build();

PolicyRole policyRoles = new PolicyRole.Builder()
        .roleId("crn:v1:bluemix:public:iam::::role:Editor")
        .build();

ResourceAttribute accountIdResourceAttribute = new ResourceAttribute.Builder()
        .name("accountId")
        .value(exampleAccountId)
        .operator("stringEquals")
        .build();

ResourceAttribute serviceNameResourceAttribute = new ResourceAttribute.Builder()
        .name("serviceType")
        .value("service")
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
        name: 'access_group_id',
        value: exampleAccessGroupId,
      },
    ],
  },
];
const policyRoles = [
  {
    role_id: 'crn:v1:bluemix:public:iam::::role:Editor',
  },
];
const accountIdResourceAttribute = {
  name: 'accountId',
  value: exampleAccountId,
  operator: 'stringEquals',
};
const serviceNameResourceAttribute = {
  name: 'serviceType',
  value: 'service',
  operator: 'stringEquals',
};
const policyResources = [
  {
    attributes: [accountIdResourceAttribute, serviceNameResourceAttribute],
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
  attributes=[SubjectAttribute(name='access_group_id', value=exampleAccessGroupId)])
policy_roles = PolicyRole(
  role_id='crn:v1:bluemix:public:iam::::role:Editor')
account_id_resource_attribute = ResourceAttribute(
  name='accountId', value=example_account_id)
service_name_resource_attribute = ResourceAttribute(
  name='serviceType', value='service')
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
  Name:  core.StringPtr("access_group_id"),
  Value: &exampleAccessGroupId,
}
policySubjects := &iampolicymanagementv1.PolicySubject{
  Attributes: []iampolicymanagementv1.SubjectAttribute{*subjectAttribute},
}
policyRoles := &iampolicymanagementv1.PolicyRole{
  RoleID: core.StringPtr("crn:v1:bluemix:public:iam::::role:Editor"),
}
accountIDResourceAttribute := &iampolicymanagementv1.ResourceAttribute{
  Name:     core.StringPtr("accountId"),
  Value:    core.StringPtr(exampleAccountID),
  Operator: core.StringPtr("stringEquals"),
}
serviceNameResourceAttribute := &iampolicymanagementv1.ResourceAttribute{
  Name:     core.StringPtr("serviceType"),
  Value:    core.StringPtr("service"),
  Operator: core.StringPtr("stringEquals"),
}
policyResources := &iampolicymanagementv1.PolicyResource{
  Attributes: []iampolicymanagementv1.ResourceAttribute{
    *accountIDResourceAttribute, *serviceNameResourceAttribute}
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

You can assign access to a group of services. To assign access to **All Identity and Access Enabled services**, specify `serviceType` for the `name` attribute, and use the `value` `service`. To assign access to **All Account Management services**, specify `serviceType` for the `name` attribute, and use the `value` `platform_service`. To assign access to the subset of account management services **All IAM Account Management services**, specify `service_group_id` for the `name` attribute, and use the `value` `IAM`.
{: tip}

## Assigning access to a group by using Terraform
{: #access_ag_terraform}
{: terraform}

After you set up your group, use the following steps to assign access to it by using Terraform.

1. Create an argument in your `main.tf` file. The following examples create an IAM policy that grants members of the access group the IAM `Viewer` platform role to all IAM-enabled services by using the `ibm_iam_access_group_policy` resource. You must have an existing IAM ID of an access group in order to complete the task.

   ```terraform
   resource "ibm_iam_access_group" "accgrp" {
    name = "test"
   }
   ```
   {: codeblock}

   ```terraform
   resource "ibm_iam_access_group_policy" "policy" {
    access_group_id = ibm_iam_access_group.accgrp.id
    roles           = ["Viewer"]
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Identity and Access Management (IAM)](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_access_group_policy){: external} page.

1. After you finish building your configuration file, initialize the Terraform CLI. For more information, see [Initializing Working Directories](https://www.terraform.io/cli/init){: external}.

   ```terraform
   terraform init
   ```
   {: pre}

1. Provision the resources from the `main.tf` file. For more information, see [Provisioning Infrastructure with Terraform](https://www.terraform.io/cli/run){: external}.

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
