---

copyright:

  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Come nascondere una risorsa pubblica agli utenti nel tuo account
{: #exclude}

Se sei un amministratore dell'account, puoi scegliere di nascondere una risorsa pubblica per tutti gli utenti nel tuo account aggiungendoli a un elenco di esclusione attraverso l'[interfaccia riga di comando](/docs/cli/reference/bluemix_cli/bx_cli.html#ibmcloud_catalog_entry_visibility_set) `ibmcloud`.
{:shortdesc: .shortdesc}

**Nota:** se si nasconde un elemento nel catalogo questo non verrà rimosso dalla CLI di Cloud Foundry o dagli elenchi di provisioning del servizio disponibili tramite la navigazione globale, ad esempio Elemento finanziario, Mobile, Watson e Applicazioni Web.

## Come faccio a sapere se dispongo dell'accesso?
{: #find-access}

Puoi utilizzare la CLI o l'interfaccia utente di Identità e accesso per determinare se disponi dell'accesso per consentire agli utenti di visualizzare una risorsa privata che è stata aggiunta all'account. Se sei un proprietario di account, puoi concedere l'accesso a un utente nel tuo account tramite l'interfaccia utente di Identity and Access Management assegnando una politica di accesso. Per ulteriori informazioni, vedi [Gestione dell'accesso al tuo account](access.html).

## Passo 1: trova una risorsa
{: #find-resource}

Immetti `ibmcloud catalog search <service-id or service-name>` per cercare una risorsa. Sostituisci service-id o service-name con un nome o un ID risorsa. Trova l'ID o il nome del servizio che desideri nascondere nelle informazioni che vengono restituite.

## Passo 2: ottieni i dettagli di quel servizio

Immetti `ibmcloud catalog service <service-id or service-name>`. Utilizzando ciò che hai trovato nel comando precedente, usa questo comando per esaminare maggiori dettagli della risorsa. Con le informazioni restituite, puoi visualizzare la gerarchia, che mostra le risorse secondarie degli elementi nella risorsa.

## Passo 3: nascondi la risorsa
{: #vis-exc}

Immetti il seguente comando per impedire al tuo account di visualizzare una risorsa pubblica.

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

Dopo l'indicatore excludes, puoi aggiungere un elenco separato da virgole di e-mail o ID account associati agli account.

Una volta eseguito il comando, il processo per nascondere la risorsa richiede 30 minuti. Dopo 30 minuti, scollegati e torna al tuo account per vedere la risorsa nascosta.

**Nota:** le voci che nascondi non sono disponibili dall'interfaccia utente e dalla CLI ibmcloud. Le voci nascoste sono ancora visibili nel marketplace di Cloud Foundry, ma un piano nascosto non può essere fornito da Cloud Foundry. Gli amministratori dell'account escluso possono ancora vedere la risorsa.

## Rimuovi un account dall'elenco di esclusione
{: #remove-exclude}

Immetti il seguente comando per rimuovere un ID account o e-mail dall'elenco di esclusione.

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`

## Gestione della visibilità di oggetti secondari di esempio
{: #child}

Puoi gestire la visibilità di tutte le tue risorse. Ogni risorsa secondaria ha le sue singole caratteristiche di visibilità.

In questo esempio, puoi escludere un account dal servizio pubblico di Cloudant.

Se immetti `ibmcloud catalog service cloudant`, puoi vedere gli elementi secondari della risorsa.

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

Trova l'ID per un oggetto ed escludi un account con `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

Per ulteriori informazioni su come funziona la visibilità, consulta le [documentazioni API](https://console.bluemix.net/apidocs/682).
