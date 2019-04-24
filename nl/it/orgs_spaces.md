---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: account, add orgs, add spaces, manage users, user access

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Aggiunta di organizzazioni e spazi
{: #orgsspacesusers}

In qualità di proprietario di un account {{site.data.keyword.Bluemix}}, puoi aggiungere organizzazioni e spazi al tuo account. Se sei un gestore organizzazione, puoi gestire le organizzazioni nell'account. Vai a **Gestisci** > **Account** e seleziona **Organizzazioni Cloud Foundry**.
{:shortdesc}

Puoi utilizzare le organizzazioni per abilitare la collaborazione tra gli utenti e facilitare il raggruppamento logico delle risorse del progetto nei seguenti modi:

   * Puoi raggruppare un insieme di spazi, applicazioni, servizi, domini, rotte e utenti nelle organizzazioni.
   * Puoi gestire l'accesso utente alle organizzazioni e agli spazi su una base individuale.

## Aggiunta di organizzazioni
{: #createorg}

Le organizzazioni possono estendersi a più regioni e sono definite dai seguenti elementi:

<dl>
<dt>Utenti</dt>
<dd>Il ruolo con l'autorizzazione di base in organizzazioni e spazi. Devi essere assegnato
a un'organizzazione prima che ti possano essere concesse altre autorizzazioni agli
spazi all'interno dell'organizzazione. Per ulteriori dettagli, consulta [Utenti ruoli](/docs/iam?topic=iam-userroles).</dd>
<dt>Domini</dt>
<dd>Fornisci la rotta su internet che è assegnata all'organizzazione. Una rotta ha un dominio secondario e un dominio. Un dominio secondario è di norma il nome dell'applicazione. Un dominio può essere un dominio di sistema o un dominio personalizzato che hai registrato per la tua applicazione.<br/>
<p>Se aggiungi un dominio personalizzato, devi configurare il server DNS per far sì che il tuo dominio personalizzato punti al dominio di sistema {{site.data.keyword.Bluemix_notm}}. In questo modo, quando {{site.data.keyword.Bluemix_notm}} riceve una richiesta per il tuo dominio personalizzato, può correttamente instradarla alla tua applicazione.</p></dd>
<dt>Quota</dt>
<dd>Rappresenta le risorse disponibili per un'organizzazione, incluso il numero di servizi e la quantità di memoria che può essere assegnata per l'utilizzo da parte dell'organizzazione. Le quote sono assegnate quando vengono create le organizzazioni. Qualsiasi applicazione o servizio in uno spazio all'interno dell'organizzazione contribuisce all'utilizzo della quota. Con gli account Pagamento a consumo o Sottoscrizione, puoi modificare la tua quota per le applicazioni e i contenitori Cloud Foundry man mano che cambiano le esigenze della tua organizzazione.</dd>
</dl>

In un account Sottoscrizione, la quota è un limite definito dall'utente che avvia le notifiche di spesa.
{: tip}

Quando aggiungi un'organizzazione, il nome deve essere univoco in {{site.data.keyword.Bluemix_notm}}. Se il nome dell'organizzazione è già utilizzato da un altro utente di {{site.data.keyword.Bluemix_notm}} pubblico, dedicato o locale, devi specificare un nuovo nome. Dopo aver aggiunto l'organizzazione, ti viene assegnata automaticamente l'autorizzazione di Gestore organizzazione, in modo che tu possa modificare il nome dell'organizzazione, aggiungere utenti e creare o eliminare spazi nell'organizzazione. Se hai un account fatturabile, puoi aggiungere tutte le organizzazioni di cui hai bisogno. Tuttavia, in un account Lite, puoi avere una sola organizzazione.

In un'organizzazione, è possibile assegnare i seguenti [ruoli utente](/docs/iam?topic=iam-userroles). A tutti gli utenti invitati all'account viene assegnato il ruolo di revisore per impostazione predefinita.

   * Gestore organizzazione
   * Gestore fatturazione dell'organizzazione
   * Revisore organizzazione

Completa la seguente procedura per aggiungere un'organizzazione:

  1. Fai clic su **Aggiungi un'organizzazione**.
  2. Immetti il nome dell'organizzazione.  
  3. Fai clic su **Aggiungi**.

<!-- Add info on Manage infrastructure option under a space -->

## Aggiunta di spazi
{: #spaceinfo}

All'interno di un'organizzazione, puoi utilizzare gli spazi per raggruppare un insieme di applicazioni, servizi e utenti. Gli spazi sono collegati a una specifica
regione in {{site.data.keyword.Bluemix_notm}}. Puoi creare gli spazi in un'organizzazione in base al ciclo di vita della distribuzione. Ad esempio, puoi creare uno spazio `dev` come un ambiente di sviluppo,
uno spazio `test` come un ambiente di test e uno
spazio `production` come un ambiente di produzione. Puoi quindi associare
le tue applicazioni agli spazi.

Dopo aver aggiunto gli utenti a un'organizzazione, puoi concedere loro le autorizzazioni per gli spazi. Analogamente alle organizzazioni, anche gli spazi hanno una serie di [ruoli Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles) con specifiche autorizzazioni che vengono assegnati ai membri del team:

  * Gestore spazio
  * Sviluppatore spazio
  * Revisore spazio

Ad un utente deve essere assegnata almeno una delle autorizzazioni nello spazio.
{: tip}

Per aggiungere uno spazio, completa la seguente procedura:

  1. Fai clic sul nome dell'organizzazione a cui vuoi aggiungere uno spazio.
  2. Fai clic su **Aggiungi uno spazio**.
  3. Seleziona una regione e immetti un nome.
  4. Fai clic su **Salva**.
