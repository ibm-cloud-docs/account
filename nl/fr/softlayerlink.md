---

copyright:
  years: 2016, 2019
lastupdated: "2019-06-20"

keywords: SoftLayer account, link account, complete account, IBM Cloud account, IBMid, switch to IBMid

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Passage à l'IBMid et liaison des comptes
{: #unifyingaccounts}

Un IBMid est un ID unique que vous utilisez pour vous connecter à votre compte {{site.data.keyword.Bluemix}} afin d'accéder à des fonctions d'infrastructure, de services et d'application et de les acheter. Tous les nouveaux comptes reçoivent automatiquement un IBMid. Les comptes SoftLayer existants, à l'exception des comptes fédérés par SAML, peuvent être activés pour passer à l'authentification IBMid. Vous pouvez également lier des comptes afin d'obtenir une vue unique de vos comptes, de la facturation et de l'utilisation.
{:shortdesc}

## Passage à l'IBMid
{: #switchtoIBMid}

Lorsque vous entamez le processus permettant de passer à un IBMid, vous pouvez à tout moment annuler l'opération, avant la fin du processus. Cependant, à chaque fois que vous vous connecterez, un message vous invitant à passer à un IBMid s'affichera. Chaque compte SoftLayer que vous prévoyez de lier à un compte {{site.data.keyword.Bluemix_notm}} doit appartenir à un IBMid unique associé à une adresse électronique unique.

Pour faire basculer votre compte SoftLayer existant vers un IBMid, vous devez créez un IBMid, puis utiliser votre code d'enregistrement pour le confirmer.

### Demande d'un IBMid et d'un code d'enregistrement
{: #reqIBMidandregcode}

1. Connectez-vous à votre compte SoftLayer et cliquez sur **OK** lorsque vous êtes invité à passer à un IBMid.

   Si vous êtes un utilisateur principal et qu'aucun message vous invitant à passer à un IBMid ne s'affiche dans le portail client, prenez contact avec l'équipe de support IBM pour obtenir de l'aide. Pour plus d'informations sur le mode de contact de l'équipe de support, voir [Support](/docs/get-support?topic=get-support-getting-customer-support).

   Si vous vous êtes déjà connecté et avez cliqué sur **Plus tard** dans l'invite, mais voulez passer à l'authentification par IBMid dans la session en cours, accédez à la page d'édition du profil utilisateur et cliquez sur **Passer à IBMid**.

2. Suivez les invites de l'assistant pour créer votre IBMid.

   Entrez une adresse e-mail qui n'est pas actuellement utilisée par un IBMid. Elle servira de nom d'utilisateur pour le nouvel IBMid et le code d'enregistrement sera envoyé à cette adresse une fois l'IBMid créé. Vous pouvez actualiser l'adresse électronique ultérieurement mais vous ne pouvez pas changer le nom d'utilisateur.

### Confirmation de votre IBMid avec le code d'enregistrement
{: #confIBMiduseregcode}

1. Une fois que vous avez reçu votre code d'enregistrement, cliquez sur le lien fourni dans le courrier électronique ou copiez l'adresse URL dans un navigateur et entrez votre code d'enregistrement. Le code d'enregistrement est valable pendant sept jours et vous ne pouvez l'utiliser qu'une fois.

2. Après avoir soumis votre code d'enregistrement, utilisez votre IBMid pour vous connecter au portail client.

   Dans l'invite de connexion au compte, accédez à la section **Connexion à un compte avec identité IBM** et cliquez sur **Connexion avec identité IBM**. N'utilisez pas les zones **Nom d'utilisateur** et **Mot de passe** que vous utilisiez auparavant avec votre ID SoftLayer.

Si vous êtes un nouveau client, vous êtes invité à entrer votre IBMid ou à créer un nouvel IBMid lorsque vous êtes sur le point de payer votre commande.
  * Pour utiliser un IBMid existant, entrez le nom d'utilisateur ou l'adresse électronique de l'IBMid, si ces données ne sont pas partagées par plusieurs IBMid.
  * Pour créer un nouvel IBMid, entrez une adresse électronique qui n'est pas déjà utilisée par un IBMid existant. Elle servira de nom d'utilisateur pour l'IBMid et votre code d'enregistrement sera envoyé à cette adresse une fois l'IBMid créé. Vous pouvez actualiser l'adresse électronique ultérieurement mais vous ne pouvez pas changer le nom d'utilisateur.

Afin de résoudre les problèmes liés à la connexion avec votre IBMid, voir [Traitement des incidents liés à l'accès à {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-accessing).


## Liaison des comptes IBMid
{: #link_accounts}

Une fois que les comptes sont devenus des comptes IBMid, vous pouvez lier les comptes SoftLayer et les comptes {{site.data.keyword.Bluemix_notm}} afin d'accéder aux ressources d'infrastructure et de plateforme à partir d'une seule connexion. Le fait de lier vos comptes vous permet également d'obtenir une seule facture pour toutes les ressources d'infrastructure et de plateforme que vous utilisez. Vous pouvez lier votre propre compte ou, si vous êtes un utilisateur principal, vous pouvez lier vos comptes utilisateur.

### Liaison de votre compte IBMid
{: #link_user_account}

Si vous êtes un client d'infrastructure classique et que vous possédez également des comptes {{site.data.keyword.Bluemix_notm}}, vous pouvez lier vos comptes afin d'obtenir une vue unique de vos comptes, de la facturation et de l'utilisation. Pour lier vos comptes, procédez comme suit :
1. Connectez-vous à votre compte SoftLayer.
2. Sur la page Récapitulatif du compte, cliquez sur l'option permettant de lier un compte IBM Cloud****.
3. Lisez les conditions d'utilisation et cliquez pour confirmer que vous les acceptez.
4. Effectuez l'une des étapes finales suivantes, en fonction de la configuration de votre compte :
  * Si un compte {{site.data.keyword.Bluemix_notm}} est associé à votre IBMid, vous êtes redirigé vers une page d'autorisation, puis ramené à l'étape de confirmation finale.
  * Si vous ne possédez aucun compte {{site.data.keyword.Bluemix_notm}}, vous êtes invité à en créer un.

Pour afficher les questions et réponses courantes concernant la liaison de votre compte, consultez les [foires aux questions](/docs/account?topic=account-al_login).

### Liaison de comptes utilisateur IBMid
{: #link_customer_accounts}

Une fois que vos comptes utilisateur sont passés à l'authentification par IBMid, les revendeurs et les distributeurs peuvent lier leurs comptes utilisateur. Pour lier des comptes client, vous devez être un utilisateur principal de SoftLayer. L'IBMid correspondant à l'utilisateur principal du compte doit être le propriétaire du compte de plateforme {{site.data.keyword.Bluemix_notm}} auquel vous établissez la liaison.

Une fois que vos comptes sont liés, il n'est pas possible de revenir en arrière.
{: note}

Tenez compte des remarques suivantes concernant la liaison de vos comptes :

  * L'utilisateur principal du compte SoftLayer qui est lié doit posséder un IBMid.
  * Chaque compte utilisateur que vous liez à un compte {{site.data.keyword.Bluemix_notm}} doit être détenu par un IBMid unique associé à une adresse électronique unique. Même si un IBMid unique peut être associé à plusieurs comptes SoftLayer, vous devez changer d'utilisateur principal afin qu'il corresponde à un IBMid unique pour chaque compte. Prenez contact avec le support pour changer l'utilisateur principal d'un compte SoftLayer. Pour plus d'informations, voir [Support pour l'infrastructure {{site.data.keyword.Bluemix_notm}}](/docs/customer-portal?topic=customer-portal-customerportal_support).
  * Lorsque vous ajoutez de nouveaux utilisateurs à un compte lié, vous devez les ajouter au compte SoftLayer et au compte {{site.data.keyword.Bluemix_notm}} pour qu'ils aient accès à toutes les fonctions de la console unifiée.
  * Si vous possédez un compte de marque, que vous utilisez Brand Agent Portal (BAP) et que vous avez besoin d'aide lors de la liaison de votre compte, prenez contact avec l'équipe Revenue Services en leur envoyant un courrier électronique à l'adresse softlayer_revenue_services_team@wwpdl.vnet.ibm.com.

Pour lier chaque compte SoftLayer à un compte de plateforme {{site.data.keyword.Bluemix_notm}} existant ou pour en créer un nouveau, procédez comme suit :

   1. Connectez-vous au portail client avec votre IBMid de compte d'utilisateur principal.
   2. Dans le portail client, cliquez sur l'option permettant de lier un compte IBM Cloud****.
   3. Lisez et acceptez les dispositions pour la liaison de comptes SoftLayer et {{site.data.keyword.Bluemix_notm}}.
   4. Suivez les invites de l'assistant en ajoutant les utilisateurs du compte SoftLayer au compte {{site.data.keyword.Bluemix_notm}}.
   5. Lorsque vous y êtes invité, effectuez l'une des actions suivantes :
     * Si vous possédez déjà un compte {{site.data.keyword.Bluemix_notm}}, indiquez l'adresse électronique qui est associée à ce compte afin de lier les comptes.
     * Si vous ne possédez pas de compte {{site.data.keyword.Bluemix_notm}}, indiquez l'adresse électronique que vous voulez utiliser, suivez les instructions pour être invité dans {{site.data.keyword.Bluemix_notm}} et créez un compte.
   6. Après avoir lié le compte, indiquez à l'utilisateur final de chaque compte qu'il doit migrer vers l'IBMid en suivant la procédure décrite dans la section [Passage à l'IBMid](#switchtoIBMid) ci-dessus.

      Migrez uniquement les comptes d'utilisateur final vers l'IBMid. Ne migrez pas les comptes de marque, qui sont les comptes parent des comptes utilisateur final et qui ne contiennent aucune ressource. Les utilisateurs des comptes de marque qui migrent vers l'IBMid perdent la possibilité de se connecter à Brand Agent Portal (BAP).
      {: important}

Prenez en compte les modifications suivantes une fois que vos comptes sont liés :

  * Vous vous connectez maintenant à la [console {{site.data.keyword.Bluemix}} ![Icône de lien externe](../icons/launch-glyph.svg)](https://cloud.ibm.com){: new_window}.
  * Vous devez utiliser vos données d'identification IBMid pour accéder à votre compte SoftLayer et à votre compte {{site.data.keyword.Bluemix_notm}}.
  * Les remises SoftLayer existantes s'appliquent à tous les tarifs {{site.data.keyword.Bluemix_notm}}.
  * Vous recevez une facture en dollars américains (USD). Si vous disposez d'un compte {{site.data.keyword.Bluemix_notm}}, la facturation via {{site.data.keyword.Bluemix_notm}} pour les ressources d'infrastructure entre en vigueur au prochain cycle de facturation après que les comptes ont été liés. Pour plus d'informations, voir [Facturation en bloc pour des comptes liés](/docs/customer-portal?topic=customer-portal-unifybillaccounts).
  * Vous pouvez surveiller l'utilisation de vos ressources d'infrastructure classique dans la console {{site.data.keyword.Bluemix_notm}}.

## Utilisation de l'authentification multi-facteur dans les comptes liés
{: #2fa}

Si vous avez un compte lié, vous pouvez utiliser la page des paramètres d'{{site.data.keyword.Bluemix_notm}} IAM**** afin d'activer l'authentification multi-facteur pour votre compte. Ce type d'authentification, également communément appelé authentification à deux facteurs (2FA), ajoute une couche de sécurité pour l'accès à votre compte en plus de des habituels IBMid et mot de passe requis. L'authentification multi-facteur pour votre compte s'applique à l'ensemble des ressources de votre compte {{site.data.keyword.Bluemix_notm}} lié. Si elle est activée à votre compte, elle s'applique également à tous les utilisateurs qui ont été ajouté au compte.

Les autres méthodes d'authentification multi-facteur ne s'effectuent pas par IBMid mais par compte. Quand un IBMid est associé à plusieurs comptes et que vous passez d'un compte à l'autre, vous devez confirmer votre identité chaque fois que vous utilisez un compte différent qui nécessite une authentification à deux facteurs. Cette règle s'applique même si le compte précédent et le nouveau compte sont tous les deux configurés avec le même mécanisme d'authentification à deux facteurs.

Si vous avez déjà activé [l'authentification à deux facteurs dans le portail client](/docs/customer-portal?topic=customer-portal-cp_setup-2fa) pour les ressources de votre infrastructure classique et que vous activez le paramètre d'authentification multi-facteur de compte {{site.data.keyword.Bluemix_notm}}, ce dernier écrase l'authentification à deux facteurs que vous avez configurée dans le portail utilisateur. Autrement dit, vous pouvez désactiver l'authentification à deux facteurs que vous avez acquise dans le portail utilisateur au profit du paramètre d'authentification multi-facteur du compte.
