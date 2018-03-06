---

copyright:

  years: 2015, 2018
lastupdated: "2018-01-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Criando organizações e espaços
{: #orgsspacesusers}

Como proprietário da conta, é possível gerenciar suas organizações e espaços por meio da página Gerenciar organizações no console do {{site.data.keyword.Bluemix}}. Gerenciadores de organização também podem usar a página Gerenciar Organizações,
para gerenciar quaisquer organizações na qual eles estão configurados como o gerente.
{:shortdesc}

Para gerenciar organizações e espaços, clique em **Gerenciar** &gt; **Conta** &gt; **Organizações do Cloud Foundry**. 


## Criando Organizações
{: #createorg}

As organizações podem abranger múltiplas regiões e elas são definidas pelos itens a seguir:

<dl>
<dt>Usuários</dt>
<dd>A função com permissão básica em organizações e espaços. Você deve estar designado a
uma organização para poder receber permissões para os espaços dentro da organização. Para
obter informações detalhadas, veja
[Usuários e funções](/docs/iam/users_roles.html#userrolesinfo).</dd>
<dt>Domínios</dt>
<dd>Fornecem a rota na Internet que é alocada para a organização. Uma rota tem um subdomínio e um domínio. Um subdomínio normalmente é o nome do aplicativo. Um
domínio pode ser um domínio do sistema ou um domínio customizado que você registrou para
seu aplicativo. Consulte [Gerenciando domínios customizados](/docs/account/manageorg.html#managedomains).<br/>
<p>**Nota:** se um domínio customizado for incluído, deve-se configurar seu servidor DNS para resolver seu domínio customizado para apontar para o domínio do sistema {{site.data.keyword.Bluemix_notm}}. Dessa
maneira, quando o
{{site.data.keyword.Bluemix_notm}}
receber uma solicitação para o domínio customizado, ele poderá roteá-lo corretamente
para o aplicativo.</p></dd>
<dt>Cota</dt>
<dd>Representa os recursos que estão disponíveis para uma organização, incluindo o número de serviços e a quantia de memória que pode ser alocada para uso pela organização. As cotas são designadas quando as organizações são criadas. Qualquer aplicativo ou serviço em um espaço dentro de uma organização contribui para o uso da cota. Com as contas pré-pagas ou de assinatura, é possível ajustar sua cota para aplicativos e contêineres do Cloud Foundry conforme as necessidades de sua organização mudam. Consulte [Gerenciando cota](/docs/account/manageorg.html#managequota).</dd>
</dl>

Em uma conta de Assinatura, a cota é um limite definido pelo usuário que aciona notificações de gastos.
{: tip}

No {{site.data.keyword.Bluemix_notm}}, é possível usar organizações para permitir a colaboração entre usuários e para facilitar o agrupamento lógico de recursos de projetos das maneiras a seguir:

   * É possível agrupar um conjunto de espaços, apps, serviços, domínios, rotas e usuários em organizações. 
   * É possível gerenciar o acesso aos espaços e organizações por usuário. 

Ao criar uma organização, o nome deve ser exclusivo no {{site.data.keyword.Bluemix_notm}}. Se o nome da organização já está em uso por outro usuário do {{site.data.keyword.Bluemix_notm}} Public, Dedicated ou Local, deve-se especificar um novo nome. Depois de criar a organização, você é designado automaticamente à permissão *Gerenciador de organização*, que permite editar o nome da organização, incluir usuários e criar ou excluir espaços na organização.

É possível contatar o suporte para excluir uma organização. Ao excluir uma organização, todos os espaços, aplicativos e serviços
dentro da organização são excluídos.

As [funções de usuário](/docs/iam/users_roles.html#userrolesinfo) a seguir podem ser designadas a usuários em uma organização. Todos os usuários convidados para a conta são designados à função de auditor por padrão.

   * Gerente da organização
   * Gerente de faturamento da organização
   * Auditor da organização

É possível criar uma organização concluindo as etapas a seguir:

1. Clique em **Gerenciar** &gt; **Conta** &gt; **Organizações do Cloud Foundry**.
2. Clique em **Incluir uma nova organização do Cloud Foundry**.
3. Insira o nome da organização.
4. Clique em ** Adicionar**.

<!-- Add info on Manage infrastructure option under a space -->

## Criando Espaços
{: #spaceinfo}

Dentro de uma organização, é possível usar espaços para
agrupar um conjunto de aplicativos, serviços e usuários. Espaços são ligados a uma região específica no
{{site.data.keyword.Bluemix_notm}}.

Depois de incluir usuários em uma organização, é possível conceder a eles permissões para os espaços. Semelhantes às organizações, os espaços também têm um conjunto de
[funções de usuário](/docs/iam/users_roles.html#userrolesinfo) com permissões específicas que são designadas a membros da equipe:

  * Gerente de espaço
  * Desenvolvedor de espaço
  * Auditor de espaço

Deve-se atribuir a um usuário pelo menos uma das permissões no espaço.
{: tip}

É possível criar espaços em
sua organização, por exemplo, um espaço *dev* como
um ambiente de desenvolvimento, um espaço *test* como um ambiente
de teste e um espaço *production* como um ambiente de
produção. Em seguida, é possível associar os apps aos espaços. Conclua as etapas a seguir para criar um espaço:

1. Clique em **Gerenciar** &gt; **Conta** &gt; **Organizações do Cloud Foundry**.
2. Determine a organização que você deseja incluir um espaço e selecione **Visualizar detalhes**.
4. Clique em **Incluir um espaço do Cloud Foundry**.
5. Insira o nome de espaço.
6. Clique em ** Adicionar**.
