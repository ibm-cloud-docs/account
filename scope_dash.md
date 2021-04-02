---

copyright:
  years: 2019, 2021
lastupdated: "2020-04-02"

keywords: dashboard, widgets display, manage visibility, customize, console, dashboard templates 

subcollection: account

---

{:shortdesc: .shortdesc}
{:screen: .screen}
{:codeblock: .codeblock}
{:pre: .pre}
{:tip: .tip}
{:note: .note}

# Working with scoped dashboards 
{: #custom-dashboard}

You can customize your dashboard in the {{site.data.keyword.cloud}} console to ensure that what is displayed is relevant to you. The dashboards that you create can be scoped to specific resources. You can share the dashboards with users in your account as a way to group resources for specific projects or teams. When you create a new dashboard, you can start from scratch with a blank template or choose one of the other available templates.
{: .shortdesc}

## Before you begin
{: #prereqs}

 IAM access policies are not required for users in your account to view a dashboard. You can share the dashboard link with users so they can view your dashboard.

Aside from being able to view dashboards, users can view resource details that are displayed within a dashboard widget only if they have the required access on the individual resource. For more information, see [IAM access](/docs/account?topic=account-userroles). 

## Creating a dashboard 
{: #creating-dash}

To create a dashboard, you select a template and then add and remove widgets based on your needs. To begin creating a dashboard, complete the following steps:  

1. In the {{site.data.keyword.cloud_notm}} console, click the Actions icon ![Action icon](../icons/action-menu-icon.svg), and select **Create a dashboard**. 
2. Select a template from the available options, and then click **Next**. 
  * Blank: Create a dashboard from scratch by adding widgets that align with your workflow.
  * Default: The default template offers a broad coverage of development, management, and infrastructure widgets.
  * Development team: Prioritizes a development or DevOps centered workflow. You can enable your team to align around relevant resources, or use this template independently.
  * Management: Optimized to provide a mix of billing, access management, and other administrative widgets.
2. Enter a name for your dashboard. The name must be 30 characters or less. 
3. Next, use the Dashboard settings pane to add relevant widgets to your dashboard. To add widgets, drag the widgets onto your dashboard. 
4. Click the Scope tab to select from the available resources in the account that you have access to. The scope determines the data that populates for the selected resources. You can filter the resource by group, tag, and location. 
   Not all widgets can be scoped. If a widget can't be scoped, it displays data for all resources. 
   {: note}
5. Click **Save dashboard**. 

## Managing your dashboard 
{: #manage-dash}

After you create a dashboard, you can manage your dashboard by in the {{site.data.keyword.Bluemix_notm}} console by going to **Manage** > **Account**, and selecting **Account resources** > **Dashboards**. Or, from your dashboard click the Actions icon ![Action icon](../icons/action-menu-icon.svg ) > **Manage my dashboards**.

Any dashboard that is shared with you appears on your dashboards page. 
{: note}

The following table outlines the different actions and user permissions that are required for users to edit, share, or work with a scoped dashboard:

| Role     |	Actions  |	
|------------|-------------------|
| Dashboard owner  | **Edit**    |
| All users with the dashboard link   | **Share**   |
| Dashboard owner | **Delete**  |
| All users with the dashboard link    | **Duplicate**  |
{: caption="Table 1. Roles for managing a scoped dashboard" caption-side="top"} 

### Sharing a dashboard
{: #share-dash}

You can share dashboards with users in your account to give them access to view the dashboard. To share a dashboard, click the Actions icon ![Action icon](../icons/action-menu-icon.svg), and select **Share**. After you share it with a user and they click the link, the dashboard is added to their account. 

### Adding widgets to your dashboard 
{: #add-widgets}

Only the user that created the dashboard can edit it. A dashboard includes widgets that are configured to display specific information that is relevant to you and your team. To edit a dashboard, click **Edit dashboard**. From here, you can use the dashboard pane to add and remove widgets, and adjust the scope of your resources. To view a list of the available widgets, see [Dashboard widgets](/docs/account?topic=account-custom-dashboard#dashboard-widget).

You can't directly edit the default console dashboard. When you click **Edit** on the default console dashboard, a duplicate version is created that you can edit. You can return to the original default console dashboard by selected the dashboard with the default label. {: note}

### Duplicating a dashboard
{: #dupe-dash}

You can duplicate a dashboard to include the same structure and layout without having to re-create the dashboard from scratch. The layout of the widgets and content that is included in the notes widget will be duplicated. You must define the scope and dashboard access separately. The scope and assigned access is not saved from the dashboard that was duplicated. 

 To duplicate a dashboard, click the Actions icon ![More Actions icon](../icons/action-menu-icon.svg) > **Duplicate**.

### Reorganizing your dashboard
{: #reorg-dashboard}

You can rearrange the widgets on your dashboard by grabbing a widget and moving it. For example, as an account owner, tracking who has access to your account might be a top priority for you. You want these details to be displayed at the top of your dashboard, but you must scroll to find the User access widget. Grab the widget to move it to the top of your dashboard.

### Removing a dashboard 
{: #remove-dash}

If you don't want to view a dashboard, you can remove the dashboard from your list. After a dashboard is removed, a user with access to that dashboard must share the dashboard link with you if you'd like to view that dashboard again. You can only remove a dashboard that was shared with you. 

1. In the {{site.data.keyword.Bluemix_notm}} console go to **Manage** > **Account**, and select **Account resources** > **Dashboards**.
2. Click the Actions icon ![Action icon](../icons/action-menu-icon.svg), and select **Remove**. 

### Deleting a dashboard 
{: #delete-dash}

You can delete a dashboard only if you created it. After you delete a dashboard, you can't recover it and it's deleted for all users.

To delete a dashboard: 
1. Expand the Actions icon ![Action icon](../icons/action-menu-icon.svg), and select **Delete**.
2. Click **Delete**. 

##  Dashboard widgets 
{: #dashboard-widget}

When you customize a dashboard, you can add widgets to ensure what is displayed is relevant to you. The widgets range from development centric to management centric, and you can add and remove them at any time. The following widgets are available to add to a dashboard: 

* Apps: Create and manage your apps by using this widget. 
* Classic infrastructure: View all useful links for classic infrastructure users. 
* Compliance and security: Monitor your overall security and compliance to internal and external regulations. 
* For you: This widget displays recommendations that are selected for you. 
* IBM Cloud status: Stay up to date on the status of resources in specific locations. 
* Kubernetes: View and track your clusters after you create them. 
* News: Stay up to date with the latest IBM Cloud News. 
* Notes: You can use this widget to provide essential information that's custom to your team. 
* Planned maintenance: View upcoming and planned maintenance events. 
* Quick start: Personalized tasks to help you get started with IBM Cloud. 
* Recent support cases: View a summary of your support cases. 
* Resource summary: Track and view the status of your resources. 
* Spending summary: View a summary of total spending over the past year.
* Toolchains: Create and manage your toolchains. 
* Usage: View billing usage details for your account. 
* User access: View and manage users in your account. 