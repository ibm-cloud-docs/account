---



copyright:

  years: 2016, 2018
lastupdated: "2018-01-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 切换到 IBM 标识
现在，在 SoftLayer 中进行认证将使用 IBM 标识来提供对所有 {{site.data.keyword.Bluemix}} 的单点登录。支持现有 SoftLayer 帐户切换到 IBM 标识认证。迁移向导将指导您完成此切换。
{:shortdesc}

开始切换到 IBM 标识的过程后，只要尚未完成切换过程，随时都可以将其取消。然而，您每次登录时，都会显示切换到 IBM 标识的提示。计划链接到 {{site.data.keyword.Bluemix_notm}} 帐户的每个 SoftLayer 帐户都必须由具有唯一电子邮件地址的唯一 IBM 标识所拥有。

要从现有 SoftLayer 帐户切换到 IBM 标识，请完成以下步骤：
1. 登录到 SoftLayer 帐户，在显示切换到 IBM 标识的提示时，单击**确定**。

   如果您是主用户并且在 {{site.data.keyword.slportal}} 中未显示切换到 IBM 标识的提示，请联系 [IBM 支持](/docs/get-support/howtogetsupport.html#getting-customer-support)以获取帮助。

   如果您先前已登录并在提示时单击了**稍后**，但在当前会话中又希望切换到 IBM 标识认证，请转至“编辑用户个人档案”页面，然后单击**切换到 IBM 标识**。

2. 遵循向导提示来创建 IBM 标识。

   输入当前任何 IBM 标识均未使用的电子邮件地址。此电子邮件地址将用作新 IBM 标识的用户名，并且在创建该 IBM 标识后会向此电子邮件地址发送注册代码。可以在日后更新与该 IBM 标识关联的电子邮件地址，但不能更改用户名。

3. 收到注册代码后，请单击电子邮件中的链接或将相应 URL 复制到浏览器中，然后输入注册代码。

   注册代码有效期为 7 天，并且只能使用一次。

4. 提交了注册代码后，使用 IBM 标识登录到客户门户网站。

   在“帐户登录”提示中，转至 **IBM 标识帐户登录**部分，并单击**使用 IBM 标识登录**。不要使用先前用于 SoftLayer 标识的**用户名**和**密码**字段。

如果您是新客户，在检查订单时，系统会要求您输入现有 IBM 标识或创建新的 IBM 标识。
  * 要使用现有 IBM 标识，请输入 IBM 标识的用户名或电子邮件地址（如果唯一，即未在多个 IBM 标识之间共享）。

  * 要创建新的 IBM 标识，请输入当前任何 IBM 标识均未使用的电子邮件地址。此电子邮件地址是该 IBM 标识的用户名，并且在创建该 IBM 标识后会向此电子邮件地址发送注册代码。可以在日后更新与该 IBM 标识关联的电子邮件地址，但不能更改用户名。

要解决使用 IBM 标识登录的任何问题，请参阅[有关访问 {{site.data.keyword.Bluemix_notm}} 的故障诊断](/docs/get-support/ts_accessing.html#accessing)。

## 启用用户帐户进行 IBM 标识认证
{: #link_accounts_resellers}

在某些情况下，经销商或分销商必须允许帐户使用 IBM 标识认证后，用户才能切换到 IBM 标识。

  * 必须为要链接到 {{site.data.keyword.Bluemix_notm}} 帐户的每个现有用户帐户启用 IBM 标识认证。然后，每个用户必须使用迁移向导来完成切换到 IBM 标识的过程，如先前部分所述。请联系 [IBM 支持](/docs/get-support/howtogetsupport.html#getting-customer-support)以启用现有 SoftLayer 帐户来使用 IBM 标识认证。

  * 要确保使用 IBM 标识创建新用户帐户，必须在直接主用户帐户上设置 `CREATE_NEW_ACCOUNT_WITH_IBMid_AUTHENTICATION` 属性。请联系 [IBM 支持](/docs/get-support/howtogetsupport.html#getting-customer-support)或供应商为您的帐户设置此属性。  

## 链接 IBM 标识用户帐户
{: #link_user_accounts}

用户帐户切换到 IBM 标识认证后，经销商和分销商可以链接 SoftLayer 和 {{site.data.keyword.Bluemix_notm}} 帐户，以利用组合的基础架构和平台资源。请务必查看以下重要注意事项：

  * 要链接的帐户的主用户必须具有 IBM 标识。
  * 链接到 {{site.data.keyword.Bluemix_notm}} 帐户的每个用户帐户都必须由具有唯一电子邮件地址的唯一 IBM 标识所拥有。尽管一个 IBM 标识可以拥有多个 SoftLayer 帐户，但您仍必须将主用户更改为对于每个帐户都唯一的 IBM 标识。请联系 [IBM SoftLayer 支持 ![外部链接图标](../icons/launch-glyph.svg)](https://knowledgelayer.softlayer.com/topic/support){: new_window}，以更改 SoftLayer 帐户的主用户。
  * 将新用户添加到链接的帐户时，必须将这些用户同时添加到 SoftLayer 帐户和 {{site.data.keyword.Bluemix_notm}} 帐户，这样这些用户才能访问统一控制台的所有功能。

要将每个帐户链接到 {{site.data.keyword.Bluemix_notm}} 帐户，请完成以下步骤：
1. 要链接到现有 {{site.data.keyword.Bluemix_notm}} 帐户或创建新帐户，请以主用户身份登录到客户门户网站，然后单击 {{site.data.keyword.Bluemix_notm}} 链接。

   作为帐户主用户的 IBM 标识必须是要链接到的 {{site.data.keyword.Bluemix_notm}} 帐户的所有者。

2. 请遵循向导提示，包括将 SoftLayer 帐户中的用户添加到 {{site.data.keyword.Bluemix_notm}} 帐户。
3. 链接帐户后，请通知每个帐户的最终用户通过执行先前部分中所述的过程来迁移到 IBM 标识。

仅将最终用户帐户迁移到 IBM 标识。请勿迁移品牌帐户，品牌帐户是最终用户帐户的父帐户，不包含任何资源。迁移到 IBM 标识的 Brand 帐户用户将无法再登录到 Brand Agent Portal (BAP)。
{: tip}  

## 链接帐户中的多因子认证使用情况
{: #2fa}

如果您拥有链接的帐户，那么可以使用身份和访问权**设置**页面为帐户启用多因子认证 (/docs/iam/mfa.html)。这通常也称为双因子验证 (2FA)，它会添加一个安全层，以支持使用除了标准的必需 IBM 标识和密码之外的其他方式访问帐户。帐户的多因子认证会应用于链接的 {{site.data.keyword.Bluemix_notm}} 帐户中的所有资源。帐户支持多因子认证时，多因子认证还会应用于已添加到该帐户的所有用户。请了解为帐户[启用多因子认证](/docs/iam/mfa.html)时要查看的注意事项的更多信息。

多因子认证不是按 IBM 标识进行的。该认证仍是按帐户进行的。当一个 IBM 标识与多个帐户相关联，而您在各帐户之间进行切换时，每次切换到要求双因子认证的不同帐户时都必须确认身份。即使优先帐户和新帐户是使用相同的双因子认证机制配置的，也是如此。

<!-- Above section is for MFA release 1/2018. Commented out section here has old content.
If you enabled two-factor authentication for your existing SoftLayer account, you are still required to enter your security code when logging in to the {{site.data.keyword.Bluemix_notm}} console. However, the two-factor authentication applies only to the resources in your Infrastructure account. You might be able to do various actions to the resources in your {{site.data.keyword.Bluemix_notm}} account without doing two-factor authentication.
Two-factor authentication is not per IBMid. It is still per account. When an IBMid is associated with multiple accounts, and you switch between accounts, you must confirm your identity every time you switch to a different account that requires two-factor authentication. This is true even if the prior account and the new account are both configured with the same two-factor authentication mechanism.
-->

