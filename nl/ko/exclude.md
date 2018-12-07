---

copyright:

  years: 2017, 2018
lastupdated: "2018-11-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}


# 사용자에게 공용 리소스 숨기기
{: #exclude}

{{site.data.keyword.Bluemix}} 계정의 관리자는 계정에 대한 액세스 권한이 있는 사용자에게 공용 리소스를 숨길 수 있습니다. 리소스를 숨겨서 비인가된 사용자에게 민감한 정보를 숨길 수 있습니다. 또는 일부 정보는 한정된 수의 사용자에 의해서만 액세스되어야 할 수 있습니다.
{:shortdesc}

카탈로그에서 리소스를 숨기는 경우 금융, 모바일, Watson 및 웹 앱 등의 {{site.data.keyword.Bluemix_notm}} 콘솔 탐색에서 사용 가능한 오퍼링 카테고리 목록에서 또는 Cloud Foundry 명령행 인터페이스(CLI)에서 해당 리소스가 제거되지는 않습니다.
{: note}

{{site.data.keyword.Bluemix}} [명령행 인터페이스(CLI)](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set) 또는 콘솔을 사용하여 계정에 추가된 개인용 리소스를 사용자가 볼 수 있도록 허용하는 액세스 권한이 있는지 여부를 판별할 수 있습니다. 계정 소유자는 액세스 정책을 지정하여 콘솔에서 계정의 사용자에게 액세스를 제공할 수 있습니다. 자세한 정보는 [계정에 대한 액세스 관리](access.html)를 참조하십시오.

## 리소스 찾기
{: #find-resource}

`ibmcloud catalog search <service-id or service-name>` 명령을 실행하여 리소스를 검색할 수 있습니다. service-id 또는 service-name 변수를 리소스 이름 또는 ID로 바꾸십시오. 리턴된 정보를 사용하여 숨기려는 서비스의 이름 또는 ID를 찾으십시오.

## 리소스의 세부사항 가져오기

`ibmcloud catalog service <service-id or service-name>` 명령을 실행하십시오. 이전 명령의 실행에서 리턴된 정보를 사용하면 이 명령을 사용하여 리소스에 대한 세부사항을 검토할 수 있습니다. 리턴된 정보를 사용하면 리소스에 있는 항목의 하위 리소스를 표시하는 계층 구조를 볼 수 있습니다.

## 리소스 숨기기
{: #vis-exc}

계정의 사용자가 공용 리소스를 볼 수 없도록 방지하려면 다음 명령을 실행하십시오.

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

제외 플래그 다음에 계정과 연관된 계정 ID 또는 이메일의 쉼표로 구분된 목록을 추가할 수 있습니다. 

명령을 실행한 후 리소스를 숨기는 프로세스는 약 30분 정도 걸립니다. 30분 후 계정에서 로그아웃한 다음 로그인하여 숨겨진 리소스를 확인하십시오. 

숨긴 항목은 콘솔 또는 CLI에서 사용 가능하지 않습니다. 제외된 계정의 관리자는 여전히 리소스를 볼 수 있습니다.
{: note}

## 제외 목록에서 계정 제거
{: #remove-exclude}

제외 목록에서 계정 ID 또는 이메일을 제거하려면 다음 명령을 실행하십시오. 

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`


## 예: 하위 오브젝트의 가시성 관리
{: #child}

모든 리소스의 가시성을 관리할 수 있습니다. 각 하위 리소스에는 개별 가시성 특성이 있습니다. 이 예에서는 Cloudant 서비스로부터 계정을 제외할 수 있는 방법을 보여줍니다. 

리소스의 모든 하위를 보려면 `ibmcloud catalog service cloudant` 명령을 실행하십시오. 

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

`ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>` 명령을 실행하여 오브젝트의 ID를 찾고 계정을 제외하십시오. 

가시성의 작동 방식에 대한 자세한 정보는 [카탈로그 API 문서](https://{DomainName}/apidocs/globalcatalog)를 참조하십시오. 
