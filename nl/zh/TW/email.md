---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-28"

keywords: notifications, email notifications, IBM Cloud notifications, notification preferences

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# 設定電子郵件喜好設定
{: #email-prefs}

視 {{site.data.keyword.Bluemix}} 帳戶類型而定，您可以選擇是否要收到有關 {{site.data.keyword.Bluemix}} 平台非計劃性事件及計劃性事件的電子郵件通知，或是收到有關非計劃性事件、維護及公告的基礎架構電子郵件通知。您也可以選擇設定標準基礎架構事件的通知訂閱。
{: shortdesc}

## 設定平台通知
{: #setting-platform-notifications}

如果您是「精簡」帳戶擁有者，可以選擇是否要收到有關 {{site.data.keyword.Bluemix}} 平台非計劃性事件（例如運作中斷）及計劃性事件（例如維護）的電子郵件通知。設定 {{site.data.keyword.Bluemix_notm}} 平台通知時，您會收到僅與 {{site.data.keyword.Bluemix_notm}} 平台相關聯的電子郵件通知。您不會收到與 {{site.data.keyword.Bluemix_notm}} 服務相關聯之事件的電子郵件通知。

您只能為您的設定檔（而不是帳戶）設定平台電子郵件通知。換言之，如果您切換至另一個帳戶，您所做的任何平台通知更新，範圍都侷限於您的設定檔，而不是您切換至的帳戶。

當您選取接收非計劃性平台事件時，只會收到可能導致運作中斷（嚴重性 1）之問題的相關電子郵件。您隨時都可以從[狀態 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/status){: new_window} 頁面中，查看所有計劃性事件和非計劃性事件。

1. 移至「虛擬人像」圖示 ![「虛擬人像」圖示](../icons/i-avatar-icon.svg) > **設定檔和設定**。
2. 按一下**通知**。
3. 選取是否要收到您想要更新之每個種類的平台通知。

  依預設，會關閉所有 {{site.data.keyword.Bluemix_notm}} 平台通知。
  {: tip}

4. 按一下**儲存**。

## 設定基礎架構通知

如果您是「隨收隨付制」或「訂閱」帳戶擁有者，可以選擇是否要收到有關非計劃性事件、維護及公告的 {{site.data.keyword.Bluemix_notm}} 基礎架構電子郵件通知。基礎架構通知的範圍侷限於您所切換至的帳戶。您可以切換至另一個帳戶，並管理該帳戶的通知。

1. 移至「虛擬人像」圖示 ![「虛擬人像」圖示](../icons/i-avatar-icon.svg) > **設定檔和設定**。
2. 按一下**通知**。
3. 選取是否要收到您想要更新之每個種類的基礎架構通知。

  依預設，會開啟所有 {{site.data.keyword.Bluemix_notm}} 基礎架構通知。
  {: tip}

4. 按一下**儲存**。

## 設定使用者通知
{: #setting-user-notifications}

設定使用者通知僅適用於標準基礎架構資源。如果您是帳戶擁有者，則可以為您帳戶中的使用者設定通知訂閱。這些訂閱適用於一組特定的開發人員服務，例如 {{site.data.keyword.autoscaling}} 及 Raid Alert Monitoring。當使用者訂閱服務時，他們會收到該服務的相關電子郵件。  

您帳戶中的使用者會收到下列重要作業事件類型的通知：

  * 非計劃性的基礎架構問題或運作中斷：根據特定客戶的特定條件，可能導致運作中斷的問題。
  * 計劃性的服務或排定的維護：讓基礎架構以最佳狀態運作所需的維護。
  * 安全漏洞：會隔離受影響的區域。建立修補程式來關閉漏洞，並對修補程式執行測試，以確保不會影響任何附屬功能。
  * 已開立的支援案例：警示使用者其帳戶上已開立的案例。

通知時機會視事件為非計劃性、計劃性還是已排定而有所不同。{{site.data.keyword.BluSoftlayer_notm}} 基礎架構原則是盡快補救問題，針對可能產生更大影響的進一步問題，能消除其風險或使其風險降到最低。有時，即使是執行計劃性維護，也只提前很短的時間進行通知。

若要為使用者設定訂閱通知，請完成下列步驟：

  1. 移至**管理 > 帳戶**，然後選取**通知**。
  2. 從表格中選取一項服務。
  3. 在「已訂閱」直欄中，為想要收到通知的使用者選取**是**。

    為了能夠輕鬆找到您所尋找的使用者，請按一下**過濾**，依據名字、姓氏或使用者名稱進行過濾。
    {: tip}
