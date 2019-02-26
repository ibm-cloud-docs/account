---

copyright:

  years: 2016, 2019

lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Alternando para o IBMid e vinculando contas
{: #unifyingaccounts}

Um IBMid é um ID único que você usa para efetuar login em sua conta do {{site.data.keyword.Bluemix}} para acessar e comprar recursos de infraestrutura, serviços e aplicativos. Todas as novas contas recebem automaticamente um IBMid e as contas existentes do SoftLayer, exceto contas federadas SAML, são ativadas para alternar para a autenticação do IBMid.
{:shortdesc}

## Alternando para o IBMid
{: #switchtoIBMid}

Ao iniciar o processo para alternar para um IBMid, sempre será possível cancelar antes de concluir o processo. No entanto, sempre que você efetuar login, o prompt para alternar para um IBMid será exibido. Cada conta do SoftLayer que você planeja vincular a uma conta do {{site.data.keyword.Bluemix_notm}} deve ser de propriedade de um IBMid exclusivo com um endereço de e-mail exclusivo.

Para alternar sua conta existente do SoftLayer para um IBMid, crie um IBMid e, em seguida, use seu código de registro para confirmá-lo.

### Solicitando um IBMid e um código de registro
{: #reqIBMidandregcode}

1. Efetue login na conta do SoftLayer e clique em **OK** quando o prompt para alternar para um IBMid for exibido.

   Se você for um usuário principal e um prompt para alternar para um IBMid não for exibido no portal do cliente, entre em contato com o suporte IBM para obter ajuda. Veja [Obtendo suporte](/docs/get-support?topic=get-support-getting-customer-support) para obter mais informações sobre como entrar em contato com o suporte.

   Se anteriormente você tiver efetuado login e tiver clicado em **Posteriormente** no prompt, mas desejar alternar para a autenticação do IBMid na sessão atual, acesse a página Editar perfil do usuário e clique em **Alternar para IBMid**.

2. Siga os prompts do assistente para criar seu IBMid.

   Insira um endereço de e-mail que não esteja atualmente em uso por nenhum IBMid. Esse endereço de e-mail é usado como o nome de usuário para o novo IBMid e é o local para onde seu código de registro é enviado após a criação do IBMid. Será possível atualizar o endereço de e-mail que está associado ao IBMid posteriormente, mas não será possível mudar o nome de usuário.

### Confirmando seu IBMid com o código de registro
{: #confIBMiduseregcode}

1. Ao receber seu código de registro, clique no link no e-mail ou copie a URL em um navegador e insira seu código de registro. O código de registro é válido por sete dias e pode ser usado apenas uma vez.

2. Depois de enviar seu código de registro, use seu IBMid para efetuar login no portal do cliente.

   No prompt Login da conta, acesse a seção **Login da conta IBMid** e clique em **Efetuar login com o IBMid**. Não use os campos **Nome do usuário** e **Senha** que foram usados anteriormente com seu ID do SoftLayer.

Se você for um novo cliente, será solicitado seu IBMid existente ou para criar um novo IBMid quando efetuar check-out da ordem.
  * Para usar um IBMid existente, insira o nome do usuário ou o endereço de e-mail do IBMid, se ele não for compartilhado entre múltiplos IBMids.
  * Para criar um novo IBMid, insira um endereço de e-mail que não esteja atualmente em uso por nenhum IBMid. Esse endereço de e-mail é o nome de usuário do IBMid e é onde seu código de registro é enviado após a criação do IBMid. Será possível atualizar o endereço de e-mail que está associado ao IBMid posteriormente, mas não será possível mudar o nome de usuário.

Para resolver quaisquer problemas ao efetuar login com seu IBMid, consulte [Resolução de problemas para acessar o {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-accessing).


## Vinculando contas do IBMid
{: #link_accounts}

Depois que as contas são alternadas para as contas do IBMid, é possível vincular contas do SoftLayer e
contas do {{site.data.keyword.Bluemix_notm}} para usar uma combinação de recursos de infraestrutura como
serviço (IaaS) e de plataforma como serviço (PaaS). Em seguida, é possível acessar recursos de IaaS e
de PaaS por meio de um login único. A vinculação de suas contas também fornecerá uma única nota para todos os recursos PaaS e IaaS que você usar. É possível vincular sua própria conta ou, caso você seja um usuário principal, vincular sua conta
do usuário.

### Vinculando suas contas do IBMid
{: #link_user_account}

Se você for um cliente de infraestrutura clássica e também tiver contas PaaS no {{site.data.keyword.Bluemix_notm}} ou criá-las, será possível vincular o IaaS e o PaaS para uma única visualização de suas contas. Para vincular suas contas, use as etapas a seguir:
1. Efetue login em sua conta do SoftLayer.
2. Na página Resumo da conta, clique em **Novo! Vincular uma conta do Bluemix**.
3. Revise os termos de uso e clique para reconhecer sua aceitação.
4. Conclua uma das etapas finais a seguir, dependendo de como sua conta foi configurada:
  * Se o seu IBMid tiver uma conta do {{site.data.keyword.Bluemix_notm}} associada, você será
direcionado para uma página de autorização, em seguida, para a etapa de confirmação final novamente.
  * Se você não tiver uma conta do {{site.data.keyword.Bluemix_notm}} associada, será
solicitado a criar uma nova conta.

Para ver perguntas e respostas comuns sobre como vincular sua conta, consulte as
[Perguntas frequentes](/docs/account?topic=account-al_login).

### Vinculando contas do usuário IBMid
{: #link_customer_accounts}

Depois de alternar contas do usuário para autenticação do IBMid, os revendedores e distribuidores podem
vincular suas contas do usuário. Para vincular contas do cliente, deve-se ser um usuário principal do
SoftLayer. O IBMid que é o usuário principal da conta deve ser o proprietário da conta da plataforma {{site.data.keyword.Bluemix_notm}} à qual você está se vinculando.

Depois de vincular as contas, elas não poderão ser desvinculadas.
{: note}

Certifique-se de revisar as notas importantes a seguir sobre vinculação de contas:

  * O usuário principal da conta do SoftLayer que está sendo vinculada deve ter um IBMid.
  * Cada conta do usuário que você vincula a uma conta do {{site.data.keyword.Bluemix_notm}} deve ser de propriedade de um IBMid exclusivo com um endereço de e-mail exclusivo. Embora um único IBMid possa ter múltiplas contas do SoftLayer, deve-se mudar o usuário principal para ser um IBMid exclusivo para cada conta. Entre em contato com o suporte para mudar o usuário principal de uma conta do SoftLayer. Consulte [Obtendo suporte para a infraestrutura do {{site.data.keyword.Bluemix_notm}}](/docs/customer-portal?topic=customer-portal-customerportal_support) para obter mais informações.
  * Ao incluir novos usuários em uma conta vinculada, deve-se incluí-los na conta do SoftLayer e do {{site.data.keyword.Bluemix_notm}} para que possam acessar todos os recursos do console unificado.
  * Se você tiver uma conta de marca, usar o Brand Agent Portal (BAP) e precisar de suporte ao vincular sua conta, entre em contato com a equipe de Serviços de renda enviando um e-mail para softlayer_revenue_services_team@wwpdl.vnet.ibm.com.

Conclua as etapas a seguir para vincular cada conta do SoftLayer a uma conta da plataforma {{site.data.keyword.Bluemix_notm}} existente ou para criar uma nova:

   1. Efetue login no portal do cliente com seu IBMid da conta do usuário principal.
   2. No portal do cliente, clique em **Vincular uma conta do Bluemix**.
   3. Leia e aceite os termos para vincular contas do SoftLayer e do {{site.data.keyword.Bluemix_notm}}.
   4. Siga os prompts do assistente, incluindo a inclusão de usuários da conta do SoftLayer na conta do {{site.data.keyword.Bluemix_notm}}.
   5. Quando for solicitado, execute uma das ações a seguir:
     * Se você já tiver uma conta do {{site.data.keyword.Bluemix_notm}}, forneça o endereço de e-mail que está associado a essa conta para vincular as contas.
     * Se você não tiver uma conta do {{site.data.keyword.Bluemix_notm}}, forneça o endereço de e-mail que deseja usar e siga as instruções para ser convidado para o {{site.data.keyword.Bluemix_notm}} e criar uma conta.
   6. Depois de vincular a conta, informe ao usuário final de cada conta para migrar para o IBMid seguindo o procedimento descrito na seção [Alternando para o IBMid](#switchtoIBMid) anterior.

      Migre somente as contas do usuário final para o IBMid. Não migre contas da marca, que são contas pai para contas do usuário final e não contêm recursos. Os usuários de conta da marca que migram para o IBMid perdem a capacidade de efetuar login no Brand Agent Portal (BAP).
      {: important}

Anote as mudanças a seguir depois que suas contas estiverem vinculadas:

  * Agora você efetua login no [console do {{site.data.keyword.Bluemix}} ![Ícone de link externo](../icons/launch-glyph.svg)](https://cloud.ibm.com){: new_window}.
  * Deve-se usar as credenciais IBMid para acessar as contas do SoftLayer e do {{site.data.keyword.Bluemix_notm}}.
  * Quaisquer descontos existentes do SoftLayer são aplicados em encargos do {{site.data.keyword.Bluemix_notm}}.
  * Você recebe uma fatura em dólares americanos (USD). Se você tiver uma conta do {{site.data.keyword.Bluemix_notm}} existente, o faturamento por meio do {{site.data.keyword.Bluemix_notm}} para recursos de infraestrutura entrará em vigor para o novo ciclo de faturamento que se inicia após as contas serem vinculadas. Para obter mais informações, consulte [Faturamento consolidado para contas vinculadas](/docs/customer-portal?topic=customer-portal-unifybillaccounts).
  * É possível monitorar o uso de seus recursos de infraestrutura clássica no console do {{site.data.keyword.Bluemix_notm}}.

## Uso da autenticação de diversos fatores em contas vinculadas
{: #2fa}

Se você tiver uma conta vinculada, será possível usar a página **Configurações** do {{site.data.keyword.Bluemix_notm}} IAM para ativar a autenticação de diversos fatores (MFA) para sua conta. Isso também é conhecido como autenticação de dois fatores (2FA) e inclui uma camada de segurança para acessar sua conta além do IBMid e senha padrão necessários. A MFA para sua conta se aplica a todos os recursos em sua conta vinculada do {{site.data.keyword.Bluemix_notm}}. Quando ela está ativada para sua conta, ela também se aplica a todos os usuários que foram incluídos em sua conta.

Outros métodos de autenticação de diversos fatores não são por IBMid. Ela é por conta. Quando um IBMid está associado a várias contas e você alterna entre elas, é necessário confirmar sua identidade toda vez que você muda para uma conta diferente que requer autenticação de dois fatores. Isso é verdadeiro mesmo se a conta anterior e a nova estão ambas configuradas com o mesmo mecanismo de autenticação de dois fatores.

Se você ativou anteriormente a [2FA no portal do cliente](/docs/customer-portal?topic=customer-portal-customerportal_2fa) para seus recursos de infraestrutura clássica e, em seguida, ativar a configuração MFA da conta do {{site.data.keyword.Bluemix_notm}}, a configuração da conta MFA substituirá a 2FA que foi configurada no portal do cliente. Isso significa que é possível desativar a 2FA que você comprou no portal do cliente em favor da configuração MFA da conta.
