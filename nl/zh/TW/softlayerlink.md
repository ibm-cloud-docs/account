---



copyright:

  years: 2016, 2018
lastupdated: "2018-01-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 切換至 IBM ID
SoftLayer 中的鑑別現在使用 IBM ID 來提供所有 {{site.data.keyword.Bluemix}} 的單一登入。讓現有 SoftLayer 帳戶可切換至 IBM ID 鑑別。移轉精靈會引導您完成這項切換。
{:shortdesc}

開始切換至 IBM ID 的程序時，在完成這項程序之前，您隨時都可以取消此切換作業。不過，在您每次登入時，都會顯示切換至 IBM ID 的提示。您計劃要鏈結至 {{site.data.keyword.Bluemix_notm}} 帳戶的每一個 SoftLayer 帳戶，都必須為具有唯一電子郵件位址的唯一 IBM ID 所擁有。

若要將現有 SoftLayer 帳戶切換至 IBM ID，請完成下列步驟：
1. 登入 SoftLayer 帳戶，並在顯示切換至 IBM ID 的提示時按一下**確定**。

   如果您是主要使用者，而 {{site.data.keyword.slportal}} 中未顯示切換至 IBM ID 的提示，請與 [IBM 支援中心](/docs/get-support/howtogetsupport.html#getting-customer-support)聯絡以取得協助。

   如果您先前已登入，並在提示時按了**稍後**，但想要在現行階段作業中切換至 IBM ID 鑑別，請移至「編輯使用者設定檔」頁面，然後按一下**切換至 IBM ID**。

2. 遵循精靈提示，以建立您的 IBM ID。

   輸入目前未被任何 IBM ID 使用的電子郵件位址。此電子郵件位址是用來作為新 IBM ID 的使用者名稱，而且是在建立 IBM ID 之後傳送登錄碼的位置。您之後可以更新與 IBM ID 相關聯的電子郵件位址，但是無法變更使用者名稱。

3. 當您收到登錄碼時，請按一下電子郵件中的鏈結，或將 URL 複製到瀏覽器，並輸入登錄碼。

   登錄碼的有效時間是 7 天，而且只能使用一次。

4. 提交登錄碼之後，請使用 IBM ID 來登入客戶入口網站。

   在「帳戶登入」提示中，移至 **IBM ID 帳戶登入**區段，然後按一下**使用 IBM ID 登入**。請不要使用您之前用於 Softlayer ID 的**使用者名稱**和**密碼**欄位。

如果您是新客戶，當您查看訂單時，系統會要求您提供現有的 IBM ID 或建立新的 IBM ID。
  * 若要使用現有的 IBM ID，請輸入使用者名稱，或唯一的 IBM ID 電子郵件位址（亦即，不是多個 IBM ID 所共用的）。

  * 若要建立新的 IBM ID，請輸入目前未被任何 IBM ID 使用的電子郵件位址。此電子郵件位址是 IBM ID 的使用者名稱，而且是在建立 IBM ID 之後傳送登錄碼的位置。您之後可以更新與 IBM ID 相關聯的電子郵件位址，但是無法變更使用者名稱。

若要解決使用 IBM ID 登入的所有問題，請參閱 [{{site.data.keyword.Bluemix_notm}} 存取疑難排解](/docs/get-support/ts_accessing.html#accessing)。

## 啟用 IBM ID 鑑別的使用者帳戶
{: #link_accounts_resellers}

在部分情況下，轉銷商或經銷商必須允許帳戶使用 IBM ID 鑑別，使用者才能切換至 IBM ID。

  * 對於每一個您要鏈結至 {{site.data.keyword.Bluemix_notm}} 帳戶的現有使用者帳戶，都必須啟用 IBM ID 鑑別。然後，每一位使用者都必須使用移轉精靈來完成切換至 IBM ID 的程序，如前一節所述。請與 [IBM 支援中心](/docs/get-support/howtogetsupport.html#getting-customer-support)聯絡，讓現有 SoftLayer 帳戶使用 IBM ID 鑑別。

  * 若要確保使用 IBM ID 來建立新的使用者帳戶，則必須在立即主要使用者帳戶上設定 `CREATE_NEW_ACCOUNT_WITH_IBMid_AUTHENTICATION` 屬性。請與 [IBM 支援中心](/docs/get-support/howtogetsupport.html#getting-customer-support)或供應商聯絡，為您的帳戶設定屬性。  

## 鏈結 IBM ID 使用者帳戶
{: #link_user_accounts}

在您的使用者帳戶切換至 IBM ID 鑑別之後，轉銷商及經銷商就可以鏈結 SoftLayer 及 {{site.data.keyword.Bluemix_notm}} 帳戶，以利用合併的基礎架構及平台資源。請務必檢閱下列重要注意事項：

  * 所鏈結帳戶的主要使用者必須具有 IBM ID。
  * 您鏈結至 {{site.data.keyword.Bluemix_notm}} 帳戶的每一個使用者帳戶，都必須為具有唯一電子郵件位址的唯一 IBM ID 所擁有。即使單一 IBM ID 可以擁有多個 SoftLayer 帳戶，您還是必須為每一個帳戶將主要使用者變更為唯一 IBM ID。請與 [IBM SoftLayer 支援中心 ![外部鏈結圖示](../icons/launch-glyph.svg)](https://knowledgelayer.softlayer.com/topic/support){: new_window} 聯絡，以變更 SoftLayer 帳戶的主要使用者。
  * 將新使用者新增至鏈結的帳戶時，您必須將他們同時新增至 SoftLayer 帳戶及 {{site.data.keyword.Bluemix_notm}} 帳戶，他們才能存取統一主控台的所有功能。

完成下列步驟，以將每一個帳戶鏈結至 {{site.data.keyword.Bluemix_notm}} 帳戶：
1. 若要鏈結至現有 {{site.data.keyword.Bluemix_notm}} 帳戶或建立新的帳戶，請以主要使用者身分登入客戶入口網站，然後按一下 {{site.data.keyword.Bluemix_notm}} 鏈結。

   作為帳戶之主要使用者的 IBM ID 必須是您所要鏈結的 {{site.data.keyword.Bluemix_notm}} 帳戶的擁有者。

2. 請遵循精靈提示（包括將 SoftLayer 帳戶中的使用者新增至 {{site.data.keyword.Bluemix_notm}} 帳戶）。
3. 在您鏈結帳戶之後，請遵循前一節中所述的程序，通知每一個帳戶的一般使用者以移轉至 IBM ID。

僅將一般使用者帳戶移轉至 IBM ID。請不要移轉品牌帳戶，這是一般使用者帳戶的母帳戶，未包含任何資源。移轉至 IBM ID 的品牌帳戶使用者將無法登入 Brand Agent Portal (BAP)。
{: tip}  

## 已鏈結帳戶中的多因子鑑別使用
{: #2fa}

如果您具有已鏈結帳戶，則可以使用「身分及存取」的**設定**頁面來啟用帳戶的多因子鑑別 (/docs/iam/mfa.html)。這通常也稱為雙因子鑑別 (2FA)，而且它會新增安全層來存取標準必要 IBM ID 及密碼以外的帳戶。您帳戶的多因子鑑別會套用至已鏈結 {{site.data.keyword.Bluemix_notm}} 帳戶中的所有資源。針對您的帳戶啟用它時，它也會套用至已新增至您帳戶的所有使用者。請進一步瞭解要在針對您的帳戶[啟用多因子鑑別](/docs/iam/mfa.html)時檢閱的考量。

多因子鑑別不是根據 IBM ID。它仍是根據帳戶。當 IBM ID 與多個帳戶相關聯，且您在帳戶之間切換時，每次切換到需要雙因子鑑別的不同帳戶時都必須確認身分。即使前一個帳戶和新的帳戶都已配置相同的雙因子鑑別機制時也是如此。

<!-- Above section is for MFA release 1/2018. Commented out section here has old content.
If you enabled two-factor authentication for your existing SoftLayer account, you are still required to enter your security code when logging in to the {{site.data.keyword.Bluemix_notm}} console. However, the two-factor authentication applies only to the resources in your Infrastructure account. You might be able to do various actions to the resources in your {{site.data.keyword.Bluemix_notm}} account without doing two-factor authentication.
Two-factor authentication is not per IBMid. It is still per account. When an IBMid is associated with multiple accounts, and you switch between accounts, you must confirm your identity every time you switch to a different account that requires two-factor authentication. This is true even if the prior account and the new account are both configured with the same two-factor authentication mechanism.
-->

