---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-02"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# 有关访问 {{site.data.keyword.Bluemix_notm}} 的故障诊断
{: #accessing}

访问 {{site.data.keyword.Bluemix}} 时的一般问题可能包括登录到 {{site.data.keyword.Bluemix_notm}} 有问题或帐户处于暂挂状态。在许多情况下，只需执行几个简单的步骤即可解决这些问题。
{:shortdesc}

## 密码不正确
{: #ts_logintobm}

您必须具有与 IBM 标识关联的有效密码才能登录到 {{site.data.keyword.Bluemix_notm}} 控制台。

您必须具有与 IBM 标识或链接帐户标识关联的有效密码才能通过 [{{site.data.keyword.slportal}}](https://control.softlayer.com)登录。

尝试登录到 {{site.data.keyword.Bluemix_notm}} 时，显示了以下错误消息：
{: tsSymptoms}

`输入的密码不正确。`

用于登录到 {{site.data.keyword.Bluemix_notm}} 的密码无效。
{: tsCauses}

使用以下其中一种解决方案：
{: tsResolve}
 * 输入正确的密码。要检查 IBM 标识和密码是否有效，可以转至“我的 IBM 个人档案”页面，单击**登录**，并在“登录”页面中输入 IBM 标识和密码。
 * 如果忘记密码，请单击**忘记密码**以重置密码。然后，返回到 [{{site.data.keyword.Bluemix_notm}} 控制台](https://console.{DomainName})或 [{{site.data.keyword.slportal}}](https://control.softlayer.com)并重新登录。
 * 如果忘记 IBM 标识或密码问题仍未解决，请联系全球 IBM 注册帮助台来获取帮助。
 * 要获取有效的 IBM 标识和密码，请转至“我的 IBM 个人档案”页面，然后单击**注册**。

**注：**如果您位于“登录到 IBM”页面上，并且登录过程出于任何原因（例如，重置密码）而中断，请返回到 [{{site.data.keyword.Bluemix_notm}} 控制台](https://console.{DomainName})或 [{{site.data.keyword.slportal}}](https://control.softlayer.com)，然后重新启动登录过程。


## 登录凭证无效
{: #ts_login_invalid_credentials}

使用 IBM 标识登录时，显示了以下消息：
{: tsSymptoms}

`提供的登录凭证无效。如果您有与帐户关联的 IBM 标识，请在此登录`

* 您已切换到 IBM 标识，但却尝试使用先前的用户名和密码通过 [{{site.data.keyword.slportal}}](https://control.softlayer.com)登录。
{: tsCauses}

* 您尝试了通过 [{{site.data.keyword.slportal}}](https://control.softlayer.com)登录，但在“用户名”和“密码”字段中输入的是 IBM 标识和密码。

单击消息中的**在此登录**，或转至“IBM 标识帐户登录”部分并单击**使用 IBM 标识登录**。
{: tsResolve}

不要使用用于先前标识的**用户名**和**密码**字段。


## 无法识别 IBM 标识或电子邮件
{: #ts_old_username}

登录到 {{site.data.keyword.Bluemix_notm}} 控制台时，显示了以下消息：
{: tsSymptoms}

`无法识别此 IBM 标识或电子邮件。`

您尝试了登录到 {{site.data.keyword.Bluemix_notm}} 控制台，但未使用有效的 IBM 标识。例如，未输入 IBM 标识的标准电子邮件地址，或者尝试使用的是先前的用户名和密码。
{: tsCauses}

您必须具有有效的 IBM 标识和密码才能登录到 {{site.data.keyword.Bluemix_notm}}。

 * 确保输入 IBM 标识的标准电子邮件地址。
 {: tsResolve}
 * 如果您是使用 {{site.data.keyword.BluSoftlayer_full}} 标识的 {{site.data.keyword.BluSoftlayer_full}} 用户，那么必须在您有权访问的每个帐户中的 {{site.data.keyword.slportal}}内切换到 IBM 标识认证，然后才能使用 IBM 标识认证进行登录。有关更多信息，请参阅[切换到 IBM 标识](/docs/account/softlayerlink.html)。


## IBM 标识与任何 IBM Cloud 帐户都不关联
{: #ts_login_noswitch}

使用 IBM 标识登录时，显示了以下消息：
{: tsSymptoms}

`由于认证成功，您已位于此页面中，但是此 IBM 标识未与任何 IBM Cloud 帐户关联。如果您认为这是错误，请联系帐户所有者或主用户。`

您已使用有效的 IBM 标识通过 [{{site.data.keyword.slportal}}](https://control.softlayer.com)登录，但未在 {{site.data.keyword.slportal}}中切换到 IBM 标识认证。
{: tsCauses}

根据需要，完成以下检查：
{: tsResolve}
 * 联系主用户或帐户管理员来检查是否支持您切换到 IBM 标识认证。
 * 确保完成“切换到 IBM 标识”步骤。请参阅[切换到 IBM 标识](/docs/account/softlayerlink.html)。
 * 确保执行**将用户标识与 IBM 标识相关联**电子邮件中的操作。检查收件箱和垃圾邮件文件夹中是否有该电子邮件。要再次获取此电子邮件（例如，如果电子邮件已到期），请转至 {{site.data.keyword.slportal}}中的“编辑用户个人档案”页面，然后单击**重新发送电子邮件**。或者，请联系 [{{site.data.keyword.Bluemix_notm}} 支持 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://ibm.biz/bluemixsupport.com){: new_window}。

**注：**如果您是直接使用 IBM 标识创建的 IBM 标识，那么会收到两封需要处理的电子邮件；一封来自 IBM 标识注册，一封来自 {{site.data.keyword.Blu_full}}。确保执行这两封电子邮件中的操作。

根据帐户的设置方式，下面的一些登录选项可能适用：
 * 使用 {{site.data.keyword.BluSoftlayer_full}} 标识的 {{site.data.keyword.BluSoftlayer_notm}} 用户必须通过 [{{site.data.keyword.slportal}}](https://control.softlayer.com)登录。
 * 使用 IBM 标识且具有或不具有链接 {{site.data.keyword.Bluemix_notm}} 帐户的 {{site.data.keyword.BluSoftlayer_notm}} 用户可以通过 [{{site.data.keyword.slportal}}](https://control.softlayer.com)登录来打开 {{site.data.keyword.slportal}}，也可以通过 [{{site.data.keyword.Bluemix_notm}} 控制台](https://console.{DomainName})登录来打开“基础架构”仪表板。


## IBM 标识与任何 {{site.data.keyword.Bluemix_notm}} 帐户都不关联
{: #ts_unabletologin}

登录到 {{site.data.keyword.Bluemix_notm}} 时，显示了以下消息：
{: tsSymptoms}

`由于认证成功，您已位于此页面中，但是此 IBM 标识未与任何 {{site.data.keyword.Bluemix_notm}} 帐户关联。`

您已使用有效的 IBM 标识通过 [{{site.data.keyword.Bluemix_notm}} 控制台](https://console.{DomainName})登录，但还没有创建 {{site.data.keyword.Bluemix_notm}} 帐户。
{: tsCauses}

要创建 {{site.data.keyword.Bluemix_notm}} 帐户，请执行注册过程。
{: tsResolve}

根据帐户的设置方式，下面的一些登录选项可能适用：
 * 没有链接帐户的 {{site.data.keyword.Bluemix_notm}} 用户必须通过 {{site.data.keyword.Bluemix_notm}} 控制台登录。
 * 具有链接帐户的 {{site.data.keyword.Bluemix_notm}} 用户可以通过 [{{site.data.keyword.Bluemix_notm}} 控制台](https://console.{DomainName})或 [{{site.data.keyword.slportal}}](https://control.softlayer.com)登录。


## 控制台未打开
{: #ts_login_stalls}

使用 IBM 标识登录时，显示了登录成功消息，但未返回到 [{{site.data.keyword.Bluemix_notm}} 控制台](https://console.{DomainName})或 [{{site.data.keyword.slportal}}](https://control.softlayer.com)。
{: tsSymptoms}

使用以下其中一种解决方案：
{: tsResolve}
 * 关闭浏览器，清除高速缓存和 cookie，然后重试登录。
 * 确保您是通过 [{{site.data.keyword.Bluemix_notm}} 控制台](https://console.{DomainName})或 [{{site.data.keyword.slportal}}](https://control.softlayer.com)登录的，而不是直接从 IBM 标识认证服务进行登录。


## IBM 标识登录未完成
{: #ts_login_ibmid}

登录到 {{site.data.keyword.Bluemix_notm}} 时，使用 IBM 标识认证未完成。
{: tsSymptoms}

IBM 标识认证服务可能发生问题。
{: tsCauses}

在 [IBM IBMid![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://status.ibm.com/wind){: new_window} 上检查该服务的状态，然后重试。
{: tsResolve}


## 帐户暂挂
{: #ts_accntpding}

如果帐户暂挂，那么无法登录到 {{site.data.keyword.Bluemix_notm}}。

在注册 {{site.data.keyword.Bluemix_notm}} 试用帐户后，可能无法登录到 {{site.data.keyword.Bluemix_notm}}。将显示以下消息：
{: tsSymptoms}

<code>帐户暂挂。请等待最多 24 小时以获取电子邮件确认并请检查垃圾邮件文件夹。如果仍未收到确认电子邮件，请联系 <a href="http://ibm.biz/bluemixsupport.com" target="_blank">{{site.data.keyword.Bluemix_notm}} 支持</a>。</code>

在注册 {{site.data.keyword.Bluemix_notm}} 试用帐户后，您将收到确认电子邮件。必须单击确认电子邮件中的链接以完成注册过程。
{: tsCauses}

确认电子邮件将发送到提供的电子邮件地址。检查收件箱和垃圾邮件文件夹。如果尚未收到确认电子邮件，请联系 [{{site.data.keyword.Bluemix_notm}} 支持 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](http://ibm.biz/bluemixsupport.com){: new_window}。  
{: tsResolve}

## 无法装入 {{site.data.keyword.Bluemix_notm}} 页面
{: #ts_err}

在使用 {{site.data.keyword.Bluemix_notm}} 控制台时，您可能无法装入控制台页面。相反，您可能会看到错误消息 BXNUI0001E 或 BXNUI0016E。

在使用 {{site.data.keyword.Bluemix_notm}} 控制台时，您可能会看到以下其中一条错误消息：
{: tsSymptoms}

`BXNUI0001E: 未装入页面，因为 {{site.data.keyword.Bluemix_notm}} 未检测到是否存在会话。`

`BXNUI0016E: 未检索到应用程序和服务，因为未装入 {{site.data.keyword.Bluemix_notm}} 页面。`

根据需要完成以下一个或多个操作：
{: tsResolve}

  * 刷新或重新启动浏览器。
  * 注销 {{site.data.keyword.Bluemix_notm}}，并重新登录。
  * 使用浏览器的隐私浏览模式。
  * 清除浏览器的 cookie 和高速缓存。
  * 使用其他浏览器。有关 {{site.data.keyword.Bluemix_notm}} 支持的浏览器版本的信息，请参阅 [{{site.data.keyword.Bluemix_notm}} 先决条件](/docs/overview/prereqs.html#prereqs)。
  * 如果安装了 cf 命令行界面，请输入 `cf apps` 命令以查看应用程序是否正在运行。
