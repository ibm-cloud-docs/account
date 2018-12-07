---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# Définition des préférences de courrier
{: #email-prefs}

En fonction de votre type de compte {{site.data.keyword.Bluemix}}, vous pouvez choisir de recevoir des notifications par courrier électronique sur les événements planifiés et les événements non planifiés de la plateforme {{site.data.keyword.Bluemix}} ou des notifications par courrier électronique d'infrastructure sur les annonces, la maintenance et les événements non planifiés. Vous pouvez également choisir de définir des abonnements de notification pour les événements d'infrastructure classiques.
{: shortdesc}

## Définition de notifications de plateforme
{: #setting-platform-notifications}

Si vous possédez un compte Lite, vous pouvez choisir de recevoir des notifications par courrier électronique concernant les événements non planifiés de la plateforme {{site.data.keyword.Bluemix}}, comme les indisponibilités et concernant les événements planifiés, comme la maintenance. Lorsque vous définissez des notifications relatives à la plateforme {{site.data.keyword.Bluemix_notm}}, vous recevez des notifications par courrier électronique associées uniquement à la plateforme {{site.data.keyword.Bluemix_notm}}. Vous ne recevez aucune notification sur les événements associés aux services {{site.data.keyword.Bluemix_notm}}.

Vous pouvez définir des notifications par courrier électronique uniquement pour votre profil et non pour le compte. Autrement dit, si vous changez de compte, toute mise à jour apportée aux notifications de plateforme est étendue à votre profil et non au nouveau compte.

Lorsque vous choisissez de recevoir des événements de plateforme non planifiés, vous recevez des courriers électroniques concernant uniquement les problèmes pouvant provoquer une indisponibilité. A tout moment, vous pouvez voir tous les événements planifiés et non planifiés sur la page [Status ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/status){: new_window}.

1. Accédez à l'icône Avatar ![Icône Avatar](../icons/i-avatar-icon.svg) &gt; **Profil et paramètres**.
2. Cliquez sur **Notifications**.
3. Choisissez si vous souhaitez recevoir des notifications relatives à la plateforme pour toutes les catégories à mettre à jour.

  Par défaut, toutes les notifications relatives à la plateforme {{site.data.keyword.Bluemix_notm}} sont désactivées.
  {: tip}

4. Cliquez sur **Sauvegarder**.

## Définition des notifications relatives à l'infrastructure

Si vous possédez un compte Paiement à la carte ou Abonnement, vous pouvez choisir de recevoir des notifications par courrier électronique relatives à l'infrastructure {{site.data.keyword.Bluemix_notm}} concernant les annonces, la maintenance et les événements non planifiés. Les notifications relatives à l'infrastructure sont étendues au compte vers lequel vous avez basculé. Vous pouvez basculer vers un autre compte et gérer les notifications pour ce compte.

1. Accédez à l'icône Avatar ![Icône Avatar](../icons/i-avatar-icon.svg) &gt; **Profil et paramètres**.
2. Cliquez sur **Notifications**.
3. Choisissez si vous souhaitez recevoir des notifications relatives à l'infrastructure pour toutes les catégories à mettre à jour.

  Par défaut, toutes les notifications relatives à l'infrastructure {{site.data.keyword.Bluemix_notm}} sont activées.
  {: tip}

4. Cliquez sur **Sauvegarder**.

## Configuration des notifications utilisateur
{: #setting-user-notifications}

La configuration des notifications utilisateur est disponible uniquement pour les ressources d'infrastructure classiques. Si vous possédez un compte, vous pouvez définir des abonnements de notification pour les utilisateurs de votre compte. Les abonnements sont destinés à un ensemble spécifique de services de développeur, comme {{site.data.keyword.autoscaling}} et Raid Alert Monitoring. Lorsqu'un utilisateur est abonné à un service, il reçoit des notifications concernant ce dernier.  

Les utilisateurs de votre compte reçoivent des notifications pour les événements opérationnels importants ayant un des types suivants :

  * Problèmes d'infrastructure non planifiés ou indisponibilités : Problèmes pouvant provoquer une indisponibilité selon certaines conditions pour des clients spécifiques.
  * Service ou maintenance planifié : Maintenance requise pour que l'infrastructure fonctionne de manière optimale.
  * Vulnérabilité en matière de sécurité : La zone concernée est isolée. Un correctif est créé pour fermer la vulnérabilité et des tests sont effectués sur le correctif afin de garantir qu'aucune fonction collatérale n'est affectée. 
  * Cas de support ouverts : Signale aux utilisateurs les cas ouverts sur leur compte.

Le délai de la notification varie selon que l'événement soit planifié ou non. La politique d'infrastructure {{site.data.keyword.BluSoftlayer_notm}} consiste à remédier au problème aussi rapidement que possible afin de supprimer ou de réduire le risque de voir des problèmes supplémentaires se développer qui pourraient avoir un impact plus conséquent. Il arrive parfois qu'une maintenance planifiée soit effectuée en ayant été notifiée très peu de temps auparavant.

Pour configurer des notifications d'abonnement pour vos utilisateurs, procédez comme suit : 

  1. Accédez à **Gérer > Compte** et sélectionnez **Notifications**. 
  2. Sélectionnez un service dans la table. 
  3. Dans la colonne Abonné, sélectionnez **Oui** pour l'utilisateur qui souhaite recevoir des notifications. 

    Pour trouver facilement l'utilisateur que vous recherchez, cliquez sur **Filtrer** et effectuez un filtrage par nom, prénom ou non d'utilisateur indiqué.
    {: tip}

