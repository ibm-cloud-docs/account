---

copyright:

  years: 2018
lastupdated: "2018-07-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 계정 계층 구조
{: #overview}

{{site.data.keyword.Bluemix}} 계정에는 상호작용하는 여러 컴포넌트와 시스템이 포함되어 있습니다. 다음 다이어그램과 각 컴포넌트에 대한 설명은 특정 컴포넌트가 어떻게 상호 관련되거나 연결되는지와 계정에서 액세스가 작동하는 방식을 이해하는 데 도움을 주기 위한 것입니다. 

<a href="https://console.stage1.bluemix.net/docs/api/content/account/images/account_diagram.svg">
  <img src="images/account_diagram.svg" alt="계정 다이어그램">
</a>

다이어그램 내에는 이해해야 할 계정 계층 구조의 컴포넌트에 대한 두 가지 기본 개념이 있습니다. 실선과 점선을 사용하여 일부 컴포넌트가 다른 컴포넌트 내에 포함되어 있음(예: 사용자가 액세스 그룹 또는 Cloud Foundry 조직에 추가됨)을 나타내는 데 도움을 줍니다. 그러나 일부 컴포넌트는 멤버십 대신 액세스를 제공하기 위해 다른 컴포넌트와 상호작용합니다. 예를 들어, 사용자는 리소스 그룹에 대한 액세스를 부여받지만 액세스 그룹에 대한 것과 동일한 방식으로 리소스 그룹의 구성원은 아닙니다. 이러한 개념은 다음 섹션에도 설명되어 있습니다.

<dl>
<dt>사용자</dt>
<dd>사용자는 계정에 초대되고 계정 내의 여러 리소스에 대한 액세스를 부여받습니다.</dd>
<dt>서비스 ID</dt>
<dd>서비스 ID는 사용자 ID가 사용자를 식별하는 방법과 비슷하게 서비스 또는 애플리케이션을 식별합니다. 작성한 서비스 ID를 사용하여 {{site.data.keyword.Bluemix_notm}} 서비스에 대해 {{site.data.keyword.Bluemix_notm}} 액세스 외부에서 애플리케이션을 사용하도록 설정할 수 있습니다. 특정 서비스 사용을 위해 권한을 제한하거나 여러 서비스에 액세스하기 위해 권한을 결합하는 특정 액세스 정책을 서비스 ID에 지정할 수 있습니다. 서비스 ID는 특정 사용자에게 묶여 있지 않으므로, 사용자가 우연히 조직을 나가게 되어 계정에서 삭제되는 경우에도 서비스 ID는 남게 되어 애플리케이션 또는 서비스가 유지되고 실행됩니다. 자세한 정보는 [서비스 ID 작성 및 작업](/docs/iam/serviceid.html#serviceids)을 참조하십시오.</dd>
<dt>서비스 인스턴스 또는 리소스</dt>
<dd>{{site.data.keyword.Bluemix_notm}}의 서비스는 리소스 그룹 또는 Cloud Foundry를 기반으로 합니다. 리소스 그룹에 추가되고 {{site.data.keyword.Bluemix_notm}} Identity and Access Management(IAM)를 사용하여 관리될 수 있는 서비스 인스턴스를 리소스라고 합니다. Cloud Foundry 조직 및 영역에 추가되는 서비스 인스턴스에는 Cloud Foundry 역할을 사용하는 별도의 액세스 관리 시스템이 있습니다. 자세한 정보는 [리소스의 개념](/docs/resources/acct_resources.html#resource)을 참조하십시오.</dd>
<dt>API 키</dt>
<dd>API(Application Programming Interface) 키는 호출 애플리케이션 또는 사용자를 식별하도록 API(Application Programming Interface)에 전달되는 고유 코드입니다. 사용자 ID와 연관된 플랫폼 API 키가 있으며 서비스 ID에 대해 작성될 수 있는 API 키가 있습니다. 자세한 정보는 [API 키 작업](/docs/iam/apikeys.html#manapikey)을 참조하십시오.</dd>
<dt>액세스 그룹</dt>
<dd>액세스 그룹을 작성하여 사용자 및 서비스 ID 세트를 단일 엔티티로 구성하고 권한을 쉽게 지정할 수 있습니다. 개별 사용자 또는 서비스 ID마다 동일한 액세스를 여러 번 지정하는 대신 그룹에 단일 정책을 지정할 수 있습니다. 자세한 정보는 [액세스 그룹 설정](/docs/iam/groups.html#groups)을 참조하십시오.</dd>
<dt>리소스 그룹</dt>
<dd>리소스 그룹은 한 번에 둘 이상의 리소스에 대한 사용자 액세스를 신속하게 지정할 수 있도록 사용자 정의할 수 있는 그룹화에서 계정 리소스를 구성하기 위한 방법입니다. IAM 액세스 제어를 사용하여 관리되는 계정 리소스는 계정 내의 리소스 그룹에 속합니다. 사용자는 리소스 그룹에 추가되지 않지만 사용자에게 리소스 그룹 내의 리소스에 대한 액세스가 제공되거나 사용자가 리소스 그룹을 관리할 수 있습니다. 리소스 그룹을 관리하기 위한 액세스 권한을 부여받은 사용자는 그룹 내에 새 인스턴스를 작성하거나, 다른 사용자의 그룹 작업 액세스 권한을 관리하거나, 지정된 IAM 역할을 기반으로 그룹 이름을 편집할 수 있습니다. 자세한 정보는 [리소스 그룹 관리](/docs/resources/resourcegroups.html#rgs) 및 [리소스 그룹 내의 리소스 구성에 대한 우수 사례](/docs/resources/bestpractice_rgs.html#bp_resourcegroups)를 참조하십시오.</dd>
<dt>Cloud Foundry 조직</dt>
<dd>계정 소유자 또는 조직 관리자는 콘솔의 Cloud Foundry 조직 페이지에서 조직 및 영역을 추가할 수 있습니다. 카탈로그에서 작성할 때 Cloud Foundry 조직 및 영역의 사용을 지원하는 서비스가 조직 및 영역에 추가됩니다. 조직에는 사용자, 도메인 및 할당량이 포함됩니다. 각 조직 내에서 서비스 인스턴스를 포함하는 영역이 추가됩니다. 자세한 정보는 [조직 및 영역 추가](/docs/account/orgs_spaces.html#orgsspacesusers)를 참조하십시오.</dd>
<dt>Cloud Foundry 영역</dt>
<dd>조직 내에서는 영역을 사용하여 애플리케이션, 서비스 및 사용자 세트를 그룹화할 수 있습니다. 영역은 {{site.data.keyword.Bluemix_notm}}에서 특정 지역과 연계됩니다. 전달 라이프사이클을 기반으로 조직에서 영역을 작성할 수 있습니다. 예를 들어, 개발 영역을 개발 환경으로, 테스트 영역을 테스트 환경으로, 프로덕션 영역을 프로덕션 환경으로 작성할 수 있습니다. 그런 다음, 앱을 영역과 연관시킬 수 있습니다. 자세한 정보는 [조직 및 영역 추가](/docs/account/orgs_spaces.html#orgsspacesusers)를 참조하십시오.</dd>
</dl>

다이어그램의 또 다른 중요한 측면은 계정 사용자에게 계정 내의 리소스에 대한 액세스를 제공하는 데 사용할 수 있는 세 가지 유형의 액세스 관리 시스템에 대한 설명입니다. 

* IAM [액세스 역할](/docs/iam/users_roles.html#iamusermanrol)은 사용자에게 리소스 그룹에 속한 모든 리소스에 대한 액세스를 제공하는 데 사용됩니다. 또한 이러한 액세스 역할은 사용자에게 리소스 그룹을 관리하고 리소스 그룹에 지정되는 새 서비스 인스턴스를 작성하기 위한 액세스 권한을 부여하는 데 사용됩니다.
* Cloud Foundry [조직 및 영역 역할](/docs/iam/cfaccess.html#cfroles)은 사용자에게 Cloud Foundry 영역에 있는 모든 서비스 인스턴스에 대한 액세스를 제공합니다.
* 인프라 [고객 포털](/docs/customer-portal/cpwhatis.html#customerportal_whatisCP) 권한은 사용자에게 고객 포털 액세스 및 고객 포털 내의 기능(예: 송장, 비용 청구, IaaS 구성, IaaS 모니터링, IaaS 구매 및 지원)에 대한 세부 단위의 [권한](/docs/iam/infrastructureaccess.html#infrapermission)을 부여하는 데 사용할 수 있습니다. 디바이스 액세스는 별도이며 디바이스 자체에서 처리됩니다.
