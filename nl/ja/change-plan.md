---



copyright:

  years: 2017, 2019
lastupdated: "2019-02-13"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# サービス・プランの変更
{: #changing}

{{site.data.keyword.Bluemix}} サービスのプランの変更は、その特定のサービスでプランの変更が有効になっていれば行うことができます。 プランを変更することによって、例えば、プランをアップグレードまたは縮小することができます。 プランの変更はサービス・インスタンス・ダッシュボードから行うことができます。
{: shortdesc}

アカウント・タイプのアップグレードに関する詳細をお探しですか? 詳しくは、[アカウント・タイプをアップグレードまたは変換するには、どのようにすればよいですか?](/docs/account?topic=account-changeacct)を参照してください。
{: tip}

サービス・プランは、特定のサービスについてのみ変更できます。 サービスでプラン変更が有効になっている場合は、サービス・インスタンス・ダッシュボードのナビゲーションに**「プラン」**オプションが表示されます。 プランを変更する場合、次に実行する一連のステップはサービスごとに異なります。

1. サービス・インスタンス・ダッシュボードで**「プラン」**をクリックします。 通常、プランのアップグレードまたは縮小が可能です。
2. プランの変更後、追加ステップを実行する必要があります。 プラン変更のタイプおよびサービスによって、ステップの内容は異なります。 例えば、プランを縮小した場合、アプリの再ステージが必要になる場合があります。 または、プランをアップグレードした場合、アプリの再ステージと他のアクションが必要になる場合があります。

   アプリを再ステージするには、リソース・リストに移動し、サービスがバインドされているアプリを見つけます。 メニュー・アイコン ![メニュー・アイコン](../icons/icon_hamburger.svg) > **「リソース・リスト」**をクリックします。 アプリ・メニューで、**「アプリの再始動」**を選択します。

  これ以上の必要なアクションについて詳しくは、サービスの資料を参照してください。

## CLI を使用したプランの変更
{: #changing_command_line}

コンソールの代替方法として、{{site.data.keyword.Bluemix_notm}} コマンド・ライン・インターフェース (CLI) を使用してサービス・プランを変更できます。

1. サービスがリソース・コントローラーを使用して使用可能になっているかどうかを確認します。

   ```
   ibmcloud catalog service <service_name>
   ```
   {:codeblock}

   サービスがリソース・コントローラー (RC) を使用して使用可能になっている場合、`RC Compatible true` とリストされます。 変更先のプランの ID をメモしてください。

   ```
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. サービス・インスタンスのプランを変更します。

   - サービスが RC 対応の場合、[`ibmcloud resource service-instance-update` コマンド](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource)を使用してプランを変更します。

     ```
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}

   - サービスが RC 対応でなく、したがって Cloud Foundry ベースである場合、[`ibmcloud cf update-service` コマンド](/docs/cli/reference/ibmcloud?topic=cloud-cli-cf#cf)を使用してプランを変更します。

     ```
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {:codeblock}
