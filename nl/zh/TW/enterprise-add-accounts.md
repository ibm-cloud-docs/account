---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, add account, import account, create account

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 新增帳戶至企業
{: #enterprise-add}

您可以將其他 {{site.data.keyword.Bluemix}} 帳戶新增至其中，以建置企業。 若要新增帳戶，您可以匯入不在另一個企業中的現有帳戶，也可以在企業內建立新的帳戶。
{:shortdesc}

在您的企業有多個帳戶之後，您可以使用帳戶群組來組織相關的帳戶。如需相關資訊，請參閱[在企業中組織帳戶](/docs/account?topic=account-enterprise-organize)。

## 匯入現有帳戶
{: #add-accounts}

您可以將現有帳戶匯入企業中。在匯入帳戶之後，無法移除它，而且每一個帳戶都只能是某個企業的一部分。如果匯入「精簡」或試用帳戶，則會自動將它升級至[隨收隨付制帳戶](/docs/account?topic=account-accounts)。

將帳戶匯入至企業後，會有下列影響：
* 帳戶的計費會轉移為由企業管理。在轉移之後，帳戶中的使用者無法存取將來計費期間的計費及付款資訊（例如發票、付款或訂閱）。若要檢視或管理計費，使用者需要受邀加入企業帳戶，並獲得該帳戶中「計費」服務的存取權。如需相關資訊，請參閱[使用企業集中管理計費及用量](/docs/billing-usage?topic=billing-usage-enterprise)。
* 帳戶內的使用者及存取權不會變更。帳戶內的存取權與企業是分開的，而且在匯入帳戶時，使用者不會自動取得企業內的存取權。
* 帳戶內的資源不會變更。具有正確存取權的使用者，可以繼續檢視帳戶中資源的用量資訊。

若要將現有帳戶匯入至企業，則需要下列存取權：

   * 在要匯入的帳戶內，您必須是帳戶擁有者，或具有帳戶內「計費」服務的「管理者」角色。
   * 在企業帳戶內，您需要「企業」服務的「編輯者」或「管理者」角色，以及「計費」服務的「管理者」角色。

若要匯入現有帳戶，請完成下列步驟：

1. 登入企業帳戶，然後移至**管理 > 企業**。
1. 按一下**帳戶**，以檢視企業中的帳戶及帳戶群組。 在「帳戶」區段中，選取**新增 > 匯入帳戶**。
1. 選取您要匯入的帳戶。

   如果未顯示任何帳戶，您可能在所有現有帳戶中都沒有正確的存取權。
  {: tip}
1. 如果您要將帳戶新增至帳戶群組，請選取要成為其母項的帳戶群組。您選取的母項會決定帳戶在企業階層中的存在位置。
1. 檢閱對您帳戶的影響的相關資訊，並選取**我瞭解對我的帳戶的影響**。然後，按一下**匯入**。

   將帳戶匯入至企業之後，就無法移除它。請確定您要將帳戶永久移至企業。
   {: important}

### 使用 CLI 匯入帳戶
{: #add-account-cli}

1. 尋找您要匯入至企業的帳戶 ID。

   ```
   ibmcloud account list
   ```
   {: codeblock}
1. 如果您要將帳戶新增至帳戶群組，請尋找企業中現有帳戶群組的名稱和 ID。

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. 將帳戶匯入至企業，並指定 `--account ID` 參數的帳戶 ID。如果您未指定母項帳戶群組，則會直接在企業下新增帳戶。

   ```
   ibmcloud enterprise account-import --account-id ID
   [--parent-account-group ACCOUNT_GROUP_NAME | --parent-account-group-id ACCOUNT_GROUP_ID]
   ```
   {: codeblock}

### 使用 API 匯入帳戶
{: #add-account-api}

若要將現有帳戶匯入至企業，請呼叫<!-- [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#import-an-account-into-an-enterprise){: external}-->「企業管理 API」，如下列要求範例所示。將 {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) 記號及 ID 變數取代為您企業的值。

```
curl -X PUT \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID/import/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" -H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID"
}'
```
{: codeblock}

## 建立新帳戶
{: #create-accounts}

您可以在企業內建立新帳戶。帳戶會建立為「隨收隨付制」帳戶，而且會根據用量向企業收費。若要建立帳戶，您需要「企業」服務的「編輯者」或「管理者」角色的存取原則。

1. 從「企業」儀表板中，按一下**帳戶**，以檢視企業中的帳戶及帳戶群組。
1. 在「帳戶」區段中，選取**新增 > 建立帳戶**。
1. 輸入在企業內唯一的帳戶名稱。因為它是多個帳戶中的其中一個，唯一的敘述性名稱可協助您一目瞭然地瞭解帳戶的用途。
1. 如果您要將不同的使用者指派為帳戶擁有者，請在**擁有者**欄位中輸入其 IBM ID。帳戶擁有者具有管理帳戶的完整存取權。
1. 如果您要將帳戶新增至帳戶群組，請選取要成為其母項的帳戶群組。您選擇的母項會決定帳戶在企業階層中的存在位置。
1. 按一下**建立**。

在建立帳戶之後，帳戶擁有者即可登入帳戶，以邀請其他使用者，並管理其存取權。

### 使用 CLI 來建立帳戶
{: #create-accounts-cli}

1. 如果您要將帳戶新增至帳戶群組，請尋找現有帳戶群組的名稱和 ID。

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. 執行下列指令，以建立帳戶。如果您未指定母項帳戶群組，則會直接在企業下新增帳戶。若要讓不同的使用者成為帳戶擁有者，請在 `--owner` 選項上指定其 IBM ID。

   ```
   ibmcloud enterprise account-create NAME
   [--parent-account-group ACCOUNT_GROUP_NAME] [--owner USER_ID]
   ```
   {: codeblock}

### 使用 API 來建立帳戶
{: #create-account-api}

若要在企業中建立新的帳戶，請呼叫「企業管理 API」，如下列要求範例所示，將 IAM 記號及 ID 變數取代為您企業的值。<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-a-new-account-in-an-enterprise){: external}. -->

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/accounts \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID",
  "name": "Sample Account",
  "owner_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}
