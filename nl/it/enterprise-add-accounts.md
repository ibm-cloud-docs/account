---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise, add account, import account, create account

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Aggiunta di account a un'azienda
{: #enterprise-add}

Puoi creare la tua azienda aggiungendo ulteriori account {{site.data.keyword.Bluemix}} ad essa. Per aggiungere degli account, puoi importare degli account esistenti che sono in un'altra azienda oppure puoi creare dei nuovi account all'interno della tua azienda.
{:shortdesc}

Una volta che la tua azienda dispone di più account, puoi organizzare gli account correlati utilizzando i gruppi di account. Per ulteriori informazioni, vedi [Organizzazione degli account in un'azienda](/docs/account?topic=account-enterprise-organize).

## Importazione di account esistenti
{: #add-accounts}

Puoi importare degli account esistenti in un'azienda. Dopo aver importato un account, non può essere rimosso e ciascun account può far parte di solo un'azienda. Se importi un account Lite o di prova, ne viene automaticamente eseguito l'upgrade a un [account Pagamento a consumo](/docs/account?topic=account-accounts).

L'importazione di un account nell'azienda ha i seguenti impatti:
* La fatturazione per le transizioni dell'account viene gestita dall'azienda. Dopo la transizione, gli utenti nell'account non possono accedere alle informazioni di pagamento e fatturazione, come le fatture, i pagamenti o le sottoscrizioni per i successivi periodi di fatturazione. Per visualizzare o gestire la fatturazione, gli utenti devono essere invitati nell'account aziendale e gli deve essere dato l'accesso al servizio di fatturazione in tale account. Per ulteriori informazioni, vedi [Gestisci centralmente la fatturazione e l'utilizzo con le aziende](/docs/billing-usage?topic=billing-usage-enterprise).
* Gli utenti e le autorizzazioni di accesso all'interno dell'account non vengono modificati. L'accesso nell'account è separato dall'azienda e gli utenti non ottengono automaticamente l'accesso nell'azienda quando l'account viene importato.
* Le risorse all'interno dell'account non vengono modificate. Gli utenti con autorizzazioni di accesso corrette possono continuare a visualizzare le informazioni di utilizzo delle risorse nell'account.

Per importare degli account esistente in un'azienda, è necessario il seguente accesso:

   * Nell'account che deve essere importato, devi essere il proprietario dell'account o avere il ruolo di amministratore sul servizio di fatturazione all'interno dell'account.
   * Nell'account aziendale, devi avere il ruolo di editor o amministratore sul servizio aziendale e il ruolo di amministratore sul servizio di fatturazione.

Per importare un account esistente, completa la seguente procedura:

1. Accedi al tuo account aziendale e vai a **Gestisci > Azienda**.
1. Fai clic su **Account** per visualizzare gli account e i gruppi di account nell'azienda. Nella sezione Account, seleziona **Aggiungi > Importa account**.
1. Seleziona l'account che vuoi importare.

   Se non viene visualizzato alcun account, probabilmente non hai l'accesso corretto in nessuno degli account esistenti.
   {: tip}
1. Se vuoi aggiungere l'account a un gruppo di account, seleziona il gruppo di account che ne deve essere l'elemento principale. L'elemento principale che selezioni determina dove si trova l'account nella gerarchia aziendale.
1. Controlla le informazioni sugli impatti sul tuo account e seleziona **Comprendo l'impatto sul mio account**. Quindi fai clic su **Importa**.

   Dopo che l'account è stato importato nell'azienda, non può essere rimosso. Devi essere sicuro di spostare in modo permanente l'account nell'azienda.
   {: important}

### Importazione degli account utilizzando la CLI
{: #add-account-cli}

1. Trova l'ID dell'account che vuoi importare nell'azienda.

   ```
   ibmcloud account list
   ```
   {: codeblock}
1. Se vuoi aggiungere l'account a un gruppo di account, trova i nomi e gli ID dei gruppi di account esistenti nell'azienda.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. Importa l'account nell'azienda, specificando l'ID account per il parametro `--account ID`. Se non specifichi un gruppo di account principale, l'account viene aggiunto direttamente sotto il livello dell'azienda.

   ```
   ibmcloud enterprise account-import --account-id ID
   [--parent-account-group ACCOUNT_GROUP_NAME | --parent-account-group-id ACCOUNT_GROUP_ID]
   ```
   {: codeblock}

### Importazione degli account utilizzando l'API
{: #add-account-api}

Per importare un account esistente nell'azienda, richiama l'[API Enterprise Management](https://{DomainName}/apidocs/enterprise-apis/enterprise#import-an-account-into-an-enterprise){: external} come mostrato nella seguente richiesta di esempio. Sostituisci le variabili ID e il token {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) con i valori dalla tua azienda.

```
curl -X PUT \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID/import/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" -H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID"
}'
```
{: codeblock}

## Creazione di nuovi account
{: #create-accounts}

Puoi creare dei nuovi account all'interno della tua azienda. Gli account vengono creati come account Pagamento a consumo e l'utilizzo viene fatturato all'azienda. Per creare un account, hai bisogno di una politica di accesso con il ruolo di editor o amministratore sul servizio aziendale.

1. Dal dashboard dell'azienda fai clic su **Account** per visualizzare gli account e i gruppi di account nell'azienda.
1. Nella sezione Account, seleziona **Aggiungi > Crea account**.
1. Immetti un nome per l'account che sia univoco nell'azienda. Poiché è uno dei tanti account, un nome univoco e descrittivo ti aiuta a comprendere immediatamente lo scopo dell'account.
1. Se vuoi assegnare un nome diverso per il proprietario dell'account, immetti il suo ID IBM nel campo **Proprietario**. Il proprietario dell'account ha l'accesso completo per gestire l'account.
1. Se vuoi aggiungere l'account a un gruppo di account, seleziona il gruppo di account che ne deve essere l'elemento principale. L'elemento principale che scegli determina dove si trova l'account nella gerarchia aziendale.
1. Fai clic su **Create**.

Dopo aver creato l'account, il proprietario dell'account può accedere all'account per invitare altri utenti e gestire il loro accesso.

### Creazione degli account utilizzando la CLI
{: #create-accounts-cli}

1. Se vuoi aggiungere l'account a un gruppo di account, trova i nomi e gli ID dei gruppi di account esistenti.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. Crea l'account immettendo il seguente comando. Se non specifichi un gruppo di account principale, l'account viene aggiunto direttamente sotto il livello dell'azienda. Per rendere un altro utente il proprietario dell'account, specifica il suo ID IBM nell'opzione `--owner`.

   ```
   ibmcloud enterprise account-create NAME
   [--parent-account-group ACCOUNT_GROUP_NAME] [--owner USER_ID]
   ```
   {: codeblock}

### Creazione degli account utilizzando l'API
{: #create-account-api}

Per creare un nuovo account nell'azienda, richiama l'API Enterprise Management come mostrato nella seguente richiesta di esempio, sostituendo le variabili ID e il token IAM con i valori dalla tua azienda. Per informazioni dettagliate sull'API, vedi [API Enterprise Management](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-a-new-account-in-an-enterprise){: external}.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/accounts \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID",
  "name": "Sample Account",
  "owner_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}
