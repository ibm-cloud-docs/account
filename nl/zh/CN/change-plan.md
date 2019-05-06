---

copyright:
  years: 2017, 2019
lastupdated: "2019-04-30"

keywords: change service, upgrade service, service plan, pricing plan

subcollection: account

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# 更改服务套餐
{: #changing}

您可以更改 {{site.data.keyword.Bluemix}} 服务的价格套餐，前提是特定服务支持套餐更改。例如，您可能希望更改套餐的情况包括要升级或降级套餐。您可以在服务实例仪表板中更改服务价格套餐。
{: shortdesc}

您在查找有关升级帐户类型的详细信息吗？有关更多信息，请参阅[升级帐户](/docs/account?topic=account-upgrading-account)。
{: tip}

只能更改特定服务的服务套餐。如果服务支持套餐更改，那么服务实例仪表板的导航中会显示**套餐**选项。每个服务在套餐更改后都有一组不同的后续步骤要执行。

1. 在 {{site.data.keyword.Bluemix_notm}} 控制台中，单击“菜单”图标 ![“菜单”图标](../icons/icon_hamburger.svg) > **资源列表**以查看资源列表。单击要更新的服务。
1. 在服务实例仪表板中，单击**套餐**。选择要更改为的套餐，然后单击**保存**。

    某些服务的套餐无法在“套餐”页面中进行选择。通常，这些套餐无法选择是因为它们需要销售团队的帮助，或者需要进行迁移后才能更改套餐。请参阅服务文档，以获取有关所需后续步骤的信息。


1. 更改套餐后，必须完成额外的步骤。步骤根据套餐更改和服务的类型而有所不同。例如，如果降级了套餐，那么可能需要重新编译打包应用程序。或者，如果升级了套餐，那么可能需要重新编译打包应用程序并执行其他操作。

   要重新编译打包应用程序，请转至资源列表，以找到与服务绑定的应用程序。单击“菜单”图标 ![“菜单”图标](../icons/icon_hamburger.svg) > **资源列表**。在应用程序菜单中，选择**重新启动应用程序**。

  有关任何进一步必需操作的更多信息，请参阅服务的文档。

## 通过 CLI 更改套餐
{: #changing_command_line}

作为控制台的替代方法，您可以使用 {{site.data.keyword.Bluemix_notm}} 命令行界面 (CLI) 来更改服务的价格套餐。

1. 检查服务是否支持资源控制器。

   ```
   ibmcloud catalog service <service_name>
   ```
   {:codeblock}

   如果服务支持资源控制器 (RC)，那么会列出 `RC Compatible true`。请记下要更改为的套餐的标识。

   ```
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. 更改服务实例的套餐。

   - 如果服务支持 RC，请使用 [`ibmcloud resource service-instance-update` 命令](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource)来更改套餐。

     ```
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}

   - 如果服务不支持 RC，因而是基于 Cloud Foundry 的服务，请使用 [`ibmcloud cf update-service` 命令](/docs/cli?topic=cloud-cli-ibmcloud_commands_services#ibmcloud_service_update)来更改套餐。

     ```
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {:codeblock}
