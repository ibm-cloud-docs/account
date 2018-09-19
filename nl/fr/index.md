---

copyright:

  years: 2015, 2018
lastupdated: "2018-09-04"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Types de compte
{: #accounts}

Vous avez le choix entre trois types de compte {{site.data.keyword.Bluemix}} : Lite, Paiement à la carte et Abonnement. Vous pouvez utiliser l'un de ces types de compte lorsque vous commencez à utiliser {{site.data.keyword.Bluemix_notm}}. Choisissez simplement le plus adapté à vos besoins.
{:shortdesc}

## Comparaison des comptes
{: #compare}

Le tableau suivant compare les types de compte Lite, Paiement à la carte et Abonnement. Pour plus de détails sur chaque compte, voir les sections qui suivent.

|  | Lite  | Paiement à la carte | Abonnement |
|--------------------|--------------------|--------------------|--------------------|
| **Accès à la mémoire Cloud Foundry gratuite** | 256 Mo | 512 Mo | 512 Mo |
| **Accès aux [plans de service Lite ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.bluemix.net/catalog/?search=label:lite){: new_window}** | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Accès à tous les plans gratuits** |  | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Accès à l'intégralité du catalogue {{site.data.keyword.Bluemix_notm}}** |  | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Accès à plusieurs régions Cloud Foundry** |  | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Sans restrictions de temps** | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Gratuité garantie** | ![Fonction disponible](../icons/icon_enabled.svg) |  |  |
| **Remise sur la tarification** |  |  | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Idéal pour l'apprentissage ou la génération de validation de concept** | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |  |
| **Adapté aux scénarios de production** |  | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
{: caption="Tableau 1. Comparaison des comptes {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Compte Lite
{: #liteaccount}

Inscrivez-vous pour un compte Lite gratuit afin de construire des applications et d'explorer des services associés à des plans Lite gratuits signalés par l'indicateur Lite ![Balise Lite](../icons/Lite.svg) dans la console {{site.data.keyword.Bluemix_notm}}. Votre compte Lite n'expire pas et votre carte de crédit n'est pas nécessaire.

Vous avez accès à un seul groupe de ressources, créé pour vous et nommé `Default`. Toutes vos instances de service gérées par {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) sont automatiquement ajoutées à ce groupe de ressources. Vous pouvez mettre à jour ce groupe de ressources à tout moment. Pour la procédure détaillée, voir [Changement de nom d'un groupe de ressources](/docs/resources/resourcegroups.html#renaming-a-resource-group).

Chaque groupe de ressources est gratuit. Lorsque vous créez une connexion entre un service géré par IAM et une application Cloud Foundry, vous créez un alias, qui est une instance de service comptabilisée dans votre quota. Voir [Qu'est-ce qu'un alias ?](/docs/resources/connecting_apps.html#what_is_alias).
{: tip}

### Quelles sont les disponibilités ?

La liste suivante répertorie les principales fonctions disponibles dans un compte Lite :

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
{: #upgrade-to-paygo}

Lorsque vous êtes prêt à aller plus loin, vous pouvez effectuer une mise à niveau de votre compte vers un compte Paiement à la carte ou un compte Abonnement. 

  * Pour effectuer une mise à niveau vers un compte Paiement à la carte, accédez à **Gérer** > **Facturation et utilisation** > **Facturation** dans la console puis cliquez sur **Ajouter une carte de crédit**.
  * Pour effectuer une mise à niveau vers un compte Abonnement, accédez à **Gérer** > **Facturation et utilisation** > **Facturation** dans la console puis cliquez sur **En savoir plus**.

## Compte Paiement à la carte
{: #paygo}

Avec un compte Paiement à la carte, vous pouvez créer plusieurs groupes de ressources de manière à faciliter la gestion du quota et l'affichage de la facturation d'utilisation d'un ensemble de ressources. Les frais sont facturés d'après votre utilisation des ressources de calcul et des services {{site.data.keyword.Bluemix_notm}} Vous êtes éligible pour des environnements d'exécution gratuits et des franchises de services. Si vous dépassez la franchise, vous recevrez une facture {{site.data.keyword.Bluemix_notm}} mensuelle. Celle-ci est facturée en dollars américains (USD) et détaille les ressources facturées.

Si vous liez votre compte Paiement à la carte à un compte SoftLayer, à compter du premier jour du mois suivant, les deux redevances seront regroupées sur votre facture {{site.data.keyword.Bluemix_notm}}.
{: tip}

Vous pouvez effectuer une mise à niveau vers un compte Paiement à la carte depuis la console {{site.data.keyword.Bluemix_notm}}. Après avoir fourni vos informations de facturation et de carte de crédit, acceptez les dispositions du contrat et soumettez votre demande de compte. Votre carte de crédit sera alors validée. Vous recevrez également un courrier électronique de confirmation concernant les informations relatives au compte. Quelques minutes après la réception du courrier électronique de confirmation, vous pouvez revenir dans la console pour continuer à construire vos applications. Si votre demande en ligne ne peut pas être traitée pour votre pays ou votre région, contactez le [Support {{site.data.keyword.Bluemix_notm}}](/docs/get-support/howtogetsupport.html).

Vous bénéficiez d'un crédit promotionnel de 200 $ après la mise à niveau vers un compte Paiement à la carte. Ce crédit est automatiquement appliqué à votre compte. Votre crédit de 200 $ est valide pendant 30 jours et est automatiquement pris en compte dans votre facture. Ce crédit ne peut pas être utilisé sur des offres de tiers.

### Mise à niveau de votre compte
{: #upgrade-to-subscription}

Vous pouvez mettre à niveau votre compte Paiement à la carte vers un compte Abonnement à tout moment. Contactez le [Service commercial {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg) pour plus de détails.

## Compte d'abonnement

Avec un compte d'abonnement, vous pouvez créer plusieurs groupes de ressources de manière à faciliter la gestion du quota et l'affichage de la facturation d'utilisation d'un ensemble de ressources. Vous vous engagez à dépenser une somme minimale combinée par mois et recevez une remise sur abonnement qui est appliquée à ce montant minimal. Vous êtes facturé au tarif plein pour toute utilisation au-delà du montant total de votre abonnement.

Si vous avez un compte d'abonnement, vous pouvez créer la plupart des services disponibles dans le [catalogue IBM Cloud](https://console.bluemix.net/catalog/). Toutefois, il peut être nécessaire d'acheter séparément certains services utilisant un plan de tarification spécifique.

Si vous liez votre compte Abonnement à un compte SoftLayer, à compter du premier jour du mois suivant, les deux redevances seront regroupées sur votre facture {{site.data.keyword.Bluemix_notm}}.
{: tip}

### Compte {{site.data.keyword.Bluemix_dedicated_notm}}

{{site.data.keyword.Bluemix_dedicated_notm}} exige un engagement minimal d'un an qui inclut :

   * Une connectivité du réseau privé virtuel vers votre infrastructure
   * Un environnement entièrement redondant dans un centre de données {{site.data.keyword.BluSoftlayer_notm}}
   * Tous les contextes d'exécution pris en charge (IBM Java Liberty, Node.js et des contextes d'exécution open source intégrés)
   * Tous les services dédiés que vous avez sélectionnés et tous les services {{site.data.keyword.Bluemix_notm}} publics
   * Le support {{site.data.keyword.Bluemix_notm}} standard

Vous pouvez aussi
commander des éléments facultatifs tels que SoftLayer DirectLink ou des options de support premium. Contactez le [service commercial {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg) pour plus d'informations.

Le prix que vous payez chaque mois au cours de cet engagement dépend des services dédiés que vous choisissez et inclut un compte d'abonnement qui vous permet d'accéder à tous les services publics. Le prix de l'utilisation des services dans l'environnement {{site.data.keyword.Bluemix_notm}} public est calculé selon votre contrat de compte d'abonnement. Vous recevez une facture pour tous les services que vous utilisez au-delà de la franchise
définie dans le contrat d'abonnement. Contactez votre représentant de compte IBM ou le [service commercial {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg) pour mettre en oeuvre votre contrat.

### Compte {{site.data.keyword.Bluemix_local_notm}}

{{site.data.keyword.Bluemix_local_notm}} exige un engagement minimal d'un an qui inclut :

   * Une fonction de distribution appelée relais qui permet à IBM de se connecter à votre déploiement local et de distribuer des mises à jour automatiquement et de manière cohérente
   * Tous les contextes d'exécution pris en charge (IBM Java Liberty, Node.js et des contextes d'exécution open source intégrés)
   * Tous les services locaux que vous avez sélectionnés, ainsi que l'accès à tous les services {{site.data.keyword.Bluemix_notm}} publics
   * Le support {{site.data.keyword.Bluemix_notm}} standard

Le prix que vous payez chaque mois au cours de cet engagement dépend des services locaux que vous choisissez et inclut un compte d'abonnement qui vous permet d'accéder à tous les services publics. Le prix de l'utilisation des services dans l'environnement {{site.data.keyword.Bluemix_notm}} public est calculé selon votre contrat de compte d'abonnement. Vous recevez une facture pour tous les services que vous utilisez au-delà de la franchise
définie dans le contrat d'abonnement. Contactez votre représentant de compte IBM ou le [service commercial {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg) pour mettre en oeuvre votre contrat.



