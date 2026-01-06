---

copyright:

  years: 2022, 2026
lastupdated: "2026-01-06"

keywords: software onboarding, controls, requirements, security, compliance, partners

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Adding compliance details
{: #catalog-format-controls}

During the onboarding process, controls that are in your readme file, formatted correctly, and supported by {{site.data.keyword.sysdigsecure_full}} appear in the controls table in your private catalog. You can click **Add controls** to add additional controls to your version. After you publish your product, users can view your controls on the About page for your product.

## Formatting controls in your readme file
{: #catalog-control-format}

To include controls with your product's information, include them in your readme file and make sure that the controls are listed in one table. The table must include the following columns:

- A Profile column
- An ID column

You can include more columns in the readme file's control table but this information might be overwritten or excluded.

### Examples
{: #catalog-controls-example}

For examples of how you can format your controls in your readme file, see the following tables:

```markdown
| Profile | ID |
|---------|----|
| NIST | SC-7(3) |
```
{: codeblock}

```markdown
| Profile | Category | ID      | Description |
|---------|----------|---------|-------------|
| NIST | [SC-7](/docs/framework-financial-services-controls?topic=framework-financial-services-controls-sc-7) | SC-7(3) | Limit the number of external network connections to the system. |
```
{: codeblock}

## Managing compliance for your product
{: #managing-compliance}

You can add controls to your software to prove that it meets security and compliance requirements. To claim compliance, you must add inventory results from {{site.data.keyword.sysdigsecure_short}}. Only controls that are supported by {{site.data.keyword.sysdigsecure_short}} appear in the catalog. You can add controls from policies and import controls from module references.

You must validate your product version before you can add inventory results from {{site.data.keyword.sysdigsecure_short}}.
{: important}

### Adding controls
{: #add-controls-sw}

To add controls, complete the following steps:

1. On the Manage compliance page, select **Add controls**.
1. Select a {{site.data.keyword.sysdigsecure_short}} instance, then a policy.

    If you haven't provisioned a {{site.data.keyword.sysdigsecure_short}} instance yet, you must [set up one](/docs/workload-protection?topic=workload-protection-provision&interface=ui) from the {{site.data.keyword.cloud_notm}} catalog and [enable Cloud Security Posture Management (CSPM)](/docs/workload-protection?topic=workload-protection-cspm-implement&interface=ui) for your {{site.data.keyword.cloud_notm}} account. Then, complete the steps to [integrate with either an existing {{site.data.keyword.sysdigsecure_short}} instance or a new instance](/docs/workload-protection?topic=workload-protection-cspm-implement&interface=ui).
    {: important}

1. Select whether you want to add the entire policy or only a subset of controls.
1. If you select to add an entire policy, continue to the next step. If you select to add a subset of controls, select the controls that you want to add.
1. Click **Add**.

### Adding inventory results from {{site.data.keyword.sysdigsecure_short}}
{: #add-inventory-results}

You can add inventory results from {{site.data.keyword.sysdigsecure_short}} so that users can see the claimed compliance when they evaluate your product in the catalog.

In {{site.data.keyword.sysdigsecure_short}}, your inventory is updated once every day. You must deploy your resources and wait for the inventory to be updated before you add the inventory to your catalog listing. For more information, go to [Inventory](/docs/workload-protection?topic=workload-protection-inventory).
{: important}

To add inventory results, complete the following steps:

1. On the Manage compliance page, click **Add results**.
1. Select the {{site.data.keyword.sysdigsecure_short}} instance that you provisioned previously.
1. Click **Apply** to apply the latest inventory results.
