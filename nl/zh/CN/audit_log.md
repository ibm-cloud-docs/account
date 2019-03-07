---

copyright:
  years: 2018, 2019
lastupdated: "2019-02-05"

keywords: audit log, user access, account log

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# 使用审计日志监视系统事件
{: #audit-log}

如果您拥有经典基础架构帐户，那么可以通过查看审计日志来监视存储复制事件。审计日志会跟踪每个用户的交互，如登录尝试、端口速度更新、电源重新启动以及由 {{site.data.keyword.BluSoftlayer_notm}} 基础架构支持人员进行的交互。
{:shortdesc}


## 查看审计日志
{: #view-audit-log}

要查看审计日志，请转至**管理 > 帐户**，然后选择**审计日志**。审计日志初始会显示帐户上的用户所做的最后 25 个交互。您可以随时查看多达 200 个交互。展开“每页项数”菜单可查看更多结果。

### 查看用户的访问日志
{: #view-access-logs}

在审计日志页面中，还可以查看由特定用户进行的每次访问尝试的数据。该日志显示每次访问尝试的日期和时间戳记以及 IP 地址。使用以下步骤查看用户的访问日志。

1. 转至**管理 > 帐户**，然后选择**审计日志**。
2. 然后，为用户选择**过滤器**，选择要查看的时间范围，然后选择对象类型。  

每个用户的访问日志都会按日期显示该用户进行的访问尝试，以及用于进行访问尝试的 IP 地址。访问日志中的信息是只读的。
