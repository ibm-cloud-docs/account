---

copyright:

  years: 2015, 2018
lastupdated: "2018-03-08"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Creazione di organizzazioni e spazi
{: #orgsspacesusers}

In qualità di proprietario dell'account, puoi gestire le tue organizzazioni e i tuoi spazi dalla pagina Gestisci organizzazioni nella console {{site.data.keyword.Bluemix}}. I gestori dell'organizzazione possono anche utilizzare la pagina Gestisci organizzazioni per gestire le organizzazioni dove sono impostati come gestore.
{:shortdesc}

Per gestire le organizzazioni e gli spazi, fai clic su **Gestisci** &gt; **Account** &gt; **Organizzazioni Cloud Foundry**. 


## Creazione di organizzazioni
{: #createorg}

Le organizzazioni possono estendersi a più regioni e sono definite dai seguenti elementi:

<dl>
<dt>Utenti</dt>
<dd>Il ruolo con l'autorizzazione di base in organizzazioni e spazi. Devi essere assegnato
a un'organizzazione prima che ti possano essere concesse altre autorizzazioni agli
spazi all'interno dell'organizzazione. Per informazioni dettagliate, vedi [Utenti e ruoli](/docs/iam/users_roles.html#userrolesinfo).</dd>
<dt>Domini</dt>
<dd>Fornisci la rotta su internet che è assegnata all'organizzazione. Una rotta ha un dominio secondario e un dominio. Un dominio secondario è di norma il
nome dell'applicazione. Un dominio può essere un dominio di sistema o un dominio personalizzato che hai registrato per la tua applicazione. Vedi [Gestione dei domini personalizzati](/docs/account/manageorg.html#managedomains).<br/>
<p>**Nota:** se aggiungi un dominio personalizzato, devi configurare il server DNS per far sì che il tuo dominio personalizzato punti al dominio di sistema {{site.data.keyword.Bluemix_notm}}. In questo modo, quando {{site.data.keyword.Bluemix_notm}} riceve una richiesta per il tuo dominio personalizzato, può correttamente instradarla alla tua applicazione.</p></dd>
<dt>Quota</dt>
<dd>Rappresenta le risorse disponibili per un'organizzazione, incluso il numero di servizi e la quantità di memoria che può essere assegnata per l'utilizzo da parte dell'organizzazione. Le quote vengono assegnate quando
vengono create le organizzazioni. Qualsiasi applicazione o servizio in uno spazio all'interno dell'organizzazione contribuisce all'utilizzo della quota. Con gli account Pagamento a consumo o Sottoscrizione, puoi modificare la tua quota per le applicazioni e i contenitori Cloud Foundry man mano che cambiano le esigenze della tua organizzazione. Vedi [Gestione della quota](/docs/account/manageorg.html#managequota).</dd>
</dl>

In un account Sottoscrizione, la quota è un limite definito dall'utente che attiva le notifiche di spesa.
{: tip}

In {{site.data.keyword.Bluemix_notm}}, puoi utilizzare le organizzazioni per abilitare la collaborazione tra gli utenti e facilitare il raggruppamento logico delle risorse del progetto nei seguenti modi:

   * Puoi raggruppare un insieme di spazi, applicazioni, servizi, domini, rotte e utenti nelle organizzazioni. 
   * Puoi gestire l'accesso agli spazi e alle organizzazioni in base ai singoli utenti. 

Quando crei un'organizzazione, il nome deve essere univoco in {{site.data.keyword.Bluemix_notm}}. Se il nome dell'organizzazione è già utilizzato da un altro utente di {{site.data.keyword.Bluemix_notm}} pubblico, dedicato o locale, devi specificare un nuovo nome. Dopo aver creato l'organizzazione, ti viene assegnata automaticamente l'autorizzazione di *Gestore organizzazione*, che ti consente di modificare il nome dell'organizzazione, aggiungere utenti e creare o eliminare spazi nell'organizzazione. Se hai un account fatturabile, puoi creare quante organizzazioni vuoi. Tuttavia, per un account Lite, puoi avere una sola organizzazione.  

Puoi contattare il supporto, se devi eliminare un'organizzazione. Quando elimini un'organizzazione, tutti gli
spazi e i servizi e tutte le applicazioni al suo interno vengono eliminati.

In un'organizzazione, è possibile assegnare i seguenti [ruoli utente](/docs/iam/users_roles.html#userrolesinfo). A tutti gli utenti invitati all'account viene assegnato il ruolo di revisore per impostazione predefinita.

   * Gestore organizzazione
   * Gestore fatturazione dell'organizzazione
   * Revisore organizzazione

Puoi creare un'organizzazione completando la seguente procedura:

1. Fai clic su **Gestisci** &gt; **Account** &gt; **Organizzazioni Cloud Foundry**.
2. Fai clic su **Aggiungi una nuova organizzazione Cloud Foundry**.
3. Immetti il nome dell'organizzazione.
4. Fai clic su **Aggiungi**.


## Creazione di spazi
{: #spaceinfo}

All'interno di un'organizzazione, puoi utilizzare gli spazi per raggruppare un insieme di applicazioni, servizi e utenti. Gli spazi sono collegati a una specifica
regione in {{site.data.keyword.Bluemix_notm}}.

Dopo aver aggiunto gli utenti a un'organizzazione, puoi concedere loro le autorizzazioni per gli spazi. Analogamente alle organizzazioni, anche gli spazi hanno una serie di [ruoli utente](/docs/iam/users_roles.html#userrolesinfo) con specifiche autorizzazioni che vengono assegnati ai membri del team:

  * Gestore spazio
  * Sviluppatore spazio
  * Revisore spazio

Ad un utente deve essere assegnata almeno una delle autorizzazioni nello spazio.
{: tip}

Puoi creare degli spazi nella tua organizzazione; ad esempio,
uno spazio *dev* come un ambiente di sviluppo,
uno spazio *test* come un ambiente di test e uno
spazio *production* come un ambiente di produzione. Puoi quindi associare
le tue applicazioni agli spazi. Per creare uno spazio, completa la seguente procedura:

1. Fai clic su **Gestisci** &gt; **Account** &gt; **Organizzazioni Cloud Foundry**.
2. Determina l'organizzazione a cui vuoi aggiungere uno spazio e seleziona **Visualizza dettagli**.
4. Fai clic su **Aggiungi uno spazio Cloud Foundry**.
5. Immetti il nome dello spazio.
6. Fai clic su **Aggiungi**.
