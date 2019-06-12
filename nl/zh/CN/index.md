---

copyright:
  years: 2015, 2019
lastupdated: "2019-06-03"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account, subscription, service bundle

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:row-headers: .row-headers}

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
{: row-headers}
{: class="comparison-table"}
{: caption="表 1. {{site.data.keyword.Bluemix_notm}} 帐户比较" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the feature. The column headers identify the account type. To understand which features apply to the account types, navigate to the row, and find the feature that you're interested in."}

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
   * Cloud Foundry 应用程序每月可以访问高达 256 MB 的免费即时运行时内存。
   * 可以供应 [{{site.data.keyword.Bluemix_notm}}“目录”![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} 中具有轻量套餐的任何服务的一个实例。
   * 超过 10 天没有开发活动，应用程序将进入休眠。您可通过继续在应用程序上工作来唤醒应用程序。
   * 超过 30 天没有开发活动，将删除轻量套餐的服务实例。

## 现收现付帐户
{: #paygo}

使用现收现付帐户，可以访问完整 {{site.data.keyword.Bluemix_notm}}“目录”（包括所有免费套餐），并且可获得双倍的免费运行时内存，即每月 512 MB。您只需为所使用的计费服务付费，而无需长期合同或任何承诺。

您可以创建多个资源组，以轻松管理配额和查看一组资源的计费使用情况。将根据您所使用的 {{site.data.keyword.Bluemix_notm}} 计算和服务收费。如果使用额超出免费运行时和服务限额，您会收到按月开具的发票，其中提供有关资源费用的详细信息。

此外，使用现收现付帐户，还可以订购高级或高端支持套餐，以获取有关生产工作负载的额外帮助。要了解更多信息，请参阅[支持套餐](/docs/get-support?topic=get-support-support-plans)。

## 预订帐户
{: #subscription-account}

使用预订帐户，可以创建多个资源组，以便轻松管理配额以及查看一组资源的计费使用情况。您需要承诺每月最低花费金额，这样才能享受适用于该最低费用的预订折扣。

例如，如果您承诺每月花费 100 美元，为期 6 个月，那么可以获得 10% 的折扣。在预订期内，只需支付 540 美元，即可获得 600 美元的使用额。预订期越长，折扣越大。

您的使用额会从您的预订总额中扣除。即使您的使用额每月都不同，也可以得到一份可预测且一致的帐单。如果您的使用额超出您的预订总额，那么会按照非折扣费率向您收取超额部分的费用。

与现收现付帐户一样，您的预订帐户可以订购高级或高端支持套餐，以便在需要时获得额外帮助。要了解更多信息，请参阅[支持套餐](/docs/get-support?topic=get-support-support-plans)。

如果您有预订帐户，那么可以创建 [{{site.data.keyword.Bluemix_notm}} 目录](https://{DomainName}/catalog){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标") 中提供的大多数服务。但某些服务会使用特定的价格套餐，要求您单独购买。

### 服务捆绑预订
{: #service-subscriptions}

使用服务捆绑预订时，您可以获得特定域中专为常见用例而设计的一组服务的访问权和信用值。您可以从涵盖 AI、分析、{{site.data.keyword.blockchainfull_notm}}、物联网 (IoT) 和云本机服务的服务捆绑中进行选择。如果您需要跨越多个域，那么可以购买多个服务捆绑预订。

您可以将服务捆绑添加到任何类型的现有帐户，包括轻量帐户。在最初 90 天，您只能使用捆绑中的服务。在最初 90 天后，您可以访问完整目录。服务捆绑预订受 [{{site.data.keyword.Bluemix_notm}} 服务描述](/docs/overview/terms-of-use?topic=overview-terms)条款约束。

服务捆绑预订不能通过 {{site.data.keyword.Bluemix_notm}} 控制台进行。要了解更多信息和购买服务捆绑，请联系 [{{site.data.keyword.Bluemix_notm}} 销售人员 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}。
{:tip}

购买服务捆绑预订后，您会收到一封电子邮件，其中包含将捆绑添加到您的帐户时要应用的特征代码。有关如何应用特征代码的更多信息，请参阅[应用特征代码](/docs/account?topic=account-codes)。当您的服务捆绑过期或您使用了所有信用值时，您可以继续使用任何服务，使用额按现收现付费率计算。

## 升级帐户
{: #upgrade-lite-account}

如果需要升级帐户，可以将[轻量帐户升级](/docs/account?topic=account-upgrading-account)为现收现付帐户或预订帐户。升级帐户可以解锁完整 {{site.data.keyword.Bluemix_notm}}“目录”，以及获取额外的免费资源等。

将轻量帐户升级为现收现付帐户后，您将获得 200 美元的促销信用值，该信用值将自动应用于您的帐户。您的 200 美元信用值有效期为 30 天，您的使用额将自动从信用额中扣除。信用值不能与第三方产品一起使用，而且只适用于部分帐户。

如果已有现收现付帐户或预订帐户，还可以将帐户转换为其他类型。有关更多信息，请参阅[升级帐户](/docs/account?topic=account-upgrading-account)。
