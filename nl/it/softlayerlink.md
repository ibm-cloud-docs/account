---

copyright:

  years: 2016, 2018

lastupdated: "2018-02-08"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Passaggio all'ID IBM e collegamento degli account
{: #unifyingaccounts}

L'autenticazione in SoftLayer utilizza adesso un ID IBM per fornire un singolo accesso per tutti i {{site.data.keyword.Bluemix}}. Un ID IBM è un singolo ID che utilizzi per accedere al tuo account {{site.data.keyword.Bluemix}} per accedere e acquistare funzioni di infrastruttura, servizi e applicazione. L'autenticazione con ID IBM è abilitata per tutti i nuovi account in SoftLayer e gli account SoftLayer esistenti sono abilitati per passare all'autenticazione con ID IBM.
{:shortdesc}

## Passaggio all'ID IBM
{: #switchtoIBMid}

Quando inizi il processo di passaggio a un ID IBM, puoi sempre annullare il passaggio prima di completare il processo. Tuttavia, ogni volta che accedi, viene visualizzato il prompt per passare a un ID IBM. Ogni account SoftLayer che prevedi di collegare a un account {{site.data.keyword.Bluemix_notm}} deve appartenere a un unico ID IBM con un indirizzo e-mail univoco.

Per passare il tuo account SoftLayer esistente a un ID IBM, crea un ID IBM e quindi utilizza il tuo codice di registrazione per confermarlo.

### Richiesta di un ID IBM e di un codice di registrazione
{: #reqIBMidandregcode}

1. Accedi al tuo account SoftLayer e fai clic su **OK** quando viene visualizzato il prompt per passare a un ID IBM.

   Se sei un utente master e non visualizzi un prompt per passare a un ID IBM nel {{site.data.keyword.slportal}}, contatta il [supporto IBM](/docs/get-support/howtogetsupport.html#getting-customer-support) per assistenza.

   Se hai già eseguito l'accesso e hai fatto clic su **Dopo** nel prompt, ma vuoi passare all'autenticazione con l'ID IBM nella sessione corrente, vai alla pagina Modifica profilo utente e fai clic su **Passa a ID IBM**.

2. Segui le istruzioni della procedura guidata per creare il tuo ID IBM.

   Immetti un indirizzo e-mail che non sia attualmente utilizzato da nessun ID IBM. Questo indirizzo e-mail viene utilizzato come nome utente per il nuovo ID IBM ed è l'indirizzo a cui viene inviato il tuo codice di registrazione una volta che l'ID IBM è stato creato. Puoi aggiornare l'indirizzo e-mail associato all'ID IBM in un secondo momento, ma non puoi modificare il nome utente.

### Conferma de tuo ID IBM con il codice di registrazione
{: #confIBMiduseregcode}

1. Quando ricevi il tuo codice di registrazione, fai clic sul link nell'e-mail o copia l'URL in un browser e immetti il codice di registrazione.

   Il codice di registrazione è valido per sette giorni e puoi utilizzarlo solo una volta.

2. Una volta inoltrato il codice di registrazione, utilizza il tuo ID IBM per accedere al portale del cliente.

   Al prompt di accesso dell'account, vai alla sezione **Accesso account ID IBM** e fai clic su **Accedi con ID IBM**. Non utilizzare i campi **Nome utente** e **Password** che utilizzavi in precedenza con il tuo ID SoftLayer.

Se sei un nuovo cliente, quando controlli il tuo ordine ti verrà chiesto il tuo ID IBM esistente o di creare un nuovo ID IBM.
  * Per utilizzare un ID IBM esistente, immetti il nome utente o l'indirizzo e-mail dell'ID IBM che sia univoco (vale a dire, che non sia condiviso tra più ID IBM).

  * Per creare un nuovo ID IBM, immetti un indirizzo e-mail che non sia attualmente utilizzato da nessun ID IBM. Questo indirizzo e-mail è il nome utente per l'ID IBM ed è l'indirizzo a cui viene inviato il tuo codice di registrazione una volta che l'ID IBM è stato creato. Puoi aggiornare l'indirizzo e-mail associato all'ID IBM in un secondo momento, ma non puoi modificare il nome utente.

Per risolvere eventuali problemi con l'accesso con il tuo ID IBM, vedi [Risoluzione dei problemi di accesso a {{site.data.keyword.Bluemix_notm}}](/docs/get-support/ts_accessing.html#accessing).


## Collegamento degli account utente ID IBM
{: #link_user_accounts}

Dopo che i tuoi account utente sono passati all'autenticazione tramite ID IBM, i rivenditori e i distributori possono collegare gli account SoftLayer e {{site.data.keyword.Bluemix_notm}} per utilizzare insieme le risorse dell'infrastruttura e della piattaforma. Assicurati di esaminare le seguenti note importanti:

  * L'utente master dell'account che viene collegato deve avere un ID IBM.
  * Ogni account utente che colleghi a un account {{site.data.keyword.Bluemix_notm}} deve appartenere a un unico ID IBM con un indirizzo e-mail univoco. Anche se un singolo ID IBM può possedere più account SoftLayer, devi modificare l'utente master in modo da essere un ID IBM univoco per ogni account. Contatta il supporto per modificare l'utente master di un account SoftLayer. Per ulteriori informazioni, vedi [Richiesta di supporto per l'infrastruttura {{site.data.keyword.Bluemix_notm}}](/docs/customer-portal/cpsupport.html).
  * Quando aggiungi nuovi utenti a un account collegato, devi aggiungerli a entrambi agli account SoftLayer e {{site.data.keyword.Bluemix_notm}} affinché possano accedere a tutte le funzionalità nella console unificata.
  * Se sei un utente dell'account dell'azienda che utilizza portale BAP (Brand Agent Portal) e hai bisogno di assistenza per collegare il tuo account, contatta il team di SoftLayer Revenue Services inviando una e-mail a softlayer_revenue_services_team@wwpdl.vnet.ibm.com.
  * Tutti gli accoint collegati in {{site.data.keyword.Bluemix_notm}} devono essere del tipo Pagamento a consumo. Puoi creare un nuovo account Pagamento a consumo, collegare un account Pagamento a consumo esistente oppure collegare un account di prova esistente, che viene quindi aggiornato a un account Pagamento a consumo. Non puoi collegare gli account Sottoscrizione.

Per collegare gli account, devi essere un utente master. L'ID IBM che è l'utente master dell'account deve essere il proprietario dell'account {{site.data.keyword.Bluemix_notm}} a cui ti colleghi. Completa la seguente procedura per collegare ciascun account SoftLayer a un account {{site.data.keyword.Bluemix_notm}} esistente o per crearne uno nuovo:

   1. Accedi al Portale del cliente con il tuo account di utente master user.
   2. Dal Portale del cliente {{site.data.keyword.Bluemix_notm}}, fai clic su **Collega un account {{site.data.keyword.Bluemix_notm}}**.
   3. Leggi e accetta le condizioni di collegamento degli account SoftLayer e {{site.data.keyword.Bluemix_notm}}.
   4. Segui le istruzioni nella procedura guidata, inclusa l'aggiunta di utenti nell'account SoftLayer all'account {{site.data.keyword.Bluemix_notm}}.
   5. Quando richiesto, fornisci l'indirizzo e-mail associato al tuo account {{site.data.keyword.Bluemix_notm}}. Se non hai un account {{site.data.keyword.Bluemix_notm}}, fornisci l'indirizzo e-mail che desideri utilizzare, segui le istruzioni per ricevere l'invito a {{site.data.keyword.Bluemix_notm}} e crea un account.
   6. Dopo aver collegato l'account, informa l'utente finale di ogni account di migrare all'ID IBM utilizzando la procedura descritta nella sezione precedente.

Migra solo gli account dell'utente finale all'ID IBM. Non migrare gli account dell'azienda che sono account principali per gli account utente finale e non contengono alcuna risorsa. Gli utenti degli account dell'azienda che eseguono la migrazione all'ID IBM perdono la possibilità di accedere al portale BAP (Brand Agent Portal).
{: tip}

Dopo che gli account sono stati collegati:

  * Devi utilizzare le credenziali dell'ID IBM per accedere a entrambi gli account SoftLayer e {{site.data.keyword.Bluemix_notm}}.
  * Eventuali sconti SoftLayer esistenti vengono applicati agli addebiti {{site.data.keyword.Bluemix_notm}}.
  * Riceverai un'unica fattura in dollari americani (USD). Se hai un account {{site.data.keyword.Bluemix_notm}} esistente, la fatturazione tramite {{site.data.keyword.Bluemix_notm}} per le risorse dell'infrastruttura parte dal nuovo ciclo di fatturazione che inizia dopo il collegamento degli account.
  * Puoi monitorare l'utilizzo delle tue risorse dell'infrastruttura nella console {{site.data.keyword.Bluemix_notm}}.

Dopo aver collegato i tuoi account, non possono essere scollegati.

## Utilizzo dell'autenticazione a più fattori negli account collegati
{: #2fa}

Se hai un account collegato, puoi utilizzare la pagina **Impostazioni** di Identità e accesso per abilitare l'autenticazione a più fattori (/docs/iam/mfa.html) per il tuo account. Questa è anche comunemente nota come autenticazione a due fattori (2FA) e aggiunge un livello di sicurezza per accedere al tuo account oltre all'ID IBM e alla password standard richiesti. L'autenticazione a più fattori per il tuo account si applica a tutte le risorse nel tuo account {{site.data.keyword.Bluemix_notm}} collegato. Se è abilitata per il tuo account, si applica anche a tutti gli utenti che sono stati aggiunti al tuo account. Scopri di più sulle considerazioni da esaminare quando si [abilita l'autenticazione a più fattori](/docs/iam/mfa.html) per il tuo account.

L'autenticazione a più fattori non è per ogni ID IBM, ma è tuttora per ogni account. Quando un ID IBM è associato a più account e tu passi da un account all'altro, devi confermare la tua identità ogni volta che passi a un account diverso che richiede l'autenticazione a due fattori. Ciò è vero anche se l'account precedente e il nuovo account sono entrambi configurati con lo stesso meccanismo di autenticazione a due fattori.
