---

copyright:

  years: 2018, 2019

lastupdated: "2019-02-05"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Surveillance des événements système avec un journal d'audit
{: #audit-log}

Si vous avez un compte d'infrastructure classique, vous pouvez surveiller les événements de réplication de stockage en consultant les journaux d'audit. Les journaux d'audit permettent d'effectuer le suivi des interactions de chaque utilisateur, comme les tentatives de connexion, les mises à jour de vitesse de port, les redémarrages d'alimentation et les interactions effectuées par l'équipe de support de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}}.
{:shortdesc}


## Affichage de votre journal d'audit
{: #view-audit-log}

Pour afficher votre journal d'audit, accédez à **Gérer > Compte** puis sélectionnez **Journal d'audit**. Le journal d'audit affiche à l'origine les 25 dernières interactions effectuées sur le compte par des utilisateurs. Vous pouvez afficher jusqu'à 200 interactions à tout moment. Développez le menu Eléments par page pour afficher plus de résultats. 

### Affichage des journaux d'accès d'un utilisateur
{: #view-access-logs}

Sur la page Journal d'audit, vous pouvez également voir les données correspondant à chaque tentative d'accès effectuée par un utilisateur spécifique. Les journaux affichent une date et un horodatage, ainsi que l'adresse IP pour chaque tentative d'accès. Procédez comme suit pour afficher les journaux d'accès d'un utilisateur :

1. Accédez à **Gérer > Compte** puis sélectionnez **Journal d'audit**. 
2. Effectuez ensuite une opération de filtrage**** pour l'utilisateur, sélectionnez la période à afficher et choisissez un type d'objet.  

Le journal d'accès de chaque utilisateur présente les tentatives d'accès effectuées par cet utilisateur par date, ainsi que l'adresse IP à partir de laquelle a eu lieu la tentative d'accès. Les informations du journal d'accès sont en lecture seule. 
