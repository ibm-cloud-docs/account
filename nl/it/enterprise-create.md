---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, multiple account

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Creazione di un'azienda
{: #create-enterprise}

Crea un'azienda {{site.data.keyword.Bluemix}} da un account Sottoscrizione esistente. L'account che utilizzi per creare l'azienda viene aggiunto in modo permanente all'azienda.
{:shortdesc}

## Prima di iniziare
{: #create-prereqs}

Per creare un'[azienda {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-enterprise), devi essere il proprietario dell'account o avere il ruolo di amministratore sul servizio di gestione dell'account di fatturazione in un account Sottoscrizione.

L'account Sottoscrizione che utilizzi per creare l'azienda viene spostato in modo permanente nell'azienda. Lo spostamento dell'account nell'azienda ha i seguenti impatti:
* La fatturazione per le transizioni dell'account viene [gestita dall'azienda](/docs/billing-usage?topic=billing-usage-enterprise). Dopo la transizione, gli utenti nell'account non possono accedere alle informazioni di pagamento e fatturazione, come le fatture, i pagamenti o le sottoscrizioni per i successivi periodi di fatturazione. Per visualizzare o gestire la fatturazione, gli utenti devono essere invitati nell'account aziendale e gli deve essere dato l'accesso al servizio di fatturazione in tale account.
* Gli utenti e le autorizzazioni di accesso all'interno dell'account non vengono modificati. L'accesso nell'account è separato dall'azienda e gli utenti non ottengono automaticamente l'accesso nell'azienda quando l'account viene aggiunto. Tuttavia, come precedentemente menzionato, le informazioni di fatturazione non sono più disponibili nell'account indipendentemente dalle autorizzazioni di accesso.
* Le risorse all'interno dell'account non vengono modificate. Gli utenti con autorizzazioni di accesso corrette possono continuare a visualizzare le informazioni di utilizzo delle risorse nell'account.

Se non hai un account Sottoscrizione, puoi eseguire l'upgrade del tuo account come descritto in [Upgrade del tuo account](/docs/account?topic=account-upgrading-account).

## Creazione di un'azienda nella console
{: #create-console}

1. Vai a **Gestisci > Azienda** e fai clic su **Crea**.
1. Immetti un nome univoco per identificare la tua azienda. Normalmente, il nome rispecchia la tua azienda o organizzazione, ad esempio `My organization's enterprise`. Puoi modificare il nome dell'azienda in un secondo momento se necessario.
1. Se la tua società o organizzazione ha un nome di dominio associato, immettilo nel campo **Dominio**. Puoi specificare qualsiasi formato di dominio o dominio secondario, ad esempio `example.com` o `my.example.com`.
1. Controlla le informazioni sull'impatto sul tuo account e seleziona **Comprendo l'impatto sul mio account**. Quindi, fai clic su **Crea**.

   Dopo che l'account è stato aggiunto nell'azienda, non può essere rimosso. Devi essere sicuro di spostare in modo permanente l'account in un'azienda.
   {: important}

Dopo alcuni istanti, la tua azienda viene creata e puoi visualizzarne il dashboard. Il tuo ID IBM viene elencato come contatto. Il contatto funge da punto focale per tutto ciò che riguarda l'azienda, come le domande sulla fatturazione o l'utilizzo. Vieni anche assegnato come proprietario dell'account aziendale, per cui puoi invitare ulteriori utenti per gestire l'azienda.

Fai clic su **Account** per visualizzare la tua gerarchia aziendale, la quale contiene due account.

* L'account aziendale, che è dove inviti gli utenti e concedi l'accesso per gestire l'azienda.
* L'account che hai utilizzato per creare l'azienda. I suoi utenti e risorse rimangono gli stessi, ma la fatturazione viene ora gestita dall'azienda.

## Creazione di un'azienda utilizzando la CLI
{: #create-cli}

1. Accedi e seleziona l'account.

   ```
   ibmcloud login
   ```
   {:codeblock}
1. Crea l'azienda eseguendo il seguente comando, dove `NAME` è un nome univoco per identificare l'azienda.

   ```
   ibmcloud enterprise create NAME [-d, --domain DOMAIN_NAME] [--primary-contact-id PRIMARY_CONTACT_USER_ID]
   ```
   {:codeblock}

   Ad esempio, il seguente comando crea un'azienda denominata `Example Corp Enterprise` con il dominio `examplecorp.com`.

   ```
   ibmcloud enterprise create "Example Corp Enterprise" -d examplecorp.com
   ```
   {:codeblock}

   Per impostazione predefinita, l'azienda viene creata con l'utente che ha attualmente eseguito l'accesso nei seguenti ruoli:
      * Il contatto dell'azienda, che identifica un responsabile da contattare per tutto ciò che riguarda l'azienda.
      * Il proprietario dell'account aziendale, che ha l'accesso completo per gestire l'account aziendale.

   Puoi specificare l'ID IBM di un altro utente nell'opzione `--primary-contact-id`. Allo stesso utente vengono assegnati entrambi i ruoli.
1. Controlla l'impatto sul tuo account e conferma che vuoi procedere immettendo `y`.
   ```
   Account abcde12345fghij67890 will be incorporated into enterprise My new enterprise
   (which cannot be undone). Do you want to proceed? [y/N]> y
   ```

Dopo aver creato l'azienda, vengono visualizzati due nuovi ID. Il primo ID è associato all'azienda e il secondo identifica l'account aziendale, che utilizzi per gestire l'azienda.

```
ID:                      09876jihgf54321edcba   
Enterprise Account ID:   edcba12345jihgf67890
```

L'account che hai utilizzato per creare l'azienda fa ora parte dell'azienda. Esegui il comando [`ibmcloud enterprise accounts`](/docs/cli?topic=cloud-cli-ibmcloud_enterprise#ibmcloud_enterprise_accounts) per visualizzare i due account nella tua azienda: l'account aziendale e quello utilizzato per creare l'azienda.

## Creazione di un'azienda utilizzando l'API
{: #create-api}

Puoi creare in modo programmatico un'azienda richiamando l'API Enterprise Management come mostrato nella seguente richiesta di esempio. Per informazioni dettagliate sull'API, vedi [API Enterprise Management](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-enterprise){: external}.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/enterprises \
-H "Authorization: Bearer <Token>" \
-H 'Content-Type: application/json' \
-d '{
  "source_account_id": "a1b2c32a5ea94809a9840f5e23c362d",
  "name": "Sample Enterprise",
  "domain": "example.com",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

## Passi successivi
{: #create-next-steps}

Crea la tua struttura aziendale aggiungendo ulteriori account esistenti o creandone di nuovi all'interno della tua azienda. Per ulteriori informazioni, vedi [Aggiunta di account alla tua azienda](/docs/account?topic=account-enterprise-add).

Puoi anche invitare ulteriori utenti nell'account aziendale in modo che ti possano aiutare a gestire l'azienda. Ad esempio, potresti voler invitare un direttore finanziario per gestire la fatturazione e tenere traccia dei costi di utilizzo e invitare dei responsabili di settore per amministrare gli account. Vedi [Invito di utenti](/docs/iam?topic=iam-iamuserinv) per ulteriori informazioni su come invitare gli utenti.
