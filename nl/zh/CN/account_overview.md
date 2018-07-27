---

copyright:

  years: 2018
lastupdated: "2018-07-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 帐户层次结构
{: #overview}

{{site.data.keyword.Bluemix}} 帐户包含许多交互组件和系统。下图及对每个组件的说明旨在帮助您了解特定组件是如何相互关联或连接的，以及访问在整个帐户中是如何工作的。 

![{{site.data.keyword.Bluemix_notm}} 帐户图](images/account_diagram.svg "{{site.data.keyword.Bluemix_notm}} 帐户图")

要获得该图的更大视图，请[单击此处](https://console.stage1.bluemix.net/docs/api/content/account/images/account_diagram.svg)。

在该图中，帐户层次结构中的组件有两个主要概念务必要理解。实线和虚线用于帮助说明某些组件包含在其他组件中，例如将用户添加到访问组或 Cloud Foundry 组织。但是，某些组件与其他组件进行交互的目的是为了提供访问权，而不是提供成员资格。例如，授予了用户对资源组的访问权，但这些用户并不会像针对访问组那样，成为资源组的成员。以下各部分还将对这些概念进行说明。

<dl>
<dt>Users</dt>
<dd>邀请用户加入帐户并向其授予对帐户内其他资源的访问权。</dd>
<dt>服务标识</dt>
<dd>服务标识用于标识服务或应用程序，类似于用户标识对用户进行标识的方式。可以使用创建的服务标识来支持 {{site.data.keyword.Bluemix_notm}} 外部的应用程序访问 {{site.data.keyword.Bluemix_notm}} 服务。您可以向服务标识分配特定访问策略，以限制使用特定服务的许可权，甚至可以将访问不同服务的许可权组合在一起。由于服务标识并不与特定用户绑定，因此即使用户离开组织并将其从帐户中删除，该服务标识仍会保留，以确保您的应用程序或服务保持正常运行。有关更多信息，请参阅[创建和使用服务标识](/docs/iam/serviceid.html#serviceids)。</dd>
<dt>服务实例或资源</dt>
<dd>{{site.data.keyword.Bluemix_notm}} 中的服务是基于资源组或基于 Cloud Foundry 的服务。可以添加到资源组并使用 {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) 进行管理的服务实例称为资源。添加到 Cloud Foundry 组织和空间的服务实例通过使用 Cloud Foundry 角色，采用单独的访问管理系统。有关更多信息，请参阅[什么是资源？](/docs/resources/acct_resources.html#resource)</dd>
<dt>API 密钥</dt>
<dd>应用程序编程接口密钥（API 密钥）是传入到应用程序编程接口 (API) 的唯一代码，用于确定调用应用程序或用户。有与用户身份关联的平台 API 密钥，也有可以为服务标识创建的 API 密钥。有关更多信息，请参阅[使用 API 密钥](/docs/iam/apikeys.html#manapikey)。</dd>
<dt>访问组</dt>
<dd>可以创建一个访问组，用于将一组用户和服务标识组织成单个实体，从而轻松分配许可权。您可以将单个策略分配给该组，而不用对每个用户或服务标识多次指定相同的访问权。有关更多信息，请参阅[设置访问组](/docs/iam/groups.html#groups)。</dd>
<dt>资源组</dt>
<dd>资源组是在可定制的分组中组织帐户资源的一种方法，以便您可以一次性快速分配对多个资源的用户访问权。使用 IAM 访问控制来管理的任何帐户资源都属于帐户中的资源组。用户不会添加到资源组，但会为用户提供对资源组内资源的访问权，或者用户可以管理资源组。授予了资源组管理访问权的用户可以在该组内创建新实例，管理其他用户使用该组的访问权，或者根据分配的 IAM 角色编辑组名。有关更多信息，请参阅[管理资源组](/docs/resources/resourcegroups.html#rgs)和[将资源组织成资源组的最佳实践](/docs/resources/bestpractice_rgs.html#bp_resourcegroups)。</dd>
<dt>Cloud Foundry 组织</dt>
<dd>作为帐户所有者或组织管理员，您可以在控制台的“Cloud Foundry 组织”页面中添加组织和空间。通过目录创建支持使用 Cloud Foundry 组织和空间的服务时，会将这些服务添加到组织和空间。组织包含用户、域和配额。在每个组织中，会添加空间，其中包含服务实例。有关更多信息，请参阅[添加组织和空间](/docs/account/orgs_spaces.html#orgsspacesusers)。</dd>
<dt>Cloud Foundry 空间</dt>
<dd>在组织内，您可以使用空间来对一组应用程序、服务和用户进行分组。空间与 {{site.data.keyword.Bluemix_notm}} 中的特定区域联系在一起。您可以基于交付生命周期在组织中创建多个空间。例如，可以创建 dev 空间（作为开发环境）、test 空间（作为测试环境）和 production 空间（作为生产环境）。然后，可以将应用程序与空间相关联。有关更多信息，请参阅[添加组织和空间](/docs/account/orgs_spaces.html#orgsspacesusers)。</dd>
</dl>

该图的另一个重要方面是描述了三种类型的访问管理系统，您可以使用这些系统为帐户用户提供对帐户内资源的访问权。 

* IAM [访问角色](/docs/iam/users_roles.html#iamusermanrol)用于向用户提供对属于一个资源组的所有资源的访问权。这些访问角色还用于为用户提供管理资源组和创建新服务实例以分配给资源组的访问权。
* Cloud Foundry [组织和空间角色](/docs/iam/cfaccess.html#cfroles)用于为用户提供对位于 Cloud Foundry 空间中的任何服务实例的访问权。
* 基础架构[客户门户网站](/docs/customer-portal/cpwhatis.html#customerportal_whatisCP)许可权可用于授予用户对客户门户网站访问以及其中各功能（例如发票、计费、配置 IaaS、监视 IaaS、购买 IaaS 和支持）的细颗粒度[许可权](/docs/iam/infrastructureaccess.html#infrapermission)。设备访问是独立的，通过设备本身进行处理。
