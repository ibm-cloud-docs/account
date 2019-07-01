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

# プライベート・リソースへのアカウントの追加
{: #include}

作成する {{site.data.keyword.Bluemix}} プライベート・リソースは、デフォルトで制限されています。 アカウントの管理者は、包含リストにユーザーを追加することで、リソースを表示できるユーザーを選択できます。また、専用リソースの所有権を移動することもできます。
{:shortdesc}

{{site.data.keyword.Bluemix}} [コマンド・ライン・インターフェース (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) またはコンソールを使用して、アカウントに追加されたプライベート・リソースをユーザーが表示することを許可するためのアクセス権限が自分にあるかどうかを判断できます。 アカウント所有者は、アクセス・ポリシーを割り当てることによって、コンソールからアカウント内のユーザーにアクセス権限を付与できます。 詳しくは、[アカウントへのアクセスの管理](/docs/account?topic=account-find-access)を参照してください。

## リソースの検出
{: #find-resource-inc}

`ibmcloud catalog service <service-id or service-name>` コマンドを実行します。 service-id 変数または service-name 変数はリソース名または ID で置き換えてください。 返される情報に、リソース内の項目の子リソースを示す階層が表示されます。

## アカウントの包含による可視性の設定
{: #vis-inc}

アカウントがプライベート・リソースを表示できるよう許可するには、以下のコマンドを実行します。

```
ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>
```
{:codeblock}

includes-add フラグの後に、アカウントに関連付けられた E メールまたは ID のコンマ区切りリストを追加できます。

コマンドを実行した後、リソースを組み込むプロセスに約 30 分かかります。 30 分後に、ログアウトしてアカウントに戻り、組み込まれたリソースを確認します。

## 組み込みリストからのアカウントの削除
{: #remove-include}

組み込みリストからアカウントを削除するには、以下のコマンドを実行します。

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## 例: 子オブジェクトの可視性の管理
{: #child-vis}

リソースの可視性もその子の可視性も管理できます。 空の includes (包含) リストは、アカウント管理者のみが表示できることを意味します。 アカウントのすべてのメンバーが表示できるようにするためには、アカウントが包含リストに入っている必要があります。

以下の例は、`ibmcloud catalog service cloudant` コマンドを実行して Cloudant サービス・インスタンスの子を表示する方法を示しています。

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

子デプロイメントのリソース ID を取得し、その後で、以下のコマンドを実行してアカウントを包含することができます。

```
ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>
```
{:codeblock}

オブジェクトの子は複雑な方法で可視性を継承できます。 子オブジェクトがプライベートである場合、独自の可視性構成があります。 しかし、子オブジェクトがパブリックに設定されている場合、その親の可視性を継承します。 プライベート子オブジェクトに可視性を設定すると、親よりも可視性が制限されることがあります。 可視性の仕組みについて詳しくは、[カタログ API 資料](https://{DomainName}/apidocs/globalcatalog)を参照してください。

## プライベート・リソースの所有権の移管
{: #owners}

プロジェクトまたは組織を去るときに、アカウント内のリソースの所有権を他のユーザーに移すことが必要な場合があります。

所有権を移管すると、自分のアカウントからはリソースを表示できなくなります。 このアクションは元に戻すことはできないため、所有権を本当に移管してもよいことを確認してください。
{: important}

[{{site.data.keyword.Bluemix}} コマンド・ライン・インターフェース (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) を使用して、プライベート・リソースの所有権を移管できます。 次のコマンドを実行します。

```
ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>
```
{:codeblock}
