---

copyright:
  years:  2023, 2024
lastupdated: "2024-01-02"

keywords: change log for access-management polices, updates to access-management polices, IAM Policy Management API change log, policies change log, access management change log

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# IAM Policy Management API change log
{: #api-change-log}

In this change log you can learn about the latest changes, improvements, and updates to the IAM Policy Management API. The change log lists changes that have been made, ordered by the date they were released. Changes to existing API versions are designed to be compatible with existing client applications.

For information about the latest changes to the IAM Policy Management SDKs and CLI, see the change logs in the SDK repositories:
- [Java SDK change log](https://github.com/IBM/platform-services-java-sdk/blob/main/CHANGELOG.md)
- [Node SDK change log](https://github.com/IBM/platform-services-node-sdk/blob/main/CHANGELOG.md)
- [Python SDK change log](https://github.com/IBM/platform-services-python-sdk/blob/main/CHANGELOG.md)
- [Go SDK change log](https://github.com/IBM/platform-services-go-sdk/blob/main/CHANGELOG.md)
- [Cloud CLI change log](https://github.com/IBM-Cloud/ibm-cloud-cli-release/releases/)

## API versioning
{: #api-versioning}

The IAM Policy Management API uses URI path versioning. Incompatible changes are versioned as major changes by incrementing the URI path number (`../v1/policies`). All other changes to the api are expected to be compatible with existing usage.

### Active version
{: #active-version}

The following table shows the behavior changes for each version.

| Version | Summary of changes |
|---|---|
|`v2`| New schema to support conditions and advanced operators dealing with date and time|
|`v1`| Initial version of IAM Policy Management API |
{: caption="Table 1. IAM Policy Management API versions" caption-side="top"}

The `v1` API is not forwards compatible with the `v2` API. You can't add conditions to a policy that is created with the `v1` API. To add conditions, you must delete the `v1` policy and replace it with a new access policy that includes conditions.
{: important}

## 25 January 2023
{: #25-jan-2023}

This change log introduces a new version (`v1 -> v2`) of the IAM Policy Management API. This version adds a new JSON schema to support a conditional policy construct and several time-based comparison operators. These operators provide the capability to restrict access based on time and date. With time-based access control, customers can establish granular policy enforcement based on a specified time period.

To get started, see [Limiting access with time-based conditions](/docs/account?topic=account-iam-time-based&interface=ui).

For detailed operator descriptions and examples, see: [Conditions in `v2` access policies](/docs/account?topic=account-iam-condition-properties#policy-condition-properties)

The new `v2/polices` schema provides backwards functional compatibility and allows for more complex comparisons and operators. The `v1/polices` schema remains supported and available. For more information, see [Comparing `/v1/policies` and `/v2/policies` syntax](/docs/account?topic=account-known-issues#compare-syntax).
