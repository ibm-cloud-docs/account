---

copyright:

  years: 2015, 2019

lastupdated: "2019-02-13"
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

# 계정 관리 문제점 해결
{: #managingaccounts}

계정 관리의 일반 문제점에는 서로 다른 앱이 동일한 도메인 이름을 보유하거나 관리자가 일부 조직을 볼 수 없는 경우가 포함됩니다. 대부분 몇 가지 간단한 단계를 수행하여 이러한 문제점에서 복구할 수 있습니다.
{:shortdesc}


## 왜 내가 다른 {{site.data.keyword.Bluemix_notm}} 위치에 액세스할 수 없습니까?
{: #nosecondreg}
{: troubleshoot}

계정 유형에서 허용하지 않으므로 새 위치를 작성할 수 없습니다.

새 {{site.data.keyword.Bluemix_notm}} 위치를 작성하려고 시도하면 오류 메시지를 수신합니다.
{: tsSymptoms}

이는 하나의 공용 위치에서만 개발을 지원하는 Lite 계정을 사용 중이기 때문일 수 있습니다.
{: tsCauses}

더 많은 위치에 액세스하려면 청구 가능 계정으로 업그레이드하십시오. **관리 > 청구 및 사용량**으로 이동하여 **지불**을 선택하십시오.
{: tsResolve}


## 왜 새 조직을 작성할 수 없습니까?
{: #nosecondorg}
{: troubleshoot}

둘 이상의 조직을 작성하려고 시도하며 Lite 계정을 보유 중입니다.  

새 조직을 작성하려고 시도하면 오류 메시지를 수신합니다.
{: tsSymptoms}

이는 하나의 조직에서만 개발을 지원하는 Lite 계정을 사용 중이기 때문일 수 있습니다.
{: tsCauses}

새 조직을 작성하려면 청구 가능 계정으로 업그레이드하십시오. **관리 > 청구 및 사용량**으로 이동하여 **업그레이드**를 선택하십시오.
{: tsResolve}


## 왜 새 Lite 플랜 인스턴스를 작성할 수 없습니까?
{: #nosecondlite}
{: troubleshoot}

추가 인스턴스를 작성하려고 시도했지만 Lite 계정을 보유 중입니다.

새 Lite 플랜 인스턴스를 작성하려고 시도하면 다음과 같은 오류 메시지를 수신합니다.
{: tsSymptoms}

`Unable to provision new Lite instance`

 해당 플랜이 무료 상태를 유지할 수 있도록 Lite 플랜 인스턴스당 1개 인스턴스의 한계가 있습니다.
{: tsCauses}

청구 가능 계정에서 사용 가능한 청구 가능 서비스 플랜 중 하나를 선택하여 서비스의 추가 인스턴스를 작성할 수 있습니다. 콘솔에서 청구 가능 계정으로 업그레이드하려면 **관리 > 청구 및 사용량**으로 이동하여 **업그레이드**를 선택하십시오.
{: tsResolve}

Lite 계정에서의 업그레이드를 원하지 않으며 기존 Lite 서비스 인스턴스를 더 이상 사용하지 않는 경우에는 대시보드에서 기존 Lite 플랜 인스턴스를 삭제한 후에 새 인스턴스를 작성할 수 있습니다.


## 어떻게 런타임 메모리 허용량이 초과되었습니까?
{: #noruntimemem}
{: troubleshoot}

계정에 대해 허용된 메모리를 초과했습니다.

앱을 배치할 수 없으며 조직의 메모리 한계를 초과했음을 알리는 오류가 수신됩니다.
{: tsSymptoms}

Lite 계정에서 Cloud Foundry 앱은 최대 256MB의 바로 사용 가능한 런타임 메모리를 사용할 수 있습니다. 청구 가능 계정의 메모리 한계는 2GB입니다.
{: tsCauses}

Lite 계정을 사용 중인 경우에는 청구 가능 계정으로 업그레이드하여 추가 메모리를 확보할 수 있습니다. **관리 > 청구 및 사용량**으로 이동하여 **업그레이드**를 선택하십시오.
{: tsResolve}

Lite 계정에서의 업그레이드를 원하지 않지만 일부 유휴 상태의 앱이 있는 경우에는 이를 삭제하여 일부 런타임 메모리를 확보할 수 있습니다.


## 왜 내 계정이 비활성화되었습니까?
{: #ts_accnt_inactive}
{: troubleshoot}

계정이 비활성 상태일 경우 {{site.data.keyword.Bluemix_notm}}에서 앱을 작성할 수 없습니다. 이 문제점을 해결하려면 지원 팀에 문의해야 합니다.

{{site.data.keyword.Bluemix_notm}}에서 앱을 작성하려고 시도할 때 다음과 같은 오류 메시지가 표시됩니다.
{: tsSymptoms}

`BXNUI0096E: 앱이 작성되지 않았습니다. 계정이 취소되었거나 일시중단되었기 때문에 계정이 비활성 상태입니다.`

계정이 취소되었거나 일시중단된 경우
{{site.data.keyword.Bluemix_notm}} 계정의 상태가 비활성화됩니다.
{: tsCauses}

계정을 다시 활성화하려면 [지원 센터](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")에서 케이스를 여십시오. 케이스에 다음 정보를 포함하십시오.
{: tsResolve}

  * {{site.data.keyword.Bluemix_notm}}에 로그인하는 데 사용하는 IBM ID.
  * 작성하는 앱이 속할 조직의 이름. 이 정보는 조직에서 올바른 역할 또는 멤버십이 지정되었는지 여부를 지원 팀이 판별하는 데 도움이 될 수 있습니다.


## 왜 사용자를 조직에 추가할 수 없습니까?
{: #ts_adduser}
{: troubleshoot}

계정 소유자이거나 관리자겸 조직 구성원인 경우에만 조직에 사용자를 추가할 수 있습니다.

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

조직의 협업자를 비롯한 모든 조직 관리자는 조직에 이미 있는 사용자를 추가, 수정 및 제거할 수 있습니다.
{: note}

조직에 사용자를 초대할 수 없으며 이를 수행하기 위해 다른 역할이 필요한 경우 조직 관리자에게 문의하여 역할을 변경하십시오. 조직 관리자를 확인하려면 다음 단계를 수행하십시오.
{: tsResolve}

  1. 콘솔 메뉴 표시줄에서 **관리 > 계정**을 클릭하고 **회사 연락처**를 선택하십시오.
  2. 자신의 조직으로 이동하여 **사용자** 탭에서 조직 관리자에 대한 정보를 확인하십시오.  

구성원이 아닌 협업자이기 때문에 사용자를 초대할 수 없는 경우에는 이전 {{site.data.keyword.Bluemix_notm}} 계정을 삭제한 후에 조직 구성원으로서 계정에 참여하도록 초대되어야 합니다. 이전 계정을 삭제하고 구성원으로 계정에 참여하려면 다음 단계를 수행하십시오.

  1. [{{site.data.keyword.Bluemix_notm}} 지원 팀 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window}에 문의하여 지원 케이스를 열고 계정의 삭제를 요청하십시오. 이전 계정과 연관된 데이터가 있어 이 데이터를 저장한 다음 새 계정으로 이동하려면 이메일에 이 정보를 포함시키십시오.
  2. 계정이 삭제되면 조직 관리자 역할을 보유한 사용자가 자신을 조직 관리자로 조직에 초대하도록 하십시오. 그런 다음 초대장을 통해 {{site.data.keyword.Bluemix_notm}}에 등록하십시오.


## 왜 내 현재 조직과 연관된 영역이 없습니까?
{: #ts_no_space}
{: troubleshoot}

현재 조직과 연관된 영역이 없으면 앱을 작성할 수 없습니다.

앱을 작성하려고 시도할 때 다음과 같은 오류 메시지가 표시됩니다.
{: tsSymptoms}

`BXNUI0097E: 앱을 추가하려면 하나 이상의 영역을 조직 및 지역과 연관시켜야 합니다. 대시보드에서 영역 작성을 클릭하십시오. 영역이 작성되면 다시 시도하십시오.`

앱은 조직 아래의 영역에서 작성되어야 합니다.
{: tsCauses}

영역을 작성하려면 다음 방법 중 하나를 사용하십시오.
{: tsResolve}

  * 콘솔 메뉴 표시줄에서 **관리 > 계정**을 클릭하고 **조직**을 선택하십시오. 그런 다음, 영역을 작성하려는 조직을 선택하고 **영역 작성**을 클릭하십시오.
  * {{site.data.keyword.Bluemix_notm}} 명령행 인터페이스에서 다음 명령을 입력하십시오. `ibmcloud account space-create <space_name> -o <organization_name>`.


## 왜 일부 앱이 도메인 이름을 공유합니까?
{: #ts_domain_diff}
{: troubleshoot}

여러 앱이 {{site.data.keyword.Bluemix_notm}}에서 URL을 공유할 수 있습니다.

이 문제점은 한 영역의 서로 다른 앱에 대해 동일한 URL 라우트를 지정한 경우에 발생할 수 있습니다.
{: tsCauses}

예를 들면, 사용자가 myApp1 앱을 {{site.data.keyword.Bluemix_notm}}로 푸시하고 도메인을 `mynewapp.us-east.cf.appdomain.cloud`로 설정합니다. 그 후 다른 myApp2 앱을 동일한 영역으로 푸시하고 해당 URL 라우트 중 하나를 `mynewapp.us-east.cf.appdomain.cloud`로 설정합니다. 이제 라우트가 두 앱 모두에 맵핑됩니다.

이는 지원되는 동작이며 이 사례를 사용하여 앱 업그레이드를 위한 작동 중지 시간을 없앨 수 있습니다. 자세한 정보는 [작동 중지 시간을 없애는 방법](/docs/overview?topic=overview-zero-downtime)을 참조하십시오.
{: tsResolve}


## 왜 관리자가 콘솔을 사용하여 모든 조직을 볼 수 없습니까?
{: #ts_ui_org}
{: troubleshoot}

관리자는 {{site.data.keyword.Bluemix_notm}} 콘솔 사용 시에 관리할 모든 조직을 표시할 수 없습니다. 관리자가 속한 조직만 표시하고 관리할 수 있습니다.

관리자로서 콘솔에서 모든 조직을 볼 수 없습니다.
{: tsSymptoms}

이는 콘솔의 제한사항입니다.
{: tsCauses}

{{site.data.keyword.Bluemix_notm}} 명령행 인터페이스에서 `ibmcloud account orgs` 및 `ibmcloud account org-create`와 같은 명령을 사용하여 모든 조직을 관리할 수 있습니다. 명령의 전체 목록을 보려면 `ibmcloud account help`를 입력하십시오.
{: tsResolve}


## 왜 내 신용카드 정보를 추가할 수 없습니까?
{: #ts_addcc}
{: troubleshoot}

Lite 계정을 청구 가능 계정으로 업그레이드하기 위해 신용카드 정보를 제출할 수 없습니다.

신용카드 추가 페이지의 **제출** 단추가 비활성화되어 있습니다.
{: tsSymptoms}

이 문제점은 신용카드 추가 페이지에서 정보가 올바르게 작성되지 않은 경우에 발생합니다.
{: tsCauses}

다음 단계를 수행하십시오.
{: tsResolve}

  1. 신용카드 추가 페이지에서 모든 필수 필드를 채우십시오.
  2. **IBM 이용 약관을 읽고 동의함**을 선택한 다음 **제출**을 클릭하십시오.
