---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-13"

keywords: change service, upgrade service, service plan

subcollection: account

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# 서비스 플랜 변경
{: #changing}

특정 {{site.data.keyword.Bluemix}} 서비스에 대해 플랜 변경이 사용으로 설정된 경우에는 해당 서비스의 플랜을 변경할 수 있습니다. 플랜을 변경하고자 할 수 있습니다(예: 플랜을 업그레이드하거나 축소함). 서비스 인스턴스 대시보드에서 플랜을 변경할 수 있습니다.
{: shortdesc}

계정 유형 업그레이드에 대한 세부사항을 알고 싶으십니까? 자세한 정보는 [계정 업그레이드](/docs/account?topic=account-upgrading-account)를 참조하십시오.
{: tip}

특정 서비스에 대해서만 서비스 플랜을 변경할 수 있습니다. 서비스에 대해 플랜 변경이 가능하면 서비스 인스턴스 대시보드가 탐색에서 **플랜** 옵션을 표시합니다. 플랜을 변경하는 경우 서비스마다 수행할 다음 단계 세트가 다릅니다.

1. 서비스 인스턴스 대시보드에서 **플랜**을 클릭하십시오. 일반적으로 플랜을 업그레이드하거나 플랜을 낮출 수 있습니다.
2. 플랜이 변경되면 추가 단계를 완료해야 합니다. 플랜 변경 유형과 서비스에 따라 단계는 달라집니다. 예를 들어, 플랜을 낮추는 경우 앱을 다시 스테이징해야 합니다. 또는 플랜을 업그레이드한 경우에는 앱을 다시 스테이징하고 기타 조치를 수행해야 할 수 있습니다.

   앱을 다시 스테이징하려면 리소스 목록으로 이동하여 서비스가 바인드되어 있는 앱을 찾으십시오. 메뉴 아이콘 ![메뉴 아이콘](../icons/icon_hamburger.svg) **> 리소스 목록**을 클릭하십시오. 앱 메뉴에서 **앱 다시 시작**을 선택하십시오.

  추가로 필요한 조치에 대한 자세한 정보는 해당 서비스에 대한 문서를 참조하십시오.

## CLI를 통한 플랜 변경
{: #changing_command_line}

콘솔을 사용하는 대신 {{site.data.keyword.Bluemix_notm}} 명령행 인터페이스(CLI)를 사용하여 서비스의 플랜을 변경할 수 있습니다.

1. 서비스가 리소스 제어기에서 사용할 수 있도록 설정되었는지 확인하십시오.

   ```
   ibmcloud catalog service <service_name>
   ```
   {:codeblock}

   서비스가 리소스 제어기(RC)에서 사용할 수 있도록 설정된 경우에는 `RC Compatible true`가 나열됩니다. 변경할 플랜의 ID를 기록하십시오.

   ```
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. 서비스 인스턴스의 플랜을 변경하십시오.

   - RC 사용 서비스의 경우에는 [`ibmcloud resource service-instance-update` 명령](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource)을 사용하여 플랜을 변경하십시오.

     ```
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}

   - RC를 사용하지 않아 Cloud Foundry를 기반으로 하는 서비스의 경우에는 [`ibmcloud cf update-service` 명령](/docs/cli/reference/ibmcloud?topic=cloud-cli-cf#cf)을 사용하여 플랜을 변경하십시오.

     ```
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {:codeblock}
