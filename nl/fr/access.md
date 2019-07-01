---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords: user access, IBM Cloud account access, account owner, delegating access, confirming access

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Gestion de l'accès utilisateur au catalogue
{: #find-access}

En tant que propriétaire de compte {{site.data.keyword.Bluemix}}, vous pouvez affecter, déléguer et confirmer l'accès des utilisateurs au catalogue en utilisant une règle {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM). Vous pouvez contrôler la visibilité des services privés ajoutés au catalogue ou aux services publics créés dans le compte. Par défaut, seul le propriétaire d'un compte peut effectuer ces tâches.

## Délégation de l'accès
{: #get-access}

Vous pouvez déléguer l'accès à votre compte pour contrôler ce que les utilisateurs peuvent voir et pour contrôler le degré de droits d'accès dont ces derniers disposent. Par exemple, un utilisateur peut uniquement lire et analyser des informations alors qu'un autre peut disposer de droits lui permettant d'éditer ces informations. Pour déléguer l'accès au compte à un autre utilisateur du compte, procédez comme suit.

1. Cliquez sur **Gérer** > **Accès (IAM)**.
2. Cliquez sur **L'accès démarre avec l'utilisateur** sur la page d'arrivée.
3. Sélectionnez un utilisateur dans votre compte.
4. Cliquez sur **Règles d'accès**.
5. Cliquez sur **Affecter un accès**. Cliquez ensuite sur **Affecter l'accès aux services de gestion de compte**.
6. Sélectionnez le catalogue des ressources globales**** dans la liste Services puis le rôle **Administrateur** dans la liste Sélectionner des rôles.

Pour accorder d'autres droits, utilisez les rôles Afficheur et Editeur. Consultez le tableau suivant pour en savoir plus sur chaque rôle IAM et ce qu'il permet à un utilisateur de faire dans le cadre de l'utilisation du catalogue pour votre compte.

| Rôles de gestion de plateforme | Actions                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| Afficheur                   | Peut afficher les services privés mais ne peut pas les changer                                                            |
| Editeur                   | Peut changer les métadonnées d'objet mais ne peut pas changer la visibilité des services privés                                |
| Administrateur            | Peut changer les métadonnées d'objet ou la visibilité des services privés et peut restreindre la visibilité d'un service public  |
{: caption="Tableau 1. Exemple d'actions et de rôles de gestion de plateforme pour le catalogue" caption-side="top"}

Pour plus d'informations sur l'affectation de l'accès aux utilisateurs, voir [Affectation de l'accès aux services de gestion de compte](/docs/iam?topic=iam-account-services).

## Confirmation de votre accès
{: #confirm-access}

Lorsque vous êtes ajouté au compte d'une autre personne, les administrateurs de compte peuvent vous déléguer des niveaux d'accès afin de vous permettre d'afficher les ressources privées qui sont ajoutées au compte. Le propriétaire du compte peut aussi déléguer les autorisations d'affichage des ressources publiques dans le catalogue de compte. Vous n'avez pas cet accès par défaut. Le propriétaire du compte doit vous accorder un rôle IAM qui vous autorise à effectuer ces tâches de gestion de ressource de compte.

Vous pouvez utiliser la console {{site.data.keyword.Bluemix_notm}} ou l'interface de ligne de commande pour déterminer si vous avez le droit d'autoriser des utilisateurs spécifiques à voir une ressource privée dans le compte.

Pour utiliser la console, procédez comme suit :

  1. Sélectionnez **Gérer > Accès (IAM)**.
  2. Cliquez sur votre nom dans la liste Utilisateurs.
  3. Cliquez sur l'onglet **Règles d'accès**, dans lequel vous pouvez visualiser les règles d'accès qui vous sont affectées. Vous devez disposer du rôle Administrateur IAM Cloud pour le catalogue de ressources de votre compte pour mettre à jour la liste incluant les comptes afin de voir les ressources privées du catalogue.


Pour utiliser l'interface [CLI](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_iam#ibmcloud_commands_iam), exécutez la commande `ibmcloud iam user-policies <your-user-name>`. L'exécution de la commande génère une erreur si vous n'êtes pas administrateur du compte.
