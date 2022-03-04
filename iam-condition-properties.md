---

copyright:

  years: 2022

lastupdated: "2022-03-04"

keywords: trusted profile, dynamic rule, operators, rules, conditions, properties

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# IAM condition properties
{: #iam-condition-properties}

The two types of conditional IAM statements that automatically grant [IAM policy subjects](/docs/account?topic=account-cloudaccess) access to targets are dynamic rules and trusted profiles. Dynamic rules automatically add federated users in your account to access groups based on specific identity attributes. Trusted profiles use the same conditional statement format to automatically grant federated users access to your account. For more information, see [Creating dynamic rules for access groups](/docs/account?topic=account-rules) and [Creating trusted profiles](/docs/account?topic=account-create-trusted-profile). 


## Condition statement properties
{: #condition-properties}

Each dynamic rule and trusted profile condition has the following properties:

Name
:   Enter a custom name for that helps you remember what type of users that you are adding to an access group or trusted profile.

Identity provider (IdP)
:   The dynamic rule or trusted profile is evaluated only if the user who is logging in authenticates by way of the enterprise IdP with this issuer URI. For IBMid, the IdP is the SAML "entityId" field, sometimes referred to as the issuer ID, and is part of the federation configuration when you are onboarding with IBMid. For AppID, equivalent syntax is the "realm ID". For more information, see [Enabling authentication from an external identity provider](https://cloud.ibm.com/docs/account?topic=account-idp-integration)

Expiration
:   The dynamic access group or trusted profile session expires after the number of hours that are specified in this property. For example, if the property is set to 24, the user’s dynamic or trusted profile session ends one day (24 hours) after they log in.



Additionally, each dynamic rule and trusted profile has one or more conditions that consist of the following properties. All properties need to apply for the overall dynamic rule evaluate to true:

Add users when
:   References an attribute name that is part of the login message that is sent from your identity provider to IBM Cloud. To learn more about how attribute names are propagated from your enterprise identity provider to the condition evaluation, see [Mapping of enterprise identity provider attributes](https://developer.ibm.com/tutorials/use-iam-access-groups-to-effectively-manage-access-to-your-cloud-resources/#mapping-of-enterprise-identity-provider-attributes){: external}.

Comparator
:   Compares the attribute that is specified in the `Add users when` field with `Values` property. You can choose from Equals, Not Equals, Equals Ignore Case, Not Equals Ignore Case, In, and Contains. Use the Contains option when the attribute statement has an array type. And, you can enter more than one value to be matched by using the In option.

Values
:   Enter an attribute value that is used by the comparator to evaluate against the `Add users when` attribute name.

## Available comparators for conditions
{: #comparators}

| Comparator | Description  | Sample condition |
|------------|--------------|------------------|
| Equals                 | Case-sensitive string comparison. Boolean or number values are converted into a string before comparison. | primaryGroup Equals “Admins” |
| Not Equals             | Negated case-sensitive string comparison. Boolean or number values are converted into a string before comparison. | primaryGroup NotEquals “Admins” |
| Equals Ignore Case     | Case-insensitive string comparison. Boolean or number values are converted into a string before comparison. | isManager EqualsIgnoreCase “tRuE” |
| Not Equals Ignore Case | Negated case-insensitive string comparison. Boolean or number values are converted into a string before comparison.	 | is_teamlead NotEqualsIgnoreCase “TrUe” |
| Contains               | Determines by using the comparator Equals if the value that is provided is part of the attribute in the login message. Can be applied only on attributes that contain arrays of strings, numbers, or Booleans. | `group` contains “Admins” |
| In                     | Short notation for multiple Equal operators. Compares the value in the login message attribute with the list of potential values in this rule. Again, Boolean or numbers are converted to a string before comparison. | jobRole in [“Manager”,”Director”,”Team-Lead”] |
{: caption="Table 1. Available comparators for conditions" caption-side="top"}

## Example
{: #example-values}

The following table includes values for each of the fields for a dynamic rule or a trusted profile condition. In this example, users who are identified as managers within the federated IdP are mapped to an {{site.data.keyword.Bluemix_notm}} access group or trusted profile that has specific access set for only managers.

| Field                           | Value                           |
|---------------------------------|---------------------------------|
| Name                            | Manager                         |
| Identity provider               | `https://idp.example.org/SAML2` |
| Session duration in hours       | 12                              |
| Add users when (attribute name) | isManager                       |
| Comparator                      | Equals                          |
| Value                           | true                            |
{: caption="Table 2. Example values" caption-side="top"}
