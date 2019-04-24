---


copyright:

  years: 2018, 2019
lastupdated: "2019-01-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}


# Impostazione della protezione dell'accesso
{: #login-settings}

Con l'accesso autorizzato, puoi impostare della protezione supplementare per il tuo accesso. Puoi impostare delle domande e delle risposte di sicurezza, selezionare una scadenza della password, impostare un'autenticazione multifattore (MFA, multifactor authentication) con passcode monouso con scadenza (TOTP, time-based one-time passcode) e impostare delle opzioni di autenticazione esterne.  
{:shortdesc}

Il proprietario di un account può richiedere l'MFA ID IBM su un account di cui sei un membro. L'MFA ID IBM sovrascrive qualsiasi altra impostazione di MFA utente. Ad esempio, quando viene impostata l'MFA ID IBM, ti viene richiesta una MFA TOTP associata al tuo ID IBM invece delle domande di sicurezza o di uno dei metodi di autenticazione esterni.
{: note}

Puoi visualizzare le seguenti opzioni di sicurezza, e abilitarle o disabilitarle, solo se il tuo amministratore ti concede l'accesso. Vai all'icona **{{site.data.keyword.avatar}}** ![Icona Avatar](../icons/i-avatar-icon.svg) > **Profilo e impostazioni** e seleziona **Impostazioni di accesso**.

## Impostazione delle domande di sicurezza
{: #security-questions}

Per impostare le tue domande di sicurezza:
1. Dalla console, vai all'icona **{{site.data.keyword.avatar}}** ![Icona Avatar](../icons/i-avatar-icon.svg) > **Profilo e impostazioni** e seleziona **Impostazioni di accesso**.
2. Fai clic su **Modifica**.
3. Seleziona le domande che vuoi ti vengano poste e rispondi ad esse. Devi utilizzare tre opzioni di domanda di sicurezza.
4. Una volta completata l'operazione, fai clic su **Salva**.  
5. Assicurati che la casella `Sì` sia selezionata perché le domande di sicurezza siano abilitate. La selezione della casella `Sì` potrebbe richiederti di eseguire nuovamente l'accesso al tuo account.  

Puoi impostare le risposte a tre domande di sicurezza per un'autenticazione supplementare all'accesso. Devi impostare le tue domande e risposte di sicurezza prima che il tuo amministratore possa abilitare questo requisito di MFA per tuo conto.

Devi essere il proprietario dell'account o disporre dell'impostazione di accesso gestito dall'utente (User-managed login) abilitata per tuo conto dall'amministratore del tuo account per attivare e disattivare le domande di sicurezza.
{: note}

## Impostazione di una scadenza della password
{: #password-expiration}

Per impostare il periodo di tempo per cui vuoi utilizzare la tua password attuale, seleziona un'opzione per la scadenza della tua password nella sezione **Scadenza password**.

La scadenza della password è impostata su mai per impostazione predefinita. Quando esegui la registrazione per un account, non ti viene mai richiesto di modificare la tua password. Quando imposti un periodo di scadenza della password, vieni avvisato della scadenza della tua password per email 14 e 7 giorni prima della scadenza impostata della password e anche il giorno stesso della scadenza.

Questa opzione è disponibile solo per gli utenti che eseguono l'accesso con un ID SoftLayer. Per aggiornare la scadenza della tua password, devi essere il proprietario di un account oppure disporre dell'impostazione di accesso gestito dall'utente (User-managed login) abilitata per tuo conto dall'amministratore del tuo account nella tua pagina dei dettagli dell'utente IAM.
{: note}

## Impostazione dell'autenticazione TOTP
{: #MFA}

Per impostare la tua autenticazione TOTP, fai clic su **Configura**.

La MFA TOTP aggiunge un livello supplementare di protezione al tuo account richiedendo un passcode TOTP, oltre all'ID e alla password standard, durante l'accesso. Devi impostare la tua autenticazione TOTP prima che il tuo amministratore possa abilitare questo requisito di MFA per tuo conto.

Ti potrebbe essere richiesto un passcode monouso con scadenza (TOTP, time-based one-time passcode) anche se l'impostazione TOTP utente non è impostata e abilitata. Ciò è dovuto al fatto che un proprietario di account potrebbe attivare l'MFA ID IBM per un account a cui si ha accesso. Questo tipo di MFA si applica a tutti gli utenti presenti nell'account quando questa impostazione viene attivata e sei obbligato a utilizzarla. Per ulteriori informazioni, vedi [Tipi di autenticazione multifattore](/docs/iam?topic=iam-types).


## Configurazione dell'autenticazione esterna
{: #third-party-MFA}

Puoi ordinare l'autenticazione Symantec oppure basata sul telefono, oppure può farlo per te l'amministratore del tuo account, per un costo mensile. Per ordinare tu l'autenticazione esterna, devi disporre delle autorizzazioni dell'infrastruttura di aggiunta di servizi. Per appurare se l'autenticazione esterna è abilitata, vai all'icona **{{site.data.keyword.avatar}}** ![Icona Avatar](../icons/i-avatar-icon.svg) > **Profilo e impostazioni** e seleziona **Impostazioni di accesso**.

### Impostazione dell'autenticazione Symantec

Se l'amministratore del tuo account sceglie di ordinare la protezione dell'identità Symantec, devi lavorare insieme a lui per aiutarlo a completare l'ordine fornendo il tuo ID credenziale:

1. Vai a [VIP Symantec](https://vip.symantec.com/).
2. Fai clic su **Scarica**.
3. Ottieni il tuo ID credenziale e fornisci l'ID al tuo amministratore per completare l'ordine.

Dopo che il tuo amministratore ha ordinato e abilitato l'opzione, puoi utilizzare l'applicazione per l'autenticazione dell'accesso.

### Impostazione dell'autenticazione basata sul telefono

Puoi configurare e utilizzare una protezione dell'identità basata sul telefono dopo che l'amministratore del tuo account la ordina e la abilita.

1. Vai all'icona **{{site.data.keyword.avatar}}** ![Icona Avatar](../icons/i-avatar-icon.svg) > **Profilo e impostazioni** e seleziona **Impostazioni di accesso**.
2. Se la MFA basata sul telefono è disabilitata, fai clic su **Vai a Dettagli utente**.
3. Nella sezione Gestisci l'accesso dell'utente, attiva l'autenticazione basata sul telefono.
4. Per fornire le informazioni di contatto per l'autenticazione, fai clic sull'icona **Modifica** ![Icona Modifica](../icons/edit-tagging.svg).
5. Completa tutti i campi. Puoi specificare se ricevere una chiamata telefonica o un messaggio di testo come metodo di autenticazione. Se vuoi richiedere un PIN, seleziona l'opzione dall'elenco **Tipo di pin** e fornisci il PIN che desideri utilizzare.  
6. Fai clic su **Applica**.
