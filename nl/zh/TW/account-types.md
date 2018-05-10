---

copyright:

  years: 2015, 2018
lastupdated: "2017-11-29"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 帳戶類型
{: #accounts}

您可以在 {{site.data.keyword.Bluemix}} 上免費開始建置。當您準備好要擴大時，只需要對超出免費額度的部分進行升級及付費。我們有四種不同的帳戶類型可供選擇：「精簡」、「隨收隨付制」、「訂閱」及「促銷」。您可以使用任何帳戶類型在 {{site.data.keyword.Bluemix_notm}} 中開始使用 - 只需要選擇最符合您需求的帳戶類型。
{:shortdesc}

## 帳戶比較
{: #compare}

下表提供「精簡」、「隨收隨付制」及「訂閱」帳戶的比較。如需有關每一個帳戶的詳細資料，請參閱下列各節。

|  | 精簡| 隨收隨付制| 訂閱| 
|--------------------|--------------------|--------------------|--------------------|
| **存取免費 Cloud Foundry 記憶體** | 256 MB | 512 MB | 512 MB | 
| **存取[精簡服務方案 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window}** | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
| **存取所有免費方案**|  | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
| **存取完整型錄**|  | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
| **沒有時間限制**| ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
| **保證零成本**| ![可用特性](../icons/icon_enabled.svg) |  |  |
| **協議的定價**|  |  | ![可用特性](../icons/icon_enabled.svg) | 
| **最適合學習或建置 POC**| ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |  | 
| **適合正式作業使用案例**|  | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) | 
{: caption="表 1. {{site.data.keyword.Bluemix_notm}} 帳戶的比較" caption-side="top"}

## 精簡帳戶
{: #liteaccount}

請註冊免費「精簡」帳戶，以在 {{site.data.keyword.Bluemix_notm}} 主控台中選取名為「精簡」並使用「精簡」標籤 ![「精簡」標籤](../icons/Lite.svg) 所顯示的免費方案，來建置應用程式以及探索服務。「精簡」帳戶不會到期，因此不需要信用卡。 

您可以存取為您所建立並命名為 `Default` 的單一資源群組。{{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) 所管理的所有服務實例都會自動新增至此資源群組。您隨時可以更新此資源群組的名稱。如需詳細步驟，請參閱[重新命名資源群組](/docs/admin/resourcegroups.html#renaming-a-resource-group)。 

每一個資源群組都是免費的。當您在 IAM 所管理的服務與 Cloud Foundry 應用程式之間建立連線時，請建立計入您配額的別名（即服務實例）。請參閱[何謂別名？](/docs/manageapps/connecting_apps.html#what_is_alias)。
{: tip}

### 可用功能

您可能會好奇「精簡」帳戶所提供的功能。請參閱下列重要特性清單：

   * 帳戶免費 - 不需要信用卡。
   * 帳戶永不到期。
   * 一個 {{site.data.keyword.Bluemix_notm}} 地區可以使用一個組織。
   * 免費 {{site.data.keyword.Bluemix_notm}} 支援。
   * 您會收到帳戶狀態及配額限制的電子郵件通知。
   * Cloud Foundry 應用程式可以同時存取最多 256 MB 的免費運行環境記憶體。 
   * 您可以使用具有 2 個 CPU 及 4 GB RAM 的 Kubernetes 叢集。
   * 您可以佈建 [{{site.data.keyword.Bluemix_notm}} 型錄 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window} 中有「精簡」方案之任何服務的一個實例。
   * 在 10 天沒有開發活動之後，您的應用程式就會進入休眠。您可以開始處理新的應用程式，而不需要擔心達到記憶體配額限制。
   * 在 30 天沒有開發活動之後，就會刪除具有精簡方案的服務實例。如此一來，在建立新的實例之前，您不需要管理刪除非作用中實例。

## 計費帳戶
{: #billableacts}

註冊 {{site.data.keyword.Bluemix_notm}} 計費方案或要求升級帳戶時，可以選取四個不同的 {{site.data.keyword.Bluemix_notm}} 帳戶。下表列出不同的帳戶類型及其付費方法。

|帳戶類型|	收費方式？|
|------------------|-----------------------|
|隨收隨付制|	費用是根據 {{site.data.keyword.Bluemix_notm}} 運算及服務的使用|
|訂閱| 您可以根據最低的每月消費承諾來取得每月折扣|
| {{site.data.keyword.Bluemix_dedicated_notm}} | 年度合約|
|{{site.data.keyword.Bluemix_local_notm}} |	年度合約|
{:caption="表 2. {{site.data.keyword.Bluemix_notm}} 計費帳戶及費用" caption-side="top"}

如果您鏈結 {{site.data.keyword.Bluemix_notm}} 計費帳戶與 SoftLayer 帳戶，從下個月 1 日開始，結合的費用即會併入 {{site.data.keyword.Bluemix_notm}} 發票。如需相關資訊，請參閱[檢視額度](/docs/pricing/viewing_usage.html#credits)。
{: tip}

### 隨收隨付制帳戶

使用「隨收隨付制」帳戶，您可以建立多個資源群組來輕鬆管理配額，以及檢視一組資源的計費使用情形。

您有資格使用免費運行環境及服務額度。如果您的用量超過免費額度，則會收到 {{site.data.keyword.Bluemix_notm}} 的月份發票。發票的計價單位為美元 (USD)，並且會詳細列出資源費用。 

在許多國家及地區中，您可以從 {{site.data.keyword.Bluemix_notm}} 主控台註冊「隨收隨付制」帳戶。提供計費及信用卡資訊、接受條款，並提交帳戶要求之後，然後會驗證您的信用卡。此外也會傳送帳戶資訊的確認電子郵件。等收到確認電子郵件過後幾分鐘，您就可以回到主控台繼續建置應用程式。

如果無法處理您所在國家或地區的線上申請，請使用 [{{site.data.keyword.Bluemix_notm}} 支援中心 ![外部鏈結圖示](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} 頁面上列出的鏈結，來聯絡 {{site.data.keyword.Bluemix_notm}} 銷售人員。

您隨時都可以將「隨收隨付制」帳戶轉換為「訂閱」帳戶。使用 [{{site.data.keyword.Bluemix_notm}} 支援中心 ![外部鏈結圖示](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} 頁面上列出的鏈結，來聯絡 {{site.data.keyword.Bluemix_notm}} 銷售人員。

### 訂閱帳戶

使用「訂閱」帳戶，您可以建立多個資源群組來輕鬆管理配額，以及檢視一組資源的計費使用情形。

您承諾每個月的最低消費金額，並獲得套用至該最低收費的訂閱折扣。您也會針對任何超出最低消費金額的用量付款。


若要註冊「訂閱」帳戶，以及取得訂閱費率及折扣的相關資訊，您必須使用 [{{site.data.keyword.Bluemix_notm}} 支援中心 ![外部鏈結圖示](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} 頁面上列出的鏈結，來聯絡 {{site.data.keyword.Bluemix_notm}} 銷售人員。

### {{site.data.keyword.Bluemix_dedicated_notm}} 帳戶

使用 {{site.data.keyword.Bluemix_dedicated_notm}}，您必須註冊至少一年期限，包括：

   * 回到您基礎架構的 VPN 連線功能
   * {{site.data.keyword.BluSoftLayer_notm}} 資料中心內的完整備用環境
   * 所有支援的運行環境（IBM Java Liberty、Node.js 及內建開放程式碼運行環境）
   * 您選取的所有專用服務及所有公用 {{site.data.keyword.Bluemix_notm}} 服務
   * 標準 {{site.data.keyword.Bluemix_notm}} 支援

您也可以訂購選購項目（例如 SoftLayer DirectLink 或超值支援選項）。如需相關資訊，請與 [{{site.data.keyword.Bluemix_notm}} 銷售人員 ![外部鏈結圖示](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} 聯絡。

您在該期間每個月所支付的金額是根據您想要的專用服務，加上讓您存取所有公用服務的「訂閱」帳戶。「{{site.data.keyword.Bluemix_notm}} 公用」中的服務使用費用是根據您的「訂閱」帳戶合約來計算。您會收到關於任何超出訂閱合約之使用服務的發票。請與 IBM 指定的客戶業務代表聯絡，或與 [{{site.data.keyword.Bluemix_notm}} 銷售人員 ![外部鏈結圖示](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} 聯絡，以開始您的合約。

### {{site.data.keyword.Bluemix_local_notm}} 帳戶

使用 {{site.data.keyword.Bluemix_local_notm}}，您必須註冊至少一年期限，包括：

   * 稱為轉遞的交付功能，讓 IBM 能連接您的本端部署，並自動且一致地交付更新
   * 所有支援的運行環境（IBM Java Liberty、Node.js 及內建開放程式碼運行環境）
   * 您選取的所有本端服務，及所有公用 {{site.data.keyword.Bluemix_notm}} 服務的存取
   * 標準 {{site.data.keyword.Bluemix_notm}} 支援

您在該期間每個月所支付的金額是根據您想要的本端服務，加上讓您存取所有公用服務的「訂閱」帳戶。「{{site.data.keyword.Bluemix_notm}} 公用」中的服務使用費用是根據您的「訂閱」帳戶合約來計算。您會收到關於任何超出訂閱合約之使用服務的發票。請與 IBM 指定的客戶業務代表聯絡，或與 [{{site.data.keyword.Bluemix_notm}} 銷售人員 ![外部鏈結圖示](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} 聯絡，以開始您的合約。

## 促銷帳戶
{: #promo}

促銷帳戶（偶而提供為特殊促銷的一部分）是無時間限制的試用，具有大部分 {{site.data.keyword.Bluemix_notm}} 型錄的存取權。此帳戶類型只能透過使用促銷代碼取得。帳戶有效性的時段會依促銷而不同。 
   
使用促銷帳戶，您可以存取為您所建立並命名為 `Default` 的單一資源群組。所有 IAM 受管理服務實例都會自動新增至此資源群組。您隨時可以更新此資源群組的名稱。如需詳細步驟，請參閱[重新命名資源群組](/docs/admin/resource-groups.html#renaming-a-resource-group)。 

每一個資源群組都是免費的。當您在 IAM 所管理的服務與 Cloud Foundry 應用程式之間建立連線時，請建立計入您配額的別名（即服務實例）。請參閱[何謂別名？](/docs/manageapps/connecting_apps.html#what_is_alias)。
{: tip}

### 我的促銷帳戶到期後會發生什麼情況？
{: #trialend}

促銷帳戶到期後，即會停止您帳戶中的應用程式。您無法註冊另一個 {{site.data.keyword.Bluemix_notm}} 帳戶，但您還是可以存取您的帳戶，以及您受邀使用的任何帳戶。

若要重新啟動應用程式，請將您的帳戶轉換成計費帳戶，方法是針對「隨收隨付制」帳戶提供信用卡資訊，或建立「訂閱」帳戶。然後，您就可以繼續使用免費的運算及服務額度。您只需要針對未包含在每月免費額度中的服務、容器及運行環境的用量進行付款。

如果您未在促銷帳戶到期之後轉換帳戶，則會在 30 天之後移除您的應用程式及服務。不過，不會刪除您的帳戶，而且您隨時都可以登入及升級至計費帳戶。此外，您會收到電子郵件通知，提醒您建立計費帳戶並避免遺失應用程式設定及服務配置。如果您不想要收到來自 {{site.data.keyword.Bluemix_notm}} 的通知，則可以隨時取消訂閱。

如果您轉換帳戶，則會將免費額度限制為一般由每一個服務所提供的額度。額度不再是許多 IBM 服務在免費試用期間所提供的無限制使用額度。
