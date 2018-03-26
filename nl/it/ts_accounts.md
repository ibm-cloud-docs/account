---

copyright:

  years: 2015, 2018

lastupdated: "2017-11-07"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Risoluzione dei problemi relativi alla gestione degli account
{: #managingaccounts}

I problemi generali con la gestione del tuo account potrebbero riguardare applicazioni diverse che condividono lo stesso nome dominio o amministratori che non riescono a visualizzare tutte le organizzazioni. In molti casi, puoi risolvere questi problemi seguendo pochi semplici passi.
{:shortdesc}

## Impossibile accedere a una regione {{site.data.keyword.Bluemix_notm}} differente
{: #nosecondreg}

Ricevi un messaggio di errore quando provi a creare una nuova regione {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Ciò è probabilmente dovuto al fatto che stai utilizzando un account Lite, che supporta lo sviluppo in una sola regione pubblica. Selezioni la regione pubblica di {{site.data.keyword.Bluemix_notm}} in cui vuoi lavorare durante la configurazione iniziale dell'account.
{: tsCauses}

Se hai un account Lite, puoi eseguire l'aggiornamento a un account fatturabile per accedere a ulteriori regioni. Vai alla pagina **Gestisci > Fatturazione e utilizzo > Fatturazione** nella console e fai clic su **Aggiungi carta di credito**. Nella pagina **Fatturazione**, puoi anche controllare se hai un account Lite.
{: tsResolve}

## Impossibile creare la nuova organizzazione
{: #nosecondorg}

Ricevi un messaggio di errore quando provi a creare una nuova organizzazione.
{: tsSymptoms}

Ciò è probabilmente dovuto al fatto che stai utilizzando un account Lite, che supporta lo sviluppo in una sola organizzazione. Crei l'organizzazione durante la configurazione iniziale del tuo account.
{: tsCauses}

Se hai un account Lite, puoi eseguire l'aggiornamento a un account fatturabile per accedere a ulteriori organizzazioni. Vai alla pagina **Gestisci > Fatturazione e utilizzo > Fatturazione** nella console e fai clic su **Aggiungi carta di credito**. Nella pagina **Fatturazione**, puoi anche controllare se hai un account Lite.
{: tsResolve}

## Impossibile creare la nuova istanza del piano Lite
{: #nosecondlite}

Ricevi il seguente messaggio di errore quando provi a creare una nuova istanza del piano Lite:
{: tsSymptoms}

`Unable to provision new Lite instance`

Esiste un limite di una singola istanza per istanza del piano Lite per consentirci di continuare a offrire tali piani gratuitamente.
{: tsCauses}

Puoi creare delle istanze aggiuntive del servizio selezionando uno dei piani del servizio fatturabili, disponibili negli account fatturabili. Per eseguire l'upgrade a un account fatturabile dalla console, vai alla pagina **Gestisci > Fatturazione e utilizzo > Fatturazione** e fai clic su **Aggiungi carta di credito**.
{: tsResolve}

Se non vuoi eseguire l'aggiornamento da un account Lite e non utilizzi più l'istanza del servizio Lite esistente, puoi eliminare l'istanza del piano Lite esistente dal dashboard e quindi creare una nuova istanza.

## È stata superata la franchigia di memoria di runtime
{: #noruntimemem}

Non riesci a distribuire applicazioni e ottieni un errore che indica che hai superato il limite di memoria della tua organizzazione.
{: tsSymptoms}

In un account Lite, le tue applicazioni Cloud Foundry possono utilizzare fino a 256 MB di memoria di runtime istantanea. Negli account fatturabili, esiste un limite di memoria di 2GB.
{: tsCauses}

Se utilizzi un account Lite, puoi ottenere della memoria aggiuntiva eseguendo l'aggiornamento a un account fatturabile. Vai alla pagina **Gestisci > Fatturazione e utilizzo > Fatturazione** nella console e fai clic su **Aggiungi carta di credito**.
{: tsResolve}

Se non vuoi eseguire l'aggiornamento da un account Lite ma hai delle applicazioni inattive, le puoi eliminare per liberare memoria di runtime.

## Account non attivo
{: #ts_accnt_inactive}

Non puoi creare un'applicazione in {{site.data.keyword.Bluemix_notm}} se il tuo account non è attivo. Per risolvere questo problema, devi contattare il team di supporto.

Quando tenti di creare un'applicazione in {{site.data.keyword.Bluemix_notm}}, viene visualizzato il seguente messaggio di errore:
{: tsSymptoms}

`BXNUI0096E: L'applicazione non è stata creata. Il tuo account non è attivo perché è stato annullato o sospeso.`

Lo stato del tuo account {{site.data.keyword.Bluemix_notm}} diventa inattivo quando l'account viene annullato o sospeso.
{: tsCauses}

Per riattivare il tuo account, contatta il [Supporto {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://ibm.biz/bluemixsupport.com){: new_window}. Includi le seguenti informazioni nell'e-mail:
{: tsResolve}

  * L'ID IBM utilizzato per accedere a {{site.data.keyword.Bluemix_notm}}.
  * Il nome dell'organizzazione in cui verrà creata la tua applicazione. Queste informazioni consentono al team di supporto di determinare se ti sono stati assegnati i ruoli o l'appartenenza appropriati nella tua organizzazione.

## Impossibile aggiungere utenti a un'organizzazione
{: #ts_adduser}

Puoi invitare più di un utente a lavorare nella stessa organizzazione. Puoi invitare utenti nella tua organizzazione solo
se sei il proprietario dell'account o se sei allo stesso tempo un gestore e un membro dell'organizzazione.

Non riesci a visualizzare il link **Invita un nuovo utente** nella sezione **Gestisci organizzazioni**.
{: tsSymptoms}

Solo i seguenti utenti {{site.data.keyword.Bluemix_notm}}
possono invitare gli utenti in un'organizzazione:
{: tsCauses}
  * Il proprietario dell'account dell'organizzazione
  * I gestori dell'organizzazione che sono anche membri, e non collaboratori,
dell'organizzazione

In {{site.data.keyword.Bluemix_notm}},
puoi essere un membro o un collaboratore di un'organizzazione.

<dl><dt>Collaboratore</dt>
<dd>Sei un collaboratore di un'organizzazione se disponi già di un account {{site.data.keyword.Bluemix_notm}} e qualcun altro ti invita nell'organizzazione.</dd>
<dt>Membro</dt>
<dd>Sei membro di un'organizzazione se non disponi di un account {{site.data.keyword.Bluemix_notm}}, ma poi qualcuno ti invita nell'organizzazione e ti registri a {{site.data.keyword.Bluemix_notm}} tramite l'invito.</dd>
</dl>

Non puoi invitare utenti nella tua organizzazione se sei un collaboratore, anche se ti è stato assegnato il ruolo di gestore organizzazione.

**Nota:** tutti i gestori organizzazione, compresi quelli che sono collaboratori di un'organizzazione, possono aggiungere, modificare e rimuovere gli utenti già presenti nell'organizzazione.

Se non riesci a inviare utenti nella tua organizzazione e per farlo hai bisogno di un ruolo differente, contatta il gestore della tua organizzazione per modificare il tuo ruolo. Per identificare il gestore della tua organizzazione, completa
la seguente procedura:
{: tsResolve}

  1. Dalla barra dei menu della console, fai clic su **Gestisci > Account > Organizzazioni**.
  2. Vai alla tua organizzazione e visualizza le informazioni del gestore organizzazione
sulla scheda **UTENTI**.  

Se non puoi invitare utenti perché sei un collaboratore e non un membro, devi eliminare il tuo account {{site.data.keyword.Bluemix_notm}} precedente ed essere inviato a entrare a far parte dell'account come membro dell'organizzazione. Per eliminare il tuo account precedente ed entrare a far parte dell'account come membro,
completa la seguente procedura:

  1. Contatta il [Supporto {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://ibm.biz/bluemixsupport){: new_window} per aprire un ticket di supporto e richiedere l'eliminazione del tuo account. Se hai dei dati associati al tuo
account precedente che vuoi salvare e passare al nuovo account,
includi queste informazioni nell'e-mail.
  2. Una volta eliminato il tuo account, fa sì che un utente con il ruolo di gestore
organizzazione ti inviti nell'organizzazione come gestore. Utilizza quindi l'invito per registrarti in
{{site.data.keyword.Bluemix_notm}}.

## La registrazione batch degli utenti non è supportata
{: #ts_batchregistration}

Quando
registri gli utenti per {{site.data.keyword.Bluemix_notm}},
devi registrare ciascun utente singolarmente.

{{site.data.keyword.Bluemix_notm}} non fornisce la capacità di registrare più utenti contemporaneamente.
{: tsSymptoms}

{{site.data.keyword.Bluemix_notm}} non
supporta la registra batch di utenti. Per registrare gli utenti per {{site.data.keyword.Bluemix_notm}},
devi registrare ciascun utente singolarmente.
{: tsCauses}

Per registrare più utenti per {{site.data.keyword.Bluemix_notm}}, completa la seguente procedura per ogni utente:
{: tsResolve}

  1. Fai clic su **ESEGUI REGISTRAZIONE** nella console {{site.data.keyword.Bluemix_notm}}.
  2. Completa i passi seguendo la procedura guidata.

## Nessuno spazio associato alla tua organizzazione corrente
{: #ts_no_space}

Non puoi creare un'applicazione se non ci sono spazi associati alla tua organizzazione corrente.

Quando tenti di creare un'applicazione in {{site.data.keyword.Bluemix_notm}}, viene visualizzato il seguente messaggio di errore:
{: tsSymptoms}

`BXNUI0097E: Prima di poter aggiungere un'applicazione, è necessario associare almeno uno spazio alla tua organizzazione e alla tua regione. Sul Dashboard, fai clic su Crea uno
spazio. Una volta creato lo spazio, prova di nuovo. `

Le applicazioni in {{site.data.keyword.Bluemix_notm}} devono essere create in uno spazio della tua organizzazione.
{: tsCauses}

Per creare uno spazio, utilizza uno dei seguenti metodi:
{: tsResolve}

  * Dalla barra dei menu della console, fai clic su **Gestisci > Account > Organizzazioni**. Quindi, seleziona l'organizzazione in cui vuoi creare lo spazio e fai clic su **Crea uno spazio**.
  * Nell'interfaccia riga di comando cf, immetti `cf create-space <space_name> -o <organization_name>`.


## Le applicazioni condividono lo stesso nome di dominio
{: #ts_domain_diff}

Potresti notare che diverse applicazioni condividono lo stesso URL in {{site.data.keyword.Bluemix_notm}}.

Questo problema potrebbe verificarsi se assegni la stessa rotta URL per le diverse applicazioni in uno spazio.
{: tsCauses}

Ad esempio, esegui il push dell'applicazione myApp1 a {{site.data.keyword.Bluemix_notm}} e imposta il dominio su "mynewapp.stage1.mybluemix.net". Esegui quindi il push di un'altra applicazione myApp2 allo stesso spazio e imposta una delle sue rotte URL su "mynewapp.stage1.mybluemix.net". La rotta è ora associata a entrambe le applicazioni.

Questo è il funzionamento supportato da {{site.data.keyword.Bluemix_notm}} e puoi utilizzare questa procedura affinché non si verifichino tempi di inattività per l'aggiornamento della tua applicazione. Per ulteriori informazioni, vedi [Using Blue-Green Deployment to Reduce Downtime and Risk ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://docs.cloudfoundry.org/devguide/deploy-apps/blue-green.html){: new_window}.
{: tsResolve}


## Gli amministratori non possono visualizzare tutte le organizzazioni utilizzando l'interfaccia utente {{site.data.keyword.Bluemix_notm}}
{: #ts_ui_org}

In qualità di amministratore, quando utilizzi l'interfaccia utente {{site.data.keyword.Bluemix_notm}}, non riesci a visualizzare tutte le organizzazioni per gestirle. Puoi visualizzare e gestire solo le organizzazioni alle quali appartieni.

In qualità di amministratore, non puoi visualizzare tutte le organizzazioni utilizzando l'interfaccia utente {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Questa è una limitazione dell'interfaccia utente {{site.data.keyword.Bluemix_notm}}.
{: tsCauses}

Puoi utilizzare i comandi come `cf orgs`, `cf create-org` e `cf delete-org` dall'interfaccia riga di comando cf per gestire tutte le organizzazioni. Per un elenco completo dei comandi cf, immetti `cf help`.
{: tsResolve}

## Impossibile aggiungere la carta di credito
{: #ts_addcc}

Non puoi inoltrare le informazioni della tua carta di credito per convertire il tuo account di prova in un account con pagamento a consumo.

Il pulsante **Inoltra** nella pagina Aggiungi carta di credito è disabilitato.
{: tsSymptoms}

Questo problema si verifica se non compili correttamente le tue informazioni nella pagina Aggiungi carta di credito.
{: tsCauses}


Completa
la seguente procedura:
{: tsResolve}

  1. Nella pagina Aggiungi carta di credito, compila tutti i campi obbligatori nelle sezioni relative a informazioni di contatto, indirizzo di contatto e indirizzo di fatturazione.
  2. Seleziona **Ho letto e accetto i termini e le condizioni IBM**
e fai clic su **Inoltra**. Viene visualizzata la sezione **Seleziona un
metodo di pagamento**.
  3. Immetti il numero della tua carta di credito, la data di scadenza e il codice di sicurezza indicato sulla carta. Fai quindi clic su **Inoltra**.
