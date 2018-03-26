---

copyright:

  years: 2016, 2018

lastupdated: "2018-03-05"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# IBM ID로 전환 및 계정 연결
{: #unifyingaccounts}

이제 SoftLayer의 인증은 IBM ID를 사용하여 모든 {{site.data.keyword.Bluemix}}에 대해 단일 로그인을 제공합니다. IBM ID는 인프라, 서비스 및 애플리케이션 기능에 대한 액세스와 구매를 위해 {{site.data.keyword.Bluemix_notm}} 계정에 로그인하는 데 사용될 수 있는 단일 ID입니다. 모든 새 계정은 자동으로 IBM ID를 받으며, SAML 연합 계정을 제외한 기존 SoftLayer 계정은 IBM ID 인증으로 전환할 수 있도록 설정됩니다.
{:shortdesc}

## IBM ID로 전환
{: #switchtoIBMid}

IBM ID로 전환하는 프로세스를 시작하는 경우, 프로세스가 완료되기 전에 언제든지 전환을 취소할 수 있습니다. 그러나 로그인할 때마다 IBM ID로 전환하기 위한 프롬프트가 표시됩니다. {{site.data.keyword.Bluemix_notm}} 계정에 연결하려는 각 SoftLayer 계정은 고유 이메일 주소를 사용하는 고유 IBM ID에서 소유해야 합니다.

기존 SoftLayer 계정을 IBM ID로 전환하려면 IBM ID를 작성한 후에 등록 코드를 사용하여 이를 확인하십시오.

### IBM ID 및 등록 코드 요청
{: #reqIBMidandregcode}

1. SoftLayer 계정에 로그인한 후에 IBM ID로 전환하기 위한 프롬프트가 표시되면 **확인**을 클릭하십시오.

   본인이 마스터 사용자이며 IBM ID로 전환하기 위한 프롬프트가 {{site.data.keyword.BluSoftlayer_full}} 인프라 고객 포털에서 표시되지 않는 경우에는 IBM 지원 센터에 문의하여 도움을 받으십시오. 지원 문의에 대한 자세한 정보는 [IBM 지원 센터](/docs/get-support/howtogetsupport.html#getting-customer-support)를 참조하십시오. 

   이미 로그인했으며 프롬프트에서 **나중에**를 클릭했지만, 현재의 세션에서 IBM ID 인증으로 전환하려는 경우에는 사용자 프로파일 편집 페이지로 이동하여 **IBM ID로 전환**을 클릭하십시오.

2. 마법사 프롬프트를 따라 IBM ID를 작성하십시오.

   현재 IBM ID에서 사용하지 않는 이메일 주소를 입력하십시오. 이 이메일 주소는 새 IBM ID의 사용자 이름으로 사용되며, IBM ID가 작성되면 이 주소로 등록 코드가 전송됩니다. 나중에 IBM ID와 연관된 이메일 주소를 업데이트할 수 있지만 사용자 이름을 변경할 수는 없습니다.

### 등록 코드로 IBM ID 확인
{: #confIBMiduseregcode}

1. 등록 코드를 수신하면 이메일의 링크를 클릭하거나 URL을 브라우저로 복사하고 등록 코드를 입력하십시오.

   등록 코드는 7일 동안 유효하며 이를 한 번만 사용할 수 있습니다.

2. 등록 코드를 제출한 후에는 IBM ID를 사용하여 고객 포털에 로그인하십시오.

   계정 로그인 프롬프트에서 **IBM ID 계정 로그인** 섹션으로 이동하고 **IBM ID로 로그인**을 클릭하십시오. 이전에 SoftLayer ID로 사용한 **사용자 이름** 및 **비밀번호** 필드를 사용하지 마십시오.

새 고객이 주문을 체크아웃하는 경우, 기존 IBM ID가 있는지 또는 새 IBM ID를 작성할 것인지 확인하게 됩니다.
  * 기존 IBM ID를 사용하려면 고유한(즉, 여러 IBM ID 간에 공유되지 않음) 경우 IBM ID의 이메일 주소 또는 사용자 이름을 입력하십시오.
  * 새 IBM ID를 작성하려면 현재 IBM ID에서 사용하지 않는 이메일 주소를 입력하십시오. 이 이메일 주소는 IBM ID의 사용자 이름이며, IBM ID가 작성된 후 이 주소로 등록 코드가 전송됩니다. 나중에 IBM ID와 연관된 이메일 주소를 업데이트할 수 있지만 사용자 이름을 변경할 수는 없습니다.

IBM ID로 로그인 시에 발생하는 문제점을 해결하려면 [{{site.data.keyword.Bluemix_notm}} 액세스에 대한 문제점 해결](/docs/troubleshoot/ts_accessing.html#accessing)을 참조하십시오.

## IBM ID 사용자 계정 연결
{: #link_user_accounts}

사용자 계정이 IBM ID인증으로 전환되면 리셀러 및 디스트리뷰터가 SoftLayer 계정과 {{site.data.keyword.Bluemix_notm}} 계정을 연결하여 결합된 IaaS(Infrastructure as a Service) 및 PaaS(Platform as a Service) 리소스를 활용할 수 있습니다. 그 후에는 한 번의 로그인으로 {{site.data.keyword.BluSoftlayer_full}} 인프라 고객 포털에서 IaaS 리소스에 액세스하고 {{site.data.keyword.Bluemix_notm}} 콘솔에서 PaaS 리소스에 액세스할 수 있습니다. 또한 계정을 연결하면 사용하는 모든 PaaS 및 IaaS 리소스에 대해 하나의 청구서만 발행됩니다. 

계정을 연결하려면 SoftLayer 마스터 사용자여야 합니다. 계정의 마스터 사용자인 IBM ID는 연결 중인 {{site.data.keyword.Bluemix_notm}} 플랫폼 계정의 소유자여야 합니다. 계정을 연결하려면 다음 중요 참고사항을 반드시 검토하십시오. 

  * 연결되는 SoftLayer 계정의 마스터 사용자에게는 IBM ID가 있어야 합니다. 
  * {{site.data.keyword.Bluemix_notm}} 계정에 연결되는 각 사용자 계정은 고유 이메일 주소가 있는 고유 IBM ID에서 소유해야 합니다. 하나의 IBM ID가 여러 SoftLayer 계정을 소유할 수 있지만, 각 계정에 대해 고유 IBM ID가 되도록 마스터 사용자를 변경해야 합니다. SoftLayer 계정의 마스터 사용자를 변경하려면 지원 팀에 문의하십시오. 자세한 정보는 [{{site.data.keyword.Bluemix_notm}} 인프라에 대한 지원 받기](/docs/customer-portal/cpsupport.html)를 참조하십시오.
  * 연결된 계정에 새 사용자를 추가하는 경우에는 통합 콘솔의 모든 기능에 액세스할 수 있도록 사용자를 SoftLayer 계정 및 {{site.data.keyword.Bluemix_notm}} 계정 모두에 추가해야 합니다.
  * 브랜드 계정을 보유하고 있고, BAP(Brand Agent Portal)를 사용하며 계정 연결 시에 지원이 필요한 경우에는 softlayer_revenue_services_team@wwpdl.vnet.ibm.com으로 이메일을 발송하여 Revenue Services 팀에 문의하십시오. 
  * {{site.data.keyword.Bluemix_notm}}의 연결된 모든 계정은 종량과금제 계정이어야 합니다. 새 종량과금제 계정을 작성하거나, 기존 종량과금제 계정을 연결하거나, 기존 평가판 계정을 연결할 수 있으며, 그런 다음 종량과금제 계정으로 업그레이드됩니다. {{site.data.keyword.Bluemix_notm}} 구독 계정은 연결할 수 없습니다. 

각 SoftLayer 계정을 기존 {{site.data.keyword.Bluemix_notm}} 플랫폼 계정에 연결하거나 새 계정을 작성하려면 다음 단계를 완료하십시오. 

   1. 마스터 사용자 계정 IBM ID를 사용하여 {{site.data.keyword.BluSoftlayer_full}} 인프라 고객 포털에 로그인하십시오. 
   2. {{site.data.keyword.Bluemix_notm}} 인프라 고객 포털에서 **Bluemix 계정 연결**을 클릭하십시오. 
   3. SoftLayer 및 {{site.data.keyword.Bluemix_notm}} 계정의 연결과 관련된 이용 약관을 읽고 이에 동의하십시오.
   4. SoftLayer 계정의 사용자를 {{site.data.keyword.Bluemix_notm}} 계정에 추가를 포함하여 마법사 프롬프트를 따르십시오.
   5. 프롬프트가 표시되면 다음 조치 중 하나를 수행하십시오. 
     * 이미 {{site.data.keyword.Bluemix_notm}} 계정이 있는 경우에는 해당 계정과 연관된 이메일 주소를 제공하여 계정을 연결하십시오. 
     * {{site.data.keyword.Bluemix_notm}} 계정이 없는 경우에는 사용할 이메일 주소를 입력한 후 지시사항에 따라 {{site.data.keyword.Bluemix_notm}}에 방문하여 계정을 작성하십시오.
   6. 계정을 연결한 후에는 앞선 [IBM ID로 전환](/docs/account/softlayerlink.html#switchtoIBMid) 절에 설명되어 있는 프로시저에 따라 IBM ID로 마이그레이션하도록 각 계정의 일반 사용자에게 알리십시오. 

일반 사용자 계정만 IBM ID로 마이그레이션하십시오. 일반 사용자 계정의 상위 계정이며 리소스를 포함하지 않는 브랜드 계정은 마이그레이션하지 마십시오. 브랜드 계정 사용자가 IBM ID로 마이그레이션하면 BAP(Brand Agent Portal) 포털에 로그인할 수 없습니다.
{: tip}

연결된 계정은 [{{site.data.keyword.Bluemix}} 콘솔 ![외부 링크 아이콘](../icons/launch-glyph.svg)](https://console.bluemix.net){: new_window}에 로그인합니다. 

또한 계정이 연결된 후에는 다음 변경사항을 참고하십시오. 
  * IBM ID 신임 정보를 사용하여 SoftLayer 계정과 {{site.data.keyword.Bluemix_notm}} 계정에 액세스하십시오.
  * 기존 SoftLayer 할인은 {{site.data.keyword.Bluemix_notm}} 비용에 적용됩니다.
  * 미국 달러(USD)로 된 송장을 받게 됩니다. 기존 {{site.data.keyword.Bluemix_notm}} 계정을 보유하고 있는 경우, {{site.data.keyword.Bluemix_notm}}를 통한 인프라 리소스의 청구는 계정이 연결된 이후 시작되는 새 청구 주기에 적용됩니다.
  * {{site.data.keyword.Bluemix_notm}} 콘솔에서 인프라 리소스의 사용량을 모니터링할 수 있습니다.

일단 계정이 연결되면 해당 연결을 해제할 수 없습니다.
{: tip}

## 연결된 계정에서 다중 인증 사용
{: #2fa}

연결된 계정이 있는 경우에는 ID 및 액세스 **설정** 페이지를 사용하여 계정에 대한 다중 인증을 사용으로 설정할 수 있습니다. 이는 일반적으로 이중 인증(2FA)이라고도 하며, 표준 필수 IBM ID 및 비밀번호 이상의 계정에 액세스하기 위해 보안 계층을 추가합니다. 계정에 대한 다중 인증은 연결된 {{site.data.keyword.Bluemix_notm}} 계정의 모든 리소스에 적용됩니다. 다중 인증이 계정에 사용 가능한 경우 계정에 추가된 모든 사용자에게도 적용됩니다.

다중 인증은 IBM ID별로 수행되지 않습니다. 계정별로 수행됩니다. IBM ID가 여러 계정과 연관되어 있고, 계정 간에 전환할 때는 이중 인증이 필요한 다른 계정으로 전환할 때마다 ID를 확인해야 합니다. 이는 이전 계정과 새 계정이 모두 같은 이중 인증 메커니즘으로 구성된 경우에도 해당됩니다.
