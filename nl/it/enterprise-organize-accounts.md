---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, create account group, organize accounts, move accounts

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Organizzazione degli account in un'azienda
{: #enterprise-organize}

Utilizza i gruppi di account per organizzare gli account correlati nella tua azienda {{site.data.keyword.Bluemix}}. Puoi creare una gerarchia aziendale a più livelli nidificando i gruppi di account all'interno di un gruppo di account. Se lo fai, puoi riorganizzare spostando gli account tra i gruppi di account.
{:shortdesc}

Ad esempio, il seguente diagramma raffigura un'azienda con quattro livelli che puoi configurare nidificando i gruppi di account. In primo luogo, crea due gruppi di account che hanno l'azienda come loro elemento principale. Successivamente, puoi creare due ulteriori gruppi di account che hanno uno di quei due gruppi di account come elemento principale. Puoi liberamente spostare gli account all'interno dei gruppi di account, a prescindere dal livello in cui sono. Tuttavia, i gruppi di account non possono essere spostati.

![Un diagramma che mostra quattro livelli aziendali. Il livello principale è l'azienda, che contiene due livelli di gruppi di account. Quindi il gruppo di account contiene gli account.](images/enterprise-hierarchy.svg "I livelli aziendali vengono creati aggiungendo i gruppi di account.")

Ricorda che come organizzi la tua azienda ha impatto su come puoi tenere traccia dei costi di utilizzo. Per ulteriori informazioni, vedi [Gestisci centralmente la fatturazione e l'utilizzo con le aziende](/docs/billing-usage?topic=billing-usage-enterprise).
{: tip}

## Creazione dei gruppi di account
{: #create-account-group}

Per creare un gruppo di account, hai bisogno del ruolo di amministratore o editor sul servizio aziendale nell'account aziendale.

1. Dal dashboard dell'azienda fai clic su **Account** per visualizzare gli account e i gruppi di account nell'azienda.
1. Nella sezione Gruppi di account, fai clic su **Crea**.
1. Immetti un nome per il gruppo di account che rispecchia gli account che conterrà. Vedi [Come posso utilizzare un'azienda?](/docs/account?topic=account-enterprise#enterprise-use-cases) per degli esempi su come puoi organizzare gli account.
1. Se vuoi che un utente aziendale diverso da te sia il contatto primario per il gruppo di account, seleziona il suo ID IBM dal menu **Contatti**. Se un utente che vuoi assegnare come contatto primario non è nell'azienda, lo devi prima invitare nell'account aziendale. Il contatto non può essere modificato dopo che crei il gruppo di account. Per ulteriori informazioni, vedi [Invito di utenti](/docs/iam?topic=iam-iamuserinv).

   Il contatto è diverso rispetto a un proprietario dell'account perché non dispone di alcun accesso aggiuntivo nel gruppo di account o nei suoi account. L'utente che selezioni come contatto funge da punto focale per tutti i problemi relativi al gruppo di account. Ad esempio, se un direttore finanziario nota che i costi di utilizzo del gruppo di account sono inaspettatamente elevati, potrebbe avvertire il contatto del gruppo di account.


1. Se vuoi che il gruppo di account sia in una parte diversa della tua gerarchia aziendale, seleziona un elemento principale diverso.

  I gruppi di account non possono essere eliminati o spostati da dove li crei.
  {: note}
1. Fai clic su **Create**.

Per creare un nuovo livello nella tua gerarchia aziendale, crea dei nuovi gruppi di account all'interno del gruppo di account. Puoi spostare gli account che sono già nell'azienda nel gruppo di account o puoi importare o creare degli account in esso. Vedi [Aggiunta di account a un'azienda](/docs/account?topic=account-enterprise-add) per ulteriori informazioni sull'importazione e la creazione degli account.

### Creazione dei gruppi di account utilizzando la CLI
{: #create-account-groups-cli}

Crea un gruppo di account immettendo il seguente comando. Per nidificare un gruppo di account all'interno di un altro gruppo di account, specifica il nome del gruppo di account nell'opzione `--parent-account-group`. Se vuoi che un altro utente sia il contatto del gruppo di account, specifica il suo ID IBM nell'opzione `--primary-contact-id`.

```
ibmcloud enterprise account-group-create NAME
[--parent-account-group ACCOUNT_GROUP_NAME] [--primary-contact-id USER_ID]
```
{: codeblock}

### Creazione dei gruppi di account utilizzando l'API
{: #create-account-groups-api}

Puoi creare in modo programmatico un gruppo di account nell'azienda richiamando l'API Enterprise Management.

La seguente richiesta di esempio crea un gruppo di account direttamente sotto il livello dell'azienda. Quando richiami l'API, sostituisci le variabili ID con i valori dalla tua azienda. Per nidificare un gruppo di account all'interno di un altro gruppo di account, specifica l'ID del gruppo di account nel CRN (Cloud Resource Name) nel seguente formato: `crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID`.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/account-groups \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID",
  "name": "Sample Account Group",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-account-group){: external}.-->

## Spostamento degli account all'interno dell'azienda
{: #move-accounts}

Puoi spostare gli account ovunque all'interno dell'azienda. Ad esempio, puoi spostare un account da un gruppo di account inferiore nel gruppo di account principale oppure muoverlo direttamente sotto l'azienda. Gli account possono essere spostati solo all'interno dell'azienda. Non possono essere spostati in una azienda diversa o rimossi dall'azienda per andare in un account autonomo.

Per spostare un account, devi avere il ruolo di amministratore sul servizio di fatturazione nell'account aziendale e il ruolo di editor o amministratore per l'intera azienda o per i gruppi di account corrente e di destinazione.

1. Dal dashboard aziendale, fai clic su **Account**.
1. Nella sezione Account, fai clic sull'icona Azioni nella riga dell'account e seleziona **Sposta account**.
1. Seleziona un nuovo elemento principale per l'account e fai clic su **Salva**.

### Spostamento di un account utilizzando la CLI
{: #move-accounts-cli}

1. Trova l'ID e il nome account elencando tutti gli account nella tua azienda.

   ```
   ibmcloud enterprise accounts --recursive
   ```
   {: codeblock}
1. Se stai spostando l'account in un gruppo di account, trova l'ID e il nome del gruppo di account.

   ```
   ibmcloud enterprise account-groups
   ```
   {: codeblock}
1. Sposta l'account specificando il nuovo elemento principale nell'opzione correlata.

   Per spostare l'account in un gruppo di account, specifica il nome del gruppo di account nell'opzione `--parent-account-group`.

   ```
   ibmcloud enterprise account-move -n NAME --parent-account-group ACCOUNT_GROUP_NAME
   ```
   {: codeblock}

   Per spostare l'account direttamente sotto l'azienda, specifica l'opzione `--parent-enterprise`.

   ```
   ibmcloud enterprise account-move -n NAME --parent-enterprise
   ```
   {: codeblock}

### Spostamento degli account utilizzando l'API
{: #move-account-api}

Puoi spostare un account richiamando l'API Enterprise Management come mostrato nella seguente richiesta di esempio. Sostituisci le variabili ID e il token IAM con i valori dalla tua azienda.

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_1"",
}'
```
{: codeblock}

<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#move-an-account-with-the-enterprise){: external}. -->
