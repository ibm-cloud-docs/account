---


copyright:

  years: 2018
lastupdated: "2018-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}


# Configuration de la sécurité de connexion
{: #login-settings}

Avec l'accès autorisé, vous pouvez configurer des options de sécurité supplémentaires pour votre connexion. Vous pouvez définir des questions et des réponses de sécurité, sélectionner une expiration de mot de passe, configurer l'authentification multi-facteur de code d'accès à usage unique à durée limité (TOTP) et configurer les options d'authentification externe.  
{:shortdesc}

Un propriétaire de compte peut exiger une authentification multi-facteur IBMid pour un compte dont vous êtes membre. L'authentification multi-facteur IBMid remplace tout autre paramètre utilisateur d'authentification multi-facteur. Par exemple, lorsque l'authentification multi-facteur IBMid est définie, vous êtes invité à effectuer l'authentification multi-facteur TOTP associée à votre ID IBMid au lieu d'utiliser des questions de sécurité ou une des méthodes d'authentification externe.
{: note}

Vous pouvez afficher les options de sécurité suivantes et les activer ou les désactiver uniquement si votre administrateur vous y autorise. Accédez à l'icône **{{site.data.keyword.avatar}}** ![Icône Avatar](../icons/i-avatar-icon.svg) > **Profil et paramètres** et sélectionnez **Paramètres de connexion**.

## Configuration des questions de sécurité
{: #security-questions}

Pour configurer vos questions de sécurité, procédez comme suit :
1. Dans la console, accédez à l'icône **{{site.data.keyword.avatar}}** ![Icône Avatar](../icons/i-avatar-icon.svg) > **Profil et paramètres** et sélectionnez **Paramètres de connexion**.
2. Cliquez sur **Editer**. 
3. Sélectionnez les questions souhaitées et posez-les. Vous devez utiliser trois options de question de sécurité.
4. Cliquez sur **Sauvegarder** une fois que vous avez terminé.  
5. Assurez-vous que la case `Oui` est cochée afin que les questions de sécurité soient activées. Si vous sélectionnez l'option `Oui`, il peut vous être demandé de vous connecter à nouveau à votre compte.  

Vous pouvez configurer des réponses à trois questions de sécurité pour une authentification supplémentaire lors de la connexion. Vous devez configurer vos questions et réponses de sécurité pour que vos administrateurs puissent activer pour vous l'exigence d'authentification multi-facteur.

Vous devez être propriétaire de compte ou votre administrateur de compte doit avoir activé pour vous le paramètre de connexion gérée par l'utilisateur pour activer et désactiver la sécurité.
{: note}

## Définition de l'expiration d'un mot de passe
{: #password-expiration}

Pour définir la durée pendant laquelle utiliser votre mot de passe actuel, sélectionnez une option pour l'expiration du mot de passe dans la section **Expiration du mot de passe**.

Par défaut, le mot de passe n'arrive jamais à expiration. Lorsque vous vous inscrivez pour un compte, il ne vous est jamais demandé de changer votre mot de passe. Lorsque vous définissez une période pour l'expiration de mot de passe, vous recevez 14 jours avant, 7 jours avant et le jour même de l'expiration une notification signalant l'expiration du mot de passe.

Cette option est disponible uniquement pour les utilisateurs qui se connectent avec un ID SoftLayer. Pour mettre à jour l'expiration de votre mot de passe, vous devez être propriétaire du compte ou votre administrateur de compte doit avoir activé pour vous le paramètre de connexion gérée par l'utilisateur sur la page des détails de l'utilisateur IAM.
{: note}

## Configuration de l'authentification TOTP
{: #MFA}

Pour configurer votre authentification TOTP, cliquez sur **Configuration**. 

L'authentification multi-facteur TOTP ajoute une couche supplémentaire de sécurité à votre compte en demandant un code d'accès TOTP en plus de l'ID et du mot de passe standard lors de la connexion. Vous devez configurer votre authentification TOTP avant que votre administrateur de compte puisse activer pour vous cette exigence d'authentification multi-facteur.

Vous pouvez également être invité à entrer un code d'accès à usage unique à durée limitée si le paramètre TOTP d'utilisateur n'est pas configuré et activé. Cela est dû au fait qu'un propriétaire de compte peut activer une authentification multi-facteur IBMid pour un compte auquel vous avez accès. Ce type d'authentification multi-facteur s'applique à tous les utilisateurs du compte lorsque ce paramètre est activé. Vous êtes tenu de l'utiliser. Pour plus d'informations, voir [Types d'authentification multi-facteur](/docs/iam/mfatypes.html#types).


## Configuration des options d'authentification externe
{: #third-party-MFA}

Vous (ou votre administrateur de compte) pouvez commander à un coût mensuel une authentification par téléphone ou Symantec. Pour que vous puissiez commander l'authentification externe, vous devez disposer de droits d'ajout d'infrastructure de services. Pour savoir si l'authentification externe est activée, accédez à l'**icône {{site.data.keyword.avatar}}** ![Icône Avatar](../icons/i-avatar-icon.svg) > **Profil et paramètres** et sélectionnez **Paramètres de connexion**. Si l'authentification multi-facteur par téléphone est désactivée, cliquez sur **Aller à > Détails de l'utilisateur**. Ce lien vous amène à la même page que si vous suiviez la procédure permettant de configurer votre authentification Symantec et de configurer votre authentification par téléphone.  

### Configuration de l'authentification Symantec

Si votre administrateur de compte choisit de commander la protection d'identité Symantec, vous devez collaborer avec lui pour effectuer la commande et fournir votre ID de données d'identification :

1. Accédez à la page [Symantec VIP](https://vip.symantec.com/).
2. Cliquez sur **Télécharger**. 
3. Procurez-vous votre ID de données d'identification et transmettez ce dernier à votre administrateur pour terminer la commande. 

Une fois que l'administrateur commande et active l'option, vous pouvez utiliser l'application pour l'authentification de connexion.

### Configuration de l'authentification par téléphone

Si votre administrateur de compte choisit de commander la protection d'identité par téléphone, vous devez la configurer après la commande par l'administrateur. Ensuite, votre administrateur peut l'activer afin que vous puissiez l'utiliser. Une fois que votre administrateur a commandé l'authentification par téléphone, procédez comme suit pour la configurer :

1. Accédez à **Gérer** > **Accès (IAM)**.
2. Cliquez sur **Utilisateurs** et sélectionnez votre nom dans la liste.
3. Sur la page **Détails de l'utilisateur** de la section **Gérer la connexion de l'utilisateur**, cliquez sur l'icône **Editer** ![Icône Editer](../icons/icon_write.svg) pour la ligne **Authentification par téléphone**.
4. Suivez les invites pour configurer votre authentification par téléphone.

Une fois que vous avez configuré votre authentification par téléphone, l'administrateur de compte peut activer l'option afin que vous soyez invité à indiquer ce type d'authentification multi-facteur lors de la connexion.


 

