---

copyright:
  years: 2015, 2019
lastupdated: "2019-08-06"

keywords: troubleshoot account, account problem, account support, account help, account error, access error, login error, error message

subcollection: account

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


# Resolução de problemas para acessar o {{site.data.keyword.Bluemix_notm}}
{: #accessing}

Problemas gerais ao acessar o {{site.data.keyword.Bluemix}} podem incluir dificuldades em efetuar login no {{site.data.keyword.Bluemix_notm}} ou em uma conta que está em um estado pendente. Em muitos casos, é possível recuperar-se desses problemas seguindo algumas etapas simples.
{:shortdesc}


## Por que a minha senha está incorreta?
{: #ts_logintobm}
{: troubleshoot}

Deve-se ter uma senha válida que esteja associada a seu IBMid ou ID do SoftLayer para efetuar login no console do {{site.data.keyword.Bluemix_notm}}.

Ao tentar efetuar login no {{site.data.keyword.Bluemix_notm}}, a mensagem de erro a seguir será exibida:
{: tsSymptoms}

`A senha inserida não está correta.`

A senha que você usou para efetuar login no {{site.data.keyword.Bluemix_notm}} não é válida.
{: tsCauses}

Use uma das opções a seguir:
{: tsResolve}
 * Acesse a [página Meu perfil IBM ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://myibm.ibm.com/dashboard/){: new_window} para confirmar que você está usando uma senha válida.
 * Caso tenha esquecido sua senha, clique em **Esqueceu sua senha** para reconfigurar sua senha.
 * Caso tenha esquecido seu IBMid ou continue tendo problemas com a senha, entre em contato com o Help desk de registro IBM mundial para obter ajuda.

Se você se conectar ao {{site.data.keyword.Bluemix_notm}} e o processo de login for interrompido por qualquer motivo, como reconfiguração de sua senha, retorne para o console e inicie o processo de login novamente.
{: tip}


## Por que meu IBMid ou e-mail não foi reconhecido?
{: #ts_old_username}
{: troubleshoot}

Para efetuar login com sucesso no console do {{site.data.keyword.Bluemix_notm}}, certifique-se de ter a autenticação do IBMid para cada conta.

Ao efetuar login no console, a mensagem a seguir será exibida:
{: tsSymptoms}

`Nós não reconhecemos este IBMid ou e-mail. `

Você tentou efetuar login no console, mas não usou um IBMid válido. Por exemplo, você não digitou um endereço de e-mail completo qualificado para o IBMid ou tentou usar um nome de usuário e senha anteriores.
{: tsCauses}

Deve-se ter um ID IBM e uma senha válidos para efetuar login no
{{site.data.keyword.Bluemix_notm}}.

 * Insira um endereço de e-mail completo para o IBMid.
 {: tsResolve}
 * Se você é um usuário do SoftLayer com um ID do SoftLayer, deve-se alternar para a autenticação do IBMid em cada conta para a qual tenha acesso antes de efetuar login. Para obter mais informações, consulte [Alternando para o IBMid](/docs/account?topic=account-unifyingaccounts).


## Por que meu IBMid não está associado a nenhuma conta do {{site.data.keyword.Bluemix_notm}}?
{: #ts_unabletologin}
{: troubleshoot}

Ao efetuar login no {{site.data.keyword.Bluemix_notm}}, a mensagem a seguir é exibida:
{: tsSymptoms}

`You have reached this page because your authentication was successful, however, this IBMid is not associated with any  {{site.data.keyword.Bluemix_notm}} accounts.`

Você efetuou login por meio do [console do {{site.data.keyword.Bluemix_notm}}](https://{DomainName}){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo") com um IBMid válido, mas não tem uma conta do {{site.data.keyword.Bluemix_notm}} criada.
{: tsCauses}

Para criar uma conta do {{site.data.keyword.Bluemix_notm}}, siga o processo de inscrição.
{: tsResolve}


## Por que o console não se abre quando eu efetuo login com meu IBMid?
{: #ts_login_stalls}
{: troubleshoot}

Quando você efetua login usando seu IBMid, uma mensagem de êxito de login é exibida, mas você não retorna ao console do {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Use uma das opções a seguir:
{: tsResolve}
 * Feche seu navegador, limpe o cache e os cookies e, em seguida, tente efetuar login novamente.
 * Efetue login por meio do [console do {{site.data.keyword.Bluemix_notm}}](https://{DomainName}){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo").


## Por que meu login do IBMid não foi concluído?
{: #ts_login_ibmid}
{: troubleshoot}

Se você efetuar login no {{site.data.keyword.Bluemix_notm}} e a autenticação de seu IBMid não for concluída, talvez haja um problema com o serviço.

Ao efetuar login no {{site.data.keyword.Bluemix_notm}}, a autenticação com o IBMid não é concluída.
{: tsSymptoms}

Pode haver um problema com o serviço de autenticação do IBMid.
{: tsCauses}

Certifique-se de que seja possível efetuar login na [IBM](https://idaas.iam.ibm.com/idaas/mtfim/sps/authsvc?PolicyId=urn:ibm:security:authentication:asf:basicldapuser){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo"). Se for possível, será um problema de aplicativo e será possível tentar efetuar login no console novamente mais tarde. Se não for possível efetuar login nessa página, entre em contato com o [help desk do IBMid ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}.  
{: tsResolve}


## Por que não posso efetuar login imediatamente depois de registrar uma conta?
{: #ts_accntpding}
{: troubleshoot}

Se a sua conta ainda estiver pendente, não será possível efetuar login no {{site.data.keyword.Bluemix_notm}}.

Depois de registrar-se para uma conta do {{site.data.keyword.Bluemix_notm}}, talvez
você não consiga efetuar login no {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Ao registrar-se para uma conta do {{site.data.keyword.Bluemix_notm}}, você receberá
um e-mail que inclui um link de confirmação. Deve-se clicar nesse link para confirmar seu registro. Se
você não confirmar seu registro, sua conta permanecerá em um estado pendente.
{: tsCauses}

O e-mail de confirmação é enviado para o endereço de e-mail que está associado a seu IBMid. Verifique sua caixa de entrada e sua pasta de spam. Se você não tiver recebido o e-mail de confirmação, acesse a [página de login do {{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com/){: new_window}![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo") e tente efetuar login. É exibida a seguinte mensagem:
{: tsResolve}

```
Para concluir seu registro, verifique seu e-mail.
Não consegue localizar o e-mail? Reenviar.
```
{:screen}

Clique em **Reenviar** para enviar outro e-mail de confirmação para o endereço de e-mail que está associado a seu IBMid. Se você ainda não conseguir concluir seu registro, entre em contato com o [Suporte do {{site.data.keyword.Bluemix_notm}}](/docs/get-support?topic=get-support-getting-customer-support).  

## Por que eu encontro páginas do console que não são carregadas?
{: #ts_err}
{: troubleshoot}

Ao usar o console do {{site.data.keyword.Bluemix_notm}}, você pode não ser capaz de carregar uma página do console. Em vez disso, as mensagens de erro BXNUI0001E ou BXNUI0016E podem ser exibidas.

Uma das mensagens de erro a seguir pode ser exibida:
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
  * Usar um navegador diferente. Para obter informações sobre as versões dos navegadores suportados pelo {{site.data.keyword.Bluemix_notm}}, consulte [Pré-requisitos do {{site.data.keyword.Bluemix_notm}}](/docs/overview?topic=overview-prereqs-platform).
  * Se você instalou a interface da linha de comandos do Cloud Foundry, insira o comando `ibmcloud cf apps` para ver se seu app está em execução.

## Como posso acessar serviços de infraestrutura em minha conta?
{: #troubleshoot-infrastructure-access}
{: troubleshoot}

Quando você tenta acessar seções de infraestrutura do console do IBM Cloud, a mensagem a seguir pode ser exibida:
{: tsSymptoms}

`Esta página não pode ser carregada porque sua conta de infraestrutura não está totalmente configurada como uma conta do IBM Cloud.`

Há vários motivos pelos quais a mensagem é exibida:
{: tsCauses}

* Você tem uma [conta Lite](/docs/account?topic=account-accounts#liteaccount), a qual não permite acesso a serviços de infraestrutura.
* Sua conta não está vinculada a uma conta de infraestrutura.


Para resolver esse problema, deve-se fazer upgrade para uma conta Pré-paga ou de Assinatura. Para obter informações, consulte [Fazendo upgrade de sua conta](/docs/account?topic=account-upgrading-account).
{: tsResolve}
