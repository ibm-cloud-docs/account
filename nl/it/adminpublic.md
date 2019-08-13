---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: create account, IBMid, sign up for account, sign up

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Registrazione a {{site.data.keyword.Bluemix_notm}}
{: #signup}

Puoi registrarti per un account {{site.data.keyword.Bluemix}} utilizzando il tuo ID IBM esistente o creando un nuovo ID IBM. Se la tua società è registrata per utilizzare un ID federato per SSO (single sign-on), registrati invece con il tuo ID federato.
{:shortdesc}

| ID di registrazione | Dettagli |    
|-----------------|---------|
|ID IBM esistente   | Se già disponi di un ID IBM, registrati a {{site.data.keyword.Bluemix_notm}} con le credenziali esistenti che utilizzi per i prodotti e servizi IBM. |
|Nuovo ID IBM        |Se non hai ancora un ID IBM, ne creerai uno quando ti registri. Con un ID IBM, puoi utilizzare un unico nome utente per accedere a tutti i prodotti e servizi IBM, incluso {{site.data.keyword.Bluemix_notm}}. |
|ID federato     | Se la tua azienda ha già richiesto di registrare le credenziali utente dal dominio aziendale con IBM, puoi registrarti a {{site.data.keyword.Bluemix_notm}} utilizzando le credenziali che usi già per l'accesso della tua azienda. Devi immettere un numero di telefono quando ti registri. |
{:caption="Tabella 1. Opzioni di ID per la registrazione a {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Registrazione con un ID IBM nuovo o esistente
{: #signup-ibmid}

Se non fai parte di una società che utilizza gli ID federati, ti registrerai a {{site.data.keyword.Bluemix_notm}} con un ID IBM.

1. Vai alla [pagina di accesso {{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com/){: new_window} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno") e fai clic su **Crea un account {{site.data.keyword.Bluemix_notm}}**.
1. Immetti il tuo indirizzo email dell'ID IBM. Se non hai un ID IBM esistente, viene creato un ID basato sull'email che immetti.
1. Completa i campi rimanenti con le tue informazioni e fai clic su **Crea account**.
1. Conferma il tuo account facendo clic sul link nell'email di conferma inviata all'indirizzo email fornito.

Se riscontri dei problemi durante l'accesso con il nuovo account, vedi [Risoluzione dei problemi relativi all'accesso a {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-accessing).

## Registrazione con un ID federato
{: #signup-federated}

Un ID federato è un ID all'interno di un dominio aziendale che è registrato con IBM, in modo che le credenziali di dominio e utente possano essere utilizzate per accedere alle applicazioni Web. Puoi registrati in {{site.data.keyword.Bluemix_notm}} con un ID federato solo se la tua società è già registrata con IBM. La registrazione di un dominio aziendale con IBM consente agli utenti di accedere a prodotti e servizi IBM utilizzando le proprie credenziali aziendali esistenti. L'autenticazione viene quindi gestita dal provider di identità della tua società utilizzando SSO. 

IBM utilizza Security Assertion Markup Language 2.0 (SAML 2.0) per questa federazione dell'entità. SAML 2.0 è una versione standard per lo scambio di dati di autenticazione tra i domini di sicurezza. Si tratta di un protocollo basato su XML che utilizza un token di sicurezza contenente asserzioni per trasmettere informazioni tra il "Provider di identità" dell'organizzazione e "IBM RP (Rely Party)", altrimenti noto come Provider di servizi.

Per informazioni su come registrare la tua società per un ID federato, vedi [IBMid Enterprise Federation Adoption Guide ![Icona link esterno](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window}. Quando richiedi di registrare gli ID federati, è necessario uno sponsor IBM, ad esempio un rappresentate di offerte o clienti.

### Accesso con un ID federato
{: #login-federated}

Quando accedi alla console {{site.data.keyword.Bluemix_notm}} con un ID federato, ti viene richiesto di accedere tramite la pagina di accesso della tua azienda. Se accedi tramite la console, dovrai specificare degli ulteriori parametri per l'autenticazione. Per ulteriori informazioni, vedi [Accesso con un ID federato](/docs/iam?topic=iam-federated_id).
