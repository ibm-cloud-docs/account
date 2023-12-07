---

copyright:
  years: 2022, 2023

lastupdated: "2023-12-07"

keywords:

subcollection: overview

content-type: conref

---

{{site.data.keyword.attribute-definition-list}}

# Content references for account subcollection.
{: #conref-example}

The following H2s and H3 sare going to be reused in several different topics that need identical information.
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
