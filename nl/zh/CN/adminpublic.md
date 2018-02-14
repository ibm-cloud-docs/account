---



copyright:

  years: 2015, 2018
lastupdated: "2017-11-07"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# 注册 {{site.data.keyword.Bluemix_notm}}

您可以通过使用现有 IBM 标识、创建新 IBM 标识或使用联合标识来注册 {{site.data.keyword.Bluemix}} 帐户。联合标识是公司域内已向 IBM 注册的标识，因此域和用户凭证可用于访问 IBM Web 应用程序。
{:shortdesc}


仅当您的公司已经和 IBM 合作进行注册时，联合标识才可用于注册 {{site.data.keyword.Bluemix_notm}}。通过向 IBM 注册公司域，用户可以使用现有公司用户凭证，登录到 IBM 产品和服务。公司的身份提供者随后会处理认证。当您使用联合标识登录到 {{site.data.keyword.Bluemix_notm}} 时，系统会提示您通过您公司的登录页面进行登录。有关向 IBM 请求注册公司或组织域的信息，或者有关该过程的更多信息，请参阅 [IBMid Enterprise Federation Adoption Guide ![外部链接图标](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window}。当您请求注册联合标识时，需要 IBM 产品负责人（如产品支持者或客户支持者）。

IBM 利用安全性断言标记语言 2.0 (SAML 2.0) 来进行此身份联合。SAML 2.0 是用于在安全域之间交换认证数据的标准版本。它是基于 XML 的协议，使用包含断言的安全性令牌在组织“身份提供者”和“IBM 依赖方 (RP)”（也称为“服务提供者”）之间传递信息。

| 注册方法| 详细信息|    
|-----------------|---------|
|现有 IBM 标识| 如果您已经具有 IBM 标识，请使用您用于其他 IBM 产品和服务的现有凭证来注册 {{site.data.keyword.Bluemix_notm}}。注册时，您需要输入电话号码。|
|新 IBM 标识| 如果您还没有 IBM 标识，可以选择创建一个。有了 IBM 标识，您就可以使用一个登录用户名登录您所使用的所有 IBM 产品和服务，包括 {{site.data.keyword.Bluemix_notm}}。您需要输入个人信息，包括姓和名、电话号码以及新凭证的密码。使用其他 IBM 产品与服务时，您可以使用此 IBM 标识进行登录。|
|联合标识| 如果您的公司已请求从公司域向 IBM 注册用户凭证，那么您可以使用已用于您公司的登录的凭证来注册 {{site.data.keyword.Bluemix_notm}}。注册时，您需要输入电话号码。|
{:caption="表 1. 注册方法" caption-side="top"}
