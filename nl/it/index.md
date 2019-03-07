---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-13"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Tipi di account
{: #accounts}

{{site.data.keyword.Bluemix_notm}} ha tre diversi tipi di account: Lite, Pagamento a consumo e Sottoscrizione. Ottieni un account Lite gratuito appena esegui la registrazione. Pagamento a consumo e Sottoscrizione sono le nostre opzioni di account fatturabili; ciascuna offerta mette a disposizione delle funzioni diverse. Confronta ciascun account e scegli quello che risponde meglio alle tue esigenze.
{:shortdesc}


## Confronto degli account
{: #compare}

La seguente tabella fornisce un confronto degli account Lite, Pagamento a consumo e Sottoscrizione. Per ulteriori dettagli su ciascun account, vedi le sezioni che seguono.

|                                         | Lite               | Pagamento a consumo      | Sottoscrizione       |
|-----------------------------------------|--------------------|--------------------|--------------------|
| **Accesso alla memoria Cloud Foundry gratuita** | 256 MB             | 512 MB             | 512 MB             |
| **Accesso ai [piani di servizio Lite ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://{DomainName}/catalog/?search=label:lite){: new_window}** | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Accesso a tutti i piani gratuiti**            |                    | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Accesso al catalogo {{site.data.keyword.Bluemix_notm}} completo** |  | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Accesso a più regioni Cloud Foundry** |               | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Nessun limite di tempo** | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Costo zero garantito**                | ![Funzione disponibile](../icons/icon_enabled.svg) |  |         |
| **Prezzo scontato**                  |                    |                    | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Ideale per l'apprendimento o la creazione di POC (Proof of Concept)** | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |  |
| **Adatto per i casi di utilizzo di produzione**        |                    | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
{: caption="Tabella 1. Confronto degli account {{site.data.keyword.Bluemix_notm}}" caption-side="top"}


## Account Lite
{: #liteaccount}

Registrati per un account Lite per iniziare a creare le tue applicazioni ed esplorare i servizi con esclusivi piani Lite gratuiti, che vengono visualizzati con una tag Lite ![Tag Lite](../icons/Lite.svg) nella console {{site.data.keyword.Bluemix_notm}}. Il tuo account Lite non scade e non è richiesta la tua carta di credito.

Hai accesso a un singolo gruppo di risorse creato per te e denominato `Default`. Tutte le tue istanze del servizio gestite da {{site.data.keyword.Bluemix_notm}} IAM (Identity and Access Management) vengono aggiunte automaticamente a questo gruppo di risorse. Puoi aggiornare il nome di questo gruppo di risorse in qualsiasi momento. Per la procedura dettagliata, vedi [Ridenominazione di un gruppo di risorse](/docs/resources?topic=resources-rgs#rename_rgs).

Ogni gruppo di risorse è gratuito. Quando crei una connessione tra un servizio gestito da IAM e un'applicazione Cloud Foundry, crei un alias, che è un'istanza del servizio, che viene conteggiato nella tua quota. Vedi [Gestione delle connessioni](/docs/resources?topic=resources-connect_app).
{: tip}

### Disponibilità
{: #lite-account-features}

Controlla il seguente elenco di funzioni chiave disponibili in un account Lite:

   * L'account è gratuito - non è richiesta una carta di credito.
   * L'account non scade mai.
   * Puoi utilizzare una sola organizzazione in una regione {{site.data.keyword.Bluemix_notm}}.
   * Supporto {{site.data.keyword.Bluemix_notm}} di base gratuito. Il supporto di base viene fornito per ambienti non di produzione o carichi di lavoro in cui non vengono utilizzate le severità tradizionali e non sono previsti specifici tempi di risposta.
   * Ricevi notifiche e-mail relative allo stato del tuo account e ai limiti di quota.
   * Le tue applicazioni Cloud Foundry possono accedere fino a 256 MB di memoria di runtime istantanea gratuita.
   * Puoi eseguire il provisioning di una singola istanza di qualsiasi servizio nel [catalogo {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} che dispone di un piano Lite.
   * Dopo 10 giorni senza attività di sviluppo, le tue applicazioni vengono sospese. Puoi ora attivare le tue applicazioni continuando a lavorare su di esse.
   * Dopo 30 giorni senza attività di sviluppo, le tue istanze del servizio con i piani Lite vengono eliminate.

### Upgrade del tuo account Lite
{: #upgrade-lite-account}

Puoi eseguire l'upgrade a un account Pagamento a consumo o Sottoscrizione. Per ulteriori informazioni, vedi [Come eseguo l'upgrade o la conversione del mio tipo di account?](/docs/account?topic=account-changeacct).

Dopo aver eseguito l'upgrade a un account Pagamento a consumo ottieni un credito promozionale di $200 che viene automaticamente applicato al tuo account. Il tuo credito di $200 è valido per 30 giorni e viene applicato automaticamente alla tua fattura. Il credito non può essere utilizzato con le offerte di terze parti.

## Account Pagamento a consumo
{: #paygo}

Con un account Pagamento a consumo, puoi creare più gruppi di risorse per gestire facilmente la quota e visualizzare l'utilizzo della fatturazione per un insieme di risorse. Gli addebiti a tuo carico si basano sul tuo utilizzo di capacità di calcolo e servizi {{site.data.keyword.Bluemix_notm}}. Hai diritto a franchigie per i runtime e i servizi. Se superi la franchigia prevista, ricevi una fattura mensile da parte di {{site.data.keyword.Bluemix_notm}}. La fattura è in dollari americani (USD) e fornisce dettagli sui costi delle risorse.

Inoltre, con un account Pagamento a consumo, puoi ordinare elementi facoltativi quali le opzioni di supporto avanzate o premium. Per ulteriori informazioni, contatta il settore [Vendite di {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg).


### Upgrade del tuo account Pagamento a consumo
{: #upgrade-to-subscription}

Per eseguire l'upgrade del tuo account Pagamento a consumo a un account Sottoscrizione, contatta il settore [Vendite di {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno").

## Account Sottoscrizione
{: #subscription-account}

Con un account Sottoscrizione, puoi creare più gruppi di risorse per gestire facilmente la quota e visualizzare l'utilizzo della fatturazione per un insieme di risorse. Ti impegni a un importo di spesa minimo combinato ogni mese e ricevi uno sconto sulla sottoscrizione che viene applicato a tale addebito minimo. Ti viene addebitata la tariffa non scontata per l'utilizzo che supera la quantità totale della tua Sottoscrizione. Per visualizzare la tua sottoscrizione, vai a **Gestisci > Fatturazione e utilizzo** e seleziona **Sottoscrizioni**.

Se hai un account Sottoscrizione, puoi creare la maggior parte dei servizi disponibili dal [catalogo {{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com/catalog/){: new_window} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno"). Tuttavia, alcuni servizi utilizzano un piano dei prezzi specifico che ti richiede di effettuarne l'acquisto separatamente.

### Account {{site.data.keyword.Bluemix_dedicated_notm}}
Con {{site.data.keyword.Bluemix_dedicated_notm}}, devi registrarti per un periodo minimo di un anno che include:

   * Connettività VPN alla tua infrastruttura
   * Ambiente totalmente ridondante in un data center {{site.data.keyword.BluSoftlayer_notm}}
   * Tutti i runtime supportati ({{site.data.keyword.runtime_liberty_short}}, {{site.data.keyword.runtime_nodejs_short}} e runtime open source integrati)
   * Tutti i servizi dedicati da te selezionati e tutti i servizi {{site.data.keyword.Bluemix_notm}} pubblici
   * Supporto {{site.data.keyword.Bluemix_notm}} standard

Puoi anche ordinare elementi facoltativi quali {{site.data.keyword.BluDirectLink}} oppure le opzioni di supporto avanzate o premium. Per ulteriori informazioni, contatta il settore [Vendite di {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg).

Quello che paghi ogni mese durante questo periodo si basa sui servizi dedicati che desideri, oltre a un account Sottoscrizione che ti dà accesso a tutti i servizi pubblici. Gli addebiti di utilizzo dei servizi in {{site.data.keyword.Bluemix_notm}} pubblico sono calcolati in base all'accordo del tuo account di sottoscrizione. Ricevi una fattura per tutti i servizi che utilizzi
oltre i limiti previsti da tale accordo di sottoscrizione. Contatta il tuo rappresentante dell'account designato IBM oppure il settore [Vendite di {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg) per un'introduzione al tuo accordo.
