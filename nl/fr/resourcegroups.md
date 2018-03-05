---



copyright:

  years: 2017, 2018
lastupdated: "2018-02-08"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Gestion des groupes de ressources
{: #rgs}

Un groupe de ressources permet d'organiser vos ressources de compte en regroupements personnalisables de manière à pouvoir affecter rapidement des accès utilisateur à plusieurs ressources à la fois. Chaque ressource de compte gérée à l'aide du contrôle d'accès {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) appartient à un groupe de ressources au sein de votre compte. Les services Cloud Foundry restent affectés à des organisations et des espaces et ne peuvent pas être ajoutés à un groupe de ressources.

Pour démarrer la gestion de vos groupes de ressources, accédez à **Gérer** &gt; **Compte** &gt; **Groupes de ressources** dans la console {{site.data.keyword.Bluemix}}. Vous pouvez alors afficher vos groupes de ressources, les renommer et créer de nouveaux groupes de ressources.

## Affichage des ressources des groupes de ressources

Pour afficher facilement les ressources que contient un groupe de ressources, filtrez par groupe de ressources à partir du tableau de bord.

## Création d'un groupe de ressources

Si vous disposez d'un compte Paiement à la carte ou Abonnement, vous pouvez créer plusieurs groupes de ressources de manière à faciliter la gestion du quota et l'affichage de la facturation d'utilisation d'un ensemble de ressources. Vous pouvez également regrouper des ressources afin de faciliter l'affectation d'accès utilisateur à plusieurs instances à la fois.

Si vous disposez d'un compte Lite ou d'un compte d'essai de 30 jours, vous ne pouvez pas créer de groupes de ressources supplémentaires, mais vous pouvez renommer votre groupe de ressources par défaut. 

Tous les groupes de ressources sont gratuits, en revanche, les connexions entre un groupe de ressources et une organisation ou un espace Cloud Foundry sont décomptées de votre quota de compte. Pour plus d'informations, voir [Qu'est-ce qu'un alias ?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

1. Accédez à **Gérer** &gt; **Compte** &gt; **Groupes de ressources**.
2. Cliquez sur **Créer un groupe de ressources**.
3. Entrez un nom pour le groupe de ressources.
4. Cliquez sur **Ajouter**.

## Modification du nom d'un groupe de ressources

Votre premier groupe de ressources, automatiquement nommé `Default`, est créé. Vous pouvez modifier le nom de ce groupe ou de tout autre groupe que vous créez.

1. Accédez à **Gérer** &gt; **Compte** &gt; **Groupes de ressources**.
2. Cliquez sur **Renommer**.
3. Entrez un nom unique, puis cliquez sur **Sauvegarder**.

## Gestion des groupes de ressources et des ressources à l'aide de l'interface de ligne de commande {{site.data.keyword.Bluemix_notm}}

L'interface de ligne de commande {{site.data.keyword.Bluemix_notm}} propose de nombreuses commandes de gestion des ressources. Pour plus d'informations, voir [Commandes de gestion des groupes de ressources et des ressources](/docs/cli/reference/bluemix_cli/bx_cli.html#commands-for-managing-resource-groups-and-resources).

## Gestion de l'accès à des groupes de ressources

Cloud IAM vous offre la possibilité de fournir un accès utilisateur à granularité fine aux ressources de votre compte. Vous pouvez utiliser Cloud IAM pour affecter à des utilisateurs des règles qui donnent accès à toutes les ressources d'un groupe de ressources, à un seul type de service au sein d'un groupe de ressources ou à une instance de service individuelle du compte. Fournir un accès à des ressources au sein d'un groupe de ressources n'accorde pas aux utilisateurs concernés de droit de gestion du groupe de ressources lui-même. Vous pouvez définir séparément un accès permettant d'afficher, d'éditer et de gérer le groupe de ressources.

Pour plus d'informations sur la gestion des accès aux groupes de ressources, voir [Gestion d'accès IAM](/docs/iam/mngiam.html#iammanidaccser).
