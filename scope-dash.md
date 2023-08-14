---

copyright:
  years: 2021, 2023
lastupdated: "2023-08-14"

keywords: dashboard, widgets display, manage visibility, customize, console, dashboard templates

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Creating and sharing a dashboard
{: #custom-dashboard}

You can customize your dashboard in the {{site.data.keyword.cloud}} console to ensure that what is displayed is relevant to you. The dashboards that you create can be scoped to specific resources. You can share the dashboards with users in your account as a way to group resources for specific projects or teams. When you create a new dashboard, you can start from scratch with a blank template or choose one of the other available templates.

IAM access policies are not required for users in your account to view a dashboard. You can share the dashboard link with users so they can view your dashboard.

Aside from being able to view dashboards, users can view resource details that are displayed within a dashboard widget only if they have the required access on the individual resource. For more information, see [IAM access](/docs/account?topic=account-userroles).

## Creating a dashboard
{: #dash-create}

To begin creating a dashboard, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions"), and select **Create a dashboard**.
2. Select a template from the available options, and then click **Next**.
   * Blank: Create a dashboard from scratch by adding widgets that align with your workflow.
   * Default: The default template offers a broad coverage of development, management, and infrastructure widgets.
   * Development team: This template promotes team alignment and resource monitoring by prioritizing a development or DevOps workflow.
   * Management: Optimized to provide a mix of billing, access management, and other administrative widgets.
3. Enter dashboard title. The title must be 30 characters or less.
4. Next, use the Dashboard settings pane to add relevant widgets to your dashboard. To add widgets, drag the widgets onto your dashboard.
5. Click the Scope tab to select from the available resources in the account that you have access to. The scope determines the data that populates for the selected resources. You can filter the resource by group, tag, and location.

   Not all widgets can be scoped. If a widget can't be scoped, it displays data for all resources.
   {: note}

6. Click **Save dashboard**.

Any dashboard that is shared with you appears on your dashboards page.
{: note}

### Managing your dashboard
{: #dash-manage}

After you create a dashboard, you can manage your dashboard by in the {{site.data.keyword.Bluemix_notm}} console by going to **Manage** > **Account**, and selecting **Account resources** > **Dashboards**. Or, from your dashboard click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Manage my dashboards**.

## Sharing a dashboard
{: #share-dash}

You can share dashboards with users in your account to give them access to view the dashboard. All users with the dashboard link can share the dashboard.

To share a dashboard, complete the following steps:

1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions").
1. Select **Share**. After you share it with a user and they click the link, the dashboard is added to their account.
