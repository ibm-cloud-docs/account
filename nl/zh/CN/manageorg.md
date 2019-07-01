---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: update orgs, update spaces, quotas, Cloud Foundry orgs, domains

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# 更新组织和空间
{: #orgupdates}

作为 {{site.data.keyword.Bluemix}} 帐户所有者或组织管理者，您可以在组织级别和空间级别执行管理任务。这些任务包括重命名组织或空间，分配或更新 Cloud Foundry 用户角色，管理域以及查看组织配额详细信息。
{:shortdesc}

转至**管理 > 帐户**，然后选择 **Cloud Foundry 组织**。

一次只能查看一个组织的资源。如果您是多个组织的成员，那么可以通过控制台菜单栏中的用户帐户首选项链接来切换组织。
{: tip}

  * 要重命名组织，请针对要重命名的组织单击“操作”图标 ![“操作”图标](../icons/action-menu-icon.svg)，然后选择**重命名**。
    {: #orgrename}

    您所做的任何更改都将应用于组织中的所有用户。

  * 要删除组织，请联系[支持](/docs/get-support?topic=get-support-getting-customer-support)。
    {: #deleteorgs}

    删除组织时，还会删除该组织内的所有空间和资源。此操作无法撤销。

  * 要删除空间，请选择在其中分配该空间的组织。单击“操作”图标 ![“操作”图标](../icons/action-menu-icon.svg)，然后选择**删除**。

    删除空间时，还会删除所有包含的资源和用户。

  * 要在组织级别编辑用户角色，请单击“操作”图标 ![“操作”图标](../icons/action-menu-icon.svg)，然后选择**用户**。
    {: #listmembers}

    根据要修改用户许可权的方式，选中或清除特定角色对应的复选框。您可以在组织级别分配的角色是“管理者”、“记帐管理者”和“审计员”。有关更多信息，请参阅 [Cloud Foundry 角色](/docs/iam?topic=iam-cfaccess#cfroles)。

  * 要编辑特定空间的用户角色，请单击在其中分配该空间的组织。然后，单击该空间的名称。

    根据要修改用户许可权的方式，选中或清除特定角色对应的复选框。可以在空间级别分配的角色是“管理者”、“开发者”和“审计员”。有关更多信息，请参阅 [Cloud Foundry 角色](/docs/iam?topic=iam-cfaccess#cfroles)。

  * 要管理域，请单击相应组织的“操作”图标 ![“操作”图标](../icons/action-menu-icon.svg)，然后选择**域**。
    {: #managedomains}

    作为帐户所有者或组织管理者，您可以针对组织及其空间内构建的应用程序，查看系统域并添加定制域。如果您是空间管理者，那么此页面将显示分配给空间的域的只读列表。

    如果您添加定制域，那么必须配置 DNS 服务器以将您的定制域解析为指向 {{site.data.keyword.Bluemix_notm}} 系统域。这样，当 {{site.data.keyword.Bluemix_notm}} 接收到定制域的请求时，可以将其正确路由到您的应用程序。系统域始终可供空间使用，另外还可为空间分配定制域。空间中创建的应用程序可使用为该空间列出的任何域。有关创建和使用定制域的更多信息，请参阅[管理域](/docs/apps?topic=creating-apps-update-domain)。

  * 要管理组织的已分配配额，请单击相应组织的“操作”图标 ![“操作”图标](../icons/action-menu-icon.svg)，然后选择**配额**。
    {: #managequota}

    在此，可以查看应用程序数、内存量和服务数等配额详细信息以及套餐详细信息。配额表示创建组织时为其分配的资源限制。组织可用的资源根据您是具有免费帐户还是计费帐户而有所不同。组织内空间中包含的任何应用程序或服务都会使用一定的已分配配额。

    要更改为组织所分配的配额，必须创建支持案例。有关更多信息，请参阅[使用支持案例](/docs/get-support?topic=get-support-open-case)。

    要查看每个位置在空间级别的配额详细信息，请单击相应组织的“操作”图标 ![“操作”图标](../icons/action-menu-icon.svg)，然后选择**配额**。然后，相应地展开每一行。
