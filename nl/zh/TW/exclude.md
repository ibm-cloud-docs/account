---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 向帳戶中的使用者隱藏公用資源
{: #exclude}

如果您是帳戶的管理者，則可以向帳戶中的每個人隱藏公用資源。請使用 `ibmcloud` [指令行介面](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set)將資源新增至排除清單。
{:shortdesc: .shortdesc}

**附註：**隱藏型錄中的資源，並不會從 Cloud Foundry CLI 或是透過廣域導覽取得的服務佈建清單（例如金融、行動、Watson 及 Web 應用程式）中移除它。

## 如何知道我是否有存取權？
{: #find-access}

您可以使用 CLI 或「身分及存取」使用者介面，以判定您是否具有存取權可讓使用者檢視已新增至帳戶的專用資源。如果您是帳戶擁有者，則可以指派存取原則，以透過 Identity and Access Management 使用者介面將存取權授與您帳戶中的使用者。如需相關資訊，請參閱[管理帳戶存取權](access.html)。

## 步驟 1：尋找資源
{: #find-resource}

輸入 `ibmcloud catalog search <service-id or service-name>` 以搜尋資源。將 service-id 或 service-name 取代為資源名稱或 ID。在傳回的資訊中，尋找您要隱藏之服務的 ID 或名稱。

## 步驟 2：取得該服務的詳細資料

輸入 `ibmcloud catalog service <service-id or service-name>`。利用前一個指令中找到的項目，使用此指令來檢查資源的更多詳細資料。您可以使用傳回的資訊來查看階層，而此階層會顯示資源中項目的子項資源。

## 步驟 3：隱藏資源
{: #vis-exc}

輸入下列指令，以防止您的帳戶看到公用資源。

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

在 `excludes` 旗標後面，您可以新增與帳戶相關聯的電子郵件或帳戶 ID 清單（以逗點區隔）。

執行指令之後，隱藏資源的處理程序需要 30 分鐘。在 30 分鐘之後，請登出並重新登入帳戶，以查看隱藏的資源。

**附註：**無法從使用者介面及 {{site.data.keyword.Bluemix}} CLI 取得您的隱藏項目。隱藏項目在 Cloud Foundry Marketplace 中仍然可見，但無法從 Cloud Foundry 佈建隱藏方案。遭排除帳戶的管理者仍然可以看到該資源。

## 從排除清單移除帳戶
{: #remove-exclude}

輸入下列指令，以從排除清單移除帳戶 ID 或電子郵件。

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`

## 管理子物件可見性範例
{: #child}

您可以管理所有資源的可見性。每一個子項資源都有其個別可見性特徵。

在此範例中，您可以從公用 Cloudant 服務中排除帳戶。

如果您輸入 `ibmcloud catalog service cloudant`，則可以看到資源的子項。

```
ID                 cloudant
Name               cloudantnosqldb
Kind               service
Provider           IBM
Tags               data_management, ibm_created, ibm_dedicated_public, lite
Active             true
Description        Cloudant NoSQL DB is a fully managed data layer designed for modern web and mobile applications that leverages a flexible JSON schema. Cloudant is built upon and compatible with Apache CouchDB and accessible through a secure HTTPS API, which scales as your application grows. Cloudant is ISO27001 and SOC2 Type 1 certified, and all data is stored in triplicate across separate physical nodes in a cluster for HA/DR within a data center.
Bindable           true
RC Compatible      false
RC Provisionable   false
Children           Name                                          Kind         ID                                               Location
                   lite                                          plan         cloudant-lite
                   |__lite-eu-gb                             deployment   cloudant-lite:eu-gb                          eu-gb
                   |  |__lite-alias-eu-gb                    alias        cloudant-lite:alias:eu-gb                    eu-gb
                   |__lite-us-south                          deployment   cloudant-lite:us-south                       us-south
                      |__lite-alias-us-south                 alias        cloudant-lite:alias:us-south                 us-south
                   standard                                      plan         cloudant-standard
                   |__standard-eu-gb                         deployment   cloudant-standard:eu-gb                      eu-gb
                   |  |__standard-alias-eu-gb                alias        cloudant-standard:alias:eu-gb                eu-gb
                   |__standard-us-south                      deployment   cloudant-standard:us-south                   us-south
                      |__standard-alias-us-south             alias        cloudant-standard:alias:us-south             us-south
```

尋找物件的 ID，並使用 `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>` 來排除帳戶。

如需可見性運作方式的相關資訊，請參閱 [API 文件](https://console.bluemix.net/apidocs/globalcatalog)。
