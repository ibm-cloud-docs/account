---

copyright:

  years: 2024

lastupdated: "2024-10-18"

keywords: Projects, usage, billing, spend, bill back

subcollection: secure-enterprise

---

{{site.data.keyword.attribute-definition-list}}

# Tracking usage and spend for projects
{: #project-usage-spend}

As a billing or FinOps manager, you need to track spending for teams in your organization and bill them back for the resources that they deploy. [Projects](#x2035151){: term} help with accounting by ensuring that all resources that are associated with a project can be tracked back to the project with tagging and resource usage reports.
{: shortdesc}





Resources in a project are automatically given service tags with the ID for the project and configuration that they're associated with. These tags are visible in usage reports or by using the command-line interface (CLI) or API. You can use these tags to filter your usage report and get a clear view of spending for projects. This way, it's easier to bill usage back to the teams that are deploying projects.

The services themselves exclusively manage service tags. Users can't add or remove service tags. For more information, see [Tag types](/docs/account?topic=account-tag&interface=ui#tag-types).
{: note}

If you're just getting started, you might want to [estimate architecture costs in a project](/docs/secure-enterprise?topic=secure-enterprise-cost-estimate-project&interface=ui).

## Mapping resources on a usage report to a project
{: #map-project-id}

1. Find the ID for a project.
   1. In the {{site.data.keyword.cloud_notm}} console, go to the account that contains a project that you're managing billing for.
   1. Click the **Navigation menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **[Projects](/projects/)** and select a project.
   1. In the project, go to the **Manage** tab.
   1. Copy the ID and save it to reference later.

   You can also use the following {{site.data.keyword.cloud_notm}} CLI command to list all projects and their IDs: `ibmcloud project list --all-pages`. For more information, see the [Project CLI reference](/docs/cli?topic=cli-projects-cli#project-cli-list-command).
   {: note}

1. Get your usage report.
   1. In the {{site.data.keyword.cloud_notm}} console, go to the enterprise account.
   1. Go to **Manage > Billing and usage**.
   1. Click **View usage > Export CSV**.
1. Open the usage report.
1. Go to the column `service_tag::project::project_id`.
1. Sort the column to organize resources by project ID.

Add up the usage cost for each resource associated with a project ID to get the total spend for a project over a billing period.

You can use the [`ibmcloud resource search`](/docs/secure-enterprise?topic=secure-enterprise-projects-cli&interface=cli#ibmcloud-resource-tag-search) command to retrieve the resources in a project based on the project ID service tag.
{: tip}
