---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Mudando a propriedade de recursos privados

É possível mudar a propriedade da conta com a interface da linha de comandos. Depois de ter criado e customizado recursos privados em seu catálogo, é possível transferir a propriedade desses recursos para outra pessoa. Depois de transferir a propriedade, você não será capaz de ver o recurso de sua conta. Não é possível desfazer a mudança da propriedade da conta, então tome cuidado.
{:shortdesc: .shortdesc}

## Como mudar o proprietário de um recurso de catálogo

Para mudar o proprietário de um recurso com a [CLI](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_settings), use o comando a seguir:

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
