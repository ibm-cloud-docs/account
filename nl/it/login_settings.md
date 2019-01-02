---


copyright:

  years: 2018
lastupdated: "2018-11-29"


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

Puoi visualizzare le seguenti opzioni di sicurezza, e abilitarle o disabilitarle, solo se il tuo amministratore ti concede l'accesso. Vai all'icona **{{site.data.keyword.avatar}}** ![Icona Avatar](../icons/i-avatar-icon.svg) > **Profile and settings** e seleziona **Login settings**.

## Impostazione delle domande di sicurezza
{: #security-questions}

Per impostare le tue domande di sicurezza:
1. Dalla console, vai all'icona **{{site.data.keyword.avatar}}** ![Icona Avatar](../icons/i-avatar-icon.svg) > **Profile and settings** e seleziona **Login settings**.
2. Fai clic su **Edit**. 
3. Seleziona le domande che vuoi ti vengano poste e rispondi ad esse. Devi utilizzare tre opzioni di domanda di sicurezza.
4. Una volta completata l'operazione, fai clic su **Save**.  
5. Assicurati che la casella `Yes` sia selezionata perché le domande di sicurezza siano abilitate. La selezione della casella `Yes` potrebbe richiederti di eseguire nuovamente l'accesso al tuo account.  

Puoi impostare le risposte a tre domande di sicurezza per un'autenticazione supplementare all'accesso. Devi impostare le tue domande e risposte di sicurezza prima che il tuo amministratore possa abilitare questo requisito di MFA per tuo conto.

Devi essere il proprietario dell'account o disporre dell'impostazione di accesso gestito dall'utente (User-managed login) abilitata per tuo conto dall'amministratore del tuo account per attivare e disattivare le domande di sicurezza.
{: note}

## Impostazione di una scadenza della password
{: #password-expiration}

Per impostare il periodo di tempo per cui vuoi utilizzare la tua password attuale, seleziona un'opzione per la scadenza della tua password nella sezione **Password expiration**.

La scadenza della password è impostata su never (mai) per impostazione predefinita. Quando esegui la registrazione per un account, non ti viene mai richiesto di modificare la tua password. Quando imposti un periodo di scadenza della password, vieni avvisato della scadenza della tua password per email 14 e 7 giorni prima della scadenza impostata della password e anche il giorno stesso della scadenza.

Questa opzione è disponibile solo per gli utenti che eseguono l'accesso con un ID SoftLayer. Per aggiornare la scadenza della tua password, devi essere il proprietario di un account oppure disporre dell'impostazione di accesso gestito dall'utente (User-managed login) abilitata per tuo conto dall'amministratore del tuo account nella tua pagina dei dettagli dell'utente IAM.
{: note}

## Impostazione dell'autenticazione TOTP
{: #MFA}

Per impostare la tua autenticazione TOTP, fai clic su **Set up**. 

La MFA TOTP aggiunge un livello supplementare di protezione al tuo account richiedendo un passcode TOTP, oltre all'ID e alla password standard, durante l'accesso. Devi impostare la tua autenticazione TOTP prima che il tuo amministratore possa abilitare questo requisito di MFA per tuo conto.

Ti potrebbe essere richiesto un passcode monouso con scadenza (TOTP, time-based one-time passcode) anche se l'impostazione TOTP utente non è impostata e abilitata. Ciò è dovuto al fatto che un proprietario di account potrebbe attivare l'MFA ID IBM per un account a cui si ha accesso. Questo tipo di MFA si applica a tutti gli utenti presenti nell'account quando questa impostazione viene attivata e sei obbligato a utilizzarla. Per ulteriori informazioni, vedi [Tipi di autenticazione multifattore](/docs/iam/mfatypes.html#types).


## Impostazione delle opzioni di autenticazione esterna
{: #third-party-MFA}

Puoi ordinare l'autenticazione Symantec oppure basata sul telefono, oppure può farlo per te l'amministratore del tuo account, per un costo mensile. Per ordinare tu l'autenticazione esterna, devi disporre delle autorizzazioni dell'infrastruttura di aggiunta di servizi. Per appurare se l'autenticazione esterna è abilitata, vai all'icona **{{site.data.keyword.avatar}}** ![Icona Avatar](../icons/i-avatar-icon.svg) > **Profile and settings** e seleziona **Login settings**. Se la MFA basata sul telefono è disabilitata, fai clic su **Go to User details**. Questo link ti porterà alla stessa pagina della procedura per impostare la tua autenticazione symantec e per impostare la tua autenticazione basata sul telefono.  

### Impostazione dell'autenticazione Symantec

Se l'amministratore del tuo account sceglie di ordinare la protezione dell'identità Symantec, devi lavorare insieme a lui per aiutarlo a completare l'ordine fornendo il tuo ID credenziale:

1. Vai a [Symantec VIP](https://vip.symantec.com/).
2. Fai clic su **Scarica**. 
3. Ottieni il tuo ID credenziale e fornisci l'ID al tuo amministratore per completare l'ordine. 

Dopo che il tuo amministratore ha ordinato e abilitato l'opzione, puoi utilizzare l'applicazione per l'autenticazione dell'accesso.

### Impostazione dell'autenticazione basata sul telefono

Se l'amministratore del tuo account sceglie di ordinare la protezione dell'identità basata sul telefono, devi impostarla dopo che il tuo amministratore l'ha ordinata. L'amministratore può quindi abilitarla per consentirti di utilizzarla. Dopo che il tuo amministratore ha ordinato l'autenticazione basata sul telefono, completa la seguente procedura per impostarla.

1. Vai a **Gestisci** > **Accesso (IAM)**.
2. Fai clic su **Utenti** e seleziona il tuo nome dall'elenco.
3. Dalla pagina **Dettagli utente** nella sezione **Gestisci l'accesso degli utenti**, fai clic sull'icona **Modifica** ![Icona Modifica](../icons/icon_write.svg) per la riga **Autenticazione basata sul telefono**.
4. Attieniti alle richieste per impostare la tua autenticazione basata sul telefono:

Dopo che hai impostato la tua autenticazione basata sul telefono, l'amministratore dell'account può abilitare l'opzione in modo che ti venga richiesto questo tipo di MFA all'accesso.


 

