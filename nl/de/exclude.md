---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Öffentliche Ressource für Benutzer im Konto ausblenden
{: #exclude}

Als Administrator des Kontos können Sie festlegen, dass eine öffentliche Ressource den Benutzern in Ihrem Konto nicht angezeigt wird. Fügen Sie die Ressource über die [Befehzlszeilenschnittstelle](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set) `ibmcloud` zu einer Ausschlussliste hinzu.
{:shortdesc: .shortdesc}

**Hinweis:** Das Ausblenden einer Ressource im Katalog bewirkt nicht, dass die Ressource aus der Cloud Foundry-Befehlszeilenschnittstelle oder den Servicebereitstellungslisten entfernt wird, die über die globale Navigation verfügbar sind (z. B. Finanzen, Mobile, Watson und Web-Apps).

## Wie kann ich feststellen, ob ich über Zugriff verfüge?
{: #find-access}

Sie können über die Befehlszeilenschnittstelle oder die IAM-Benutzerschnittstelle ermitteln, ob Sie über den erforderlichen Zugriff verfügen, um dafür zu sorgen, dass Benutzern eine private Ressource angezeigt wird, die dem Konto hinzugefügt wurde. Als Kontoeigner können Sie einem Benutzer in Ihrem Konto über die IAM-Benutzerschnittstelle Zugriff erteilen, indem Sie eine Zugriffsrichtlinie zuordnen. Weitere Informationen finden Sie in [Zugriff auf Konto verwalten](access.html).

## Schritt 1: Ressource suchen
{: #find-resource}

Geben Sie `ibmcloud catalog search <service-id or service-name>` ein, um eine Ressource zu suchen. Ersetzen Sie 'service-id or service-name' durch den Namen oder die ID einer Ressource. Suchen Sie den Namen bzw. die ID des Service, der ausgeblendet werden soll, in den zurückgegebenen Informationen.

## Schritt 2: Details zum Service abrufen

Geben Sie den Befehl `ibmcloud catalog service <service-id or service-name>` ein. Verwenden Sie diesen Befehl, um mithilfe der mit dem vorherigen Befehl ermittelten Informationen weitere Details zu der Ressource zu untersuchen. In den zurückgegebenen Informationen wird die Hierarchie angezeigt, die Aufschluss über die untergeordneten Ressourcen der Elemente in Ihrer Ressource gibt.

## Schritt 3: Ressource ausblenden
{: #vis-exc}

Geben Sie den folgenden Befehl ein, um zu verhindern, dass Ihrem Konto eine öffentliche Ressource angezeigt wird.

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

Nach dem Flag `excludes` können Sie eine durch Kommas getrennte Liste mit E-Mail-Adressen oder IDs angeben, die Konten zugeordnet sind.

Der Prozess für das Ausblenden der Ressource nimmt nach der Befehlseingabe etwa 30 Minuten in Anspruch. Melden Sie sich nach 30 Minuten ab und erneut mit Ihrem Konto an, um die ausgeblendete Ressource anzuzeigen.

**Hinweis:** Einträge, die von Ihnen ausgeblendet wurden, stehen nicht über die Benutzerschnittstelle oder die {{site.data.keyword.Bluemix}}-Befehlszeilenschnittstelle zur Verfügung. Die ausgeblendeten Einträge werden weiterhin im Cloud Foundry-Marktplatz angezeigt, ein ausgeblendeter Plan kann jedoch nicht über Cloud Foundry bereitgestellt werden. Administratoren des ausgeschlossenen Kontos wird die Ressource weiterhin angezeigt.

## Konto aus Ausschlussliste entfernen
{: #remove-exclude}

Geben Sie den folgenden Befehl ein, um eine Konto-ID oder E-Mail-Adresse aus der Ausschlussliste zu entfernen.

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`

## Beispiel zum Verwalten der Sichtbarkeit untergeordneter Objekte
{: #child}

Sie können die Sichtbarkeit Ihrer gesamten Ressourcen verwalten. Die einzelnen untergeordneten Ressourcen verfügen über eigene Sichtbarkeitsmerkmale.

Bei dem folgenden Beispiel schließen Sie ein Konto vom öffentlichen Cloudant-Service aus.

Die Eingabe von `ibmcloud catalog service cloudant` bewirkt, dass die untergeordneten Elemente der Ressource angezeigt werden.

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

Suchen Sie die ID für ein Objekt und schließen Sie das Konto mit dem Befehl `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

Weitere Informationen zur Sichtbarkeit finden Sie in der [API-Dokumentation](https://console.bluemix.net/apidocs/globalcatalog).
