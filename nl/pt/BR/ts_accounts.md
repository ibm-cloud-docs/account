---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-24"
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Resolução de problemas para gerenciamento de contas
{: #managingaccounts}

Os problemas gerais com o gerenciamento de sua conta podem incluir apps diferentes que têm o mesmo nome de domínio ou os administradores não podem visualizar todas as organizações. Em muitos casos, é possível recuperar-se desses problemas seguindo algumas etapas simples.
{:shortdesc}


## Por que não posso acessar um local do {{site.data.keyword.Bluemix_notm}} diferente?
{: #nosecondreg}
{: troubleshoot}

Não é possível criar um novo local porque seu tipo de conta não permite isso.

Você recebe uma mensagem de erro ao tentar criar um novo local do {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Isso é provavelmente porque você está usando uma conta Lite, que suporta o desenvolvimento em somente um local público.
{: tsCauses}

Para acessar mais locais, faça upgrade para uma conta faturável. Acesse **Gerenciar > Faturamento e uso** e selecione **Pagamentos**.
{: tsResolve}


## Por que não posso criar uma nova organização?
{: #nosecondorg}
{: troubleshoot}

Você tenta criar mais de uma organização e tem uma conta Lite.  

Você receberá uma mensagem de erro ao tentar criar uma nova organização.
{: tsSymptoms}

Isso é provavelmente porque você está usando uma conta Lite, que suporta o desenvolvimento em somente uma organização.
{: tsCauses}

Para criar uma nova organização, faça upgrade para uma conta faturável. Acesse **Gerenciar > Faturamento e uso** e selecione **Upgrades**.
{: tsResolve}


## Por que não posso criar uma nova instância do plano Lite?
{: #nosecondlite}
{: troubleshoot}

Você tenta criar uma instância extra, mas tem uma conta Lite.

Você recebe a mensagem de erro a seguir quando tenta criar uma nova instância do plano Lite:
{: tsSymptoms}

`Não é possível provisionar uma nova instância Lite`

Há um limite de uma instância por instância do plano Lite para assegurar que esses planos permaneçam grátis.
{: tsCauses}

É possível criar mais instâncias do serviço selecionando um dos planos de serviços faturáveis que estão disponíveis nas contas faturáveis. Para fazer upgrade para uma conta faturável por meio do console, acesse **Gerenciar > Faturamento e uso** e selecione **Upgrades**.
{: tsResolve}

Se você não desejar fazer upgrade de uma conta Lite e não estiver mais usando a sua instância de serviço Lite existente, será possível excluir a instância do plano Lite existente do painel e, em seguida, criar uma nova instância.


## Como eu excedi o abono de memória de tempo de execução?
{: #noruntimemem}
{: troubleshoot}

Você ultrapassou a memória permitida para sua conta.

Não é possível implementar apps e um erro está informando que você excedeu o limite de memória de sua organização.
{: tsSymptoms}

Em uma conta Lite, os aplicativos do Cloud Foundry podem usar até 256 MB de memória de tempo de execução instantânea. Em contas faturáveis, há um limite de 2 GB de memória.
{: tsCauses}

Se você estiver usando uma conta Lite, será possível obter mais memória fazendo upgrade para uma conta faturável. Acesse **Gerenciar > Faturamento e uso** e selecione **Upgrades**.
{: tsResolve}

Se você não desejar fazer upgrade de uma conta Lite, mas tiver alguns apps inativos, será possível excluí-los para liberar alguma memória de tempo de execução.


## Por que minha conta está inativa?
{: #ts_accnt_inactive}
{: troubleshoot}

Não será possível criar um app no {{site.data.keyword.Bluemix_notm}} se a sua conta estiver inativa. Deve-se entrar em contato com a equipe de suporte para corrigir esse problema.

Quando você tenta criar um app no {{site.data.keyword.Bluemix_notm}}, a mensagem de erro a seguir é exibida:
{: tsSymptoms}

`BXNUI0096E: O app não foi criado. Sua conta está inativa porque ela foi cancelada
ou suspensa.`

O status de sua conta do {{site.data.keyword.Bluemix_notm}}
torna-se inativo quando a conta é cancelada ou suspensa.
{: tsCauses}

Para reativar sua conta, abra um caso por meio do [centro de suporte](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo"). Inclua as informações a seguir em seu caso:
{: tsResolve}

  * O ID IBM que você usa para efetuar login no {{site.data.keyword.Bluemix_notm}}.
  * O nome da organização em que seu app está sendo criado. Essas informações podem ajudar a equipe de suporte a determinar se você está designado às funções ou associação corretas em sua organização.


## Por que não posso incluir usuários em uma organização?
{: #ts_adduser}
{: troubleshoot}

É possível convidar os usuários para sua organização somente se você for o proprietário da conta ou se for um gerente e um membro da organização.

Não é possível ver o link **Convidar um novo usuário** na seção **Gerenciar organizações**.
{: tsSymptoms}

Somente os usuários {{site.data.keyword.Bluemix_notm}} a seguir
podem convidar usuários para uma organização:
{: tsCauses}
  * O proprietário da conta da organização
  * Os gerenciadores de organização que também são membros, não colaboradores, da organização

No
{{site.data.keyword.Bluemix_notm}}, é possível ser um membro ou um colaborador de uma organização:

<dl><dt>Colaborador</dt>
<dd>Você será um colaborador de uma organização se já tiver uma conta do {{site.data.keyword.Bluemix_notm}} e alguém convidá-lo para a organização.</dd>
<dt>Membro</dt>
<dd>Você será um membro de uma organização se não tiver uma conta do {{site.data.keyword.Bluemix_notm}}, mas alguém convidá-lo para a organização e você se inscrever para o {{site.data.keyword.Bluemix_notm}} por meio do convite.</dd>
</dl>

Não será possível convidar usuários para sua organização se você for um colaborador da organização, mesmo que esteja designado como um gerenciador de organização.

Todos os gerenciadores de organização, incluindo colaboradores em uma organização, podem incluir, modificar e remover usuários que já estão na organização.
{: note}

Se não for possível convidar usuários para sua organização e você precisar de uma função diferente para fazer isso, entre em contato com o gerenciador de organização para mudar sua função. Para identificar o gerente da organização, conclua as
etapas a seguir:
{: tsResolve}

  1. Na barra de menus do console, clique em **Gerenciar > Conta** e selecione **Contatos da empresa**.
  2. Acesse sua organização e visualize as informações sobre o gerente da organização na guia **USUÁRIOS**.  

Caso não seja possível convidar usuários porque você é um colaborador e não um membro, deve-se excluir sua conta anterior do {{site.data.keyword.Bluemix_notm}} e, em seguida, ser convidado para se associar à conta como um membro da organização. Para excluir sua conta anterior e se associar à conta como um membro,
conclua as etapas a seguir:

  1. Entre em contato com o [Suporte do {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} para abrir um caso de suporte e solicitar que sua conta seja excluída. Se houver dados associados à sua conta antiga que você deseja salvar e mover para a nova conta, inclua essas informações em seu e-mail.
  2. Após sua conta ser excluída, peça a um usuário com a função de gerenciador de organização para convidá-lo para a organização como um gerenciador de organização. Em seguida, inscreva-se no {{site.data.keyword.Bluemix_notm}} a partir do convite.


## Por que não há espaços associados à minha organização atual?
{: #ts_no_space}
{: troubleshoot}

Não será possível criar um app se não houver espaço associado à sua organização atual.

Ao tentar criar um app, a mensagem de erro a seguir é exibida:
{: tsSymptoms}

`BXNUI0097E: Para que seja possível incluir um app, pelo menos um espaço deve estar associado à sua organização e região. No Painel, clique em Criar um espaço. Quando o espaço for criado, tente novamente. `

Os apps devem ser criados em um espaço em sua organização.
{: tsCauses}

Para criar um espaço, use um dos métodos a seguir:
{: tsResolve}

  * Na barra de menus do console, clique em **Gerenciar > Conta** e selecione **Organizações**. Em seguida, selecione a organização na qual você deseja criar o espaço e clique em **Criar um espaço**.
  * Na interface da linha de comandos do Cloud Foundry, digite `cf create-space <space_name> -o <organization_name>`.


## Por que alguns apps compartilham um nome de domínio?
{: #ts_domain_diff}
{: troubleshoot}

Você pode observar que vários aplicativos compartilham uma URL no {{site.data.keyword.Bluemix_notm}}.

Esse problema pode ocorrer quando você designa a mesma rota de URL a diferentes apps em um espaço.
{: tsCauses}

Por exemplo, você envia por push o app myApp1 para o {{site.data.keyword.Bluemix_notm}} e configura o domínio para `mynewapp.stage1.mybluemix.net`. Em seguida, envia por push outro app myApp2 para o mesmo espaço e configura uma de suas rotas de URL para `mynewapp.stage1.mybluemix.net`. A rota agora é mapeada para ambos os apps.

Esse é um comportamento suportado e é possível usar essa prática para atingir o tempo de inatividade zero para o upgrade do app. Para obter mais informações, veja [Como assegurar tempo de inatividade zero](/docs/overview/zero_downtime.html#zero-downtime).
{: tsResolve}


## Por que os administradores não podem usar o console para visualizar todas as organizações?
{: #ts_ui_org}
{: troubleshoot}

Como um administrador, não é possível exibir cada organização para administrá-las quando você usa o console do {{site.data.keyword.Bluemix_notm}}. Você pode exibir e administrar apenas as organizações às quais pertence.

Como um administrador, não é possível visualizar todas as organizações por meio do console.
{: tsSymptoms}

Essa é uma limitação do console.
{: tsCauses}

É possível usar comandos como `cf orgs`, `cf create-org` e `cf delete-org` na interface da linha de comandos do Cloud Foundry para gerenciar todas as organizações. Para obter uma lista completa de comandos do Cloud Foundry, insira `cf help`.
{: tsResolve}

## Por que não posso incluir minhas informações de cartão de crédito?
{: #ts_addcc}
{: troubleshoot}

Não é possível enviar suas informações de cartão de crédito para fazer upgrade de sua conta Lite para uma conta faturável.

O botão **Enviar** na página Incluir cartão de crédito está desativado.
{: tsSymptoms}

Esse problema ocorre quando as suas informações não são preenchidas corretamente na página Incluir cartão de crédito.
{: tsCauses}

Conclua
as etapas a seguir:
{: tsResolve}

  1. Na página Incluir cartão de crédito, preencha todos os campos obrigatórios. 
  2. Selecione **Eu li e concordo com os Termos e Condições da IBM**, em seguida, clique em **Enviar**. 
  
