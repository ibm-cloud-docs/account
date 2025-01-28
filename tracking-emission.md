---
copyright:

  years: 2022, 2025
lastupdated: "2025-01-28"

keywords: carbon calculator, cloud carbon calculator, emission calculator, carbon footprint, sustainability, FAQs

subcollection: account
---

{{site.data.keyword.attribute-definition-list}}

# Tracking account emissions with carbon calculator
{: #tracking-emissions-account}

The carbon emissions factor, a ratio of emissions per unit of energy, is being updated for higher accuracy and is temporarily unavailable. For urgent inquiries related to carbon emissions factor data, contact support.
{: important}

To view emissions data for your account, you must be assigned the viewer or higher role on the billing service to view and export the emissions data for the entire account. An account or billing administrator role is required to grant other users access to the Billing service. For more information about assigning access, see [Assigning access to account management services](/docs/account?topic=account-account-services&interface=api#billing-acct-mgmt-api).

Emissions from key greenhouse gases are measured in metric tons of carbon dioxide-equivalent (kgCO~2~e). You can view your account's emissions data in the {{site.data.keyword.cloud_notm}} console. Go to **Manage** > **Billing and Usage** > **Carbon Calculator** to view the following widgets:

* Total emissions: The total emissions are calculated by comparing the energy-related usage with data center energy sources. You can download the total emissions data in CSV format.

* Emissions by location: The energy consumption is calculated by using usage units such as CPU. Two or more resources are required to display the location data.

* Emissions by service: The GHG emissions are broken down by service.

* Emissions by resource group: The GHG emissions are broken down by group. Most services are displayed by resource group. However, Classic Infrastructure is displayed in a dedicated group. The emissions are displayed only if a group contains those services.

## Tracking enterprise emissions with the carbon calculator
{: #tracking-emissions-enterprise}

The enterprise level view of carbon calculator enables you to view and export emissions data for your entire enterprise account. You must be assigned the `Usage report viewer` role on the enterprise service in the enterprise parent account in order to view and export the emissions data at the enterprise level. For more information about assigning access, see [Assigning access to account management services](/docs/account?topic=account-account-services&interface=api#billing-acct-mgmt-api).

In the enterprise level view, you can filter your emissions data down to a specific account group or account by clicking that entity in the account hierarchy. The enterprise view provides two additional widgets:

* Emissions by account group: GHG emissions broken down by account group. This widget is displayed if the entity being viewed contains account groups. Miscellaneous emissions do not belong to an account group.
* Emissions by account: GHG emissions are broken down by account. This widget is displayed if the entity that is being viewed contains only accounts.

Learn more about setting up and managing [Enterprise accounts](/docs/enterprise-management?topic=enterprise-management-what-is-enterprise).

## Working with the carbon calculator API
{: #tracking-emissions-api}

Users can pull emissions data or incorporate that data into their own applications and processes by leveraging the [Carbon Calculator API](/apidocs/carbon-calculator).
