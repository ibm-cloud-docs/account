---



copyright:

  years: 2016, 2018
lastupdated: "2017-10-13"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} Standard Account Limited Release
{: #betaintro}

L'édition {{site.data.keyword.Bluemix}} Standard Account Limited Release introduit un nouveau compte gratuit, lequel permet de travailler d'une nouvelle façon dans le cloud public {{site.data.keyword.Bluemix_notm}}. Le compte standard
n'expire jamais, contrairement au compte d'essai {{site.data.keyword.Bluemix_notm}} de 30 jours. Vous pouvez continuer à
utiliser vos applications {{site.data.keyword.Bluemix_notm}}
sans vous soucier des restrictions de temps. 
{:shortdesc}

Les utilisateurs aux Royaume-Uni et dans les régions Sud des Etats-Unis sont éligibles pour un compte Standard. Si vous n'êtes pas situé dans l'une de ces régions, vous pouvez néanmoins créer un compte Standard en demandant à un ami de vous inviter ou en contactant notre équipe commerciale à l'adresse CloudDigitalSales@us.ibm.com. En tant que propriétaire d'un compte Standard, vous pouvez inviter des amis et des collègues à participer.  

## Présentation du compte {{site.data.keyword.Bluemix_notm}} standard
{: #standardaccount}

Vous vous demandez sans doute en quoi le compte Standard diffère du
compte d'essai. Les tableaux suivants récapitulent les détails clés d'un compte {{site.data.keyword.Bluemix_notm}} Standard. 

|Quelles sont les nouveautés du compte standard ? |    
|-----------------|
| Le compte n'expire jamais. |
| Les applications Cloud Foundry peuvent accéder à 256 Mo de mémoire d'exécution instantanée et gratuite. |
| Vous pouvez accéder à des plans Lite gratuits pour des services Watson en demande comme Conversation, Internet of Things Platform, Cloudant NoSQLDB. Pour plus d'informations, voir [Qu'est-ce qui est disponible dans le compte standard ?](/docs/pricing/standard_account.html#whatsavailable). |
| Vos applications passent en veille au bout de dix jours d'inactivité en termes de développement. |
| Vos instances de service sont supprimées au bout de 30 jours d'inactivité. |
{:caption="Tableau 1. Quelles sont les nouveautés du compte standard ?" caption-side="top"}

|Qu'est-ce qui ne change pas quand un compte d'essai est converti ? | 
|-----------------|
|Le compte est gratuit ; vous n'avez pas besoin de carte de crédit. |
|Vous pouvez continuer à utiliser vos instances de plans Lite. |
|Votre organisation, vos espaces et les paramètres d'accès des membres d'équipe associés restent les mêmes. Vous pouvez transférer une organisation vers votre nouveau compte. |
|Le niveau de support {{site.data.keyword.Bluemix_notm}} reste le même. |
{:caption="Tableau 2. Qu'est-ce qui ne change pas ?" caption-side="top"}

**Remarque** : Si votre compte d'essai n'est pas converti, un message s'affiche expliquant pourquoi. Votre compte d'essai comporte peut-être plusieurs organisations ou des applications qui ne peuvent pas être transférées. Effectuez l'action appropriée, puis faites une nouvelle tentative
de conversion.

Lorsque vous possédez un compte Standard, vous pouvez inviter des membres d'équipe à collaborer au sein de votre organisation et de vos espaces, afficher votre utilisation, créer des espaces, mettre à jour votre profil de compte et gérer votre organisation.

## Plans Lite
{: #liteplans}
   
Les plans Lite, également disponibles dans un compte de type Paiement à
la carte, sont structurés sous forme de quota gratuit. Vous pouvez utiliser
vos projets gratuitement, sans risque de générer une facture par accident.
Le quota peut fonctionner pour une période spécifique, par exemple, un mois,
ou sur la base d'une utilisation unique. Voici quelques exemples de quotas de plans Lite :

<ul>
<li>Nombre maximal de périphériques enregistrés</li>
<li>Nombre maximal de liaisons d'application</li>
<li>Limite de stockage de données chiffrées, par exemple, 1 Go</li>
<li>Débit de mise à disposition</li>
</ul> 

Un compte standard vous permet d'utiliser n'importe quel élément du
catalogue {{site.data.keyword.Bluemix_notm}} doté d'un plan Lite. Les
plans Lite sont faciles à trouver. Par défaut, lorsque vous accédez au
catalogue, tous les services dotés d'un plan Lite sont affichés et identifiés par une balise Lite ![balise Lite](../icons/Lite.svg). Sélectionnez un service pour afficher les détails du quota du plan Lite associé.

## Qu'est-ce qui est disponible dans un compte Standard ?
{: #whatsavailable}

Avec un compte standard, vos applications Cloud Foundry peuvent accéder, au maximum, à 256 Mo de mémoire d'exécution instantanée. Si vous dépassez votre quota alloué, vous pouvez arrêter certaines applications afin de libérer de la mémoire d'exécution. Vous pouvez également exploiter un cluster Kubernetes avec 2 UC et 4 Go de mémoire RAM. 

Vous pouvez utiliser n'importe quel service du catalogue {{site.data.keyword.Bluemix_notm}} doté d'un plan Lite. Toutefois, vous ne pouvez mettre à disposition qu'une seule instance par plan Lite. Dans l'édition Standard Account Limited Release, les services suivants proposent un plan Lite :

<ul>
<li>{{site.data.keyword.prf_hublong}}</li>
<li>{{site.data.keyword.mobilepushfull}}</li>
<li>{{site.data.keyword.cloudantfull}}</li>
<li>{{site.data.keyword.conversationfull}}</li>
<li>{{site.data.keyword.iot_full}}</li>
<li>{{site.data.keyword.languagetranslatorfull}}</li>
<li>{{site.data.keyword.personalityinsightsfull}}</li>
<li>{{site.data.keyword.toneanalyzerfull}}</li>
</ul>

Certains services ne sont pas disponibles dans toutes les régions {{site.data.keyword.Bluemix_notm}}. Pour plus d'informations, voir [Services par région](/docs/services/services_region.html#services_region).

Nous étendrons cette liste de services, donc restez à l'écoute !

### Limites de quota

Quand vos limites de quota sont atteintes, votre application est arrêtée
ou votre service est désactivé. Si le plan Lite spécifie que le quota est
fourni sur une base mensuelle, l'utilisation des ressources est réinitialisée
le premier de chaque mois et vous pouvez alors réutiliser le service. Lorsque
vous approchez ou atteignez la limite de quota, vous recevrez un courrier électronique de notification. 

Vous pouvez mettre à disposition 1 instance par plan Lite. 

**Remarque** : Ces limitation s'appliquent à un compte Standard uniquement. Vous pouvez à tout moment procéder à une mise à niveau vers un compte de type Paiement à la carte ou Abonnement. Vous
ne payez que ce que vous utilisez au-delà des franchises. Pour plus d'informations sur les comptes de type Paiement à la carte et Abonnement, voir [Types de compte](/docs/accounts/account-types.html).

## Fonctions d'efficience
{: #devactivity}

Pour vous aider à gérer vos ressources, nous avons inclus des fonctions d'efficience axées sur l'activité de développement et l'utilisation.

### Mise en veille automatique de l'application

Vos applications passent en veille après 10 jours d'inactivité en
termes de développement. Cela facilite l'utilisation d'une nouvelle
application, car vous évitez ainsi  d'atteindre la limite du quota de mémoire
de 256 Mo. 

Pour activer vos applications, commencez à les réutiliser sur la ligne de commande Cloud Foundry ou la console {{site.data.keyword.Bluemix_notm}}. 
 
 Voici la liste de toutes les commandes qui permettent d'activer votre application :
  * cf push
  * cf restate
  * cf restart
  * cf ssh
  * cf scale
  * cf stop
  * cf start
  * cf create-route
  * cf map-route
  * cf unmap-route
  * cf delete-route
  * cf enable-ssh
  * cf disable-ssh

Pour plus d'informations sur l'utilisation de commandes, voir [Commandes Cloud Foundry](/docs/cli/reference/cfcommands/index.html).

 **Remarque** : Si votre application est déjà activée pour SSH, vous ne pouvez pas utiliser les commandes `cf enable-ssh` et `cf disable-sh` pour ranimer votre application. 

### Récupération de place

Vos services de plan Lite sont supprimés en l'absence d'activité pendant 30 jours. Il n'est donc pas nécessaire de supprimer les instances inactives lorsque vous souhaitez en créer une nouvelle. 
 
## Participation au compte Standard Account Limited Release
{: #lgainvitation}

Vous pouvez demander à un ami disposant d'un compte Standard de vous inviter ou contacter notre équipe commerciale à l'adresse CloudDigitalSales@us.ibm.com. Vous êtes le bienvenu si vous désirez l'essayer !

Si vous recevez une invitation d'un ami ou d'un vendeur {{site.data.keyword.Bluemix_notm}}, votre invitation exclusive est envoyée à l'adresse électronique que vous avez fournie. Lorsque vous recevez l'invitation, suivez les instructions du courrier électronique pour vous inscrire pour un compte Standard. 
