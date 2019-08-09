---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, enterprise users, enterprise access, enterprise tutorial

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Introduzione a un'azienda
{: #enterprise-tutorial}

Questa esercitazione illustra come configurare un'azienda per dipartimento in modo che puoi gestire e tenere traccia dei costi di utilizzo per più account {{site.data.keyword.Bluemix}}. Completando questa esercitazione, impari come creare un'azienda, aggiungere account e organizzarli in gruppi di account, invitare utenti ed esplorare le sottoscrizioni.
{:shortdesc}

L'esercitazione utilizza una società fittizia chiamata *Example Corp* che vuole creare un'azienda con la seguente struttura. Una volta completata l'esercitazione, adatta ogni passo in modo che corrisponda agli account e alla struttura desiderata della tua organizzazione.

![Un'azienda a quattro livelli che raggruppa gli account in base al dipartimento in un'organizzazione. Ad esempio, gruppi di account denominati Marketing, Development e Sales. I gruppi di account contengono gli account dei team all'interno di tali dipartimenti. Ad esempio il gruppo di account Sales contiene gli account Direct, Online e Enablement.](images/enterprise-by-dept.svg "Un'azienda che organizza gli account in base al dipartimento nell'organizzazione.")

## Prima di iniziare
{: #setting-prereqs}

Leggi [Cos'è un'azienda?](/docs/account?topic=account-enterprise) per imparare i principi di base di come funzionano la gestione dell'account, la fatturazione, le risorse e la gestione di utente e accesso in un'azienda.

Verifica di avere l'accesso richiesto in un account Sottoscrizione, che viene utilizzato come account di base da cui crei l'azienda. Per creare un'azienda, devi essere il proprietario dell'account o avere il ruolo di amministratore sul servizio di gestione dell'account di fatturazione.

La creazione di un'azienda da un account e l'importazione degli account esistenti non possono essere annullate. Questa esercitazione viene fornita come esempio di procedura che puoi seguire per configurare un'azienda per dipartimento, ma dovresti pianificare attentamente la tua struttura aziendale per soddisfare le esigenze della tua organizzazione.
{:important}

## Passo 1. Crea l'azienda
{: #create_enterprise_tutorial}

Le aziende vengono create da un account Sottoscrizione esistente. Quando crei l'azienda, l'account viene aggiunto alla gerarchia aziendale. La fatturazione delle transizioni viene gestita dall'azienda, ma i relativi utenti e risorse rimangono gli stessi e non vengono minimamente influenzati. Per una descrizione completa degli impatti sull'account, vedi [Creazione di un'azienda](/docs/account?topic=account-create-enterprise).

1. Vai a **Gestisci** > **Azienda** e fai clic su **Crea**.
2. Immetti il nome della tua società, ad esempio Example Corp, per identificare la tua azienda.
3. Immetti il dominio della tua società, ad esempio `examplecorp.com`.
4. Controlla le informazioni sull'impatto sul tuo account e seleziona **Comprendo l'impatto sul mio account**. Quindi, fai clic su **Crea**. L'account fa ora permanentemente parte dell'azienda e non può essere rimosso.

Dopo aver creato la tua azienda, vieni reindirizzato al dashboard aziendale. Da qui, puoi visualizzare i dettagli, gli account, gli utenti e le informazioni di fatturazione dell'azienda. Vai alla pagina **Account** per visualizzare la tua struttura aziendale, in cui vedi i seguenti account:
  * Un account aziendale con lo stesso nome della tua azienda. Questo account viene utilizzato per la gestione dell'azienda.
  * L'account da cui hai creato l'azienda. Gli utenti possono continuare ad utilizzare le risorse nell'account non interessato.

## Passo 2. Crea una struttura aziendale con i gruppi di account
{: #account_groups_tutorial}

Utilizza i gruppi di account per organizzare gli account correlati. Il secondo e il terzo livello della gerarchia dell'azienda Example Corp. contengono i gruppi di account Marketing, Development, Sales, Design e Engineering. Completa la seguente procedura per creare i gruppi di account:

1. Dal dashboard dell'azienda fai clic su **Account** per visualizzare gli account e i gruppi di account nell'azienda.
2. Nella sezione del gruppo di account, fai clic su **Crea**.
3. Immetti il nome del gruppo di account, ad esempio `Marketing`.
4. Nel campo del contatto, immetti l'ID IBM dell'utente che vuoi sia il contatto principale del gruppo di account. Poiché un gruppo di account non può contenere alcuna risorsa, non ha un proprietario come un account.
5. Seleziona **Example Corp** come account principale.
6. Fai clic su **Crea**.

Ripeti i passi per creare i gruppi di account Sales, Development, Design e Engineering. Quando crei i gruppi di account Design e Engineering, assicurati di aggiungere Development come gruppo di account principale.

## Passo 3. Importa degli account esistenti
{: #existing_accounts_tutorial}

Ora che hai creato una struttura aziendale, puoi importare un account esistente nell'azienda. Quando importi un account, viene permanentemente aggiunto all'azienda. Proprio come quando crei un'azienda, la fatturazione per le transizioni degli account importati viene gestita dall'azienda, ma i relativi utenti e risorse rimangono gli stessi. Per i dettagli, vedi [Importazione di account esistenti](/docs/account?topic=account-enterprise-add#add-accounts).

Per importare un account esistente, è necessario il seguente accesso:

* All'interno dell'account da importare, devi essere il proprietario dell'account o avere il ruolo di amministratore sui servizi di gestione dell'account di fatturazione e aziendale all'interno dell'account.
* Nell'account aziendale, devi avere il ruolo di editor o amministratore sul servizio aziendale e il ruolo di amministratore sul servizio di fatturazione.

Completa la seguente procedura per importare l'account UX-UI di esempio nel gruppo di account Design:
1. Dal dashboard dell'azienda fai clic su **Account** per visualizzare gli account e i gruppi di account nell'azienda.
2. Nella sezione Account, fai clic su **Aggiungi** > **Importa account**.
3. Seleziona **UX-UI** dall'elenco **Account**.

  Se non viene visualizzato alcun account, probabilmente non hai l'accesso corretto in nessuno degli account esistenti.
  {: tip}

4. Seleziona **Design** come elemento principale dell'account UX-UI. Questo determina dove si trova l'account nella gerarchia aziendale.
5. Controlla le informazioni sugli impatti sul tuo account e seleziona **Comprendo l'impatto sul mio account**. Quindi fai clic su **Importa**.

Ripeti la procedura per importare ulteriori account.

## Passo 4. Crea dei nuovi account
{: #create-accounts_tutorial}

Puoi creare dei nuovi account all'interno della tua azienda. Gli account vengono creati come account Pagamento a consumo e l'utilizzo viene fatturato all'azienda. Per creare un account, hai bisogno di una politica di accesso con il ruolo di editor o amministratore sul servizio aziendale.

Completa la seguente procedura per creare l'account Web di esempio nella tua azienda:

1. Dal dashboard dell'azienda fai clic su **Account** per visualizzare gli account e i gruppi di account nell'azienda.
1. Nella sezione Account, seleziona **Aggiungi** > **Crea account**.
1. Immetti `Web` come nome dell'account.
1. Se vuoi assegnare un nome diverso per il proprietario dell'account, immetti il suo ID IBM nel campo **Proprietario**. Il proprietario dell'account ha l'accesso completo per gestire l'account.
1. Seleziona **Marketing** come elemento principale di questo account.
1. Fai clic su **Create**.

Dopo aver creato l'account, il proprietario dell'account può accedere all'account per invitare altri utenti e gestire il loro accesso.

Ripeti la procedura per creare ulteriori account. Ad esempio, l'azienda Example Corp ha la seguente gerarchia di gruppi di account principali e account secondari.

|Elemento secondario|Elemento principale|
| ----- | -------|
| Print | Marketing |
| Frontend | Engineering |
| Backend | Engineering |
| Direct | Sales |
| Online | Sales |
| Enablement | Sales |
{:caption="Tabella 1. Gerarchia di gruppi di account principali e account secondari" caption-side="top"}

## Passo 5. Esplora le sottoscrizioni
{: #explore-sub_tutorial}

Puoi esplorare le sottoscrizioni nell'azienda dal dashboard aziendale. Tutte le sottoscrizioni esistenti dagli account importati nell'azienda vengono spostate nell'account aziendale e aggiunte al [pool di crediti](/docs/billing-usage?topic=billing-usage-enterprise#credit-pool) dell'azienda.

1. Torna al dashboard aziendale facendo clic su **Dashboard**. Nella sezione Fatturazione, puoi visualizzare il credito disponibile, il credito rimanente e le date di scadenza della sottoscrizione.
1. Per visualizzare i dettagli di tutte le sottoscrizioni nell'azienda, fai clic su **Visualizza sottoscrizioni**.

   Nella sezione Sottoscrizione piattaforma, puoi visualizzare la data di inizio, la data di fine, il credito iniziale e il credito disponibile della sottoscrizione. Per aggiungere ulteriori crediti, puoi acquistare ulteriori sottoscrizioni e applicare il codice di sottoscrizione.

## Passo 6. Assegna agli utenti negli account secondari l'accesso per creare le risorse
{: #users_create_resources}

Prima di cominciare, assicurati di passare all'account in cui vuoi creare la risorsa. In questo caso, passa all'account *Print*. Se vuoi che gli utenti nel tuo account creino le risorse dal catalogo e le assegnino a un gruppo di risorse, devi assegnare due tipi di politiche di accesso.
* Assegna una politica di accesso con il ruolo di visualizzatore o superiore sul gruppo di risorse.
* Assegna una politica di accesso con il ruolo di editor o amministratore sul servizio.

Completa la seguente procedura per assegnare l'accesso richiesto:

1. Vai a **Gestisci** > **Accesso (IAM)** e seleziona **Utenti**.
2. Seleziona un nome utente dall'elenco.
3. Fai clic sulla scheda **Politiche di accesso** > **Assegna accesso**.
4. Fai clic su **Assegna l'accesso in un gruppo di risorse**.
5. Seleziona il gruppo di risorse a cui vuoi assegnare l'accesso utente.
6. Seleziona il ruolo di visualizzatore o superiore sul gruppo di risorse.
7. Seleziona il servizio a cui vuoi assegnare l'accesso utente.
  * Se vuoi che l'utente sia in grado di eseguire il provisioning di tutti i servizi, seleziona **Tutti i servizi**.
  * Se vuoi assegnare all'utente un accesso specifico, seleziona un servizio dall'elenco. L'utente ha accesso solo al servizio selezionato.
8. Seleziona il ruolo di editor o amministratore.
9. Fai clic su **Assegna**.

## Passo 7. Visualizza l'utilizzo da tutti gli account
{: #usage_tutorial}

1. Accedi all'account dell'azienda Example Corp.
2. Vai a **Gestisci > Fatturazione e utilizzo** e seleziona **Utilizzo**.

   La pagina Utilizzo visualizza i costi di tutto l'utilizzo nella tua azienda, suddiviso per account e gruppo di account. Le informazioni di utilizzo per i servizi dell'infrastruttura classica non sono incluse nel periodo di fatturazione corrente. Per ulteriori informazioni, vedi [Visualizzazione dell'utilizzo per le tue risorse dell'infrastruttura classica](/docs/billing-usage?topic=billing-usage-infra-usage).
3. Fai clic su **Marketing** nella tabella per visualizzare l'utilizzo nel gruppo di account. In modo simile al livello aziendale, l'utilizzo viene suddiviso per account e gruppo di account.
4. Per visualizzare l'utilizzo per risorsa, vai al livello dell'account facendo clic sui gruppi di account nella tabella o selezionando l'account dal menu **Azienda**. I costi vengono mostrati per ogni tipo di risorsa utilizzata durante il periodo di tempo.

Ripeti la procedura per visualizzare l'utilizzo dei gruppi di account Development, Sales, Design e Engineering.

   Dall'account aziendale, non puoi visualizzare i dati di utilizzo per il piano o l'istanza della risorsa perché questo richiede l'accesso all'account. Fai clic su **Passa all'account** per visualizzare i dati dell'account. Hai bisogno dell'accesso di fatturazione alle risorse e ai servizi nell'account. Per ulteriori informazioni, vedi [Visualizzazione del tuo utilizzo](/docs/billing-usage?topic=billing-usage-viewingusage).

I dati vengono mostrati nell'account aziendale solo per l'utilizzo che si verifica per gli account nell'azienda. Per visualizzare l'utilizzo prima dell'aggiunta di un account all'azienda, accedi a tale account e seleziona il periodo di tempo pertinente.
{: note}
