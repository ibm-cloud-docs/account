---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, create account group, organize accounts, move accounts

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 在企業中組織帳戶
{: #enterprise-organize}

使用帳戶群組，在您的 {{site.data.keyword.Bluemix}} 企業中組織相關的帳戶。您可以藉由在帳戶群組內巢狀內嵌帳戶群組，來建立多層的企業階層。如果需要，您可以在帳戶群組之間移動帳戶來進行重組。
{:shortdesc}

例如，下圖說明您可以藉由巢狀內嵌帳戶群組來設定的四個層級企業。首先，您可以建立兩個將企業作為母項的帳戶群組。然後，您可以建立兩個其他的帳戶群組，將其中一個帳戶群組作為母項。您可以在帳戶群組內自由移動帳戶，不論它們位於哪個層級。不過，無法移動帳戶群組。

![此圖顯示四個企業層級。最上層是企業，其中包含兩個層級的帳戶群組。然後，帳戶群組會包含帳戶。](images/enterprise-hierarchy.svg "藉由新增帳戶群組來建立企業層級。"){: caption="圖 1. 四層式的企業階層" caption-side="bottom"}

請記住，您組織企業的方式會影響您如何追蹤用量成本。如需相關資訊，請參閱[使用企業集中管理計費及用量](/docs/billing-usage?topic=billing-usage-enterprise)。
{: tip}

## 建立帳戶群組
{: #create-account-group}

若要建立帳戶群組，您需要企業帳戶中「企業」服務的「管理者」或「編輯者」角色。

1. 從「企業」儀表板中，按一下**帳戶**，以檢視企業中的帳戶及帳戶群組。
1. 在「帳戶群組」區段中，按一下**建立**。
1. 輸入帳戶群組的名稱，該名稱反映其將包含的帳戶。請參閱[如何使用企業？](/docs/account?topic=account-enterprise#enterprise-use-cases)，以作為您如何組織帳戶的範例。
1. 如果您想要讓除了自己之外的企業使用者成為帳戶群組的主要聯絡人，請從**聯絡人**功能表中選取其 IBM ID。如果您想要指派為聯絡人的使用者不在企業中，請先邀請該使用者加入企業帳戶。建立帳戶群組之後，就無法變更聯絡人。如需相關資訊，請參閱[邀請使用者](/docs/iam?topic=iam-iamuserinv)。

   聯絡人與帳戶擁有者不同，因為他們在帳戶群組或其帳戶內沒有任何其他存取權。您選取作為聯絡人的使用者會作為所有帳戶群組問題的焦點。例如，如果財務主管通知帳戶群組的用量成本非預期地高，則他們可能會通知帳戶群組聯絡人。


1. 如果您要帳戶群組位於企業階層的不同部分，請選取不同的母項。

  無法從建立帳戶群組的位置刪除或移動帳戶群組。
  {: note}
1. 按一下**建立**。

若要在企業階層中建立新的層級，請在帳戶群組內建立新的帳戶群組。您可以將已在企業中的帳戶移至帳戶群組，也可以在其中匯入或建立帳戶。如需匯入及建立帳戶的相關資訊，請參閱[新增帳戶至企業](/docs/account?topic=account-enterprise-add)。

### 使用 CLI 來建立帳戶群組
{: #create-account-groups-cli}

執行下列指令，以建立帳戶群組。若要在另一個帳戶群組內巢狀內嵌帳戶群組，請在 `--parent-account-group` 選項指定帳戶群組的名稱。如果您要讓不同的使用者成為帳戶群組的聯絡人，請在 `--primary-contaid-id` 選項上指定其 IBM ID。

```
ibmcloud enterprise account-group-create NAME
[--parent-account-group ACCOUNT_GROUP_NAME] [--primary-contact-id USER_ID]
```
{: codeblock}

### 使用 API 來建立帳戶群組
{: #create-account-groups-api}

您可以透過呼叫「企業管理 API」，以程式化方式在企業中建立帳戶群組。

下列要求範例會直接在企業層級下建立帳戶群組。當您呼叫 API 時，請將 ID 變數取代為您企業的值。若要在另一個帳戶群組內巢狀內嵌帳戶群組，請以下列格式指定「雲端資源名稱 (CRN)」中帳戶群組的 ID：`crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID`。

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/account-groups \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID",
  "name": "Sample Account Group",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

如需 API 的詳細資訊，請參閱[企業管理 API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-account-group){: external}。

## 在企業內移動帳戶
{: #move-accounts}

您可以在企業內的任何位置移動帳戶。例如，您可以將帳戶從較低帳戶群組移至其母項帳戶群組，或者您可以將它直接移至企業下。帳戶只能在企業內移動。它們無法移至不同的企業，或從企業中移除，以成為獨立式帳戶。

若要移動帳戶，您需要企業帳戶中「計費」服務的「管理者」角色，以及整個企業或現行和目標帳戶群組兩者的「編輯者」或「管理者」角色。

1. 從「企業」儀表板中，按一下**帳戶**。
1. 在「帳戶」區段中，按一下帳戶列中的「動作」圖示，然後選取**移動帳戶**。
1. 選取帳戶的新母項，然後按一下**儲存**。

### 使用 CLI 來移動帳戶
{: #move-accounts-cli}

1. 列出企業中的所有帳戶，以尋找帳戶名稱和 ID。

   ```
   ibmcloud enterprise accounts --recursive
   ```
   {: codeblock}
1. 如果您要將帳戶移至帳戶群組，請尋找帳戶群組名稱和 ID。

   ```
   ibmcloud enterprise account-groups
   ```
   {: codeblock}
1. 在相關選項上指定新的母項，以移動帳戶。

   若要將帳戶移至帳戶群組，請在 `--parent-account-group` 選項指定帳戶群組名稱。

   ```
   ibmcloud enterprise account-move -n NAME --parent-account-group ACCOUNT_GROUP_NAME
   ```
   {: codeblock}

   若要將帳戶直接移至企業下，請指定 `--parent-enterprise` 選項。

   ```
   ibmcloud enterprise account-move -n NAME --parent-enterprise
   ```
   {: codeblock}

### 使用 API 來移動帳戶
{: #move-account-api}

您可以呼叫「企業管理 API」來移動帳戶，如下列範例要求所示。將 IAM 記號及 ID 變數取代為您企業的值。

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_1"",
}'
```
{: codeblock}

如需 API 的詳細資訊，請參閱[企業管理 API](https://{DomainName}/apidocs/enterprise-apis/enterprise#move-an-account-with-the-enterprise){: external}。
