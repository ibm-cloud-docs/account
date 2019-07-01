---

copyright:
  years: 2015, 2019
lastupdated: "2019-06-19"

keywords: platform notifications, email notifications, IBM Cloud notifications, notification preferences, email preferences, user notifications, infrastructure notifications

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# 设置电子邮件首选项
{: #email-prefs}

根据您的 {{site.data.keyword.Bluemix}} 帐户类型，您可以选择是接收有关 {{site.data.keyword.Bluemix}} 平台计划外事件和计划内事件的电子邮件通知，还是接收有关计划外事件、维护和声明的基础架构电子邮件通知。您还可以选择为经典基础架构事件设置通知预订。
{: shortdesc}

## 设置平台通知
{: #setting-platform-notifications}

如果您是轻量帐户所有者，那么可以选择是否接收有关 {{site.data.keyword.Bluemix}} 平台计划外事件（如中断）和计划内事件（如维护）的电子邮件通知。设置 {{site.data.keyword.Bluemix_notm}} 平台通知时，您将收到仅与 {{site.data.keyword.Bluemix_notm}} 平台关联的电子邮件通知。您不会收到有关与 {{site.data.keyword.Bluemix_notm}} 服务关联的事件的电子邮件通知。

您只能为个人档案（而非帐户）设置平台电子邮件通知。换言之，如果切换到另一个帐户，那么您所进行的任何平台通知更新的作用域都仅限定为您的个人档案，而不是您切换到的帐户。

选择接收计划外平台事件时，您只会收到有关可能导致中断的问题（严重性 1）的电子邮件。您可以随时在[状态 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/status){: new_window} 页面上查看所有计划内和计划外事件。

1. 转至“头像”图标 ![“头像”图标](../icons/i-avatar-icon.svg) &gt; **个人档案和设置**。
2. 单击**通知**。
3. 选择是否接收要更新的每个类别的平台通知。

  缺省情况下，所有 {{site.data.keyword.Bluemix_notm}} 平台通知均已关闭。
  {: tip}

4. 单击**保存**。

## 设置基础架构通知

如果您是现收现付或预订帐户所有者，那么可以选择是否接收有关计划外事件、维护和公告的 {{site.data.keyword.Bluemix_notm}} 基础架构电子邮件通知。基础架构通知的作用域限定为您切换到的帐户。您可以切换到其他帐户并管理该帐户的通知。

1. 转至“头像”图标 ![“头像”图标](../icons/i-avatar-icon.svg) &gt; **个人档案和设置**。
2. 单击**通知**。
3. 选择是否接收要更新的每个类别的基础架构通知。

  缺省情况下，所有 {{site.data.keyword.Bluemix_notm}} 基础架构通知均已开启。
  {: tip}

4. 单击**保存**。

## 设置用户通知
{: #setting-user-notifications}

设置用户通知仅可用于经典基础架构资源。如果您是帐户所有者，那么可以为帐户中的用户设置通知预订。预订针对的是一组特定开发者服务，如 {{site.data.keyword.autoscaling}} 和 Raid Alert Monitoring。用户预订服务时，会收到有关该服务的电子邮件。  

帐户中的用户会收到以下类型的重要运作事件的通知：

  * 计划外基础架构问题或中断：基于特定客户的特定条件可能导致中断的问题。
  * 计划内服务或安排的维护：使基础架构保持以最佳状态运行所需的维护。
  * 安全漏洞：受影响的区域已隔离。会创建补丁来修复漏洞，并对补丁执行测试以确保不会影响附带功能。
  * 已打开支持案例：提醒用户其帐户有打开的案例。

通知的计时根据事件是计划外、计划内还是安排的事件而有所不同。{{site.data.keyword.BluSoftlayer_notm}} 基础架构策略是尽快补救问题，以消除或尽可能降低出现进一步问题而可能产生更大影响的风险。有时甚至执行计划内维护也只提前很短的时间通知。

要为用户设置预订通知，请完成以下步骤：

  1. 转至**管理 > 帐户**，然后选择**通知**。
  2. 从表中选择服务。
  3. 在“已预订”列中，为要接收通知的用户选择**是**。

    要轻松找到您要查找的用户，请单击**过滤器**，然后按名字、姓氏或用户名进行过滤。
    {: tip}
