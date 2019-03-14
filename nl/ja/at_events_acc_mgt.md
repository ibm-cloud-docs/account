---

copyright:
  years: 2016, 2018

lastupdated: "2018-10-31"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# {{site.data.keyword.cloudaccesstrailshort}} イベント  
{: #at_events}

セキュリティー担当者、監査員、またはマネージャーは、{{site.data.keyword.cloudaccesstrailfull}} サービスを使用して、ユーザーおよびアプリケーションが {{site.data.keyword.Bluemix}} アカウントとどのように対話しているのかをトラッキングできます。 
{:shortdesc}

例えば、ユーザーまたはアプリケーションがパスワード、API キー、認証コード、またはパスコードを使用して {{site.data.keyword.Bluemix_notm}} にログインすると、それぞれの試行ごとに {{site.data.keyword.cloudaccesstrailshort}} イベントが生成されます。 

{{site.data.keyword.cloudaccesstrailfull_notm}} サービスは、{{site.data.keyword.Bluemix_notm}} 内のサービスの状態を変更するユーザー開始アクティビティーを記録します。 詳しくは、[{{site.data.keyword.cloudaccesstrailshort}} ](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov ) についてのページを参照してください。

ユーザーのアクションのモニターを開始するには、[{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla)を参照してください。 

## アカウント管理のイベント
{: #account}

次の表に、呼び出されたときにイベントを生成する API メソッドのリストを示します。

<table>
  <caption>イベントを生成するアクション</caption>
  <tr>
    <th>アクション</th>
	  <th>説明</th>
  </tr>
  <tr>
    <td>billing.account.create</td>
	  <td>アカウントをプロビジョンすると、そのアカウントにアカウント ID が割り当てられた後に、イベントが生成されます。</td>
  </tr>
  <tr>
    <td>billing.account.update</td>
	  <td>アカウントに関する情報を更新すると、イベントが生成されます。</td>
  </tr>
  <tr>
    <td>billing.account.active</td>
	  <td>アカウントを検証すると、イベントが生成されます。つまり、アカウントがアクティブ状態になると、イベントが生成されます。</td>
  </tr>
  <tr>
    <td>billing.account.subscription.create</td>
	  <td><a href="/docs/account/index.html#subscription-account">サブスクリプション・アカウント</a>を作成すると、イベントが生成されます。</td>
  </tr>
</table>



## ユーザー管理のイベント
{: #users}

次の表に、呼び出されたときにイベントを生成する API メソッドのリストを示します。

<table>
  <caption>イベントを生成するアクション</caption>
  <tr>
    <th>アクション</th>
	  <th>説明</th>
  </tr>
  <tr>
    <td>billing.account.user.create</td>
	  <td>アカウントに参加するようにユーザーに招待を送信すると、イベントが生成されます。 </br>アカウント内のユーザーでこのアクションを実行できるのは、アカウント所有者のみです。</td>
  </tr>
  <tr>
    <td>billing.user.active</td>
	  <td>アカウント内のユーザーをアクティブにすると、イベントが生成されます。 </br>このイベントは、そのユーザーが自分の E メール・アドレスを検証したときに生成されます。</td>
  </tr>
  <tr>
    <td>billing.account.user.delete</td>
	  <td>アカウントからユーザーを削除すると、イベントが生成されます。 </br>アカウント内のユーザーでこのアクションを実行できるのは、アカウント所有者のみです。</td>
  </tr>
</table>

## 組織管理のイベント
{: #org}

次の表に、呼び出されたときにイベントを生成する API メソッドのリストを示します。

<table>
  <caption>イベントを生成するアクション</caption>
  <tr>
    <th>アクション</th>
	  <th>説明</th>
  </tr>
  <tr>
    <td>billing.account.org.create</td>
	  <td>アカウントに組織を追加すると、イベントが生成されます。</td>
  </tr>
</table>

## イベントを検索する場所
{: #ui}

{{site.data.keyword.cloudaccesstrailshort}} イベントは、{{site.data.keyword.Bluemix_notm}} 内にある {{site.data.keyword.cloudaccesstrailshort}} **ダラス・アカウント・ドメイン**で使用可能です。詳しくは、[アカウント・イベントの表示](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events)を参照してください。

{{site.data.keyword.cloudaccesstrailshort}} イベントは、アクションが発生したのと同じ地域内の {{site.data.keyword.cloudaccesstrailshort}} サービスに自動的に転送されます。
