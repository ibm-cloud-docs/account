---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Eigentumsrecht für private Ressourcen ändern

Sie können das Eigentumsrecht für Konten über die Befehlszeilenschnittstelle ändern. Nach dem Erstellen und Anpassen privater Ressourcen in Ihrem Katalog können Sie das Eigentum an diesen Ressourcen an andere übertragen. Nach der Übertragung des Eigentums wird Ihnen die Ressource über Ihr eigenes Konto nicht mehr angezeigt. Änderungen am Eigentumsrecht für ein Konto können nicht rückgängig gemacht werden. Es ist somit Vorsicht geboten.
{:shortdesc: .shortdesc}

## Katalogressourceneigner ändern

Ändern Sie den Eigner einer Ressource über die [Befehlszeilenschnittstelle (CLI)](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_settings) mit dem folgenden Befehl:

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
