---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, multiple account

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Criando uma empresa
{: #create-enterprise}

Você cria uma empresa {{site.data.keyword.Bluemix}} por meio de uma conta de Assinatura existente. A conta que você usa para criar a empresa está permanentemente incluída na empresa.
{:shortdesc}

## Antes de começar
{: #create-prereqs}

Para criar uma [empresa do {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-enterprise), deve-se ser o proprietário da conta ou ter a função de Administrador no Serviço de gerenciamento de conta de cobrança em uma conta de Assinatura.

A conta de Assinatura que você usa para criar a empresa é movida permanentemente para a empresa. Mover a conta para a empresa tem os impactos a seguir:
* O faturamento da conta passa a ser [gerenciado pela empresa](/docs/billing-usage?topic=billing-usage-enterprise). Após a transição, os usuários na conta não poderão acessar as informações de faturamento e pagamento, como faturas, pagamentos ou assinaturas, para períodos de faturamento futuros. Para visualizar ou gerenciar o faturamento, os usuários precisam ser convidados para a conta corporativa e receber acesso ao serviço de Faturamento nessa conta.
* Os usuários e as permissões de acesso dentro da conta não são mudados. O acesso dentro da conta é separado da empresa, e os usuários não obtêm acesso automaticamente dentro da empresa quando a conta é incluída. No entanto, conforme mencionado anteriormente, as informações de faturamento não estão mais disponíveis dentro da conta, independentemente das permissões de acesso.
* Os recursos dentro da conta não são mudados. Os usuários com as permissões de acesso corretas podem continuar a visualizar informações de uso de recursos na conta.

Se você não tiver uma conta de Assinatura, será possível fazer upgrade de sua conta conforme descrito em [Fazendo upgrade de sua conta](/docs/account?topic=account-upgrading-account).

## Criando uma empresa no console
{: #create-console}

1. Acesse **Gerenciar > Empresa** e clique em **Criar**.
1. Insira um nome exclusivo para identificar sua empresa. Geralmente, o nome reflete sua empresa ou organização, como a `My organization's enterprise`. É possível editar o nome corporativo mais tarde, se necessário.
1. Se a sua empresa ou organização tiver um nome de domínio associado, insira-o no campo **Domínio**. É possível especificar qualquer formato de domínio ou subdomínio, como `example.com` ou `my.example.com`.
1. Revise as informações sobre o impacto em sua conta e selecione **Eu entendo o impacto em minha conta**. Em seguida, clique em **Criar**.

   Depois que a conta for incluída na empresa, ela não poderá ser removida. Certifique-se de que deseja mover permanentemente a conta para uma empresa.
   {: important}

Após alguns instantes, sua empresa será criada e será possível visualizar o painel corporativo. Seu IBMid é listado como o contato. O contato serve como um ponto focal para quaisquer interesses corporativos, como perguntas de faturamento ou uso. Você também será designado como o proprietário da conta corporativa, portanto, poderá convidar usuários adicionais para gerenciar a empresa.

Clique em **Contas** para visualizar a hierarquia corporativa, que contém duas contas.

* A conta corporativa, que é aquela em que você convida usuários e concede acesso para gerenciar a empresa.
* A conta que você usou para criar a empresa. Seus usuários e recursos permanecem os mesmos, mas o faturamento agora é gerenciado pela empresa.

## Criando uma empresa usando a CLI
{: #create-cli}

1. Efetue login e selecione a conta.

   ```
   ibmcloud login
   ```
   {:codeblock}
1. Crie a empresa ao executar o comando a seguir, em que `NAME` é um nome exclusivo para identificar a empresa.

   ```
   ibmcloud enterprise create NAME [-d, --domain DOMAIN_NAME] [--primary-contact-id PRIMARY_CONTACT_USER_ID]
   ```
   {:codeblock}

   Por exemplo, o comando a seguir cria uma empresa que é denominada `Example Corp Enterprise` com o domínio `examplecorp.com`.

   ```
   ibmcloud enterprise create "Example Corp Enterprise" -d examplecorp.com
   ```
   {:codeblock}

   Por padrão, a empresa é criada com o usuário com login efetuado atualmente nas funções a seguir:
      * O contato para a empresa, que identifica um ponto focal para notificar com interesses relacionados à empresa
      * O proprietário da conta corporativa, que tem acesso total para gerenciar a conta corporativa

   É possível especificar o IBMid para um usuário diferente na opção `--primary-contact-id`. O mesmo usuário é designado a ambas as funções.
1. Revise o impacto em sua conta e confirme se você deseja continuar inserindo `y`.
   ```
   A conta abcde12345fghij67890 será incorporada na empresa Minha nova empresa (o que não pode ser desfeito). Deseja continuar? [y/N]> y
   ```

Depois que a empresa é criada, dois novos IDs são exibidos. O primeiro ID está associado à empresa, e o segundo ID identifica a conta corporativa, que você usa para gerenciar a empresa.

```
ID:                      09876jihgf54321edcba   
Enterprise Account ID:   edcba12345jihgf67890
```

A conta que você usou para criar a empresa é agora uma parte da empresa. Execute o comando [`ibmcloud enterprise accounts`](/docs/cli?topic=cloud-cli-ibmcloud_enterprise#ibmcloud_enterprise_accounts) para visualizar as duas contas em sua empresa: a conta corporativa e a conta que você usou para criar a empresa.

## Criando uma empresa usando a API
{: #create-api}

É possível criar programaticamente uma empresa chamando a API de gerenciamento corporativo, conforme mostrado na solicitação de amostra a seguir. Para obter informações detalhadas sobre a API, consulte [API de gerenciamento corporativo](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-enterprise){: external}.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/enterprises \
-H "Authorization: Bearer <Token>" \
-H 'Content-Type: application/json' \
-d '{
  "source_account_id": "a1b2c32a5ea94809a9840f5e23c362d",
  "name": "Sample Enterprise",
  "domain": "example.com",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

## Próximas Etapas
{: #create-next-steps}

Construa sua estrutura corporativa, incluindo mais contas existentes ou criando novas contas dentro de sua empresa. Para obter mais informações, consulte [Incluindo contas em sua empresa](/docs/account?topic=account-enterprise-add).

Também é possível convidar usuários adicionais para a conta corporativa para que eles possam ajudar a gerenciar a empresa. Por exemplo, talvez você queira convidar um executivo financeiro para gerenciar o faturamento, controlar os custos de uso e convidar os líderes de departamento para administrar contas. Consulte [Convidando usuários](/docs/iam?topic=iam-iamuserinv) para obter mais informações sobre como convidar usuários.
