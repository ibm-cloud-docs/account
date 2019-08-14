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


# Meilleures pratiques pour la configuration d'une entreprise
{: #enterprise-best-practices}

Les meilleures pratiques suivantes mettent à votre disposition les fondements de votre réussite dans votre entreprise de configuration d'une entreprise {{site.data.keyword.cloud}}.
{:shortdesc}

## Organisation des comptes en fonction du mode de suivi souhaité de la facturation
{: #organize-enterprise-usage}

Un des principaux avantages des entreprises d'{{site.data.keyword.cloud_notm}} réside dans le fait que ces dernières vous permettent de consulter et de gérer centralement la facturation et l'utilisation dans plusieurs comptes. L'utilité de cette fonction dépend de la structure de votre entreprise car les données d'utilisation sont regroupées par compte et groupe de comptes. Créez des groupes de comptes pour les projets qui dépendent du même budget. Voir [Comment puis-je utiliser une entreprise ?](/docs/account?topic=account-enterprise#enterprise-use-cases) pour des exemples.

L'administrateur d'entreprise ou votre responsable financier peut ne pas bien connaître chaque compte individuel ou groupe de comptes. Pour faciliter l'identification de leur rôle, attribuez à chacun d'entre eux un nom significatif. Si votre entreprise utilise des codes de facturation, vous pouvez également les intégrer au nom. Par exemple, au lieu d'utiliser un groupe de comptes `devteam` incluant les comptes `fed ui` et `be api`, créez le groupe de comptes `Développement - A2B3` incluant les comptes `Equipe d'interface utilisateur de front-end` et `Equipe d'API de back-end`.

Un utilisateur d'entreprise disposant de l'accès de type Administrateur ou Editeur peut éditer les noms d'entreprise et de groupe de comptes mais non ceux des comptes. Pour éditer un nom de compte, l'utilisateur doit être dans le compte lui-même.
{:tip}

Etant donné que vous avez une vue unifiée de l'ensemble de l'utilisation organisée par vos comptes et vos groupes de comptes, vous pouvez facturer les coûts aux équipes associées. Pour plus d'informations, voir [Recouvrement des coûts pour l'utilisation de l'entreprise](/docs/billing-usage?topic=billing-usage-enterprise-usage#enterprise-cost-recovery).

## Création d'une hiérarchie d'entreprise cohérente
{: #accounts-vs-groups}

Lorsque vous configurez votre entreprise, vous créez une hiérarchie d'entreprise qui correspond à votre société ou à votre organisation. Lorsque vous créez des comptes et des groupes de comptes, planifiez un schéma cohérent pour le mode d'utilisation des couches d'entreprise suivantes par votre société :
- Groupes de ressources ainsi qu'organisations et espaces Cloud Foundry dans un compte
- Comptes dans un groupe de comptes
- Groupes de comptes dans l'entreprise

Par exemple, votre société peut créer des comptes pour chaque équipe, avec des groupes de ressources ou des organisations Cloud Foundry dans le compte pour les environnements de développement, de test et de production. Une autre société peut avoir des comptes distincts pour chaque environnement, qui sont regroupés dans des groupes de comptes pour chaque équipe.

Lorsque vous choisissez de structurer votre entreprise, soyez le plus cohérent possible pour simplifier la gestion de l'entreprise. 
Etant donné qu'il est facile de créer et d'effectuer le suivi de nouveaux comptes, il peut être tentant de créer un grand nombre de comptes séparés à la demande des utilisateurs. Toutefois, chaque compte génère une charge de gestion supplémentaire. 
Lorsque vous planifiez de structurer votre entreprise, gardez à l'esprit les points suivants :
- Pour chaque compte créé, les utilisateurs doivent être invités et leur accès doit être géré séparément.
- Lorsque la structure est incohérente, il peut être plus difficile de déterminer à qui accorder l'accès dans chaque compte et de déterminer quelle équipe utilise des ressources.
- Les utilisateurs peuvent collaborer sur des ressources et des services uniquement dans un compte individuel. Les ressources ne peuvent pas être déplacées entre différents comptes.

## Configuration des règles d'accès dans une entreprise
{: #access-enterprise}

Comme toujours, suivez les meilleures pratiques pour l'affectation du nombre minimal de règles d'accès et de niveaux d'accès. Ainsi, vous passez moins de temps à affecter l'accès aux utilisateurs et vous pouvez vous concentrer sur le développement dans {{site.data.keyword.cloud_notm}}, tout en vous assurant que vous n'accordez pas trop d'accès aux utilisateurs qui n'en ont pas besoin.

Les groupes d'accès constituent un outil utile pour l'affectation de l'accès à un groupe d'utilisateurs et à des ID de service ayant tous besoin du même accès. En utilisant des groupes d'accès, vous pouvez rationaliser la gestion de l'accès en affectant le nombre minimal de règles d'accès aux groupes d'utilisateurs. Par exemple, si vous souhaitez que vos cinq utilisateurs puissent gérer toutes les tâches liées à la facturation et à la gestion des comptes pour l'entreprise, vous pouvez ajouter ces utilisateurs à un groupe d'accès appelé `Administrateurs`. Dans le groupe d'accès, vous pouvez affecter deux règles : une avec le rôle administrateur sur le service de gestion des comptes Facturation et un autre avec le rôle administrateur sur tous les services de gestion du compte. Lorsque les utilisateurs n'ont plus les mêmes responsabilités ou ne font plus partie des mêmes équipes, vous pouvez ajouter ou retirer des utilisateurs dans le groupe d'accès au lieu d'ajouter ou de retirer les mêmes règles pour les utilisateurs individuels. Voir [Affectation de l'accès d'entreprise](/docs/iam?topic=iam-assign-access-enterprise) pour plus d'informations.

## Utilisation de ressources dans une entreprise
{: #child-resources-enterprise}

Créez des ressources uniquement dans des comptes enfant que vous importez ou créez au sein de l'entreprise. 
Bien qu'il soit possible de créer des ressources au sein du compte d'entreprise, ce n'est pas une pratique recommandée pour les raisons suivantes :
 - Le compte d'entreprise est toujours un enfant direct de l'entreprise et ne peut pas être déplacé. Vous ne pouvez donc pas modifier le mode de signalement de l'utilisation pour les ressources.
 - Le compte d'entreprise contient les utilisateurs et l'accès pour la gestion de l'entreprise et sa facturation. Ainsi, seuls les utilisateurs ayant ces responsabilités doivent être ajoutés au compte.

Les utilisateurs de chaque compte de l'entreprise peuvent créer, utiliser et traiter des ressources comme ils le feraient dans un compte autonome. Pour plus de détails, voir [Utilisation des ressources et des services](/docs/resources?topic=resources-resource). Les utilisateurs d'entreprise ne peuvent pas directement utiliser de ressources dans les comptes enfant mais ils peuvent surveiller les types de ressource et les plans utilisés dans chaque compte en consultant leur utilisation. Pour plus d'informations, voir [Affichage de l'utilisation dans une entreprise](/docs/billing-usage?topic=billing-usage-enterprise-usage).


