---

copyright:

  years: 2017, 2018
lastupdated: "2018-11-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}


# 向使用者隱藏公用資源
{: #exclude}

身為 {{site.data.keyword.Bluemix}} 帳戶的管理者，您可以向具有帳戶存取權的使用者隱藏公用資源。您可能會隱藏資源，以向非授權使用者隱藏機密性資訊，或是部分資訊可能需要只由有限數量的人員存取。
{:shortdesc}

隱藏型錄中的資源，並不會將它從 Cloud Foundry 指令行介面 (CLI) 或從可由 {{site.data.keyword.Bluemix_notm}} 主控台導覽的供應項目種類清單（例如金融、行動、Watson 及 Web 應用程式）中移除。
{: note}

您可以使用 {{site.data.keyword.Bluemix}} [指令行介面 (CLI)](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set) 或主控台，來判定您是否有權可容許使用者檢視已新增至帳戶的專用資源。如果您是帳戶擁有者，則可以透過主控台來指派存取原則，將存取權授與給您帳戶中的使用者。如需相關資訊，請參閱[管理帳戶存取權](access.html)。

## 尋找資源
{: #find-resource}

執行 `ibmcloud catalog search <service-id or service-name>` 指令，以搜尋資源。將 service-id 或 service-name 變數取代為資源名稱或 ID。使用所傳回的資訊，來尋找您要隱藏之服務的 ID 或名稱。

## 取得資源的詳細資料

執行 `ibmcloud catalog service <service-id or service-name>` 指令。利用執行前一個指令所傳回的資訊，使用此指令來檢查資源的其他詳細資料。您可以使用所傳回的資訊來檢視階層，而此階層會顯示資源中各項目的子項資源。

## 隱藏資源
{: #vis-exc}

執行下列指令，以防止您帳戶中的使用者檢視公用資源。

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

您可以在 excludes 旗標之後，新增與帳戶相關聯的電子郵件或帳戶 ID 清單（以逗點區隔）。

執行指令之後，隱藏資源的處理程序大約需要 30 分鐘。30 分鐘之後，請登出並重新登入帳戶，以查看隱藏的資源。

您隱藏的項目無法從主控台或 CLI 中取得。遭排除帳戶的管理者仍然可以檢視該資源。
{: note}

## 從排除清單移除帳戶
{: #remove-exclude}

執行下列指令，以從排除清單移除帳戶 ID 或電子郵件。

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`


## 範例：管理子物件的可見性
{: #child}

您可以管理所有資源的可見性。每一個子項資源都有其個別可見性特徵。此範例顯示如何從 Cloudant 服務排除帳戶。

執行 `ibmcloud catalog service cloudant` 指令，來檢視資源的所有子項。

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

尋找物件的 ID，並藉由執行 `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add<account-id or account-email>` 指令來排除帳戶。

如需可見性運作方式的相關資訊，請參閱[型錄 API 文件](https://{DomainName}/apidocs/globalcatalog)。
