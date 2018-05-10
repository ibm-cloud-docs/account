---

copyright:

  years: 2015, 2018
lastupdated: "2018-03-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Tipi di account
{: #accounts}

Puoi iniziare a creare su {{site.data.keyword.Bluemix}} gratuitamente. Abbiamo tre diversi tipi di account tra cui puoi scegliere: Lite, Pagamento a consumo e Sottoscrizione. Puoi utilizzare qualsiasi tipo di account per iniziare a utilizzare {{site.data.keyword.Bluemix_notm}} - scegli semplicemente quello più adatto alle tue esigenze.
{:shortdesc}

## Confronto degli account
{: #compare}

La seguente tabella fornisce un confronto degli account Lite, Pagamento a consumo e Sottoscrizione. Per ulteriori dettagli su ciascun account, vedi le sezioni che seguono.

|  | Lite  | Pagamento a consumo | Sottoscrizione |
|--------------------|--------------------|--------------------|--------------------|
| **Accesso alla memoria Cloud Foundry gratuita** | 256 MB | 512 MB | 512 MB |
| **Accesso ai [piani di servizio Lite ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://console.bluemix.net/catalog/?search=label:lite){: new_window}** | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Accesso a tutti i piani gratuiti** |  | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Accesso al catalogo completo** |  | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Accesso a più regioni Cloud Foundry** |  | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Nessun limite di tempo** | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Costo zero garantito** | ![Funzione disponibile](../icons/icon_enabled.svg) |  |  |
| **Prezzo negoziato** |  |  | ![Funzione disponibile](../icons/icon_enabled.svg) |
| **Ideale per l'apprendimento o la creazione di POC** | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |  |
| **Adatto per i casi di utilizzo di produzione** |  | ![Funzione disponibile](../icons/icon_enabled.svg) | ![Funzione disponibile](../icons/icon_enabled.svg) |
{: caption="Tabella 1. Confronto degli account {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Account Lite
{: #liteaccount}

Registrati per un account Lite gratuito per creare applicazioni ed esplorare servizi con piani gratuiti selezionati che sono denominati Lite e visualizzati con una tag Lite ![Tag Lite](../icons/Lite.svg) nella console {{site.data.keyword.Bluemix_notm}}. Il tuo account Lite non scade e non è richiesta la tua carta di credito.

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

## Account fatturabili
{: #billableacts}

La seguente tabella elenca i diversi tipi di account e i relativi tipi di addebito.

|Tipo di account |	Modalità di addebito |
|------------------|-----------------------|
|Pagamento a consumo |	Gli addebiti si basano sull'utilizzo che fai di elaborazione e servizi {{site.data.keyword.Bluemix_notm}} |
|Sottoscrizione | Puoi ottenere uno sconto mensile basato su un impegno di spesa mensile minimo. |
| {{site.data.keyword.Bluemix_dedicated_notm}} | Contratto annuale |
|{{site.data.keyword.Bluemix_local_notm}} |	Contratto annuale |
{:caption="Tabella 2. Account fatturabili {{site.data.keyword.Bluemix_notm}} e addebiti" caption-side="top"}

Se colleghi il tuo account fatturabile {{site.data.keyword.Bluemix_notm}} con un account SoftLayer, a partire dal primo giorno del mese successivo, gli addebiti combinati vengono inclusi nella tua fattura {{site.data.keyword.Bluemix_notm}}. Per ulteriori informazioni, vedi [Visualizzazione dei crediti](/docs/billing-usage/viewing_usage.html#credits).
{: tip}

### Account Pagamento a consumo

Con un account Pagamento a consumo, puoi creare più gruppi di risorse per gestire facilmente la quota e visualizzare l'utilizzo della fatturazione per un insieme di risorse. Hai diritto a franchigie per i runtime e i servizi. Se superi la franchigia consentita, riceverai una fattura mensile da parte di {{site.data.keyword.Bluemix_notm}}. La fattura sarà in dollari americani (USD) e verranno descritti gli addebiti delle risorse.

In molti paesi e regioni, puoi registrarti per un account Pagamento a consumo dalla console {{site.data.keyword.Bluemix_notm}}. Una volta che hai fornito le informazioni per la fatturazione e quelle relative alla tua carta di credito, accetta i termini e le condizioni e inoltra la richiesta di account. La tua carta di credito verrà quindi convalidata. Riceverai anche un'e-mail di conferma relativa alle informazioni dell'account. Qualche minuto dopo aver ricevuto l'e-mail di conferma, puoi tornare alla console per continuare a creare le tue applicazioni. 

Se non è possibile elaborare la tua richiesta online per il tuo paese o la tua regione, contatta il [Supporto {{site.data.keyword.Bluemix_notm}} ](https://ibm.biz/bluemixsupport){: new_window} ![Icona link esterno](../icons/launch-glyph.svg). Dopo aver eseguito l'accesso al portale del servizio {{site.data.keyword.Bluemix_notm}}, fai clic su **Contatta il supporto** e seleziona l'opzione **Fatturazione, Account o Accesso**.

Puoi convertire il tuo account Pagamento a consumo in un account Sottoscrizione in qualsiasi momento. Per ulteriori dettagli, contatta il settore [Vendite di {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg).
{: tip}

### Account Sottoscrizione

Con un account Sottoscrizione, puoi creare più gruppi di risorse per gestire facilmente la quota e visualizzare l'utilizzo della fatturazione per un insieme di risorse.

Ti impegni a un importo di spesa minimo ogni mese e ricevi uno sconto sulla sottoscrizione che viene applicato a tale addebito minimo. Puoi anche pagare per qualsiasi
utilizzo che ecceda l'importo di spesa minimo.

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

## Account di prova
{: #trial}

Gli account di prova sono disponibili in tutte le regioni. Con una prova gratuita di 30 giorni, puoi iniziare subito a creare le tue applicazioni e ad esplorare i servizi in {{site.data.keyword.Bluemix_notm}}.

Quando ti registri per una versione di prova gratuita con il tuo ID {{site.data.keyword.Bluemix_notm}}, al tuo account vengono fornite gratuitamente le seguenti risorse:

  * Un massimo di 2 GB di memoria
  * 10 servizi
  * 1 certificato SSL

Hai anche accesso a un singolo gruppo di risorse creato per te e denominato `Default`. Tutte le tue istanze del servizio gestito da IAM vengono aggiunte automaticamente a questo gruppo di risorse. Puoi aggiornare il nome di questo gruppo di risorse in qualsiasi momento. Per la procedura dettagliata, vedi [Ridenominazione di un gruppo di risorse](/docs/account/resourcegroups.html#renaming-a-resource-group).

Ogni gruppo di risorse è gratuito. Quando crei una connessione tra un servizio gestito da IAM e un'applicazione Cloud Foundry, crei un alias, che è un'istanza del servizio, che viene conteggiato nella tua quota. Vedi [Cos'è un alias?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

### Cosa succede al termine della prova gratuita?
{: #trialend}

Quando la prova gratuita scade 30 giorni dopo la tua registrazione, le applicazioni nel tuo account vengono arrestate. Non puoi registrarti per un altro account {{site.data.keyword.Bluemix_notm}}, ma puoi ancora accedere al tuo account e a tutti gli account ai quali sei invitato.

Per riavviare le tue applicazioni, converti il tuo account in un account fatturabile fornendo le informazioni della tua carta di credito per un account Pagamento a consumo o creando un account Sottoscrizione. Dopo, puoi continuare a utilizzare le franchigie relative a elaborazione e servizi. Paghi solo per l'utilizzo di servizi, contenitori e runtime non incluso nella tua franchigia mensile.

  * Per eseguire l'aggiornamento a un account Pagamento a consumo, nella console vai a **Gestisci** > **Fatturazione e utilizzo** > **Fatturazione** e fai clic su **Aggiungi carta di credito**.
  * Per registrare un account Sottoscrizione, contatta il settore [Vendite di {{site.data.keyword.Bluemix_notm}} ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icona link esterno](../icons/launch-glyph.svg).

Se non converti il tuo account dopo la scadenza della versione di prova gratuita, le tue applicazioni e i tuoi servizi verranno rimossi dopo 30 giorni. Tuttavia, il tuo account non viene eliminato e puoi effettuare l'accesso e l'aggiornamento a un account fatturabile in qualsiasi momento. Inoltre, riceverai delle notifiche e-mail per ricordarti di creare un account fatturabile ed evitare di perdere le tue impostazioni dell'applicazione e configurazioni del servizio. Se preferisci non ricevere le notifiche da {{site.data.keyword.Bluemix_notm}}, puoi annullare la sottoscrizione in qualsiasi momento.

Se converti il tuo account, le tue franchigie sono limitate a quelle normalmente fornite da ciascun servizio. Le franchigie non sono più quelle di utilizzo illimitato offerte da molti dei servizi IBM durante la versione di prova gratuita.

