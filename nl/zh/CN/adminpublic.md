---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: create account, IBMid, sign up for account, sign up

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# 注册 {{site.data.keyword.Bluemix_notm}}
{: #signup}

您可以使用现有 IBM 标识或者创建新的 IBM 标识来注册 {{site.data.keyword.Bluemix}} 帐户。如果公司注册为使用联合标识用于单点登录 (SSO)，那么请改为使用联合标识注册。
{:shortdesc}

| 注册标识 |详细信息|    
|-----------------|---------|
|现有 IBM 标识|如果您已经具有 IBM 标识，请使用您用于其他 IBM 产品和服务的现有凭证来注册 {{site.data.keyword.Bluemix_notm}}。|
|新 IBM 标识|如果您还没有 IBM 标识，可以在注册时创建一个。有了 IBM 标识，您就可以使用一个用户名登录所有 IBM 产品和服务，包括 {{site.data.keyword.Bluemix_notm}}。|
|联合标识|如果您的公司已请求从您公司的域向 IBM 注册用户凭证，那么您可以使用已用于您公司的登录名的凭证来注册 {{site.data.keyword.Bluemix_notm}}。注册时必须输入电话号码。|
{:caption="表 1. 用于注册 {{site.data.keyword.Bluemix_notm}} 的标识选项" caption-side="top"}

## 使用新的或现有的 IBM 标识注册
{: #signup-ibmid}

如果您不属于使用联合标识的公司，那么请使用 IBM 标识注册 {{site.data.keyword.Bluemix_notm}}。

1. 转至 [{{site.data.keyword.Bluemix_notm}} 登录页面](https://cloud.ibm.com/){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")，然后单击**创建 {{site.data.keyword.Bluemix_notm}} 帐户**。
1. 输入 IBM 标识电子邮件地址。如果没有现有的 IBM 标识，就会根据您输入的电子邮件创建一个标识。
1. 在其余字段中填充信息，然后单击**创建帐户**。
1. 通过单击发送到您提供的电子邮件地址的确认电子邮件中的链接来确认帐户。

如果在登录新帐户时遇到任何问题，请参阅[有关访问 {{site.data.keyword.Bluemix_notm}} 的故障诊断](/docs/account?topic=account-accessing)以获取帮助。

## 使用联合标识注册
{: #signup-federated}

联合标识是公司域内已向 IBM 注册的标识，因此域和用户凭证可用于访问 IBM Web 应用程序。只有在您的公司已经向 IBM 注册的情况下，才能使用联合标识来注册 {{site.data.keyword.Bluemix_notm}}。通过向 IBM 注册公司域，用户可以使用现有公司用户凭证，登录到 IBM 产品和服务。公司的身份提供者随后会使用 SSO 来处理认证。

IBM 使用安全性断言标记语言 2.0 (SAML 2.0) 来进行此身份联合。SAML 2.0 是用于在安全域之间交换认证数据的标准版本。它是基于 XML 的协议，使用包含断言的安全性令牌在组织“身份提供者”和“IBM 依赖方 (RP)”（也称为“服务提供者”）之间传递信息。

有关为公司注册联合标识的信息，请参阅 [IBMid Enterprise Federation Adoption Guide ![外部链接图标](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window}。当您请求注册联合标识时，需要 IBM 产品负责人（如产品支持者或客户支持者）。

### 使用联合标识登录
{: #login-federated}

当您使用联合标识登录到 {{site.data.keyword.Bluemix_notm}} 控制台时，系统会提示您通过您公司的登录页面进行登录。如果您通过 CLI 登录，那么需要指定其他认证参数。有关更多信息，请参阅[使用联合标识登录](/docs/iam?topic=iam-federated_id)。
