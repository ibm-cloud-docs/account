---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 變更專用資源所有權

您可以使用指令行介面來變更帳戶所有權。在型錄中建立及自訂專用資源之後，就可以將這些資源的所有權移轉給其他人。移轉所有權之後，就無法再看到您帳戶中的資源。無法復原帳戶所有權的變更，因此請格外小心。
{:shortdesc: .shortdesc}

## 如何變更型錄資源的擁有者

若要變更資源的擁有者，請在 [CLI](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_settings) 中使用下列指令：

`ibmcloud catalog entry-visibility-set <service-id> --owner<account-id or account-email>`
