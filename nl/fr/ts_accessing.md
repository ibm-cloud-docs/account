---

copyright:

  years: 2015, 2018

lastupdated: "2017-11-10"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Traitement des incidents liés à l'accès à {{site.data.keyword.Bluemix_notm}}
{: #accessing}

Des problèmes d'ordre général relatifs à l'accès à {{site.data.keyword.Bluemix}} peuvent survenir par exemple lors de l'ouverture d'une session {{site.data.keyword.Bluemix_notm}} ou si un compte est bloqué à l'état en attente. Dans de nombreux cas, ces problèmes peuvent être résolus en quelques opérations simples.
{:shortdesc}

## Mot de passe incorrect
{: #ts_logintobm}

Vous devez disposer d'un mot de passe valide associé à votre IBMid pour pouvoir vous connecter à la console {{site.data.keyword.Bluemix_notm}}.

Vous devez disposer d'un mot de passe valide associé à votre IBMid ou à votre ID de compte lié pour vous connecter au portail client de l'infrastructure [{{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com){: new_window}.

Lorsque vous tentez de vous connecter à {{site.data.keyword.Bluemix_notm}}, le message d'erreur suivant s'affiche :
{: tsSymptoms}

`Le mot de passe que vous avez entré est incorrect.`

Le mot de passe que vous avez utilisé pour vous connecter à {{site.data.keyword.Bluemix_notm}} n'est pas valide.
{: tsCauses}

Utilisez l'une des solutions suivantes :
{: tsResolve}
 * Entrez le mot de passe correct. Pour vérifier si l'IBMid et le mot de passe sont valides, accédez à la page My IBM profile, cliquez sur **Log in** et entrez votre IBMid et votre mot de passe sur la page Log in.
 * Si vous avez oublié votre mot de passe, cliquez sur **Forgot your password** pour le réinitialiser. Revenez ensuite à la [console {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.{DomainName}){: new_window} ou au [portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com){: new_window} et reconnectez-vous.
 * Si vous avez oublié votre IBMid ou que les problèmes avec votre mot de passe persistent, prenez contact avec le service Worldwide IBM Registration Helpdesk pour obtenir de l'aide.
 * Pour obtenir un IBMid et un mot de passe valides, accédez à la page My IBM profile, puis cliquez sur **Register**.

Remarques :
<!-- begin STAGING ONLY -->
 * Pour les employés IBM, il est possible que l'IBMid soit différent de l'ID intranet.
 <!-- end STAGING ONLY -->
 * Si vous êtes sur la page de connexion à IBM et que le processus de connexion est interrompu pour quelque raison que ce soit (réinitialisation de votre mot de passe, par exemple), revenez à la [console {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.{DomainName}){: new_window} ou au [portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com){: new_window} et relancez le processus de connexion.


## Données d'identification incorrectes
{: #ts_login_invalid_credentials}

Lorsque vous vous connectez à l'aide de votre IBMid, le message suivant s'affiche :
{: tsSymptoms}

`Données d'identification incorrectes. Si vous possédez un IBMid associé à votre compte, connectez-vous ici`

* Vous êtes passé à un IBMid, mais vous avez tenté de vous connecter via le [portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com){: new_window} en utilisant vos nom d'utilisateur et mot de passe précédents.
{: tsCauses}

* Vous avez tenté de vous connecter via le [portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com){: new_window}, mais vous avez entré vos IBMid et mot de passe dans les zones de nom d'utilisateur et de mot de passe.

Cliquez sur **log in here** dans le message ou accédez à la section IBMid Account Login et cliquez sur **Log in with IBMid**.
{: tsResolve}

N'utilisez pas les zones **Username** et **Password** que vous utilisiez avec votre ID précédent.


## IBMid ou adresse électronique non reconnu
{: #ts_old_username}

Lorsque vous vous connectez à la console {{site.data.keyword.Bluemix_notm}}, le message suivant s'affiche :
{: tsSymptoms}

`Nous ne reconnaissons pas cet IBMid ou cette adresse électronique. `

Vous avez tenté de vous connecter à la console {{site.data.keyword.Bluemix_notm}} avec un IBMid qui n'est pas valide. Par exemple, vous n'avez pas entré une adresse électronique qualifiée complète pour l'IBMid ou vous avez tenté d'utiliser vos nom d'utilisateur et mot de passe précédents.
{: tsCauses}

Vous devez disposer d'un IBMid et d'un mot de passe valides pour vous connecter à {{site.data.keyword.Bluemix_notm}}.

 * Prenez soin d'entrer une adresse électronique qualifiée complète pour l'IBMid.
 {: tsResolve}
 * Si vous êtes un utilisateur {{site.data.keyword.BluSoftlayer_full}} disposant d'un ID {{site.data.keyword.BluSoftlayer_full}}, vous devez passer à l'authentification par IBMid sur le portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} pour chaque compte auquel vous avez accès avant de pouvoir vous connecter via l'authentification par IBMid.
 Pour plus d'informations, voir [Passage à l'IBMid](/docs/account/softlayerlink.html#switching-to-ibmid).


## L'IBMid n'est associé à aucun compte IBM Cloud
{: #ts_login_noswitch}

Lorsque vous vous connectez à l'aide de votre IBMid, le message suivant s'affiche :
{: tsSymptoms}

`Vous accédez à cette page car votre authentification a abouti. Toutefois, cet IBMid n'est associé à aucun compte Bluemix. Si vous pensez
que ce message ne s'affiche pas à bon escient, prenez contact avec votre propriétaire de compte ou votre utilisateur principal.`

Vous vous êtes connecté à partir du [portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com){: new_window} avec un IBMid valide, mais vous n'êtes pas passé à l'authentification par IBMid depuis le portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}}.
{: tsCauses}

Effectuez les vérifications suivantes :
{: tsResolve}
 * Prenez contact avec votre utilisateur principal ou votre administrateur de compte pour vérifier que vous pouvez passer à l'authentification via IBMid.
 * Prenez soin d'exécuter l'étape de passage à l'IBMid. Voir [Passage à l'IBMid](/docs/account/softlayerlink.html#switching-to-ibmid).
 * Prenez soin d'exécuter les actions décrites dans le courrier électronique **Associate your user ID with an IBMid**. Recherchez le courrier électronique dans votre boîte de réception et dans votre dossier de courrier indésirable. Pour recevoir à nouveau l'e-mail, par exemple s'il est arrivé à expiration, accédez à la page d'édition du profil utilisateur du portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} et cliquez sur **Renvoyer le courrier électronique**. Vous pouvez également contacter le Support [{{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://ibm.biz/bluemixsupport.com){: new_window}.

**Remarque :** Si vous avez créé votre IBMid directement avec IBMid, deux courriers électroniques vous sont envoyés, l'un par le service d'enregistrement IBMid et l'autre par {site.data.keyword.Blu_full}}. Prenez soin d'exécuter les actions décrites dans ces deux courriers électroniques.

Selon la configuration de votre compte, certaines des options de connexion suivantes peuvent s'appliquer à votre cas :
 * Les utilisateurs {{site.data.keyword.BluSoftlayer_notm}} dotés d'un ID {{site.data.keyword.BluSoftlayer_full}} doivent se connecter via le [portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com){: new_window}.
 * Les utilisateurs {{site.data.keyword.BluSoftlayer_notm}} dotés d'un IBMid, avec ou sans compte {{site.data.keyword.Bluemix_notm}} lié, peuvent se connecter via le [portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com){: new_window} pour ouvrir le portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}}, ou via la [console {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.{DomainName}){: new_window} pour ouvrir le tableau de borde de l'infrastructure.


## L'IBMid n'est associé à aucun compte {{site.data.keyword.Bluemix_notm}}
{: #ts_unabletologin}

Lorsque vous vous connectez à {{site.data.keyword.Bluemix_notm}}, le message suivant s'affiche :
{: tsSymptoms}

`Vous accédez à cette page car votre authentification a abouti. Toutefois, cet IBMid n'est associé à aucun compte {{site.data.keyword.Bluemix_notm}}.`

Vous pouvez êtes connecté à partir de la [console {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.{DomainName}){: new_window} avec un IBMid valide, mais vous n'avez pas encore créé de compte {{site.data.keyword.Bluemix_notm}}.
{: tsCauses}

Pour créer un compte {{site.data.keyword.Bluemix_notm}}, suivez le processus d'inscription.
{: tsResolve}

Selon la configuration de votre compte, certaines des options de connexion suivantes peuvent s'appliquer à votre cas :
 * Les utilisateurs {{site.data.keyword.Bluemix_notm}} ne possédant pas de compte lié doivent se connecter via la console {{site.data.keyword.Bluemix_notm}}.
 * Les utilisateurs {{site.data.keyword.Bluemix_notm}} possédant un compte lié peuvent se connecter via la [console {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.{DomainName}){: new_window} ou le [portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com){: new_window}.


## La console ne s'ouvre pas
{: #ts_login_stalls}

Lorsque vous vous connectez à l'aide de votre IBMid, un message indiquant que la connexion a abouti s'affiche, mais vous ne revenez pas à la [console {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.{DomainName}){: new_window} ou au [portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com){: new_window}
{: tsSymptoms}

Utilisez l'une des solutions suivantes :
{: tsResolve}
 * Fermez votre navigateur, effacez le contenu du cache et supprimez les cookies, puis essayez à nouveau de vous connecter.
 * Veillez à vous connecter à partir de la [console {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://console.{DomainName}){: new_window} ou du [portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://control.softlayer.com){: new_window} plutôt que directement depuis le service d'authentification par IBMid.


## La connexion via IBMid n'aboutit pas
{: #ts_login_ibmid}

Lorsque vous vous connectez à {{site.data.keyword.Bluemix_notm}}, l'authentification via IBMid n'aboutit pas.
{: tsSymptoms}

Il s'agit peut-être d'un problème lié au service d'authentification via IBMid.
{: tsCauses}

Vérifiez le statut du service sur le site [IBM IBMid ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://new.wind.ibmcloud.com/webapp/#/status/a1a0c5d743d94a6a9597087541564d8e){: new_window}, puis essayez à nouveau l'opération.
{: tsResolve}


## Compte en attente
{: #ts_accntpding}

Si votre compte est en attente, vous ne pouvez pas vous connecter à {{site.data.keyword.Bluemix_notm}}.

Après avoir procédé à votre enregistrement pour un compte d'essai {{site.data.keyword.Bluemix_notm}}, il est possible que vous ne puissiez pas vous connecter à {{site.data.keyword.Bluemix_notm}}. Le message suivant s'affiche :
{: tsSymptoms}

<code>Votre compte est en attente. La confirmation par courrier électronique peut prendre jusqu'à 24 heures ; vérifiez également votre dossier de courrier indésirable. Si vous ne recevez pas votre confirmation par courrier électronique, contactez le <a href="http://ibm.biz/bluemixsupport.com" target="_blank">support {{site.data.keyword.Bluemix_notm}}</a>.</code>

Après avoir procédé à votre inscription pour un compte d'essai {{site.data.keyword.Bluemix_notm}}, vous recevez une confirmation par courrier électronique. Cliquez
sur le lien que contient ce courrier électronique pour compléter le processus d'enregistrement.
{: tsCauses}

La confirmation par courrier électronique est envoyée à l'adresse de courrier électronique que vous avez indiquée. Vérifiez votre boîte de réception et votre dossier de courrier indésirable. Si vous ne recevez pas de confirmation par courrier électronique, contactez le [support {{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://ibm.biz/{{site.data.keyword.Bluemix_notm}}support.com){: new_window}.  
{: tsResolve}


<!-- begin STAGING ONLY -->

## Incident lors de l'accès à un site Web externe
{: #ts_bmlinkid}

Pour vous connecter à {{site.data.keyword.Bluemix_notm}} en utilisant votre ID intranet IBM, vous devez lier votre ID intranet à votre IBMid.

Après que vous avez cliqué sur **Inscrivez-vous avec votre ID intranet** depuis la page de connexion de {{site.data.keyword.Bluemix_notm}}, il est possible que le message suivant s'affiche :
{: tsSymptoms}

`Incident lors de l'accès à un site Web externe`

Ce problème survient lorsque vous vous connectez à {{site.data.keyword.Bluemix_notm}} en utilisant un ID intranet IBM qui n'est pas lié à un IBMid. Votre IBMid est l'ID que vous utilisez pour vous connecter à www.ibm.com.
{: tsCauses}

En tant qu'employé IBM, avant de vous connecter à {{site.data.keyword.Bluemix_notm}} en utilisant votre ID intranet IBM, vous devez lier ce dernier à votre IBMid externe. Pour lier les deux ID, procédez comme suit :
{: tsResolve}

  1. Sur la page [Central Sign-on ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://w3-03.sso.ibm.com/tools/cso/index.jsp){: new_window}, cliquez sur **My Sign-ons**.
  2. Sur la page My Sign-ons, cliquez sur **Link IDs**, puis entrez votre IBMid et votre mot de passe sur la page {{site.data.keyword.Bluemix_notm}} Sign in. Après cela, votre ID intranet et votre IBMid sont automatiquement liés.


<!-- end STAGING ONLY -->

## La page {{site.data.keyword.Bluemix_notm}} ne peut pas être chargée
{: #ts_err}

Lorsque vous utilisez la console {{site.data.keyword.Bluemix_notm}}, il est possible que vous ne puissiez pas charger une page de console. A la place, un message d'erreur BXNUI0001E ou BXNUI0016E peut s'afficher.

L'un des messages d'erreur suivants peut s'afficher lorsque vous utilisez la console {{site.data.keyword.Bluemix_notm}} :
{: tsSymptoms}

`BXNUI0001E : La page n'a pas été chargée car {{site.data.keyword.Bluemix_notm}} n'a pas détecté s'il existait une session.`

`BXNUI0016E : Les applications et les services n'ont pas été extraits car une page {{site.data.keyword.Bluemix_notm}} n'a pas été chargée.`

Effectuez une ou plusieurs des actions suivantes :
{: tsResolve}

  * Actualisez ou redémarrez votre navigateur.
  * Déconnectez-vous de {{site.data.keyword.Bluemix_notm}}, puis reconnectez-vous.
  * Utilisez le mode de navigation privée de votre navigateur.
  * Effacez les cookies et le cache du navigateur.
  * Utilisez un navigateur différent. Pour plus d'informations sur les versions des navigateurs qui sont prises en charge par {{site.data.keyword.Bluemix_notm}}, voir [Prérequis {{site.data.keyword.Bluemix_notm}}](/docs/overview/whatisbluemix.html#prereqs).
  * Si vous avez installé l'interface de ligne de commande cf, entrez la commande `cf apps` pour déterminer si votre app est en cours d'exécution.
