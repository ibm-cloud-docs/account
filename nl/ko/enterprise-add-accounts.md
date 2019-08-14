---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise, add account, import account, create account

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 엔터프라이즈에 계정 추가
{: #enterprise-add}

{{site.data.keyword.Bluemix}} 계정을 추가해 엔터프라이즈를 확장할 수 있습니다. 계정을 추가하려는 경우에는 다른 엔터프라이즈에 속해 있지 않은 기존 계정을 가져오거나 엔터프라이즈 내에서 새 계정을 작성할 수 있습니다.
{:shortdesc}

엔터프라이즈에 여러 계정이 속하게 되면 계정 그룹을 사용하여 서로 관련된 계정을 그룹으로 구성할 수 있습니다. 자세한 정보는 [엔터프라이즈의 계정 체계화](/docs/account?topic=account-enterprise-organize)를 참조하십시오.

## 기존 계정 가져오기
{: #add-accounts}

기존 계정을 엔터프라이즈로 가져올 수 있습니다. 가져온 계정은 제거할 수 없으며, 각 계정은 하나의 엔터프라이즈에만 속할 수 있습니다. Lite 또는 평가판 계정을 가져오는 경우 이는 자동으로 [종량과금제 계정](/docs/account?topic=account-accounts)으로 업그레이드됩니다.

엔터프라이즈로 계정을 가져오면 다음과 같은 영향이 있습니다.
* 계정에 대한 청구가 엔터프라이즈에 의해 관리되도록 전환됩니다. 전환 후, 해당 계정의 사용자는 미래 청구 기간에 대한 청구서, 지불 또는 구독과 같은 청구 및 지불 정보에 액세스할 수 없습니다. 청구를 보거나 관리하려면 해당 사용자가 엔터프라이즈 계정에 초대되어 해당 계정의 청구 서비스에 대한 액세스 권한을 부여받아야 합니다. 자세한 정보는 [엔터프라이즈의 청구 및 사용량을 중앙 집중식으로 관리](/docs/billing-usage?topic=billing-usage-enterprise)를 참조하십시오.
* 계정 내의 사용자 및 액세스 권한은 변경되지 않습니다. 계정 내의 액세스 권한은 엔터프라이즈와 별개이며, 사용자는 계정을 가져올 때 자동으로 엔터프라이즈 내부에 대한 액세스 권한을 얻지 않습니다.
* 계정 내의 리소스는 변경되지 않습니다. 적절한 액세스 권한이 있는 사용자는 해당 계정의 리소스에 대한 사용량 정보를 계속해서 볼 수 있습니다.

기존 계정을 엔터프라이즈로 가져오려면 다음 액세스 권한이 필요합니다.

   * 가져오는 계정에서 사용자가 계정 소유자이거나, 사용자에게 계정 내의 청구 서비스에 대한 관리자 역할이 있어야 합니다.
   * 엔터프라이즈에서 사용자에게 엔터프라이즈 서비스에 대한 편집자 또는 관리자 역할이 있고, 청구 서비스에 대한 관리자 역할이 있어야 합니다.

기존 계정을 가져오려면 다음 단계를 완료하십시오.

1. 엔터프라이즈 계정에 로그인하여 **관리 > 엔터프라이즈**로 이동하십시오.
1. **계정**을 클릭하여 엔터프라이즈의 계정 및 계정 그룹을 보십시오. 계정 섹션에서 **추가 > 계정 가져오기**를 선택하십시오.
1. 가져올 계정을 선택하십시오.

   표시되는 계정이 없는 경우에는 기존 계정에서 적절한 액세스 권한이 없을 가능성이 높습니다.
   {: tip}
1. 계정을 계정 그룹에 추가하려는 경우에는 해당 계정의 상위로 설정할 계정 그룹을 선택하십시오. 선택되는 상위가 해당 계정이 엔터프라이즈 계층 구조에서 차지하는 위치를 결정합니다.
1. 계정에 미치는 영향에 대한 정보를 검토하고 **계정에 미치는 영향을 이해했습니다**를 선택하십시오. 그 후 **가져오기**를 클릭하십시오.

   계정을 엔터프라이즈로 가져온 후에는 제거할 수 없습니다. 계정을 영구적으로 엔터프라이즈로 이동할 것인지 확인하십시오.
   {: important}

### CLI를 사용한 계정 가져오기
{: #add-account-cli}

1. 엔터프라이즈로 가져올 계정의 ID를 찾으십시오.

   ```
ibmcloud account list
   ```
   {: codeblock}
1. 계정을 계정 그룹에 추가하려는 경우에는 엔터프라이즈에 있는 기존 계정 그룹의 이름 및 ID를 찾으십시오.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. `--account ID` 매개변수에 계정 ID를 지정하여 계정을 엔터프라이즈로 가져오십시오. 상위 계정 그룹을 지정하지 않으면 계정이 엔터프라이즈 바로 아래에 추가됩니다.

   ```
   ibmcloud enterprise account-import --account-id ID
   [--parent-account-group ACCOUNT_GROUP_NAME | --parent-account-group-id ACCOUNT_GROUP_ID]
   ```
   {: codeblock}

### API를 사용한 계정 가져오기
{: #add-account-api}

기존 계정을 엔터프라이즈로 가져오려는 경우에는 다음 샘플 요청에 표시되어 있는 바와 같이 [엔터프라이즈 관리 API](https://{DomainName}/apidocs/enterprise-apis/enterprise#import-an-account-into-an-enterprise){: external}를 호출하십시오. {{site.data.keyword.Bluemix_notm}} Identity and Access Management(IAM) 토큰 및 ID 변수를 자신의 엔터프라이즈의 값으로 대체하십시오.

```
curl -X PUT \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID/import/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" -H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID"
}'
```
{: codeblock}

## 새 계정 작성
{: #create-accounts}

엔터프라이즈에서 새 계정을 작성할 수 있습니다. 이 계정은 종량과금제 계정으로 작성되며 사용량은 엔터프라이즈에 청구됩니다. 계정을 작성하려면 엔터프라이즈 서비스에 대한 편집자 또는 관리자 역할이 있는 액세스 정책이 필요합니다.

1. 엔터프라이즈 대시보드에서 **계정**을 클릭하여 엔터프라이즈의 계정 및 계정 그룹을 보십시오.
1. 계정 섹션에서 **추가 > 계정 작성**을 선택하십시오.
1. 계정의 이름을 엔터프라이즈에서 고유하도록 입력하십시오. 이는 많은 계정 중 하나이므로, 고유한 설명적 이름을 지정하면 계정의 용도를 한 눈에 파악하는 데 도움이 됩니다.
1. 다른 사용자를 계정 소유자로 지정하려는 경우에는 **소유자** 필드에 해당 사용자의 IBM ID를 입력하십시오. 계정 소유자는 계정을 관리하기 위한 전체 액세스 권한을 갖습니다.
1. 계정을 계정 그룹에 추가하려는 경우에는 해당 계정의 상위로 설정할 계정 그룹을 선택하십시오. 선택되는 상위가 해당 계정이 엔터프라이즈 계층 구조에서 차지하는 위치를 결정합니다.
1. **작성**을 클릭하십시오.

계정을 작성하고 나면, 계정 소유자는 계정에 로그인하여 다른 사용자를 초대하고 이들의 액세스 권한을 관리할 수 있습니다.

### CLI를 사용한 계정 작성
{: #create-accounts-cli}

1. 계정을 계정 그룹에 추가하려는 경우에는 기존 계정 그룹의 이름 및 ID를 찾으십시오.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. 다음 명령을 실행하여 계정을 작성하십시오. 상위 계정 그룹을 지정하지 않으면 계정이 엔터프라이즈 바로 아래에 추가됩니다. 다른 사용자를 계정 소유자로 설정하려면 `--owner` 옵션에 해당 사용자의 IBM ID를 지정하십시오.

   ```
   ibmcloud enterprise account-create NAME
   [--parent-account-group ACCOUNT_GROUP_NAME] [--owner USER_ID]
   ```
   {: codeblock}

### API를 사용한 계정 작성
{: #create-account-api}

엔터프라이즈에 새 계정을 작성하려는 경우에는 IAM 토큰 및 ID 변수를 자신의 엔터프라이즈의 값으로 대체하여, 다음 샘플 요청에 표시되어 있는 바와 같이 엔터프라이즈 관리 API를 호출하십시오. API에 대한 세부사항은 [엔터프라이즈 관리 API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-a-new-account-in-an-enterprise){: external}를 참조하십시오.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/accounts \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID",
  "name": "Sample Account",
  "owner_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}
