---

copyright:

  years: 2018, 2020

lastupdated: "2020-04-16"

keywords: dynamic rules,access groups,specific identity attributes,identity provider,federated ID,

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}

# Creating dynamic rules for access groups
{: #rules}

You can create dynamic rules to automatically add federated users to access groups based on specific identity attributes. When your users log in with a federated ID, the data from the identity provider dynamically maps your users to an access group based on the rules that you set.
{:shortdesc}

Users already have specific identity information within your company's domain, and when they log in with a federated ID, this data can be passed through by using SAML assertions. The SAML assertions or attribute statements that are configured within the identity provider provide the data that is used to create each rule. For example, you might have a true or false attribute statement that defines users as a manager. This information can be used to add all users who are managers to a specific access group for managers that you created in your {{site.data.keyword.Bluemix}} account. For more information, see the tutorial about how to [Control access to cloud resources](https://developer.ibm.com/tutorials/use-iam-access-groups-to-effectively-manage-access-to-your-cloud-resources/){: external} and an [Example rule](/docs/iam?topic=iam-rules#example).

Only users who are already invited to the account can be mapped to access groups by using dynamic rules.
{: note}

## Setting up rules
{: #setup_rules}

Dynamic rules are created by setting conditions that must be matched by the data that is configured within the identity provider and passed in with a user's federated ID during login. You can add more than one condition for a rule. All conditions set in the rule must be met for a user to be added to an access group. 

To create a rule, follow these steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Access Groups**.
2. Select the name of the access group that you want to create a rule for to open the group details page.
3. Select the **Dynamic rules** tab.
4. Click **Add rule**.
5. Enter the information from your identity provider that is dynamically provided for you on the Add rule page. The following list provides details for each required field.

You can think of an access group rule as a key:value pair. The key is what you add in the `Add users when` field, and the value is what you enter in the `Values` field. 
{: tip}

<dl>
<dt>Name</dt>
<dd>Enter a custom name for your rule that helps you remember what type of users that you are adding to an access group.</dd>
<dt>Identity provider</dt>
<dd>Enter the URI for your identity provider. This is the SAML "entityId" field, which is sometimes referred to as the issuer ID, for the identity provider as part of the federation configuration for onboarding with IBMid.</dd>
<dt>Expiration (in hours)</dt>
<dd>You can use this option to provide extra security by setting a time limit for the assigned access. Each user must log in every 24 hours to refresh their access, but you can set the access to expire in as little as an hour's time. Group membership is revoked after this time period expires.</dd>
<dt>Add users when</dt>
<dd>The attribute statement name must be entered in this field. This value is specific to your identity provider.</dd>
<dt>Comparator</dt>
<dd>You can choose from Equals, Not Equals, Equals Ignore Case, Not Equals Ignore Case, In, and Contains. Use the Contains option when the attribute statement has an array type. And, you can enter more than one value to be matched by using the In option.</dd>
<dt>Value</dt>
<dd>Enter the attribute value for the attribute statement that the rule is comparing against.</dd>
</dl>

Users added to access groups by using dynamic rules don't display as group members on the users list for the access group. To check a specific user's membership to an access group, you can select that user's name from the account **Users** page, and then click **Access groups**.
{: note}

## Example rule
{: #example}

The following example includes values for each of the fields on the **Add rule** page. In this rule, users who are identified as managers within the federated identity provider are mapped to an {{site.data.keyword.Bluemix_notm}} access group that has specific access set for only managers.

| Field                           | Value                           |
|---------------------------------|---------------------------------|
| Name                            | Manager group rule              |
| Identity provider               | `https://idp.example.org/SAML2` |
| Expiration (in hours)           | 12                              |
| Add users when (attribute name) | isManager                       |
| Comparator                      | Equals                          |
| Value                           | true                            |
{: caption="Table 1. Example dynamic rule for access groups" caption-side="top"}
