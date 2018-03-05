---

copyright:

  years: 2016, 2018

lastupdated: "2018-02-08"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Passage à l'IBMid et liaison des comptes
{: #unifyingaccounts}

Désormais, l'authentification dans SoftLayer utilise un IBMid afin de fournir une connexion unique pour {{site.data.keyword.Bluemix}} dans son intégralité. Un IBMid est un ID unique que vous utilisez pour vous connecter à votre compte {{site.data.keyword.Bluemix}} afin d'accéder à des fonctions d'infrastructure, de services et d'application et de les acheter. L'authentification par IBMid est activée pour tous les nouveaux comptes dans SoftLayer et les comptes SoftLayer existants sont activés pour passer à l'authentification par IBMid.
{:shortdesc}

## Passage à l'IBMid
{: #switchtoIBMid}

Lorsque vous entamez le processus permettant de passer à un IBMid, vous pouvez à tout moment annuler l'opération, avant la fin du processus. Cependant, à chaque fois que vous vous connecterez, un message vous invitant à passer à un IBMid s'affichera. Chaque compte SoftLayer que vous prévoyez de lier à un compte {{site.data.keyword.Bluemix_notm}} doit appartenir à un IBMid unique associé à une adresse électronique unique.

Pour faire basculer votre compte SoftLayer existant vers un IBMid, vous devez créez un IBMid, puis utiliser votre code d'enregistrement pour le confirmer. 

### Demande d'un IBMid et d'un code d'enregistrement
{: #reqIBMidandregcode}

1. Connectez-vous à votre compte SoftLayer et cliquez sur **OK** lorsque vous êtes invité à passer à un IBMid.

   Si vous êtes un utilisateur principal et qu'aucun message vous invitant à passer à un IBMid ne s'affiche dans le portail {{site.data.keyword.slportal}}, prenez contact avec le [support IBM](/docs/get-support/howtogetsupport.html#getting-customer-support) pour obtenir de l'aide.

   Si vous vous êtes déjà connecté et avez cliqué sur **Plus tard** dans l'invite, mais voulez passer à l'authentification par IBMid dans la session en cours, accédez à la page d'édition du profil utilisateur et cliquez sur **Passer à l'IBMid**.

2. Suivez les invites de l'assistant pour créer votre IBMid.

   Entrez une adresse électronique qui n'est associée à aucun IBMid. Elle servira de nom d'utilisateur pour le nouvel IBMid et le code d'enregistrement sera envoyé à cette adresse une fois l'IBMid créé. Vous pouvez mettre l'adresse électronique à jour ultérieurement mais vous ne pouvez pas changer le nom d'utilisateur.

### Confirmation de votre IBMid avec le code d'enregistrement
{: #confIBMiduseregcode}

1. Une fois que vous avez reçu votre code d'enregistrement, cliquez sur le lien dans le courrier électronique ou copiez l'adresse URL dans un navigateur et entrez votre code d'enregistrement.

   Le code d'enregistrement est valable pendant sept jours et vous ne pouvez l'utiliser qu'une fois.

2. Après avoir soumis votre code d'enregistrement, utilisez votre IBMid pour vous connecter au portail client.

   A l'invite de connexion au compte, accédez à la section **Connexion à un compte par ID IBM** et cliquez sur **Connexion par ID IBM**. N'utilisez pas les zones **Nom d'utilisateur** et **Mot de passe** que vous avez précédemment utilisées avec votre ID SoftLayer.

Si vous êtes un nouveau client, vous êtes invité à entrer votre IBMid ou à en créer un lorsque vous êtes sur le point de payer votre commande.
  * Pour utiliser un IBMid existant, entrez le nom d'utilisateur ou l'adresse électronique de l'IBMid, si ces informations sont uniques (c'est-à-dire si elles ne sont pas partagées par plusieurs IBMid).

  * Pour créer un IBMid, entrez une adresse électronique qui n'est utilisée par aucun IBMid. Elle servira de nom d'utilisateur pour l'IBMid et votre code d'enregistrement sera envoyé à cette adresse une fois l'IBMid créé. Vous pouvez mettre l'adresse électronique à jour ultérieurement mais vous ne pouvez pas changer le nom d'utilisateur.

Afin de résoudre les problèmes liés à la connexion avec votre IBMid, voir [Traitement des incidents liés à l'accès à {{site.data.keyword.Bluemix_notm}}](/docs/get-support/ts_accessing.html#accessing).


## Liaison de comptes utilisateur IBMid
{: #link_user_accounts}

Une fois que vos comptes utilisateur sont passés à l'authentification par IBMid, les revendeurs et les distributeurs peuvent lier les comptes SoftLayer et {{site.data.keyword.Bluemix_notm}} pour combiner des ressources d'infrastructure et de plateforme. Veillez à passer en revue les remarques importantes suivantes :

  * L'utilisateur principal du compte qui est lié doit posséder un IBMid.
  * Chaque compte utilisateur que vous liez à un compte {{site.data.keyword.Bluemix_notm}} doit être détenu par un IBMid unique associé à une adresse électronique unique. Même si un IBMid unique peut être associé à plusieurs comptes SoftLayer, vous devez changer l'utilisateur principal afin qu'il corresponde à un IBMid unique pour chaque compte. Prenez contact avec le support pour changer l'utilisateur principal d'un compte SoftLayer. Pour plus d'informations, voir [Support pour l'infrastructure {{site.data.keyword.Bluemix_notm}}](/docs/customer-portal/cpsupport.html).
  * Lorsque vous ajoutez de nouveaux utilisateurs à un compte lié, vous devez les ajouter au compte SoftLayer et au compte {{site.data.keyword.Bluemix_notm}} pour qu'ils aient accès à toutes les fonctionnalités de la console unifiée.
  * Si vous êtes un utilisateur de compte de marque qui utilise Brand Agent Portal (BAP) et que vous avez besoin de support lors de la liaison de votre compte, prenez contact avec l'équipe SoftLayer Revenue Services en leur en voyant un courrier électronique à l'adresse softlayer_revenue_services_team@wwpdl.vnet.ibm.com.
  * Tous les comptes liés dans {{site.data.keyword.Bluemix_notm}} doivent être de type Paiement à la carte. Vous pouvez créer un nouveau compte Paiement à la carte, lier un compte Paiement à la carte existant, ou lier un compte d'essai existant, qui est ensuite mis à niveau vers un compte Paiement à la carte. Vous ne pouvez pas lier des comptes de type Abonnement.

Pour lier des comptes, vous devez être un utilisateur principal. L'IBMid correspondant à l'utilisateur principal du compte doit être le propriétaire du compte {{site.data.keyword.Bluemix_notm}} auquel vous établissez la liaison. Pour lier chaque compte SoftLayer à un compte {{site.data.keyword.Bluemix_notm}} existant ou pour en créer un nouveau, procédez comme suit :

   1. Connectez-vous au portail client avec votre compte d'utilisateur principal. 
   2. A partir du portail client {{site.data.keyword.Bluemix_notm}}, cliquez sur **Lier un compte {{site.data.keyword.Bluemix_notm}}**.
   3. Lisez et acceptez les dispositions pour la liaison de comptes SoftLayer et {{site.data.keyword.Bluemix_notm}}.
   4. Suivez les invites de l'assistant en ajoutant les utilisateurs du compte SoftLayer au compte {{site.data.keyword.Bluemix_notm}}.
   5. A l'invite, indiquez l'adresse électronique associée à votre compte {{site.data.keyword.Bluemix_notm}}. Si vous ne disposez pas d'un compte {{site.data.keyword.Bluemix_notm}}, indiquez l'adresse électronique que vous voulez utiliser, suivez les instructions pour être invité dans {{site.data.keyword.Bluemix_notm}} et créez un compte.
   6. Après avoir lié le compte, indiquez à l'utilisateur final de chaque compte qu'il doit migrer vers l'IBMid en suivant la procédure décrite dans la section précédente.

Migrez uniquement les comptes d'utilisateur final vers l'IBMid. Ne migrez pas les comptes de marque, qui sont les comptes parent des comptes utilisateur final et qui ne contiennent aucune ressource. Les utilisateurs des comptes de marque qui migrent vers l'IBMid perdent la possibilité de se connecter à Brand Agent Portal (BAP).
{: tip}

Une fois que vos comptes sont liés :

  * Vous devez utiliser vos données d'identification IBMid pour accéder à votre compte SoftLayer et à votre compte
{{site.data.keyword.Bluemix_notm}}.
  * Les remises SoftLayer existantes sont appliquées à tous les prix {{site.data.keyword.Bluemix_notm}}.
  * Vous recevez une facture en dollars américains (USD). Si vous disposez d'un compte {{site.data.keyword.Bluemix_notm}}, la facturation via  {{site.data.keyword.Bluemix_notm}} pour les ressources d'infrastructure entre en  vigueur au cycle de facturation suivant la liaison des comptes.

  * Vous pouvez surveiller l'utilisation de vos ressources d'infrastructure dans la console {{site.data.keyword.Bluemix_notm}}.

Une fois vos comptes liés, cette opération est irréversible.

## Utilisation de l'authentification multi-facteur dans les comptes liés
{: #2fa}

Si vous disposez d'un compte lié, vous pouvez utiliser la page **Paramètres** d'Identity and Access pour activer l'authentification multi-facteur (/docs/iam/mfa.html) pour votre compte. Ce type d'authentification, également communément appelé authentification à deux facteurs (2FA), ajoute une couche de sécurité pour l'accès à votre compte en plus de des habituels IBMid et mot de passe requis. L'authentification multi-facteur pour votre compte s'applique à l'ensemble des ressources de votre compte {{site.data.keyword.Bluemix_notm}} lié. Si elle est activée à votre compte, elle s'applique également à tous les utilisateurs qui ont été ajouté au compte. Vous trouverez des informations supplémentaires sur les considérations à prendre en compte lors de l'[activation de l'authentification multi-facteur](/docs/iam/mfa.html) pour votre compte.

L'authentification multi-facteur ne s'effectue pas par IBMid, mais encore par compte. Quand un IBMid est associé à plusieurs comptes et que vous passez d'un compte à l'autre, vous devez confirmer votre identité chaque fois que vous utilisez un compte différent qui nécessite une authentification à deux facteurs. Cette règle s'applique même si le compte précédent et le nouveau compte sont tous les deux configurés avec le même mécanisme d'authentification à deux facteurs.
