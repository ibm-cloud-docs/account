---

copyright:

  years: 2017, 2018
lastupdated: "2017-12-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 將帳戶新增至專用資源
{: #include}

依預設，會限制您建立的任何專用資源。如果您是帳戶的管理者，則可以選擇誰可以看到您的資源，方法是使用 `bx` [指令行介面](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_catalog_entry_visibility_set)將他們新增至 includes 清單。
{:shortdesc: .shortdesc}

## 如何知道我是否有存取權？
{: #find-access}

您可以使用 CLI 或「身分及存取」使用者介面，以判定您是否具有存取權可讓使用者檢視已新增至帳戶的專用資源。如果您是帳戶擁有者，則可以指派存取原則，以透過 Identity and Access Management 使用者介面將存取權授與您帳戶中的使用者。如需相關資訊，請參閱[管理帳戶存取權](access.html)。

## 步驟 1：尋找資源
{: #find-resource}

輸入 `bx catalog service <service-id or service-name>`。將 service-id 或 service-name 取代為您的資源名稱或 ID。您可以使用傳回的資訊來查看階層，而此階層會顯示資源中項目的子項資源。

## 步驟 2：包括帳戶以設定可見性
{: #vis-inc}

輸入下列指令，以容許帳戶看到您的專用資源。

`bx catalog entry-visibility-set <service-id> --includes-add<account-id or account-email>`

在 includes-add 旗標後面，您可以新增與帳戶相關聯的電子郵件或 ID 清單（以逗點區隔）。

執行指令之後，包含資源的處理程序需要 30 分鐘。在 30 分鐘之後，請登出並重新登入帳戶，以查看包含的資源。

## 從 includes 清單中移除帳戶
{: #remove-exclude}

輸入下列指令，以從 includes 清單中移除帳戶。

`bx catalog entry-visibility-set <service-id> --includes-remove<account-id or account-email>`

## 管理子物件可見性
{: #child-vis}

您可以管理資源或其子項的可見性。

空的 includes 清單表示只有您的帳戶管理者才能看到它。您的帳戶必須在 includes 清單中，帳戶的所有成員才能看到它。

例如，如果您輸入 `bx catalog service <your_service>`，則可以看到資源的子項。

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

您可以取得子部署的資源 ID，然後使用下列指令來包括帳戶：`bx catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`.

物件的子項可以透過複雜的方式來繼承可見性。如果子物件為專用，則會有自己的可見性配置。不過，如果子物件設為公用，則會繼承其母項的可見性。設定專用子物件的可見性時，其可見性限制可能會高於母項。

如需可見性運作方式的相關資訊，請參閱 [API 文件](https://console.bluemix.net/apidocs/682)。
