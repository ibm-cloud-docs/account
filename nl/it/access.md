---

copyright:

  years: 2017, 2019
lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Gestione dell'accesso utente al catalogo
{: #find-access}

In qualità di proprietario dell'account {{site.data.keyword.Bluemix}}, puoi assegnare agli utenti l'accesso al catalogo utilizzando una politica {{site.data.keyword.Bluemix_notm}} IAM (Identity and Access Management). Puoi controllare la visibilità dei servizi privati aggiunti al catalogo dell'account o dei servizi pubblici creati nell'account. Per impostazione predefinita, solo il proprietario dell'account può completare queste attività.

## Delega dell'accesso
{: #get-access}

Puoi delegare l'accesso sul tuo account per controllare cosa possono vedere gli utenti e per controllare di quanta autorizzazione detti utenti dispongono. Ad esempio, alcune informazioni potrebbero essere appropriate per la lettura e l'analisi solo per un utente mentre a un altro utente potrebbe essere concessa l'autorizzazione di modificare tali informazioni. Per delegare l'accesso all'account a un altro utente nell'account, completa la seguente procedura.

1. Fai clic su **Gestisci** > **Accesso (IAM)**.
2. Fai clic su **L'accesso inizia con l'utente** nella pagina di destinazione.
3. Seleziona un utente nel tuo account.
4. Fai clic su **Politiche di accesso**.
5. Fai clic su **Assegna accesso**. Fai quindi clic su **Assegna l'accesso ai servizi di gestione account**.
6. Seleziona il **Catalogo risorse globali** dall'elenco Servizi e il ruolo **Amministratore** dall'elenco Seleziona i ruoli.

Per concedere altre autorizzazioni, utilizza i ruoli Visualizzatore ed Editor. Esamina la seguente tabella per ulteriori informazioni su ciò che ciascun ruolo IAM consente di fare a un utente nel contesto del catalogo per il tuo account.

| Ruolo di gestione della piattaforma | Azioni                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| Visualizzatore                   | Può visualizzare i servizi privati ma non può modificarli.                                                            |
| Editor                   | Può modificare i metadati dell'oggetto ma non può modificare la visibilità per i servizi privati.                                |
| Amministratore            | Può modificare i metadati dell'oggetto o la visibilità per i servizi privati e limitare la visibilità di un servizio pubblico.  |
{: caption="Tabella 1. Ruoli e azioni di esempio di gestione della piattaforma per il catalogo" caption-side="top"}

Per ulteriori informazioni sull'assegnazione dell'accesso agli utenti, vedi [Assegnazione dell'accesso ai servizi di gestione dell'account](/docs/iam?topic=iam-account-services).

## Conferma del tuo accesso
{: #confirm-access}

Quando vieni aggiunto all'account di un'altra persona, gli amministratori dell'account ti potrebbero delegare dei livelli di accesso in modo da consentirti di visualizzare le risorse private che sono state aggiunte all'account. Il proprietario dell'account potrebbe anche indicare la delega per chi può visualizzare le risorse pubbliche nel catalogo dell'account. Non hai questo accesso per impostazione predefinita. Il proprietario dell'account può concederti un ruolo IAM in modo da consentirti di disporre dell'accesso per completare queste attività di gestione delle risorse dell'account.

Puoi utilizzare la console {{site.data.keyword.Bluemix_notm}} o l'interfaccia riga di comando (CLI, command-line interface) per determinare se disponi dell'accesso per abilitare specifici utenti a visualizzare una risorsa privata nell'account.

Per utilizzare la console, completa la seguente procedura:

  1. Vai a **Gestisci > Accesso (IAM)**.
  2. Fai clic sul tuo nome dall'elenco Utenti.
  3. Fai clic sulla scheda **Politiche di accesso**, in cui puoi visualizzare le tue politiche di accesso assegnate. Devi disporre del ruolo di amministratore Cloud IAM per la risorsa del catalogo nel tuo account per aggiornare l'elenco che include gli account e per visualizzare le risorse private nel catalogo.


Per utilizzare la [CLI](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_iam#ibmcloud_commands_iam), esegui il comando `ibmcloud iam user-policies <your-user-name>`. Il comando restituisce un errore se non sei un amministratore per l'account.
