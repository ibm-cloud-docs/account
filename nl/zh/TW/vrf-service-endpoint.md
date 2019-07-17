---

copyright:
  years: 2019
lastupdated: "2019-07-01"

keywords: VRF, virtual routing and forwarding, service endpoint, private network

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 啟用 VRF 和服務端點
{: #vrf-service-endpoint}

依預設，您可以透過 {{site.data.keyword.Bluemix}} 公用網路來連接至帳戶中的資源。您可以啟用虛擬遞送及轉遞 (VRF)，將您帳戶及其所有資源的 IP 遞送移至個別的遞送表。如果已啟用 VRF，則您可以啟用 {{site.data.keyword.Bluemix_notm}} 服務端點，以直接連接至資源，而不使用公用網路。
{:shortdesc}

若要啟用虛擬遞送及轉遞，以及 {{site.data.keyword.Bluemix_notm}} 服務端點，您需要計費帳戶。

## 啟用 VRF
{: #vrf}

VRF 容許遞送表的多個實例存在於路由器中，並同步運作。當您啟用 VRF 時，會為您的帳戶建立個別的遞送表，並在 {{site.data.keyword.Bluemix_notm}} 網路上分開遞送通往您帳戶資源以及來自帳戶資源的連線。VRF 會在帳戶層次啟用，因此所有資源都受到此網路變更的影響。如需 VRF 技術的相關資訊，以及其如何影響您帳戶的網路遞送，請參閱 [{{site.data.keyword.Bluemix_notm}} 上的虛擬遞送及轉遞](/docs/resources?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud)。

啟用 VRF 會永久地變更您帳戶的網路功能。請務必瞭解這對您帳戶和資源的影響。啟用 VRF 之後，便無法將其停用。
{: important}

若要啟用 VRF，請使用您的要求建立支援案例。

1. 在主控台中，移至**支援**，然後按一下**建立案例**。
1. 選取**帳戶及存取**作為支援類型。
1. 在**主旨**欄位中，輸入`專用網路問題`。
1. 在**說明**欄位中，輸入下列訊息，並將 _enter your account number_ 取代為您的 {{site.data.keyword.Bluemix_notm}} 帳號。

   `We are requesting that account *enter your account number* is moved to its own VRF. We understand the risks and approve the change. Please reply back with the scheduled window(s) of time where this change will be made so we can prepare for the migration.`

{{site.data.keyword.Bluemix_notm}} 網路工程團隊將與案例擁有者聯絡，以排定時間讓帳戶的網路轉換成 VRF。在轉換程序期間，與您帳戶中資源的連線可能會因封包遺失而不穩定。轉換大約需要 15 到 30 分鐘，視您帳戶的複雜性而定。如果您的帳戶有舊式 {{site.data.keyword.BluDirectLink}} 連線，可能會花費更多時間。


## 啟用服務端點
{: #service-endpoint}

當您的帳戶中啟用 {{site.data.keyword.Bluemix_notm}} 服務端點時，您可以選擇在建立資源時公開專用網路端點。然後，您可以透過 {{site.data.keyword.Bluemix_notm}} 專用網路而非公用網路，直接連接至此端點。因為使用專用網路端點的資源沒有網際網路可遞送的 IP 位址，所以這些資源的連線會更安全。如需相關資訊，請參閱[專用網路連線的服務端點](/docs/resources?topic=resources-service-endpoints)。

在啟用服務端點之前，必須先針對您的帳戶啟用 VRF。
{: note}

若要從 CLI 啟用服務端點，您需要有 [{{site.data.keyword.Bluemix_notm}} CLI](/docs/cli?topic=cloud-cli-getting-started) 0.13 版或更新版本。

1.  檢查是否已在帳戶中啟用服務端點。

    ```
    ibmcloud account show
    ```
    {: codeblock}

    如果如下列範例中所示，`Service Endpoint Enabled` 是 `false`，則未啟用服務端點。

    ```
    Retrieving account Mia Example's Account of m.example@example.com...
    OK

    Account ID:                   abc123d0bc2edefthyufffc9b5ca318   
    Currently Targeted Account:   true   
    Linked Softlayer Account:     0123456   
    Service Endpoint Enabled:     false  
    ```
    {: screen}
1. 執行下列指令以啟用服務端點。

   ```
   ibmcloud account update --service-endpoint-enable true
   ```
   {: codeblock}

   可能需要數分鐘，此變更才會生效。指令完成之後，您可以再次執行 `ibmcloud account show` 指令進行驗證。

    如果您的帳戶未啟用 VRF，則執行此指令會提示您建立要案例來啟用它。請輸入 `y` 來建立支援案例。在帳戶中啟用 VRF 之後，重新執行指令以啟用帳戶中的服務端點連線功能。

    ```
    Service Endpoint is not available in linked Softlayer Account 1008967.
    Enable VRF(Virtual Routing and Forwarding) first to proceed.
    Learn more about VRF here - https://cloud.ibm.com/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html.

    Do you want to open a ticket to enable it?[y/N]> y
    Ticket 70729615 was opened successfully. Follow the link https://control.softlayer.com/support/tickets/70729876 to check the details and track the status of the ticket. You will be required to login to view this ticket.
    Account ID:    1008967
    Ticket:        Private Network Question
    ```
    {: screen}


啟用服務端點之後，您可以建立透過 {{site.data.keyword.Bluemix_notm}} 專用網路進行連接的資源。如需支援服務端點的服務清單，以及相關資訊，請參閱[設定專用網路端點](/docs/resources?topic=resources-private-network-endpoints)。
