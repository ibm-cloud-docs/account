---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: create account, IBMid, sign up for account, sign up

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Inscrevendo-se para o {{site.data.keyword.Bluemix_notm}}
{: #signup}

É possível inscrever-se em uma conta do {{site.data.keyword.Bluemix}} usando seu IBMid existente ou criando um novo IBMid. Se a sua empresa estiver registrada para usar um ID federado para conexão única (SSO), inscreva-se com seu ID federado no lugar.
{:shortdesc}

| ID de inscrição | Detalhes |    
|-----------------|---------|
|ID IBM existente   | Se você já tiver um ID IBM, inscreva-se para o {{site.data.keyword.Bluemix_notm}} com suas credenciais existentes que você usa para outros produtos e serviços IBM. |
|Novo ID IBM        | Se ainda não tiver um IBMid, você criará um ao inscrever-se. Com um IBMid, é possível usar um nome de usuário para efetuar login em todos os produtos e serviços IBM, incluindo o {{site.data.keyword.Bluemix_notm}}. |
|ID federado     | Se sua empresa já solicitou para registrar as credenciais do usuário por meio do domínio de sua
empresa com a IBM, será possível inscrever-se para o {{site.data.keyword.Bluemix_notm}} usando as
credenciais que você já usa para login de sua empresa. Deve-se inserir um número do telefone ao se inscrever. |
{:caption="Tabela 1. Opções de ID para inscrição no {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Inscrevendo-se com um IBMid novo ou existente
{: #signup-ibmid}

Caso não faça parte de uma empresa que usa IDs federados, você se inscreverá no {{site.data.keyword.Bluemix_notm}} com um IBMid.

1. Acesse a [ página de login do {{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com/){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo") e clique em **Criar uma conta do {{site.data.keyword.Bluemix_notm}}**.
1. Insira seu endereço de e-mail do IBMid. Se você não tiver um IBMid existente, um ID será criado com base no e-mail que você inserir.
1. Preencha os campos restantes com suas informações e clique em **Criar conta**.
1. Confirme sua conta clicando no link no e-mail de confirmação que é enviado para o endereço de e-mail fornecido.

Se você encontrar algum problema ao efetuar login com sua nova conta, consulte [Resolução de problemas para acessar o {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-accessing) para obter ajuda.

## Inscrevendo-se com um ID federado
{: #signup-federated}

Um ID federado é um ID dentro do domínio de uma empresa que
foi registrado na IBM para que as credenciais de domínio e do usuário possam ser usadas para acessar
aplicativos da web da IBM. É possível se inscrever no {{site.data.keyword.Bluemix_notm}} com um ID federado apenas se sua empresa já está registrada com a IBM. O registro do domínio de uma empresa na IBM permite que
os usuários efetuem log-in nos produtos e serviços IBM usando suas credenciais de usuário
da empresa existentes. A autenticação é, então, manipulada pelo provedor de identidade de sua empresa usando a SSO.

A IBM usa o Security Assertion Markup Language 2.0 (SAML 2.0) para essa federação de identidade. O SAML 2.0 é uma versão padrão para trocar dados de autenticação entre os domínios de segurança. Ele é um protocolo baseado em XML que usa um token de segurança que contém asserções para transmitir informações entre o "provedor de identidade" das organizações e o "IBM Rely Party (RP)", também conhecido como o provedor de serviços.

Para obter informações sobre como registrar sua empresa para um ID federado, consulte o [Guia de adoção do IBMid Enterprise Federation ![Ícone de link externo](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window}. Um patrocinador IBM, como um defensor da oferta ou do cliente, é necessário quando você solicita o registro de IDs federados.

### Efetuando login com um ID federado
{: #login-federated}

Ao efetuar login no console do {{site.data.keyword.Bluemix_notm}} com um ID federado, você será solicitado a efetuar login por meio da página de login da sua empresa. Se você efetuar login por meio de uma CLI, será necessário especificar parâmetros adicionais para se autenticar. Para obter mais informações, consulte [Efetuando login com um ID federado](/docs/iam?topic=iam-federated_id).
