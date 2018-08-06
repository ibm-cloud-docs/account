---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Modifica della proprietà delle risorse private

Puoi modificare la proprietà dell'account tramite l'interfaccia della riga di comando. Dopo aver creato e personalizzato le risorse private nel tuo catalogo, puoi trasferire la proprietà di tali risorse a qualcun altro. Dopo aver trasferito la proprietà, non sarai in grado di vedere la risorsa dal tuo account. La modifica della proprietà dell'account non può essere annullata, quindi fai attenzione.
{:shortdesc: .shortdesc}

## Come cambiare il proprietario di una risorsa del catalogo

Per cambiare il proprietario di una risorsa, mediante la [CLI](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_settings) utilizza il seguente comando:

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
