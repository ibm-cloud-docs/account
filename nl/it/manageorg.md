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

# Gestione delle organizzazioni
In qualità di proprietario dell'account o di gestore dell'organizzazione, puoi eseguire attività di gestione dell'organizzazione, che includono la rinominazione dell'organizzazione, l'eliminazione di un'organizzazione o uno spazio, l'aggiornamento dei ruoli e la gestione della quota e dei domini.
{:shortdesc}

Per gestire le tue organizzazioni dalla console {{site.data.keyword.Bluemix}}, fai clic su **Gestisci > Account > Organizzazioni Cloud Foundry**. Puoi visualizzare le risorse di una sola organizzazione alla volta. Se sei membro di più organizzazioni, puoi passare da un'organizzazione all'altra utilizzando il link delle preferenze dell'account utente nella barra dei menu della console.

## Rinominazione di organizzazioni
{: #orgrename}

Per rinominare la tua organizzazione, completa la seguente procedura:
1. Fai clic su **Gestisci** > **Account** > **Organizzazioni Cloud Foundry**.
2. Determina quale organizzazione vuoi rinominare e fai clic su **Visualizza dettagli**.
3. Fai clic su **Modifica organizzazione Cloud Foundry**.
4. Fai clic su **Modifica** accanto al nome dell'organizzazione.
5. Immetti il nuovo nome per l'organizzazione e fai clic su **Salva**.

## Eliminazione di organizzazioni e spazi
{: #deleteorgs}

### Eliminazione di un'organizzazione

Quando elimini un'organizzazione, tutti gli
spazi e i servizi e tutte le applicazioni al suo interno vengono eliminati. Ricorda che le operazioni di eliminazione non possono essere annullate. 

### Eliminazione di uno spazio

Per eliminare uno spazio, completa la seguente procedura:

1. Fai clic su **Gestisci** > **Account** > **Organizzazioni Cloud Foundry**.
2. Seleziona l'organizzazione che vuoi eliminare e fai clic su **Visualizza dettagli**.
3. Determina quale spazio eliminare e fai clic su **Modifica spazio**.
4. Fai clic su **Elimina spazio Cloud Foundry**.

## Modifica dei ruoli utente
{: #listmembers}

### Modifica dei ruoli utente per un'organizzazione specifica 

Completa la seguente procedura per modificare i ruoli degli utenti per una specifica organizzazione:

1. Fai clic su **Gestisci** > **Account** > **Organizzazioni Cloud Foundry**.
2. Determina quale organizzazione vuoi modificare e fai clic su **Visualizza dettagli** e quindi su **Modifica organizzazione**.
4. Puoi visualizzare i membri della tua organizzazione e i loro ruoli nella scheda **UTENTI**.

### Modifica dei ruoli utente per uno spazio specifico

Completa la seguente procedura per modificare i ruoli degli utenti per uno specifico spazio:

1. Fai clic su **Gestisci** > **Account** > **Organizzazioni Cloud Foundry**.
2. Seleziona l'organizzazione per cui desideri visualizzare i membri e fai clic su **Visualizza dettagli**.
3. Determina quale spazio vuoi modificare e fai clic su **Modifica spazio**.
4. Puoi visualizzare i membri del tuo spazio e i loro ruoli nella scheda **UTENTI**.

## Gestione della quota
{: #managequota}

In qualità di proprietario dell'account o di gestore dell'organizzazione {{site.data.keyword.Bluemix_notm}}, puoi visualizzare la quota utilizzata e assegnata per un'organizzazione. La quota rappresenta i limiti di risorse per l'organizzazione, che viene assegnata quando l'organizzazione viene creata. Le risorse disponibili per un'organizzazione variano a seconda che tu disponga di un account gratuito o di un account fatturabile. Applicazioni o servizi in uno spazio all'interno dell'organizzazione contribuiscono tutti all'utilizzo della quota assegnata.

Per visualizzare la quota utilizzata e assegnata per un'organizzazione, completa la seguente procedura:

1. Fai clic su **Gestisci** &gt; **Account** &gt; **Organizzazioni Cloud Foundry**.
2. Identifica l'organizzazione per cui vuoi visualizzare la quota e fai clic su **Visualizza dettagli**.
3. Fai clic su **Modifica organizzazione**.
4. Se hai degli spazi definiti in più di un'organizzazione, seleziona la specifica regione che vuoi visualizzare.
5. Fai clic su **QUOTA**. 
6. Per impostazione predefinita, si apre la pagina della quota **Cloud Foundry**. Puoi visualizzare i dettagli della quota per le seguenti risorse:
 * MEMORIA
 * SERVIZI
 * PIANO
 * PREZZO
7. Fai clic su **Contenitori** per visualizzare l'assegnazione della quota utilizzate e disponibile per i contenitori. L'assegnazione del contenitore varia a seconda del piano prezzi. Puoi visualizzare i dettagli della quota per le seguenti risorse:
 * MEMORIA
 * IP PUBBLICO
 * CONDIVISIONI FILE
8. Fai clic su **Server virtuali** per visualizzare le macchine virtuali.

I contenitori non sono disponibili nella regione Sydney per {{site.data.keyword.Bluemix_notm}}. 
{: tip}

Per ulteriori informazioni sui contenitori, vedi [Quota](/docs/containers/container_planning.html#container_planning_quota) nella documentazione dei contenitori.
Per modificare la quota assegnata a un'organizzazione, devi aprire un ticket di supporto. Per ulteriori informazioni sull'apertura di un ticket di supporto, vedi [Richiesta di assistenza clienti](/docs/get-support/howtogetsupport.html#getting-customer-support). 

## Gestione dei domini
{: #managedomains}

In qualità di proprietario dell'account o di gestore dell'organizzazione {{site.data.keyword.Bluemix_notm}}, puoi visualizzare il dominio di sistema e aggiungere domini personalizzati per le applicazioni create all'interno di un'organizzazione e dei suoi spazi. In qualità di gestore spazio, la scheda **Domini** per uno spazio è un elenco di sola lettura dei domini assegnati allo spazio.

1. Fai clic su **Gestisci** &gt; **Account** &gt; **Organizzazioni Cloud Foundry**.
2. Identifica l'organizzazione per cui vuoi visualizzare o modificare i domini.
3. Seleziona **Visualizza dettagli** per tale organizzazione.
4. Fai clic su **Modifica organizzazione**.
5. Fai clic su **DOMINI**.

Se aggiungi un dominio personalizzato, devi configurare il server DNS per far sì che il tuo dominio personalizzato punti al dominio di sistema {{site.data.keyword.Bluemix_notm}}. In questo modo, quando {{site.data.keyword.Bluemix_notm}} riceve una richiesta per il tuo dominio personalizzato, può correttamente instradarla alla tua applicazione. Il dominio di sistema è sempre disponibile per uno spazio e a uno spazio è anche possibile assegnare dei domini personalizzati. Le applicazioni create in uno spazio possono utilizzare qualsiasi dominio elencato per quello spazio. Per ulteriori informazioni sulla creazione e l'utilizzo dei domini personalizzati, vedi [Utilizzo di un dominio personalizzato](/docs/apps/updapps.html#domain).
