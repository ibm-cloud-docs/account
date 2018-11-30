---



copyright:

  years: 2017, 2018
lastupdated: "2018-11-19"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Changing your plan
{: #changing}

You can change your {{site.data.keyword.Bluemix}} service plan if plan changes are enabled for the specific service. You might want to change your plan, for example, to upgrade or reduce your plan. You can change your plan from your service instance dashboard.
{: shortdesc}

Are you looking for details about upgrading your account type? See [How do I upgrade or change my account type?](/docs/account/account_faq.html#changeacct) for more information. 
{: tip}

You can change the service plans for only certain services. If plan changes are enabled for the service, the service instance dashboard displays a **Plan** option in the navigation. Each service has a different set of next steps to follow if you change your plan.

1. Click **Plan** in the service instance dashboard. Typically, you can upgrade your plan or reduce your plan.
2. After you change your plan, you must complete extra steps. The steps vary depending on the type of plan change and the service. For example, if you reduced your plan, you might need to restage your app. Or, if you upgraded your plan, you might need to restage your app and take other actions.

To restage your app, go to your resource list to find the app that the service is bound to. Click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) **> Resource list**. In the app menu, select **Restart App**.

Other next step actions depend on the service. See the following table for specific actions.

|Service |	Information|
|--------|-------------|
|Presence Insights 	|If you have a Lite plan and exceed the free allowances, a 403 message displays or is logged to indicate that you are no longer authorized, and your service instance is disabled. Also, POST REST API calls are rejected with a 403 response.<br/><br/>If your service is disabled because you exceed the free allowance, you can upgrade from a Lite plan to a Paid plan. Your service is reenabled within 2 hours.<br/><br/>If you have a Paid plan, you can reduce your plan to the Lite plan, while your usage stays within the Lite plan allowance for events and total storage.<br/><br/>When you upgrade or reduce your plan, you don't need to restage or restart your apps.|
{:caption="Table 1. Next steps for changing your plan" caption-side="top"}


## Changing your plan through the command-line interface
{: #changing_command_line}

Optionally, you can change your service plan through the command-line interface by entering the following command:

```
cf update-service <service_name> [-p <new_plan>]
```
