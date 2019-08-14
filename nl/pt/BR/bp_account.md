---

copyright:
  years: 2018, 2019
lastupdated: "2019-07-08"

keywords: organizing resource group, account best practices, best practices account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Melhores práticas para configurar a conta
{: #account_setup}

Essas melhores práticas fornecem os blocos de construção básicos para obter sucesso antes de iniciar a criação de recursos. Se você estiver pronto para obter apps para produção e configurar um ambiente para seus desenvolvedores, revise as seções a seguir para configurar sua conta.
{:shortdesc}

As melhores práticas a seguir focam na utilização de serviços ativados pelo IAM. Atualmente, nem todos os serviços no {{site.data.keyword.cloud}} estão ativados para IAM. As políticas, os grupos de recursos e os grupos de acesso do IAM não se aplicam a instâncias de serviço que pertencem a uma organização e um espaço do Cloud Foundry. Ainda é possível usar as organizações e os espaços do Cloud Foundry e os grupos de recursos em sua conta, mas deve-se designar aos usuários acesso a esses recursos separadamente. Para obter informações sobre organizações e espaços do Cloud Foundry, veja [Incluindo organizações e espaços](/docs/account?topic=account-orgsspacesusers).
{: note}

## O que faz uma boa estratégia de grupo de recursos?
{: #resource-group-strategy}

Os administradores poderão ter melhor controle do uso de recursos no nível de ambiente do projeto se um grupo de recursos por ambiente do projeto for usado. Por exemplo, um projeto típico tem ambientes de desenvolvimento, teste e produção. Um projeto denominado `CustApp` teria os grupos de recursos a seguir:

* `CustApp-Dev`
* `CustApp-Test`
* `CustApp-Prod`

É possível conceder acesso a usuários. Por exemplo, um desenvolvedor geralmente tem permissões de acesso bastante abrangentes para o grupo de recursos de desenvolvimento e muito mais rígidas ou nenhum acesso ao grupo de recursos de produção.

Se você tiver uma conta Pré-paga ou de Assinatura, será possível criar mais grupos de recursos:

1. Acesse **Gerenciar > Conta**. Expanda **Recursos da conta** e selecione **Grupos de recursos**.
3. Clique em **Criar**.
4. Insira o nome de seu grupo de recursos.
5. Clique em **Incluir**.

Para obter mais informações sobre qual tipo de conta funcionará melhor para você, veja [Tipos de conta](/docs/account?topic=account-accounts).


## Configurando seu grupos de recursos
{: #setting-up-rgs}

Os grupos de recursos são um contêiner lógico para organizar seus recursos ativados para IAM. Todos os serviços que são gerenciados usando o controle de acesso do {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) pertencem a um grupo de recursos. Você designa um recurso para seu grupo de recursos ao criá-lo por meio do catálogo. Não é possível mudar a designação do grupo de recursos depois de configurá-la, esse é o motivo pelo qual é importante configurar alguns de seus grupos de recursos agora.

Se você tiver uma conta Lite, terá acesso a um único grupo de recursos que é criado para você. Não é possível editar grupos de recursos extras. Considere [fazer upgrade de sua conta](/docs/account?topic=account-upgrading-account) para criar e trabalhar com múltiplos grupos de recursos.
{: note}


## Incluindo recursos em um grupo de recursos
{: #adding-resources}

É possível incluir um recurso em um grupo de recursos ao criar um recurso ativado pelo IAM por meio do catálogo. Ao selecionar o recurso, certifique-se de que o grupo de recursos de destino esteja selecionado. Depois que um recurso é criado, não é possível mudar seu grupo de recursos designado. Se você designar acidentalmente um recurso ao grupo de recursos incorreto, exclua o recurso e crie um novo.

### Acesso necessário para incluir um recurso em um grupo de recursos
{: #rg_access}

Como proprietário da conta, é possível incluir recursos em qualquer grupo de recursos. Outros usuários devem ter acesso concedido usando uma política de acesso do IAM para incluir recursos em grupos de recursos. Há duas funções mínimas de gerenciamento de plataforma que devem ser designadas aos usuários para incluir recursos em um grupo de recursos:

* Função de visualizador ou superior no grupo de recursos
* Função de editor ou superior no recurso ou serviço

Para incluir um recurso em um grupo de recursos, conclua as etapas a seguir:

1. Acesse **Gerenciar > Conta** e selecione **Grupos de recursos**.
2. Clique no ícone Ações ![Ícone Ações](../icons/action-menu-icon.svg) para o grupo de recursos no qual você deseja incluir recursos e selecione **Incluir recursos**.
3. Depois de ser redirecionado para o catálogo, selecione o recurso que você gostaria de incluir.
4. Selecione o grupo de recursos para o qual você deseja designá-lo.
5. Clique em **Criar**.

É possível sempre ir diretamente para o catálogo para criar recursos e designá-los a um grupo de recursos.
{: tip}

Para obter mais informações, consulte [Melhores práticas para organizar recursos em um grupo de recursos](/docs/resources?topic=resources-bp_resourcegroups).


## Usando tags para organizar recursos
{: #tags}

Use tags para organizar seus recursos e controlar os custos de uso. É possível identificar recursos relacionados e visualizá-los em toda a sua conta filtrando por tags em seu painel. As tags de par chave:valor podem ajudar você a organizar seus ambientes de desenvolvimento, projetos, conformidade e otimização.

Para incluir uma tag em um recurso, conclua as etapas a seguir:

1. Clique no ícone Menu ![Ícone Menu](../icons/icon_hamburger.svg) > **Lista de recursos** para visualizar sua lista de recursos. Localize o recurso que você deseja identificar.
2. Se o recurso já tiver uma tag, passe o mouse sobre a tag existente e clique no ícone Editar ![Ícone Editar](../icons/edit-tagging.svg). Se o recurso não tiver uma tag, passe o mouse sobre **--** na coluna `Tags` e clique em **Incluir tags**.
3. Digite um nome para a tag e pressione Enter após cada tag, se você estiver incluindo mais de uma.
4. Para remover uma tag do recurso, clique no ícone Remover ![Ícone Remover](../icons/close-tagging.svg) próximo à tag.
5. Salve suas mudanças.

Para obter mais informações sobre quais recursos podem ser identificados e como designar acesso para delegar funcionalidade de identificação aos usuários em sua conta, veja [Trabalhando com tags](/docs/resources?topic=resources-tag).


## Próximas Etapas

Configure grupos de acesso para os usuários e IDs de serviço que requerem o mesmo acesso a recursos e grupos de recursos em sua conta. É possível designar um número mínimo de políticas de acesso, o que economiza tempo. Para obter mais informações, veja [Melhores práticas para designar acesso](/docs/iam?topic=iam-account_setup).
