---

copyright:

  years: 2015, 2018
lastupdated: "2018-08-14"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 帳戶類型
{: #accounts}

您可以選擇三種 {{site.data.keyword.Bluemix}} 帳戶類型：「精簡」、「隨收隨付制」及「訂閱」。您可以使用任何帳戶類型在 {{site.data.keyword.Bluemix_notm}} 中開始使用 - 請選擇最符合您需求的帳戶類型。
{:shortdesc}

## 比較帳戶
{: #compare}

下表提供「精簡」、「隨收隨付制」及「訂閱」帳戶的比較。如需有關每一個帳戶的詳細資料，請參閱下列各節。

|  |精簡|隨收隨付制|訂閱|
|--------------------|--------------------|--------------------|--------------------|
|**存取免費 Cloud Foundry 記憶體** |256 MB |512 MB |512 MB |
|**存取[精簡服務方案 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/catalog/?search=label:lite){: new_window}** | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
|**存取所有免費方案**|  | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
|**存取完整 {{site.data.keyword.Bluemix_notm}} 型錄**|  | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
|**存取多個 Cloud Foundry 地區** |  | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
|**沒有時間限制**| ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
|**保證零成本**| ![可用特性](../icons/icon_enabled.svg) |  |  |
|**定價折扣** |  |  | ![可用特性](../icons/icon_enabled.svg) |
|**最適合學習或建置概念證明**| ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |  |
|**適合正式作業使用案例**|  | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
{: caption="表 1. {{site.data.keyword.Bluemix_notm}} 帳戶的比較" caption-side="top"}

## 精簡帳戶
{: #liteaccount}

請註冊「精簡」帳戶，以使用精選的免費「精簡」方案開始建置應用程式與探索服務，這些服務在 {{site.data.keyword.Bluemix_notm}} 主控台中顯示時會有「精簡」標籤 ![「精簡」標籤](../icons/Lite.svg)。「精簡」帳戶不會到期，因此不需要信用卡。

您可以存取為您所建立並命名為 `Default` 的單一資源群組。{{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) 所管理的所有服務實例都會自動新增至此資源群組。您隨時可以更新此資源群組的名稱。如需詳細步驟，請參閱[重新命名資源群組](/docs/resources/resourcegroups.html#renaming-a-resource-group)。

每一個資源群組都是免費的。當您在 IAM 所管理的服務與 Cloud Foundry 應用程式之間建立連線時，請建立計入您配額的別名（即服務實例）。請參閱[何謂別名？](/docs/resources/connecting_apps.html#what_is_alias)。
{: tip}

### 可用功能

請參閱下列清單，其會列出「精簡」帳戶提供的重要特性：

   * 帳戶免費 - 不需要信用卡。
   * 帳戶永不到期。
   * 一個 {{site.data.keyword.Bluemix_notm}} 地區可以使用一個組織。
   * 基本 {{site.data.keyword.Bluemix_notm}} 支援是免費的。針對未使用傳統嚴重性且未規定特定回應時間的非正式作業環境或工作負載，提供了基本支援。
   * 您會收到帳戶狀態及配額限制的電子郵件通知。
   * Cloud Foundry 應用程式可以同時存取最多 256 MB 的免費運行環境記憶體。
   * 您可以佈建 [{{site.data.keyword.Bluemix_notm}} 型錄 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window} 中有「精簡」方案之任何服務的一個實例。
   * 在 10 天沒有開發活動之後，您的應用程式就會進入休眠。您可以開始處理新的應用程式，而不需要擔心達到記憶體配額限制。
   * 在 30 天沒有開發活動之後，就會刪除具有精簡方案的服務實例。如此一來，在建立新的實例之前，您不需要管理刪除非作用中實例。

### 升級帳戶
{: #upgrade-to-paygo}

當您準備好要擴大時，可將「精簡」帳戶升級至「隨收隨付制」或「訂閱」帳戶。 

  * 若要升級為「隨收隨付制」帳戶，請移至主控台中的**管理** > **計費及用量** > **計費**，然後按一下**新增信用卡**。

  * 若要升級至「訂閱」帳戶，請移至主控台中的**管理** > **計費及用量** > **計費**，然後按一下**進一步瞭解**。

## 隨收隨付制帳戶
{: #paygo}

使用「隨收隨付制」帳戶，您可以建立多個資源群組來輕鬆管理配額，以及檢視一組資源的計費使用情形。您的費用是根據 {{site.data.keyword.Bluemix_notm}} 運算及服務的使用。您有資格使用免費運行環境及服務額度。如果您的用量超過免費額度，則會收到 {{site.data.keyword.Bluemix_notm}} 的月份發票。發票的計價單位為美元 (USD)，並且會提供資源費用的詳細資料。

如果您鏈結「隨收隨付制」帳戶與 SoftLayer 帳戶，從下個月 1 日開始，結合的費用即會含在 {{site.data.keyword.Bluemix_notm}} 發票中。
{: tip}

您可以從 {{site.data.keyword.Bluemix_notm}} 主控台升級至「隨收隨付制」帳戶。提供計費及信用卡資訊、接受條款，並提交帳戶要求之後，便會驗證您的信用卡。您也會收到有關帳戶資訊的確認電子郵件。等收到確認電子郵件過後幾分鐘，您就可以回到主控台繼續建置應用程式。如果無法處理您所在國家或地區的線上申請，請與 [{{site.data.keyword.Bluemix_notm}} 支援中心](/docs/get-support/howtogetsupport.html)聯絡。

在您升級至「隨收隨付制」帳戶之後，您會得到促銷扣抵 200 美元，不需要任何動作即可開始使用它。您的 $200 額度有效期限為 30 天，且會自動套用至您的發票。此額度無法用於協力廠商供應項目。

### 升級帳戶
{: #upgrade-to-subscription}

您隨時都可以將「隨收隨付制」帳戶升級為「訂閱」帳戶。如需其他詳細資料，請與 [{{site.data.keyword.Bluemix_notm}} 銷售人員 ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg) 聯絡。


## 訂閱帳戶

使用「訂閱」帳戶，您可以建立多個資源群組來輕鬆管理配額，以及檢視一組資源的計費使用情形。您承諾每個月的最低消費金額，並獲得套用至該最低收費的訂閱折扣。您也會針對任何超出最低消費金額的用量付款。


如果您鏈結「訂閱」帳戶與 SoftLayer 帳戶，從下個月 1 日開始，結合的費用即會含在 {{site.data.keyword.Bluemix_notm}} 發票中。
{: tip}

### {{site.data.keyword.Bluemix_dedicated_notm}} 帳戶

使用 {{site.data.keyword.Bluemix_dedicated_notm}}，您必須註冊至少一年期限，包括：

   * 回到您基礎架構的 VPN 連線功能
   * {{site.data.keyword.BluSoftlayer_notm}} 資料中心內的完整備用環境
   * 所有支援的運行環境（IBM Java Liberty、Node.js 及內建開放程式碼運行環境）
   * 您選取的所有專用服務及所有公用 {{site.data.keyword.Bluemix_notm}} 服務
   * 標準 {{site.data.keyword.Bluemix_notm}} 支援

您也可以訂購選購項目（例如 SoftLayer DirectLink 或超值支援選項）。如需相關資訊，請與 [{{site.data.keyword.Bluemix_notm}} 銷售人員 ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg) 聯絡。

您在該期間每個月所支付的金額是根據您想要的專用服務，加上讓您存取所有公用服務的「訂閱」帳戶。{{site.data.keyword.Bluemix_notm}} Public 中的服務使用費用是根據您的「訂閱」帳戶合約來計算。您會收到關於任何超出訂閱合約之使用服務的發票。請與 IBM 指定的客戶業務代表聯絡，或與 [{{site.data.keyword.Bluemix_notm}} 銷售人員](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg) 聯絡，以開始您的合約。

### {{site.data.keyword.Bluemix_local_notm}} 帳戶

使用 {{site.data.keyword.Bluemix_local_notm}}，您必須註冊至少一年期限，包括：

   * 稱為轉遞的交付功能，讓 IBM 能連接您的本端部署，並自動且一致地交付更新
   * 所有支援的運行環境（IBM Java Liberty、Node.js 及內建開放程式碼運行環境）
   * 您選取的所有本端服務，及所有公用 {{site.data.keyword.Bluemix_notm}} 服務的存取
   * 標準 {{site.data.keyword.Bluemix_notm}} 支援

您在該期間每個月所支付的金額是根據您想要的本端服務，加上讓您存取所有公用服務的「訂閱」帳戶。{{site.data.keyword.Bluemix_notm}} Public 中的服務使用費用是根據您的「訂閱」帳戶合約來計算。您會收到關於任何超出訂閱合約之使用服務的發票。請與 IBM 指定的客戶業務代表聯絡，或與 [{{site.data.keyword.Bluemix_notm}} 銷售人員](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg) 聯絡，以開始您的合約。



