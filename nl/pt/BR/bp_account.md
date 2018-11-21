---

copyright:

  years: 2018
lastupdated: "2018-10-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Melhores práticas para configurar sua conta
{: #account_setup}

Melhores práticas fornecem os blocos de construção básicos para o sucesso antes de iniciar a criação de recursos. Se você estiver pronto para obter apps para produção e configurar um ambiente para seus desenvolvedores, revise as seções a seguir para configurar sua conta.
{:shortdesc}

As melhores práticas a seguir focam na utilização de serviços ativados pelo IAM. Atualmente, nem todos os serviços no {{site.data.keyword.cloud}} estão ativados para IAM. Se uma instância de serviço em sua conta pertencer a uma organização ou espaço do Cloud Foundry, políticas, grupos de recursos e grupos de acesso do IAM não se aplicarão a ela. Ainda é possível usar organizações e espaços do Cloud Foundry e grupos de recursos em sua conta, mas é necessário designar aos usuários acesso a esses recursos separadamente. Para obter informações sobre como trabalhar com organizações e espaços do Cloud Foundry, consulte [Incluindo organizações e espaços](/docs/account/orgs_spaces.html#orgsspacesusers).
{: tip}

## O que é uma boa estratégia de grupo de recursos?
{: #resource-group-strategy}

Como um grupo de recursos é um contêiner lógico para recursos, usar um grupo de recursos por ambiente de projeto é um bom ponto de início. Essa estratégia permite que os administradores controlem e vejam o uso do recurso no nível do ambiente do projeto. Por exemplo, um projeto típico tem ambientes de desenvolvimento, teste e produção. Portanto, um projeto chamado `CustApp` teria os grupos de recursos a seguir:

* CustApp-Dev
* CustApp-Test
* CustApp-Prod

O acesso pode, então, ser concedido aos usuários. Por exemplo, um desenvolvedor geralmente tem direitos de acesso bastante amplos para o grupo de recursos de desenvolvimento e muito mais rígidos ou nenhum acesso ao grupo de recursos de produção.

Se você tiver uma conta pré-paga ou de assinatura, poderá criar grupos de recursos adicionais: 

1. Acesse **Gerenciar** &gt; **Conta** &gt; **Grupos de recursos**.
2. Clique em **Criar um grupo de recursos**.
3. Insira o nome de seu grupo de recursos.
4. Clique em **Incluir**.

## Configurando seu grupos de recursos
{: #setting-up-rgs}

Os grupos de recursos são um contêiner lógico para organizar seus recursos ativados para IAM. Todos os serviços que são gerenciados usando o controle de acesso do IAM pertencem a um grupo de recursos. Você designa um recurso para seu grupo de recursos ao criá-lo por meio do catálogo. Não é possível mudar a designação do grupo de recursos depois de configurá-la, esse é o motivo pelo qual é importante configurar alguns de seus grupos de recursos agora.

Se você tiver uma conta de avaliação ou Lite, usará o grupo de recursos padrão e não poderá criar nenhum adicional.
{: tip}

## Incluindo recursos em um grupo de recursos
{: #adding-resources}

Ao criar um recurso ativado para IAM por meio do catálogo, o grupo de recursos para o qual você deseja designá-lo deve ser selecionado. Depois que um recurso é criado, não é possível mudar o grupo de recursos para o qual ele é designado. Se um erro for cometido nesse estágio, será necessário excluir o recurso e criar um novo recurso.

### Acesso necessário para incluir um recurso em um grupo de recursos
{: #rg_access}

O proprietário da conta do {{site.data.keyword.cloud_notm}} pode incluir recursos em qualquer grupo de recursos. No entanto, outros usuários devem ter acesso concedido usando uma política de acesso do IAM. Há duas funções mínimas de gerenciamento de plataforma que devem ser designadas aos usuários para incluir recursos em um grupo de recursos:

* Função de visualizador ou superior no próprio grupo de recursos
* Função de editor ou superior no recurso ou serviço

Para incluir um recurso em um grupo de recursos, conclua as etapas a seguir:

1. Acesse **Gerenciar** &gt; **Conta** &gt; **Grupos de recursos**.
2. Clique no menu do ícone Mais ações ![ícone Mais ações](../icons/overflow-menu.svg) para o grupo de recursos no qual você deseja incluir recursos e selecione **Incluir recursos**.
3. Quando você for redirecionado para o catálogo, selecione o recurso que gostaria de incluir.
4. Selecione o grupo de recursos para o qual você deseja designá-lo.
5. Clique em **Criar**.

É possível sempre ir diretamente para o catálogo para criar recursos e designá-los a um grupo de recursos.
{: tip} 

Para obter mais informações, consulte [Melhores práticas para organizar recursos em um grupo de recursos](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).

## Próximas etapas

Configure grupos de acesso para os usuários e IDs de serviço que requerem o mesmo acesso a recursos e grupos de recursos em sua conta. É possível designar um número mínimo de políticas de acesso, o que economiza tempo. Para obter mais informações, consulte [Melhores práticas para designar acesso](/docs/iam/bp_access.html).

Consulte [Melhores práticas para organizar usuários, equipes e aplicativos](/docs/tutorials/users-teams-applications.html#best-practices-for-organizing-users-teams-applications), para obter mais informações sobre a configuração de usuários e equipes em sua conta.
