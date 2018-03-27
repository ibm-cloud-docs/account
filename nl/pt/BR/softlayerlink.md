---

copyright:

  years: 2016, 2018

lastupdated: "2018-03-05"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Alternando para o IBMid e vinculando contas
{: #unifyingaccounts}

A autenticação no SoftLayer agora usa o IBMid para fornecer um único login para todos os {{site.data.keyword.Bluemix}}. Um IBMid é um ID único que você usa para efetuar login em sua conta do {{site.data.keyword.Bluemix_notm}} para acessar e comprar infraestrutura, serviços e recursos de aplicativos. Todas as novas contas recebem automaticamente um IBMid e as contas existentes do SoftLayer, exceto contas federadas SAML, são ativadas para alternar para a autenticação do IBMid.
{:shortdesc}

## Alternando para o IBMid
{: #switchtoIBMid}

Ao iniciar o processo para alternar para um IBMid, sempre será possível cancelar antes de concluir o processo. No entanto, sempre que você efetuar login, o prompt para alternar para um IBMid será exibido. Cada conta do SoftLayer que você planejar vincular a uma conta do {{site.data.keyword.Bluemix_notm}} deverá pertencer a um IBMid exclusivo com um endereço de e-mail exclusivo.

Para alternar sua conta existente do SoftLayer para um IBMid, crie um IBMid e, em seguida, use seu código de registro para confirmá-lo.

### Solicitando um IBMid e um código de registro
{: #reqIBMidandregcode}

1. Efetue login na conta do SoftLayer e clique em **OK** quando o prompt para alternar para um IBMid for exibido.

   Se você for um usuário principal e um prompt para alternar para um IBMid não for exibido no portal do cliente da infraestrutura do {{site.data.keyword.BluSoftlayer_full}}, entre em contato com o suporte IBM para obter ajuda. Veja [Suporte IBM](/docs/get-support/howtogetsupport.html#getting-customer-support) para obter mais informações sobre como entrar em contato com o suporte.

   Se anteriormente você tiver efetuado login e tiver clicado em **Posteriormente** no prompt, mas desejar alternar para a autenticação do IBMid na sessão atual, acesse a página Editar perfil do usuário e clique em **Alternar para IBMid**.

2. Siga os prompts do assistente para criar seu IBMid.

   Insira um endereço de e-mail que não esteja atualmente em uso por nenhum IBMid. Esse endereço de e-mail é usado como o nome de usuário para o novo IBMid e é o local para onde seu código de registro é enviado após a criação do IBMid. Será possível atualizar o endereço de e-mail que está associado ao IBMid posteriormente, mas não será possível mudar o nome de usuário.

### Confirmando seu IBMid com o código de registro
{: #confIBMiduseregcode}

1. Ao receber seu código de registro, clique no link no e-mail ou copie a URL em um navegador e insira seu código de registro.

   O código de registro é válido por sete dias e pode ser usado apenas uma vez.

2. Depois de enviar seu código de registro, use seu IBMid para efetuar login no portal do cliente.

   No prompt Login da conta, acesse a seção **Login da conta IBMid** e clique em **Efetuar login com o IBMid**. Não use os campos **Nome do usuário** e **Senha** que foram usados anteriormente com seu ID do SoftLayer.

Se você for um novo cliente, será solicitado seu IBMid existente ou para criar um novo IBMid quando efetuar check-out da ordem.
  * Para usar um IBMid existente, insira o nome do usuário ou o endereço de e-mail do IBMid se ele for exclusivo (isto é, ele não é compartilhado com múltiplos IBMids).
  * Para criar um novo IBMid, insira um endereço de e-mail que não esteja atualmente em uso por nenhum IBMid. Esse endereço de e-mail é o nome de usuário do IBMid e é onde seu código de registro é enviado após a criação do IBMid. Será possível atualizar o endereço de e-mail que está associado ao IBMid posteriormente, mas não será possível mudar o nome de usuário.

Para resolver quaisquer problemas ao efetuar login com seu IBMid, veja [Resolução de problemas para acessar o {{site.data.keyword.Bluemix_notm}}](/docs/troubleshoot/ts_accessing.html#accessing).

## Vinculando as contas de usuário IBMid
{: #link_user_accounts}

Após as suas contas do usuário serem alternadas para a autenticação de IBMid, os revendedores e distribuidores poderão vincular as contas do SoftLayer e as contas do {{site.data.keyword.Bluemix_notm}} para fazer uso de recursos combinados de infraestrutura como serviço (IaaS) e plataforma como serviço (PaaS). Será possível então acessar recursos IaaS do portal do cliente da infraestrutura do {{site.data.keyword.BluSoftlayer_full}} e recursos PaaS do console do {{site.data.keyword.Bluemix_notm}}, todos de um único login. A vinculação de suas contas também fornecerá uma única nota para todos os recursos PaaS e IaaS que você usar.

Para vincular contas, deve-se ser um usuário principal do SoftLayer. O IBMid que é o usuário principal da conta deve ser o proprietário da conta da plataforma {{site.data.keyword.Bluemix_notm}} à qual você está se vinculando. Revise as notas importantes a seguir para vincular contas:

  * O usuário principal da conta do SoftLayer que está sendo vinculada deve ter um IBMid.
  * Cada conta do usuário que você vincula a uma conta do {{site.data.keyword.Bluemix_notm}} deve ser de propriedade de um IBMid exclusivo com um endereço de e-mail exclusivo. Embora um único IBMid possa ter múltiplas contas do SoftLayer, deve-se mudar o usuário principal para ser um IBMid exclusivo para cada conta. Entre em contato com o suporte para mudar o usuário principal de uma conta do SoftLayer. Consulte [Obtendo suporte para a infraestrutura do {{site.data.keyword.Bluemix_notm}}](/docs/customer-portal/cpsupport.html) para obter informações adicionais.
  * Ao incluir novos usuários em uma conta vinculada, deve-se incluí-los na conta do SoftLayer e do {{site.data.keyword.Bluemix_notm}} para que possam acessar todos os recursos do console unificado.
  * Se você tiver uma conta de marca, usar o Brand Agent Portal (BAP) e precisar de suporte ao vincular sua conta, entre em contato com a equipe de Serviços de renda enviando um e-mail para softlayer_revenue_services_team@wwpdl.vnet.ibm.com.
  * Todas as contas vinculadas no {{site.data.keyword.Bluemix_notm}} devem ser contas pré-paga. É possível criar uma nova conta pré-paga, vincular uma conta pré-paga existente ou vincular uma conta para teste existente, que é, então, atualizada para uma conta pré-paga. Não é possível vincular a contas de assinatura do {{site.data.keyword.Bluemix_notm}}.

Conclua as etapas a seguir para vincular cada conta do SoftLayer a uma conta da plataforma {{site.data.keyword.Bluemix_notm}} existente ou para criar uma nova:

   1. Efetue login no portal do cliente da infraestrutura do {{site.data.keyword.BluSoftlayer_full}} com o seu IBMid da conta do usuário principal.
   2. No portal do cliente da infraestrutura do {{site.data.keyword.Bluemix_notm}}, clique em **Vincular uma conta do Bluemix**.
   3. Leia e aceite os termos para vincular contas do SoftLayer e do {{site.data.keyword.Bluemix_notm}}.
   4. Siga os prompts do assistente, incluindo a inclusão de usuários da conta do SoftLayer na conta do {{site.data.keyword.Bluemix_notm}}.
   5. Quando for solicitado, execute uma das ações a seguir:
     * Se você já tiver uma conta do {{site.data.keyword.Bluemix_notm}}, forneça o endereço de e-mail que está associado a essa conta para vincular as contas.
     * Se você não tiver uma conta do {{site.data.keyword.Bluemix_notm}}, forneça o endereço de e-mail que deseja usar e siga as instruções para ser convidado para o {{site.data.keyword.Bluemix_notm}} e criar uma conta.
   6. Depois de vincular a conta, informe ao usuário final de cada conta para migrar para o IBMid seguindo o procedimento descrito na seção [Alternando para o IBMid](/docs/account/softlayerlink.html#switchtoIBMid) anterior.

Migre somente as contas do usuário final para o IBMid. Não migre contas da marca, que são contas pai para contas do usuário final e não contêm recursos. Os usuários de conta da marca que migram para o IBMid perdem a capacidade de efetuar login no Brand Agent Portal (BAP).
{: tip}

As contas vinculadas efetuam login no console do [{{site.data.keyword.Bluemix}} ![Ícone de link externo](../icons/launch-glyph.svg)](https://console.bluemix.net){: new_window}.

Além disso, observe as mudanças a seguir após suas contas serem vinculadas:
  * Deve-se usar as credenciais IBMid para acessar as contas do SoftLayer e do {{site.data.keyword.Bluemix_notm}}.
  * Quaisquer descontos existentes do SoftLayer são aplicados em encargos do {{site.data.keyword.Bluemix_notm}}.
  * Você receberá uma única fatura em dólares dos Estados Unidos (USD). Se você tiver uma conta do {{site.data.keyword.Bluemix_notm}} existente, o faturamento por meio do {{site.data.keyword.Bluemix_notm}} para recursos de infraestrutura entrará em vigor para o novo ciclo de faturamento que se inicia após as contas serem vinculadas.
  * É possível monitorar o uso de seus recursos de infraestrutura no console do {{site.data.keyword.Bluemix_notm}}.

Depois de vincular suas contas, elas não podem ser desvinculadas.
{: tip}

## Uso da autenticação de diversos fatores em contas vinculadas
{: #2fa}

Se você tiver uma conta vinculada, será possível usar a página **Configurações** de Identidade e Acesso para ativar a autenticação de diversos fatores para a sua conta. Isso também é conhecido como autenticação de dois fatores (2FA) e inclui uma camada de segurança para acessar sua conta além do IBMid e senha padrão necessários. A autenticação de diversos fatores para sua conta se aplica a todos os recursos em sua conta vinculada do {{site.data.keyword.Bluemix_notm}}. Quando ela está ativada para sua conta, ela também se aplica a todos os usuários que foram incluídos em sua conta.

A autenticação de diversos fatores não é por IBMid. Ela ainda é por conta. Quando um IBMid está associado a várias contas e você alterna entre elas, é necessário confirmar sua identidade toda vez que você muda para uma conta diferente que requer autenticação de dois fatores. Isso é verdadeiro mesmo se a conta anterior e a nova estão ambas configuradas com o mesmo mecanismo de autenticação de dois fatores.
