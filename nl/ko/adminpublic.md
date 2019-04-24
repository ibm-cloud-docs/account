---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-08"

keywords: create account, IBMid, sign up for account, sign up

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# {{site.data.keyword.Bluemix_notm}} 등록
{: #signup}

기존 IBM ID를 사용하거나, 새 IBM ID를 작성하여 {{site.data.keyword.Bluemix}} 계정을 등록할 수 있습니다. 회사가 싱글 사인온(SSO)용으로 연합 ID를 사용하도록 등록된 경우, 연합 ID를 사용하여 등록하십시오.
{:shortdesc}

| 등록 ID |세부사항 |    
|-----------------|---------|
|기존 IBM ID   |IBM ID가 이미 있는 경우 기타 IBM 제품과 서비스에 사용하는 기존 인증 정보로 {{site.data.keyword.Bluemix_notm}}에 등록하십시오. |
|새 IBM ID        | IBM ID가 없는 경우에는 등록할 때 작성할 수 있습니다. IBM ID를 사용하면 {{site.data.keyword.Bluemix_notm}}를 비롯하여 모든 IBM 제품과 서비스에 하나의 사용자 이름을 사용하여 로그인할 수 있습니다. |
|연합 ID     |사용자 회사가 회사 도메인에서 생성된 사용자 인증 정보를 IBM에 등록하도록 요청한 경우 회사의 로그인에 이미 사용하고 있는 인증 정보를 이용해 {{site.data.keyword.Bluemix_notm}}에 등록할 수 있습니다. 등록할 때 전화번호를 입력해야 합니다. |
{:caption="표 1. {{site.data.keyword.Bluemix_notm}}에 등록하기 위한 ID 옵션" caption-side="top"}

## 신규 또는 기존 IBM ID로 등록
{: #signup-ibmid}

연합 ID를 사용하는 회사의 일원이 아닌 경우, IBM ID를 사용하여 {{site.data.keyword.Bluemix_notm}}에 등록하십시오.

1. [{{site.data.keyword.Bluemix_notm}} 로그인 페이지](https://cloud.ibm.com/){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon")로 이동하여 **{{site.data.keyword.Bluemix_notm}} 계정 작성**을 클릭하십시오.
1. IBM ID 이메일 주소를 입력하십시오. 기존 IBM ID가 없는 경우, 사용자가 입력한 이메일을 기반으로 하여 ID가 작성됩니다.
1. 사용자의 정보로 나머지 필드를 완료하고 **계정 작성**을 클릭하십시오.


## 연합 ID로 등록
{: #signup-federated}

연합 ID는 도메인과 사용자 인증 정보를 사용하여 IBM 웹 애플리케이션에 액세스할 수 있도록 IBM에 등록된 회사의 도메인 내에서 사용되는 ID입니다. 사용자 회사가 이미 IBM에 등록된 경우에만 연합 ID를 사용하여 {{site.data.keyword.Bluemix_notm}}에 등록할 수 있습니다. 회사의 도메인을 IBM에 등록하면 사용자가 기존 회사 사용자 인증 정보를 사용하여 IBM 제품과 서비스에 로그인할 수 있습니다. 그런 다음 회사의 ID 제공자가 SSO를 사용하여 인증을 처리합니다.

IBM은 이 ID 연합에 SAML 2.0(Security Assertion Markup Language 2.0)을 사용합니다. SAML 2.0은 보안 도메인 간에 인증 데이터를 교환하기 위한 표준 버전입니다. 이는 조직 "ID 제공자" 및 "IBM RP(Rely Party)"(또는 서비스 제공자라고 함) 간의 정보 전달을 위한 어설션이 포함된 보안 토큰을 사용하는 XML 기반 프로토콜입니다.

사용자의 회사를 연합 ID용으로 등록하는 방법에 대한 정보는 [IBMid Enterprise Federation Adoption Guide ![External link icon](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window}를 참조하십시오. 연합 ID 등록을 요청하는 경우 오퍼링 중재자 또는 클라이언트 중재자와 같은 IBM 스폰서가 필요합니다.

### 연합 ID로 로그인
{: #login-federated}

연합 ID를 사용하여 {{site.data.keyword.Bluemix_notm}} 콘솔에 로그인하는 경우에는 회사의 로그인 페이지를 통해 로그인하도록 프롬프트가 표시됩니다. CLI를 통해 로그인하는 경우, 인증에 필요한 추가 매개변수를 지정해야 합니다. 자세한 정보는 [연합 ID로 로그인](/docs/iam?topic=iam-federated_id)을 참조하십시오.
