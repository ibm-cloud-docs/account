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


# 變更服務方案
{: #changing}

您可以變更 {{site.data.keyword.Bluemix}} 服務的方案（如果已啟用該特定服務的方案變更）。您可能想要變更方案，例如，升級或降低方案。您可以從服務實例儀表板變更方案。
{: shortdesc}

您在尋找關於升級帳戶類型的詳細資料嗎？如需相關資訊，請參閱[升級帳戶](/docs/account?topic=account-upgrading-account)。
{: tip}

您只能針對特定服務變更服務方案。如果已啟用服務的方案變更，則服務實例儀表板會在導覽中顯示**方案**選項。如果您變更方案，則每一個服務都會有要遵循的不同後續步驟集。

1. 按一下服務實例儀表板中的**方案**。您一般可以升級方案，或降低方案。
2. 在變更方案之後，您必須完成額外步驟。步驟會視方案變更類型及服務而不同。例如，如果您降低方案，則可能需要重新編譯打包應用程式。或者，如果您升級方案，則可能需要重新編譯打包應用程式，然後採取其他動作。

   若要重新編譯打包應用程式，請移至資源清單，尋找服務所連結的應用程式。按一下「功能表」圖示 ![「功能表」圖示](../icons/icon_hamburger.svg)** > 資源清單**。在應用程式功能表中，選取**重新啟動應用程式**。

  如需任何進一步必要動作的相關資訊，請參閱該服務的文件。

## 透過 CLI 變更方案
{: #changing_command_line}

作為主控台的替代方案，您可以使用 {{site.data.keyword.Bluemix_notm}} 指令行介面 (CLI) 來變更服務的方案。

1. 檢查服務是否已啟用資源控制器。

   ```
   ibmcloud catalog service <service_name>
   ```
   {:codeblock}

   如果服務已啟用資源控制器 (RC)，它會列出 `RC Compatible true`。請記下您要變更至的方案 ID。

   ```
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. 變更服務實例的方案。

   - 如果服務已啟用 RC，請使用 [`ibmcloud resource service-instance-update` 指令](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource)來變更方案。

     ```
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}

   - 如果服務未啟用 RC 而因此基於 Cloud Foundry，請使用 [`ibmcloud cf update-service` 指令](/docs/cli/reference/ibmcloud?topic=cloud-cli-cf#cf)來變更方案。

     ```
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {:codeblock}
