---

copyright:
  years: 2015, 2019
lastupdated: "2019-06-19"

keywords: account, add orgs, add spaces, cloud foundry orgs

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Incluindo organizações e espaços
{: #orgsspacesusers}

Como um proprietário da conta do {{site.data.keyword.Bluemix}}, é possível incluir organizações e espaços em sua conta. Se você for um gerenciador de organização, será possível gerenciar as organizações na conta. 
{:shortdesc}

## Conceitos de organização do Cloud Foundry
{: #cf-org-concepts}

É possível gerenciar as organizações e os espaços do Cloud Foundry acessando **Gerenciar** > **Conta** e selecionando **Recursos da conta > Organizações do Cloud Foundry**.

As organizações permitem a colaboração entre os usuários e facilitam o agrupamento lógico de recursos de projetos das formas a seguir:

   * É possível agrupar um conjunto de espaços, apps, serviços, domínios, rotas e usuários juntos em
suas organizações.
   * É possível gerenciar o acesso de usuário às organizações e aos espaços individualmente.

As organizações, que podem abranger múltiplas regiões, são definidas pelos itens a seguir:

<dl>
<dt>Espaços</dt>
<dd>Um subgrupo dentro de uma organização que pode ser usado para organizar aplicativos, serviços e usuários. Espaços são ligados a uma região específica no
{{site.data.keyword.Bluemix_notm}}. </dd>
<dt>Usuários</dt>
<dd>A função com permissão básica em organizações e espaços. Você deve estar designado a uma organização antes de poder receber outras permissões para os espaços dentro da organização. Para obter mais detalhes, consulte [Acesso ao Cloud Foundry](/docs/iam?topic=iam-cfaccess).</dd>
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

## Incluindo organizações
{: #createorg}

Se você tiver uma conta faturável, será possível incluir quantas organizações forem necessárias. As contas Lite podem ter apenas uma organização, que já está criada em sua conta.

1. Acesse **Gerenciar** > **Conta** e selecione **Recursos da conta > Organizações do Cloud Foundry**. Clique em **Criar**.
2. Insira um nome de organização. O nome deve ser exclusivo no {{site.data.keyword.Bluemix_notm}}.

   Se o nome da organização já estiver em uso por outro usuário do {{site.data.keyword.Bluemix_notm}} Public, Dedicated ou Local, você terá que especificar um nome diferente.
3. Clique em **Incluir**.

Depois de incluir a organização, a permissão de gerenciador de organização é automaticamente designada a você, então é possível editar o nome da organização, incluir usuários e criar ou excluir espaços na organização.

É possível designar as [funções do Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles) a seguir para os usuários em uma organização. Todos os usuários convidados para a conta recebem a função de auditor por padrão.

   * Gerente da organização
   * Gerente de faturamento da organização
   * Auditor da organização

## Incluindo espaços
{: #spaceinfo}

Dentro de uma organização, é possível usar espaços para
agrupar um conjunto de aplicativos, serviços e usuários. Os espaços são definidos dentro de uma única região do {{site.data.keyword.Bluemix_notm}}. É possível criar espaços em uma organização com base no ciclo de
vida de entrega. Por exemplo, é possível criar um espaço `dev` como um ambiente de
desenvolvimento, um espaço `test` como um ambiente de teste e um
espaço `production` como um ambiente de produção. Em seguida, é possível associar os apps aos espaços.

Para incluir um espaço em uma organização, conclua as etapas a seguir.

1. Na página Organizações do Cloud Foundry, clique no nome da organização na qual você deseja incluir um espaço.
2. Clique em **Incluir um espaço**.
3. Selecione uma região e insira um nome.
4. Clique em **Salvar**.

Depois de incluir usuários em uma organização, é possível conceder a eles permissões para os espaços. Semelhantemente às organizações, os espaços também têm um conjunto de [funções do Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles) com permissões específicas que são designadas aos membros da equipe:

  * Gerente de espaço
  * Desenvolvedor de espaço
  * Auditor de espaço

Deve-se atribuir a um usuário pelo menos uma das permissões no espaço.
{: tip}
