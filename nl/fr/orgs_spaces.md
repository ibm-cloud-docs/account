---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-08"

keywords: account, add orgs, add spaces, manage users, user access

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Ajout d'organisations et d'espaces
{: #orgsspacesusers}

En tant que propriétaire de compte {{site.data.keyword.Bluemix}}, vous pouvez ajouter des organisations et des espaces à votre compte. Si vous êtes responsable d'une organisation, vous pouvez gérer les organisations du compte. Pour gérer des espaces et des organisations Cloud Foundry accédez à **Gérer** > **Compte**, puis sélectionnez **Ressources de compte > Organisations Cloud Foundry**.
{:shortdesc}

## Concepts liés aux organisations Cloud Foundry
{: #cf-org-concepts}

Vous pouvez utiliser des organisations afin de permettre la collaboration entre les utilisateurs et de faciliter le regroupement logique des ressources de projet comme suit :

   * Vous pouvez regrouper un ensemble d'espaces, d'applications, de services, de domaines, de routes et d'utilisateurs dans des organisations.
   * Vous pouvez gérer les accès utilisateur aux organisations et aux espaces de manière individuelle.

Les organisations peuvent couvrir plusieurs régions et elles sont définies par les éléments suivants :

<dl>
<dt>Espaces</dt>
<dd>Sous-groupe au sein d'une organisation qui vous permet d'organiser des applications, des services et des utilisateurs. Les espaces sont liés à une région spécifique dans {{site.data.keyword.Bluemix_notm}}. </dd>
<dt>Utilisateurs</dt>
<dd>Rôle disposant du droit d'accès de base dans les organisations et les espaces. Vous devez être affecté à une organisation pour pouvoir obtenir d'autres droits d'accès aux espaces de l'organisation. Pour plus d'informations, voir [Accès Cloud Foundry](/docs/iam?topic=iam-cfaccess).</dd>
<dt>Domaines</dt>
<dd>Indiquez la route Internet allouée à l'organisation. Une route comporte un sous-domaine et un domaine. En général, le sous-domaine est le nom de l'application. Un domaine peut être un domaine de système ou un domaine personnalisé que vous avez enregistré pour votre application.<br/>
<p>Si vous ajoutez un domaine personnalisé, vous devez configurer votre serveur DNS pour qu'il résolve votre domaine personnalisé, de telle sorte qu'il désigne le domaine de système {{site.data.keyword.Bluemix_notm}}. Ainsi, lorsqu'{{site.data.keyword.Bluemix_notm}} reçoit une demande pour votre domaine personnalisé, il peut l'acheminer correctement vers votre application.</p></dd>
<dt>Quota</dt>
<dd>Représente les ressources disponibles pour une organisation, notamment le nombre de services et la quantité de mémoire pouvant être alloués à l'organisation. Des quotas sont affectés lors de la création des organisations. Toute application ou tout service dans un espace d'une organisation contribue à l'utilisation du quota. Avec les comptes de type Paiement à la carte ou Abonnement, vous pouvez ajuster votre quota pour les applications et les conteneurs Cloud Foundry à mesure que les besoins de votre organisation changent.</dd>
</dl>

Dans un compte d'abonnement, le quota est une limite définie par l'utilisateur qui déclenche l'envoi de notifications concernant les dépenses.
{: tip}

## Ajout d'organisations
{: #createorg}

Si vous avez un compte facturable, vous pouvez ajouter autant d'organisations que nécessaire. Les comptes Lite ne peuvent avoir qu'une seule organisation, déjà créée dans votre compte.

1. Accédez à **Gérer** > **Compte**, puis sélectionnez **Ressources de compte > Organisations Cloud Foundry**. Cliquez sur **Créer**.
2. Entrez un nom d'organisation. Ce nom doit être unique dans {{site.data.keyword.Bluemix_notm}}.

   Si le nom d'organisation est déjà utilisé par un autre utilisateur d'environnement {{site.data.keyword.Bluemix_notm}} public, dédié ou local, vous devez spécifier un autre nom.
3. Cliquez sur **Ajouter**.

Une fois que vous avez ajouté l'organisation, le droit Responsable de l'organisation vous est automatiquement affecté. Il vous permet d'éditer le nom d'organisation, d'ajouter des utilisateurs et de créer et de supprimer des espaces dans l'organisation.

Vous pouvez affecter les [rôles Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles) suivants aux utilisateurs d'une organisation. Le rôle d'auditeur est affecté par défaut à tous les utilisateurs invités dans le compte.

   * Responsable de l'organisation
   * Responsable de la facturation de l'organisation
   * Auditeur de l'organisation

## Ajout d'espaces
{: #spaceinfo}

Dans une organisation, vous pouvez utiliser des espaces pour regrouper un ensemble d'applications, de services et d'utilisateurs. Les espaces sont définis au sein d'une seule région {{site.data.keyword.Bluemix_notm}}. Vous pouvez créer des espaces dans une organisation en fonction du cycle de vie de distribution. Par exemple, vous pouvez créer un espace `dev` en tant qu'environnement de développement, un espace `test` en tant qu'environnement de test et un espace `production` en tant qu'environnement de production. Ensuite, vous pouvez associer vos applications à des espaces.

Pour ajouter un espace à une organisation, procédez comme suit : 

1. Sur la page Organisations Cloud Foundry, cliquez sur le nom de l'organisation à laquelle vous voulez ajouter un espace.
2. Cliquez sur **Ajouter un espace**.
3. Sélectionnez une région et entrez un nom.
4. Cliquez sur **Sauvegarder**.

Une fois que vous avez ajouté des utilisateurs à une organisation, vous pouvez leur affecter des droits d'accès pour les espaces. A l'instar des organisations, les espaces possèdent également un ensemble de [rôles Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles) associés à des droits d'accès spécifiques pouvant être affectés aux membres d'équipe :

  * Responsable de l'espace
  * Développeur de l'espace
  * Auditeur de l'espace

Un utilisateur doit disposer d'au moins l'un des droits dans l'espace.
{: tip}
