---


copyright:
  years: 2024
lastupdated: "2024-05-30"

keywords: onboard software, pricing plans, manage plans, usage-based plan, software, catalog, partner center, catalog, private catalog, catalog management

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Managing software plans in catalogs
{: #sw-manage-plans}

When you onboard your software to a catalog, you must define a pricing model for it. Currently, {{site.data.keyword.cloud_notm}} supports free, usage-based, and bring your own license (BYOL) plans that you can add to a specific version of your software. By adding pricing plans, you are indicating whether you offer your product as a paid integrated product and customers need to pay to use it, as a product that customers need to purchase a license for, or as a product that does not require any payment or license to use. 
{: shortdesc}

After adding a plan to your software in Partner Center, you can manage it in your catalog as well. Managing your plan includes adding features to it, changing the state of the plan, deprecating it, or updating plan details.

Usage-based pricing plans are available only for software that are onboarded with the virtual server image delivery method.
{: note}

## Before you begin
{: #prereqs-manage-plans-cm}

Before you can review and manage pricing plans in your catalog, complete the following tasks:

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

If you need to permanently delete your pricing plan, you can deprecate it first. That way, your plan remains available during a 90-day deprecation period, and will be archived after 90 days.

### Publishing a plan
{: #plan-publish}

After you provided metering evidence, added features to your plan, and your plan details are approved in Partner Center, you can make your plan available for use and change its state to `published`. To publish your plan, complete the following steps:

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
1. Click **Pricing plans** and select the plan that you want to publish.
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
