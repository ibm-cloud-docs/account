---

copyright:
  years: 2019
lastupdated: "2019-07-15"

keywords: IBM Cloud account, account differences, account overview, account components, how access works

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Cosa c'è in un account?
{: #overview}

Il tuo account {{site.data.keyword.Bluemix}} include molti componenti e sistemi che interagiscono. Concetti su come alcuni componenti sono connessi o su come funziona l'accesso ti aiutano a comprendere come configurare il tuo account.
{:shortdesc}

All'interno del seguente diagramma, sono presenti due concetti principali per i componenti nella gerarchia dell'account che è importante comprendere. L'utilizzo delle linee continue e delle linee tratteggiate aiuta ad illustrare che alcuni componenti sono contenuti all'interno di altri, ad esempio gli utenti vengono aggiunti ai gruppi di accesso o alle organizzazioni Cloud Foundry. Tuttavia, alcuni componenti interagiscono con altri per fornire l'accesso invece dell'appartenenza. Ad esempio, agli utenti viene concesso l'accesso ai gruppi di risorse ma non sono membri di un gruppo di risorse nello stesso modo in cui lo sono per i gruppi di accesso. 

<figure>
<a href="https://cloud.ibm.com/docs/api/content/account/images/account_diagram.svg">
<img src="images/account_diagram.svg" alt="Un diagramma che mostra i componenti in un account, inclusi i servizi, gli utenti e i componenti secondari di ognuno di essi."></a>
<figcaption>Figura 1. Sistemi e componenti dell'account</figcaption>
</figure>

<dl>
<dt>Utenti</dt>
<dd>Gli utenti sono invitati all'account e viene loro concesso l'accesso alle risorse nell'account.</dd>
<dt>ID servizio</dt>
<dd>Un ID servizio identifica un servizio o un'applicazione analogamente a come un ID utente identifica un utente. Puoi utilizzare un ID servizio da te creato per abilitare un'applicazione esterna a {{site.data.keyword.Bluemix_notm}} ad accedere ai tuoi servizi. Puoi assegnare delle specifiche politiche di accesso all'ID servizio che limitano le autorizzazioni per l'utilizzo di specifici servizi o anche combinare le autorizzazioni per l'accesso a servizi differenti. Poiché gli ID servizio non sono collegati a uno specifico utente, se capita che un utente lasci un'organizzazione e venga eliminato dall'account, l'ID servizio rimane, garantendo che la tua applicazione o il tuo servizio continuino a essere attivi e in esecuzione. Per ulteriori informazioni, vedi [Creazione e gestione degli ID servizio](/docs/iam?topic=iam-serviceids#serviceids).</dd>
<dt>Risorse o istanze del servizio</dt>
<dd>I servizi in {{site.data.keyword.Bluemix_notm}} sono basati sui gruppi di risorse o su Cloud Foundry. Le istanze del servizio che possono essere aggiunte a un gruppo di risorse e gestite utilizzando {{site.data.keyword.Bluemix_notm}} IAM (Identity and Access Management) sono dette risorse. Le istanze del servizio che vengono aggiunte agli spazi e alle organizzazioni Cloud Foundry hanno un sistema di gestione dell'accesso separato mediante l'utilizzo di ruoli Cloud Foundry. Per ulteriori informazioni, vedi [Che cosa è una risorsa?](/docs/resources?topic=resources-resource#resource)</dd>
<dt>Chiavi API</dt>
<dd>Una chiave API è un codice univoco passato a una API per identificare l'applicazione o l'utente chiamante. Puoi utilizzare le chiavi API della piattaforma, che sono associate alle identità utente, e puoi creare altre chiavi API per gli ID servizio. Per ulteriori informazioni, vedi [Descrizione delle chiavi API](/docs/iam?topic=iam-manapikey#manapikey).</dd>
<dt>Gruppi di accesso</dt>
<dd>Puoi creare un gruppo di accesso per organizzare un insieme di utenti e ID servizio in una sola entità e assegnare facilmente le autorizzazioni. Puoi assegnare una sola politica al gruppo invece di assegnare lo stesso accesso più volte per ogni utente o ID del servizio individuale. Per ulteriori informazioni, vedi [Configurazione dei gruppi di accesso](/docs/iam?topic=iam-groups#groups).</dd>
<dt>Gruppo di risorse</dt>
<dd>Puoi utilizzare un gruppo di risorse per organizzare le risorse del tuo account in raggruppamenti personalizzabili in modo da poter assegnare rapidamente l'accesso agli utenti a più di un risorsa per volta. Qualsiasi risorsa dell'account gestita attraverso il controllo dell'accesso IAM (Identity and Access Management) appartiene a un gruppo di risorse all'interno del tuo account. Gli utenti non vengono aggiunti ai gruppi di risorse ma ad essi viene concesso l'accesso alle risorse all'interno oppure possono gestire il gruppo di risorse. Gli utenti a cui viene concesso l'accesso per gestire il gruppo di risorse possono creare nuove istanze all'interno del gruppo, gestire l'accesso di altri utenti per gestire il gruppo oppure modificare il nome del gruppo in base al ruolo IAM assegnato. Per ulteriori informazioni, vedi [Gestione di gruppi di risorse](/docs/resources?topic=resources-rgs#rgs) e [Prassi ottimali per organizzare le risorse nei gruppi di risorse](/docs/resources?topic=resources-bp_resourcegroups#bp_resourcegroups).</dd>
<dt>Organizzazioni Cloud Foundry</dt>
<dd>In qualità di proprietario dell'account o gestore dell'organizzazione, puoi aggiungere organizzazioni e spazi dalla pagina delle organizzazioni Cloud Foundry nella console. I servizi che supportano l'utilizzo delle organizzazioni e degli spazi Cloud Foundry vengono aggiunti a un'organizzazione e a uno spazio quando li crei dal catalogo. Le organizzazioni contengono utenti, domini e quote. All'interno di ogni organizzazione, vengono aggiunti degli spazi, che contengono le istanze del servizio. Per ulteriori informazioni, vedi [Aggiunta di organizzazioni e spazi](/docs/account?topic=account-orgsspacesusers#orgsspacesusers).</dd>
<dt>Spazi Cloud Foundry</dt>
<dd>All'interno di un'organizzazione, puoi utilizzare gli spazi per raggruppare un insieme di applicazioni, servizi e utenti. Gli spazi sono collegati a una specifica
regione in {{site.data.keyword.Bluemix_notm}}. Puoi creare gli spazi in un'organizzazione in base al ciclo di vita della distribuzione. Ad esempio, puoi creare uno spazio dev come un ambiente di sviluppo,
uno spazio test come un ambiente di test e uno spazio production come un ambiente di produzione. Puoi quindi associare
le tue applicazioni agli spazi. Per ulteriori informazioni, vedi [Aggiunta di organizzazioni e spazi](/docs/account?topic=account-orgsspacesusers#orgsspacesusers).</dd>
</dl>

Un altro aspetto importante del diagramma precedente è la raffigurazione dei tre tipi di sistemi di gestione dell'accesso che puoi utilizzare per fornire agli utenti dell'account l'accesso alle risorse all'interno dell'account.

  * Puoi utilizzare i [ruoli di accesso](/docs/iam?topic=iam-userroles#iamusermanrol) IAM per fornire agli utenti l'accesso a tutte le risorse che appartengono a un gruppo di risorse. Puoi anche concedere l'accesso agli utenti per gestire i gruppi di risorse e creare nuove istanze del servizio che vengono assegnate a un gruppo di risorse.
  * Puoi utilizzare i [ruoli di spazio e organizzazione](/docs/iam?topic=iam-cfaccess#cfroles) Cloud Foundry per fornire agli utenti l'accesso a qualsiasi istanza del servizio che si trova in uno spazio Cloud Foundry.
  * Puoi utilizzare le autorizzazioni dell'infrastruttura classica per concedere agli utenti delle [autorizzazioni](/docs/iam?topic=iam-infrapermission#infrapermission) più granulari per l'infrastruttura classica. Assegni l'accesso ai dispositivi e l'accesso alle sottoreti VPN separatamente.
