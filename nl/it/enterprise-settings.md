---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise settings, manage enterprise, view enterprise, rename enterprise

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Gestione della tua azienda
{: #enterprise-settings}

Dal dashboard della tua azienda {{site.data.keyword.Bluemix}}, puoi visualizzare i dettagli dell'azienda, effettuare azioni comuni come aggiungere e invitare gli utenti e visualizzare le informazioni di fatturazione. Puoi anche ridenominare la tua azienda sul dashboard tramite la CLI o l'API.
{:shortdesc}

Per gestire le impostazioni aziendali, hai bisogno del ruolo di amministratore o editor sul servizio aziendale nell'account aziendale.
{: tip}

## Gestione della tua azienda nella console
{: #enterprise-manage}

Per visualizzare il tuo dashboard aziendale, vai a **Gestisci > Azienda**. Il dashboard fornisce una panoramica di account, utenti e credito di sottoscrizione nella tua azienda. Il dashboard ha link rapidi in modo da poter eseguire le seguenti azioni comuni:
   * [Aggiungi account nuovi o esistenti alla tua azienda](/docs/account?topic=account-enterprise-add)
   * [Invita gli utenti nell'account aziendale](/docs/iam?topic=iam-iamuserinv)
   * [Visualizza e gestisci il credito di sottoscrizione](/docs/billing-usage?topic=billing-usage-subscriptions)

Inoltre, puoi ridenominare la tua azienda facendo clic su **Ridenomina** nella sezione dei dettagli dell'azienda.

## Gestione della tua azienda dalla CLI
{: #enterprise-manage-cli}

* Visualizza le informazioni sull'azienda come il nome, il dominio, il proprietario e le date di creazione e aggiornamento.

  ```
  ibmcloud enterprise show
  ```
  {: codeblock}
* Ridenomina l'azienda specificando il nuovo nome con l'opzione `-n` nel seguente comando.

   ```
   ibmcloud enterprise update -n NEW_NAME
   ```
   {:codeblock}

## Gestione della tua azienda utilizzando l'API
{: #enterprise-manage-api}

Puoi aggiornare in modo programmatico un'azienda richiamando l'API Enterprise Management come mostrato nella seguente richiesta di esempio. Puoi aggiornare il nome o il dominio dell'azienda passando i nuovi valori sulla chiamata API. Per informazioni dettagliate sull'API, vedi la [documentazione API Enterprise Management](https://{DomainName}/apidocs/enterprise-apis/enterprise#update-an-enterprise){: external}.

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID" \
-H "Authorization: $IAM_TOKEN" \
-H 'Content-Type: application/json' \
-d '{
  "name": "Brand New Sample Enterprise",
  "domain": "new.example.com"
}'
```
