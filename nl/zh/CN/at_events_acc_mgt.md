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


# {{site.data.keyword.cloudaccesstrailshort}} 事件  
{: #at_events}

作为安全主管、审计员或管理者，您可以使用 {{site.data.keyword.cloudaccesstrailfull}} 服务来跟踪用户和应用程序如何与 {{site.data.keyword.Bluemix}} 帐户进行交互。
{:shortdesc}

例如，当用户或应用程序使用密码、API 密钥和认证代码或通行码登录到 {{site.data.keyword.Bluemix_notm}} 时，系统会为每次尝试生成一个 {{site.data.keyword.cloudaccesstrailshort}} 事件。 

{{site.data.keyword.cloudaccesstrailfull_notm}} 服务会记录 {{site.data.keyword.Bluemix_notm}} 中用户发起的更改服务状态的活动。有关更多信息，请参阅[关于 {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov )。

要开始监视用户的操作，请参阅 [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla)。 

## 用于管理帐户的事件
{: #account}

下表列出了在调用时会生成事件的 API 方法：

<table>
  <caption>生成事件的操作</caption>
  <tr>
    <th>操作</th>
	  <th>描述
</th>
  </tr>
  <tr>
    <td>billing.account.create</td>
	  <td>供应帐户时以及将帐户标识分配给帐户后，将生成一个事件。</td>
  </tr>
  <tr>
    <td>billing.account.update</td>
	  <td>更新帐户相关信息时，将生成一个事件。</td>
  </tr>
  <tr>
    <td>billing.account.active</td>
	  <td>验证帐户时或在帐户变为活动状态后，将生成一个事件。</td>
  </tr>
  <tr>
    <td>billing.account.subscription.create</td>
	  <td>创建<a href="/docs/account/index.html#subscription-account">预订帐户</a>时，将生成一个事件。</td>
  </tr>
</table>



## 用于管理用户的事件
{: #users}

下表列出了在调用时会生成事件的 API 方法：

<table>
  <caption>生成事件的操作</caption>
  <tr>
    <th>操作</th>
	  <th>描述
</th>
  </tr>
  <tr>
    <td>billing.account.user.create</td>
	  <td>向用户发送加入帐户邀请时，将生成一个事件。</br>帐户所有者是帐户中可执行此操作的唯一用户。</td>
  </tr>
  <tr>
    <td>billing.user.active</td>
	  <td>激活帐户中的用户时，将生成一个事件。</br>用户验证其电子邮件地址时，将生成该事件。</td>
  </tr>
  <tr>
    <td>billing.account.user.delete</td>
	  <td>从帐户中除去用户时，将生成一个事件。</br>帐户所有者是帐户中可执行此操作的唯一用户。</td>
  </tr>
</table>

## 用于管理组织的事件
{: #org}

下表列出了在调用时会生成事件的 API 方法：

<table>
  <caption>生成事件的操作</caption>
  <tr>
    <th>操作</th>
	  <th>描述
</th>
  </tr>
  <tr>
    <td>billing.account.org.create</td>
	  <td>将组织添加到帐户时，将生成一个事件。</td>
  </tr>
</table>

## 在何处查找事件
{: #ui}

{{site.data.keyword.cloudaccesstrailshort}} 事件位于 {{site.data.keyword.cloudaccesstrailshort}} **达拉斯帐户域**中，而该帐户域位于 {{site.data.keyword.Bluemix_notm}} 中。有关更多信息，请参阅[查看帐户事件](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events)。

{{site.data.keyword.cloudaccesstrailshort}} 事件会自动转发到操作发生所在区域中的 {{site.data.keyword.cloudaccesstrailshort}} 服务。
