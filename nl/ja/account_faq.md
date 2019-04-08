---

copyright:
  years: 2015, 2019
lastupdated: "2019-03-25"

keywords: account, upgrade, account settings, IBM Cloud account, Lite account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:tip: .tip}

# FAQ
{: #accountfaqs}

## アカウントを作成するには、どのようにすればよいですか?
{: #create-account}
{: faq}

[{{site.data.keyword.Bluemix}}](https://cloud.ibm.com){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") にアクセスし、**「{{site.data.keyword.Bluemix_notm}} アカウントの作成」**をクリックして、有効期限が切れることのないライト・アカウントを作成します。 含まれるフィーチャーについて詳しくは、『[ライト・アカウント](/docs/account?topic=account-liteaccount#liteaccount)』を参照してください。


## アカウントを作成するときに発生したエラーを解決するには、どのようにすればよいですか?
{: #account-error}
{: faq}

{{site.data.keyword.Bluemix_notm}} アカウントにログインできる場合は、[サポート](https://test.cloud.ibm.com/unifiedsupport/supportcenter)にアクセスして、以下のいずれかのオプションを選択してください。

* 拡張サポートまたはプレミアム・サポートのお客様の場合は、**「ライブ・チャット」** をクリックして、{{site.data.keyword.Bluemix_notm}} サポート担当者にご相談ください。
* 「_お困りですか?_」セクションで、**「Case の作成 (Create a case)」**をクリックしして、サポート Case を作成します。

   Case のオープン後に、E メール通知が送信されます。 その後のコミュニケーションについての指示に従ってください。

{{site.data.keyword.Bluemix}} アカウントにログインできない場合は、[アカウント要求を作成してください](https://watson.service-now.com/x_ibmwc_open_case_app.do#!/create){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")。


## Cloud Foundry とは?
{: #cloud-foundry}
{: faq}

Cloud Foundry は、クラウド上でアプリケーションを作成およびデプロイするために、{{site.data.keyword.Bluemix_notm}} Public を通して利用可能な、オープン・ソース Platform as a Service (PaaS) オプションです。 特定の地域内で使用可能なリソースおよびアプリを編成するために Cloud Foundry の組織およびスペースが使用されます。

組織とスペースの管理について詳しくは、[組織およびスペースの追加](/docs/account?topic=account-orgsspacesusers#orgsspacesusers)を参照してください。 また、Cloud Foundry スペースでリソースに対するアクセス権限を提供する方法について詳しく知りたい場合は、[Cloud Foundry アクセス権限](/docs/iam?topic=iam-cfaccess#cfaccess)を参照してください。


## 組織を別のアカウントに移動できますか?
{: #move-org-diff-account}
{: faq}

現在のところ、組織を別のアカウントに移動することはできません。 ただし、この機能を再現するために、別のアカウントで同じ資格情報を使用して組織を再作成することは可能です。 詳しくは、『[組織およびスペースの追加](https://cloud.ibm.com/docs/account?topic=account-orgsspacesusers#createorg)』を参照してください。


## どの Cloud Foundry 地域を使用できますか?
{: #whichregions}
{: faq}

ライト・アカウントでは、1 つの地域でのみ作業できます。 従量課金 (PAYG) アカウントまたはサブスクリプション・アカウントでは、使用可能なすべての地域にアクセスできます。


## サービスのライト価格プランはどのようなものですか
{: #whatisliteplan}
{: faq}

ライト・プランは、無料割り当て量ベースのサービス・プランです。 サービスのライト・プランを使用すると、いかなる料金も発生せずに、アプリを作成できます。 ライト・プランは、1 カ月サイクル (毎月更新) ベースまたは 1 回限りの使用量ベースで提供されます。 ライト・プラン・サービスごとに 1 つのインスタンスを使用できます。 ライト価格プランは、すべてのアカウントで提供されます。 ライト・アカウントについて詳しくは、『[アカウント・タイプ](/docs/account?topic=account-accounts#accounts)』を参照してください。


## ライト・プランのインスタンスが毎月の割り当て量に達すると、どうなりますか?
{: #monthlyquota}
{: faq}

ライト・プランのインスタンスがいずれかの割り当て量の制限に達すると、その月のサービスは使用停止されます。 割り当て量の制限は、インスタンスごとではなく、組織ごとに課せられます。 同じ組織内で作成された新しいインスタンスには、これまでのインスタンスによる使用量が反映されます。 割り当て量の制限は、毎月 1 日にリセットされます。

使用量を確認するには、**「管理」 > 「請求および使用量」**に移動し、**「使用量」**を選択します。 詳しくは、[「使用量の表示」](/docs/billing-usage?topic=billing-usage-viewingusage)を参照してください。

サービスの停止または削除は、リソース・リストから行うことができます。 詳しくは、『[{{site.data.keyword.Bluemix_notm}} コンソールのナビゲート](/docs/overview?topic=overview-ui)』を参照してください。


## 作成できるリソース・グループ数、組織数、スペース数はいくつですか?
{: #resourcelimit}
{: faq}

有料アカウントを使用している場合は、アカウント内で作成できるリソース・グループ、組織、またはスペースの数に制限はありません。 しかし、ライト・アカウントの場合は、1 つの組織と 1 つのリソース・グループに制限されます。

## アカウント・タイプをアップグレードまたは変換するには、どのようにすればよいですか?
{: #changeacct}
{: faq}

* ライト・アカウントから従量課金 (PAYG) アカウントまたはサブスクリプション・アカウントにアップグレードするには、[「アカウント設定」](https://{DomainName}/account/settings)に進みます。
  * 従量課金 (PAYG) アカウントにアップグレードするには、**「クレジット・カードの追加」**をクリックします。
  * サブスクリプション・アカウントにアップグレードするには、**「アップグレード」**をクリックします。
* 従量課金 (PAYG) アカウント・タイプとサブスクリプション・アカウント・タイプの間で変換を行うには、[{{site.data.keyword.Bluemix_notm}} 営業担当員 ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} にお問い合わせください。

詳しくは、『[アカウントのアップグレード](/docs/account?topic=account-upgrading-account)』を参照してください。

## ライト・アカウントをアップグレードした場合、既存のインスタンスを引き続き使用できますか?
{: #nochange}
{: faq}

はい。有料アカウントにアップグレードした場合、ライト・アカウントで作成したインスタンスは引き続き使用できます。

## クレジット・カードを更新するには、どのようにすればいいですか?
{: #updatepayment}
{: faq}

アカウントに関連付けられている支払い方法は、コンソールで[「支払い」](https://cloud.ibm.com/billing/payments)に進むことによって更新できます。 「支払い方法の追加」の下で、新しいカードの請求先情報を入力し、**「クレジット・カードの追加」**をクリックします。

異なる支払い方法に切り替えるには、**「他の方法で支払う」**を選択し、**「変更要求の送信」**をクリックします。 支払い方法を変更するためのサポート Case が作成されます。

## パスワードをリセットするには、どのようにすればよいですか?
{: #reset-password}
{: faq}

アカウントのパスワードをリセットするには、アバターのアイコン ![アバター・アイコン](../icons/i-avatar-icon.svg) **>「プロファイルと設定」**に移動します。 次に、アカウント・ユーザー情報のタイルから**「変更またはリセット」**をクリックします。

VPN パスワードをリセットするには、以下のステップを実行します。

  1. **「管理」 > 「アクセス (IAM)」**に移動して、**「ユーザー」**を選択します。
  2. ユーザーを選択します。
  3. 「VPN サブネット」セクションで、編集アイコン ![編集アイコン](../icons/icon_write.svg) をクリックして、新しい VPN パスワードを入力します。
  5. **「適用」**をクリックします。

## アカウントを取り消すには、どのようにすればよいですか?
{: #cancelaccount}
{: faq}

取り消しをご希望でしょうか。 取り消しを行う前に、アカウントに関してお手伝いさせていただくことがあれば、サポートにお問い合わせください。

取り消しを行う場合、アカウントを取り消す方法は、アカウントのタイプによって異なります。 アカウントのタイプをチェックするには、[「アカウント設定」](https://cloud.ibm.com/account/settings) に移動し、_「アカウント・タイプ」_の下で確認してください。

* 従量課金 (PAYG) アカウントまたはサブスクリプション・アカウントの場合、アカウントを取り消す最も簡単な方法は、[ライブ・チャット](https://{DomainName}/unifiedsupport/supportcenter)で連絡するか、1-866-325-0045 に電話をかけて 3 番目のオプションを選択することです。 あるいは、サポート Case を開くこともできます。
* ライト・アカウントを取り消すには、[「アカウント設定」](https://cloud.ibm.com/account/settings)に進み、**「アカウントの非アクティブ化」**をクリックします。

## アカウントを削除するには、どのようにすればよいですか?
{: #deleteaccount}
{: faq}

[{{site.data.keyword.Bluemix_notm}} サポート ![外部リンク・アイコン](../icons/launch-glyph.svg)](https://{DomainName}/unifiedsupport/supportcenter){: new_window} に連絡して、サポート Case をオープンし、アカウントの削除を依頼してください。 古いアカウントに関連付けられているデータで、新規アカウントに移行したいものがあれば、その情報を E メールに記載してください。


## アカウントが非アクティブになったのはなぜですか?
{: #account-deactivated}
{: faq}

以下の理由でアカウントが非アクティブになることがあります。

- トライアル・アカウントの場合、トライアル期間が終わった。 アカウントを再アクティブ化するには、アカウントにログインし、従量課金 (PAYG) アカウントにアップグレードします。
- 権限があるユーザーがアカウントを取り消した。
- アカウントが中断状態になった。 IBM の裁量により、{{site.data.keyword.Bluemix_notm}} サービスの容認できる使用行動に違反したアカウントは、予告なしに使用不可にされることがあります。 ユーザーが攻撃的なアクションを通知された後に使用行動を修正した場合、一部のサービスが復元されることがあります。

アカウントが誤って非アクティブになったと思われる場合は、1-866-325-0045 に電話し、3 番目のオプションを選択することによって、サポートに連絡してください。

## サポートを依頼するには、どのようにすればよいですか
{: #contactsupport}
{: faq}

コンソールのメニュー・バーで**「サポート」**をクリックして、サポート・センターにアクセスしてください。 サポートについて詳しくは、[サポートの利用](/docs/get-support?topic=get-support-support-plans] を参照してください。


## 無料トライアルに登録できますか?
{: #freetrial}
{: faq}

認定された学術機関の教師および生徒は {{site.data.keyword.Bluemix_notm}} トライアル・アカウントを使用できます。 トライアル・アカウントの資格を得るには、[Harness the Power of IBM ![外部リンク・アイコン](../icons/launch-glyph.svg)](https://onthehub.com/ibm/){: new_window} にアクセスし、機関の資格情報を検証します。


## アカウントをリンクした後、ログインするにはどうすればよいですか?
{: #al_login}
{: faq}

アカウントをリンクした後、IBMid を使用して、{{site.data.keyword.Bluemix}} コンソールにログインします。


## アカウントをリンクすると、サポートについてどのような影響がありますか?
{: #al_support}
{: faq}

アカウントをリンクした後、{{site.data.keyword.Bluemix_notm}} プラットフォームをアカウントに追加すると、同じレベルのサポートが維持されます。


## アカウントのリンクについて支援を得る他の方法はありますか?
{: #al_morehelp}
{: faq}

  1. [IaaS アカウントと PaaS アカウントをリンクする手順についてのブログ](https://www.ibm.com/blogs/bluemix/2018/03/follow-steps-link-iaas-paas-accounts/){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") を参照して有用な情報を見つけてください。
  2. {{site.data.keyword.BluSoftlayer_full}} のカスタマー・ポータルで、**「販売ライブ・チャット (Sales Live Chat)」**を開き、アカウントに関する質問をしてください。
  3. カスタマー・ポータルからチケットをオープンします。 **「サポート」** > **「チケットの追加
」**を選択し、次に、**「サブジェクト」**フィールドで**「アカウンティング要求 (Accounting Request)」**を選択して、アカウントの質問を適格なサポート・チームに送付します。

## 複数のアカウントを持っている場合、アカウントをリンクするにはどうすればよいですか?
{: #al_multacct}
{: faq}

複数の SoftLayer アカウントを持っている場合、一致する {{site.data.keyword.Bluemix_notm}} プラットフォーム・アカウントを持つアカウントと、付随する IBMid をリンクする必要があります。

一致する {{site.data.keyword.Bluemix_notm}} プラットフォーム・アカウントと、付随する IBMid アカウントがない場合は、新しい SoftLayer アカウントを作成してアカウントをリンクすることができます。

## アカウントをリンクすると何かインセンティブはありますか?
{: #al_incent}
{: faq}

アカウントをリンクすると、200 ドルのプロモーション・クレジットを使用して {{site.data.keyword.Bluemix_notm}} サービスを試すことができます。

200 ドルのプロモーション・クレジットについて詳しくは、[従量課金 (PAYG) アカウント](/docs/account?topic=account-accounts#paygo)を参照してください。

## {{site.data.keyword.Bluemix_notm}} プラットフォーム・サービスを SoftLayer アカウントに追加するとはどういう意味ですか?
{: #al_owaffslacct}
{: faq}

それは、アカウントがすべての {{site.data.keyword.Bluemix_notm}} プラットフォームのオファリングにアクセスできることを意味します。 {{site.data.keyword.Bluemix_notm}} プラットフォームのオファリングをアカウントに追加した後、アカウント・マスターはユーザーがオファリングにアクセスできるようにする必要があります。

アカウント・マスターであることについて詳しくは、[ユーザーの操作](/docs/iam?topic=iam-iamuserinv#iamuserinv)を参照してください。

## アカウントをリンクすると、SoftLayer マスター・アカウント ID にどのような影響がありますか?
{: #al_howaffslmastacct}
{: faq}

{{site.data.keyword.Bluemix_notm}} コンソールには IBMid を使用してアクセスできるため、カスタマー・ポータルへのサインインに Softlayer アカウントの ID を引き続き使用できます。

## 複数のアカウントを切り替えるには、どのようにすればよいですか?
{: #switch-between-accounts}
{: faq}

アカウントを複数お持ちの場合、アカウント名をクリックして、アクセス権限のある別のアカウントを選択できます。  

![アカウント切り替えの画面キャプチャー](images/account-faq.svg "アカウント切り替えの画面キャプチャー")

## アカウント所有者を切り替えることはできますか?
{: #switch-account-owners}
{: faq}

アカウント所有者を切り替えることはできませんが、リソース所有者を変更することはできます。 所有権の切り替えについて詳しくは、『[プライベート・リソースの所有権の移動](/docs/account?topic=account-include#owners)』を参照してください。

## {{site.data.keyword.Bluemix_notm}} ではユーザーのバッチ登録はサポートされていますか?
{: #batch-registration}
{:faq}

{{site.data.keyword.Bluemix_notm}} 用にユーザーを登録する時は、各ユーザーを個別に登録しなければなりません。 {{site.data.keyword.Bluemix_notm}} では、ユーザーのバッチ登録はサポートしていません。

[{{site.data.keyword.Bluemix}}](https://cloud.ibm.com){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") にアクセスし、**「{{site.data.keyword.Bluemix_notm}} アカウントの作成」**をクリックします。 次に、個々のユーザーごとにアカウント登録フォームに記入します。

## タグとは何ですか?
{: #know-about-tags}
{: faq}

タグを使用すると、リソース・リストからタグをフィルタリングすることによって、アカウント全体でリソースを編成および表示することができます。 詳しくは、『[タグの処理](/docs/resources?topic=resources-tag)』を参照してください。

## アカウント内のタグを表示できるのは誰ですか?
{: #tags-visibility-account}
{: faq}

タグはアカウント全体で可視です。 リソースを表示する権限があれば、アタッチされているすべてのタグを表示できます。 詳しくは、『[リソースにタグ付けする権限をユーザーに付与する](/docs/resources?topic=resources-access#access)』を参照してください。

## タグを追加または削除するために必要な権限は何ですか?
{: #permissions-add-remove-tags}
{: faq}

リソースのタグを追加または削除するには、少なくとも、IAM 対応リソースに対するエディター役割か、または、そのリソースに対する Cloud Foundry スペース内での開発者役割を持っている必要があります。 詳しくは、『[リソースにタグ付けする権限をユーザーに付与する](/docs/resources?topic=resources-access#access)』を参照してください。

## タグを削除することはできますか?
{: # delete-tag}
{: faq}

タグを削除するには、その前にすべてのリソースからそのタグを削除する必要があります。 それでも削除できない場合は、自分には表示権限がないリソースにそのタグがアタッチされている可能性があります。 同じ請求アカウント内の異なるユーザーによって、同じタグがいくつかのリソースにアタッチされることがあり得ます。 アカウントのすべてのリソースに対してすべてのユーザーが同じ可視性を持つわけではありません。

## タグの名前を変更できますか?
{: #rename-tag}
{: faq}

タグの名前を編集することはできません。 タグの名前を変更するには、タグを削除し、新しいタグを使用してリソースを再割り当てします。  
