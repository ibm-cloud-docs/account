---

copyright:

  years: 2022

lastupdated: "2022-03-30"

keywords: trusted profile, dynamic rule, operators, rules, conditions, properties, IAM

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# IAM condition properties
{: #iam-condition-properties}

Dynamic rules and trusted profiles both use conditional IAM statememnts that you specify to automatically add federated users to access groups or trusted profiles. When your users log in with a federated ID, the data from the identity provider (IdP) dynamically maps your users to an access group based or trusted profile based on the rules or conditions that you set. For more information, see [Creating dynamic rules for access groups](/docs/account?topic=account-rules) and [Creating trusted profiles](/docs/account?topic=account-create-trusted-profile). 

## Rule and profile details
{: #general-details}

Each dynamic rule and trusted profile has the following properties:

Name
:   Enter a custom name that helps you remember what type of users you are adding to an access group or trusted profile.

Identity provider (IdP)
:   The dynamic rule or trusted profile is evaluated only if the user who is logging in authenticates by using the enterprise IdP with this issuer URI. Your IdP URL is displayed in the console for you to copy and paste when you create a dynamic rule or trusted profile. For example, `https://w3id.sso.ibm.com/auth/sps/samlidp2/saml20`. You can also view this by clicking `View identity provider (IdP) data`. For IBMid, the IdP is the SAML "entityId" field, sometimes referred to as the issuer ID, and is part of the federation configuration when you are onboarding with IBMid. For AppID, equivalent syntax is the "realm ID". For more information, see [Enabling authentication from an external identity provider](/docs/account?topic=account-idp-integration)

Session duration
:   The dynamic access group or trusted profile session expires after the number of hours that are specified in this property. For example, if the property is set to 24 hours, the user’s dynamic or trusted profile session ends one day (24 hours) after they log in.

## Condition statement properties
{: #condition-properties}

Additionally, each dynamic rule and trusted profile has one or more conditions that consist of the following properties. Users ned to satisfy all conditions for the overall dynamic rule or trusted profile authentication to evaluate to true:

Add users when
:   An attribute name that is part your identity provider data. To learn more about how attribute names are created from your enterprise identity provider to the condition evaluation, see [Mapping of enterprise identity provider attributes](https://developer.ibm.com/tutorials/use-iam-access-groups-to-effectively-manage-access-to-your-cloud-resources/#mapping-of-enterprise-identity-provider-attributes){: external}.

Comparator
:   Compares the attribute that is specified in the `Add users when` field with the `Values` property. You can choose from Equals, Not Equals, Equals Ignore Case, Not Equals Ignore Case, In, and Contains. Use the Contains option when the attribute statement has an array type. You can enter more than one value to be matched by using the In option.

Values
:   An attribute value that is used by the comparator to evaluate against the `Add users when` attribute name.

You can think of a dynamic rule or trusted profile condition as a key:value pair. The key is what you add in the `Add users when` field, and the value is what you enter in the `Values` field. 
{: tip}

## Available comparators for conditions
{: #comparators}

| Comparator | Description  | Sample condition |
|------------|--------------|------------------|
| Equals                 | Case-sensitive string comparison. Boolean or number values are converted into a string before comparison. | primaryGroup Equals “Admins” |
| Not Equals             | Negated case-sensitive string comparison. Boolean or number values are converted into a string before comparison. | primaryGroup NotEquals “Admins” |
| Equals Ignore Case     | Case-insensitive string comparison. Boolean or number values are converted into a string before comparison. | isManager EqualsIgnoreCase “tRuE” |
| Not Equals Ignore Case | Negated case-insensitive string comparison. Boolean or number values are converted into a string before comparison.	 | is_teamlead NotEqualsIgnoreCase “TrUe” |
| Contains               | If the attribute is an array of strings, numbers, or Booleans, `Contains` will determine by using the comparator Equals if the value that is provided is part of the array in the login message. If the attribute is a single string instead, `Contains` will determine if the value that is provided is contained in the string attribute in the login message. | `group` contains “Admins” |
| In                     | Short notation for multiple Equal operators. Compares the value in the login message attribute with the list of potential values in this rule. Boolean or numbers are converted to a string before comparison. | jobRole in [“Manager”,”Director”,”Team-Lead”] |
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
