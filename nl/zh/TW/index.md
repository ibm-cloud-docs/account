---

copyright:
  years: 2015, 2019
lastupdated: "2019-03-19"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account, subscription, service bundle

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 帳戶類型
{: #accounts}

{{site.data.keyword.Bluemix_notm}} 有三種不同的帳戶類型：「精簡」、「隨收隨付制」及「訂閱」。只要進行註冊，您就會取得一個免費的「精簡」帳戶。「隨收隨付制」和「訂閱」是計費帳戶選項，每個選項都提供不同的特性。請比較每個帳戶，並選擇最符合您需求的帳戶。
{:shortdesc}

## 比較帳戶
{: #compare}

下表提供「精簡」、「隨收隨付制」及「訂閱」帳戶的比較。如需有關每一個帳戶的詳細資料，請參閱下列各節。

|                                         |精簡|隨收隨付制|訂閱|
|-----------------------------------------|--------------------|--------------------|--------------------|
|**存取免費 Cloud Foundry 記憶體** |256 MB |512 MB |512 MB |
|**存取[精簡服務方案 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://{DomainName}/catalog/?search=label:lite){: new_window}** | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
|**存取所有免費方案**|                    | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
|**存取完整 {{site.data.keyword.Bluemix_notm}} 型錄**|  | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
|**存取多個 Cloud Foundry 地區** |               | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
|**沒有時間限制**| ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
|**保證零成本**| ![可用特性](../icons/icon_enabled.svg) |  |         |
|**定價折扣** |                    |                    | ![可用特性](../icons/icon_enabled.svg) |
|**最適合學習或建置概念證明**| ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |  |
|**適合正式作業使用案例**|                    | ![可用特性](../icons/icon_enabled.svg) | ![可用特性](../icons/icon_enabled.svg) |
{: caption="表 1. {{site.data.keyword.Bluemix_notm}} 帳戶的比較" caption-side="top"}


## 精簡帳戶
{: #liteaccount}

請註冊「精簡」帳戶，以使用精選的免費「精簡」方案開始建置應用程式與探索服務，這些服務在 {{site.data.keyword.Bluemix_notm}} 主控台中顯示時會有「精簡」標籤 ![「精簡」標籤](../icons/Lite.svg)。「精簡」帳戶不會到期，因此不需要信用卡。

您可以存取為您所建立並命名為 `Default` 的單一資源群組。{{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) 所管理的所有服務實例都會自動新增至此資源群組。您隨時可以更新此資源群組的名稱。如需詳細步驟，請參閱[重新命名資源群組](/docs/resources?topic=resources-rgs#rename_rgs)。

每一個資源群組都是免費的。當您在 IAM 所管理的服務與 Cloud Foundry 應用程式之間建立連線時，請建立計入您配額的別名（即服務實例）。請參閱[管理連線](/docs/resources?topic=resources-connect_app)。
{: tip}

### 可用功能
{: #lite-account-features}

請參閱下列清單，其會列出「精簡」帳戶提供的重要特性：

   * 帳戶免費 - 不需要信用卡。
   * 帳戶永不到期。
   * 一個 {{site.data.keyword.Bluemix_notm}} 地區可以使用一個組織。
   * 基本 {{site.data.keyword.Bluemix_notm}} 支援是免費的。針對未使用傳統嚴重性且未規定特定回應時間的非正式作業環境或工作負載，提供了基本支援。
   * 您會收到帳戶狀態及配額限制的電子郵件通知。
   * Cloud Foundry 應用程式每個月可以同時存取最多 256 MB 的免費運行環境記憶體。
   * 您可以佈建 [{{site.data.keyword.Bluemix_notm}} 型錄 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} 中有「精簡」方案之任何服務的一個實例。
   * 在 10 天沒有開發活動之後，您的應用程式就會進入休眠。您可以繼續處理這些活動來起動您的應用程式。
   * 在 30 天沒有開發活動之後，就會刪除具有精簡方案的服務實例。

## 隨收隨付制帳戶
{: #paygo}

使用隨收隨付制帳戶，您可以存取完整的 {{site.data.keyword.Bluemix_notm}} 型錄，包括所有免費方案，且您每個月會得到兩倍的免費運行環境記憶體 512 MB。您只需支付所使用的可計費服務，不會有任何長期合約或承諾消費。

您可以建立多個資源群組來輕鬆管理配額，以及檢視一組資源的計費用量。您的費用是根據 {{site.data.keyword.Bluemix_notm}} 運算及服務的用量。如果您的用量超過免費的運行環境和服務額度，則會收到月份的發票，其中會提供關於資源費用的詳細資料。

此外，您也可以使用「隨收隨付制」帳戶來訂購進階或超值支援方案，以獲得正式作業工作負載的額外協助。請在[支援方案](/docs/get-support?topic=get-support-support-plans)中進一步瞭解。

## 訂閱帳戶
{: #subscription-account}

使用「訂閱」帳戶，您可以建立多個資源群組來輕鬆管理配額，以及檢視一組資源的計費用量。您承諾每個月的最低消費金額，並獲得套用至該最低收費的訂閱折扣。

例如，如果您承諾消費一個月 $100 元且達 6 個月，您會獲得 10% 的折扣。在訂閱期限內，您會獲得 $600 元的用量，但只支付 $540 元。訂閱期限越長，折扣便越大。

您的用量會從訂閱金額總計扣除。即使您的用量每月改變，您都能獲得可預測且一致的計費。如果您的用量超過訂閱金額總計，會針對超過的部分向您收取未經折扣的費率。

如同隨收隨付制帳戶，您的訂閱帳戶讓您能訂購進階或超值支援方案，以獲得所需的額外協助。請在[支援方案](/docs/get-support?topic=get-support-support-plans)中進一步瞭解。

如果您具有訂閱帳戶，則可以從 [{{site.data.keyword.Bluemix_notm}} 型錄](https://{DomainName}/catalog){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示") 建立大部分可用的服務。不過，部分服務會使用需要您個別購買的特定定價方案。

### 服務組合訂閱
{: #service-subscriptions}

服務組合訂閱讓您能存取特定網域內的一組服務，並獲得其額度（這些服務以熱門的使用案例為目標）。您可以從服務組合進行選擇，範圍跨越 AI、分析、{{site.data.keyword.blockchainfull_notm}}、物聯網 (IoT) 及雲端原生服務。如果您的需要橫跨多個網域，可以購買多個服務組合訂閱。

您可以將服務組合新增至任何類型的現有帳戶，包括精簡帳戶。在前 90 天內，您會受到限制，只能使用組合內的服務。起始 90 天之後，您便可以存取完整型錄。服務組合訂閱受到 [{{site.data.keyword.Bluemix_notm}} 服務說明](/docs/overview/terms-of-use?topic=overview-terms)條款的規範。

服務組合訂閱無法透過 {{site.data.keyword.Bluemix_notm}} 主控台取得。若要進一步瞭解及購買服務組合，請與 [{{site.data.keyword.Bluemix_notm}} 銷售人員 ![外部鏈結圖示](../icons/launch-glyph.svg "外部鏈結圖示")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} 聯絡。
{:tip}

購買服務組合訂閱之後，您會收到一封電子郵件，內含特性碼可供您套用以將組合新增至您的帳戶。如需如何套用特性碼的相關資訊，請參閱[套用特性碼](/docs/account?topic=account-codes)。服務組合到期，或是您已使用所有額度時，可以繼續使用任何服務，用量將會以隨收隨付制費率收費。

### {{site.data.keyword.Bluemix_dedicated_notm}} 帳戶
使用 {{site.data.keyword.Bluemix_dedicated_notm}}，您必須註冊至少一年期限，包括：

   * 回到您基礎架構的 VPN 連線功能
   * {{site.data.keyword.BluSoftlayer_notm}} 資料中心內的完整備用環境
   * 所有支援的運行環境（{{site.data.keyword.runtime_liberty_short}}、{{site.data.keyword.runtime_nodejs_short}} 及內建開放程式碼運行環境）
   * 您選取的所有專用服務及所有公用 {{site.data.keyword.Bluemix_notm}} 服務
   * 標準 {{site.data.keyword.Bluemix_notm}} 支援

您也可以訂購選購項目，例如 {{site.data.keyword.BluDirectLink}} 或是進階或超值支援選項。如需相關資訊，請與 [{{site.data.keyword.Bluemix_notm}} 銷售人員 ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg) 聯絡。

您在該期間每個月所支付的金額是根據您想要的專用服務，加上讓您存取所有公用服務的「訂閱」帳戶。{{site.data.keyword.Bluemix_notm}} Public 中的服務使用費用是根據您的「訂閱」帳戶合約來計算。您會收到關於任何超出訂閱合約之使用服務的發票。請與 IBM 指定的客戶業務代表聯絡，或與 [{{site.data.keyword.Bluemix_notm}} 銷售人員](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部鏈結圖示](../icons/launch-glyph.svg) 聯絡，以開始您的合約。

## 升級帳戶
{: #upgrade-lite-account}

當您準備好將帳戶帶到下個層次時，可以[將精簡帳戶升級](/docs/account?topic=account-upgrading-account)至隨收隨付制帳戶或訂閱帳戶。升級帳戶可以解開完整的 {{site.data.keyword.Bluemix_notm}} 型錄、提供您額外的免費資源等等。

將精簡帳戶升級至隨收隨付制帳戶之後，您會得到 $200 元的促銷額度，此額度會自動套用至您的帳戶。您的 $200 元額度有效期限為 30 天，且用量會自動從額度金額扣除。此額度無法用於協力廠商供應項目，且額度可能無法適用於所有帳戶。

如果您已經有「隨收隨付制」或「訂閱」帳戶，也可以將帳戶轉換成不同的類型。如需相關資訊，請參閱[升級帳戶](/docs/account?topic=account-upgrading-account)。
