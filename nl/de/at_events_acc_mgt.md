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


# {{site.data.keyword.cloudaccesstrailshort}}-Ereignisse  
{: #at_events}

Als Sicherheitsbeauftragter, Prüfer oder Manager können Sie den {{site.data.keyword.cloudaccesstrailfull}}-Service verwenden, um die Interaktion von Benutzern und Anwendungen mit dem {{site.data.keyword.Bluemix}}-Konto zu verfolgen.
{:shortdesc}

Wenn sich ein Benutzer oder eine Anwendung beispielsweise bei {{site.data.keyword.Bluemix_notm}} mit einem Kennwort, einem API-Schlüssel und einem Authentifizierungscode oder einem Kenncode anmeldet, wird für jeden Anmeldeversuch ein {{site.data.keyword.cloudaccesstrailshort}}-Ereignis generiert.  

Der Service {{site.data.keyword.cloudaccesstrailfull_notm}} zeichnet die von Benutzern eingeleiteten Aktivitäten auf, durch die sich der Status eines Service in {{site.data.keyword.Bluemix_notm}} ändert. Weitere Informationen hierzu finden Sie im Abschnitt mit [Informationen zu {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov ).

Weitere Informationen zum Einstieg in die Überwachung von Benutzeraktionen finden Sie in [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla). 

## Ereignisse bei der Verwaltung von Konten
{: #account}

In der folgenden Tabelle sind die API-Methoden aufgelistet, bei deren Aufruf ein Ereignis generiert wird.

<table>
  <caption>Aktionen, die Ereignisse generieren</caption>
  <tr>
    <th>Aktion</th>
	  <th>Beschreibung</th>
  </tr>
  <tr>
    <td>billing.account.create</td>
	  <td>Ein Ereignis wird generiert, wenn Sie ein Konto bereitstellen, und nach dem Zuordnen der Konto-ID für das Konto.</td>
  </tr>
  <tr>
    <td>billing.account.update</td>
	  <td>Ein Ereignis wird generiert, wenn Sie Informationen zu dem Konto aktualisieren.</td>
  </tr>
  <tr>
    <td>billing.account.active</td>
	  <td>Ein Ereignis wird generiert, wenn Sie das Konto prüfen oder wenn das Konto in den aktiven Status versetzt wird.</td>
  </tr>
  <tr>
    <td>billing.account.subscription.create</td>
	  <td>Ein Ereignis wird generiert, wenn Sie ein <a href="/docs/account/index.html#subscription-account">Abonnementkonto</a> erstellen.</td>
  </tr>
</table>



## Ereignisse bei der Verwaltung von Benutzern
{: #users}

In der folgenden Tabelle sind die API-Methoden aufgelistet, bei deren Aufruf ein Ereignis generiert wird.

<table>
  <caption>Aktionen, die Ereignisse generieren</caption>
  <tr>
    <th>Aktion</th>
	  <th>Beschreibung</th>
  </tr>
  <tr>
    <td>billing.account.user.create</td>
	  <td>Ein Ereignis wird generiert, wenn Sie einem Benutzer eine Einladung senden, an einem Konto teilzunehmen. </br>Der Kontoeigner ist der einzige Benutzer des Kontos, der diese Aktion ausführen kann. </td>
  </tr>
  <tr>
    <td>billing.user.active</td>
	  <td>Ein Ereignis wird generiert, wenn Sie den Benutzer in dem Konto aktivieren. </br>Das Ereignis wird generiert, wenn der Benutzer seine E-Mail-Adresse bestätigt. </td>
  </tr>
  <tr>
    <td>billing.account.user.delete</td>
	  <td>Ein Ereignis wird generiert, wenn Sie einen Benutzer aus dem Konto entfernen. </br>Der Kontoeigner ist der einzige Benutzer des Kontos, der diese Aktion ausführen kann. </td>
  </tr>
</table>

## Ereignisse bei der Verwaltung von Organisationen
{: #org}

In der folgenden Tabelle sind die API-Methoden aufgelistet, bei deren Aufruf ein Ereignis generiert wird.

<table>
  <caption>Aktion, die Ereignisse generiert</caption>
  <tr>
    <th>Aktion</th>
	  <th>Beschreibung</th>
  </tr>
  <tr>
    <td>billing.account.org.create</td>
	  <td>Ein Ereignis wird generiert, wenn Sie eine Organisation zu dem Konto hinzufügen. </td>
  </tr>
</table>

## Wo werden Ereignisse angezeigt?
{: #ui}

{{site.data.keyword.cloudaccesstrailshort}}-Ereignisse sind in der {{site.data.keyword.cloudaccesstrailshort}}-**Kontodomäne 'Dallas'** verfügbar, die in {{site.data.keyword.Bluemix_notm}} zur Verfügung steht. Weitere Informationen finden Sie in [Kontoereignisse anzeigen](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events).

{{site.data.keyword.cloudaccesstrailshort}}-Ereignisse werden automatisch an den {{site.data.keyword.cloudaccesstrailshort}}-Service in derselben Region weitergeleitet, in der die Aktion ausgeführt wird. 
