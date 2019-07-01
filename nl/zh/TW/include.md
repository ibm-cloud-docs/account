---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords: add user, share resource, private resource, share catalog, find resource, set visibility

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 將帳戶新增至專用資源
{: #include}

依預設，會限制您建立的任何 {{site.data.keyword.Bluemix}} 專用資源。如果您是帳戶的管理者，則可以藉由將使用者新增至包含清單，來選擇可以檢視資源的人員。
您還可以轉移專用資源的所有權。
{:shortdesc}

您可以使用 {{site.data.keyword.Bluemix}} [指令行介面 (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) 或主控台，來判定您是否有權可容許使用者檢視已新增至帳戶的專用資源。如果您是帳戶擁有者，則可以透過主控台來指派存取原則，將存取權授與給您帳戶中的使用者。如需相關資訊，請參閱[管理對帳戶的存取權](/docs/account?topic=account-find-access)。

## 尋找資源
{: #find-resource-inc}

執行 `ibmcloud catalog service <service-id or service-name>` 指令。將 service-id 或 service-name 變數取代為資源名稱或 ID。使用所傳回的資訊來檢視階層，而此階層會顯示資源中各項目的子項資源。

## 藉由包含帳戶來設定可見性
{: #vis-inc}

執行下列指令，以容許帳戶查看您的專用資源。

```
ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>
```
{:codeblock}

在 includes-add 旗標後面，您可以新增與帳戶相關聯的電子郵件或 ID 清單（以逗點區隔）。

執行指令之後，包含資源的處理程序大約需要 30 分鐘。在 30 分鐘之後，請登出並重新登入帳戶，以查看包含的資源。

## 從包含清單移除帳戶
{: #remove-include}

執行下列指令，以從包含清單移除帳戶。

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## 範例：管理子物件的可見性
{: #child-vis}

您可以管理資源或其子項的可見性。空的包含清單表示只有帳戶管理者才能進行檢視。您的帳戶必須內含在包含清單中，帳戶的所有成員才能進行檢視。

下列範例顯示如何執行 `ibmcloud catalog service cloudant` 指令，以檢視 Cloudant 服務實例的子項。

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

您可以取得子項部署的資源 ID，然後執行下列指令來包含帳戶：

```
ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>
```
{:codeblock}

物件的子項可以透過複雜的方式來繼承可見性。如果子物件為專用，則會有自己的可見性配置。不過，如果子物件設為公用，則會繼承其母項的可見性。設定專用子物件的可見性時，其可見性限制可能會高於母項。如需可見性運作方式的相關資訊，請參閱[型錄 API 文件](https://{DomainName}/apidocs/globalcatalog)。

## 移轉專用資源的所有權
{: #owners}

如果您離開專案或組織，您可能希望將您帳戶中的資源的所有權轉移給其他某個人。


移轉所有權之後，就無法再從您的帳戶檢視該資源。請確定您要移轉所有權，因為此動作無法復原。
{: important}

您可以使用 [{{site.data.keyword.Bluemix}} 指令行介面 (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) 來移轉專用資源的所有權。請執行下列指令：

```
ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>
```
{:codeblock}
