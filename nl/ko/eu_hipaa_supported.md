---

copyright:
  years: 2018, 2019
lastupdated: "2019-06-19"

keywords: GDPR, HIPAA, data security, PHI, europe

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:important: .important}
{:tip: .tip}
{:note: .note}

# EU 및 HIPAA 지원 설정 사용
{: #eu-hipaa-supported}

계정 소유자는 EU 지원 및 HIPAA 지원이 되도록 {{site.data.keyword.cloud}} 계정을 설정할 수 있습니다. 예를 들어, 리소스를 사용하여 유럽 시민의 개인 데이터를 처리하는 경우 EU 지원 설정을 사용하도록 선택할 수 있습니다. 그리고 HIPAA 사용 서비스에 PHI(Protected Health Information)를 포함하려는 경우에는 HIPAA 지원 설정의 사용을 선택할 수 있습니다.
{:shortdesc}


## EU 지원 설정 사용
{: #bill_eusupported}

EU 지원 설정을 사용하면 EU 지역의 {{site.data.keyword.Bluemix_notm}} 지원 팀 구성원이 제공하는 레벨 1과 레벨 2 지원이 제한됩니다. 그러나 EU 지역 외부에 있는 팀은 {{site.data.keyword.Bluemix_notm}} 처리 활동을 수행할 수 있습니다. EU의 레벨 1 또는 레벨 2 지원 팀이 문제를 해결하지 못하면 글로벌 팀에 문의할 수 있습니다. 항상 EU 지원 팀의 지시가 있을 때 그리고 데이터의 보안 또는 개인정보 보호에 대한 영향이 없는 경우에만 글로벌 팀에 문의합니다.

이 설정을 사용하면 저장 및 처리되는 데이터가 EU 지역의 IBM 지원 팀에 의해 제한되고 제어될 수 있도록 EU 지원 서비스에 엄격한 액세스 제어가 있습니다. 유럽 외 지역의 {{site.data.keyword.Bluemix_notm}} 전문가가 이 데이터에 대한 액세스를 필요로 하는 경우, EU 지원 팀 구성원은 액세스 요청을 검토합니다. EU 지원 팀 구성원이 글로벌 클라우드 전문가에게 요청된 시스템에 대해서만 그리고 액세스가 취소된 후 특정 시간 범위 동안만 필요한 액세스를 제공합니다. 이 프로세스에서 데이터는 항상 보호됩니다.

  1. {{site.data.keyword.Bluemix_notm}} 콘솔에서 **관리 > 계정**으로 이동하여 **계정 설정**을 선택하십시오.
  2. **설정**을 클릭하십시오.
  3. 설정 사용에 대한 정보를 읽고 **본 이용 약관을 이해했으며 이에 동의함**을 선택하십시오.
  4. **설정**을 클릭하십시오.

   EU 지원 설정을 사용으로 설정하고 나면, EU 지원 태그를 사용하여 카탈로그에서 EU 지원 플랜이 포함된 오퍼링을 검색할 수 있습니다.


## HIPAA 지원 설정 사용
{: #enabling-hipaa}

미국 의료 보험 이동 및 책임법(HIPAA)과 경제 및 임상 보건 의료 정보 기술(HITECH)법은 전자 의료 거래 및 정보 취급 표준을 정의합니다. 귀하 또는 귀사가 HIPAA에서 정의한 대상 법인인 경우, HIPAA 및 HITECH 법에 따라 규제되는 중요 워크로드를 실행할 때 HIPAA 지원 설정을 실행해야 합니다. [ {{site.data.keyword.Bluemix_notm}}의 규제 준수](https://www.ibm.com/cloud/compliance){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")에서 {{site.data.keyword.Bluemix_notm}} 규제 준수에 대해 자세히 알아보십시오.

이 설정을 활성화하면 다음과 같은 효과가 있습니다.

* 카탈로그에서 HIPAA 사용 서비스를 필터링할 수 있습니다.
* 계정에 PHI(Protected Health Information)가 저장되어 있음을 IBM에 알립니다.
* 대상 법인에 대해 IBM BAA(Business Associate Addendum)를 디지털 방식으로 수락합니다.

사용자 또는 회사가 HIPAA에서 정의한 대상 법인인 경우에만 이 설정을 활성화하십시오. 귀하 또는 귀사가 대상 법인의 비즈니스 관계자인 경우 [contact {{site.data.keyword.Bluemix_notm}} 영업](https://www.ibm.com/account/reg/us-en/signup?formid=MAIL-wcp){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")에 문의하여 해당 BAA를 수락하십시오. 대상 법인 및 비즈니스 관계자의 HIPAA 정의에 대한 자세한 내용은 [US Department of Health & Human Services](https://www.hhs.gov/hipaa/for-professionals/covered-entities/index.html){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘") 웹 사이트를 참조하십시오.
{: important}

HIPAA 지원 설정을 활성화한 계정은 여전히 전체 서비스 카탈로그에 액세스할 수 있습니다. {{site.data.keyword.Bluemix_notm}} 서비스는 일반적으로 여러 가지 플랜을 제공합니다. 서비스의 HIPAA 사용 레이블은 사용 가능한 모든 플랜에 적용되거나 특정 계획 또는 구성으로 제한될 수 있습니다. 고객은 PHI를 HIPAA 지원 오퍼링 플랜으로 제한하고 HIPAA 및 HITECH에 따라 설계할 단독 책임이 있습니다.

1. **관리 > 계정**으로 이동하여 콘솔에서 **계정 설정**을 선택하십시오.
2. HIPAA 지원 옵션의 경우 **켜짐**을 클릭하십시오.
3. 이 설정 사용에 대한 정보를 읽으십시오.

  설정을 사용으로 설정한 후에는 사용 안함으로 설정할 수 없습니다.
  {: note}

4. **승인**을 선택하고 **제출**을 클릭하십시오.

  HIPAA 지원 설정을 사용으로 설정하고 나면 HIPAA 지원 태그를 사용하여 카탈로그에서 HIPAA가 사용되는 오퍼링을 검색할 수 있습니다.
