---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise account, multiple accounts, organization, hierarchy

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# O que é uma empresa?
{: #enterprise}

As empresas {{site.data.keyword.Bluemix}} fornecem uma maneira de gerenciar centralmente o faturamento e o uso de recursos em múltiplas contas. Dentro de uma empresa, você cria uma hierarquia com multicamadas de contas, com faturamento e pagamentos para todas as contas gerenciadas no nível corporativo.
{:shortdesc}

Quando comparado ao uso de múltiplas contas independentes, as empresas oferecem os principais benefícios a seguir:
- Gerenciamento de conta centralizado: visualize sua hierarquia corporativa inteira em uma visão rápida, sem precisar alternar contas. É possível incluir contas existentes ou criar novas contas diretamente dentro da empresa.
- Faturamento de assinatura consolidada: rastreie suas assinaturas e gastos de crédito para todas as contas por meio de uma única visualização. Seu crédito de assinatura é agrupado e compartilhado entre as contas na empresa.
- Relatório de uso descendente: em sua conta corporativa, é possível visualizar o uso de todas as contas em sua empresa, organizadas por grupo de contas.

## Hierarquia corporativa
{: #enterprise-hierarchy}

Em seu núcleo, uma empresa consiste em três blocos de construção principais:
- A conta corporativa, que serve como a conta pai para todas as outras contas na empresa. A conta corporativa gerencia o faturamento para a empresa inteira, com os custos de uso de todas as contas sendo acumuladas e pagas na conta corporativa.
- Grupos de contas, que podem ser usados para organizar contas relacionadas. Os grupos de contas não podem conter os recursos em si, mas é possível visualizar custos para uso de recursos das contas que eles contêm.
- Contas, que são exatamente como as contas do {{site.data.keyword.Bluemix_notm}} independentes que contêm recursos e grupos de recursos, organizações e espaços do Cloud Foundry e permissões de acesso independentes. No entanto, uma grande diferença é que cada conta em uma empresa não gerencia seu próprio faturamento ou pagamentos porque eles são manipulados no nível de conta corporativa.

Você cria camadas em sua empresa aninhando um grupo de contas dentro de um grupo de contas. ![Um diagrama que mostra quatro camadas corporativas. A camada principal é a corporativa, que contém duas camadas de grupos de contas. Em seguida, o grupo de contas contém contas.](images/enterprise-hierarchy.svg "As camadas corporativas são criadas incluindo grupos de contas.")

Uma empresa pode conter até 10 camadas de contas e grupos de contas. Em sua forma mais básica, uma empresa possui duas camadas: a conta corporativa e uma conta-filha única.

Sua estrutura corporativa é flexível e pode crescer e mudar conforme suas necessidades. É possível incluir e remover grupos de contas e mover contas entre os grupos de contas. Se o propósito de um grupo de contas mudar, será possível renomeá-lo para refletir melhor as contas que ele contém.

## Faturamento consolidado
{: #enterprise-billing}

Em uma empresa, todos os faturamentos são gerenciados por meio da conta corporativa de nível superior. As empresas requerem [faturamento de assinatura](/docs/account?topic=account-accounts#subscription-account), o que significa que você adquire uma assinatura por uma quantia de crédito para gastar durante o prazo de assinatura, e o uso é deduzido do crédito de assinatura a uma taxa descontada. O crédito de assinatura, assim como o crédito de quaisquer promoções, é incluído no conjunto de crédito corporativo, que é compartilhado entre todas as contas na empresa. Conforme as contas usam os recursos, o crédito é gasto do conjunto de crédito.

![Um diagrama que mostra que o crédito das contas é incluído no conjunto de crédito corporativo, que é gerenciado pelo administrador de faturamento na conta corporativa.](images/enterprise-billing.svg "O faturamento para todas as contas é gerenciado pelo administrador de faturamento na conta corporativa.")

Como o faturamento é consolidado, as empresas tornam o gerenciamento de faturamento e pagamentos em múltiplas contas mais fácil com esses principais benefícios:
* Um conjunto de crédito de assinaturas que se estende por múltiplas contas, para que seja possível dimensionar suas assinaturas para todo o uso em vez de uso por conta
* Uma única fatura para todo o uso dentro da empresa, portanto, o entendimento dos custos é mais fácil
* Um único local para gerenciar os métodos de pagamento, para que seja possível atualizar uma vez para todas as contas

Saiba mais em [Gerenciar centralmente o faturamento e o uso com empresas](/docs/billing-usage?topic=billing-usage-enterprise).

## Gerenciamento de recursos
{: #enterprise-resources}

Recursos e serviços em uma empresa funcionam da mesma forma que em contas independentes. Cada conta em uma empresa pode conter recursos em grupos de recursos e serviços em organizações e espaços do Cloud Foundry. Os grupos de contas não podem conter recursos. Para obter mais informações, consulte [Trabalhando com recursos e serviços](/docs/resources?topic=resources-resource).

![Um diagrama que mostra que os recursos estão contidos em contas na empresa.](images/enterprise-resources.svg "Os recursos são ligados à conta na empresa, assim como uma conta independente.")

Assim como com todas as contas, os recursos são ligados ao grupo de recursos e à conta em que eles são criados, portanto, não podem ser movidos entre as contas na empresa. No entanto, a estrutura de conta flexível da empresa significa que é possível mover recursos dentro da empresa movendo as contas que os contêm.

## Relatório de uso descendente
{: #enterprise-usage}

Na conta corporativa, é possível visualizar o uso do recurso de todas as contas na empresa. No nível corporativo, você vê os custos de uso estimados que são divididos por conta e grupos de contas. É possível navegar para baixo dentro da estrutura corporativa para ver os custos em cada nível. No nível de conta, os usuários corporativos podem visualizar custos para cada tipo de recurso ou serviço na conta.

Como o acesso na empresa é separado do acesso em cada conta, os usuários corporativos não podem criar nem gerenciar automaticamente os recursos dentro das contas-filhas. Da mesma forma, os usuários em cada conta podem continuar visualizando seu uso passado e atual na página Uso, independentemente de eles terem acesso corporativo.

Para obter mais informações, consulte [Visualizando o uso em uma empresa](/docs/billing-usage?topic=billing-usage-enterprise-usage).

## Gerenciamento de acesso e de usuário isolado
{: #enterprise-access}

As empresas mantêm o gerenciamento de usuário e acesso isolado entre a empresa e suas contas-filhas para fornecer maior segurança para os dados de suas contas. Os usuários e seu acesso designado na conta corporativa são completamente separados daqueles nas contas-filhas, e nenhum acesso é herdado automaticamente entre os dois tipos de contas.

As listas de usuários para cada conta são visíveis apenas para os usuários que são convidados para essa conta. Apenas porque um usuário é convidado e recebe acesso para gerenciar a empresa inteira, isso não significa que ele possa visualizar os usuários convidados para cada conta-filha. O gerenciamento de usuário em cada empresa e cada conta é totalmente separado e deve ser gerenciado pelo proprietário da conta ou por um usuário, dada a função de Administrador no Serviço de gerenciamento de conta de gerenciamento de usuário na conta específica.

Semelhante a como o gerenciamento de usuário é totalmente separado em cada conta e a própria empresa, assim é o gerenciamento de acesso. Essa separação significa que os usuários que gerenciam sua empresa não podem acessar os recursos da conta dentro das contas-filhas, a menos que você especificamente permita que eles façam isso. Por exemplo, seu executivo financeiro pode ter a função de Administrador no Serviço de gerenciamento de conta de faturamento dentro da conta corporativa, que fornece a eles acesso às informações de faturamento e pagamento e dados de uso para o tipo de recurso. Mas, a menos que eles sejam convidados para uma conta-filha e tenham acesso designado ao Serviço de gerenciamento de conta de faturamento para essa conta, eles não podem visualizar ofertas nem atualizar os limites de gastos para a conta-filha.

Para obter mais informações, consulte [Gerenciamento de usuários para empresas](/docs/iam?topic=iam-enterprise-access).

## Como posso usar uma empresa?
{: #enterprise-use-cases}

As empresas podem ajudar a simplificar o gerenciamento de conta e faturamento para cenários complexos diferentes. As empresas podem ser benéficas para gerenciar qualquer organização grande, mas dois casos de uso primário nos quais você pode desejar criá-los são empresas grandes e instituições educacionais.

Como você estrutura a sua empresa depende de como você deseja analisar o uso e os custos, como estornar o uso para um grupo específico. Organize sua empresa de acordo com o que você deseja rastrear e gerencie o faturamento e o uso.
{:tip}

### Grandes empresas ou organizações
{: #enterprise-orgs}

As empresas podem ser valiosas para organizações grandes que, de outra forma, requerem múltiplas contas separadas para seus departamentos ou equipes. Usando os grupos de contas, é possível modelar sua hierarquia corporativa de acordo com a estrutura de sua organização.

#### Organizar por departamento
{: #enterprise-by-dept}

Se a sua organização tiver equipes globais que compartilhem um orçamento, será possível modelar sua estrutura corporativa de acordo com seus departamentos. Com essa estrutura, é possível visualizar os custos de uso que são agregados para cada departamento.

![Uma empresa de quatro camadas que agrupa contas de acordo com o departamento em uma organização. Por exemplo, os grupos de contas são chamados Marketing, Desenvolvimento e Vendas. Os grupos de contas contêm contas para equipes dentro desses departamentos. Por exemplo, o grupo de contas Vendas contém contas para Direto, On-line e Ativação.](images/enterprise-by-dept.svg "Uma empresa que organiza contas de acordo com o departamento na organização.")

#### Organizar por geografia
{: #enterprise-by-geo}

Ou, se a sua organização tiver orçamentos separados por geografia, será possível estruturar sua empresa para agrupar custos para cada entidade geográfica.

![Uma empresa de quatro camadas que agrupa contas de acordo com a geografia. Por exemplo, os grupos de contas são chamados Américas, Europa e Ásia-Pacífico. Os grupos de contas contêm contas para países dentro dessas localizações. Por exemplo, o grupo de contas Ásia-Pacífico contém contas para China, Japão e Índia.](images/enterprise-by-geo.svg "Uma empresa que organiza contas de acordo com a geografia.")

### Instituições educacionais
{: #enterprise-edu}

As instituições educacionais podem desejar fornecer contas do {{site.data.keyword.Bluemix_notm}} para seus estudantes para que eles possam aprender habilidades valiosas por meio de projetos práticos que usam serviços do {{site.data.keyword.Bluemix_notm}}. Para essas instituições, como universidades tradicionais ou plataformas de aprendizado on-line, é possível agrupar contas por departamento ou área de assunto e, em seguida, criar contas para cada curso.

Dentro de cada conta, os estudantes podem criar recursos para construir seus projetos e colaborar com outros estudantes na conta. A universidade tem uma visão completa dos custos de cada departamento e curso.

![Uma empresa de três camadas que modela como uma universidade pode organizar suas contas. Por exemplo, os grupos de contas são chamados para cada departamento: Ciência de dados, Ciência da computação e Engenharia de computação. Cada grupo de contas contém contas individuais para cada classe, como DS101 e DS102.](images/enterprise-edu.svg "Uma empresa para uma universidade que possui grupos de contas para cada departamento e contas individuais para cada classe.")
