---



copyright:

  years: 2017, 2018
lastupdated: "2018-03-22"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Gestione dei gruppi di risorse
{: #rgs}

Un gruppo di risorse è un modo per organizzare le risorse dell'account in raggruppamenti personalizzabili, in modo da poter assegnare rapidamente agli utenti l'accesso a più di una risorsa alla volta. Qualsiasi risorsa dell'account gestita attraverso il controllo dell'accesso {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) appartiene a un gruppo di risorse all'interno del tuo account. I servizi Cloud Foundry rimangono assegnati alle organizzazioni e agli spazi e non possono essere aggiunti a un gruppo di risorse.

Per iniziare a gestire i tuoi gruppi di risorse, vai a **Gestisci** &gt; **Account** &gt; **Gruppi di risorse** nella console {{site.data.keyword.Bluemix}}. Da lì puoi visualizzare i tuoi gruppi di risorse, rinominarli e creare nuovi gruppi di risorse.


## Creazione di un gruppo di risorse

Se disponi di un account Pagamento a consumo o Sottoscrizione, puoi creare più gruppi di risorse per gestire facilmente la quota e visualizzare l'utilizzo della fatturazione per un insieme di risorse. Puoi anche raggruppare le risorse per facilitare l'assegnazione dell'accesso degli utenti a più di un'istanza alla volta.

Se disponi di un account Lite o una prova gratuita di 30 giorni, non puoi creare ulteriori gruppi di risorse, ma puoi rinominare il tuo gruppo di risorse predefinito. 

Ogni gruppo di risorse è gratuito, tuttavia le connessioni tra un gruppo di risorse e un'organizzazione o uno spazio Cloud Foundry vengono conteggiate nella quota del tuo account. Per ulteriori informazioni, vedi [Cos'è un alias?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

1. Vai a **Gestisci** &gt; **Account** &gt; **Gruppi di risorse**.
2. Fai clic su **Crea un gruppo di risorse**.
3. Immetti un nome per il tuo gruppo di risorse.
4. Fai clic su **Aggiungi**.

## Aggiunta di risorse a un gruppo di risorse 

I servizi che sono gestiti utilizzando IAM appartengono a un gruppo di risorse invece che a un'organizzazione o uno spazio Cloud Foundry. Quando crei un'istanza del servizio per uno di questi servizi dal catalogo, ti viene richiesto di assegnare l'istanza a un gruppo di risorse. La tua selezione del gruppo di risorse al momento della creazione dell'istanza è finale e non può essere modificata.

## Visualizzazione delle risorse nei gruppi di risorse

Per visualizzare facilmente le risorse contenute in un gruppo, filtra per gruppo di risorse dal tuo dashboard.

## Ridenominazione di un gruppo di risorse

Il tuo primo gruppo di risorse viene creato e denominato `Default` automaticamente. Puoi scegliere di aggiornare il nome di questo gruppo o di qualsiasi altro gruppo che hai creato.

1. Vai a **Gestisci** &gt; **Account** &gt; **Gruppi di risorse**.
2. Fai clic su **Rinomina**.
3. Immetti un nome univoco e fai clic su **Salva**.

## Gestione dei gruppi di risorse e delle risorse utilizzando la CLI {{site.data.keyword.Bluemix_notm}}

La CLI {{site.data.keyword.Bluemix_notm}} ha diversi comandi che supportano la gestione delle risorse. Per ulteriori informazioni, vedi [Comandi per gestire i gruppi di risorse e le risorse](/docs/cli/reference/bluemix_cli/bx_cli.html#commands-for-managing-resource-groups-and-resources).

## Gestione dell'accesso ai tuoi gruppi di risorse

Cloud IAM ti offre la possibilità di fornire all'utente l'accesso specifico alle risorse nel tuo account. Puoi utilizzare Cloud IAM per assegnare politiche agli utenti, che forniscono all'utente l'accesso a tutte le risorse in un gruppo di risorse, a un singolo tipo di servizio all'interno di un gruppo di risorse o a una singola istanza del servizio nell'account. Fornire agli utenti l'accesso alle risorse all'interno di un gruppo di risorse non dà loro l'accesso per gestire il gruppo di risorse stesso. Puoi impostare l'accesso per la possibilità di visualizzare, modificare e gestire separatamente il gruppo di risorse effettivo.

Per ulteriori informazioni sulla gestione dell'accesso ai gruppi di risorse, vedi [Gestione dell'accesso IAM](/docs/iam/mngiam.html#iammanidaccser).
