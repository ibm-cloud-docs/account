---

copyright:

  years: 2016, 2018

lastupdated: "2018-03-05"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# IBM ID への切り替えとアカウントのリンク
{: #unifyingaccounts}

SoftLayer での認証は、IBM ID を使用して {{site.data.keyword.Bluemix}} のすべてに対して単一のログインを提供するようになりました。 IBM ID は、{{site.data.keyword.Bluemix_notm}} アカウントにログインして、インフラストラクチャー、サービス、およびアプリケーション機能のアクセスおよび購入に使用できる単一 ID です。 すべての新しいアカウントは自動的に IBM ID を受け取り、SAML フェデレーテッド・アカウントを除く既存の SoftLayer アカウントは IBM ID 認証に切り替えることができます。
{:shortdesc}

## IBM ID への切り替え
{: #switchtoIBMid}

IBM ID への切り替えを開始しても、処理が完了する前であればいつでも切り替えを取り消すことができます。 ただし、ログインするたびに、IBM ID への切り替えを促すプロンプトが表示されます。 {{site.data.keyword.Bluemix_notm}} アカウントにリンクする予定の各 SoftLayer アカウントは、固有の E メール・アドレスを持つ固有の IBM ID によって所有される必要があります。

既存の SoftLayer アカウントを IBM ID に切り替えるには、IBM ID を作成し、次に登録コードを使用してその ID を確認します。

### IBM ID および登録コードの要求
{: #reqIBMidandregcode}

1. SoftLayer アカウントにログインし、IBM ID への切り替えを促すプロンプトが表示されたら、**「OK」**をクリックします。

   マスター・ユーザーであって、{{site.data.keyword.BluSoftlayer_full}} インフラストラクチャーのカスタマー・ポータルに IBM ID への切り替えを求めるプロンプトが表示されない場合は、IBM サポートにお問い合わせください。サポートへの問い合わせについて詳しくは、[IBM サポート](/docs/get-support/howtogetsupport.html#getting-customer-support)を参照してください。

   既にログインしており、プロンプトに対して**「後で」**をクリックしたものの、IBM ID 認証への切り替えを現行セッションで行うことにした場合は、「ユーザー・プロファイルの編集」ページに移動し、**「IBM ID への切り替え」**をクリックします。

2. ウィザードのプロンプトに従って IBM ID を作成します。

   どの IBM ID でも現在使用されていない E メール・アドレスを入力します。 この E メール・アドレスは、新規 IBM ID のユーザー名として使用され、IBM ID の作成後に登録コードが送信される宛先となります。 IBM ID に関連付けられている E メール・アドレスは後で更新できますが、ユーザー名は変更できません。

### 登録コードを使用した IBM ID の確認
{: #confIBMiduseregcode}

1. 登録コードを受信したら、E メールのリンクをクリックするか、URL をブラウザーにコピーして、登録コードを入力します。

   コードは 7 日間有効で、1 回のみ使用できます。

2. 登録コードを送信した後、IBM ID を使用してカスタマー・ポータルにログインします。

   「アカウントのログイン」プロンプトで、**「IBM ID アカウントでのログイン」**セクションに移動し、**「IBM ID でログイン」**をクリックします。 以前に SoftLayer ID で使用していた**「ユーザー名」**と**「パスワード」**のフィールドは使用しないでください。

新規のお客様の場合、注文を清算する際、既存の IBM ID を入力するか、新規 IBM ID を作成するよう求められます。
  * 既存の IBM ID を使用するには、ユーザー名を入力するか、または IBM ID の E メール・アドレスが固有の場合 (つまり、複数の IBM ID 間で共有されていない場合) は E メール・アドレスを入力します。
  * 新規 IBM ID を作成するには、どの IBM ID でも現在使われていない E メール・アドレスを入力します。 この E メール・アドレスは、IBM ID のユーザー名であり、IBM ID の作成後に登録コードが送信される宛先となります。 IBM ID に関連付けられている E メール・アドレスは後で更新できますが、ユーザー名を変更することはできません。

IBM ID でのログインに関する問題を解決するには、『[{{site.data.keyword.Bluemix_notm}} へのアクセスに関するトラブルシューティング](/docs/troubleshoot/ts_accessing.html#accessing)』を参照してください。

## IBM ID ユーザー・アカウントのリンク
{: #link_user_accounts}

ユーザー・アカウントを IBM ID 認証に切り替えた後、販売店および流通業者は SoftLayer アカウントと {{site.data.keyword.Bluemix_notm}} アカウントをリンクして、Infrastructure as a Service (IaaS) リソースと Platform as a Service (PaaS) リソースを組み合わせて使用できるようになります。その後、1 回のログインで、{{site.data.keyword.BluSoftlayer_full}} インフラストラクチャーのカスタマー・ポータルから IaaS リソースに、また、{{site.data.keyword.Bluemix_notm}} コンソールから PaaS リソースにアクセスできます。アカウントをリンクすると、使用するすべての PaaS リソースおよび IaaS リソースに対する単一の請求書も提供されます。

アカウントをリンクするには、SoftLayer マスター・ユーザーでなければなりません。 アカウントのマスター・ユーザーである IBM ID は、リンクする先の {{site.data.keyword.Bluemix_notm}} プラットフォーム・アカウントの所有者でなければなりません。 アカウントをリンクするには、必ず、以下の重要な注意事項を確認してください。

  * リンクされる SoftLayer アカウントのマスター・ユーザーは、IBM ID を持っていなければなりません。
  * {{site.data.keyword.Bluemix_notm}} アカウントにリンクする各ユーザー・アカウントは、固有の E メール・アドレスを持つ固有の IBM ID によって所有される必要があります。 単一の IBM ID が複数の SoftLayer アカウントを所有することは可能ですが、マスター・ユーザーを、アカウントごとに固有の IBM ID となるように変更する必要があります。 SoftLayer アカウントのマスター・ユーザーを変更するには、サポートに連絡してください。 詳しくは、『[{{site.data.keyword.Bluemix_notm}} インフラストラクチャーのサポートの利用](/docs/customer-portal/cpsupport.html)』を参照してください。
  * リンクされたアカウントに新規ユーザーを追加する場合、ユーザーを SoftLayer アカウントと {{site.data.keyword.Bluemix_notm}} アカウントの両方に追加して、統合されたコンソールのすべての機能にアクセスできるようにする必要があります。
  * ブランド・アカウントを持っていて、Brand Agent Portal (BAP) を使用している場合、アカウントのリンクにサポートが必要であれば、softlayer_revenue_services_team@wwpdl.vnet.ibm.com に E メールを送信して、Revenue Services チームに連絡してください。
  * {{site.data.keyword.Bluemix_notm}} でリンクされるアカウントはすべて、従量課金 (PAYG) アカウントでなければなりません。 新しい従量課金 (PAYG) アカウントを作成するか、既存の従量課金 (PAYG) アカウントをリンクするか、または既存のトライアル・アカウントをリンクできます (既存のトライアル・アカウントは、従量課金 (PAYG) アカウントにアップグレードされます)。 {{site.data.keyword.Bluemix_notm}} サブスクリプション・アカウントにリンクすることはできません。

各 SoftLayer アカウントを既存の {{site.data.keyword.Bluemix_notm}} プラットフォーム・アカウントにリンクしたり、新規のアカウントを作成したりするには、以下の手順を実行します。

   1. マスター・ユーザー・アカウントの IBM ID を使用して、{{site.data.keyword.BluSoftlayer_full}} インフラストラクチャーのカスタマー・ポータルにログインします。
   2. {{site.data.keyword.Bluemix_notm}} インフラストラクチャーのカスタマー・ポータルで、**「Bluemix アカウントのリンク (Link a Bluemix Account)」**をクリックします。
   3. SoftLayer アカウントと {{site.data.keyword.Bluemix_notm}} アカウントをリンクする場合のご利用条件を読み、同意します。
   4. SoftLayer アカウントのユーザーを {{site.data.keyword.Bluemix_notm}} アカウントに追加する操作も含めて、ウィザードのプロンプトに従います。
   5. プロンプトが表示されたら、次のいずれかの操作を行います。
     * 既に {{site.data.keyword.Bluemix_notm}} アカウントを持っている場合は、そのアカウントに関連付けられている E メール・アドレスを入力して、アカウントをリンクします。
     * {{site.data.keyword.Bluemix_notm}} アカウントを持っていない場合は、使用する E メール・アドレスを指定し、{{site.data.keyword.Bluemix_notm}} への招待の手順に従ってアカウントを作成します。
   6. アカウントをリンクした後、各アカウントのエンド・ユーザーに通知して、前述の [IBM ID への切り替え](/docs/account/softlayerlink.html#switchtoIBMid)セクションに説明されている手順に従って IBM ID にマイグレーションするように指示します。

エンド・ユーザー・アカウントのみを IBM ID にマイグレーションしてください。 ブランド・アカウント (エンド・ユーザー・アカウントの親アカウントであり、リソースを含んでいない) はマイグレーションしないでください。 ブランド・アカウント・ユーザーは、IBM ID にマイグレーションすると、Brand Agent Portal (BAP) にログインできなくなります。
{: tip}

リンクされたアカウントは、[{{site.data.keyword.Bluemix}} コンソール ![外部リンク・アイコン](../icons/launch-glyph.svg)](https://console.bluemix.net){: new_window} にログインします。

また、アカウントがリンクされると、次のように変わることに注意してください。
  * SoftLayer と {{site.data.keyword.Bluemix_notm}} アカウントの両方にアクセスするために、IBM ID 資格情報を使用する必要があります。
  * 既存の SoftLayer 割引は、{{site.data.keyword.Bluemix_notm}} の料金全体に適用されます。
  * 米国ドル (USD) 単位の 1 つの請求書を受け取ります。 既存の {{site.data.keyword.Bluemix_notm}} アカウントがある場合、インフラストラクチャー・リソースに対する {{site.data.keyword.Bluemix_notm}} からの請求は、両方のアカウントをリンクした後に開始される新しい請求処理サイクルで有効になります。
  * インフラストラクチャー・リソースの使用量は、{{site.data.keyword.Bluemix_notm}} コンソールでモニターできます。

アカウントをリンクした後は、リンクを解除することはできません。
{: tip}

## リンクされたアカウントでの多要素認証の使用法
{: #2fa}

リンクされたアカウントを持っている場合、ID およびアクセスの**「設定」**ページを使用して、ご使用のアカウントで多要素認証認証を有効にすることができます。 これは、一般的に 2 要素認証 (2FA) とも呼ばれ、標準的な必須の IBM ID とパスワード以外の認証要素を使用してアカウントにアクセスするためのセキュリティー層を追加します。 ご使用のアカウントの多要素認証は、リンクされている {{site.data.keyword.Bluemix_notm}} アカウント内のすべてのリソースに適用されます。 ご使用のアカウントで有効になっている場合は、そのアカウントに追加されているすべてのユーザーにも適用されます。

多要素認証は、IBM ID ごとには行われません。 従来どおり、アカウント単位です。 IBM ID が複数のアカウントに関連付けられていて、アカウント間で切り替えを行う場合、2 要素認証を必要とする別のアカウントに切り替えるたびに ID を確認する必要があります。 これは、前のアカウントと新しいアカウントが両方とも同じ 2 要素認証メカニズムを使用して構成されている場合でも同じです。
