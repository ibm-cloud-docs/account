---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: account, add orgs, add spaces, manage users, user access

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Incluindo organizações e espaços
{: #orgsspacesusers}

Como um proprietário da conta do {{site.data.keyword.Bluemix}}, é possível incluir organizações e espaços em sua conta. Se você for um gerenciador de organização, será possível gerenciar as organizações na conta. Acesse **Gerenciar** > **Conta** e selecione **Organizações do Cloud Foundry**.
{:shortdesc}

É possível usar as organizações para permitir a colaboração entre usuários e para facilitar o agrupamento
lógico de recursos de projetos das maneiras a seguir:

   * É possível agrupar um conjunto de espaços, apps, serviços, domínios, rotas e usuários juntos em
suas organizações.
   * É possível gerenciar o acesso de usuário às organizações e aos espaços individualmente.

## Incluindo organizações
{: #createorg}

As organizações, que podem abranger múltiplas regiões, são definidas pelos itens a seguir:

<dl>
<dt>Usuários</dt>
<dd>A função com permissão básica em organizações e espaços. Deve-se estar designado a uma
organização para poder receber outras permissões para os espaços dentro da organização. Para obter mais
detalhes, consulte [Usuários e funções](/docs/iam?topic=iam-userroles).</dd>
<dt>Domínios</dt>
<dd>Forneça a rota na Internet que está alocada para a organização. Uma rota tem um subdomínio e um domínio. Normalmente, um subdomínio é o nome do aplicativo. Um domínio pode ser um domínio do sistema ou um domínio customizado que você registrou para seu aplicativo.<br/>
<p>Se você incluir um domínio customizado, deverá
configurar seu servidor DNS para resolver seu domínio customizado para apontar para o
domínio do sistema {{site.data.keyword.Bluemix_notm}}. Dessa
maneira, quando o
{{site.data.keyword.Bluemix_notm}}
receber uma solicitação para o domínio customizado, ele poderá roteá-lo corretamente
para o aplicativo.</p></dd>
<dt>Cota</dt>
<dd>Representa os recursos que estão disponíveis para uma organização, incluindo o número de serviços e a
quantia de memória que pode ser alocada para uso pela organização. As cotas são designadas quando as
organizações são criadas. Qualquer aplicativo ou serviço em um espaço dentro de uma organização contribui para
o uso da cota. Com as contas Pay-As-You-Go ou Assinatura, é possível ajustar sua cota para aplicativos e
contêineres do Cloud Foundry de acordo com as necessidades de sua organização.</dd>
</dl>

Em uma conta de Assinatura, a cota é um limite definido pelo usuário que inicia as notificações de gastos.
{: tip}

Ao incluir uma organização, o nome deve ser exclusivo no
{{site.data.keyword.Bluemix_notm}}. Se o nome da organização já estiver em uso por outro
usuário do {{site.data.keyword.Bluemix_notm}} Public, Dedicated ou Local, um novo nome deverá
ser especificado. Depois de incluir a organização, você é designado automaticamente à permissão do Gerenciador de organização, portanto, é possível editar o nome da organização, incluir usuários e criar ou excluir espaços na organização. Se você tiver uma conta faturável, será possível incluir quantas organizações forem necessárias. No entanto, em uma conta Lite, é possível ter apenas uma organização.

As [funções de usuário](/docs/iam?topic=iam-userroles) a seguir podem ser designadas a usuários em uma organização. Todos os usuários que são convidados para a conta são designados à função de auditor por padrão.

   * Gerente da organização
   * Gerente de faturamento da organização
   * Auditor da organização

Conclua as etapas a seguir para incluir uma organização:

  1. Clique em **Incluir uma organização**.
  2. Insira o nome da organização.  
  3. Clique em **Incluir**.

<!-- Add info on Manage infrastructure option under a space -->

## Incluindo espaços
{: #spaceinfo}

Dentro de uma organização, é possível usar espaços para
agrupar um conjunto de aplicativos, serviços e usuários. Espaços são ligados a uma região específica no
{{site.data.keyword.Bluemix_notm}}. É possível criar espaços em uma organização com base no ciclo de
vida de entrega. Por exemplo, é possível criar um espaço `dev` como um ambiente de
desenvolvimento, um espaço `test` como um ambiente de teste e um
espaço `production` como um ambiente de produção. Em seguida, é possível associar os apps aos espaços.

Depois de incluir usuários em uma organização, é possível conceder a eles permissões para os espaços. Semelhantemente às organizações, os espaços também têm um conjunto de [funções do Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles) com permissões específicas que são designadas aos membros da equipe:

  * Gerente de espaço
  * Desenvolvedor de espaço
  * Auditor de espaço

Deve-se atribuir a um usuário pelo menos uma das permissões no espaço.
{: tip}

Conclua as etapas a seguir para incluir um espaço:

  1. Clique no nome da organização na qual você deseja incluir um espaço.
  2. Clique em **Incluir um espaço**.
  3. Selecione uma região e insira um nome.
  4. Clique em **Salvar**.
