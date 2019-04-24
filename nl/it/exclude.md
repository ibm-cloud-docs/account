---

copyright:

  years: 2017, 2019
lastupdated: "2019-01-28"

keywords: hide resource, limit viewer, exclude user, hide service

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}


# Nascondimento di una risorsa pubblica agli utenti
{: #exclude}

In qualità di amministratore per il tuo account {{site.data.keyword.Bluemix}}, puoi nascondere una risorsa pubblica agli utenti che hanno accesso all'account. Potresti nascondere le risorse per tenere nascoste agli utenti non autorizzati delle informazioni sensibili oppure potrebbero esserci delle informazioni a cui deve poter accedere solo un numero limitato di persone.
{:shortdesc}

Nascondere una risorsa nel catalogo non la rimuove dalla CLI Cloud Foundry o dall'elenco delle categorie dell'offerta disponibile dalla navigazione della console {{site.data.keyword.Bluemix_notm}}, come Elemento finanziario, Mobile, Watson e Applicazioni Web.
{: note}

Puoi utilizzare l'{{site.data.keyword.Bluemix}} [interfaccia riga di comando (CLI, command-line interface)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) o la console per determinare se disponi dell'accesso per consentire agli utenti di visualizzare una risorsa privata che era stata aggiunta all'account. Se sei un proprietario di account, puoi concedere l'accesso a un utente nel tuo account dalla console assegnando una politica di accesso. Per ulteriori informazioni, vedi [Gestione dell'accesso al tuo account](/docs/account?topic=account-find-access).

## Individuazione di una risorsa
{: #find-resource-exc}

Per cercare una risorsa, esegui il comando `ibmcloud catalog search <service-id or service-name>`. Sostituisci le variabili service-id o service-name con un nome o un ID risorsa. Utilizza le informazioni restituite per trovare l'ID o il nome del servizio che vuoi nascondere.

## Ottenimento dei dettagli della risorsa

Esegui `ibmcloud catalog service <service-id or service-name>`. Utilizzando le informazioni restituite dall'esecuzione del comando precedente, utilizza questo comando per esaminare ulteriori dettagli sulla risorsa. Con le informazioni restituite, puoi visualizzare la gerarchia, che mostra le risorse secondarie degli elementi nella tua risorsa.

## Nascondimento della risorsa
{: #vis-exc}

Esegui il seguente comando per impedire agli utenti nel tuo account di visualizzare una risorsa pubblica.

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

Puoi aggiungere un elenco separato da virgole di email o ID account associati agli account dopo l'indicatore excludes.

Dopo che hai eseguito il comando, il processo per nascondere la risorsa impiega circa 30 minuti. Dopo 30 minuti, scollegati ed esegui nuovamente l'accesso al tuo account per vedere la risorsa nascosta.

Gli elementi che nascondi non sono disponibili dalla console o dalla CLI. Gli amministratori dell'account escluso possono ancora vedere la risorsa.
{: note}

## Rimozione di un account dall'elenco di esclusione
{: #remove-exclude}

Esegui il seguente comando per rimuovere un ID account o una email dall'elenco di esclusione.

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`


## Esempio: gestione della visibilità degli oggetti secondari
{: #child}

Puoi gestire la visibilità di tutte le tue risorse. Ogni risorsa secondaria ha le sue singole caratteristiche di visibilità. Questo esempio mostra come è possibile escludere un account dal servizio Cloudant.

Esegui il comando `ibmcloud catalog service cloudant` per visualizzare tutti gli elementi secondari della risorsa.

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

Trova l'ID per un oggetto ed escludi un account eseguendo il comando `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

Per ulteriori informazioni su come funziona la visibilità, consulta la [documentazione sulle API del catalogo](https://{DomainName}/apidocs/globalcatalog).
