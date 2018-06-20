---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-02"

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

Deve-se ter uma senha válida que esteja associada a seu IBMid ou ID da conta vinculada ao efetuar login por meio do [{{site.data.keyword.slportal}}](https://control.softlayer.com).

Ao tentar efetuar login no {{site.data.keyword.Bluemix_notm}}, a mensagem de erro a seguir será exibida:
{: tsSymptoms}

`A senha inserida não está correta.`

A senha que você usou para efetuar login no {{site.data.keyword.Bluemix_notm}} não é válida.
{: tsCauses}

Use uma das soluções a seguir:
{: tsResolve}
 * Digite a senha correta. Para verificar se seu IBMid e senha são válidos, é possível acessar a página Meu perfil IBM, clicar em **Efetuar login** e inserir seu IBMid e senha na página Efetuar login.
 * Caso tenha esquecido sua senha, clique em **Esqueceu sua senha** para reconfigurar sua senha. Em seguida, retorne ao [Console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou ao [{{site.data.keyword.slportal}}](https://control.softlayer.com) e efetue login novamente.
 * Caso tenha esquecido seu IBMid ou continue tendo problemas com a senha, entre em contato com o Help desk de registro IBM mundial para obter ajuda.
 * Para obter um IBMid e uma senha válidos, acesse a página Meu perfil IBM e, em seguida, clique em **Registrar**.

**Nota:** se você estiver na página Conectar à IBM e o processo de login for interrompido por algum motivo (por exemplo, reconfigurando sua senha), retorne para o [Console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou para o [{{site.data.keyword.slportal}}](https://control.softlayer.com) e inicie o processo de login novamente.


## Credenciais de login inválidas
{: #ts_login_invalid_credentials}

Ao efetuar login usando seu IBMid, a mensagem a seguir é exibida:
{: tsSymptoms}

`Credenciais de login inválidas fornecidas. Se você tiver um IBMid associado à sua conta, efetue login aqui`

* Você alternou para um IBMid, mas tentou efetuar login por meio do [{{site.data.keyword.slportal}}](https://control.softlayer.com) usando seu nome do usuário e senha anteriores.
{: tsCauses}

* Você tentou efetuar login por meio do [{{site.data.keyword.slportal}}](https://control.softlayer.com), mas inseriu seu IBMid e senha nos campos Nome do usuário e Senha.

Clique em **efetuar login aqui** na mensagem ou acesse a seção Login da conta IBMid e clique em **Efetuar login com o IBMid**.
{: tsResolve}

Não use os campos **Nome do usuário** e **Senha** que você usou com seu ID anterior.


## IBMid ou e-mail não reconhecido
{: #ts_old_username}

Ao efetuar login no console do {{site.data.keyword.Bluemix_notm}}, a mensagem a seguir será exibida:
{: tsSymptoms}

`Nós não reconhecemos este IBMid ou e-mail. `

Você tentou efetuar login no console do {{site.data.keyword.Bluemix_notm}}, mas não usou um IBMid válido. Por exemplo, você não inseriu um endereço de e-mail completo para o IBMid ou tentou usar um nome do usuário e senha anteriores.
{: tsCauses}

Deve-se ter um ID IBM e uma senha válidos para efetuar login no
{{site.data.keyword.Bluemix_notm}}.

 * Assegure-se de inserir um endereço de e-mail completo para o IBMid.
 {: tsResolve}
 * Se você é um usuário do {{site.data.keyword.BluSoftlayer_full}} com um ID do {{site.data.keyword.BluSoftlayer_full}}, deve-se alternar para a autenticação do IBMid no {{site.data.keyword.slportal}} em cada conta à qual você tenha acesso antes de efetuar login usando a autenticação do IBMid.
 Para obter mais informações, veja [Alternando para o IBMid](/docs/account/softlayerlink.html).


## O IBMid não está associado a nenhuma conta do IBM Cloud
{: #ts_login_noswitch}

Ao efetuar login usando seu IBMid, a mensagem a seguir é exibida:
{: tsSymptoms}

`You have reached this page because your authentication was successful, however, this IBMid is not associated with any IBM Cloud accounts. If you believe this to be in error, contact your Account Owner or Master User.`

Você efetuou login no [{{site.data.keyword.slportal}}](https://control.softlayer.com) com um IBMid válido, mas não alternou para a autenticação do IBMid do {{site.data.keyword.slportal}}.
{: tsCauses}

Conclua as verificações a seguir, conforme apropriado:
{: tsResolve}
 * Entre em contato com o usuário principal ou com o administrador da conta para verificar se você está ativado para alternar para a autenticação do IBMid.
 * Assegure-se de que você conclua a etapa Alternar para o IBMid. Veja [Alternando para o IBMid](/docs/account/softlayerlink.html).
 * Assegure-se de que você siga as ações no e-mail **Associar seu ID do usuário a um IBMid**. Verifique sua caixa de entrada e sua pasta de lixo eletrônico para o e-mail. Para obter o e-mail novamente, por exemplo, se ele tiver expirado, acesse a página Editar perfil do usuário no {{site.data.keyword.slportal}} e clique em **Reenviar e-mail**. Como alternativa, entre em contato com o [Suporte do {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://ibm.biz/bluemixsupport.com){: new_window}.

**Nota:** se você criou seu IBMid diretamente com o IBMid, receberá dois e-mails para processar; um do registro do IBMid e um do {{site.data.keyword.Blu_full}}. Assegure-se de seguir as ações dos dois e-mails.

Dependendo de como sua conta foi configurada, algumas dessas opções de login podem se aplicar a você:
 * Os usuários do {{site.data.keyword.BluSoftlayer_notm}} com IDs do {{site.data.keyword.BluSoftlayer_full}} devem efetuar login por meio do [{{site.data.keyword.slportal}}](https://control.softlayer.com).
 * Os usuários do {{site.data.keyword.BluSoftlayer_notm}} com um IBMid e com ou sem uma conta do {{site.data.keyword.Bluemix_notm}} vinculada podem efetuar login por meio do [{{site.data.keyword.slportal}}](https://control.softlayer.com) para abrir o {{site.data.keyword.slportal}} ou por meio do [Console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) para abrir o painel de Infraestrutura.


## O IBMid não está associado a nenhuma conta do {{site.data.keyword.Bluemix_notm}}
{: #ts_unabletologin}

Ao efetuar login no {{site.data.keyword.Bluemix_notm}}, a mensagem a seguir é exibida:
{: tsSymptoms}

`You have reached this page because your authentication was successful, however, this IBMid is not associated with any  {{site.data.keyword.Bluemix_notm}} accounts.`

Você efetuou login por meio do [Console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) com um IBMid válido, mas não tem uma conta do {{site.data.keyword.Bluemix_notm}} criada ainda.
{: tsCauses}

Para criar uma conta do {{site.data.keyword.Bluemix_notm}}, siga o processo de inscrição.
{: tsResolve}

Dependendo de como sua conta foi configurada, algumas dessas opções de login podem se aplicar a você:
 * Os usuários do {{site.data.keyword.Bluemix_notm}} sem uma conta vinculada devem efetuar login por meio do console do {{site.data.keyword.Bluemix_notm}}.
 * Os usuários do {{site.data.keyword.Bluemix_notm}} com uma conta vinculada podem efetuar login por meio do [Console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou do [{{site.data.keyword.slportal}}](https://control.softlayer.com).


## O console não se abre
{: #ts_login_stalls}

Ao efetuar login usando seu IBMid, uma mensagem de êxito de login é exibida, mas você não retorna ao [Console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou ao [{{site.data.keyword.slportal}}](https://control.softlayer.com)
{: tsSymptoms}

Use uma das soluções a seguir:
{: tsResolve}
 * Feche seu navegador, limpe o cache e os cookies e, em seguida, tente efetuar login novamente.
 * Assegure-se de efetuar login por meio do [Console do {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou do [{{site.data.keyword.slportal}}](https://control.softlayer.com), em vez de diretamente do serviço de autenticação do IBMid.


## O login do IBMid não é concluído
{: #ts_login_ibmid}

Ao efetuar login no {{site.data.keyword.Bluemix_notm}}, a autenticação com o IBMid não é concluída.
{: tsSymptoms}

Pode haver um problema com o serviço de autenticação do IBMid.
{: tsCauses}

Verifique o status do serviço em [IBMid da IBM ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://status.ibm.com/wind){: new_window} e, em seguida, tente novamente.
{: tsResolve}


## A conta está pendente
{: #ts_accntpding}

Se a sua conta estiver pendente, não será possível efetuar login no {{site.data.keyword.Bluemix_notm}}.

Depois de registrar-se em uma conta para teste do {{site.data.keyword.Bluemix_notm}}, você pode não ser capaz de efetuar login no {{site.data.keyword.Bluemix_notm}}. É exibida a seguinte mensagem:
{: tsSymptoms}

<code>Sua conta está pendente. Aguarde até 24 horas pela confirmação por e-mail e verifique também sua pasta de spam. Se você ainda não recebeu sua confirmação por e-mail, entre em contato com o <a href="http://ibm.biz/bluemixsupport.com" target="_blank">Suporte do {{site.data.keyword.Bluemix_notm}}</a>.</code>

Depois de registrar-se em uma conta para teste do {{site.data.keyword.Bluemix_notm}}, você recebe um e-mail de confirmação. Deve-se clicar no link
que está no e-mail de confirmação para concluir o processo de registro.
{: tsCauses}

O e-mail de confirmação é enviado ao endereço de e-mail fornecido. Verifique sua caixa de entrada e sua pasta de spam. Se você não tiver recebido o e-mail de confirmação, entre em contato com o [Suporte do {{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](http://ibm.biz/bluemixsupport.com){: new_window}.  
{: tsResolve}

## A página do {{site.data.keyword.Bluemix_notm}} não pode ser carregada
{: #ts_err}

Ao usar o console do {{site.data.keyword.Bluemix_notm}}, você pode não ser capaz de carregar uma página do console. Em vez disso, talvez você veja as mensagens de erro BXNUI0001E ou BXNUI0016E.

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
  * Usar um navegador diferente. Para obter informações sobre as versões dos navegadores que são suportados pelo {{site.data.keyword.Bluemix_notm}}, veja [Pré-requisitos do {{site.data.keyword.Bluemix_notm}}](/docs/overview/prereqs.html#prereqs).
  * Se você tiver instalado a interface de linha de comandos cf, insira o comando `cf apps` para ver se seu app está em execução.
