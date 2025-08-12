## Manage compliance
{: #manage-compliance}
{: step}

You can add profiles and controls to your software to prove that it meets security and compliance requirements. You must use {{site.data.keyword.compliance_short}} to scan the resources created during validation.

Only profiles and controls that are supported by the {{site.data.keyword.compliance_short}} and validated by {{site.data.keyword.compliance_short}} scans appear in the catalog.

### Run a Security and Compliance Center scan
{: #run-scc-compliance-center-scan}
{: ui}

When you claim profiles and controls, you must evaluate the resources that were created during validation to ensure compliance. To run a scan, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) **> Security and Compliance** to access {{site.data.keyword.compliance_short}}.
2. In the navigation, click **Profile**.
3. Click the **Overflow** menu in the row of the profile that you want to evaluate and select **Run scan**.
4. Click **Run scan**.

After your scan completes, you can return to your private catalog to continue the onboarding process.

### Adding compliance controls
{: #adding-compliance-control}
{: ui}

Add the profiles and controls that you want to claim.

1. In the Manage compliance section of your product, select **Add claims**.
1. Select the profile that you want to add.
1. Choose to add the entire profile or a subset of controls.
1. If you choose an entire profile, continue to the next step. If you choose to add a subset of controls, select the controls that you want to add.
1. Click **Add**.

### Applying {{site.data.keyword.compliance_short}} scans
{: #apply-scc-scan}
{: ui}

Add the scans that you previously ran in the {{site.data.keyword.compliance_short}}. {{site.data.keyword.compliance_short}} scans determine adherence to regulatory controls. For more information, see [Scanning your resources](/docs/security-compliance?topic=security-compliance-scan-resources).

1. Click **Add scan**.
1. Select the profile that you used for the evaluation.
1. Select the {{site.data.keyword.compliance_short}} scan.
1. Click **Apply scan**.
1. Click **Next**.
