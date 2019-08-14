---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: troubleshoot enterprise, enterprise problem, account problem, enterprise support, enterprise help, error message

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

# Resolução de problemas para uma empresa
{: #enterprise_help}

Os problemas gerais com o gerenciamento de sua empresa podem incluir problemas quando você tenta aplicar códigos de assinatura ou de recurso ou quando tenta incluir uma conta na empresa. Em muitos casos, é possível recuperar-se desses problemas seguindo algumas etapas simples.

## Por que não posso visualizar a empresa inteira?
{: #troubleshoot-view-enterprise}
{: troubleshoot}

Se você não estiver vendo a empresa inteira, talvez seja necessário verificar qual acesso está designado a você.

É possível ver algumas das contas na empresa, mas não na hierarquia corporativa inteira. A hierarquia de contas mostra somente as contas às quais você tem acesso, não a conta corporativa inteira.
{: tsSymptoms}

Você tem o acesso designado a somente determinadas contas na empresa.
{: tsCauses}

Para verificar qual acesso você está designado, conclua as etapas a seguir:
{: tsResolve}

1. Acesse **Gerenciar** &gt; **Acesso (IAM)** > **Usuários**.
2. Selecione seu nome.
2. Clique na guia **Políticas de acesso**.

Entre em contato com o proprietário corporativo para solicitar o acesso correto.

Se você for o proprietário da empresa, conclua as etapas a seguir para designar um acesso de usuário à empresa inteira:
1. Acesse **Gerenciar** > **Acesso (IAM)** > **Usuários**.
2. Selecione o nome do usuário.
2. Clique na guia **Políticas de acesso** > **Designar acesso** > **Designar acesso a serviços de gerenciamento de conta**.
3. Selecione **Empresa** como o serviço e selecione o nome de sua empresa.
4. Selecione o grupo de contas ou a conta na empresa para a qual você deseja fornecer o acesso de usuário. Por exemplo, se você desejar que um usuário tenha acesso para visualizar apenas uma única conta, selecione a conta e designe ao usuário a função de Visualizador ou superior. Se você desejar que um usuário tenha acesso para visualizar a empresa inteira, deixe o grupo de contas e as seleções de conta em branco e designe o acesso.

## Por que não posso importar uma conta existente na empresa?
{: #troubleshoot-existing-enterprise}
{: troubleshoot}

Quando você tenta importar uma conta existente na empresa, ocorre um dos problemas a seguir:
{: tsSymptoms}
* Quando você clica em **Incluir conta existente** na seção Conta, a conta que você deseja incluir não está listada.
* Você não tem a opção de clicar em **Importar conta**.

Você não está designado ao acesso correto ou a conta não é elegível para ser importada.
{: tsCauses}

Se você não puder ver a conta existente que deseja importar, será necessária a função de Administrador no serviço Faturamento da conta existente.
{: tsResolve}

Se a opção **Importar conta** não estiver disponível, verifique se você tem a função de Administrador ou de Editor no serviço Faturamento da empresa e a função de Administrador ou Editor no serviço Corporativo para o grupo de empresas ou de conta pai.

Se a conta que você deseja importar for uma conta Pré-paga e ainda não puder importá-la depois de verificar se você tem acesso, a conta pode não ser elegível para ser importada na empresa. Algumas contas Pré-pagas não podem ser diretamente importadas em uma empresa, como muitas contas Pré-pagas que são faturadas em dólares dos Estados Unidos (USD). Entre em contato com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}![Ícone de link externo](../icons/launch-glyph.svg) para converter a conta em uma conta de Assinatura e, em seguida, importe-a na empresa.

## Por que não posso criar uma nova conta na empresa?
{: #troubleshoot-add-enterprise}
{: troubleshoot}

Não é possível clicar em **Incluir conta** na seção Conta.
{: tsSymptoms}

Você não tem o acesso correto designado.
{: tsCauses}

Para criar uma conta na empresa, deve-se ter o acesso a seguir.
{: tsResolve}
1. Função de Administrador no serviço Faturamento da empresa.
2. A função de Administrador ou de Editor no serviço Corporativo para o grupo de empresas ou de conta pai de destino.

## Por que não posso ver as assinaturas corporativas?
{: #troubleshoot-viewsub-enterprise}
{: troubleshoot}

Quando você vai visualizar a página Assinaturas por meio de uma conta-filha, a mensagem a seguir é exibida:
{: tsSymptoms}

`Looks like you don't have permission to view subscription data for this account. Contact your account owner or administrator to request access.`

A mensagem a seguir é exibida na seção Faturamento em seu painel corporativo:

`Looks like you don't have permission to view this information. Learn more about IAM access.`

O acesso às informações de faturamento e pagamento para os períodos de faturamento futuros é restrito aos usuários na conta corporativa. Os usuários em uma conta-filha não podem acessar informações de faturamento e pagamento, como assinaturas, mesmo se anteriormente tinham acesso na conta.
{: tsCauses}

Para visualizar ou gerenciar faturamento, é necessário ser convidado para a conta corporativa e receber acesso ao serviço Faturamento nessa conta. Entre em contato com o proprietário da conta para solicitar acesso.
{: tsResolve}

## Por que não posso aplicar um código de assinatura à minha conta?  
{: #troubleshoot-promo-enterprise}
{: troubleshoot}

Não é possível incluir um código de assinatura em sua conta porque você não tem o acesso correto.  
{: tsSymptoms}

Como sua conta é uma conta-filha na empresa, não é possível aplicar códigos de assinatura. Os códigos de assinatura devem ser aplicados no nível corporativo.
{: tsCauses}

Entre em contato com o proprietário ou com o administrador da empresa para incluir o código de assinatura. Quando o código de assinatura é incluído, ele se aplica a todas as contas na empresa. Para obter mais informações, consulte [Gerenciando assinaturas](/docs/billing-usage?topic=billing-usage-subscriptions).
{: tsResolve}
