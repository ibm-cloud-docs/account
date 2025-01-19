---
copyright:
  years: 2024
lastupdated: "2025-01-17"

keywords: location management, locations, region

subcollection: hybrid-workloads

---

{{site.data.keyword.attribute-definition-list}}


# Managing workload deployment locations
{: #managing_locations}

As an administrator on the Catalog management service, you can manage the list of allowed workload deployment locations for your account or enterprise. Deploy your apps to the location that is nearest to your customers to achieve low application latency and to meet data residency requirements.
{: shortdesc}

{{site.data.keyword.Bluemix_notm}} has a resilient global network of region and data center locations. Deploying your workload to the public cloud might not always align with your latency or data residency needs, especially for industries with strict data governance regulations. You can use {{site.data.keyword.satellitelong}} to create a representation of an environment in your infrastructure provider, like an on-premises data center, and manage hybrid deployment locations from a single pane of glass in the {{site.data.keyword.Bluemix_notm}} console.

## Before you begin
{: #before_begin}

- You must be an Administrator on the Catalog management service to edit the location filters. Otherwise, the page is read only.
- Create a Satellite location. Depending on your infrastructure provider, you have different options to create a Satellite location. For more information, see [Create a Satellite location overview](/docs/satellite?topic=satellite-locations).
- Editing the location filters for an account, enterprise, or account group affects the resources that users can view in the {{site.data.keyword.Bluemix_notm}} catalog in those accounts. Users can view only services that are available in the locations that you allow. For more information, see [Service and infrastructure availability by location](/docs/overview?topic=overview-services_region).

## Setting location filters for an account
{: #location_filters}

Add and remove allowed locations by applying filters. The filter or combination of filters that you apply determines the list that you view in the Locations section.

To set the location filters, complete the following steps:

1. In the {{site.data.keyword.Bluemix_notm}} console, go to **Manage** > **Catalog** > **Locations**.
1. Switch to the enterprise account, if applicable, by using the account switcher that's located in the console header.
   1. Keep the account group scoped to None to apply your allowlist to the entire enterprise.
   1. Click **Change** to scope the allowlist to a specific account group.

   To view and manage locations for an individual account, you must switch to that account. If an allowlist is set at the enterprise level, individual accounts can still manage their own allowlists. However, individual accounts can manage only locations within the enterprise allowlist.
   {: note}

1. Filter to the deployment locations that you want to allow.
   * Enable applicable toggles. For example, you might have sensitive data and want to keep workloads on-premises to ensure that data is stored within a controlled and secure environment. In that case, enable On-premises to filter to locations that your organization hosts locally on your own physical infrastructure.
   * Click **More filters** to refine your search to different location parameters, like geography or country.
   * Manually query the filter locations search bar and specify a combination of location parameters.

   The toggles and filters are most effective for straightforward location combinations or for grasping the workings of the filtering syntax. You can see how the advanced syntax develops in the search bar as you adjust the toggles and filters. To create more complex combinations, see [Filtering syntax](/docs-draft/hybrid-workloads?topic=hybrid-workloads-managing_locations#filtering_syntax).
   {: note}

1. Click **Revert to saved filter** if you want to keep exploring all available deployment locations.
1. Or, click **Save filter** to apply your allowlist.

Expand the **Change logs** section to view a history of changes to the allowlist and who made them.
{: tip}

## Filtering syntax
{: #filtering_syntax}

The search bar provides you with the most flexible way to search for and combine different location criteria, such as specific capabilities or by region ID. You can combine these criteria by using the following operators to define your workload deployment allowlist:
* `|` to designate OR
* `^` to designate AND
* `(,)` for grouping

### Location parameters
{: #define_dimensions}

Filter by different location parameters by using the syntax shown in each example.

| Parameter                          | Example                          | Description                                    |
|------------------------------------|----------------------------------|------------------------------------------------|
| Geography                          | `geo_id:na,ap`                   | Geography ID is either `na` or `ap`            |
| Country                            | `country_id:us,ca,jp`            | Country ID is either `us`, `ca`, or `jp`       |
| Region ID                          | `id:a,b,c`                       | Region ID is either `a`, `b`, `c`              |
| Metro                              | `metro_id:dal`                   | Metro ID is `dal`                              |
| Capability                         | `cap:on-prem`                    | Capability on-premises is registered               |
| Tag                                | `tag:t1`                         | Regions with a `t1` tag                        |
| Location type                      | `public:false`                   | Private regions                                |
| Kind                               | `kind:region`                    | [Group of one or more zones](/docs/overview?topic=overview-locations#table-mzr)|
{: caption="Example syntax for different location parameters." caption-side="top"}

### Combining multiple locations
{: #predefined_syntax}

If you have more complex and specific location requirements, you might need to use operators to create a combination that works for you.

| Example                  | Description                                                             |
|--------------------------|-------------------------------------------------------------------------|
| `country:de,uk\|id:my-private-region`    | All regions in `de` or `uk` countries as well as (OR) region (id) `my-private-region`|
| `geo_id:na^cap:name:power` | Any region in North America geography that has a (AND) power capability |
{: caption="Example syntax for specifying multiple location criteria." caption-side="top"}
