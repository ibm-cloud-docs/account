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


# {{site.data.keyword.cloudaccesstrailshort}}events  
{: #at_events}

身為安全性管理者、審核員或管理員，您可以使用 {{site.data.keyword.cloudaccesstrailfull}} 服務來追蹤使用者及應用程式如何與 {{site.data.keyword.Bluemix}} 帳戶互動。
{:shortdesc}

例如，使用者或應用程式使用密碼 (Password)、API 金鑰及鑑別碼或密碼 (Passcode) 來登入 {{site.data.keyword.Bluemix_notm}} 時，會針對每次嘗試產生一個 {{site.data.keyword.cloudaccesstrailshort}} 事件。 

{{site.data.keyword.cloudaccesstrailfull_notm}} 服務會記錄由使用者起始並且會變更 {{site.data.keyword.Bluemix_notm}} 中服務狀態的活動。如需相關資訊，請參閱[關於 {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov )。

若要開始監視您使用者的動作，請參閱 [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla)。 

## 管理帳戶的事件
{: #account}

下表列出在呼叫時會產生事件的 API 方法：

<table>
  <caption>產生事件的動作</caption>
  <tr>
    <th>動作</th>
	  <th>說明</th>
  </tr>
  <tr>
    <td>billing.account.create</td>
	  <td>當您在將帳戶 ID 指派給帳戶之後佈建帳戶，即會產生事件。</td>
  </tr>
  <tr>
    <td>billing.account.update</td>
	  <td>當您更新帳戶的相關資訊，即會產生事件。</td>
  </tr>
  <tr>
    <td>billing.account.active</td>
	  <td>當您驗證帳戶，即會產生事件，或者當帳戶轉變為作用中狀態，即會產生事件。</td>
  </tr>
  <tr>
    <td>billing.account.subscription.create</td>
	  <td>當您建立<a href="/docs/account/index.html#subscription-account">訂閱帳戶</a>，即會產生事件。</td>
  </tr>
</table>



## 管理使用者的事件
{: #users}

下表列出在呼叫時會產生事件的 API 方法：

<table>
  <caption>產生事件的動作</caption>
  <tr>
    <th>動作</th>
	  <th>說明</th>
  </tr>
  <tr>
    <td>billing.account.user.create</td>
	  <td>當您將邀請傳送給使用者以加入帳戶，即會產生事件。</br>帳戶擁有者是帳戶中唯一可執行此動作的使用者。</td>
  </tr>
  <tr>
    <td>billing.user.active</td>
	  <td>當您啟動帳戶中的使用者，即會產生事件。</br>當使用者驗證其電子郵件位址，即會產生事件。</td>
  </tr>
  <tr>
    <td>billing.account.user.delete</td>
	  <td>當您從帳戶中移除使用者，即會產生事件。</br>帳戶擁有者是帳戶中唯一可執行此動作的使用者。</td>
  </tr>
</table>

## 管理組織的事件
{: #org}

下表列出在呼叫時會產生事件的 API 方法：

<table>
  <caption>產生事件的動作</caption>
  <tr>
    <th>動作</th>
	  <th>說明</th>
  </tr>
  <tr>
    <td>billing.account.org.create</td>
	  <td>當您將組織新增至帳戶，即會產生事件。</td>
  </tr>
</table>

## 尋找事件的位置
{: #ui}

{{site.data.keyword.cloudaccesstrailshort}} 事件提供於 {{site.data.keyword.cloudaccesstrailshort}} **達拉斯帳戶網域**，這提供於 {{site.data.keyword.Bluemix_notm}}。如需相關資訊，請參閱[檢視帳戶事件](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events)。

{{site.data.keyword.cloudaccesstrailshort}} 事件會自動轉遞至發生該動作之相同地區中的 {{site.data.keyword.cloudaccesstrailshort}} 服務。
