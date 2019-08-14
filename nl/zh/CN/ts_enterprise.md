---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: troubleshoot enterprise, enterprise problem, account problem, enterprise support, enterprise help, error message

subcollection: account
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

# 有关企业的故障诊断
{: #enterprise_help}

管理企业时，可能会遇到的一般问题包括尝试应用预订或特征代码，或者尝试向企业添加帐户时发生问题。在许多情况下，只需执行几个简单的步骤即可解决这些问题。


## 为什么无法查看整个企业？
{: #troubleshoot-view-enterprise}
{: troubleshoot}

如果您看不到整个企业，那么可能需要检查分配给您的访问权。

您可以查看企业中的若干帐户，但无法查看整个企业层次结构。帐户层次结构仅显示您有权访问的帐户，而不是显示整个企业帐户。
{: tsSymptoms}

您仅分配有对企业中某些帐户的访问权。
{: tsCauses}

要检查分配给您的访问权，请完成以下步骤：
{: tsResolve}

1. 转至**管理** &gt; **访问权 (IAM)** > **用户**。
2. 选择您的姓名。
2. 单击**访问策略**选项卡。

请联系企业所有者以请求正确的访问权。

如果您是企业的所有者，请完成以下步骤，为用户分配对整个企业的访问权：
1. 转至**管理** > **访问权 (IAM)** > **用户**。
2. 选择用户的名称。
2. 单击**访问策略**选项卡 > **分配访问权** > **分配对帐户管理服务的访问权**。
3. 选择**企业**作为服务，然后选择企业的名称。
4. 选择企业中要授权用户访问的帐户组或帐户。例如，如果您希望用户只有权查看单个帐户，请选择该帐户并为用户分配查看者角色或更高的角色。如果希望用户有权查看整个企业，请将帐户组和帐户选择保留空白，然后分配相应访问权。

## 为何无法将现有帐户导入到企业？
{: #troubleshoot-existing-enterprise}
{: troubleshoot}

尝试将现有帐户导入到企业时，发生以下其中一个问题：
{: tsSymptoms}
* 单击“帐户”部分中的**添加现有帐户**时，未列出要添加的帐户。
* 没有选项可用于单击**导入帐户**。

没有为您分配正确的访问权，或者该帐户不是合格的导入帐户。
{: tsCauses}

如果您看不到要导入的现有帐户，说明您需要对现有帐户的计费服务具有管理员角色。
{: tsResolve}

如果**导入帐户**选项不可用，请验证您是否具有企业计费服务的管理员或编辑者角色，以及父企业或帐户组的企业服务的管理员或编辑者角色。

如果您要导入的帐户是“现收现付”帐户，并且您在验证访问权之后仍无法导入，那么可能是因为帐户不合格，无法导入企业。有些“现收现付”帐户无法直接导入企业，比如很多以美元 (USD) 计费的“现收现付”帐户。请与 [{{site.data.keyword.Bluemix_notm}} 销售人员](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![外部链接图标](../icons/launch-glyph.svg) 联系以将帐户转换为预订帐户，然后再将其导入企业。

## 为什么无法在企业中创建新帐户？
{: #troubleshoot-add-enterprise}
{: troubleshoot}

无法在“帐户”部分中单击**添加帐户**。
{: tsSymptoms}

您未分配有正确的访问权。
{: tsCauses}

要在企业中创建帐户，您必须具有以下访问权。
{: tsResolve}
1. 对企业计费服务的管理员角色。
2. 对目标父企业或帐户组的企业服务的管理员或编辑者角色

## 为什么看不到企业预订？
{: #troubleshoot-viewsub-enterprise}
{: troubleshoot}

从子帐户查看“预订”页面时，将显示以下消息：
{: tsSymptoms}

`似乎您无权查看此帐户的预订数据。请联系帐户所有者或管理员以请求相应访问权。`

在企业仪表板的“计费”部分中将显示以下消息：

`似乎您无权查看此信息。请了解有关 IAM 访问权的更多信息。`

对未来结算周期的帐单和付款信息的访问权仅限于企业帐户中的用户。子帐户中的用户无法访问帐单和付款信息，例如预订，即使他们先前在该帐户中具有相应访问权。
{: tsCauses}

要查看或管理计费，您需要受邀加入企业帐户，并在该帐户中获得对计费服务的访问权。请联系企业所有者以请求相应访问权。
{: tsResolve}

## 为何无法将预订代码应用于帐户？  
{: #troubleshoot-promo-enterprise}
{: troubleshoot}

无法将预订代码添加到帐户，因为您没有正确的访问权。  
{: tsSymptoms}

因为您的帐户是企业的子帐户，因此无法应用预订代码。预订代码必须在企业级别应用。
{: tsCauses}

请联系企业的所有者或管理员以添加预订代码。添加预订代码后，该代码将应用于企业中的所有帐户。有关更多信息，请参阅[管理预订](/docs/billing-usage?topic=billing-usage-subscriptions)。
{: tsResolve}
