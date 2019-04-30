---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: account owner, user roles, manage account, orgs, spaces

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# Mise à jour d'organisations et d'espaces
{: #orgupdates}

En tant que propriétaire de compte {{site.data.keyword.Bluemix}} ou responsable de l'organisation, vous pouvez effectuer des tâches de gestion au niveau de l'organisation et au niveau de l'espace. Ces tâches incluent notamment le changement de nom d'une organisation ou d'un espace, l'affectation ou la mise à jour des rôles des utilisateurs Cloud Foundry, la gestion de domaines et l'affichage des détails de quota d'organisation.
{:shortdesc}

Accédez à **Gérer > Compte** puis sélectionnez **Organisations Cloud Foundry**.

Vous ne pouvez afficher les ressources que d'une seule organisation à la fois. Si vous êtes membre de plusieurs organisations, vous pouvez passer d'une organisation à une autre depuis le lien des préférences du compte utilisateur dans la barre de menus de la console.
{: tip}

  * Pour renommer une organisation, cliquez sur l'icône Actions ![Icône Action](../icons/action-menu-icon.svg) pour l'organisation à renommer puis sélectionnez **Renommer**.
    {: #orgrename}

    Toutes les modifications effectuées s'appliquent à tous les utilisateurs de l'organisation.

  * Pour supprimer une organisation, prenez contact avec le [support](/docs/get-support?topic=get-support-getting-customer-support).
    {: #deleteorgs}

    Lorsqu'une organisation est supprimée, tous les espaces et toutes les ressources qu'elle comporte sont également supprimés. Cette action ne peut pas être annulée.

  * Pour supprimer un espace, sélectionnez l'organisation dans laquelle l'espace est affecté. Cliquez ensuite sur l'icône Actions ![Icône Action](../icons/action-menu-icon.svg) et sélectionnez **Supprimer**.

    Lorsque vous supprimez un espace, toutes les ressources et tous les utilisateurs qu'il comporte sont également supprimés.

  * Pour éditer des rôles utilisateur au niveau de l'organisation, cliquez sur l'icône Actions ![Icône Action](../icons/action-menu-icon.svg) et sélectionnez **Utilisateurs**.
    {: #listmembers}

    Selon la manière dont vous souhaitez modifier les droits d'accès des utilisateurs, sélectionnez ou désélectionnez la case à cocher correspondant à un rôle spécifique. Les rôles que vous pouvez affecter au niveau de l'organisation sont les suivants : Responsable, Responsable de la facturation et Auditeur. Pour plus d'informations, voir [Rôles Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles).

  * Pour éditer des rôles utilisateur pour un espace spécifique, cliquez sur l'organisation dans laquelle l'espace est affecté. Cliquez ensuite sur le nom de l'espace.

    Selon la manière dont vous souhaitez modifier les droits d'accès des utilisateurs, sélectionnez ou désélectionnez la case à cocher correspondant à un rôle spécifique. Les rôles que vous pouvez affecter au niveau de l'espace sont les suivants : Responsable, Développeur et Auditeur. Pour plus d'informations, voir [Rôles Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles).

  * Pour gérer vos domaines, cliquez sur l'icône Actions ![Icône Action](../icons/action-menu-icon.svg) pour l'organisation concernée puis sélectionnez **Domaines**.
    {: #managedomains}

    En tant que propriétaire de compte ou responsable de l'organisation, vous pouvez afficher le domaine de système et ajouter des données personnalisés pour les applications construites dans une organisation et ses espaces. Si vous êtes responsable de l'espace, cette page affiche une liste en lecture seule des domaines affectés à l'espace.

    Si vous ajoutez un domaine personnalisé, vous devez configurer votre serveur DNS pour qu'il résolve votre domaine personnalisé, de telle sorte qu'il désigne le domaine de système {{site.data.keyword.Bluemix_notm}}. Ainsi, lorsque {{site.data.keyword.Bluemix_notm}} reçoit une demande pour votre domaine personnalisé, celle-ci est correctement acheminée vers votre application. Le domaine de système est toujours disponible dans un espace, et des domaines personnalisés peuvent également être alloués à un espace. Les applications créées dans un espace peuvent utiliser tout domaine répertorié pour cet espace. Pour plus d'informations sur la création et l'utilisation de domaines personnalisés, voir [Gestion de vos domaines](/docs/apps?topic=creating-apps-update-domain#update-domain).

  * Pour gérer le quota alloué pour une organisation, cliquez sur l'icône Actions ![Icône Action](../icons/action-menu-icon.svg) pour l'organisation concernée puis sélectionnez **Quotas**.
    {: #managequota}

    Vous alors pouvez afficher les détails de quota pour le nombre d'applications, la quantité de mémoire, le nombre de services et les détails de plan. Le quota représente les limites de ressources pour l'organisation et est affecté lors de la création de l'organisation. Les ressources disponibles pour une organisation varient selon que vous disposez d'un compte gratuit ou facturable. Toute application ou tout service dans un espace de l'organisation contribue à l'utilisation du quota attribué.

    Pour changer le quota alloué à une organisation, vous devez créer un cas de support. Pour plus d'informations, voir [Utilisation de cas de support](/docs/get-support?topic=get-support-open-case).

    Pour afficher les détails de quota au niveau des espaces pour chaque emplacement, cliquez sur l'icône Actions ![Icône Action](../icons/action-menu-icon.svg) pour l'organisation concernée puis sélectionnez **Quotas**. Développez ensuite chaque ligne en fonction de vos besoins.
