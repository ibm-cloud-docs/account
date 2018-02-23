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


# {{site.data.keyword.Bluemix_notm}} 액세스 문제점 해결
{: #accessing}

{{site.data.keyword.Bluemix}} 액세스와 관련한 일반적인 문제점에는 {{site.data.keyword.Bluemix_notm}}에 로그인할 수 없거나 계정이 보류 상태인 경우가 있습니다. 대부분 몇 가지 간단한 단계를 수행하여 이러한 문제점에서 복구할 수 있습니다.
{:shortdesc}

## 올바르지 않은 비밀번호
{: #ts_logintobm}

{{site.data.keyword.Bluemix_notm}} 콘솔에 로그인하려면 IBM ID와 연관된 올바른 비밀번호가 있어야 합니다.

[{{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com){: new_window}을 통해 로그인하려면 IBM ID 또는 연결된 계정 ID와 연관된 올바른 비밀번호가 있어야 합니다.

{{site.data.keyword.Bluemix_notm}}에 로그인하려고 할 때 다음 오류 메시지가 표시됩니다.
{: tsSymptoms}

`입력한 비밀번호가 올바르지 않습니다.`

{{site.data.keyword.Bluemix_notm}}에 로그인하는 데 사용한 비밀번호가 올바르지 않습니다.
{: tsCauses}

다음 솔루션 중 하나를 사용하십시오.
{: tsResolve}
 * 올바른 비밀번호를 입력하십시오. IBM ID와 비밀번호가 올바른지 확인하기 위해 내 IBM 프로파일 페이지로 이동하여 **로그인**을 클릭하고 로그인 페이지에 IBM ID와 비밀번호를 입력할 수 있습니다.
 * 비밀번호를 잊어버린 경우에는 **비밀번호를 잊으셨습니까?**를 클릭하여 비밀번호를 재설정하십시오. 그런 다음 [{{site.data.keyword.Bluemix_notm}} 콘솔 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}){: new_window} 또는 [{{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com){: new_window}로 돌아간 후 다시 로그인하십시오.
 * IBM ID를 잊어버렸거나 비밀번호와 관련된 문제점이 지속되는 경우 전세계 IBM Registration 헬프 데스크에 지원을 요청하십시오.
 * 올바른 IBM ID 및 비밀번호를 얻으려면 내 IBM 프로파일 페이지로 이동한 다음 **등록**을 클릭하십시오.

참고:
<!-- begin STAGING ONLY -->
 * IBM 직원의 경우 IBM ID와 인트라넷 ID는 서로 다를 수 있습니다.
 <!-- end STAGING ONLY -->
 * IBM 페이지에 로그인되어 있으며 특정 이유(예: 비밀번호 재설정)로 인해 로그인 프로세스가 중단된 경우에는 [{{site.data.keyword.Bluemix_notm}} 콘솔 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}){: new_window} 또는 [{{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com){: new_window}로 돌아가서 로그인 프로세스를 다시 시작하십시오.


## 올바르지 않은 로그인 신임 정보
{: #ts_login_invalid_credentials}

IBM ID를 사용하여 로그인할 때 다음 메시지가 표시됩니다.
{: tsSymptoms}

올바르지 않은 로그인 신임 정보가 제공되었습니다. IBM ID가 계정과 연관되어 있는 경우 여기에 로그인하십시오.`

* IBM ID로 전환되었지만 이전 사용자 이름과 비밀번호를 사용하여 [{{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com){: new_window}을 통해 로그인을 시도했습니다.
{: tsCauses}

* [{{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com){: new_window}을 통해 로그인을 시도했지만 사용자 이름과 비밀번호 필드에 IBM ID 및 비밀번호를 입력했습니다.

메시지에서 **여기에 로그인**을 클릭하거나 IBM ID 계정 로그인 섹션으로 이동하고 **IBM ID로 로그인**을 클릭하십시오.
{: tsResolve}

이전 ID와 사용한 **사용자 이름** 및 **비밀번호** 필드는 사용하지 마십시오.


## 인식할 수 없는 IBM ID 또는 이메일
{: #ts_old_username}

{{site.data.keyword.Bluemix_notm}} 콘솔에 로그인할 때 다음 메시지가 표시됩니다.
{: tsSymptoms}

`이 IBM ID 또는 이메일을 인식할 수 없습니다.`

{{site.data.keyword.Bluemix_notm}} 콘솔에 로그인하려고 했지만 올바른 IBM ID를 사용하지 않았습니다. 예를 들어, IBM ID의 완전한 이메일 주소를 입력하지 않았거나 이전의 사용자 이름 및 비밀번호를 사용하려고 시도했습니다.
{: tsCauses}

{{site.data.keyword.Bluemix_notm}}에 로그인하려면 올바른 IBM ID와 비밀번호가 있어야 합니다.

 * IBM ID의 완전한 이메일 주소를 입력했는지 확인하십시오.
 {: tsResolve}
 * {{site.data.keyword.BluSoftlayer_full}} ID를 보유한 {{site.data.keyword.BluSoftlayer_full}} 사용자인 경우에는 IBM ID 인증을 사용하여 로그인하기 전에 액세스를 보유한 각 계정마다 {{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털에서 IBM ID 인증으로 전환해야 합니다.
 자세한 정보는 [IBM ID로 전환](/docs/account/softlayerlink.html#switching-to-ibmid)을 참조하십시오.


## IBM ID가 IBM Cloud 계정과 연관되어 있지 않음
{: #ts_login_noswitch}

IBM ID를 사용하여 로그인할 때 다음 메시지가 표시됩니다.
{: tsSymptoms}

`인증에 성공하여 이 페이지로 이동되었습니다. 하지만 이 IBM ID는 IBM Cloud 계정과 연관되어 있지 않습니다. 오류로 간주되면 계정 소유자 또는 마스터 사용자에게 문의하십시오.`

올바른 IBM ID로 [{{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com){: new_window}에 로그인했지만, {{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털에서 IBM ID 인증으로 전환되지 않았습니다.
{: tsCauses}

다음 검사를 완료하십시오.
{: tsResolve}
 * IBM ID 인증으로 전환할 수 있는지 확인하려면 마스터 사용자 또는 계정 관리자에게 문의하십시오.
 * IBM ID로 전환 단계를 완료했는지 확인하십시오. [IBM ID로 전환](/docs/account/softlayerlink.html#switching-to-ibmid)을 참조하십시오.
 * **사용자 ID를 IBM ID와 연관** 이메일에 있는 조치대로 수행하고 있는지 확인하십시오. 받은 편지함 및 정크 메일 폴더에서 이메일을 확인하십시오. 이메일을 다시 받으려면(예: 만료된 경우) {{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털에서 사용자 프로파일 편집 페이지로 이동하여 **이메일 재발송**을 클릭하십시오. 또는 [{{site.data.keyword.Bluemix_notm}} 지원 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibm.biz/bluemixsupport.com){: new_window}에 문의하십시오.

**참고:** IBM ID로 직접 자신의 IBM ID를 작성한 경우에는 처리할 두 개의 이메일을 수신합니다(IBM ID 등록 및 {site.data.keyword.Blu_full}}에서 각각 1개). 두 개의 이메일에 있는 조치를 따라야 합니다.

계정 설정의 방법에 따라 로그인 옵션 중 일부가 적용될 수 있습니다.
 * {{site.data.keyword.BluSoftlayer_full}} ID를 보유한 {{site.data.keyword.BluSoftlayer_notm}} 사용자는 [{{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com){: new_window}을 통해 로그인해야 합니다.
 * IBM ID를 보유한 {{site.data.keyword.BluSoftlayer_notm}} 사용자는 연결된 {{site.data.keyword.Bluemix_notm}} 계정을 보유하고 있는지와 상관없이 [{{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com){: new_window}을 통해 로그인하여 {{site.data.keyword.BluSoftlayer_notm}}을 열거나 [{{site.data.keyword.Bluemix_notm}} 콘솔 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}){: new_window}을 통해 로그인하여 인프라 대시보드를 열 수 있습니다.


## IBM ID가 {{site.data.keyword.Bluemix_notm}} 계정과 연관되어 있지 않음
{: #ts_unabletologin}

{{site.data.keyword.Bluemix_notm}}에 로그인할 때 다음 메시지가 표시됩니다.
{: tsSymptoms}

`인증에 성공하여 이 페이지로 이동되었습니다. 하지만 이 IBM ID는 {{site.data.keyword.Bluemix_notm}} 계정과 연관되어 있지 않습니다.`

올바른 IBM ID로 [{{site.data.keyword.Bluemix_notm}} 콘솔 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}){: new_window}에서 로그인했지만 {{site.data.keyword.Bluemix_notm}} 계정이 아직 작성되지 않았습니다.
{: tsCauses}

{{site.data.keyword.Bluemix_notm}} 계정을 작성하려면 등록 프로세스를 따르십시오.
{: tsResolve}

계정 설정의 방법에 따라 로그인 옵션 중 일부가 적용될 수 있습니다.
 * 연결된 계정이 없는 {{site.data.keyword.Bluemix_notm}} 사용자는 {{site.data.keyword.Bluemix_notm}} 콘솔을 통해 로그인해야 합니다.
 * 연결된 계정이 있는 {{site.data.keyword.Bluemix_notm}} 사용자는 [{{site.data.keyword.Bluemix_notm}} 콘솔 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}){: new_window} 또는 [{{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com){: new_window}을 통해 로그인할 수 있습니다.


## 콘솔이 열리지 않음
{: #ts_login_stalls}

IBM ID를 사용하여 로그인하면 로그인 성공 메시지가 표시되지만, [{{site.data.keyword.Bluemix_notm}} 콘솔 ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.{DomainName}){: new_window} 또는 [{{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com){: new_window}로 돌아가지 않습니다.
{: tsSymptoms}

다음 솔루션 중 하나를 사용하십시오.
{: tsResolve}
 * 브라우저를 닫고 캐시 및 쿠키를 지운 다음 다시 로그인을 시도하십시오.
 * IBM ID 인증 서비스에서 직접 로그인하지 않고 [{{site.data.keyword.Bluemix_notm}} 콘솔 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.{DomainName}){: new_window} 또는 [{{site.data.keyword.BluSoftlayer_notm}} 인프라 고객 포털 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://control.softlayer.com){: new_window}에서 로그인하는지 확인하십시오.


## IBM ID 로그인이 완료되지 않음
{: #ts_login_ibmid}

{{site.data.keyword.Bluemix_notm}}에 로그인하면 IBM ID 인증이 완료되지 않습니다.
{: tsSymptoms}

IBM 인증 서비스에 문제점이 있을 수 있습니다.
{: tsCauses}

[IBM IBM ID ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://new.wind.ibmcloud.com/webapp/#/status/a1a0c5d743d94a6a9597087541564d8e){: new_window}에서 서비스의 상태를 확인한 후에 다시 시도하십시오.
{: tsResolve}


## 계정이 보류 중임
{: #ts_accntpding}

계정이 보류 중인 경우 {{site.data.keyword.Bluemix_notm}}에 로그인할 수 없습니다.

{{site.data.keyword.Bluemix_notm}} 평가판 계정에 등록한 후에는 {{site.data.keyword.Bluemix_notm}}에 로그인할 수 없습니다. 다음 메시지가 표시됩니다.
{: tsSymptoms}

<code>사용자 계정이 보류 중입니다. 사용자 계정의 이메일 확인을 위해 최대 24시간 동안 기다려야 할 수 있습니다. 스팸 폴더도 확인하십시오. 아직 이메일 확인을 받지 못한 경우에는 <a href="http://ibm.biz/bluemixsupport.com" target="_blank">{{site.data.keyword.Bluemix_notm}} 지원</a>에 문의하십시오.</code>

{{site.data.keyword.Bluemix_notm}} 평가판 계정에 등록하면 확인 이메일을 받게 됩니다. 확인 이메일에 있는 링크를 클릭하여 등록 프로세스를 완료해야 합니다.
{: tsCauses}

확인 이메일이 사용자가 제공한 이메일 주소로 전송됩니다. 받은 편지함과 스팸 폴더를 확인하십시오. 확인 이메일을 수신하지 못한 경우 [{{site.data.keyword.Bluemix_notm}} 지원 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](http://ibm.biz/{{site.data.keyword.Bluemix_notm}}support.com){: new_window}에 문의하십시오.  
{: tsResolve}


<!-- begin STAGING ONLY -->

## 외부 웹 사이트 액세스 문제점
{: #ts_bmlinkid}

IBM 인트라넷 ID를 사용하여 {{site.data.keyword.Bluemix_notm}}에 로그인하려면 IBM ID로 인트라넷 ID를 연결해야 합니다.

{{site.data.keyword.Bluemix_notm}} 로그인 페이지에서 **인트라넷 ID로 로그인**을 선택하면 다음 메시지가 표시됩니다.
{: tsSymptoms}

`외부 웹 사이트 액세스 문제점`

IBM ID에 연결되지 않은 IBM 인트라넷 ID를 사용하여 {{site.data.keyword.Bluemix_notm}}에 로그인할 때 이러한 문제점이 발생합니다. IBM ID는 www.ibm.com에 로그인하는 데 사용하는 ID입니다.
{: tsCauses}

IBM 직원이 IBM 인트라넷 ID를 사용하여 {{site.data.keyword.Bluemix_notm}}에 로그인하려면 외부 IBM ID에 인트라넷 ID를 연결해야 합니다. 두 개의 ID를 연결하려면 다음 단계를 완료하십시오.
{: tsResolve}

  1. [Central Sign-on ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://w3-03.sso.ibm.com/tools/cso/index.jsp){: new_window} 페이지에서 **My Sign-ons**를 클릭하십시오.
  2. My Sign-ons 페이지에서 **Link IDs**를 클릭하고 {{site.data.keyword.Bluemix_notm}} 로그인 페이지에 IBM ID와 비밀번호를 입력하십시오. 그러면 인트라넷 ID와 IBM ID가 자동으로 연결됩니다.


<!-- end STAGING ONLY -->

## {{site.data.keyword.Bluemix_notm}} 페이지를 로드할 수 없음
{: #ts_err}

{{site.data.keyword.Bluemix_notm}} 콘솔을 사용하면 콘솔 페이지를 로드하지 못할 수 있습니다. 대신, BXNUI0001E 또는 BXNUI0016E 오류 메시지가 표시될 수 있습니다.

{{site.data.keyword.Bluemix_notm}} 콘솔을 사용할 경우 다음과 같은 오류 메시지가 표시될 수 있습니다.
{: tsSymptoms}

`BXNUI0001E: {{site.data.keyword.Bluemix_notm}}에서 세션이 있는지 발견하지 못했으므로 페이지가 로드되지 않았습니다.`

`BXNUI0016E: {{site.data.keyword.Bluemix_notm}} 페이지가 로드되지 않았으므로 앱과 서비스가 검색되지 않았습니다.`

필요에 따라 다음 조치 중 하나 이상을 완료하십시오.
{: tsResolve}

  * 브라우저를 새로 고치거나 다시 시작하십시오.
  * {{site.data.keyword.Bluemix_notm}}에서 로그아웃한 후 다시 로그인하십시오.
  * 브라우저의 개인용 브라우징 모드를 사용하십시오.
  * 브라우저의 쿠키와 캐시를 지우십시오.
  * 다른 브라우저를 사용하십시오. {{site.data.keyword.Bluemix_notm}}에서 지원하는 브라우저 버전에 대한 정보는 [{{site.data.keyword.Bluemix_notm}} 필수 소프트웨어](/docs/overview/whatisbluemix.html#prereqs)를 참조하십시오.
  * cf 명령행 인터페이스를 설치한 경우 `cf apps` 명령을 입력하여 앱이 실행 중인지 확인하십시오.
