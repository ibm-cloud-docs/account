---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-08"

keywords: create account, IBMid, sign up for account, sign up

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Registrazione a {{site.data.keyword.Bluemix_notm}}
{: #signup}

Puoi registrarti a un account {{site.data.keyword.Bluemix}} utilizzando il tuo ID IBM esistente o creandone uno nuovo. Se la tua azienda è registrata per utilizzare un ID federato per SSO (single sign-on), utilizza invece il tuo ID federato per registrarti.
{:shortdesc}

| ID di registrazione | Dettagli |    
|-----------------|---------|
|ID IBM esistente   | Se già disponi di un ID IBM, registrati a {{site.data.keyword.Bluemix_notm}} con le credenziali esistenti che utilizzi per i prodotti e servizi IBM. |
|Nuovo ID IBM        | Se non hai ancora un ID IBM, ne creerai uno al momento della registrazione. Con un ID IBM, puoi utilizzare un unico nome utente per accedere a tutti i prodotti e servizi IBM, incluso {{site.data.keyword.Bluemix_notm}}. |
|ID federato     | Se la tua azienda ha già richiesto di registrare le credenziali utente dal dominio aziendale con IBM, puoi registrarti a {{site.data.keyword.Bluemix_notm}} utilizzando le credenziali che usi già per l'accesso della tua azienda. Devi immettere un numero di telefono quando ti registri. |
{:caption="Tabella 1. Opzioni ID per la registrazione su {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Registrazione con un nuovo ID IBM o con uno esistente
{: #signup-ibmid}

Se non fai parte di un'azienda che utilizza ID federati, dovrai registrarti su {{site.data.keyword.Bluemix_notm}} con un ID IBM.

1. Vai alla [pagina di accesso {{site.data.keyword.Bluemix_notm}} ](https://cloud.ibm.com/){: new_window} ![Icona link esterno](../icons/launch-glyph.svg "Icona link esterno") e fai clic su **Crea un account {{site.data.keyword.Bluemix_notm}}**.
1. Immetti il tuo indirizzo email dell'ID IBM. Se non hai un ID IBM esistente, ne viene creato uno in base all'indirizzo email che inserisci. 
1. Completa i campi rimanenti con le tue informazioni e fai clic su **Crea account**.


## Registrazione con un ID federato
{: #signup-federated}

Un ID federato è un ID all'interno di un dominio aziendale che è registrato con IBM, in modo che le credenziali di dominio e utente possano essere utilizzate per accedere alle applicazioni Web. Puoi registrarti su {{site.data.keyword.Bluemix_notm}} con un ID federato solo se la tua azienda è già registrata con IBM. La registrazione di un dominio aziendale con IBM consente agli utenti di accedere a prodotti e servizi IBM utilizzando le proprie credenziali aziendali esistenti. L'autenticazione viene quindi gestita dal provider di identità della tua azienda utilizzando SSO.

IBM utilizza Security Assertion Markup Language 2.0 (SAML 2.0) per questa federazione dell'entità. SAML 2.0 è una versione standard per lo scambio di dati di autenticazione tra i domini di sicurezza. Si tratta di un protocollo basato su XML che utilizza un token di sicurezza contenente asserzioni per trasmettere informazioni tra il "Provider di identità" dell'organizzazione e "IBM Rely Party (RP)" altrimenti noto come Provider di servizi. 

Per informazioni su come registrare la tua azienda per un ID federato, vedi [IBMid Enterprise Federation Adoption Guide ![Icona link esterno](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window}. Quando richiedi di registrare gli ID federati, è necessario uno sponsor IBM, ad esempio un rappresentate di offerte o clienti.

### Accesso con un ID federato
{: #login-federated}

Quando accedi alla console {{site.data.keyword.Bluemix_notm}} con un ID federato, ti viene richiesto di accedere tramite la pagina di accesso della tua azienda. Se esegui l'accesso tramite una CLI, dovrai specificare altri parametri per eseguire l'autenticazione. Per ulteriori informazioni, vedi [Accesso con un ID federato](/docs/iam?topic=iam-federated_id).
