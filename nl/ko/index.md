---

copyright:
  years: 2015, 2019
lastupdated: "2019-03-19"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account, subscription, service bundle

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 계정 유형
{: #accounts}

{{site.data.keyword.Bluemix_notm}}에는 세 개의 서로 다른 계정 유형(Lite, 종량과금제, 구독)이 있습니다. 등록 즉시 무료 Lite 계정을 받을 수 있습니다. 종량과금제 및 구독은 청구 가능한 계정 옵션이며, 각각 서로 다른 기능을 제공합니다. 각 계정을 비교하고 사용자의 요구사항에 가장 적합한 계정을 선택하십시오.
{:shortdesc}

## 계정 비교
{: #compare}

다음 표에는 Lite, 종량과금제 및 구독 계정이 비교되어 있습니다. 각각의 계정에 대한 추가 세부사항은 후속 절을 참조하십시오.

|                                         |Lite               |종량과금제      |구독       |
|-----------------------------------------|--------------------|--------------------|--------------------|
|**무료 Cloud Foundry 메모리에 액세스** |256MB             |512MB             |512MB             |
| **[Lite 서비스 플랜에 액세스 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://{DomainName}/catalog/?search=label:lite){: new_window}** | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**모든 무료 플랜에 액세스**            |                    | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**전체 {{site.data.keyword.Bluemix_notm}} 카탈로그에 액세스** |  | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**다중 Cloud Foundry 지역에 액세스** |               | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**시간 제한사항 없음** | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**보증된 제로 코스트**                | ![기능 사용 가능](../icons/icon_enabled.svg) |  |         |
|**중단된 가격**                  |                    |                    | ![기능 사용 가능](../icons/icon_enabled.svg) |
|**개념 증명 학습 또는 빌드에 최적임** | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |  |
|**프로덕션 유스 케이스에 최적임**        |                    | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
{: caption="표 1. {{site.data.keyword.Bluemix_notm}} 계정의 비교" caption-side="top"}


## Lite 계정
{: #liteaccount}

{{site.data.keyword.Bluemix_notm}} 콘솔에서 Lite 태그 ![Lite 태그](../icons/Lite.svg)와 함께 표시된, 무료로 선택할 수 있는 Lite 플랜을 통해 Lite 계정으로 가입하여 앱 빌드 및 서비스 탐색을 시작하십시오. Lite 계정은 만료되지 않으며 신용카드가 필요하지 않습니다.

본인용으로 작성된 `Default`로 이름 지정된 단일 리소스 그룹에 대한 액세스를 보유합니다. {{site.data.keyword.Bluemix_notm}} Identity and Access Management(IAM)에서 관리하는 모든 서비스 인스턴스는 자동으로 이 리소스 그룹에 추가됩니다. 언제든지 이 리소스 그룹의 이름을 업데이트할 수 있습니다. 세부 단계는 [리소스 그룹 이름 바꾸기](/docs/resources?topic=resources-rgs#rename_rgs)를 참조하십시오.

각각의 리소스 그룹은 무료입니다. Cloud Foundry 앱 및 IAM에서 관리되는 서비스 간의 연결을 작성할 때 할당량으로 계수되는 별명(서비스 인스턴스임)을 작성합니다. [연결 관리](/docs/resources?topic=resources-connect_app)를 참조하십시오.
{: tip}

### 사용 가능한 기능
{: #lite-account-features}

Lite 계정에 사용 가능한 다음 주요 기능 목록을 확인하십시오.

   * 계정이 무료로 제공됨 - 신용카드가 필요하지 않습니다.
   * 계정이 만료되지 않습니다.
   * 하나의 {{site.data.keyword.Bluemix_notm}} 지역에서 하나의 조직을 사용할 수 있습니다.
   * 기본 {{site.data.keyword.Bluemix_notm}} 지원은 무료입니다. 기본 지원은 기존의 심각도가 사용되지 않고 특정 응답 시간이 규정되지 않은 프로덕션 이외의 환경 또는 워크로드에 제공됩니다.
   * 계정 상태 및 할달량 한계에 대한 이메일 알림을 받습니다.
   * Cloud Foundry 앱은 매월 최대 256MB의 바로 사용 가능한 무료 런타임 메모리에 액세스할 수 있습니다.
   * Lite 플랜을 보유하는 [{{site.data.keyword.Bluemix_notm}} 카탈로그 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window}에서 서비스의 1개 인스턴스를 프로비저닝할 수 있습니다.
   * 개발 활동이 없는 상태로 10일 후에는 앱이 휴면 상태가 됩니다. 앱에 대한 작업을 재개하여 앱의 휴면 상태를 해제할 수 있습니다.
   * 개발 활동이 없는 상태로 30일 후에는 Lite 플랜의 서비스 인스턴스가 삭제됩니다.

## 종량과금제 계정
{: #paygo}

종량과금제 계정을 사용하면 모든 무료 플랜을 포함한 전체 {{site.data.keyword.Bluemix_notm}} 카탈로그에 액세스할 수 있으며, 매월 512MB의 무료 런타임 메모리를 두 배로 확보할 수 있습니다. 장기 계약이나 약정 없이 사용한 청구 가능한 서비스에 대해서만 비용을 지불하게 됩니다. 

여러 리소스 그룹을 작성하여 할당량을 쉽게 관리하고 리소스 세트에 대한 청구 사용량을 볼 수 있습니다. 비용은 {{site.data.keyword.Bluemix_notm}} 컴퓨팅 및 서비스의 사용을 기준으로 청구됩니다. 사용 가능한 런타임 및 서비스 허용량을 초과하여 사용하는 경우 리소스 비용에 대한 세부사항을 제공하는 월별 청구서를 받습니다.

또한 종량과금제 계정을 사용하면 고급 또는 프리미엄 지원 플랜을 주문하여 프로덕션 워크로드에 대한 추가 지원을 받을 수 있습니다. [지원 플랜](/docs/get-support?topic=get-support-support-plans)에서 자세히 알아보십시오.

## 구독 계정
{: #subscription-account}

구독 계정이 있으면 여러 개의 리소스 그룹을 작성하여 할당량을 손쉽게 관리하고 리소스 세트에 대한 청구 사용량을 볼 수 있습니다. 매월 최소 지출 금액을 약정하고 해당 최소 비용에 적용되는 구독 할인을 받습니다. 

예를 들어 월 100달러를 6개월 동안 지출하겠다고 약속하면 10% 할인을 받을 수 있습니다. 구독 기간 동안 사용료는 600달러이지만 540달러만 지불하면 됩니다. 구독 기간이 길수록 할인이 많아집니다. 

총 구독 금액에서 사용량이 차감됩니다. 월마다 사용량이 다르더라도 예측 가능하고 일관된 청구서를 받을 수 있습니다. 사용량이 총 구독 금액을 초과하는 경우 초과 사용량에 대해 할인되지 않은 요금이 부과됩니다. 

종량과금제 계정과 마찬가지로 구독 계정은 고급 또는 프리미엄 지원 플랜을 주문하여 필요할 경우 추가 지원을 받을 수 있습니다. [지원 플랜](/docs/get-support?topic=get-support-support-plans)에서 자세히 알아보십시오.

구독 계정이 있으면 [{{site.data.keyword.Bluemix_notm}} 카탈로그](https://cloud.ibm.com/catalog/){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")에서 사용 가능한 대부분의 서비스를 작성할 수 있습니다. 그러나 일부 서비스는 별도 구매를 요구하는 특정 가격 플랜을 사용합니다.

### 서비스 번들 구독
{: #service-subscriptions}

서비스 번들 구독은 인기 있는 유스 케이스를 대상으로 하는 특정 도메인 내의 서비스에 대한 액세스 및 크레딧을 제공합니다. AI, 분석, {{site.data.keyword.blockchainfull_notm}}, IoT(Internet of Things) 및 클라우드 네이티브 서비스를 포함하는 서비스 번들 중에서 선택할 수 있습니다. 여러 도메인을 교차해야 하는 경우 여러 서비스 번들 구독을 구입할 수 있습니다. 

Lite 계정을 포함하여 모든 유형의 기존 계정에 서비스 번들을 추가할 수 있습니다. 처음 90일 동안은 번들 내의 서비스 사용으로 제한됩니다. 처음 90일이 지나면 전체 카탈로그에 액세스할 수 있습니다. 서비스 번들 구독에는 [{{site.data.keyword.Bluemix_notm}} 서비스 명세서](/docs/overview/terms-of-use?topic=overview-terms) 조항이 적용됩니다. 

서비스 번들 구독은 {{site.data.keyword.Bluemix_notm}} 콘솔을 통해 이용할 수 없습니다. 서비스 번들에 대해 자세히 알아보고 구매하려면 [{{site.data.keyword.Bluemix_notm}} 영업![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}에 문의하십시오.
{:tip}

서비스 번들 구독을 구입하면 번들을 계정에 추가하기 위해 적용하는 기능 코드가 포함된 이메일을 받습니다. 기능 코드를 적용하는 방법에 대한 자세한 내용은 [기능 코드 적용](/docs/account?topic=account-codes)을 참조하십시오. 서비스 번들이 만료되거나 모든 크레딧을 사용하는 경우, 사용량을 종량과금제 요금으로 지불하면서 모든 서비스를 계속 사용할 수 있습니다. 

### {{site.data.keyword.Bluemix_dedicated_notm}} 계정
{{site.data.keyword.Bluemix_dedicated_notm}}에서는 다음을 포함하여 최소 기간인 1년 동안은 등록해야 합니다.

   * VPN 연결을 인프라에 다시 연결
   * {{site.data.keyword.BluSoftlayer_notm}} 데이터 센터의 완전한 중복 환경
   * 지원되는 모든 런타임({{site.data.keyword.runtime_liberty_short}}, {{site.data.keyword.runtime_nodejs_short}} 및 기본 제공 오픈 소스 런타임)
   * 선택한 모든 데디케이티드 서비스 및 모든 퍼블릭 {{site.data.keyword.Bluemix_notm}} 서비스
   * 표준 {{site.data.keyword.Bluemix_notm}} 지원

{{site.data.keyword.BluDirectLink}} 또는 고급 또는 프리미엄 지원 옵션 등의 선택적 항목을 주문할 수도 있습니다. 자세한 정보는 [{{site.data.keyword.Bluemix_notm}} 영업 팀 ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg)에 문의하십시오.

해당 기간 동안 매월 지불하는 항목은 원하는 데디케이티드 서비스 및 모든 퍼블릭 서비스에 대한 액세스를 제공하는 구독 계정을 기반으로 합니다. {{site.data.keyword.Bluemix_notm}} 퍼블릭에서 서비스의 사용 비용은 구독 계정 계약을 기반으로 계산됩니다. 해당 구독 계약 외에 추가로 사용하는 모든 서비스에 대해 송장이 발급됩니다. 계약에 착수하려면 IBM이 지정한 계정 담당자 또는 [{{site.data.keyword.Bluemix_notm}} 영업 팀](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg)에 문의하십시오.

## 계정 업그레이드
{: #upgrade-lite-account}

계정을 한 단계 끌어올릴 준비가 되면 종량과금제 계정 또는 구독 계정으로 [Lite 계정을 업그레이드](/docs/account?topic=account-upgrading-account)할 수 있습니다. 계정을 업그레이드하면 전체 {{site.data.keyword.Bluemix_notm}} 카탈로그를 이용할 수 있으며 추가 무료 리소스 등이 제공됩니다. 

Lite 계정을 종량과금제 계정으로 업그레이드하면 200달러의 프로모션 크레딧이 자동으로 계정에 적용됩니다. 사용자의 200달러 크레딧은 30일 동안 유효하며, 사용량이 자동으로 크레딧 금액에서 차감됩니다. 이 크레딧은 서드파티 오퍼링과 함께 사용할 수 없으며 일부 계정에 대해서는 해당 크레딧을 사용할 수 없습니다.

종량과금제 또는 구독 계정이 이미 있는 경우 계정을 다른 유형으로 변환할 수도 있습니다. 자세한 정보는 [계정 업그레이드](/docs/account?topic=account-upgrading-account)를 참조하십시오.
