---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, enterprise users, enterprise access, enterprise tutorial

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Introdução a uma empresa
{: #enterprise-tutorial}

Este tutorial orienta você em como configurar uma empresa por departamento para que seja possível gerenciar e rastrear custos de uso para múltiplas contas do {{site.data.keyword.Bluemix}}. Ao concluir esse tutorial, você aprenderá como criar uma empresa, incluir contas e organizá-las em grupos de contas, convidar usuários e explorar assinaturas.
{:shortdesc}

O tutorial usa uma empresa fictícia chamada *Corporação de exemplo* que deseja criar uma empresa com a estrutura a seguir. Conforme você concluir o tutorial, adapte cada etapa para corresponder às contas de sua organização e à estrutura desejada.

![Uma empresa de quatro camadas que agrupa contas de acordo com o departamento em uma organização. Por exemplo, os grupos de contas são chamados de Marketing, Desenvolvimento e Vendas. Os grupos de contas contêm contas para equipes dentro desses departamentos. Por exemplo, o grupo de contas Vendas contém contas para Direto, On-line e Ativação.](images/enterprise-by-dept.svg "Uma empresa que organiza contas de acordo com o departamento na organização.")

## Antes de começar
{: #setting-prereqs}

Leia [O que é uma empresa?](/docs/account?topic=account-enterprise) para aprender os princípios básicos de como o gerenciamento de conta, o faturamento, os recursos e o gerenciamento de usuário e de acesso funcionam em uma empresa.

Verifique se você tem o acesso necessário em uma Conta de assinatura, que serve como a conta base da qual você cria a empresa. Para criar uma empresa, deve-se ser o proprietário da conta ou ter a função de Administrador no Serviço de gerenciamento de conta de cobrança.

A criação de uma empresa por meio de uma conta e a importação de contas existentes não podem ser desfeitas. Esse tutorial é fornecido como um exemplo das etapas que podem ser seguidas para configurar uma empresa por departamento, mas é necessário planejar cuidadosamente sua estrutura corporativa acerca das necessidades de sua organização.
{:important}

## Etapa 1. Criar a empresa
{: #create_enterprise_tutorial}

As empresas são criadas por meio de uma Conta de assinatura existente. Quando você cria a empresa, a conta é incluída na hierarquia corporativa. O faturamento passa a ser gerenciado pela empresa, mas seus usuários e recursos permanecem os mesmos e são completamente não afetados. Para obter uma descrição completa dos impactos da conta, consulte [Criando uma empresa](/docs/account?topic=account-create-enterprise).

1. Acesse **Gerenciar** > **Empresa** e clique em **Criar**.
2. Insira o nome de sua empresa, como Corporação de exemplo, para identificar sua empresa.
3. Insira o domínio de sua empresa, como `examplecorp.com`.
4. Revise as informações sobre o impacto em sua conta e selecione **Eu entendo o impacto em minha conta**. Em seguida, clique em **Criar**. A conta agora é permanentemente parte da empresa e não pode ser removida.

Depois que sua empresa for criada, você será direcionado para o painel corporativo. Daqui, é possível visualizar os detalhes da empresa, as contas, os usuários e as informações de faturamento. Acesse a página **Contas** para visualizar sua estrutura corporativa, na qual você vê as contas a seguir:
  * Uma conta corporativa com o mesmo nome que sua empresa. Essa conta é usada para gerenciamento corporativo.
  * A conta por meio da qual você criou a empresa. Os usuários podem continuar trabalhando com recursos na conta não afetada.

## Etapa 2. Criar uma estrutura corporativa com grupos de contas
{: #account_groups_tutorial}

Use os grupos de contas para organizar contas relacionadas. A segunda camada e a terceira camada da hierarquia corporativa da Corporação de exemplo contêm os grupos de contas Marketing, Desenvolvimento, Vendas, Design e Engenharia. Conclua as etapas a seguir para criar os grupos de contas:

1. No painel corporativo, clique em **Contas** para visualizar contas e grupos de contas na empresa.
2. Na seção do grupo de contas, clique em **Criar**.
3. Insira o nome do grupo de contas, tal como `Marketing`.
4. No campo de contato, insira o IBMid para o usuário que você deseja que seja o contato principal para o grupo de contas. Como um grupo de contas não pode conter nenhum recurso, ele não tem um proprietário como uma conta.
5. Selecione **Corporação de exemplo** como a conta pai.
6. Clique em **Criar**.

Repita as etapas para criar os grupos de contas de Vendas, Desenvolvimento, Design e Engenharia. Ao criar os grupos de contas de Design e Engenharia, certifique-se de incluir Desenvolvimento como o grupo de contas pai.

## Etapa 3. Importar contas existentes
{: #existing_accounts_tutorial}

Agora que você criou uma estrutura corporativa, é possível importar uma conta existente para a empresa. Quando você importa uma conta, ela é incluída permanentemente na empresa. Assim como quando você cria uma empresa, o faturamento para as contas importadas passa a ser gerenciado pela empresa, mas seus usuários e recursos permanecem os mesmos. Para obter detalhes, consulte [Importando contas existentes](/docs/account?topic=account-enterprise-add#add-accounts).

Para importar uma conta existente, o acesso a seguir é necessário:

* Dentro da conta a ser importada, deve-se ser o proprietário da conta ou ter a função de Administrador nos serviços de gerenciamento de Conta corporativa e de faturamento dentro da conta.
* Dentro da conta corporativa, a função de Editor ou de Administrador no Serviço corporativo e a função de Administrador no serviço de Faturamento são necessárias.

Conclua as etapas a seguir para importar a conta de UX-UI de exemplo para o grupo de contas de Design:
1. No painel corporativo, clique em **Contas** para visualizar as contas e os grupos de contas na empresa.
2. Na seção Contas, clique em **Incluir** > **Conta de importação**.
3. Selecione **UX-UI** na lista **Conta**.

  Se nenhuma conta é exibida, é provável que você não tenha o acesso correto em nenhuma conta existente.
  {: tip}

4. Selecione **Design** como o pai da conta UX-UI. Isso determina onde a conta existe na hierarquia corporativa.
5. Revise as informações sobre os impactos em sua conta e selecione **Eu entendo o impacto em minha conta**. Em seguida, clique em **Importar**.

Repita as etapas para importar mais contas.

## Etapa 4. Criar novas contas
{: #create-accounts_tutorial}

É possível criar novas contas em sua empresa. As contas são criadas como contas Pré-pagas, e o uso é faturado para a empresa. Para criar uma conta, é necessário ter uma política de acesso com a função de Editor ou de Administrador no Serviço corporativo.

Conclua as etapas a seguir para criar a conta da web de exemplo em sua empresa:

1. No painel corporativo, clique em **Contas** para visualizar as contas e os grupos de contas na empresa.
1. Na seção Contas, selecione **Incluir** > **Criar conta**.
1. Insira `Web` como o nome da conta.
1. Se você desejar designar um usuário diferente como o proprietário da conta, insira seu IBMid no campo **Proprietário**. O proprietário da conta tem acesso total para gerenciar a conta.
1. Selecione **Marketing** como o pai dessa conta.
1. Clique em **Criar**.

Depois de criar a conta, o proprietário da conta poderá efetuar login na conta para convidar outros usuários e gerenciar seu acesso.

Repita as etapas para criar mais contas. Como exemplo, a empresa Corporação de exemplo possui a conta-filha a seguir e a hierarquia do grupo de contas pai.

| Filho | Pai |
| ----- | -------|
| Imprimir | Marketing |
| Front-end | Engenharia |
| Back-end | Engenharia |
| Direto | Vendas |
| On-line | Vendas |
| Ativação | Vendas |
{:caption="Tabela 1. Hierarquia do grupo de contas-filhas e de contas pai" caption-side="top"}

## Etapa 5. Explorar assinaturas
{: #explore-sub_tutorial}

É possível explorar assinaturas na empresa por meio do painel corporativo. Quaisquer assinaturas existentes de contas que são importadas para a empresa são movidas para a conta corporativa e incluídas no [conjunto de crédito](/docs/billing-usage?topic=billing-usage-enterprise#credit-pool) corporativo.

1. Volte para o painel corporativo clicando em **Painel**. Na seção Faturamento, é possível visualizar o crédito disponível, o crédito restante e as datas de expiração da assinatura.
1. Para visualizar detalhes sobre todas as assinaturas na empresa, clique em **Visualizar assinaturas**.

   Na seção de assinatura da Plataforma, é possível visualizar a data de início, a data de encerramento, o crédito inicial e o crédito disponível da assinatura. Para incluir mais crédito, é possível comprar assinaturas adicionais e aplicar o código de assinatura.

## Etapa 6. Designar usuários no acesso de contas-filhas para criar recursos
{: #users_create_resources}

Antes de iniciar, certifique-se de alternar para a conta na qual você deseja criar o recurso. Nesse caso, alterne para a conta *Imprimir*. Se você desejar que os usuários em sua conta criem recursos por meio do catálogo e os designem a um grupo de recursos, deverá designar dois tipos de políticas de acesso.
* Designar uma política de acesso com a função de Visualizador ou superior no grupo de recursos.
* Designar uma política de acesso com a função de Editor ou de Administrador no serviço.

Conclua as etapas a seguir para designar o acesso necessário:

1. Acesse **Gerenciar** > **Acesso (IAM)** e selecione **Usuários**.
2. Selecione um nome de usuário na lista.
3. Clique na guia **Políticas de acesso** > **Designar acesso**.
4. Clique em **Designar acesso dentro de um grupo de recursos**.
5. Selecione o grupo de recursos ao qual você deseja designar o acesso de usuário.
6. Selecione a função de Visualizador ou superior no grupo de recursos.
7. Selecione o serviço ao qual você deseja designar o acesso de usuário.
  * Se você desejar que o usuário seja capaz de fornecer qualquer serviço, selecione **Todos os serviços**.
  * Se você desejar designar o acesso específico do usuário, selecione um serviço na lista. O usuário tem acesso somente ao serviço selecionado.
8. Selecione a função de Editor ou de Administrador.
9. Clique em **Designar**.

## Etapa 7. Visualizar o uso de todas as contas
{: #usage_tutorial}

1. Efetue login na conta corporativa da Corporação de exemplo.
2. Acesse **Gerenciar > Faturamento e uso** e selecione **Uso**.

   A página Uso exibe os custos para todo o uso em sua empresa, que é dividido por conta e grupo de contas. As informações de uso para serviços de infraestrutura clássica não são incluídas para o período de faturamento atual. Para obter mais informações, consulte [Visualizando o uso de seus recursos de infraestrutura clássica](/docs/billing-usage?topic=billing-usage-infra-usage).
3. Clique em **Marketing** na tabela para visualizar o uso dentro do grupo de contas. Semelhante ao nível corporativo, o uso é dividido pela conta e pelo grupo de contas.
4. Para visualizar o uso por recurso, acesse o nível de conta clicando em grupos de contas na tabela ou selecionando a conta no menu **Empresa**. Os custos são mostrados para cada tipo de recurso que foi usado durante o prazo.

Repita as etapas para visualizar o uso para os grupos de contas de Desenvolvimento, Vendas, Design e Engenharia.

   Na conta corporativa, não é possível visualizar dados de uso para o plano de recursos ou para a instância porque isso requer acesso dentro da conta. Clique em **Alternar para a conta** para visualizar dados para a conta. Você precisa de acesso de faturamento aos recursos e serviços na conta. Consulte [Visualizando seu uso](/docs/billing-usage?topic=billing-usage-viewingusage) para obter mais informações.

Os dados são mostrados na conta corporativa somente para uso que é incorrido por contas na empresa. Para visualizar o uso de antes de uma conta ter sido incluída na empresa, efetue login nessa conta e selecione o prazo relevante.
{: note}
