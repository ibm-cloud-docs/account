---

copyright:

  years: 2017, 2018
lastupdated: "2018-01-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 更改专用资源所有权

可以使用命令行界面来更改帐户所有权。在目录中创建并定制了专用资源后，可以将这些资源的所有权转移给其他某个人。转移所有权后，您即无法查看您的帐户中的资源。更改帐户所有权无法撤销，因此请慎用。
{:shortdesc: .shortdesc}

## 如何更改目录资源的所有者

要更改资源的所有者，请通过 [CLI](/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_settings) 使用以下命令：

`bx catalog entry-visibility-set <service-id> --owner<account-id or account-email>`
