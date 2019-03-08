---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-28"

keywords: user access, IBM Cloud account access, account owner

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Gerenciando o acesso de usuário ao catálogo
{: #find-access}

Como um proprietário da conta do {{site.data.keyword.Bluemix}}, é possível designar aos usuários acesso ao catálogo usando uma política do {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM). É possível controlar a visibilidade de serviços privados que são incluídos no catálogo de conta ou serviços públicos que são criados na conta. Por padrão, somente o proprietário da conta pode concluir essas tarefas.

## Delegando acesso
{: #get-access}

É possível delegar acesso em sua conta para controlar o que os usuários podem ver e para controlar a autoridade que esses usuários têm. Por exemplo, algumas informações podem ser apropriadas somente para um usuário ler e analisar, enquanto outro pode receber a autoridade para editar essas informações. Para delegar acesso de conta a outro usuário na conta, conclua as etapas a seguir.

1. Clique em **Gerenciar** > **Acesso (IAM)**.
2. Clique em **O acesso inicia com o usuário** na página de entrada.
3. Selecione um usuário em sua conta.
4. Clique em **Políticas de acesso**.
5. Clique em **Designar acesso**. Em seguida, clique em **Designar serviços de gerenciamento de conta**.
6. Selecione o **Catálogo de recursos globais** na lista Serviços e a função **Administrador** na lista Selecionar funções.

Para conceder outras permissões, use as funções Visualizador e Editor. Revise a tabela a seguir para saber mais sobre o que cada função do IAM permite que um usuário faça dentro do contexto de trabalho com o catálogo para sua conta.

| Função de gerenciamento da plataforma | Ações                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| Visualizador                   | É possível visualizar serviços privados, mas mudá-los, não                                                            |
| Aplicativos                   | É possível mudar os metadados do objeto, mas não é possível mudar a visibilidade para serviços privados                                |
| Administrador            | É possível mudar os metadados do objeto ou a visibilidade para serviços privados e restringir a visibilidade de um serviço público  |
{: caption="Tabela 1. Exemplo de funções e ações de gerenciamento de plataforma para o catálogo" caption-side="top"}

Para obter mais informações sobre como designar acesso a usuários, consulte [Designando acesso a serviços de gerenciamento de conta](/docs/iam?topic=iam-account-services).

## Confirmando seu acesso
{: #confirm-access}

Quando você é incluído na conta de outra pessoa, os administradores de conta podem delegar níveis de acesso a você para que seja possível visualizar recursos privados que são incluídos na conta. O proprietário da conta também pode delegar para quem pode visualizar recursos públicos no catálogo da conta. Você não tem esse acesso por padrão. O proprietário da conta deve conceder a você uma função do IAM, para que seja possível ter acesso para concluir essas tarefas de gerenciamento de recursos da conta.

É possível usar o console ou a interface da linha de comandos (CLI) do {{site.data.keyword.Bluemix_notm}} para determinar se você tem acesso para permitir que usuários específicos visualizem um recurso privado na conta.

Para usar o console, conclua as etapas a seguir:

  1. Acesse **Gerenciar > Acesso (IAM)**.
  2. Clique em seu nome na lista Usuários.
  3. Clique na guia **Políticas de acesso**, na qual é possível visualizar suas políticas de acesso designadas. Deve-se ter a função de administrador do Cloud IAM para o recurso de catálogo em sua conta para atualizar a lista que inclui as contas para ver os recursos privados no catálogo.


Para usar a [CLI](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_iam#ibmcloud_commands_iam), execute o comando `ibmcloud iam user-policies <your-user-name>`. O comando retornará um erro se você não for um administrador para a conta.
