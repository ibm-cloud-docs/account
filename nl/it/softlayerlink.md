---

copyright:

  years: 2016, 2018

lastupdated: "2018-11-17"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Passaggio all'ID IBM e collegamento degli account
{: #unifyingaccounts}

Un ID IBM è un singolo ID che utilizzi per accedere al tuo account {{site.data.keyword.Bluemix}} per accedere e acquistare funzioni di infrastruttura, servizi e applicazione. Tutti i nuovi account ricevono automaticamente un ID IBM e gli account SoftLayer esistenti, con l'eccezione degli account federati SAML, sono abilitati per passare all'autenticazione ID IBM.
{:shortdesc}

## Passaggio all'ID IBM
{: #switchtoIBMid}

Quando inizi il processo di passaggio a un ID IBM, puoi sempre annullare il passaggio prima di completare il processo. Tuttavia, ogni volta che accedi, viene visualizzato il prompt per passare a un ID IBM. Ogni account SoftLayer che prevedi di collegare a un account {{site.data.keyword.Bluemix_notm}} deve appartenere a un unico ID IBM con un indirizzo e-mail univoco.

Per passare il tuo account SoftLayer esistente a un ID IBM, crea un ID IBM e quindi utilizza il tuo codice di registrazione per confermarlo.

### Richiesta di un ID IBM e di un codice di registrazione
{: #reqIBMidandregcode}

1. Accedi al tuo account SoftLayer e fai clic su **OK** quando viene visualizzato il prompt per passare a un ID IBM.

   Se sei un utente master e non viene visualizzato un prompt per passare a un ID IBM nel portale del cliente, contatta il supporto IBM per assistenza. Vedi [Richiesta di supporto](/docs/get-support/howtogetsupport.html#getting-customer-support) per ulteriori informazioni su come contattare il supporto.

   Se hai già eseguito l'accesso e hai fatto clic su **Dopo** nel prompt, ma vuoi passare all'autenticazione con l'ID IBM nella sessione corrente, vai alla pagina Modifica profilo utente e fai clic su **Passa a ID IBM**.

2. Segui le istruzioni della procedura guidata per creare il tuo ID IBM.

   Immetti un indirizzo e-mail che non sia attualmente utilizzato da nessun ID IBM. Questo indirizzo e-mail viene utilizzato come nome utente per il nuovo ID IBM ed è l'indirizzo a cui viene inviato il tuo codice di registrazione una volta che l'ID IBM è stato creato. Puoi aggiornare l'indirizzo e-mail associato all'ID IBM in un secondo momento, ma non puoi modificare il nome utente.

### Conferma de tuo ID IBM con il codice di registrazione
{: #confIBMiduseregcode}

1. Quando ricevi il tuo codice di registrazione, fai clic sul link nell'e-mail o copia l'URL in un browser e immetti il codice di registrazione. Il codice di registrazione è valido per sette giorni e puoi utilizzarlo solo una volta.

2. Una volta inoltrato il codice di registrazione, utilizza il tuo ID IBM per accedere al portale clienti.

   Al prompt di accesso dell'account, vai alla sezione **Accesso account ID IBM** e fai clic su **Accedi con ID IBM**. Non utilizzare i campi **Nome utente** e **Password** che utilizzavi in precedenza con il tuo ID SoftLayer.

Se sei un nuovo cliente, quando controlli il tuo ordine ti verrà chiesto il tuo ID IBM esistente o di creare un nuovo ID IBM.
  * Per utilizzare un ID IBM esistente, immetti il nome utente o l'indirizzo e-mail dell'ID IBM se non è condiviso tra più ID IBM.
  * Per creare un nuovo ID IBM, immetti un indirizzo e-mail che non sia attualmente utilizzato da nessun ID IBM. Questo indirizzo e-mail è il nome utente per l'ID IBM ed è l'indirizzo a cui viene inviato il tuo codice di registrazione una volta che l'ID IBM è stato creato. Puoi aggiornare l'indirizzo e-mail associato all'ID IBM in un secondo momento, ma non puoi modificare il nome utente.

Per risolvere eventuali problemi con l'accesso con il tuo ID IBM, vedi [Risoluzione dei problemi di accesso a {{site.data.keyword.Bluemix_notm}}](/docs/account/ts_accessing.html#accessing).


## Collegamento degli account ID IBM
{: #link_accounts}

Dopo che gli account sono diventati account ID IBM, puoi collegare gli account SoftLayer e {{site.data.keyword.Bluemix_notm}} per utilizzare insieme le risorse IaaS (Infrastructure as a service) e PaaS (Platform as a Service). Quindi, puoi accedere alle risorse IaaS e PaaS da un singolo accesso. Il collegamento dei tuoi account ti fornisce inoltre una sola fattura per tutte le risorse PaaS e IaaS che utilizzi. Puoi collegare il tuo account o, se sei un utente master, puoi collegare i tuoi account utente.

### Collegamento del tuo account ID IBM
{: #link_user_account}

Se sei un cliente dell'infrastruttura classica e hai anche degli account PaaS in {{site.data.keyword.Bluemix_notm}} o li crei, puoi collegare IaaS e PaaS per una singola visualizzazione dei tuoi account. Per collegare i tuoi account, utilizza la seguente procedura:
1. Accedi al tuo account SoftLayer.
2. Dalla pagina Riepilogo account, fai clic su **Nuovo! Collega un account Bluemix**.
3. Rivedi i termini di utilizzo e fai clic per confermare.
4. Completa uno dei seguenti passi finali, a seconda di come è configurato il tuo account:
  * Se il tuo ID IBM ha un account {{site.data.keyword.Bluemix_notm}} associato, sarai reindirizzato a una pagina di autorizzazione, quindi tornerai al passo di conferma finale.
  * Se non hai un account {{site.data.keyword.Bluemix_notm}} associato, ti viene richiesto di crearne uno.

Per vedere le domande e le risposte comuni sul collegamento del tuo account, controlla le [FAQ](/docs/account/account_faq.html#al_login).

### Collegamento degli account utente ID IBM
{: #link_customer_accounts}

Dopo che i tuoi account utente sono passati all'autenticazione tramite ID IBM, i rivenditori e i distributori possono collegare i propri account utente. Per collegare gli account utente, devi essere un utente master SoftLayer. L'ID IBM che è l'utente master dell'account deve essere il proprietario dell'account della piattaforma {{site.data.keyword.Bluemix_notm}} a cui ti colleghi. 

Dopo aver collegato i tuoi account, non è possibile scollegarli.
{: note}

Assicurati di esaminare le seguenti note importanti sul collegamento degli account:

  * L'utente master dell'account SoftLayer che viene collegato deve avere un ID IBM.
  * Ogni account utente che colleghi a un account {{site.data.keyword.Bluemix_notm}} deve appartenere a un unico ID IBM con un indirizzo e-mail univoco. Anche se un singolo ID IBM può possedere più account SoftLayer, devi modificare l'utente master in modo da essere un ID IBM univoco per ogni account. Contatta il supporto per modificare l'utente master di un account SoftLayer. Per ulteriori informazioni, vedi [Richiesta di supporto per l'infrastruttura {{site.data.keyword.Bluemix_notm}}](/docs/customer-portal/cpsupport.html).
  * Quando aggiungi nuovi utenti a un account collegato, devi aggiungerli a entrambi agli account SoftLayer e {{site.data.keyword.Bluemix_notm}} affinché possano accedere a tutte le funzionalità nella console unificata.
  * Se hai un account aziendale, utilizza il portale BAP (Brand Agent Portal) e se hai bisogno di assistenza quando colleghi il tuo account, contatta il team di Revenue Services inviando una e-mail a softlayer_revenue_services_team@wwpdl.vnet.ibm.com.

Completa la seguente procedura per collegare ciascun account SoftLayer a un account della piattaforma {{site.data.keyword.Bluemix_notm}} esistente o per crearne uno nuovo:

   1. Accedi al portale del cliente con il tuo ID IBM dell'account utente master.
   2. Dal portale del cliente, fai clic su **Collega un account Bluemix**.
   3. Leggi e accetta le condizioni di collegamento degli account SoftLayer e {{site.data.keyword.Bluemix_notm}}.
   4. Segui le istruzioni nella procedura guidata, inclusa l'aggiunta di utenti nell'account SoftLayer all'account {{site.data.keyword.Bluemix_notm}}.
   5. Quando ti viene richiesto, scegli una delle seguenti azioni:
     * Se hai già un account {{site.data.keyword.Bluemix_notm}}, fornisci l'indirizzo e-mail associato a tale account per collegare gli account.
     * Se non hai un account {{site.data.keyword.Bluemix_notm}}, fornisci l'indirizzo e-mail che desideri utilizzare e segui le istruzioni per ricevere l'invito a {{site.data.keyword.Bluemix_notm}} e creare un account.
   6. Dopo aver collegato l'account, informa l'utente finale di ogni account di migrare all'ID IBM utilizzando la procedura descritta nella sezione precedente [Passaggio all'ID IBM](/docs/account/softlayerlink.html#switchtoIBMid).

      Migra solo gli account dell'utente finale all'ID IBM. Non migrare gli account dell'azienda che sono account principali per gli account utente finale e non contengono alcuna risorsa. Gli utenti degli account dell'azienda che eseguono la migrazione all'ID IBM perdono la possibilità di accedere al portale BAP (Brand Agent Portal).
      {: important}

Tieni presente le seguenti modifiche dopo che i tuoi account sono stati collegati:
  
  * Puoi ora accedere alla [console {{site.data.keyword.Bluemix}} ![Icona link esterno](../icons/launch-glyph.svg)](https://cloud.ibm.com){: new_window}.
  * Devi utilizzare le credenziali dell'ID IBM per accedere a entrambi gli account SoftLayer e {{site.data.keyword.Bluemix_notm}}.
  * Eventuali sconti SoftLayer esistenti vengono applicati agli addebiti {{site.data.keyword.Bluemix_notm}}.
  * Ricevi un'unica fattura in dollari americani (USD). Se hai un account {{site.data.keyword.Bluemix_notm}} esistente, la fatturazione tramite {{site.data.keyword.Bluemix_notm}} per le risorse dell'infrastruttura parte dal nuovo ciclo di fatturazione che inizia dopo il collegamento degli account. Per ulteriori informazioni, vedi [Fatturazione consolidata per gli account collegati](/docs/customer-portal/linking_accounts.html).
  * Puoi monitorare l'utilizzo delle tue risorse dell'infrastruttura classica nella console {{site.data.keyword.Bluemix_notm}}.

## Utilizzo dell'autenticazione a più fattori negli account collegati
{: #2fa}

Se hai un account collegato, puoi utilizzare la pagina **Impostazioni** di {{site.data.keyword.Bluemix_notm}} per abilitare l'autenticazione multifattore (MFA, multi-factor authentication) per il tuo account. Questa è anche comunemente nota come autenticazione a due fattori (2FA) e aggiunge un livello di sicurezza per accedere al tuo account oltre all'ID IBM e alla password standard richiesti. La MFA per il tuo account si applica a tutte le risorse nel tuo account {{site.data.keyword.Bluemix_notm}} collegato. Se è abilitata per il tuo account, si applica anche a tutti gli utenti che sono stati aggiunti al tuo account.

Altri metodi di autenticazione multifattore non sono per singolo ID IBM. Sono per singolo account. Quando un ID IBM è associato a più account e tu passi da un account all'altro, devi confermare la tua identità ogni volta che passi a un account diverso che richiede l'autenticazione a due fattori. Ciò è vero anche se l'account precedente e il nuovo account sono entrambi configurati con lo stesso meccanismo di autenticazione a due fattori.

Se hai precedentemente abilitato [2FA nel portale del cliente](/docs/customer-portal/cpenable2fa.html#customerportal_2fa) per le risorse della tua infrastruttura classica, e abiliti quindi l'impostazione MFA dell'account {{site.data.keyword.Bluemix_notm}}, l'impostazione dell'account MFA sovrascrive la 2FA che avevi impostato nel portale del cliente. Questo significa che puoi disabilitare la 2FA da te acquistata nel portale del cliente a favore dell'impostazione MFA dell'account. 
