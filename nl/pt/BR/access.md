---

copyright:

  years: 2017, 2018
lastupdated: "2018-10-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Gerenciando acesso ao catálogo
{: #find-access}

Como um proprietário da conta, é possível designar acesso usando uma política do IAM. Isso permite que os usuários tenham a capacidade de controlar a visibilidade de serviços privados incluídos no catálogo de conta ou nos serviços públicos que são criados na conta. Por padrão, somente o proprietário da conta pode concluir essas tarefas.

## Como delegar acesso como um proprietário da conta?
{: #get-access}

Como um proprietário da conta, é possível fornecer acesso à conta designando uma política de acesso a um usuário por meio da IU do Identity and Access. Para assegurar o acesso necessário para o usuário, selecione o recurso **Catálogo global** e a função de **Administrador** para a política de acesso.

Para conceder outras permissões, use as funções `viewer` e `editor` do Identity and Access Management (IAM). Revise a tabela a seguir para saber mais sobre o que cada função do IAM permite que um usuário faça dentro do contexto de trabalho com o catálogo para sua conta.

| Função de gerenciamento de plataforma | Descrição das ações |
|:-----------------|:-----------------|
| Visualizador | É possível ver serviços privados, mas não é possível fazer mudanças. |
| Aplicativos | É possível fazer mudanças nos metadados do objeto, mas não é possível mudar a visibilidade. |
| Administrador | É possível mudar os metadados do objeto ou a visibilidade.  |
{: caption="Tabela 1. Exemplo de funções e ações de gerenciamento de plataforma para o serviço de catálogo" caption-side="top"}

Para obter instruções passo a passo sobre como designar acesso a usuários em sua conta, acesse a documentação [Acesso a recursos](/docs/iam/mngiam.html#iammanidaccser#resourceaccess).

## Como verificar se eu tenho acesso?

Quando você é incluído na conta de outra pessoa, ela pode delegar níveis de acesso a você para que seja possível visualizar recursos privados que são incluídos na conta. O proprietário da conta também pode delegar isso para quem vê recursos públicos no catálogo de contas. Você não tem esse acesso por padrão. O proprietário da conta deve conceder a você uma função do IAM que permite ter acesso para concluir essas tarefas de gerenciamento de recurso de conta.

É possível usar a CLI ou a IU do Identity and Access para determinar se você tem acesso para permitir que usuários específicos visualizem um recurso privado que é incluído na conta.

Para usar a UI do Identity and Access, conclua as etapas a seguir:

1. Acesse **Gerenciar** > **Acesso (IAM)** e, em seguida, clique em **Usuários**.
2. Clique em seu nome na lista Usuários.
3. Clique na guia **Políticas de acesso**, na qual é possível visualizar suas políticas de acesso designadas. Deve-se ter a função de administrador do Cloud IAM para o recurso de catálogo em sua conta para atualizar a lista que inclui as contas para ver os recursos privados no catálogo.

Para usar a [CLI do {{site.data.keyword.Bluemix_notm}}](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_iam), conclua as etapas a seguir:

Insira o comando a seguir com seu nome de usuário `ibmcloud iam user-policies <your-username>` para descobrir se você é um administrador de contas selecionadas na CLI. Caso não seja um administrador para sua conta, esses comandos retornarão um erro informando que você não está autorizado.
{: tip}
