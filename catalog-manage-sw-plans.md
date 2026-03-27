---


copyright:

  years: 2024, 2026
lastupdated: "2026-03-27"

keywords: onboard software, pricing plans, manage plans, usage-based plan, software, catalog, partner center, catalog, private catalog, catalog management

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Managing software plans in catalogs
{: #sw-manage-plans}

When you onboard your software to a catalog, you must define a pricing model for it. Currently, {{site.data.keyword.cloud_notm}} supports free, usage-based, and bring your own license (BYOL) plans that you can add to a specific version of your software. By adding pricing plans, you are indicating whether you offer your product as a paid integrated product and customers need to pay to use it, as a product that customers need to purchase a license for, or as a product that does not require any payment or license to use.
{: shortdesc}

After adding a plan to your software in Partner Center, you can manage it in your catalog as well. Managing your plan includes adding features to it, viewing associated licenses, changing the state of the plan, deprecating it, or updating plan details.

Usage-based pricing plans are available only for software that is onboarded with the virtual server image delivery method.
{: note}

## Before you begin
{: #prereqs-manage-plans-cm}

Before you can manage pricing plans in your catalog, complete the following tasks:

1. Onboard software to your account. For more information, see [Onboarding software to your account](/docs/account?topic=account-create-private-catalog&interface=ui).
1. Define your pricing model for your software by completing the following steps:
    1. In the {{site.data.keyword.cloud_notm}} console, click **Manage > Catalogs > Private catalogs**.
    1. Select the private catalog that contains the software that you want to add a plan to.
    1. Select the product in your catalog that you want to add a plan to and click **Actions... > Manage in Partner Center**.
    1. In Partner Center, go to **Pricing**, and click **Add plan**. To add a specific type of pricing plan to your software, follow the instructions in the [Defining your pricing model for software](/docs/sell?topic=sell-sw-pricing) documentation.

## Adding features to a pricing plan
{: #add-pricing-plan-features}

You can add a list of features that identifies and differentiates your pricing plan. By providing a list of features, you can help customers choose the most suitable pricing plan.

You must add features to your plan before you can publish it.
{: important}

To add features to your pricing plan, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage > Catalogs > Private catalogs**.
1. Select the private catalog that contains your software.
1. Select the product in your catalog with the pricing plan that you want to add features to.
1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") in the **Features** section.
1. Click **Add feature** and provide a descriptive title and a brief description for each feature.
1. Click **Save**.

## Providing plan evidence
{: #provide-plan-evidence}

To review how customers understand and experience your pricing plan, and validate that your metered plans are correctly configured, you must submit the resource usage for your software instance. Submitting your resource usage includes calling the Usage Metering API and providing the evidence of your testing.

You must provide evidence for your pricing plan and receive approval for it before you can publish the plan.
{: important}

To provide pricing plan evidence, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage > Catalogs > Private catalogs**.
1. Select the private catalog that contains your software.
1. Select the product in your catalog with the pricing plan that you want to provide evidence for.
1. Click **Pricing plans** and select the plan that you want to provide evidence for.
1. Click **Actions... > Provide plan evidence**. This step takes you to Partner Center.
1. In Partner Center, click **Test estimation and metering** and provide your metering evidence details. For more information, see [Gather usage information from the running software instance](/docs/account?topic=account-working-catalog-vsivpc-tutorial#working-gather-usage).

## Changing the state of a pricing plan
{: #change-plan-state}

Software pricing plans can have one of the following states: `draft`, `evidence accepted`, `published`, `deprecated`, or `archived`. After you add a plan to your product, the plan is automatically in the `draft` state first. Plans in the `draft` and `evidence accepted` states are visible and usable by editors of the private catalog. However, if your product is published, but your plan is still in the `draft` state, it will not be available to others without editor access. To make a plan available with your product in the catalog, you must publish your plan as well.

To remove a pricing plan, deprecate it first. The plan remains available during a 90-day deprecation period and is archived after 90 days.

### Publishing a plan
{: #plan-publish}

After you provide metering evidence, add features to your plan, and your plan details are approved in Partner Center, you can make your plan available for use and change its state to `published`. To publish your plan, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage > Catalogs > Private catalogs**.
1. Select the private catalog that contains your software.
1. Select the product in your catalog with the pricing plan that you want to publish.
1. Click **Pricing plans** and select the plan that you want to publish.
1. Click **Actions... > Publish plan > Yes**.

### Deprecating a plan
{: #plan-deprecate}

To deprecate your plan, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage > Catalogs > Private catalogs**.
1. Select the private catalog that contains your software.
1. Select the product in your catalog with the pricing plan that you want to deprecate.
1. Click **Pricing plans** and select the plan that you want to deprecate.
1. Click **Actions... > Deprecate plan > Yes**.

## Updating pricing plan details
{: #update-pricing-plan-details}

You can update certain pricing plan details from your catalog, including the pricing plan name, description, and the version range that the plan applies to. 

With version ranges, you can specify all versions of your software so that the plan is still applicable to newer versions as they are released. You can't remove a published plan from a published version by changing the version range. You must either deprecate the plan or deprecate the version.
{: note}

Complete the following steps to make any updates to your plan details:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage > Catalogs > Private catalogs**.
1. Select the private catalog that contains your software.
1. Select the product in your catalog with the pricing plan that you want to make updates to.
1. In the **Pricing plan details** section, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") and update the **Name**, **Description**, and **Version range** fields if needed.
1. Click **Save**.

Pricing plan details, such as name and description can be updated from Partner Center as well. However, managing plan metrics is available only from Partner Center until your plan is published.
{: note}

## Viewing plan metrics
{: #view-plan-metrics}

For software instances with usage-based pricing plans, you can view the metrics that are used to calculate charges for your software. The **Plan metrics** section displays detailed information about each metric, including the unit display name, unit name, charge unit quantity, and price. For more information, see [Adding metrics to your software](/docs/sell?topic=sell-software-add-metrics).

To view plan metrics for your software instance, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Resource list**.
1. Expand the **Compute** section and select your software instance.
1. In the navigation menu, click **Pricing plan**.
1. In the **Plan metrics** section, review the metrics that are associated with your pricing plan.
1. Use the search field to filter metrics by name or unit.
1. Review the following information for each metric:
   * **Unit display name**: The name of the metric unit
   * **Unit name**: The technical identifier for the metric unit
   * **Charge unit quantity**: The quantity of units that are charged
   * **Price**: The cost per unit

For usage-based pricing plans, metrics are automatically tracked and reported through the Usage Metering API. For more information about configuring and testing metrics, see [Defining your pricing model for software](/docs/sell?topic=sell-sw-pricing). 

## Viewing plan licenses
{: #view-plan-licenses}

When you onboard your product to {{site.data.keyword.cloud_notm}}, you must define a pricing model for your software in Partner Center. If you choose to add a usage-based pricing plan for your software, you can optionally include licenses in the plan. Licenses allow your customers to select licensed plans directly from the catalog, without needing to manage them separately outside of {{site.data.keyword.cloud_notm}}.

Adding licenses to a pricing plan is available only for select IBM Business Partners. License entitlements require a configured license provider, which defines the license for your product. For more information, contact [{{site.data.keyword.cloud_notm}} Support](/unifiedsupport/supportcenter){: external}.
{: preview}

For software instances with usage-based pricing plans, you can view license information that is associated with your deployed software. The **Plan licenses** section displays the entitlement ID and detailed license information, including the license name, provider, and vendor. 

Licenses are restricted on specific accounts, so you must be on the provider’s license visibility list to add licenses to your pricing plan, and then view certain license details. 

If your account doesn't have access to see full details of the license, you can view only the license name, provider ID, and vendor details.
{: note}

To view plan licenses for your software instance, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Resource list**.
1. Expand the **Compute** section and select your software instance.
1. In the navigation menu, click **Pricing plan**.
1. In the **Plan licenses** section, review the entitlement ID and license details.
