---

copyright:

  years: 2017, 2018
lastupdated: "2018-11-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}


# Ocultando um recurso público de usuários
{: #exclude}

Como um administrador para sua conta do {{site.data.keyword.Bluemix}}, é possível ocultar um recurso público de usuários que têm acesso à conta. Você pode ocultar recursos para manter as informações confidenciais ocultas de usuários não autorizados ou algumas informações podem precisar ser acessadas somente por um número finito de pessoas.
{:shortdesc}

Ocultar um recurso no catálogo não o remove da interface da linha de comandos (CLI) do Cloud Foundry ou da lista de categorias de oferta que está disponível na navegação do console do {{site.data.keyword.Bluemix_notm}}, como Finanças, Dispositivo móvel, Watson e Apps da web.
{: note}

É possível usar a [interface da linha de comandos (CLI)](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set) do {{site.data.keyword.Bluemix}} ou o console para determinar se você tem acesso para permitir que os usuários visualizem um recurso privado que foi incluído na conta. Se você for um proprietário da conta, será possível fornecer acesso a um usuário em sua conta por meio do console designando uma política de acesso. Para obter mais informações, consulte [Gerenciando o acesso à sua conta](access.html).

## Localizando um recurso
{: #find-resource}

Execute o comando `ibmcloud catalog search <service-id or service-name>` para procurar um recurso. Substitua as variáveis service-id ou service-name por um nome de recurso ou ID. Use as informações que são retornadas para localizar o ID ou o nome do serviço que você deseja ocultar.

## Obtendo os detalhes do recurso

Execute o comando `ibmcloud catalog service <service-id or service-name>`. Usando as informações que são retornadas da execução do comando anterior, use este comando para examinar mais detalhes sobre o recurso. Com as informações que são retornadas, é possível visualizar a hierarquia, que mostra os recursos-filhos dos itens em seu recurso.

## Ocultando o recurso
{: #vis-exc}

Execute o comando a seguir para evitar que os usuários em sua conta visualizem um recurso público.

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

É possível incluir uma lista separada por vírgula de e-mails ou IDs de conta associados a contas após a sinalização de exclusão.

Depois de executar o comando, o processo para ocultar o recurso leva aproximadamente 30 minutos. Depois de 30 minutos, efetue logout e efetue login novamente em sua conta para ver o recurso oculto.

As entradas que você oculta não estão disponíveis por meio do console ou da CLI. Os administradores da conta excluída ainda podem visualizar o recurso.
{: note}

## Removendo uma conta da lista de exclusão
{: #remove-exclude}

Execute o comando a seguir para remover um ID da conta ou e-mail da lista de exclusão.

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`


## Exemplo: gerenciando a visibilidade de objetos-filhos
{: #child}

É possível gerenciar a visibilidade de todos os seus recursos. Cada recurso-filho tem suas características de visibilidade individual. Este exemplo mostra como é possível excluir uma conta do serviço Cloudant.

Execute o comando `ibmcloud catalog service cloudant` para visualizar todos os filhos do recurso.

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

Localize o ID para um objeto e exclua uma conta executando o comando `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

Para obter mais informações sobre como a visibilidade funciona, veja os [docs da API do catálogo](https://{DomainName}/apidocs/globalcatalog).
