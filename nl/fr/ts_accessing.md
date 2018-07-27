---

copyright:

  years: 2015, 2018

lastupdated: "2018-07-09"

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

Vous devez également disposer d'un mot de passe valide associé à votre IBMid ou à votre ID de compte lié pour vous connecter au portail [{{site.data.keyword.slportal}}](https://control.softlayer.com).

Lorsque vous tentez de vous connecter à {{site.data.keyword.Bluemix_notm}}, le message d'erreur suivant s'affiche :
{: tsSymptoms}

`Le mot de passe que vous avez entré est incorrect.`

Le mot de passe que vous avez utilisé pour vous connecter à {{site.data.keyword.Bluemix_notm}} n'est pas valide.
{: tsCauses}

Utilisez l'une des solutions suivantes :
{: tsResolve}
 * Entrez le mot de passe correct. Pour vérifier si l'IBMid et le mot de passe sont valides, accédez à la page My IBM profile, cliquez sur **Log in** et entrez votre IBMid et votre mot de passe sur la page Log in.
 * Si vous avez oublié votre mot de passe, cliquez sur **Forgot your password** pour le réinitialiser. Revenez ensuite à la console [{{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou au portail [{{site.data.keyword.slportal}}](https://control.softlayer.com) et reconnectez-vous.
 * Si vous avez oublié votre IBMid ou que les problèmes avec votre mot de passe persistent, prenez contact avec le service Worldwide IBM Registration Helpdesk pour obtenir de l'aide.
 * Pour obtenir un IBMid et un mot de passe valides, accédez à la page My IBM profile, puis cliquez sur **Register**.

**Remarque :** Si vous êtes sur la page Sign in to IBM et que le processus de connexion est interrompu pour une raison quelconque (réinitialisation de votre mot de passe, par exemple), revenez à la [console {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou au portail [{{site.data.keyword.slportal}}](https://control.softlayer.com) et relancez le processus de connexion.


## Données d'identification incorrectes
{: #ts_login_invalid_credentials}

Lorsque vous vous connectez à l'aide de votre IBMid, le message suivant s'affiche :
{: tsSymptoms}

`Données d'identification incorrectes. Si vous possédez un IBMid associé à votre compte, connectez-vous ici`

* Vous êtes passé à l'utilisation d'un IBMid, mais vous avez tenté de vous connecter via le portail [{{site.data.keyword.slportal}}](https://control.softlayer.com) à l'aide de votre nom d'utilisateur et de votre mot mot de passe précédents.
{: tsCauses}

* Vous avez tenté de vous connecter via le portail [{{site.data.keyword.slportal}}](https://control.softlayer.com), mais vous avez entré votre IBMid et le mot de passe correspondant dans les zones Username et Password.

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
 * Si vous êtes un utilisateur {{site.data.keyword.BluSoftlayer_full}} disposant d'un ID {{site.data.keyword.BluSoftlayer_full}}, vous devez passer à l'authentification par IBMid dans le portail {{site.data.keyword.slportal}} dans chaque compte auquel vous avez accès pour pouvoir vous connecter via l'authentification par IBMid.
 Pour plus d'informations, voir [Passage à l'IBMid](/docs/account/softlayerlink.html).


## L'IBMid n'est associé à aucun compte IBM Cloud
{: #ts_login_noswitch}

Lorsque vous vous connectez à l'aide de votre IBMid, le message suivant s'affiche :
{: tsSymptoms}

`Vous accédez à cette page car votre authentification a abouti. Toutefois, cet IBMid n'est associé à aucun compte Bluemix. Si vous pensez que ce message ne s'affiche pas à bon escient, prenez contact avec votre propriétaire de compte ou votre utilisateur principal.`

Vous vous êtes connecté à partir du portail [{{site.data.keyword.slportal}}](https://control.softlayer.com) à l'aide d'un IBMid valide, mais vous n'êtes pas passé à l'authentification via IBMid dans le portail {{site.data.keyword.slportal}}.
{: tsCauses}

Effectuez les vérifications suivantes :
{: tsResolve}
 * Prenez contact avec votre utilisateur principal ou votre administrateur de compte pour vérifier que vous pouvez passer à l'authentification via IBMid.
 * Prenez soin d'exécuter l'étape de passage à l'IBMid. Voir [Passage à l'IBMid](/docs/account/softlayerlink.html).
 * Prenez soin d'exécuter les actions décrites dans le courrier électronique **Associate your user ID with an IBMid**. Recherchez le courrier électronique dans votre boîte de réception et dans votre dossier de courrier indésirable. Pour que le courrier électronique vous soit de nouveau envoyé, par exemple, s'il a expiré, accédez à la page d'édition du profil utilisateur dans le portail {{site.data.keyword.slportal}} et cliquez sur **Resend Email**. Vous pouvez également contacter le Support [{{site.data.keyword.Bluemix_notm}} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://ibm.biz/bluemixsupport.com){: new_window}.

**Remarque :** Si vous avez créé votre IBMid directement avec IBMid, deux courriers électroniques vous sont envoyés, l'un par le service d'enregistrement IBMid et l'autre par {{site.data.keyword.Blu_full}}. Prenez soin d'exécuter les actions décrites dans ces deux courriers électroniques.

Selon la configuration de votre compte, certaines des options de connexion suivantes peuvent s'appliquer à votre cas :
 * Les utilisateurs {{site.data.keyword.BluSoftlayer_notm}} associés à un ID {{site.data.keyword.BluSoftlayer_full}} doivent se connecter via le portail [{{site.data.keyword.slportal}}](https://control.softlayer.com).
 * Les utilisateurs {{site.data.keyword.BluSoftlayer_notm}} disposant d'un IBMid et possédant ou non un compte {{site.data.keyword.Bluemix_notm}} lié peuvent se connecter via le portail [{{site.data.keyword.slportal}}](https://control.softlayer.com) afin d'ouvrir le portail {{site.data.keyword.slportal}} ou via la console [{{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) afin d'ouvrir le tableau de bord Infrastructure.


## L'IBMid n'est associé à aucun compte {{site.data.keyword.Bluemix_notm}}
{: #ts_unabletologin}

Lorsque vous vous connectez à {{site.data.keyword.Bluemix_notm}}, le message suivant s'affiche :
{: tsSymptoms}

`Vous accédez à cette page car votre authentification a abouti. Toutefois, cet IBMid n'est associé à aucun compte {{site.data.keyword.Bluemix_notm}}.`

Vous vous êtes connecté à partir de la console [{{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) à l'aide d'un IBMid valide, mais vous ne possédez pas encore de compte {{site.data.keyword.Bluemix_notm}}.
{: tsCauses}

Pour créer un compte {{site.data.keyword.Bluemix_notm}}, suivez le processus d'inscription.
{: tsResolve}

Selon la configuration de votre compte, certaines des options de connexion suivantes peuvent s'appliquer à votre cas :
 * Les utilisateurs {{site.data.keyword.Bluemix_notm}} ne possédant pas de compte lié doivent se connecter via la console {{site.data.keyword.Bluemix_notm}}.
 * Les utilisateurs {{site.data.keyword.Bluemix_notm}} possédant un compte lié peuvent se connecter via la console [{{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou le portail [{{site.data.keyword.slportal}}](https://control.softlayer.com).


## La console ne s'ouvre pas
{: #ts_login_stalls}

Lorsque vous vous connectez à l'aide de votre IBMid, un message indiquant que la connexion a abouti s'affiche, mais vous ne revenez pas à la console [{{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou au portail [{{site.data.keyword.slportal}}](https://control.softlayer.com)
{: tsSymptoms}

Utilisez l'une des solutions suivantes :
{: tsResolve}
 * Fermez votre navigateur, effacez le contenu du cache et supprimez les cookies, puis essayez à nouveau de vous connecter.
 * Prenez soin de vous connecter à partir de la console [{{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ou du portail [{{site.data.keyword.slportal}}](https://control.softlayer.com) et non directement depuis le service d'authentification via IBMid.


## La connexion via IBMid n'aboutit pas
{: #ts_login_ibmid}

Lorsque vous vous connectez à {{site.data.keyword.Bluemix_notm}}, l'authentification via IBMid n'aboutit pas.
{: tsSymptoms}

Il s'agit peut-être d'un problème lié au service d'authentification via IBMid.
{: tsCauses}

Assurez-vous que vous pouvez vous connecter à la [page d'accueil IBM ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/us-en/){: new_window}. Dans ce cas, le problème est lié à l'application et vous pouvez faire une nouvelle tentative ultérieurement. Si vous ne pouvez pas vous connecter à cette page, contactez le [centre d'assistance ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}.
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

La confirmation par courrier électronique est envoyée à l'adresse de courrier électronique que vous avez indiquée. Vérifiez votre boîte de réception et votre dossier de courrier indésirable. Si vous ne recevez pas de confirmation par courrier électronique, contactez le [support {{site.data.keyword.Bluemix_notm}}  ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](http://ibm.biz/bluemixsupport.com){: new_window}.  
{: tsResolve}

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
  * Utilisez un navigateur différent. Pour plus d'informations sur les versions des navigateurs qui sont prises en charge par {{site.data.keyword.Bluemix_notm}}, voir [Prérequis {{site.data.keyword.Bluemix_notm}}](/docs/overview/prereqs.html#prereqs).
  * Si vous avez installé l'interface de ligne de commande Cloud Foundry, entrez la commande `cf apps` pour déterminer si votre application est en cours d'exécution.
