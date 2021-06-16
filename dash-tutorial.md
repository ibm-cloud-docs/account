---

copyright:
   years: 2021
lastupdated: "2021-06-16"

keywords: dashboard, custom dashboard

subcollection: account

content-type: tutorial
completion-time: 10m

---

{:shortdesc: .shortdesc}
{:screen: .screen}  
{:codeblock: .codeblock}  
{:pre: .pre}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}
{:step: data-tutorial-type='step'}
{:video: .video}


# Customizing your {{site.data.keyword.Bluemix_notm}} dashboard 
{: #tutorial-custom-dash}
{: toc-content-type="tutorial"}
{: toc-completion-time="10m"}

This tutorial walks you through how to customize your dashboard in the {{site.data.keyword.Bluemix}} console to ensure that what is displayed is relevant to you. By completing this tutorial, you learn how to create a new dashboard, add and organize widgets, duplicate a dashboard, share a dashboard with other users, and delete unused dashboards.
{: shortdesc}

The tutorial uses a fictitious project manager who is named Cora. She wants to understand total resource usage over the past year and how her team's budget is used to build a new chatbot with specific resources related to AI and machine learning. As you complete the tutorial, adapt each step to match your project's needs.

## Create a dashboard
{: #tutorial-dash-new}
{: step}

First, create a new dashboard and select a template. 

1. In the {{site.data.keyword.cloud_notm}} console, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Create a dashboard**. 
2. Select the Management template from the available options, and then click **Create**. 

  The Management template is optimized to provide a mix of billing, access management, and other administrative widgets that Cora needs.
  
2. Enter your dashboard title in 30 characters or less. 
3. Next, use the Dashboard settings panel to add relevant widgets to your dashboard. To add widgets, drag the widgets onto your dashboard. Add the **Notes** widget to your dashboard. This widget is where Cora can provide essential information that's custom for the team that she shares the dashboard with. 
5. Click the **Scope** tab to select from the available resources in the account that you have access to. The scope determines the data that populates for the selected resources. You can filter the resource by group, tag, and location. Cora wants to select only resources that are related to AI and machine learning, so she filters by the resource group that exists for her team's chatbot project. 
   Not all widgets can be scoped. If a widget can't be scoped, the data for all resources is displayed. 
   {: note}
6. Reorganize the layout to fit your needs. Cora moves Notes to the first row, next to Resource summary. In the next row, she includes the Usage, User access, and {{site.data.keyword.cloud_notm}} status widgets.  
7. Click **Save dashboard**. 

### Watch and learn
{: dash-tutorial-video}
The following video provides a demo of the process detailed in Step 1. [Create a dashboard](docs/account?topic=account-tutorial-custom-dash#tutorial-dash-new): ![Create a custom dashboard in {{site.data.keyword.Bluemix_notm}}.](images/scope-dash-tutorial.mp4){: video data-script="#video-transcript-dash-tutorial" width="800" height="450" controls loop}

## Share a dashboard with teammates
{: #tutorial-dash-share}
{: step}

You can share dashboards with users in your account to give them access to view the dashboard. Cora wants to share her custom Management dashboard with her program director so they can talk about resource allocation and the budget for the next year. 

To share a dashboard, click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Share**. After you share it with a user and they click the link, the dashboard is added to their account. 

All users with the dashboard link can share the dashboard, which means other users can see the populated data that they have permission to view. If they don’t have the same permissions as the owner, for example, if they don’t have access to Cora’s chatbot resource group, they cannot view that data. Users without permissions to the scoped resources are able to view the dashboard layout, but not the populated data. A user with insufficient permissions might see a warning icon next to the dashboard that indicates a scoping error and that the data that's displayed might not be complete. Make sure that the users you share a dashboard with have access to the resources you scope the dashboard to.

## Duplicate a dashboard
{: #tutorial-dash-dupe}
{: step}

Cora decides that the team of developers she manages doesn't need to see the Usage for the project. Other than the Usage widget, she wants to share with them essentially the same dashboard that she shared with her program director. 

You can duplicate a dashboard to include the same structure and layout without having to re-create the dashboard from scratch. 

1.  To duplicate a dashboard, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Duplicate**.  
2. Define the scope. The scope and assigned access is not saved from the dashboard that was duplicated. Cora applies the resource group filter for the chatbot project just like she did for the original dashboard.
3. Click **Save dashboard**. 
4. Click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Share** to share the new dashboard with the correct users. 

## Next steps
{: #tutorial-dash-step-next}

When the chatbot project is complete, Cora's team of developers might want to remove the dashboard from their view, even if Cora wants to keep it around to reference later. You can remove a dashboard only if it was shared with you.

1. In the {{site.data.keyword.Bluemix_notm}} console go to **Manage** > **Account**, and select **Account resources** > **Dashboards**.
2. Click the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Remove**. 

Is your dashboard no longer in use? Delete the dashboard that you created as a part of this tutorial. After you delete a dashboard, you can't recover it and it is deleted for all users. Only the dashboard owner can delete a dashboard.

To delete a dashboard, complete the following steps: 
1. Expand the **Actions** icon ![Action icon](../icons/action-menu-icon.svg "Actions"), and select **Delete**.
2. Click **Delete**. 
