---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, multiple account

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 建立企業
{: #create-enterprise}

您可以從現有「訂閱」帳戶中建立 {{site.data.keyword.Bluemix}} 企業。您用來建立企業的帳戶會永久地新增至企業。
{:shortdesc}

## 開始之前
{: #create-prereqs}

若要建立 [{{site.data.keyword.Bluemix_notm}} 企業](/docs/account?topic=account-enterprise)，您必須是帳戶擁有者，或具有「訂閱」帳戶中「計費」帳戶管理服務的「管理者」角色。

您用來建立企業的「訂閱」帳戶會永久地移至企業。將帳戶移至企業後，會有下列影響：
* 帳戶的計費會轉移為[由企業管理](/docs/billing-usage?topic=billing-usage-enterprise)。在轉移之後，帳戶中的使用者無法存取將來計費期間的計費及付款資訊（例如發票、付款或訂閱）。若要檢視或管理計費，使用者需要受邀加入企業帳戶，並獲得該帳戶中「計費」服務的存取權。
* 帳戶內的使用者及存取權不會變更。帳戶內的存取權與企業是分開的，而且在新增帳戶時，使用者不會自動取得企業內的存取權。不過，如前所述，不論存取權為何，帳戶內的計費資訊都無法再使用。
* 帳戶內的資源不會變更。具有正確存取權的使用者，可以繼續檢視帳戶中資源的用量資訊。

如果您沒有「訂閱」帳戶，則可以升級您的帳戶，如[升級帳戶](/docs/account?topic=account-upgrading-account)所述。

## 在主控台中建立企業
{: #create-console}

1. 移至**管理 > 企業**，然後按一下**建立**。
1. 輸入唯一名稱，以識別您的企業。一般而言，名稱會反映貴公司或組織，例如 `My organization's enterprise`。您稍後可以編輯此企業名稱（必要的話）。
1. 如果貴公司或組織有關聯的網域名稱，請在**網域**欄位中輸入它。您可以指定任何網域或子網域格式，例如 `example.com` 或 `my.example.com`。
1. 檢閱對您帳戶的影響的相關資訊，並選取**我瞭解對我帳戶的影響**。然後，按一下**建立**。

   將帳戶新增至企業之後，就無法移除它。請確定您要將帳戶永久地移至企業。
   {: important}

幾分鐘之後，您的企業就會建立，您可以檢視企業儀表板。您的 IBM ID 會被列為聯絡人。該聯絡人是所有企業考量的焦點，例如計費或用量問題。您同時也獲指派為企業帳戶擁有者，因此您可以邀請其他使用者來管理企業。

按一下**帳戶**，以檢視包含兩個帳戶的企業階層。

* 企業帳戶，您可以在其中邀請使用者，並授與存取權以管理企業。
* 您用來建立企業的帳戶。其使用者及資源仍維持相同，但現在由企業管理計費。

## 使用 CLI 來建立企業
{: #create-cli}

1. 登入，並選取帳戶。

   ```
   ibmcloud login
   ```
   {:codeblock}
1. 執行下列指令，以建立企業，其中 `NAME` 是識別企業的唯一名稱。

   ```
   ibmcloud enterprise create NAME [-d, --domain DOMAIN_NAME] [--primary-contact-id PRIMARY_CONTACT_USER_ID]
   ```
   {:codeblock}

   例如，下列指令會建立名為 `Example Corp Enterprise` 且具有 `examplecorp.com` 網域的企業。

   ```
   ibmcloud enterprise create "Example Corp Enterprise" -d examplecorp.com
   ```
   {:codeblock}

   依預設，企業是使用下列角色中目前登入的使用者建立的：
      * 企業的聯絡人，可識別焦點人員，以通知企業相關的問題
      * 企業帳戶的擁有者，其具有管理企業帳戶的完整存取權

   您可以在 `--primary-contact-id` 選項上指定不同使用者的 IBM ID。相同的使用者會指派給這兩個角色。
1. 檢閱對您帳戶的影響，並輸入 `y` 確認您要繼續。
   ```
   Account abcde12345fghij67890 will be incorporated into enterprise My new enterprise
   (which cannot be undone). Do you want to proceed? [y/N]> y
   ```

建立企業之後，會顯示兩個新的 ID。第一個 ID 與企業相關聯，第二個 ID 會識別您用來管理企業的企業帳戶。

```
ID:                      09876jihgf54321edcba   
Enterprise Account ID:   edcba12345jihgf67890
```

您用來建立企業的帳戶現在是企業的一部分。執行 [`ibmcloud enterprise accounts`](/docs/cli?topic=cloud-cli-ibmcloud_enterprise#ibmcloud_enterprise_accounts) 指令，以檢視您企業中的兩個帳戶：企業帳戶，以及您用來建立企業的帳戶。

## 使用 API 來建立企業
{: #create-api}

您可以透過呼叫「企業管理 API」，以程式設計方式建立企業，如下列要求範例所示。<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-enterprise){: external}.-->

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/enterprises \
-H "Authorization: Bearer <Token>" \
-H 'Content-Type: application/json' \
-d '{
  "source_account_id": "a1b2c32a5ea94809a9840f5e23c362d",
  "name": "Sample Enterprise",
  "domain": "example.com",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

## 後續步驟
{: #create-next-steps}

新增其他現有帳戶，或在企業內建立新帳戶，以建置企業結構。如需相關資訊，請參閱[新增帳戶至您的企業](/docs/account?topic=account-enterprise-add)。

您也可以邀請其他使用者加入企業帳戶，讓他們可以協助管理企業。例如，您可能想要邀請財務主管來管理計費及追蹤用量成本，並邀請部門領導人來管理帳戶。如需如何邀請使用者的相關資訊，請參閱[邀請使用者](/docs/iam?topic=iam-iamuserinv)。
