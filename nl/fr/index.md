---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-10"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account, subscription, service bundle

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Types de compte
{: #accounts}

{{site.data.keyword.Bluemix_notm}} propose trois différents types de compte : Lite, Paiement à la carte et Abonnement. Dès que vous vous inscrivez, vous obtenez un compte Lite gratuit. Les comptes Paiement à la carte et Abonnement constituent nos options de compte facturables, chacune d'entre elles proposant différentes fonctions. Comparez chaque compte et choisissez celui qui correspond le mieux à vos besoins.
{:shortdesc}

## Comparaison des comptes
{: #compare}

Le tableau suivant compare les types de compte Lite, Paiement à la carte et Abonnement. Pour plus de détails sur chaque compte, voir les sections qui suivent.

|                                         | Lite               | Paiement à la carte      | Abonnement       |
|-----------------------------------------|--------------------|--------------------|--------------------|
| **Accès à la mémoire Cloud Foundry gratuite** | 256 Mo             | 512 Mo             | 512 Mo             |
| **Accès aux [plans de service Lite ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://{DomainName}/catalog/?search=label:lite){: new_window}** | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Accès à tous les plans gratuits**            |                    | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Accès à l'intégralité du catalogue {{site.data.keyword.Bluemix_notm}}** |  | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Accès à plusieurs régions Cloud Foundry** |               | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Sans restrictions de temps** | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Gratuité garantie**                | ![Fonction disponible](../icons/icon_enabled.svg) |  |         |
| **Remise sur la tarification**                  |                    |                    | ![Fonction disponible](../icons/icon_enabled.svg) |
| **Idéal pour l'apprentissage ou la génération de validation de concept** | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |  |
| **Adapté aux scénarios de production**        |                    | ![Fonction disponible](../icons/icon_enabled.svg) | ![Fonction disponible](../icons/icon_enabled.svg) |
{: caption="Tableau 1. Comparaison des comptes {{site.data.keyword.Bluemix_notm}}" caption-side="top"}


## Compte Lite
{: #liteaccount}

Inscrivez-vous pour un compte Lite gratuit afin de construire des applications et d'explorer des services associés à des plans Lite gratuits signalés par l'indicateur Lite ![Balise Lite](../icons/Lite.svg) dans la console {{site.data.keyword.Bluemix_notm}}. Votre compte Lite n'expire pas et votre carte de crédit n'est pas nécessaire.

Vous avez accès à un seul groupe de ressources, créé pour vous et nommé `Default`. Toutes vos instances de service gérées par {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) sont automatiquement ajoutées à ce groupe de ressources. Vous pouvez mettre à jour ce groupe de ressources à tout moment. Pour la procédure détaillée, voir [Changement de nom d'un groupe de ressources](/docs/resources?topic=resources-rgs#rename_rgs).

Chaque groupe de ressources est gratuit. Lorsque vous créez une connexion entre un service géré par IAM et une application Cloud Foundry, vous créez un alias, qui est une instance de service comptabilisée dans votre quota. Voir [Gestion des connexions](/docs/resources?topic=resources-connect_app).
{: tip}

### Quelles sont les disponibilités ?
{: #lite-account-features}

La liste suivante répertorie les principales fonctions disponibles dans un compte Lite :

   * Le compte est gratuit - Pas besoin de carte de crédit.
   * Le compte n'expire jamais.
   * Vous pouvez utiliser une organisation dans une seule région {{site.data.keyword.Bluemix_notm}}.
   * Support de base {{site.data.keyword.Bluemix_notm}} gratuit. Le support de base est assuré pour les environnements non destinés à la production ou les charges de travail pour lesquels les niveaux de gravité traditionnels ne sont pas utilisés et des temps de réponse spécifiques ne sont pas stipulés.
   * Des notifications vous sont envoyées par courrier électronique quant au statut de votre compte et à vos limites de quota.
   * Vos applications Cloud Foundry peuvent utiliser jusqu'à 256 Mo de mémoire d'exécution gratuite et instantanée par mois.
   * Vous pouvez mettre à disposition une instance de n'importe quel service du catalogue [{{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} doté d'un plan Lite.
   * Après 10 jours sans activité de développement, vos applications passent en veille. Vous pouvez réactiver vos applications en continuant de les utiliser.
   * Après 30 jours sans activité de développement, vos instances de service non associées à des plans Lite sont supprimées.

## Compte Paiement à la carte
{: #paygo}

Avec un compte Paiement à la carte, vous pouvez accéder à l'ensemble du catalogue {{site.data.keyword.Bluemix_notm}} (tous les plans gratuits, notamment) et vous disposez du double de mémoire par mois, soit 512 Mo. Vous paierez uniquement les services facturables utilisés sans aucun engagement ou contrat à long terme.

Vous pouvez créer plusieurs groupes de ressources de manière à faciliter la gestion du quota et l'affichage de la facturation d'utilisation d'un ensemble de ressources. Les frais sont facturés d'après votre utilisation des ressources de calcul et des services {{site.data.keyword.Bluemix_notm}}. Si votre utilisation dépasse les franchises de service et d'exécution, vous recevez une facture mensuelle qui inclut des détails sur les ressources facturées.

De plus, avec un compte Paiement à la carte, vous pouvez commander des plans de support avancés ou premium pour obtenir de l'aide supplémentaire en matière de charge de travail de production. Pour en savoir plus, voir [Plans de support](/docs/get-support?topic=get-support-support-plans).

## Compte d'abonnement
{: #subscription-account}

Avec un compte d'abonnement, vous pouvez créer plusieurs groupes de ressources de manière à faciliter la gestion du quota et l'affichage de la facturation d'utilisation d'un ensemble de ressources. Vous vous engagez à dépenser une somme minimale par mois et recevez une remise sur abonnement qui est appliquée à ce montant minimal.

Par exemple, si vous vous engagez à dépenser 100 $ par mois pendant 6 mois, vous obtenez une remise de 10 %. Pendant la durée de l'abonnement, vous disposerez de 600 $ d'utilisation mais n'en paierez que 540 $. Plus la durée de l'abonnement est longue, plus la remise est importante.

Votre utilisation est déduite du montant total de votre abonnement. Même si votre utilisation est différente tous les mois, vous obtiendrez une facturation prévisible et cohérente. Si votre utilisation dépasse la quantité totale de votre abonnement, l'excédent vous est facturé au tarif non remisé.

Tout comme avec les comptes Paiement à la carte, votre compte d'abonnement permet de commander des plans de support avancés ou premium pour obtenir de l'aide supplémentaire si vous en avez besoin. Pour en savoir plus, voir [Plans de support](/docs/get-support?topic=get-support-support-plans).

Si vous avez un compte Abonnement, vous pouvez créer la plupart des services disponibles dans le catalogue [{{site.data.keyword.Bluemix_notm}}](https://{DomainName}/catalog){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe"). Toutefois, il peut être nécessaire d'acheter séparément certains services utilisant un plan de tarification spécifique.

### Abonnement à une offre groupée de services
{: #service-subscriptions}

Les abonnements à des offres groupées de services vous permettent d'accéder à un ensemble de services dans un domaine spécifique qui sont ciblés pour les cas d'utilisation les plus répandus et de bénéficier d'un crédit pour ces services. Vous pouvez choisir l'offre groupée de services souhaitée parmi les services d'intelligence artificielle, d'analyse, {{site.data.keyword.blockchainfull_notm}}, Internet of Things (IoT) et les services natifs de cloud. Si vous avez besoin de plusieurs de ces services, vous pouvez acheter plusieurs abonnements d'offre groupée de services.

Vous pouvez ajouter des offres groupées de services à tout type de compte existant, y compris les comptes Lite. Pendant les 90 premiers jours, vous êtes limité à l'utilisation des services de l'offre groupée. Après cette période, vous pouvez accéder à l'ensemble du catalogue. Les abonnements à des offres groupées de services sont sujets aux conditions [Description de service {{site.data.keyword.Bluemix_notm}}](/docs/overview/terms-of-use?topic=overview-terms).

Les abonnements aux offres groupées de services ne sont pas disponibles dans la console {{site.data.keyword.Bluemix_notm}}. Pour en savoir plus et acheter une offre groupée de services, contactez le [service commercial {{site.data.keyword.Bluemix_notm}}![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}.
{:tip}

Une fois que vous avez acheté une offre groupée de services, vous recevez un courrier électronique avec un code de fonction à appliquer pour ajouter l'offre à votre compte. Pour plus d'informations sur l'application des codes de fonction, voir [Application de codes de fonction](/docs/account?topic=account-codes). Lorsque votre offre groupée de services arrive à expiration ou lorsque vous avez utilisé l'intégralité de votre crédit, vous pouvez continuer à utiliser des services en étant facturé selon le tarif Paiement à la carte.

## Mise à niveau de votre compte
{: #upgrade-lite-account}

Lorsque vous êtes prêt à faire passer votre compte au niveau suivant, vous pouvez [mettre à jour votre compte Lite](/docs/account?topic=account-upgrading-account) en compte Paiement à la carte ou en compte d'abonnement. La mise à niveau de votre compte déverrouille l'ensemble du catalogue {{site.data.keyword.Bluemix_notm}} et vous offre notamment des ressources gratuites supplémentaires.

Une fois votre compte Lite mis à niveau en compte Paiement à la carte, vous obtenez un crédit promotionnel de 200 $ automatiquement appliqué à votre compte. Ce crédit est valide pendant 30 jours et votre utilisation est automatiquement déduite du montant crédité. Il ne peut pas être utilisé sur des offres de tiers et il est possible qu'il ne soit pas disponible pour tous les comptes.

Si vous avez déjà un compte Paiement à la carte ou Abonnement, vous pouvez également convertir votre compte en un autre type de compte. Pour plus d'informations, voir [Mise à niveau de votre compte](/docs/account?topic=account-upgrading-account).
