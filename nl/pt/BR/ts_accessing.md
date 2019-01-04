---

copyright:

  years: 2015, 2018

lastupdated: "2018-07-09"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Resolução de problemas para acessar o {{site.data.keyword.Bluemix_notm}}
{: #accessing}

Problemas gerais ao acessar o {{site.data.keyword.Bluemix}} podem incluir dificuldades em efetuar login no {{site.data.keyword.Bluemix_notm}} ou em uma conta que está em um estado pendente. Em muitos casos, é possível recuperar-se desses problemas seguindo algumas etapas simples.
{:shortdesc}

## Senha incorreta
{: #ts_logintobm}

Deve-se ter uma senha válida que esteja associada a seu IBMid para efetuar login no console do {{site.data.keyword.Bluemix_notm}}.

Deve-se também ter uma senha válida que esteja associada a seu IBMid ou ID de conta vinculada para efetuar login por meio do [portal do cliente](https://control.softlayer.com).

Ao tentar efetuar login no {{site.data.keyword.Bluemix_notm}}, a mensagem de erro a seguir será exibida:
{: tsSymptoms}

`A senha inserida não está correta.`

A senha que você usou para efetuar login no {{site.data.keyword.Bluemix_notm}} não é válida.
{: tsCauses}

Use uma das soluções a seguir:
{: tsResolve}
 * Digite a senha correta. Para verificar se o seu IBMid e senha são válidos, é possível acessar a página Meu perfil IBM, clicar em Efetuar login e inserir seu IBMid e senha na página Efetuar Login.
 * Caso tenha esquecido sua senha, clique em **Esqueceu sua senha** para reconfigurar sua senha. Em seguida, retorne ao [console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou ao portal do cliente do [](https://control.softlayer.com) e efetue login novamente.
 * Se tiver esquecido o seu IBMid ou continuar tendo problemas com a senha, entre em contato com o IBM Registration Help Desk no mundo todo para obter ajuda.
 * Para obter um IBMid e uma senha válidos, acesse a página Meu perfil IBM e, em seguida, clique em **Registrar**.

**Nota:** se você estiver na página de conexão e o processo de login for interrompido por qualquer razão (por exemplo, a reconfiguração da senha), retorne ao [console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou ao portal do cliente do [](https://control.softlayer.com) e inicie o processo de login novamente.


## Credenciais de login inválidas
{: #ts_login_invalid_credentials}

Ao efetuar login usando seu IBMid, a mensagem a seguir é exibida:
{: tsSymptoms}

`Credenciais de login inválidas fornecidas. Se você tiver um IBMid associado à sua conta, efetue login aqui`

* Você alternou para um IBMid, mas tentou efetuar login por meio do portal do cliente do [](https://control.softlayer.com) usando seu nome de usuário e senha anteriores.
{: tsCauses}

* Você tentou efetuar login por meio do portal do cliente do [](https://control.softlayer.com), mas inseriu seu IBMid e senha nos campos de nome de usuário e senha.

Clique em **efetuar login aqui** na mensagem ou acesse a seção Login da conta IBMid e clique em **Efetuar login com o IBMid**.
{: tsResolve}

Não use os campos **Nome de usuário** e **Senha** que você usou com o seu ID anterior.


## IBMid ou e-mail não reconhecido
{: #ts_old_username}

Ao efetuar login no console do {{site.data.keyword.Bluemix_notm}}, a mensagem a seguir será exibida:
{: tsSymptoms}

`Nós não reconhecemos este IBMid ou e-mail. `

Você tentou efetuar login no console do {{site.data.keyword.Bluemix_notm}}, mas não usou um IBMid válido. Por exemplo, você não inseriu um endereço de e-mail completo para o IBMid ou tentou usar um nome de usuário e senha anteriores.
{: tsCauses}

Deve-se ter um ID IBM e uma senha válidos para efetuar login no
{{site.data.keyword.Bluemix_notm}}.

 * Assegure-se de inserir um endereço de e-mail completo para o IBMid.
 {: tsResolve}
 * Se você é um usuário do SoftLayer com um ID do SoftLayer, deve alternar para a autenticação do IBMid no portal do cliente em cada conta à qual você tem acesso antes de poder efetuar login usando a autenticação do IBMid.
 Para obter mais informações, consulte [Alternando para o IBMid](/docs/account/softlayerlink.html).


## O IBMid não está associado a nenhuma conta do IBM Cloud
{: #ts_login_noswitch}

Ao efetuar login usando seu IBMid, a mensagem a seguir é exibida:
{: tsSymptoms}

`You have reached this page because your authentication was successful, however, this IBMid is not associated with any IBM Cloud accounts. If you believe this to be in error, contact your Account Owner or Master User.`

Você efetuou login por meio do [portal do cliente](https://control.softlayer.com) com um IBMid válido, mas não foi alternado para a autenticação do IBMid por meio do portal do cliente.
{: tsCauses}

Conclua as verificações a seguir:
{: tsResolve}
 * Entre em contato com o usuário principal ou com o administrador da conta para verificar se você está ativado para alternar para a autenticação do IBMid.
 * Assegure-se de que você conclua a etapa Alternar para o IBMid. Consulte [Alternando para o IBMid](/docs/account/softlayerlink.html).
 * Assegure-se de que você siga as ações no e-mail **Associar seu ID do usuário a um IBMid**. Verifique sua caixa de entrada e sua pasta de lixo eletrônico para o e-mail. Para obter o e-mail novamente, por exemplo, se ele tiver expirado, acesse a página Editar perfil do usuário no portal do cliente e clique em **Reenviar e-mail**. Como alternativa, entre em contato com o [Suporte do {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://ibm.biz/bluemixsupport.com){: new_window}.

Dependendo de como a sua conta é configurada, algumas opções de login podem se aplicar:
 * Os usuários do SoftLayer com IDs do SoftLayer devem efetuar login por meio do [portal do cliente](https://control.softlayer.com).
 * Os usuários do SoftLayer com um IBMid, com ou sem uma conta vinculada do {{site.data.keyword.Bluemix_notm}}, podem efetuar login por meio do [portal do cliente](https://control.softlayer.com) para abrir o portal do cliente ou por meio do [console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) para abrir o painel Infraestrutura.


## O IBMid não está associado a nenhuma conta do {{site.data.keyword.Bluemix_notm}}
{: #ts_unabletologin}

Ao efetuar login no {{site.data.keyword.Bluemix_notm}}, a mensagem a seguir é exibida:
{: tsSymptoms}

`You have reached this page because your authentication was successful, however, this IBMid is not associated with any  {{site.data.keyword.Bluemix_notm}} accounts.`

Você efetuou login por meio do [console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) com um IBMid válido, mas ainda não tem uma conta do {{site.data.keyword.Bluemix_notm}} criada.
{: tsCauses}

Para criar uma conta do {{site.data.keyword.Bluemix_notm}}, siga o processo de inscrição.
{: tsResolve}

Dependendo de como a sua conta é configurada, algumas opções de login podem se aplicar:
 * Os usuários do {{site.data.keyword.Bluemix_notm}} sem uma conta vinculada devem efetuar login por meio do console do {{site.data.keyword.Bluemix_notm}}.
 * Os usuários do {{site.data.keyword.Bluemix_notm}} com uma conta vinculada podem efetuar login por meio do [console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou do [portal do cliente](https://control.softlayer.com).


## O console não se abre
{: #ts_login_stalls}

Ao efetuar login usando seu IBMid, uma mensagem de êxito de login é exibida, mas você não é retornado para o [console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou para o [portal do cliente](https://control.softlayer.com)
{: tsSymptoms}

Use uma das soluções a seguir:
{: tsResolve}
 * Feche seu navegador, limpe o cache e os cookies e, em seguida, tente efetuar login novamente.
 * Assegure-se de efetuar login por meio do [console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou do [portal do cliente](https://control.softlayer.com), em vez de diretamente do serviço de autenticação do IBMid.


## O login do IBMid não é concluído
{: #ts_login_ibmid}

Ao efetuar login no {{site.data.keyword.Bluemix_notm}}, a autenticação com o IBMid não é concluída.
{: tsSymptoms}

Pode haver um problema com o serviço de autenticação do IBMid.
{: tsCauses}

Verifique se é possível efetuar login na [página inicial da IBM ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/us-en/){: new_window}. Se você puder, será um problema de aplicativo e será possível tentar novamente depois. Se não for possível efetuar login nessa página, entre em contato com o [Help Desk ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}.
{: tsResolve}


## A conta está pendente
{: #ts_accntpding}

Se a sua conta estiver pendente, não será possível efetuar login no {{site.data.keyword.Bluemix_notm}}.

Depois de se registrar para uma conta {{site.data.keyword.Bluemix_notm}} Lite, talvez você não consiga efetuar login no {{site.data.keyword.Bluemix_notm}}. É exibida a seguinte mensagem:
{: tsSymptoms}

<code>Sua conta está pendente. Aguarde até 24 horas pela confirmação por email e verifique também sua pasta de spam. Se você ainda não recebeu sua confirmação por e-mail, entre em contato com o <a href="http://ibm.biz/bluemixsupport.com" target="_blank">Suporte do {{site.data.keyword.Bluemix_notm}}</a>.</code>

Depois de se registrar para uma conta {{site.data.keyword.Bluemix_notm}} Lite, você recebe um e-mail de confirmação. Deve-se clicar no link
que está no email de confirmação para concluir o processo de registro.
{: tsCauses}

O email de confirmação é enviado ao endereço de email fornecido. Verifique sua caixa de entrada e sua pasta de spam. Se você não recebeu o e-mail de confirmação, entre em contato com o suporte do [{{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://ibm.biz/bluemixsupport.com){: new_window}.  
{: tsResolve}

## A página do {{site.data.keyword.Bluemix_notm}} não pode ser carregada
{: #ts_err}

Ao usar o console do {{site.data.keyword.Bluemix_notm}}, você pode não ser capaz de carregar uma página do console. Em vez disso, talvez você consulte as mensagens de erro BXNUI0001E ou BXNUI0016E.

É possível ver uma das mensagens de erro a seguir ao usar o console do {{site.data.keyword.Bluemix_notm}}:
{: tsSymptoms}

`BXNUI0001E: The page wasn't loaded because {{site.data.keyword.Bluemix_notm}} didn't detect whether a session exists.`

`BXNUI0016E: The apps and services weren't retrieved because an {{site.data.keyword.Bluemix_notm}} page didn't load.`

Conclua uma ou mais das ações a seguir, conforme necessário:
{: tsResolve}

  * Atualizar ou reiniciar seu navegador.
  * Efetuar logout do {{site.data.keyword.Bluemix_notm}} e
efetuar login novamente.
  * Usar o modo de navegação privada do seu navegador.
  * Limpar os cookies e o cache do navegador.
  * Usar um navegador diferente. Para obter informações sobre as versões dos navegadores que são suportados pelo {{site.data.keyword.Bluemix_notm}}, consulte [Pré-requisitos do {{site.data.keyword.Bluemix_notm}}](/docs/overview/prereqs.html#prereqs).
  * Se você instalou a interface da linha de comandos do Cloud Foundry, insira o comando `cf apps` para ver se seu app está em execução.
