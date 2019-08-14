---

copyright:
  years: 2019
lastupdated: "2019-08-05"

keywords: enterprise, enterprise resources, enterprise account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Melhores práticas para configurar uma empresa
{: #enterprise-best-practices}

Estas melhores práticas fornecem os blocos de construção básicos para a configuração de uma empresa do {{site.data.keyword.cloud}}.
{:shortdesc}

## Organizando contas de acordo com o modo como você deseja rastrear o faturamento
{: #organize-enterprise-usage}

Um dos principais benefícios das empresas do {{site.data.keyword.cloud_notm}} é que elas permitem que você visualize e gerencie centralmente o faturamento e o uso em múltiplas contas. A utilidade desse recurso depende de sua estrutura corporativa, pois os dados de uso são agregados por cada grupo de contas e conta. Crie grupos de contas para projetos que funcionem sob um orçamento comum. Consulte [Como posso usar uma empresa?](/docs/account?topic=account-enterprise#enterprise-use-cases) para obter exemplos.

O administrador corporativo ou o seu executivo financeiro podem não estar familiarizados com cada conta individual ou grupo de contas. Para facilitar a identificação de seus propósitos, forneça a cada conta e grupo de contas um nome legível. Se sua empresa usar códigos de faturamento, será possível incluí-los no nome. Por exemplo, em vez de um grupo de contas `devteam` com contas `fed ui` e `be api`, crie o grupo de contas `Development - A2B3` com contas `Front-end UI team` e `Back-end API team`.

Um usuário corporativo com acesso de Administrador ou de Editor pode editar os nomes da empresa e do grupo de contas, mas ele não pode mudar os nomes de conta. Para editar um nome de conta, um usuário deve estar na conta em si.
{:tip}

Como você tem uma visualização unificada de todo o uso que é organizado por seus grupos de contas e contas, é possível estornar custos de uso às equipes associadas. Para obter mais informações, consulte [Recuperando custos para uso corporativo](/docs/billing-usage?topic=billing-usage-enterprise-usage#enterprise-cost-recovery).

## Criando uma hierarquia corporativa consistente
{: #accounts-vs-groups}

Ao configurar sua empresa, você cria uma hierarquia corporativa que reflete sua empresa ou sua organização. À medida que você cria contas e grupos de contas, planeje um esquema consistente para o modo como sua empresa usa as camadas corporativas a seguir:
- Grupos de recursos e organizações e espaços do Cloud Foundry em uma conta
- Contas dentro de um grupo de contas
- Grupos de contas dentro da empresa

Por exemplo, sua empresa pode criar contas para cada equipe, com grupos de recursos ou organizações do Cloud Foundry dentro da conta para ambientes de desenvolvimento, de teste e de produção. Outra empresa pode ter contas distintas para cada ambiente, que são agrupadas em grupos de contas para cada equipe.

Independentemente de como você escolhe estruturar sua empresa, seja o mais consistente possível a fim de simplificar o gerenciamento corporativo. Como é fácil criar e controlar novas contas, pode ser tentador criar um monte de contas separadas, conforme os usuários solicitarem. Porém, cada conta introduz um gasto adicional de gerenciamento. Enquanto você planeja como estruturar sua empresa, tenha em mente os pontos a seguir:
- Para cada conta que você criar, os usuários devem ser convidados e seu acesso deve ser gerenciado separadamente.
- Uma estrutura inconsistente pode tornar mais difícil determinar a quem dar acesso dentro de cada conta e quais equipes estão usando recursos.
- Os usuários podem colaborar com recursos e serviços em uma conta individual apenas. Os recursos não podem ser movidos entre as contas.

## Configurando políticas de acesso em uma empresa
{: #access-enterprise}

Como sempre, siga a melhor prática para designar o número mínimo de políticas de acesso e de níveis de acesso. Isso permite que você gaste menos tempo atribuindo acesso a usuários e mais tempo se concentrando no desenvolvimento no {{site.data.keyword.cloud_notm}}, ao mesmo tempo em que assegura que você não forneça muito acesso aos usuários que não precisem.

Os grupos de acesso são uma ferramenta útil para designar acesso a um grupo de usuários e a IDs de serviço que precisam do mesmo acesso. Com o uso dos grupos de acesso, é possível simplificar o gerenciamento de acesso designando o número mínimo de políticas de acesso a grupos de usuários. Como um exemplo, se você tiver cinco usuários que deseje que gerenciem todas as tarefas relacionadas ao faturamento e gerenciamento de contas para a empresa, será possível incluí-los em um grupo de acesso que é chamado de `Administradores`. No grupo de acesso, é possível designar duas políticas: uma com a função de administrador no serviço de gerenciamento de conta de cobrança e uma com a função de administrador em todos os serviços de gerenciamento de conta na conta. À medida que os usuários mudam de equipe ou as responsabilidades dos cargos deles são alteradas, será possível incluir ou remover usuários do grupo de acesso em vez de incluir ou remover as mesmas políticas dos usuários individuais. Consulte [Designando acesso corporativo](/docs/iam?topic=iam-assign-access-enterprise) para obter mais informações.

## Trabalhando com recursos em uma empresa
{: #child-resources-enterprise}

Crie recursos apenas em contas-filhas que você importar ou criar dentro da empresa. Embora seja possível criar recursos dentro da conta corporativa, não é uma melhor prática pelos motivos a seguir:
 - A conta corporativa é sempre uma filha direta da empresa e não pode ser movida, de modo que você não terá a flexibilidade para mudar como o uso é relatado para os recursos.
 - A conta corporativa contém os usuários e o acesso para gerenciar a empresa e seu faturamento, portanto, somente usuários com essas responsabilidades devem ser incluídos na conta.

Os usuários em cada conta na empresa podem criar, usar e colaborar em recursos exatamente da mesma forma que você pode fazer isso em uma conta independente. Para obter detalhes, consulte [Trabalhando com recursos e serviços](/docs/resources?topic=resources-resource). Os usuários corporativos não podem trabalhar diretamente com recursos dentro de contas-filhas, mas eles podem monitorar os tipos de recursos e os planos que são usados em cada conta visualizando seu uso. Para obter mais informações, consulte [Visualizando o uso em uma empresa](/docs/billing-usage?topic=billing-usage-enterprise-usage).


