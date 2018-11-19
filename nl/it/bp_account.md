---

copyright:

  years: 2018
lastupdated: "2018-10-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Procedure consigliate per la configurazione del tuo account
{: #account_setup}

Le procedure consigliate forniscono gli elementi fondamentali per la riuscita prima di iniziare a creare le risorse. Se sei pronto a ricevere le applicazioni per la produzione e a configurare un ambiente per i tuoi sviluppatori, consulta le seguenti sezioni per configurare il tuo account.
{:shortdesc}

Le seguenti procedure consigliate si focalizzano sull'utilizzo dei servizi abilitati IAM. Al momento, non tutti i servizi in {{site.data.keyword.cloud}} sono abilitati IAM. Se un'istanza del servizio nel tuo account appartiene a un'organizzazione o spazio Cloud Foundry, le politiche IAM, i gruppi di risorse e i gruppi di accesso non si applicano ad essa. Puoi ancora utilizzare sia gli organizzazioni che gli spazi Cloud Foundry e i gruppi di risorse nel tuo account, ma devi assegnare agli utenti l'accesso a tali risorse separatamente. Per ulteriori informazioni sull'utilizzo di organizzazioni e spazi Cloud Foundry, vedi [Aggiunta di organizzazioni e spazi](/docs/account/orgs_spaces.html#orgsspacesusers).
{: tip}

## Che cosa è una buona strategia del gruppo di risorse?
{: #resource-group-strategy}

Dato che un gruppo di risorse è un contenitore logico per le risorse, utilizzare un gruppo di risorse per l'ambiente del progetto è un buon punto di partenza. Questa strategia consente agli amministratori di controllare e visualizzare l'utilizzo delle risorse a livello dell'ambiente del progetto. Ad esempio, un progetto tipico ha ambienti di sviluppo, test e produzione. Di conseguenza, un progetto denominato `CustApp` avrebbe i seguenti gruppi di risorse:

* CustApp-Dev
* CustApp-Test
* CustApp-Prod

L'accesso può quindi essere concesso agli utenti. Ad esempio, uno sviluppatore di solito ha diritti di accesso di ampia portata al gruppo di risorse di sviluppo ed è molto più limitato o non ha accesso al gruppo di risorse di produzione.

Se hai un account di sottoscrizione o di pagamento a consumo, puoi creare ulteriori gruppi di risorse: 

1. Vai a **Gestisci** &gt; **Account** &gt; **Gruppi di risorse**.
2. Fai clic su **Crea un gruppo di risorse**.
3. Immetti il nome del tuo gruppo di risorse.
4. Fai clic su **Aggiungi**.

## Configurazione dei tuoi gruppi di risorse
{: #setting-up-rgs}

I gruppi di risorse sono un contenitore logico per l'organizzazione delle risorse abilitate IAM. Tutti i servizi gestiti utilizzando il controllo dell'accesso IAM appartengono a un gruppo di risorse. Assegni una risorsa al suo gruppo di risorse quando la crei dal catalogo. Non puoi modificare l'assegnazione al gruppo di risorse dopo che l'hai configurata, ed è per questo che è importante configurare ora alcuni dei tuoi gruppi di risorse.

Se hai un account di prova o Lite, utilizza il gruppo di risorse predefinito e non puoi crearne di ulteriori.
{: tip}

## Aggiunta di risorse a un gruppo di risorse
{: #adding-resources}

Quando crei una risorsa abilitata IAM dal catalogo, devi selezionare il gruppo di risorse che vuoi assegnarle. Dopo aver creato una risorsa, non puoi modificare il gruppo di risorse a cui è assegnata. Se si commette un errore in questa fase, ti viene richiesto di eliminare la risorsa e crearne una nuova.

### Accesso richiesto per l'aggiunta di una risorsa a un gruppo di risorse
{: #rg_access}

Il proprietario dell'account {{site.data.keyword.cloud_notm}} può aggiungere le risorse a qualsiasi gruppo di risorse. Tuttavia, agli altri utenti deve essere concesso l'accesso utilizzando una politica di accesso IAM. Ci sono minimo due ruoli di gestione della piattaforma che devono essere assegnati agli utenti per aggiungere le risorse a un gruppo di risorse: 

* Ruolo visualizzatore o superiore sul gruppo di risorse stesso
* Ruolo editor o superiore sulla risorsa o sul servizio 

Per aggiungere una risorsa a un gruppo di risorse, completa la seguente procedura:

1. Vai a **Gestisci** &gt; **Account** &gt; **Gruppi di risorse**.
2. Fai clic sul menu ![icona Ulteriori azioni](../icons/overflow-menu.svg) dell'icona Ulteriori azioni di un gruppo di risorse a cui vuoi aggiungere le risorse e seleziona **Aggiungi risorse**.
3. Quando vieni reindirizzato al catalogo, seleziona la risorsa che vuoi aggiungere.
4. Seleziona il gruppo di risorse a cui vuoi assegnarla.
5. Fai clic su **Crea**.

Puoi sempre andare direttamente al catalogo per creare le risorse e assegnarle a un gruppo di risorse.
{: tip} 

Per ulteriori informazioni, consulta [Procedure ottimali per organizzare le risorse in un gruppo di risorse](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).

## Passi successivi

Configura i gruppi di accesso per gli utenti e gli ID servizio che richiedono lo stesso accesso alle risorse e ai gruppi di risorse nel tuo account. Puoi assegnare un numero minimo di politiche di accesso, per risparmiare tempo. Per ulteriori informazioni, consulta [Procedure consigliate per l'assegnazione dell'accesso](/docs/iam/bp_access.html).

Consulta [Procedure consigliate per organizzare utenti, team e applicazioni](/docs/tutorials/users-teams-applications.html#best-practices-for-organizing-users-teams-applications), per ulteriori informazioni sulla configurazione degli utenti e dei team nel tuo account:
