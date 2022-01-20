---

copyright:

  years: 2018, 2022

lastupdated: "2022-01-20"

keywords: tagging, enabling others to tag, tagging permissions

subcollection: account

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}
{:codeblock: .codeblock}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Granting users access to tag resources
{: #access}

As the account owner, you might want to delegate some of the responsibility of tagging resources. For users to attach tags to a resource, you must grant them the appropriate access. Use {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) access policies to grant users access to resources in a resource group. Use Cloud Foundry roles to grant users access to resources in a Cloud Foundry org and space.
{: shortdesc}

Tags are visible account-wide and can be replicated across geographic regions. Since tags are not regulated information, avoid creating tags that use personal information, such as your name, address, phone number, email address, or other identifying or proprietary information.
{: important}

## Tagging permissions
{: #tagging-permissions}

Any user in an account can view tags. When a resource is tagged, all users who have read access to the resource can view the tag. To attach or detach a tag on a resource, certain access roles or permissions are needed depending on the resource type and tag type. See the following table to understand what role is needed for each resource type.


| Resource type | Role |
|--------|---------------|
| IAM-enabled | To attach or detach user tags, editor or administrator on the resource \n To attach or detach access management tags, administrator on the resource \n To view the assigned policies on the resource that has an access management tag that is attached, viewer role |
| Cloud Foundry | Developer on the space that the resource belongs to  |
| Bare metal on classic infrastructure| View hardware details and access to a specific set of services or all bare metal servers |
| Dedicated Hosts on classic infrastructure | View virtual dedicated host details and access to a specific set of services or all dedicated hosts |
| Virtual Server on classic infrastructure | View virtual server details and access to a specific set of services or all virtual servers |
| Cloud Object Storage S3 on classic infrastructure | Storage manage permission |
| File Storage on classic infrastructure | Storage manage permission |
| Evault backup on classic infrastructure | Storage manage permission |
| Content Delivery Network on classic infrastructure | Manage CDN account permission |
| Direct Link on classic infrastructure | Account member |
| Hardware Firewall | Manage Firewalls |
| FortiGate Security Appliance | Manage Firewalls |
| IBM Cloud Load Balancer | Manage Load Balancers |
| Gateway Appliance | Manage Network Gateways |
{: caption="Table 1. Required roles for attaching and detaching tags" caption-side="top"}
{: summary="This is a simple data table."}


## Granting users access to tag IAM-enabled resources
{: #iam-managed}
{: ui}

Complete the following steps to assign the editor role for a user to tag IAM-enabled resources: 

1. From the {{site.data.keyword.Bluemix_notm}} console, click **Manage > Access (IAM)**, and select **Access groups**.
2. Click **Create**.
3. Enter a group name and description, and click **Create**.
4. Add users to the access group by clicking **Add users**, selecting one or more users from the table, and clicking **Add to group**.
5. Click **Access policies** > **Assign access**.
6. Select **All Identity and Access enabled services** or a specific service as the type of access to assign.
7. Select a specific region or accept the default **All regions** option. 
8. Select **Editor** from the list of platform access roles, and click **Add**.
9. Review your access summary, and click **Assign**. 

## Granting users access to tag IAM-enabled resources by using the API
{: #iam-managed-api}
{: api}

To assign the editor role for a user to tag IAM-enabled resources, call the [IAM Policy Management API](https://cloud.ibm.com/apidocs/iam-policy-management){: external} as shown in the following example request. Replace variables with your target service and resource name. 
```bash
curl -X POST 'https://iam.test.cloud.ibm.com/v1/policies' -H 'Authorization: Bearer $TOKEN' -H 'Content-Type: application/json' -d '{
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
{: codeblock}
{: javascript}

```python
policy_subjects = PolicySubject(
                attributes=[SubjectAttribute(name='iam_id', value=example_user_id)])
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
{: codeblock}
{: go}

## Granting users access to tag Cloud Foundry resources
{: #cf_tag_access}
{: ui}

Complete the following steps to assign the developer space role for a user to tag Cloud Foundry resources:

1. Click **Manage > Access (IAM)**, and select **Users**.
2. Click the user's name from the table.
3. Click **Cloud Foundry access** > **Assign organization**.
4. Select the organization that contains the service instance you want to provide the user access to.
5. Select a specific location. 
6. Select **Developer** as the space role.
7. Click **Save role**.

## Granting users access to tag Cloud Foundry resources by using the API
{: #cf_tag_access-api}
{: api}

To assign the developer space role for a user to tag Cloud Foundry resources, call the [Cloud Controller API](http://v3-apidocs.cloudfoundry.org/version/3.97.0/index.html#create-a-role){: external} as shown in the following examples. 

1. Add the target user to the organization if they are not in it already. 

   ```bash
   curl “https://api.example.org/v3/roles” 
    -X POST 
    -H “Authorization: bearer <token>” 
    -H “Content-type: application/json” 
    -d ‘{
    “type”: “organization_user”,
    “relationships”: {
      “user”: {
      “data”: {
        “guid”: “<user_guid>”
      }
      },
      “organization”: {
      “data”: {
        “guid”: “<org_guid>”
      }
      }
    }’
   ```
   {: codeblock}
   {: curl}

1. Assign the target user the Space Developer role in the organizaiton.

   ```bash
   curl “https://api.example.org/v3/roles” 
    -X POST 
    -H “Authorization: bearer <token>” 
    -H “Content-type: application/json” 
    -d ‘{
    “type”: “space_developer”,
    “relationships”: {
      “user”: {
      “data”: {
        “guid”: “<user_guid>”
      }
      },
      “space”: {
      “data”: {
        “guid”: “<space_guid>”
      }
      }
    }
    }’
   ```
   {: codeblock}
   {: curl}

## Granting users access to tag classic infrastructure resources
{: #classic-infra}
{: ui}

The taggable resources for classic infrastructure are Virtual Guest, Virtual Dedicated Host, Network Application Delivery Controller, Gateway Member, Subnet, VLAN, and VLAN Firewall (Dedicated). Complete the following steps to assign the Manager service access role for a user to tag classic infrastructure services:

1. Click **Manage > Access (IAM)**, and select **Users**.
2. Click the user's name from the table.
3. Click **Classic infrastructure**
4. From the **Permissions** tab, expand the **Devices** category.
5. Select **View Hardware Details** and **View Virtual Server Details**. If you need to assign access to Cloud Object Storage S3, File Storage, or Evault Backup, assign the **Storage manage** permission. If you need to assign access to Content Delivery Network, assign the **Manage CDN Account** permission.
6. Click **Save**.
7. Click the **Devices** tab.
8. Select **All bare metal servers** or **All virtual servers**. Your selection depends on the resource that you want the user to be able to tag.
