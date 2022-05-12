---

copyright:

  years: 2022

lastupdated: "2022-05-12"

keywords: trusted profile, dynamic rule, operators, rules, conditions, properties

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# IAM condition properties
{: #iam-condition-properties}

Dynamic rules and trusted profiles both use conditional IAM statements that you specify to automatically add federated users to access groups or trusted profiles. When users log in with a federated ID, the data from the identity provider (IdP) dynamically maps them to an access group based on conditions that you set. For more information, see [Creating dynamic rules for access groups](/docs/account?topic=account-rules) and [Creating trusted profiles](/docs/account?topic=account-create-trusted-profile). 

## Rule and profile details
{: #general-details}

Each dynamic rule and trusted profile trust relationship has the following properties:

Name
:   Enter a custom name that helps you remember what type of users you are adding to an access group or trusted profile.

Identity provider (IdP)
:   The dynamic rule or trusted profile is evaluated only if the user who is logging in authenticates by using the enterprise IdP with this issuer URI. Your IdP URL is displayed in the console for you to copy and paste when you create a dynamic rule or trusted profile. For example, `https://w3id.sso.ibm.com/auth/sps/samlidp2/saml20`. You can also view th IdP by clicking `View identity provider (IdP) data`. For IBMid, the IdP is the SAML "entityId" field, sometimes referred to as the issuer ID, and is part of the federation configuration when you are onboarding with IBMid. For AppID, equivalent syntax is the "realm ID". For more information, see [Enabling authentication from an external identity provider](/docs/account?topic=account-idp-integration)

Session duration
:   The dynamic access group membership or trusted profile session expires after the number of hours that are specified in this property. For example, if the property is set to 24 hours, the user’s dynamic or trusted profile session ends one day (24 hours) after they log in.

## Condition statement properties
{: #condition-properties}

Additionally, each dynamic rule and trusted profile trust relationship has one or more conditions that consist of the following properties. Users need to satisfy all conditions for the overall dynamic rule or trusted profile authentication to evaluate to true:

Allow users when
:   An attribute name that is part your identity provider data. To learn more about how attribute names are created from your enterprise identity provider to the condition evaluation, see [Mapping of enterprise identity provider attributes](https://developer.ibm.com/tutorials/use-iam-access-groups-to-effectively-manage-access-to-your-cloud-resources/#mapping-of-enterprise-identity-provider-attributes){: external}.

Comparator
:   Compares the attribute that is specified in the `Allow users when` field with the `Values` property. You can choose from Equals, Not Equals, Equals Ignore Case, Not Equals Ignore Case, In, and Contains. Use the Contains option when the attribute statement has an array type. You can enter more than one value to be matched by using the In option.

Values
:   An attribute value that is used by the comparator to evaluate against the `Allow users when` attribute name.

You can think of a dynamic rule or trusted profile condition as a key:value pair. The key is what you add in the `Allow users when` field, and the value is what you enter in the `Values` field. 
{: tip}

## Available comparators for conditions
{: #comparators}

| Comparator | Description  | Sample condition |
|------------|--------------|------------------|
| Equals                 | Case-sensitive string comparison. Boolean or number values are converted into a string before comparison. | primaryGroup Equals “Admins” |
| Not Equals             | Negated case-sensitive string comparison. Boolean or number values are converted into a string before comparison. | primaryGroup NotEquals “Admins” |
| Equals Ignore Case     | Case-insensitive string comparison. Boolean or number values are converted into a string before comparison. | isManager EqualsIgnoreCase “tRuE” |
| Not Equals Ignore Case | Negated case-insensitive string comparison. Boolean or number values are converted into a string before comparison.	 | is_teamlead NotEqualsIgnoreCase “TrUe” |
| Contains               | If the attribute is an array of strings, numbers, or Booleans, `Contains` determines by using the comparator `Equals` if the value that is provided is part of the array in the login message. If the attribute is a single string instead, `Contains` determines whether the value that is provided is contained in the string attribute in the login message. | `group` contains “Admins” |
| In                     | Short notation for multiple Equal operators. Compares the value in the login message attribute with the list of potential values in this rule. Boolean or numbers are converted to a string before comparison. | jobRole in [“Manager”,”Director”,”Team-Lead”] |
{: caption="Table 1. Available comparators for conditions" caption-side="top"}

## Example
{: #example-values}

The following table includes values for each of the fields for a dynamic rule or a trusted profile condition. In this example, users who are identified as managers within the federated IdP are mapped to an {{site.data.keyword.Bluemix_notm}} access group or trusted profile that has specific access set for only managers.

| Field                           | Value                           |
|---------------------------------|---------------------------------|
| Name                            | `Manager`                         |
| Identity provider               | `https://idp.example.org/SAML2` |
| Session duration in hours       | `12`                              |
| Allow users when (attribute name) | `isManager`                       |
| Comparator                      | `Equals`                          |
| Value                           | `true`                            |
{: caption="Table 2. Example values" caption-side="top"}

## Compute resource attribute names
{: #cr-attribute-names}

To establish trust with a compute resource in a trusted profile, you can use the {{site.data.keyword.cloud_notm}} console, {{site.data.keyword.cloud_notm}} CLI, or the IAM API. If you select **All service resources** and add conditions to filter the compute resource instances that can apply the profile, the conditions are built based on the following resource attributes.

### Kubernetes and Red Hat OpenShift attribute names
{: #cr-kub-rhos}

| {{site.data.keyword.cloud_notm}} console name | CLI and API name | Description         |
|---------------------------------|---------------------------------|---------------------| 
| Resource group ID      | `resource_group_id` | The ID of the resource group that contains this cluster. You can identify the resource group of a cluster by using its overview page in the IBM Cloud Console. |
| Resource group name    | `resource_group_name` | The name of the resource group that contains this cluster. |
| Service instance       | `service_instance`    | The ID of this cluster. You can retrieve this value from the cluster's overview page in the IBM Cloud Console as "Cluster ID" or using the IBM Cloud CLI. |
| Location               | `location`            | Location of the cluster derived from its cloud resource name. |
| Namespace              | `namespace`           | Namespace of the service account that is used to retrieve a Compute Resource token and get an IAM token. |
| Service account        | `name`                | Name of the service account that is used to retrieve a Compute Resource token and get an IAM token. |
| Pod                    | `pod`                 | The name of the Kubernetes pod that runs the code that wants to retrieve an IAM token. |
{: caption="Table 3. Kubernetes and Red Hat OpenShift attribute names" caption-side="top"}

### Virtual server for VPC attribute names
{: #cr-vpc}

| {{site.data.keyword.cloud_notm}} console name | CLI and API name | Description         |
|---------------------------------|---------------------------------|---------------------| 
| Resource group ID      | `resource_group_id`   | The ID of the resource group that contains this cluster. You can identify the resource group of a cluster by using its overview page in the IBM Cloud Console. |
| Resource group name    | `resource_group_name` | The name of the resource group that contains this cluster. |
| Resource ID            | `resource`            | The ID of the virtual server for VPC. |
| Instance group name    | `instance_group_name` | Name of the instance group, if this virtual server is part of one. |
| Region                 | `region`              | Region into which this virtual server is deployed. |
| Subnet                 | `subnet_id`           | The subnet ID of the virtual server for VPC, if one is available. |
| VPC ID                 | `vpc_id`              | The VPC ID of the virtual server for VPC, if one is available. |
| Zone                   | `zone`                | Zone name in which this virtual server is deployed to. |
{: caption="Table 4. Virtual server for VPC attribute names" caption-side="top"}


### {{site.data.keyword.cloud_notm}} CLI command examples
{: #cr-rule-cli-examples}

The following examples show how you can use the attribute names in the CLI to build trusted profile links and conditions. 

#### Linking a trusted profile to Kubernetes a cluster 
{: #tp-link-cluster}

To link the trusted profile `Test` to the Kubernetes cluster `c0pigdctkkc07fs7pm06` in the account `444aebb0657c7f0f3aae8e7bdc78709a` and service account `my-service-account` in the namespace `my-namespace`, specify the following command:

```bash
ibmcloud iam trusted-profile-link-create Test --name NewLink4IKS --cr-type IKS_SA \
               --link-crn 
crn:v1:bluemix:public:containers-kubernetes:us-east:a/444aebb0657c7f0f3aae8e7bdc78709a:c0pigdctkkc07fs7pm06:: \
              --link-namespace "my-namespace" \
              --link-name "my-service-account"
```
{: pre}

#### Creating trusted profile conditions for Kubernetes
{: #tp-condition-cluster}

To connect the trusted profile with the ID `Profile-b2f13064-2b8c-4e4b-9181-c1973a408e3c` to all service accounts in the Kubernetes cluster `c0pigdctkkc07fs7pm06` in the account `444aebb0657c7f0f3aae8e7bdc78709a` and the service account namespace `my-namespace`, specify the following command:

```bash
ibmcloud iam trusted-profile-rule-create Profile-b2f13064-2b8c-4e4b-9181-c1973a408e3c \
              --name NewRule4IKS --type Profile-CR --cr-type IKS_SA \
               --conditions "claim:service_instance,operator:EQUALS,vlaue:c0pigdctkkc07fs7pm06" \
               --conditions "claim:namespace,operator:EQUALS,value:my-namespace"
```
{: pre}

#### Creating trusted profile conditions for VPC
{: #tp-condition-vpc}

To connect the trusted profile with the ID `Profile-b2f13064-2b8c-4e4b-9181-c1973a408e3c` to all virtual servers in one VPC `r206-1db73eed-b0fb-b04f-bb57-4d3a3c2dff9d` in the account `444aebb0657c7f0f3aae8e7bdc78709a`, specify the following command:

```bash
ibmcloud iam trusted-profile-rule-create Profile-b2f13064-2b8c-4e4b-9181-c1973a408e3c \
              --name NewRule4VSI --type Profile-CR --cr-type VSI \
               --conditions "claim:vpc_id,operator:EQUALS,value:r206-1db73eed-b0fb-b04f-bb57-4d3a3c2dff9d"
```
{: pre}
