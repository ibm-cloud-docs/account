---

copyright:
  years: 2023, 2024
lastupdated: "2024-01-02"
keywords: access policy, access, policy, restriction, time based restriction, time based, time based conditions, conditions

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Limiting access with time-based conditions
{: #iam-time-based}

Set up time-based conditions to designate temporary access to resources in your account or allow access to resources during specific time windows. You can create time-based conditions that grant one-time temporary access for a specific time and date range, or you can set up recurring weekly access. For example, you might want to give a user access to account resources during only their working hours by specifying recurring access, or you might have a contractor or a user that needs to demo features of a service and they only need temporary access.
{: shortdesc}

Time-based conditions don't account for Daylight Saving Time (DST) changes for time zones that observe DST. Administrators must update the policies according to DST changes to accurately enforce time-based conditions. For example, the Eastern time zone is UTC-4 hours during Daylight Saving Time rather than -5 hours as it is during standard time. Standard time begins in November and ends in March, when DST begins.
{: important}

The {{site.data.keyword.containershort}} doesn't adhere to time-based conditions. For example, a policy with a time-based condition that grants access to All Identity and Access enabled services includes access to {{site.data.keyword.containershort}} resources. The subject of the policy has access to some {{site.data.keyword.containershort}} resources outside of the specified time-based condition.
{: preview}

Time-based conditions for access policies help you apply the principle of least privilege for assigning access and reduce the attack surface if a security breach occurs.

To review a user's access, see [Reviewing assigned access in the console](/docs/account?topic=account-assign-access-resources&interface=ui#review-your-access-console).
{: tip}

## Condition patterns
{: #condition-patterns}

The following patterns represent the allowed condition permutations:

| Pattern | Example |
|---------|---------|
| time-based-conditions:once | Temporary access on a specific day from 9 AM to 5 PM UTC-5. |
| time-based-conditions:weekly:all-day | Recurring access Mon-Fri UTC-5 all day. |
| time-based-conditions:weekly:custom-hours | Recurring access Mon-Fri 9 AM to 5 PM UTC-5. |
{: caption="Table 1. Allowed condition patterns for time-based conditions." caption-side="top"}

IAM prevents combining one-time temporary conditions with weekly recurring conditions in the same policy definition.
{: note}


## Before you begin
{: #before-you-begin-time-based-cli}
{: cli}

Make sure that you have the latest version of the {{site.data.keyword.cloud_notm}} CLI so that you can use conditions in your access policies.

To determine your {{site.data.keyword.cloud_notm}} CLI version, run the following command:

```bash
ibmcloud -v
```
{: codeblock}

You must use the latest version of the CLI. If you aren't using the latest version, run the following command to update your CLI:

```bash
ibmcloud update
```
{: codeblock}

If you are running the current release, the following output is displayed:

```bash
Checking for updates...
No update required. Your CLI is already up-to-date.
```
{: screen}

For more information, see [Installing the stand-alone IBM Cloud CLI](/docs/cli?topic=cli-install-ibmcloud-cli).

## Before you begin
{: #before-you-begin-time-based-api}
{: api}

Make sure that you call the `v2/policies` URI, which is `https://iam.coud.ibm.com/v2/policies`, so that you can use conditions in your access policies. For more information, see the [IAM Policy Management API](/apidocs/iam-policy-management) and [change log](/docs/account?topic=account-api-change-log).


## Creating a temporary time-based condition
{: #iam-time-based-temp-ui}
{: ui}

You can assign access for a finite duration by specifying a date and time range that determines when the condition grants and terminates access. For example, you might have a user that needs to present a demonstration on your account for a few hours or a contractor that needs temporary access to a service over a couple days.

Complete the following steps to assign an access policy with a temporary time-based condition:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)**
1. Select **Users**, **Trusted profiles**, **Service IDs**, or **Access groups**, depending on the entity to which you want to assign access.
1. Click the entity's name from the list and go to **Access**.
1. Click **Assign access**.
1. Select a service and click **Next**.
    * If you want the user to be able to create any service, select **All Identity and Access enabled services**.
    * If you want to assign the user access to a specific service, select it from the list.
1. Select the resource that you want to assign the user access to, or select All resources. Click **Next**.
1. (Optional) Select a resource group access role. Click **Next**.
1. Select any combination of service access and platform access roles, and click **Next**.
1. Click **Add condition** and select **One-time**.
1. Select the time zone.

As an example, let's say that you're creating a conditional policy for a developer that is based in Dublin. In this case, select `UTC+1` so that the date and time range that you select in the next step enforces access at the correct time for that location.
{: tip}

1. Complete the fields for the date and time range that that determines when the condition grants and terminates access.
1. Click **Create**.
1. Click **Review**.
1. Click **Add** to add your policy configuration to your policy summary.
1. Click **Assign**.

Temporary policies aren't automatically removed. To avoid reaching the policy limit in the account, administrators can remove the policy manually after it expires.
{: note}

For more information about time-based conditions for access policies, see [Conditions in access policies](/docs/account?topic=account-iam-condition-properties&interface=ui#policy-condition-properties).

## Creating a temporary time-based condition by using the CLI
{: #iam-time-based-temp-cli}
{: cli}

You can assign access for a finite duration by specifying a date and time range that determines when the condition grants and terminates access. For example, you might have a user that needs to present a demonstration on your account for a few hours or a contractor that needs temporary access to a service over a couple days.

The following example shows you how to create a one-time time-based condition for you account by granting the user temporary access as an Operator for all Account Management Services.

1. Log in to {{site.data.keyword.cloud}} CLI. If you have multiple accounts, you are prompted to select which account to use. If you do not specify a region with the `-r` flag, you must also select a region.

   ```bash
   ibmcloud login
   ```
   {: codeblock}

   If your credentials are rejected, you might be using a federated ID. To log in with a federated ID, use the `--sso` flag. See [Logging in with a federated ID](/docs/account?topic=account-federated_id) for more details.
   {: tip}

   If it's the first time you're using the {{site.data.keyword.cloud_notm}} CLI, check out the [getting started tutorial](/docs/cli?topic=cli-getting-started).
1. Create an access policy and assign it to a user or a service ID by using the command [**`ibmcloud iam user-policy-create`**](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_user_policy_create).
1. Assign access to **All Account Management services** with the `Operator` role:

   ```bash
   ibmcloud iam service-policy-create name@example.com --roles Administrator --account-management --api-version v2
   ```
   {: codeblock}

1. Use the following example of a temporary time-based access policy in JSON schema to create your own conditions:

    ```json
    {
      "type": "access",
      "description": "time-based conditions policy example restricting access to the full day of 2022-12-23 UTC",
      "control": {
        "grant": {
          "roles": [
            {
              "role_id": "crn:v1:bluemix:public:iam::::role:Operator"
            }
          ]
        }
      },
      "resource": {
        "attributes": [
          {
            "operator": "stringEquals",
            "value": "d4b763ad0cbd4dca8dd1edb427d7a77e",
            "key": "accountId"
          },
          {
            "value": "platform_service",
            "operator": "stringEquals",
            "key": "serviceType"
          }
        ]
      },
      "pattern": "time-based-conditions:once",
      "rule": {
        "operator": "and",
        "conditions": [
          {
            "key": "{{environment.attributes.current_date_time}}",
            "operator": "dateTimeGreaterThanOrEquals",
            "value": "2022-12-23T00:00:00+00:00"
          },
          {
            "key": "{{environment.attributes.current_date_time}}",
            "operator": "dateTimeLessThanOrEquals",
            "value": "2022-12-23T23:59:59+00:00"
          }
        ]
      },
      "subject": {
        "attributes": [
          {
            "key": "iam_id",
            "operator": "stringEquals",
            "value": "IBMid-550000HFVV"
          }
        ]
      }
    }
    ```
    {: codeblock}

Temporary policies, which use the pattern `time-based-conditions:once`, aren't automatically removed when they expire. To avoid reaching the policy limit in the account, administrators can remove the policy manually after it expires.
{: note}

For more information about time-based conditions for access policies, see [Conditions in access policies](/docs/account?topic=account-iam-condition-properties&interface=ui#policy-condition-properties).

## Creating a temporary time-based condition by using the API
{: #iam-time-based-temp-api}
{: api}

You can assign access for a finite duration by specifying a date and time range that determines when the condition grants and terminates access. For example, you might have a user that needs to present a demonstration on your account for a few hours or a contractor that needs temporary access to a service over a couple days.

The following examples show you how to create a one-time time-based condition for you account by granting the user temporary access as an Operator for all Account Management Services.

```go
	subjectAttribute := &iampolicymanagementv1.V2PolicyAttribute{
				Key:  core.StringPtr("iam_id"),
				Operator: core.StringPtr("stringEquals"),
				Value: &exampleUserID,
			}
			policySubject := &iampolicymanagementv1.V2PolicyBaseSubject{
				Attributes: []iampolicymanagementv1.V2PolicyAttribute{*subjectAttribute},
			}
			policyRole := &iampolicymanagementv1.PolicyRole{
				RoleID: core.StringPtr("crn:v1:bluemix:public:iam::::role:Operator"),
			}
			v2PolicyGrant := &iampolicymanagementv1.V2PolicyBaseControlGrant{
				Roles: []iampolicymanagementv1.PolicyRole{*policyRole},
			}
			v2PolicyControl := &iampolicymanagementv1.V2PolicyBaseControl{
				Grant: v2PolicyGrant,
			}
			accountIDResourceAttribute := &iampolicymanagementv1.V2PolicyAttribute{
				Key:     core.StringPtr("accountId"),
				Operator: core.StringPtr("stringEquals"),
				Value:    core.StringPtr(exampleAccountID),
			}
			serviceNameResourceAttribute := &iampolicymanagementv1.V2PolicyAttribute{
				Key:     core.StringPtr("serviceType"),
				Operator: core.StringPtr("stringEquals"),
				Value:    core.StringPtr("service"),
			}
			policyResource := &iampolicymanagementv1.V2PolicyBaseResource{
				Attributes: []iampolicymanagementv1.V2PolicyAttribute{
					*accountIDResourceAttribute, *serviceNameResourceAttribute},
			}

			startConditionAttribute :=  &iampolicymanagementv1.V2PolicyAttribute{
				Key:     core.StringPtr("{{environment.attributes.current_time}}"),
				Operator: core.StringPtr("dateTimeGreaterThanOrEquals"),
				Value:    core.StringPtr("2022-12-23T00:00:00+00:00"),
			}
			endConditionAttribute :=  &iampolicymanagementv1.V2PolicyAttribute{
				Key:     core.StringPtr("{{environment.attributes.current_time}}"),
				Operator: core.StringPtr("dateTimeLessThanOrEquals"),
				Value:    core.StringPtr("2022-12-23T23:59:59+00:00"),
			}
			policyRule := &iampolicymanagementv1.V2PolicyBaseRule{
				Operator: core.StringPtr("and"),
				Conditions: []iampolicymanagementv1.V2PolicyAttribute{
					*startConditionAttribute, *endConditionAttribute},
			}

			options := iamPolicyManagementService.NewV2CreatePolicyOptions(
				"access",
				v2PolicyControl,
			)
			options.SetSubject(policySubject)
			options.SetResource(policyResource)
			options.SetRule(policyRule)
			options.SetPattern(*core.StringPtr("time-based-conditions:once"))

			policy, response, err := iamPolicyManagementService.V2CreatePolicy(options)
			if err != nil {
				panic(err)
			}
			b, _ := json.MarshalIndent(policy, "", "  ")
			fmt.Println(string(b))
```
{: go}
{: codeblock}

```java
V2PolicyAttribute subjectAttribute = new V2PolicyAttribute.Builder()
              .key("iam_id")
              .value(EXAMPLE_USER_ID)
              .operator("stringEquals")
              .build();

      V2PolicyBaseSubject policySubject = new V2PolicyBaseSubject.Builder()
              .addAttributes(subjectAttribute)
              .build();

      V2PolicyAttribute accountIdResourceAttribute = new V2PolicyAttribute.Builder()
              .key("accountId")
              .value(exampleAccountId)
              .operator("stringEquals")
              .build();

      V2PolicyAttribute serviceNameResourceAttribute = new V2PolicyAttribute.Builder()
              .key("serviceName")
              .value("iam-groups")
              .operator("stringEquals")
              .build();

      V2PolicyBaseResource policyResource = new V2PolicyBaseResource.Builder()
              .addAttributes(accountIdResourceAttribute)
              .addAttributes(serviceNameResourceAttribute)
              .build();

      PolicyRole policyRoles = new PolicyRole.Builder()
              .roleId("crn:v1:bluemix:public:iam::::role:Operator")
              .build();

      V2PolicyBaseControlGrant policyGrant = new V2PolicyBaseControlGrant.Builder()
              .roles(Arrays.asList(policyRoles))
              .build();

      V2PolicyBaseControl policyControl = new V2PolicyBaseControl.Builder()
              .grant(policyGrant)
              .build();

      V2PolicyAttribute startConditionAttribute = new V2PolicyAttribute.Builder()
              .key("{{environment.attributes.current_time}}")
              .value("2022-12-23T00:00:00+00:00")
              .operator("dateTimeGreaterThanOrEquals")
              .build();

      V2PolicyAttribute endConditionAttribute = new V2PolicyAttribute.Builder()
              .key("{{environment.attributes.current_time}}")
              .value("2022-12-23T23:59:59+00:00")
              .operator("dateTimeLessThanOrEquals")
              .build();

      V2PolicyBaseRuleV2RuleWithConditions policyRule = new V2PolicyBaseRuleV2RuleWithConditions.Builder()
              .operator("and")
              .conditions(new ArrayList<V2PolicyAttribute>(Arrays.asList(startConditionAttribute, endConditionAttribute)))
              .build();

      V2CreatePolicyOptions options = new V2CreatePolicyOptions.Builder()
              .type("access")
              .subject(policySubject)
              .control(policyControl)
              .resource(policyResource)
              .rule(policyRule)
              .pattern("time-based-conditions:once")
              .build();

      Response<V2Policy> response = service.v2CreatePolicy(options).execute();
      V2Policy policy = response.getResult();
```
{: codeblock}
{: java}

```javascript
const policySubject = {
      attributes: [
        {
          key: 'iam_id',
          operator: 'stringEquals',
          value: exampleUserId,
        },
      ],
    };
    const policyResourceAccountAttribute = {
      key: 'accountId',
      value: exampleAccountId,
      operator: 'stringEquals',
    };
    const policyResourceServiceAttribute = {
      key: 'serviceName',
      operator: 'stringEquals',
      value: 'iam-groups',
    };
    const policyResource = {
      attributes: [policyResourceAccountAttribute, policyResourceServiceAttribute]
    };
    const policyControl = {
      grant: {
        roles: [{
          role_id: 'crn:v1:bluemix:public:iam::::role:Operator',
        }],
      }
    };
    const policyRule = {
      operator: 'and',
      conditions: [
          {
              key: '{{environment.attributes.current_time}}',
              operator: 'dateTimeGreaterThanOrEquals',
              value: '2022-12-23T00:00:00+00:00',
          },
          {
              key: '{{environment.attributes.current_time}}',
              operator: 'dateTimeLessThanOrEquals',
              value: '2022-12-23T23:59:59+00:00',
          },
      ],
    }
    const policyPattern = 'time-based-conditions:once'
    const params = {
      type: 'access',
      subject: policySubject,
      control: policyControl,
      resource: policyResource,
      rule: policyRule,
      pattern: policyPattern,
    };

    try {
      const res = await iamPolicyManagementService.v2CreatePolicy(params);
      examplePolicyId = res.result.id;
      console.log(JSON.stringify(res.result, null, 2));
    } catch (err) {
      console.warn(err)
    }
```
{: codeblock}
{: javascript}

```python
policy_subject = V2PolicyBaseSubject(
                attributes=[V2PolicyAttribute(key='iam_id', value=example_user_id, operator='stringEquals')]
            )
            policy_role = PolicyRole(role_id='crn:v1:bluemix:public:iam::::role:Operator')
            account_id_resource_attribute = V2PolicyAttribute(
                key='accountId', value=example_account_id, operator='stringEquals'
            )
            service_name_resource_attribute = V2PolicyAttribute(
                key='serviceType', value='service', operator='stringEquals'
            )
            policy_resource = PolicyResource(
                attributes=[account_id_resource_attribute, service_name_resource_attribute],
            )
            policy_control = V2PolicyBaseControl(grant=V2PolicyBaseControlGrant(roles=[policy_role]))
            policy_rule = V2PolicyBaseRuleV2RuleWithConditions(
                operator='and',
                conditions=[
                    V2PolicyAttribute(
                        key='{{environment.attributes.current_time}}',
                        operator='dateTimeGreaterThanOrEquals',
                        value='2022-12-23T00:00:00+00:00',
                    ),
                    V2PolicyAttribute(
                        key='{{environment.attributes.current_time}}',
                        operator='dateTimeLessThanOrEquals',
                        value='2022-12-23T23:59:59+00:00',
                    ),
                ],
            )
            policy_pattern = 'time-based-conditions:once'

            policy = iam_policy_management_service.v2_create_policy(
                type='access',
                subject=policy_subject,
                control=policy_control,
                resource=policy_resource,
                rule=policy_rule,
                pattern=policy_pattern,
            ).get_result()

            print(json.dumps(policy, indent=2))
```
{: codeblock}
{: python}

Temporary policies, which use the pattern `time-based-conditions:once`, aren't automatically removed. To avoid reaching the policy limit in the account, administrators can remove the policy manually after it expires.
{: note}

For more information about time-based conditions for access policies, see [Conditions in access policies](/docs/account?topic=account-iam-condition-properties&interface=ui#policy-condition-properties).

## Creating a temporary time-based condition by using Terraform
{: #iam-time-based-temp-terra}
{: terraform}

Before you can assign recurring access by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

You can assign access for a finite duration by specifying a date and time range that determines when the condition grants and terminates access. For example, you might have a user that needs to present a demonstration on your account for a few hours or a contractor that needs temporary access to a service over a couple days.

Complete the following steps to assign an access policy with a temporary time-based condition:

1. The following example configures a policy for a user with the Viewer role on the Kubernetes service. The policy grants access from 12 AM to 11:59 PM on on 12 December 2022.

    For more information about time-based conditions for access policies, see [Conditions in access policies](/docs/account?topic=account-iam-condition-properties&interface=ui#policy-condition-properties).

    ```terraform
    resource "ibm_iam_user_policy" "policy" {
      ibm_id = "test@in.ibm.com"
      roles      = ["Viewer"]
      resources {
        service = "kms"
      }
      rule_conditions {
        key = "{{environment.attributes.current_date_time}}"
        operator = "dateTimeGreaterThanOrEquals"
        value = ["2022-12-23T00:00:00+00:00"]
      }
      rule_conditions {
        key = "{{environment.attributes.current_date_time}}"
        operator = "dateTimeLessThanOrEquals"
        value = ["2022-12-23T23:59:59+00:00"]
      }
      rule_operator = "and"
      pattern = "time-based-conditions:once"
    }
    ```
    {: codeblock}

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


## Creating a recurring time-based condition
{: #iam-time-based-recur-ui}
{: ui}

You can assign recurring access at a weekly cadence. You might want to give users access to account resources during only their working hours.

Complete the following steps to assign an access policy with a recurring time-based condition:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)**
1. Select **Users**, **Trusted profiles**, **Service IDs**, or **Access groups**, depending on the entity to which you want to assign access.
1. Click the identity's name from the list and go to **Access**.
1. Click **Assign access**.
1. Select a service and click **Next**.
    * If you want the user to be able to create any service, select **All Identity and Access enabled services**.
    * If you want to assign the user access to a specific service, select it from the list.
1. Select the resource that you want to assign the user access to, or select All resources. Click **Next**.
1. (Optional) Select a resource group access role. Click **Next**.
1. Select any combination of service access and platform access roles, and click **Next**.
1. Click **Add condition** and select **Weekly**.
1. Select the time zone for the conditional policy.

As an example, let's say that you're creating a conditional policy for a developer that is based in Dublin. In this case, select `UTC+1` so that the date and time range that you select next is enforced at the correct time for that location.
{: tip}

1. Select the days of the week that you want the condition to grant access.
   * (Optional) Set the **All day** toggle to **No** to specify a timeframe for the days that you select.
1. Click **Create**.
1. Click **Review**.
1. Click **Add** to add your policy configuration to your policy summary.
1. Click **Assign**.

For more information about time-based conditions for access policies, see [Conditions in access policies](/docs/account?topic=account-iam-condition-properties&interface=ui#policy-condition-properties).


## Creating a recurring time-based condition by using the CLI
{: #iam-time-based-recur-cli}
{: cli}

You can assign recurring access at a weekly cadence. You might want to give users access to account resources during only their working hours.

The following example shows you how to create a recurring time-based condition for a user. The policy assigns access during working hours Monday through Friday as an Editor for all Account Management Services.

1. Log in to {{site.data.keyword.cloud}} CLI. If you have multiple accounts, you are prompted to select which account to use. If you do not specify a region with the `-r` flag, you must also select a region.

   ```bash
   ibmcloud login
   ```
   {: codeblock}

   If your credentials are rejected, you might be using a federated ID. To log in with a federated ID, use the `--sso` flag. See [Logging in with a federated ID](/docs/account?topic=account-federated_id) for more details.
   {: tip}

   If it's your first time using the {{site.data.keyword.cloud_notm}} CLI, check out the [getting started tutorial](/docs/cli?topic=cli-getting-started).
1. Create an access policy and assign it to a user or a service ID by using the command [**`ibmcloud iam user-policy-create`**](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_user_policy_create).
1. Assign access to **All Account Management services** with the `Editor` role:

   ```bash
   ibmcloud iam service-policy-create name@example.com --roles Editor --account-management --api-version v2
   ```
   {: codeblock}

1. Use the following example of a recurring weelky time-based policy in JSON schema to create your own conditions:

    ```json
    {
      "type": "access",
      "description": "time-based conditions policy example restricting access to the full day of 2022-12-23 UTC",
      "control": {
        "grant": {
          "roles": [
            {
              "role_id": "crn:v1:bluemix:public:iam::::role:Editor"
            }
          ]
        }
      },
      "resource": {
        "attributes": [
          {
            "operator": "stringEquals",
            "value": "d4b763ad0cbd4dca8dd1edb427d7a77e",
            "key": "accountId"
          },
          {
            "value": "platform_service",
            "operator": "stringEquals",
            "key": "serviceType"
          }
        ]
      },
      "pattern": "time-based-conditions:weekly",
      "rule": {
        "operator": "and",
        "conditions": [
          {
            "key": "{{environment.attributes.day_of_week}}",
            "operator": "dayOfWeekAnyOf",
            "value": [
              1,
              2,
              3,
              4,
              5
            ]
          },
          {
            "key": "{{environment.attributes.current_time}}",
            "operator": "timeGreaterThanOrEquals",
            "value": "00:00:00+00:00"
          },
          {
            "key": "{{environment.attributes.current_time}}",
            "operator": "timeLessThanOrEquals",
            "value": "23:59:59+00:00"
          }
        ]
      },
      "subject": {
        "attributes": [
          {
            "key": "iam_id",
            "operator": "stringEquals",
            "value": "IBMid-550000HFVV"
          }
        ]
      }
    }
    ```
    {: codeblock}

For more information about time-based conditions for access policies, see [Conditions in access policies](/docs/account?topic=account-iam-condition-properties&interface=ui#policy-condition-properties).

## Creating a recurring time-based condition by using the API
{: #iam-time-based-recur-api}
{: api}

You can assign recurring access at a weekly cadence. You might want to give users access to account resources during only their working hours.

The following examples show you how to create a recurring time-based condition for a user. The policy assigns access during working hours Monday through Friday as an Editor for all Account Management Services.

```go
subjectAttribute := &iampolicymanagementv1.V2PolicyAttribute{
				Key:  core.StringPtr("iam_id"),
				Operator: core.StringPtr("stringEquals"),
				Value: &exampleUserID,
			}
			policySubject := &iampolicymanagementv1.V2PolicyBaseSubject{
				Attributes: []iampolicymanagementv1.V2PolicyAttribute{*subjectAttribute},
			}
			policyRole := &iampolicymanagementv1.PolicyRole{
				RoleID: core.StringPtr("crn:v1:bluemix:public:iam::::role:Editor"),
			}
			v2PolicyGrant := &iampolicymanagementv1.V2PolicyBaseControlGrant{
				Roles: []iampolicymanagementv1.PolicyRole{*policyRole},
			}
			v2PolicyControl := &iampolicymanagementv1.V2PolicyBaseControl{
				Grant: v2PolicyGrant,
			}
			accountIDResourceAttribute := &iampolicymanagementv1.V2PolicyAttribute{
				Key:     core.StringPtr("accountId"),
				Operator: core.StringPtr("stringEquals"),
				Value:    core.StringPtr(exampleAccountID),
			}
			serviceNameResourceAttribute := &iampolicymanagementv1.V2PolicyAttribute{
				Key:     core.StringPtr("serviceType"),
				Operator: core.StringPtr("stringEquals"),
				Value:    core.StringPtr("service"),
			}
			policyResource := &iampolicymanagementv1.V2PolicyBaseResource{
				Attributes: []iampolicymanagementv1.V2PolicyAttribute{
					*accountIDResourceAttribute, *serviceNameResourceAttribute},
			}
			weeklyConditionAttribute :=  &iampolicymanagementv1.V2PolicyAttribute{
				Key:     core.StringPtr("{{environment.attributes.day_of_week}}"),
				Operator: core.StringPtr("dayOfWeekAnyOf"),
				Value:    []int{1,2,3,4,5},
			}
			startConditionAttribute :=  &iampolicymanagementv1.V2PolicyAttribute{
				Key:     core.StringPtr("{{environment.attributes.current_time}}"),
				Operator: core.StringPtr("timeGreaterThanOrEquals"),
				Value:    core.StringPtr("09:00:00+00:00"),
			}
			endConditionAttribute :=  &iampolicymanagementv1.V2PolicyAttribute{
				Key:     core.StringPtr("{{environment.attributes.current_time}}"),
				Operator: core.StringPtr("timeLessThanOrEquals"),
				Value:    core.StringPtr("17:00:00+00:00"),
			}
			policyRule := &iampolicymanagementv1.V2PolicyBaseRule{
				Operator: core.StringPtr("and"),
				Conditions: []iampolicymanagementv1.V2PolicyAttribute{
					*weeklyConditionAttribute, *startConditionAttribute, *endConditionAttribute},
			}

			options := iamPolicyManagementService.NewV2CreatePolicyOptions(
				"access",
				v2PolicyControl,
			)
			options.SetSubject(policySubject)
			options.SetResource(policyResource)
			options.SetRule(policyRule)
			options.SetPattern(*core.StringPtr("time-based-conditions:weekly"))

			policy, response, err := iamPolicyManagementService.V2CreatePolicy(options)
			if err != nil {
				panic(err)
			}
			b, _ := json.MarshalIndent(policy, "", "  ")
			fmt.Println(string(b))
```
{: codeblock}
{: go}

```java
V2PolicyAttribute subjectAttribute = new V2PolicyAttribute.Builder()
              .key("iam_id")
              .value(EXAMPLE_USER_ID)
              .operator("stringEquals")
              .build();

      V2PolicyBaseSubject policySubject = new V2PolicyBaseSubject.Builder()
              .addAttributes(subjectAttribute)
              .build();

      V2PolicyAttribute accountIdResourceAttribute = new V2PolicyAttribute.Builder()
              .key("accountId")
              .value(exampleAccountId)
              .operator("stringEquals")
              .build();

      V2PolicyAttribute serviceNameResourceAttribute = new V2PolicyAttribute.Builder()
              .key("serviceName")
              .value("iam-groups")
              .operator("stringEquals")
              .build();

      V2PolicyBaseResource policyResource = new V2PolicyBaseResource.Builder()
              .addAttributes(accountIdResourceAttribute)
              .addAttributes(serviceNameResourceAttribute)
              .build();

      PolicyRole policyRoles = new PolicyRole.Builder()
              .roleId("crn:v1:bluemix:public:iam::::role:Editor")
              .build();

      V2PolicyBaseControlGrant policyGrant = new V2PolicyBaseControlGrant.Builder()
              .roles(Arrays.asList(policyRoles))
              .build();

      V2PolicyBaseControl policyControl = new V2PolicyBaseControl.Builder()
              .grant(policyGrant)
              .build();

      V2PolicyAttribute weeklyConditionAttribute = new V2PolicyAttribute.Builder()
              .key("{{environment.attributes.day_of_week}}")
              .value(new ArrayList<Integer>(Arrays.asList(1, 2, 3, 4, 5)))
              .operator("dayOfWeekAnyOf")
              .build();

      V2PolicyAttribute startConditionAttribute = new V2PolicyAttribute.Builder()
              .key("{{environment.attributes.current_time}}")
              .value("09:00:00+00:00")
              .operator("timeGreaterThanOrEquals")
              .build();

      V2PolicyAttribute endConditionAttribute = new V2PolicyAttribute.Builder()
              .key("{{environment.attributes.current_time}}")
              .value("17:00:00+00:00")
              .operator("timeLessThanOrEquals")
              .build();

      V2PolicyBaseRuleV2RuleWithConditions policyRule = new V2PolicyBaseRuleV2RuleWithConditions.Builder()
              .operator("and")
              .conditions(new ArrayList<V2PolicyAttribute>(Arrays.asList(weeklyConditionAttribute, startConditionAttribute, endConditionAttribute)))
              .build();

      V2CreatePolicyOptions options = new V2CreatePolicyOptions.Builder()
              .type("access")
              .subject(policySubject)
              .control(policyControl)
              .resource(policyResource)
              .rule(policyRule)
              .pattern("time-based-conditions:weekly")
              .build();

      Response<V2Policy> response = service.v2CreatePolicy(options).execute();
      V2Policy policy = response.getResult();

      System.out.println(policy);
```
{: codeblock}
{: java}

```javascript
const policySubject = {
      attributes: [
        {
          key: 'iam_id',
          operator: 'stringEquals',
          value: exampleUserId,
        },
      ],
    };
    const policyResourceAccountAttribute = {
      key: 'accountId',
      value: exampleAccountId,
      operator: 'stringEquals',
    };
    const policyResourceServiceAttribute = {
      key: 'serviceName',
      operator: 'stringEquals',
      value: 'iam-groups',
    };
    const policyResource = {
      attributes: [policyResourceAccountAttribute, policyResourceServiceAttribute]
    };
    const policyControl = {
      grant: {
        roles: [{
          role_id: 'crn:v1:bluemix:public:iam::::role:Editor',
        }],
      }
    };
    const policyRule = {
      operator: 'and',
      conditions: [
          {
              key: '{{environment.attributes.day_of_week}}',
              operator: 'dayOfWeekAnyOf',
              value: [1, 2, 3, 4, 5],
          },
          {
              key: '{{environment.attributes.current_time}}',
              operator: 'timeGreaterThanOrEquals',
              value: '09:00:00+00:00',
          },
          {
              key: '{{environment.attributes.current_time}}',
              operator: 'timeLessThanOrEquals',
              value: '17:00:00+00:00',
          },
      ],
    }
    const policyPattern = 'time-based-conditions:weekly'
    const params = {
      type: 'access',
      subject: policySubject,
      control: policyControl,
      resource: policyResource,
      rule: policyRule,
      pattern: policyPattern,
    };

    try {
      const res = await iamPolicyManagementService.v2CreatePolicy(params);
      examplePolicyId = res.result.id;
      console.log(JSON.stringify(res.result, null, 2));
    } catch (err) {
      console.warn(err)
    }
```
{: codeblock}
{: javascript}

```python
policy_subject = V2PolicyBaseSubject(
                attributes=[V2PolicyAttribute(key='iam_id', value=example_user_id, operator='stringEquals')]
            )
            policy_role = PolicyRole(role_id='crn:v1:bluemix:public:iam::::role:Editor')
            account_id_resource_attribute = V2PolicyAttribute(
                key='accountId', value=example_account_id, operator='stringEquals'
            )
            service_name_resource_attribute = V2PolicyAttribute(
                key='serviceName', value='iam-groups', operator='stringEquals'
            )
            policy_resource = PolicyResource(
                attributes=[account_id_resource_attribute, service_name_resource_attribute],
            )
            policy_control = V2PolicyBaseControl(grant=V2PolicyBaseControlGrant(roles=[policy_role]))
            policy_rule = V2PolicyBaseRuleV2RuleWithConditions(
                operator='and',
                conditions=[
                    V2PolicyAttribute(
                        key='{{environment.attributes.day_of_week}}', operator='dayOfWeekAnyOf', value=[1, 2, 3, 4, 5]
                    ),
                    V2PolicyAttribute(
                        key='{{environment.attributes.current_time}}',
                        operator='timeGreaterThanOrEquals',
                        value='09:00:00+00:00',
                    ),
                    V2PolicyAttribute(
                        key='{{environment.attributes.current_time}}',
                        operator='timeLessThanOrEquals',
                        value='17:00:00+00:00',
                    ),
                ],
            )
            policy_pattern = 'time-based-conditions:weekly'

            policy = iam_policy_management_service.v2_create_policy(
                type='access',
                subject=policy_subject,
                control=policy_control,
                resource=policy_resource,
                rule=policy_rule,
                pattern=policy_pattern,
            ).get_result()

            print(json.dumps(policy, indent=2))
```
{: codeblock}
{: python}

For more information about time-based conditions for access policies, see [Conditions in access policies](/docs/account?topic=account-iam-condition-properties&interface=ui#policy-condition-properties).

## Creating a recurring time-based condition by using Terraform
{: #iam-time-based-recur-terra}
{: terraform}

Before you can assign recurring access by using Terraform, make sure that you have completed the following:

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you define resources by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

You might want to give users access to account resources during only their working hours. Complete the following steps to assign an access policy with a recurring at a weekly cadence:

1. The following example configures a policy for a user with the Viewer role on the Kubernetes service. The policy grants access on Monday, Tuesday, Wednesday, and Thursday from 9 AM to 5 PM.

    For more information about time-based conditions for access policies, see [Conditions in access policies](/docs/account?topic=account-iam-condition-properties&interface=ui#policy-condition-properties).

    ```terraform
    resource "ibm_iam_user_policy" "policy" {
      ibm_id = "test@in.ibm.com"
      roles      = ["Viewer"]
      resources {
        service = "kms"
      }
      rule_conditions {
        key = "{{environment.attributes.day_of_week}}"
        operator = "dayOfWeekAnyOf"
        value = ["1+00:00","2+00:00","3+00:00","4+00:00"]
      }
      rule_conditions {
        key = "{{environment.attributes.current_time}}"
        operator = "timeGreaterThanOrEquals"
        value = ["09:00:00+00:00"]
      }
      rule_conditions {
        key = "{{environment.attributes.current_time}}"
        operator = "timeLessThanOrEquals"
        value = ["17:00:00+00:00"]
      }
      rule_operator = "and"
      pattern = "time-based-conditions:weekly:custom-hours"
    }
    ```
    {: codeblock}

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
