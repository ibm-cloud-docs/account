---



copyright:

  years: 2017, 2018
lastupdated: "2018-03-22"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Gerenciando grupos de recursos
{: #rgs}

Um grupo de recursos é uma maneira de organizar seus recursos de conta em
agrupamentos customizáveis, de modo que possa designar rapidamente aos usuários acesso a
mais de um recurso por vez. Qualquer recurso de conta que é gerenciado usando o controle de acesso do
{{site.data.keyword.Bluemix}} Identity and Access Management (IAM) pertence a um
grupo de recursos em sua conta. Os serviços do Cloud Foundry permanecem designados a organizações e espaços e não podem ser incluídos em um grupo de recursos.

Para começar a gerenciar seus grupos de recursos, acesse **Gerenciar** &gt; **Conta** &gt; **Grupos de recursos** no console do {{site.data.keyword.Bluemix}}. A partir daí, é possível visualizar os grupos de recursos, renomeá-los e criar novos grupos de recursos.


## Criando um grupo de recursos

Se você tiver uma conta pré-paga ou de assinatura, será possível criar múltiplos grupos de recursos para gerenciar a cota e visualizar o uso de faturamento facilmente para um conjunto de recursos. Também será possível agrupar recursos para tornar mais fácil a designação de acesso de usuários para mais de uma instância por vez.

Se você tiver uma conta Lite ou uma avaliação de 30 dias, não será possível criar grupos de recursos adicionais, mas será possível renomear seu grupo de recursos padrão. 

Cada grupo de recursos é grátis, no entanto, as conexões entre um grupo de recursos e uma organização ou espaço do Cloud Foundry contam para sua cota de conta. Para obter mais informações, veja [O que é um alias?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

1. Acesse **Gerenciar** &gt; **Conta** &gt; **Grupos de recursos**.
2. Clique em **Criar um grupo de recursos**.
3. Insira um nome para seu grupo de recursos.
4. Clique em ** Adicionar**.

## Incluindo recursos em um grupo de recursos

Os serviços que são gerenciados usando o IAM pertencem a um grupo de recursos, não a uma
organização ou espaço do Cloud Foundry. Ao criar uma instância de serviço para um desses serviços do catálogo,
é solicitado que você designe a instância a um grupo de recursos. A seleção de grupo de recursos no momento da
criação da instância é definitiva e não pode ser mudada.

## Visualizando recursos em grupos de recursos

Para visualizar facilmente os recursos contidos em um grupo de recursos, filtre por grupo de recursos de seu painel.

## Renomeando um grupo de recursos

O primeiro grupo de recursos é criado e nomeado `Padrão` para você. É possível escolher atualizar o nome desse grupo ou quaisquer outros grupos criados.

1. Acesse **Gerenciar** &gt; **Conta** &gt; **Grupos de recursos**.
2. Clique em **Renomear**.
3. Insira um nome exclusivo e clique em **Salvar**.

## Gerenciando recursos e grupos de recursos usando o {{site.data.keyword.Bluemix_notm}} CLI

O {{site.data.keyword.Bluemix_notm}} CLI possui vários comandos que suportam o gerenciamento de recurso. Para obter mais informações, consulte [Comandos para gerenciar recursos e grupos de recursos](/docs/cli/reference/bluemix_cli/bx_cli.html#commands-for-managing-resource-groups-and-resources).

## Gerenciando o acesso a seus grupos de recursos

O Cloud IAM oferece a flexibilidade para fornecer acesso de usuário de baixa granularidade aos recursos em sua conta. É possível usar o Cloud IAM para designar políticas a usuários, que fornecem acesso de usuário a todos os recursos em um grupo de recursos, um único tipo de serviço em um grupo de recursos ou uma instância de serviço individual na conta. Fornecer aos usuários o acesso a recursos em um grupo de recursos não concede a eles o acesso para gerenciar o grupo de recursos em si. É possível configurar o acesso para a capacidade de visualizar, editar e gerenciar o grupo de recursos reais separadamente.

Para obter mais informações sobre como gerenciar o acesso a grupos de recursos, veja [Gerenciando acesso ao IAM](/docs/iam/mngiam.html#iammanidaccser).
