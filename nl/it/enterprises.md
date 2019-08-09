---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise account, multiple accounts, organization, hierarchy

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Cos'è un'azienda?
{: #enterprise}

Le aziende di {{site.data.keyword.Bluemix}} forniscono un modo per gestire in modo centralizzato la fatturazione e l'utilizzo di risorse tra più account. All'interno di un'azienda, crei una gerarchia di account a più livelli, con fatturazione e pagamenti di tutti gli account gestiti al livello aziendale.
{:shortdesc}

In confronto all'utilizzo di più account autonomi, le aziende offrono i seguenti vantaggi chiave:
- Gestione dell'account centralizzata: visualizza immediatamente la tua gerarchia aziendale completa, senza dover passare da un account a un altro. Puoi aggiungere account esistenti o crearne di nuovi direttamente all'interno dell'azienda.
- Fatturazione di sottoscrizione consolidata: tieni traccia della tua spesa di crediti e sottoscrizioni per tutti gli account da una singola vista. Il tuo credito di sottoscrizione viene aggregato e condiviso tra gli account nell'azienda. 
- Report dell'utilizzo dall'alto verso il basso: dal tuo account aziendale, puoi visualizzare l'utilizzo di tutti gli account nella tua azienda, organizzati per gruppo di account.

## Gerarchia aziendale
{: #enterprise-hierarchy}

Al suo interno, un'azienda è formata da tre blocchi di creazione principali:
- L'account aziendale, che funziona da account principale per tutti gli altri account nell'azienda. L'account aziendale gestisce la fatturazione per l'intera azienda, con i costi di utilizzo da tutti gli account sommati e pagati dall'account aziendale.
- I gruppi di account, che puoi utilizzare per organizzare gli account correlati. I gruppi di account non possono contenere le risorse stesse, ma puoi visualizzare i costi per l'utilizzo delle risorse dagli account che contengono.
- Gli account, sono proprio come gli account {{site.data.keyword.Bluemix_notm}} autonomi in quanto contengono le risorse e i gruppi di risorse, le organizzazioni e gli spazi Cloud Foundry e le autorizzazioni di accesso indipendenti. Tuttavia, una differenza importante è che ciascun account in un'azienda non gestisce la propria fatturazione e i propri pagamenti perché sono gestiti al livello dell'account aziendale.

Crea i livelli nella tua azienda nidificando un gruppo di account all'interno di un gruppo di account.
![Un diagramma che mostra quattro livelli aziendali. Il livello principale è l'azienda, che contiene due livelli di gruppi di account. Quindi il gruppo di account contiene gli account.](images/enterprise-hierarchy.svg "I livelli aziendali vengono creati aggiungendo i gruppi di account.")

Un'azienda può contenere fino a 10 livelli di account e gruppi di account. Nel suo formato più basilare, un'azienda ha due livelli: l'account aziendale e un solo account secondario.

La tua struttura aziendale è flessibile e può crescere e essere modificata in base ai tuoi bisogni. Puoi aggiungere e rimuovere i gruppi di account e spostare gli account tra i gruppi di account. Se lo scopo di un gruppo di account viene modificato, puoi ridenominarlo per rispecchiare meglio gli account che contiene.

## Fatturazione consolidata
{: #enterprise-billing}

In un'azienda, tutta la fatturazione è gestita tramite l'account aziendale di livello superiore. Le aziende richiedono la [fatturazione di sottoscrizione](/docs/account?topic=account-accounts#subscription-account), che significa che acquisti una sottoscrizione per l'ammontare di crediti che spendi durante il termine di sottoscrizione e l'utilizzo viene dedotto dal credito di sottoscrizione ad una tariffa scontata. Il credito di sottoscrizione, così come il credito da tutte le promozioni, viene aggiunto al pool di crediti aziendale, che viene condiviso tra tutti gli account nell'azienda. Quando gli account utilizzano le risorse, il credito viene speso da pool di crediti.

![Un diagramma che mostra che il credito dagli account viene aggiunto al pool di crediti aziendale, che è gestito dall'amministratore nell'account aziendale.](images/enterprise-billing.svg "La fatturazione per tutti gli account viene gestita dall'amministratore della fatturazione nell'account aziendale.")

Poiché la fatturazione è consolidata, le aziende rendono più facile la gestione di fatturazione e pagamenti tra più account con questi vantaggi chiave:
* Un pool di crediti di sottoscrizioni che copre più account, in modo da poter calibrare le tue sottoscrizioni per tutto il tuo utilizzo invece di quello per account.
* Una sola fattura per tutto l'utilizzo all'interno dell'azienda, per cui comprendere i costi è facile.
* Un unico posto in cui gestire i metodi di pagamento, per cui puoi eseguire un solo aggiornamento per tutti gli account.

Ulteriori informazioni in [Gestisci centralmente la fatturazione e l'utilizzo con le aziende](/docs/billing-usage?topic=billing-usage-enterprise).

## Gestione delle risorse
{: #enterprise-resources}

Le risorse e i servizi all'interno di un'azienda funzionano allo stesso modo degli account autonomi. Ogni account in un'azienda può contenere le risorse nei gruppi di risorse e i servizi nelle organizzazioni e negli spazi Cloud Foundry. I gruppi di account non possono contenere le risorse. Per ulteriori informazioni, vedi [Gestione di risorse e servizi](/docs/resources?topic=resources-resource).

![Un diagramma che mostra quali risorse sono contenute negli account nell'azienda.](images/enterprise-resources.svg "Le risorse sono collegate all'account nell'azienda, così come un account autonomo.")

Come per tutti gli account, le risorse sono collegate al gruppo di risorse e all'account in cui sono state create, per cui non possono essere spostate tra gli account nell'azienda. Tuttavia, la struttura flessibile dell'azienda significa che puoi spostare le risorse all'interno dell'azienda spostando gli account che le contengono.

## Report dell'utilizzo dall'alto verso il basso 
{: #enterprise-usage}

Dall'account aziendale, puoi visualizzare l'utilizzo di risorse da tutti gli account nell'azienda. A partire dal livello aziendale, vedi i costi di utilizzo stimati suddivisi per account e gruppi di account. Puoi scorrere verso il basso nella struttura aziendale per vedere i costi all'interno di ogni livello. Al livello dell'account, gli utenti aziendali possono visualizzare i costi per ogni tipo di risorsa o servizio nell'account.

Poiché l'accesso nell'azienda è separato dall'accesso in ogni account, gli utenti aziendali non possono automaticamente creare o gestire le risorse all'interno degli account secondari. In modo simile, gli utenti in ogni account possono continuare a visualizzare il proprio utilizzo corrente e passato dalla pagina degli utilizzi indipendentemente dal fatto che dispongono dell'accesso all'azienda.

Per ulteriori informazioni, vedi [Visualizzazione dell'utilizzo in un'azienda](/docs/billing-usage?topic=billing-usage-enterprise-usage).

## Gestione di accesso e utente isolata 
{: #enterprise-access}

Le aziende mantengono la gestione di accesso e utente isolata tra l'azienda e i suoi account secondari per fornire una maggiore sicurezza per i dati dei tuoi account. Gli utenti e i loro accesso assegnato nell'account aziendale sono completamente separati da quelli negli account secondari e non viene ereditato automaticamente alcun accesso tra i due tipi di account.

Gli elenchi utente di ogni account sono visibili solo per gli utenti che sono stati invitati in tali account. Solo perché un utente viene invitato e gli viene fornito l'accesso per gestire l'intera azienda, non significa che possa visualizzare gli utenti invitati in ogni account secondario. La gestione utente in ogni azienda e ogni account è completamente separata e deve essere gestita dal proprietario dell'account o da un utente a cui è stato fornito il ruolo di amministratore sul servizio di gestione dell'account di gestione dell'utente nell'account specifico.

In modo simile a come la gestione utente viene completamente separata in ogni account e l'azienda stessa, lo è anche la gestione dell'accesso. Questa separazione significa che gli utenti che gestiscono la tua azienda non possono accedere alle risorse dell'account all'interno degli account secondari a meno che non li abiliti nello specifico. Ad esempio, il tuo direttore finanziario può avere il ruolo di amministratore sul servizio di gestione dell'account di fatturazione all'interno dell'account aziendale, che gli fornisce l'accesso alle informazioni di fatturazione e pagamento e ai dati di utilizzo fino al tipo di risorsa. Ma, a meno che non siano invitati in un account secondario e gli venga assegnato l'accesso al servizio di gestione dell'account di fatturazione di tale account, non possono visualizzare le offerte o aggiornare i limiti di spesa dell'account secondario.

Per ulteriori informazioni, vedi [Gestione dell'utente per le aziende](/docs/iam?topic=iam-enterprise-access).

## Come posso utilizzare un'azienda? 
{: #enterprise-use-cases}

Le aziende possono essere utili per semplificare la gestione di fatturazione e account per scenari altrimenti complessi. Le aziende possono essere vantaggiose per gestire tutte le grandi organizzazioni, ma due casi di utilizzo principali per cui potresti volerle creare sono le grandi società e le istituzioni educative.

Come strutturi la tua azienda dipende da come vuoi analizzare i costi e l'utilizzo, ad esempio come addebitare i costi a un gruppo particolare. Organizza la tua azienda in base a come vuoi tenere traccia e gestire la fatturazione e l'utilizzo.
{:tip}

### Grandi società o organizzazioni
{: #enterprise-orgs}

Le aziende possono essere preziose per le grandi organizzazioni che altrimenti richiedono più account separati per i loro dipartimenti o team. Utilizzando i gruppi di account, puoi modellare la tua gerarchia aziendale dopo la struttura della tua organizzazione.

#### Organizza per dipartimento
{: #enterprise-by-dept}

Se la tua organizzazione ha dei team globali che condividono un budget, puoi modellare la tua struttura aziendale dopo i loro dipartimenti. Con questa struttura, puoi visualizzare i costi di utilizzo che vengono aggregati per ogni dipartimento.

![Un'azienda a quattro livelli che raggruppa gli account in base al dipartimento in un'organizzazione. Ad esempio, gruppi di account denominati Marketing, Development e Sales. I gruppi di account contengono gli account dei team all'interno di tali dipartimenti. Ad esempio il gruppo di account Sales contiene gli account Direct, Online e Enablement.](images/enterprise-by-dept.svg "Un'azienda che organizza gli account in base al dipartimento nell'organizzazione.")

#### Organizza per area geografica
{: #enterprise-by-geo}

Oppure, se la tua organizzazione ha budget separati per area geografica, puoi strutturare la tua azienda per raggruppare i costi per ogni entità geografica.

![Un'azienda a quattro livelli che raggruppa gli account in base all'area geografica. Ad esempio, i gruppi di account sono denominati Americas, Europe e Asia-Pacific. I gruppi di account contengono i paesi all'interno di tali ubicazioni. Ad esempio il gruppo di account Asia-Pacific contiene gli account China, Japan e India.](images/enterprise-by-geo.svg "Un'azienda che organizza gli account in base all'area geografica.")

### Istituzioni educative 
{: #enterprise-edu}

Le istituzioni educative potrebbero voler fornire ai propri studenti degli account {{site.data.keyword.Bluemix_notm}} in modo che possano imparare capacità preziose tramite progetti pratici che utilizzano i servizi {{site.data.keyword.Bluemix_notm}}. Per queste istituzioni, ad esempio le università tradizionali o le piattaforme di apprendimento online, puoi raggruppare gli account per dipartimento o area tematica e poi creare gli account per ogni corso.

All'interno di ogni account, gli studenti possono creare delle risorse per creare i propri progetti e collaborare con altri studenti nell'account. L'università ha una vista completa dei costi di ogni dipartimento e corso.

![Un'azienda a tre livelli che modella come un'università può organizzare i propri account. Ad esempio, i gruppi di account vengono denominati per ogni dipartimento: Data Science, Computer Science e Computer Engineering. Ogni gruppo di account contiene singoli account per ogni classe, ad esempio DS101 e DS102.](images/enterprise-edu.svg "Un'azienda per un'università che ha dei gruppi di account per ogni dipartimento e singoli account per ogni classe.")
