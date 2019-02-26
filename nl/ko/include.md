---

copyright:

  years: 2017, 2019
lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 개인용 리소스에 계정 추가
{: #include}

작성된 {{site.data.keyword.Bluemix}} 개인용 리소스에는 기본적으로 제한이 있습니다. 계정의 관리자인 경우에는 포함 목록에 사용자를 추가하여 리소스를 볼 수 있는 사용자를 선택할 수 있습니다.
{:shortdesc: .shortdesc}

{{site.data.keyword.Bluemix}} [명령행 인터페이스(CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) 또는 콘솔을 사용하여 계정에 추가된 개인용 리소스를 사용자가 볼 수 있도록 허용하는 액세스 권한이 있는지 여부를 판별할 수 있습니다. 계정 소유자는 액세스 정책을 지정하여 콘솔에서 계정의 사용자에게 액세스를 제공할 수 있습니다. 자세한 정보는 [계정에 대한 액세스 관리](/docs/account?topic=account-find-access)를 참조하십시오.

## 리소스 찾기
{: #find-resource}

`ibmcloud catalog service <service-id or service-name>` 명령을 실행하십시오. service-id 또는 service-name 변수를 리소스 이름 또는 ID로 바꾸십시오. 리턴된 정보를 사용하면 리소스에 있는 항목의 하위 리소스를 표시하는 계층 구조를 볼 수 있습니다.

## 계정을 포함하여 가시성 설정
{: #vis-inc}

계정이 개인용 리소스를 볼 수 있도록 하려면 다음 명령을 실행하십시오.

`ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

includes-add 플래그 뒤에 계정과 연관된 ID 또는 쉼표로 구분된 이메일 목록을 추가할 수 있습니다.

명령을 실행한 후 리소스를 포함하는 프로세스는 약 30분 정도 걸립니다. 30분 후 계정에서 로그아웃한 다음 로그인하여 포함된 리소스를 확인하십시오.

## 포함 목록에서 계정 제거
{: #remove-exclude}

포함 목록에서 계정을 제거하려면 다음 명령을 실행하십시오.

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## 예: 하위 오브젝트의 가시성 관리
{: #child-vis}

리소스 또는 그 하위의 가시성을 관리할 수 있습니다. 비어 있는 포함 목록은 계정 관리자만 이를 볼 수 있음을 의미합니다. 이를 보려면 계정이 계정의 모든 구성원에 대한 포함 목록에 있어야 합니다.

다음 예에서는 `ibmcloud catalog service cloudant` 명령을 실행하여 Cloudant 서비스 인스턴스의 하위를 보는 방법을 보여줍니다.

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

하위 배치에 대한 리소스 ID를 가져온 후에 다음 명령을 실행하여 계정을 포함할 수 있습니다.

`ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`

오브젝트의 하위는 복잡한 방식으로 가시성을 상속할 수 있습니다. 하위 오브젝트가 개인용이면 고유 가시성 구성이 있습니다. 하지만 하위 오브젝트가 공용으로 설정된 경우에는 해당 상위 가시성을 상속합니다. 개인용 하위 오브젝트의 가시성을 설정하면 상위보다 더 해당 가시성이 제한될 수 있습니다. 가시성의 작동 방식에 대한 자세한 정보는 [카탈로그 API 문서](https://{DomainName}/apidocs/globalcatalog)를 참조하십시오.

## 개인용 리소스의 소유권 이전
{: #owners}

프로젝트 또는 조직을 떠나는 경우 계정의 소유권을 다른 사용자에게 이전하고자 할 수 있습니다.
{:shortdesc}

일단 소유권이 이전되면 계정에서 리소스를 더 이상 볼 수 없습니다. 이 조치를 되돌릴 수 없으므로 소유권 이전을 원하는지를 확실히 결정해야 합니다.
{: important}

[{{site.data.keyword.Bluemix}} 명령행 인터페이스(CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli)를 사용하여 개인용 리소스의 소유권을 이전할 수 있습니다. 다음 명령을 실행하십시오.

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
