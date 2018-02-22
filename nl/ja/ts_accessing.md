---

copyright:

  years: 2015, 2018

lastupdated: "2017-11-10"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# {{site.data.keyword.Bluemix_notm}} へのアクセスに関するトラブルシューティング
{: #accessing}

{{site.data.keyword.Bluemix}} へのアクセスに関する一般的な問題には、{{site.data.keyword.Bluemix_notm}} にログインできない、アカウントが保留状態にあるなどがあります。 多くの場合、いくつかの簡単なステップを実行することで、これらの問題から復旧することが可能です。
{:shortdesc}

## 誤ったパスワード
{: #ts_logintobm}

{{site.data.keyword.Bluemix_notm}} コンソールにログインするには、IBM ID に関連付けられている有効なパスワードが必要です。

[{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com){: new_window} からログインするには、IBM ID またはリンクされたアカウント ID に関連付けられた有効なパスワードを持っている必要があります。

{{site.data.keyword.Bluemix_notm}} にログインしようとすると、以下のエラー・メッセージが表示されます。
{: tsSymptoms}

`入力したパスワードは正しくありません。`

{{site.data.keyword.Bluemix_notm}} へのログインに使用したパスワードが無効です。
{: tsCauses}

以下のいずれかの解決策を使用してください。
{: tsResolve}
 * 正しいパスワードを入力します。 自分の IBM ID とパスワードが有効であるかどうかを確認するには、「My IBM 」の「プロファイル」ページに移動して、**「ログイン」**をクリックし、「ログイン」ページで IBM ID とパスワードを入力します。
 * パスワードを忘れた場合は、**「パスワードを忘れた場合 (Forgot your password)」**をクリックして、パスワードをリセットします。 次に、[{{site.data.keyword.Bluemix_notm}} コンソール ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.{DomainName}){: new_window} または [{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com){: new_window} に戻り、再びログインします。
 * IBM ID を忘れた場合、あるいはパスワードに関する問題が続く場合は、Worldwide IBM Registration Help Desk にご相談ください。
 * 有効な IBM ID とパスワードを取得するには、「My IBM」の「プロファイル」ページに移動して、**「登録」**をクリックします。

注:
<!-- begin STAGING ONLY -->
 * IBM 従業員の場合、IBM ID はイントラネット ID と異なる可能性があります。
 <!-- end STAGING ONLY -->
 * 「IBM にサインインする」ページを表示しているときに何らかの理由 (例えば、パスワードのリセットなど) でログイン・プロセスが中断された場合は、[{{site.data.keyword.Bluemix_notm}} コンソール ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.{DomainName}){: new_window} または [{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com){: new_window} に戻り、再びログイン・プロセスを開始してください。


## 無効なログイン資格情報
{: #ts_login_invalid_credentials}

IBM ID を使用してログインすると、以下のメッセージが表示されます。
{: tsSymptoms}

`無効なログイン資格情報が入力されました。 IBM ID をアカウントに関連付けている場合は、ここからログインしてください`

* IBM ID に切り替えましたが、以前のユーザー名とパスワードを使用して [{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com){: new_window} からログインしようとしました。
{: tsCauses}

* [{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com){: new_window} からログインしようとしましたが、「ユーザー名」フィールドと「パスワード」フィールドに IBM ID とパスワードを入力しました。

メッセージ内の**「ここからログイン」**をクリックするか、「IBM ID アカウントでのログイン」セクションに移動して**「IBM ID でログイン」**をクリックします。
{: tsResolve}

以前の ID で使用していた**「ユーザー名」**と**「パスワード」**のフィールドは使用しないでください。


## 認識されない IBM ID または E メール
{: #ts_old_username}

{{site.data.keyword.Bluemix_notm}} コンソールにログインすると、以下のメッセージが表示されます。
{: tsSymptoms}

`この IBM ID または E メールを認識できません。(We didn't recognize this IBM ID or email.)`

{{site.data.keyword.Bluemix_notm}} コンソールにログインしようとしましたが、有効な IBM ID を使用しませんでした。 例えば、IBM ID に完全修飾 E メール・アドレスを入力しなかったか、以前のユーザー名とパスワードを使用しようとしました。
{: tsCauses}

{{site.data.keyword.Bluemix_notm}} にログインするには、有効な IBM ID とパスワードが必要です。

 * IBM ID には必ず完全修飾 E メール・アドレスを入力してください。
 {: tsResolve}
 * {{site.data.keyword.BluSoftlayer_full}} ID を持つ {{site.data.keyword.BluSoftlayer_full}} ユーザーの場合、IBM ID 認証を使用してログインするには、あらかじめアクセス権限を持つアカウントごとに {{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータルで IBM ID 認証に切り替えておく必要があります。
 詳しくは、[IBM ID への切り替え](/docs/account/softlayerlink.html#switching-to-ibmid)を参照してください。


## IBM ID がどの IBM Cloud アカウントにも関連付けられていない
{: #ts_login_noswitch}

IBM ID を使用してログインすると、以下のメッセージが表示されます。
{: tsSymptoms}

`このページは、認証が正常に行われたために表示されています。ただし、この IBM ID は IBM クラウド・アカウントに関連付けられていません。(You have reached this page because your authentication was successful, however, this IBMid is not associated with any IBM Cloud accounts.) これがエラーと思われる場合は、アカウント所有者またはマスター・ユーザーにお問い合わせください。(If you believe this to be in error, contact your Account Owner or Master User.)`

有効な IBM ID を使用して [{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com){: new_window} からログインしましたが、{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータルから IBM ID 認証に切り替えられていません。
{: tsCauses}

必要に応じて、以下の確認を行ってください。
{: tsResolve}
 * マスター・ユーザーまたはアカウント管理者に連絡して、IBM ID 認証への切り替えが有効になっているかどうかを確認します。
 * 「IBM ID への切り替え」ステップが完了していることを確認します。 [IBM ID への切り替え](/docs/account/softlayerlink.html#switching-to-ibmid)を参照してください。
 * **「ユーザー ID と IBM ID の関連付け」** E メールのアクションに従っていることを確認します。 受信ボックスとジャンク・メール・フォルダーを調べて E メールを見つけてください。 この E メールを再度取得するには (例えば、有効期限が切れた場合)、{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータルの「ユーザー・プロファイルの編集」ページに移動し、**「E メールの再送」**をクリックします。 あるいは、[{{site.data.keyword.Bluemix_notm}} サポート![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](http://ibm.biz/bluemixsupport.com){: new_window}に連絡してください。

**注:** IBM ID を使用して直接 IBM ID を作成した場合、処理する必要がある 2 つの E メールを受け取ります。1 つは IBM ID 登録からのもので、もう 1 つは {site.data.keyword.Blu_full}} からのものです。 両方の E メールのアクションに従っていることを確認してください。

アカウントのセットアップに応じて、以下の一部のログイン・オプションが適用されることがあります。
 * {{site.data.keyword.BluSoftlayer_full}} ID を持っている {{site.data.keyword.BluSoftlayer_notm}} ユーザーは、[{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com){: new_window} からログインする必要があります。
 * IBM ID を持っている {{site.data.keyword.BluSoftlayer_notm}} ユーザーは、リンクされている {{site.data.keyword.Bluemix_notm}} アカウントの有無に関係なく、[{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com){: new_window} からログインして {{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータルを開くか、[{{site.data.keyword.Bluemix_notm}} コンソール ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.{DomainName}){: new_window} からログインしてインフラストラクチャー・ダッシュボードを開くことができます。


## IBM ID がどの {{site.data.keyword.Bluemix_notm}} アカウントにも関連付けられていない
{: #ts_unabletologin}

{{site.data.keyword.Bluemix_notm}} にログインすると、以下のメッセージが表示されます。
{: tsSymptoms}

`このページは、認証が正常に行われたために表示されています。ただし、この IBM ID はどの {{site.data.keyword.Bluemix_notm}} アカウントにも関連付けられていません。(You have reached this page because your authentication was successful, however, this IBMid is not associated with any IBM Cloud accounts.)`

有効な IBM ID を使用して [{{site.data.keyword.Bluemix_notm}} コンソール![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://console.{DomainName}){: new_window}からログインしましたが、まだ {{site.data.keyword.Bluemix_notm}} アカウントが作成されていません。
{: tsCauses}

{{site.data.keyword.Bluemix_notm}} アカウントを作成するには、登録プロセスに従います。
{: tsResolve}

アカウントのセットアップに応じて、以下の一部のログイン・オプションが適用されることがあります。
 * リンクされたアカウントを持たない {{site.data.keyword.Bluemix_notm}} ユーザーは、{{site.data.keyword.Bluemix_notm}} コンソールを介してログインする必要があります。
 * リンクされたアカウントを持つ {{site.data.keyword.Bluemix_notm}} ユーザーは、[{{site.data.keyword.Bluemix_notm}} コンソール ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.{DomainName}){: new_window} または [{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com){: new_window} からログインできます。


## コンソールが開かない
{: #ts_login_stalls}

IBM ID を使用してログインすると、ログイン成功のメッセージが表示されますが、[{{site.data.keyword.Bluemix_notm}} コンソール ![外部リンク・アイコンicon](../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.{DomainName}){: new_window} または [{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン ")](https://control.softlayer.com){: new_window} には戻りません。
{: tsSymptoms}

以下のいずれかの解決策を使用してください。
{: tsResolve}
 * ブラウザーを閉じ、キャッシュと Cookie を消去してから、ログインを再試行します。
 * IBM ID 認証サービスから直接ではなく、必ず [{{site.data.keyword.Bluemix_notm}} コンソール ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://console.{DomainName}){: new_window} または [{{site.data.keyword.BluSoftlayer_notm}} インフラストラクチャーのカスタマー・ポータル ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://control.softlayer.com){: new_window} からログインするようにしてください。


## IBM ID のログインが完了しない
{: #ts_login_ibmid}

{{site.data.keyword.Bluemix_notm}} にログインしたときに、IBM ID を使用した認証が完了しません。
{: tsSymptoms}

IBM ID 認証サービスに問題がある可能性があります。
{: tsCauses}

[IBM IBMid ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://new.wind.ibmcloud.com/webapp/#/status/a1a0c5d743d94a6a9597087541564d8e){: new_window} で、サービスの状況を確認し、再試行してください。
{: tsResolve}


## アカウントが保留になっている
{: #ts_accntpding}

アカウントが保留になっている場合は、{{site.data.keyword.Bluemix_notm}} にログインできません。

{{site.data.keyword.Bluemix_notm}} トライアル・アカウントに登録した後、{{site.data.keyword.Bluemix_notm}} にログインできない場合があります。 次のメッセージが表示されます。
{: tsSymptoms}

<code>アカウントが保留になっています。 E メールの確認を最大 24 時間待って、スパム・フォルダーも確認してください。 それでも確認の E メールが届かない場合は、<a href="http://ibm.biz/bluemixsupport.com" target="_blank">{{site.data.keyword.Bluemix_notm}} サポート</a>までお問い合わせください。</code>

{{site.data.keyword.Bluemix_notm}} トライアル・アカウントに登録した後、確認の E メールが届きます。 その確認 E メールに記載されたリンクをクリックして、登録プロセスを完了する必要があります。
{: tsCauses}

確認の E メールは、ユーザーが入力した E メール・アドレス宛に送信されます。 受信ボックスとスパム・フォルダーを確認してください。 確認の E メールが届かない場合は、[{{site.data.keyword.Bluemix_notm}} サポート![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](http://ibm.biz/{{site.data.keyword.Bluemix_notm}}support.com){: new_window}にお問い合わせください。  
{: tsResolve}


<!-- begin STAGING ONLY -->

## 外部 Web サイトへのアクセスの問題
{: #ts_bmlinkid}

IBM イントラネット ID を使用して {{site.data.keyword.Bluemix_notm}} にログインするには、イントラネット ID を IBM ID にリンクする必要があります。

{{site.data.keyword.Bluemix_notm}} の「サインイン」ページで**「イントラネット ID を使用してサインイン (Sign in with your intranet ID)」**を選択すると、以下のメッセージが表示されることがあります。
{: tsSymptoms}

`外部 Web サイトへのアクセス時の問題 (Problem Accessing External Website)`

この問題は、IBM ID にリンクされていない IBM イントラネット ID を使用して {{site.data.keyword.Bluemix_notm}} にログインした場合に発生します。 IBM ID は、www.ibm.com へのログインに使用する ID です。
{: tsCauses}

IBM 従業員が自分の IBM イントラネット ID を使用して {{site.data.keyword.Bluemix_notm}} にログインするには、その前にそのイントラネット ID を外部の IBM ID にリンクしておく必要があります。 2 つの ID をリンクするには、以下のステップを実行します。
{: tsResolve}

  1. [Central Sign-on ![「外部リンク」アイコン](../icons/launch-glyph.svg "「外部リンク」アイコン")](https://w3-03.sso.ibm.com/tools/cso/index.jsp){: new_window} ページで、**「マイ・サインオン (My Sign-ons)」**をクリックします。
  2. 「マイ・サインオン (My Sign-ons)」ページで、**「ID のリンク (Link IDs)」**をクリックして、{{site.data.keyword.Bluemix_notm}} の「サインイン (Sign in)」ページで自分の IBM ID とパスワードを入力します。 その後、イントラネット ID と IBM ID が自動的にリンクされます。


<!-- end STAGING ONLY -->

## {{site.data.keyword.Bluemix_notm}} ページをロードできない
{: #ts_err}

{{site.data.keyword.Bluemix_notm}} コンソールを使用する際、コンソール・ページをロードできない場合があります。 代わりに、エラー・メッセージ BXNUI0001E または BXNUI0016E が表示されることがあります。

{{site.data.keyword.Bluemix_notm}} コンソールを使用する際、次のいずれかのエラー・メッセージが表示される可能性があります。
{: tsSymptoms}

`BXNUI0001E: セッションが存在しているかどうかを {{site.data.keyword.Bluemix_notm}} が検出しなかったため、ページはロードされませんでした。`

`BXNUI0016E: {{site.data.keyword.Bluemix_notm}} ページがロードされなかったため、アプリおよびサービスは取得されませんでした。`

必要に応じて、以下の 1 つ以上のアクションを実行してください。
{: tsResolve}

  * ブラウザーを最新表示または再始動します。
  * {{site.data.keyword.Bluemix_notm}} をいったんログアウトしてから、再度ログインします。
  * ブラウザーのプライベート表示モードを使用します。
  * ブラウザーの Cookie およびキャッシュをクリアします。
  * 異なるブラウザーを使用します。 {{site.data.keyword.Bluemix_notm}} によりサポートされているブラウザーのバージョンについて詳しくは、[{{site.data.keyword.Bluemix_notm}} の前提条件](/docs/overview/whatisbluemix.html#prereqs)を参照してください。
  * cf コマンド・ライン・インターフェースがインストール済みであれば、`cf apps` コマンドを入力してアプリが実行中であるかどうか確認します。
