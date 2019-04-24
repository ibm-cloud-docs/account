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


# {{site.data.keyword.Bluemix_notm}} 액세스 문제점 해결
{: #accessing}

{{site.data.keyword.Bluemix}} 액세스와 관련한 일반적인 문제점에는 {{site.data.keyword.Bluemix_notm}}에 로그인할 수 없거나 계정이 보류 상태인 경우가 있습니다. 대부분 몇 가지 간단한 단계를 수행하여 이러한 문제점에서 복구할 수 있습니다.
{:shortdesc}


## 왜 내 비밀번호가 올바르지 않습니까?
{: #ts_logintobm}
{: troubleshoot}

{{site.data.keyword.Bluemix_notm}} 콘솔에 로그인하려면 IBM ID 또는 SoftLayer ID와 연관된 올바른 비밀번호가 있어야 합니다.

{{site.data.keyword.Bluemix_notm}}에 로그인하려고 할 때 다음 오류 메시지가 표시됩니다.
{: tsSymptoms}

`The password that you entered is not correct.`

{{site.data.keyword.Bluemix_notm}}에 로그인하는 데 사용한 비밀번호가 올바르지 않습니다.
{: tsCauses}

다음 옵션 중 하나를 사용하십시오.
{: tsResolve}
 * [내 IBM 프로파일 페이지 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://myibm.ibm.com/dashboard/){: new_window}로 이동하여 올바른 비밀번호를 사용 중인지 확인하십시오.
 * 비밀번호를 잊어버린 경우에는 **비밀번호를 잊으셨습니까?**를 클릭하여 비밀번호를 재설정하십시오.
 * IBM ID를 잊어버렸거나 비밀번호와 관련된 문제점이 지속되는 경우 전세계 IBM Registration 헬프 데스크에 지원을 요청하십시오.

{{site.data.keyword.Bluemix_notm}}에 로그인 중이며 로그인 프로세스가 어떠한 이유(예: 비밀번호 재설정)로 중단된 경우에는 콘솔로 돌아가서 로그인 프로세스를 다시 시작하십시오.
{: tip}


## 왜 내 IBM ID 또는 이메일이 인식되지 않습니까?
{: #ts_old_username}
{: troubleshoot}

이메일로 로그인하려면 각 계정에 대한 IBM ID 인증을 보유 중인지 확인해야 합니다.

{{site.data.keyword.Bluemix_notm}} 콘솔에 로그인할 때 다음 메시지가 표시됩니다.
{: tsSymptoms}

`We didn't recognize this IBMid or email.`

콘솔에 로그인하려고 시도했지만 올바른 IBM ID를 사용하지 않았습니다. 예를 들어, IBM ID의 완전한 이메일 주소를 입력하지 않았거나 이전의 사용자 이름과 비밀번호를 사용하려고 시도했습니다.
{: tsCauses}

{{site.data.keyword.Bluemix_notm}}에 로그인하려면 올바른 IBM ID와 비밀번호가 있어야 합니다.

 * IBM ID의 완전한 이메일 주소를 입력하십시오.
 {: tsResolve}
 * SoftLayer ID를 보유한 SoftLayer 사용자인 경우에는 로그인하기 전에 액세스를 보유한 각 계정의 IBM ID 인증으로 전환해야 합니다. 자세한 정보는 [IBM ID로 전환](/docs/account?topic=account-unifyingaccounts)을 참조하십시오.


## 왜 내 IBM ID가 {{site.data.keyword.Bluemix_notm}} 계정과 연관되지 않습니까?
{: #ts_unabletologin}
{: troubleshoot}

{{site.data.keyword.Bluemix_notm}}에 로그인할 때 다음 메시지가 표시됩니다.
{: tsSymptoms}

`You have reached this page because your authentication was successful, however, this IBMid is not associated with any {{site.data.keyword.Bluemix_notm}} accounts.`

올바른 IBM ID로 [{{site.data.keyword.Bluemix_notm}} 콘솔](https://{DomainName}){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")에서 로그인했지만 작성된 {{site.data.keyword.Bluemix_notm}} 계정이 없습니다.
{: tsCauses}

{{site.data.keyword.Bluemix_notm}} 계정을 작성하려면 등록 프로세스를 따르십시오.
{: tsResolve}


## 왜 내 IBM ID를 사용하여 로그인할 때 콘솔이 열리지 않습니까?
{: #ts_login_stalls}
{: troubleshoot}

로그인 성공 메시지를 받았지만 콘솔로 돌아가지 않습니다.

IBM ID를 사용하여 로그인하면 로그인 성공 메시지가 표시되지만 [{{site.data.keyword.Bluemix_notm}} 콘솔](https://{DomainName}){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")로 돌아가지 않습니다.
{: tsSymptoms}

다음 옵션 중 하나를 사용하십시오.
{: tsResolve}
 * 브라우저를 닫고 캐시 및 쿠키를 지운 다음 다시 로그인을 시도하십시오.
 * [{{site.data.keyword.Bluemix_notm}} 콘솔](https://{DomainName}){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")에서 로그인하십시오.


## 왜 내 IBM ID 로그인이 완료되지 않았습니까?
{: #ts_login_ibmid}
{: troubleshoot}

{{site.data.keyword.Bluemix_notm}}에 로그인 중이며 IBM ID의 인증이 완료되지 않은 경우에는 서비스에 문제가 있을 수 있습니다.

{{site.data.keyword.Bluemix_notm}}에 로그인하면 IBM ID 인증이 완료되지 않습니다.
{: tsSymptoms}

IBM 인증 서비스에 문제점이 있을 수 있습니다.
{: tsCauses}

[IBM](https://idaas.iam.ibm.com/idaas/mtfim/sps/authsvc?PolicyId=urn:ibm:security:authentication:asf:basicldapuser){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")에 로그인할 수 있는지 확인하십시오. 로그인할 수 있으면 이는 애플리케이션 문제이며 나중에 다시 콘솔에 로그인을 시도할 수 있습니다. 해당 페이지에 로그인할 수 없는 경우에는 [IBM ID 헬프 데스크 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}에 문의하십시오.  
{: tsResolve}


## 왜 계정을 등록한 후에 즉시 로그인할 수 없습니까?
{: #ts_accntpding}
{: troubleshoot}

계정이 보류 중인 경우 {{site.data.keyword.Bluemix_notm}}에 로그인할 수 없습니다.

{{site.data.keyword.Bluemix_notm}} Lite 계정에 등록한 후에는 {{site.data.keyword.Bluemix_notm}}에 로그인할 수 없습니다. 다음 메시지가 표시됩니다.
{: tsSymptoms}

<code>Your account is pending. Please wait up to 24 hours for email confirmation and also check your spam folder. If you still have not received your email confirmation, contact <a href="http://ibm.biz/bluemixsupport.com" target="_blank">{{site.data.keyword.Bluemix_notm}} Support</a>.</code>

{{site.data.keyword.Bluemix_notm}} Lite 계정에 등록하면 등록 확인을 위해 반드시 클릭해야 하는 링크가 포함된 이메일을 수신합니다.  
{: tsCauses}

확인 이메일은 IBM ID와 연관된 이메일 주소로 발송됩니다. 받은 편지함과 스팸 폴더를 확인하십시오. 확인 이메일을 받지 못한 경우, [{{site.data.keyword.Bluemix_notm}} Support](/docs/get-support?topic=get-support-getting-customer-support)에 문의하십시오.  
{: tsResolve}


## 왜 로드되지 않는 콘솔 페이지가 나타납니까?
{: #ts_err}
{: troubleshoot}

{{site.data.keyword.Bluemix_notm}} 콘솔을 사용하면 콘솔 페이지를 로드하지 못할 수 있습니다. 대신, BXNUI0001E 또는 BXNUI0016E 오류 메시지가 표시될 수 있습니다.

다음과 같은 오류 메시지 중 하나가 표시될 수 있습니다.
{: tsSymptoms}

`BXNUI0001E: {{site.data.keyword.Bluemix_notm}}에서 세션이 있는지 발견하지 못했으므로 페이지가 로드되지 않았습니다.`

`BXNUI0016E: {{site.data.keyword.Bluemix_notm}} 페이지가 로드되지 않았으므로 앱과 서비스가 검색되지 않았습니다.`

필요에 따라 다음 조치 중 하나 이상을 완료하십시오.
{: tsResolve}

  * 브라우저를 새로 고치거나 다시 시작하십시오.
  * {{site.data.keyword.Bluemix_notm}}에서 로그아웃한 후 다시 로그인하십시오.
  * 브라우저의 개인용 브라우징 모드를 사용하십시오.
  * 브라우저의 쿠키와 캐시를 지우십시오.
  * 다른 브라우저를 사용하십시오. {{site.data.keyword.Bluemix_notm}}에서 지원하는 브라우저 버전에 대한 정보는 [{{site.data.keyword.Bluemix_notm}} 필수 소프트웨어](/docs/overview?topic=overview-prereqs-platform)를 참조하십시오.
  * Cloud Foundry 명령행 인터페이스를 설치한 경우에는 `ibmcloud cf apps` 명령을 입력하여 앱이 실행 중인지 확인하십시오.
