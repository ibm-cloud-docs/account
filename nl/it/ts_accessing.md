---

copyright:

  years: 2015, 2018

lastupdated: "2018-11-28"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}


# Risoluzione dei problemi di accesso a {{site.data.keyword.Bluemix_notm}}
{: #accessing}

I problemi generali con l'accesso a {{site.data.keyword.Bluemix}} potrebbero includere le difficoltà ad accedere a {{site.data.keyword.Bluemix_notm}} o un account che si trova in uno stato di sospensione. In molti casi, puoi risolvere questi problemi seguendo pochi semplici passi.
{:shortdesc}


## Perché la mia password non è corretta?
{: #ts_logintobm}
{: troubleshoot}

Per accedere alla console {{site.data.keyword.Bluemix_notm}}, devi disporre di una password valida associata al tuo ID IBM o al tuo ID SoftLayer.

Quando tenti di accedere a {{site.data.keyword.Bluemix_notm}}, viene visualizzato il seguente messaggio di errore:
{: tsSymptoms}

`La password immessa non è corretta.`

La password che hai utilizzato per accedere a {{site.data.keyword.Bluemix_notm}} non è valida.
{: tsCauses}

Utilizza una delle seguenti opzioni:
{: tsResolve}
 * Vai alla [pagina Il mio profilo IBM ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://myibm.ibm.com/dashboard/){: new_window} per confermare che stai utilizzando una password valida.
 * Se hai dimenticato la password, fai clic su **Password dimenticata** per reimpostarla.
 * Se hai dimenticato il tuo ID IBM o continui ad avere problemi con la tua password, contatta l'Help Desk Worldwide IBM Registration per ottenere assistenza.

Se esegui l'accesso a {{site.data.keyword.Bluemix_notm}} e il processo di accesso viene interrotto per un qualsiasi motivo, come ad esempio la reimpostazione della tua password, ritorna alla console e avvia nuovamente il processo di accesso.
{: tip}


## Perché il mio ID IBM o la mia email non sono stati riconosciuti?
{: #ts_old_username}
{: troubleshoot}

Per accedere correttamente alla tua email, devi assicurarti di avere l'autenticazione ID IBM per ciascun account.

Quando accedi alla console {{site.data.keyword.Bluemix_notm}}, viene visualizzato il seguente messaggio:
{: tsSymptoms}

`ID IBM o indirizzo e-mail non riconosciuto.`

Hai provato ad accedere alla console ma non hai utilizzato un ID IBM valido. Ad esempio, non hai immesso un indirizzo email completo per l'ID IBM oppure hai provato a utilizzare un nome utente e una password precedenti.
{: tsCauses}

Per accedere a {{site.data.keyword.Bluemix_notm}}, devi disporre di un ID IBM e password validi.

 * Immetti un indirizzo email completo per l'ID IBM.
 {: tsResolve}
 * Se sei un utente SoftLayer con un ID SoftLayer, devi passare all'autenticazione ID IBM in ciascun account a cui hai accesso prima di poter eseguire l'accesso. Per ulteriori informazioni, vedi [Passaggio all'ID IBM](/docs/account?topic=account-unifyingaccounts).


## Perché il mio ID IBM non è associato ad alcun account {{site.data.keyword.Bluemix_notm}}?
{: #ts_unabletologin}
{: troubleshoot}

Quando accedi a {{site.data.keyword.Bluemix_notm}}, viene visualizzato il seguente messaggio:
{: tsSymptoms}

`Hai raggiunto questa pagina perché l'autenticazione ha avuto esito positivo, tuttavia questo ID IBM non è associato ad alcun account {{site.data.keyword.Bluemix_notm}}.`

Hai eseguito l'accesso dalla [console {{site.data.keyword.Bluemix_notm}}](https://{DomainName}){: new_window} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno") con un ID IBM valido ma non hai un account {{site.data.keyword.Bluemix_notm}} che sia stato creato.
{: tsCauses}

Per creare un account {{site.data.keyword.Bluemix_notm}}, segui il processo di registrazione.
{: tsResolve}


## Perché la console non si apre quando eseguo l'accesso con il mio ID IBM?
{: #ts_login_stalls}
{: troubleshoot}

Quando ottieni un messaggio di accesso eseguito correttamente ma non ritorni alla console.

Quando esegui l'accesso utilizzando il tuo ID IBM, viene visualizzato un messaggio di accesso eseguito correttamente ma non ritorni alla [console {{site.data.keyword.Bluemix_notm}}](https://{DomainName}){: new_window} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno").
{: tsSymptoms}

Utilizza una delle seguenti opzioni:
{: tsResolve}
 * Chiudi il browser, cancella la cache e i cookie e riprova a eseguire l'accesso.
 * Accedi dalla [console {{site.data.keyword.Bluemix_notm}}](https://{DomainName}){: new_window} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno").


## Perché il mio accesso ID IBM non è stato completato?
{: #ts_login_ibmid}
{: troubleshoot}

Se accedi a {{site.data.keyword.Bluemix_notm}} e l'autenticazione del tuo ID IBM non viene completata, potrebbe esserci un problema con il servizio.

Quando accedi a {{site.data.keyword.Bluemix_notm}}, l'autenticazione tramite l'ID IBM non viene completata.
{: tsSymptoms}

Potrebbe esserci un problema con il servizio di autenticazione ID IBM.
{: tsCauses}

Assicurati di poter accedere a [IBM](https://idaas.iam.ibm.com/idaas/mtfim/sps/authsvc?PolicyId=urn:ibm:security:authentication:asf:basicldapuser){: new_window} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno"). In caso affermativo, si tratta di un problema dell'applicazione e puoi provare ad accedere nuovamente alla console in un secondo momento. Se non puoi accedere a tale pagina, contatta l'[IBMid help desk ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}.  
{: tsResolve}


## Perché non posso accedere immediatamente dopo che ho registrato un account?
{: #ts_accntpding}
{: troubleshoot}

Se il tuo account è in sospeso, non puoi accedere a {{site.data.keyword.Bluemix_notm}}.

Dopo aver eseguito la registrazione per un account Lite {{site.data.keyword.Bluemix_notm}}, potresti non riuscire ad accedere a {{site.data.keyword.Bluemix_notm}}. Viene visualizzato il seguente messaggio:
{: tsSymptoms}

<code>Your account is pending. Please wait up to 24 hours for email confirmation and also check your
spam folder. If you still have not received your e-mail confirmation, contact <a href="http://ibm.biz/bluemixsupport.com" target="_blank">{{site.data.keyword.Bluemix_notm}} Support</a>.</code>

Quando esegui la registrazione per un account {{site.data.keyword.Bluemix_notm}} Lite, ricevi una email che include un link su cui devi fare clic per confermare la tua registrazione.  
{: tsCauses}

L'email di conferma viene inviata all'indirizzo email associato al tuo ID IBM. Controlla la cartella della posta in arrivo e quella dello spam. Se non hai ricevuto l'email di conferma, contatta il [Supporto {{site.data.keyword.Bluemix_notm}}](/docs/get-support?topic=get-support-getting-customer-support).  
{: tsResolve}


## Perché mi imbatto in pagine della console che non si caricano?
{: #ts_err}
{: troubleshoot}

Quando utilizzi la console {{site.data.keyword.Bluemix_notm}}, potresti non riuscire a caricare una pagina della console. Potresti visualizzare invece i messaggi di errore BXNUI0001E o BXNUI0016E.

Potresti vedere uno dei seguenti messaggi di errore:
{: tsSymptoms}

`BXNUI0001E: La pagina non è stata caricata perché {{site.data.keyword.Bluemix_notm}} non ha rilevato se esiste una sessione.`

`BXNUI0016E: Le applicazioni e i servizi non sono stati recuperati perché una pagina di {{site.data.keyword.Bluemix_notm}} non è stata caricata.`

Completa una o più delle seguenti azioni, secondo necessità:
{: tsResolve}

  * Aggiorna o riavvia il tuo browser.
  * Disconnettiti da {{site.data.keyword.Bluemix_notm}} e
riesegui l'accesso.
  * Utilizza la modalità di navigazione privata del tuo browser.
  * Cancella i cookie e la cache del browser.
  * Utilizza un browser differente. Per informazioni sulle versioni dei browser supportate da {{site.data.keyword.Bluemix_notm}}, vedi [Prerequisiti di {{site.data.keyword.Bluemix_notm}}](/docs/overview?topic=overview-prereqs-platform).
  * Se hai installato l'interfaccia riga di comando Cloud Foundry, immetti il comando `ibmcloud cf apps` per vedere se la tua applicazione è in esecuzione.
