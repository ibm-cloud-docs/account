---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: troubleshoot enterprise, enterprise problem, account problem, enterprise support, enterprise help, error message

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

# 엔터프라이즈의 문제점 해결
{: #enterprise_help}

엔터프라이즈 관리에 대한 일반적인 문제점에는 구독 또는 기능 코드를 적용할 때 발생하는 문제나 엔터프라이즈에 계정을 추가할 때 발생하는 문제 등이 있습니다. 대부분 몇 가지 간단한 단계를 수행하여 이러한 문제점에서 복구할 수 있습니다.

## 전체 엔터프라이즈를 볼 수 없는 이유는 무엇입니까?
{: #troubleshoot-view-enterprise}
{: troubleshoot}

전체 엔터프라이즈가 표시되지 않는 경우에는 자신에게 지정된 액세스 권한을 확인해야 합니다.

엔터프라이즈에 있는 몇몇 계정은 표시되지만 전체 엔터프라이즈 계층 구조가 표시되지 않습니다. 계정 계층 구조가 사용자에게 액세스 권한이 있는 계정만 표시하며, 전체 엔터프라이즈 계정을 표시하지 않습니다.
{: tsSymptoms}

사용자에게 엔터프라이즈에 있는 특정 계정에 대해서만 액세스 권한이 지정되었습니다.
{: tsCauses}

자신에게 지정된 액세스 권한을 확인하려면 다음 단계를 완료하십시오.
{: tsResolve}

1. **관리** &gt; **액세스(IAM)** > **사용자**로 이동하십시오.
2. 이름을 선택하십시오.
2. **액세스 정책** 탭을 클릭하십시오.

엔터프라이즈 소유자에게 문의하여 올바른 액세스 권한을 요청하십시오.

자신이 엔터프라이즈의 소유자인 경우, 특정 사용자에게 전체 엔터프라이즈에 대한 액세스 권한을 지정하려면 다음 단계를 완료하십시오.
1. **관리** > **액세스(IAM)** > **사용자**로 이동하십시오.
2. 사용자의 이름을 선택하십시오.
2. **액세스 정책 ** 탭 > **액세스 지정** > **계정 관리 서비스에 대한 액세스 지정**을 클릭하십시오.
3. **엔터프라이즈**를 서비스로 선택하고 엔터프라이즈의 이름을 선택하십시오.
4. 사용자에게 액세스 권한을 부여할 엔터프라이즈의 계정 또는 계정 그룹을 선택하십시오. 예를 들어, 사용자가 하나의 계정만 볼 수 있는 액세스 권한을 갖도록 하려면 해당 계정을 선택하고 뷰어 이상의 역할을 지정하십시오. 사용자가 전체 엔터프라이즈를 볼 수 있는 액세스 권한을 갖도록 하려면 계정 그룹 및 계정 선택을 공백으로 두고 액세스 권한을 지정하십시오.

## 엔터프라이즈에 기존 계정을 가져올 수 없는 이유는 무엇입니까?
{: #troubleshoot-existing-enterprise}
{: troubleshoot}

기존 계정을 엔터프라이즈로 가져오려고 하면 다음 문제 중 하나가 발생합니다.
{: tsSymptoms}
* 계정 섹션에서 **기존 계정 추가**를 클릭하면 추가하려는 계정이 나열되지 않습니다.
* **계정 가져오기**를 클릭할 수 있는 옵션이 없습니다.

사용자에게 올바른 액세스 권한이 지정되지 않았거나 계정을 가져올 자격이 없습니다.
{: tsCauses}

가져올 기존 계정이 나열되지 않는 경우에는 기존 계정의 청구 서비스에 대한 관리자 역할이 있어야 합니다.
{: tsResolve}

**계정 가져오기** 옵션을 사용할 수 없으면 사용자에게 엔터프라이즈의 청구 서비스에 대한 관리자 또는 편집자 역할, 그리고 상위 엔터프라이즈 또는 계정 그룹의 엔터프라이즈 서비스에 대한 관리자 또는 편집자 역할이 있는지 확인하십시오.

가져오려는 계정이 종량과금제 계정이며 액세스 권한이 있는지 확인한 다음에도 여전히 가져올 수 없는 경우, 계정을 엔터프라이즈로 가져올 권한이 없을 수 있습니다. 미국 달러(USD)로 청구되는 많은 종량과금제 계정과 같은 일부 종량과금제 계정은 엔터프라이즈로 직접 가져올 수 없습니다. 계정을 구독 계정으로 변환한 다음 엔터프라이즈로 가져오려면 [{{site.data.keyword.Bluemix_notm}} 영업](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![외부 링크 아이콘](../icons/launch-glyph.svg) 담당자에게 문의하십시오.

## 엔터프라이즈에서 새 계정을 작성할 수 없는 이유는 무엇입니까?
{: #troubleshoot-add-enterprise}
{: troubleshoot}

계정 섹션에서 **계정 추가**를 클릭할 수 없습니다.
{: tsSymptoms}

사용자에게 올바른 액세스 권한이 지정되지 않았습니다.
{: tsCauses}

엔터프라이즈에서 계정을 작성하려면 다음 액세스 권한이 있어야 합니다.
{: tsResolve}
1. 엔터프라이즈의 청구 서비스에 대한 관리자 역할입니다.
2. 대상 상위 엔터프라이즈 또는 계정 그룹의 엔터프라이즈 서비스에 대한 관리자 또는 편집자 역할입니다.

## 엔터프라이즈 구독을 볼 수 없는 이유는 무엇입니까?
{: #troubleshoot-viewsub-enterprise}
{: troubleshoot}

하위 계정에서 구독 페이지를 보기 위해 이동하면 다음 메시지가 표시됩니다.
{: tsSymptoms}

`Looks like you don't have permission to view subscription data for this account. Contact your account owner or administrator to request access.`

엔터프라이즈 대시보드의 청구 섹션에 다음 메시지가 표시됩니다.

`Looks like you don't have permission to view this information. Learn more about IAM access.`

미래 청구 기간의 청구 및 지불 정보에 대한 액세스는 엔터프라이즈 계정의 사용자에게로 제한됩니다. 하위 계정의 사용자는 이전에 해당 계정에서 액세스 권한이 있던 경우에도 구독과 같은 청구 및 지불 정보에 액세스할 수 없습니다.
{: tsCauses}

청구를 보거나 관리하려면 해당 사용자가 엔터프라이즈 계정에 초대되어 해당 계정의 청구 서비스에 대한 액세스 권한을 부여받아야 합니다. 계정 소유자에게 문의하여 액세스 권한을 요청하십시오.
{: tsResolve}

## 내 계정에 구독 코드를 적용할 수 없는 이유는 무엇입니까?  
{: #troubleshoot-promo-enterprise}
{: troubleshoot}

사용자에게 올바른 액세스 권한이 없어 구독 코드를 계정에 추가할 수 없습니다.  
{: tsSymptoms}

사용자의 계정이 엔터프라이즈의 하위 계정에 있으므로 구독 코드를 적용할 수 없습니다. 구독 코드는 엔터프라이즈 레벨에서 적용해야 합니다.
{: tsCauses}

엔터프라이즈의 소유자 또는 관리자에게 구독 코드를 추가하도록 요청하십시오. 구독 코드가 추가되면 엔터프라이즈의 모든 계정에 적용됩니다. 자세한 정보는 [구독 관리](/docs/billing-usage?topic=billing-usage-subscriptions)를 참조하십시오.
{: tsResolve}
