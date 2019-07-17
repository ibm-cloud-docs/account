---

copyright:
  years: 2019
lastupdated: "2019-07-01"

keywords: VRF, virtual routing and forwarding, service endpoint, private network

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# VRF 및 서비스 엔드포인트 사용
{: #vrf-service-endpoint}

기본적으로 {{site.data.keyword.Bluemix}} 공용 네트워크를 통해 계정의 리소스에 연결합니다. VRF(Virtual Routing and Forwarding)를 사용하여 계정의 IP 라우팅 및 모든 해당 리소스를 개별 라우팅 테이블로 이동할 수 있습니다. VRF가 사용 가능한 경우 공용 네트워크를 사용하지 않고 {{site.data.keyword.Bluemix_notm}} 서비스 엔드포인트를 사용하여 리소스에 직접 연결할 수 있습니다.
{:shortdesc}

VRF(Virtual Routing and Forwarding) 및 {{site.data.keyword.Bluemix_notm}} 서비스 엔드포인트를 사용하려면 청구 가능한 계정이 필요합니다.

## VRF 사용
{: #vrf}

VRF를 사용하면 라우팅 테이블의 여러 인스턴스가 라우터에 존재하고 동시에 작동할 수 있습니다. VRF를 사용으로 설정하면 개별 라우팅 테이블이 계정에 맞게 작성되고 계정의 리소스 연결이 {{site.data.keyword.Bluemix_notm}} 네트워크에서 개별적으로 라우팅됩니다. VRF는 계정 레벨에서 사용 가능하므로 모든 리소스가 이 네트워크 변경의 영향을 받습니다. VRF 기술 및 계정의 네트워크 라우팅에 미치는 영향에 대한 자세한 정보는 [{{site.data.keyword.Bluemix_notm}}의 VRF(Virtual Routing and Forwarding)](/docs/resources?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud)를 참조하십시오.

VRF를 사용으로 설정하면 계정의 네트워크가 영구적으로 변경됩니다. 계정 및 리소스에 대한 영향을 확인하십시오. VRF를 사용으로 설정한 후에는 사용 안함으로 설정할 수 없습니다.
{: important}

VRF를 사용으로 설정하려면 요청과 함께 지원 케이스를 작성하십시오.

1. 콘솔에서 **지원**으로 이동하고 **케이스 작성**을 클릭하십시오.
1. **계정 및 액세스**를 지원 유형으로 선택하십시오.
1. **주제** 필드에 `개인 네트워킹 질문`을 입력하십시오.
1. **설명** 필드에 _enter your account number_를 {{site.data.keyword.Bluemix_notm}} 계정 번호로 바꿔 다음 메시지를 입력하십시오.

   `We are requesting that account *enter your account number* is moved to its own VRF. We understand the risks and approve the change. Please reply back with the scheduled window(s) of time where this change will be made so we can prepare for the migration.`

{{site.data.keyword.Bluemix_notm}} 네트워크 엔지니어링 팀이 케이스 소유자에게 연락하여 계정의 네트워킹을 VRF로 변환하는 시간을 스케줄합니다. 변환 프로세스 중에 계정의 리소스 연결이 패킷 손실로 인해 불안정해질 수 있습니다. 이 변환은 계정의 복잡도에 따라 약 15 - 30분이 소요됩니다. 계정에 레거시 {{site.data.keyword.BluDirectLink}} 연결이 있는 경우 시간이 더 걸릴 수 있습니다.


## 서비스 엔드포인트 사용
{: #service-endpoint}

{{site.data.keyword.Bluemix_notm}} 서비스 엔드포인트를 계정에 사용하는 경우 리소스 작성 시 사설 네트워크 엔드포인트를 노출하도록 선택할 수 있습니다. 그런 다음 공용 네트워크가 아닌 {{site.data.keyword.Bluemix_notm}} 사설 네트워크를 통해 이 엔드포인트에 직접 연결할 수 있습니다. 사설 네트워크 엔드포인트를 사용하는 리소스에 인터넷 라우팅 가능 IP 주소가 없으므로 이러한 리소스에 대한 연결이 더 안전합니다. 자세한 정보는 [사설 네트워크 연결을 위한 서비스 엔드포인트](/docs/resources?topic=resources-service-endpoints)를 참조하십시오.

서비스 엔드포인트를 사용하려면 먼저 계정에 대해 VRF를 사용으로 설정해야 합니다.
{: note}

CLI에서 서비스 엔드포인트를 사용으로 설정하려면 [{{site.data.keyword.Bluemix_notm}} CLI](/docs/cli?topic=cloud-cli-getting-started)의 버전 0.13 이상이 필요합니다.

1.  서비스 엔드포인트가 계정에서 이미 사용 가능한지 확인하십시오.

    ```
ibmcloud account show
    ```
    {: codeblock}

    다음 예제에 표시된 대로 `Service Endpoint Enabled`가 `false`인 경우 서비스 엔드포인트를 사용할 수 없습니다.

    ```
    Retrieving account Mia Example's Account of m.example@example.com...
    OK

    Account ID:                   abc123d0bc2edefthyufffc9b5ca318   
    Currently Targeted Account:   true   
    Linked Softlayer Account:     0123456   
    Service Endpoint Enabled:     false  
    ```
    {: screen}
1. 다음 명령을 실행하여 서비스 엔드포인트를 사용으로 설정하십시오.

   ```
ibmcloud account update --service-endpoint-enable true
   ```
   {: codeblock}

   이 변경사항을 적용하려면 몇 분이 걸릴 수 있습니다. 명령이 완료되면 `ibmcloud account show` 명령을 다시 실행하여 확인할 수 있습니다.

    계정에 VRF를 사용할 수 없는 경우 이 명령을 실행하면 이를 사용으로 설정할 케이스를 작성할지 묻는 프롬프트가 표시됩니다. `y`를 입력하여 지원 케이스를 작성하십시오. 계정에서 VRF를 사용으로 설정한 후 다시 명령을 실행하여 계정에서 서비스 엔드포인트 연결을 사용으로 설정하십시오.

    ```
    Service Endpoint is not available in linked Softlayer Account 1008967.
    Enable VRF(Virtual Routing and Forwarding) first to proceed.
    Learn more about VRF here - https://cloud.ibm.com/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html.

    Do you want to open a ticket to enable it?[y/N]> y
    Ticket 70729615 was opened successfully. Follow the link https://control.softlayer.com/support/tickets/70729876 to check the details and track the status of the ticket. You will be required to login to view this ticket.
    Account ID:    1008967
    Ticket:        Private Network Question
    ```
    {: screen}


서비스 엔드포인트가 사용 가능하게 되면 {{site.data.keyword.Bluemix_notm}} 사설 네트워크를 통해 연결되는 리소스를 작성할 수 있습니다. 서비스 엔드포인트를 지원하는 서비스 목록 및 자세한 정보는 [사설 네트워크 엔드포인트 설정](/docs/resources?topic=resources-private-network-endpoints)을 참조하십시오.
