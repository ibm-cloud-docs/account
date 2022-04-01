---

copyright:
  years: 2020, 2021
lastupdated: "2022-02-18"

keywords: catalog, private catalogs, IAM access, roles, private catalog service, access groups, permissions, IAM, catalog management, access group

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Assigning access to catalogs
{: #catalog-access}

As the account owner, you assign users specific catalog management access depending on what tasks they are performing. To streamline the process of assigning access, you can use access groups to organize a set of users into a single entity. That way, you can assign a single policy to the group one time, and then add or remove users from the group as needed. 
{: shortdesc}

For more details, see [Managing access in {{site.data.keyword.cloud_notm}}](/docs/account?topic=account-cloudaccess).

## Setting up your access groups in the console
{: #catalog-access-groups-console}
{: ui}

See the following sections for details about creating your access groups and assigning specific IAM policies to each one.

### Administrator access in the console
{: #catalog-access-console-admin}
{: ui}

Administrator access is required for setting account-level filters to the {{site.data.keyword.cloud_notm}} catalog.   

1. Log in to your {{site.data.keyword.cloud_notm}} account.
2. Go to **Manage** > **Access (IAM)** > **Access groups** in the {{site.data.keyword.cloud_notm}} console.
3. Click **Create**.
4. Enter `private-catalog-admins` as the group name, and click **Create**. 
5. Click **Access policies** > **Assign access**.
6. Select **Account management**.
7. Select **Catalog Management** from the **What type of access do you want to assign?** list.
8. Select the catalog that you want users to access.
9. In the Platform access section, select the **Administrator** role.
10. Click **Add** > **Assign**.

### Editor access in the console
{: #catalog-access-console-editor}
{: ui}

Editor access is required for creating private catalogs, setting filters at the private catalog level, adding your software to your private catalog, and updating, deprecating, and restoring your software.    

1. Go to **Access groups**, and click **Create**.
2. Enter `private-catalog-editors` as the group name, and click **Create**.
3. Click **Access policies** > **Assign access**.
4. Select **Account management**.
5. Select **Catalog Management** from the **What type of access do you want to assign?** list.
6. Select the catalog that you want users to access.
7. In the Platform access section, select the **Editor** role.
8. Click **Add**.
9. Select **IAM services** > **Kubernetes Service**.
10. Select your cluster, and then select the **Administrator** and **Manager** roles.
11. Click **Add**.
12. Select **IAM services** > **Schematics**.
13. Select the **Manager** role.
14. Click **Add** > **Assign**.

### Viewer access in the console
{: #catalog-access-console-viewer}
{: ui}

Viewer access is required for viewing private catalogs, the filtered {{site.data.keyword.cloud_notm}} catalog, and the filter settings.  

1. Go to **Access groups**, and click **Create**.
2. Enter `private-catalog-viewers` as the group name, and click **Create**.
3. Click **Access policies** > **Assign access**.
4. Select **Account management**.
5. Select **Catalog Management** from the **What type of access do you want to assign?** list.
6. Select the catalog that you want users to access.
7. In the Platform access section, select the **Viewer** role.
8. Click **Add** > **Assign**.

You also need to have viewer access on the resource group to which your private catalog is assigned. You can assign your private catalog to a resource group when you complete the steps for creating your private catalog. For more information, see [Customizing the IBM Cloud catalog for all account users](/docs/account?topic=account-filter-account). 

To assign viewer access to your private catalog's resource group, use the following steps:

1. Go to **Users** and select the user. 
1. Select **Access policies** > **Assign access**. 
1. From the **Assign users additional access** section, select **IAM services**.  
1. Select **All Identity and Access enabled services** and your private catalogs resource group from the **What type of access do you want to assign?** list.
1. In the Platform access section, select the **Viewer** role.
1. Click **Add** > **Assign**.

## Add users to your access groups in the console
{: #catalog-access-console-users}
{: ui}

After you set up your access groups, complete the following steps to add users to the groups:

1. Go to **Users**, and click **Invite users**.
2. Specify the email addresses of the users. If you are inviting more than one user with a single invitation, they are all assigned the same access.
3. Select one of the three access groups you previously created, and click **Add** > **Invite**.
4. Repeat the steps to add users to your other access groups. 

## Setting up your access groups by using the CLI
{: #catalog-access-groups-cli}
{: cli}

To assign access, run the [`ibmcloud iam user-policy-create`](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_user_policy_create) command. 

### Administrator access by using the CLI
{: #catalog-access-cli-admin}
{: cli}

Run the following command to assign administrator access:

```bash
ibmcloud iam user-policy-create USER_NAME --roles Administrator --service-name globalcatalog-collection
```
{: codeblock}

### Editor access by using the CLI
{: #catalog-access-cli-editor}
{: cli}

Run the following command to assign editor access:

```bash
ibmcloud iam user-policy-create USER_NAME --roles Editor --service-name globalcatalog-collection
```
{: codeblock}

### Viewer access by using the CLI
{: #catalog-access-cli-viewer}
{: cli}

Run the following command to set viewer access:

```bash
ibmcloud iam user-policy-create USER_NAME --roles Viewer --service-name globalcatalog-collection
```
{: codeblock}

## Add users to your access groups by using the CLI
{: #catalog-access-cli-users}
{: cli}

To add users to an access group by using the CLI, run the [`ibmcloud iam access-group-user-add`](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_access_group_user_add) command.

```bash
ibmcloud iam access-group-user-add GROUP_NAME USER_NAME [USER_NAME2...]
```
{: codeblock}

For example the following command adds user `name@example.com` to the `example_group` access group.

```bash
ibmcloud iam access-group-user-add example_group name@example.com
```
{: codeblock}


## Setting up your access groups by using the API
{: #catalog-access-groups-api}
{: api}

To assign access, call the [IAM Policy Management API](https://cloud.ibm.com/apidocs/iam-policy-management?code=go#create-policy) as shown in the follwing example. Replace the `role_id` vaiable with the role you want to assign: `Viewer`, `Editor`, or `Administrator`. 

```bash
curl -X POST 'https://iam.cloud.ibm.com/v1/policies' -H 'Authorization: Bearer $TOKEN' -H 'Content-Type: application/json' -d '{
  "type": "access",
  "description": "Editor role for SERVICE_NAME RESOURCE_NAME",
  "subjects": [
    {
      "attributes": [
        {
          "name": "iam_id",
          "value": "IBMid-123453user"
        }
      ]
    }
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
{: curl}

```java
SubjectAttribute subjectAttribute = new SubjectAttribute.Builder()
        .name("iam_id")
        .value(EXAMPLE_USER_ID)
        .build();

PolicySubject policySubjects = new PolicySubject.Builder()
        .addAttributes(subjectAttribute)
        .build();

PolicyRole policyRoles = new PolicyRole.Builder()
        .roleId("crn:v1:bluemix:public:iam::::role:Viewer")
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

ResourceTag policyResourceTag = new ResourceTag.Builder()
        .name("project")
        .value("prototype")
        .operator("stringEquals")
        .build();

PolicyResource policyResources = new PolicyResource.Builder()
        .addAttributes(accountIdResourceAttribute)
        .addAttributes(serviceNameResourceAttribute)
        .addTags(policyResourceTag)
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
{: codeblock}
{: java}

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
    role_id: 'crn:v1:bluemix:public:iam::::role:Viewer',
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
const policyResourceTag = {
  name: 'project',
  operator: 'stringEquals',
  value: 'prototype',
};
const policyResources = [
  {
    attributes: [accountIdResourceAttribute, serviceNameResourceAttribute],
    tags: [policyResourceTag],
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
{: codeblock}
{: javascript}

```python
policy_subjects = PolicySubject(
  attributes=[SubjectAttribute(name='iam_id', value=example_user_id)])
policy_roles = PolicyRole(
  role_id='crn:v1:bluemix:public:iam::::role:Viewer')
account_id_resource_attribute = ResourceAttribute(
  name='accountId', value=example_account_id)
service_name_resource_attribute = ResourceAttribute(
  name='serviceType', value='service')
policy_resource_tag = ResourceTag(
  name='project', value='prototype')
policy_resources = PolicyResource(
  attributes=[account_id_resource_attribute,
        service_name_resource_attribute],
  tags=[policy_resource_tag])

policy = iam_policy_management_service.create_policy(
  type='access',
  subjects=[policy_subjects],
  roles=[policy_roles],
  resources=[policy_resources]
).get_result()

print(json.dumps(policy, indent=2))
```
{: codeblock}
{: python}

```go
subjectAttribute := &iampolicymanagementv1.SubjectAttribute{
  Name:  core.StringPtr("iam_id"),
  Value: &exampleUserID,
}
policySubjects := &iampolicymanagementv1.PolicySubject{
  Attributes: []iampolicymanagementv1.SubjectAttribute{*subjectAttribute},
}
policyRoles := &iampolicymanagementv1.PolicyRole{
  RoleID: core.StringPtr("crn:v1:bluemix:public:iam::::role:Viewer"),
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
policyResourceTag := &iampolicymanagementv1.ResourceTag{
  Name:     core.StringPtr("project"),
  Value:    core.StringPtr("prototype"),
  Operator: core.StringPtr("stringEquals"),
}
policyResources := &iampolicymanagementv1.PolicyResource{
  Attributes: []iampolicymanagementv1.ResourceAttribute{
    *accountIDResourceAttribute, *serviceNameResourceAttribute},
  Tags: []iampolicymanagementv1.ResourceTag{*policyResourceTag},
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
{: codeblock}
{: go}

### Expected response
{: #expected-response-access}

```bash
{
  "id": "12345678-abcd-1a2b-a1b2-1234567890ab",
  "type": "access",
  "description": "Viewer role access for all instances of SERVICE_NAME in the account.",
  "subjects": [
    {
      "attributes": [
        {
          "name": "iam_id",
          "value": "IBMid-123453user"
        }
      ]
    }
  ],
  "roles": [
    {
      "roles_id": "crn:v1:bluemix:public:iam::::role:Viewer"
    }
  ],
  "resources": [
    {
      "attributes": [
        {
          "name": "accountId",
          "value": "ACCOUNT_ID",
          "operator": "stringEquals"
        },
        {
          "name": "serviceName",
          "value": "SERVICE_NAME",
          "operator": "stringEquals"
        }
      ]
    },
    {
      "tags": [
        {
          "name": "project",
          "value": "moonshot",
          "operator": "stringEquals"
        },
        {
          "name": "pipeline",
          "value": "test",
          "operator": "stringEquals"
        }
      ]
    }
  ],
  "href": "https://iam.cloud.ibm.com/v1/policies/12345678-abcd-1a2b-a1b2-1234567890ab",
  "created_at": "2018-08-30T14:09:09.907Z",
  "created_by_id": "USER_ID",
  "last_modified_at": "2018-08-30T14:09:09.907Z",
  "last_modified_by_id": "USER_ID",
  "state": "active"
}
```
{: codeblock}
{: curl}

```java
{
  "id": "12345678-abcd-1a2b-a1b2-1234567890ab",
  "type": "access",
  "description": "Viewer role access for all instances of SERVICE_NAME in the account.",
  "subjects": [
    {
      "attributes": [
        {
          "name": "iam_id",
          "value": "IBMid-123453user"
        }
      ]
    }
  ],
  "roles": [
    {
      "roles_id": "crn:v1:bluemix:public:iam::::role:Viewer"
    }
  ],
  "resources": [
    {
      "attributes": [
        {
          "name": "accountId",
          "value": "ACCOUNT_ID",
          "operator": "stringEquals"
        },
        {
          "name": "serviceName",
          "value": "SERVICE_NAME",
          "operator": "stringEquals"
        }
      ]
    },
    {
      "tags": [
        {
          "name": "project",
          "value": "moonshot",
          "operator": "stringEquals"
        },
        {
          "name": "pipeline",
          "value": "test",
          "operator": "stringEquals"
        }
      ]
    }
  ],
  "href": "https://iam.cloud.ibm.com/v1/policies/12345678-abcd-1a2b-a1b2-1234567890ab",
  "created_at": "2018-08-30T14:09:09.907Z",
  "created_by_id": "USER_ID",
  "last_modified_at": "2018-08-30T14:09:09.907Z",
  "last_modified_by_id": "USER_ID",
  "state": "active"
}
```
{: codeblock}
{: java}

```javascript
{
  "id": "12345678-abcd-1a2b-a1b2-1234567890ab",
  "type": "access",
  "description": "Viewer role access for all instances of SERVICE_NAME in the account.",
  "subjects": [
    {
      "attributes": [
        {
          "name": "iam_id",
          "value": "IBMid-123453user"
        }
      ]
    }
  ],
  "roles": [
    {
      "roles_id": "crn:v1:bluemix:public:iam::::role:Viewer"
    }
  ],
  "resources": [
    {
      "attributes": [
        {
          "name": "accountId",
          "value": "ACCOUNT_ID",
          "operator": "stringEquals"
        },
        {
          "name": "serviceName",
          "value": "SERVICE_NAME",
          "operator": "stringEquals"
        }
      ]
    },
    {
      "tags": [
        {
          "name": "project",
          "value": "moonshot",
          "operator": "stringEquals"
        },
        {
          "name": "pipeline",
          "value": "test",
          "operator": "stringEquals"
        }
      ]
    }
  ],
  "href": "https://iam.cloud.ibm.com/v1/policies/12345678-abcd-1a2b-a1b2-1234567890ab",
  "created_at": "2018-08-30T14:09:09.907Z",
  "created_by_id": "USER_ID",
  "last_modified_at": "2018-08-30T14:09:09.907Z",
  "last_modified_by_id": "USER_ID",
  "state": "active"
}
```
{: codeblock}
{: javascript}

```python
{
  "id": "12345678-abcd-1a2b-a1b2-1234567890ab",
  "type": "access",
  "description": "Viewer role access for all instances of SERVICE_NAME in the account.",
  "subjects": [
    {
      "attributes": [
        {
          "name": "iam_id",
          "value": "IBMid-123453user"
        }
      ]
    }
  ],
  "roles": [
    {
      "roles_id": "crn:v1:bluemix:public:iam::::role:Viewer"
    }
  ],
  "resources": [
    {
      "attributes": [
        {
          "name": "accountId",
          "value": "ACCOUNT_ID",
          "operator": "stringEquals"
        },
        {
          "name": "serviceName",
          "value": "SERVICE_NAME",
          "operator": "stringEquals"
        }
      ]
    },
    {
      "tags": [
        {
          "name": "project",
          "value": "moonshot",
          "operator": "stringEquals"
        },
        {
          "name": "pipeline",
          "value": "test",
          "operator": "stringEquals"
        }
      ]
    }
  ],
  "href": "https://iam.cloud.ibm.com/v1/policies/12345678-abcd-1a2b-a1b2-1234567890ab",
  "created_at": "2018-08-30T14:09:09.907Z",
  "created_by_id": "USER_ID",
  "last_modified_at": "2018-08-30T14:09:09.907Z",
  "last_modified_by_id": "USER_ID",
  "state": "active"
}
```
{: codeblock}
{: python}

```go
{
  "id": "12345678-abcd-1a2b-a1b2-1234567890ab",
  "type": "access",
  "description": "Viewer role access for all instances of SERVICE_NAME in the account.",
  "subjects": [
    {
      "attributes": [
        {
          "name": "iam_id",
          "value": "IBMid-123453user"
        }
      ]
    }
  ],
  "roles": [
    {
      "roles_id": "crn:v1:bluemix:public:iam::::role:Viewer"
    }
  ],
  "resources": [
    {
      "attributes": [
        {
          "name": "accountId",
          "value": "ACCOUNT_ID",
          "operator": "stringEquals"
        },
        {
          "name": "serviceName",
          "value": "SERVICE_NAME",
          "operator": "stringEquals"
        }
      ]
    },
    {
      "tags": [
        {
          "name": "project",
          "value": "moonshot",
          "operator": "stringEquals"
        },
        {
          "name": "pipeline",
          "value": "test",
          "operator": "stringEquals"
        }
      ]
    }
  ],
  "href": "https://iam.cloud.ibm.com/v1/policies/12345678-abcd-1a2b-a1b2-1234567890ab",
  "created_at": "2018-08-30T14:09:09.907Z",
  "created_by_id": "USER_ID",
  "last_modified_at": "2018-08-30T14:09:09.907Z",
  "last_modified_by_id": "USER_ID",
  "state": "active"
}
```
{: codeblock}
{: go}

## Add users to your access groups by using the API
{: #catalog-access-api-users}
{: api}

To add users to an access group by using the API, call the [IAM Access Groups API](https://cloud.ibm.com/apidocs/iam-access-groups#add-members-to-access-group) as shown in the following example.

```bash
curl -X PUT -H "Authorization: {iam_token}" -H "Accept: application/json" -H "Content-Type: application/json" -d '{"members": [ {"iam_id": "IBMid-user1", "type": "user"}, {"iam_id": "iam-ServiceId-123", "type": "service"} ]}' "{base_url}/groups/{access_group_id}/members"
```
{: codeblock}
{: curl}

```java
AddGroupMembersRequestMembersItem member1 = new AddGroupMembersRequestMembersItem.Builder()
  .iamId("IBMid-user1")
  .type("user")
  .build();
AddGroupMembersRequestMembersItem member2 = new AddGroupMembersRequestMembersItem.Builder()
  .iamId("iam-ServiceId-123")
  .type("service")
  .build();
AddMembersToAccessGroupOptions addMembersToAccessGroupOptions = new AddMembersToAccessGroupOptions.Builder()
  .accessGroupId(testGroupId)
  .addMembers(member1)
  .addMembers(member2)
  .build();
Response<AddGroupMembersResponse> response = service.addMembersToAccessGroup(addMembersToAccessGroupOptions).execute();
AddGroupMembersResponse addGroupMembersResponse = response.getResult();

System.out.println(addGroupMembersResponse);
```
{: codeblock}
{: java}

```javascript
const groupMember1 = {
  iam_id: 'IBMid-user1',
  type: 'user',
};
const groupMember2 = {
  iam_id: 'iam-ServiceId-123',
  type: 'service',
};
const params = {
  accessGroupId: testGroupId,
  members: [groupMember1, groupMember2],
};

iamAccessGroupsService.addMembersToAccessGroup(params)
  .then(res => {
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
member1 = AddGroupMembersRequestMembersItem(
  iam_id='IBMid-user1', type='user')
member2 = AddGroupMembersRequestMembersItem(
  iam_id='iam-ServiceId-123', type='service')
members = [member1, member2]

add_group_members_response = iam_access_groups_service.add_members_to_access_group(
  access_group_id=test_group_id,
  members=members
).get_result()

print(json.dumps(add_group_members_response, indent=2))
```
{: codeblock}
{: python}

```go
groupMembers := []iamaccessgroupsv2.AddGroupMembersRequestMembersItem{
  iamaccessgroupsv2.AddGroupMembersRequestMembersItem{
    IamID: core.StringPtr("IBMid-user1"),
    Type:  core.StringPtr("user"),
  },
  iamaccessgroupsv2.AddGroupMembersRequestMembersItem{
    IamID: core.StringPtr("iam-ServiceId-123"),
    Type:  core.StringPtr("service"),
  },
}
addMembersToAccessGroupOptions := iamAccessGroupsService.NewAddMembersToAccessGroupOptions(testGroupID)
addMembersToAccessGroupOptions.SetMembers(groupMembers)
addGroupMembersResponse, response, err := iamAccessGroupsService.AddMembersToAccessGroup(addMembersToAccessGroupOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(addGroupMembersResponse, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

### Expected response
{: #expected-response-api}

```bash
{
  "members": [
    {
      "iam_id": "$IBM_ID",
      "type": "user",
      "created_at": "2019-01-01T01:01:00Z",
      "created_by_id": "CREATOR_ID",
      "status_code": 200
    },
    {
      "iam_id": "$SERVICE_ID",
      "status_code": 400,
      "trace": "12345678-abcd-1a2b-a1b2-1234567890ab",
      "errors": [
        {
          "code": "error_occurred",
          "message": "The service id is missing or incorrect"
        }
      ]
    }
  ]
}
```
{: codeblock}
{: curl}

```java
{
  "members": [
    {
      "iam_id": "$IBM_ID",
      "type": "user",
      "created_at": "2019-01-01T01:01:00Z",
      "created_by_id": "CREATOR_ID",
      "status_code": 200
    },
    {
      "iam_id": "$SERVICE_ID",
      "status_code": 400,
      "trace": "12345678-abcd-1a2b-a1b2-1234567890ab",
      "errors": [
        {
          "code": "error_occurred",
          "message": "The service id is missing or incorrect"
        }
      ]
    }
  ]
}
```
{: codeblock}
{: java}

```javascript
{
  "members": [
    {
      "iam_id": "$IBM_ID",
      "type": "user",
      "created_at": "2019-01-01T01:01:00Z",
      "created_by_id": "CREATOR_ID",
      "status_code": 200
    },
    {
      "iam_id": "$SERVICE_ID",
      "status_code": 400,
      "trace": "12345678-abcd-1a2b-a1b2-1234567890ab",
      "errors": [
        {
          "code": "error_occurred",
          "message": "The service id is missing or incorrect"
        }
      ]
    }
  ]
}
```
{: codeblock}
{: javascript}

```python
{
  "members": [
    {
      "iam_id": "$IBM_ID",
      "type": "user",
      "created_at": "2019-01-01T01:01:00Z",
      "created_by_id": "CREATOR_ID",
      "status_code": 200
    },
    {
      "iam_id": "$SERVICE_ID",
      "status_code": 400,
      "trace": "12345678-abcd-1a2b-a1b2-1234567890ab",
      "errors": [
        {
          "code": "error_occurred",
          "message": "The service id is missing or incorrect"
        }
      ]
    }
  ]
}
```
{: codeblock}
{: python}

```go
{
  "members": [
    {
      "iam_id": "$IBM_ID",
      "type": "user",
      "created_at": "2019-01-01T01:01:00Z",
      "created_by_id": "CREATOR_ID",
      "status_code": 200
    },
    {
      "iam_id": "$SERVICE_ID",
      "status_code": 400,
      "trace": "12345678-abcd-1a2b-a1b2-1234567890ab",
      "errors": [
        {
          "code": "error_occurred",
          "message": "The service id is missing or incorrect"
        }
      ]
    }
  ]
}
```
{: codeblock}
{: go}

## Add users to your access groups by using Terraform
{: #catalog-access-terra-users}
{: terraform}

To add users to an access group by using Terraform, follow these steps:

1. In your Terraform configuration file, find the Terraform code that you used to [create the access group](/docs/account?topic=account-groups&interface=terraform#create-ag-terraform) and note the `access_group_id` assigned to your access group.
2. Add a member to the access group.
   ```terraform
   resource "ibm_iam_access_group_members" "accgroupmem" {
   access_group_id = ibm_iam_access_group.accgroup.id
   ibm_ids = ["test@in.ibm.com"]
   }
   ```
   {: codeblock}
   
   For more information, see the argument reference details on the [Terraform Identity and Access Management (IAM)](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_access_group_members){: external} page.
   
3. Initialize the Terraform CLI.
   ```terraform
   terraform init
   ```
   {: pre}
   
4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to update the access group.
   ```terraform
   terraform plan
   ```
   {: pre}

5. Update the access group.
   ```terraform
   terraform apply
   ```
   {: pre}

   