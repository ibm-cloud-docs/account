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


# パブリック・リソースをユーザーに非表示にする
{: #exclude}

{{site.data.keyword.Bluemix}} アカウントの管理者は、アカウントへのアクセス権限を持っているユーザーに対してパブリック・リソースを非表示にすることができます。許可されていないユーザーに機密情報を知られないようにリソースを非表示にすることができます。また、情報によっては、アクセスする必要があるユーザーが有限の数に限定されるものがあります。
{:shortdesc}

カタログ内のリソースを非表示にしても、Cloud Foundry コマンド・ライン・インターフェース (CLI) から、または {{site.data.keyword.Bluemix_notm}} コンソールのナビゲーションで使用可能なオファリング・カテゴリー・リスト (金融、モバイル、Watson、Web アプリなど) からリソースを削除することにはなりません。
{: note}

{{site.data.keyword.Bluemix}} [コマンド・ライン・インターフェース (CLI)](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set) またはコンソールを使用して、アカウントに追加されたプライベート・リソースをユーザーが表示することを許可するためのアクセス権限が自分にあるかどうかを判断できます。アカウント所有者は、アクセス・ポリシーを割り当てることによって、コンソールからアカウント内のユーザーにアクセス権限を付与できます。詳しくは、[アカウントへのアクセスの管理](access.html)を参照してください。

## リソースの検出
{: #find-resource}

`ibmcloud catalog search <service-id or service-name>` コマンドを実行してリソースを検索します。 service-id 変数または service-name 変数はリソース名または ID に置換してください。返ってきた情報を使用して、非表示にするサービスの ID または名前を見つけます。

## リソースの詳細の取得

`ibmcloud catalog service <service-id or service-name>` コマンドを実行します。前のコマンドの実行で返された情報を使用して、このコマンドを使用してリソースの詳細を調べます。返される情報で、リソース内の項目の子リソースを示す階層が表示されます。

## リソースを非表示にする
{: #vis-exc}

アカウント内のユーザーがパブリック・リソースを表示できないようにするには、以下のコマンドを実行します。

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

excludes (除外) フラグの後に、アカウントに関連付けられた E メールまたはアカウント ID のコンマ区切りリストを追加できます。

コマンドを実行した後、リソースを非表示にするプロセスに約 30 分かかります。 30 分後に、ログアウトしてからアカウントにログインし直し、非表示にされたリソースを確認します。

非表示にした項目は、コンソールおよび CLI からは使用できません。除外されたアカウントの管理者は、引き続きリソースを表示できます。
{: note}

## 除外リストからのアカウントの削除
{: #remove-exclude}

除外リストからアカウント ID または E メールを削除するには、以下のコマンドを実行します。

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`


## 例: 子オブジェクトの可視性の管理
{: #child}

すべてのリソースの可視性を管理できます。 各子リソースには、それぞれの可視性の特性があります。 この例では、Cloudant サービスからアカウントを除外する方法を示します。

`ibmcloud catalog service cloudant` コマンドを実行して、リソースのすべての子を表示します。

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

オブジェクトの ID を見つけて、`ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>` コマンドを実行してアカウントを除外します。

可視性の仕組みについて詳しくは、[カタログ API 資料](https://{DomainName}/apidocs/globalcatalog)を参照してください。
