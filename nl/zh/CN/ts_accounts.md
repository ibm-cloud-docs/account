---

copyright:

  years: 2015, 2018

lastupdated: "2018-09-25"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 有关管理帐户的故障诊断
{: #managingaccounts}

管理帐户会发生的一般问题可能包括不同的应用程序共享同一域名或管理员无法查看所有组织。在许多情况下，只需执行几个简单的步骤即可解决这些问题。
{:shortdesc}

## 无法访问不同的 {{site.data.keyword.Bluemix_notm}} 区域
{: #nosecondreg}

尝试创建新 {{site.data.keyword.Bluemix_notm}} 区域时收到错误消息。
{: tsSymptoms}

这可能是因为您使用的是轻量帐户，该帐户仅支持在一个公共区域中进行开发。您选择在首次设置帐户时要在其中工作的 {{site.data.keyword.Bluemix_notm}} 公共区域。
{: tsCauses}

如果您拥有轻量帐户，那么可以升级到计费帐户以访问其他区域。请转至控制台中的**管理 > 计费和使用情况 > 计费**页面，然后单击**添加信用卡**。在**计费**页面上，还可以检查您是否拥有轻量帐户。
{: tsResolve}

## 无法创建新组织
{: #nosecondorg}

尝试创建新组织时收到错误消息。
{: tsSymptoms}

这可能是因为您使用的是轻量帐户，该帐户仅支持在一个组织中进行开发。您在首次设置帐户时创建组织。
{: tsCauses}

如果您拥有轻量帐户，那么可以升级到计费帐户以访问其他组织。请转至控制台中的**管理 > 计费和使用情况 > 计费**页面，然后单击**添加信用卡**。在**计费**页面上，还可以检查您是否拥有轻量帐户。
{: tsResolve}

## 无法创建轻量套餐实例
{: #nosecondlite}

尝试创建轻量套餐实例时收到以下错误消息：
{: tsSymptoms}

`无法供应新轻量实例`

每个轻量套餐实例只能有一个实例，在此限制下这些套餐是免费的。
{: tsCauses}

通过选择其中一个计费服务套餐（在计费帐户中提供），可以创建服务的其他实例。要从控制台升级到计费帐户，请转至**管理 > 计费和使用情况 > 计费**页面，然后单击**添加信用卡**。
{: tsResolve}

如果您不想从轻量帐户升级且不再使用现有的轻量服务实例，那么可以从仪表板中删除现有轻量套餐实例，然后创建新实例。

## 超过运行时内存限额
{: #noruntimemem}

您无法部署应用程序，且会获取错误，说明您已超出组织的内存限制。
{: tsSymptoms}

在轻量帐户中，Cloud Foundry 应用程序最多可以使用 256 MB 的即时运行时内存。在计费帐户中，存在 2 GB 的内存限制。
{: tsCauses}

如果使用的是轻量帐户，那么可以升级到计费帐户以获取其他内存。请转至控制台中的**管理 > 计费和使用情况 > 计费**页面，然后单击**添加信用卡**。
{: tsResolve}

如果您不想从轻量帐户升级，但拥有一些空闲的应用程序，那么可以删除空闲的应用程序以释放一些运行时内存。

## 帐户不活动
{: #ts_accnt_inactive}

如果您的帐户处于不活动状态，那么无法在 {{site.data.keyword.Bluemix_notm}} 中创建应用程序。必须联系支持团队来解决此问题。

尝试在 {{site.data.keyword.Bluemix_notm}} 中创建应用程序时，您会看到以下错误消息：
{: tsSymptoms}

`BXNUI0096E: 未创建应用程序。您的帐户处于不活动状态，因为它已被取消或暂挂。`

当您的 {{site.data.keyword.Bluemix_notm}} 帐户被取消或暂挂时，其状态会变为不活动。
{: tsCauses}

要重新激活您的帐户，请联系 [{{site.data.keyword.Bluemix_notm}} 支持 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://ibm.biz/bluemixsupport.com){: new_window}。请在电子邮件中包含以下信息：
{: tsResolve}

  * 您用于登录到 {{site.data.keyword.Bluemix_notm}} 的 IBM 标识。
  * 要在其中创建应用程序的组织的名称。此信息可帮助支持团队确定在您组织内是否为您分配了正确的角色或成员资格。

## 无法向组织添加用户
{: #ts_adduser}

您可以邀请多个用户在同一组织下工作。只有帐户所有者或组织管理员才能邀请用户加入组织。

在**管理组织**部分中看不到**邀请新用户**链接。
{: tsSymptoms}

只有以下 {{site.data.keyword.Bluemix_notm}} 用户才能邀请用户加入组织：
{: tsCauses}
  * 组织的帐户所有者
  * 组织的管理员

**注：**所有组织管理员都可以添加、修改和除去组织中的已有用户。

如果无法邀请用户加入您的组织，请联系组织管理员。要识别组织管理员，请完成以下步骤：
{: tsResolve}

  1. 在控制台菜单栏中，单击**管理 > 帐户 > 组织**。
  2. 转至您的组织，并查看**用户**选项卡上的组织管理员信息。  

## 不支持用户批量注册
{: #ts_batchregistration}

在对 {{site.data.keyword.Bluemix_notm}} 注册用户时，必须单独注册每个用户。

{{site.data.keyword.Bluemix_notm}} 不提供同时注册多个用户的功能。
{: tsSymptoms}

{{site.data.keyword.Bluemix_notm}} 不支持用户批量注册。要对 {{site.data.keyword.Bluemix_notm}} 注册用户，必须单独注册每个用户。
{: tsCauses}

要对 {{site.data.keyword.Bluemix_notm}} 注册多个用户，请为每个用户完成以下步骤：
{: tsResolve}

  1. 在 {{site.data.keyword.Bluemix_notm}} 控制台中单击**注册**。
  2. 按照向导的提示完成每个步骤。

## 没有空间与当前组织关联
{: #ts_no_space}

如果没有空间与您的当前组织关联，那么无法创建应用程序。

尝试在 {{site.data.keyword.Bluemix_notm}} 中创建应用程序时，您会看到以下错误消息：
{: tsSymptoms}

`BXNUI0097E: 在添加应用程序之前，必须至少有一个空间与您的组织和区域相关联。在“仪表板”上，单击“创建空间”。创建空间后，请重试。`

{{site.data.keyword.Bluemix_notm}} 中的应用程序必须在组织下的空间内创建。
{: tsCauses}

要创建空间，请使用以下某种方法： 
{: tsResolve}

  * 在控制台菜单栏中，单击**管理 > 帐户 > 组织**。然后，选择要在其中创建空间的组织，并单击**创建空间**。
  * 在 Cloud Foundry 命令行界面中，输入 `cf create-space <space_name> -o <organization_name>`.


## 应用程序共享相同的域名
{: #ts_domain_diff}

您可能注意到数个应用程序在 {{site.data.keyword.Bluemix_notm}} 中共享同一 URL。

当您为空间内的不同应用程序分配相同 URL 路径时，可能会发生此问题。
{: tsCauses}

例如，将 myApp1 应用程序推送到 {{site.data.keyword.Bluemix_notm}}，并将域设置为“mynewapp.stage1.mybluemix.net”。然后，将另一个应用程序 myApp2 推送到同一空间，并将该应用程序的其中一个 URL 路径设置为“mynewapp.stage1.mybluemix.net”。现在，该路径映射到两个应用程序。

此行为受 {{site.data.keyword.Bluemix_notm}} 支持，您可以使用这一做法来杜绝应用程序升级时的停机状况。有关更多信息，请参阅 [Using Blue-Green Deployment to Reduce Downtime and Risk ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://docs.cloudfoundry.org/devguide/deploy-apps/blue-green.html){: new_window}。
{: tsResolve}


## 管理员无法使用 {{site.data.keyword.Bluemix_notm}} 用户界面查看所有组织
{: #ts_ui_org}

作为管理员，使用 {{site.data.keyword.Bluemix_notm}} 用户界面时，无法显示要管理的每一个组织。您仅可以显示和管理您所属的那些组织。

作为管理员，您无法使用 {{site.data.keyword.Bluemix_notm}} 用户界面查看所有组织。
{: tsSymptoms}

这是 {{site.data.keyword.Bluemix_notm}} 用户界面的限制。
{: tsCauses}

您可以通过 Cloud Foundry 命令行界面，使用命令（如 `cf orgs`、`cf create-org` 和 `cf delete-org`）来管理所有组织。要想获取 cf 命令的完整清单，请输入 `cf help`。
{: tsResolve}

## 无法添加信用卡
{: #ts_addcc}

无法提交信用卡信息以将轻量帐户转换为计费帐户。

“添加信用卡”页面上的**提交**按钮已禁用。
{: tsSymptoms}

在“添加信用卡”页面上未正确填写您的信息时会发生此问题。
{: tsCauses}


请完成以下步骤：
{: tsResolve}

  1. 在“添加信用卡”页面上，填写联系人信息、联系人地址和帐单地址部分中的所有必填字段。
  2. 选择**我已阅读并同意 IBM 条款和条件**，然后单击**提交**。此时将显示**选择付款方式**部分。
  3. 输入您的信用卡卡号、到期日期以及安全代码。然后，单击**提交**。
