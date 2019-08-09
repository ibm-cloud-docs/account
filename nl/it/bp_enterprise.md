---

copyright:
  years: 2019
lastupdated: "2019-07-23"

keywords: enterprise, enterprise resources, enterprise account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Procedure consigliate per la configurazione di un'azienda
{: #enterprise-best-practices}

Queste procedure consigliate sono un primo passo necessario per configurare un'azienda {{site.data.keyword.cloud}}.
{:shortdesc}

## Organizzazione degli account in base a come vuoi tracciare la fatturazione
{: #organize-enterprise-usage}

Un vantaggio chiave delle aziende {{site.data.keyword.cloud_notm}} è che ti consentono di visualizzare e gestire in modo centralizzato la fatturazione e l'utilizzo tra più account. L'utilità di questa funzionalità dipende dalla tua struttura aziendale, perché i dati di utilizzo vengono aggregati per ogni account e gruppo di account. Crea dei gruppi di account per i progetti che vengono utilizzati in un budget comune. Ad esempio, vedi [Come posso utilizzare un'azienda?](/docs/account?topic=account-enterprise#enterprise-use-cases).

L'amministratore aziendale o il tuo direttore finanziario potrebbe non avere familiarità con ogni singolo account o con il gruppo di account. Per rendere più facile identificare il loro scopo, dai ad ogni account o gruppo di account un nome leggibile. Se la tua società utilizza i codici di fatturazione, puoi anche incorporarli nel nome. Ad esempio, invece di un gruppo di account `devteam` con gli account `fed ui` e `be api`, crea il gruppo di account `Development - A2B3` con gli account `Front-end UI team` e `Back-end API team`.

Un utente aziendale con accesso da amministratore o editor può modificare i nomi dell'azienda e del gruppo di account, ma non può modificare i nomi degli account. Per modificare un nome account, un utente deve far parte dell'account stesso.
{:tip}

Poiché hai una vista unificata di tutti gli utilizzi organizzati dai tuoi account e gruppi di account, puoi addebitare i costi di utilizzo ai team associati. Per ulteriori informazioni, vedi [Recupero dei costi per l'utilizzo aziendale](/docs/billing-usage?topic=billing-usage-enterprise-usage#enterprise-cost-recovery).

## Creazione di una gerarchia aziendale coerente
{: #accounts-vs-groups}

Quando configuri la tua azienda, crea una gerarchia aziendale che rispecchia la tua società o organizzazione. Quando crei gli account e i gruppi di account, pensa a uno schema coerente di come la tua società utilizza i seguenti livelli aziendali:
- I gruppi di risorse e le organizzazioni e gli spazi Cloud Foundry all'interno di un account
- Gli account all'interno di un gruppo di account
- I gruppi di account all'interno dell'azienda

Ad esempio, la tua azienda potrebbe creare degli account per ogni team, con dei gruppi di risorse o delle organizzazioni Cloud Foundry all'interno dell'account per ambienti di sviluppo, test e produzione. Un'altra azienda potrebbe avere account separati per ogni ambiente, che vengono raggruppati in gruppi di account per ogni team.

Tuttavia scegli di strutturare la tua azienda in modo che sia il più coerente possibile per semplificare la gestione aziendale. Poiché è facile creare e tenere traccia dei nuovi account, si può essere tentati di creare molti account separati quando gli utenti li richiedono. Tuttavia, ogni account introduce ulteriori carichi di gestione. Quando pensi come strutturare la tua azienda, tieni presente i seguenti punti.
- Per ogni account che crei, gli utenti devono essere invitati e il loro accesso deve essere gestito in modo separato.
- Una struttura non coerente può rendere difficile determinare a chi fornire l'accesso all'interno di ciascun account e quali team utilizzano le risorse.
- Gli utenti possono collaborare su risorse e servizi solo all'interno di un account. Le risorse non possono essere spostate tra gli account.

## Utilizzo delle risorse in un'azienda
{: #child-resources-enterprise}

Nell'azienda, crea delle risorse solo negli account secondari che importi o crei all'interno dell'azienda. Sebbene sia possibile creare le risorse all'interno dell'account aziendale, non è una prassi ottimale per i seguenti motivi:
 - L'account aziendale è sempre un account secondario diretto dell'azienda e non può essere spostato, per cui non avrai la flessibilità di modificare il modo in cui l'utilizzo viene segnalato per le risorse.
 - L'account aziendale contiene gli utenti e l'accesso per la gestione dell'azienda e della relativa fatturazione, per cui solo gli utenti con tali responsabilità dovrebbero essere aggiunti all'account.

Gli utenti in ogni account nell'azienda possono creare, utilizzare e collaborare sulle risorse come è possibile fare in un account autonomo. Per i dettagli, vedi [Gestione di risorse e servizi](/docs/resources?topic=resources-resource). Gli utenti aziendali non possono utilizzare direttamente le risorse negli account secondari, ma possono monitorare i piani e i tipi di risorse utilizzati in ogni account visualizzandone l'utilizzo. Per ulteriori informazioni, vedi [Visualizzazione dell'utilizzo in un'azienda](/docs/billing-usage?topic=billing-usage-enterprise-usage).

## Configurazione delle politiche di accesso in un'azienda
{: #access-enterprise}

Come sempre, segui le procedure consigliate per l'assegnazione del numero minimo di politiche di accesso e livelli di accesso. Questo ti consente di utilizzare meno tempo nell'assegnazione dell'accesso agli utenti e più tempo nel focalizzarti sullo sviluppo in {{site.data.keyword.cloud_notm}}, assicurandoti di non fornire un accesso non voluto agli utenti che non devono averlo.

I gruppi di accesso sono uno strumento utile per assegnare l'accesso a un gruppo di utenti e ID servizio che hanno tutti bisogno dello stesso accesso. Utilizzando i gruppi di accesso, puoi semplificare la gestione dell'accesso assegnando il numero minimo di politiche di accesso ai gruppi di utenti.  Ad esempio, se hai cinque utenti che vuoi gestiscano tutte le attività correlate alla gestione dell'account e alla fatturazione per l'azienda, puoi combinarli in un gruppo di accesso denominato `Administrators`. Nel gruppo di accesso puoi assegnare due politiche: una con il ruolo di amministratore sul servizio di gestione dell'account di fatturazione e una con il ruolo di amministratore su tutti i servizi di gestione dell'account. Quando gli utenti modificano i team e le responsabilità di lavoro, puoi aggiungerli o rimuoverli dal gruppo di accesso invece di aggiungere o rimuovere le stesse politiche dai singoli utenti.
