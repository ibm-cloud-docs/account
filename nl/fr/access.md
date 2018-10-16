---

copyright:

  years: 2017, 2018
lastupdated: "2018-10-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Gestion de l'accès au catalogue
{: #find-access}

En tant que propriétaire de compte, vous pouvez affecter des accès en utilisant une règle IAM. Cela permet aux utilisateurs de gérer la visibilité des services privés ajoutés au catalogue de compte ou des services publics qui ont été créés dans le compte. Par défaut, seul le propriétaire d'un compte peut effectuer ces tâches.

## Comment déléguer l'accès en tant que propriétaire de compte ?
{: #get-access}

En tant que propriétaire de compte, vous pouvez donner accès au compte en affectant une règle d'accès à un utilisateur via l'interface utilisateur Identity and Access. Pour vous assurer que l'utilisateur dispose de l'accès nécessaire, sélectionnez la ressource relative au catalogue global et le rôle **Administrateur** pour la règle d'accès.

Pour accorder d'autres droits, utilisez les rôles IAM (Identity and Access Management) `Afficheur` et `Editeur`. Consultez le tableau suivant pour en savoir plus sur chaque rôle IAM et ce qu'il permet à un utilisateur de faire dans le cadre de l'utilisation du catalogue pour votre compte.

| Rôle Gestion de la plateforme | Description des actions |
|:-----------------|:-----------------|
| Afficheur | Peut voir les services privés, mais ne peut pas apporter de modifications. |
| Editeur | Peut modifier les métadonnées d'objet mais ne peut pas changer la visibilité. |
| Administrateur | Peut changer les métadonnées d'objet ou la visibilité.  |
{: caption="Tableau 1. Exemple d'actions et de rôles de gestion de plateforme pour le service de catalogue" caption-side="top"}

Pour des instructions pas à pas sur l'affectation d'un accès à votre compte aux utilisateurs, voir la documentation [Accès aux ressources](/docs/iam/mngiam.html#iammanidaccser#resourceaccess).

## Comment vérifier si j'ai accès ?

Quand vous êtes ajouté au compte d'une autre personne, cette dernière peut vous déléguer des niveaux d'accès afin de vous permettre d'afficher les ressources privées qui sont ajoutées au compte. Le propriétaire du compte peut aussi déléguer les autorisations d'affichage des ressources publiques dans le catalogue de compte. Vous n'avez pas cet accès par défaut. Le propriétaire du compte doit vous accorder un rôle IAM qui vous autorise à effectuer ces tâches de gestion de ressource de compte.

Vous pouvez utiliser l'interface de ligne de commande ou l'interface utilisateur Identity and Access pour déterminer si vous avez le droit d'autoriser des utilisateurs spécifiques à afficher une ressource privée qui est ajoutée au compte.

Pour vous servir de l'interface utilisateur Identity and Access, procédez comme suit :

1. Accédez à **Gérer** > **Accès (IAM)**, puis cliquez sur **Utilisateurs**.
2. Cliquez sur votre nom dans la liste Utilisateurs.
3. Cliquez sur l'onglet **Règles d'accès**, dans lequel vous pouvez visualiser les règles d'accès qui vous sont affectées. Vous devez disposer du rôle Administrateur IAM Cloud pour le catalogue de ressources de votre compte pour mettre à jour la liste incluant les comptes afin de voir les ressources privées du catalogue.

Pour utiliser l'[interface de ligne de commande {{site.data.keyword.Bluemix_notm}}](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_iam), procédez comme suit :

Entrez la commande suivante, accompagnée de votre nom d'utilisateur `ibmcloud iam user-policies <your-username>` pour voir si vous êtes administrateur des comptes sélectionnés dans l'interface de ligne de commande. Si vous n'êtes pas administrateur de l'un ou plusieurs des comptes, ces commandes renvoient une erreur indiquant que vous n'êtes pas autorisé.
{: tip}
