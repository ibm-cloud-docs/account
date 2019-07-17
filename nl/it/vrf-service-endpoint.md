---

copyright:
  years: 2019
lastupdated: "2019-07-01"

keywords: VRF, virtual routing and forwarding, service endpoint, private network

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Abilitazione di VRF e degli endpoint del servizio
{: #vrf-service-endpoint}

Per impostazione predefinita, ti connetti alle risorse nel tuo account sulla rete pubblica {{site.data.keyword.Bluemix}}. Puoi abilitare VRF (virtual routing and forwarding) per spostare l'instradamento IP per il tuo account e tutte le sue risorse in una tabella di instradamento separata. Se VRF è abilitato, puoi procedere ad abilitare gli endpoint del servizio {{site.data.keyword.Bluemix_notm}} per connetterti direttamente alle risorse senza utilizzare la rete pubblica.
{:shortdesc}

Per abilitare VRF (virtual routing and forwarding) e l'endpoint del servizio {{site.data.keyword.Bluemix_notm}}, devi avere un account fatturabile.

## Abilitazione di VRF
{: #vrf}

VRF consente a più istanze di una tabella di instradamento di esistere in un router e di funzionare simultaneamente. Quando abiliti VRF, viene creata una tabella di instradamento separata per il tuo account e le connessioni verso e dalle risorse del tuo account vengono instradate separatamente sulla rete {{site.data.keyword.Bluemix_notm}}. VRF è abilitato a livello di account, quindi tutte le risorse sono interessate da questa modifica di rete. Per ulteriori informazioni sulla tecnologia VRF e su come influenza l'instradamento di rete del tuo account, vedi [VRF (virtual routing and forwarding) su {{site.data.keyword.Bluemix_notm}}](/docs/resources?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud).

L'abilitazione di VRF altera in modo permanente la rete per il tuo account. Assicurati di capire l'impatto sul tuo account e sulle tue risorse. Una volta che lo hai abilitato, VRF non può essere disabilitato.
{: important}

Per abilitare VRF, crea un caso di supporto con la tua richiesta.

1. Nella console, vai a **Supporto** e fai clic su **Crea un caso**.
1. Seleziona **Account e accesso** come tipo di supporto.
1. Nel campo **Oggetto** , immetti `Private networking question`.
1. Nel campo **Descrizione**. immetti il seguente messaggio, sostituendo _enter your account number_ con il tuo numero di account {{site.data.keyword.Bluemix_notm}}.

   `We are requesting that account *enter your account number* is moved to its own VRF. We understand the risks and approve the change. Please reply back with the scheduled window(s) of time where this change will be made so we can prepare for the migration.`

Il team di progettazione di rete {{site.data.keyword.Bluemix_notm}} contatterà il proprietario del caso per pianificare una data/ora di esecuzione della conversione della rete del tuo account in VRF. Durante il processo di conversione, le connessioni alle risorse presenti nel tuo account potrebbero essere instabili a causa della perdita di pacchetti. La conversione impiega circa 15-30 minuti, a seconda della complessità del tuo account. Se il tuo account ha delle connessioni {{site.data.keyword.BluDirectLink}} legacy, ci potrebbe volere più tempo.


## Abilitazione degli endpoint del servizio
{: #service-endpoint}

Quando gli endpoint del servizio {{site.data.keyword.Bluemix_notm}} sono abilitati nel tuo account, puoi scegliere di esporre un endpoint di rete privato quando crei una risorsa. Puoi quindi connetterti direttamente a questo endpoint sulla rete privata {{site.data.keyword.Bluemix_notm}} piuttosto che sulla rete pubblica. Poiché le risorse che usano gli endpoint di rete privata non hanno un indirizzo IP instradabile su internet, le connessioni a queste risorse sono più sicure. Per ulteriori informazioni, vedi [Endpoint del servizio per le connessioni di rete privata](/docs/resources?topic=resources-service-endpoints).

Prima di poter abilitare gli endpoint del servizio, VRF deve essere abilitato per il tuo account.
{: note}

Per abilitare gli endpoint del servizio dalla CLI, hai bisogno della versione 0.13 o successiva della CLI [{{site.data.keyword.Bluemix_notm}}](/docs/cli?topic=cloud-cli-getting-started).

1.  Controlla se gli endpoint del servizio sono già abilitati nel tuo account.

    ```
    ibmcloud account show
    ```
    {: codeblock}

    Se `Service Endpoint Enabled` è `false` come mostrato nel seguente esempio, gli endpoint del servizio non sono abilitati.

    ```
    Retrieving account Mia Example's Account of m.example@example.com...
    OK

    Account ID:                   abc123d0bc2edefthyufffc9b5ca318   
    Currently Targeted Account:   true   
    Linked Softlayer Account:     0123456   
    Service Endpoint Enabled:     false  
    ```
    {: screen}
1. Abilita gli endpoint del servizio eseguendo il seguente comando.

   ```
   ibmcloud account update --service-endpoint-enable true
   ```
   {: codeblock}

   Potrebbe volerci qualche minuto perché questa modifica diventi effettiva. Una volta completato il comando, puoi eseguire nuovamente il comando `ibmcloud account show` per verificare.

    Se VRF non è abilitato per il tuo account, l'esecuzione di questo comando ti richiede di creare un caso per abilitarlo. Immetti `y` per creare il caso di supporto. Dopo che VRF è abilitato nell'account, esegui nuovamente il comando per abilitare la connettività di endpoint del servizio nel tuo account.

    ```
    Service Endpoint is not available in linked Softlayer Account 1008967.
    Enable VRF(Virtual Routing and Forwarding) first to proceed.
    Learn more about VRF here - https://cloud.ibm.com/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html.

    Do you want to open a ticket to enable it?[y/N]> y
    Ticket 70729615 was opened successfully. Follow the link https://control.softlayer.com/support/tickets/70729876 to check the details and track the status of the ticket. You will be required to login to view this ticket.
    Account ID:    1008967
    Ticket:        Private Network Question
    ```
    {: screen}


Dopo che gli endpoint del servizio sono stati abilitati, puoi creare risorse che si connettono sulla rete privata {{site.data.keyword.Bluemix_notm}}. Per un elenco dei servizi che supportano gli endpoint del servizio e ulteriori informazioni, vedi [Impostazione degli endpoint di rete privata](/docs/resources?topic=resources-private-network-endpoints).
