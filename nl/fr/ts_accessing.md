---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-23"

keywords: troubleshoot account, account problem, account support, account help, account error, access error, login error, error message

subcollection: account

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


# Traitement des incidents liés à l'accès à {{site.data.keyword.Bluemix_notm}}
{: #accessing}

Des problèmes d'ordre général relatifs à l'accès à {{site.data.keyword.Bluemix}} peuvent survenir par exemple lors de l'ouverture d'une session {{site.data.keyword.Bluemix_notm}} ou si un compte est bloqué à l'état en attente. Dans de nombreux cas, ces problèmes peuvent être résolus en quelques opérations simples.
{:shortdesc}


## Pourquoi mon mot de passe est-il incorrect ?
{: #ts_logintobm}
{: troubleshoot}

Vous devez disposer d'un mot de passe valide associé à votre IBMid ou à votre ID SoftLayer pour pouvoir vous connecter à la console {{site.data.keyword.Bluemix_notm}}.

Lorsque vous tentez de vous connecter à {{site.data.keyword.Bluemix_notm}}, le message d'erreur suivant s'affiche :
{: tsSymptoms}

`Le mot de passe que vous avez entré est incorrect.`

Le mot de passe que vous avez utilisé pour vous connecter à {{site.data.keyword.Bluemix_notm}} n'est pas valide.
{: tsCauses}

Utilisez l'une des méthodes suivantes :
{: tsResolve}
 * Accédez à la page [de profil IBM ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://myibm.ibm.com/dashboard/){: new_window} pour confirmer que vous utilisez un mot de passe valide.
 * Si vous avez oublié votre mot de passe, cliquez sur **Mot de passe oublié ?** pour le réinitialiser.
 * Si vous avez oublié votre IBMid ou que les problèmes avec votre mot de passe persistent, prenez contact avec le service Worldwide IBM Registration Helpdesk pour obtenir de l'aide.

Si vous vous connectez à {{site.data.keyword.Bluemix_notm}} et que le processus de connexion est interrompu, quelle qu'en soit la raison (réinitialisation de votre mot de passe, par exemple), revenez à la console et démarrez à nouveau le processus de connexion.
{: tip}


## Pourquoi mon adresse électronique ou mon IBMid n'a-t-il pas été reconnu ?
{: #ts_old_username}
{: troubleshoot}

Pour vous connecter à votre messagerie électronique, vous devez vous assurer que vous disposez de l'authentification IBMid pour chaque compte.

Lorsque vous vous connectez à la console {{site.data.keyword.Bluemix_notm}}, le message suivant s'affiche :
{: tsSymptoms}

`Nous ne reconnaissons pas cet IBMid ou cette adresse électronique. `

Vous avez tenté de vous connecter à la console mais n'avez pas utilisé d'IBMid valide. Par exemple, vous n'avez pas entré d'adresse électronique complète pour l'IBMid ou vous avez tenté d'utiliser vos nom d'utilisateur et mot de passe précédents.
{: tsCauses}

Vous devez disposer d'un IBMid et d'un mot de passe valides pour vous connecter à {{site.data.keyword.Bluemix_notm}}.

 * Entrez une adresse électronique complète pour l'IBMid.
 {: tsResolve}
 * Si vous êtes utilisateur SoftLayer disposant d'un ID SoftLayer, vous devez utiliser l'authentification IBMid dans chaque compte auquel vous avez accès avant de pouvoir vous connecter. Pour plus d'informations, voir [Passage à l'IBMid](/docs/account?topic=account-unifyingaccounts).


## Pourquoi mon IBMid n'est-il associé à aucun compte {{site.data.keyword.Bluemix_notm}} ?
{: #ts_unabletologin}
{: troubleshoot}

Lorsque vous vous connectez à {{site.data.keyword.Bluemix_notm}}, le message suivant s'affiche :
{: tsSymptoms}

`Vous accédez à cette page car votre authentification a abouti. Toutefois, cet IBMid n'est associé à aucun compte {{site.data.keyword.Bluemix_notm}}.`

Vous vous êtes connecté à partir de la [console {{site.data.keyword.Bluemix_notm}}](https://{DomainName}){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe") à l'aide d'un IBMid valide, mais vous ne possédez pas de compte {{site.data.keyword.Bluemix_notm}}.
{: tsCauses}

Pour créer un compte {{site.data.keyword.Bluemix_notm}}, suivez le processus d'inscription.
{: tsResolve}


## Dans quel cas la console ne s'ouvre-t-elle pas lorsque je me connecte avec mon IBMid ?
{: #ts_login_stalls}
{: troubleshoot}

Lorsqu'un message de succès de connexion est généré mais que la console ne s'affiche pas à nouveau.

Lorsque vous vous connectez à l'aide de votre IBMid, un message indiquant que la connexion a abouti s'affiche mais la [console {{site.data.keyword.Bluemix_notm}} ](https://{DomainName}){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe") ne s'affiche pas à nouveau.
{: tsSymptoms}

Utilisez l'une des méthodes suivantes :
{: tsResolve}
 * Fermez votre navigateur, effacez le contenu du cache et supprimez les cookies, puis essayez à nouveau de vous connecter.
 * Connectez-vous à partir de la [console {{site.data.keyword.Bluemix_notm}}](https://{DomainName}){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe").


## Pourquoi ma connexion IBMid n'a-t-elle pas abouti ?
{: #ts_login_ibmid}
{: troubleshoot}

Si vous vous connectez à {{site.data.keyword.Bluemix_notm}} et que l'authentification de votre IBMid n'aboutit pas, il peut exister un problème lié au service.

Lorsque vous vous connectez à {{site.data.keyword.Bluemix_notm}}, l'authentification via IBMid n'aboutit pas.
{: tsSymptoms}

Il s'agit peut-être d'un problème lié au service d'authentification via IBMid.
{: tsCauses}

Vérifiez que vous pouvez vous connecter à [IBM](https://idaas.iam.ibm.com/idaas/mtfim/sps/authsvc?PolicyId=urn:ibm:security:authentication:asf:basicldapuser){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe"). Dans ce cas, le problème est lié à l'application et vous pouvez tenter à nouveau de vous connecter à la console. Si vous ne pouvez pas vous connecter à cette page, contactez le [centre d'assistance IBMid ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}.  
{: tsResolve}


## Pourquoi ne puis-je pas me connecter immédiatement après l'enregistrement d'un compte ?
{: #ts_accntpding}
{: troubleshoot}

Si votre compte est toujours en attente, vous ne pouvez pas vous connecter à {{site.data.keyword.Bluemix_notm}}.

Après vous être inscrit pour obtenir un compte {{site.data.keyword.Bluemix_notm}}, il se peut que vous ne puissiez pas vous connecter à {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Lorsque vous vous inscrivez pour obtenir un compte {{site.data.keyword.Bluemix_notm}}, vous recevez un message électronique incluant un lien de confirmation. Vous devez cliquer sur ce lien pour confirmer votre inscription. Si vous ne confirmez pas votre inscription, votre compte reste en attente.
{: tsCauses}

La confirmation par courrier électronique est envoyée à l'adresse électronique associée à votre IBMid. Vérifiez votre boîte de réception et votre dossier de courrier indésirable. Si vous n'avez pas reçu le courrier électronique de confirmation, accédez à la [page de connexion {{site.data.keyword.Bluemix_notm}} ](https://cloud.ibm.com/){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe") et essayez de vous connecter. Le message suivant s'affiche :
{: tsResolve}

```
Pour finaliser votre enregistrement, consultez votre messagerie. Vous ne trouvez pas le courrier électronique ? Renvoyer
```
{:screen}

Cliquez sur **Renvoyer** pour envoyer un autre courrier électronique de confirmation à l'adresse électronique qui est associée à votre IBMid. Si vous ne parvenez toujours pas à finaliser votre inscription, contactez le [support {{site.data.keyword.Bluemix_notm}}](/docs/get-support?topic=get-support-getting-customer-support).  


## Pourquoi certaines pages de la console ne se chargent-elles pas ?
{: #ts_err}
{: troubleshoot}

Lorsque vous utilisez la console {{site.data.keyword.Bluemix_notm}}, il est possible que vous ne puissiez pas charger une page de console. A la place, un message d'erreur BXNUI0001E ou BXNUI0016E peut s'afficher.

Un des messages d'erreur suivants peut s'afficher :
{: tsSymptoms}

`BXNUI0001E : La page n'a pas été chargée car {{site.data.keyword.Bluemix_notm}} n'a pas détecté s'il existait une session.`

`BXNUI0016E : Les applications et les services n'ont pas été extraits car une page {{site.data.keyword.Bluemix_notm}} n'a pas été chargée.`

Effectuez une ou plusieurs des actions suivantes :
{: tsResolve}

  * Actualisez ou redémarrez votre navigateur.
  * Déconnectez-vous de {{site.data.keyword.Bluemix_notm}}, puis reconnectez-vous.
  * Utilisez le mode de navigation privée de votre navigateur.
  * Effacez les cookies et le cache du navigateur.
  * Utilisez un navigateur différent. Pour plus d'informations sur les versions de navigateur prises en charge par {{site.data.keyword.Bluemix_notm}}, voir [Prérequis {{site.data.keyword.Bluemix_notm}}](/docs/overview?topic=overview-prereqs-platform).
  * Si vous avez installé l'interface de ligne de commande Cloud Foundry, entrez la commande `ibmcloud cf apps` pour déterminer si votre application est en cours d'exécution.
