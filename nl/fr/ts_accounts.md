---

copyright:

  years: 2015, 2018

lastupdated: "2018-10-24"
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Traitement des incidents liés à la gestion des comptes
{: #managingaccounts}

Vous pouvez rencontrer des problèmes d'ordre général lorsque vous gérez votre compte, par exemple, différentes applications ont le même nom de domaine ou les administrateurs ne peuvent pas afficher toutes les organisations. Dans de nombreux cas, ces problèmes peuvent être résolus en quelques opérations simples.
{:shortdesc}


## Pourquoi ne puis-je pas accéder à un autre emplacement {{site.data.keyword.Bluemix_notm}} ?
{: #nosecondreg}
{: troubleshoot}

Vous ne pouvez pas créer de nouvel emplacement car votre type de compte ne permet pas cette action.

Vous recevez un message d'erreur lorsque vous tentez de créer un emplacement {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Il est probable que vous utilisiez un compte Lite, lequel ne permet un développement que dans un seul emplacement public. 
{: tsCauses}

Pour pouvoir accéder à des emplacements supplémentaires, vous devez utiliser un compte facturable. Accédez à **Gérer > Facturation et utilisation** et sélectionnez **Paiements**. 
{: tsResolve}


## Pourquoi ne puis-je pas créer de nouvelle organisation ?
{: #nosecondorg}
{: troubleshoot}

Vous tentez de créer plusieurs organisations et vous avez un compte Lite.  

Vous recevez un message d'erreur lorsque vous tentez de créer une organisation.
{: tsSymptoms}

Il est probable que vous utilisiez un compte Lite, lequel ne permet un développement que dans une seule organisation. 
{: tsCauses}

Pour créer une organisation, une mise à niveau vers un compte facturable est requise. Accédez à **Gérer > Facturation et utilisation** et sélectionnez **Mises à niveau**. 
{: tsResolve}


## Pourquoi ne puis-je pas créer de nouvelle instance de plan Lite ?
{: #nosecondlite}
{: troubleshoot}

Vous tentez de créer une instance supplémentaire mais vous avez un compte Lite.

Vous recevez le message d'erreur suivant lorsque vous tentez de créer une nouvelle instance de plan Lite :
{: tsSymptoms}

`Impossible de mettre à disposition une nouvelle instance Lite`

Pour pouvoir maintenir la gratuité de ces plans, une seule instance est permise par plan Lite.
{: tsCauses}

Vous pouvez créer d'autres instances du service en sélectionnant l'un des plans de service facturables, disponibles dans les comptes facturables. Pour effectuer une mise à niveau vers un compte facturable depuis la console, accédez à **Gérer > Facturation et utilisation** et sélectionnez **Mises à niveau**.
{: tsResolve}

Si vous ne souhaitez pas effectuer de mise à niveau depuis un compte Lite et que vous n'utilisez plus votre instance de service Lite existante, vous pouvez supprimer cette instance de plan de service à partir du tableau de bord Services, puis en créer une nouvelle.


## Comment ai-je dépassé la franchise de mémoire d'exécution ?
{: #noruntimemem}
{: troubleshoot}

Vous avez dépassé la mémoire autorisée pour votre compte.

Vous ne parvenez pas à déployer des applications et un message s'affiche indiquant que vous avez dépassé la limite de mémoire allouée à votre organisation.
{: tsSymptoms}

Dans un compte Lite, vos applications Cloud Foundry peuvent utiliser jusqu'à 256 Mo de mémoire d'exécution simultanée. Dans les comptes facturables, il existe une limite de mémoire de 2 Go.
{: tsCauses}

Si vous utilisez un compte Lite, vous pouvez obtenir plus de mémoire en effectuant une mise à niveau vers un compte facturable. Accédez à **Gérer > Facturation et utilisation** et sélectionnez **Mises à niveau**.
{: tsResolve}

Si vous ne souhaitez pas effectuer de mise à niveau depuis un compte Lite, mais disposez de diverses applications inactives, vous pouvez les supprimer pour libérer de la mémoire d'exécution.


## Pourquoi mon compte est-il inactif ?
{: #ts_accnt_inactive}
{: troubleshoot}

Vous ne pouvez pas créer d'application dans {{site.data.keyword.Bluemix_notm}} si votre compte est inactif. Vous devez prendre contact avec l'équipe de support pour résoudre ce problème.

Lorsque vous tentez de créer une application dans {{site.data.keyword.Bluemix_notm}}, le message d'erreur suivant s'affiche :
{: tsSymptoms}

`BXNUI0096E: L'application n'a pas été créée. Votre compte est inactif car il a été annulé ou suspendu.`

Le statut de votre compte {{site.data.keyword.Bluemix_notm}} devient inactif lorsque le compte est annulé ou suspendu.
{: tsCauses}

Pour réactiver votre compte, ouvrez un cas dans le [centre de support](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe"). Indiquez les informations suivantes dans votre cas :
{: tsResolve}

  * L'IBMid que vous utilisez pour vous connecter à {{site.data.keyword.Bluemix_notm}}.
  * Le nom de l'organisation dans laquelle votre application est créée. Ces informations peuvent être utiles à l'équipe de support pour déterminer si l'appartenance ou les rôles appropriés vous ont été affectés dans votre organisation.


## Pourquoi ne puis-je pas ajouter d'utilisateurs à une organisation ?
{: #ts_adduser}
{: troubleshoot}

Vous pouvez inviter des utilisateurs dans votre organisation uniquement si vous êtes le propriétaire du compte ou si vous êtes à la fois responsable et membre de l'organisation.

Le lien **Inviter un nouvel utilisateur** n'apparaît pas dans votre section **Gérer les organisations**.
{: tsSymptoms}

Seuls les utilisateurs {{site.data.keyword.Bluemix_notm}} suivants peuvent inviter des utilisateurs dans une organisation :
{: tsCauses}
  * Le propriétaire de compte de l'organisation
  * Les responsables d'organisation qui sont également membres et non collaborateurs de l'organisation

Dans {{site.data.keyword.Bluemix_notm}}, vous pouvez être, soit un membre, soit un collaborateur d'une organisation :

<dl><dt>Collaborateur</dt>
<dd>Vous êtes collaborateur d'une organisation si vous disposez déjà d'un compte {{site.data.keyword.Bluemix_notm}} et que vous avez été invité dans l'organisation.</dd>
<dt>Membre</dt>
<dd>Vous êtes membre d'une organisation si vous n'avez pas de compte {{site.data.keyword.Bluemix_notm}} mais que vous avez été invité à l'organisation et que vous vous êtes inscrit à {{site.data.keyword.Bluemix_notm}} à partir de l'invitation.</dd>
</dl>

Vous ne pouvez pas inviter d'utilisateurs dans votre organisation si vous êtes un collaborateur de l'organisation même si vous avez été désigné comme responsable de l'organisation.

Tous les responsables de l'organisation, y compris ceux qui sont des collaborateurs d'une organisation peuvent ajouter, modifier et retirer des utilisateurs se trouvant déjà dans l'organisation.
{: note}

Si vous ne pouvez pas inviter d'utilisateurs dans votre organisation et que vous avez besoin d'un autre rôle pour ce faire, prenez contact avec le responsable de l'organisation afin qu'il change votre rôle. Pour identifier le responsable de votre organisation, procédez comme suit :
{: tsResolve}

  1. Dans la barre de menus de la console, cliquez sur **Gérer > Compte** et sélectionnez **Contacts de la société**.
  2. Sélectionnez votre organisation et affichez les informations relatives au responsable dans l'onglet **Utilisateurs**.  

Si vous ne parvenez pas à inviter des utilisateurs car vous êtes collaborateur et non membre, vous devez supprimer votre compte {{site.data.keyword.Bluemix_notm}} précédent, puis être invité à rejoindre le compte en tant que membre de l'organisation. Pour supprimer votre compte précédent et rejoindre le compte en tant que membre, procédez comme suit :

  1. Contactez le [support {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} pour ouvrir un cas de support et demander la suppression de votre compte. Si des données sont associées à votre ancien compte et que vous souhaitez les sauvegarder et utiliser le nouveau compte, incluez ces informations dans votre message électronique.
  2. Une fois que votre compte est supprimé, faites en sorte qu'un utilisateur ayant le rôle Responsable d'organisation vous invite dans l'organisation en tant que responsable d'organisation. Ensuite, inscrivez-vous à {{site.data.keyword.Bluemix_notm}} à partir de l'invitation.


## Pourquoi aucun espace n'est-il associé à mon organisation en cours ?
{: #ts_no_space}
{: troubleshoot}

Vous ne pouvez pas créer d'application si aucun espace n'est associé à votre organisation en cours.

Lorsque vous tentez de créer une application, le message d'erreur suivant s'affiche :
{: tsSymptoms}

`BXNUI0097E: Pour qu'une application puisse être ajoutée, un espace au moins doit être associé à votre organisation et à votre région. Dans le tableau de bord, cliquez sur Créer un espace. Une fois l'espace créé, essayez à nouveau.`

Les applications doivent être créées dans un espace sous votre organisation.
{: tsCauses}

Pour créer un espace, appliquez l'une des méthodes suivantes :
{: tsResolve}

  * Dans la barre de menus de la console, cliquez sur **Gérer > Compte** et sélectionnez **Organisations**. Ensuite, sélectionnez l'organisation dans laquelle vous voulez créer l'espace, puis cliquez sur **Créer un espace**.
  * Dans l'interface de ligne de commande Cloud Foundry, entrez `cf create-space <space_name> -o <organization_name>`.


## Pourquoi certaines applications partagent-elles un nom de domaine ?
{: #ts_domain_diff}
{: troubleshoot}

Il se peut que plusieurs applications partagent une adresse URL dans {{site.data.keyword.Bluemix_notm}}.

Ce problème peut se produire lorsque vous affectez la même route d'adresse URL à plusieurs applications dans un espace.
{: tsCauses}

Par exemple, vous envoyez par commande push l'application myApp1 dans {{site.data.keyword.Bluemix_notm}} et définissez le nom de domaine `mynewapp.mybluemix.net`. Puis, vous envoyez par commande push une autre application myApp2 dans le même espace et affectez `mynewapp.mybluemix.net` à l'une de ses routes d'URL. La route est désormais mappée aux deux applications.

Il s'agit du comportement pris en charge ; il permet d'obtenir un temps d'indisponibilité nul pour la mise à niveau de votre application. Pour plus d'informations, voir [Comment garantir un temps d'indisponibilité nul](/docs/overview/zero_downtime.html#zero-downtime). 
{: tsResolve}


## Pourquoi les administrateurs ne peuvent-ils pas utiliser la console pour afficher toutes les organisations ?
{: #ts_ui_org}
{: troubleshoot}

En tant qu'administrateur, vous ne pouvez pas afficher chaque organisation pour les gérer lorsque vous utilisez la console {{site.data.keyword.Bluemix_notm}}. Vous pouvez afficher et administrer uniquement les organisations auxquelles vous appartenez.

En tant qu'administrateur, vous ne pouvez pas afficher toutes les organisations à partir de la console. 
{: tsSymptoms}

Il s'agit d'une limitation de la console. 
{: tsCauses}

Vous pouvez utiliser des commandes telles que `cf orgs`, `cf create-org` et `cf delete-org` à partir de l'interface de ligne de commande Cloud Foundry pour gérer toutes les organisations. Pour obtenir une liste complète des commandes Cloud Foundry, entrez `cf help`.
{: tsResolve}

## Pourquoi ne puis-je pas ajouter mes informations de carte de crédit ?
{: #ts_addcc}
{: troubleshoot}

Vous ne pouvez pas soumettre vos informations de carte de crédit pour convertir votre compte Lite en compte facturable.

Le bouton **Soumettre** sur la page Ajout d'une carte de crédit est désactivé.
{: tsSymptoms}

Ce problème survient lorsque vos informations ne sont pas entrées correctement sur la page Ajout d'une carte de crédit.
{: tsCauses}

Procédez comme suit :
{: tsResolve}

  1. Sur la page Ajouter une carte de crédit, renseignez toutes les zones requises. 
  2. Sélectionnez l'option indiquant que vous avez lu et accepté les dispositions d'IBM****, puis cliquez sur **Soumettre**. 
  
