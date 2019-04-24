---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-13"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 帐户类型
{: #accounts}

{{site.data.keyword.Bluemix_notm}} 有三种不同的帐户类型：轻量、现收现付和预订。您注册后，随即会获得免费的轻量帐户。“现收现付”和“预订”是计费帐户选项，每个选项提供有不同的功能。请比较每个帐户并选择最适合您需要的帐户类型。
{:shortdesc}


## 对比帐户
{: #compare}

下表提供了轻量、现收现付和预订帐户的比较。有关每种帐户的更多详细信息，请参阅后面的各部分。

|                                         |轻量|现收现付|预订|
|-----------------------------------------|--------------------|--------------------|--------------------|
|**访问免费的 Cloud Foundry 内存**|256 MB|512 MB|512 MB|
|**访问[轻量服务套餐 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://{DomainName}/catalog/?search=label:lite){: new_window}**| ![功能可用](../icons/icon_enabled.svg) | ![功能可用](../icons/icon_enabled.svg) | ![功能可用](../icons/icon_enabled.svg) |
|**访问所有免费套餐**|                    | ![功能可用](../icons/icon_enabled.svg) | ![功能可用](../icons/icon_enabled.svg) |
|**访问完整 {{site.data.keyword.Bluemix_notm}} 目录**|  | ![功能可用](../icons/icon_enabled.svg) | ![功能可用](../icons/icon_enabled.svg) |
|**访问多个 Cloud Foundry 区域**|               | ![功能可用](../icons/icon_enabled.svg) | ![功能可用](../icons/icon_enabled.svg) |
|**无时间限制**| ![功能可用](../icons/icon_enabled.svg) | ![功能可用](../icons/icon_enabled.svg) | ![功能可用](../icons/icon_enabled.svg) |
|**保证零成本**| ![功能可用](../icons/icon_enabled.svg) |  |         |
|**折扣定价**|                    |                    | ![功能可用](../icons/icon_enabled.svg) |
|**学习或构建概念验证的最佳选择**| ![功能可用](../icons/icon_enabled.svg) | ![功能可用](../icons/icon_enabled.svg) |  |
|**适合生产用例**|                    | ![功能可用](../icons/icon_enabled.svg) | ![功能可用](../icons/icon_enabled.svg) |
{: caption="表 1. {{site.data.keyword.Bluemix_notm}} 帐户比较" caption-side="top"}


## 轻量帐户
{: #liteaccount}

注册轻量帐户可在 {{site.data.keyword.Bluemix_notm}} 控制台中使用所选的显示有轻量标记 ![轻量标记](../icons/Lite.svg) 的免费轻量套餐来构建应用程序和探索服务。轻量帐户不会到期，也无需信用卡。

您有权访问为您创建的名为 `Default` 的单个资源组。由 {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) 管理的所有服务实例都会自动添加到此资源组。可以随时更新此资源组的名称。有关详细步骤，请参阅[重命名资源组](/docs/resources?topic=resources-rgs#rename_rgs)。

每个资源组都是免费的。在创建 IAM 管理的服务与 Cloud Foundry 应用程序之间的连接时，将创建别名（即服务实例），此别名会计入配额。请参阅[管理连接](/docs/resources?topic=resources-connect_app)。
{: tip}

### 可用功能
{: #lite-account-features}

请查看轻量帐户中提供的关键功能的以下列表：

   * 帐户是免费的 - 不需要信用卡。
   * 帐户永不过期。
   * 可以在一个 {{site.data.keyword.Bluemix_notm}} 区域中使用一个组织。
   * 基本 {{site.data.keyword.Bluemix_notm}} 支持是免费的。对于非生产环境或未使用传统严重性和未规定特定响应时间的工作负载，提供了基本支持。
   * 您会收到有关帐户状态和配额限制的电子邮件通知。
   * Cloud Foundry 应用程序可以访问高达 256 MB 的免费即时运行时内存。
   * 可以供应 [{{site.data.keyword.Bluemix_notm}}“目录”![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} 中具有轻量套餐的任何服务的一个实例。
   * 超过 10 天没有开发活动，应用程序将进入休眠。您可通过继续在应用程序上工作来唤醒应用程序。
   * 超过 30 天没有开发活动，将删除轻量套餐的服务实例。

### 升级轻量帐户
{: #upgrade-lite-account}

您可以升级到现收现付帐户或预订帐户。有关更多信息，请参阅[如何升级或转换帐户类型？](/docs/account?topic=account-changeacct)。

升级到现收现付帐户后，您将获得 200 美元的促销信用值，该信用值会自动应用于您的帐户。200 美元信用值的有效期为 30 天，而且会自动应用于您的发票。该信用值不能用于第三方产品。

## 现收现付帐户
{: #paygo}

使用现收现付帐户，可以创建多个资源组，以便轻松管理配额并查看一组资源的计费使用情况。将根据您所使用的 {{site.data.keyword.Bluemix_notm}} 计算和服务收费。您有资格获取免费运行时和服务限额。如果使用量超过免费限额，那么您将收到按月开具的 {{site.data.keyword.Bluemix_notm}} 发票。发票将采用美元 (USD) 计费，并提供有关您的资源费用的详细信息。

此外，使用现收现付帐户，您可以订购可选项，例如高级或高端支持选项。有关更多信息，请联系 [{{site.data.keyword.Bluemix_notm}} 销售人员](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部链接图标](../icons/launch-glyph.svg)。


### 升级现收现付帐户
{: #upgrade-to-subscription}

要将现收现付帐户升级到预订帐户，请联系 [{{site.data.keyword.Bluemix_notm}} 销售人员](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")。

## 预订帐户
{: #subscription-account}

使用预订帐户，可以创建多个资源组，以便轻松管理配额并查看一组资源的计费使用情况。每月有最低组合消费，达到该最低消费可享受相应的预订折扣。对于超出预订总额的任何使用量，将按非折扣费率计费。要查看预订，请转至**管理 > 计费和使用情况**，然后选择**预订**。

如果您有预订帐户，那么可以创建 [{{site.data.keyword.Bluemix_notm}} 目录](https://cloud.ibm.com/catalog/){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标") 中提供的大多数服务。但某些服务会使用特定的价格套餐，要求您单独购买。

### {{site.data.keyword.Bluemix_dedicated_notm}} 帐户
使用 {{site.data.keyword.Bluemix_dedicated_notm}} 时，对于以下项，必须至少注册为期一年的使用期限：

   * 连回基础架构的 VPN 连接
   * {{site.data.keyword.BluSoftlayer_notm}} 数据中心内完全冗余的环境
   * 所有受支持的运行时（{{site.data.keyword.runtime_liberty_short}}、{{site.data.keyword.runtime_nodejs_short}} 和内置开放式源代码运行时）
   * 所有您选择的专用服务以及所有公共 {{site.data.keyword.Bluemix_notm}} 服务
   * 标准 {{site.data.keyword.Bluemix_notm}} 支持

您还可订购可选项，例如，{{site.data.keyword.BluDirectLink}} 或者高级或高端支持选项。有关更多信息，请联系 [{{site.data.keyword.Bluemix_notm}} 销售人员](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部链接图标](../icons/launch-glyph.svg)。

在该期限内，您每月所支付的费用取决于所需的专用服务以及预订帐户（通过该帐户，您可以访问所有公共服务）。{{site.data.keyword.Bluemix_notm}} Public 中服务的使用量费用按照您的预订帐户协议进行计算。如果使用了超过该预订协议的服务，那么您会收到相应发票。请联系 IBM 指定的客户代表或联系 [{{site.data.keyword.Bluemix_notm}} 销售人员](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部链接图标](../icons/launch-glyph.svg) 来着手处理您的协议。
