---


copyright:

  years: 2018
lastupdated: "2018-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}


# Configurando a segurança de login
{: #login-settings}

Com acesso autorizado, é possível configurar a segurança extra para seu login. É possível configurar perguntas e respostas de segurança, selecionar uma expiração de senha, configurar a autenticação de diversos fatores (MFA) do time-based one-time passcode (TOTP) e configurar as opções de autenticação externa.  
{:shortdesc}

Um proprietário da conta pode requerer a MFA do IBMid em uma conta da qual você é um membro. A MFA do IBMid substitui qualquer outra configuração de MFA. Por exemplo, quando a MFA do IBMid está configurada, você recebe uma solicitação para fornecer uma MFA do TOTP associada a seu IBMid em vez de perguntas de segurança ou um dos métodos de autenticação externa.
{: note}

Será possível visualizar as opções de segurança a seguir e ativar ou desativá-las somente se seu administrador conceder acesso a você. Acesse **Ícone do {{site.data.keyword.avatar}}**![Ícone do Avatar](../icons/i-avatar-icon.svg) > **Perfil e configurações** e selecione **Configurações de login**.

## Configurando perguntas de segurança
{: #security-questions}

Para configurar suas perguntas de segurança:
1. No console, acesse **Ícone do {{site.data.keyword.avatar}}**![Ícone do Avatar](../icons/i-avatar-icon.svg) > **Perfil e configurações** e selecione **Configurações de login**.
2. Clique em **Editar**. 
3. Selecione as perguntas que você deseja ter e respondê-las. Deve-se usar três opções de pergunta de segurança.
4. Clique em **Salvar** quando tiver concluído.  
5. Certificar-se de que a caixa `Yes` esteja marcada para que as perguntas de segurança sejam ativadas. Marcar a caixa `Yes` pode solicitar que você se conecte à sua conta novamente.  

É possível configurar respostas para três perguntas de segurança para autenticação extra no login. Deve-se configurar suas perguntas e respostas de segurança antes que seu administrador possa ativar esse requisito da MFA para você.

Deve-se ser o proprietário da conta ou ter a configuração Login gerenciado pelo usuário ativada para você por seu administrador de conta para ativar e desativar perguntas de segurança.
{: note}

## Configurando uma expiração de senha
{: #password-expiration}

Para configurar o período de tempo que você gostaria de usar sua senha atual, selecione uma opção para que sua senha expire na seção **Expiração de senha**.

A expiração de senha é configurada para nunca por padrão. Quando você se inscreve para uma conta, nunca é necessário mudar sua senha. Ao configurar um período de expiração da senha, você é notificado sobre a expiração de senha por e-mail 14 dias antes, 7 dias antes e no dia em que a senha está configurada para expirar.

Essa opção está disponível somente para usuários que efetuam login com um ID do SoftLayer. Para atualizar sua expiração de senha, deve-se ser um proprietário da conta ou ter a configuração Login gerenciado pelo usuário ativada para você por seu administrador de conta na página de detalhes do Usuário do IAM.
{: note}

## Configurando a autenticação do TOTP
{: #MFA}

Para configurar sua autenticação do TOTP, clique em **Configurar**. 

A MFA do TOTP inclui uma camada extra de segurança em sua conta, requerendo uma senha TOTP, além do ID padrão e da senha durante o login. Deve-se configurar a autenticação do TOTP antes que seu administrador de conta possa ativar esse requisito da MFA para você.

Também poderá ser solicitada a você uma senha única baseada em tempo se a configuração TOTP não estiver configurada e ativada. Isso é porque um proprietário da conta pode ativar a MFA do IBMid para uma conta para a qual você tenha acesso. Esse tipo de MFA se aplica a cada usuário na conta quando essa configuração está ativada e é necessário usá-la. Para obter mais informações, veja [Tipos de autenticação de diversos fatores](/docs/iam/mfatypes.html#types).


## Configurando opções de autenticação externa
{: #third-party-MFA}

Você ou seu administrador de conta pode pedir a autenticação da Symantec ou baseada em telefone para por um custo mensal. Para pedir a autenticação externa, é necessário ter as permissões de inclusão de infraestrutura de serviços. Para descobrir se a autenticação externa está ativada, acesse o ícone **{{site.data.keyword.avatar}}** ![Ícone do Avatar](../icons/i-avatar-icon.svg) > **Perfil e configurações** e selecione **Configurações de login**. Se a MFA baseada em telefone estiver desativada, clique em **Acessar detalhes do usuário**. Esse link levará você para a mesma página que as etapas para configurar sua autenticação da symantec e configurar sua autenticação baseada em telefone.  

### Configurando a autenticação da Symantec

Se seu administrador de conta escolher pedir proteção de identidade Symantec, deve-se trabalhar com seu administrador para ajudá-lo a concluir a ordem, fornecendo seu ID de credencial:

1. Acesse [Symantec VIP](https://vip.symantec.com/).
2. Clique em **Download**. 
3. Obtenha seu ID de credencial e forneça o ID para o seu administrador para concluir a ordem. 

Depois que seu administrador pede e ativa a opção, é possível usar o app para autenticação de login.

### Configurando a autenticação baseada em telefone

Se o seu administrador de conta escolhe pedir proteção de identidade baseada em telefone, deve-se configurá-la após ela ser pedida por seu administrador. Em seguida, seu administrador pode ativá-la para que você use. Depois que seu administrador pedir a autenticação baseada em telefone, conclua as etapas a seguir para configurá-la:

1. Acesse **Gerenciar** > **Acesso (IAM)**.
2. Clique em **Usuários** e selecione seu nome na lista.
3. Na página **Detalhes do usuário** na seção **Gerenciar login do usuário**, clique no ícone **Editar** ![Ícone Editar](../icons/icon_write.svg) para a linha **Autenticação baseada em telefone**.
4. Siga os prompts para configurar a autenticação baseada em telefone.

Depois de ter configurado sua autenticação baseada em telefone, o administrador de conta pode ativar a opção para você ser solicitado para esse tipo de MFA no login.


 

