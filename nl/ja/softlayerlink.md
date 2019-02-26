---

copyright:

  years: 2016, 2019

lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# IBM ID への切り替えとアカウントのリンク
{: #unifyingaccounts}

IBM ID は、{{site.data.keyword.Bluemix}} アカウントにログインして、インフラストラクチャー、サービス、およびアプリケーション機能のアクセスおよび購入に使用できる単一 ID です。 すべての新しいアカウントは自動的に IBM ID を受け取り、SAML フェデレーテッド・アカウントを除く既存の SoftLayer アカウントは IBM ID 認証に切り替えることができます。
{:shortdesc}

## IBM ID への切り替え
{: #switchtoIBMid}

IBM ID への切り替えを開始しても、処理が完了する前であればいつでも切り替えを取り消すことができます。 ただし、ログインするたびに、IBM ID への切り替えを促すプロンプトが表示されます。 {{site.data.keyword.Bluemix_notm}} アカウントにリンクする予定の各 SoftLayer アカウントは、固有の E メール・アドレスを持つ固有の IBM ID によって所有される必要があります。

既存の SoftLayer アカウントを IBM ID に切り替えるには、IBM ID を作成し、次に登録コードを使用してその ID を確認します。

### IBM ID および登録コードの要求
{: #reqIBMidandregcode}

1. SoftLayer アカウントにログインし、IBM ID への切り替えを促すプロンプトが表示されたら、**「OK」**をクリックします。

   マスター・ユーザーであって、IBM ID への切り替えを促すプロンプトがカスタマー・ポータルに表示されない場合、IBM サポートに連絡して支援を依頼してください。 サポートへの問い合わせについて詳しくは、『[サポートの利用](/docs/get-support?topic=get-support-getting-customer-support)』を参照してください。

   既にログインしており、プロンプトに対して**「後で」**をクリックしたものの、IBM ID 認証への切り替えを現行セッションで行うことにした場合は、「ユーザー・プロファイルの編集」ページに移動し、**「IBM ID への切り替え」**をクリックします。

2. ウィザードのプロンプトに従って IBM ID を作成します。

   どの IBM ID でも現在使用されていない E メール・アドレスを入力します。 この E メール・アドレスは、新規 IBM ID のユーザー名として使用され、IBM ID の作成後に登録コードが送信される宛先となります。 IBM ID に関連付けられている E メール・アドレスは後で更新できますが、ユーザー名は変更できません。

### 登録コードを使用した IBM ID の確認
{: #confIBMiduseregcode}

1. 登録コードを受信したら、E メールのリンクをクリックするか、URL をブラウザーにコピーして、登録コードを入力します。 コードは 7 日間有効で、1 回のみ使用できます。

2. 登録コードを送信した後、IBM ID を使用してカスタマー・ポータルにログインします。

   「アカウントのログイン」プロンプトで、**「IBM ID アカウントでのログイン」**セクションに移動し、**「IBM ID でログイン」**をクリックします。 以前に SoftLayer ID で使用していた**「ユーザー名」**と**「パスワード」**のフィールドは使用しないでください。

新規のお客様の場合、注文を清算する際、既存の IBM ID を入力するか、新規 IBM ID を作成するよう求められます。
  * 既存の IBM ID を使用するには、その IBM ID のユーザー名または E メール・アドレスを入力します (それが複数の IBM ID 間で共有されていない場合)。
  * 新規 IBM ID を作成するには、どの IBM ID でも現在使われていない E メール・アドレスを入力します。 この E メール・アドレスは、IBM ID のユーザー名であり、IBM ID の作成後に登録コードが送信される宛先となります。 IBM ID に関連付けられている E メール・アドレスは後で更新できますが、ユーザー名を変更することはできません。

IBM ID でのログインに関する問題を解決するには、[{{site.data.keyword.Bluemix_notm}} へのアクセスに関するトラブルシューティング](/docs/account?topic=account-accessing)を参照してください。


## IBM ID アカウントのリンク
{: #link_accounts}

アカウントを IBM ID アカウントに切り替えた後、Infrastructure as a Service (IaaS) リソースと Platform as a Service (PaaS) リソースを組み合わせて使用するために、SoftLayer アカウントと {{site.data.keyword.Bluemix_notm}} アカウントをリンクできます。 その後、単一のログインから IaaS リソースと PaaS リソースにアクセスできます。 アカウントをリンクすると、使用するすべての PaaS リソースおよび IaaS リソースに対する単一の請求書も提供されます。 自分自身のアカウントをリンクするか、マスター・ユーザーの場合は、複数のユーザー・アカウントをリンクできます。

### IBM ID アカウントのリンク
{: #link_user_account}

クラシック・インフラストラクチャーのカスタマーであり、{{site.data.keyword.Bluemix_notm}} 内に PaaS アカウントも持っているか作成した場合は、それらのアカウントを単一のビューで表示できるように IaaS と PaaS をリンクできます。 複数のアカウントをリンクするには、以下の手順を使用します。
1. SoftLayer アカウントにログインします。
2. 「アカウント要約」ページで、**「新規! Bluemix アカウントをリンクします」**をクリックします。
3. ご利用条件を検討し、クリックして受け入れることを確認します。
4. アカウントのセットアップ方法に応じて、以下のいずれかの最終ステップを実行します。
  * IBM ID に {{site.data.keyword.Bluemix_notm}} アカウントが関連付けられている場合は、許可ページに誘導されてから、再び最終確認ステップに誘導されます。
  * {{site.data.keyword.Bluemix_notm}} アカウントに関連付けられていない場合は、新しいアカウントを作成するよう求めるプロンプトが出されます。

アカウントのリンクに関する一般的な質問と回答を表示するには、[FAQ](/docs/account?topic=account-al_login) を確認します。

### IBM ID ユーザー・アカウントのリンク
{: #link_customer_accounts}

お客様のユーザー・アカウントが IBM ID 認証に切り替えられた後、販売店および流通業者は、自分たちのユーザー・アカウントをリンクすることができます。 カスタマー・アカウントをリンクするには、SoftLayer マスター・ユーザーでなければなりません。 アカウントのマスター・ユーザーである IBM ID は、リンクする先の {{site.data.keyword.Bluemix_notm}} プラットフォーム・アカウントの所有者でなければなりません。

アカウントをリンクした後は、リンクを解除することはできません。
{: note}

アカウントのリンクについての以下の重要な注意事項を必ず確認してください。

  * リンクされる SoftLayer アカウントのマスター・ユーザーは、IBM ID を持っていなければなりません。
  * {{site.data.keyword.Bluemix_notm}} アカウントにリンクする各ユーザー・アカウントは、固有の E メール・アドレスを持つ固有の IBM ID によって所有される必要があります。 単一の IBM ID が複数の SoftLayer アカウントを所有することは可能ですが、マスター・ユーザーを、アカウントごとに固有の IBM ID となるように変更する必要があります。 SoftLayer アカウントのマスター・ユーザーを変更するには、サポートに連絡してください。 詳しくは、[{{site.data.keyword.Bluemix_notm}} インフラストラクチャーのサポートの利用](/docs/customer-portal?topic=customer-portal-customerportal_support)を参照してください。
  * リンクされたアカウントに新規ユーザーを追加する場合、ユーザーを SoftLayer アカウントと {{site.data.keyword.Bluemix_notm}} アカウントの両方に追加して、統合されたコンソールのすべての機能にアクセスできるようにする必要があります。
  * ブランド・アカウントを持っていて、Brand Agent Portal (BAP) を使用している場合、アカウントのリンク時にサポートが必要であれば、softlayer_revenue_services_team@wwpdl.vnet.ibm.com に E メールを送信して、Revenue Services チームに連絡してください。

各 SoftLayer アカウントを既存の {{site.data.keyword.Bluemix_notm}} プラットフォーム・アカウントにリンクしたり、新規のアカウントを作成したりするには、以下の手順を実行します。

   1. マスター・ユーザー・アカウントの IBM ID を使用して、カスタマー・ポータルにログインします。
   2. カスタマー・ポータルで**「Bluemix アカウントをリンクします」**をクリックします。
   3. SoftLayer アカウントと {{site.data.keyword.Bluemix_notm}} アカウントをリンクする場合のご利用条件を読み、同意します。
   4. SoftLayer アカウントのユーザーを {{site.data.keyword.Bluemix_notm}} アカウントに追加する操作も含めて、ウィザードのプロンプトに従います。
   5. プロンプトが表示されたら、次のいずれかの操作を行います。
     * 既に {{site.data.keyword.Bluemix_notm}} アカウントを持っている場合は、そのアカウントに関連付けられている E メール・アドレスを入力して、アカウントをリンクします。
     * {{site.data.keyword.Bluemix_notm}} アカウントを持っていない場合は、使用する E メール・アドレスを指定し、{{site.data.keyword.Bluemix_notm}} への招待の手順に従ってアカウントを作成します。
   6. アカウントをリンクした後、各アカウントのエンド・ユーザーに通知して、前述の [IBM ID への切り替え](#switchtoIBMid)セクションに説明されている手順に従って IBM ID にマイグレーションするように指示します。

      エンド・ユーザー・アカウントのみを IBM ID にマイグレーションしてください。 ブランド・アカウント (エンド・ユーザー・アカウントの親アカウントであり、リソースを含んでいない) はマイグレーションしないでください。 ブランド・アカウント・ユーザーは、IBM ID にマイグレーションすると、Brand Agent Portal (BAP) にログインできなくなります。
      {: important}

アカウントがリンクされると、次のように変わることに注意してください。

  * [{{site.data.keyword.Bluemix}} コンソール ![外部リンク・アイコン](../icons/launch-glyph.svg)](https://cloud.ibm.com){: new_window} にログインします。
  * SoftLayer と {{site.data.keyword.Bluemix_notm}} アカウントの両方にアクセスするために、IBM ID 資格情報を使用する必要があります。
  * 既存の SoftLayer 割引は、{{site.data.keyword.Bluemix_notm}} の料金全体に適用されます。
  * 米国ドル (USD) 単位の 1 つの請求書を受け取ります。 既存の {{site.data.keyword.Bluemix_notm}} アカウントがある場合、インフラストラクチャー・リソースに対する {{site.data.keyword.Bluemix_notm}} からの請求は、両方のアカウントをリンクした後に開始される新しい請求処理サイクルで有効になります。 詳しくは『[リンクされたアカウントの統合請求](/docs/customer-portal?topic=customer-portal-unifybillaccounts)』を参照してください。
  * クラシック・インフラストラクチャー・リソースの使用量は、{{site.data.keyword.Bluemix_notm}} コンソールでモニターできます。

## リンクされたアカウントでの多要素認証の使用法
{: #2fa}

リンクされたアカウントを持っている場合、{{site.data.keyword.Bluemix_notm}} IAM **「設定」**ページを使用して、アカウントに対して多要素認証 (MFA) を有効にすることができます。 これは、一般的に 2 要素認証 (2FA) とも呼ばれ、標準的な必須の IBM ID とパスワード以外の認証要素を使用してアカウントにアクセスするためのセキュリティー層を追加します。 ご使用のアカウントの MFA は、リンクされている {{site.data.keyword.Bluemix_notm}} アカウント内のすべてのリソースに適用されます。 ご使用のアカウントで有効になっている場合は、そのアカウントに追加されているすべてのユーザーにも適用されます。

その他の多要素認証方式は、IBM ID 単位ではありません。 アカウント単位です。 IBM ID が複数のアカウントに関連付けられていて、アカウント間で切り替えを行う場合、2 要素認証を必要とする別のアカウントに切り替えるたびに ID を確認する必要があります。 これは、前のアカウントと新しいアカウントが両方とも同じ 2 要素認証メカニズムを使用して構成されている場合でも同じです。

前にクラシック・インフラストラクチャー・リソースに対して[カスタマー・ポータルで 2FA ](/docs/customer-portal?topic=customer-portal-customerportal_2fa)を有効にした場合、その後で {{site.data.keyword.Bluemix_notm}} アカウント MFA 設定を有効にすると、カスタマー・ポータルでセットアップした 2FA はアカウント MFA 設定でオーバーライドされます。 これは、アカウント MFA 設定を優先して、購入した 2FA をカスタマー・ポータルで無効にできることを意味します。
