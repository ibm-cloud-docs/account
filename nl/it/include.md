---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-28"

keywords: add user, share resource, private resource, share catalog

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Aggiunta di account alla tua risorsa privata
{: #include}

Qualsiasi risorsa privata {{site.data.keyword.Bluemix}} che crei è limitata per impostazione predefinita. Se sei un amministratore per l'account, puoi scegliere chi può visualizzare la tua risorsa aggiungendo l'utente a un elenco di inclusione.
{:shortdesc: .shortdesc}

Puoi utilizzare l'{{site.data.keyword.Bluemix}} [interfaccia riga di comando (CLI, command-line interface)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) o la console per determinare se disponi dell'accesso per consentire agli utenti di visualizzare una risorsa privata che era stata aggiunta all'account. Se sei un proprietario di account, puoi concedere l'accesso a un utente nel tuo account dalla console assegnando una politica di accesso. Per ulteriori informazioni, vedi [Gestione dell'accesso al tuo account](/docs/account?topic=account-find-access).

## Individuazione della tua risorsa
{: #find-resource-inc}

Esegui `ibmcloud catalog service <service-id or service-name>`. Sostituisci le variabili service-id o service-name con il nome o l'ID della tua risorsa. Utilizza le informazioni restituite per visualizzare la gerarchia, che mostra le risorse secondarie degli elementi nella tua risorsa.

## Impostazione della visibilità includendo un account
{: #vis-inc}

Esegui il seguente comando per consentire a un account di visualizzare la tua risorsa privata.

`ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

Dopo l'indicatore includes-add, puoi aggiungere un elenco separato da virgole di e-mail o ID associati agli account.

Dopo che hai eseguito il comando, il processo per includere la risorsa richiede circa 30 minuti. Dopo 30 minuti, scollegati e torna al tuo account per vedere la risorsa inclusa.

## Rimozione di un account dall'elenco di inclusione
{: #remove-include}

Esegui il seguente comando per rimuovere un account dall'elenco di inclusione.

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## Esempio: gestione della visibilità degli oggetti secondari
{: #child-vis}

Puoi gestire la visibilità della tua risorsa o dei suoi elementi secondari. Un elenco di inclusione vuoto significa che solo gli amministratori dell'account possono visualizzarlo. Perché possa essere visualizzato da tutti i membri dell'account, il tuo account deve essere inserito nell'elenco di inclusione.

Il seguente esempio mostra come puoi eseguire il comando `ibmcloud catalog service cloudant` per visualizzare gli elementi secondari di un'istanza del servizio Cloudant.

```
ID                 cloudant
Nome               cloudantnosqldb
Tipo               service
Provider           IBM
Tag                data_management, ibm_created, ibm_dedicated_public, lite
Attivo             true
Descrizione        Cloudant NoSQL DB è un livello dati completamente gestito progettato per le moderne applicazioni Web e mobili che utilizza uno schema JSON flessibile. Cloudant è costruito e compatibile con Apache CouchDB ed è accessibile tramite un'API HTTPS sicura, che si adatta all'ampliamento della tua applicazione. Cloudant è certificato ISO27001 e SOC2 di Tipo 1 e tutti i dati vengono memorizzati in triplice copia su nodi fisici separati in un cluster per HA/DR all'interno di un data center.
Associabile        true
Compatibile RC     false
Con provisioning RC false
Elemento secondario Nome                                          Tipo         ID                                      Ubicazione
                   lite                                          plan         cloudant-lite
                   |__lite-eu-gb                             deployment   cloudant-lite:eu-gb                          eu-gb
                   |  |__lite-alias-eu-gb                    alias        cloudant-lite:alias:eu-gb                    eu-gb
                   |__lite-us-south                          deployment   cloudant-lite:us-south                       us-south
                      |__lite-alias-us-south                 alias        cloudant-lite:alias:us-south                 us-south
                   standard                                      plan         cloudant-standard
                   |__standard-eu-gb                         deployment   cloudant-standard:eu-gb                      eu-gb
                   |  |__standard-alias-eu-gb                alias        cloudant-standard:alias:eu-gb                eu-gb
                   |__standard-us-south                      deployment   cloudant-standard:us-south                   us-south
                      |__standard-alias-us-south             alias        cloudant-standard:alias:us-south             us-south
```

Puoi ottenere l'ID risorsa per la distribuzione secondaria e quindi includere un account eseguendo il seguente comando:

`ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`

Gli elementi secondari di un oggetto possono ereditare la visibilità in modi complessi. Se l'oggetto secondario è privato, ha la propria configurazione di visibilità. Tuttavia, se l'oggetto secondario è impostato su pubblico, eredita la visibilità del suo elemento principale. L'impostazione della visibilità su un oggetto secondario privato potrebbe limitare la sua visibilità a più dell'elemento principale. Per ulteriori informazioni su come funziona la visibilità, consulta la [documentazione sulle API del catalogo](https://{DomainName}/apidocs/globalcatalog).

## Trasferimento della proprietà di una risorsa privata
{: #owners}

Se lasci il tuo progetto o la tua organizzazioni, potresti voler trasferire la proprietà del tuo account a qualcun altro.
{:shortdesc}

Dopo che hai trasferito la proprietà, non puoi più visualizzare la risorsa dal tuo account. Assicurati che vuoi trasferire la proprietà poiché i risultati prodotti da questa azione non possono essere annullati.
{: important}

Puoi utilizzare l'[{{site.data.keyword.Bluemix}}interfaccia riga di comandi (CLI, command-line interface)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) per trasferire la proprietà di una risorsa privata. Immetti il seguente comando:

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
