---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, multiple account

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Unternehmen erstellen
{: #create-enterprise}

Sie können ein {{site.data.keyword.Bluemix}}-Unternehmen aus einem vorhandenen Abonnementkonto erstellen. Das Konto, das Sie zur Erstellung des Unternehmens verwenden, wird dem Unternehmen permanent hinzugefügt.
{:shortdesc}

## Vorbereitende Schritte
{: #create-prereqs}

Um ein [{{site.data.keyword.Bluemix_notm}}-Unternehmen](/docs/account?topic=account-enterprise) zu erstellen, müssen Sie der Kontoeigner sein oder über die Rolle "Administrator" für den Abrechnungskontoverwaltungsservice in einem Abonnementkonto verfügen.

Das Abonnementkonto, das Sie zur Erstellung des Unternehmens verwenden, wird permanent in das Unternehmen verschoben. Wenn Sie ein Konto in das Unternehmen verschieben, hat das die folgenden Auswirkungen:
* Die Abrechnung für das Konto [geht an das Unternehmen über](/docs/billing-usage?topic=billing-usage-enterprise). Nach der Übertragung können die Benutzer für zukünftige Abrechnungszeiträume in dem Konto nicht auf Abrechnungs- und Zahlungsinformationen (wie z. B. Rechnungen, Zahlungen oder Abonnements) zugreifen. Zum Anzeigen oder Verwalten der Abrechnung müssen die Benutzer für das Unternehmenskonto eingeladen werden und in diesem Konto Zugriff auf den Abrechnungsservice erhalten.
* Benutzer- und Zugriffsberechtigungen in dem Konto werden nicht geändert. Der Zugriff im Konto ist vom Unternehmen getrennt und die Benutzer erhalten nicht automatisch Zugriff im Unternehmen, wenn das Konto hinzugefügt wird. Allerdings sind die Abrechnungsinformationen, wie bereits erwähnt, unabhängig von den Zugriffsberechtigungen nicht mehr im Konto verfügbar.
* Die Ressourcen innerhalb des Kontos werden nicht geändert. Benutzer mit den richtigen Zugriffsberechtigungen können weiterhin Nutzungsinformationen für die Ressourcen in dem Konto anzeigen.

Wenn Sie kein Abonnementkonto haben, können Sie ein Upgrade für Ihr Konto durchführen (eine Beschreibung dazu finden Sie unter [Upgrade für Konto durchführen](/docs/account?topic=account-upgrading-account)).

## Unternehmen in der Konsole erstellen
{: #create-console}

1. Rufen Sie **Verwalten > Unternehmen** auf und klicken Sie auf **Erstellen**.
1. Geben Sie einen eindeutigen Namen ein, um Ihr Unternehmen zu identifizieren. In der Regel spiegelt der Name Ihr Unternehmen oder Ihre Organisation wider, z. B. `My organization's enterprise`. Sie können den Unternehmensnamen später bei Bedarf bearbeiten.
1. Wenn Ihr Unternehmen oder Ihre Organisation einen zugehörigen Domänennamen hat, geben Sie ihn im Feld **Domäne** ein. Sie können ein beliebiges Domänen- oder Unterdomänenformat angeben, z. B. `example.com` oder `my.example.com`.
1. Lesen Sie die Informationen zu den Auswirkungen auf Ihr Konto und wählen Sie **Ich bin mir über die Auswirkungen auf mein Konto im Klaren** aus. Klicken Sie anschließend auf **Erstellen**.

   Nachdem das Konto zum Unternehmen hinzugefügt wurde, kann es nicht mehr entfernt werden. Stellen Sie sicher, dass Sie das Konto dauerhaft in ein Unternehmen verschieben möchten.
   {: important}

Nach einer kurzen Zeit wird Ihr Unternehmen erstellt und Sie können das Dashboard für das Unternehmen anzeigen. Ihre IBMid wird als Kontakt aufgelistet. Der Kontakt dient als Ansprechpartner für alle das Unternehmen betreffenden Fragen, z. B. zu Abrechnung und Nutzung. Sie sind außerdem als Eigner des Unternehmenskontos zugewiesen, sodass Sie zusätzliche Benutzer für die Verwaltung des Unternehmens einladen können.

Klicken Sie auf **Konten**, um die Unternehmenshierarchie anzuzeigen, die zwei Konten enthält.

* Das Unternehmenskonto, über das Sie Benutzer einladen und Zugriff für die Verwaltung des Unternehmens erteilen.
* Das Konto, das Sie zur Erstellung des Unternehmens verwendet haben. Seine Benutzer und Ressourcen bleiben gleich, aber die Abrechnung erfolgt jetzt durch das Unternehmen.

## Unternehmen über die Befehlszeilenschnittstelle (CLI) erstellen
{: #create-cli}

1. Melden Sie sich an und wählen Sie das Konto aus.

   ```
   ibmcloud login
   ```
   {:codeblock}
1. Erstellen Sie das Unternehmen, indem Sie den folgenden Befehl ausführen, wobei `NAME` für einen eindeutigen Namen zur Identifizierung des Unternehmens steht.

   ```
   ibmcloud enterprise create NAME [-d, --domain DOMAIN_NAME] [--primary-contact-id PRIMARY_CONTACT_USER_ID]
   ```
   {:codeblock}

   Der folgende Befehl erstellt beispielsweise ein Unternehmen mit dem Namen `Example Corp Enterprise` mit der Domäne `examplecorp.com`.

   ```
   ibmcloud enterprise create "Example Corp Enterprise" -d examplecorp.com
   ```
   {:codeblock}

   Standardmäßig wird das Unternehmen mit dem derzeit angemeldeten Benutzer in den folgenden Rollen erstellt:
      * Als Kontakt für das Unternehmen, der einen zentralen Ansprechpartner identifiziert, der bei unternehmensbezogenen Fragestellungen zurate gezogen wird
      * Als Eigner des Unternehmenskontos, der über uneingeschränkten Zugriff auf dieses Konto verfügt

   Sie können die IBMid für einen anderen Benutzer in der Option `--primary-contact-id` angeben. Beiden Rollen wird derselbe Benutzer zugewiesen.
1. Prüfen Sie eventuelle Auswirkungen auf Ihr Konto und bestätigen Sie, dass Sie den Vorgang fortsetzen möchten, indem Sie `y` eingeben.
   ```
   Account abcde12345fghij67890 will be incorporated into enterprise My new enterprise
   (which cannot be undone). Do you want to proceed? [y/N]> y
   ```

Nachdem das Unternehmen erstellt wurde, werden zwei neue IDs angezeigt. Die erste ID ist dem Unternehmen zugeordnet und die zweite ID gibt das Unternehmenskonto an, das Sie für die Verwaltung des Unternehmens verwenden.

```
ID:                      09876jihgf54321edcba   
Enterprise Account ID:   edcba12345jihgf67890
```

Das Konto, das Sie zum Erstellen des Unternehmens verwendet haben, ist jetzt Teil des Unternehmens. Führen Sie den Befehl [`ibmcloud enterprise accounts`](/docs/cli?topic=cloud-cli-ibmcloud_enterprise#ibmcloud_enterprise_accounts) aus, um diese beiden Konten in Ihrem Unternehmen anzuzeigen: das Unternehmenskonto und das Konto, das Sie zum Erstellen des Unternehmens verwendet haben.

## Unternehmen über die Anwendungsprogrammierschnittstelle (API) erstellen
{: #create-api}

Sie können ein Unternehmen über das Programm erstellen, indem Sie die Enterprise Management API aufrufen, wie dies in der folgenden Beispielanforderung dargestellt wird. <!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-enterprise){: external}.-->

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/enterprises \
-H "Authorization: Bearer <Token>" \
-H 'Content-Type: application/json' \
-d '{
  "source_account_id": "a1b2c32a5ea94809a9840f5e23c362d",
  "name": "Sample Enterprise",
  "domain": "example.com",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

## Nächste Schritte
{: #create-next-steps}

Erweitern Sie Ihre Unternehmensstruktur, indem Sie mehr vorhandene Konten hinzufügen oder neue Konten in Ihrem Unternehmen erstellen. Weitere Informationen finden Sie unter [Konten zu einem Unternehmen hinzufügen](/docs/account?topic=account-enterprise-add).

Sie können auch zusätzliche Benutzer für das Unternehmenskonto einladen, sodass diese bei der Verwaltung des Unternehmens mitwirken können. Beispielsweise könnten Sie einen Finanzverantwortlichen dazu einladen, die Abrechnung durchzuführen und die Nutzungskosten zu verfolgen, und Sie könnten Abteilungsleiter zur Verwaltung von Konten einladen. Weitere Informationen zum Einladen von Benutzern finden Sie unter [Benutzer einladen](/docs/iam?topic=iam-iamuserinv).
