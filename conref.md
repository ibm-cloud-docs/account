---

copyright:

  years: 2022, 2025
lastupdated: "2025-11-15"

keywords:

subcollection: account

content-type: conref

---

{{site.data.keyword.attribute-definition-list}}

# Content references for account subcollection
{: #conref-example}

The following H2s and H3s are going to be reused in several different topics that need identical information.
{: shortdesc}

* H2 - **Define IAM access** is used in the following files:
   * catalog-vsi-tutorial.md
   * catalog-vsipower-tutorial.md
   * catalog-terraform-template-tutorial.md

   See `define-iam-segment.md`.

   {{_include-segments/define-iam-segment.md}}

* H3 - **Edit output value descriptions** is used in the following files:
   * catalog-vsi-tutorial.md
   * catalog-vsipower-tutorial.md
   * catalog-terraform-template-tutorial.md

   See `edit-output-segment.md`.

   {{_include-segments/edit-output-segment.md}}

* H2 - **Manage compliance** is used in the following files:
   * catalog-vsi-tutorial.md
   * catalog-vsivpc-tutorial.md
   * catalog-vsipower-tutorial.md
   * catalog-operator-tutorial.md
   * catalog-opbundle-tutorial.md
   * catalog-terraform-template-tutorial.md

   See `manage-compliance-segment.md`.

   {{_include-segments/manage-compliance-segment.md}}

* Paragraph - Intro to **String comparisons** is used in the following files:
   * known-issues.md
   * iam-wildcard.md
   * iam-condition-properties.md

{{_include-segments/string-compare-intro-reuse.md}}

The following table lists the string comparison operators that you can use to build access policies with `/v2/policies` syntax. For more information about each version, see [Comparing `/v1/policies` and `/v2/policies` syntax](/docs/account?topic=account-known-issues#compare-syntax). For example use cases of the operators, see [Resource attribute-based conditions](/docs/account?topic=account-iam-condition-properties&interface=ui#resource-based-conditions).
{: #string-compare-intro-reuse}

* Table - **String comparisons** is used in the following files:
   * known-issues.md
   * iam-wildcard.md

{{_include-segments/string-compare-table-reuse.md}}

| Operator   | Description  |
|------------|--------------|
| `stringEquals`  | Case-sensitive string comparison. Boolean or number values are converted into a string before comparison. |
| `stringMatch`  | Case-sensitive string match is performed between the pattern and the target string by using either an asterisk (`*`), question mark (`?`), both, or none (same as literal value). An asterisk (`*`) represents any sequence of zero or more characters in the string, and a question mark (`?`) represents any single character. You can also express an asterisk `*` and question mark `?` as a literal value by enclosing each within two sets of curly brackets `{{}}`. |
| `stringExists`  |  Boolean where `true` indicates that the string must be present and can be empty. `false` indicates that the string must not be present. |
| `stringEqualsAnyOf` | Case-sensitive exact string matching any of the strings in an array of strings. Limit of 10 values. |
| `stringMatchAnyOf` | Case-sensitive string matching any of the strings in an array of strings. The string values can include either an asterisk (`*`), question mark (`?`), both, or none (same as literal value). An asterisk (`*`) represents any sequence of zero or more characters in the string, and a question mark (`?`) represents any single character. You can also express an asterisk `*` and question mark `?` as a literal value by enclosing each within two sets of curly brackets `{{}}`. Limit of 10 values. |
{: caption="The string comparison operators available for conditions in access policies." caption-side="top"}
{: #string-compare-table-reuse}

* H3 - **Federating users to IBM Cloud** is used in the following files:
   * iam-identities.md
   * iam-mappings.md

{{_include-segments/federating-segment.md}}
