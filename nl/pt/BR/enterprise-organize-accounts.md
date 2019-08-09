---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, create account group, organize accounts, move accounts

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Organizando contas em uma empresa
{: #enterprise-organize}

Use os grupos de contas para organizar contas relacionadas em sua empresa {{site.data.keyword.Bluemix}}. É possível criar uma hierarquia corporativa com multicamadas, aninhando grupos de contas dentro de um grupo de contas. Se for necessário, será possível reorganizar movendo as contas entre os grupos de contas.
{:shortdesc}

Por exemplo, o diagrama a seguir descreve uma empresa de quatro camadas que é possível configurar aninhando grupos de contas. Primeiro, você cria dois grupos de contas que têm a empresa como o pai. Em seguida, é possível criar dois grupos de contas adicionais que tenham um desses grupos de contas como um pai. É possível mover as contas livremente dentro dos grupos de contas, não importa em qual camada eles estejam. No entanto, os grupos de contas não podem ser movidos.

![Um diagrama que mostra quatro camadas corporativas. A camada principal é a corporativa, que contém duas camadas de grupos de contas. Em seguida, o grupo de contas contém contas.](images/enterprise-hierarchy.svg "Camadas corporativas são criadas incluindo grupos de contas.")

Lembre-se de que como você organiza a sua empresa impacta como é possível controlar os custos de uso. Para obter mais informações, consulte [Gerenciando centralmente faturamento e uso com empresas](/docs/billing-usage?topic=billing-usage-enterprise).
{: tip}

## Criando grupos de contas
{: #create-account-group}

Para criar um grupo de contas, é necessária a função de Administrador ou de Editor no serviço Corporativo na conta corporativa.

1. No painel corporativo, clique em **Contas** para visualizar as contas e os grupos de contas na empresa.
1. Na seção Grupos de contas, clique em **Criar**.
1. Insira um nome para o grupo de contas que reflita as contas que ele conterá. Consulte [Como posso usar uma empresa?](/docs/account?topic=account-enterprise#enterprise-use-cases) para obter exemplos de como você pode organizar contas.
1. Se você desejar que um usuário corporativo diferente de você mesmo seja o contato principal para o grupo de contas, selecione seu IBMid no menu **Contato**. Se um usuário que você deseja designar como o contato não estiver na empresa, convide-o primeiro para a conta corporativa. Não é possível mudar o contato após a criação do grupo de contas. Consulte [Convidando usuários](/docs/iam?topic=iam-iamuserinv) para obter mais informações.

   O contato é diferente de um proprietário da conta, pois não tem acesso adicional ao grupo de contas ou a suas contas. O usuário que você seleciona como contato age como um ponto focal para quaisquer problemas do grupo de contas. Por exemplo, se um executivo financeiro perceber que os custos de uso do grupo de contas estão inesperadamente altos, ele poderá notificar o contato do grupo de contas.


1. Se você desejar que o grupo de contas esteja em uma parte diferente da hierarquia corporativa, selecione um pai diferente.

  Não é possível excluir ou mover os grupos de contas do local onde foram criados.
  {: note}
1. Clique em **Criar**.

Para criar uma nova camada em sua hierarquia corporativa, crie novos grupos de contas dentro do grupo de contas. É possível mover as contas que já estão na empresa para o grupo de contas ou é possível importar ou criar contas dentro dele. Consulte [Incluindo contas em uma empresa](/docs/account?topic=account-enterprise-add) para obter mais informações sobre como importar e criar contas.

### Criando grupos de contas usando a CLI
{: #create-account-groups-cli}

Crie um grupo de contas executando o comando a seguir. Para aninhar um grupo de contas em outro grupo de contas, especifique o nome do grupo de contas na opção `--parent-account-group`. Se você deseja que um usuário diferente seja o contato para o grupo de contas, especifique seu IBMid na opção `--primary-contact-id`.

```
ibmcloud enterprise account-group-create NAME
[--parent-account-group ACCOUNT_GROUP_NAME] [--primary-contact-id USER_ID]
```
{: codeblock}

### Criando grupos de contas usando a API
{: #create-account-groups-api}

É possível criar programaticamente um grupo de contas na empresa chamando a API de gerenciamento corporativo.

A solicitação de amostra a seguir cria um grupo de contas diretamente sob o nível corporativo. Quando você chamar a API, substitua as variáveis de ID pelos valores de sua empresa. Para aninhar o grupo de contas dentro de outro grupo de contas, especifique o ID do grupo de contas no Cloud Resource Name (CRN) no formato a seguir: `crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID`.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/account-groups \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID",
  "name": "Sample Account Group",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-account-group){: external}.-->

## Movendo contas dentro da empresa
{: #move-accounts}

É possível mover contas em qualquer lugar dentro de sua empresa. Por exemplo, é possível mover uma conta de um grupo de contas inferior para seu grupo de contas pai ou você pode movê-la diretamente sob a empresa. As contas podem ser movidas somente dentro da empresa. Não é possível movê-las para uma empresa diferente ou removê-las da empresa para serem uma conta independente.

Para mover uma conta, você precisa da função de Administrador no serviço de Faturamento na conta corporativa e da função de Editor ou de Administrador na empresa inteira ou em ambos os grupos de contas, o atual e o de destino.

1. No painel corporativo, clique em **Contas**.
1. Na seção Contas, clique no ícone Ações na linha para a conta e selecione **Mover conta**.
1. Selecione o novo pai para a conta e clique em **Salvar**.

### Movendo uma conta usando a CLI
{: #move-accounts-cli}

1. Localize o nome da conta e o ID listando todas as contas em sua empresa.

   ```
   ibmcloud enterprise accounts --recursive
   ```
   {: codeblock}
1. Se você estiver movendo a conta para um grupo de contas, localize o nome do grupo de contas e o ID.

   ```
   ibmcloud enterprise account-groups
   ```
   {: codeblock}
1. Mova a conta especificando o novo pai na opção relacionada.

   Para mover a conta para um grupo de contas, especifique o nome do grupo de contas na opção `--parent-account-group`.

   ```
   ibmcloud enterprise account-move -n NAME --parent-account-group ACCOUNT_GROUP_NAME
   ```
   {: codeblock}

   Para mover a conta diretamente sob a empresa, especifique a opção `--parent-enterprise`.

   ```
   ibmcloud enterprise account-move -n NAME --parent-enterprise
   ```
   {: codeblock}

### Movendo contas usando a API
{: #move-account-api}

É possível mover uma conta ao chamar a API de gerenciamento corporativo conforme mostrado na solicitação de amostra a seguir. Substitua as variáveis de token e ID do IAM pelos valores de sua empresa.

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_1"",
}'
```
{: codeblock}

<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#move-an-account-with-the-enterprise){: external}. -->
