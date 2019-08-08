---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, enterprise settings, manage enterprise, view enterprise, rename enterprise

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# エンタープライズの管理
{: #enterprise-settings}

{{site.data.keyword.Bluemix}} エンタープライズのダッシュボードから、エンタープライズ詳細の表示、一般的なアクションの実行 (アカウントの追加やユーザーの招待など)、および請求情報の表示を行うことができます。ダッシュボードで、または CLI または API を使用して、エンタープライズの名前を変更することもできます。
{:shortdesc}

エンタープライズ設定を管理するには、エンタープライズ・アカウント内のエンタープライズ・サービスに対する管理者またはエディターの役割が必要です。
{: tip}

## コンソールでのエンタープライズの管理
{: #enterprise-manage}

エンタープライズ・ダッシュボードを表示するには、**「管理」 > 「エンタープライズ」**と移動します。ダッシュボードには、エンタープライズ内のアカウント、ユーザー、およびサブスクリプション・クレジットの概要が表示されます。ダッシュボードにはクイック・リンクがあり、以下の一般的なアクションを実行できます。
   * [エンタープライズへの新規アカウントまたは既存アカウントの追加](/docs/account?topic=account-enterprise-add)
   * [エンタープライズ・アカウントへのユーザーの招待](/docs/iam?topic=iam-iamuserinv)
   * [サブスクリプション・クレジットの表示と管理](/docs/billing-usage?topic=billing-usage-subscriptions)

また、「エンタープライズ詳細」セクションで**「名前変更」**をクリックすることによって、エンタープライズの名前を変更できます。

## CLI からのエンタープライズの管理
{: #enterprise-manage-cli}

* エンタープライズ情報 (名前、ドメイン、所有者、作成日、更新日など) を表示します。

  ```
  ibmcloud enterprise show
  ```
  {: codeblock}
* 次のコマンドの `-n` オプションに新しい名前を指定して、エンタープライズの名前を変更します。

   ```
   ibmcloud enterprise update -n NEW_NAME
   ```
   {:codeblock}

## API を使用したエンタープライズの管理
{: #enterprise-manage-api}

以下のサンプル要求に示すように、Enterprise Management API を呼び出すことによって、プログラマチックにエンタープライズを更新できます。API 呼び出しで新しい値を渡すことによって、エンタープライズ名またはドメインを更新できます。<!--For detailed information about the API, see the [Enterprise Management API documentation](https://{DomainName}/apidocs/enterprise-apis/enterprise#update-an-enterprise){: external}.-->

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID" \
-H "Authorization: $IAM_TOKEN" \
-H 'Content-Type: application/json' \
-d '{
  "name": "Brand New Sample Enterprise",
  "domain": "new.example.com"
}'
```
