---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords: add user, share resource, private resource, share catalog, find resource, set visibility

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Incluindo contas em seu recurso privado
{: #include}

Qualquer recurso privado do {{site.data.keyword.Bluemix}} que você cria é restrito por padrão. Se você for um administrador para a conta, será possível escolher quem pode visualizar seu recurso, incluindo o usuário em uma lista de inclusão. Também é possível transferir a propriedade de um recurso privado.
{:shortdesc}

É possível usar a [interface da linha de comandos (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) do {{site.data.keyword.Bluemix}} ou o console para determinar se você tem acesso para permitir que usuários visualizem um recurso privado que foi incluído na conta. Se você for um proprietário da conta, será possível fornecer acesso a um usuário em sua conta por meio do console designando uma política de acesso. Para obter mais informações, consulte [Gerenciando o acesso à sua conta](/docs/account?topic=account-find-access).

## Localizando seu recurso
{: #find-resource-inc}

Execute o comando `ibmcloud catalog service <service-id or service-name>`. Substitua as variáveis service-id ou service-name por seu nome de recurso ou ID. Use as informações que são retornadas para visualizar a hierarquia, que mostra os recursos-filhos dos itens em seu recurso.

## Configurando a visibilidade incluindo uma conta
{: #vis-inc}

Execute o comando a seguir para permitir que uma conta veja seu recurso privado.

```
ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>
```
{:codeblock}

Após a sinalização includes-add, é possível incluir uma lista separada por vírgula de e-mails ou IDs associados a contas.

Depois de executar o comando, o processo para incluir o recurso leva aproximadamente 30 minutos. Após 30 minutos, efetue logout e login novamente em sua conta para ver o recurso incluído.

## Removendo uma conta da lista de inclusão
{: #remove-include}

Execute o comando a seguir para remover uma conta da lista de inclusões.

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## Exemplo: gerenciando a visibilidade de objetos-filhos
{: #child-vis}

É possível gerenciar a visibilidade de seu recurso ou seus filhos. Uma lista de inclusões vazia significa que somente os administradores de conta podem visualizá-la. Sua conta deve ser incluída na lista de inclusão para todos os membros da conta para visualizá-la.

O exemplo a seguir mostra como é possível executar o comando `ibmcloud catalog service cloudant` para visualizar os filhos de uma instância de serviço do Cloudant.

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

É possível obter o ID do recurso para a implementação filha e, em seguida, incluir uma conta executando o comando a seguir:

```
ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>
```
{:codeblock}

Os filhos de um objeto podem herdar visibilidade de formas complexas. Se o objeto-filho for privado, ele terá sua própria configuração de visibilidade. No entanto, se o objeto-filho for configurado como público, ele herdará a visibilidade de seu pai. Configurar a visibilidade em um objeto-filho privado pode restringir sua visibilidade para mais do que o pai. Para obter mais informações sobre como a visibilidade funciona, veja os [Docs da API do catálogo](https://{DomainName}/apidocs/globalcatalog).

## Transferindo a propriedade de um recurso privado
{: #owners}

Se você deixar seu projeto ou organização, talvez queira transferir a propriedade dos recursos em sua conta para outra pessoa.

Depois de transferir a propriedade, não é mais possível visualizar o recurso por meio de sua conta. Certifique-se de que deseja transferir a propriedade, porque essa ação não pode ser desfeita.
{: important}

É possível usar a [interface da linha de comandos (CLI) do {{site.data.keyword.Bluemix}}](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) para transferir a propriedade de um recurso privado. Execute o seguinte comando:

```
ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>
```
{:codeblock}
