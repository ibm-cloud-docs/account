---

copyright:

  years: 2017, 2018
lastupdated: "2017-11-21"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Gerenciando acesso ao catálogo
{: #find-access}

Como um proprietário da conta, você pode desejar designar acesso usando uma política do IAM para permitir aos usuários em sua conta a capacidade de controlar a visibilidade de serviços privados incluídos no catálogo de conta ou serviços públicos que foram criados na conta. Por padrão, somente o proprietário da conta tem a capacidade para concluir essas tarefas.

## Como delegar acesso como um proprietário da conta?
{: #get-access}

Se você é um proprietário da conta, é possível conceder acesso a um usuário em sua conta por meio da UI do Identity and Access designando uma política de acesso. Para assegurar que o usuário tenha o acesso necessário, selecione o recurso **Catálogo global** e a função de **Administrador** para a política de acesso.

Você pode desejar conceder outras permissões aos usuários em sua conta usando as funções `viewer` e `editor` do Identity and Access Management (IAM). Revise a tabela a seguir para saber mais sobre o que cada função do IAM permite que um usuário faça dentro do contexto de trabalho com o catálogo para sua conta.

| Função de gerenciamento de plataforma | Descrição das ações |
|:-----------------|:-----------------|
| Viewer | É possível ver os serviços privados, mesmo se a conta não tiver sido incluída, mas não é possível fazer mudanças. |
| Aplicativos | É possível fazer mudanças nos metadados do objeto, mas não é possível mudar a visibilidade. |
| Administrador | É possível mudar os metadados do objeto ou a visibilidade.  |
{: caption="Tabela 1. Exemplo de funções e ações de gerenciamento de plataforma para o serviço de catálogo" caption-side="top"}

Para obter instruções passo a passo sobre como designar acesso a usuários em sua conta, acesse a documentação [Acesso a recursos](/docs/iam/mngiam.html#iammanidaccser#resourceaccess).


## Como verificar se eu tenho acesso?

Quando você é incluído na conta de outra pessoa, ela pode delegar certos níveis de acesso a você para que seja possível visualizar recursos privados que foram incluídos na conta. O proprietário da conta também pode delegar a capacidade de gerenciar quem vê recursos públicos no catálogo de conta. Você não tem esse acesso por padrão. O proprietário da conta deve conceder a você uma função do IAM que permite ter acesso para concluir essas tarefas de gerenciamento de recurso de conta.

É possível usar a CLI ou a UI do Identity and Access para determinar se você tem acesso para permitir que usuários específicos visualizem um recurso privado que foi incluído na conta.

Para usar a UI do Identity and Access, conclua as etapas a seguir:

1. Acesse **Gerenciar** > **Segurança** > **Identity and Acess** e, em seguida, clique em **Usuários**.
2. Clique em seu nome na lista Usuários.
3. Na seção **Políticas de acesso**, é possível visualizar suas políticas de acesso designado. Deve-se ter a função de administrador do Cloud IAM para o recurso de catálogo em sua conta para atualizar a lista que inclui as contas para ver os recursos privados no catálogo.

Para usar o [bx CLI](/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_iam), conclua as etapas a seguir:

Insira o comando a seguir com seu nome do usuário `bx iam user-policies <your-username>` para descobrir se você é um administrador de contas selecionadas na CLI. Caso não seja um administrador para sua conta, esses comandos retornarão um erro informando que você não está autorizado.
{: tip}
