---

copyright:

  years: 2015, 2018

lastupdated: "2018-11-28"

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


# 有关访问 {{site.data.keyword.Bluemix_notm}} 的故障诊断
{: #accessing}

访问 {{site.data.keyword.Bluemix}} 时的一般问题可能包括登录到 {{site.data.keyword.Bluemix_notm}} 有问题或帐户处于暂挂状态。在许多情况下，只需执行几个简单的步骤即可解决这些问题。
{:shortdesc}


## 为什么我的密码不正确？
{: #ts_logintobm}
{: troubleshoot}

您必须具有与 IBM 标识或 SoftLayer 标识关联的有效密码才能登录到 {{site.data.keyword.Bluemix_notm}} 控制台。

尝试登录到 {{site.data.keyword.Bluemix_notm}} 时，显示了以下错误消息：
{: tsSymptoms}

`输入的密码不正确。`

用于登录到 {{site.data.keyword.Bluemix_notm}} 的密码无效。
{: tsCauses}

使用以下其中一个选项：
{: tsResolve}
 * 转至[我的 IBM 个人档案页面 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://myibm.ibm.com/dashboard/){: new_window} 以确认您使用的密码是否有效。
 * 如果忘记密码，请单击**忘记密码**以重置密码。 
 * 如果忘记 IBM 标识或密码问题仍未解决，请联系全球 IBM 注册帮助台来获取帮助。

如果您登录到 {{site.data.keyword.Bluemix_notm}}，但由于任何原因（例如，重置密码）而导致登录过程中断，请返回到控制台并重新启动登录过程。
{: tip}


## 为什么无法识别我的 IBM 标识或电子邮件？
{: #ts_old_username}
{: troubleshoot}

要成功登录到电子邮件，您必须确保每个帐户都使用 IBM 标识认证。

登录到 {{site.data.keyword.Bluemix_notm}} 控制台时，显示了以下消息：
{: tsSymptoms}

`无法识别此 IBM 标识或电子邮件。`

您尝试登录到控制台，但未使用有效的 IBM 标识。例如，未输入 IBM 标识的标准电子邮件地址，或者尝试使用的是先前的用户名和密码。
{: tsCauses}

您必须具有有效的 IBM 标识和密码才能登录到 {{site.data.keyword.Bluemix_notm}}。

 * 输入 IBM 标识的标准电子邮件地址。
 {: tsResolve}
 * 如果您是使用 SoftLayer 标识的 SoftLayer 用户，那么必须在您有权访问的每个帐户中切换到 IBM 标识认证，然后才能登录。有关更多信息，请参阅[切换到 IBM 标识](/docs/account/softlayerlink.html)。


## 为什么我的 IBM 标识未与任何 {{site.data.keyword.Bluemix_notm}} 帐户关联？
{: #ts_unabletologin}
{: troubleshoot}

登录到 {{site.data.keyword.Bluemix_notm}} 时，显示了以下消息：
{: tsSymptoms}

`由于认证成功，您已位于此页面中，但是此 IBM 标识未与任何 {{site.data.keyword.Bluemix_notm}} 帐户关联。`

您已使用有效的 IBM 标识通过 [{{site.data.keyword.Bluemix_notm}} 控制台](https://{DomainName}){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标") 登录，但还没有创建 {{site.data.keyword.Bluemix_notm}} 帐户。
{: tsCauses}

要创建 {{site.data.keyword.Bluemix_notm}} 帐户，请执行注册过程。
{: tsResolve}


## 我使用自己的 IBM 标识登录时，为什么控制台不打开？
{: #ts_login_stalls}
{: troubleshoot}

您获得了登录成功消息，但未返回到控制台。

使用 IBM 标识登录时，显示了登录成功消息，但未返回到 [{{site.data.keyword.Bluemix_notm}} 控制台 ](https://{DomainName}){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")。
{: tsSymptoms}

使用以下其中一个选项：
{: tsResolve}
 * 关闭浏览器，清除高速缓存和 cookie，然后重试登录。
 * 通过 [{{site.data.keyword.Bluemix_notm}} 控制台 ](https://{DomainName}){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标") 登录。


## 为什么我的 IBM 标识登录无法完成？
{: #ts_login_ibmid}
{: troubleshoot}

如果您登录到 {{site.data.keyword.Bluemix_notm}}，但 IBM 标识认证无法完成，说明服务可能存在问题。 

登录到 {{site.data.keyword.Bluemix_notm}} 时，使用 IBM 标识认证未完成。
{: tsSymptoms}

IBM 标识认证服务可能发生问题。
{: tsCauses}

确保您可以登录到 [IBM](https://idaas.iam.ibm.com/idaas/mtfim/sps/authsvc?PolicyId=urn:ibm:security:authentication:asf:basicldapuser){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")。如果可以登录，说明这是应用程序问题，您可以稍后重试登录到控制台。如果无法登录到该页面，请联系 [IBM 标识帮助台 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}。
  
{: tsResolve}


## 为什么无法在注册帐户后立即登录？
{: #ts_accntpding}
{: troubleshoot}

如果帐户暂挂，那么无法登录到 {{site.data.keyword.Bluemix_notm}}。

在注册 {{site.data.keyword.Bluemix_notm}} 轻量帐户后，可能无法登录到 {{site.data.keyword.Bluemix_notm}}。将显示以下消息：
{: tsSymptoms}

<code>帐户暂挂。请等待最多 24 小时以获取电子邮件确认并请检查垃圾邮件文件夹。如果仍未收到确认电子邮件，请联系 <a href="http://ibm.biz/bluemixsupport.com" target="_blank">{{site.data.keyword.Bluemix_notm}} 支持</a>。</code>

在注册 {{site.data.keyword.Bluemix_notm}} 轻量帐户后，您将收到包含链接的电子邮件，您必须单击该链接以确认注册。  
{: tsCauses}

确认电子邮件将发送到与您的 IBM 标识关联的电子邮件地址。检查收件箱和垃圾邮件文件夹。如果未收到确认电子邮件，请联系 [{{site.data.keyword.Bluemix_notm}} 支持人员](/docs/get-support/howtogetsupport.html)。  
{: tsResolve}


## 为什么会遇到无法装入的控制台页面？
{: #ts_err}
{: troubleshoot}

在使用 {{site.data.keyword.Bluemix_notm}} 控制台时，您可能无法装入控制台页面。相反，您可能会看到错误消息 BXNUI0001E 或 BXNUI0016E。

您可能会看到以下其中一条错误消息：
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
  * 如果安装了 Cloud Foundry 命令行界面，请输入 `ibmcloud cf apps` 命令以查看应用程序是否正在运行。
