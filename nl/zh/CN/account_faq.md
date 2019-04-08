---

copyright:
  years: 2015, 2019
lastupdated: "2019-03-25"

keywords: account, upgrade, account settings, IBM Cloud account, Lite account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:tip: .tip}

# 常见问题
{: #accountfaqs}

## 如何创建帐户？
{: #create-account}
{: faq}

转至 [{{site.data.keyword.Bluemix}}](https://cloud.ibm.com){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")，然后单击**创建 {{site.data.keyword.Bluemix_notm}} 帐户**以创建永不到期的轻量帐户。请参阅[轻量帐户](/docs/account?topic=account-liteaccount#liteaccount)以获取有关包含的功能的更多详细信息。


## 如何解决在创建帐户时发生的错误？
{: #account-error}
{: faq}

如果您能够登录到 {{site.data.keyword.Bluemix_notm}} 帐户，请转至[支持](https://test.cloud.ibm.com/unifiedsupport/supportcenter)页面，然后选择以下某个选项。

* 如果您拥有高级支持或高端支持，请单击**实时交谈**，与 {{site.data.keyword.Bluemix_notm}} 支持代表进行交谈。
* 通过在_需要更多帮助_部分中单击**创建案例**来创建支持案例。

   提交案例后，您会收到一封电子邮件。请按照指示信息作进一步的沟通。

如果无法登录到 {{site.data.keyword.Bluemix}} 帐户，请[创建帐户请求](https://watson.service-now.com/x_ibmwc_open_case_app.do#!/create){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")。


## 什么是 Cloud Foundry？
{: #cloud-foundry}
{: faq}

Cloud Foundry 是一个开放式源代码的平台即服务 (PaaS) 选项，可通过 {{site.data.keyword.Bluemix_notm}} Public 来访问，用于在云上构建和部署应用程序。Cloud Foundry 组织和空间用于组织特定区域内提供的资源和应用程序。

有关管理组织和空间的更多信息，请参阅[添加组织和空间](/docs/account?topic=account-orgsspacesusers#orgsspacesusers)。此外，如果您有兴趣了解如何在 Cloud Foundry 空间中提供对资源的访问权，请参阅 [Cloud Foundry 访问权](/docs/iam?topic=iam-cfaccess#cfaccess)。


## 我可以将组织移动到另一个帐户中吗？
{: #move-org-diff-account}
{: faq}

目前，您还不能将组织移动到其他帐户中。但是，可以在其他帐户中使用相同凭证来重新创建该组织以模拟此功能。有关更多信息，请参阅[添加组织和空间](https://cloud.ibm.com/docs/account?topic=account-orgsspacesusers#createorg)。


## 我可以使用哪些 Cloud Foundry 区域？
{: #whichregions}
{: faq}

在轻量帐户中，您仅可以在一个区域中工作。在现收现付或预订帐户中，您可以访问所有可用区域。


## 什么是服务的轻量价格套餐？
{: #whatisliteplan}
{: faq}

轻量套餐是基于配额的免费服务套餐。您可以使用服务轻量套餐来构建应用程序，而不会产生任何费用。轻量套餐可能以每月为周期（每月续约）或按一次性使用来提供。每个轻量套餐服务可以有 1 个实例。所有帐户中都提供轻量价格套餐。有关轻量帐户的更多信息，请参阅[帐户类型](/docs/account?topic=account-accounts#accounts)。


## 轻量套餐实例达到每月配额时会发生什么情况？
{: #monthlyquota}
{: faq}

达到轻量套餐实例的任何配额限制都会暂挂该月的服务。配额限制按组织设置，而不是按实例设置的。在同一组织中创建的新实例会反映出先前实例的任何使用情况。配额限制会在每个月的第 1 天重置。

通过转至**管理 > 计费和使用情况**，然后选择**使用情况**来查看使用情况。有关更多信息，请参阅[查看使用情况](/docs/billing-usage?topic=billing-usage-viewingusage)。

如果要停止或删除服务，可以通过资源列表来执行此操作。请在[探索 {{site.data.keyword.Bluemix_notm}} 控制台](/docs/overview?topic=overview-ui)中了解更多信息。


## 我可以创建多少个资源组、组织或空间？
{: #resourcelimit}
{: faq}

如果您拥有计费帐户，那么可以在您的帐户中创建任意数量的资源组、组织或空间。但是，如果您拥有轻量帐户，那么只能创建一个组织和一个资源组。

## 如何升级或转换帐户类型？
{: #changeacct}
{: faq}

* 要从轻量帐户升级到现收现付帐户或预订帐户，请转至[帐户设置](https://{DomainName}/account/settings)。
  * 要升级为现收现付帐户，请单击**添加信用卡**。
  * 要升级为预订帐户，请单击**升级**。
* 要在现收现付帐户类型和预订帐户类型之间进行转换，请联系 [{{site.data.keyword.Bluemix_notm}} 销售人员 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}。

要了解更多信息，请参阅[升级帐户](/docs/account?topic=account-upgrading-account)。

## 如果升级轻量帐户，可以继续使用现有实例吗？
{: #nochange}
{: faq}

可以，可以升级到计费帐户，并继续使用通过轻量帐户创建的实例。

## 如何更新信用卡？
{: #updatepayment}
{: faq}

您可以通过转至控制台中的[付款](https://cloud.ibm.com/billing/payments)，更新与帐户关联的付款方式。在“添加付款方式”下，输入新卡的帐单信息，然后单击**添加信用卡**。

要切换到其他付款方式，请选择**其他付款方式**，然后单击**提交变更请求**。这将为您创建一个用于更改付款方式的支持案例。

## 如何重置密码？
{: #reset-password}
{: faq}

要重置帐户密码，请转至“头像”图标 ![“头像”图标](../icons/i-avatar-icon.svg) > **个人档案和设置**。接着，单击“帐户用户信息”磁贴中的**更改或重置**。

要重置 VPN 密码，请完成以下步骤：

  1. 转至**管理 > 访问权 (IAM)**，然后选择**用户**。
  2. 选择用户。
  3. 在“VPN 子网”部分中，单击“编辑”图标 ![“编辑”图标](../icons/icon_write.svg) 以输入新的 VPN 密码。
  5. 单击**应用**。

## 如何取消帐户？
{: #cancelaccount}
{: faq}

您要取消帐户，我们非常遗憾！在此之前，如果有任何方法我们可以帮助您解决您的帐户问题，请与我们的支持人员联系。

如果您决定取消帐户，请查看您的帐户类型，它决定了您可以如何取消帐户。您可以转至[帐户设置](https://cloud.ibm.com/account/settings)，然后在_帐户类型_下查看您的帐户类型。

* 对于现收现付帐户或预订帐户，取消帐户的最快方法是通过[实时交谈](https://{DomainName}/unifiedsupport/supportcenter)或致电 1-866-325-0045 并选择第三个选项来联系我们。也可以打开一个支持案例。
* 要取消轻量帐户，请转至[帐户设置](https://cloud.ibm.com/account/settings)，然后单击**取消激活帐户**。

## 如何删除帐户？
{: #deleteaccount}
{: faq}

联系 [{{site.data.keyword.Bluemix_notm}} 支持人员 ![外部链接图标](../icons/launch-glyph.svg)](https://{DomainName}/unifiedsupport/supportcenter){: new_window}，以打开一个支持案例，请求删除您的帐户。如果存在与旧帐户相关联的数据并且想要将其移动到新帐户，请在您的电子邮件中包含此信息。


## 为什么我的帐户已停用？
{: #account-deactivated}
{: faq}

帐户可能停用的原因如下：

- 对于试用帐户，可能是因为试用期结束。要重新激活帐户，请登录到帐户，并将其升级为现收现付帐户。
- 授权用户取消了该帐户。
- 帐户已暂挂。对于违反 {{site.data.keyword.Bluemix_notm}} 服务的可接受使用行为的帐户，IBM 将酌情直接禁用这些帐户而不另行通知。如果用户在收到攻击行为的通知后更正了其使用行为，IBM 将酌情复原一些服务。

如果您认为自己的帐户被错误停用，请致电 1-866-325-0045 并选择第三个选项来联系支持人员。

## 如何获得支持？
{: #contactsupport}
{: faq}

在控制台菜单栏中，单击**支持**以转至支持中心。要了解有关支持的更多信息，请参阅 [获取支持](/docs/get-support?topic=get-support-support-plans]。


## 我能注册以进行免费试用吗？
{: #freetrial}
{: faq}

{{site.data.keyword.Bluemix_notm}} 试用帐户适用于经认可的学术机构的教师和学生。要获得使用试用帐户的资格，请转至 [Harness the Power of IBM ![外部链接图标](../icons/launch-glyph.svg)](https://onthehub.com/ibm/){: new_window}，并验证您的机构凭证。


## 链接帐户后，如何登录？
{: #al_login}
{: faq}

链接帐户后，可以使用您的 IBM 标识登录到 {{site.data.keyword.Bluemix}} 控制台。


## 链接帐户后，对我的支持有什么影响？
{: #al_support}
{: faq}

链接帐户之后，向帐户添加 {{site.data.keyword.Bluemix_notm}} 平台时，支持级别保持不变。


## 还有其他方法可获取链接帐户的帮助吗？
{: #al_morehelp}
{: faq}

  1. 有关有用的信息，请参阅 [Follow these Steps to Link your IaaS and PaaS Accounts](https://www.ibm.com/blogs/bluemix/2018/03/follow-steps-link-iaas-paas-accounts/){: new_window} 博客 ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")。
  2. 在 {{site.data.keyword.BluSoftlayer_full}} 客户门户网站中，打开**销售实时交谈**以询问帐户问题。
  3. 从客户门户网站中开具凭单。选择**支持** > **添加凭单**，然后在**主题**字段中，选择**帐户请求**以将帐户问题传递给正确的支持团队。

## 如果有多个帐户，该如何链接帐户？
{: #al_multacct}
{: faq}

如果您有多个 SoftLayer 帐户，那么必须链接具有匹配 {{site.data.keyword.Bluemix_notm}} 平台帐户和附带 IBM 标识的帐户。

如果您没有匹配的 {{site.data.keyword.Bluemix_notm}} 平台帐户，也没有附带的 IBM 标识帐户，那么可以创建新的 SoftLayer 帐户来链接这些帐户。

## 链接帐户有奖励吗？
{: #al_incent}
{: faq}

如果您链接帐户，那么可以使用 200 美元促销信用值来试用 {{site.data.keyword.Bluemix_notm}} 服务。

要了解有关 200 美元促销信用值的更多信息，请参阅[现收现付帐户](/docs/account?topic=account-accounts#paygo)。

## 向 SoftLayer 帐户添加 {{site.data.keyword.Bluemix_notm}} 平台服务意味着什么？
{: #al_owaffslacct}
{: faq}

这意味着您的帐户可以访问所有 {{site.data.keyword.Bluemix_notm}} 平台产品。将 {{site.data.keyword.Bluemix_notm}} 平台产品添加到帐户后，帐户主用户必须向用户授予对该产品的访问权。

有关成为帐户主用户的更多信息，请参阅[使用用户](/docs/iam?topic=iam-iamuserinv#iamuserinv)。

## 链接帐户对 SoftLayer 主帐户标识有怎样的影响？
{: #al_howaffslmastacct}
{: faq}

您依旧可以使用 SoftLayer 帐户的标识来登录到客户门户网站，因为 {{site.data.keyword.Bluemix_notm}} 控制台允许使用 IBM 标识进行访问。

## 如何在多个帐户之间切换？
{: #switch-between-accounts}
{: faq}

如果您有多个帐户，那么可以单击您的帐户名称以选择您有权访问的其他帐户。  

![帐户切换器截屏。](images/account-faq.svg "帐户切换器截屏")

## 我可以切换帐户所有者吗？
{: #switch-account-owners}
{: faq}

您不能切换帐户所有者，但可以更改资源所有者。要了解有关切换所有权的更多信息，请参阅[转移专用资源所有权](/docs/account?topic=account-include#owners)。

## {{site.data.keyword.Bluemix_notm}} 支持批量注册用户吗？
{: #batch-registration}
{:faq}

在对 {{site.data.keyword.Bluemix_notm}} 注册用户时，必须单独注册每个用户。{{site.data.keyword.Bluemix_notm}} 不支持用户批量注册。

转至 [{{site.data.keyword.Bluemix}}](https://cloud.ibm.com){: new_window} ![外部链接图标](../icons/launch-glyph.svg "外部链接图标")，然后单击**创建 {{site.data.keyword.Bluemix_notm}} 帐户**。接着，为每个单独的用户填写帐户注册表单。

## 什么是标记？
{: #know-about-tags}
{: faq}

可以使用标记来组织整个帐户中的资源，然后通过在资源列表中过滤标记来查看这些资源。有关更多信息，请参阅[使用标记](/docs/resources?topic=resources-tag)。

## 谁可以查看帐户中的标记？
{: #tags-visibility-account}
{: faq}

标记在整个帐户中可见。如果您有权查看资源，那么就可以查看所有附加的标记。有关更多信息，请参阅[授予用户标记资源的访问权](/docs/resources?topic=resources-access#access)。

## 添加或除去标记需要哪些许可权？
{: #permissions-add-remove-tags}
{: faq}

您必须至少具有对启用 IAM 的资源的“编辑者”角色，或在资源上的 Cloud Foundry 空间中具有“开发者”角色，才能对该资源添加或除去标记。有关更多信息，请参阅[授予用户标记资源的访问权](/docs/resources?topic=resources-access#access)。

## 可以删除标记吗？
{: # delete-tag}
{: faq}

您必须先从所有资源中除去标记，然后才能删除该标记。如果仍然无法将其删除，说明该标记可能附加到您无权查看的资源。同一标记可能会被同一计费帐户中的其他用户附加到多个资源。用户对帐户上所有资源拥有的可视性各不相同。

## 可以重命名标记吗？
{: #rename-tag}
{: faq}

您无法编辑标记的名称。要重命名标记，请将其除去，然后为资源重新分配新标记。  
