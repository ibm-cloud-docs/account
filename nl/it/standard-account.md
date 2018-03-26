---



copyright:

  years: 2016, 2018
lastupdated: "2017-10-13"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Release limitata dell'account Standard {{site.data.keyword.Bluemix_notm}}
{: #betaintro}

La release limitata dell'account Standard {{site.data.keyword.Bluemix}} introduce un nuovo account gratuito, che offre un nuovo modo di lavorare in {{site.data.keyword.Bluemix_notm}} pubblico. A differenza di una versione di prova di 30 giorni {{site.data.keyword.Bluemix_notm}}, un account standard non ha una scadenza. Puoi continuare a lavorare sulle tue applicazioni {{site.data.keyword.Bluemix_notm}} senza preoccuparti dei limiti di tempo. 
{:shortdesc}

Gli utenti nelle regioni Regno Unito e Stati Uniti Sud sono eleggibili per un account Standard. Se non ti trovi in queste regioni, puoi comunque creare un account Standard chiedendo un invito a un amico o contattando il nostro team di vendite all'indirizzo sales@bluemix.net. Come proprietario di un account Standard, potrai invitare amici e colleghi a partecipare.  

## Presentazione dell'Account standard {{site.data.keyword.Bluemix_notm}}
{: #standardaccount}

Potresti chiederti qual è la differenza tra un account standard e un account di prova. Nelle seguenti tabelle vengono riepilogati i dettagli chiave relativi a un account standard {{site.data.keyword.Bluemix_notm}}. 

|Novità in un account standard |    
|-----------------|
| L'account non scade mai. |
| Le applicazioni Cloud Foundry possono accedere fino a 256 MB di memoria di runtime istantanea gratuita. |
| Puoi accedere ai piani Lite gratuiti per i servizi Watson richiesti come Conversation, Internet of Things Platform, Cloudant NoSQLDB. Per ulteriori informazioni, vedi [Disponibilità](/docs/pricing/standard_account.html#whatsavailable). |
| Le tue applicazioni verranno sospese se non vengono svolte attività di sviluppo per 10 giorni. |
| Le tue istanze del servizio vengono eliminate dopo 30 giorni di inattività. |
{:caption="Tabella 1. Novità in un account standard" caption-side="top"}

|Cosa rimane invariato quando si converte un account di prova? | 
|-----------------|
|L'account è gratuito -- non ti serve una carta di credito. |
|Puoi continuare a utilizzare le tue istanze del piano Lite. |
|L'organizzazione, gli spazi e le impostazioni di accesso dei membri del team associate rimangono uguali. È possibile trasferire un'organizzazione al tuo nuovo account. |
|Il livello di supporto di {{site.data.keyword.Bluemix_notm}} rimane lo stesso. |
{:caption="Tabella 2. Cosa rimane invariato" caption-side="top"}

**Nota**: se il tuo account di prova non viene convertito, viene visualizzato un messaggio che ne spiega il motivo. Potresti avere più di un'organizzazione nel tuo account di prova esistente o applicazioni che non è possibile trasferire. Effettua l'operazione appropriata e prova a convertire di nuovo l'account.

Quando sei proprietario di un account standard, puoi invitare i membri del team a collaborare nella tua organizzazione e nei tuoi spazi, visualizzare il tuo utilizzo, creare gli spazi, aggiornare il profilo del tuo account e gestire la tua organizzazione.

## Piani Lite
{: #liteplans}
   
I piani Lite, disponibili anche nell'account Pagamento a consumo, sono strutturati come quota gratuita. Puoi lavorare tranquillamente sui tuoi progetti senza il rischio di generare una fattura accidentale. La quota potrebbe essere applicata per uno specifico periodo di tempo, ad esempio un mese, oppure una tantum. Di seguito sono riportati alcuni esempi di quote dei piani Lite:

<ul>
<li>Numero massimo di dispositivi registrati.</li>
<li>Numero massimo di bind di applicazione.</li>
<li>Limite di archiviazione di dati crittografati, ad esempio 1 GB.</li>
<li>Capacità produttiva fornita.</li>
</ul> 

In un account standard, puoi utilizzare qualsiasi servizio del catalogo {{site.data.keyword.Bluemix_notm}} che disponga di un piano Lite. I piani Lite sono facili da individuare. Per impostazione predefinita, quando accedi al catalogo, tutti i servizi con un piano Lite vengono visualizzati e identificati con una tag Lite ![tag Lite](../icons/Lite.svg). Seleziona un servizio per visualizzare i dettagli della quota per il piano Lite associato.

## Cosa è disponibile in un account standard?
{: #whatsavailable}

Con un account standard, le tue applicazioni Cloud Foundry possono accedere fino a un massimo di 256 MB di memoria di runtime istantanea. Se superi la quota assegnata, puoi arrestare alcune delle applicazioni per liberare memoria di runtime. Puoi anche lavorare con un cluster Kubernetes con 2 CPU e 4 GB di RAM. 

Puoi utilizzare qualsiasi servizio del catalogo {{site.data.keyword.Bluemix_notm}} che disponga di un piano Lite. Tuttavia, puoi eseguire il provisioning di soltanto una istanza per piano Lite. Nella Release limitata dell'account Standard, i seguenti servizi offrono un piano Lite:

<ul>
<li>{{site.data.keyword.prf_hublong}}</li>
<li>{{site.data.keyword.mobilepushfull}}</li>
<li>{{site.data.keyword.cloudantfull}}</li>
<li>{{site.data.keyword.conversationfull}}</li>
<li>{{site.data.keyword.iot_full}}</li>
<li>{{site.data.keyword.languagetranslatorfull}}</li>
<li>{{site.data.keyword.personalityinsightsfull}}</li>
<li>{{site.data.keyword.toneanalyzerfull}}</li>
</ul>

Alcuni servizi non sono disponibili in tutte le regioni {{site.data.keyword.Bluemix_notm}}. Per ulteriori informazioni, vedi [Servizi per regione](/docs/services/services_region.html#services_region).

Prossimamente l'elenco verrà aggiornato con altri servizi.

### Limiti di quota

Quando si raggiungono i limiti di quota, la tua applicazione viene arrestata o il tuo servizio viene disabilitato. Se il piano Lite specifica che la quota viene fornita su base mensile, l'utilizzo delle risorse viene ripristinato il 1° di ogni mese, giorno in cui potrai riattivare il servizio. Quando stai per raggiungere il limite di quota o si già al limite, ricevi un'e-mail di notifica. 

Puoi eseguire il provisioning di 1 istanza per piano Lite. 

**Nota**: queste limitazioni si applicano solo a un account Standard. In qualsiasi momento, puoi effettuare l'aggiornamento a un account Pagamento a consumo o Sottoscrizione. Paghi solo per ciò che utilizzi oltre i limiti concessi dalle franchigie. Per ulteriori informazioni sugli account Pagamento a consumo e Sottoscrizione,
vedi [Tipi di account](/docs/accounts/account-types.html).

## Funzioni di efficienza
{: #devactivity}

Per aiutarti a gestire le tue risorse, abbiamo incluso funzioni di efficienza che si basano sull'attività di sviluppo e sull'utilizzo.

### Sospensione automatica delle applicazioni

Le applicazioni verranno sospese dopo 10 giorni di inattività dello sviluppo. Ciò è utile quando vuoi lavorare su una nuova applicazione perché non ti ritroverai a raggiungere il limite di 512 MB di quota di memoria. 

Per riattivare le tue applicazioni, inizia di nuovo a utilizzarle nella riga di comando Cloud Foundry o nella console {{site.data.keyword.Bluemix_notm}}. 
 
 Ecco un elenco di tutti i comandi che riattiveranno la tua applicazione:
  * push cf
  * cf restate
  * cf restart
  * cf ssh
  * cf scale
  * cf stop
  * cf start
  * cf create-route
  * cf map-route
  * cf unmap-route
  * cf delete-route
  * cf enable-ssh
  * cf disable-ssh

Per i dettagli sull'utilizzo dei comandi, vedi [Comandi Cloud Foundry](/docs/cli/reference/cfcommands/index.html).

 **Nota**: se la tua applicazione è già abilitata a SSH, non puoi utilizzare i comandi `cf enable-ssh` e `cf disable-sh` per riattivare la tua applicazione. 

### Garbage collection

I tuoi servizi con piano Lite vengono eliminati in assenza di attività per 30 giorni. Questo significa che non devi eliminare le istanze inattive quando vuoi crearne una nuova. 
 
## Partecipazione alla Release limitata dall'account Standard
{: #lgainvitation}

Puoi chiedere un invito a un amico che ha un account Standard o contattare il nostro team di vendite all'indirizzo sales@bluemix.net. Ci piacerebbe che lo provassi.

Se ricevi un invito da un amico o un da venditore {{site.data.keyword.Bluemix_notm}}, il tuo invito esclusivo viene inviato all'indirizzo e-mail che hai fornito. Una volta ricevuto l'invito, completa le istruzioni riportate nell'e-mail per registrare un account standard. 
