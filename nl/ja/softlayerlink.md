---



copyright:

  years: 2016, 2018
lastupdated: "2018-01-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# IBM ID への切り替え
SoftLayer での認証は、IBM ID を使用して {{site.data.keyword.Bluemix}} のすべてに対して単一のログインを提供するようになりました。 既存の SoftLayer アカウントは IBM ID 認証への切り替えが有効になっています。 マイグレーション・ウィザードを使用して、この切り替えの処理を行います。
{:shortdesc}

IBM ID への切り替えを開始しても、処理が完了する前であればいつでも切り替えを取り消すことができます。 ただし、ログインするたびに、IBM ID への切り替えを促すプロンプトが表示されます。 {{site.data.keyword.Bluemix_notm}} アカウントにリンクする予定の各 SoftLayer アカウントは、固有の E メール・アドレスを持つ固有の IBM ID によって所有される必要があります。

既存の SoftLayer アカウントを IBM ID に切り替えるには、以下の手順を実行します。
1. SoftLayer アカウントにログインし、IBM ID への切り替えを促すプロンプトが表示されたら、**「OK」**をクリックします。

   マスター・ユーザーであるのに {{site.data.keyword.slportal}} に IBM ID への切り替えを促すプロンプトが表示されない場合、[IBM サポート](/docs/get-support/howtogetsupport.html#getting-customer-support)に連絡して、支援を依頼してください。

   既にログインしており、プロンプトに対して**「後で」**をクリックしたものの、IBM ID 認証への切り替えを現行セッションで行うことにした場合は、「ユーザー・プロファイルの編集」ページに移動し、**「IBM ID への切り替え」**をクリックします。

2. ウィザードのプロンプトに従って IBM ID を作成します。

   どの IBM ID でも現在使用されていない E メール・アドレスを入力します。 この E メール・アドレスは、新規 IBM ID のユーザー名として使用され、IBM ID の作成後に登録コードが送信される宛先となります。 IBM ID に関連付けられている E メール・アドレスは後で更新できますが、ユーザー名は変更できません。

3. 登録コードを受信したら、E メールのリンクをクリックするか、URL をブラウザーにコピーして、登録コードを入力します。

   コードは 7 日間有効で、1 回のみ使用できます。

4. 登録コードを送信した後、IBM ID を使用してカスタマー・ポータルにログインします。

   「アカウントのログイン」プロンプトで、**「IBM ID アカウントでのログイン」**セクションに移動し、**「IBM ID でログイン」**をクリックします。 以前に SoftLayer ID で使用していた**「ユーザー名」**と**「パスワード」**のフィールドは使用しないでください。

新規のお客様の場合、注文を清算する際、既存の IBM ID を入力するか、新規 IBM ID を作成するよう求められます。
  * 既存の IBM ID を使用するには、ユーザー名を入力するか、または IBM ID の E メール・アドレスが固有の場合 (つまり、複数の IBM ID 間で共有されていない場合) は E メール・アドレスを入力します。

  * 新規 IBM ID を作成するには、どの IBM ID でも現在使われていない E メール・アドレスを入力します。 この E メール・アドレスは、IBM ID のユーザー名であり、IBM ID の作成後に登録コードが送信される宛先となります。 IBM ID に関連付けられている E メール・アドレスは後で更新できますが、ユーザー名を変更することはできません。

IBM ID でのログインに関する問題を解決するには、『[{{site.data.keyword.Bluemix_notm}} へのアクセスに関するトラブルシューティング](/docs/get-support/ts_accessing.html#accessing)』を参照してください。

## IBM ID の認証用のユーザー・アカウントの有効化
{: #link_accounts_resellers}

場合によっては、アカウントでの IBM ID 認証の使用を販売店または流通業者が前もって有効にしておかないと、ユーザーが IBM ID に切り替えることができないことがあります。

  * IBM ID 認証は、{{site.data.keyword.Bluemix_notm}} アカウントにリンクする既存のユーザー・アカウントごとに有効にする必要があります。 その後、各ユーザーは、前のセクションで説明されているように、マイグレーション・ウィザードを使用して IBM ID に切り替えるプロセスを完了する必要があります。 既存の SoftLayer アカウントが IBM ID 認証を使用できるようにするには、[IBM サポート](/docs/get-support/howtogetsupport.html#getting-customer-support)に連絡してください。

  * 新規ユーザー・アカウントが確実に IBM ID を使用して作成されるようにするには、即時マスター・ユーザー・アカウントに `CREATE_NEW_ACCOUNT_WITH_IBMid_AUTHENTICATION` 属性が設定される必要があります。 [IBM サポート](/docs/get-support/howtogetsupport.html#getting-customer-support)またはベンダーに連絡して、アカウントに属性を設定するように依頼してください。  

## IBM ID ユーザー・アカウントのリンク
{: #link_user_accounts}

ユーザー・アカウントを IBM ID 認証に切り替えた後、販売店および流通業者は SoftLayer アカウントと {{site.data.keyword.Bluemix_notm}} アカウントをリンクして、結合されたインフラストラクチャーおよびプラットフォームのリソースを利用できます。 必ず、以下の重要な注意事項を確認してください。

  * リンクされるアカウントのマスター・ユーザーは、IBM ID を持っていなければなりません。
  * {{site.data.keyword.Bluemix_notm}} アカウントにリンクする各ユーザー・アカウントは、固有の E メール・アドレスを持つ固有の IBM ID によって所有される必要があります。 単一の IBM ID が複数の SoftLayer アカウントを所有することは可能ですが、マスター・ユーザーを、アカウントごとに固有の IBM ID となるように変更する必要があります。 SoftLayer アカウントのマスター・ユーザーを変更するには、[IBM SoftLayer サポート![「外部リンク」アイコン](../icons/launch-glyph.svg)](https://knowledgelayer.softlayer.com/topic/support){: new_window}に連絡してください。
  * リンクされたアカウントに新規ユーザーを追加する場合、ユーザーを SoftLayer アカウントと {{site.data.keyword.Bluemix_notm}} アカウントの両方に追加して、統合されたコンソールのすべての機能にアクセスできるようにする必要があります。

各アカウントを {{site.data.keyword.Bluemix_notm}} アカウントにリンクするには、以下のステップを実行します。
1. 既存の {{site.data.keyword.Bluemix_notm}} アカウントにリンクするか、新規に作成するには、マスター・ユーザーとしてカスタマー・ポータルにログインし、{{site.data.keyword.Bluemix_notm}} リンクをクリックします。

   アカウントのマスター・ユーザーである IBM ID は、リンクする先の {{site.data.keyword.Bluemix_notm}} アカウントの所有者でなければなりません。

2. SoftLayer アカウントのユーザーを {{site.data.keyword.Bluemix_notm}} アカウントに追加する操作も含めて、ウィザードのプロンプトに従います。
3. アカウントをリンクした後、各アカウントのエンド・ユーザーに通知して、前のセクションに説明されている手順に従って IBM ID にマイグレーションするように指示します。

エンド・ユーザー・アカウントのみを IBM ID にマイグレーションしてください。 ブランド・アカウント (エンド・ユーザー・アカウントの親アカウントであり、リソースを含んでいない) はマイグレーションしないでください。 ブランド・アカウント・ユーザーは、IBM ID にマイグレーションすると、Brand Agent Portal (BAP) にログインできなくなります。
{: tip}  

## リンクされたアカウントでの多要素認証の使用法
{: #2fa}

リンクされたアカウントを持っている場合、ID およびアクセスの**「設定」**ページを使用して、ご使用のアカウントで多要素認証認証 (/docs/iam/mfa.html) を有効にすることができます。これは、一般的に 2 要素認証 (2FA) とも呼ばれ、標準的な必須の IBM ID とパスワード以外の認証要素を使用してアカウントにアクセスするためのセキュリティー層を追加します。ご使用のアカウントの多要素認証は、リンクされている {{site.data.keyword.Bluemix_notm}} アカウント内のすべてのリソースに適用されます。ご使用のアカウントで多要素認証が有効になっている場合は、そのアカウントに追加されているすべてのユーザーにも適用されます。ご使用のアカウントで[多要素認証を有効にする](/docs/iam/mfa.html)際に検討すべき考慮事項について確認してください。

多要素認証は、IBM ID ごとには行われません。従来どおり、アカウント単位です。 IBM ID が複数のアカウントに関連付けられていて、アカウント間で切り替えを行う場合、2 要素認証を必要とする別のアカウントに切り替えるたびに ID を確認する必要があります。 これは、前のアカウントと新しいアカウントが両方とも同じ 2 要素認証メカニズムを使用して構成されている場合でも同じです。

<!-- Above section is for MFA release 1/2018. Commented out section here has old content.
If you enabled two-factor authentication for your existing SoftLayer account, you are still required to enter your security code when logging in to the {{site.data.keyword.Bluemix_notm}} console. However, the two-factor authentication applies only to the resources in your Infrastructure account. You might be able to do various actions to the resources in your {{site.data.keyword.Bluemix_notm}} account without doing two-factor authentication.
Two-factor authentication is not per IBMid. It is still per account. When an IBMid is associated with multiple accounts, and you switch between accounts, you must confirm your identity every time you switch to a different account that requires two-factor authentication. This is true even if the prior account and the new account are both configured with the same two-factor authentication mechanism.
-->

