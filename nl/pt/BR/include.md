---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Incluindo contas em seu recurso privado
{: #include}

Qualquer recurso privado criado é restrito por padrão. Se você é um administrador da conta, é possível escolher quem pode ver seu recurso incluindo-o em uma lista de inclusão com a [interface da linha de comandos](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set) do {{site.data.keyword.Bluemix}}.
{:shortdesc: .shortdesc}

## Como eu sei se tenho acesso?
{: #find-access}

É possível usar a CLI ou a IU de identidade e acesso para determinar se você tem acesso para permitir que os usuários visualizem um recurso privado que foi incluído na conta. Se você for um proprietário da conta, será possível fornecer acesso a um usuário na sua conta por meio da UI Identity and Access Management atribuindo uma política de acesso. Para obter mais informações, consulte [Gerenciando o acesso à sua conta](access.html).

## Etapa 1: Localizar o recurso
{: #find-resource}

Insira `ibmcloud catalog service <service-id or service-name>`. Substitua service-id ou service-name pelo nome ou ID do recurso. Com as informações retornadas, é possível ver a hierarquia, que mostra os recursos-filho dos itens no seu recurso.

## Etapa 2: Configurar a visibilidade incluindo uma conta
{: #vis-inc}

Insira o comando a seguir para permitir que uma conta veja seu recurso privado.

`ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

Após a sinalização includes-add, é possível incluir uma lista separada por vírgula de e-mails ou IDs associados a contas.

Depois de executar o comando, o processo para incluir o recurso leva 30 minutos. Após 30 minutos, efetue logout e login novamente em sua conta para ver o recurso incluído.

## Remover uma conta da lista de inclusão
{: #remove-exclude}

Insira o comando a seguir para remover uma conta da lista `includes`.

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## Gerenciando a visibilidade de objetos-filhos
{: #child-vis}

É possível gerenciar a visibilidade de seu recurso ou seus filhos.

Uma lista de inclusões vazia significa que somente os administradores de conta podem vê-la. Sua conta deverá estar na lista de inclusão para que todos os membros dela possam vê-la.

Por exemplo, se você inserir `ibmcloud catalog service <your_service>`, será possível ver os filhos do recurso.

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

É possível obter o ID do recurso para a implementação filha e, então, incluir uma conta usando o comando a seguir. `ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`.

Os filhos de um objeto podem herdar visibilidade de formas complexas. Se o objeto-filho for privado, ele terá sua própria configuração de visibilidade. No entanto, se o objeto-filho for configurado como público, ele herdará a visibilidade de seu pai. Configurar a visibilidade em um objeto-filho privado pode fazer com que a visibilidade dele fique ainda mais restrita que a do pai.

Para obter mais informações sobre como a visibilidade funciona, veja os [Docs da API](https://console.bluemix.net/apidocs/globalcatalog).
