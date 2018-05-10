---

copyright:

  years: 2015, 2018

lastupdated: "2017-11-10"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# {{site.data.keyword.Bluemix_notm}} 存取的疑難排解
{: #accessing}

在存取 {{site.data.keyword.Bluemix}} 時發生的一般問題，可能包括無法登入 {{site.data.keyword.Bluemix_notm}}，或是帳戶處於擱置狀態。在許多情況下，您可以遵照一些簡單的步驟，從這些問題回復。
{:shortdesc}

## 密碼不正確
{: #ts_logintobm}

您必須要有與 IBM ID 相關聯的有效密碼，才能登入 {{site.data.keyword.Bluemix_notm}} 主控台。

您必須要有與 IBM ID 或已鏈結帳戶 ID 相關聯的有效密碼，才能透過 [{{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com){: new_window} 登入。

當您嘗試登入 {{site.data.keyword.Bluemix_notm}} 時，顯示下列錯誤訊息：
{: tsSymptoms}

`The password that you entered is not correct.`

您用來登入 {{site.data.keyword.Bluemix_notm}} 的密碼無效。
{: tsCauses}

使用下列其中一個解決方案：
{: tsResolve}
 * 輸入正確的密碼。若要檢查您的 IBM ID 和密碼是否有效，您可以移至「我的 IBM 設定檔」頁面，按一下**登入**，然後在「登入」頁面上輸入您的 IBM ID 和密碼。
 * 如果您忘記密碼，請按一下**忘記密碼**來重設密碼。然後，回到 [{{site.data.keyword.Bluemix_notm}} 主控台 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.{DomainName}){: new_window} 或 [{{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com){: new_window}，並重新登入。
 * 如果您忘記 IBM ID 或是持續發生密碼問題，請與 Worldwide IBM Registration Help Desk 聯絡以取得協助。
 * 若要取得有效的 IBM ID 和密碼，請移至「我的 IBM 設定檔」頁面，然後按一下**登錄**。

附註：
<!-- begin STAGING ONLY -->
 * 對於 IBM 員工，您的 IBM ID 可能與您的內部網路 ID 不同。
 <!-- end STAGING ONLY -->
 * 如果您在「登入 IBM」頁面上，而登入處理程序因任何原因（例如，正在重設密碼）而中斷，請回到 [{{site.data.keyword.Bluemix_notm}} 主控台 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.{DomainName}){: new_window} 或 [{{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com){: new_window}，並重新開始登入處理程序。


## 登入認證無效
{: #ts_login_invalid_credentials}

當您使用 IBM ID 登入時，顯示下列訊息：
{: tsSymptoms}

`提供的登入認證無效。如果您有與帳戶相關聯的 IBM ID，請在這裡登入`

* 您已切換至 IBM ID，但嘗試使用先前的使用者名稱及密碼透過 [{{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com){: new_window} 登入。
{: tsCauses}

* 您嘗試透過 [{{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com){: new_window} 登入，但在「使用者名稱」及「密碼」欄位中輸入您的 IBM ID 及密碼。

按一下訊息中的**在這裡登入**，或移至「IBM ID 帳戶登入」區段，然後按一下**使用 IBM ID 登入**。
{: tsResolve}

請不要使用用於前一個 ID 的**使用者名稱**及**密碼**欄位。


## 無法辨識的 IBM ID 或電子郵件
{: #ts_old_username}

當您登入 {{site.data.keyword.Bluemix_notm}} 主控台時，顯示下列訊息：
{: tsSymptoms}

`We didn't recognize this IBMid or email.`

您嘗試登入 {{site.data.keyword.Bluemix_notm}} 主控台，但未使用有效的 IBM ID。例如，您未輸入 IBM ID 的完整電子郵件位址，或是嘗試使用先前的使用者名稱和密碼。
{: tsCauses}

您必須具有有效的 IBM ID 及密碼才能登入 {{site.data.keyword.Bluemix_notm}}。

 * 確定您輸入的是 IBM ID 的完整電子郵件位址。
 {: tsResolve}
 * 如果您是具有 {{site.data.keyword.BluSoftlayer_full}} ID 的 {{site.data.keyword.BluSoftlayer_full}} 使用者，則必須先在 {{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站中，於您可存取的每一個帳戶中切換至 IBM ID 鑑別，才能使用 IBM ID 鑑別登入。
 如需相關資訊，請參閱[切換至 IBM ID](/docs/account/softlayerlink.html#switching-to-ibmid)。


## IBM ID 未與任何 IBM Cloud 帳戶相關聯
{: #ts_login_noswitch}

當您使用 IBM ID 登入時，顯示下列訊息：
{: tsSymptoms}

`You have reached this page because your authentication was successful, however, this IBMid is not associated with any IBM Cloud accounts. If you believe this to be in error, contact your Account Owner or Master User.`

您已從 [{{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com){: new_window} 使用有效的 IBM ID 進行登入，但未從 {{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站中切換至 IBM ID 鑑別。
{: tsCauses}

請視情況完成下列檢查：
{: tsResolve}
 * 與主要使用者或帳戶管理者聯絡，確定您可以切換至 IBM ID 鑑別。
 * 確定您完成「切換至 IBM ID」步驟。請參閱[切換至 IBM ID](/docs/account/softlayerlink.html#switching-to-ibmid)。
 * 確定您遵循**建立使用者 ID 與 IBM ID 的關聯**電子郵件中的動作。檢查您的收件匣及垃圾郵件資料夾，以尋找此電子郵件。若要重新取得電子郵件（例如，如果它已到期），請移至 {{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站中的「編輯使用者設定檔」頁面，然後按一下**重新傳送電子郵件**。或者，請聯絡 [{{site.data.keyword.Bluemix_notm}} 支援中心 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://ibm.biz/bluemixsupport.com){: new_window}。

**附註：**如果您是直接以 IBM ID 來建立您的 IBM ID，則會收到兩封要處理的電子郵件；一封來自 IBM ID 登錄，另一封來自 {site.data.keyword.Blu_full}}。請務必遵循這兩封電子郵件中的動作。

視帳戶的設定方式而定，您可能可以使用其中一些登入選項：
 * 具有 {{site.data.keyword.BluSoftlayer_full}} ID 的 {{site.data.keyword.BluSoftlayer_notm}} 使用者必須透過 [{{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com){: new_window} 登入。
 * 具有 IBM ID 並且具有（或沒有）已鏈結 {{site.data.keyword.Bluemix_notm}} 帳戶的 {{site.data.keyword.BluSoftlayer_notm}} 使用者，可以透過 [{{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com){: new_window} 登入來開啟 {{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站，或透過 [{{site.data.keyword.Bluemix_notm}} 主控台 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.{DomainName}){: new_window} 來開啟「基礎架構」儀表板。


## IBM ID 未與任何 {{site.data.keyword.Bluemix_notm}} 帳戶相關聯
{: #ts_unabletologin}

當您登入 {{site.data.keyword.Bluemix_notm}} 時，顯示下列訊息：
{: tsSymptoms}

`You have reached this page because your authentication was successful, however, this IBMid is not associated with any  {{site.data.keyword.Bluemix_notm}} accounts.`

您已從 [{{site.data.keyword.Bluemix_notm}} 主控台 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.{DomainName}){: new_window} 使用有效的 IBM ID 進行登入，但尚未建立 {{site.data.keyword.Bluemix_notm}} 帳戶。
{: tsCauses}

若要建立 {{site.data.keyword.Bluemix_notm}} 帳戶，請遵循註冊處理程序。
{: tsResolve}

視帳戶的設定方式而定，您可能可以使用其中一些登入選項：
 * 沒有已鏈結帳戶的 {{site.data.keyword.Bluemix_notm}} 使用者必須透過 {{site.data.keyword.Bluemix_notm}} 主控台登入。
 * 具有已鏈結帳戶的 {{site.data.keyword.Bluemix_notm}} 使用者可以透過 [{{site.data.keyword.Bluemix_notm}} 主控台 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.{DomainName}){: new_window} 或 [{{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com){: new_window} 登入。


## 主控台未開啟
{: #ts_login_stalls}

當您使用 IBM ID 登入時，會顯示登入成功訊息，但您未回到 [{{site.data.keyword.Bluemix_notm}} 主控台 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.{DomainName}){: new_window} 或 [{{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com){: new_window}
{: tsSymptoms}

使用下列其中一個解決方案：
{: tsResolve}
 * 關閉您的瀏覽器，清除快取和 Cookie，然後嘗試重新登入。
 * 確定您是從 [{{site.data.keyword.Bluemix_notm}} 主控台 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.{DomainName}){: new_window} 或 [{{site.data.keyword.BluSoftlayer_notm}} 基礎架構客戶入口網站 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://control.softlayer.com){: new_window} 登入，而不是直接從 IBM ID 鑑別服務登入。


## IBM ID 登入未完成
{: #ts_login_ibmid}

當您登入 {{site.data.keyword.Bluemix_notm}} 時，未完成以 IBM ID 進行鑑別。
{: tsSymptoms}

IBM ID 鑑別服務可能有問題。
{: tsCauses}

在 [IBM IBMid ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://new.wind.ibmcloud.com/webapp/#/status/a1a0c5d743d94a6a9597087541564d8e){: new_window} 檢查服務狀態，然後重試。
{: tsResolve}


## 帳戶擱置
{: #ts_accntpding}

如果您的帳戶處於擱置狀態，即無法登入 {{site.data.keyword.Bluemix_notm}}。

在登錄取得 {{site.data.keyword.Bluemix_notm}} 試用帳戶之後，您可能無法登入 {{site.data.keyword.Bluemix_notm}}。系統會顯示下列訊息：
{: tsSymptoms}

<code>您的帳戶處於擱置狀態。請稍候，最晚 24 小時即會收到電子郵件確認信，同時也請檢查垃圾郵件資料夾。如果您仍未收到確認電子郵件，請與 <a href="http://ibm.biz/bluemixsupport.com" target="_blank">{{site.data.keyword.Bluemix_notm}} 支援中心</a>聯絡。</code>

在登錄取得 {{site.data.keyword.Bluemix_notm}} 試用帳戶之後，您會收到一封確認電子郵件。您必須按一下此封確認電子郵件中的鏈結，才能完成登錄程序。
{: tsCauses}

確認電子郵件會寄送到您提供的電子郵件位址。檢查您的收件匣和垃圾郵件資料夾。如果您尚未收到確認電子郵件，請與 [{{site.data.keyword.Bluemix_notm}} 支援中心 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://ibm.biz/{{site.data.keyword.Bluemix_notm}}support.com){: new_window} 聯絡。  
{: tsResolve}


<!-- begin STAGING ONLY -->

## 存取外部網站時發生問題
{: #ts_bmlinkid}

若要使用 IBM 內部網路 ID 來登入 {{site.data.keyword.Bluemix_notm}}，您必須鏈結內部網路 ID 與 IBM ID。

從「{{site.data.keyword.Bluemix_notm}} 登入」頁面選取**使用內部網路 ID 進行登入**之後，可能會顯示下列訊息：
{: tsSymptoms}

`存取外部網站時發生問題`

使用未鏈結至 IBM ID 的 IBM 內部網路 ID 登入 {{site.data.keyword.Bluemix_notm}} 時，會發生此問題。IBM ID 是您用來登入 www.ibm.com 的 ID。
{: tsCauses}

身為 IBM 員工，您必須先鏈結內部網路 ID 與外部 IBM ID，才能使用 IBM 內部網路 ID 來登入 {{site.data.keyword.Bluemix_notm}}。若要鏈結這兩個 ID，請完成下列步驟：
{: tsResolve}

  1. 在[中央登入 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://w3-03.sso.ibm.com/tools/cso/index.jsp){: new_window} 頁面上，按一下**我的登入**。
  2. 在「我的登入」頁面上，按一下**鏈結 ID**，然後在「{{site.data.keyword.Bluemix_notm}} 登入」頁面上輸入 IBM ID 及密碼。在那之後，將會自動鏈結內部網路 ID 及 IBM ID。


<!-- end STAGING ONLY -->

## 無法載入 {{site.data.keyword.Bluemix_notm}} 頁面
{: #ts_err}

當您使用 {{site.data.keyword.Bluemix_notm}} 主控台時，可能無法載入主控台頁面。反之，可能會看到錯誤訊息 BXNUI0001E 或 BXNUI0016E。

當您使用 {{site.data.keyword.Bluemix_notm}} 主控台時，可能會看到下列其中一則錯誤訊息：
{: tsSymptoms}

`BXNUI0001E: The page wasn't loaded because {{site.data.keyword.Bluemix_notm}} didn't detect whether a session exists.`

`BXNUI0016E: The apps and services weren't retrieved because an {{site.data.keyword.Bluemix_notm}} page didn't load.`

請視需要完成下列一個以上的動作：
{: tsResolve}

  * 重新整理或重新啟動瀏覽器。
  * 登出 {{site.data.keyword.Bluemix_notm}} 然後再重新登入。
  * 使用瀏覽器的專用瀏覽模式。
  * 清除瀏覽器的 Cookie 及快取。
  * 使用不同的瀏覽器。如需 {{site.data.keyword.Bluemix_notm}} 所支援瀏覽器版本的相關資訊，請參閱 [{{site.data.keyword.Bluemix_notm}} 必要條件](/docs/overview/whatisbluemix.html#prereqs)。
  * 如果您已安裝 cf 指令行介面，請輸入 `cf apps` 指令，以查看您的應用程式是否正在執行中。
