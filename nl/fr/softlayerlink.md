---

copyright:

  years: 2016, 2018

lastupdated: "2018-05-01"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Passage à l'IBMid et liaison des comptes
{: #unifyingaccounts}

Désormais, l'authentification dans SoftLayer utilise un IBMid afin de fournir une connexion unique pour {{site.data.keyword.Bluemix}} dans son intégralité. Un IBMid est un ID unique que vous utilisez pour vous connecter à votre compte {{site.data.keyword.Bluemix_notm}} afin d'accéder à des fonctions d'infrastructure, de services et d'application et de les acheter. Tous les nouveaux comptes reçoivent automatiquement un IBMid et les comptes SoftLayer existants, à l'exception des comptes fédérés SAML, sont activés pour passer à l'authentification par IBMid.
{:shortdesc}

## Passage à l'IBMid
{: #switchtoIBMid}

Lorsque vous entamez le processus permettant de passer à un IBMid, vous pouvez à tout moment annuler l'opération, avant la fin du processus. Cependant, à chaque fois que vous vous connecterez, un message vous invitant à passer à un IBMid s'affichera. Chaque compte SoftLayer que vous prévoyez de lier à un compte {{site.data.keyword.Bluemix_notm}} doit appartenir à un IBMid unique associé à une adresse électronique unique.

Pour faire basculer votre compte SoftLayer existant vers un IBMid, vous devez créez un IBMid, puis utiliser votre code d'enregistrement pour le confirmer.

### Demande d'un IBMid et d'un code d'enregistrement
{: #reqIBMidandregcode}

1. Connectez-vous à votre compte SoftLayer et cliquez sur **OK** lorsque vous êtes invité à passer à un IBMid.

   Si vous êtes un utilisateur principal et qu'aucun message vous invitant à passer à un IBMid ne s'affiche dans le portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_full}}, prenez contact avec le support IBM pour obtenir de l'aide. Pour plus d'informations sur la prise de contact avec le support, voir [Support IBM](/docs/get-support/howtogetsupport.html#getting-customer-support).

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

Afin de résoudre les problèmes liés à la connexion avec votre IBMid, voir [Traitement des incidents liés à l'accès à {{site.data.keyword.Bluemix_notm}}](/docs/troubleshoot/ts_accessing.html#accessing).


## Liaison de comptes IBMid
{: #link_accounts}

Une fois que les comptes sont devenus des comptes IBMid, vous pouvez lier les comptes SoftLayer et {{site.data.keyword.Bluemix_notm}} pour utiliser des ressources IaaS (infrastructure sous forme de services) et PaaS (plateforme sous forme de services) combinées. Vous pouvez ensuite accéder aux ressources IaaS et PaaS à partir d'une seule connexion. Le fait de lier vos comptes vous permet également d'obtenir une seule facture pour toutes les ressources PaaS et IaaS que vous utilisez. Vous pouvez lier votre propre compte ou, si vous êtes un utilisateur maître, vous pouvez lier vos comptes utilisateur.

### Liaison de votre compte IBMid
{: #link_user_account}

Si vous êtes un client d'infrastructure {{site.data.keyword.BluSoftlayer_full}} et que vous possédez également des comptes PaaS dans {{site.data.keyword.Bluemix_notm}} ou que vous les créez, vous pouvez lier IaaS et PaaS pour une vue unique de vos comptes. Pour lier vos comptes, procédez comme suit :
1. Connectez-vous à votre compte SoftLayer.
2. Depuis la page Récapitulatif du compte, cliquez sur **Nouveau ! Liez un compte Bluemix**.
3. Lisez les conditions d'utilisation et cliquez pour confirmer que vous les acceptez.
4. Effectuez l'une des étapes finales suivantes, en fonction de la configuration de votre compte :
  * Si un compte {{site.data.keyword.Bluemix_notm}} est associé à votre IBMid, vous êtes redirigé vers une page d'autorisation, puis ramené à l'étape de confirmation finale.
  * Si vous ne possédez aucun compte {{site.data.keyword.Bluemix_notm}}, vous êtes invité à en créer un.

Pour afficher les questions et réponses courantes concernant la liaison de votre compte, consultez les [foires aux questions](/docs/account/account_faq.html#al_login).

### Liaison de comptes utilisateur IBMid
{: #link_customer_accounts}

Une fois que vos comptes utilisateur sont passés à l'authentification par IBMid, les revendeurs et les distributeurs peuvent lier leurs comptes utilisateur. Pour lier des comptes client, vous devez être un utilisateur maître SoftLayer. L'IBMid correspondant à l'utilisateur principal du compte doit être le propriétaire du compte de plateforme {{site.data.keyword.Bluemix_notm}} auquel vous établissez la liaison. Prenez soin de passer en revue les remarques importantes suivantes avant de lier vos comptes :

  * L'utilisateur principal du compte SoftLayer qui est lié doit posséder un IBMid.
  * Chaque compte utilisateur que vous liez à un compte {{site.data.keyword.Bluemix_notm}} doit être détenu par un IBMid unique associé à une adresse électronique unique. Même si un IBMid unique peut être associé à plusieurs comptes SoftLayer, vous devez changer l'utilisateur principal afin qu'il corresponde à un IBMid unique pour chaque compte. Prenez contact avec le support pour changer l'utilisateur principal d'un compte SoftLayer. Pour plus d'informations, voir [Support pour l'infrastructure {{site.data.keyword.Bluemix_notm}}](/docs/customer-portal/cpsupport.html).
  * Lorsque vous ajoutez de nouveaux utilisateurs à un compte lié, vous devez les ajouter au compte SoftLayer et au compte {{site.data.keyword.Bluemix_notm}} pour qu'ils aient accès à toutes les fonctionnalités de la console unifiée.
  * Si vous possédez un compte de marque, vous utilisez Brand Agent Portal (BAP) et vous avez besoin de support lors de la liaison de votre compte, prenez contact avec l'équipe Revenue Services en leur en voyant un courrier électronique à l'adresse softlayer_revenue_services_team@wwpdl.vnet.ibm.com.
  * Tous les comptes liés dans {{site.data.keyword.Bluemix_notm}} doivent être de type Paiement à la carte. Vous pouvez créer un nouveau compte Paiement à la carte, lier un compte Paiement à la carte existant, ou lier un compte d'essai existant, qui est ensuite mis à niveau vers un compte Paiement à la carte. Vous ne pouvez pas lier des comptes  {{site.data.keyword.Bluemix_notm}} de type Abonnement.

Pour lier chaque compte SoftLayer à un compte de plateforme {{site.data.keyword.Bluemix_notm}} existant ou pour en créer un nouveau, procédez comme suit :

   1. Connectez-vous au portail client de l'infrastructure {{site.data.keyword.BluSoftlayer_full}} avec votre IBMid de compte d'utilisateur principal.
   2. A partir du portail client de l'infrastructure {{site.data.keyword.Bluemix_notm}}, cliquez sur **Lier un compte Bluemix**.
   3. Lisez et acceptez les dispositions pour la liaison de comptes SoftLayer et {{site.data.keyword.Bluemix_notm}}.
   4. Suivez les invites de l'assistant en ajoutant les utilisateurs du compte SoftLayer au compte {{site.data.keyword.Bluemix_notm}}.
   5. Lorsque vous y êtes invité, effectuez l'une des actions suivantes :
     * Si vous possédez déjà un compte {{site.data.keyword.Bluemix_notm}}, indiquez l'adresse électronique qui est associée à ce compte afin de lier les comptes.
     * Si vous ne possédez pas de compte {{site.data.keyword.Bluemix_notm}}, indiquez l'adresse électronique que vous voulez utiliser, suivez les instructions pour être invité dans {{site.data.keyword.Bluemix_notm}} et créez un compte.
   6. Après avoir lié le compte, indiquez à l'utilisateur final de chaque compte qu'il doit migrer vers l'IBMid en suivant la procédure décrite dans la section précédente intitulée [Passage à l'IBMid](/docs/account/softlayerlink.html#switchtoIBMid).

Migrez uniquement les comptes d'utilisateur final vers l'IBMid. Ne migrez pas les comptes de marque, qui sont les comptes parent des comptes utilisateur final et qui ne contiennent aucune ressource. Les utilisateurs des comptes de marque qui migrent vers l'IBMid perdent la possibilité de se connecter à Brand Agent Portal (BAP).
{: tip}

Les comptes liés se connectent à la console [{{site.data.keyword.Bluemix}} ![Icône de lien externe](../icons/launch-glyph.svg)](https://console.bluemix.net){: new_window}.

De plus, tenez compte des changements suivants après la liaison de vos comptes :
  * Vous devez utiliser vos données d'identification IBMid pour accéder à votre compte SoftLayer et à votre compte
{{site.data.keyword.Bluemix_notm}}.
  * Les remises SoftLayer existantes sont appliquées à tous les prix {{site.data.keyword.Bluemix_notm}}.
  * Vous recevez une facture en dollars américains (USD). Si vous disposez d'un compte {{site.data.keyword.Bluemix_notm}}, la facturation via {{site.data.keyword.Bluemix_notm}} pour les ressources d'infrastructure entre en vigueur au prochain cycle de facturation après que les comptes ont été liés. Pour plus d'informations, voir [Facturation en bloc pour des comptes liés](/docs/account/linking_accounts.html).
  * Vous pouvez surveiller l'utilisation de vos ressources d'infrastructure dans la console {{site.data.keyword.Bluemix_notm}}.

Une fois vos comptes liés, cette opération est irréversible.
{: tip}

## Utilisation de l'authentification multi-facteur dans les comptes liés
{: #2fa}

Si vous disposez d'un compte lié, vous pouvez utiliser la page **Paramètres** d'Identity and Access afin d'activer l'authentification multi-facteur pour votre compte. Ce type d'authentification, également communément appelé authentification à deux facteurs (2FA), ajoute une couche de sécurité pour l'accès à votre compte en plus de des habituels IBMid et mot de passe requis. L'authentification multi-facteur pour votre compte s'applique à l'ensemble des ressources de votre compte {{site.data.keyword.Bluemix_notm}} lié. Si elle est activée à votre compte, elle s'applique également à tous les utilisateurs qui ont été ajouté au compte.

L'authentification multi-facteur ne s'effectue pas par IBMid, mais par compte. Quand un IBMid est associé à plusieurs comptes et que vous passez d'un compte à l'autre, vous devez confirmer votre identité chaque fois que vous utilisez un compte différent qui nécessite une authentification à deux facteurs. Cette règle s'applique même si le compte précédent et le nouveau compte sont tous les deux configurés avec le même mécanisme d'authentification à deux facteurs.

Si vous avez déjà activé [l'authentification à deux facteurs dans le portail de contrôle](/docs/customer-portal/cpenable2fa.html#customerportal_2fa) pour les ressources de votre infrastructure et que vous activez le paramètre d'authentification multi-facteur de compte {{site.data.keyword.Bluemix_notm}}, celui-ci écrase l'authentification à deux facteurs que vous avez configurée dans le portail de contrôle. Cela signifie que vous pouvez désactiver l'authentification à deux facteurs que vous avez acquise dans le portail de contrôle au profit du paramètre d'authentification multi-facteur de compte. Toutefois, si vous êtes un utilisateur fédéré, l'authentification multi-facteur ne s'applique pas. Par conséquent, vous souhaiterez peut-être conserver votre portail de contrôle configuré avec l'authentification à deux facteurs afin de garantir la sécurité des ressources de votre infrastructure.
