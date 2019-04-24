---

copyright:
  years: 2015, 2019
lastupdated: "2019-03-19"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account, subscription, service bundle

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# アカウント・タイプ
{: #accounts}

{{site.data.keyword.Bluemix_notm}} には、ライト・アカウント、従量課金 (PAYG) アカウント、およびサブスクリプション・アカウントという 3 つのアカウント・タイプがあります。 無料のライト・アカウントは、登録するとすぐに取得できます。 従量課金 (PAYG) アカウントとサブスクリプション・アカウントは有料のオプションであり、それぞれ異なる機能を提供します。 各アカウントを比較して、ニーズに最も適したものを選択してください。
{:shortdesc}

## アカウントの比較
{: #compare}

次の表は、ライト・アカウント、従量課金 (PAYG) アカウント、およびサブスクリプション・アカウントを比較しています。 各アカウントについて詳しくは、以降のセクションを参照してください。

|                                         | ライト               | 従量課金 (PAYG)      | サブスクリプション       |
|-----------------------------------------|--------------------|--------------------|--------------------|
| **無料 Cloud Foundry メモリーへのアクセス** | 256 MB             | 512 MB             | 512 MB             |
| **[ライト・サービス・プラン ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://{DomainName}/catalog/?search=label:lite){: new_window} へのアクセス** | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
| **すべての無料プランへのアクセス**            |                    | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
| **フル {{site.data.keyword.Bluemix_notm}} カタログへのアクセス** |  | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
| **複数の Cloud Foundry 地域へのアクセス** |               | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
| **時間制限なし** | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
| **保証されたゼロ・コスト**                | ![フィーチャー使用可能](../icons/icon_enabled.svg) |  |         |
| **割引価格**                  |                    |                    | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
| **PoC (概念検証) の学習または構築に最適** | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |  |
| **実動ユース・ケース向き**        |                    | ![フィーチャー使用可能](../icons/icon_enabled.svg) | ![フィーチャー使用可能](../icons/icon_enabled.svg) |
{: caption="表 1. {{site.data.keyword.Bluemix_notm}} アカウントの比較" caption-side="top"}


## ライト・アカウント
{: #liteaccount}

「ライト」タグ ![「ライト」タグ](../icons/Lite.svg) 付きで {{site.data.keyword.Bluemix_notm}} コンソールに表示される無料ライト・プランを選択してアプリの作成とサービスの探索を開始するには、ライト・アカウントを申し込みます。 ライト・アカウントには有効期限はなく、クレジット・カードは必要ありません。

`Default` という名前の単一リソース・グループが作成され、それにアクセスできるようになります。 {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) によって管理されるすべてのサービスのインスタンスがこのリソース・グループに自動的に追加されます。 いつでもこのリソース・グループの名前を更新できます。 詳しい手順については、[リソース・グループの名前変更](/docs/resources?topic=resources-rgs#rename_rgs)を参照してください。

各リソース・グループは無料です。 IAM によって管理されるサービスと Cloud Foundry アプリとの間に接続を作成すると、別名が作成されます。これはサービス・インスタンスであり、割り当て量に計上されます。 [接続の管理](/docs/resources?topic=resources-connect_app)を参照してください。
{: tip}

### プランの内容
{: #lite-account-features}

ライト・アカウントの主な特徴は次のリストのとおりです。

   * アカウントは無料です。クレジット・カードは必要ありません。
   * アカウントには有効期限がありません。
   * 1 つの {{site.data.keyword.Bluemix_notm}} 地域で 1 つの組織を使用できます。
   * 基本的な {{site.data.keyword.Bluemix_notm}} のサポートを無料で受けられます。 基本サポートは、従来の重大度が使用されず、特定の応答時間が要求されない非実稼働環境またはワークロードに対して提供されます。
   * アカウント状況および割り当て量限度に関する E メール通知を受け取ります。
   * Cloud Foundry アプリは、1 カ月当たり 256 MB までの瞬間的ランタイム・メモリーに無料でアクセスできます。
   * [{{site.data.keyword.Bluemix_notm}} カタログ ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} 内のライト・プランがあるどのサービスについても、1 つのインスタンスをプロビジョンできます。
   * 開発アクティビティーが行われない状態が 10 日間続くと、アプリはスリープ状態になります。 アプリの作業を続行すると、アプリをウェイクアップできます。
   * 開発アクティビティーが行われない状態が 30 日間続くと、ライト・プランでのサービス・インスタンスは削除されます。

## 「従量課金 (PAYG)」アカウント
{: #paygo}

従量課金 (PAYG) アカウントを使用すると、すべての無料プランを含む {{site.data.keyword.Bluemix_notm}} カタログ全体にアクセスでき、1 カ月当たり 2 倍の 512 MB の無料ランタイム・メモリーを取得します。 長期の契約や確約なしに、使用した有料サービスに対してのみお支払いいただきます。

複数のリソース・グループを作成して、リソースの集合での割り当て量の管理および有料使用量の表示を簡単に行うことができます。 {{site.data.keyword.Bluemix_notm}} の計算とサービスの使用量に基づいて課金されます。 使用量がランタイムおよびサービスの無料枠を超えると、リソースの課金の詳細を示す月次請求書を受け取ることになります。

また、従量課金 (PAYG) アカウントでは、拡張サポート・プランやプレミアム・サポート・プランを発注して、実稼働のワークロードに関する追加のヘルプを利用することができます。 詳しくは、『[サポート・プラン](/docs/get-support?topic=get-support-support-plans)』を参照してください。

## 「サブスクリプション」アカウント
{: #subscription-account}

サブスクリプション・アカウントを使用すると、複数のリソース・グループを作成して、リソースの集合での割り当て量の管理および有料使用量の表示を簡単に行うことができます。 毎月の最小消費量を確約すると、最低料金に適用されるサブスクリプションの割引を受けます。

例えば、6 カ月の間、1 カ月に $100 分を消費することを確約すると、10% の割引を受けることができます。 このサブスクリプション期間中は、$600 分の使用量を得ることができますが、お支払いは $540 のみになります。 サブスクリプション期間が長くなるほど、多くの割引を受けることになります。

使用量はサブスクリプションの合計量から差し引かれます。 使用量が月ごとに変化する場合でも、予測可能で一貫性のある請求になります。 使用量がサブスクリプションの合計量を超えた場合は、超過分に対して割引なしのレートで課金されます。

従量課金 (PAYG) アカウントと同様に、サブスクリプション・アカウントでは、拡張サポート・プランやプレミアム・サポート・プランを発注して、必要な場合に追加のヘルプを利用することができます。 詳しくは、『[サポート・プラン](/docs/get-support?topic=get-support-support-plans)』を参照してください。

サブスクリプション・アカウントを使用している場合、[{{site.data.keyword.Bluemix_notm}} カタログ](https://{DomainName}/catalog){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") から使用可能なほとんどのサービスを作成できます。 ただし、いくつかのサービスでは、個別に購入する必要のある特定の料金プランが使用されています。

### サービス・バンドル・サブスクリプション
{: #service-subscriptions}

サービス・バンドル・サブスクリプションは、特定のドメイン内のよく利用されるユース・ケースをターゲットとした一連のサービスに対するアクセス権限とクレジットを提供します。 AI、分析、{{site.data.keyword.blockchainfull_notm}}、Internet of Things (IoT)、およびクラウド・ネイティブの各サービスにわたるサービス・バンドルから選択することができます。 ニーズが複数のドメインにまたがる場合は、複数のサービス・バンドル・サブスクリプションを発注することができます。

サービス・バンドルは、ライト・アカウントを含むすべてのタイプの既存アカウントに追加することができます。 最初の 90 日間、使用するサービスはバンドル内のサービスに限定されます。 最初の 90 日が経過した後は、カタログ全体にアクセスできます。 サービス・バンドル・サブスクリプションには、[{{site.data.keyword.Bluemix_notm}} サービス記述書](/docs/overview/terms-of-use?topic=overview-terms)のご利用条件が適用されます。

サービス・バンドル・サブスクリプションは、{{site.data.keyword.Bluemix_notm}} コンソールからはご利用になれません。 サービス・バンドルの詳細と購入については、[{{site.data.keyword.Bluemix_notm}} 営業担当員 ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} にお問い合わせください。
{:tip}

サービス・バンドル・サブスクリプションの購入後は、アカウントにバンドルを追加するために適用するフィーチャー・コードが記載された E メールを受信します。 フィーチャー・コードの適用方法について詳しくは、『[フィーチャー・コードの適用](/docs/account?topic=account-codes)』を参照してください。 サービス・バンドルが期限切れになった場合、またはすべてのクレジットを使用した場合は、使用量が従量課金 (PAYG) のレートで課金されるようにした状態で、どのサービスでも継続して使用することができます。

### {{site.data.keyword.Bluemix_dedicated_notm}} アカウント
{{site.data.keyword.Bluemix_dedicated_notm}} を使用するには、以下が含まれている最低 1 年間の契約が必要になります。

   * ご使用のインフラストラクチャーへの VPN 接続
   * {{site.data.keyword.BluSoftlayer_notm}} データ・センター内の完全に冗長な環境
   * サポートされているすべてのランタイム ({{site.data.keyword.runtime_liberty_short}}、{{site.data.keyword.runtime_nodejs_short}}、および標準装備であるオープン・ソースの各ランタイム)
   * 選択したすべての専用サービスおよびすべてのパブリック {{site.data.keyword.Bluemix_notm}} サービス
   * 標準 {{site.data.keyword.Bluemix_notm}} サポート

{{site.data.keyword.BluDirectLink}} や、拡張サポートまたはプレミアム・サポートのオプションなど、オプション項目を注文することもできます。 詳しくは、[{{site.data.keyword.Bluemix_notm}} 営業担当](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg) にお問い合わせください。

その期間中の月々の支払額は、希望する専用サービスと、すべてのパブリック・サービスへのアクセス権限を付与するサブスクリプション・アカウントに基づきます。 {{site.data.keyword.Bluemix_notm}} Public のサービスの使用料は、サブスクリプション・アカウントの契約に基づいて計算されます。 サブスクリプション契約の対象ではないサービスを使用した場合には、請求書が送付されます。 契約を開始する場合は、IBM 指定アカウント担当者または [{{site.data.keyword.Bluemix_notm}} 営業担当](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg) に連絡してください。

## アカウントのアップグレード
{: #upgrade-lite-account}

ご使用のアカウントを次のレベルに進める準備ができたら、ライト・アカウントを従量課金 (PAYG) アカウントまたはサブスクリプション・アカウントに[アップグレード](/docs/account?topic=account-upgrading-account)することができます。 アカウントをアップグレードすると、{{site.data.keyword.Bluemix_notm}} カタログ全体のロックの解除や、無料の追加リソースの提供などが行われます。

ライト・アカウントを従量課金 (PAYG) アカウントにアップグレードすると、$200 のプロモーション・クレジットを取得し、そのクレジットが自動的にアカウントに適用されます。 この $200 分のクレジットは 30 日間有効であり、クレジットの容量から使用量が自動的に差し引かれます。 このクレジットを、サード・パーティーのオファリングで使用することはできません。また、一部のアカウントではクレジットを使用できない場合があります。

すでに従量課金 (PAYG) アカウントまたはサブスクリプション・アカウントを使用している場合は、別のタイプのアカウントに切り替えることもできます。 詳しくは、『[アカウントのアップグレード](/docs/account?topic=account-upgrading-account)』を参照してください。
