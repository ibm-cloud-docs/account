---

copyright:

  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# パブリック・リソースをアカウントのユーザーに非表示にする
{: #exclude}

アカウントの管理者である場合には、`ibmcloud` [コマンド・ライン・インターフェース](/docs/cli/reference/bluemix_cli/bx_cli.html#ibmcloud_catalog_entry_visibility_set)を使用して除外リストに追加することによって、パブリック・リソースをアカウントの全員に非表示にすることを選択できます。
{:shortdesc: .shortdesc}

**注:** カタログ内の項目を非表示にすることは、Cloud Foundry CLI から、またはグローバル・ナビゲーションで使用可能なサービス・プロビジョニング・リスト (財務、モバイル、Watson、Web アプリなど) から項目を削除することにはなりません。

## アクセス権限の有無を確認する方法
{: #find-access}

アカウントに追加されたプライベート・リソースをユーザーが表示できるようにするためのアクセス権限があるかどうかを判断するために、CLI または ID およびアクセスの UI を使用することができます。 アカウント所有者の場合は、ID およびアクセス管理の UI でアクセス・ポリシーを割り当てることにより、アカウント内のユーザーにアクセス権限を付与できます。 詳しくは、『[アカウントへのアクセスの管理](access.html)』を参照してください。

## ステップ 1: リソースの検出
{: #find-resource}

`ibmcloud catalog search <service-id or service-name>` を入力してリソースを検索します。 service-id または service-name をリソース名または ID に置換します。 返ってきた情報で、非表示にするサービスの ID または名前を見つけます。

## ステップ 2: そのサービスの詳細の取得

`ibmcloud catalog service <service-id or service-name>`を入力します。 前のコマンドで見つかった情報を使用して、このコマンドを使用してリソースの詳細を調べます。 返ってきた情報に、リソースの項目の子リソースを示した階層が表示されます。

## ステップ 3: リソースを非表示にする
{: #vis-exc}

パブリック・リソースがアカウントで見られないようにするには、以下のコマンドを入力します。

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

excludes フラグの後に、アカウントに関連付けられた E メールまたはアカウント ID のコンマ区切りリストを追加できます。

コマンドを実行した後、リソースを非表示にするプロセスに 30 分かかります。 30 分後に、ログアウトしてアカウントに戻り、非表示にされたリソースを確認します。

**注:** 非表示にした項目は UI および ibmcloud CLI から使用できません。 非表示にされた項目は Cloud Foundry マーケットプレイスで引き続き表示されますが、非表示のプランは Cloud Foundry からプロビジョンできません。 除外されたアカウントの管理者は、引き続きリソースを表示できます。

## 除外リストからのアカウントの削除
{: #remove-exclude}

除外リストからアカウント ID または E メールを削除するには、以下のコマンドを入力します。

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`

## 子オブジェクトの可視性の管理の例
{: #child}

すべてのリソースの可視性を管理できます。 各子リソースには、それぞれの可視性の特性があります。

この例では、パブリック Cloudant サービスからアカウントを除外できます。

`ibmcloud catalog service cloudant` を入力すると、リソースの子を表示できます。

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

オブジェクトの ID を見つけて、`ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>` を使用してアカウントを除外します。

可視性の仕組みについての詳細は、[API の資料](https://console.bluemix.net/apidocs/682)を参照してください。
