---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-18"

keywords: troubleshoot enterprise, enterprise problem, account problem, enterprise support, enterprise help, error message

subcollection: account
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Risoluzione dei problemi per un'azienda
{: #enterprise_help}

Problemi generali con la gestione della tua azienda possono includere degli errori quando tenti di applicare i tuoi codici di sottoscrizione e funzione o quando tenti di aggiungere un account all'azienda. In molti casi, puoi risolvere questi problemi seguendo pochi semplici passi.

## Perché non posso visualizzare l'intera azienda?
{: #troubleshoot-view-enterprise}
{: troubleshoot}

Se non visualizzi l'intera azienda, potresti dover controllare quale accesso ti è stato assegnato.

Puoi visualizzare alcuni account nell'azienda ma non l'intera gerarchia aziendale. La gerarchia aziendale mostra solo gli account a cui hai accesso, non l'intero account aziendale.
{: tsSymptoms}

Ti è stato assegnato l'accesso a solo alcuni account nell'azienda.
{: tsCauses}

Per controllare quale accesso ti è stato assegnato, completa la seguente procedura:
{: tsResolve}

1. Vai a **Gestisci** &gt; **Accesso (IAM)** > **Utenti**.
2. Seleziona il tuo nome.
2. Fai clic sulla scheda **Politiche di accesso**.

Contatta il proprietario dell'azienda per richiedere l'accesso corretto.

Se sei il proprietario dell'azienda, completa la seguente procedura per assegnare a un utente l'accesso all'intera azienda:
1. Vai a **Gestisci** > **Accesso (IAM)** > **Utenti**.
2. Seleziona il nome dell'utente. 
2. Fai clic sulla scheda **Politiche di accesso** > **Assegna accesso** > **Assegna l'accesso ai servizi di gestione dell'account**.
3. Seleziona **Azienda** come servizio e seleziona il nome della tua azienda.
4. Seleziona il gruppo di account o l'account nell'azienda a cui vuoi fornire l'accesso all'utente. Ad esempio, se vuoi che un utente abbia l'accesso per visualizzare un solo account, seleziona l'account e assegna all'utente il ruolo di visualizzatore o superiore. Se vuoi che un utente abbia l'accesso per visualizzare l'intera azienda, lascia la selezione di gruppo di account e account vuota e assegna l'accesso.

## Perché non posso aggiungere un account esistente all'azienda?
{: #troubleshoot-existing-enterprise}
{: troubleshoot}

Quando tenti di aggiungere un account esistente all'azienda, si verifica uno dei seguenti errori:
{: tsSymptoms}
* Quando fai clic su **Aggiungi account esistente** nella sezione Account, l'account che vuoi aggiungere non è elencato.
* Non hai l'opzione di fare clic su **Aggiungi account esistente**.

Non ti è stato assegnato l'accesso corretto.
{: tsCauses}

Se non puoi visualizzare l'account esistente elencato come opzione, hai bisogno del ruolo di amministratore sul servizio di fatturazione dell'account esistente.
{: tsResolve}

Per aggiungere un account esistente all'azienda, hai bisogno del ruolo di amministratore o editor sul servizio di fatturazione dell'azienda e il ruolo di amministratore o editor sul servizio dell'azienda per l'azienda o il gruppo di account principale.

## Perché non posso creare un nuovo account nell'azienda?
{: #troubleshoot-add-enterprise}
{: troubleshoot}

Non puoi fare clic su **Aggiungi account** nella sezione Account.
{: tsSymptoms}

Non ti è stato assegnato l'accesso corretto.
{: tsCauses}

Per creare un account nell'azienda, devi avere il seguente accesso.
{: tsResolve}
1. Ruolo di amministratore sul servizio di fatturazione dell'azienda.
2. Ruolo di amministratore o editor sul servizio dell'azienda per l'azienda o il gruppo di account principale di destinazione.

## Perché non posso visualizzare le sottoscrizioni aziendali?
{: #troubleshoot-viewsub-enterprise}
{: troubleshoot}

Quando visualizzi la pagina Sottoscrizioni da un account secondario, viene visualizzato il seguente messaggio:
{: tsSymptoms}

`Looks like you don't have permission to view subscription data for this account. Contact your account owner or administrator to request access.`

Il seguente messaggio viene visualizzato nella sezione Fatturazione sul tuo dashboard aziendale:

`Looks like you don't have permission to view this information. Learn more about IAM access.`

L'accesso alle informazioni di fatturazione e pagamento per i successivi periodi di fatturazione è limitato agli utenti nell'account aziendale. Gli utenti in un account secondario non possono accedere alle informazioni di fatturazione e pagamento, ad esempio le sottoscrizioni, anche se precedentemente ne avevano accesso nell'account.
{: tsCauses}

Per visualizzare o gestire la fatturazione, devi essere invitato nell'account aziendale e ti deve essere dato l'accesso al servizio di fatturazione in tale account. Contatta il proprietario dell'account per richiedere l'accesso.
{: tsResolve}

## Perché non posso applicare un codice di sottoscrizione al mio account?  
{: #troubleshoot-promo-enterprise}
{: troubleshoot}

Non puoi aggiungere un codice di sottoscrizione al tuo account perché non disponi dell'accesso corretto.  
{: tsSymptoms}

Poiché sei un account secondario sull'azienda, non puoi applicare i codici di sottoscrizione. I codici di sottoscrizione devono essere applicati al livello aziendale.
{: tsCauses}

Contatta il proprietario o l'amministratore dell'azienda per aggiungere il codice di sottoscrizione. Quando viene aggiunto il codice di sottoscrizione, si applica a tutti gli account nell'azienda. Per ulteriori informazioni, vedi [Gestione delle sottoscrizioni](/docs/billing-usage?topic=billing-usage-subscriptions).
{: tsResolve}
