---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: create account, IBMid, sign up for account, sign up

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# 註冊 {{site.data.keyword.Bluemix_notm}}
{: #signup}

您可以使用現有 IBM ID 或建立新的 IBM ID 來註冊 {{site.data.keyword.Bluemix}} 帳戶。如果您的公司已登錄使用聯合 ID 進行單一登入 (SSO)，請改用您的聯合 ID 註冊。
{:shortdesc}

|註冊 ID |詳細資料|    
|-----------------|---------|
|現有 IBM ID|如果您已經有 IBM ID，請使用用於其他 IBM 產品及服務的現有認證來註冊 {{site.data.keyword.Bluemix_notm}}。|
|新的 IBM ID|如果您還沒有 IBM ID，您將在註冊時建立。使用 IBM ID，您可以使用一個使用者名稱登入所有 IBM 產品及服務（包括 {{site.data.keyword.Bluemix_notm}}）。|
|聯合 ID|如果您的公司已要求向 IBM 登錄公司網域中的使用者認證，您可以使用已用於公司登入的認證來註冊 {{site.data.keyword.Bluemix_notm}}。在您註冊時，必須輸入一個電話號碼。|
{:caption="表 1. 註冊 {{site.data.keyword.Bluemix_notm}} 的 ID 選項" caption-side="top"}

## 使用新的或現有 IBM ID 進行註冊
{: #signup-ibmid}

如果您不隸屬於使用聯合 ID 的公司，您將使用 IBM ID 來註冊 {{site.data.keyword.Bluemix_notm}}。

1. 移至 [{{site.data.keyword.Bluemix_notm}} 登入頁面](https://cloud.ibm.com/){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")，然後按一下**建立 {{site.data.keyword.Bluemix_notm}} 帳戶**。
1. 輸入您的 IBM ID 電子郵件位址。如果您沒有現有的 IBM ID，則會根據您輸入的電子郵件建立一個 ID。
1. 以您的資訊完成剩餘欄位，然後按一下**建立帳戶**。
1. 按一下傳送至您所提供電子郵件位址之確認電子郵件中的鏈結來確認您的帳戶。

若您使用新帳戶登入時發生問題，請參閱[存取 {{site.data.keyword.Bluemix_notm}} 的疑難排解](/docs/account?topic=account-accessing)以取得協助。

## 使用聯合 ID 進行註冊
{: #signup-federated}

聯合 ID 是已向 IBM 登錄之公司網域內的 ID，因此您可以使用網域及使用者認證來存取 IBM Web 應用程式。只有在貴公司已向 IBM 登錄時，才能使用聯合 ID 來註冊 {{site.data.keyword.Bluemix_notm}}。向 IBM 登錄公司網域，可讓使用者使用其現有公司使用者認證來登入 IBM 產品和服務。然後，透過公司的身分提供者使用 SSO 來處理鑑別。

IBM 使用 Security Assertion Markup Language 2.0 (SAML 2.0) 來進行這個識別身分同盟。SAML 2.0 是適用於在安全網域之間交換鑑別資料的標準版本。它是一種 XML 型通訊協定，使用包含主張的安全記號在組織「身分提供者」與 "IBM Rely Party (RP)"（另稱為「服務提供者」）之間傳遞資訊。

如需如何登錄貴公司聯合 ID 的相關資訊，請參閱 [IBMid Enterprise Federation Adoption Guide ![外部鏈結圖示](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window}。當您要求登錄聯合 ID 時，需要有 IBM 贊助者（例如供應項目代言人或用戶端代言人）。

### 使用聯合 ID 進行登入
{: #login-federated}

當您使用聯合 ID 登入 {{site.data.keyword.Bluemix_notm}} 主控台時，系統會提示您透過公司的登入頁面進行登入。如果您透過 CLI 登入，將需要指定其他參數來進行鑑別。如需相關資訊，請參閱[使用聯合 ID 進行登入](/docs/iam?topic=iam-federated_id)。
