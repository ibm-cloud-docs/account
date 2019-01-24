---

copyright:

  years: 2017, 2018
lastupdated: "2018-11-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}


# Öffentliche Ressource für Benutzer ausblenden
{: #exclude}

Als Administrator für Ihr {{site.data.keyword.Bluemix}}-Konto können Sie eine öffentliche Ressource für Benutzer ausblenden, die über Zugriff auf das Konto verfügen. Das Ausblenden von Ressourcen kann erfolgen, um zu verhindern, dass nicht berechtigte Benutzer sensible Informationen anzeigen können. Ein anderer Grund kann sein, dass auf bestimmte Informationen nur eine begrenzte Zahl von Personen zugreifen muss.
{:shortdesc}

Durch das Ausblenden einer Ressource im Katalog wird diese Ressource nicht aus der Cloud Foundry-Befehlszeilenschnittstelle (CLI) oder aus den Angebotskategorielisten entfernt, die über die {{site.data.keyword.Bluemix_notm}}-Konsolennavigation verfügbar sind (z. B. Finanzen, Mobile, Watson und Web-Apps).
{: note}

Über die [Befehlszeilenschnittstelle (CLI)](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set) oder die Konsole von {{site.data.keyword.Bluemix}} können Sie ermitteln, ob Sie über die erforderliche Zugriffsberechtigung verfügen, um Benutzern das Anzeigen einer privaten Ressource zu ermöglichen, die zum Konto hinzugefügt wurde. Als Kontoeigner können Sie einem Benutzer in Ihrem Konto die Zugriffsberechtigung über die Konsole erteilen, indem Sie eine Zugriffsrichtlinie zuweisen. Weitere Informationen finden Sie in [Zugriff auf Konto verwalten](access.html).

## Ressource suchen
{: #find-resource}

Führen Sie den Befehl `ibmcloud catalog search <service-id or service-name>` aus, um nach einer Ressource zu suchen. Ersetzen Sie die Variable 'service-id or service-name' durch den Namen oder die ID einer Ressource. Mithilfe der zurückgegebenen Informationen können Sie nach der ID oder dem Namen des Service suchen, der ausgeblendet werden soll. 

## Details der Ressource abrufen

Führen Sie den Befehl `ibmcloud catalog service <service-id or service-name>` aus. Verwenden Sie diesen Befehl, um mithilfe der mit dem vorherigen Befehl ermittelten Informationen weitere Details zu der Ressource abzurufen. Mit den zurückgegebenen Informationen können Sie die Hierarchie anzeigen, die Aufschluss über die untergeordneten Ressourcen der Elemente in Ihrer Ressource gibt. 

## Ressource ausblenden
{: #vis-exc}

Führen Sie den folgenden Befehl aus, um zu verhindern, dass Benutzer in Ihrem Konto eine öffentliche Ressource anzeigen. 

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

Nach dem Flag 'exclude' können Sie eine durch Kommas getrennte Liste mit E-Mail-Adressen oder Konto-IDs hinzufügen, die Konten zugeordnet sind. 

Der Prozess für das Ausblenden der Ressource nimmt nach der Befehlseingabe etwa 30 Minuten in Anspruch. Melden Sie sich nach 30 Minuten ab und erneut an Ihrem Konto an, um die ausgeblendete Ressource anzuzeigen. 

Einträge, die Sie ausblenden, sind in der Konsole oder in der Befehlszeilenschnittstelle nicht verfügbar. Administratoren des ausgeschlossenen Kontos können die Ressource weiterhin anzeigen. {: note}

## Konto aus der Ausschlussliste entfernen
{: #remove-exclude}

Führen Sie den folgenden Befehl aus, um eine Konto-ID oder E-Mail-Adresse aus der Ausschlussliste zu entfernen. 

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`


## Beispiel: Sichtbarkeit untergeordneter Objekte verwalten
{: #child}

Sie können die Sichtbarkeit Ihrer gesamten Ressourcen verwalten. Die einzelnen untergeordneten Ressourcen verfügen über eigene Sichtbarkeitsmerkmale. Dieses Beispiel zeigt, wie Sie ein Konto vom Cloudant-Service ausschließen können. 

Führen Sie den Befehl `ibmcloud catalog service cloudant` aus, um alle untergeordneten Elemente der Ressource anzuzeigen. 

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

Suchen Sie die ID für ein Objekt und schließen Sie ein Konto aus, indem Sie den Befehl `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>` ausführen. 

Weitere Informationen zur Funktionsweise der Sichtbarkeit finden Sie in den [Katalog-API-Dokumenten](https://{DomainName}/apidocs/globalcatalog). 
