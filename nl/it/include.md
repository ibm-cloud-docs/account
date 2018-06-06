---

copyright:

  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Aggiunta di account alla tua risorsa privata
{: #include}

Qualsiasi risorsa privata che crei è riservata per impostazione predefinita. Se sei un amministratore dell'account, puoi scegliere chi può vedere la tua risorsa aggiungendo gli utenti in un elenco di inclusione attraverso l'[interfaccia riga di comando](/docs/cli/reference/bluemix_cli/bx_cli.html#ibmcloud_catalog_entry_visibility_set) `ibmcloud`.
{:shortdesc: .shortdesc}

## Come faccio a sapere se dispongo dell'accesso?
{: #find-access}

Puoi utilizzare la CLI o l'interfaccia utente di Identità e accesso per determinare se disponi dell'accesso per consentire agli utenti di visualizzare una risorsa privata che è stata aggiunta all'account. Se sei un proprietario di account, puoi concedere l'accesso a un utente nel tuo account tramite l'interfaccia utente di Identity and Access Management assegnando una politica di accesso. Per ulteriori informazioni, vedi [Gestione dell'accesso al tuo account](access.html).

## Passo 1: trova la tua risorsa
{: #find-resource}

Immetti `ibmcloud catalog service <service-id or service-name>`. Sostituisci service-id o service-name con il nome o l'ID della tua risorsa. Con le informazioni restituite, puoi visualizzare la gerarchia, che mostra le risorse secondarie degli elementi nella risorsa.

## Passo 2: imposta la visibilità includendo un account
{: #vis-inc}

Immetti il seguente comando per consentire a un account di visualizzare la tua risorsa privata.

`ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

Dopo l'indicatore includes-add, puoi aggiungere un elenco separato da virgole di e-mail o ID associati agli account.

Una volta eseguito il comando, il processo per includere la risorsa richiede 30 minuti. Dopo 30 minuti, scollegati e torna al tuo account per vedere la risorsa inclusa.

## Rimuovi un account dall'elenco di inclusione
{: #remove-exclude}

Immetti il seguente comando per rimuovere un account dall'elenco di inclusione.

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## Gestione della visibilità di oggetti secondari
{: #child-vis}

Puoi gestire la visibilità della tua risorsa o dei suoi elementi secondari.

Un elenco di inclusione vuoto significa che solo gli amministratori del tuo account possono vederla. Perché possa essere vista da tutti i membri dell'account, il tuo account deve essere nell'elenco di inclusione.

Ad esempio, se immetti `ibmcloud catalog service <your_service>`, puoi vedere gli elementi secondari della risorsa.

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

Puoi ottenere l'ID risorsa per la distribuzione secondaria e quindi includere un account utilizzando il seguente comando. `ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`.

Gli elementi secondari di un oggetto possono ereditare la visibilità in modi complessi. Se l'oggetto secondario è privato, ha la propria configurazione di visibilità. Tuttavia, se l'oggetto secondario è impostato su pubblico, eredita la visibilità del suo elemento principale. L'impostazione della visibilità su un oggetto secondario privato può limitare la sua visibilità più dell'elemento principale.

Per ulteriori informazioni su come funziona la visibilità, consulta le [documentazioni API](https://console.bluemix.net/apidocs/682).
