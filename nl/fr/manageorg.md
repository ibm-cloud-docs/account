---

copyright:

  years: 2015, 2018
lastupdated: "2018-03-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Mise à jour d'organisations et d'espaces
{: #orgupdates}

En tant que propriétaire de compte ou responsable de l'organisation, vous pouvez effectuer des tâches de gestion au niveau de l'organisation et au niveau de l'espace.
Ces tâches incluent notamment le changement de nom d'une organisation ou d'un espace, l'affectation ou la mise à jour des rôles des utilisateurs Cloud Foundry, la gestion de domaines et l'affichage des détails de quota d'organisation. {:shortdesc}

Pour gérer vos organisations depuis la console {{site.data.keyword.Bluemix}}, cliquez sur **Gérer > Compte > Organisations Cloud Foundry**. Vous ne pouvez afficher les ressources que d'une seule organisation à la fois. Si vous êtes membre de plusieurs organisations, vous pouvez passer d'une organisation à une autre depuis le lien des préférences du compte utilisateur dans la barre de menus de la console.

## Modification du nom d'une organisation
{: #orgrename}

Procédez comme indiqué ci-après pour renommer votre organisation. Attention, les modifications que vous effectuez s'appliquent à tous les utilisateurs de l'organisation. 

1. Cliquez sur **Gérer** > **Compte** > **Organisations Cloud Foundry**.
2. Cliquez sur l'icône Actions pour l'organisation que vous souhaitez renommer et sélectionnez **Renommer**.  
3. Entrez le nouveau nom et cliquez sur **Sauvegarder**.

## Suppression d'organisations et d'espaces
{: #deleteorgs}

### Suppression d'une organisation

Pour supprimer une organisation, prenez contact avec le [support](/docs/get-support/howtogetsupport.html). Lorsqu'une organisation est supprimée, tous les espaces et toutes les ressources qu'elle comporte sont également supprimés. N'oubliez pas qu'une opération de suppression est irréversible.  

### Suppression d'un espace

Lorsque vous supprimez un espace, toutes les ressources et tous les utilisateurs qu'il comporte sont également supprimés. Pour supprimer un espace, procédez comme suit :

1. Cliquez sur **Gérer** > **Compte** > **Organisations Cloud Foundry**.
2. Cliquez sur l'organisation dans laquelle l'espace est affecté. 
3. Cliquez sur l'icône Actions, puis sélectionnez **Supprimer**.
4. Confirmez que vous voulez supprimer l'espace en entrant son nom dans la zone, puis cliquez sur **Supprimer**.

## Edition des rôles utilisateur
{: #listmembers}

Les rôles que vous pouvez affecter au niveau de l'organisation sont les suivants : Responsable, Responsable de la facturation et Auditeur.
Les rôles que vous pouvez affecter au niveau de l'espace sont les suivants : Responsable, Développeur et Auditeur.
Pour obtenir des descriptions de rôle détaillés, voir [Rôles Cloud Foundry](/docs/iam/cfaccess.html#cfroles).

### Edition des rôles utilisateur au niveau de l'organisation

Procédez comme suit afin d'éditer les rôles utilisateur pour une organisation spécifique :

1. Cliquez sur **Gérer** > **Compte** > **Organisations Cloud Foundry**.
2. Cliquez sur l'icône Actions, puis sélectionnez **Utilisateurs**.
3. Selon la manière dont vous souhaitez modifier les droits d'accès des utilisateurs, sélectionnez ou désélectionnez la case à cocher correspondant à un rôle spécifique.
4. Confirmez vos modifications en cliquant sur **Sauvegarder**. 

### Edition des rôles utilisateur au niveau de l'espace

Procédez comme suit afin d'éditer les rôles utilisateur pour un espace spécifique :

1. Cliquez sur **Gérer** > **Compte** > **Organisations Cloud Foundry**.
2. Cliquez sur l'organisation dans laquelle l'espace est affecté. 
3. Cliquez sur le nom de l'espace.
4. Selon la manière dont vous souhaitez modifier les droits d'accès des utilisateurs, sélectionnez ou désélectionnez la case à cocher correspondant à un rôle spécifique.
5. Confirmez vos modifications en cliquant sur **Sauvegarder**.

## Gestion des domaines
{: #managedomains}

En tant que propriétaire de compte ou responsable de l'organisation, vous pouvez afficher le domaine de système et ajouter des
données personnalisés pour les applications construites dans une organisation et ses espaces. Si vous êtes responsable de l'espace, l'onglet **Domaines** est une liste en lecture seule des domaines affectés à l'espace.

1. Cliquez sur **Gérer** &gt; **Compte** &gt; **Organisations Cloud Foundry**.
2. Cliquez sur l'icône Actions pour l'organisation, puis sélectionnez **Domaines**.

Si vous ajoutez un domaine personnalisé, vous devez configurer votre serveur DNS pour qu'il résolve votre domaine personnalisé, de telle sorte qu'il désigne le domaine de système {{site.data.keyword.Bluemix_notm}}. Ainsi, lorsque {{site.data.keyword.Bluemix_notm}} reçoit une demande pour votre domaine personnalisé, celle-ci est correctement acheminée vers votre application. Le domaine de système est toujours disponible dans un espace, et des domaines personnalisés peuvent également être alloués à un espace. Les applications créées dans un espace peuvent utiliser tout domaine répertorié pour cet espace. Pour plus d'informations sur la création et l'utilisation de domaines personnalisés, voir [Création et utilisation d'un domaine personnalisé](/docs/apps/updapps.html#domain).

## Gestion du quota
{: #managequota}

Vous pouvez afficher le quota utilisé et le quota attribué pour une organisation. Le quota représente les limites de ressources pour l'organisation et est affecté lors de la création de l'organisation. Les ressources disponibles pour une organisation varient selon que vous disposez d'un compte gratuit ou facturable. Toute application ou tout service dans un espace de l'organisation contribue à l'utilisation du quota attribué. 

Procédez comme suit afin d'afficher le quota utilisé et le quota alloué pour une organisation :

1. Cliquez sur **Gérer** &gt; **Compte** &gt; **Organisations Cloud Foundry**.
2. Cliquez sur l'icône Actions pour l'organisation spécifique, puis sélectionnez **Quotas**.

   Par défaut, la page de quota **Cloud Foundry** s'ouvre. A partir de là, vous pouvez afficher les détails de quota des ressources suivantes :
 
   * Le nombre d'applications
   * La quantité de mémoire 
   * Le nombre de services 
   * Les détails du plan 

3. Développez la région des détails pour consulter les quotas au niveau de l'espace. 

Pour modifier le quota alloué à une organisation, vous devez ouvrir un ticket de demande de service. Pour plus d'informations, voir [Support client](/docs/get-support/howtogetsupport.html#getting-customer-support). 

