---

copyright:

  years: 2017, 2018
lastupdated: "2017-11-21"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Gestione dell'accesso al catalogo
{: #find-access}

In qualità di proprietario dell'account, potresti voler assegnare l'accesso utilizzando una politica IAM per consentire agli utenti nel tuo account di controllare la visibilità dei servizi privati aggiunti al catalogo dell'account o dei servizi pubblici che sono stati creati nell'account. Per impostazione predefinita, solo il proprietario dell'account ha la possibilità di completare queste attività.

## Come posso delegare l'accesso come proprietario dell'account?
{: #get-access}

Se sei un proprietario di account, puoi concedere l'accesso a un utente nel tuo account tramite l'interfaccia utente di Identità e accesso assegnando una politica di accesso. Per garantire che l'utente abbia l'accesso necessario, seleziona la risorsa **Catalogo globale** e il ruolo **Amministratore** per la politica di accesso.

Potresti voler concedere altre autorizzazioni agli utenti nel tuo account utilizzando i ruoli IAM (Identity and Access Management) di `visualizzatore` ed `editor`. Esamina la seguente tabella per ulteriori informazioni su ciò che ciascun ruolo IAM consente di fare a un utente nel contesto del catalogo per il tuo account.

| Ruolo di gestione della piattaforma | Descrizione delle azioni |
|:-----------------|:-----------------|
| Visualizzatore | Può vedere i servizi privati, anche se l'account non è stato incluso, ma non può apportare modifiche. |
| Editor | Può apportare modifiche ai metadati dell'oggetto ma non può modificare la visibilità. |
| Amministratore | Può modificare i metadati dell'oggetto o la visibilità.  |
{: caption="Tabella 1. Ruoli e azioni di esempio per la gestione della piattaforma per il servizio del catalogo" caption-side="top"}

Per istruzioni dettagliate sull'assegnazione dell'accesso agli utenti nel tuo account, vai alla documentazione [Accesso alle risorse](/docs/iam/mngiam.html#iammanidaccser#resourceaccess).


## Come verifico se dispongo dell'accesso?

Quando vieni aggiunto all'account di un'altra persona, ti potrebbero delegare determinati livelli di accesso in modo da poter visualizzare le risorse private che sono state aggiunte all'account. Il proprietario dell'account ti potrebbe anche delegare la possibilità di gestire chi vede le risorse pubbliche nel catalogo dell'account. Non hai questo accesso per impostazione predefinita. Il proprietario dell'account deve concederti un ruolo IAM che ti consenta di avere accesso per completare queste attività di gestione delle risorse dell'account.

Puoi utilizzare la CLI o l'interfaccia utente di Identità e accesso per determinare se disponi dell'accesso per consentire a utenti specifici di visualizzare una risorsa privata che è stata aggiunta all'account.

Per utilizzare l'interfaccia utente di Identità e accesso, completa la seguente procedura:

1. Vai a **Gestisci** > **Sicurezza** > **Identità e accesso** e fai clic su **Utenti**.
2. Fai clic sul tuo nome dall'elenco Utenti.
3. Nella sezione **Politiche di accesso**, puoi visualizzare le tue politiche di accesso assegnate. Devi disporre del ruolo di amministratore Cloud IAM per la risorsa del catalogo nel tuo account per aggiornare l'elenco che include gli account e per visualizzare le risorse private nel catalogo.

Per utilizzare la [CLI bx](/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_iam), completa la seguente procedura:

Immetti il seguente comando con il tuo nome utente `bx iam user-policies <your-username>` per scoprire se sei un amministratore degli account selezionati nella CLI. Se non sei un amministratore per il tuo account, questi comandi restituiscono un errore che indica che non sei autorizzato.
{: tip}
