---

copyright:

  years: 2016, 2018

lastupdated: "2018-11-17"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# 切換至 IBM ID 並鏈結帳戶
{: #unifyingaccounts}

IBM ID 是您用來登入 {{site.data.keyword.Bluemix}} 帳戶以便存取及購買基礎架構、服務及應用程式特性的單一 ID。所有新帳戶會自動收到 IBM ID，而現有的 SoftLayer 帳戶（SAML 聯合帳戶除外）會啟用切換至 IBM ID 鑑別。
{:shortdesc}

## 切換至 IBM ID
{: #switchtoIBMid}

開始切換至 IBM ID 的程序時，在完成這項程序之前，您隨時都可以取消此切換作業。不過，在您每次登入時，都會顯示切換至 IBM ID 的提示。您計劃要鏈結至 {{site.data.keyword.Bluemix_notm}} 帳戶的每一個 SoftLayer 帳戶，都必須為具有唯一電子郵件位址的唯一 IBM ID 所擁有。

若要將現有 SoftLayer 帳戶切換至 IBM ID，您需要建立 IBM ID 然後使用登錄碼來確認它。

### 要求 IBM ID 及登錄碼
{: #reqIBMidandregcode}

1. 登入 SoftLayer 帳戶，並在顯示切換至 IBM ID 的提示時按一下**確定**。

   如果您是主要使用者，而客戶入口網站中未顯示切換至 IBM ID 的提示，請與 IBM 支援中心聯絡以取得協助。如需與支援中心聯絡的相關資訊，請參閱[取得支援](/docs/get-support/howtogetsupport.html#getting-customer-support)。

   如果您先前已登入，並在提示時按了**稍後**，但想要在現行階段作業中切換至 IBM ID 鑑別，請移至「編輯使用者設定檔」頁面，然後按一下**切換至 IBM ID**。

2. 遵循精靈提示，以建立您的 IBM ID。

   輸入目前未被任何 IBM ID 使用的電子郵件位址。此電子郵件位址是用來作為新 IBM ID 的使用者名稱，而且在建立 IBM ID 之後會將登錄碼傳送到此處。您之後可以更新與 IBM ID 相關聯的電子郵件位址，但是無法變更使用者名稱。

### 使用登錄碼來確認 IBM ID
{: #confIBMiduseregcode}

1. 當您收到登錄碼時，請按一下電子郵件中的鏈結，或將 URL 複製到瀏覽器，並輸入登錄碼。登錄碼的有效時間是 7 天，而且只能使用一次。

2. 提交登錄碼之後，請使用 IBM ID 來登入客戶入口網站。

   在「帳戶登入」提示中，移至 **IBM ID 帳戶登入**區段，然後按一下**使用 IBM ID 登入**。請不要使用您之前用於 Softlayer ID 的**使用者名稱**和**密碼**欄位。

如果您是新客戶，當您查看訂單時，系統會要求您提供現有的 IBM ID 或建立新的 IBM ID。
  * 若要使用現有的 IBM ID，請輸入使用者名稱，或 IBM ID 的電子郵件位址（如果它未在多個 IBM ID 之間共用的話）。
  * 若要建立新的 IBM ID，請輸入目前未被任何 IBM ID 使用的電子郵件位址。此電子郵件位址是 IBM ID 的使用者名稱，而且是在建立 IBM ID 之後傳送登錄碼的位置。您之後可以更新與 IBM ID 相關聯的電子郵件位址，但是無法變更使用者名稱。

若要解決使用 IBM ID 進行登入的所有問題，請參閱 [{{site.data.keyword.Bluemix_notm}} 存取的疑難排解](/docs/account/ts_accessing.html#accessing)。


## 鏈結 IBM ID 帳戶
{: #link_accounts}

帳戶切換至 IBM ID 帳戶之後，您可以鏈結 SoftLayer 帳戶及 {{site.data.keyword.Bluemix_notm}} 帳戶，以利用合併的基礎架構即服務 (Iaas) 及平台即服務 (PaaS) 資源。然後，您就可以從單一登入存取 IaaS 資源和 PaaS 資源。鏈結您的帳戶也會讓您針對您使用的所有 PaaS 及 IaaS 資源收到單一張帳單。您可以鏈結自己的帳戶，或者，如果您是主要使用者，則可以鏈結您的使用者帳戶。

### 鏈結 IBM ID 帳戶
{: #link_user_account}

如果您是標準基礎架構客戶，且您的 {{site.data.keyword.Bluemix_notm}} 中也有 PaaS 帳戶或是建立它們，則可以鏈結 IaaS 和 PaaS 來取得帳戶的單一視圖。若要鏈結帳戶，請使用下列步驟：
1. 登入您的 SoftLayer 帳戶。
2. 從「帳戶摘要」頁面，按一下**新增功能！鏈結 Bluemix 帳戶**。
3. 檢閱使用條款，並按一下以確認接受。
4. 根據帳戶的設定方式，完成下列其中一個最終步驟：
  * 如果您的 IBM ID 有相關聯的 {{site.data.keyword.Bluemix_notm}} 帳戶，會導向至授權頁面，然後回到最終確認步驟。
  * 如果您沒有相關聯的 {{site.data.keyword.Bluemix_notm}} 帳戶，則系統會提示您建立新帳戶。

若要查看有關鏈結帳戶的一般問與答，請參閱[常見問題](/docs/account/account_faq.html#al_login)。

### 鏈結 IBM ID 使用者帳戶
{: #link_customer_accounts}

在您的使用者帳戶切換至 IBM ID 鑑別之後，轉銷商及經銷商就可以鏈結他們的使用者帳戶。您必須是 SoftLayer 主要使用者，才能鏈結客戶帳戶。作為帳戶之主要使用者的 IBM ID 必須是您所要鏈結的 {{site.data.keyword.Bluemix_notm}} 平台帳戶的擁有者。 

帳戶在鏈結之後，即無法解除鏈結。
{: note}

請務必檢閱有關鏈結帳戶的下列重要注意事項：

  * 所鏈結 SoftLayer 帳戶的主要使用者必須具有 IBM ID。
  * 您鏈結至 {{site.data.keyword.Bluemix_notm}} 帳戶的每一個使用者帳戶，都必須為具有唯一電子郵件位址的唯一 IBM ID 所擁有。即使單一 IBM ID 可以擁有多個 SoftLayer 帳戶，您還是必須為每一個帳戶將主要使用者變更為唯一 IBM ID。請與支援中心聯絡，以變更 SoftLayer 帳戶的主要使用者。如需相關資訊，請參閱[取得 {{site.data.keyword.Bluemix_notm}} 基礎架構的支援](/docs/customer-portal/cpsupport.html)。
  * 將新使用者新增至已鏈結帳戶時，您必須將他們同時新增至 SoftLayer 帳戶及 {{site.data.keyword.Bluemix_notm}} 帳戶，他們才能存取統一主控台的所有功能。
  * 如果您有品牌帳戶、使用 Brand Agent Portal (BAP)，而且在鏈結帳戶時需要支援，則請傳送電子郵件到下列位址以與 Revenue Services 團隊聯絡：softlayer_revenue_services_team@wwpdl.vnet.ibm.com。

完成下列步驟，以將每一個 SoftLayer 帳戶鏈結至現有的 {{site.data.keyword.Bluemix_notm}} 平台帳戶或建立新帳戶：

   1. 使用您的主要使用者帳戶 IBM ID 來登入客戶入口網站。
   2. 從客戶入口網站中，按一下**鏈結 Bluemix 帳戶**。
   3. 閱讀並接受將 SoftLayer 帳戶與 {{site.data.keyword.Bluemix_notm}} 帳戶鏈結所適用的條款。
   4. 請遵循精靈提示（包括將 SoftLayer 帳戶中的使用者新增至 {{site.data.keyword.Bluemix_notm}} 帳戶）。
   5. 看到提示時，請執行下列其中一個動作：
     * 如果您已有 {{site.data.keyword.Bluemix_notm}} 帳戶，請提供與該帳戶相關聯的電子郵件位址來鏈結帳戶。
     * 如果您沒有 {{site.data.keyword.Bluemix_notm}} 帳戶，請提供您要使用的電子郵件位址，並遵循指示以受邀加入 {{site.data.keyword.Bluemix_notm}}，然後建立帳戶。
   6. 在您鏈結帳戶之後，請遵循前面[切換至 IBM ID](/docs/account/softlayerlink.html#switchtoIBMid) 一節中所述的程序，通知每一個帳戶的一般使用者以移轉至 IBM ID。

      僅將一般使用者帳戶移轉至 IBM ID。請不要移轉品牌帳戶，這是一般使用者帳戶的母帳戶，未包含任何資源。移轉至 IBM ID 的品牌帳戶使用者將無法登入 Brand Agent Portal (BAP)。
      {: important}

請注意，鏈結帳戶之後有下列變更：
  
  * 您現在會登入 [{{site.data.keyword.Bluemix}} 主控台 ![外部鏈結圖示](../icons/launch-glyph.svg)](https://cloud.ibm.com){: new_window}。
  * 您必須使用 IBM ID 認證來存取 SoftLayer 及 {{site.data.keyword.Bluemix_notm}} 帳戶。
  * 任何現有 SoftLayer 折扣都會套用至 {{site.data.keyword.Bluemix_notm}} 費用。
  * 您收到一張計價單位為美元 (USD) 的發票。如果您有現有的 {{site.data.keyword.Bluemix_notm}} 帳戶，則會在鏈結帳戶之後開始的新計費週期，透過 {{site.data.keyword.Bluemix_notm}} 收取基礎架構資源的費用。如需相關資訊，請參閱[已鏈結帳戶的合併計費](/docs/customer-portal/linking_accounts.html)。
  * 您可以在 {{site.data.keyword.Bluemix_notm}} 主控台中監視標準基礎架構資源的用量。

## 已鏈結帳戶中的多因子鑑別使用
{: #2fa}

如果您具有已鏈結帳戶，則可以使用 {{site.data.keyword.Bluemix_notm}} IAM 的**設定**頁面來啟用帳戶的多因子鑑別 (MFA)。這通常也稱為雙因子鑑別 (2FA)，而且它會新增安全層來存取標準必要 IBM ID 及密碼以外的帳戶。您帳戶的 MFA 會套用至已鏈結 {{site.data.keyword.Bluemix_notm}} 帳戶中的所有資源。針對您的帳戶啟用它時，它也會套用至已新增至您帳戶的所有使用者。

其他多因子鑑別方法並不是根據 IBM ID。它是根據帳戶。當 IBM ID 與多個帳戶相關聯，且您在帳戶之間切換時，每次切換到需要雙因子鑑別的不同帳戶時都必須確認身分。即使前一個帳戶和新的帳戶都已配置相同的雙因子鑑別機制時也是如此。

如果您先前[在客戶入口網站啟用了標準基礎架構資源的 2FA](/docs/customer-portal/cpenable2fa.html#customerportal_2fa)，然後啟用了 {{site.data.keyword.Bluemix_notm}} 帳戶 MFA 設定，則 MFA 帳戶設定會置換您在客戶入口網站中設定的 2FA。這表示您可以停用在客戶入口網站中購買的 2FA，而支持帳戶 MFA 設定。 
