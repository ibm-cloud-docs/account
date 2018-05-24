---

copyright:

  years: 2015, 2018
lastupdated: "2018-03-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Atualizando organizações e espaços
{: #orgupdates}

Como proprietário da conta ou gerenciador de organização, é possível executar tarefas de
gerenciamento no nível de organização e no nível de espaço. Essas tarefas incluem renomeação de uma organização
ou espaço, designação ou atualização de funções de usuários do Cloud Foundry, gerenciamento de domínios e
visualização dos detalhes da cota da organização. 
{:shortdesc}

Para gerenciar suas organizações no console do {{site.data.keyword.Bluemix}}, clique em **Gerenciar > Conta > Organizações do Cloud Foundry**. É possível visualizar recursos somente de uma organização por vez. Se você for membro de diversas
organizações, será possível alternar as organizações por meio do link de preferências de conta do usuário na
barra de menus do console.

## Renomeando organizações
{: #orgrename}

Conclua as etapas a seguir para renomear sua organização. Observe que quaisquer mudanças feitas se aplicam a
todos os usuários na organização.

1. Clique em **Gerenciar** > **Conta** > **Organizações do Cloud Foundry**.
2. Clique no ícone Ações para a organização que você deseja renomear e selecione
**Renomear**.  
3. Insira o novo nome e clique em **Salvar**.

## Excluindo organizações e espaços
{: #deleteorgs}

### Excluindo uma organização

Para excluir uma organização, entre em contato com o
[Suporte](/docs/get-support/howtogetsupport.html). Quando uma organização é excluída, todos
os espaços e recursos dentro da organização também são excluídos. Certifique-se de observar que as operações
de exclusão não podem ser revertidas. 

### Excluindo um espaço

Ao excluir um espaço, todos os recursos e usuários incluídos também serão excluídos. Conclua as etapas a seguir para excluir um espaço:

1. Clique em **Gerenciar** > **Conta** > **Organizações do Cloud Foundry**.
2. Clique na organização à qual o espaço está designado.
3. Clique no ícone Ações e selecione **Excluir**.
4. Confirme que você deseja excluir o espaço digitando o nome do espaço no campo e clique em
**Excluir**.

## Editando funções de usuário
{: #listmembers}

As funções que podem ser designadas no nível da organização são Gerenciador, Gerenciador de faturamento e
Auditor. As funções que podem ser designadas no nível de espaço são Gerenciador, Desenvolvedor e Auditor. Para
obter as descrições detalhadas sobre função, consulte [Funções do Cloud
Foundry](/docs/iam/cfaccess.html#cfroles).

### Editando funções de usuário no nível de organização

Conclua as etapas a seguir para editar as funções de usuário para uma organização específica:

1. Clique em **Gerenciar** > **Conta** > **Organizações do Cloud Foundry**.
2. Clique no ícone Ações e selecione **Usuários**.
3. Dependendo de como desejar modificar as permissões de usuário, selecione ou desmarque a caixa de seleção para uma função específica.
4. Confirme suas mudanças clicando em **Salvar**. 

### Editando funções de usuário no nível de espaço

Conclua as etapas a seguir para editar as funções de usuário de um espaço específico:

1. Clique em **Gerenciar** > **Conta** > **Organizações do Cloud Foundry**.
2. Clique na organização à qual o espaço está designado.
3. Clique no nome do espaço.
4. Dependendo de como desejar modificar as permissões de usuário, selecione ou desmarque a caixa de seleção para uma função específica.
5. Confirme suas mudanças clicando em **Salvar**.

## Gerenciando Domínios
{: #managedomains}

Como proprietário da conta ou gerenciador de organização, é possível visualizar o domínio do sistema
e incluir domínios customizados para aplicativos que são construídos dentro de uma organização e seus espaços. Como gerenciador de espaço, a guia **Domínios** é uma lista somente leitura dos
domínios que são designados ao espaço.

1. Clique em **Gerenciar** &gt; **Conta** &gt; **Organizações do Cloud Foundry**.
2. Clique no ícone Ações para a organização e selecione **Domínios**.

Se você incluir um domínio customizado, deverá
configurar seu servidor DNS para resolver seu domínio customizado para apontar para o
domínio do sistema {{site.data.keyword.Bluemix_notm}}. Dessa maneira, quando o
{{site.data.keyword.Bluemix_notm}} recebe uma solicitação para seu domínio customizado, ela é roteada
corretamente para seu app. O domínio do sistema está sempre disponível para um espaço e domínios customizados também podem ser alocados para um espaço. Os apps criados em um espaço podem usar qualquer um dos domínios listados para esse espaço. Para obter mais informações sobre como criar e usar domínios customizados, consulte [Usando um domínio customizado](/docs/apps/updapps.html#domain).

## Gerenciando cota
{: #managequota}

É possível visualizar a cota usada e alocada para uma organização. A cota representa os limites de
recurso para a organização, que é designada quando a organização é criada. Os recursos que estão disponíveis
para uma organização variam dependendo se você tem uma conta grátis ou uma conta faturável. Qualquer
aplicativo ou serviço incluído em um espaço dentro da organização contribui para o uso da cota alocada.

Para visualizar a cota usada e alocada de uma organização, conclua as etapas a seguir:

1. Clique em **Gerenciar** &gt; **Conta** &gt; **Organizações do Cloud Foundry**.
2. Clique no ícone Ações para a organização específica e selecione **Cotas**.

   Por padrão, a página de cota **Cloud Foundry** é exibida. Por meio dela, é
possível visualizar os detalhes da cota para os recursos a seguir:
 
   * O número de apps
   * A quantia de memória 
   * O número de serviços 
   * Detalhes do plano 

3. Expanda os detalhes da região para visualizar a cota no nível de espaço. 

Para mudar a cota que é alocada para uma organização, deve-se abrir um chamado de suporte. Para obter
mais informações, consulte
[Obtendo suporte ao cliente](/docs/get-support/howtogetsupport.html#getting-customer-support). 

