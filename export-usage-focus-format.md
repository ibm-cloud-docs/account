---

copyright:
  years: 2026

lastupdated: "2026-04-22"

keywords: usage export, FOCUS format, FinOps, cost management, billing data, CSV export, multi-cloud, cost optimization, FOCUS v1.2

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Exporting usage data in FOCUS format
{: #export-usage-focus}

Export your {{site.data.keyword.cloud}} usage data in FinOps Open Cost & Usage Specification (FOCUS) format to simplify multi-cloud cost management and enable seamless integration with FinOps tools.
{: shortdesc}

The FOCUS format is a cross-cloud standard developed by the FinOps Foundation that normalizes billing and usage data across cloud providers. {{site.data.keyword.Bluemix_notm}} now supports FOCUS v1.2 (FinOps Open Cost and Usage Specification) format for cost and usage reporting. By exporting your {{site.data.keyword.cloud_notm}} usage data in FOCUS format, you can analyze {{site.data.keyword.Bluemix_notm}} costs alongside AWS, Azure, and GCP data without custom transformation. For more information, see the [FinOps Foundation FOCUS v1.2 specification](https://focus.finops.org/focus-specification/v1-2/).

## Before you begin
{: #export-focus-prereqs}

Before you export usage data in FOCUS format, ensure that you have the following access and resources:

* Billing Administrator or Account Owner access to the {{site.data.keyword.cloud_notm}} account
* Access to the {{site.data.keyword.cloud_notm}} console or CLI
* Understanding of your cost management and FinOps tool requirements

## Understanding FOCUS format benefits
{: #focus-benefits}

The FOCUS format provides several advantages for managing your cloud costs:

Enhanced multi-cloud visibility
:   Normalize {{site.data.keyword.Bluemix_notm}} usage data with AWS Cost and Usage Reports (CUR), Azure CSV exports, and GCP billing data for unified cost analysis.

Direct tool integration
:   Import FOCUS-formatted data directly into FinOps platforms such as Apptio Cloudability, CloudHealth, Kubecost, and other cost optimization tools without custom transformation scripts.

Reduced onboarding time
:   Eliminate manual data transformation processes, reducing the time and cost required to integrate {{site.data.keyword.Bluemix_notm}} billing data into your cost management workflows.

Improved transparency
:   Access standardized billing dimensions that align with industry best practices, making it easier to understand and validate your {{site.data.keyword.Bluemix_notm}} charges.

Competitive parity
:   Benefit from the same standardized format used by other leading cloud service providers, ensuring consistent cost management practices across your multi-cloud environment.

## Exporting usage data
{: #export-instance-level}
{: ui}

Instance-level usage data provides granular details about individual resource instances, enabling detailed cost allocation and chargeback.

1. Log in to the [{{site.data.keyword.cloud_notm}} console](https://cloud.ibm.com){: external}.
2. Go to **Manage** > **Billing and usage** > **Usage**.
3. Click **FOCUS** button. The system downloads a CSV file containing instance-level usage data in FOCUS v1.2 format, with additional columns for resource-specific details.

### Fully Supported Fields
{: #account-focus-columns}

IBM CSV file includes all mandatory FOCUS v1.2 fields:

| Field | Type | Description |
| ----- | ---- | ----------- |
| `BilledCost` | Decimal | Cost billed to customer |
| `BillingCurrency` | String | Currency code (ISO 4217) |
| `ChargeCategory` | String | Type of charge (Usage, Purchase, Tax, Adjustment) |
| `ChargeDescription` | String | Description of the charge |
| `ChargePeriodEnd` | DateTime | End of charge period (ISO 8601) |
| `ChargePeriodStart` | DateTime | Start of charge period (ISO 8601) |
| `EffectiveCost` | Decimal | Amortized cost after discounts |
| `ListUnitPrice` | Decimal | List price per unit before discounts |
| `PricingCategory` | String | Pricing model |
| `PricingQuantity` | Decimal | Quantity used for pricing |
| `PricingUnit` | String | Unit of measure for pricing |
| `ProviderName` | String | Always "IBM" |
| `PublisherName` | String | Service publisher name |
| `ResourceId` | String | Unique resource identifier |
| `ResourceName` | String | Resource name |
| `ServiceCategory` | String | High-level service category |
| `ServiceName` | String | Name of the service |
| `SkuId` | String | SKU identifier |
{: caption="Fully supported MUST fields" caption-side="bottom"}

### Additional Supported Fields
{: #additional-focus-fields}

Beyond the 16 mandatory fields, {{site.data.keyword.Bluemix_notm}} FOCUS reports include 39 additional fields:

| Category | Field Name |
| --- | --- |
| **Account & Billing:** | `BillingAccountId`, `BillingAccountName`, `BillingAccountType`, `BillingPeriodEnd`, `BillingPeriodStart`, `InvoiceIssuerName` |
| **Geographic:** | `AvailabilityZone`, `RegionId`, `RegionName` |
| **Commitment & Discount:** | `CommitmentDiscountCategory`, `CommitmentDiscountId`, `CommitmentDiscountName`, `CommitmentDiscountType`, `CommitmentDiscountUnit` |
| **Cost Breakdown:** | `ContractedCost`, `ContractedUnitPrice`, `ListCost` |
| **Charge Details:** | `ChargeClass`, `ChargeFrequency` |
| **Consumption:** | `ConsumedQuantity`, `ConsumedUnit` |
| **Pricing:** | `PricingCurrency`, `SkuMeter` |
| **Resource Metadata:** | `ResourceType`, `ServiceSubcategory`, `Tags` |
| **IBM-Specific Extensions:** | `x_DiscountId`, `x_DiscountName`, `x_DiscountQuantity`, `x_OfferId`, `x_OfferCredit` |
{: caption="Additional supported fields" caption-side="bottom"}

## Exporting usage data using the API
{: #export-focus-api}
{: api}

You can automate usage data exports using the {{site.data.keyword.cloud_notm}} Usage Reports API. For more information, see [Usage Reports API](/apidocs/metering-reporting?code=python#get-resource-usage-account-focus).

1. Obtain an API key with appropriate billing access. For more information, see [Managing API keys](/docs/iam?topic=iam-userapikey).

2. Use the following API endpoint to export usage data:

   ```bash
   curl -X GET "https://billing.cloud.ibm.com/v4/accounts/{account_id}/focus/{month}" \
     -H "Authorization: Bearer {iam_token}" \
     -H "Accept: text/csv"
   ```
   {: pre}

3. For instance-level usage data, use the following endpoint:

   ```bash
   curl -X GET "https://billing.cloud.ibm.com/v4/accounts/{account_id}/focus/{month}" \
     -H "Authorization: Bearer {iam_token}" \
     -H "Accept: text/csv"
   ```
   {: pre}

Replace `{account_id}` with your {{site.data.keyword.Bluemix_notm}} account ID (required), `{month}` with the report month in YYYY-MM format (e.g., 2024-01), and `{iam_token}` with your IAM access token.

### API parameters
{: #api-parameters}

The FOCUS export API supports the following parameters:

`account_id` (required)
:   The {{site.data.keyword.Bluemix_notm}} account ID.

`month` (required)
:   Report month in YYYY-MM format (e.g., 2024-01).

**Headers:**

`Authorization` (required)
:   Bearer token for IAM authentication.

`x-focus-version` (optional)
:   FOCUS version to use (default: 1.2). Set to `true` to bypass cache and generate fresh report.

**Query Parameters:**

`_limit` (optional)
:   Pagination limit, max 250 (default: 200).

**Validating FOCUS format exports:**

To ensure your exported data meets FOCUS v1.2 specifications, you can validate the files using the FOCUS validator tool from the FinOps Foundation. The {{site.data.keyword.cloud_notm}} FOCUS exports are designed to pass validation with 100% compliance on all 16 mandatory MUST fields.

## Comparing IBM native and FOCUS v1.2 formats
{: #compare-formats}

Both IBM native and FOCUS v1.2 formats are available for usage exports. The following table highlights key differences:

| Aspect | IBM Native Format | FOCUS v1.2 Format |
| ------ | ----------------- | ----------------- |
| Column names | IBM-specific naming conventions | Standardized FOCUS v1.2 column names |
| Multi-cloud compatibility | {{site.data.keyword.Bluemix_notm}} only | Compatible with AWS, Azure, GCP |
| FinOps tool support | Requires custom transformation | Direct import supported |
| Data granularity | Same level of detail | Same level of detail |
| Compliance | IBM-specific | 100% compliant with FOCUS v1.2 (16/16 MUST fields) |
| Use case | IBM-specific analysis and reporting | Multi-cloud cost management and FinOps tools |
{: caption="Format comparison" caption-side="bottom"}

You can export data in both formats simultaneously to support different use cases within your organization.

## Next steps
{: #export-focus-next-steps}

After exporting your usage data in FOCUS format, you can:

* [Configure cost allocation tags](/docs/account?topic=account-tag) to improve cost attribution and chargeback
* [Analyze your usage](/docs/account?topic=account-viewingusage) to identify cost optimization opportunities
* [Implement FinOps best practices](https://www.finops.org/framework/){: external} for cloud cost optimization
