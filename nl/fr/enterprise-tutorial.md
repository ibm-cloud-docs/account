---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, enterprise users, enterprise access, enterprise tutorial

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Entreprise - Premiers pas
{: #enterprise-tutorial}

Ce tutoriel vous guide lors de la configuration d'une entreprise par service afin que vous puissiez gérer et effectuer le suivi des coûts d'utilisation pour plusieurs comptes {{site.data.keyword.Bluemix}}. Vous apprendrez également à créer une entreprise, ajouter des comptes et les organiser dans des groupes de comptes, inviter des utilisateurs et explorer des abonnements.
{:shortdesc}

Ce tutoriel utilise une société fictive appelée *Example Corp* qui souhaite créer une entreprise avec la structure suivante. Lorsque vous suivez le tutoriel, adaptez chaque étape en fonction de la structure souhaitée et des comptes de votre organisation.

![Entreprise à quatre niveaux qui regroupe les comptes en fonction des services de l'organisation. Par exemple, les groupes de comptes sont nommés Marketing, Développement et Ventes. Le groupe de comptes contient des comptes pour les équipes de ces services. Par exemple, le groupe de comptes Ventes contient des comptes appelés Direct, En ligne et Activation.](images/enterprise-by-dept.svg "Entreprise organisant les comptes en fonction des services de l'organisation.")

## Avant de commencer
{: #setting-prereqs}

Voir [Qu'est-ce qu'une entreprise ?](/docs/account?topic=account-enterprise) pour obtenir des informations sur la gestion des comptes, la facturation, les ressources et la gestion des accès et des utilisateurs dans une entreprise. 

Vérifiez que vous disposez de l'accès requis dans un compte Abonnement, qui sert de compte de base à partir duquel vous créez l'entreprise. Pour effectuer cette action, vous devez être propriétaire de compte ou disposer du rôle Administrateur sur le service de gestion des comptes Facturation.

La création d'une entreprise à partir d'un compte et l'importation de comptes existants ne peuvent pas être annulées. Ce tutoriel est fourni en tant qu'exemple de procédure que vous pouvez suivre pour configurer une entreprise par service. Cependant, vous devez planifier avec soin la structure de votre entreprise en fonction des besoins de votre organisation.
{:important}

## Etape 1. Création de l'entreprise
{: #create_enterprise_tutorial}

Les entreprises sont créées à partir d'un compte Abonnement existant. Lorsque vous créez l'entreprise, le compte est ajouté à la hiérarchie de l'entreprise. La facturation du compte est désormais gérée par l'entreprise mais ses utilisateurs et ses ressources restent identiques et ne sont pas affectés. Pour obtenir une description complète des conséquences sur les comptes, voir [Création d'une entreprise](/docs/account?topic=account-create-enterprise).

1. Accédez à **Gérer** > **Entreprise** puis cliquez sur **Créer**.
2. Entrez le nom de votre entreprise (Example Corp, par exemple) pour identifier votre entreprise.
3. Entrez le domaine de votre entreprise, comme `examplecorp.com`.
4. Consultez les informations sur les conséquences pour votre compte puis sélectionnez **Je comprends l'impact sur mon compte**. Cliquez ensuite sur **Créer**. Le compte fait désormais définitivement partie de l'entreprise et ne peut pas être retiré.

Une fois que votre entreprise est créée, le tableau de bord de l'entreprise s'affiche. Vous pouvez alors consulter les détails de l'entreprise, les comptes, les utilisateurs et les informations de facturation. Accédez à la page **Comptes** pour afficher la structure de l'entreprise où vous pouvez voir les comptes suivants :
  * Un compte d'entreprise ayant le même nom que votre entreprise. Ce compte est utilisé pour la gestion d'entreprise.
  * Le compte à partir duquel vous avez créé l'entreprise. Les utilisateurs peuvent continuer à utiliser les ressources du compte qui ne sont pas affectées.

## Etape 2. Création d'une structure d'entreprise avec des groupes de comptes
{: #account_groups_tutorial}

Utilisez des groupes de comptes afin d'organiser les comptes liés. Le deuxième et le troisième niveaux de la hiérarchie de la structure Example Corp. contiennent les groupes de comptes Marketing, Développement, Ventes, Conception et Ingénierie. Procédez comme suit pour créer les groupes de comptes :

1. Dans le tableau de bord de l'entreprise, cliquez sur **Comptes** pour afficher les comptes et les groupes de comptes de l'entreprise.
2. Dans la section de groupe de comptes, cliquez sur **Créer**.
3. Entrez le nom du groupe de comptes (`Marketing`, par exemple).
4. Dans la zone de contact, entrez l'IBMid de l'utilisateur devant être le contact principal pour le groupe de comptes. Etant donné qu'un groupe de comptes ne peut pas contenir de ressources, il n'a pas de propriétaire, contrairement à un compte.
5. Sélectionnez **Example Corp** comme compte parent.
6. Cliquez sur **Créer**.

Répétez la procédure pour créer les groupes de comptes Ventes, Développement, Conception et Ingénierie. Lorsque vous créez les groupes de comptes Conception et Ingénierie, ajoutez le compte Développement comme groupe de comptes parent.

## Etape 3. Importation de comptes existants
{: #existing_accounts_tutorial}

Maintenant que vous avez créé une structure d'entreprise, vous pouvez importer dans l'entreprise un compte existant. Lorsque vous importez un compte, il est ajouté définitivement à l'entreprise. Comme lors de la création d'une entreprise, la facturation des comptes importés est désormais gérée par l'entreprise mais ses utilisateurs et ses ressources restent identiques. Pour plus de détails, voir [Importation de comptes existants](/docs/account?topic=account-enterprise-add#add-accounts).

Pour importer un compte existant, l'accès suivant est requis :

* Dans le compte à importer, vous devez être propriétaire du compte ou disposer du rôle Administrateur sur les services de gestion des comptes Entreprise et Facturation dans le compte.
* Dans le compte d'entreprise, vous devez disposer du rôle Editeur ou Administrateur sur le service Entreprise et du rôle Administrateur sur le service Facturation.

Procédez comme suit pour importer le compte UX-UI exemple dans le groupe de comptes Conception :
1. Dans le tableau de bord d'entreprise, cliquez sur **Comptes** pour afficher les comptes et les groupes de comptes de l'entreprise.
2. Dans la section Comptes, cliquez sur **Ajouter** > **Importer le compte**.
3. Sélectionnez **UX-UI** dans la liste **Compte**.

  Si aucun compte n'est affiché, il est fort probable que vous ne disposiez pas de l'accès correct pour les comptes existants.
  {: tip}

4. Sélectionnez **Conception** comme parent du compte UX-UI. Cette sélection permet de déterminer l'emplacement du compte dans la hiérarchie d'entreprise.
5. Consultez les informations sur les conséquences pour votre compte puis sélectionnez **Je comprends l'impact sur mon compte**. Cliquez ensuite sur **Importer**.

Répétez la procédure pour importer d'autres comptes.

## Etape 4. Création de comptes
{: #create-accounts_tutorial}

Vous pouvez créer des comptes dans votre entreprise. Les comptes créés sont des comptes Paiement à la carte et l'utilisation est facturée à l'entreprise. Pour créer un compte, vous avez besoin d'une règle d'accès avec le rôle Editeur ou Administrateur sur le service Entreprise.

Procédez comme suit pour créer le compte Web exemple dans votre entreprise :

1. Dans le tableau de bord Entreprise, cliquez sur **Comptes** pour afficher les comptes et les groupes de comptes de l'entreprise.
1. Dans la section Comptes, sélectionnez **Ajouter** > **Créer un compte**.
1. Entrez `Web` comme nom de compte.
1. Si vous souhaitez définir un autre utilisateur comme propriétaire de compte, entrez son IBMid dans la zone **Propriétaire**. Le propriétaire de compte a un accès complet au compte.
1. Sélectionnez **Marketing** comme parent de ce compte.
1. Cliquez sur **Créer**.

Une fois que vous avez créé le compte, le propriétaire du compte peut se connecter au compte pour inviter d'autres utilisateurs et gérer l'accès.

Répétez la procédure pour créer d'autres comptes. Par exemple, l'entreprise Example Corp inclut le compte enfant et la hiérarchie de groupes de comptes parent suivants.

| Enfant | Parent |
| ----- | -------|
| Impression | Marketing |
| Front-end | Ingénierie |
| Back-end | Ingénierie |
| Direct | Ventes |
| En ligne | Ventes |
| Activation | Ventes |
{:caption="Tableau 1. Compte enfant et hiérarchie de groupes de comptes parent" caption-side="top"}

## Etape 5. Exploration d'abonnements
{: #explore-sub_tutorial}

Vous pouvez explorer les abonnements de l'entreprise à partir du tableau de bord de l'entreprise. Tout abonnement existant des comptes importés dans l'entreprise est déplacé dans le compte d'entreprise et ajouté au [pool de crédit](/docs/billing-usage?topic=billing-usage-enterprise#credit-pool) de l'entreprise.

1. Retournez au tableau de bord Entreprise en cliquant sur **Tableau de bord**. Dans la section Facturation, vous pouvez consulter le crédit disponible, le crédit restant et les dates d'expiration de l'abonnement.
1. Pour consulter les détails de tous les abonnements de l'entreprise, cliquez sur **Afficher les abonnements**.

   Dans la section Abonnements de plateforme, vous pouvez afficher la date de début d'abonnement, la date de fin, le crédit de départ et le crédit disponible. Pour ajouter du crédit supplémentaire, vous pouvez acheter des abonnements et appliquer le code d'abonnement.

## Etape 6. Affectation de l'accès aux utilisateurs des comptes enfant leur permettant de créer des ressources
{: #users_create_resources}

Avant de commencer, assurez-vous de vous trouver dans le compte où vous souhaitez créer la ressource. Accédez au compte *Impression*. Si vous souhaitez que les utilisateurs de votre compte créent des ressources à partir du catalogue et qu'ils les affectent à un groupe de ressources, vous devez affecter deux types de règle d'accès.
* Affectez une règle d'accès avec le rôle Afficheur ou un rôle supérieur sur le groupe de ressources.
* Affectez une règle d'accès avec le rôle Editeur ou Administrateur sur le service.

Procédez comme suit pour affecter l'accès requis :

1. Accédez à **Gérer** > **Accès (IAM)** puis sélectionnez **Utilisateurs**.
2. Sélectionnez un nom d'utilisateur dans la liste.
3. Cliquez sur l'onglet **Règles d'accès** puis sélectionnez **Affecter un accès**.
4. Cliquez sur **Affecter l'accès au sein d'un groupe de ressources**.
5. Sélectionnez le groupe de ressources auquel vous souhaitez affecter l'accès utilisateur.
6. Sélectionnez le rôle Afficheur ou un rôle supérieur sur le groupe de ressources.
7. Sélectionnez le service auquel vous souhaitez affecter l'accès utilisateur.
  * Si vous souhaitez que l'utilisateur puisse mettre à disposition un service, sélectionnez **Tous les services**.
  * Si vous souhaitez affecter à l'utilisateur un accès spécifique, sélectionnez un service dans la liste. L'utilisateur a accès uniquement au service sélectionné.
8. Sélectionnez le rôle Editeur ou Administrateur.
9. Cliquez sur **Affecter**.

## Etape 7. Consultation de l'utilisation de tous les comptes
{: #usage_tutorial}

1. Connectez-vous au compte d'entreprise Example Corp.
2. Accédez à **Gérer > Facturation et utilisation** puis sélectionnez **Utilisation**.

   La page Utilisation affiche les coûts de l'ensemble de l'utilisation dans votre entreprise, répartie par compte et groupe de comptes. Les informations d'utilisation des services d'infrastructure classique ne sont pas incluses pour la période de facturation en cours. Pour plus d'informations, voir [Affichage de l'utilisation pour vos ressources de l'infrastructure classique](/docs/billing-usage?topic=billing-usage-infra-usage).
3. Cliquez sur **Marketing** dans le tableau pour afficher l'utilisation dans le groupe de comptes. Comme pour le niveau d'entreprise, l'utilisation est répartie par compte et groupe de comptes.
4. Pour afficher l'utilisation par ressource, accédez au niveau de compte en cliquant sur les groupes de comptes dans le tableau ou en sélectionnant le compte dans le menu **Entreprise**. Les coûts sont affichés pour chaque type de ressource utilisé pendant la période définie.

Répétez la procédure pour afficher l'utilisation pour les groupes de comptes Développement, Ventes, Conception et Ingénierie.

   A partir du compte d'entreprise, vous ne pouvez pas consulter les données d'utilisation de l'instance ou du plan de ressources car l'accès dans le compte est requis. Cliquez sur **Passer au compte** pour afficher les données du compte. Vous avez besoin de l'accès de facturation aux ressources et aux services du compte. Pour plus d'informations, voir [Affichage de votre utilisation](/docs/billing-usage?topic=billing-usage-viewingusage).

Les données s'affichent dans le compte d'entreprise uniquement pour l'utilisation facturée par les comptes de l'entreprise. Pour afficher l'utilisation avant l'ajout d'un compte à l'entreprise, connectez-vous à ce dernier et sélectionnez la période souhaitée.
{: note}
