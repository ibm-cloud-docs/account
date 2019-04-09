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


# Aggiornamento di organizzazioni e spazi
{: #orgupdates}

In qualità di proprietario dell'account o di gestore organizzazione {{site.data.keyword.Bluemix}}, puoi eseguire attività di gestione a livello dell'organizzazione e dello spazio. Queste attività includono la ridenominazione di un'organizzazione o di uno spazio, l'assegnazione o l'aggiornamento dei ruoli utente Cloud Foundry, la gestione dei domini e la visualizzazione dei dettagli della quota dell'organizzazione.
{:shortdesc}

Vai a **Gestisci > Account** e seleziona **Organizzazioni Cloud Foundry**.

Puoi visualizzare le risorse di una sola organizzazione alla volta. Se sei membro di più organizzazioni, puoi passare da un'organizzazione all'altra utilizzando il link delle preferenze dell'account utente nella barra dei menu della console.
{: tip}

  * Per rinominare un'organizzazione, fai clic sull'icona Azioni ![Icona Azioni](../icons/action-menu-icon.svg) per l'organizzazione che vuoi rinominare e seleziona **Rinomina**.
    {: #orgrename}

    Le modifiche da te apportate si applicano a tutti gli utenti nell'organizzazione.

  * Per eliminare un'organizzazione, contatta il [Supporto](/docs/get-support?topic=get-support-getting-customer-support).
    {: #deleteorgs}

    Quando un'organizzazione viene eliminata, tutti gli spazi e le risorse nell'organizzazione vengono eliminati. I risultati prodotti da questa azione non possono essere annullati.

  * Per eliminare uno spazio, seleziona l'organizzazione in cui è assegnato lo spazio. Fai quindi clic sull'icona Azioni ![Icona Azioni](../icons/action-menu-icon.svg) e seleziona **Elimina**.

    Quando elimini uno spazio, vengono eliminati anche tutti gli utenti e le risorse inclusi.

  * Per modificare i ruoli utente a livello dell'organizzazione, fai clic sull'icona Azioni ![Icona Azioni](../icons/action-menu-icon.svg) e seleziona **Utenti**.
    {: #listmembers}

    A seconda di come vuoi modificare le autorizzazioni dell'utente, seleziona o deseleziona la casella di spunta di un ruolo specifico. I ruoli che puoi assegnare a livello dell'organizzazione sono Gestore, Gestore fatturazione e Revisore. Per ulteriori informazioni, vedi [Ruoli Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles).

  * Per modificare i ruoli utente per uno specifico spazio, fai clic sull'organizzazione in cui è assegnato lo spazio. Fai quindi clic sul nome dello spazio.

    A seconda di come vuoi modificare le autorizzazioni dell'utente, seleziona o deseleziona la casella di spunta di un ruolo specifico. I ruoli che puoi assegnare a livello dello spazio sono Gestore, Sviluppatore e Revisore. Per ulteriori informazioni, vedi [Ruoli Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles).

  * Per gestire i tuoi domini, fai clic sull'icona Azioni ![Icona Azioni](../icons/action-menu-icon.svg) per la rispettiva organizzazione e seleziona **Domini**.
    {: #managedomains}

    In qualità di proprietario dell'account o di gestore dell'organizzazione, puoi visualizzare il dominio di sistema e aggiungere domini personalizzati per le applicazioni create all'interno di un'organizzazione e dei relativi spazi. Se sei un gestore spazio, questa pagina visualizza l'elenco di sola lettura dei domini che sono assegnati allo spazio.

    Se aggiungi un dominio personalizzato, devi configurare il server DNS per far sì che il tuo dominio personalizzato punti al dominio di sistema {{site.data.keyword.Bluemix_notm}}. In questo modo, quando {{site.data.keyword.Bluemix_notm}} riceve una richiesta per il tuo dominio personalizzato, viene correttamente instradata alla tua applicazione. Il dominio di sistema è sempre disponibile per uno spazio e a uno spazio è anche possibile assegnare dei domini personalizzati. Le applicazioni create in uno spazio potrebbero utilizzare uno qualsiasi dei domini elencati per tale spazio. Per ulteriori informazioni sulla creazione e l'utilizzo dei domini personalizzati, vedi [Gestione dei tuoi domini](/docs/apps?topic=creating-apps-update-domain).

  * Per gestire la quota assegnata per un'organizzazione, fai clic sull'icona Azioni ![Icona Azioni](../icons/action-menu-icon.svg) per la rispettiva organizzazione e seleziona **Quote**.
    {: #managequota}

    Da qui puoi visualizzare i dettagli della quota per il numero di applicazioni, la quantità di memoria, il numero di servizi e i dettagli del piano. La quota rappresenta i limiti di risorse per l'organizzazione, che viene assegnata quando l'organizzazione viene creata. Le risorse disponibili per un'organizzazione variano a seconda che tu disponga di un account gratuito o di un account fatturabile. Tutte le applicazioni o tutti i servizi inclusi in uno spazio all'interno dell'organizzazione contribuiscono all'utilizzo della quota assegnata.

    Per modificare la quota assegnata ad un'organizzazione, devi creare un caso di supporto. Per ulteriori informazioni, vedi [Gestione dei casi di supporto](/docs/get-support?topic=get-support-open-case).

    Per visualizzare i dettagli della quota a livello dello spazio per ciascuna ubicazione, fai clic sull'icona Azioni ![Icona Azioni](../icons/action-menu-icon.svg) per la rispettiva organizzazione e seleziona **Quote**. Espandi quindi ciascuna riga come appropriato.
