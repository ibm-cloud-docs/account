---

copyright:

  years: 2015, 2018
lastupdated: "2018-01-23"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Utilisation des organisations
En tant que propriétaire de compte ou responsable de l'organisation, vous pouvez effectuer des tâches de gestion de l'organisation, notamment renommer votre organisation, supprimer une organisation ou un espace, mettre à jour les rôles d'organisation ou d'espace et gérer le quota et les domaines.
{:shortdesc}

Pour gérer vos organisations depuis la console {{site.data.keyword.Bluemix}}, cliquez sur **Gérer > Compte > Organisations Cloud Foundry**. Vous ne pouvez afficher les ressources que d'une seule organisation à la fois. Si vous êtes membre de plusieurs organisations, vous pouvez passer d'une organisation à l'autre depuis le lien des préférences du compte utilisateur dans la barre de menus de la console.

## Modification du nom d'une organisation
{: #orgrename}

Procédez comme suit pour renommer votre organisation :
1. Cliquez sur **Gérer** > **Compte** > **Organisations Cloud Foundry**.
2. Déterminez quelle organisation vous voulez renommer, puis cliquez sur **Afficher les détails**.
3. Cliquez sur **Editer une organisation Cloud Foundry**.
4. Cliquez sur **Editer** à côté du nom de l'organisation.
5. Entrez le nouveau nom d'organisation et cliquez sur **Sauvegarder**.

## Suppression d'organisations et d'espaces
{: #deleteorgs}

### Suppression d'une organisation

Lorsque vous supprimez une organisation, tous les espaces, toutes les applications et tous les services au sein de l'organisation sont supprimés. N'oubliez pas qu'une opération de suppression est irréversible. 

### Suppression d'un espace

Pour supprimer un espace, procédez comme suit :

1. Cliquez sur **Gérer** > **Compte** > **Organisations Cloud Foundry**.
2. Sélectionnez l'organisation à éditer, puis cliquez sur **Afficher les détails**.
3. Déterminez l'espace à supprimer, puis cliquez sur **Editer l'espace**.
4. Cliquez sur **Supprimer un espace Cloud Foundry**.

## Edition des rôles utilisateur
{: #listmembers}

### Edition des rôles utilisateur d'une organisation spécifique 

Procédez comme suit afin d'éditer les rôles utilisateur pour une organisation spécifique :

1. Cliquez sur **Gérer** > **Compte** > **Organisations Cloud Foundry**.
2. Déterminez quelle organisation vous voulez éditer et cliquez sur **Afficher les détails**, puis sur **Editer l'organisation**.
4. Les membres de votre organisation et leurs rôles s'affichent dans l'onglet **UTILISATEURS**.

### Edition des rôles utilisateur d'un espace spécifique

Procédez comme suit afin d'éditer les rôles utilisateur pour un espace spécifique :

1. Cliquez sur **Gérer** > **Compte** > **Organisations Cloud Foundry**.
2. Sélectionnez l'organisation dont vous voulez afficher les membres, puis cliquez sur **Afficher les détails**.
3. Déterminez l'espace à éditer, puis cliquez sur **Editer l'espace**.
4. Les membres de votre espace et leurs rôles s'affichent dans l'onglet **UTILISATEURS**.

## Gestion du quota
{: #managequota}

En tant que propriétaire de compte {{site.data.keyword.Bluemix_notm}} ou responsable de l'organisation, vous pouvez afficher le quota alloué et le quota utilisé pour une organisation. Le quota représente les limites de ressources pour l'organisation et est affecté lorsque l'organisation est créée. Les ressources disponibles pour une organisation varient selon que vous disposez d'un compte gratuit ou facturable. Toute application ou tout service dans un espace de l'organisation contribue à l'utilisation du quota alloué.

Procédez comme suit afin d'afficher le quota utilisé et le quota alloué pour une organisation :

1. Cliquez sur **Gérer** &gt; **Compte** &gt; **Organisations Cloud Foundry**.
2. Identifiez l'organisation pour laquelle afficher le quota, puis cliquez sur **Afficher les détails**.
3. Cliquez sur **Editer l'organisation**.
4. Si des espaces sont définis dans plusieurs régions, sélectionnez la région que vous souhaitez visualiser.
5. Cliquez sur **QUOTA**. 
6. Par défaut, la page du quota **Cloud Foundry** s'ouvre. Vous pouvez afficher les détails de quota des ressources suivantes :
 * MEMOIRE
 * Services
 * PLAN
 * PRIX
7. Cliquez sur **Conteneurs** pour afficher l'allocation des quotas de conteneur utilisé et disponible. L'allocation de conteneur varie en fonction du plan de tarification. Vous pouvez afficher les détails de quota des ressources suivantes :
 * MEMOIRE
 * Adresse IP publique
 * PARTAGE DE FICHIERS
8. Cliquez sur **Serveurs virtuels** pour visualiser les machines virtuelles.

Les conteneurs ne sont pas disponibles dans la région {{site.data.keyword.Bluemix_notm}} Sydney. 
{: tip}

Pour plus d'informations sur les conteneurs, voir [Quota](/docs/containers/container_planning.html#container_planning_quota) dans la documentation sur les conteneurs.
Pour modifier le quota alloué à une organisation, vous devez ouvrir un ticket de demande de service. Pour plus d'informations sur l'ouverture d'un ticket de demande de service, voir [Support client](/docs/get-support/howtogetsupport.html#getting-customer-support). 

## Gestion des domaines
{: #managedomains}

En tant que propriétaire de compte {{site.data.keyword.Bluemix_notm}} ou responsable de l'organisation, ous pouvez afficher le domaine de système et ajouter des données personnalisés pour les applications construites dans une organisation et ses espaces. Si vous êtes responsable de l'espace, l'onglet **Domaines** d'un espace est une liste en lecture seule des domaines affectés à l'espace.

1. Cliquez sur **Gérer** &gt; **Compte** &gt; **Organisations Cloud Foundry**.
2. Identifiez l'organisation que vous désirez éditer ou éditer les domaines.
3. Sélectionnez **Afficher les détails** pour cette organisation.
4. Cliquez sur **Editer l'organisation**.
5. Cliquez sur **DOMAINES**.

Si vous ajoutez un domaine personnalisé, vous devez configurer votre serveur DNS pour qu'il résolve votre domaine personnalisé, de telle sorte qu'il désigne le domaine de système {{site.data.keyword.Bluemix_notm}}. Ainsi, lorsque {{site.data.keyword.Bluemix_notm}} reçoit une demande pour votre domaine personnalisé, il peut l'acheminer correctement vers votre appli. Le domaine de système est toujours disponible dans un espace, et des domaines personnalisés peuvent également être alloués à un espace. Les applis créées dans un espace peuvent utiliser tout domaine répertorié pour cet espace. Pour plus d'informations sur la création et l'utilisation de domaines personnalisés, voir [Création et utilisation d'un domaine personnalisé](/docs/apps/updapps.html#domain).
