---

copyright:

  years: 2015, 2018
lastupdated: "2017-11-29"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 계정 유형
{: #accounts}

{{site.data.keyword.Bluemix}}에서 무료로 빌드를 시작할 수 있습니다. 확장할 준비가 되면 업그레이드한 후에 무료 사용량을 초과하는 사용 내역에 대해서만 비용을 지불하십시오. 라이트, 종량과금제, 구독 및 프로모션 등 네 개의 서로 다른 계정 유형에서 선택할 수 있습니다. 임의의 계정 유형을 사용하여 {{site.data.keyword.Bluemix_notm}}에서 시작할 수 있습니다. 단순히 요구사항에 최적인 유형을 선택하십시오. 
{:shortdesc}

## 계정 비교
{: #compare}

다음 표에는 라이트, 종량과금제 및 구독 계정이 비교되어 있습니다. 각각의 계정에 대한 추가 세부사항은 후속 절을 참조하십시오.

|  | 라이트  | 종량과금제 | 구독 | 
|--------------------|--------------------|--------------------|--------------------|
| **무료 Cloud Foundry 메모리에 액세스** | 256MB | 512MB | 512MB | 
| **[라이트 서비스 플랜 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window}**에 액세스 | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
| **모든 무료 사용제에 액세스** |  | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
| **전체 카탈로그에 액세스** |  | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
| **시간 제한사항 없음** | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |
| **보증된 제로 코스트** | ![기능 사용 가능](../icons/icon_enabled.svg) |  |  |
| **협의된 가격 책정** |  |  | ![기능 사용 가능](../icons/icon_enabled.svg) | 
| **POC 학습 또는 빌드에 최적임** | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) |  | 
| **프로덕션 유스 케이스에 최적임** |  | ![기능 사용 가능](../icons/icon_enabled.svg) | ![기능 사용 가능](../icons/icon_enabled.svg) | 
{: caption="표 1. {{site.data.keyword.Bluemix_notm}} 계정의 비교" caption-side="top"}

## 라이트 계정
{: #liteaccount}

{{site.data.keyword.Bluemix_notm}} 콘솔에서 라이트 태그 ![라이트 태그](../icons/Lite.svg)로 표시되며 이름이 라이트인 선택 무료 사용제로 서비스를 탐색하고 앱을 빌드하려면 무료 라이트 계정에 등록하십시오. 라이트 계정은 만료되지 않으며 신용카드가 필요하지 않습니다. 

본인용으로 작성된 `Default`로 이름 지정된 단일 리소스 그룹에 대한 액세스를 보유합니다. {{site.data.keyword.Bluemix_notm}} Identity and Access Management(IAM)에서 관리하는 모든 서비스 인스턴스는 자동으로 이 리소스 그룹에 추가됩니다. 언제든지 이 리소스 그룹의 이름을 업데이트할 수 있습니다. 세부 단계는 [리소스 그룹 이름 바꾸기](/docs/admin/resourcegroups.html#renaming-a-resource-group)를 참조하십시오. 

각각의 리소스 그룹은 무료입니다. Cloud Foundry 앱 및 IAM에서 관리하는 서비스 간에 연결을 작성할 때는 할당량으로 계수되는 별명(서비스 인스턴스임)을 작성하십시오. [별명의 개념](/docs/manageapps/connecting_apps.html#what_is_alias)을 참조하십시오.
{: tip}

### 사용 가능한 기능

라인트 계정에서 제공되는 내용이 궁금할 수 있습니다. 다음 주요 기능 목록을 확인하십시오.

   * 계정이 무료로 제공됨 - 신용카드가 필요하지 않습니다.
   * 계정이 만료되지 않습니다.
   * 하나의 {{site.data.keyword.Bluemix_notm}} 지역에서 하나의 조직을 사용할 수 있습니다.
   * 무료 {{site.data.keyword.Bluemix_notm}} 지원이 제공됩니다.
   * 계정 상태 및 할달량 한계에 대한 이메일 알림을 받습니다.
   * Cloud Foundry 앱이 최대 256MB의 바로 사용 가능한 무료 런타임 메모리에 액세스할 수 있습니다. 
   * 2개의 CPU 및 4GB RAM으로 Kubernetes 클러스터 관련 작업을 수행할 수 있습니다.
   * 라이트 플랜을 보유하는 [{{site.data.keyword.Bluemix_notm}} 카탈로그 ![외부 링크 아이콘](../icons/launch-glyph.svg "외부 링크 아이콘")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window}에서 서비스의 1개 인스턴스를 프로비저닝할 수 있습니다.
   * 개발 활동이 없는 상태로 10일 후에는 앱이 휴면 상태가 됩니다.  메모리 할당량 한계 도달에 대해 걱정할 필요 없이 새 앱에 대한 작업을 시작할 수 있습니다.
   * 개발 활동이 없는 상태로 30일 후에는 라이트 플랜의 서비스 인스턴스가 삭제됩니다.  이러한 방법으로 새로 작성하기 전에 비활성 인스턴스 삭제를 관리할 필요가 없습니다.

## 청구 가능 계정
{: #billableacts}

{{site.data.keyword.Bluemix_notm}} 청구 가능 플랜을 등록하거나 계정에 대한 업그레이드를 요청할 때는 네 개의 서로 다른 {{site.data.keyword.Bluemix_notm}} 계정 중에서 선택할 수 있습니다. 여러 가지 계정 유형과 그 청구 방법이 다음 표에 나열되어 있습니다.

|계정 유형 |	비용 청구 방법 |
|------------------|-----------------------|
|종량과금제 |	{{site.data.keyword.Bluemix_notm}} 컴퓨팅 및 서비스의 사용을 기준으로 비용이 청구됩니다. |
|구독 | 매월 최소 지출 약정에 따라 월별 할인을 받을 수 있습니다. |
| {{site.data.keyword.Bluemix_dedicated_notm}} | 연간 계약 |
|{{site.data.keyword.Bluemix_local_notm}} |	연간 계약 |
{:caption="표 2. {{site.data.keyword.Bluemix_notm}} 청구 가능 계정 및 비용" caption-side="top"}

{{site.data.keyword.Bluemix_notm}} 청구 가능 계정을 SoftLayer 계정과 연결하면 다음 달 초부터 결합된 비용이 {{site.data.keyword.Bluemix_notm}} 송장에 포함됩니다. 자세한 정보는
[크레딧 보기](/docs/pricing/viewing_usage.html#credits)를
참조하십시오.
{: tip}

### 종량과금제 계정

종량과금제 계정이 있으면 여러 개의 리소스 그룹을 작성하여 할당량을 손쉽게 관리하고 리소스 세트에 대한 청구 사용량을 볼 수 있습니다.

무료 런타임 및 서비스 허용량을 제공받을 수 있습니다. 무료 사용량을 초과하여 사용하면 매월 {{site.data.keyword.Bluemix_notm}} 송장을 받습니다. 송장은 미국 달러(USD)로 청구되며 리소스 비용에 대한 세부사항이 기재되어 있습니다. 

많은 국가와 지역에서는 {{site.data.keyword.Bluemix_notm}} 콘솔에서 종량과금제 계정을 등록할 수 있습니다. 청구 및 신용카드 정보를 입력한 후에 이용 약관에 동의하고 계정 요청을 제출하십시오. 그러면 신용카드의 유효성이 검증됩니다. 계정 정보 확인 이메일도 전송됩니다. 확인 이메일을 받은 이후 몇 분이 지나면 콘솔로 돌아가서 앱 빌드를 계속 진행할 수 있습니다.

해당 국가 또는 지역에 대해 온라인 요청을 처리할 수 없는 경우에는 [{{site.data.keyword.Bluemix_notm}} 지원 ![외부 링크 아이콘](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} 페이지에 나열된 링크를 사용하여 {{site.data.keyword.Bluemix_notm}} 영업 팀에 문의하십시오.

종량과금제 계정은 언제든지 구독 계정으로 변환할 수 있습니다. [{{site.data.keyword.Bluemix_notm}} 지원 ![외부 링크 아이콘](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} 페이지에 나열된 링크를 사용하여 {{site.data.keyword.Bluemix_notm}} 영업 팀에 문의하십시오.

### 구독 계정

구독 계정이 있으면 여러 개의 리소스 그룹을 작성하여 할당량을 손쉽게 관리하고 리소스 세트에 대한 청구 사용량을 볼 수 있습니다.

매월 최소 지출 금액을 지불하며 해당 최소 비용에 적용되는 구독 할인을 받습니다. 최소 지출 금액을 초과하는 사용량에 대해서는 비용이 청구됩니다.

구독 계정에 등록하고 구독 요금 및 할인에 대한 자세한 정보를 보려면 [{{site.data.keyword.Bluemix_notm}} 지원 ![외부 링크 아이콘](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window} 페이지에 나열된 링크를 사용하여 {{site.data.keyword.Bluemix_notm}} 영업 팀에 문의해야 합니다.

### {{site.data.keyword.Bluemix_dedicated_notm}} 계정

{{site.data.keyword.Bluemix_dedicated_notm}}에서는 다음을 포함하여 최소 기간인 1년 동안은 등록해야 합니다.

   * 인프라에 대한 VPN 연결
   * {{site.data.keyword.BluSoftLayer_notm}} 데이터 센터의 완전한 중복 환경
   * 지원되는 모든 런타임(IBM Java Liberty, Node.js 및 기본 제공 오픈 소스 런타임)
   * 선택한 모든 데디케이티드 서비스 및 모든 퍼블릭 {{site.data.keyword.Bluemix_notm}} 서비스
   * 표준 {{site.data.keyword.Bluemix_notm}} 지원

SoftLayer DirectLink 또는 프리미엄 지원 옵션과 같은 선택적 항목을 주문할 수도 있습니다. 자세한 정보는 [{{site.data.keyword.Bluemix_notm}} 영업 팀 ![외부 링크 아이콘](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window}에 문의하십시오.

해당 기간 동안 매월 지불하는 항목은 원하는 데디케이티드 서비스 및 모든 퍼블릭 서비스에 대한 액세스를 제공하는 구독 계정을 기반으로 합니다. {{site.data.keyword.Bluemix_notm}} 퍼블릭에서 서비스의 사용 비용은 구독 계정 계약을 기반으로 계산됩니다. 해당 구독 계약 외에 추가로 사용하는 모든 서비스에 대해 송장이 발급됩니다. 계약을 체결하려면 IBM 지정 계정 담당자에게 문의하거나 [{{site.data.keyword.Bluemix_notm}} 영업 팀 ![외부 링크 아이콘](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window}에 문의하십시오.

### {{site.data.keyword.Bluemix_local_notm}} 계정

{{site.data.keyword.Bluemix_local_notm}}에서는 다음을 포함하여 최소 기간인 1년 동안은 등록해야 합니다.

   * 릴레이라고도 하며 IBM이 사용자의 로컬 배치에 연결하고 업데이트를 자동으로 일괄적으로 전달할 수 있도록 하는 전달 기능
   * 지원되는 모든 런타임(IBM Java Liberty, Node.js 및 기본 제공 오픈 소스 런타임)
   * 선택한 모든 로컬 서비스 및 모든 퍼블릭 {{site.data.keyword.Bluemix_notm}} 서비스에 대한 액세스
   * 표준 {{site.data.keyword.Bluemix_notm}} 지원

해당 기간 동안 매월 지불하는 항목은 원하는 로컬 서비스 및 모든 퍼블릭 서비스에 대한 액세스를 제공하는 구독 계정을 기반으로 합니다. {{site.data.keyword.Bluemix_notm}} 퍼블릭에서 서비스의 사용 비용은 구독 계정 계약을 기반으로 계산됩니다. 해당 구독 계약 외에 추가로 사용하는 모든 서비스에 대해 송장이 발급됩니다. 계약을 체결하려면 IBM 지정 계정 담당자에게 문의하거나 [{{site.data.keyword.Bluemix_notm}} 영업 팀 ![외부 링크 아이콘](../icons/launch-glyph.svg)](http://ibm.biz/bluemixsupport){: new_window}에 문의하십시오.

## 프로모션 계정
{: #promo}

프로모션 계정은 가끔씩 특별 프로모션의 일부로 제공되며 대부분의 {{site.data.keyword.Bluemix_notm}} 카탈로그에 액세스할 수 있는 권한이 포함된 일정 기한 내의 무료 평가판입니다. 이 계정 유형은 프로모션 코드를 통해서만 사용할 수 있습니다. 계정의 유효성 기간은 프로모션에 따라 다릅니다.  
   
프로모션 계정과 함께 본인용으로 작성된 `Default`로 이름 지정된 단일 리소스 그룹에 대한 액세스를 보유합니다. 모든 IAM-관리 서비스 인스턴스는 이 리소스 그룹에 자동으로 추가됩니다. 언제든지 이 리소스 그룹의 이름을 업데이트할 수 있습니다. 세부 단계는 [리소스 그룹 이름 바꾸기](/docs/admin/resource-groups.html#renaming-a-resource-group)를 참조하십시오. 

각각의 리소스 그룹은 무료입니다. Cloud Foundry 앱 및 IAM에서 관리하는 서비스 간에 연결을 작성할 때는 할당량으로 계수되는 별명(서비스 인스턴스임)을 작성하십시오. [별명의 개념](/docs/manageapps/connecting_apps.html#what_is_alias)을 참조하십시오.
{: tip}

### 프로모션 계정이 만료되면 발생하는 사항
{: #trialend}

프로모션 계정이 만료되면 사용자 계정의 앱이 중지됩니다. 다른 {{site.data.keyword.Bluemix_notm}} 계정은 등록할 수는 없지만, 자신의 계정과 초대를 받은 계정에는 계속 액세스할 수 있습니다.

앱을 다시 시작하려면 종량과금제 계정에 대한 신용카드 정보를 제공하거나 구독 계정을 작성하여 계정을 청구 가능 계정으로 변환하십시오. 그러면 무료 컴퓨팅 및 서비스 허용량을 계속 사용할 수 있습니다. 매월 무료 사용량에 포함되지 않은 서비스, 컨테이너 및 런타임 사용량에 대해서만 지불합니다.

프로모션 계정이 만료된 후에 계정을 변환하지 않으면 앱과 서비스가 30일 이후 제거됩니다. 그러나 사용자의 계정은 삭제되지 않고 언제든지 로그인해서 청구 가능 계정으로 업그레이드할 수 있습니다.  또한 청구 가능 계정을 작성하고 앱 설정과 서비스 구성의 유실을 피하도록 상기시키는 이메일 알림을 받습니다. {{site.data.keyword.Bluemix_notm}}에서 알림을 수신하기를 원하지 않는 경우, 언제든지 등록을 해지할 수 있습니다.

계정을 변환하면 무료 사용량이 각 서비스에서 일반적으로 제공하는 허용량으로 제한됩니다. 이 허용량은 무료 평가판 사용 중 여러 IBM 서비스에서 제공하는 무제한 사용 허용량이 아닙니다.
