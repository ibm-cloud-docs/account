---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise settings, manage enterprise, view enterprise, rename enterprise

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 管理企業
{: #enterprise-settings}

從 {{site.data.keyword.Bluemix}} 企業的儀表板中，您可以檢視企業詳細資料、採取一般動作（例如新增帳戶及邀請使用者），以及檢視計費資訊。您也可以在儀表板上，或者使用 CLI 或 API 來重新命名企業。
{:shortdesc}

若要管理企業設定，您需要企業帳戶中「企業」服務的「管理者」或「編輯者」角色。
{: tip}

## 在主控台中管理企業
{: #enterprise-manage}

若要檢視企業儀表板，請移至**管理 > 企業**。儀表板提供企業中帳戶、使用者及訂閱額度的概觀。儀表板具有快速鏈結，讓您可以執行下列一般動作：
   * [將新的或現有帳戶新增至企業](/docs/account?topic=account-enterprise-add)
   * [邀請使用者加入企業帳戶](/docs/iam?topic=iam-iamuserinv)
   * [檢視及管理訂閱額度](/docs/billing-usage?topic=billing-usage-subscriptions)

此外，您也可以藉由按一下「企業」詳細資料區段中的**重新命名**來重新命名企業。

## 從 CLI 管理企業
{: #enterprise-manage-cli}

* 檢視企業資訊，例如名稱、網域、擁有者，以及建立和更新日期。

  ```
  ibmcloud enterprise show
  ```
  {: codeblock}
* 在下列指令的 `-n` 選項上指定新名稱，以重新命名企業。

   ```
   ibmcloud enterprise update -n NEW_NAME
   ```
   {:codeblock}

## 使用 API 管理企業
{: #enterprise-manage-api}

您可以透過呼叫「企業管理 API」，以程式化方式更新企業，如下列要求範例所示。您可以在 API 呼叫上傳遞新值，以更新企業名稱或網域。如需 API 的詳細資訊，請參閱[企業管理 API 文件](https://{DomainName}/apidocs/enterprise-apis/enterprise#update-an-enterprise){: external}。

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
