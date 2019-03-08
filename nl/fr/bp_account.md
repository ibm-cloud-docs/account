---

copyright:
  years: 2018, 2019
lastupdated: "2019-01-28"

keywords: resource group, account access, user access, IAM, organize

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Meilleures pratiques pour la configuration de votre compte
{: #account_setup}

Les meilleures pratiques suivantes mettent à votre disposition les fondements de votre réussite dans votre entreprise de création de ressources. Si vous êtes prêt à déployer des applications en production et à configurer un environnement pour vos développeurs, passez en revue les sections suivantes pour configurer votre compte.
{:shortdesc}

Les meilleures pratiques décrites ci-après concernent essentiellement l'utilisation des services activés par IAM. Actuellement, les services d'{{site.data.keyword.cloud}} ne sont pas tous activés par IAM. Les règles IAM, les groupes de ressources et les groupes d'accès ne s'appliquent pas aux instances de service qui appartiennent à un espace et à une organisation Cloud Foundry. Vous pouvez tout de même utiliser des groupes de ressources ainsi que des organisations et des espaces Cloud Foundry dans votre compte. Toutefois, vous devez affecter séparément l'accès utilisateur à ces ressources. Pour plus d'informations sur les espaces et les organisations Cloud Foundry, voir [Ajout d'organisations et d'espaces](/docs/account?topic=account-orgsspacesusers).
{: note}

## Qu'est-ce qu'une bonne stratégie de groupe de ressources ?
{: #resource-group-strategy}

Les administrateurs peuvent avoir un meilleur contrôle de l'utilisation des ressources au niveau de l'environnement de projet si un groupe de ressources par environnement de projet est utilisé. Par exemple, un projet typique comprend des environnements de développement, de test et de production. Un projet nommé `CustApp` comporterait les groupes de ressources suivants :

* `CustApp-Dev`
* `CustApp-Test`
* `CustApp-Prod`

Vous pouvez octroyer l'accès aux utilisateurs. Par exemple, un développeur dispose généralement de droits d'accès plutôt étendus au groupe de ressources de développement et de droits d'accès plus restreints, voire inexistants, au groupe de ressources de production.

Si vous disposez d'un compte Paiement à la carte ou Abonnement, vous pouvez créer des groupes de ressources supplémentaires :

1. Accédez à **Gérer** > **Compte** et sélectionnez **Groupes de ressources** dans le menu **Ressources de compte**.
3. Cliquez sur **Créer**.
4. Entrez le nom de votre groupe de ressources.
5. Cliquez sur **Ajouter**.

Pour plus d'informations sur le type de compte vous correspondant le mieux, voir [Types de compte](/docs/account?topic=account-accounts).


## Configuration de vos groupes de ressources
{: #setting-up-rgs}

Les groupes de ressources sont un conteneur logique vous permettant d'organiser vos ressources activées par IAM. Tous les services gérés à l'aide du contrôle d'accès {{site.data.keyword.cloud_notm}} IAM (Identity and Access Management) appartiennent à un groupe de ressources. Vous affectez une ressource à son groupe de ressources lorsque vous le créez à partir du catalogue. Vous ne pouvez pas modifier l'affectation de groupe de ressources après l'avoir définie, et c'est pourquoi il est important de configurer certains de vos groupes de ressources dès maintenant.

Si vous avez un compte Lite, vous avez accès à un groupe de ressources unique créé pour vous. Vous ne pouvez pas créer de groupes de ressources supplémentaires. Pensez à [mettre à niveau votre compte](/docs/account?topic=account-changeacct#changeacct) pour créer et utiliser plusieurs groupes de ressources.
{: note}


## Ajout de ressources à un groupe de ressources
{: #adding-resources}

Vous pouvez ajouter une ressource à un groupe de ressources lorsque vous créez une ressource activée par IAM à partir du catalogue. Lorsque vous sélectionnez la ressource, assurez-vous que le groupe de ressources cible est sélectionné. Une fois qu'une ressource est créée, vous ne pouvez pas changer son groupe de ressources affecté. Si vous affectez par erreur une ressource au groupe de ressources incorrect, supprimez la ressource et créez-en une nouvelle.

### Droits d'accès requis pour l'ajout d'une ressource à un groupe de ressources
{: #rg_access}

En tant que propriétaire de compte, vous pouvez ajouter des ressources à un groupe de ressources. Les droits d'accès doivent être accordés aux autres utilisateurs à l'aide d'une règle d'accès IAM pour ajouter des ressources aux groupes de ressources. Les deux rôles de gestion de plateforme minimum qui doivent être affectés aux utilisateurs pour leur permettre d'ajouter des ressources à un groupe de ressources sont les suivants :

* Rôle Afficheur ou supérieur sur le groupe de ressources
* Rôle Editeur ou supérieur sur la ressource ou le service

Pour ajouter une ressource à un groupe de ressources, procédez comme suit :

1. Accédez à **Gérer > Compte** et sélectionnez **Groupes de ressources**.
2. Cliquez sur l'icône Actions ![Icône Actions](../icons/action-menu-icon.svg) pour le groupe de ressources auquel vous souhaitez ajouter des ressources et sélectionnez **Ajouter des ressources**.
3. Lorsque vous êtes redirigé vers le catalogue, sélectionnez la ressource que vous souhaitez ajouter.
4. Sélectionnez le groupe de ressources auquel vous souhaitez l'affecter.
5. Cliquez sur **Créer**.

Vous pouvez toujours accéder directement au catalogue pour créer des ressources et les affecter à un groupe de ressources.
{: tip}

Pour plus d'informations, voir [Meilleures pratiques pour l'organisation des ressources dans un groupe de ressources](/docs/resources?topic=resources-bp_resourcegroups).


## Utilisation d'étiquettes pour l'organisation des ressources
{: #tags}

Utilisez des étiquettes pour organiser vos ressources et effectuer le suivi des coûts d'utilisation. Vous pouvez marquer à l'aide d'étiquettes les ressources liées puis parcourir votre compte en filtrant par étiquettes depuis votre tableau de bord. Les étiquettes de paire clé:valeur vous permettent d'organiser vos environnements de développement, les projets, la conformité et l'optimisation.

Pour ajouter une étiquette à une ressource, procédez comme suit :

1. Cliquez sur l'icône Menu ![Icône Menu](../icons/icon_hamburger.svg) > **Liste de ressources** pour afficher votre liste de ressources. Recherchez la ressource à étiqueter.
2. Si la ressource comporte déjà une étiquette, survolez l'étiquette existante puis cliquez sur l'icône Editer ![Icône Editer](../icons/edit-tagging.svg). Si la ressource n'inclut pas d'étiquette, survolez **--** dans la colonne `Etiquettes` puis cliquez sur **Ajouter des étiquettes**.
3. Entrez un nom pour l'étiquette puis appuyez sur la touche Entrée après chaque étiquette si vous en ajoutez plusieurs.
4. Pour retirer une étiquette de la ressource, cliquez sur l'icône Retirer ![Icône Retirer](../icons/close-tagging.svg) en regard de l'étiquette.
5. Sauvegardez vos modifications.

Pour plus d'informations sur les ressources pouvant être étiquetées et sur le mode d'affectation de l'accès afin de déléguer la fonctionnalité d'étiquetage aux utilisateurs de votre compte, voir [Utilisation d'étiquettes](/docs/resources?topic=resources-tag).


## Etapes suivantes

Configurez des groupes d'accès pour les utilisateurs et les ID de service qui requièrent le même accès aux ressources et aux groupes de ressources dans votre compte. Vous pouvez affecter un nombre minimal de règles d'accès, afin de gagner du temps. Pour plus d'informations, voir [Meilleures pratiques pour l'affectation d'accès](/docs/iam?topic=iam-cfaccess).
