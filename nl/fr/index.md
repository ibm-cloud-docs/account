---

copyright:

  years: 2015, 2018
lastupdated: "2018-03-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Types de compte
{: #accounts}

Vous pouvez commencer à construire des applications dans {{site.data.keyword.Bluemix}} gratuitement. Vous avez le choix entre trois types de compte différents : Lite, Paiement à la carte et Abonnement. Vous pouvez utiliser l'un de ces types de compte pour vous initier à {{site.data.keyword.Bluemix_notm}} - choisissez simplement le plus adapté à vos besoins.
{:shortdesc}

## Comparaison des types de compte
{: #compare}

Le tableau suivant compare les types de compte Lite, Paiement à la carte et Abonnement. Pour plus de détails sur chaque compte, voir les sections qui suivent.

|  | Lite  | Paiement à la carte | Abonnement |
|--------------------|--------------------|--------------------|--------------------|
| **Accès à la mémoire Cloud Foundry gratuite** | 256 Mo | 512 Mo | 512 Mo |
| **Accès aux [plans de service Lite ![External link icon](../icons/launch-glyph.svg "External link icon")](https://console.bluemix.net/catalog/?search=label:lite){: new_window}** | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Accès à tous les plans gratuits** |  | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Accès à l'intégralité du catalogue** |  | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Accès à plusieurs régions Cloud Foundry** |  | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Sans restrictions de temps** | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Gratuité garantie** | ![Fonction disponible](../icons/icon_enabled.svg) |  |  |
| **Tarification négociée** |  |  | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Idéal pour l'apprentissage ou la génération de POC** | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |  |
| **Adapté aux scénarios de production** |  | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
{: caption="Tableau 1. Comparaison des comptes {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Compte Lite
{: #liteaccount}

Inscrivez-vous pour un compte Lite gratuit afin de construire des applications et d'explorer des services associés à des plans Lite gratuits affichés avec un indicateur Lite ![Indicateur Lite](../icons/Lite.svg) dans la console {{site.data.keyword.Bluemix_notm}}. Votre compte Lite n'expire pas et votre carte de crédit n'est pas nécessaire.

Vous avez accès à un seul groupe de ressources, créé pour vous et nommé `Default`. Toutes vos instances de service gérées par {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) sont automatiquement ajoutées à ce groupe de ressources. Vous pouvez mettre à jour ce groupe de ressources à tout moment. Pour la procédure détaillée, voir [Changement de nom d'un groupe de ressources](/docs/account/resourcegroups.html#renaming-a-resource-group).

Chaque groupe de ressources est gratuit. Lorsque vous créez une connexion entre un service géré par IAM et une application Cloud Foundry, vous créez un alias, qui est une instance de service comptabilisée dans votre quota. Voir [Qu'est-ce qu'un alias ?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

### Quelles sont les disponibilités ?

Vous vous demandez sûrement ce que comporte l'offre de compte Lite. La liste suivante en répertorie les principales fonctions :

   * Le compte est gratuit - Pas besoin de carte de crédit.
   * Le compte n'expire jamais.
   * Vous pouvez utiliser une organisation dans une seule région {{site.data.keyword.Bluemix_notm}}.
   * Support de base {{site.data.keyword.Bluemix_notm}} gratuit. Le support de base est assuré pour les environnements non destinés à la production ou les charges de travail pour lesquels les niveaux de gravité traditionnels ne sont pas utilisés et des temps de réponse spécifiques ne sont pas stipulés.
   * Des notifications vous sont envoyées par courrier électronique quant au statut de votre compte et à vos limites de quota.
   * Vos applications Cloud Foundry ont accès à 256 Mo de mémoire d'exécution gratuite et instantanée.
   * Vous pouvez mettre à disposition une instance de n'importe quel service du catalogue [{{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window} doté d'un plan Lite.
   * Après 10 jours sans activité de développement, vos applications passent en veille. Vous pouvez commencer à travailler sur de nouvelles applications sans vous soucier d'atteindre les limites de quota de mémoire.
   * Après 30 jours sans activité de développement, vos instances de service non associées à des plans Lite sont supprimées. Ainsi, vous n'avez pas à gérer la suppression des instances inactives avant d'en créer de nouvelles.

### Mise à niveau de votre compte

Lorsque vous êtes prêt à aller plus loin, effectuez une mise à niveau vers un compte Paiement à la carte et ne payez que ce que vous utilisez au-delà des franchises. Après la mise à niveau, vous pouvez continuer à utiliser les instances que vous avez créées avec votre compte Lite. Dans la console, accédez à **Gérer** > **Facturation et utilisation** > **Facturation** et cliquez sur **Ajouter une carte de crédit**. 

## Comptes facturables
{: #billableacts}

Le tableau suivant recense les différents types de compte et leurs méthodes de facturation.

|Type de compte |	Comment suis-je facturé ? |
|------------------|-----------------------|
|Paiement à la carte |	Les frais sont facturés d'après votre utilisation des ressources de calcul et des services {{site.data.keyword.Bluemix_notm}} |
|Abonnement | Vous pouvez bénéficier d'une réduction mensuelle avec un engagement de consommation mensuelle minimum |
| {{site.data.keyword.Bluemix_dedicated_notm}} | Contrat annuel |
|{{site.data.keyword.Bluemix_local_notm}} |	Contrat annuel |
{:caption="Tableau 2. Comptes {{site.data.keyword.Bluemix_notm}} facturables et redevances" caption-side="top"}

Si vous liez votre compte {{site.data.keyword.Bluemix_notm}} facturable à un compte SoftLayer, à compter du premier jour du mois suivant, les deux redevances sont regroupées sur votre facture {{site.data.keyword.Bluemix_notm}}. Pour plus d'informations, voir [Affichage des crédits](/docs/billing-usage/viewing_usage.html#credits).
{: tip}

### Compte Paiement à la carte

Avec un compte Paiement à la carte, vous pouvez créer plusieurs groupes de ressources de manière à faciliter la gestion du quota et l'affichage de la facturation d'utilisation d'un ensemble de ressources. Vous êtes éligible pour des environnements d'exécution gratuits et des franchises de services. Si vous utilisez plus que la franchise, vous recevrez une facture {{site.data.keyword.Bluemix_notm}} mensuelle. Celle-ci est en dollars américains (USD) et détaille le prix des ressources.

Dans de nombreux pays et régions, vous pouvez créer un compte Paiement à la carte depuis la console {{site.data.keyword.Bluemix_notm}}. Après avoir fourni vos informations de facturation et de carte de crédit, acceptez les dispositions du contrat et soumettez votre demande de compte. Votre carte de crédit sera alors validée. Vous recevrez également un courrier électronique de confirmation concernant les informations relatives au compte. Quelques minutes après la réception du courrier électronique de confirmation, vous pouvez revenir dans la console pour continuer à construire vos applications. 

Si votre demande en ligne ne peut pas être traitée pour votre pays ou votre région, contactez le [support {{site.data.keyword.Bluemix_notm}}](https://ibm.biz/bluemixsupport){: new_window} ![External link icon](../icons/launch-glyph.svg). Une fois que vous êtes connecté au portail des services {{site.data.keyword.Bluemix_notm}}, cliquez sur **Contacter le support** et sélectionner l'option **Facturation, Compte ou Connexion**.

Vous pouvez convertir votre compte Paiement à la carte en compte d'abonnement à tout moment. Contactez le [Service commercial {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) pour plus de détails.
{: tip}

### Compte d'abonnement

Avec un compte d'abonnement, vous pouvez créer plusieurs groupes de ressources de manière à faciliter la gestion du quota et l'affichage de la facturation d'utilisation d'un ensemble de ressources.

Vous vous engagez à dépenser une somme minimale par mois et recevez une remise sur abonnement qui est appliquée à ce montant minimal. Vous payez également toute utilisation dépassant le montant minimal.

Pour souscrire à un compte Abonnement et obtenir plus d'informations sur les tarifs et les remises associés à ces comptes, vous devez contacter le [service commercial {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg).

### Compte {{site.data.keyword.Bluemix_dedicated_notm}}

{{site.data.keyword.Bluemix_dedicated_notm}} exige un engagement minimal d'un an qui inclut :

   * Une connectivité du réseau privé virtuel vers votre infrastructure
   * Un environnement entièrement redondant dans un centre de données {{site.data.keyword.BluSoftLayer_notm}}
   * Tous les contextes d'exécution pris en charge (IBM Java Liberty, Node.js et des contextes d'exécution open source intégrés)
   * Tous les services dédiés que vous avez sélectionnés et tous les services {{site.data.keyword.Bluemix_notm}}
publics
   * Le support {{site.data.keyword.Bluemix_notm}} standard

Vous pouvez aussi
commander des éléments facultatifs tels que SoftLayer DirectLink ou des options de support premium. Contactez le [service commercial {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External  link icon](../icons/launch-glyph.svg) pour plus d'informations.

Le prix que vous payez chaque mois au cours de cet engagement dépend des services dédiés que vous choisissez et inclut un compte d'abonnement qui vous permet d'accéder à tous les services publics. Le prix de l'utilisation des services dans l'environnement {{site.data.keyword.Bluemix_notm}} public est calculé selon votre contrat de compte d'abonnement. Vous recevez une facture pour tous les services que vous utilisez au-delà de la franchise
définie dans le contrat d'abonnement. Contactez votre représentant de compte IBM ou le [service commercial {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) pour mettre en oeuvre votre contrat.

### Compte {{site.data.keyword.Bluemix_local_notm}}

{{site.data.keyword.Bluemix_local_notm}} exige un engagement minimal d'un an qui inclut :

   * Une fonction de distribution appelée relais qui permet à IBM de se connecter à votre déploiement local et de distribuer des mises à jour
automatiquement et de manière cohérente
   * Tous les contextes d'exécution pris en charge (IBM Java Liberty, Node.js et des contextes d'exécution open source intégrés)
   * Tous les services locaux que vous avez sélectionnés, ainsi que l'accès à tous
les services {{site.data.keyword.Bluemix_notm}} publics
   * Le support {{site.data.keyword.Bluemix_notm}} standard

Le prix que vous payez chaque mois au cours de cet engagement dépend des services locaux que vous choisissez et inclut un compte d'abonnement qui vous permet d'accéder à tous les services publics. Le prix de l'utilisation des services dans l'environnement {{site.data.keyword.Bluemix_notm}} public est calculé selon votre contrat de compte d'abonnement. Vous recevez une facture pour tous les services que vous utilisez au-delà de la franchise
définie dans le contrat d'abonnement. Contactez votre représentant de compte IBM ou le [service commercial {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) pour mettre en oeuvre votre contrat.

## Compte d'essai
{: #trial}

Les comptes de type Trial sont disponibles dans toutes les régions. Ce compte d'essai gratuit de 30 jours vous permet de commencer de suite à construire vos applications et à explorer des services dans {{site.data.keyword.Bluemix_notm}}.

Lorsque vous vous inscrivez pour un essai gratuit avec votre ID {{site.data.keyword.Bluemix_notm}}, votre compte est doté gratuitement des ressources suivantes :

  * 2 Go de mémoire maximum
  * 10 services
  * 1 certificat SSL

Vous avez également accès à un unique groupe de ressources, créé pour vous et nommé `Default`. Toutes vos instances de service gérées par IAM sont automatiquement ajoutées à ce groupe de ressources. Vous pouvez mettre à jour ce groupe de ressources à tout moment. Pour la procédure détaillée, voir [Changement de nom d'un groupe de ressources](/docs/account/resourcegroups.html#renaming-a-resource-group).

Chaque groupe de ressources est gratuit. Lorsque vous créez une connexion entre un service géré par IAM et une application Cloud Foundry, vous créez un alias, qui est une instance de service comptabilisée dans votre quota. Voir [Qu'est-ce qu'un alias ?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

### Que se passe-t-il à la fin de la période d'essai gratuite ?
{: #trialend}

Votre essai gratuit prend fin 30 jours après votre inscription et les applications de votre compte sont alors arrêtées. Vous ne pouvez pas vous inscrire pour un autre compte {{site.data.keyword.Bluemix_notm}}, mais pouvez néanmoins continuer à accéder à votre compte et aux comptes dans lesquels vous avez été invité.

Pour redémarrer vos applications, convertissez votre compte en compte payant, soit en fournissant vos informations de carte de crédit pour souscrire à un compte de type Paiement à la carte, soit en créant un compte d'abonnement. Vous pouvez ensuite continuer à utiliser vos franchises de calcul et de services. Vous n'êtes facturé alors que pour l'utilisation de services, de conteneurs et d'environnements d'exécution non couverts par votre franchise mensuelle gratuite.

  * Pour effectuer une mise à niveau vers un compte Paiement à la carte, accédez à **Gérer** > **Facturation et utilisation** > **Facturation** dans la console, et cliquez sur **Ajouter une carte de crédit**.
  * Pour souscrire à un compte Abonnement, contactez le [service commercial {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg).

Si vous ne convertissez pas votre compte à la fin de la période d'essai gratuit, vos applications et services sont supprimées au bout de 30 jours. Toutefois, votre compte ne sera pas supprimé et vous pourrez vous connecter et effectuer une mise à niveau vers un compte facturable n'importe quand. Vous recevrez également des notifications par courrier électronique pour vous rappeler qu'il vous faut créer un compte facturable pour ne pas perdre vos paramètres d'applications et vos configurations de services. Si vous préférez ne pas recevoir de notifications de {{site.data.keyword.Bluemix_notm}}, vous pouvez vous désabonner à tout moment.

Si vous convertissez votre compte, les franchises sont celles normalement proposées par chaque service. Elles
ne sont plus illimitées comme celles proposées par de nombreux services IBM au cours de l'essai gratuit.

