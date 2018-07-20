---

copyright:

  years: 2015, 2018

lastupdated: "2018-07-09"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Risoluzione dei problemi di accesso a {{site.data.keyword.Bluemix_notm}}
{: #accessing}

I problemi generali con l'accesso a {{site.data.keyword.Bluemix}} potrebbero includere le difficoltà ad accedere a {{site.data.keyword.Bluemix_notm}} o un account che si trova in uno stato di sospensione. In molti casi, puoi risolvere questi problemi seguendo pochi semplici passi.
{:shortdesc}

## Password errata
{: #ts_logintobm}

Per accedere alla console {{site.data.keyword.Bluemix_notm}}, devi disporre di una password valida associata al tuo ID IBM.

Per eseguire l'accesso tramite il [{{site.data.keyword.slportal}}](https://control.softlayer.com), devi disporre anche di una password valida associata al tuo ID IBM o ID dell'account collegato.

Quando tenti di accedere a {{site.data.keyword.Bluemix_notm}}, viene visualizzato il seguente messaggio di errore:
{: tsSymptoms}

`La password immessa non è corretta.`

La password che hai utilizzato per accedere a {{site.data.keyword.Bluemix_notm}} non è valida.
{: tsCauses}

Utilizza una delle seguenti soluzioni:
{: tsResolve}
 * Immetti la password corretta. Per controllare se il tuo ID IBM e la tua password sono validi, puoi andare alla pagina Il mio profilo IBM, fai clic su **Accedi** e immettere il tuo ID IBM e la relativa password nella pagina di accesso.
 * Se hai dimenticato la password, fai clic su **Password dimenticata** per reimpostarla. Torna quindi alla [console {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) o al [{{site.data.keyword.slportal}}](https://control.softlayer.com) ed effettua di nuovo l'accesso.
 * Se hai dimenticato il tuo ID IBM o continui ad avere problemi con la tua password, contatta l'Help Desk Worldwide IBM Registration per ottenere assistenza.
 * Per ottenere un ID IBM e password validi, vai alla pagina Il mio profilo IBM e fai clic su **Registrati**.

**Nota:**  se ti trovi nella pagina di accesso a IBM e il processo di accesso viene interrotto per un qualsiasi motivo (ad esempio, la reimpostazione della password), torna alla [console {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) o al [{{site.data.keyword.slportal}}](https://control.softlayer.com) e inizia di nuovo il processo di accesso.


## Credenziali di accesso non valide
{: #ts_login_invalid_credentials}

Quando accedi utilizzando il tuo ID IBM, viene visualizzato il seguente messaggio:
{: tsSymptoms}

`Invalid login credentials provided. If you have an IBMid associated with your account, please log in here`

* Sei passato a un ID IBM, ma hai tentato di effettuare l'accesso tramite il [{{site.data.keyword.slportal}}](https://control.softlayer.com) utilizzando il tuo nome utente e password precedenti.
{: tsCauses}

* Hai tentato di accedere tramite il [{{site.data.keyword.slportal}}](https://control.softlayer.com), ma hai immesso il tuo ID IBM e la password nei campi Nome utente e Password.

Fai clic su **log in here** nel messaggio o vai alla sezione di accesso degli account ID IBM e fai clic su **Accedi con ID IBM**.
{: tsResolve}

Non utilizzare i campi **Nome utente** e **Password** che utilizzavi con il tuo precedente ID.


## ID IBM o e-mail non riconosciuti
{: #ts_old_username}

Quando accedi alla console {{site.data.keyword.Bluemix_notm}}, viene visualizzato il seguente messaggio:
{: tsSymptoms}

`ID IBM o indirizzo e-mail non riconosciuto.`

Hai tentato di accedere alla console {{site.data.keyword.Bluemix_notm}}, ma non hai utilizzato un ID IBM valido. Ad esempio, non hai immesso un indirizzo e-mail completo per l'ID IBM oppure hai tentato di utilizzare un nome utente e una password precedenti.
{: tsCauses}

Per accedere a {{site.data.keyword.Bluemix_notm}}, devi disporre di un ID IBM e password validi.

 * Assicurati di immettere un indirizzo e-mail completo per l'ID IBM.
 {: tsResolve}
 * Se sei un utente {{site.data.keyword.BluSoftlayer_full}} con un ID {{site.data.keyword.BluSoftlayer_full}}, devi passare all'autenticazione tramite ID IBM nel {{site.data.keyword.slportal}} per ogni account a cui hai accesso prima di poter accedere con l'autenticazione ID IBM.
 Per ulteriori informazioni, vedi [Passaggio all'ID IBM](/docs/account/softlayerlink.html).


## ID IBM non associato ad alcun account IBM Cloud
{: #ts_login_noswitch}

Quando accedi utilizzando il tuo ID IBM, viene visualizzato il seguente messaggio:
{: tsSymptoms}

`Hai raggiunto questa pagina perché l'autenticazione ha avuto esito positivo, tuttavia questo ID IBM non è associato ad alcun account Bluemix. Se credi che si tratti di un errore, contatta il proprietario dell'account o l'utente master.`

Hai effettuato l'accesso dal [{{site.data.keyword.slportal}}](https://control.softlayer.com) con un ID IBM valido, ma non sei passato all'autenticazione tramite ID IBM dal {{site.data.keyword.slportal}}.
{: tsCauses}

Completa i seguenti controlli, come appropriato:
{: tsResolve}
 * Contatta il tuo utente master o amministratore account per verificare di essere autorizzato a passare all'autenticazione con ID IBM.
 * Assicurati di completare il passo relativo al passaggio all'ID IBM. Vedi [Passaggio all'ID IBM](/docs/account/softlayerlink.html).
 * Assicurati di seguire i passaggi indicati nell'e-mail per **Associare il tuo ID utente a un ID IBM**. Controlla la cartella della posta in arrivo e quella della posta indesiderata per cercare l'e-mail. Per ricevere di nuovo l'e-mail, ad esempio nel caso in cui sia scaduta, vai alla pagina Modifica profilo utente nel {{site.data.keyword.slportal}} e fai clic su **Invia nuovamente e-mail**. In alternativa, contatta il [Supporto {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://ibm.biz/bluemixsupport.com){: new_window}.

**Nota:** se hai creato il tuo ID IBM direttamente con l'ID IBM, riceverai due e-mail per il processo: una dalla registrazione dell'ID IBM e una da {{site.data.keyword.Blu_full}}. Assicurati di seguire i passaggi indicati in entrambe le e-mail.

A seconda di come è configurato il tuo account, potrebbero essere applicabili alcune di queste opzioni di accesso:
 * Gli utenti {{site.data.keyword.BluSoftlayer_notm}} con ID {{site.data.keyword.BluSoftlayer_full}} devono eseguire l'accesso tramite il [{{site.data.keyword.slportal}}](https://control.softlayer.com).
 * Gli utenti {{site.data.keyword.BluSoftlayer_notm}} con un ID IBM e con o senza un account {{site.data.keyword.Bluemix_notm}} collegato, possono eseguire l'accesso tramite il [{{site.data.keyword.slportal}}](https://control.softlayer.com) per aprire il {{site.data.keyword.slportal}} o tramite la [console {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) per aprire il dashboard Infrastruttura.


## ID IBM non associato ad alcun account {{site.data.keyword.Bluemix_notm}}
{: #ts_unabletologin}

Quando accedi a {{site.data.keyword.Bluemix_notm}}, viene visualizzato il seguente messaggio:
{: tsSymptoms}

`Hai raggiunto questa pagina perché l'autenticazione ha avuto esito positivo, tuttavia questo ID IBM non è associato ad alcun account {{site.data.keyword.Bluemix_notm}}.`

Hai effettuato l'accesso dalla [console {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) con un ID IBM valido, ma non hai ancora creato un account {{site.data.keyword.Bluemix_notm}}.
{: tsCauses}

Per creare un account {{site.data.keyword.Bluemix_notm}}, segui il processo di registrazione.
{: tsResolve}

A seconda di come è configurato il tuo account, potrebbero essere applicabili alcune di queste opzioni di accesso:
 * Gli utenti {{site.data.keyword.Bluemix_notm}} senza un account collegato devono eseguire l'accesso tramite la console {{site.data.keyword.Bluemix_notm}}.
 * Gli utenti {{site.data.keyword.Bluemix_notm}} con un account collegato possono eseguire l'accesso tramite la [console {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) o il [{{site.data.keyword.slportal}}](https://control.softlayer.com).


## La console non si apre
{: #ts_login_stalls}

Quando accedi utilizzando il tuo ID IBM, viene visualizzato un messaggio di esito positivo dell'accesso ma non ritorni alla [console {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) o al [{{site.data.keyword.slportal}}](https://control.softlayer.com)
{: tsSymptoms}

Utilizza una delle seguenti soluzioni:
{: tsResolve}
 * Chiudi il browser, cancella la cache e i cookie e riprova a eseguire l'accesso.
 * Assicurati di eseguire l'accesso dalla [console {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) o dal [{{site.data.keyword.slportal}}](https://control.softlayer.com), piuttosto che direttamente dal servizio di autenticazione tramite ID IBM.


## L'accesso tramite ID IBM non viene completato
{: #ts_login_ibmid}

Quando accedi a {{site.data.keyword.Bluemix_notm}}, l'autenticazione tramite l'ID IBM non viene completata.
{: tsSymptoms}

Potrebbe esserci un problema con il servizio di autenticazione ID IBM.
{: tsCauses}

Verifica se puoi accedere alla [home page IBM ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/us-en/){: new_window}. Se puoi, si tratta di un problema dell'applicazione e puoi riprovare più tardi. Se non riesci ad accedere a tale pagina, contatta l'[Help Desk ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}.
{: tsResolve}


## L'account è in sospeso
{: #ts_accntpding}

Se il tuo account è in sospeso, non puoi accedere a {{site.data.keyword.Bluemix_notm}}.

Dopo aver eseguito la registrazione per un account di prova {{site.data.keyword.Bluemix_notm}}, potresti non riuscire ad accedere a {{site.data.keyword.Bluemix_notm}}. Viene visualizzato il seguente messaggio:
{: tsSymptoms}

<code>Your account is pending. Please wait up to 24 hours for email confirmation and also check your
spam folder. If you still have not received your e-mail confirmation, contact <a href="http://ibm.biz/bluemixsupport.com" target="_blank">{{site.data.keyword.Bluemix_notm}} Support</a>.</code>

Dopo aver eseguito la registrazione per un account di prova {{site.data.keyword.Bluemix_notm}}, riceverai un'e-mail di conferma. Dovrai fare clic sul link
che si trova nella email di conferma per completare il processo di registrazione.
{: tsCauses}

L'e-mail di conferma viene inviata all'indirizzo di posta
da te fornito. Controlla la cartella della posta in arrivo e quella dello spam. Se non hai ricevuto un'e-mail di conferma, contatta il [Supporto {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](http://ibm.biz/bluemixsupport.com){: new_window}.  
{: tsResolve}

## Impossibile caricare una pagina
{{site.data.keyword.Bluemix_notm}}
{: #ts_err}

Quando utilizzi la console {{site.data.keyword.Bluemix_notm}}, potresti non riuscire a caricare una pagina della console. Potresti visualizzare invece i messaggi di errore BXNUI0001E o BXNUI0016E.

Quando usi la console {{site.data.keyword.Bluemix_notm}} potresti visualizzare uno dei seguenti messaggi di errore:
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
  * Utilizza un browser differente. Per informazioni sulle versioni dei browser supportati da {{site.data.keyword.Bluemix_notm}}, vedi [Prerequisiti di {{site.data.keyword.Bluemix_notm}}](/docs/overview/prereqs.html#prereqs).
  * Se hai installato l'interfaccia riga di comando cf, immetti il comando `cf apps` per vedere se la tua applicazione è in esecuzione.
