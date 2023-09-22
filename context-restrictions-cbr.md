---

copyright:
  years:  2023
lastupdated: "2023-09-22"

keywords: cbr, context-based restrictions, protecting cbr resources, security

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Protecting context-based restrictions resources with context-based restrictions
{: #context-restrictions-cbr}

Context-based restrictions can define and enforce access restrictions for its own {{site.data.keyword.cloud}} resources. You can define these restrictions based on contexts, such as network zones and endpoint types. For more information, see [What are context-based restrictions](/docs/account?topic=account-context-restrictions-whatis&interface=ui).
{: shortdesc}

The context-based restriction service manages rules and network zones, so it is possible to lose all ability to manage these resources if you cannot satisfy a rule on the context-based restriction service. Attempts to create or update such a rule are permitted only if the context of the request satisfies the new or modified rule.

If you can no longer satisfy a rule that targets the Context-based restrictions service, [open a support case](/unifiedsupport/cases/form) and provide a context that you can satisfy to restore your access.
{: tip}

## Restricting the ability to manage rules and network zones
{: #cbr-rules-ui}
{: ui}

To configure this rule, target the **Context-based restrictions** service. For more information about the steps to set up a rule, see [Creating rules](/docs/account?topic=account-context-restrictions-create&interface=ui#context-restrictions-create-rules).

A rule scoped to **All resources** is applicable to all current and future resources that are managed by the service. If you want to restrict operations for a specific resource, scope the rule to **Specific resources > Resource type**.

To complete any rule or network zone management operation, a user must be assigned the correct role with an IAM access policy and they must satisfy the context-based restrictions rule.
{: note}

## Restricting the ability to manage rules and network zones by using the API
{: #cbr-rules-api}
{: api}

The following example shows a rule in JSON format that protects rule and network zone management operations:

```json
{
  "resources": [
    {
      "attributes": [
        {
          "name": "accountId",
          "value": "my-AccountID"
        },
        {
          "name": "serviceName",
          "value": "context-based-restrictions"
        }
      ]
    }
  ],
  "description": "",
  "contexts": [
    {
      "attributes": [
        {
          "name": "networkZoneId",
          "value": "my-zoneID"
        }
      ]
    }
  ],
  "enforcement_mode": "report"
}
```
{: curl}
{: codeblock}

A rule that specifies only the `accountId` and `serviceName` resource attributes is applicable to all current and future resources that are managed by the service. If you want to restrict operations for a specific resource, include the corresponding `resourceType` resource attribute.  Valid `resourceType` values for the Context-based restrictions service are `rule` and `zone`.

To complete any rule or network zone management operation, a user must be assigned the correct role with an IAM access policy and they must satisfy the context-based restrictions rule.
{: note}
