---

copyright:
  years: 2018, 2019
lastupdated: "2019-03-20"

keywords: GDPR, HIPAA, data security, PHI, account settings, europe

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 「EU サポート対象」および「HIPAA サポートあり」設定の有効化
{: #eu-hipaa-supported}

アカウント所有者は、アカウントで「EU サポート対象」および「HIPAA サポートあり」を有効にすることができます。 例えばヨーロッパ市民の個人データを処理するためにリソースを使用する場合などに、「EU サポート対象」設定を有効にすることを選択できます。 HIPAA 対応サービスに Protected Health Information (PHI) を組み込むことを計画している場合は、「HIPAA サポートあり」設定を有効にすることを選択できます。
{:shortdesc}


## 「EU サポート対象」設定の有効化
{: #bill_eusupported}

「EU サポート対象」設定を有効にすると、レベル 1 およびレベル 2 のサポートは EU 域内の {{site.data.keyword.Bluemix_notm}} サポート・チーム・メンバーによって提供されるように制限されます。 ただし、{{site.data.keyword.Bluemix_notm}} 処理アクティビティーは、EU 域外のチームによって実行される場合があります。 問題が EU のレベル 1 またはレベル 2 のサポート・チームでは解決されない場合は、グローバル・チームに連絡が行くこともあります。 グローバル・チームへの連絡は、必ず EU サポート・チームの指示の下で、お客様のデータのセキュリティーやプライバシーに影響しない場合に限って行われます。

この設定を有効にすることで、EU サポート対象サービスでは厳しいアクセス制御が有効になり、お客様が保管および処理するデータは EU 域内の IBM サポート・チームによってのみアクセスおよび制御されることが確実になります。 ヨーロッパ域外の {{site.data.keyword.Bluemix_notm}} 専門家がこのデータにアクセスする必要がある場合は、EU サポート・チーム・メンバーによってアクセス要求が審査されます。 EU サポート・チーム・メンバーはグローバル・クラウドの専門家に対して、要求があったシステムのみを対象に、特定の時間フレームに限って、必要なアクセスを許可します。その時間が経過した後、アクセス権限は取り消されます。 このプロセスの初めから終わりまで、お客様のデータは常に保護されます。

  1. {{site.data.keyword.Bluemix_notm}} コンソールで、**「管理」 > 「アカウント」**と進み、**「アカウント設定」**を選択します。
  2. **「オン」**をクリックします。
  3. 設定の有効化についての説明を読み、**「これらの条件を理解し、同意します」**を選択します。
  4. **「オン」**をクリックします。

   「EU サポートあり」設定を有効にした後、「EU サポートあり」タグを使用して、EU がサポートしているプランのあるオファリングのカタログを検索できます。


## 「HIPAA サポートあり」設定の有効化
{: #enabling-hipaa}

米国における医療保険の積算と責任に関する法律 (HIPAA) と経済的および臨床的健全性のための医療情報技術 (HITECH) に関する法律は、電子的な医療トランザクションおよび情報の取り扱いの標準を定めています。 お客様またはお客様の会社が HIPAA が定める適用対象事業体である場合、HIPAA および HITECH 法によって規定されている機密性の高いワークロードを実行する場合は、「HIPAA サポートあり」設定を有効にする必要があります。 {{site.data.keyword.Bluemix_notm}} コンプライアンスについて詳しくは、『[Compliance on the {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud/compliance){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン ")』を参照してください。

この設定を有効にすると、次の影響があります。

* カタログで HIPAA 対応サービスをフィルター処理できるようになります
* ご使用のアカウントに保護医療情報 (PHI) が保管されていることが IBM に示されます
* 適用対象事業体に対する IBM Business Associate Addendum (BAA) にデジタル処理で同意します

この設定は、お客様またはお客様の会社が HIPAA が定める適用対象事業体である場合にのみ有効にしてください。 お客様またはお客様の会社が適用対象事業体の事業提携者の場合は、[{{site.data.keyword.Bluemix_notm}} 営業担当員](https://www.ibm.com/account/reg/us-en/signup?formid=MAIL-wcp){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") にお問い合わせいただき、該当する BAA に同意してください。 適用対象事業体および事業提携者の HIPAA 定義について詳しくは、『[US Department of Health & Human Services](https://www.hhs.gov/hipaa/for-professionals/covered-entities/index.html){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")』Web サイトを参照してください。
{: important}

「HIPAA サポートあり」設定を有効にしたアカウントは、サービスのカタログ全体に引き続きアクセスできます。{{site.data.keyword.Bluemix_notm}} サービスでは通常、複数のプランが提供されます。 サービスの「HIPAA 使用可能」ラベルは、使用可能なすべてのプランに適用することも、特定のプランまたは構成に制限することもできます。 お客様は、PHI を HIPAA 対応オファリング・プランに制限すること、および HIPAA および HITECH に準拠して設計を行うことに関して一切の責任を負うものとします。

1. コンソールで、**「管理」 > 「アカウント」**と進み、**「アカウント設定」**を選択します。
2. 「HIPAA サポートあり」オプションに対して、**「オン」**をクリックします。
3. この設定の有効化に関する説明を読みます。

  設定を有効にした後に、無効にすることはできません。
  {: note}

4. **「同意する」**を選択し、**「送信」**をクリックします。

  「HIPAA サポートあり」設定を有効にした後、「HIPAA 使用可能」タグを使用して、HIPAA 対応になっているオファリングのカタログを検索できます。
