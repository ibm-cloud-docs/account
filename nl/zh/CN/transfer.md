---

copyright:
  years: 2019
lastupdated: "2019-07-31"

keywords: change owner, transfer account, transfer account ownership, switch owner, transfer owner

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}

# 转移帐户所有权
{: #transfer}

您可以通过更新公司概要文件，将整个 {{site.data.keyword.cloud}} 帐户转移给其他所有者。如果需要转移其他所有者的帐户，请使用公司信息创建支持案例。
{:shortdesc}

只能转移现收现付帐户或预订帐户。

您可以通过使用 `ibmcloud catalog` 命令转移帐户中单个资源的所有权。有关更多信息，请参阅[转移专用资源所有权](/docs/account?topic=account-include#owners)。
{: tip}

## 转移您拥有的帐户
{: #transfer-own}

如果您是帐户所有者并能够登录到帐户，请完成以下步骤来转移帐户所有权。

1. 在控制台中，转至**管理 > 帐户**，然后选择**公司概要文件**。
1. 单击**请求概要文件更新**。
1. 使用新的所有者信息来更新帐户概要文件。
1. 单击**提交更新请求**。

更改经过 {{site.data.keyword.cloud_notm}} 团队复查后才会生效。

## 转移其他所有者的帐户
{: #transfer-lost}

如果帐户的所有者离开了公司，因此需要转移帐户，那么必须选择一个新的所有者，然后提交支持案例以请求转移。 

新的所有者必须是帐户中的用户，并且不能是其他 {{site.data.keyword.cloud_notm}} 帐户的所有者。如果用户不在帐户中，那么其他用户可以将其邀请到帐户中，或者，也可以请求将其添加到您创建的支持案例的帐户中。如果他们已经拥有 {{site.data.keyword.cloud_notm}} 帐户，那么您可以请求将其现在拥有的帐户移动给其他用户或者取消该帐户。

在请求帐户转移的支持案例中，必须附加公司的正式文件，其中包含以下信息。
- 正式的公司抬头
- 公司章程（如果适用）
- 此人不再与公司关联的声明
- 要将帐户所有者更改为新所有者的说明
- 新帐户所有者的姓氏和名字
- 新帐户所有者的电子邮件地址和电话号码
- 公司高管的签名
- 要转移的帐户的帐号

   登录到帐户后，您可以在 {{site.data.keyword.cloud_notm}} 菜单栏中帐户名称旁边找到帐号。例如，您可能会看到“1234567 - IBM”，其中帐号为 1234567。
   {: tip}

   ![控制台菜单栏中帐户选择器的截屏。帐户选择器显示帐户名称和帐号，您可选择当前帐户以显示您可以访问的其他帐户的列表。](images/account-faq.svg "帐户选择器显示帐户名称和帐号，您可选择当前帐户以显示您可以访问的其他帐户的列表。")

要创建支持案例，请转至**支持**，然后单击**创建案例**。提交案例之前，将正式请求文档附加到案例。
