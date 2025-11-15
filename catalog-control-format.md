---

copyright:

  years: 2022, 2025
lastupdated: "2025-11-15"

keywords: software onboarding, controls, requirements, security, compliance, partners

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Adding compliance details
{: #catalog-format-controls}

During the onboarding process, controls that are in your readme file, formatted correctly, and supported by Security and Compliance Center appear in the controls table in your private catalog. You can click **Add controls** to add additional controls to your version.  After you share your product or publish to your account, users can view your controls on the About page for your product.

If you want to include custom controls with your product, see [Building custom profiles](/docs/security-compliance?topic=security-compliance-build-custom-profiles&interface=ui).
{: note}

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
| NIST | [SC-7](https://test.cloud.ibm.com/docs/framework-financial-services-controls?topic=framework-financial-services-controls-sc-7) | SC-7(3) | Limit the number of external network connections to the system. |
```
{: codeblock}

## Managing compliance information for your product
{: #managing-compliance}

After you add your controls, you must run a Code Risk Analyzer scan and add a Security and Compliance Center scan.

You must validate your version before you can run a Code Risk Analyzer scan or add a Security and Compliance Center scan.
{: important}

### Running Code Risk Analyzer scan
{: #catalog-cra-scan}

Scan your source code with Code Risk Analyzer to identify any security vulnerabilities that you need to address.

1. Click **Run scan**.
2. Wait for scan to finish.

### Adding a {{site.data.keyword.compliance_short}} scan
{: #submit-scc-scan}

To include controls with your product, you must add scans that you previously ran in the Security and Compliance Center. Security and Compliance Center scans determine adherence to regulatory controls. For more information, see [Running a scan on demand](/docs/security-compliance?topic=security-compliance-attachments#scan-ondemand).

1. On the Manage compliance page go to **Add Security and Compliance Center scan** and select a profile that you previously scanned.
1. Select a Security and Compliance Center scan.
   If you don't see any scans, you need to run a scan in Security and Compliance Center. For more information, see [Running a scan on demand](/docs/security-compliance?topic=security-compliance-attachments#scan-ondemand)..
1. Click **Add scan**.

These results are displayed on your About page for your product as evidence that the controls that you listed for your product are validated as compliant.
