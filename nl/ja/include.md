---

copyright:

  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# プライベート・リソースへのアカウントの追加
{: #include}

作成したプライベート・リソースは、デフォルトで制限されています。 アカウントの管理者である場合には、`ibmcloud` [コマンド・ライン・インターフェース](/docs/cli/reference/bluemix_cli/bx_cli.html#ibmcloud_catalog_entry_visibility_set)を使用して組み込みリストに追加することによって、リソースを表示できる人を選択することができます。
{:shortdesc: .shortdesc}

## アクセス権限の有無を確認する方法
{: #find-access}

アカウントに追加されたプライベート・リソースをユーザーが表示できるようにするためのアクセス権限があるかどうかを判断するために、CLI または ID およびアクセスの UI を使用することができます。 アカウント所有者の場合は、ID およびアクセス管理の UI でアクセス・ポリシーを割り当てることにより、アカウント内のユーザーにアクセス権限を付与できます。 詳しくは、『[アカウントへのアクセスの管理](access.html)』を参照してください。

## ステップ 1: リソースの検索
{: #find-resource}

`ibmcloud catalog service <service-id or service-name>`を入力します。 service-id または service-name をリソース名または ID に置換します。 返ってきた情報に、リソースの項目の子リソースを示した階層が表示されます。

## ステップ 2: アカウントの組み込みによる可視性の設定
{: #vis-inc}

アカウントがプライベート・リソースを表示できるよう許可するには、以下のコマンドを入力します。

`ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

includes-add フラグの後に、アカウントに関連付けられた E メールまたは ID のコンマ区切りリストを追加できます。

コマンドを実行した後、リソースを組み込むプロセスに 30 分かかります。 30 分後に、ログアウトしてアカウントに戻り、組み込まれたリソースを確認します。

## 組み込みリストからのアカウントの削除
{: #remove-exclude}

組み込みリストからアカウントを削除するには、以下のコマンドを入力します。

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## 子オブジェクトの可視性の管理
{: #child-vis}

リソースの可視性もその子の可視性も管理できます。

組み込みリストが空であることは、アカウント管理者のみが表示できるということを意味します。 アカウントのすべてのメンバーが表示できるようにするためには、自分のアカウントが組み込みリストに載っている必要があります。

例えば、`ibmcloud catalog service <your_service>` を入力すると、リソースの子を表示できます。

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

子デプロイメントのリソース ID を取得して、以下のコマンドを使用してアカウントを組み込むことができます。 `ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`.

オブジェクトの子は複雑な方法で可視性を継承できます。 子オブジェクトがプライベートである場合、独自の可視性構成があります。 しかし、子オブジェクトがパブリックに設定されている場合、その親の可視性を継承します。 プライベート子オブジェクトに可視性を設定すると、親よりも可視性が制限されることがあります。

可視性の仕組みについての詳細は、[API の資料](https://console.bluemix.net/apidocs/682)を参照してください。
