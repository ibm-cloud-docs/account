---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: create account, IBMid, sign up for account, sign up

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# {{site.data.keyword.Bluemix_notm}} への登録
{: #signup}

{{site.data.keyword.Bluemix}} アカウントを登録するには、既存の IBMid を使用するか、新しい IBMid を作成します。 シングル・サインオン用にフェデレーテッド ID を使用するようお客様の会社が登録されている場合は、フェデレーテッド ID を使用して登録します。
{:shortdesc}

| 登録 ID | 詳細 |    
|-----------------|---------|
|既存の IBMid   | IBMid を既にお持ちの場合は、IBM の他の製品やサービスに使用する既存の資格情報で {{site.data.keyword.Bluemix_notm}} に登録します。 |
|新しい IBMid        | IBMid をまだお持ちではない場合は、登録時に IBMid を作成します。 IBMid を使用すると、1 つのユーザー名を、{{site.data.keyword.Bluemix_notm}} など、IBM のすべての製品およびサービスへのログインに使用できます。 |
|フェデレーテッド ID     | お客様が、自社のドメインのユーザー資格情報を IBM に登録する申請を済ませている場合は、会社のログインに既に使用している資格情報で {{site.data.keyword.Bluemix_notm}} へのアカウント登録を行えます。 登録する際には、電話番号を入力する必要があります。 |
{:caption="表 1. {{site.data.keyword.Bluemix_notm}} への登録に用いる ID オプション" caption-side="top"}

## 新規または既存の IBMid を使用した登録
{: #signup-ibmid}

フェデレーテッド ID を使用する会社に属していない場合は、IBMid を使用して {{site.data.keyword.Bluemix_notm}} に登録します。

1. [{{site.data.keyword.Bluemix_notm}} ログイン・ページ](https://cloud.ibm.com/){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") に移動して、**「{{site.data.keyword.Bluemix_notm}} アカウントの作成」**をクリックします。
1. IBMid 用の E メール・アドレスを入力します。 既存の IBMid がない場合は、入力した E メールに基づいて ID が作成されます。
1. 残りのフィールドに情報を入力し、**「アカウントの作成」**をクリックします。
1. 指定した E メール・アドレスに送信された確認メールのリンクをクリックして、アカウントを確認します。

新しいアカウントでのログインで問題が発生した場合は、[{{site.data.keyword.Bluemix_notm}} へのアクセスに関するトラブルシューティング](/docs/account?topic=account-accessing)を参照してください。

## フェデレーテッド ID を使用した登録
{: #signup-federated}

フェデレーテッド ID は、IBM に登録済みの会社ドメイン内の ID で、これにより、ドメインとユーザーの資格情報を使用して IBM Web アプリケーションにアクセスできます。 お客様の会社が既に IBM への登録を済ませている場合にのみ、フェデレーテッド ID を使用して {{site.data.keyword.Bluemix_notm}} に登録できます。 会社のドメインを IBM に登録すると、会社の既存のユーザー資格情報で IBM の製品やサービスにログインできるようになります。 その後、認証は、お客様の会社の ID プロバイダーによって SSO を使用して処理されます。

IBM では、この ID 連携のために Security Assertion Markup Language 2.0 (SAML 2.0) を使用しています。 SAML 2.0 は、セキュリティー・ドメイン間で認証データを交換するための標準版です。 これは XML ベースのプロトコルであり、アサーションが格納されたセキュリティー・トークンを使用して、組織の「ID プロバイダー」と「IBM Rely Party (RP)」(サービス・プロバイダー) の間で情報を受け渡します。

フェデレーテッド ID 用にお客様の会社を登録する方法について詳しくは、[IBMid Enterprise Federation Adoption Guide![外部リンク・アイコン](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window} を参照してください。 フェデレーテッド ID の登録を申請する際には、IBM のサポート役 (オファリング担当者やお客様担当者など) が必要です。

### フェデレーテッド ID を使用したログイン
{: #login-federated}

フェデレーテッド ID で {{site.data.keyword.Bluemix_notm}} コンソールにログインすると、お客様の会社のログイン・ページを通じたログインを求められます。 CLI を通じてログインする場合は、認証のために追加パラメーターを指定する必要があります。 詳しくは、[フェデレーテッド ID を使用したログイン](/docs/iam?topic=iam-federated_id)を参照してください。
