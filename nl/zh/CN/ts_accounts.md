---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-24"
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# 有关管理帐户的故障诊断
{: #managingaccounts}

管理帐户时会发生的一般问题可能包括不同的应用程序具有同一域名，或管理员无法查看所有组织。在许多情况下，只需执行几个简单的步骤即可解决这些问题。
{:shortdesc}


## 为什么无法访问其他 {{site.data.keyword.Bluemix_notm}} 位置？
{: #nosecondreg}
{: troubleshoot}

您无法创建新位置是因为您的帐户类型不允许这样做。

尝试创建新 {{site.data.keyword.Bluemix_notm}} 位置时收到错误消息。
{: tsSymptoms}

这可能是因为您使用的是轻量帐户，该帐户仅支持在一个公共位置中进行开发。
{: tsCauses}

要访问更多位置，请升级到计费帐户。转至**管理 > 计费和使用情况**，然后选择**付款**。
{: tsResolve}


## 为什么无法创建新的组织？
{: #nosecondorg}
{: troubleshoot}

您尝试创建多个组织，但您拥有的是轻量帐户。  

尝试创建新组织时收到错误消息。
{: tsSymptoms}

这可能是因为您使用的是轻量帐户，该帐户仅支持在一个组织中进行开发。
{: tsCauses}

要创建新的组织，请升级到计费帐户。请转至**管理 > 计费和使用情况**，然后选择**升级**。
{: tsResolve}


## 为什么无法创建新的轻量套餐实例？
{: #nosecondlite}
{: troubleshoot}

您尝试创建额外的实例，但您拥有的是轻量帐户。

尝试创建新的轻量套餐实例时，收到以下错误消息：
{: tsSymptoms}

`无法供应新轻量实例`

每个轻量套餐实例只能有一个实例，此限制确保这些套餐始终是免费的。
{: tsCauses}

计费帐户中提供了多个计费服务套餐，您可以从中选择一个计费服务套餐来创建多个服务实例。要从控制台升级到计费帐户，请转至**管理 > 计费和使用情况**，然后选择**升级**。
{: tsResolve}

如果您不想从轻量帐户升级且不再使用现有的轻量服务实例，那么可以从仪表板中删除现有轻量套餐实例，然后创建新实例。


## 我怎么会超过运行时内存限额？
{: #noruntimemem}
{: troubleshoot}

您已超过了帐户允许使用的内存。

您无法部署应用程序，并且有错误说明您已超出组织的内存限制。
{: tsSymptoms}

在轻量帐户中，Cloud Foundry 应用程序最多可以使用 256 MB 的即时运行时内存。在计费帐户中，内存限制为 2 GB。
{: tsCauses}

如果使用的是轻量帐户，那么可以升级到计费帐户，以便获取更多内存。请转至**管理 > 计费和使用情况**，然后选择**升级**。
{: tsResolve}

如果您不想从轻量帐户升级，但拥有一些空闲的应用程序，那么可以删除空闲的应用程序以释放一些运行时内存。


## 为什么我的帐户处于不活动状态？
{: #ts_accnt_inactive}
{: troubleshoot}

如果您的帐户处于不活动状态，那么无法在 {{site.data.keyword.Bluemix_notm}} 中创建应用程序。必须联系支持团队来解决此问题。

尝试在 {{site.data.keyword.Bluemix_notm}} 中创建应用程序时，显示了以下错误消息：
{: tsSymptoms}

`BXNUI0096E: 未创建应用程序。您的帐户处于不活动状态，因为它已被取消或暂挂。`

如果您的 {{site.data.keyword.Bluemix_notm}} 帐户已取消或暂挂，那么其状态会变为不活动。
{: tsCauses}

要重新激活您的帐户，请在[支持中心](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标") 开具用例。请在用例中包含以下信息：
{: tsResolve}

  * 您用于登录到 {{site.data.keyword.Bluemix_notm}} 的 IBM 标识。
  * 要在其中创建应用程序的组织的名称。此信息可帮助支持团队确定在您组织内是否为您分配了正确的角色或成员资格。


## 为什么无法向组织添加用户？
{: #ts_adduser}
{: troubleshoot}

仅当您是帐户所有者或者同时是组织的管理者和成员时，您才能邀请用户加入组织。

在**管理组织**部分中看不到**邀请新用户**链接。
{: tsSymptoms}

只有以下 {{site.data.keyword.Bluemix_notm}} 用户才能邀请用户加入组织：
{: tsCauses}
  * 组织的帐户所有者
  * 组织管理者兼组织成员，而不是组织的合作者

在 {{site.data.keyword.Bluemix_notm}} 中，您可以是组织的成员，也可以是组织的合作者：

<dl><dt>合作者</dt>
<dd>如果您已拥有 {{site.data.keyword.Bluemix_notm}} 帐户，并且有其他人邀请您加入组织，那么您会成为该组织的合作者。</dd>
<dt>成员</dt>
<dd>如果您没有 {{site.data.keyword.Bluemix_notm}} 帐户，但有人邀请您加入组织，然后您通过邀请注册了 {{site.data.keyword.Bluemix_notm}}，那么您会成为该组织的成员。</dd>
</dl>

如果您是组织的合作者，即使被指定为组织管理者，也不能邀请用户加入组织。

所有组织管理者（包括组织的合作者）都可以添加、修改和除去组织中的已有用户。
{: note}

如果无法邀请用户加入您的组织，并需要其他角色来完成此操作，请联系组织管理员来更改您的角色。要识别组织管理员，请完成以下步骤：
{: tsResolve}

  1. 在控制台菜单栏中，单击**管理 > 帐户**，然后选择**公司联系人**。
  2. 转至您的组织，并查看**用户**选项卡上的组织管理员信息。  

如果您由于是合作者（而非成员）而无法邀请用户，那么您必须删除您先前的 {{site.data.keyword.Bluemix_notm}} 帐户，然后受邀以组织成员身份加入该帐户。要删除您先前的帐户并以成员身份加入帐户，请完成以下步骤：

  1. 联系 [{{site.data.keyword.Bluemix_notm}} 支持人员 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window}，以开具一个支持用例，请求删除您的帐户。如果存在与旧帐户相关联的数据并且想要将其保存并移动到新帐户，请在您的电子邮件中包含此信息。
  2. 在您的帐户被删除后，让具有组织管理者角色的用户以组织管理者身份邀请您加入组织。然后，通过邀请注册 {{site.data.keyword.Bluemix_notm}}。


## 为什么没有空间与我的当前组织相关联？
{: #ts_no_space}
{: troubleshoot}

如果没有空间与您的当前组织关联，那么无法创建应用程序。

尝试创建应用程序时，显示了以下错误消息：
{: tsSymptoms}

`BXNUI0097E: 在添加应用程序之前，必须至少有一个空间与您的组织和区域相关联。在“仪表板”上，单击“创建空间”。创建空间后，请重试。`

应用程序必须在组织下的空间内创建。
{: tsCauses}

要创建空间，请使用以下某种方法： 
{: tsResolve}

  * 在控制台菜单栏中，单击**管理 > 帐户**，然后选择**组织**。然后，选择要在其中创建空间的组织，并单击**创建空间**。
  * 在 Cloud Foundry 命令行界面中，输入 `cf create-space <space_name> -o <organization_name>`.


## 为什么某些应用程序共享一个域名？
{: #ts_domain_diff}
{: troubleshoot}

您可能注意到，有多个应用程序在 {{site.data.keyword.Bluemix_notm}} 中共享一个 URL。

当您为空间内的不同应用程序分配相同 URL 路径时，可能会发生此问题。
{: tsCauses}

例如，将 myApp1 应用程序推送到 {{site.data.keyword.Bluemix_notm}}，并将域设置为 `mynewapp.stage1.mybluemix.net`。然后，将另一个应用程序 myApp2 推送到同一空间，并将该应用程序的其中一个 URL 路径设置为 `mynewapp.stage1.mybluemix.net`。现在，该路径映射到两个应用程序。

这是受支持行为，您可以使用这一做法来杜绝应用程序升级时的停机状况。有关更多信息，请参阅[如何确保零停机时间](/docs/overview/zero_downtime.html#zero-downtime)。
{: tsResolve}


## 为什么管理员无法使用控制台来查看所有组织？
{: #ts_ui_org}
{: troubleshoot}

作为管理员，您在使用 {{site.data.keyword.Bluemix_notm}} 控制台时，无法显示要管理的每一个组织。您仅可以显示和管理您所属的那些组织。

作为管理员，您无法通过控制台查看所有组织。
{: tsSymptoms}

这是控制台的限制。
{: tsCauses}

您可以通过 Cloud Foundry 命令行界面，使用命令（如 `cf orgs`、`cf create-org` 和 `cf delete-org`）来管理所有组织。要获取 Cloud Foundry 命令的完整列表，请输入 `cf help`。
{: tsResolve}

## 为什么无法添加信用卡信息？
{: #ts_addcc}
{: troubleshoot}

无法提交信用卡信息以将轻量帐户升级到计费帐户。

“添加信用卡”页面上的**提交**按钮已禁用。
{: tsSymptoms}

在“添加信用卡”页面上未正确填写您的信息时会发生此问题。
{: tsCauses}

请完成以下步骤：
{: tsResolve}

  1. 在“添加信用卡”页面上，填写所有必填字段。 
  2. 选择**我已阅读并同意 IBM 条款和条件**，然后单击**提交**。 
  
