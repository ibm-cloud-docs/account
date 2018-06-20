---

copyright:

  years: 2015, 2018

lastupdated: "2017-11-09"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Traitement des incidents liés à la gestion des comptes
{: #managingaccounts}

Vous pouvez rencontrer des problèmes d'ordre général lorsque vous gérez votre compte, par exemple, différentes applications partagent le même nom de domaine ou les administrateurs ne peuvent pas afficher toutes les organisations. Dans de nombreux cas, ces problèmes peuvent être résolus en quelques opérations simples.
{:shortdesc}

## Impossible d'accéder à une région {{site.data.keyword.Bluemix_notm}} différente
{: #nosecondreg}

Vous recevez un message d'erreur lorsque vous tentez de créer une nouvelle région {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Il est probable que vous utilisez un compte Lite, lequel ne permet un développement que dans une seule région publique. La région {{site.data.keyword.Bluemix_notm}} publique dans laquelle vous désirez travailler est sélectionnée lors de la configuration initiale du compte.
{: tsCauses}

Si vous utilisez un compte Lite, vous pouvez effectuer une mise à niveau vers un compte facturable pour pouvoir accéder à d'autres régions. Accédez à **Gérer > Facturation et utilisation > Facturation** dans la console, puis cliquez sur **Ajouter une carte de crédit**. Sur la page **Facturation**, vous pouvez également vérifier si votre compte est un compte Lite.
{: tsResolve}

## Impossible de créer une nouvelle organisation
{: #nosecondorg}

Vous recevez un message d'erreur lorsque vous tentez de créer une nouvelle organisation.
{: tsSymptoms}

Il est probable que vous utilisez un compte Lite, lequel ne permet un développement que dans une seule organisation. Votre organisation est créée lors de la configuration initiale de votre compte.
{: tsCauses}

Si vous utilisez un compte Lite, vous pouvez effectuer une mise à niveau vers un compte facturable pour pouvoir accéder à d'autres organisations. Accédez à **Gérer > Facturation et utilisation > Facturation** dans la console, puis cliquez sur **Ajouter une carte de crédit**. Sur la page **Facturation**, vous pouvez également vérifier si votre compte est un compte Lite.
{: tsResolve}

## Impossible de créer une instance de plan Lite
{: #nosecondlite}

Vous recevez le message d'erreur suivant lorsque vous tentez de créer une instance de plan Lite :
{: tsSymptoms}

`Impossible de mettre à disposition une nouvelle instance Lite`

Pour pouvoir maintenir la gratuité de ces plans, une seule instance est permise par plan Lite.
{: tsCauses}

Vous pouvez créer des instances supplémentaires du service en sélectionnant l'un des plans de service facturables, lesquels sont disponibles dans les comptes facturables. Pour effectuer une mise à niveau vers un compte facturable depuis la console, accédez à **Gérer > Facturation et utilisation > Facturation**, puis cliquez sur **Ajouter une carte de crédit**.
{: tsResolve}

Si vous ne souhaitez pas effectuer une mise à niveau depuis un compte Lite et n'utilisez plus votre instance de service Lite existante, vous pouvez supprimer cette instance de plan de service depuis le tableau de bord Services, puis en créer une nouvelle.

## Allocation de mémoire d'exécution dépassée
{: #noruntimemem}

Vous ne parvenez pas à déployer des applications et un message d'erreur vous avise que vous avez dépassé la limite de mémoire allouée à votre organisation.
{: tsSymptoms}

Dans un compte Lite, vos applications Cloud Foundry peuvent utiliser jusqu'à 256 Mo de mémoire d'exécution simultanée. Dans les comptes facturables, cette limite est portée à 2 Go.
{: tsCauses}

Si vous utilisez un compte Lite, vous pouvez bénéficier d'une mémoire supplémentaire en effectuant une mise à niveau vers un compte facturable. Accédez à **Gérer > Facturation et utilisation > Facturation** dans la console, puis cliquez sur **Ajouter une carte de crédit**.
{: tsResolve}

Si vous ne souhaitez pas effectuer une mise à niveau depuis un compte Lite, mais disposez de diverses applications inactives, vous pouvez les supprimer pour libérer de la mémoire d'exécution.

## Le compte est inactif
{: #ts_accnt_inactive}

Vous ne pouvez pas créer d'application dans {{site.data.keyword.Bluemix_notm}} si votre compte est inactif. Vous devez prendre contact avec l'équipe de support pour résoudre ce problème.

Lorsque vous tentez de créer une application dans {{site.data.keyword.Bluemix_notm}}, le message d'erreur suivant s'affiche :
{: tsSymptoms}

`BXNUI0096E: L'application n'a pas été créée. Votre compte est inactif car il a été annulé ou suspendu.`

Le statut de votre compte {{site.data.keyword.Bluemix_notm}} devient inactif lorsque le compte est annulé ou suspendu.
{: tsCauses}

Pour réactiver votre compte, contactez le Support [{{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://ibm.biz/bluemixsupport.com){: new_window}. Indiquez les informations suivantes dans votre courrier électronique :
{: tsResolve}

  * L'IBMid que vous utilisez pour vous connecter à {{site.data.keyword.Bluemix_notm}}.
  * Le nom de l'organisation dans laquelle votre application est créée. Ces informations peuvent être utiles à l'équipe de support pour déterminer si l'appartenance ou les rôles appropriés vous ont été affectés dans votre organisation.

## Impossible d'ajouter des utilisateurs à une organisation
{: #ts_adduser}

Vous pouvez inviter plusieurs utilisateurs dans la même organisation. Vous pouvez inviter des utilisateurs dans votre organisation uniquement si vous êtes propriétaire de compte ou un responsable l'organisation.

Le lien **Inviter un nouvel utilisateur** n'apparaît pas dans votre section **Gérer les organisations**.
{: tsSymptoms}

Seuls les utilisateurs {{site.data.keyword.Bluemix_notm}} suivants peuvent inviter des utilisateurs dans une organisation :
{: tsCauses}
  * Le propriétaire de compte de l'organisation
  * Les responsables de l'organisation

**Remarque :** Tous les responsables de l'organisation peuvent ajouter, modifier ou retirer des utilisateurs qui se trouvent déjà dans l'organisation.

Si vous ne pouvez pas inviter d'utilisateurs dans votre organisation, prenez contact avec le responsable de l'organisation. Pour identifier le responsable de votre organisation, procédez comme suit :
{: tsResolve}

  1. Dans la barre de menus de la console, sélectionnez **Gérer > Compte > Organisations**.
  2. Sélectionnez votre organisation et affichez les informations relatives au responsable dans l'onglet **Utilisateurs**.  

## L'enregistrement d'utilisateurs par lots n'est pas pris en charge
{: #ts_batchregistration}

Lorsque vous enregistrez des utilisateurs pour {{site.data.keyword.Bluemix_notm}}, vous devez enregistrer chaque utilisateur individuellement.

{{site.data.keyword.Bluemix_notm}} ne permet pas d'enregistrer plusieurs utilisateurs simultanément.
{: tsSymptoms}

{{site.data.keyword.Bluemix_notm}} ne prend pas en charge l'enregistrement d'utilisateurs par lots. Pour enregistrer des utilisateurs pour {{site.data.keyword.Bluemix_notm}}, vous devez enregistrer chaque utilisateur individuellement.
{: tsCauses}

Pour enregistrer plusieurs utilisateurs pour {{site.data.keyword.Bluemix_notm}}, vous devez effectuer les opérations suivantes pour chaque utilisateur :
{: tsResolve}

  1. Cliquez sur **Inscription** dans la console {{site.data.keyword.Bluemix_notm}}.
  2. Suivez les étapes de l'assistant.

## Aucun espace n'est associé à votre organisation en cours
{: #ts_no_space}

Vous ne pouvez pas créer d'application si aucun espace n'est associé à votre organisation en cours.

Lorsque vous tentez de créer une application dans {{site.data.keyword.Bluemix_notm}}, le message d'erreur suivant s'affiche :
{: tsSymptoms}

`BXNUI0097E: Pour qu'une application puisse être ajoutée, un espace au moins doit être associé à votre organisation et à votre région. Dans le tableau de bord, cliquez sur Créer un espace. Une fois l'espace créé, essayez à nouveau.`

Les applications dans {{site.data.keyword.Bluemix_notm}} doivent être créées dans un espace sous votre organisation.
{: tsCauses}

Pour créer un espace, appliquez l'une des méthodes suivantes :
{: tsResolve}

  * Dans la barre de menus de la console, sélectionnez **Gérer > Compte > Organisations**. Ensuite, sélectionnez l'organisation dans laquelle vous voulez créer l'espace, puis cliquez sur **Créer un espace**.
  * Dans l'interface de ligne de commande cf, entrez `cf create-space <space_name> -o <organization_name>`.


## Les applications partagent le même nom de domaine
{: #ts_domain_diff}

Il se peut que plusieurs applications partagent la même adresse URL dans {{site.data.keyword.Bluemix_notm}}.

Ce problème peut se produire lorsque vous affectez la même route d'adresse URL à plusieurs applications dans un espace.
{: tsCauses}

Par exemple, vous envoyez par commande push l'application myApp1 dans {{site.data.keyword.Bluemix_notm}} et définissez le nom de domaine "mynewapp.stage1.mybluemix.net". Puis, vous envoyez par commande push une autre application myApp2 dans le même espace et affectez "mynewapp.mybluemix.net" à l'une de ses routes d'URL. La route est désormais mappée aux deux applications.

Il s'agit du comportement de {{site.data.keyword.Bluemix_notm}} pris en charge ; il permet d'obtenir un temps d'indisponibilité nul pour la mise à niveau de votre application. Pour plus d'informations, voir [Using Blue-Green Deployment to Reduce Downtime and Risk ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://docs.cloudfoundry.org/devguide/deploy-apps/blue-green.html){: new_window}.
{: tsResolve}


## Les administrateurs ne peuvent pas visualiser toutes les organisations à l'aide de l'interface utilisateur {{site.data.keyword.Bluemix_notm}}
{: #ts_ui_org}

En tant qu'administrateur, lorsque vous utilisez l'interface utilisateur {{site.data.keyword.Bluemix_notm}}, vous ne pouvez pas afficher chaque organisation à des fins d'administration. Vous pouvez afficher et administrer uniquement les organisations auxquelles vous appartenez.

En tant qu'administrateur, vous ne pouvez pas afficher toutes les organisations à l'aide de l'interface utilisateur {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Il s'agit d'une limitation de l'interface utilisateur {{site.data.keyword.Bluemix_notm}}.
{: tsCauses}

Vous pouvez utiliser des commandes telles que `cf orgs`, `cf create-org` et `cf delete-org` à partir de l'interface de ligne de commande cf pour gérer toutes les organisations. Pour obtenir une liste complète des commandes cf, entrez `cf help`.
{: tsResolve}

## La carte de crédit ne peut pas être ajoutée
{: #ts_addcc}

Vous ne pouvez pas soumettre vos informations de carte de crédit pour convertir votre compte d'essai en compte Paiement à la carte.

Le bouton **Soumettre** sur la page Ajout d'une carte de crédit est désactivé.
{: tsSymptoms}

Ce problème survient lorsque vos informations ne sont pas remplies correctement sur la page Ajout d'une carte de crédit.
{: tsCauses}


Procédez comme suit :
{: tsResolve}

  1. Sur la page Ajout d'une carte de crédit, remplissez toutes les zones requises qui se trouvent dans les sections relatives aux coordonnées, à l'adresse de contact et à l'adresse de facturation.
  2. Sélectionnez **I have read and agree to IBM's Terms and Conditions**, puis cliquez sur **Soumettre**. La section **Select a payment method** s'affiche.
  3. Entrez votre numéro de carte de crédit, la date d'expiration de votre carte et le code de sécurité qui se trouve sur votre carte. Cliquez sur **Soumettre**.
