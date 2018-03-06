---

copyright:

  years: 2016, 2018

lastupdated: "2018-02-08"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 切換至 IBM ID 並鏈結帳戶
{: #unifyingaccounts}

SoftLayer 中的鑑別現在使用 IBM ID 來提供所有 {{site.data.keyword.Bluemix}} 的單一登入。IBM ID 是您用來登入 {{site.data.keyword.Bluemix}} 帳戶以便存取及購買基礎架構、服務及應用程式特性的單一 ID。已針對 SoftLayer 中的所有新建帳戶啟用 IBM ID 鑑別，現有的 SoftLayer 帳戶也可以切換至 IBM ID 鑑別。
{:shortdesc}

## 切換至 IBM ID
{: #switchtoIBMid}

開始切換至 IBM ID 的程序時，在完成這項程序之前，您隨時都可以取消此切換作業。不過，在您每次登入時，都會顯示切換至 IBM ID 的提示。您計劃要鏈結至 {{site.data.keyword.Bluemix_notm}} 帳戶的每一個 SoftLayer 帳戶，都必須為具有唯一電子郵件位址的唯一 IBM ID 所擁有。

若要將現有 SoftLayer 帳戶切換至 IBM ID，您需要建立 IBM ID 然後使用登錄碼來確認它。

### 要求 IBM ID 及登錄碼
{: #reqIBMidandregcode}

1. 登入 SoftLayer 帳戶，並在顯示切換至 IBM ID 的提示時按一下**確定**。

   如果您是主要使用者，而 {{site.data.keyword.slportal}} 中未顯示切換至 IBM ID 的提示，請與 [IBM 支援中心](/docs/get-support/howtogetsupport.html#getting-customer-support)聯絡以取得協助。

   如果您先前已登入，並在提示時按了**稍後**，但想要在現行階段作業中切換至 IBM ID 鑑別，請移至「編輯使用者設定檔」頁面，然後按一下**切換至 IBM ID**。

2. 遵循精靈提示，以建立您的 IBM ID。

   輸入目前未被任何 IBM ID 使用的電子郵件位址。此電子郵件位址是用來作為新 IBM ID 的使用者名稱，而且在建立 IBM ID 之後會將登錄碼傳送到此處。您之後可以更新與 IBM ID 相關聯的電子郵件位址，但是無法變更使用者名稱。

### 使用登錄碼來確認 IBM ID
{: #confIBMiduseregcode}

1. 當您收到登錄碼時，請按一下電子郵件中的鏈結，或將 URL 複製到瀏覽器，並輸入登錄碼。

   登錄碼的有效時間是 7 天，而且只能使用一次。

2. 提交登錄碼之後，請使用 IBM ID 來登入客戶入口網站。

   在「帳戶登入」提示中，移至 **IBM ID 帳戶登入**區段，然後按一下**使用 IBM ID 登入**。請不要使用您之前用於 Softlayer ID 的**使用者名稱**和**密碼**欄位。

如果您是新客戶，當您查看訂單時，系統會要求您提供現有的 IBM ID 或建立新的 IBM ID。
  * 若要使用現有的 IBM ID，請輸入使用者名稱，或唯一的 IBM ID 電子郵件位址（亦即，不是多個 IBM ID 所共用的）。

  * 若要建立新的 IBM ID，請輸入目前未被任何 IBM ID 使用的電子郵件位址。此電子郵件位址是 IBM ID 的使用者名稱，而且是在建立 IBM ID 之後傳送登錄碼的位置。您之後可以更新與 IBM ID 相關聯的電子郵件位址，但是無法變更使用者名稱。

若要解決使用 IBM ID 登入的所有問題，請參閱 [{{site.data.keyword.Bluemix_notm}} 存取疑難排解](/docs/get-support/ts_accessing.html#accessing)。


## 鏈結 IBM ID 使用者帳戶
{: #link_user_accounts}

在您的使用者帳戶切換至 IBM ID 鑑別之後，轉銷商及經銷商就可以鏈結 SoftLayer 及 {{site.data.keyword.Bluemix_notm}} 帳戶，以利用合併的基礎架構及平台資源。請務必檢閱下列重要注意事項：

  * 所鏈結帳戶的主要使用者必須具有 IBM ID。
  * 您鏈結至 {{site.data.keyword.Bluemix_notm}} 帳戶的每一個使用者帳戶，都必須為具有唯一電子郵件位址的唯一 IBM ID 所擁有。即使單一 IBM ID 可以擁有多個 SoftLayer 帳戶，您還是必須為每一個帳戶將主要使用者變更為唯一 IBM ID。請與支援中心聯絡，以變更 SoftLayer 帳戶的主要使用者。如需相關資訊，請參閱[取得 {{site.data.keyword.Bluemix_notm}} 基礎架構的支援](/docs/customer-portal/cpsupport.html)。
  * 將新使用者新增至鏈結的帳戶時，您必須將他們同時新增至 SoftLayer 帳戶及 {{site.data.keyword.Bluemix_notm}} 帳戶，他們才能存取統一主控台的所有功能。
  * 如果您是使用 Brand Agent Portal (BAP) 的品牌帳戶使用者，而且在鏈結帳戶時需要支援，則請傳送電子郵件到下列位址以與 SoftLayer Revenue Services 團隊聯絡：softlayer_revenue_services_team@wwpdl.vnet.ibm.com。
  * {{site.data.keyword.Bluemix_notm}} 中的所有已鏈結帳戶都必須是「隨收隨付制」帳戶。您可以建立新的「隨收隨付制」帳戶、鏈結現有「隨收隨付制」帳戶，或鏈結現有試用帳戶，而試用帳戶接著會升級至「隨收隨付制」帳戶。您無法鏈結「訂閱」帳戶。


您必須是主要使用者，才能鏈結帳戶。作為帳戶之主要使用者的 IBM ID 必須是您所要鏈結的 {{site.data.keyword.Bluemix_notm}} 帳戶的擁有者。完成下列步驟，以將每一個 SoftLayer 帳戶鏈結至現有的 {{site.data.keyword.Bluemix_notm}} 帳戶或建立新帳戶：

   1. 使用主要使用者帳戶來登入「客戶入口網站」。
   2. 從「{{site.data.keyword.Bluemix_notm}} 客戶入口網站」中，按一下**鏈結 {{site.data.keyword.Bluemix_notm}} 帳戶**。
   3. 閱讀並接受將 SoftLayer 帳戶與 {{site.data.keyword.Bluemix_notm}} 帳戶鏈結所適用的條款。
   4. 請遵循精靈提示（包括將 SoftLayer 帳戶中的使用者新增至 {{site.data.keyword.Bluemix_notm}} 帳戶）。
   5. 當系統要求時，提供與 {{site.data.keyword.Bluemix_notm}} 帳戶相關聯的電子郵件位址。如果您沒有 {{site.data.keyword.Bluemix_notm}} 帳戶，請提供您要使用的電子郵件位址，並遵循指示以受邀加入 {{site.data.keyword.Bluemix_notm}}，然後建立帳戶。
   6. 在您鏈結帳戶之後，請遵循前一節中所述的程序，通知每一個帳戶的一般使用者以移轉至 IBM ID。

僅將一般使用者帳戶移轉至 IBM ID。請不要移轉品牌帳戶，這是一般使用者帳戶的母帳戶，未包含任何資源。移轉至 IBM ID 的品牌帳戶使用者將無法登入 Brand Agent Portal (BAP)。
{: tip}

鏈結帳戶之後：

  * 您必須使用 IBM ID 認證來存取 SoftLayer 及 {{site.data.keyword.Bluemix_notm}} 帳戶。
  * 任何現有 SoftLayer 折扣都會套用至 {{site.data.keyword.Bluemix_notm}} 費用。
  * 您將收到一張計價單位為美元 (USD) 的發票。如果您有現有的 {{site.data.keyword.Bluemix_notm}} 帳戶，則會在鏈結帳戶之後開始的新計費週期，透過 {{site.data.keyword.Bluemix_notm}} 收取基礎架構資源的費用。
  * 您可以在 {{site.data.keyword.Bluemix_notm}} 主控台中監視基礎架構資源的用量。

帳戶在鏈結之後，即無法解除鏈結。

## 已鏈結帳戶中的多因子鑑別使用
{: #2fa}

如果您具有已鏈結帳戶，則可以使用「身分及存取」的**設定**頁面來啟用帳戶的多因子鑑別 (/docs/iam/mfa.html)。這通常也稱為雙因子鑑別 (2FA)，而且它會新增安全層來存取標準必要 IBM ID 及密碼以外的帳戶。您帳戶的多因子鑑別會套用至已鏈結 {{site.data.keyword.Bluemix_notm}} 帳戶中的所有資源。針對您的帳戶啟用它時，它也會套用至已新增至您帳戶的所有使用者。請進一步瞭解要在針對您的帳戶[啟用多因子鑑別](/docs/iam/mfa.html)時檢閱的考量。

多因子鑑別不是根據 IBM ID。它仍是根據帳戶。當 IBM ID 與多個帳戶相關聯，且您在帳戶之間切換時，每次切換到需要雙因子鑑別的不同帳戶時都必須確認身分。即使前一個帳戶和新的帳戶都已配置相同的雙因子鑑別機制時也是如此。
