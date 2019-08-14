---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise, add account, import account, create account

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Incluindo contas em uma empresa
{: #enterprise-add}

É possível construir sua empresa incluindo mais contas {{site.data.keyword.Bluemix}} nela. Para incluir contas, é possível importar contas existentes que não estejam em outra empresa ou é possível criar novas contas dentro de sua empresa.
{:shortdesc}

Depois que sua empresa tiver múltiplas contas, será possível organizar contas relacionadas usando grupos de contas. Para obter mais informações, consulte [Organizando contas em uma empresa](/docs/account?topic=account-enterprise-organize).

## Importando contas existentes
{: #add-accounts}

É possível importar contas existentes em uma empresa. Depois de importar uma conta, ela não poderá ser removida e cada conta poderá ser parte de apenas uma empresa. Se você importar uma conta Lite ou para teste, ela será submetida a um upgrade automático para uma [conta Pré-paga](/docs/account?topic=account-accounts).

A importação de uma conta na empresa tem os impactos a seguir:
* O faturamento da conta passa a ser gerenciado pela empresa. Após a transição, os usuários na conta não poderão acessar as informações de faturamento e pagamento, como faturas, pagamentos ou assinaturas, para períodos de faturamento futuros. Para visualizar ou gerenciar o faturamento, os usuários precisam ser convidados para a conta corporativa e receber acesso ao serviço de Faturamento nessa conta. Consulte [Gerenciar centralmente o faturamento e o uso com as empresas](/docs/billing-usage?topic=billing-usage-enterprise) para obter mais informações.
* Os usuários e as permissões de acesso dentro da conta não são mudados. O acesso dentro da conta é separado da empresa, e os usuários não obtêm acesso automaticamente dentro da empresa quando a conta é importada.
* Os recursos dentro da conta não são mudados. Os usuários com as permissões de acesso corretas podem continuar a visualizar informações de uso de recursos na conta.

Para importar contas existentes em uma empresa, o acesso a seguir é necessário:

   * Dentro da conta a ser importada, deve-se ser o proprietário da conta ou ter a função de Administrador no serviço de Faturamento dentro da conta.
   * Dentro da conta corporativa, a função de Editor ou de Administrador no Serviço corporativo e a função de Administrador no serviço de Faturamento são necessárias.

Para importar uma conta existente, conclua as etapas a seguir:

1. Efetue login em sua conta corporativa e acesse **Gerenciar > Empresa**.
1. Clique em **Contas** para visualizar as contas e os grupos de contas na empresa. Na seção Contas, selecione **Incluir > Importar conta**.
1. Selecione a conta que você deseja importar.

   Se nenhuma conta é exibida, é provável que você não tenha o acesso correto em nenhuma conta existente.
   {: tip}
1. Se você desejar incluir a conta em um grupo de contas, selecione o grupo de contas que será o pai. O pai que você seleciona determina onde a conta existe na hierarquia corporativa.
1. Revise as informações sobre impactos em sua conta e selecione **Eu entendo o impacto em minha conta**. Em seguida, clique em **Importar**.

   Depois que a conta é importada na empresa, ela não pode ser removida. Certifique-se de que deseja mover permanentemente a conta para a empresa.
   {: important}

### Importando contas usando a CLI
{: #add-account-cli}

1. Localize o ID da conta que você deseja importar na empresa.

   ```
   ibmcloud account list
   ```
   {: codeblock}
1. Se você desejar incluir a conta em um grupo de contas, localize os nomes e os IDs de grupos de contas existentes na empresa.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. Importe a conta na empresa especificando o ID da conta para o parâmetro `--account ID`. Se você não especificar um grupo de contas pai, a conta será incluída diretamente sob a empresa.

   ```
   ibmcloud enterprise account-import --account-id ID
   [--parent-account-group ACCOUNT_GROUP_NAME | --parent-account-group-id ACCOUNT_GROUP_ID]
   ```
   {: codeblock}

### Importando contas usando a API
{: #add-account-api}

Para importar uma conta existente na empresa, chame a [API de gerenciamento corporativo](https://{DomainName}/apidocs/enterprise-apis/enterprise#import-an-account-into-an-enterprise){: external} conforme mostrado na solicitação de amostra a seguir. Substitua as variáveis de token e ID do {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) pelos valores de sua empresa.

```
curl -X PUT \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID/import/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" -H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID"
}'
```
{: codeblock}

## Criando novas contas
{: #create-accounts}

É possível criar novas contas em sua empresa. As contas são criadas como contas Pré-pagas, e o uso é faturado para a empresa. Para criar uma conta, é necessário ter uma política de acesso com a função de Editor ou de Administrador no Serviço corporativo.

1. No painel corporativo, clique em **Contas** para visualizar contas e grupos de contas na empresa.
1. Na seção Contas, selecione **Incluir > Criar conta**.
1. Insira um nome para a conta que seja exclusivo dentro da empresa. Como essa é uma de muitas contas, um nome exclusivo e descritivo ajuda você a entender o propósito da conta em uma visão rápida.
1. Se você desejar designar um usuário diferente como o proprietário da conta, insira seu IBMid no campo **Proprietário**. O proprietário da conta tem acesso total para gerenciar a conta.
1. Se você desejar incluir a conta em um grupo de contas, selecione o grupo de contas que será o pai. O pai que você escolhe determina onde a conta existe na hierarquia corporativa.
1. Clique em **Criar**.

Depois de criar a conta, o proprietário da conta poderá efetuar login na conta para convidar outros usuários e gerenciar seu acesso.

### Criando contas usando a CLI
{: #create-accounts-cli}

1. Se você desejar incluir a conta em um grupo de contas, localize os nomes e os IDs de grupos de contas existentes.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. Crie a conta executando o comando a seguir. Se você não especificar um grupo de contas pai, a conta será incluída diretamente sob a empresa. Para fazer com que um usuário diferente seja o proprietário da conta, especifique seu IBMid na opção `--owner`.

   ```
   ibmcloud enterprise account-create NAME
   [--parent-account-group ACCOUNT_GROUP_NAME] [--owner USER_ID]
   ```
   {: codeblock}

### Criando contas usando a API
{: #create-account-api}

Para criar uma nova conta na empresa, chame a API de gerenciamento corporativo conforme mostrado na solicitação de amostra a seguir, substituindo as variáveis de token e de ID do IAM pelos valores de sua empresa. Para obter informações detalhadas sobre a API, consulte [API de gerenciamento corporativo](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-a-new-account-in-an-enterprise){: external}.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/accounts \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID",
  "name": "Sample Account",
  "owner_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}
