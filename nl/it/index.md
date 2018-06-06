---

copyright:

  years: 2015, 2018
lastupdated: "2018-05-25"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Tipi di account
{: #accounts}

Puoi scegliere tra tre tipi di account {{site.data.keyword.Bluemix}}: Lite, Pagamento a consumo e Sottoscrizione. Puoi utilizzare qualsiasi tipo di account per iniziare a utilizzare {{site.data.keyword.Bluemix_notm}} - scegli semplicemente quello più adatto alle tue esigenze.
{:shortdesc}

## Confronto degli account
{: #compare}

La seguente tabella fornisce un confronto degli account Lite, Pagamento a consumo e Sottoscrizione. Per ulteriori dettagli su ciascun account, vedi le sezioni che seguono.

|  | Lite  | Pagamento a consumo | Sottoscrizione |
|--------------------|--------------------|--------------------|--------------------|
| **Accesso alla memoria Cloud Foundry gratuita** | 256 MB | 512 MB | 512 MB |
| **Accesso ai [piani di servizio Lite ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/catalog/?search=label:lite){: new_window}** | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Accesso a tutti i piani gratuiti** |  | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Accesso al catalogo {{site.data.keyword.Bluemix_notm}} completo** |  | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Accesso a più regioni Cloud Foundry** |  | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Nessun limite di tempo** | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Costo zero garantito** | ![Funzione disponibile](../icons/icon_enabled.svg) |  |  |
| **Prezzo scontato** |  |  | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Ideale per l'apprendimento o la creazione di POC (Proof of Concept)** | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |  |
| **Adatto per i casi di utilizzo di produzione** |  | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
{: caption="Tabella 1. Confronto degli account {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Account Lite
{: #liteaccount}

Registrati per un account Lite per iniziare a creare le tue applicazioni ed esplorare i servizi con esclusivi piani Lite gratuiti, che vengono visualizzati con una tag Lite ![Tag Lite](../icons/Lite.svg) nella console {{site.data.keyword.Bluemix_notm}}. Il tuo account Lite non scade e non è richiesta la tua carta di credito.

Hai accesso a un singolo gruppo di risorse creato per te e denominato `Default`. Tutte le tue istanze dei servizi gestite da {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) vengono aggiunte automaticamente a questo gruppo di risorse. Puoi aggiornare il nome di questo gruppo di risorse in qualsiasi momento. Per la procedura dettagliata, vedi [Ridenominazione di un gruppo di risorse](/docs/account/resourcegroups.html#renaming-a-resource-group).

Ogni gruppo di risorse è gratuito. Quando crei una connessione tra un servizio gestito da IAM e un'applicazione Cloud Foundry, crei un alias, che è un'istanza del servizio, che viene conteggiato nella tua quota. Vedi [Cos'è un alias?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

### Disponibilità

Potresti chiederti cosa offra un account Lite. Controlla il seguente elenco di funzioni principali:

   * L'account è gratuito - non è richiesta una carta di credito.
   * L'account non scade mai.
   * Puoi utilizzare una sola organizzazione in una regione {{site.data.keyword.Bluemix_notm}}.
   * Supporto {{site.data.keyword.Bluemix_notm}} di base gratuito. Il supporto di base viene fornito per ambienti non di produzione o carichi di lavoro in cui non vengono utilizzate le severità tradizionali e non sono previsti specifici tempi di risposta.
   * Ricevi notifiche e-mail relative allo stato del tuo account e ai limiti di quota.
   * Le tue applicazioni Cloud Foundry possono accedere fino a 256 MB di memoria di runtime istantanea gratuita.
   * Puoi eseguire il provisioning di un'istanza di qualsiasi servizio nel [catalogo {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window} che dispone di un piano Lite.
   * Dopo 10 giorni senza attività di sviluppo, le tue applicazioni vengono sospese. Puoi iniziare a lavorare su nuove applicazioni senza doverti preoccupare di superare i limiti di quota della memoria.
   * Dopo 30 giorni senza attività di sviluppo, le tue istanze del servizio con i piani Lite vengono eliminate. In questo modo, non devi gestire l'eliminazione di istanze inattive prima di crearne di nuove.

### Aggiornamento del tuo account

Quando sei pronto a passare alla fase successiva, esegui l'aggiornamento a un account Pagamento a consumo e paga solo per ciò che usi oltre le franchigie. Dopo aver eseguito l'upgrade, puoi continuare a utilizzare tutte le istanze che hai creato con il tuo account Lite. Nella console, vai a **Gestisci** > **Fatturazione e utilizzo** > **Fatturazione** e fai clic su **Aggiungi carta di credito**.

## Account Pagamento a consumo
{: #paygo}

Con un account Pagamento a consumo, puoi creare più gruppi di risorse per gestire facilmente la quota e visualizzare l'utilizzo della fatturazione per un insieme di risorse. Gli addebiti a tuo carico si basano sul tuo utilizzo di elaborazione e servizi {{site.data.keyword.Bluemix_notm}}. Hai diritto a franchigie per i runtime e i servizi. Se superi la franchigia prevista, ricevi una fattura mensile da parte di {{site.data.keyword.Bluemix_notm}}. La fattura è in dollari americani (USD) e fornisce dettagli sui costi delle risorse.

Se colleghi il tuo account Pagamento a consumo a un account SoftLayer, a partire dal primo giorno del mese successivo, gli addebiti combinati vengono inclusi nella tua fattura {{site.data.keyword.Bluemix_notm}}.
{: tip}

Puoi eseguire l'aggiornamento a un account Pagamento a consumo dalla console {{site.data.keyword.Bluemix_notm}}. Dopo aver fornito le informazioni di fatturazione e carta di credito, accetta i termini e le condizioni e invia la richiesta di account. La tua carta di credito viene quindi convalidata. Ricevi anche un'e-mail di conferma in merito alle informazioni sull'account. Qualche minuto dopo aver ricevuto l'e-mail di conferma, puoi tornare alla console per continuare a creare le tue applicazioni. Se non è possibile elaborare la tua richiesta online per il tuo paese o la tua regione, contatta il [Supporto {{site.data.keyword.Bluemix_notm}}](/docs/get-support/howtogetsupport.html).

Dopo aver eseguito l'aggiornamento a un account Pagamento a consumo ottieni un credito promozionale di $200 e non dovrai eseguire alcuna operazione per iniziare a utilizzarlo. Il tuo credito di $200 è valido per 30 giorni e viene applicato automaticamente alla tua fattura. Il credito non può essere utilizzato con le offerte dell'infrastruttura o di terze parti.

### Aggiornamento del tuo account

Puoi aggiornare il tuo account Pagamento a consumo a un account Sottoscrizione in qualsiasi momento. Per ulteriori dettagli, contatta il settore [Vendite di {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg).

## Account Sottoscrizione

Con un account Sottoscrizione, puoi creare più gruppi di risorse per gestire facilmente la quota e visualizzare l'utilizzo della fatturazione per un insieme di risorse. Ti impegni a un importo di spesa minimo ogni mese e ricevi uno sconto sulla sottoscrizione che viene applicato a tale addebito minimo. Puoi anche pagare per qualsiasi
utilizzo che ecceda l'importo di spesa minimo.

Se colleghi il tuo account Sottoscrizione a un account SoftLayer, a partire dal primo giorno del mese successivo, gli addebiti combinati vengono inclusi nella tua fattura {{site.data.keyword.Bluemix_notm}}.
{: tip}

Per registrare un account Sottoscrizione e per ulteriori informazioni sulle tariffe di sottoscrizione e sugli sconti, devi contattare il settore [Vendite di {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg)

### Account {{site.data.keyword.Bluemix_dedicated_notm}}

Con {{site.data.keyword.Bluemix_dedicated_notm}}, devi registrarti per un periodo minimo di un anno che include:

   * Connettività VPN alla tua infrastruttura
   * Ambiente totalmente ridondante in un data center {{site.data.keyword.BluSoftLayer_notm}}
   * Tutti i runtime supportati (IBM Java Liberty, Node.js e runtime open source integrati)
   * Tutti i servizi dedicati da te selezionati e tutti i servizi {{site.data.keyword.Bluemix_notm}} pubblici
   * Supporto {{site.data.keyword.Bluemix_notm}} standard

Puoi anche ordinare elementi facoltativi quali SoftLayer DirectLink oppure opzioni di supporto premium. Per ulteriori informazioni, contatta il settore [Vendite di {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg).

Quello che paghi ogni mese durante questo periodo si basa sui servizi dedicati che desideri, oltre a un account Sottoscrizione che ti dà accesso a tutti i servizi pubblici. Gli addebiti di utilizzo dei servizi in {{site.data.keyword.Bluemix_notm}} pubblico sono calcolati in base all'accordo del tuo account di sottoscrizione. Ricevi una fattura per tutti i servizi che utilizzi
oltre i limiti previsti da tale accordo di sottoscrizione. Contatta il tuo rappresentante dell'account designato IBM oppure il settore [Vendite di {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg) per un'introduzione al tuo accordo.

### Account {{site.data.keyword.Bluemix_local_notm}}

Con {{site.data.keyword.Bluemix_local_notm}}, devi registrarti per un periodo minimo di un anno che include:

   * Una capacità di consegna denominata Relay che consente a IBM di connettersi alla tua distribuzione locale e
di fornire automaticamente e costantemente gli aggiornamenti
   * Tutti i runtime supportati (IBM Java Liberty, Node.js e runtime open source integrati)
   * Tutti i servizi locali da te selezionati e l'accesso a tutti i servizi {{site.data.keyword.Bluemix_notm}} pubblici
   * Supporto {{site.data.keyword.Bluemix_notm}} standard

Quello che paghi ogni mese durante questo periodo si basa sui servizi locali che desideri, oltre a un account Sottoscrizione che ti dà accesso a tutti i servizi pubblici. Gli addebiti di utilizzo dei servizi in {{site.data.keyword.Bluemix_notm}} pubblico sono calcolati in base all'accordo del tuo account di sottoscrizione. Ricevi una fattura per tutti i servizi che utilizzi
oltre i limiti previsti da tale accordo di sottoscrizione. Contatta il tuo rappresentante dell'account designato IBM oppure il settore [Vendite di {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg) per un'introduzione al tuo accordo.

