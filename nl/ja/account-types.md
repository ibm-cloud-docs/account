---

copyright:

  years: 2015, 2018
lastupdated: "2018-08-14"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# アカウント・タイプ
{: #accounts}

{{site.data.keyword.Bluemix}} での構築は無料で開始できます。 規模を拡大する段階になったら、アップグレードし、無料枠を超える使用分のみを支払います。 {{site.data.keyword.Bluemix}} には、ライト・アカウント、従量課金 (PAYG) アカウント、サブスクリプション・アカウント、およびプロモーション・アカウントという 4 つのアカウント・タイプがあります。ニーズに最も適したものを選択してください。
{:shortdesc}

## アカウントの比較
{: #compare}

次の表は、ライト・アカウント、従量課金 (PAYG) アカウント、およびサブスクリプション・アカウントを比較しています。  

|  | ライト  | 従量課金 (PAYG) | 　サブスクリプション |
|--------------------|--------------------|--------------------|--------------------|
| **無料 Cloud Foundry メモリーへのアクセス** | 256 MB | 512 MB | 512 MB |
| **[ライト・サービス・プラン ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window} へのアクセス** | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
| **すべての無料プランへのアクセス** |  | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
| **フルカタログへのアクセス** |  | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
| **時間制限なし** | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
| **保証されたゼロ・コスト** | ![フィーチャー使用可能](../icons/icon_enabled.svg) |  |  |
| **価格交渉** |  |  | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
| **POC の学習または構築に最適** | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |  |
| **実動ユース・ケース向き** |  | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
{: caption="表 1. {{site.data.keyword.Bluemix_notm}} アカウントの比較" caption-side="top"}

## ライト・アカウント
{: #liteaccount}

無料のライト・アカウントに登録すると、「ライト」タグ ![「ライト」タグ](../icons/Lite.svg) 付きで {{site.data.keyword.Bluemix_notm}} コンソールに表示される無料プランを選択できるサービスの探索、およびアプリの作成を行うことができます。 ライト・アカウントには有効期限はなく、クレジット・カードは必要ありません。

`Default` という名前の単一リソース・グループが作成され、それにアクセスできるようになります。 {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) によって管理されるすべてのサービス・インスタンスがこのリソース・グループに自動的に追加されます。 いつでもこのリソース・グループの名前を更新できます。 詳しい手順については、[リソース・グループの名前変更](/docs/admin/resourcegroups.html#renaming-a-resource-group)を参照してください。

各リソース・グループは無料です。 IAM によって管理されるサービスと Cloud Foundry アプリとの間に接続を作成すると、別名が作成されます。これはサービス・インスタンスであり、割り当て量に計上されます。 [別名とは?](/docs/manageapps/connecting_apps.html#what_is_alias) を参照してください。
{: tip}

### プランの内容

ここでは、ライト・アカウントで提供される内容について説明します。 主な特徴は以下のリストのとおりです。

   * アカウントは無料です。クレジット・カードは必要ありません。
   * アカウントには有効期限がありません。
   * 1 つの {{site.data.keyword.Bluemix_notm}} 地域で 1 つの組織を使用できます。
   * 無料の {{site.data.keyword.Bluemix_notm}} サポート。
   * アカウント状況および割り当て量限度に関する E メール通知を受け取ります。
   * Cloud Foundry アプリは 256 MB までの瞬間的ランタイム・メモリーに無料でアクセスできます。
   * 2 CPU と 4 GB の RAM で Kubernetes クラスターでの作業ができます。
   * [{{site.data.keyword.Bluemix_notm}} カタログ ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window} 内のライト・プランがあるどのサービスについても、1 つのインスタンスを保有できます。
   * 開発アクティビティーが行われない状態が 10 日間続くと、アプリはスリープ状態になります。 メモリー割り当て量限度に達することを気にせずに、新規アプリの作業を開始できます。
   * 開発アクティビティーが行われない状態が 30 日間続くと、ライト・プランでのサービス・インスタンスは削除されます。 したがって、新しくインスタンスを作成する前に、非アクティブなインスタンスの削除を管理する必要はありません。

## 有料アカウント
{: #billableacts}

{{site.data.keyword.Bluemix_notm}} の有料プランに登録したり、アカウントのアップグレードを要求したりする際は、4 つの異なる {{site.data.keyword.Bluemix_notm}} アカウントから選択できます。 以下の表に、各種アカウント・タイプとそれらの課金方法を示します。

|アカウント・タイプ |	課金方法 |
|------------------|-----------------------|
|従量課金 (PAYG) |	{{site.data.keyword.Bluemix_notm}} の計算とサービスの使用量に基づいて課金されます。 |
|サブスクリプション | 月々の最小消費量契約に基づいて、月々の割引を受けることができます。 |
| {{site.data.keyword.Bluemix_dedicated_notm}} | 年間契約 |
|{{site.data.keyword.Bluemix_local_notm}} |	年間契約 |
{:caption="表 2. {{site.data.keyword.Bluemix_notm}} の有料アカウントと料金" caption-side="top"}

{{site.data.keyword.Bluemix_notm}} 有料アカウントを SoftLayer アカウントとリンクすると、翌月の最初から、合計した料金が {{site.data.keyword.Bluemix_notm}} 請求書に含まれるようになります。 詳しくは、[「クレジットの表示」](/docs/pricing/viewing_usage.html#credits)を参照してください。
{: tip}

### 「従量課金 (PAYG)」アカウント

従量課金 (PAYG) アカウントを使用すると、複数のリソース・グループを作成して、リソースの集合での割り当て量の管理および有料使用量の表示を簡単に行うことができます。

ランタイムおよびサービスの無料枠が適用されます。 使用量が無料枠を超えると、月次の {{site.data.keyword.Bluemix_notm}} 請求書を受け取ることになります。 請求書は米国ドル (USD) 単位であり、リソースの課金について詳しく示されます。

多くの国および地域では、{{site.data.keyword.Bluemix_notm}} コンソールから従量課金 (PAYG) アカウントに申し込むことができます。 請求情報およびクレジット・カード情報を入力した後、契約条件を受け入れてアカウント要求を送信します。 その後、クレジット・カードが検証されます。 また、アカウント情報の確認の E メールが送信されます。 確認 E メールを受信してから数分たつと、コンソールに戻ってアプリケーションの作成を継続することができます。

お客様の国または地域でオンライン要求を処理できない場合は、[{{site.data.keyword.Bluemix_notm}} サポート ![外部リンク・アイコン](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} のページにリストされているリンクを使用して、{{site.data.keyword.Bluemix_notm}} 営業担当にお問い合わせください。

いつでも、「従量課金 (PAYG)」アカウントを「サブスクリプション」アカウントに切り替えることができます。 [{{site.data.keyword.Bluemix_notm}} サポート ![外部リンク・アイコン](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} ページにリストされているリンクを使用して、{{site.data.keyword.Bluemix_notm}} 営業担当にお問い合わせください。

### 「サブスクリプション」アカウント

サブスクリプション・アカウントを使用すると、複数のリソース・グループを作成して、リソースの集合での割り当て量の管理および有料使用量の表示を簡単に行うことができます。

毎月最小の使用容量に対してコミットし、最小の課金に適用されるサブスクリプションの割引を受けます。 また、最小の使用容量を超過した使用量に対しても料金を支払います。

「サブスクリプション」アカウントの登録、およびサブスクリプション・レートや割引についての詳細は、[{{site.data.keyword.Bluemix_notm}} サポート![外部リンク・アイコン](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window}ページにリストされているリンクを使用して、{{site.data.keyword.Bluemix_notm}} 営業担当にお問い合わせください。

### {{site.data.keyword.Bluemix_dedicated_notm}} アカウント

{{site.data.keyword.Bluemix_dedicated_notm}} を使用するには、以下が含まれている最低 1 年間の契約が必要になります。

   * ご使用のインフラストラクチャーへの VPN 接続
   * {{site.data.keyword.BluSoftlayer_notm}} データ・センター内の完全に冗長な環境
   * サポートされているすべてのランタイム (IBM Java Liberty、Node.js、および標準装備であるオープン・ソースの各ランタイム)
   * 選択したすべての専用サービスおよびすべてのパブリック {{site.data.keyword.Bluemix_notm}} サービス
   * 標準 {{site.data.keyword.Bluemix_notm}} サポート

SoftLayer DirectLink やプレミアム・サポートのオプションなど、オプション項目をオーダーすることもできます。 詳しくは、[{{site.data.keyword.Bluemix_notm}} 営業担当![外部リンク・アイコン](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window}にお問い合わせください。

その期間中の月々の支払額は、希望する専用サービスと、すべてのパブリック・サービスへのアクセス権限を付与するサブスクリプション・アカウントに基づきます。 {{site.data.keyword.Bluemix_notm}} Public のサービスの使用料は、サブスクリプション・アカウントの契約に基づいて計算されます。 サブスクリプション契約の対象ではないサービスを使用した場合には、請求書が送付されます。 契約を開始する場合は、IBM 指定アカウント担当者または [{{site.data.keyword.Bluemix_notm}} 営業担当![外部リンク・アイコン](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window}に連絡してください。

### {{site.data.keyword.Bluemix_local_notm}} アカウント

{{site.data.keyword.Bluemix_local_notm}} を使用するには、以下が含まれている最低 1 年間の契約が必要になります。

   * IBM がローカル・デプロイメントに接続して、自動的に、一貫性を持って配信の更新を有効にする中継といわれるデリバリー機能
   * サポートされているすべてのランタイム (IBM Java Liberty、Node.js、および標準装備であるオープン・ソースの各ランタイム)
   * 選択したすべてのローカル・サービスおよびすべての Public {{site.data.keyword.Bluemix_notm}} サービスへのアクセス
   * 標準 {{site.data.keyword.Bluemix_notm}} サポート

その期間中の月々の支払額は、希望するローカル・サービスと、すべてのパブリック・サービスへのアクセス権限を付与するサブスクリプション・アカウントに基づきます。 {{site.data.keyword.Bluemix_notm}} Public のサービスの使用料は、サブスクリプション・アカウントの契約に基づいて計算されます。 サブスクリプション契約の対象ではないサービスを使用した場合には、請求書が送付されます。 契約を開始する場合は、IBM 指定アカウント担当者または [{{site.data.keyword.Bluemix_notm}} 営業担当![外部リンク・アイコン](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window}に連絡してください。

## プロモーション・アカウント
{: #promo}

特別なプロモーションの一部として時々提供されるプロモーション・アカウントは、{{site.data.keyword.Bluemix_notm}} カタログのほとんどにアクセスできる、期限を設けた無料のトライアル・アカウントです。 このアカウント・タイプは、プロモーション・コードの使用を通じてのみ使用可能です。 このアカウントの有効期間は、プロモーションによって異なります。

プロモーション・アカウントでは、ユーザーのために作成され、`Default` と命名された単一リソース・グループにアクセスできます。 IAM によって管理されるすべてのサービス・インスタンスがこのリソース・グループに自動的に追加されます。 いつでもこのリソース・グループの名前を更新できます。 詳しい手順については、[リソース・グループの名前変更](/docs/admin/resource-groups.html#renaming-a-resource-group)を参照してください。

各リソース・グループは無料です。 IAM によって管理されるサービスと Cloud Foundry アプリとの間に接続を作成すると、別名が作成されます。これはサービス・インスタンスであり、割り当て量に計上されます。 [別名とは?](/docs/manageapps/connecting_apps.html#what_is_alias) を参照してください。
{: tip}

### プロモーション・アカウントの有効期限が切れたらどうなりますか?
{: #trialend}

プロモーション・アカウントの有効期限が切れると、ご使用のアカウント内のアプリが停止されます。 {{site.data.keyword.Bluemix_notm}} アカウントにもう一度登録することはできませんが、ご使用のアカウントおよび招待されたアカウントには引き続きアクセスできます。

アプリを再開するには、アカウントを有料アカウントに切り替えるため、従量課金 (PAYG) アカウントのクレジット・カード情報を指定するか、または、サブスクリプション・アカウントを作成します。 それにより、計算とサービスの無料枠を引き続きご使用いただけます。 毎月の無料枠に含まれないサービス、コンテナー、およびランタイムの使用量についてのみお支払いただきます。

プロモーション・アカウントの有効期限が切れた後にアカウントを変換しない場合、ご使用のアプリとサービスは 30 日後に削除されます。 ただし、アカウントは削除されず、ユーザーはいつでもログインして、有料アカウントにアップグレードすることができます。 また、有料アカウントを作成して、アプリの設定およびサービス構成を失わないよう注意をうながす E メール通知を受け取ります。 {{site.data.keyword.Bluemix_notm}} から通知を受け取りたくない場合は、いつでもアンサブスクライブできます。

アカウントを切り替えた場合、無料枠は、各サービスにより通常提供される枠内に制限されます。 無料枠は、無料トライアル期間中に IBM サービスの多くが提供する無制限の使用ではなくなります。
