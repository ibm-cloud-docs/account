---



copyright:

  years: 2016, 2018
lastupdated: "2017-10-13"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} 标准帐户受限发行版
{: #betaintro}

{{site.data.keyword.Bluemix}} 标准帐户受限发行版引入了新的免费帐户，通过该帐户，可在公共 {{site.data.keyword.Bluemix_notm}} 中以全新的方式工作。与 30 天 {{site.data.keyword.Bluemix_notm}} 试用帐户不同，标准帐户永不过期。您可以持续使用 {{site.data.keyword.Bluemix_notm}} 应用程序，而无需考虑任何时间限制。
{:shortdesc}

英国和美国南部区域中的用户有资格使用标准帐户。如果您不在这两个区域中，也仍然可以通过要求朋友邀请您，或者通过 CloudDigitalSales@us.ibm.com 与我们的销售团队取得联系来创建标准帐户。作为标准帐户所有者，您可以邀请朋友和同事参与。  

## {{site.data.keyword.Bluemix_notm}} 标准帐户简介
{: #standardaccount}

您可能想知道标准帐户与试用帐户相比有何不同。以下各表汇总了有关 {{site.data.keyword.Bluemix_notm}} 标准帐户的重要详细信息。 

|标准帐户中的新增功能？|    
|-----------------|
|帐户永不过期。|
|Cloud Foundry 应用程序可以访问高达 256 MB 的可用即时运行时内存。|
|可以访问免费轻量套餐以使用 Conversation、Internet of Things Platform、Cloudant NoSQLDB 等按需供应的 Watson 服务。有关更多信息，请参阅[可用功能](/docs/pricing/standard_account.html#whatsavailable)。|
|如果超过 10 天没有任何开发活动，那么您的应用程序将休眠。|
|您的服务实例将在处于不活动状态 30 天后删除。|
{:caption="表 1. 标准帐户中的新增功能" caption-side="top"}

|转换试用帐户时哪些内容不会更改？| 
|-----------------|
|帐户是免费的 -- 不需要信用卡。|
|可以继续使用您的轻量套餐实例。|
|您的组织、空间和相关联团队成员权限设置仍保持相同。一个组织可转移到您的新帐户。|
|{{site.data.keyword.Bluemix_notm}} 支持的级别仍相同。|
{:caption="表 2. 未更改的内容" caption-side="top"}

**注**：如果未转换试用帐户，那么您将看到一条说明原因的消息。您可能在现有试用帐户中有多个组织，或者有无法转移的应用程序。您可以采取适当的操作，然后重新尝试转换帐户。


当您拥有标准帐户时，您可以邀请团队成员在您的组织和空间中进行协作、查看您的使用情况、创建空间、更新您的帐户概要文件以及管理您的组织。

## 轻量套餐
{: #liteplans}
   
轻量套餐（也在现买现付帐户中提供）构造为免费配额。您可以高枕无忧地处理您的项目，而不会有生成意外帐单的风险。配额可能会运作一段特定时间，例如，一个月或一次性使用。以下是轻量套餐配额的一些示例：

<ul>
<li>最大数目的已注册设备。</li>
<li>最大数目的应用程序绑定。</li>
<li>加密数据存储限制，例如 1 GB。</li>
<li>供应的吞吐量。</li>
</ul> 

在标准帐户中，您可以使用 {{site.data.keyword.Bluemix_notm}}“目录”中具有轻量套餐的任何内容。轻量套餐很容易找到。缺省情况下，当您访问“目录”时，即会通过轻量标记 ![轻量标记](../icons/Lite.svg) 显示并识别具有轻量套餐的所有服务。选择某个服务以查看相关联轻量套餐的配额详细信息。

## 标准帐户中提供的功能？
{: #whatsavailable}

使用标准帐户，Cloud Foundry 应用程序可以访问最多 256 MB 的即时运行时内存。如果超过分配的配额，您可以停止一些应用程序，以释放运行时内存。您还可以使用具有 2 个 CPU 和 4 GB RAM 的 Kubernetes 集群。 

您可以使用 {{site.data.keyword.Bluemix_notm}}“目录”中任一轻量套餐服务。不过，每个轻量套餐只能供应 1 个实例。在标准帐户受限发行版中，以下服务提供轻量套餐：

<ul>
<li>{{site.data.keyword.prf_hublong}}</li>
<li>{{site.data.keyword.mobilepushfull}}</li>
<li>{{site.data.keyword.cloudantfull}}</li>
<li>{{site.data.keyword.conversationfull}}</li>
<li>{{site.data.keyword.iot_full}}</li>
<li>{{site.data.keyword.languagetranslatorfull}}</li>
<li>{{site.data.keyword.personalityinsightsfull}}</li>
<li>{{site.data.keyword.toneanalyzerfull}}</li>
</ul>

有些服务并非在所有 {{site.data.keyword.Bluemix_notm}} 区域中都可用。有关更多信息，请参阅[按区域列出的服务](/docs/services/services_region.html#services_region)。

我们将随时对此服务列表进行补充，敬请关注！

### 配额限制

当达到配额限制时，将停止您的应用程序或禁用您的服务。如果轻量套餐指定按月提供配额，那么将在每月 1 号重置资源使用情况，这时您可以恢复使用服务。当您将要达到或已达到配额限制时，会收到通知电子邮件。 

您可以针对每个轻量套餐供应 1 个实例。 

**注**：这些限制仅适用于标准帐户。您可以随时升级到现买现付或预订帐户。您仅需要为超出免费限额的使用部分付费。有关现买现付帐户和预订帐户的更多信息，请参阅[帐户类型](/docs/accounts/account-types.html)。

## 效率功能
{: #devactivity}

为了帮助您管理资源，我们纳入了基于开发活动和使用情况的效率功能。

### 应用程序自动休眠

如果应用程序的开发处于不活动状态的时间超过 10 天，该应用程序将进入休眠。当您想要使用新应用程序时，这非常有用，因为您将发现自己不会达到 256 MB 的内存配额限制。 

要唤醒应用程序，可在 Cloud Foundry 命令行或 {{site.data.keyword.Bluemix_notm}} 控制台中重新开始使用它们。 
 
 下面是将唤醒应用程序的所有命令的列表：
  * cf push
  * cf restate
  * cf restart
  * cf ssh
  * cf scale
  * cf stop
  * cf start
  * cf create-route
  * cf map-route
  * cf unmap-route
  * cf delete-route
  * cf enable-ssh
  * cf disable-ssh

有关命令用法详细信息，请参阅 [Cloud Foundry 命令](/docs/cli/reference/cfcommands/index.html)。

 **注**：如果您的应用程序已启用 SSH，那么无法使用 `cf enable-ssh` 和 `cf disable-sh` 命令来唤醒应用程序。 

### 垃圾回收

如果轻量套餐服务处于不活动状态超过 30 天，那么会删除这些服务。这意味着，要创建新的实例时，不必删除不活动的实例。 
 
## 参与标准帐户受限发行版
{: #lgainvitation}

您可以要求已经拥有标准帐户的朋友邀请您，或者通过 CloudDigitalSales@us.ibm.com 与我们的销售团队取得联系。我们期待您的试用！

如果收到朋友或 {{site.data.keyword.Bluemix_notm}} 销售商发来的邀请，那么对您的专属邀请会发送到您提供的电子邮件地址。当您收到邀请时，请完成电子邮件中的指示信息，以注册标准帐户。 
