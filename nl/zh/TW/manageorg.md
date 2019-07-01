---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: update orgs, update spaces, quotas, Cloud Foundry orgs, domains

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# 更新組織及空間
{: #orgupdates}

身為 {{site.data.keyword.Bluemix}} 帳戶擁有者或組織管理員，您可以在組織層次及空間層次執行管理作業。這些作業包括重新命名組織或空間、指派或更新 Cloud Foundry 使用者角色、管理網域，以及檢視組織配額的詳細資料。
{:shortdesc}

移至**管理 > 帳戶**，然後選取 **Cloud Foundry 組織**。

一次只能檢視一個組織的資源。如果您隸屬於多個組織，則可以從主控台功能表列中的使用者帳戶喜好設定鏈結來切換組織。
{: tip}

  * 若要重新命名組織，請針對您要重新命名的組織按一下「動作」圖示 ![「動作」圖示](../icons/action-menu-icon.svg)，然後選取**重新命名**。
    {: #orgrename}

    您所做的任何變更都適用於組織中的所有使用者。

  * 若要刪除組織，請與[支援中心](/docs/get-support?topic=get-support-getting-customer-support)聯絡。
    {: #deleteorgs}

    刪除組織時，也會刪除組織內的所有空間及資源。此動作無法回復。

  * 若要刪除空間，請選取已指派空間的組織。然後，按一下「動作」圖示 ![「動作」圖示](../icons/action-menu-icon.svg)，再選取**刪除**。

    當您刪除空間時，也會刪除所有包含的資源和使用者。

  * 若要編輯組織層次的使用者角色，請按一下「動作」圖示 ![「動作」圖示](../icons/action-menu-icon.svg)，然後選取**使用者**。
    {: #listmembers}

    視您想要如何修改使用者許可權，選取或清除特定角色的方框。您可以在組織層次指派的角色為「管理員」、「帳單管理員」及「審核員」。如需相關資訊，請參閱 [Cloud Foundry 角色](/docs/iam?topic=iam-cfaccess#cfroles)。

  * 若要編輯特定空間的使用者角色，請按一下已指派空間的組織。然後，按一下空間的名稱。

    視您想要如何修改使用者許可權，選取或清除特定角色的方框。您可以在空間層次指派的角色為「管理員」、「開發人員」及「審核員」。如需相關資訊，請參閱 [Cloud Foundry 角色](/docs/iam?topic=iam-cfaccess#cfroles)。

  * 若要管理網域，請針對個別組織按一下「動作」圖示 ![「動作」圖示](../icons/action-menu-icon.svg)，然後選取**網域**。
    {: #managedomains}

    身為帳戶擁有者或組織管理員，您可以檢視系統網域，以及新增在組織及其空間內建置之應用程式的自訂網域。如果您是空間管理員，此頁面會顯示已指派給空間之網域的唯讀清單。

    如果您新增自訂網域，則必須配置 DNS 伺服器來解析自訂網域，以指向 {{site.data.keyword.Bluemix_notm}} 系統網域。使用此方式，{{site.data.keyword.Bluemix_notm}} 接到您的自訂網域的要求時，可以將它適當地遞送至您的應用程式。空間隨時都可以使用系統網域，也可以將自訂網域配置給空間。在空間中建立的應用程式，可能會使用針對該空間所列出的任何網域。如需建立及使用自訂網域的相關資訊，請參閱[管理網域](/docs/apps?topic=creating-apps-update-domain)。

  * 若要管理組織的已配置配額，請針對個別組織按一下「動作」圖示 ![「動作」圖示](../icons/action-menu-icon.svg)，然後選取**配額**。
    {: #managequota}

    從這裡，您可以檢視應用程式數目、記憶體數量、服務數目及方案詳細資料等配額詳細資料。此配額代表建立組織時指派給組織的資源限制。根據您具有免費帳戶還是計費帳戶，組織可用的資源會不同。組織空間中內含的任何應用程式或服務都會影響已配置配額的使用。

    若要變更配置給組織的配額，您必須建立支援案例。如需相關資訊，請參閱[使用支援案例](/docs/get-support?topic=get-support-open-case)。

    若要檢視每個位置的空間層次配額詳細資料，請針對個別組織按一下「動作」圖示 ![「動作」圖示](../icons/action-menu-icon.svg)，然後選取**配額**。然後，相應地展開每一列。
