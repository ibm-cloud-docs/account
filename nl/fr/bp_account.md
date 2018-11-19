---

copyright:

  years: 2018
lastupdated: "2018-10-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Meilleures pratiques pour la configuration de votre compte
{: #account_setup}

Les meilleures pratiques constituent les fondements de votre réussite dans votre entreprise de création de ressources. Si vous êtes prêt à déployer des applications en production et à configurer un environnement pour vos développeurs, passez en revue les sections suivantes pour configurer votre compte.
{:shortdesc}

Les meilleures pratiques décrites ci-après concernent essentiellement l'utilisation des services activés par IAM. Actuellement, les services d'{{site.data.keyword.cloud}} ne sont pas tous activés par IAM. Si une instance de service de votre compte appartient à une organisation et un espace Cloud Foundry, les règles, groupes de ressources et groupes d'accès IAM ne s'appliquent pas à cette instance. Vous pouvez tout de même utiliser des organisations et des espaces et des groupes de ressources Cloud Foundry dans votre compte, mais vous devez affecter aux utilisateurs un accès à ces ressources de manière distincte. Pour plus d'informations sur la gestion des organisations et espaces Cloud Foundry, voir [Ajout d'organisations et d'espaces](/docs/account/orgs_spaces.html#orgsspacesusers).
{: tip}

## Qu'est-ce qu'une bonne stratégie de groupe de ressources ?
{: #resource-group-strategy}

Dans la mesure où un groupe de ressources est un conteneur logique de ressources, utiliser un groupe de ressources par environnement de projet est un bon début. Cette stratégie permet aux administrateurs de contrôler et d'afficher l'utilisation des ressources au niveau de l'environnement de projet. Par exemple, un projet typique comprend des environnements de développement, de test et de production. Par conséquent, un projet nommé `CustApp` comporterait les groupes de ressources suivants :

* CustApp-Dev
* CustApp-Test
* CustApp-Prod

L'accès peut ensuite être accordé aux utilisateurs. Par exemple, un développeur dispose généralement de droits d'accès plutôt étendus au groupe de ressources de développement et des droits d'accès plus restreints, voir inexistants, au groupe de ressources de production. 

Si vous disposez d'un compte Paiement à la carte ou Abonnement, vous pouvez créer des groupes de ressources supplémentaires : 

1. Accédez à **Gérer** &gt; **Compte** &gt; **Groupes de ressources**.
2. Cliquez sur **Créer un groupe de ressources**.
3. Entrez le nom de votre groupe de ressources.
4. Cliquez sur **Ajouter**.

## Configuration de vos groupes de ressources
{: #setting-up-rgs}

Les groupes de ressources sont un conteneur logique vous permettant d'organiser vos ressources activées par IAM. Tous les services qui sont gérés à l'aide du contrôle d'accès IAM appartiennent à un groupe de ressources. Vous affectez une ressource à son groupe de ressources lorsque vous le créez à partir du catalogue. Vous ne pouvez pas modifier l'affectation de groupe de ressources après l'avoir définie, et c'est pourquoi il est important de configurer certains de vos groupes de ressources dès maintenant. 

Si vous disposez d'un compte d'essai ou d'un compte Lite, vous utilisez le groupe de ressources par défaut et vous ne pouvez pas en créer d'autres.
{: tip}

## Ajout de ressources à un groupe de ressources
{: #adding-resources}

Lorsque vous créez une resource activée pour IAM depuis le catalogue, le groupe de ressources que vous souhaitez lui affecter doit être sélectionné. Une fois qu'une ressource est créée, vous ne pouvez pas modifier le groupe de ressources auquel elle est affectée. En cas d'erreur à ce stade, vous devez supprimer la ressource et en créer une nouvelle. 

### Droits d'accès requis pour l'ajout d'une ressource à un groupe de ressources
{: #rg_access}

Le propriétaire de compte {{site.data.keyword.cloud_notm}} peut ajouter des ressources à n'importe quel groupe de ressources. Toutefois, les droits d'accès doivent être accordés aux autres utilisateurs à l'aide d'une règle d'accès IAM. Les deux rôles de gestion de plateforme minimum qui doivent être affectés aux utilisateurs pour leur permettre d'ajouter des ressources à un groupe de ressources sont les suivants :

* Rôle Afficheur ou supérieur sur le groupe de ressources lui-même
* Rôle Editeur ou supérieur sur la ressource ou le service

Pour ajouter une ressource à un groupe de ressources, procédez comme suit :

1. Accédez à **Gérer** &gt; **Compte** &gt; **Groupes de ressources**.
2. Cliquez sur l'icône Plus d'actions ![icône Plus d'actions](../icons/overflow-menu.svg) pour le groupe de ressources auquel vous souhaitez ajouter des ressources et sélectionnez **Ajouter des ressources**.
3. Lorsque vous êtes redirigé vers le catalogue, sélectionnez la ressource que vous souhaitez ajouter. 
4. Sélectionnez le groupe de ressources auquel vous souhaitez l'affecter. 
5. Cliquez sur **Créer**.

Vous pouvez toujours accéder directement au catalogue pour créer des ressources et les affecter à un groupe de ressources.
{: tip} 

Pour plus d'informations, voir [Meilleures pratiques pour l'organisation des ressources dans un groupe de ressources](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).

## Etapes suivantes

Configurez des groupes d'accès pour les utilisateurs et les ID de service qui requièrent le même accès aux ressources et aux groupes de ressources dans votre compte. Vous pouvez affecter un nombre minimal de règles d'accès, afin de gagner du temps. Pour plus d'informations, voir [Meilleures pratiques pour l'affectation d'accès](/docs/iam/bp_access.html).

Consultez [Meilleures pratiques pour l'organisation des utilisateurs, des équipes et des applications](/docs/tutorials/users-teams-applications.html#best-practices-for-organizing-users-teams-applications) pour plus d'informations sur la configuration d'utilisateurs et d'équipes dans votre compte. 
