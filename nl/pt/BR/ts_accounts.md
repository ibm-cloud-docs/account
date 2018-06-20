---

copyright:

  years: 2015, 2018

lastupdated: "2017-11-09"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Resolução de problemas para gerenciamento de contas
{: #managingaccounts}

Os problemas gerais ao gerenciar sua conta podem incluir apps diferentes que compartilham o mesmo nome de domínio ou administradores que não podem visualizar todas as organizações. Em muitos casos, é possível recuperar-se desses problemas seguindo algumas etapas simples.
{:shortdesc}

## Impossível acessar um {{site.data.keyword.Bluemix_notm}} de região diferente
{: #nosecondreg}

Você recebe uma mensagem de erro quando tenta criar uma nova região do {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Isso é provavelmente porque você está usando uma conta Lite, que suporta desenvolvimento somente em uma região pública. Você seleciona a região pública do {{site.data.keyword.Bluemix_notm}} na qual deseja trabalhar quando a conta é configurada pela primeira vez.
{: tsCauses}

Se você tiver uma conta Lite, será possível fazer upgrade para uma conta faturável para acessar regiões adicionais. Acesse a página **Gerenciar > Faturamento e uso > Faturamento** no console e clique em **Incluir cartão de crédito**. Na página **Faturamento**, é possível também verificar se você tem uma conta Lite.
{: tsResolve}

## Impossível criar nova organização
{: #nosecondorg}

Você receberá uma mensagem de erro quando tentar criar uma nova organização.
{: tsSymptoms}

Isso é provavelmente porque você está usando uma conta Lite, que suporta desenvolvimento em somente uma organização. Você cria a organização quando sua conta é configurada pela primeira vez.
{: tsCauses}

Se você tiver uma conta Lite, será possível fazer upgrade para uma conta faturável para acessar organizações adicionais. Acesse a página **Gerenciar > Faturamento e uso > Faturamento** no console e clique em **Incluir cartão de crédito**. Na página **Faturamento**, é possível também verificar se você tem uma conta Lite.
{: tsResolve}

## Não é possível criar instância do plano Lite
{: #nosecondlite}

Você recebe a mensagem de erro a seguir quando tenta criar uma instância do plano Lite:
{: tsSymptoms}

`Não é possível provisionar uma nova instância Lite`

Há um limite de uma instância por instância do plano Lite para nos permitir manter esses planos grátis.
{: tsCauses}

É possível criar instâncias adicionais do serviço selecionando um dos planos de serviço faturáveis, que estão disponíveis nas contas faturáveis. Para fazer upgrade para uma conta faturável do console, acesse a página **Gerenciar > Faturamento e uso > Faturamento** e clique em **Incluir cartão de crédito**.
{: tsResolve}

Se você não desejar fazer upgrade de uma conta Lite e não estiver mais usando sua instância de serviço Lite existente, será possível excluir a instância do plano Lite existente do painel e, em seguida, criar uma nova instância.

## Excedido o abono de memória de tempo de execução
{: #noruntimemem}

Você não consegue implementar apps e obtém um erro informando que excedeu o limite de memória de sua organização.
{: tsSymptoms}

Em uma conta Lite, seus apps Cloud Foundry podem usar até 256 MB de memória instantânea de tempo de execução. Em contas faturáveis, há um limite de memória de 2 GB.
{: tsCauses}

Se você estiver usando uma conta Lite, será possível obter memória adicional fazendo upgrade para uma conta faturável. Acesse a página **Gerenciar > Faturamento e uso > Faturamento** no console e clique em **Incluir cartão de crédito**.
{: tsResolve}

Se você não desejar fazer upgrade de uma conta Lite, mas tiver alguns apps inativos, será possível excluir os apps inativos para liberar memória de tempo de execução.

## A conta está inativa
{: #ts_accnt_inactive}

Não será possível criar um app no {{site.data.keyword.Bluemix_notm}} se a sua conta estiver inativa. Deve-se entrar em contato com a equipe de suporte para corrigir esse problema.

Ao tentar criar um app no {{site.data.keyword.Bluemix_notm}}, você vê a mensagem de erro a seguir:
{: tsSymptoms}

`BXNUI0096E: O app não foi criado. Sua conta está inativa porque ela foi cancelada
ou suspensa.`

O status de sua conta do {{site.data.keyword.Bluemix_notm}} torna-se inativo quando a conta é cancelada ou suspensa.
{: tsCauses}

Para reativar sua conta, entre em contato com o [Suporte do {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://ibm.biz/bluemixsupport.com){: new_window}. Inclua as informações a seguir no e-mail:
{: tsResolve}

  * O ID IBM que você usa para efetuar login no {{site.data.keyword.Bluemix_notm}}.
  * O nome da organização em que seu app está sendo criado. Essas informações podem ajudar a equipe de suporte a determinar se você está designado às funções ou associação corretas em sua organização.

## Não é possível incluir usuários em uma organização
{: #ts_adduser}

É possível convidar mais de um usuário para trabalhar sob a mesma organização. É possível convidar os usuários para a sua organização somente se você é o proprietário da conta ou se você é um gerente da organização.

Não é possível ver o link **Convidar um novo usuário** na seção **Gerenciar organizações**.
{: tsSymptoms}

Somente os usuários {{site.data.keyword.Bluemix_notm}} a seguir
podem convidar usuários para uma organização:
{: tsCauses}
  * O proprietário da conta da organização
  * Gerenciadores da organização

**Nota:** todos os gerenciadores de organização podem incluir, modificar e remover usuários que já estão na organização.

Se não for possível convidar usuários para sua organização, entre em contato com o gerenciador de organização. Para identificar o gerente da organização, conclua as
etapas a seguir:
{: tsResolve}

  1. Na barra de menus do console, clique em **Gerenciar > Conta > Organizações**.
  2. Acesse sua organização e visualize as informações sobre o gerente da organização na guia **USUÁRIOS**.  

## O registro em lote de usuários não é suportado
{: #ts_batchregistration}

Ao
registrar usuários para {{site.data.keyword.Bluemix_notm}},
deve-se registrar cada usuário individualmente.

O {{site.data.keyword.Bluemix_notm}} não fornece a capacidade para registrar múltiplos usuários ao mesmo tempo.
{: tsSymptoms}

O {{site.data.keyword.Bluemix_notm}} não suporta registro de lote de usuários. Para registrar usuários para o {{site.data.keyword.Bluemix_notm}},
deve-se registrar cada usuário individualmente.
{: tsCauses}

Para registrar múltiplos usuários para o {{site.data.keyword.Bluemix_notm}}, conclua as etapas a seguir para cada usuário:
{: tsResolve}

  1. Clique em **INSCREVER-SE** no console do {{site.data.keyword.Bluemix_notm}}.
  2. Conclua as etapas seguindo o assistente.

## Nenhum espaço está associado com a sua organização atual
{: #ts_no_space}

Não será possível criar um app se não houver espaço associado à sua organização atual.

Ao tentar criar um app no {{site.data.keyword.Bluemix_notm}}, você vê a mensagem de erro a seguir:
{: tsSymptoms}

`BXNUI0097E: Para que seja possível incluir um app, pelo menos um espaço deve estar associado à sua organização e região. No Painel, clique em Criar um espaço. Quando o espaço for criado, tente novamente. `

Os apps no {{site.data.keyword.Bluemix_notm}} devem ser criados em um espaço em sua organização.
{: tsCauses}

Para criar um espaço, use um dos métodos a seguir:
{: tsResolve}

  * Na barra de menus do console, clique em **Gerenciar > Conta > Organizações**. Em seguida, selecione a organização na qual você deseja criar o espaço e clique em **Criar um espaço**.
  * Na interface da linha de comandos cf, digite `cf create-space <space_name> -o <organization_name>`.


## Os apps compartilham o mesmo nome de domínio
{: #ts_domain_diff}

É possível observar que vários apps compartilham a mesma URL no {{site.data.keyword.Bluemix_notm}}.

Esse problema pode ocorrer quando você designa a mesma rota de URL a diferentes apps em um espaço.
{: tsCauses}

Por exemplo, você envia por push o app myApp1 para o {{site.data.keyword.Bluemix_notm}} e configura o domínio como "mynewapp.stage1.mybluemix.net". Em seguida, você envia por push outro app myApp2 para o mesmo espaço e configura uma de suas rotas de URL como "mynewapp.stage1.mybluemix.net". A rota agora é mapeada para ambos os apps.

Esse é o comportamento suportado do {{site.data.keyword.Bluemix_notm}} e é possível usar essa prática para atingir o tempo de inatividade zero para o upgrade de seu app. Para obter mais informações, veja [Usando a implementação blue-green para reduzir o tempo de inatividade e o risco ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://docs.cloudfoundry.org/devguide/deploy-apps/blue-green.html){: new_window}.
{: tsResolve}


## Os administradores não podem visualizar todas as organizações usando a interface com o usuário do {{site.data.keyword.Bluemix_notm}}
{: #ts_ui_org}

Como administrador, quando você utiliza a interface com o usuário do
{{site.data.keyword.Bluemix_notm}}, não é possível exibir cada organização para
administrá-las. Você pode exibir e administrar apenas as organizações às quais pertence.

Como administrador, não é possível ver todas as organizações usando a interface com o usuário do {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Essa é uma limitação da interface com o usuário do {{site.data.keyword.Bluemix_notm}}.
{: tsCauses}

É possível usar comandos, como `cf orgs`, `cf create-org` e `cf delete-org` da interface da linha de comandos cf para gerenciar todas as organizações. Para obter uma lista completa de
comandos cf, insira `cf help`.
{: tsResolve}

## O cartão de crédito não pode ser incluído
{: #ts_addcc}

Não é possível enviar suas informações de cartão de crédito para converter sua conta para teste em uma conta Pré-pago.

O botão **Enviar** na página Incluir cartão de crédito está desativado.
{: tsSymptoms}

Esse problema acontece quando suas informações não são preenchidas corretamente na página Incluir cartão de crédito.
{: tsCauses}


Conclua
as etapas a seguir:
{: tsResolve}

  1. Na página Incluir cartão de crédito, preencha todos os campos obrigatórios nas seções de informações de contato, endereço de contato e endereço para cobrança.
  2. Selecione **Eu li e concordo com os Termos e Condições da IBM**,
em seguida, clique em **Enviar**. A seção **Selecionar um método de pagamento** é exibida.
  3. Insira seu número do cartão de crédito, a data de validade de seu cartão e o código de segurança no cartão. Em seguida, clique em **Enviar**.
