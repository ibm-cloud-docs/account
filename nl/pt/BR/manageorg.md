---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: update orgs, update spaces, quotas, Cloud Foundry orgs, domains

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# Atualizando organizações e espaços
{: #orgupdates}

Como um proprietário da conta do {{site.data.keyword.Bluemix}} ou gerenciador de organização, é possível executar tarefas de gerenciamento no nível de organização e no nível de espaço. Essas tarefas incluem renomeação de uma organização
ou espaço, designação ou atualização de funções de usuários do Cloud Foundry, gerenciamento de domínios e
visualização dos detalhes da cota da organização.
{:shortdesc}

Acesse **Gerenciar > Conta** e selecione **Organizações do Cloud Foundry**.

É possível visualizar os recursos de somente uma organização por vez. Se você for membro de diversas
organizações, será possível alternar as organizações por meio do link de preferências de conta do usuário na
barra de menus do console.
{: tip}

  * Para renomear uma organização, clique no ícone Ações ![Ícone de ação](../icons/action-menu-icon.svg) para a organização que você deseja renomear e selecione **Renomear**.
    {: #orgrename}

    Quaisquer mudanças feitas se aplicam a todos os usuários na organização.

  * Para excluir uma organização, entre em contato com o
[Suporte](/docs/get-support?topic=get-support-getting-customer-support).
    {: #deleteorgs}

    Quando uma organização é excluída, todos
os espaços e recursos dentro da organização também são excluídos. Essa ação não pode ser revertida.

  * Para excluir um espaço, selecione a organização à qual o espaço está designado. Em seguida, clique no ícone Ações ![Ícone de ação](../icons/action-menu-icon.svg) e selecione **Excluir**.

    Ao excluir um espaço, todos os recursos e usuários incluídos também serão excluídos.

  * Para editar funções de usuário no nível de organização, clique no ícone Ações ![Ícone de ação](../icons/action-menu-icon.svg) e selecione **Usuários**.
    {: #listmembers}

    Dependendo de como desejar modificar as permissões de usuário, selecione ou desmarque a caixa de seleção para uma função específica. As funções que podem ser designadas no nível de organização são Gerente, Gerente de faturamento e Auditor. Para obter mais informações, consulte [Funções do Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles).

  * Para editar funções de usuário para um espaço específico, clique na organização à qual o espaço é designado. Em seguida, clique no nome do espaço.

    Dependendo de como desejar modificar as permissões de usuário, selecione ou desmarque a caixa de seleção para uma função específica. As funções que podem ser designadas no nível de espaço são Gerente, Desenvolvedor e Auditor. Para obter mais informações, consulte [Funções do Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles).

  * Para gerenciar seus domínios, clique no ícone Ações ![Ícone de ação](../icons/action-menu-icon.svg) para a respectiva organização e selecione **Domínios**.
    {: #managedomains}

    Como proprietário da conta ou gerenciador de organização, é possível visualizar o domínio do sistema
e incluir domínios customizados para aplicativos que são construídos dentro de uma organização e seus espaços. Se você for um gerenciador de espaço, essa página exibirá a lista somente leitura dos domínios que estão designados ao espaço.

    Se você incluir um domínio customizado, deverá
configurar seu servidor DNS para resolver seu domínio customizado para apontar para o
domínio do sistema {{site.data.keyword.Bluemix_notm}}. Dessa maneira, quando o
{{site.data.keyword.Bluemix_notm}} recebe uma solicitação para seu domínio customizado, ela é roteada
corretamente para seu app. O domínio do sistema está sempre disponível para um espaço e domínios customizados também podem ser alocados para um espaço. Os apps que são criados em um espaço podem usar qualquer um dos domínios que estão listados para esse espaço. Para obter mais informações sobre a criação e o uso de domínios customizados, consulte [Gerenciando seus domínios](/docs/apps?topic=creating-apps-update-domain).

  * Para gerenciar a cota alocada para uma organização, clique no ícone Ações ![Ícone de ação](../icons/action-menu-icon.svg) para a respectiva organização e selecione **Cotas**.
    {: #managequota}

    Deste ponto, é possível visualizar os detalhes da cota para o número de apps, quantia de memória, número de serviços e detalhes de planejamento. A cota representa os limites de recurso para a organização, que é designada quando a organização é criada. Os recursos que estão disponíveis
para uma organização variam dependendo se você tem uma conta grátis ou uma conta faturável. Qualquer aplicativo ou serviço incluído em um espaço dentro da organização contribui para o uso da cota alocada.

    Para mudar a cota que está alocada para uma organização, deve-se criar um caso de suporte. Para obter mais informações, veja [Trabalhando com casos de suporte](/docs/get-support?topic=get-support-open-case).

    Para visualizar os detalhes da cota no nível de espaço para cada local, clique no ícone Ações ![Ícone de ação](../icons/action-menu-icon.svg) para a respectiva organização e selecione **Cotas**. Em seguida, expanda cada linha de forma apropriada.
