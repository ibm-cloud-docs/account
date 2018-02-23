---

copyright:

  years: 2017, 2018
lastupdated: "2017-12-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 계정의 사용자에게 공용 리소스 숨기기
{: #exclude}

계정 관리자는 `bx` [명령행 인터페이스](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_catalog_entry_visibility_set)를 통해 제외 목록에 공용 리소스를 추가하여 계정의 모든 사용자에게 이 공용 리소스를 숨기도록 선택할 수 있습니다.
{:shortdesc: .shortdesc}

**참고:** 카탈로그에서 항목을 숨기면 Cloud Foundry CLI 또는 글로벌 탐색을 통해 사용 가능한 서비스 프로비저닝 목록(예: 금융, 모바일, Watson 및 웹 앱)에서 항목이 제거되지 않습니다.

## 액세스 권한이 있는지 여부를 확인하는 방법
{: #find-access}

CLI 또는 ID 및 액세스 UI를 사용하여 사용자가 계정에 추가된 개인용 리소스를 볼 수 있도록 하는 액세스 권한이 있는지 여부를 판별할 수 있습니다. 계정 소유자는 액세스 정책을 지정하여 Identity and Access Management UI를 통해 계정의 사용자에게 액세스를 제공할 수 있습니다. 자세한 정보는 [계정에 대한 액세스 관리](access.html)를 참조하십시오.

## 1단계: 리소스 찾기
{: #find-resource}

`bx catalog search <service-id or service-name>`을 입력하여 리소스를 검색하십시오. service-id 또는 service-name을 리소스 이름 또는 ID로 바꾸십시오. 리턴되는 정보에서 숨기려는 서비스의 이름 또는 ID를 찾으십시오.

## 2단계: 서비스 세부사항 가져오기

`bx catalog service <service-id or service-name>`을 입력하십시오. 이전 명령에서 찾은 내용을 사용할 때 리소스의 세부사항을 검토하려면 이 명령을 사용하십시오. 리턴되는 정보를 사용하면 리소스에 있는 항목의 하위 리소스를 표시하는 계층 구조를 볼 수 있습니다.

## 3단계: 리소스 숨기기
{: #vis-exc}

계정이 공용 리소스를 볼 수 없도록 하려면 다음 명령을 입력하십시오.

`bx catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

제외 플래그 다음에 계정과 연관된 계정 ID 또는 이메일의 쉼표로 구분된 목록을 추가할 수 있습니다.

명령을 실행한 후 리소스를 숨기는 프로세스는 30분 정도 걸립니다. 30분 후 계정에서 로그아웃한 다음 로그인하여 숨겨진 리소스를 확인하십시오.

**참고:** 숨겨진 항목은 UI 및 bx CLI에서 사용할 수 없습니다. 숨겨진 항목은 Cloud Foundry 마켓플레이스에 여전히 표시되지만, 숨겨진 플랜은 Cloud Foundry에서 프로비저닝되지 않습니다. 제외된 계정의 관리자는 여전히 리소스를 볼 수 있습니다.

## 제외 목록에서 계정 제거
{: #remove-exclude}

제외 목록에서 계정 ID 또는 이메일을 제거하려면 다음 명령을 입력하십시오.

`bx catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`

## 하위 오브젝트의 가시성 관리 예
{: #child}

모든 리소스의 가시성을 관리할 수 있습니다. 각 하위 리소스에는 개별 가시성 특성이 있습니다.

이 예에서 공용 Cloudant 서비스로부터 계정을 제외할 수 있습니다.

`bx catalog service cloudant`를 입력하면 리소스의 하위를 볼 수 있습니다.

```
ID                 cloudant
Name               cloudantnosqldb
Kind               service
Provider           IBM
Tags               data_management, ibm_created, ibm_dedicated_public, lite
Active             true
Description        Cloudant NoSQL DB is a fully managed data layer designed for modern web and mobile applications that leverages a flexible JSON schema. Cloudant is built upon and compatible with Apache CouchDB and accessible through a secure HTTPS API, which scales as your application grows. Cloudant is ISO27001 and SOC2 Type 1 certified, and all data is stored in triplicate across separate physical nodes in a cluster for HA/DR within a data center.
Bindable           true
RC Compatible      false
RC Provisionable   false
Children           Name                                          Kind         ID                                               Location
                   lite                                          plan         cloudant-lite
                   |__lite-eu-gb                             deployment   cloudant-lite:eu-gb                          eu-gb
                   |  |__lite-alias-eu-gb                    alias        cloudant-lite:alias:eu-gb                    eu-gb
                   |__lite-us-south                          deployment   cloudant-lite:us-south                       us-south
                      |__lite-alias-us-south                 alias        cloudant-lite:alias:us-south                 us-south
                   standard                                      plan         cloudant-standard
                   |__standard-eu-gb                         deployment   cloudant-standard:eu-gb                      eu-gb
                   |  |__standard-alias-eu-gb                alias        cloudant-standard:alias:eu-gb                eu-gb
                   |__standard-us-south                      deployment   cloudant-standard:us-south                   us-south
                      |__standard-alias-us-south             alias        cloudant-standard:alias:us-south             us-south
```

오브젝트에 대한 ID를 찾고 다음 명령으로 계정을 제외시키십시오. `bx catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

가시성 작동 방식에 대한 자세한 정보는 [API 문서](https://console.bluemix.net/apidocs/682)를 참조하십시오.
