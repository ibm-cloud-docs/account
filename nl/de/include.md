---

copyright:

  years: 2017, 2019
lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Konten zur privaten Ressource hinzufügen
{: #include}

Der Zugriff auf jede private {{site.data.keyword.Bluemix}}-Ressource, die Sie erstellen, ist standardmäßig eingeschränkt. Als Administrator des Kontos können Sie die Benutzer auswählen, denen Ihre Ressource angezeigt wird, indem Sie diese Benutzer zu einer Einschlussliste hinzufügen.
{:shortdesc: .shortdesc}

Über die [Befehlszeilenschnittstelle (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) oder die Konsole von {{site.data.keyword.Bluemix}} können Sie ermitteln, ob Sie über die erforderliche Zugriffsberechtigung verfügen, um Benutzern das Anzeigen einer privaten Ressource zu ermöglichen, die zum Konto hinzugefügt wurde. Als Kontoeigner können Sie einem Benutzer in Ihrem Konto die Zugriffsberechtigung über die Konsole erteilen, indem Sie eine Zugriffsrichtlinie zuweisen. Weitere Informationen finden Sie in [Zugriff auf Konto verwalten](/docs/account?topic=account-find-access).

## Eigene Ressource suchen
{: #find-resource}

Führen Sie den Befehl `ibmcloud catalog service <service-id or service-name>` aus. Ersetzen Sie die Variable 'service-id or service-name' durch den Namen oder die ID Ihrer Ressource. Verwenden Sie die zurückgegebenen Informationen zum Anzeigen der Hierarchie, in der die untergeordneten Ressourcen der Elemente in Ihrer Ressource enthalten sind.

## Sichtbarkeit durch das Einbeziehen eines Kontos festlegen
{: #vis-inc}

Führen Sie den folgenden Befehl aus, um es einem Konto zu ermöglichen, Ihre private Ressource anzuzeigen.

`ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

Geben Sie im Anschluss an das Flag 'includes-add' eine durch Kommas unterteilte Aufzählung von E-Mail-Adressen oder IDs an, die Konten zugeordnet sind.

Der Prozess für das Einbeziehen der Ressource nimmt nach der Befehlseingabe etwa 30 Minuten in Anspruch. Melden Sie sich nach 30 Minuten ab und erneut mit Ihrem Konto an, um die aufgenommene Ressource angezeigt zu bekommen.

## Konto aus der Einschlussliste entfernen
{: #remove-exclude}

Führen Sie den folgenden Befehl aus, um ein Konto aus der Einschlussliste zu entfernen.

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## Beispiel: Sichtbarkeit untergeordneter Objekte verwalten
{: #child-vis}

Sie können die Sichtbarkeit Ihrer Ressource und der untergeordneten Elemente verwalten. Ist die Einschlussliste leer, bedeutet das, dass sie nur den Administratoren des Kontos angezeigt wird. Ihr Konto muss in der Einschlussliste für alle Mitglieder des Kontos enthalten sein, damit sie angezeigt wird.

Das folgende Beispiel veranschaulicht, wie der Befehl `ibmcloud catalog service cloudant` ausgeführt werden kann, um die untergeordneten Elemente einer Cloudant-Serviceinstanz anzuzeigen.

```
ID                 cloudant
Name               cloudantnosqldb
Kind               service
Provider           IBM
Tags               data_management, ibm_created, ibm_dedicated_public, lite
Active             true
Description        Cloudant NoSQL DB is a fully managed data layer designed for modern web and mobile applications that leverages a flexible JSON schema. Cloudant is built upon and compatible with Apache CouchDB and accessible through a secure HTTPS API, which scales as your application grows. Cloudant is ISO27001 and SOC2 Type 1 certified, and all data is stored in triplicate across separate physical nodes in a cluster for HA/DR within a data center.
Bindable           true
RC Compatible      false
RC Provisionable   false
Children           Name                                          Kind         ID                                               Location
                   lite                                          plan         cloudant-lite
                   |__lite-eu-gb                             deployment   cloudant-lite:eu-gb                          eu-gb
                   |  |__lite-alias-eu-gb                    alias        cloudant-lite:alias:eu-gb                    eu-gb
                   |__lite-us-south                          deployment   cloudant-lite:us-south                       us-south
                      |__lite-alias-us-south                 alias        cloudant-lite:alias:us-south                 us-south
                   standard                                      plan         cloudant-standard
                   |__standard-eu-gb                         deployment   cloudant-standard:eu-gb                      eu-gb
                   |  |__standard-alias-eu-gb                alias        cloudant-standard:alias:eu-gb                eu-gb
                   |__standard-us-south                      deployment   cloudant-standard:us-south                   us-south
                      |__standard-alias-us-south             alias        cloudant-standard:alias:us-south             us-south
```

Sie können die Ressourcen-ID für die untergeordnete Bereitstellung abrufen und anschließend mit dem folgenden Befehl ein Konto einbeziehen:

`ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`

Die untergeordneten Elemente eines Objekts können die Sichtbarkeit übernehmen. Diese Vererbung ist jedoch relativ komplex. Ist das untergeordnete Objekt privat, wird die zugehörigen eigene Sichtbarkeitskonfiguration angewendet. Ist das untergeordnete Objekt jedoch als öffentlich konfiguriert, wird die Sichtbarkeit des übergeordneten Elements übernommen. Durch das Festlegen der Sichtbarkeit eines privaten untergeordneten Objekts wird die Sichtbarkeit möglicherweise auf mehr als das übergeordnete Objekt eingeschränkt. Weitere Informationen zur Funktionsweise der Sichtbarkeit finden Sie in den [Katalog-API-Dokumenten](https://{DomainName}/apidocs/globalcatalog).

## Eigentumsrecht für eine private Ressource übertragen
{: #owners}

Beim Verlassen Ihres Projekts oder Ihrer Organisation können Sie das Eigentumsrecht für Ihr Konto einer anderen Person übertraten.
{:shortdesc}

Nachdem Sie das Eigentumsrecht übertragen haben, können Sie die Ressource nicht mehr von Ihrem Konto aus anzeigen. Stellen Sie sicher, dass Sie das Eigentumsrecht übertragen möchten, da diese Aktion nicht rückgängig gemacht werden kann.
{: important}

Sie können die [{{site.data.keyword.Bluemix}}-Befehlszeilenschnittstelle (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) verwenden, um das Eigentumsrecht für eine private Ressource zu übertragen. Führen Sie den folgenden Befehl aus:

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
