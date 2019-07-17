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

# 启用 VRF 和服务端点
{: #vrf-service-endpoint}

缺省情况下，通过 {{site.data.keyword.Bluemix}} 公用网络连接到帐户中的资源。您可以启用虚拟路由和转发 (VRF) 以将帐户的 IP 路由及其所有资源移至单独的路由表中。如果启用 VRF，那么可启用 {{site.data.keyword.Bluemix_notm}} 服务端点以直接连接至资源而不使用公用网络。
{:shortdesc}

要启用虚拟路由和转发以及 {{site.data.keyword.Bluemix_notm}} 服务端点，需要计费帐户。

## 启用 VRF
{: #vrf}

VRF 允许路由器中存在路由表的多个实例并且同时工作。在启用 VRF 时，将针对帐户创建单独的路由表，并且在 {{site.data.keyword.Bluemix_notm}} 网络上单独路由与帐户资源之间的连接。VRF 在帐户级别启用，因此所有资源都受此联网更改的影响。有关 VRF 技术及其对帐户网络路由的影响的更多信息，请参阅 [{{site.data.keyword.Bluemix_notm}} 上的虚拟路由和转发](/docs/resources?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud)。

启用 VRF 会永久更改帐户的联网。请确保了解对帐户和资源的影响。启用 VRF 后，无法禁用。
{: important}

要启用 VRF，请通过请求创建支持案例。

1. 在控制台中，转至**支持**，然后单击**创建案例**。
1. 选择**帐户和访问权**作为支持类型。
1. 在**主题**字段中，输入`专用联网问题`。
1. 在**描述**字段中，输入以下消息，将_输入您的帐号_替换为您的 {{site.data.keyword.Bluemix_notm}} 帐号。

   `我们请求将帐户 *输入您的帐号* 移动到其自己的 VRF。我们了解相关风险并同意更改。请在回复中告知安排执行此更改的时间范围，以便我们准备进行迁移。`

{{site.data.keyword.Bluemix_notm}} 网络工程团队将与案例所有者联系以安排将帐户联网转换为 VRF 的时间。转换过程中，由于包丢失，与帐户中资源的连接可能不稳定。根据帐户的复杂性，转换大约需要 15 到 30 分钟时间。如果帐户具有旧的 {{site.data.keyword.BluDirectLink}} 连接，那么可能需要更多时间。


## 启用服务端点
{: #service-endpoint}

在帐户中启用 {{site.data.keyword.Bluemix_notm}} 服务端点时，可以选择在创建资源时公开专用网络端点。然后，可以直接通过 {{site.data.keyword.Bluemix_notm}} 专用网络连接到此端点，而不是公用网络。因为使用专用网络端点的资源没有可通过因特网路由的 IP 地址，因此与这些资源的连接更加安全。有关更多信息，请参阅[专用网络连接的服务端点](/docs/resources?topic=resources-service-endpoints)。

必须先针对帐户启用 VRF，然后才能启用服务端点。
{: note}

要从 CLI 启用服务端点，需要 V0.13 或更高版本的 [{{site.data.keyword.Bluemix_notm}} CLI](/docs/cli?topic=cloud-cli-getting-started)。

1.  检查是否已在帐户中启用服务端点。

    ```
ibmcloud account show
```
    {: codeblock}

    如果如以下示例中所示，`服务端点已启用`为 `false`，那么未启用服务端点。

    ```
    正在检索 m.example@example.com 的帐户 Mia Example's Account..
    OK

    帐户标识：                    abc123d0bc2edefthyufffc9b5ca318   
    当前目标帐户：                true   
    链接的 Softlayer 帐户：       0123456   
    服务端点已启用：              false  
    ```
    {: screen}
1. 通过运行以下命令来启用服务端点。

   ```
ibmcloud account update --service-endpoint-enable true
```
   {: codeblock}

   此更改可能需要几分钟时间才能生效。命令完成后，您可以再次运行 `ibmcloud account show` 命令以进行验证。

    如果未针对帐户启用 VRF，那么运行此命令将提示您创建案例以进行启用。输入 `y` 以创建支持案例。在帐户中启用 VRF 后，再次运行命令以启用帐户中的服务端点连接。

    ```
    服务端点在链接的 Softlayer 帐户 1008967 中不可用。
    在继续操作之前，请先启用 VRF（虚拟路由和转发）。
    要了解有关 VRF 的更多信息，请参阅 https://cloud.ibm.com/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html。

    是否要开具凭单以启用 VRF？[y/N]> y
    已成功开具凭单 70729615。请访问链接 https://control.softlayer.com/support/tickets/70729876 以检查详细信息并跟踪凭单的状态。您需要登录才能查看此凭单。
    帐户标识：     1008967
    凭单：         专用网络问题
    ```
    {: screen}


启用服务端点后，可以创建通过 {{site.data.keyword.Bluemix_notm}} 专用网络连接的资源。有关支持服务端点的服务列表和更多信息，请参阅[设置专用网络端点](/docs/resources?topic=resources-private-network-endpoints)。
