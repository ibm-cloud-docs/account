---

copyright:
  years: 2018, 2019
lastupdated: "2019-01-28"

keywords: resource group, account access, user access, IAM, organize

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Procedure consigliate per la configurazione del tuo account
{: #account_setup}

Le procedure consigliate sono un primo passo necessario per avere successo quando inizi a creare le risorse. Se sei pronto a ricevere le applicazioni per la produzione e a configurare un ambiente per i tuoi sviluppatori, consulta le seguenti sezioni per configurare il tuo account.
{:shortdesc}

Le seguenti procedure consigliate si focalizzano sull'utilizzo dei servizi abilitati IAM. Al momento, non tutti i servizi in {{site.data.keyword.cloud}} sono abilitati IAM. Le politiche IAM, i gruppi di risorse e i gruppi di accesso non si applicano alle istanze del servizio che appartengono a un'organizzazione e a uno spazio Cloud Foundry. Puoi ancora utilizzare sia le organizzazioni che gli spazi Cloud Foundry e i gruppi di risorse nel tuo account, ma devi assegnare agli utenti l'accesso a tali risorse separatamente. Per informazioni sulle organizzazioni e gli spazi Cloud Foundry, vedi [Aggiunta di organizzazioni e spazi](/docs/account?topic=account-orgsspacesusers).
{: note}

## Cosa rende buona una strategia del gruppo di risorse?
{: #resource-group-strategy}

Gli amministratori possono avere un migliore controllo dell'utilizzo delle risorse a livello dell'ambiente del progetto se viene utilizzato un singolo gruppo di risorse per ogni ambiente di progetto. Ad esempio, un tipico progetto ha ambienti di sviluppo, test e produzione. Un progetto denominato `CustApp` avrà i seguenti gruppi di risorse:

* `CustApp-Dev`
* `CustApp-Test`
* `CustApp-Prod`

Puoi concedere l'accesso agli utenti. Ad esempio, uno sviluppatore di solito dispone di autorizzazioni di accesso di portata adeguatamente ampia al gruppo di risorse di sviluppo e un accesso molto più limitato, o per niente consentito, al gruppo di risorse di produzione.

Se disponi di un account Pagamento a consumo o Sottoscrizione, puoi creare ulteriori gruppi di risorse:

1. Vai a **Gestisci** > **Account** e seleziona **Gruppi di risorse** dal menu **Risorse account**.
3. Fai clic su **Crea**.
4. Immetti il nome del tuo gruppo di risorse.
5. Fai clic su **Aggiungi**.

Per ulteriori informazioni su quale tipo di account funziona meglio per te, vedi [Tipi di account](/docs/account?topic=account-accounts).


## Configurazione dei tuoi gruppi di risorse
{: #setting-up-rgs}

I gruppi di risorse sono un contenitore logico per l'organizzazione delle risorse abilitate IAM. Tutti i servizi gestiti utilizzando il controllo dell'accesso {{site.data.keyword.cloud_notm}} IAM (Identity and Access Management) appartengono a un gruppo di risorse. Assegni una risorsa al suo gruppo di risorse quando la crei dal catalogo. Non puoi modificare l'assegnazione al gruppo di risorse dopo che l'hai configurata, ed è per questo che è importante configurare ora alcuni dei tuoi gruppi di risorse.

Se disponi di un account Lite, hai accesso a un singolo gruppo di risorse creato per tuo conto. Non puoi creare dei gruppi di risorse supplementari. Considera [un upgrade del tuo account](/docs/account?topic=account-upgrading-account) per creare e gestire più gruppi di risorse.
{: note}


## Aggiunta di risorse a un gruppo di risorse
{: #adding-resources}

Puoi aggiungere una risorsa a un gruppo di risorse quando crei una risorsa abilitata a IAM dal catalogo. Quando selezioni la risorsa, assicurati che il gruppo di risorse di destinazione sia selezionato. Dopo che una risorsa è stata creata, non puoi modificare il gruppo di risorse a cui è stata assegnata. Se assegni accidentalmente una risorsa a un gruppo di risorse errato, elimina la risorsa e creane una nuova.

### Accesso richiesto per l'aggiunta di una risorsa a un gruppo di risorse
{: #rg_access}

In qualità di proprietario dell'account, puoi aggiungere risorse a qualsiasi gruppo di risorse. Agli altri utenti deve essere concesso l'accesso utilizzando una politica di accesso IAM per aggiungere le risorse ai gruppi di risorse. Ci sono minimo due ruoli di gestione della piattaforma che devono essere assegnati agli utenti per aggiungere le risorse a un gruppo di risorse:

* Ruolo Visualizzatore o superiore sul gruppo di risorse
* Ruolo Editor o superiore sulla risorsa o sul servizio

Per aggiungere una risorsa a un gruppo di risorse, completa la seguente procedura:

1. Vai a **Gestisci > Account** e seleziona **Gruppi di risorse**.
2. Fai clic sull'icona Azioni ![Icona Azioni](../icons/action-menu-icon.svg) per il gruppo di risorse a cui vuoi aggiungere le risorse e seleziona **Aggiungi risorse**.
3. Dopo che sei stato reindirizzato al catalogo, seleziona la risorsa che vuoi aggiungere.
4. Seleziona il gruppo di risorse a cui vuoi assegnarla.
5. Fai clic su **Crea**.

Puoi sempre andare direttamente al catalogo per creare le risorse e assegnarle a un gruppo di risorse.
{: tip}

Per ulteriori informazioni, consulta [Procedure ottimali per organizzare le risorse in un gruppo di risorse](/docs/resources?topic=resources-bp_resourcegroups).


## Utilizzo di tag per organizzare le risorse
{: #tags}

Utilizza le tag per organizzare le tue risorse e tracciare i costi d'utilizzo. Puoi aggiungere tag alle risorse correlate e visualizzarle in tutto il tuo account filtrando in base alle tag dal tuo dashboard. Le tag di coppia chiave-valore possono aiutarti a organizzare i tuoi ambienti di sviluppo, i tuoi progetti, la conformità e l'ottimizzazione.

Per aggiungere una tag a una risorsa, completa la seguente procedura:

1. Fai clic sull'icona Menu ![Icona Menu](../icons/icon_hamburger.svg) > **Elenco risorse** per visualizzare il tuo elenco di risorse. Trova la risorsa a cui vuoi aggiungere delle tag.
2. Se la risorsa già presenta una tag, passa il puntatore del mouse sulla tag esistente e fai clic sull'icona Modifica ![Icona Modifica](../icons/edit-tagging.svg). Se la risorsa non presenta una tag, passa il puntatore del mouse su **--** nella colonna `Tag` e fai clic su **Aggiungi tag**.
3. Immetti un nome per la tag e premi Invio dopo ciascuna tag, se ne stai aggiungendo più di una.
4. Per rimuovere una tag dalla risorsa, fai clic sull'icona Rimuovi ![Icona Rimuovi](../icons/close-tagging.svg) accanto alla tag.
5. Salva le tue modifiche.

Per ulteriori informazioni su quali sono le risorse a cui possono essere aggiunte delle tag e su come assegnare l'accesso per delegare la funzionalità di aggiunta di tag agli utenti nel tuo account, vedi [Gestione delle tag](/docs/resources?topic=resources-tag).


## Passi successivi

Configura i gruppi di accesso per gli utenti e gli ID servizio che richiedono lo stesso accesso alle risorse e ai gruppi di risorse nel tuo account. Puoi assegnare un numero minimo di politiche di accesso, per risparmiare tempo. Per ulteriori informazioni, consulta [Procedure consigliate per l'assegnazione dell'accesso](/docs/iam?topic=iam-cfaccess).
