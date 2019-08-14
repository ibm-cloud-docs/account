---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, multiple account

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 엔터프라이즈 작성
{: #create-enterprise}

{{site.data.keyword.Bluemix}} 엔터프라이즈는 기존 구독 계정으로부터 작성합니다. 엔터프라이즈를 작성하는 데 사용되는 계정은 해당 엔터프라이즈에 영구적으로 추가됩니다.
{:shortdesc}

## 시작하기 전에
{: #create-prereqs}

[{{site.data.keyword.Bluemix_notm}} 엔터프라이즈](/docs/account?topic=account-enterprise)를 작성하려면 구독 계정의 계정 소유자이거나, 이 계정의 청구 계정 관리 서비스에 대한 관리자 역할이 있어야 합니다.

엔터프라이즈를 작성하는 데 사용되는 구독 계정은 해당 엔터프라이즈로 영구적으로 이동됩니다. 엔터프라이즈로 계정을 이동하면 다음과 같은 영향이 있습니다.
* 계정에 대한 청구가 [엔터프라이즈에 의해 관리](/docs/billing-usage?topic=billing-usage-enterprise)되도록 전환됩니다. 전환 후, 해당 계정의 사용자는 미래 청구 기간에 대한 청구서, 지불 또는 구독과 같은 청구 및 지불 정보에 액세스할 수 없습니다. 청구를 보거나 관리하려면 해당 사용자가 엔터프라이즈 계정에 초대되어 해당 계정의 청구 서비스에 대한 액세스 권한을 부여받아야 합니다.
* 계정 내의 사용자 및 액세스 권한은 변경되지 않습니다. 계정 내의 액세스 권한은 엔터프라이즈와 별개이며, 사용자는 계정이 추가될 때 자동으로 엔터프라이즈 내부에 대한 액세스 권한을 얻지 않습니다. 그러나 이전에 언급된 바와 같이, 계정 내에서는 액세스 권한에 관계없이 더 이상 청구 정보를 사용할 수 없습니다.
* 계정 내의 리소스는 변경되지 않습니다. 적절한 액세스 권한이 있는 사용자는 해당 계정의 리소스에 대한 사용량 정보를 계속해서 볼 수 있습니다.

구독 계정이 없는 경우에는 [계정 업그레이드](/docs/account?topic=account-upgrading-account)에 설명되어 있는 바와 같이 계정을 업그레이드할 수 있습니다.

## 콘솔에서의 엔터프라이즈 작성
{: #create-console}

1. **관리 > 엔터프라이즈**로 이동하여 **작성**을 클릭하십시오.
1. 엔터프라이즈를 식별하기 위한 고유 이름을 입력하십시오. 일반적으로 이 이름은 `My organization's enterprise`와 같이 자신의 회사 또는 조직을 반영합니다. 필요한 경우에는 나중에 엔터프라이즈 이름을 편집할 수 있습니다.
1. 회사 또는 조직에 연관된 도메인 이름이 있는 경우에는 이를 **도메인** 필드에 입력하십시오. `example.com` 또는 `my.example.com`과 같이 임의의 도메인 또는 하위 도메인 형식을 지정할 수 있습니다.
1. 계정에 미치는 영향에 대한 정보를 검토하고 **계정에 미치는 영향을 이해했습니다**를 선택하십시오. 그 후 **작성**을 클릭하십시오.

   계정을 엔터프라이즈에 추가한 후에는 제거할 수 없습니다. 계정을 영구적으로 엔터프라이즈로 이동할 것인지 확인하십시오.
   {: important}

잠시 후 엔터프라이즈가 작성되고 엔터프라이즈 대시보드를 볼 수 있게 됩니다. 사용자의 IBM ID가 담당자로 나열되어 있습니다. 담당자는 청구 또는 사용량 질문과 같은 엔터프라이즈 관련 문제에 대한 담당자 역할을 수행합니다. 사용자는 엔터프라이즈를 관리할 추가 사용자를 초대할 수 있도록 엔터프라이즈 계정 소유자로도 지정됩니다.

**계정**을 클릭하여 다음 두 개의 계정을 포함하는 엔터프라이즈 계층 구조를 보십시오.

* 사용자를 초대하고 엔터프라이즈를 관리할 수 있도록 액세스 권한을 부여하는 엔터프라이즈 계정.
* 엔터프라이즈를 작성하는 데 사용한 계정. 해당 사용자와 리소스는 동일하게 유지되지만, 청구는 이제 엔터프라이즈에 의해 관리됩니다.

## CLI를 사용한 엔터프라이즈 작성
{: #create-cli}

1. 로그인하여 계정을 선택하십시오.

   ```
ibmcloud login
   ```
   {:codeblock}
1. 다음 명령을 실행하여 엔터프라이즈를 작성하십시오. 여기서 `NAME`은 엔터프라이즈를 식별하는 고유 이름입니다.

   ```
   ibmcloud enterprise create NAME [-d, --domain DOMAIN_NAME] [--primary-contact-id PRIMARY_CONTACT_USER_ID]
   ```
   {:codeblock}

   예를 들면, 다음 명령은 `examplecorp.com` 도메인이 있는 `Example Corp Enterprise`라는 엔터프라이즈를 작성합니다.

   ```
   ibmcloud enterprise create "Example Corp Enterprise" -d examplecorp.com
   ```
   {:codeblock}

   기본적으로 엔터프라이즈는 다음 역할이 있는 현재 로그인된 사용자를 사용하여 작성됩니다.
      * 엔터프라이즈 관련 문제에 대해 알릴 사람을 나타내는 엔터프라이즈 담당자
      * 엔터프라이즈 계정 관리에 대한 전체 액세스 권한이 있는 엔터프라이즈 계정 소유자

   `--primary-contact-id` 옵션에 다른 사용자의 IBM ID를 지정할 수 있습니다. 해당 사용자에게도 두 역할이 모두 지정됩니다.
1. 계정에 대한 영향을 검토하고 `y`를 입력하여 계속할 것임을 확인하십시오.
   ```
   Account abcde12345fghij67890 will be incorporated into enterprise My new enterprise
   (which cannot be undone). Do you want to proceed? [y/N]> y
   ```

엔터프라이즈가 작성되고 나면 두 개의 새 ID가 표시됩니다. 첫 번째 ID는 엔터프라이즈와 연관되어 있으며, 두 번째 ID는 엔터프라이즈를 관리하는 데 사용하는 엔터프라이즈 계정을 식별합니다.

```
ID:                      09876jihgf54321edcba   
Enterprise Account ID:   edcba12345jihgf67890
```

엔터프라이즈를 작성하는 데 사용된 계정은 이제 해당 엔터프라이즈의 일부입니다. [`ibmcloud enterprise accounts`](/docs/cli?topic=cloud-cli-ibmcloud_enterprise#ibmcloud_enterprise_accounts) 명령을 실행하여 엔터프라이즈에 있는 두 개의 계정(엔터프라이즈 계정과 엔터프라이즈를 작성하는 데 사용한 계정)을 보십시오.

## API를 사용한 엔터프라이즈 작성
{: #create-api}

다음 샘플 요청에 표시되어 있는 바와 같이 엔터프라이즈 관리 API를 호출하여 엔터프라이즈를 프로그래밍 방식으로 작성할 수 있습니다. API에 대한 세부사항은 [엔터프라이즈 관리 API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-enterprise){: external}를 참조하십시오.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/enterprises \
-H "Authorization: Bearer <Token>" \
-H 'Content-Type: application/json' \
-d '{
  "source_account_id": "a1b2c32a5ea94809a9840f5e23c362d",
  "name": "Sample Enterprise",
  "domain": "example.com",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

## 다음 단계
{: #create-next-steps}

기존 계정을 추가하거나 엔터프라이즈에서 새 계정을 작성하여 엔터프라이즈 구조를 확장하십시오. 자세한 정보는 [엔터프라이즈에 계정 추가](/docs/account?topic=account-enterprise-add)를 참조하십시오.

엔터프라이즈 관리를 도울 수 있도록 추가 사용자를 엔터프라이즈 계정으로 초대할 수도 있습니다. 예를 들면, 청구를 관리하고 사용량 비용을 추적할 재무 담당자를 초대하거나 계정을 관리할 부서 책임자를 초대할 수 있습니다. 사용자 초대 방법에 대한 자세한 정보는 [사용자 초대](/docs/iam?topic=iam-iamuserinv)를 참조하십시오.
