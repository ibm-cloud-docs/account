---

copyright:

  years: 2020, 2025
lastupdated: "2025-06-10"

keywords: account known issues, catalog known issues, catalog management, private catalogs, catalogs, IBM Cloud catalog, IAM, maximum limits for creating IAM resources, delete users from account, context-based restrictions

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Known issues and limitations
{: #known-issues}

Known issues and limitations include not being able to restrict access to some products in the {{site.data.keyword.cloud}} catalog, and the maximum limits for creating {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) resources.
{: shortdesc}

To review the default limits for your account, see [{{site.data.keyword.cloud_notm}} IAM limits](/docs/account?topic=account-cloudaccess#iam_limits).
{: note}



## Google login doesn't support federated IDs
{: #google-fed-id}

Google ID login isn't available for users with federated IDs due to additional access that might be required by their corporate external identity provider (IdP).

## Catalog management settings don't apply to some {{site.data.keyword.IBM_notm}} products
{: #settings-noapply}

Some products are not affected by the following catalog visibility settings:

- Turning off the visibility of the {{site.data.keyword.Bluemix_notm}} catalog
- Excluding all {{site.data.keyword.Bluemix_notm}} products from the catalog
- Excluding all {{site.data.keyword.Bluemix_notm}} products from your private catalogs

You can view and manage catalog visibility settings by going to **Manage > Catalogs > Settings** in the {{site.data.keyword.Bluemix_notm}} console.
{: note}

Users can still create instances of the following products by using an API or the CLI, regardless of the [catalog visibility setting](/docs/account?topic=account-filter-account&interface=ui#catalog-filters-customize) in the account or private catalog:

* {{site.data.keyword.block_storage_is_short}}
* {{site.data.keyword.vpx_full}}
* Fortigate Security Appliance
* Hardware Firewall
* Hardware Firewall Dedicated
* {{site.data.keyword.backup_notm}}
* {{site.data.keyword.cloud_notm}} {{site.data.keyword.baremetal_short}}
* {{site.data.keyword.cloud_notm}} {{site.data.keyword.blockstorageshort}}
* {{site.data.keyword.registrylong_notm}}
* {{site.data.keyword.cloud_notm}} Content Delivery Network
* {{site.data.keyword.cloud_notm}} Direct Link
* {{site.data.keyword.cloud_notm}} Direct Link on Classic
* {{site.data.keyword.IBM_notm}} {{site.data.keyword.openwhisk_short}}
* {{site.data.keyword.cloud_notm}} Gateway Appliance
* {{site.data.keyword.cloud_notm}} Hardware Security Modules
* {{site.data.keyword.containerlong_notm}}
* {{site.data.keyword.cos_full_notm}}
* {{site.data.keyword.bplong_notm}}
* {{site.data.keyword.cloud_notm}} Load Balancer
* {{site.data.keyword.cloud_notm}} {{site.data.keyword.BluVirtServers_short}}
* Subnets and IPs
* Virtual Private Cloud
* Virtual Server for VPC
* VLANs
* VPN
* VPN for VPC

## Policy limitations based on attributes
{: #access-tag-limits}

Access management tags are available only when you create an access policy that is scoped for all IAM-enabled services. In this case, when you enable the access based on tags, no other attributes can be added. And, when you base your policy on a specific location or resource group, no tag can be added to the access policy.

## Access policy version limitations
{: #policy-version-limit}

As of 25 January 2023, IAM supports two versions of the IAM Policy Management API: `/v2/policies` and `/v1/policies`. `v1/polices` allows for string comparisons against attributes in the subject and resources of a policy. `v2/polices` introduces a new schema that provides backwards functional compatibility while allowing for more complex comparisons and operators and time based conditions.

### String comparisons
{: #policy-string-comparison}

{{_include-segments/string-compare-intro-reuse.md}}

You can have up to 10 conditions and nesting up to 2 levels.
{: important}

{{_include-segments/string-compare-table-reuse.md}}

For example, the following statement contains an `operator` element that uses `stringEquals` to specify that the account ID and service name must exactly match the `value` element. The statement also contains an `operator` element that uses `stringMatch` to specify a naming pattern for {{site.data.keyword.messagehub}} topics that you might use to organize access to those specific resources. This way, you can assign one policy to all topics in your account that begin with `messagehub-topic-dev`.

```json
"resource": {
		"attributes": [
			{
				"operator": "stringEquals",
				"value": "0aeab68aabd14d89bd72e4330150710a0",
				"key": "accountId"
			},
			{
				"value": "messagehub",
				"operator": "stringEquals",
				"key": "serviceName"
			},
			{
				"value": "messagehub-topic-dev*",
				"operator": "stringMatch",
				"key": "resource"
			}
		]
	},
```
{: codeblock}

[Authorization policies](/docs/account?topic=account-serviceauth) are currently only supported in `/v1/policies`.
{: note}

### Checking a policy version in the console
{: #check-policy-version}

Time-based and resource attribute-based conditions for IAM access policies use `/v2/policies` syntax. Policies that use `/v1/policies` syntax aren't eligible to add time-based and resource attribute-based conditions. To update `/v1/policies` to `/v2/policies` by using the API, see [Updating `/v1/policies` to `/v2/policies` with conditions by using the API](/docs/account?topic=account-known-issues#update-policy-version). To check whether you can add these conditions to an existing policy in the console, complete the following steps.

1. Go to **Manage > Access (IAM)**.
1. Select **Users**, **Trusted profiles**, **Service IDs**, or **Access groups**, depending on the policy you want to check.
1. Select a specific users, trusted profile, service ID, or access group.
1. Go to **Access** > **Access policies**.
1. Click on a policy. `/v1/policies` are indicated by the following notification:

   > Conditions unavailable for v1 policies

1. (Optional) To add conditions to a policy that uses `/v1/policies` syntax, delete the original policy and create a new one. In the console, new policies use `/v2/policies` syntax.

#### Updating `/v1/policies` to `/v2/policies` with conditions by using the API
{: #update-policy-version}

Policies that use `/v1/policies` syntax aren't eligible to add time-based and resource attribute-based conditions. To update the version, you can use the [PUT /v2/policies/{id}](/apidocs/iam-policy-management#replace-v2-policy) with the V1 ID and any conditions you want to include. For more information, see [`/v2/policies`](/docs/account?topic=account-known-issues#v2-policies).

### Comparing `/v1/policies` and `/v2/policies` syntax
{: #compare-syntax}

The policy in each example grants a user access to the Billing service with the Editor role. The `/v2/policies` example includes temporary time-based conditions, indicated by the `"conditions"` parameter.

When editing, creating, and deleting policies, use the corresponding API version.
{: tip}

#### `/v1/policies`
{: #v1-policies}

```json
{
	"type": "access",
	"roles": [
		{
			"role_id": "crn:v1:bluemix:public:iam::::role:Editor"
		}
	],
	"resources": [
		{
			"attributes": [
				{
					"name": "accountId",
					"value": "000c49bc2724a07000010b1da94c4d0"
				},
				{
					"name": "serviceName",
					"value": "billing"
				}
			]
		}
	],
	"subjects": [
		{
			"attributes": [
				{
					"name": "iam_id",
					"value": "IBMid-00000AV0S0"
				}
			]
		}
	]
}
```
{: codeblock}

When you list policies with `/v1/policies` the API returns `/v1/` and a placeholder policy for each `/v2/` policy that's in the account. For more information, see [`/v1/policies` returns a placeholder for `/v2/` policies the account](/docs/account?topic=account-known-issues#placeholder-v2)
{: note}


#### `/v2/policies`
{: #v2-policies}

```json
{
	"type": "access",
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
				"value": "000c49bc2724a07000010b1da94c4d0",
				"key": "accountId"
			},
			{
				"value": "billing",
				"operator": "stringEquals",
				"key": "serviceName"
			}
		]
	},
	"rule": {
		"operator": "and",
		"conditions": [
			{
				"key": "{{environment.attributes.current_date_time}}",
				"operator": "dateTimeGreaterThanOrEquals",
				"value": "2023-01-01T09:00:00+00:00"
			},
			{
				"key": "{{environment.attributes.current_date_time}}",
				"operator": "dateTimeLessThanOrEquals",
				"value": "2023-01-06T17:59:59+00:00"
			}
		]
	},
	"pattern": "time-based-conditions:once",
	"subject": {
		"attributes": [
			{
				"key": "iam_id",
				"operator": "stringEquals",
				"value": "IBMid-00000AV0S0"
			}
		]
	}
}
```
{: codeblock}

#### `/v1/policies` returns a placeholder for `/v2/` policies
{: #placeholder-v2}

When you list policies with `/v1/policies` the API returns `/v1/` and a placeholder policy for each `/v2/` policy that's in the account. The placeholders indicate the existence of additional policies in the account while abiding by the `/v1/` schema. To see the full content of a `/v2/` policy, list policies by using `/v2/policies` or retrieve the individual policy by using `GET: v2/policies/<ID>`. For example, see the following placeholder policy:

```json
{
    "id": "33b901fa-8ec5-4432-a2e6-24b6a212c20a",
	"type": "access",
	"description": "**This is a unsupported policy version placeholder, to view the full content, please call GET with provided href**",
	"subjects": [{
		"attributes": [{
			"name": "iam_id",
			"value": "unsupported version"
		}]
	}],
	"roles": [{
		"role_id": "crn:v1:bluemix:public:iam::::role:UnsupportedVersion",
		"display_name": "Unsupported Version",
		"description": "**This is a unsupported policy version placeholder, to view the full content, please call GET with provided href**"
	}],
	"resources": [{
		"attributes": [{
			"name": "accountId",
			"value": "000c49bc2724a07000010b1da94c4d0"
		}]
	}],
    "href": "https://iam.cloud.ibm.com/v2/policies/88b901fa-6ec5-888-a2e6-24b6a212c20a"
}
```
{: codeblock}

## Services impacted by limiting external identity interactions
{: #external-id-interaction-limitation}

Limiting external identity interactions requires that users with an IAM access policy on resources in your account access those resources only when authenticated in your account or an account in the allowlist. The following services, or some of their features, might not function as expected if the external identity interactions setting is set to **Limited** mode:

- {{site.data.keyword.satellitelong_notm}}
- {{site.data.keyword.cos_full_notm}} -  public access buckets will not be accessible
- {{site.data.keyword.codeenginefull_notm}}
- {{site.data.keyword.DRA_full}}
- Access Report (Generating CSV or JSON resource access report)

For more information about this setting, see [Managing external identity interactions](/docs/account?topic=account-cross-acct).
