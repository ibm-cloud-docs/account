---

copyright:

  years: 2015, 2018

lastupdated: "2017-11-07"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 계정 관리 문제점 해결
{: #managingaccounts}

계정 관리와 관련한 일반 문제점에는 여러 앱이 동일한 도메인 이름을 공유하거나 관리자가 일부 조직을 볼 수 없는 경우가 포함됩니다. 대부분 몇 가지 간단한 단계를 수행하여 이러한 문제점에서 복구할 수 있습니다.
{:shortdesc}

## 다른 {{site.data.keyword.Bluemix_notm}} 지역에 액세스할 수 없음
{: #nosecondreg}

새 {{site.data.keyword.Bluemix_notm}} 지역을 작성하려고 시도하면 오류 메시지를 수신합니다.
{: tsSymptoms}

아마도 하나의 퍼블릭 지역에서만 개발을 지원하는 라이트 계정을 사용 중이기 때문입니다. 사용자는 계정이 처음 설정될 때 작업할 {{site.data.keyword.Bluemix_notm}} 퍼블릭 지역을 선택합니다.
{: tsCauses}

라이트 계정을 사용하는 경우 추가 지역에 액세스하기 위해 청구 가능 계정으로 업그레이드할 수 있습니다. **관리 > 청구 및 사용량 > 청구** 페이지로 이동하여 **신용카드 추가**를 클릭하십시오. **청구** 페이지에서 라이트 계정을 보유 중인지 확인할 수도 있습니다.
{: tsResolve}

## 새 조직을 작성할 수 없음
{: #nosecondorg}

새 조직을 작성하려고 시도하면 오류 메시지를 수신합니다.
{: tsSymptoms}

아마도 하나의 조직에서만 개발을 지원하는 라이트 계정을 사용 중이기 때문입니다. 사용자는 계정이 처음 설정될 때 조직을 작성합니다.
{: tsCauses}

라이트 계정이 있는 경우에는 추가 조직에 액세스하기 위해 청구 가능 계정으로 업그레이드할 수 있습니다. **관리 > 청구 및 사용량 > 청구** 페이지로 이동하여 **신용카드 추가**를 클릭하십시오. **청구** 페이지에서 라이트 계정을 보유 중인지 확인할 수도 있습니다.
{: tsResolve}

## 새 라이트 플랜 인스턴스를 작성할 수 없음
{: #nosecondlite}

새 라이트 플랜 인스턴스를 작성하려고 시도하면 다음과 같은 오류 메시지를 수신합니다.
{: tsSymptoms}

`Unable to provision new Lite instance`

무료로 제공되는 라이트 플랜에는 라이트 플랜 인스턴스당 한 개 인스턴스의 한계가 있습니다.
{: tsCauses}

청구 가능 계정에서 사용 가능한 청구 가능 서비스 플랜 중 하나를 선택하여 서비스의 추가 인스턴스를 작성할 수 있습니다. 콘솔에서 청구 가능 계정으로 업그레이드하려면 **관리 > 청구 및 사용량 > 청구** 페이지로 이동하여 **신용카드 추가**를 클릭하십시오.
{: tsResolve}

라이트 계정에서 업그레이드를 원하지 않으며 기존 라이트 서비스 인스턴스를 더 이상 사용하지 않는 경우 대시보드에서 기존 라이트 플랜 인스턴스를 삭제한 후에 새 인스턴스를 작성할 수 있습니다.

## 런타임 메모리 허용량 초과
{: #noruntimemem}

앱을 배치할 수 없으며 조직의 메모리 한계를 초과했다는 오류가 수신됩니다.
{: tsSymptoms}

라이트 계정에서 Cloud Foundry 앱은 최대 256MB의 바로 사용 가능한 런타임 메모리를 사용할 수 있습니다. 청구 가능 계정의 메모리 한계는 2GB입니다.
{: tsCauses}

라이트 계정을 사용 중인 경우에는 청구 가능 계정으로 업그레이드하여 추가 메모리를 확보할 수 있습니다. **관리 > 청구 및 사용량 > 청구** 페이지로 이동하여 **신용카드 추가**를 클릭하십시오.
{: tsResolve}

라이트 계정에서 업그레이드를 원하지 않지만 일부 유휴 상태의 앱이 있는 경우에는 유휴 상태 앱을 삭제하여 일부 런타임 메모리를 확보할 수 있습니다.

## 계정이 비활성화됨
{: #ts_accnt_inactive}

계정이 비활성 상태일 경우 {{site.data.keyword.Bluemix_notm}}에서 앱을 작성할 수 없습니다. 이 문제점을 해결하려면 지원 팀에 문의해야 합니다.

{{site.data.keyword.Bluemix_notm}}에서 앱을 작성하려고 할 때 다음과 같은 오류 메시지가 표시됩니다.
{: tsSymptoms}

`BXNUI0096E: 앱이 작성되지 않았습니다. 계정이 취소되었거나 일시중단되었기 때문에 계정이 비활성 상태입니다.`

계정이 취소되었거나 일시중단된 경우 {{site.data.keyword.Bluemix_notm}} 계정의 상태가 비활성화됩니다.
{: tsCauses}

계정을 다시 활성화하려면 [{{site.data.keyword.Bluemix_notm}} 지원 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibm.biz/bluemixsupport.com){: new_window}에 문의하십시오. 이메일에 다음 정보를 포함하십시오.
{: tsResolve}

  * {{site.data.keyword.Bluemix_notm}}에 로그인하는 데 사용하는 IBM ID.
  * 작성하는 앱이 속할 조직의 이름. 이 정보는 지원 팀이 조직의 사용자에게 올바른 역할 또는 멤버십이 지정되었는지 판별하는 데 도움이 됩니다.

## 사용자를 조직에 추가할 수 없음
{: #ts_adduser}

동일한 조직에서 작업할 사용자를 두 명 이상 초대할 수 있습니다. 계정 소유자이거나 조직의 관리자이자 구성원인 경우에만 조직에 사용자를 추가할 수 있습니다.

**조직 관리** 섹션에서 **새 사용자 초대** 링크를 볼 수 없습니다.
{: tsSymptoms}

다음 {{site.data.keyword.Bluemix_notm}} 사용자만 사용자를 조직에 초대할 수 있습니다.
{: tsCauses}
  * 조직의 계정 소유자
  * 조직의 협업자가 아니라 구성원인 조직 관리자

{{site.data.keyword.Bluemix_notm}}에서 사용자는 조직의 구성원이거나 협업자일 수 있습니다.

<dl><dt>협업자</dt>
<dd>{{site.data.keyword.Bluemix_notm}} 계정을 이미 가지고 있으며 다른 사용자가 조직에 사용자를 초대한 경우에는 조직의 협업자가 됩니다.</dd>
<dt>구성원</dt>
<dd>{{site.data.keyword.Bluemix_notm}} 계정은 없지만 다른 사용자가 조직에 사용자를 초대하고 초대에서 {{site.data.keyword.Bluemix_notm}}에 등록한 경우에는 조직의 구성원이 됩니다.</dd>
</dl>

조직의 협업자인 경우에는 조직 관리자로 지정되었더라도 조직에 사용자를 초대할 수 없습니다.

**참고:** 조직의 협업자를 비롯한 모든 조직 관리자는 이미 조직에 있는 사용자를 추가, 수정 및 제거할 수 있습니다.

조직에 사용자를 초대할 수 없으며 이를 수행하기 위해 다른 역할이 필요한 경우 조직 관리자에게 문의하여 역할을 변경하십시오. 조직 관리자를 확인하려면 다음 단계를 수행하십시오.
{: tsResolve}

  1. 콘솔 메뉴 표시줄에서 **관리 > 계정 > 조직**을 클릭하십시오.
  2. 자신의 조직으로 이동하여 **사용자** 탭에서 조직 관리자에 대한 정보를 확인하십시오.  

구성원이 아닌 협업자이기 때문에 사용자를 초대할 수 없는 경우 이전 {{site.data.keyword.Bluemix_notm}} 계정을 삭제한 다음 조직의 구성원으로 계정을 결합하도록 초대 받아야 합니다. 이전 계정을 삭제하고 구성원으로 계정에 참여하려면 다음 단계를 수행하십시오.

  1. [{{site.data.keyword.Bluemix_notm}} 지원 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibm.biz/bluemixsupport){: new_window}에 문의하여 지원 티켓을 열고 계정 삭제를 요청하십시오. 이전 계정과 연관된 데이터가 있어 이 데이터를 저장한 다음 새 계정으로 이동하려면 이메일에 이 정보를 포함시키십시오.
  2. 계정이 삭제되면 조직 관리자 역할을 보유한 사용자가 자신을 조직 관리자로 조직에 초대하도록 하십시오. 그런 다음 초대장을 통해 {{site.data.keyword.Bluemix_notm}}에 등록하십시오.

## 사용자 일괄 등록이 지원되지 않음
{: #ts_batchregistration}

{{site.data.keyword.Bluemix_notm}}에 사용자를 등록할 경우 각 사용자를 개별적으로 등록해야 합니다.

{{site.data.keyword.Bluemix_notm}}는 여러 사용자를 동시에 등록하는 기능을 제공하지 않습니다.
{: tsSymptoms}

{{site.data.keyword.Bluemix_notm}}에서는 사용자 일괄 등록을 지원하지 않습니다. {{site.data.keyword.Bluemix_notm}}에 사용자를 등록하려면 각 사용자를 개별적으로 등록해야 합니다.
{: tsCauses}

{{site.data.keyword.Bluemix_notm}}에 여러 사용자를 등록하려면 사용자마다 다음 단계를 완료하십시오.
{: tsResolve}

  1. {{site.data.keyword.Bluemix_notm}} 콘솔에서 **등록**을 클릭하십시오.
  2. 마법사의 안내에 따라 단계를 완료하십시오.

## 현재 조직과 연관된 영역이 없음
{: #ts_no_space}

현재 조직과 연관된 영역이 없으면 앱을 작성할 수 없습니다.

{{site.data.keyword.Bluemix_notm}}에서 앱을 작성하려고 할 때 다음과 같은 오류 메시지가 표시됩니다.
{: tsSymptoms}

`BXNUI0097E: 앱을 추가하려면 하나 이상의 영역을 조직 및 지역과 연관시켜야 합니다. 대시보드에서 영역 작성을 클릭하십시오. 영역이 작성되면 다시 시도하십시오.`

{{site.data.keyword.Bluemix_notm}}의 앱은 조직 아래 영역에 작성되어야 합니다.
{: tsCauses}

영역을 작성하려면 다음 방법 중 하나를 사용하십시오.
{: tsResolve}

  * 콘솔 메뉴 표시줄에서 **관리 > 계정 > 조직**을 클릭하십시오. 그런 다음, 영역을 작성하려는 조직을 선택하고 **영역 작성**을 클릭하십시오.
  * cf 명령 인터페이스에서 `cf create-space <space_name> -o <organization_name>`를 입력하십시오.


## 앱이 동일한 도메인 이름을 공유함
{: #ts_domain_diff}

여러 앱이 {{site.data.keyword.Bluemix_notm}}에서 동일한 URL을 공유할 수 있습니다.

이 문제점은 한 영역의 서로 다른 앱에 대해 동일한 URL 라우트를 지정한 경우에 발생할 수 있습니다.
{: tsCauses}

예를 들어, myApp1 앱을 {{site.data.keyword.Bluemix_notm}}로 푸시하고 도메인을 "mynewapp.stage1.mybluemix.net"으로 설정하십시오. 그런 다음 다른 myApp2 앱을 동일한 영역으로 푸시하고 URL 라우트 중 하나를 "mynewapp.stage1.mybluemix.net"으로 설정하십시오. 이제 라우트가 두 앱 모두에 맵핑됩니다.

이는 {{site.data.keyword.Bluemix_notm}}의 지원되는 동작이므로 이 동작을 사용하여 앱 업그레이드 시 무중단을 실현할 수 있습니다. 자세한 정보는 [Using Blue-Green Deployment to Reduce Downtime and Risk ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://docs.cloudfoundry.org/devguide/deploy-apps/blue-green.html){: new_window}를 참조하십시오.
{: tsResolve}


## 관리자는 {{site.data.keyword.Bluemix_notm}} 사용자 인터페이스를 사용하여 모든 조직을 볼 수 없음
{: #ts_ui_org}

관리자는 {{site.data.keyword.Bluemix_notm}} 사용자 인터페이스를 사용할 때 모든 조직을 표시하여 관리할 수 없습니다. 관리자가 속한 조직만 표시하고 관리할 수 있습니다.

관리자는 {{site.data.keyword.Bluemix_notm}} 사용자 인터페이스를 사용하여 모든 조직을 볼 수는 없습니다.
{: tsSymptoms}

이는 {{site.data.keyword.Bluemix_notm}} 사용자 인터페이스의 제한사항입니다.
{: tsCauses}

cf 명령행 인터페이스에서 `cf orgs`, `cf create-org` 및 `cf delete-org`와 같은 명령을 사용하여 모든 조직을 관리할 수 있습니다. cf 명령의 전체 목록을 보려면 `cf help`를 입력하십시오.
{: tsResolve}

## 신용카드를 추가할 수 없음
{: #ts_addcc}

평가판 계정을 종량과금제 계정으로 변환하기 위해 신용카드 정보를 제출할 수 없습니다.

신용카드 추가 페이지의 **제출** 단추가 비활성화되어 있습니다.
{: tsSymptoms}

이 문제점은 신용카드 추가 페이지에 정보가 올바르게 채워지지 않은 경우에 발생합니다.
{: tsCauses}


다음 단계를 수행하십시오.
{: tsResolve}

  1. 신용카드 추가 페이지에서 연락처 정보, 연락처 주소, 청구 주소 섹션에 있는 모든 필수 필드에 정보를 입력하십시오.
  2. **IBM 이용 약관을 읽고 동의함**을 선택한 다음 **제출**을 클릭하십시오. **결제 방법** 섹션이 표시됩니다.
  3. 신용카드 번호, 카드 만기 날짜 및 카드 상의 보안 코드를 입력하십시오. 그런 다음 **제출**을 클릭하십시오.
