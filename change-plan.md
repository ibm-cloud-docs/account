---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-13"

keywords: change service, upgrade service, service plan

subcollection: account

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Changing service plans
{: #changing}

You can change the plan of an {{site.data.keyword.Bluemix}} service if plan changes are enabled for the specific service. You might want to change your plan, for example, to upgrade or reduce your plan. You can change your plan from your service instance dashboard.
{: shortdesc}

Are you looking for details about upgrading your account type? See [How do I upgrade or convert my account type?](/docs/account?topic=account-changeacct) for more information.
{: tip}

You can change the service plans for only certain services. If plan changes are enabled for the service, the service instance dashboard displays a **Plan** option in the navigation. Each service has a different set of next steps to follow if you change your plan.

1. Click **Plan** in the service instance dashboard. Typically, you can upgrade your plan or reduce your plan.
2. After you change your plan, you must complete extra steps. The steps vary depending on the type of plan change and the service. For example, if you reduced your plan, you might need to restage your app. Or, if you upgraded your plan, you might need to restage your app and take other actions.

   To restage your app, go to your resource list to find the app that the service is bound to. Click the Menu icon ![Menu icon](../icons/icon_hamburger.svg) **> Resource list**. In the app menu, select **Restart App**.

  For more information about any further required actions, see the documentation for the service.

## Changing a plan through the CLI
{: #changing_command_line}

As an alternative to the console, you can change a service's plan by using the {{site.data.keyword.Bluemix_notm}} command-line interface (CLI).

1. Check whether the service is enabled with the resource controller.

   ```
   ibmcloud catalog service <service_name>
   ```
   {:codeblock}

   If the service is enabled with the resource controller (RC), it lists `RC Compatible true`. Make note of the ID of the plan that you want to change to.

   ```
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. Change the plan for your service instance.

   - If the service is RC-enabled, change your plan using the [`ibmcloud resource service-instance-update` command](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource).

     ```
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}

   - If the service is not RC-enabled and is therefore based on Cloud Foundry, change your plan using the [`ibmcloud cf update-service` command](/docs/cli/reference/ibmcloud?topic=cloud-cli-cf#cf).

     ```
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {:codeblock}
