---

copyright:
  years: 2016, 2018

lastupdated: "2018-10-31"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Evénements {{site.data.keyword.cloudaccesstrailshort}}  
{: #at_events}

En tant que responsable de la sécurité, auditeur ou responsable, vous pouvez utiliser le service {{site.data.keyword.cloudaccesstrailfull}} pour suivre comment les utilisateurs et les applications interagissent avec le compte {{site.data.keyword.Bluemix}}.
{:shortdesc}

Par exemple, lorsqu'un utilisateur ou une application se connecte à {{site.data.keyword.Bluemix_notm}}, en utilisant un mot de passe, une clé d'API et un code d'authentification ou un code d'accès, un événement {{site.data.keyword.cloudaccesstrailshort}} est généré pour chaque tentative.  

Le service {{site.data.keyword.cloudaccesstrailfull_notm}} enregistre les activités initiées par l'utilisateur qui changent l'état d'un service dans {{site.data.keyword.Bluemix_notm}}. Pour plus d'informations, voir [About {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov ).

Pour commencer à surveiller les actions utilisateur, voir [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla). 

## Evénements pour la gestion des comptes
{: #account}

Le tableau suivant répertorie les méthodes d'API générant un événement lorsqu'elles sont appelées :

<table>
  <caption>Actions générant des événements</caption>
  <tr>
    <th>Action</th>
	  <th>Description</th>
  </tr>
  <tr>
    <td>billing.account.create</td>
	  <td>Un événement est généré lorsque vous mettez à disposition un compte et qu'un ID lui est affecté.</td>
  </tr>
  <tr>
    <td>billing.account.update</td>
	  <td>Un événement est généré lorsque vous mettez à jour les informations sur le compte.</td>
  </tr>
  <tr>
    <td>billing.account.active</td>
	  <td>Un événement est généré lorsque vous vérifiez le compte ou lorsque le compte passe à l'état actif.</td>
  </tr>
  <tr>
    <td>billing.account.subscription.create</td>
	  <td>Un événement est généré lorsque vous créez un <a href="/docs/account/index.html#subscription-account">compte d'abonnement</a>.</td>
  </tr>
</table>



## Evénements liés à la gestion des utilisateurs
{: #users}

Le tableau suivant présente les méthodes d'API générant un événement lors de leur appel :

<table>
  <caption>Actions qui génèrent des événements</caption>
  <tr>
    <th>Action</th>
	  <th>Description</th>
  </tr>
  <tr>
    <td>billing.account.user.create</td>
	  <td>Un événement est généré lorsque vous envoyez une invitation à un utilisateur pour qu'il rejoigne un compte. </br>Le propriétaire du compte est le seul utilisateur pouvant effectuer cette action.</td>
  </tr>
  <tr>
    <td>billing.user.active</td>
	  <td>Un événement est généré lorsque vous activez l'utilisateur dans le compte. </br>L'événement est généré lorsque l'utilisateur confirme son adresse électronique.</td>
  </tr>
  <tr>
    <td>billing.account.user.delete</td>
	  <td>Un événement est généré lorsque vous supprimez un utilisateur du compte. </br>Le propriétaire du compte est le seul utilisateur pouvant effectuer cette action.</td>
  </tr>
</table>

## Evénements liés à la gestion des organisations
{: #org}

Le tableau suivant présente la méthode d'API générant un événement lors de son appel :

<table>
  <caption>Action générant des événements</caption>
  <tr>
    <th>Action</th>
	  <th>Description</th>
  </tr>
  <tr>
    <td>billing.account.org.create</td>
	  <td>Un événement est généré lorsque vous ajoutez une organisation au compte.</td>
  </tr>
</table>

## Où rechercher les événements ?
{: #ui}

Les événements {{site.data.keyword.cloudaccesstrailshort}} sont disponibles dans le **domaine de compte Dallas** {{site.data.keyword.cloudaccesstrailshort}}, lui même disponible dans {{site.data.keyword.Bluemix_notm}}. Pour plus d'informations, voir [Affichage des événements de compte](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events).

Les événements {{site.data.keyword.cloudaccesstrailshort}} sont automatiquement transmis au service {{site.data.keyword.cloudaccesstrailshort}} dans la région où l'action se produit.
