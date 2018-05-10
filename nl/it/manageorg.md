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

# Aggiornamento di organizzazioni e spazi 
{: #orgupdates}

In qualità di proprietario dell'account o di gestore dell'organizzazione, puoi effettuare attività di gestione al livello dell'organizzazione e dello spazio. Queste attività includono la ridenominazione di un'organizzazione o di uno spazio, l'assegnazione o l'aggiornamento dei ruoli utente Cloud Foundry, la gestione dei domini e la visualizzazione dei dettagli della quota dell'organizzazione.
{:shortdesc}

Per gestire le tue organizzazioni dalla console {{site.data.keyword.Bluemix}}, fai clic su **Gestisci > Account > Organizzazioni Cloud Foundry**. Puoi visualizzare le risorse di una sola organizzazione alla volta. Se sei membro di più organizzazioni, puoi passare da un'organizzazione all'altra utilizzando il link delle preferenze dell'account utente nella barra dei menu della console. 

## Rinominazione di organizzazioni
{: #orgrename}

Completa la seguente procedura per rinominare la tua organizzazione. Nota che le modifiche apportate si applicano a tutti gli utenti nell'organizzazione. 

1. Fai clic su **Gestisci** > **Account** > **Organizzazioni Cloud Foundry**.
2. Fai clic sull'icona Azioni per l'organizzazione che vuoi rinominare e seleziona **Rinomina**.   
3. Immetti il nuovo nome e fai clic su **Salva**. 

## Eliminazione di organizzazioni e spazi
{: #deleteorgs}

### Eliminazione di un'organizzazione

Per eliminare un'organizzazione, contatta il [Supporto](/docs/get-support/howtogetsupport.html). Quando un'organizzazione viene eliminata, tutti gli spazi e le risorse nell'organizzazione vengono eliminati. Ricorda che le operazioni di eliminazione non possono essere annullate.  

### Eliminazione di uno spazio

Quando elimini uno spazio, vengono eliminati anche tutti gli utenti e le risorse inclusi. Per eliminare uno spazio, completa la seguente procedura:

1. Fai clic su **Gestisci** > **Account** > **Organizzazioni Cloud Foundry**.
2. Fai clic sull'organizzazione in cui è assegnato lo spazio. 
3. Fai clic sull'icona Azioni e seleziona **Elimina**.
4. Conferma di voler eliminare lo spazio immettendo il nome dello spazio nel campo e fai clic su **Elimina**.

## Modifica dei ruoli utente
{: #listmembers}

I ruoli che puoi assegnare al livello dell'organizzazione sono gestore, gestore della fatturazione e revisore. I ruoli che puoi assegnare al livello dello spazio sono gestore, sviluppatore e revisore. Per le descrizioni del ruolo dettagliate, vedi [Ruoli Cloud Foundry](/docs/iam/cfaccess.html#cfroles).

### Modifica dei ruoli utente al livello dell'organizzazione 

Completa la seguente procedura per modificare i ruoli degli utenti per una specifica organizzazione: 

1. Fai clic su **Gestisci** > **Account** > **Organizzazioni Cloud Foundry**.
2. Fai clic sull'icona Azioni e seleziona **Utenti**.
3. A seconda di come vuoi modificare le autorizzazioni dell'utente, seleziona o deseleziona la casella di spunta di un ruolo specifico.
4. Conferma le tue modifiche facendo clic su **Salva**.  

### Modifica dei ruoli utente al livello dello spazio 

Completa la seguente procedura per modificare i ruoli degli utenti per uno specifico spazio:

1. Fai clic su **Gestisci** > **Account** > **Organizzazioni Cloud Foundry**.
2. Fai clic sull'organizzazione in cui è assegnato lo spazio. 
3. Fai clic sul nome dello spazio.
4. A seconda di come vuoi modificare le autorizzazioni dell'utente, seleziona o deseleziona la casella di spunta di un ruolo specifico.
5. Conferma le tue modifiche facendo clic su **Salva**. 

## Gestione dei domini
{: #managedomains}

In qualità di proprietario dell'account o di gestore dell'organizzazione, puoi visualizzare il dominio di sistema e aggiungere domini personalizzati per le applicazioni create all'interno di un'organizzazione e dei relativi spazi. In qualità di gestore dello spazio, la scheda **Domini** è un elenco di sola lettura dei domini assegnati allo spazio. 

1. Fai clic su **Gestisci** &gt; **Account** &gt; **Organizzazioni Cloud Foundry**.
2. Fai clic sull'icona Azioni per l'organizzazione e seleziona **Domini**.

Se aggiungi un dominio personalizzato, devi configurare il server DNS per far sì che il tuo dominio personalizzato punti al dominio di sistema {{site.data.keyword.Bluemix_notm}}. In questo modo, quando {{site.data.keyword.Bluemix_notm}} riceve una richiesta per il tuo dominio personalizzato, viene correttamente instradata alla tua applicazione. Il dominio di sistema è sempre disponibile per uno spazio e a uno spazio è anche possibile assegnare dei domini personalizzati. Le applicazioni create in uno spazio possono utilizzare qualsiasi dominio elencato per quello spazio. Per ulteriori informazioni sulla creazione e l'utilizzo dei domini personalizzati, vedi [Utilizzo di un dominio personalizzato](/docs/apps/updapps.html#domain).

## Gestione della quota
{: #managequota}

Puoi visualizzare la quota assegnata e utilizzata per un'organizzazione. La quota rappresenta i limiti di risorse per l'organizzazione, che viene assegnata quando l'organizzazione viene creata. Le risorse disponibili per un'organizzazione variano a seconda che tu disponga di un account gratuito o di un account fatturabile. Tutte le applicazioni o i servizi inclusi in uno spazio all'interno dell'organizzazione contribuiscono tutti all'utilizzo della quota assegnata. 

Per visualizzare la quota utilizzata e assegnata per un'organizzazione, completa la seguente procedura:

1. Fai clic su **Gestisci** &gt; **Account** &gt; **Organizzazioni Cloud Foundry**.
2. Fai clic sull'icona Azioni per l'organizzazione specifica e seleziona **Quote**.

   Per impostazione predefinita, viene visualizzata la pagina della quota **Cloud Foundry**. Da qui, puoi visualizzare i dettagli della quota per le seguenti risorse: 
 
   * Il numero di applicazioni
   * La quantità di memoria  
   * Il numero di servizi  
   * I dettagli del piano 

3. Espandi i dettagli della regione per visualizzare la quota al livello dello spazio.  

Per modificare la quota assegnata a un'organizzazione, devi aprire un ticket di supporto. Per ulteriori informazioni, vedi [Richiesta di assistenza clienti](/docs/get-support/howtogetsupport.html#getting-customer-support). 

