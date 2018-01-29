---



copyright:

  years: 2017, 2018
lastupdated: "2018-01-29"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Changing your plan
{: #changing}

You can change your service plan in {{site.data.keyword.Bluemix}} in the service instance dashboard if plan changes are enabled for that service.

Only certain services provide the ability for you to change the service plan. If plan changes are enabled for the service, the service instance dashboard displays a **Plan** option in the navigation. Each service has a different set of next steps to follow if you change your plan.

1. To change your plan, click **Plan** in the service instance dashboard. Typically, you can upgrade your plan or reduce your plan.
2. After you change your plan, you must complete a set of next steps. The steps vary depending on the type of plan change and the service. For example, if you reduced your plan, you might need to restage your app. Or, if you upgraded your plan, you might need to restage your app and take other actions.<br/><br/>To restage your app, go to the {{site.data.keyword.Bluemix_notm}} dashboard and find the app that the service is bound to. In the app menu, select **Restart App**.<br/><br/>Other next step actions depend on the service. See the following table for specific actions.

|Service |	Information|
|--------|-------------|
|Presence Insights 	|If you have a Lite plan and exceed the free allowances, a 403 message displays or is logged to indicate that you are no longer authorized, and your service instance is disabled. In addition, POST REST API calls are rejected with a 403 response.<br/><br/>If your service is disabled because you exceed the free allowance, you can upgrade from a Lite plan to a Paid plan. Your service is re-enabled within 2 hours.<br/><br/>If you have a Paid plan, you can reduce your plan to the Lite plan, as long as your usage stays within the Lite plan allowance for events and total storage.<br/><br/>When you upgrade or reduce your plan, you do not need to restage or restart your apps.|
{:caption="Table 1. Next steps for changing your plan" caption-side="top"}

## Changing your plan through the command-line interface
{: #changing_command_line}

Optionally, you can change your service plan through the command-line interface by entering the following command:
```
cf update-service <service_name> [-p <new_plan>]
```
