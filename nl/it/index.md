---

copyright:
  years: 2015, 2019
lastupdated: "2019-08-02"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account, subscription, service bundle

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:row-headers: .row-headers}

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
{: row-headers}
{: class="comparison-table"}
{: caption="Tabella 1. Confronto degli account {{site.data.keyword.Bluemix_notm}}" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the feature. The column headers identify the account type. To understand which features apply to the account types, navigate to the row, and find the feature that you're interested in."}

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
   * Le tue applicazioni Cloud Foundry possono accedere fino a 256 MB di memoria di runtime istantanea gratuita al mese.
   * Puoi eseguire il provisioning di una singola istanza di qualsiasi servizio nel [catalogo {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} che dispone di un piano Lite.
   * Dopo 10 giorni senza attività di sviluppo, le tue applicazioni vengono sospese. Puoi ora attivare le tue applicazioni continuando a lavorare su di esse.
   * Dopo 30 giorni senza attività di sviluppo, le tue istanze del servizio con i piani Lite vengono eliminate.

## Account Pagamento a consumo
{: #paygo}

Con un account Pagamento a consumo, puoi accedere all'intero catalogo di {{site.data.keyword.Bluemix_notm}}, inclusi tutti i piani gratuiti e ottenere il doppio della memoria di runtime gratuita a 512 MB al mese. Paghi solo i servizi fatturabili che utilizzi, senza impegni o contratti a lungo termine. Quando esegui l'upgrade a un account Pagamento a consumo, ricevi un [credito di $200](#upgrade-lite-account) per aiutarti a iniziare a lavorare.

Puoi creare più gruppi di risorse per gestire facilmente la quota e visualizzare l'utilizzo della fatturazione per un insieme di risorse. Gli addebiti a tuo carico si basano sul tuo utilizzo di capacità di calcolo e servizi {{site.data.keyword.Bluemix_notm}}. Se superi le franchigie per runtime e servizi gratuite, ricevi una fattura mensile che ti fornisce i dettagli sui tuoi costi delle risorse.

Inoltre, con un account Pagamento a consumo, puoi ordinare dei piani di supporto premium o avanzato per ottenere un ulteriore aiuto con i tuoi carichi di lavoro di produzione. Ulteriori informazioni in [Piani di supporto](/docs/get-support?topic=get-support-support-plans).

## Account Sottoscrizione
{: #subscription-account}

Con un account Sottoscrizione, puoi creare più gruppi di risorse per gestire facilmente la quota e visualizzare l'utilizzo della fatturazione per un insieme di risorse. Ti impegni a un importo di spesa minimo ogni mese e ricevi uno sconto sulla sottoscrizione che viene applicato a tale addebito minimo.

Ad esempio, se ti impegni a spendere $100 al mese per 6 mesi, puoi avere uno sconto del 10% . Durante il periodo di sottoscrizione, hai $600 di utilizzo ma paghi solo $540. Più lungo è il termine di sottoscrizione, migliore è lo sconto.

Il tuo utilizzo viene dedotto dalla tua quantità di sottoscrizione totale. Anche se il tuo utilizzo varia da mese a mese, puoi ottenere una fatturazione coerente e prevedibile. Se il tuo utilizzo supera la tua quantità di sottoscrizione totale, ti sarà fatto un addebito della tariffa non scontata per l'eccedenza.

Come con gli account Pagamento a consumo, il tuo account Sottoscrizione ti consente di ordinare piani di supporto premium o avanzato per avere un ulteriore aiuto se ne hai bisogno. Ulteriori informazioni in [Piani di supporto](/docs/get-support?topic=get-support-support-plans).

Se hai un account Sottoscrizione, puoi creare la maggior parte dei servizi disponibili dal [catalogo {{site.data.keyword.Bluemix_notm}}](https://{DomainName}/catalog){: new_window} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno"). Tuttavia, alcuni servizi utilizzano un piano dei prezzi specifico che ti richiede di effettuarne l'acquisto separatamente.

### Sottoscrizioni al bundle di servizi
{: #service-subscriptions}

Le sottoscrizioni al bundle di servizi ti forniscono l'accesso e il credito per una serie di servizi in un determinato dominio destinati a casi di utilizzo popolari. Puoi scegliere dai bundle di servizi che comprendono i servizi IA, analisi, {{site.data.keyword.blockchainfull_notm}}, Internet of Things (IoT) e nativi cloud. Se le tue esigenze spaziano tra più domini, puoi acquistare più sottoscrizioni di bundle di servizi.

Puoi aggiungere i bundle di servizi a qualsiasi tipo di account esistente, inclusi gli account Lite. Per i primi 90 giorni, sei limitato all'utilizzo dei servizi all'interno del bundle. Dopo i 90 giorni iniziali, puoi accedere al catalogo completo. Le sottoscrizioni al bundle di servizi sono soggette ai termini della [Descrizione del servizio {{site.data.keyword.Bluemix_notm}}](/docs/overview/terms-of-use?topic=overview-terms).

Le sottoscrizioni al bundle di servizi non sono disponibili tramite la console {{site.data.keyword.Bluemix_notm}}. Per ulteriori informazioni e l'acquisto di un bundle di servizi, contatta il settore [Vendite {{site.data.keyword.Bluemix_notm}} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}.
{:tip}

Dopo aver acquistato una sottoscrizione al bundle di servizi, riceverai un'email con un codice sottoscrizione che devi applicare per aggiungere il bundle al tuo account. Per ulteriori informazioni su come applicare i codici sottoscrizione, vedi [Gestione delle sottoscrizioni](/docs/billing-usage?topic=billing-usage-subscriptions). Quando il tuo bundle di servizi scade o utilizzi tutto il credito, puoi continuare ad utilizzare tutti i servizi, con l'utilizzo addebitato alla tariffa di pagamento a consumo.

## Upgrade del tuo account
{: #upgrade-lite-account}

Quando sei pronto per portare il tuo account al prossimo livello, puoi [eseguire l'upgrade di un account Lite](/docs/account?topic=account-upgrading-account) a un account Pagamento a consumo o Sottoscrizione. L'upgrade del tuo account sblocca l'intero catalogo {{site.data.keyword.Bluemix_notm}}, ti fornisce ulteriori risorse gratuite e altro.

Dopo aver eseguito l'upgrade del tuo account Lite a un account Pagamento a consumo, ricevi un credito promozionale di $200 che viene automaticamente applicato al tuo account. Il tuo credito di $200 è valido per 30 giorni e il tuo utilizzo viene automaticamente dedotto dall'importo del credito. Il credito non può essere utilizzato con le offerte di terze parti e potrebbe non essere disponibile per tutti gli account.

Se hai già un account Pagamento a consumo o Sottoscrizione, puoi anche convertire il tuo account in un tipo diverso. Per ulteriori informazioni, vedi [Upgrade del tuo account](/docs/account?topic=account-upgrading-account).
