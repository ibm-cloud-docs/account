---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, create account group, organize accounts, move accounts

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 엔터프라이즈의 계정 체계화
{: #enterprise-organize}

{{site.data.keyword.Bluemix}} 엔터프라이즈에서 서로 관련된 계정을 체계화하려면 계정 그룹을 사용하십시오. 계정 그룹에 계정 그룹을 중첩시켜 다중 엔터프라이즈 계층 구조를 작성할 수 있습니다. 필요한 경우에는 계정 그룹 간에 계정을 이동하여 그룹을 재구성할 수 있습니다.
{:shortdesc}

예를 들면, 다음 다이어그램은 계정 그룹을 중첩시켜 구성할 수 있는 4계층 엔터프라이즈를 보여줍니다. 여기서는 먼저 엔터프라이즈를 상위로 갖는 두 개의 계정 그룹을 작성합니다. 그 후 이들 계정 그룹 중 하나를 상위로 갖는 두 개의 추가 계정 그룹을 작성할 수 있습니다. 계정 그룹 간에는 현재 계정이 속한 계층에 관계없이 계정을 자유롭게 이동할 수 있습니다. 그러나 계정 그룹은 이동할 수 없습니다. 

![네 개의 엔터프라이즈 계층을 보여주는 다이어그램입니다. 최상위 계층은 두 개의 계정 그룹 계층을 포함하는 엔터프라이즈입니다. 계정 그룹은 계정을 포함합니다. ](images/enterprise-hierarchy.svg "엔터프라이즈 계층은 계정 그룹을 추가하여 작성됩니다. "){: caption="Figure 1. A four-tier enterprise hierarchy" caption-side="bottom"}

엔터프라이즈를 체계화하는 방식은 사용량 비용을 추적하는 방법에 영향을 준다는 점을 기억하십시오. 자세한 정보는 [엔터프라이즈의 청구 및 사용량을 중앙 집중식으로 관리](/docs/billing-usage?topic=billing-usage-enterprise)를 참조하십시오.
{: tip}

## 계정 그룹 작성
{: #create-account-group}

계정 그룹을 작성하려면 엔터프라이즈 계정의 엔터프라이즈 서비스에 대한 관리자 또는 편집자 역할이 있어야 합니다. 

1. 엔터프라이즈 대시보드에서 **계정**을 클릭하여 엔터프라이즈의 계정 및 계정 그룹을 보십시오. 
1. 계정 그룹 섹션에서 **작성**을 클릭하십시오. 
1. 포함할 계정을 반영하는 계정 그룹 이름을 입력하십시오. 계정 체계화 방법의 예는 [엔터프라이즈 사용 방법](/docs/account?topic=account-enterprise#enterprise-use-cases)을 참조하십시오. 
1. 자신 외의 엔터프라이즈 사용자를 계정 그룹의 기본 담당자로 설정하려는 경우에는 **담당자** 메뉴에서 해당 사용자의 IBM ID를 지정하십시오. 담당자로 지정하려는 사용자가 엔터프라이즈에 속하지 않은 경우에는 먼저 해당 사용자를 엔터프라이즈 계정으로 초대하십시오. 계정 그룹을 작성한 후에는 담당자를 변경할 수 없습니다. 자세한 정보는 [사용자 초대](/docs/iam?topic=iam-iamuserinv)를 참조하십시오.

   담당자는 계정 그룹 또는 해당 계정에서 추가 액세스 권한을 갖지 않는다는 점에서 계정 소유자와 다릅니다. 담당자로 선택되는 사용자는 계정 그룹 문제에 대한 담당자 역할을 수행합니다. 예를 들어, 재무 담당자는 계정 그룹의 사용량 비용이 예상외로 높은 것을 발견하는 경우 이를 계정 그룹 담당자에게 알릴 수 있습니다. 


1. 계정 그룹이 엔터프라이즈 계층 구조의 다른 부분에 속하도록 하려는 경우에는 다른 상위를 선택하십시오. 

  계정 그룹은 삭제하거나 작성된 위치에서 이동할 수 없습니다.
  {: note}
1. **작성**을 클릭하십시오.

엔터프라이즈 계층 구조에 새 계층을 작성하려면 계정 그룹 내에 새 계정 그룹을 작성하십시오. 이미 엔터프라이즈에 속한 계정을 이 계정 그룹으로 이동하거나, 이 계정 그룹 내에서 계정을 가져오거나 작성할 수 있습니다. 계정 가져오기 및 작성에 대한 자세한 정보는 [엔터프라이즈에 계정 추가](/docs/account?topic=account-enterprise-add)를 참조하십시오. 

### CLI를 사용한 계정 그룹 작성
{: #create-account-groups-cli}

다음 명령을 실행하여 계정 그룹을 작성하십시오. 계정 그룹을 다른 계정 그룹 내에 중첩시키려면 `--parent-account-group` 옵션에 계정 그룹의 이름을 지정하십시오. 다른 사용자가 계정 그룹의 담당자가 되도록 하려면 `--primary-contact-id` 옵션에 해당 사용자의 IBM ID를 지정하십시오. 

```
ibmcloud enterprise account-group-create NAME
[--parent-account-group ACCOUNT_GROUP_NAME] [--primary-contact-id USER_ID]
```
{: codeblock}

### API를 사용한 계정 그룹 작성
{: #create-account-groups-api}

엔터프라이즈 관리 API를 호출하여 프로그래밍 방식으로 엔터프라이즈에 계정 그룹을 작성할 수 있습니다. 

다음 샘플 요청은 엔터프라이즈 레벨 바로 아래에 하나의 계정 그룹을 작성합니다. 이 API를 호출할 때는 ID 변수를 자신의 엔터프라이즈의 값으로 대체하십시오. 계정 그룹을 다른 계정 그룹 내에 중첩시키려면 `crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID` 형식으로 클라우드 리소스 이름(CRN)에 계정 그룹의 ID를 지정하십시오. .

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/account-groups \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID",
  "name": "Sample Account Group",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-account-group){: external}.-->

## 엔터프라이즈 내에서의 계정 이동
{: #move-accounts}

엔터프라이즈 내에서는 어디로든 계정을 이동할 수 있습니다. 예를 들면 계정을 하위 계정 그룹에서 상위 계정 그룹으로 이동하거나, 엔터프라이즈 바로 아래로 이동할 수 있습니다. 계정은 엔터프라이즈 내에서만 이동할 수 있습니다. 이를 다른 엔터프라이즈로 이동하거나, 엔터프라이즈에서 제거하여 독립형 계정으로 전환할 수는 없습니다. 

계정을 이동하려면 엔터프라이즈 계정의 청구 서비스에 대한 관리자, 전체 엔터프라이즈에 대한 관리자 역할, 또는 현재 및 대상 계정 그룹에 대한 관리자 역할이 필요합니다. 

1. 엔터프라이즈 대시보드에서 **계정**을 클릭하십시오. 
1. 계정 섹션에서 계정에 대한 행에 있는 조치 아이콘을 클릭하고 **계정 이동**을 선택하십시오. 
1. 계정의 새 상위를 선택하고 **저장**을 클릭하십시오. 

### CLI를 사용한 계정 이동
{: #move-accounts-cli}

1. 엔터프라이즈에 있는 모든 계정을 나열하여 계정 이름 및 ID를 찾으십시오. 

   ```
   ibmcloud enterprise accounts --recursive
   ```
   {: codeblock}
1. 계정을 계정 그룹으로 이동하는 경우에는 해당 계정 그룹 이름과 ID를 찾으십시오. 

   ```
   ibmcloud enterprise account-groups
   ```
   {: codeblock}
1. 관련 옵션에 새 상위를 지정하여 계정을 이동하십시오. 

   계정을 계정 그룹으로 이동하려면 `--parent-account-group` 옵션에 계정 그룹 이름을 지정하십시오. 

   ```
   ibmcloud enterprise account-move -n NAME --parent-account-group ACCOUNT_GROUP_NAME
   ```
   {: codeblock}

   계정을 엔터프라이즈 바로 아래로 이동하려면 `--parent-enterprise` 옵션을 지정하십시오. 

   ```
   ibmcloud enterprise account-move -n NAME --parent-enterprise
   ```
   {: codeblock}

### API를 사용한 계정 이동
{: #move-account-api}

다음 샘플 요청에 표시되어 있는 바와 같이 엔터프라이즈 관리 API를 호출하여 계정을 이동할 수 있습니다. IAM 토큰 및 ID 변수를 자신의 엔터프라이즈의 값으로 대체하십시오. 

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_1"",
}'
```
{: codeblock}

<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#move-an-account-with-the-enterprise){: external}. -->
