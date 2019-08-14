---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: account settings, delete account, account errors, reassign account, view tags, batch registration, transfer account ownership

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:tip: .tip}

# Foire aux question concernant les comptes
{: #accountfaqs}

Les foires aux questions concernant {{site.data.keyword.cloud}} peuvent inclure des questions sur les comptes Lite, la réaffectation d'utilisateur, les erreurs de compte ou les étiquettes de compte. Pour trouver toutes les foires aux questions concernant {{site.data.keyword.cloud_notm}}, consultez notre bibliothèque de foires aux questions.
{: shortdesc}

## Comment créer un compte ?
{: #create-account}
{: faq}

Accédez à [{{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe") puis cliquez sur **Créer un compte {{site.data.keyword.Bluemix_notm}}** pour créer un compte Lite n'arrivant jamais à expiration. Pour plus de détails sur les fonctions incluses, voir [Compte Lite](/docs/account?topic=account-liteaccount#liteaccount).


## Comment résoudre les erreurs survenant lors de la création de mon compte ?
{: #account-error}
{: faq}

Si vous pouvez vous connecter à un compte {{site.data.keyword.Bluemix_notm}}, accédez au [support](https://test.cloud.ibm.com/unifiedsupport/supportcenter) et choisissez une des options suivantes.

* Si vous disposez du support avancé ou premium, cliquez sur **Dialogue en ligne** pour parler à un responsable de l'assistance technique {{site.data.keyword.Bluemix_notm}}.
* Créez un cas de support en cliquant sur **Créer un cas** dans la section _Besoin d'aide ?_

   Un message électronique vous sera envoyé après l'ouverture du cas. Suivez les instructions pour toute communication supplémentaire.

Si vous ne pouvez pas vous connecter à un compte {{site.data.keyword.Bluemix_notm}}, [créez une demande de compte](https://watson.service-now.com/x_ibmwc_open_case_app.do#!/create){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe").

## Qu'est-ce que Cloud Foundry ?
{: #cloud-foundry}
{: faq}

Cloud Foundry est une plateforme sous forme de services (PaaS) à source ouverte disponible via {{site.data.keyword.Bluemix_notm}} Public pour la génération et le déploiement d'applications sur le cloud. Les organisations et les espaces Cloud Foundry sont utilisés pour organiser les ressources et les applications disponibles dans des régions spécifiques.

Pour plus d'informations sur la gestion des organisations et des espaces, voir [Ajout d'organisations et d'espaces](/docs/account?topic=account-orgsspacesusers#orgsspacesusers). Pour plus d'informations sur l'accès aux ressources d'un espace Cloud Foundry, voir [Accès Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfaccess).


## Puis-je déplacer une organisation dans un autre compte ?
{: #move-org-diff-account}
{: faq}

Vous ne pouvez pas actuellement déplacer une organisation vers un autre compte. Toutefois, vous pouvez recréer l'organisation avec les mêmes données d'identification dans un autre compte pour reproduire cette fonctionnalité. Pour plus d'informations, voir [Ajout d'organisations et d'espaces](https://cloud.ibm.com/docs/account?topic=account-orgsspacesusers#createorg).


## Quelles régions Cloud Foundry puis-je utiliser ?
{: #whichregions}
{: faq}

Dans un compte Lite, vous ne pouvez travailler que dans une seule région. Dans un compte Paiement à la carte ou Abonnement, vous pouvez accéder à toutes les régions disponibles.


## Qu'est-ce qu'un plan de tarification Lite pour des services ?
{: #whatisliteplan}
{: faq}

Un plan Lite désigne un plan de service basé sur un quota gratuit. Vous pouvez utiliser un plan de service Lite pour construire une application sans encourir aucun frais. Un plan Lite peut être proposé sur une base mensuelle (renouvelé chaque mois) ou ponctuelle. Vous ne pouvez avoir qu'une seule instance par plan de service Lite. Les plans de tarification Lite sont offerts dans tous les comptes. Pour plus d'informations sur les comptes Lite, voir [Types de compte](/docs/account?topic=account-accounts#accounts).


## Que se passe-t-il lorsque mon quota mensuel d'instances de plan Lite est atteint ?
{: #monthlyquota}
{: faq}

Lorsque la limite de quota relative aux instances de plan Lite est atteinte, le service est suspendu pour le mois concerné. Les limites de quota sont définies au niveau des organisations et non au niveau des instances. Les nouvelles instances créées dans la même organisation reflètent les utilisations depuis les instances précédentes. Les limites de quota sont réinitialisées le premier jour de chaque mois.

Pour vérifier votre utilisation, accédez à **Gérer > Facturation et utilisation** puis sélectionnez **Utilisation**. Pour plus d'informations, voir [Affichage de votre utilisation](/docs/billing-usage?topic=billing-usage-viewingusage).

## Comment supprimer un service de mon compte ?
{: #accounts-service-removal}
{: faq}

Si vous souhaitez supprimer un service, vous pouvez le faire depuis la liste de ressources. Découvrez comment dans [Utilisation des ressources et des services](/docs/resources?topic=resources-resources-faq#service-removal).

## Combien de groupes de ressources, d'organisations ou d'espaces puis-je créer ?
{: #resourcelimit}
{: faq}

Si vous avez un compte facturable, le nombre de groupes de ressources, d'organisations ou d'espaces que vous pouvez créer dans votre compte est illimité. En revanche, si vous utilisez un compte Lite, vous êtes limité à une organisation et à un groupe de ressources.

## Comment mettre à niveau ou convertir mon type de compte ?
{: #changeacct}
{: faq}

Pour mettre à niveau un compte Lite, accédez à [Paramètres de compte](https://{DomainName}/account/settings). Dans la section Mise à niveau du compte, cliquez sur **Ajouter une carte de crédit** pour effectuer une mise à niveau vers un compte de paiement à la carte ou cliquez sur **Mise à niveau** pour une mise à niveau vers un compte d'abonnement. Vous pouvez également appliquer un code de fonction promotionnel pour convertir votre compte Lite en compte d'essai sur la page Paramètres de compte.

Pour effectuer une conversion entre des types de compte Paiement à la carte et Abonnement, prenez contact avec le [service commercial {{site.data.keyword.Bluemix_notm}}![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}.

Si vous ne savez pas quel est votre type de compte, consultez la page Paramètres de compte. Pour plus d'informations, voir [Mise à niveau de votre compte](/docs/account?topic=account-upgrading-account).

## Si je mets à niveau mon compte Lite, puis-je continuer d'utiliser mes instances existantes ?
{: #nochange}
{: faq}

Oui, si vous procédez à une mise à niveau vers un compte facturable, vous pouvez continuer d'utiliser les instances créées avec votre compte Lite.

## Comment mettre à jour ma carte de crédit ?
{: #updatepayment}
{: faq}

Mettre à jour votre carte de crédit équivaut à ajouter une nouvelle carte. Accédez à [Paiements](https://{DomainName}/billing/payments) et, dans la section Ajouter méthode de paiement, entrez les informations de facturation correspondant à votre nouvelle carte puis cliquez sur **Ajouter une carte de crédit**.

Pour utiliser une autre méthode de paiement, sélectionnez **Payer autrement** puis cliquez sur **Soumettre la demande de changement**. Un cas de support concernant le changement de méthode de paiement sera créé pour vous.

## Comment modifier mes paramètres de notification par courrier électronique ?
{: #change-email-prefs}
{: faq}

Vous pouvez modifier les notifications par courrier électronique que vous recevez pour des événements planifiés ou non planifiés ainsi que les annonces dans vos paramètres de profil.
1. Accédez à [Notifications](https://cloud.ibm.com/user/notifications) dans vos paramètres de profil.
1. Sélectionnez si vous voulez recevoir des notifications par courrier électronique pour chaque type d'événement.

Concernant les services d'infrastructure classique, les propriétaires de compte peuvent également abonner des utilisateurs à des notifications provenant de ces services en accédant à **Gérer > Compte > Notifications**.

Pour plus d'informations, voir [Définition des préférences de courrier](/docs/account?topic=account-email-prefs).

## Comment réinitialiser mon mot de passe ?
{: #reset-password}
{: faq}

Pour réinitialiser votre mot de passe de compte, accédez à l'icône **Avatar** ![Icône Avatar](../icons/i-avatar-icon.svg) **> Profil et paramètres**. Cliquez ensuite sur **Modifier ou Réinitialiser** dans la section d'informations Utilisateurs du compte.

Pour réinitialiser votre mot de passe VPN, procédez comme suit :

  1. Accédez à **Gérer > Accès (IAM)** puis sélectionnez **Utilisateurs**.
  2. Sélectionnez l'utilisateur.
  3. Dans la section Sous-réseaux VPN, cliquez sur l'icône Editer ![Icône Editer](../icons/icon_write.svg) pour entrer un nouveau mot de passe VPN.
  5. Cliquez sur **Appliquer**.

## Comment résilier mon compte ?
{: #cancelaccount}
{: faq}

Nous nous désolons de votre départ. Si nous pouvons vous être utile, n'hésitez pas à contacter le support.

Si vous maintenez votre décision malgré tout, le mode de résiliation de votre compte dépend du type de ce dernier. Pour connaître votre type de compte, accédez à la section [Paramètres de compte](https://cloud.ibm.com/account/settings) et consultez les données indiquées dans _Type de compte_.

* Pour les comptes Paiement à la carte ou Abonnement, la manière la plus rapide d'annuler votre compte consiste à nous contacter via la [discussion en ligne](https://{DomainName}/unifiedsupport/supportcenter) ou en nous appelant au numéro 1-866-325-0045 et en sélectionnant la troisième option. Vous pouvez également ouvrir un cas de support.
* Pour annuler un compte Lite, accédez à [Paramètres de compte](https://cloud.ibm.com/account/settings) et cliquez sur **Désactiver le compte**.

## Comment supprimer mon compte ?
{: #deleteaccount}
{: faq}

Contactez le [service de support {{site.data.keyword.Bluemix_notm}}![Icône de lien externe](../icons/launch-glyph.svg)](https://{DomainName}/unifiedsupport/supportcenter){: new_window} pour ouvrir un cas de support et demander la suppression de votre compte. Si des données sont associées à votre ancien compte et que vous souhaitez les déplacer vers un nouveau compte, incluez ces informations dans votre message électronique.

## Comment puis-je retirer mes données à caractère personnel d'{{site.data.keyword.Bluemix_notm}} ?
{: #remove-pi}
{: faq}

Pour comprendre comment IBM gère les informations personnelles, voir la [déclaration de confidentialité IBM![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe")](https://www.ibm.com/privacy/){: new_window}. Dans la section Your Rights, lisez les informations expliquant ce que vous pouvez demander à retirer. Cliquez sur le lien dans la section pour soumettre une demande de retrait de vos informations personnelles.

## Pourquoi mon compte est-il désactivé ?
{: #account-deactivated}
{: faq}

Votre compte peut être désactivé pour les raisons suivantes :

- La période d'essai est terminée pour les comptes d'essai. Pour réactiver votre compte, connectez-vous à ce dernier et effectuez une mise à niveau vers un compte Paiement à la carte. 
Quelques jours peuvent être nécessaires pour réactiver complètement votre compte.
- Un utilisateur autorisé a annulé le compte.
- Le compte a été suspendu. IBM peut, à sa seule discrétion, désactiver sans aucun préavis les comptes ne respectant pas les comportements d'utilisation acceptables des services {{site.data.keyword.Bluemix_notm}}. Certains services peuvent être restaurés si les utilisateurs modifient leur comportement après avoir reçu une notification signalant l'action fautive.

Si vous pensez que votre compte a été désactivé à tort, contactez le service de support en appelant le 1-866-325-0045 et en sélectionnant la troisième option.

## A quelles formes de support peut-on accéder ?
{: #contactsupport}
{: faq}

Cliquez sur **Support** dans la barre de menus de la console pour accéder au centre de support. Pour plus d'informations, voir [Support](/docs/get-support?topic=get-support-support-plans).

## Puis-je souscrire à un essai gratuit ?
{: #freetrial}
{: faq}

Les comptes {{site.data.keyword.Bluemix_notm}} Lite fournissent l'accès aux services gratuits du plan Lite. Vous pouvez utiliser ces services aussi longtemps que vous voulez sans être facturé et votre compte n'expire jamais. [Inscrivez-vous pour obtenir un compte Lite](https://{DomainName}/registration).

Des comptes d'essai {{site.data.keyword.Bluemix_notm}} sont disponibles pour les enseignants et les étudiants d'institutions académiques accréditées. Pour être éligible pour un compte d'essai, accédez au site [Harness the Power of IBM ![Icône de lien externe](../icons/launch-glyph.svg)](https://ibm.biz/academic){: new_window} et validez les données d'identification de votre institution. Contrairement aux comptes Lite, les comptes d'essai expirent à la fin de la période d'essai.

## Puis-je me connecter à la console {{site.data.keyword.Bluemix_notm}} avec mon ID SoftLayer ?
{: #slid}
{: faq}

Oui, vous pouvez utiliser votre ID SoftLayer pour vous connecter à la console. Accédez à la [page de connexion](https://cloud.ibm.com/login){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe") et sélectionnez **ID SoftLayer** dans la liste d'**ID**.  

## Après avoir lié mon compte, comment puis-je me connecter ?
{: #al_login}
{: faq}

Une fois que avez lié votre compte, utilisez votre IBMid pour établir une connexion à la console {{site.data.keyword.Bluemix}}.

## Une fois que j'ai lié mon compte, quel est l'impact sur mon support ?
{: #al_support}
{: faq}

Une fois que vous avez lié votre compte, vous conservez le même niveau de support lorsque vous ajoutez la plateforme {{site.data.keyword.Bluemix_notm}} à votre compte.

## Existe-t-il d'autres moyens pour obtenir de l'aide relative à la liaison de mon compte ?
{: #al_morehelp}
{: faq}

  1. Consultez le blogue [Steps to Link your IaaS and PaaS Accounts](https://www.ibm.com/blogs/bluemix/2018/03/follow-steps-link-iaas-paas-accounts/){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe") pour obtenir des informations utiles.
  2. A partir du portail client {{site.data.keyword.BluSoftlayer_full}}, ouvrez une session de **discussion en ligne avec le service commercial** pour poser des questions relatives à votre compte.
  3. Ouvrez un ticket à partir du portail client. Sélectionnez **Support** > **Ajouter un ticket** puis, dans la zone **Objet**, sélectionnez **Demande pour comptabilisation** afin de transmettre votre question sur votre compte à l'équipe de support appropriée.

## Comment puis-je lier mon compte si je possède plusieurs comptes ?
{: #al_multacct}
{: faq}

Si vous possédez plusieurs comptes SoftLayer, vous devez lier les comptes ayant un compte de plateforme {{site.data.keyword.Bluemix_notm}} correspondant et un IBMid associé.

Si vous n'avez pas de compte de plateforme {{site.data.keyword.Bluemix_notm}} correspondant et de compte IBMid associé, un nouveau compte SoftLayer peut être créé pour lier les comptes.

## Des primes s'appliquent-elles pour la liaison de mes comptes ?
{: #al_incent}
{: faq}

Lorsque vous liez vos comptes, vous pouvez utiliser un crédit promotionnel de 200 $ afin d'essayer des services {{site.data.keyword.Bluemix_notm}}.

Pour en savoir plus sur le crédit promotionnel de 200 $, voir la rubrique présentant le [compte Paiement à la carte](/docs/account?topic=account-accounts#paygo).

## Que se passe-t-il si j'ajoute des services de plateforme {{site.data.keyword.Bluemix_notm}} à mon compte SoftLayer ?
{: #al_owaffslacct}
{: faq}

Avec cet ajout, votre compte a accès à toutes les offres de la plateforme {{site.data.keyword.Bluemix_notm}}. Une fois que vous avez ajouté l'offre de plateforme {{site.data.keyword.Bluemix_notm}} à votre compte, votre responsable de compte doit activer l'accès à l'offre pour l'utilisateur.

Pour plus d'informations sur la fonction de responsable de compte, voir [Gestion des utilisateurs](/docs/iam?topic=iam-iamuserinv#iamuserinv).

## De quelle manière la liaison de compte impacte-t-elle mon ID de compte principal SoftLayer ?
{: #al_howaffslmastacct}
{: faq}

Vous pouvez toujours utiliser l'ID de votre compte SoftLayer pour vous connecter au portail client car la console {{site.data.keyword.Bluemix_notm}} est accessible à l'aide des IBMid.

## Comment puis-je visualiser les comptes que je possède ?
{: #accounts-owned}
{: faq}

L'en-tête de console IBM Cloud répertorie tous les comptes qui sont affiliés à votre ID de connexion, y compris ceux que vous possédez. Vous pouvez visualiser votre rôle dans chaque compte sur la page [Utilisateurs](https://{DomainName}/iam/users).

Vous pouvez également définir vos comptes à partir de l'interface de ligne de commande en exécutant la commande `ibmcloud account list`.

## Comment puis-je passer d'un compte à un autre ?
{: #switch-between-accounts}
{: faq}

Si vous possédez plusieurs comptes, vous pouvez cliquer sur le nom de votre compte dans la barre de menus de la console pour sélectionner un autre compte auquel vous avez accès.  

![Capture d'écran du sélecteur de compte dans la barre de menus de la console. Le sélecteur de compte affiche le nom de compte et le numéro de compte, et vous sélectionnez le compte en cours pour afficher la liste d'autres comptes auxquels vous pouvez accéder.](images/account-faq.svg "Le sélecteur de compte affiche le nom de compte et le numéro de compte, et vous sélectionnez le compte en cours pour afficher la liste d'autres comptes auxquels vous pouvez accéder.")

## Puis-je changer le propriétaire d'un compte ?
{: #switch-account-owners}
{: faq}

Vous pouvez transférer la propriété de ressources individuelles au sein de votre compte à quelqu'un d'autre à l'aide de la commande `ibmcloud catalog`. Pour en savoir plus sur, voir [Transfert de la propriété d'une ressource privée](/docs/account?topic=account-include#owners).

Pour transférer la propriété de la totalité de votre compte, mettez à jour votre [profil de société](https://{DomainName}/account/company-profile). Pour plus d'informations, voir [Transfert de propriété de votre compte](/docs/account?topic=account-transfer).

## Comment modifier le nom ou l'IBMid dans mon profil ?
{: #change-profile-settings}
{: faq}

Vous pouvez modifier vos informations personnelles, telles que le nom, le courrier électronique ou le numéro de téléphone, en cliquant sur l'icône **Avatar** ![IcôneAvatar](../icons/i-avatar-icon.svg) **> Profil et paramètres**. Vous ne pouvez pas modifier votre IBMid, mais vous pouvez, au besoin, en créer un nouveau. Le [centre d'assistance mondial IBM piur les IBMid](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html) est disponible pour vous aider sur les questions générales liées aux ID qui ne concernent pas votre compte {{site.data.keyword.Bluemix_notm}}.


## Comment puis-je changer la langue associée à mon compte ?
{: #switch-account-lang}
{: faq}

La langue utilisée dépend des paramètres de votre navigateur Web. Pour afficher le contenu dans votre langue maternelle, mettez à jour les paramètres linguistiques de votre navigateur.

## {{site.data.keyword.Bluemix_notm}} prend-il en charge l'enregistrement par lots d'utilisateurs ?
{: #batch-registration}
{:faq}

Lorsque vous enregistrez des utilisateurs pour {{site.data.keyword.Bluemix_notm}}, vous devez enregistrer chaque utilisateur individuellement. {{site.data.keyword.Bluemix_notm}} ne prend pas en charge l'enregistrement d'utilisateurs par lots.

Accédez à [{{site.data.keyword.Bluemix}}](https://cloud.ibm.com){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe") puis cliquez sur **Créer un compte {{site.data.keyword.Bluemix_notm}}**. Remplissez ensuite le formulaire d'enregistrement de compte pour chaque utilisateur individuel.

## Qu'est-ce qu'une étiquette ?
{: #know-about-tags}
{: faq}

Vous pouvez utiliser des étiquettes pour organiser et afficher des ressources de votre compte en filtrant des étiquettes dans votre liste de ressources. Pour plus d'informations, voir [Utilisation d'étiquettes](/docs/resources?topic=resources-tag).

## Qui peut voir les étiquettes d'un compte ?
{: #tags-visibility-account}
{: faq}

Les étiquettes sont visibles dans votre compte. Si vous êtes autorisé à voir une ressource, vous pouvez également voir toutes les étiquettes qui lui sont associées. Pour plus d'informations, voir [Octroi aux utilisateurs de l'accès leur permettant d'étiqueter des ressources](/docs/resources?topic=resources-access#access).

## De quels droits dois-je disposer pour ajouter ou retirer des étiquettes ?
{: #permissions-add-remove-tags}
{: faq}

Vous devez disposer au moins du rôle Editeur pour les ressources activées par IAM ou du rôle Développeur dans un espace Cloud Foundry sur une ressource pour ajouter ou retirer des étiquettes sur cette dernière. Pour plus d'informations, voir [Octroi aux utilisateurs de l'accès leur permettant d'étiqueter des ressources](/docs/resources?topic=resources-access#access).

## Puis-je supprimer mon étiquette ?
{: # delete-tag}
{: faq}

Avant de pouvoir supprimer une étiquette, vous devez la retirer de toutes les ressources. Si vous ne pouvez toujours pas la supprimer, il est possible que l'étiquette soit associée à une ressource que vous n'êtes pas autorisé à consulter. La même étiquette peut être associée à plusieurs ressources par différents utilisateurs du même compte de facturation. Les utilisateurs ne peuvent pas tous voir les mêmes ressources du compte.

## Puis-je renommer une étiquette ?
{: #rename-tag}
{: faq}

Vous ne pouvez pas modifier le nom d'une étiquette. Pour renommer une étiquette, retirez-la et réaffectez la ressource avec une nouvelle étiquette.  
