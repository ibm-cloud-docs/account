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


# {{site.data.keyword.cloudaccesstrailshort}}eventi  
{: #at_events}

In qualità di responsabile della sicurezza, revisore o gestore, puoi utilizzare il servizio {{site.data.keyword.cloudaccesstrailfull}} per tracciare come gli utenti e le applicazioni interagiscono con l'account {{site.data.keyword.Bluemix}}.
{:shortdesc}

Ad esempio, quando un utente o un'applicazione eseguono l'accesso a {{site.data.keyword.Bluemix_notm}} utilizzando una password, una chiave API e un codice di autenticazione o un passcode, viene generato un evento {{site.data.keyword.cloudaccesstrailshort}} per ciascun tentativo. 

Il servizio {{site.data.keyword.cloudaccesstrailfull_notm}} registra le attività avviate dall'utente che modificano lo stato di un servizio in {{site.data.keyword.Bluemix_notm}}. Per ulteriori informazioni, vedi [Informazioni su {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov ).

Per iniziare a monitorare le azioni del tuo utente, vedi [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla). 

## Eventi per la gestione degli account
{: #account}

La seguente tabella elenca il metodo API che genera un evento quando ne viene eseguito il richiamo:

<table>
  <caption>Azioni che generano eventi</caption>
  <tr>
    <th>Azione</th>
	  <th>Descrizione</th>
  </tr>
  <tr>
    <td>billing.account.create</td>
	  <td>Un evento viene generato quando esegui il provisioning di un account e dopo che l'ID account è stato assegnato all'account.</td>
  </tr>
  <tr>
    <td>billing.account.update</td>
	  <td>Un evento viene generato quando aggiorni le informazioni sull'account.</td>
  </tr>
  <tr>
    <td>billing.account.active</td>
	  <td>Un evento viene generato quando verifichi l'account o un evento viene generato quando l'account passa allo stato attivo.</td>
  </tr>
  <tr>
    <td>billing.account.subscription.create</td>
	  <td>Un evento viene generato quando crei un <a href="/docs/account/index.html#subscription-account">account sottoscrizione</a>.</td>
  </tr>
</table>



## Eventi per la gestione degli utenti
{: #users}

La seguente tabella elenca il metodo API che genera un evento quando ne viene eseguito il richiamo:

<table>
  <caption>Azioni che generano eventi</caption>
  <tr>
    <th>Azione</th>
	  <th>Descrizione</th>
  </tr>
  <tr>
    <td>billing.account.user.create</td>
	  <td>Un evento viene generato quando invii a un utente un invito a unirsi a un account. </br>Il proprietario dell'account è il solo utente nell'account che può eseguire questa azione.</td>
  </tr>
  <tr>
    <td>billing.user.active</td>
	  <td>Un evento viene generato quando attivi l'utente nell'account. </br>Quando l'utente verifica il suo indirizzo email, l'evento viene generato.</td>
  </tr>
  <tr>
    <td>billing.account.user.delete</td>
	  <td>Un evento viene generato quando rimuovi un utente dall'account. </br>Il proprietario dell'account è il solo utente nell'account che può eseguire questa azione.</td>
  </tr>
</table>

## Eventi per la gestione delle organizzazioni
{: #org}

La seguente tabella elenca il metodo API che genera un evento quando ne viene eseguito il richiamo:

<table>
  <caption>Azione che genera gli eventi</caption>
  <tr>
    <th>Azione</th>
	  <th>Descrizione</th>
  </tr>
  <tr>
    <td>billing.account.org.create</td>
	  <td>Un evento viene generato quando aggiungi un'organizzazione all'account.</td>
  </tr>
</table>

## Dove cercare gli eventi
{: #ui}

Gli eventi {{site.data.keyword.cloudaccesstrailshort}} sono disponibili nel {{site.data.keyword.cloudaccesstrailshort}} **dominio dell'account Dallas** che è disponibile in {{site.data.keyword.Bluemix_notm}}. Per ulteriori informazioni, vedi [Visualizzazione degli eventi dell'account](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events).

Gli eventi {{site.data.keyword.cloudaccesstrailshort}} vengono automaticamente inoltrati al servizio {{site.data.keyword.cloudaccesstrailshort}} nella stessa regione dove si verifica l'azione.
