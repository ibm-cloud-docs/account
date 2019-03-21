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


# {{site.data.keyword.cloudaccesstrailshort}} 이벤트  
{: #at_events}

보안 담당자, 감사자 또는 관리자인 경우에는 {{site.data.keyword.cloudaccesstrailfull}} 서비스를 사용하여 사용자와 애플리케이션이 {{site.data.keyword.Bluemix}} 계정과 상호작용하는 방식을 추적할 수 있습니다.{:shortdesc}

예를 들어, 사용자 또는 애플리케이션이 비밀번호, API 키, 인증 코드 또는 패스코드를 사용하여 {{site.data.keyword.Bluemix_notm}}에 로그인할 때 각 시도에 대해 {{site.data.keyword.cloudaccesstrailshort}} 이벤트가 생성됩니다. 

{{site.data.keyword.cloudaccesstrailfull_notm}} 서비스는 {{site.data.keyword.Bluemix_notm}}의 서비스 상태를 변경하는 사용자가 시작한 활동을 기록합니다. 자세한 정보는 [{{site.data.keyword.cloudaccesstrailshort}} 정보](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov )를 참조하십시오.

사용자의 조치에 대한 모니터링을 시작하려면 [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla)의 내용을 참조하십시오. 

## 계정 관리를 위한 이벤트
{: #account}

다음 표에는 호출 시 이벤트를 생성하는 API 메소드가 나열되어 있습니다.

<table>
  <caption>이벤트를 생성하는 조치</caption>
  <tr>
    <th>조치</th>
	  <th>설명</th>
  </tr>
  <tr>
    <td>billing.account.create</td>
	  <td>계정을 프로비저닝하고 계정 ID가 계정에 지정된 후에 이벤트가 생성됩니다.</td>
  </tr>
  <tr>
    <td>billing.account.update</td>
	  <td>계정에 대한 정보를 업데이트할 때 이벤트가 생성됩니다.</td>
  </tr>
  <tr>
    <td>billing.account.active</td>
	  <td>계정을 확인하거나 계정이 활성 상태가 될 때 이벤트가 생성됩니다.</td>
  </tr>
  <tr>
    <td>billing.account.subscription.create</td>
	  <td><a href="/docs/account/index.html#subscription-account">구독 계정</a>을 작성할 때 이벤트가 생성됩니다.</td>
  </tr>
</table>



## 사용자 관리를 위한 이벤트
{: #users}

다음 표에는 호출 시 이벤트를 생성하는 API 메소드가 나열되어 있습니다.

<table>
  <caption>이벤트를 생성하는 조치</caption>
  <tr>
    <th>조치</th>
	  <th>설명</th>
  </tr>
  <tr>
    <td>billing.account.user.create</td>
	  <td>사용자에게 계정 가입 초대를 보내면 이벤트가 생성됩니다. </br>계정 소유자는 이 조치를 수행할 수 있는 계정의 유일한 사용자입니다.</td>
  </tr>
  <tr>
    <td>billing.user.active</td>
	  <td>계정에서 사용자를 활성화하면 이벤트가 생성됩니다. </br>사용자가 자신의 이메일 주소를 확인할 때 이벤트가 생성됩니다.</td>
  </tr>
  <tr>
    <td>billing.account.user.delete</td>
	  <td>계정에서 사용자를 제거할 때 이벤트가 생성됩니다. </br>계정 소유자는 이 조치를 수행할 수 있는 계정의 유일한 사용자입니다.</td>
  </tr>
</table>

## 조직 관리를 위한 이벤트
{: #org}

다음 표에는 호출 시 이벤트를 생성하는 API 메소드가 나열되어 있습니다.

<table>
  <caption>이벤트를 생성하는 조치</caption>
  <tr>
    <th>조치</th>
	  <th>설명</th>
  </tr>
  <tr>
    <td>billing.account.org.create</td>
	  <td>계정에 조직을 추가할 때 이벤트가 생성됩니다.</td>
  </tr>
</table>

## 이벤트 확인 위치
{: #ui}

{{site.data.keyword.cloudaccesstrailshort}} 이벤트는 {{site.data.keyword.Bluemix_notm}}에서 사용 가능한 {{site.data.keyword.cloudaccesstrailshort}} **Dallas 계정 도메인**에서 사용할 수 있습니다. 자세한 정보는 [계정 이벤트 보기](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events)를 참조하십시오.

{{site.data.keyword.cloudaccesstrailshort}} 이벤트는 자동으로 조치가 발생한 동일한 지역 내의 {{site.data.keyword.cloudaccesstrailshort}} 서비스로 전달됩니다. 
