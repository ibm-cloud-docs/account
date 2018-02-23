---

copyright:

  years: 2017, 2018
lastupdated: "2017-12-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 개인용 리소스에 계정 추가
{: #include}

작성한 개인용 리소스는 기본적으로 제한됩니다. 계정 관리자는 `bx` [명령행 인터페이스](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_catalog_entry_visibility_set)를 통해 포함 목록에 리소스를 추가하여 이 리소스를 볼 수 있는 사용자를 선택할 수 있습니다.
{:shortdesc: .shortdesc}

## 액세스 권한이 있는지 여부를 확인하는 방법
{: #find-access}

CLI 또는 ID 및 액세스 UI를 사용하여 사용자가 계정에 추가된 개인용 리소스를 볼 수 있도록 하는 액세스 권한이 있는지 여부를 판별할 수 있습니다. 계정 소유자는 액세스 정책을 지정하여 Identity and Access Management UI를 통해 계정의 사용자에게 액세스를 제공할 수 있습니다. 자세한 정보는 [계정에 대한 액세스 관리](access.html)를 참조하십시오.

## 1단계: 리소스 찾기
{: #find-resource}

`bx catalog service <service-id or service-name>`을 입력하십시오. service-id 또는 service-name을 리소스 이름 또는 ID로 바꾸십시오. 리턴되는 정보를 사용하면 리소스에 있는 항목의 하위 리소스를 표시하는 계층 구조를 볼 수 있습니다.

## 2단계: 계정을 포함하여 가시성 설정
{: #vis-inc}

계정이 개인용 리소스를 볼 수 있도록 하려면 다음 명령을 입력하십시오.

`bx catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

포함-추가 플래그 다음에 계정과 연관된 ID 또는 이메일의 쉼표로 구분된 목록을 추가할 수 있습니다.

명령을 실행한 후 리소스를 포함하는 프로세스는 30분 정도 걸립니다. 30분 후 계정에서 로그아웃한 다음 로그인하여 포함된 리소스를 확인하십시오.

## 포함 목록에서 계정 제거
{: #remove-exclude}

포함 목록에서 계정을 제거하려면 다음 명령을 입력하십시오.

`bx catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## 하위 오브젝트의 가시성 관리
{: #child-vis}

리소스 또는 그 하위의 가시성을 관리할 수 있습니다.

비어 있는 포함 목록은 계정 관리자만 볼 수 있음을 의미합니다. 이를 보려면 계정이 계정의 모든 구성원에 대한 포함 목록에 있어야 합니다.

예를 들어, `bx catalog service <your_service>`를 입력하면 리소스의 하위를 볼 수 있습니다.

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

하위 배치에 대한 리소스 ID를 가져온 다음 다음 명령을 사용하여 계정을 포함할 수 있습니다. `bx catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`.

오브젝트의 하위는 복잡한 방식으로 가시성을 상속할 수 있습니다. 하위 오브젝트가 개인용이면 고유 가시성 구성이 있습니다. 하지만 하위 오브젝트가 공용으로 설정된 경우에는 해당 상위 가시성을 상속합니다. 개인용 하위 오브젝트에서 가시성을 설정하면 상위보다 많이 가시성을 제한할 수 있습니다.

가시성 작동 방식에 대한 자세한 정보는 [API 문서](https://console.bluemix.net/apidocs/682)를 참조하십시오.
