---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise settings, manage enterprise, view enterprise, rename enterprise

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 엔터프라이즈 관리
{: #enterprise-settings}

{{site.data.keyword.Bluemix}} 엔터프라이즈의 대시보드에서는 엔터프라이즈 세부사항을 보고, 계정 추가 및 사용자 초대와 같은 일반적인 조치를 수행하고, 청구 정보를 볼 수 있습니다. 대시보드에서, 또는 CLI나 API를 사용하여 엔터프라이즈의 이름을 바꿀 수도 있습니다.
{:shortdesc}

엔터프라이즈 설정을 관리하려면 엔터프라이즈 계정의 엔터프라이즈 서비스에 대한 관리자 또는 편집자 역할이 있어야 합니다.
{: tip}

## 콘솔에서의 엔터프라이즈 관리
{: #enterprise-manage}

엔터프라이즈 대시보드를 보려면 **관리 > 엔터프라이즈**로 이동하십시오. 이 대시보드는 엔터프라이즈에 있는 계정, 사용자 및 구독 크레딧에 대한 개요를 제공합니다. 대시보드에는 다음과 같은 일반 조치를 수행할 수 있도록 하는 빠른 링크가 있습니다.
   * [엔터프라이즈에 새 계정 또는 기존 계정 추가](/docs/account?topic=account-enterprise-add)
   * [엔터프라이즈 계정에 사용자 초대](/docs/iam?topic=iam-iamuserinv)
   * [구독 크레딧 보기 및 관리](/docs/billing-usage?topic=billing-usage-subscriptions)

엔터프라이즈 세부사항 섹션에서 **이름 바꾸기**를 클릭하여 엔터프라이즈의 이름을 바꿀 수도 있습니다.

## CLI에서의 엔터프라이즈 관리
{: #enterprise-manage-cli}

* 이름, 도메인, 소유자, 작성 및 업데이트 날짜와 같은 엔터프라이즈 정보를 보십시오.

  ```
  ibmcloud enterprise show
  ```
  {: codeblock}
* 다음 명령의 `-n` 옵션에 새 이름을 지정하여 엔터프라이즈의 이름을 바꾸십시오.

   ```
   ibmcloud enterprise update -n NEW_NAME
   ```
   {:codeblock}

## API를 사용한 엔터프라이즈 관리
{: #enterprise-manage-api}

다음 샘플 요청에 표시되어 있는 바와 같이 엔터프라이즈 관리 API를 호출하여 엔터프라이즈를 프로그래밍 방식으로 업데이트할 수 있습니다. API 호출에서 새 값을 전달하여 엔터프라이즈 이름 또는 도메인을 업데이트할 수 있습니다. API에 대한 세부사항은 [엔터프라이즈 관리 API 문서](https://{DomainName}/apidocs/enterprise-apis/enterprise#update-an-enterprise){: external}를 참조하십시오.

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID" \
-H "Authorization: $IAM_TOKEN" \
-H 'Content-Type: application/json' \
-d '{
  "name": "Brand New Sample Enterprise",
  "domain": "new.example.com"
}'
```
