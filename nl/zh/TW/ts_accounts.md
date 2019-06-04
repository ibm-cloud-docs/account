---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-29"

keywords: troubleshoot account, account problem, account support, account help, org error, resource error, error message

subcollection: account
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

# 管理帳戶的疑難排解
{: #managingaccounts}

管理帳戶的一般問題，可能包括不同應用程式具有相同的網域名稱，或是管理者無法檢視所有組織。在許多情況下，您可以遵照一些簡單的步驟，從這些問題回復。
{:shortdesc}


## 為什麼我無法存取不同的 {{site.data.keyword.Bluemix_notm}} 位置？
{: #nosecondreg}
{: troubleshoot}

您無法建立新的位置，因為您的帳戶類型不容許。

當您嘗試建立新的 {{site.data.keyword.Bluemix_notm}} 位置時，收到錯誤訊息。
{: tsSymptoms}

這可能是因為您使用「精簡」帳戶，此帳戶僅支援在一個公用位置中進行開發。
如需「精簡」帳戶特性的相關資訊，請參閱[精簡帳戶](/docs/account?topic=account-accounts#liteaccount)。
{: tsCauses}

若要存取更多位置，請升級至計費帳戶。移至**管理 > 帳戶**，然後選取**帳戶設定**。在「帳戶升級」區段中，選取您的升級選項。
{: tsResolve}


## 為什麼我無法建立新的組織？
{: #nosecondorg}
{: troubleshoot}

您嘗試建立多個組織，而您具有「精簡」帳戶。  

當您嘗試建立新的組織時，收到錯誤訊息。
{: tsSymptoms}

您可能會看到此錯誤，因為您使用的是「精簡」帳戶，此帳戶僅支援在一個組織中進行開發。如需「精簡」帳戶特性的相關資訊，請參閱[精簡帳戶](/docs/account?topic=account-accounts#liteaccount)。
{: tsCauses}

若要建立新的組織，請升級至計費帳戶。移至**管理 > 計費及用量**，然後選取**付款**。
{: tsResolve}


## 為什麼我無法建立新的精簡方案實例？
{: #nosecondlite}
{: troubleshoot}

您嘗試建立額外的實例，但您具有「精簡」帳戶。

當您嘗試建立新的「精簡」方案實例時，收到下列錯誤訊息：
{: tsSymptoms}

`無法佈建新的「精簡」實例`

每個「精簡」方案實例限制為只能有一個實例，以確保這些方案保持免費。
如需「精簡」帳戶特性的相關資訊，請參閱[精簡帳戶](/docs/account?topic=account-accounts#liteaccount)。
{: tsCauses}

您可以選取其中一個計費服務方案（可在計費帳戶中取得）來建立其他服務實例。若要從主控台升級至計費帳戶，請移至**管理 > 帳戶**，然後選取**帳戶設定**。
{: tsResolve}

如果您不想要從「精簡」帳戶升級，而且不再使用現有「精簡」服務實例，則可以從儀表板刪除現有「精簡」方案實例，然後建立新的實例。


## 我怎麼超出了運行環境記憶體額度？
{: #noruntimemem}
{: troubleshoot}

您已經超過帳戶容許的記憶體。

您無法部署應用程式，並有錯誤指出您已超出組織的記憶體限制。
{: tsSymptoms}

在「精簡」帳戶中，Cloud Foundry 應用程式可以同時使用最多 256 MB 的運行環境記憶體。在計費帳戶中，有一項 2 GB 的記憶體限制。
{: tsCauses}

如果您使用的是「精簡」帳戶，則可以升級至計費帳戶來取得更多記憶體。移至**管理 > 帳戶**，然後選取**帳戶設定**。如需「精簡」帳戶特性的相關資訊，請參閱[精簡帳戶](/docs/account?topic=account-accounts#liteaccount)。
{: tsResolve}

如果您不想要從「精簡」帳戶升級，但有一些閒置應用程式，則可以刪除這些閒置應用程式來釋放一些運行環境記憶體。


## 為什麼我的帳戶為非作用中？
{: #ts_accnt_inactive}
{: troubleshoot}

如果帳戶處於非作用中，則無法在 {{site.data.keyword.Bluemix_notm}} 中建立應用程式。您必須與支援團隊聯絡以修正此問題。

嘗試在 {{site.data.keyword.Bluemix_notm}} 中建立應用程式時，會顯示下列錯誤訊息：
{: tsSymptoms}

`BXNUI0096E: 未建立應用程式。您的帳戶處於非作用中狀態，因為它已取消或已暫停。`

當帳戶被取消或暫停時，{{site.data.keyword.Bluemix_notm}} 帳戶的狀態會變成非作用中。
{: tsCauses}

若要重新啟動您的帳戶，請在[支援中心](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示") 中開立案例。在您的案例中，包含下列資訊：
{: tsResolve}

  * 您用來登入 {{site.data.keyword.Bluemix_notm}} 的 IBM ID。
  * 您的應用程式建立所在的組織名稱。此資訊可協助支援團隊判斷您在組織中獲指派的角色或成員資格是否正確。


## 為什麼我無法將使用者新增至組織？
{: #ts_adduser}
{: troubleshoot}

只有在您是帳戶擁有者，或同時為組織的管理員與成員時，才能邀請使用者加入您的組織。

您無法在**管理組織**區段中看到**邀請新使用者**鏈結。
{: tsSymptoms}

只有下列 {{site.data.keyword.Bluemix_notm}} 使用者可以邀請使用者加入組織：
{: tsCauses}
  * 組織的帳戶擁有者
  * 同時為組織成員（非合作人員）的組織管理員

在 {{site.data.keyword.Bluemix_notm}} 中，您可以是組織的成員或合作人員：

<dl><dt>合作人員</dt>
<dd>如果您已有 {{site.data.keyword.Bluemix_notm}} 帳戶，而某人邀請您加入組織，則您是組織的合作人員。</dd>
<dt>成員</dt>
<dd>如果您沒有 {{site.data.keyword.Bluemix_notm}} 帳戶，但某人邀請您加入組織，且您透過該邀請註冊 {{site.data.keyword.Bluemix_notm}}，則您是組織的成員。</dd>
</dl>

如果您是組織的合作人員，即使您已獲指派為組織管理員，也無法邀請使用者加入您的組織。

所有組織管理員（包括組織的合作人員）都可以新增、修改及移除已經在組織中的使用者。
{: note}

如果您無法邀請使用者加入您的組織，而需要不同的角色來完成這項動作，請與組織管理員聯絡，以變更您的角色。若要識別您的組織管理員，請完成下列步驟：
{: tsResolve}

  1. 從主控台功能表列，按一下**管理 > 帳戶**，然後選取**公司聯絡人**。
  2. 移至您的組織，然後檢視**使用者**標籤上的組織管理員資訊。  

如果您因為自己是合作人員而非成員，以致於無法邀請使用者，則必須刪除您先前的 {{site.data.keyword.Bluemix_notm}} 帳戶，然後受邀以組織成員身分加入帳戶。若要刪除先前的帳戶並以成員的身分加入帳戶，請完成下列步驟：

  1. 與 [{{site.data.keyword.Bluemix_notm}} 支援中心 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} 聯絡以開立支援案例，並要求刪除您的帳戶。如果您的資料與要儲存並移至新帳戶的舊帳戶相關聯，請在電子郵件中包含此資訊。
  2. 刪除您的帳戶之後，請讓具有組織管理員角色的使用者，邀請您以組織管理員的身分加入組織。然後，透過該邀請註冊 {{site.data.keyword.Bluemix_notm}}。


## 為什麼沒有任何空間與我的現行組織相關聯？
{: #ts_no_space}
{: troubleshoot}

如果沒有空間與您的現行組織相關聯，則您無法建立應用程式。

當您嘗試建立應用程式時，會顯示下列錯誤訊息：
{: tsSymptoms}

`BXNUI0097E: 必須至少有一個空間與您的組織和地區相關聯，您才能新增應用程式。在「儀表板」上，按一下「建立空間」。建立空間後，請重試。`

應用程式必須在組織下的空間中建立。
{: tsCauses}

若要建立空間，請使用下列其中一種方法：
{: tsResolve}

  * 從主控台功能表列中，按一下**管理 > 帳戶**。展開**帳戶資源**，並按一下 **Cloud Foundry 組織**。然後，選取您要在其中建立空間的組織，並且按一下**新增空間**。
  * 在 {{site.data.keyword.Bluemix_notm}} 指令行介面中，鍵入 `ibmcloud account space-create <space_name> -o<organization_name>`。


## 為什麼部分應用程式會共用網域名稱？
{: #ts_domain_diff}
{: troubleshoot}

您可能注意到 {{site.data.keyword.Bluemix_notm}} 中有數個應用程式共用 URL。

當您將相同的 URL 路徑指派給空間中的不同應用程式時，可能就會發生此問題。
{: tsCauses}

例如，您將 myApp1 應用程式推送至 {{site.data.keyword.Bluemix_notm}}，並將網域設為 `mynewapp.us-east.cf.appdomain.cloud`。然後，將另一個 myApp2 應用程式推送至相同的空間，並將其中一個 URL 路徑設為 `mynewapp.us-east.cf.appdomain.cloud`。路徑現在同時對映至這兩個應用程式。

這是受支援的行為，而且您可以使用此作法，讓應用程式升級達到運作零中斷。如需相關資訊，請參閱[如何確保運作零中斷](/docs/overview?topic=overview-zero-downtime)。
{: tsResolve}


## 為什麼管理者無法使用主控台來檢視所有組織？
{: #ts_ui_org}
{: troubleshoot}

身為管理者，當您使用 {{site.data.keyword.Bluemix_notm}} 主控台時，無法顯示每個組織來進行管理。您只能顯示及管理您所屬的那些組織。

身為管理者，您無法從主控台檢視所有組織。
{: tsSymptoms}

此行為是主控台的限制。
{: tsCauses}

您可以從 {{site.data.keyword.Bluemix_notm}} 指令行介面使用 `ibmcloud account orgs` 及 `ibmcloud account org-create` 之類的指令來管理所有組織。如需完整的指令清單，請輸入 `ibmcloud account help`。
{: tsResolve}


## 為什麼我無法提交表單來新增信用卡資訊？
{: #ts_addcc}
{: troubleshoot}

您無法提交信用卡資訊，以將「精簡」帳戶升級至計費帳戶。

「新增信用卡」頁面上的**提交**按鈕已停用。
{: tsSymptoms}

若未正確在「新增信用卡」頁面上填寫您的資訊，即會發生此問題。
{: tsCauses}

請完成下列步驟：
{: tsResolve}

  1. 在「新增信用卡」頁面上，完成所有必要欄位。
  2. 選取**我已閱讀並同意 IBM 條款**，然後按一下**提交**。

## 無法透過主控台使用選項時，該如何新增信用卡？
{: #ts_ccibm}
{: troubleshoot}

您想要輸入信用卡來支付 {{site.data.keyword.Bluemix_notm}} 服務的費用，但該選項並未出現。

當您嘗試輸入信用卡資訊時，您會看到下列錯誤：
{: tsSymptoms}

`您的付款透過 IBM.com 進行管理。若要檢視付款並維護帳單，您可以造訪 IBM.com 入口網站，該入口網站中包含了您 IBM ID 帳戶的所有內容。`

您可以按一下**瀏覽**來存取 ibm.com 網站，但您並未看到輸入信用卡資訊的位置。

我們會透過 {{site.data.keyword.Bluemix_notm}} 主控台安全地處理信用卡交易。不過，在某些國家/地區中，我們必須採取其他步驟來確保信用卡資料的完整性。這些信用卡要求都是透過 ibm.com 網站來完成。這兩種方法可確保安全地處理您的信用卡資訊。   
{: tsCauses}

若要提供付款的信用卡資訊，請完成下列步驟：
{: tsResolve}

  1. 移至 [ibm.com ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](http://www.ibm.com){: new_window}，並使用您用來登入 {{site.data.keyword.Bluemix_notm}} 的相同 IBM ID 及密碼來進行登入。
  1. 按一下「虛擬人像」圖示 ![「虛擬人像」圖示](../icons/i-avatar-icon.svg)，然後選取**計費**。
  1. 按一下**管理付款方法**。
  1. 輸入您的信用卡資訊，然後按一下**登錄**。

將會驗證這項資訊，並將其新增至 {{site.data.keyword.Bluemix_notm}} 帳戶作為任何費用的付款方法。
