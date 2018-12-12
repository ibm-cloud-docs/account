---

copyright:

  years: 2015, 2018

lastupdated: "2018-11-28"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# {{site.data.keyword.Bluemix_notm}} 存取的疑難排解
{: #accessing}

在存取 {{site.data.keyword.Bluemix}} 時發生的一般問題，可能包括無法登入 {{site.data.keyword.Bluemix_notm}}，或是帳戶處於擱置狀態。在許多情況下，您可以遵照一些簡單的步驟，從這些問題回復。
{:shortdesc}


## 為什麼我的密碼不正確？
{: #ts_logintobm}
{: troubleshoot}

您必須要有與 IBM ID 或 SoftLayer ID 相關聯的有效密碼，才能登入 {{site.data.keyword.Bluemix_notm}} 主控台。

當您嘗試登入 {{site.data.keyword.Bluemix_notm}} 時，顯示下列錯誤訊息：
{: tsSymptoms}

`The password that you entered is not correct.`

您用來登入 {{site.data.keyword.Bluemix_notm}} 的密碼無效。
{: tsCauses}

請使用下列其中一個選項：
{: tsResolve}
 * 移至[我的 IBM 設定檔頁面 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://myibm.ibm.com/dashboard/){: new_window}，以確認您使用的是有效的密碼。
 * 如果您忘記密碼，請按一下**忘記密碼**來重設密碼。 
 * 如果您忘記 IBM ID 或是持續發生密碼問題，請與 Worldwide IBM Registration Help Desk 聯絡以取得協助。

如果您登入 {{site.data.keyword.Bluemix_notm}}，而登入處理程序因任何原因（例如重設密碼）而中斷，請回到主控台，然後再重新開始登入處理程序
{: tip}


## 為什麼我的 IBM ID 或電子郵件無法辨識？
{: #ts_old_username}
{: troubleshoot}

若要順利登入您的電子郵件，您必須確定每個帳戶都有 IBM ID 鑑別。

當您登入 {{site.data.keyword.Bluemix_notm}} 主控台時，顯示下列訊息：
{: tsSymptoms}

`We didn't recognize this IBMid or email.`

您嘗試登入主控台，但未使用有效的 IBM ID。例如，您未輸入 IBM ID 的完整電子郵件位址，或是嘗試使用先前的使用者名稱和密碼。
{: tsCauses}

您必須具有有效的 IBM ID 及密碼才能登入 {{site.data.keyword.Bluemix_notm}}。

 * 輸入 IBM ID 的完整電子郵件位址。
 {: tsResolve}
 * 如果您是具有 SoftLayer ID 的 SoftLayer 使用者，則必須先在您具有存取權的每個帳戶中切換至 IBM ID 鑑別，然後才能登入。如需相關資訊，請參閱[切換至 IBM ID](/docs/account/softlayerlink.html)。


## 為什麼我的 IBM ID 未與任何 {{site.data.keyword.Bluemix_notm}} 帳戶相關聯？
{: #ts_unabletologin}
{: troubleshoot}

當您登入 {{site.data.keyword.Bluemix_notm}} 時，顯示下列訊息：
{: tsSymptoms}

`You have reached this page because your authentication was successful, however, this IBMid is not associated with any  {{site.data.keyword.Bluemix_notm}} accounts.`

您已從 [{{site.data.keyword.Bluemix_notm}} 主控台 ](https://{DomainName}){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示") 使用有效的 IBM ID 進行登入，但並未建立 {{site.data.keyword.Bluemix_notm}} 帳戶。
{: tsCauses}

若要建立 {{site.data.keyword.Bluemix_notm}} 帳戶，請遵循註冊處理程序。
{: tsResolve}


## 當我使用 IBM ID 登入時，為什麼主控台未開啟？
{: #ts_login_stalls}
{: troubleshoot}

當您收到登入成功訊息，但未回到主控台時。

當您使用 IBM ID 登入時，會顯示登入成功訊息，但您未回到 [{{site.data.keyword.Bluemix_notm}} 主控台](https://{DomainName}){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")。
{: tsSymptoms}

請使用下列其中一個選項：
{: tsResolve}
 * 關閉您的瀏覽器，清除快取和 Cookie，然後嘗試重新登入。
 * 從 [{{site.data.keyword.Bluemix_notm}} 主控台](https://{DomainName}){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示") 登入。


## 為什麼我的 IBM ID 登入未完成？
{: #ts_login_ibmid}
{: troubleshoot}

如果您登入 F{site.data.keyword.Bluemix_notm}}，且 IBM ID 鑑別未完成，則表示服務可能有問題。 

當您登入 {{site.data.keyword.Bluemix_notm}} 時，未完成以 IBM ID 進行鑑別。
{: tsSymptoms}

IBM ID 鑑別服務可能有問題。
{: tsCauses}

請確定您可以登入 [IBM](https://idaas.iam.ibm.com/idaas/mtfim/sps/authsvc?PolicyId=urn:ibm:security:authentication:asf:basicldapuser){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")。如果可以，便是應用程式的問題，您可以稍後再嘗試登入主控台。如果無法登入該頁面，請洽詢 [IBM ID 服務台 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}。  
{: tsResolve}


## 在登錄帳戶之後，為什麼我無法立即登入？
{: #ts_accntpding}
{: troubleshoot}

如果您的帳戶處於擱置狀態，即無法登入 {{site.data.keyword.Bluemix_notm}}。

在登錄取得 {{site.data.keyword.Bluemix_notm}} 精簡帳戶之後，您可能無法登入 {{site.data.keyword.Bluemix_notm}}。系統會顯示下列訊息：
{: tsSymptoms}

<code>您的帳戶處於擱置狀態。請稍候，最晚 24 小時即會收到電子郵件確認信，同時也請檢查垃圾郵件資料夾。如果您仍未收到確認電子郵件，請與 <a href="http://ibm.biz/bluemixsupport.com" target="_blank">{{site.data.keyword.Bluemix_notm}} 支援中心</a>聯絡。</code>

當您登錄 {{site.data.keyword.Bluemix_notm}}「精簡」帳戶時，會收到一封電子郵件，其中包含一個鏈結，您必須按一下以確認登錄。  
{: tsCauses}

確認電子郵件會傳送至與您 IBM ID 相關聯的電子郵件位址。檢查您的收件匣和垃圾郵件資料夾。如果未收到確認電子郵件，請與 [{{site.data.keyword.Bluemix_notm}} 支援中心](/docs/get-support/howtogetsupport.html)聯絡。  
{: tsResolve}


## 為什麼我會遇到無法載入的主控台頁面？
{: #ts_err}
{: troubleshoot}

當您使用 {{site.data.keyword.Bluemix_notm}} 主控台時，可能無法載入主控台頁面。反之，可能會看到錯誤訊息 BXNUI0001E 或 BXNUI0016E。

您可能會看到下列其中一則錯誤訊息：
{: tsSymptoms}

`BXNUI0001E: The page wasn't loaded because {{site.data.keyword.Bluemix_notm}} didn't detect whether a session exists.`

`BXNUI0016E: The apps and services weren't retrieved because an {{site.data.keyword.Bluemix_notm}} page didn't load.`

請視需要完成下列一個以上的動作：
{: tsResolve}

  * 重新整理或重新啟動瀏覽器。
  * 登出 {{site.data.keyword.Bluemix_notm}} 然後再重新登入。
  * 使用瀏覽器的專用瀏覽模式。
  * 清除瀏覽器的 Cookie 及快取。
  * 使用不同的瀏覽器。如需 {{site.data.keyword.Bluemix_notm}} 所支援瀏覽器版本的相關資訊，請參閱 [{{site.data.keyword.Bluemix_notm}} 必要條件](/docs/overview/prereqs.html#prereqs)。
  * 如果您已安裝 Cloud Foundry 指令行介面，請輸入 `ibmcloud cf apps` 指令，以查看您的應用程式是否在執行中。
