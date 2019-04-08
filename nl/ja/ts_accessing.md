---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-28"

keywords: troubleshoot account, account problem, account support, account help, account error, access error, login error, error message

subcollection: account

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# {{site.data.keyword.Bluemix_notm}} へのアクセスに関するトラブルシューティング
{: #accessing}

{{site.data.keyword.Bluemix}} へのアクセスに関する一般的な問題には、{{site.data.keyword.Bluemix_notm}} にログインできない、アカウントが保留状態にあるなどがあります。 多くの場合、いくつかの簡単なステップを実行することで、これらの問題から復旧することが可能です。
{:shortdesc}


## パスワードが正しくないのはなぜですか?
{: #ts_logintobm}
{: troubleshoot}

{{site.data.keyword.Bluemix_notm}} コンソールにログインするには、IBMid または SoftLayer ID に関連付けられている有効なパスワードが必要です。

{{site.data.keyword.Bluemix_notm}} にログインしようとすると、以下のエラー・メッセージが表示されます。
{: tsSymptoms}

`入力したパスワードは正しくありません。`

{{site.data.keyword.Bluemix_notm}} へのログインに使用したパスワードが無効です。
{: tsCauses}

以下のいずれかの方法を使用してください。
{: tsResolve}
 * [IBM プロファイル・ページ ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://myibm.ibm.com/dashboard/){: new_window} にアクセスして、有効なパスワードを使用していることを確認します。
 * パスワードを忘れた場合は、**「パスワードを忘れた場合 (Forgot your password)」**をクリックして、パスワードをリセットします。
 * IBMid を忘れた場合、あるいはパスワードに関する問題が続く場合は、Worldwide IBM Registration Help Desk にご相談ください。

{{site.data.keyword.Bluemix_notm}} にサインインし、ログイン・プロセスが何らかの理由 (例えば、パスワードのリセット) で中断された場合、コンソールに戻り、ログイン・プロセスを最初からやり直してください。
{: tip}


## IBMid または E メールが認識されなかったのはなぜですか?
{: #ts_old_username}
{: troubleshoot}

E メールに正常にログインするには、アカウントごとに IBMid 認証があることを確認する必要があります。

{{site.data.keyword.Bluemix_notm}} コンソールにログインすると、以下のメッセージが表示されます。
{: tsSymptoms}

`この IBMid または E メールを認識できません。(We didn't recognize this IBMid or email.)`

コンソールにログインしようとしましたが、有効な IBMid を使用しませんでした。 例えば、IBMid に完全修飾 E メール・アドレスを入力しなかったか、以前のユーザー名とパスワードを使用しようとしました。
{: tsCauses}

{{site.data.keyword.Bluemix_notm}} にログインするには、有効な IBMid とパスワードが必要です。

 * IBMid の完全修飾 E メール・アドレスを入力してください。
 {: tsResolve}
 * SoftLayer ID を使用している SoftLayer ユーザーの場合、ログインできるためには、アクセス権限を持つ各アカウントで IBMid 認証に切り替えておく必要があります。 詳しくは、[IBMid への切り替え](/docs/account?topic=account-unifyingaccounts)を参照してください。


## IBMid がどの {{site.data.keyword.Bluemix_notm}} アカウントにも関連付けられていないのはなぜですか?
{: #ts_unabletologin}
{: troubleshoot}

{{site.data.keyword.Bluemix_notm}} にログインすると、以下のメッセージが表示されます。
{: tsSymptoms}

`このページは、認証が正常に行われたために表示されています。ただし、この IBMid はどの {{site.data.keyword.Bluemix_notm}} アカウントにも関連付けられていません。(You have reached this page because your authentication was successful, however, this IBMid is not associated with any IBM Cloud accounts.)`

有効な IBMid を使用して [{{site.data.keyword.Bluemix_notm}} コンソール](https://{DomainName}){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") からログインしましたが、{{site.data.keyword.Bluemix_notm}} アカウントが作成されていません。
{: tsCauses}

{{site.data.keyword.Bluemix_notm}} アカウントを作成するには、登録プロセスに従います。
{: tsResolve}


## IBMid でログインしたときにコンソールが開かないのはなぜですか?
{: #ts_login_stalls}
{: troubleshoot}

ログイン成功メッセージが出されますが、コンソールに戻りません。

IBMid を使用してログインすると、ログインに成功したというメッセージが表示されますが、[{{site.data.keyword.Bluemix_notm}} コンソール](https://{DomainName}){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") に戻りません。
{: tsSymptoms}

以下のいずれかの方法を使用してください。
{: tsResolve}
 * ブラウザーを閉じ、キャッシュと Cookie を消去してから、ログインを再試行します。
 * [{{site.data.keyword.Bluemix_notm}} コンソール](https://{DomainName}){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") からログインします。


## IBMid ログインが完了しなかったのはなぜですか?
{: #ts_login_ibmid}
{: troubleshoot}

{{site.data.keyword.Bluemix_notm}} にログインし、IBMid の認証が完了しない場合、このサービスに問題がある可能性があります。

{{site.data.keyword.Bluemix_notm}} にログインしたときに、IBMid を使用した認証が完了しません。
{: tsSymptoms}

IBMid 認証サービスに問題がある可能性があります。
{: tsCauses}

[IBM](https://idaas.iam.ibm.com/idaas/mtfim/sps/authsvc?PolicyId=urn:ibm:security:authentication:asf:basicldapuser){: new_window} ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン") にログインできるかどうか確認してください。 できる場合、これはアプリケーション問題であり、後でコンソールへのログインを再試行できます。 このページにログインできない場合、[IBMid ヘルプ・デスク ![外部リンク・アイコン](../icons/launch-glyph.svg "外部リンク・アイコン")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window} にお問い合わせください。  
{: tsResolve}


## アカウントを登録した直後にログインできないのはなぜですか?
{: #ts_accntpding}
{: troubleshoot}

アカウントが保留になっている場合は、{{site.data.keyword.Bluemix_notm}} にログインできません。

{{site.data.keyword.Bluemix_notm}} ライト・アカウントに登録した後、{{site.data.keyword.Bluemix_notm}} にログインできない場合があります。 次のメッセージが表示されます。
{: tsSymptoms}

<code>アカウントが保留になっています。 E メールの確認を最大 24 時間待って、スパム・フォルダーも確認してください。 それでも確認の E メールが届かない場合は、<a href="https://ibm.biz/ibmcloudsupport" target="_blank">{{site.data.keyword.Bluemix_notm}} サポート</a>までお問い合わせください。</code>

{{site.data.keyword.Bluemix_notm}} ライト・アカウントに登録すると E メールが届きます。そのメールに含まれているリンクをクリックして登録を確認する必要があります。  
{: tsCauses}

確認の E メールは、IBMid と関連付けられた E メール・アドレスに送信されます。 受信ボックスとスパム・フォルダーを確認してください。 確認の E メールが届かない場合は、[{{site.data.keyword.Bluemix_notm}} サポート](/docs/get-support?topic=get-support-getting-customer-support)にお問い合わせください。  
{: tsResolve}


## ロードされないコンソール・ページがあるのはなぜですか?
{: #ts_err}
{: troubleshoot}

{{site.data.keyword.Bluemix_notm}} コンソールを使用する際、コンソール・ページをロードできない場合があります。 代わりに、エラー・メッセージ BXNUI0001E または BXNUI0016E が表示されることがあります。

以下のいずれかのエラー・メッセージが表示されます。
{: tsSymptoms}

`BXNUI0001E: セッションが存在しているかどうかを {{site.data.keyword.Bluemix_notm}} が検出しなかったため、ページはロードされませんでした。`

`BXNUI0016E: {{site.data.keyword.Bluemix_notm}} ページがロードされなかったため、アプリおよびサービスは取得されませんでした。`

必要に応じて、以下の 1 つ以上のアクションを実行してください。
{: tsResolve}

  * ブラウザーを最新表示または再始動します。
  * {{site.data.keyword.Bluemix_notm}} をいったんログアウトしてから、再度ログインします。
  * ブラウザーのプライベート表示モードを使用します。
  * ブラウザーの Cookie およびキャッシュをクリアします。
  * 異なるブラウザーを使用します。 {{site.data.keyword.Bluemix_notm}} によりサポートされているブラウザーのバージョンについて詳しくは、[{{site.data.keyword.Bluemix_notm}} の前提条件](/docs/overview?topic=overview-prereqs-platform)を参照してください。
  * Cloud Foundry コマンド・ライン・インターフェースがインストール済みであれば、`ibmcloud cf apps` コマンドを入力してアプリが実行中であるかどうか確認します。
