---

copyright:

  years: 2015, 2018
lastupdated: "2018-01-23"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Trabalhando com organizações
Como um proprietário da conta ou um gerenciador de organização, é possível executar tarefas de gerenciamento da organização, incluindo renomear sua organização, excluir uma organização ou um espaço, atualizar funções da organização ou do espaço e gerenciar cotas e domínios.
{:shortdesc}

Para gerenciar suas organizações no console do {{site.data.keyword.Bluemix}}, clique em **Gerenciar > Conta > Organizações do Cloud Foundry**. É
possível visualizar recursos de uma organização por vez somente. Se você for um membro de múltiplas organizações, poderá alternar organizações do link de preferências de conta do usuário na barra de menus do console.

## Renomeando organizações
{: #orgrename}

Conclua as etapas a seguir para renomear sua organização:
1. Clique em **Gerenciar** > **Conta** > **Organizações do Cloud Foundry**.
2. Determine qual organização você deseja renomear e clique em **Visualizar detalhes**.
3. Clique em **Editar organização do Cloud Foundry**.
4. Clique em **Editar** próximo ao nome da organização.
5. Digite o novo nome da organização e clique em **Salvar**.

## Excluindo organizações e espaços
{: #deleteorgs}

### Excluindo uma organização

Ao excluir uma organização, todos os espaços, aplicativos e serviços
dentro da organização são excluídos. Observe que as operações de exclusão não podem ser revertidas. Entre em contato com o suporte para excluir uma organização.

### Excluindo um espaço

Conclua as etapas a seguir para excluir um espaço:

1. Clique em **Gerenciar** > **Conta** > **Organizações do Cloud Foundry**.
2. Selecione a organização que você deseja editar e clique em **Visualizar detalhes**.
3. Determine qual espaço para excluir e clique em **Editar espaço**.
4. Clique em **Excluir espaço do Cloud Foundry**.

## Editando funções de usuário
{: #listmembers}

### Editando funções de usuário para uma organização específica 

Conclua as etapas a seguir para editar as funções de usuário de uma organização específica:

1. Clique em **Gerenciar** > **Conta** > **Organizações do Cloud Foundry**.
2. Determine qual organização você deseja editar e clique em **Visualizar detalhes**, em seguida, **Editar organização**.
4. É possível ver os membros de sua organização e suas funções na guia **USUÁRIOS**.

### Editando funções de usuário para um espaço específico

Conclua as etapas a seguir para editar as funções de usuário de um espaço específico:

1. Clique em **Gerenciar** > **Conta** > **Organizações do Cloud Foundry**.
2. Selecione a organização para a qual você deseja visualizar os membros e clique em **Visualizar detalhes**.
3. Determine qual espaço você deseja editar e clique em **Editar espaço**.
4. É possível ver os membros de seu espaço e suas funções na guia **USUÁRIOS**.

## Gerenciando cota
{: #managequota}

Como proprietário da conta ou gerenciador de organização do {{site.data.keyword.Bluemix_notm}}, é possível visualizar a cota usada e alocada para uma organização. A cota representa os limites de recurso para a organização, a qual é designada quando a organização é criada. Os recursos que estão disponíveis para uma organização variam dependendo se você tem uma conta grátis ou faturável. Qualquer aplicativo ou serviço em um espaço dentro da organização contribui
para o uso da cota alocada.

Para visualizar a cota usada e alocada de uma organização, conclua as etapas a seguir:

1. Clique em **Gerenciar** &gt; **Conta** &gt; **Organizações do Cloud Foundry**.
2. Identifique a organização para a qual deseja visualizar a cota e clique em **Visualizar detalhes**.
3. Clique em **Editar organização**.
4. Se você tiver espaços definidos em mais de uma região, selecione a região específica que deseja visualizar.
5. Clique em **COTA**. 
6. Por padrão, a página de cota do **Cloud Foundry** é aberta. É possível visualizar os detalhes da cota para os recursos a seguir:
 * MEMÓRIA
 * SERVIÇOS
 * PLANO
 * PREÇO
7. Clique em **Contêineres** para visualizar a alocação de cota de contêiner usada e disponível. A alocação de contêiner varia dependendo
de seu plano de precificação. É possível visualizar os detalhes da cota para os recursos a seguir:
 * MEMÓRIA
 * IP PÚBLICO
 * COMPARTILHAMENTOS DE ARQUIVO
8. Clique em **Servidores virtuais** para visualizar as máquinas virtuais.

Os contêineres não estão disponíveis na região de Sydney do {{site.data.keyword.Bluemix_notm}}. 
{: tip}

Para obter mais informações sobre contêineres, consulte [Cota](/docs/containers/container_planning.html#container_planning_quota) na
documentação de Contêineres.
Para mudar a cota que está alocada para uma organização, deve-se abrir um chamado de suporte. Para obter mais informações sobre como abrir um chamado de suporte,
consulte [Obtendo suporte ao cliente](/docs/get-support/howtogetsupport.html#getting-customer-support). 

## Gerenciando Domínios
{: #managedomains}

Como proprietário da conta ou gerenciador de organização do {{site.data.keyword.Bluemix_notm}}, é possível visualizar o domínio do sistema e incluir domínios customizados para aplicativos que são construídos dentro de uma organização e seus espaços. Como um gerenciador de espaço, a guia **Domínios** para um espaço é uma lista somente leitura dos domínios designados ao espaço.

1. Clique em **Gerenciar** &gt; **Conta** &gt; **Organizações do Cloud Foundry**.
2. Identifique a organização para a qual deseja visualizar ou editar domínios.
3. Selecione **Visualizar detalhes** para essa organização.
4. Clique em **Editar organização**.
5. Clique em **DOMÍNIOS**.

Se você incluir um domínio customizado, deverá
configurar seu servidor DNS para resolver seu domínio customizado para apontar para o
domínio do sistema {{site.data.keyword.Bluemix_notm}}. Dessa maneira, quando o {{site.data.keyword.Bluemix_notm}} receber uma solicitação para seu domínio customizado, ele poderá roteá-la adequadamente para seu app. O domínio do sistema está sempre disponível para um espaço e domínios customizados também podem ser alocados para um espaço. Os apps criados em um espaço podem usar qualquer um dos domínios listados para esse espaço. Para obter mais informações sobre como criar e usar domínios customizados, consulte [Usando um domínio customizado](/docs/apps/updapps.html#domain).
