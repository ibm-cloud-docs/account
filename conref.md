---

copyright:
  years: 2022, 2024

lastupdated: "2024-01-02"

keywords:

subcollection: overview

content-type: conref

---

{{site.data.keyword.attribute-definition-list}}

# Content references for account subcollection.
{: #conref-example}

The following H2s and H3s are going to be reused in several different topics that need identical information.
{: shortdesc}


{{site.data.content.output-values}}

{{site.data.content.define-IAM-access}}


* H2 - **Define IAM access** is used in the following files:
   * catalog-vsi-tutorial.md
   * catalog-vsipower-tutorial.md
   * catalog-terraform-template-tutorial.md
* H3 - **Edit output value descriptions** is used in the following files:
   * catalog-vsi-tutorial.md
   * catalog-vsipower-tutorial.md
   * catalog-terraform-template-tutorial.md

## Edit output value descriptions
{: #output-values}
{: step}

You can improve the descriptions for your Terraform template's output values to help users better understand the purpose of the parameters. The description of any output value that you include in your template can be updated.

To add output values, you need to include them in a new imported version of your Terraform template.
{: note}

Complete the following steps to edit the product's output value descriptions:

1. Click **Configure version** > **Next**.
1. From the Output value descriptions section, provide a new description for the parameter that you want to update.
1. Click **Next**.
{: #steps-output-value-description}

## Define IAM access
{: #define-IAM-access}
{: step}

After you configure your deployment values, you can add the service access and platform access roles that are required to install your product.

Use the following steps to define your product's access:

1. Click **Configure version** > **Next** > **Next**.
1. Click **Add**.
1. Select the service and the required service and platform access.
   * The service access role allows access for using the service and performing service API calls.
   * The platform access role enables actions to be performed on platform resources, such as creating an instance, connecting instances to apps, and assigning user access.
1. Click **Save**.
{: #steps-define-IAM-access}


<!--- String comparisons used in known-issues.md and iam-wildcard.md--->

The following table lists the string comparison operators that you can use to build access policies with `/v2/policies` syntax. For more information about each version, see [Comparing `/v1/policies` and `/v2/policies` syntax](/docs/account?topic=account-known-issues#compare-syntax). For example use cases of the operators, see [Resource attribute-based conditions](/docs/account?topic=account-iam-condition-properties&interface=ui#resource-based-conditions).
{: #string-compare-intro-reuse}

| Operator   | Description  |
|------------|--------------|
| `stringEquals`  | Case-sensitive string comparison. Boolean or number values are converted into a string before comparison. |
| `stringMatch`  | Case-sensitive string match is performed between the pattern and the target string by using either an asterisk (`*`), question mark (`?`), or both. An asterisk (`*`) represents any sequence of zero or more characters in the string, and a question mark (`?`) represents any single character. You can also express an asterisk `*` and question mark `?` as a literal value by enclosing each within two sets of curly brackets `{{}}`. |
| `stringExists`  |  Boolean where `true` indicates that the string must be present and can be empty. `false` indicates that the string must not be present. |
| `stringEqualsAnyOf` | Case-sensitive exact string matching any of the strings in an array of strings. Limit of 10 values. |
| `stringMatchAnyOf` | Case-sensitive string matching any of the strings in an array of strings. The values can include a multi-character wildcard (`*`), which matches any sequence of zero or more characters, a single-character wildcard (`?`), matching any single character, or both. You can also express an asterisk `*` and question mark `?` as a literal value by enclosing each within two sets of curly brackets `{{}}`. Limit of 10 values. |
{: caption="Table 3. The string comparison operators available for conditions in access policies." caption-side="top"}
{: #string-compare-table-reuse}

<!--- H3 "Federating users to IBM Cloud" is used in iam-identities.md and iam-mappings.md--->

{{site.data.content.federation-iam}}

### Federating users to {{site.data.keyword.cloud_notm}}
{: #federation-iam}

{{site.data.keyword.cloud_notm}} offers two ways for you to federate your corporate identity provider (IdP), which simplifies login by giving your employees access to {{site.data.keyword.cloud_notm}} with their company username and password. You can [federate with IBMid](https://www.ibm.com/docs/en/ief){: external}, or you have the option to create an {{site.data.keyword.appid_full_notm}} service instance and use that as a way to federate users into an {{site.data.keyword.cloud_notm}} account. For more information, see [Enabling authentication from an external identity provider](/docs/account?topic=account-idp-integration).

Both federation options require that the user is a member of the account, or has access to the account by a trusted profile to be able to complete operations. If trusted profiles are not configured, the account owner or administrator must invite individual IBMids into the {{site.data.keyword.cloud_notm}} account. Only if the invited IBMid accepts the invitation is the user added the account as an active user. In the case of {{site.data.keyword.appid_short}}, the user is automatically onboarded to {{site.data.keyword.cloud_notm}} without a need to invite each user to the account. In both types of federation, the users are active {{site.data.keyword.cloud_notm}} account users that can access the platform, including IAM-enabled resources and classic infrastructure all depending on their assigned access.

Trusted profiles deal with federated users differently. If the customer federates their corporate IdP, users from that IdP aren't added to an account as what we might consider a typical user. Instead, users' SAML-based IdP attributes are evaluated at login and if they meet all of the conditions for a trusted profile, they are prompted to apply one or more trusted profiles. Trusted profiles grant users the level of access that they need to complete specialized and specific tasks in a limited time-period, for example, 1 - 4 hours. Time-based access allows frequent authentication checks for reduced security risks. These are usually critical tasks that you would want to avoid doing unintentionally in daily work. Users don't need to onboard to IBM Cloud, they're automatically added through the trust relationship. If a user leaves your company, you can delete the user's corporate identity in your directory, which revokes access to {{site.data.keyword.cloud_notm}}.
