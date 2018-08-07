---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Ocultando um recurso público de usuários em sua conta
{: #exclude}

É possível ocultar um recurso público de todos em sua conta se você é o administrador dela. Inclua o recurso em uma lista de exclusão com a [interface da linha de comandos](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set) do `ibmcloud`.
{:shortdesc: .shortdesc}

**Nota:** ocultar um recurso no catálogo não o remove da CLI do Cloud Foundry ou das listas de fornecimento de serviço disponíveis por meio da navegação global, como Finanças, Dispositivo móvel, Watson e Apps da web.

## Como eu sei se tenho acesso?
{: #find-access}

É possível usar a CLI ou a IU de identidade e acesso para determinar se você tem acesso para permitir que os usuários visualizem um recurso privado que foi incluído na conta. Se você for um proprietário da conta, será possível fornecer acesso a um usuário na sua conta por meio da UI Identity and Access Management atribuindo uma política de acesso. Para obter mais informações, consulte [Gerenciando o acesso à sua conta](access.html).

## Etapa 1: Localizar um recurso
{: #find-resource}

Insira `ibmcloud catálogo de procura <service-id or service-name>` para procurar um recurso. Substitua service-id ou serviço-name por um nome ou ID do recurso. Localize o ID ou nome do serviço que você deseja ocultar nas informações retornadas.

## Etapa 2: Obter os detalhes desse serviço

Insira `ibmcloud catalog service <service-id or service-name>`. Usando o que você localizou no comando anterior, use esse comando para examinar mais detalhes do recurso. Com as informações retornadas, é possível ver a hierarquia, que mostra os recursos-filho dos itens no seu recurso.

## Etapa 3: Ocultar o recurso
{: #vis-exc}

Insira o comando a seguir para evitar que sua conta veja um recurso público.

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

Após a sinalização `excludes`, é possível incluir uma lista separada por vírgula de e-mails ou um ID de conta associado a contas.

Depois de executar o comando, o processo para ocultar o recurso leva 30 minutos. Após 30 minutos, efetue logout e login novamente em sua conta para ver o recurso oculto.

**Nota:** as entradas que forem ocultadas não ficarão disponíveis na IU e na CLI do {{site.data.keyword.Bluemix}}. As entradas ocultas ainda estão visíveis no mercado de trabalho do Cloud Foundry, mas um plano oculto não pode ser provisionado no Cloud Foundry. Os administradores da conta excluída ainda podem ver o recurso.

## Remover uma conta da lista de exclusão
{: #remove-exclude}

Insira o comando a seguir para remover um ID de conta ou um e-mail da lista de exclusão.

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`

## Gerenciando visibilidade de exemplo de objetos-filhos
{: #child}

É possível gerenciar a visibilidade de todos os seus recursos. Cada recurso-filho tem suas características de visibilidade individual.

Neste exemplo, é possível excluir uma conta do serviço Cloudant público.

Se você inserir `ibmcloud catalog service cloudant`, será possível ver os filhos dos recursos.

```
ID cloudant Name cloudantnosqldb Kind service Provider IBM Tags data_management, ibm_created, ibm_dedicated_public, lite Active true Description Cloudant NoSQL DB é uma camada de dados totalmente gerenciada para aplicativos móveis e da web modernos que alavancam um esquema JSON flexível. O Cloudant é criado e compatível com o Apache CouchDB e é acessível por meio de uma API de HTTPS segura, que aumenta conforme seu aplicativo cresce. O Cloudant é certificado para ISO27001 e SOC2 Tipo 1 e todos os dados são armazenados em triplicata em diferentes nós físicos em um cluster de HA/DR em um data center.
Bindable           true
RC Compatible      false
RC Provisionable   false
Children           Name                                          Kind         ID                                               Location
                   lite                                          plan         cloudant-lite
                   |__lite-eu-gb                             deployment   cloudant-lite:eu-gb                          eu-gb
                   |  |__lite-alias-eu-gb                    alias        cloudant-lite:alias:eu-gb                    eu-gb
                   |__lite-us-south                          deployment   cloudant-lite:us-south                       us-south
                      |__lite-alias-us-south                 alias        cloudant-lite:alias:us-south                 us-south
                   standard                                      plan         cloudant-standard
                   |__standard-eu-gb                         deployment   cloudant-standard:eu-gb                      eu-gb
                   |  |__standard-alias-eu-gb                alias        cloudant-standard:alias:eu-gb                eu-gb
                   |__standard-us-south                      deployment   cloudant-standard:us-south                   us-south
                      |__standard-alias-us-south             alias        cloudant-standard:alias:us-south             us-south
```

Localize o ID de um objeto e exclua uma conta com o `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

Para obter mais informações sobre como a visibilidade funciona, veja os [Docs da API](https://console.bluemix.net/apidocs/globalcatalog).
