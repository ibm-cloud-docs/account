---



copyright:

  years: 2016, 2018
lastupdated: "2018-01-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# IBM ID로 전환
이제 SoftLayer의 인증은 IBM ID를 사용하여 모든 {{site.data.keyword.Bluemix}}에 대해 단일 로그인을 제공합니다. 기존 SoftLayer 계정을 사용하여 IBM ID 인증으로 전환할 수 있습니다. 마이그레이션 마법사를 통해 이러한 전환을 수행할 수 있습니다.
{:shortdesc}

IBM ID로 전환하는 프로세스를 시작하는 경우, 프로세스가 완료되기 전에 언제든지 전환을 취소할 수 있습니다. 그러나 로그인할 때마다 IBM ID로 전환하기 위한 프롬프트가 표시됩니다. {{site.data.keyword.Bluemix_notm}} 계정에 연결하려는 각 SoftLayer 계정은 고유 이메일 주소를 사용하는 고유 IBM ID에서 소유해야 합니다.

기존 SoftLayer 계정을 IBM ID로 전환하려면 다음 단계를 완료하십시오.
1. SoftLayer 계정에 로그인한 후에 IBM ID로 전환하기 위한 프롬프트가 표시되면 **확인**을 클릭하십시오.

   본인이 마스터 사용자이며 IBM ID로 전환하기 위한 프롬프트가 {{site.data.keyword.slportal}}에서 표시되지 않는 경우에는 [IBM 지원 센터](/docs/get-support/howtogetsupport.html#getting-customer-support)에 문의하여 도움을 받으십시오.

   이미 로그인했으며 프롬프트에서 **나중에**를 클릭했지만, 현재의 세션에서 IBM ID 인증으로 전환하려는 경우에는 사용자 프로파일 편집 페이지로 이동하여 **IBM ID로 전환**을 클릭하십시오.

2. 마법사 프롬프트를 따라 IBM ID를 작성하십시오.

   현재 IBM ID에서 사용하지 않는 이메일 주소를 입력하십시오. 이 이메일 주소는 새 IBM ID의 사용자 이름으로 사용되며, IBM ID가 작성된 후 이 주소로 등록 코드가 전송됩니다. 나중에 IBM ID와 연관된 이메일 주소를 업데이트할 수 있지만 사용자 이름을 변경할 수는 없습니다.

3. 등록 코드를 수신하면 이메일의 링크를 클릭하거나 URL을 브라우저로 복사하고 등록 코드를 입력하십시오.

   등록 코드는 7일 동안 유효하며 이를 한 번만 사용할 수 있습니다.

4. 등록 코드를 제출한 후에는 IBM ID를 사용하여 고객 포털에 로그인하십시오.

   계정 로그인 프롬프트에서 **IBM ID 계정 로그인** 섹션으로 이동하고 **IBM ID로 로그인**을 클릭하십시오. 이전에 SoftLayer ID로 사용한 **사용자 이름** 및 **비밀번호** 필드를 사용하지 마십시오.

새 고객이 주문을 체크아웃하는 경우, 기존 IBM ID가 있는지 또는 새 IBM ID를 작성할 것인지 확인하게 됩니다.
  * 기존 IBM ID를 사용하려면 고유한(즉, 여러 IBM ID 간에 공유되지 않음) 경우 IBM ID의 이메일 주소 또는 사용자 이름을 입력하십시오.

  * 새 IBM ID를 작성하려면 현재 IBM ID에서 사용하지 않는 이메일 주소를 입력하십시오. 이 이메일 주소는 IBM ID의 사용자 이름이며, IBM ID가 작성된 후 이 주소로 등록 코드가 전송됩니다. 나중에 IBM ID와 연관된 이메일 주소를 업데이트할 수 있지만 사용자 이름을 변경할 수는 없습니다.

IBM ID로 로그인 시에 발생하는 문제점을 해결하려면 [{{site.data.keyword.Bluemix_notm}} 액세스에 대한 문제점 해결](/docs/get-support/ts_accessing.html#accessing)을 참조하십시오. 

## IBM ID 인증을 사용하도록 사용자 계정 설정
{: #link_accounts_resellers}

일부의 경우, 사용자가 IBM ID로 전환하기 전에 리셀러 또는 디스트리뷰터가 IBM ID 인증을 사용하도록 계정을 설정해야 합니다.

  * {{site.data.keyword.Bluemix_notm}} 계정에 연결하고자 하는 각각의 기존 사용자 계정에 대해 IBM ID 인증을 사용해야 합니다. 그다음, 앞 절에서 설명한 대로 각 사용자는 마이그레이션 마법사를 사용하여 IBM ID로 전환하는 프로세스를 완료해야 합니다. 기존 SoftLayer 계정을 설정하여 IBM ID 인증을 사용하려면 [IBM 지원 센터](/docs/get-support/howtogetsupport.html#getting-customer-support)에 문의하십시오.

  * 새 사용자 계정을 IBM ID로 작성하려면 직접적인 마스터 사용자 계정에 `CREATE_NEW_ACCOUNT_WITH_IBMid_AUTHENTICATION` 속성을 설정해야 합니다. 계정에 대한 속성을 설정하려면 [IBM 지원 센터](/docs/get-support/howtogetsupport.html#getting-customer-support) 또는 공급업체에 문의하십시오.  

## IBM ID 사용자 계정 연결
{: #link_user_accounts}

사용자 계정이 IBM ID 인증으로 전환된 이후, 리셀러 및 디스트리뷰터는 SoftLayer 및 {{site.data.keyword.Bluemix_notm}} 계정을 연결하여 결합된 인프라와 플랫폼 리소스를 활용할 수 있습니다. 다음 중요 참고사항을 반드시 검토하십시오.

  * 연결되는 계정의 마스터 사용자에게는 IBM ID가 있어야 합니다.
  * {{site.data.keyword.Bluemix_notm}} 계정에 연결되는 각 사용자 계정은 고유 이메일 주소가 있는 고유 IBM ID에서 소유해야 합니다. 하나의 IBM ID가 여러 SoftLayer 계정을 소유할 수 있지만, 각 계정에 대해 고유 IBM ID가 되도록 마스터 사용자를 변경해야 합니다. SoftLayer 계정의 마스터 사용자를 변경하려면 [IBM SoftLayer 지원 ![외부 링크 아이콘](../icons/launch-glyph.svg)](https://knowledgelayer.softlayer.com/topic/support){: new_window}에 문의하십시오.
  * 연결된 계정에 새 사용자를 추가하는 경우에는 통합 콘솔의 모든 기능에 액세스할 수 있도록 사용자를 SoftLayer 계정 및 {{site.data.keyword.Bluemix_notm}} 계정 모두에 추가해야 합니다.

다음 단계를 완료하여 각각의 계정을 {{site.data.keyword.Bluemix_notm}} 계정에 연결하십시오.
1. 기존 {{site.data.keyword.Bluemix_notm}} 계정에 연결하거나 새 계정을 작성하려면 마스터 사용자로서 고객 포털에 로그인하고 {{site.data.keyword.Bluemix_notm}} 링크를 클릭하십시오.

   계정의 마스터 사용자인 IBM ID는 연결 중인 {{site.data.keyword.Bluemix_notm}} 계정의 소유자여야 합니다.

2. SoftLayer 계정의 사용자를 {{site.data.keyword.Bluemix_notm}} 계정에 추가를 포함하여 마법사 프롬프트를 따르십시오.
3. 계정이 연결되면 앞 절에서 설명한 프로시저에 따라 IBM ID로 마이그레이션하도록 각 계정의 일반 사용자에게 알리십시오.

일반 사용자 계정만 IBM ID로 마이그레이션하십시오. 일반 사용자 계정의 상위 계정이며 리소스를 포함하지 않는 브랜드 계정은 마이그레이션하지 마십시오. 브랜드 계정 사용자가 IBM ID로 마이그레이션하면 BAP(Brand Agent Portal) 포털에 로그인할 수 없습니다.
{: tip}  

## 연결된 계정에서 다중 인증 사용
{: #2fa}

연결된 계정이 있는 경우, ID 및 액세스 **설정** 페이지를 통해 계정에 대한 다중 인증(/docs/iam/mfa.html)을 사용할 수 있습니다. 이는 일반적으로 이중 인증(2FA)이라고도 하며, 표준 필수 IBM ID 및 비밀번호 이상의 계정에 액세스하기 위해 보안 계층을 추가합니다. 계정에 대한 다중 인증은 연결된 {{site.data.keyword.Bluemix_notm}} 계정의 모든 리소스에 적용됩니다. 다중 인증이 계정에 사용 가능한 경우 계정에 추가된 모든 사용자에게도 적용됩니다. 계정에 대한 [다중 인증 사용](/docs/iam/mfa.html)을 수행할 때 검토할 수 있도록 고려사항에 대해 자세히 알아보십시오. 

다중 인증은 IBM ID별로 수행되지 않습니다. 계정별로 수행됩니다. IBM ID가 여러 계정과 연관되어 있고, 계정 간에 전환할 때는 이중 인증이 필요한 다른 계정으로 전환할 때마다 ID를 확인해야 합니다. 이는 이전 계정과 새 계정이 모두 같은 이중 인증 메커니즘으로 구성된 경우에도 해당됩니다.

<!-- Above section is for MFA release 1/2018. Commented out section here has old content.
If you enabled two-factor authentication for your existing SoftLayer account, you are still required to enter your security code when logging in to the {{site.data.keyword.Bluemix_notm}} console. However, the two-factor authentication applies only to the resources in your Infrastructure account. You might be able to do various actions to the resources in your {{site.data.keyword.Bluemix_notm}} account without doing two-factor authentication.
Two-factor authentication is not per IBMid. It is still per account. When an IBMid is associated with multiple accounts, and you switch between accounts, you must confirm your identity every time you switch to a different account that requires two-factor authentication. This is true even if the prior account and the new account are both configured with the same two-factor authentication mechanism.
-->

