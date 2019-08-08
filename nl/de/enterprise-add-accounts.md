---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, add account, import account, create account

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Konten zu einem Unternehmen hinzufügen
{: #enterprise-add}

Sie können Ihr Unternehmen erweitern, indem Sie zusätzliche {{site.data.keyword.Bluemix}}-Konten zu diesem Unternehmen hinzufügen. Zum Hinzufügen von Konten können Sie vorhandene Konten importieren, die nicht in einem anderen Unternehmen enthalten sind, oder Sie können neue Konten in Ihrem Unternehmen erstellen.
{:shortdesc}

Wenn Ihr Unternehmen über mehrere Konten verfügt, können Sie zugehörige Konten unter Verwendung von Kontogruppen organisieren. Weitere Informationen finden Sie unter [Konten in einem Unternehmen organisieren](/docs/account?topic=account-enterprise-organize).

## Vorhandene Konten importieren
{: #add-accounts}

Sie können vorhandene Konten in ein Unternehmen importieren. Nachdem Sie ein Konto importiert haben, kann es nicht mehr entfernt werden, und jedes Konto kann nur Teil eines einzigen Unternehmens sein. Wenn Sie ein Lite- oder Testkonto importieren, wird automatisch ein Upgrade auf ein [nutzungsabhängiges Konto](/docs/account?topic=account-accounts) durchgeführt.

Wenn Sie ein Konto in das Unternehmen importieren, hat das die folgenden Auswirkungen:
* Die Abrechnung für das Konto geht an das Unternehmen über. Nach der Übertragung können die Benutzer für zukünftige Abrechnungszeiträume in dem Konto nicht auf Abrechnungs- und Zahlungsinformationen (wie z. B. Rechnungen, Zahlungen oder Abonnements) zugreifen. Zum Anzeigen oder Verwalten der Abrechnung müssen die Benutzer für das Unternehmenskonto eingeladen werden und in diesem Konto Zugriff auf den Abrechnungsservice erhalten. Weitere Informationen dazu finden Sie unter [Abrechnung und Nutzung zentral mit Unternehmen verwalten](/docs/billing-usage?topic=billing-usage-enterprise).
* Benutzer- und Zugriffsberechtigungen in dem Konto werden nicht geändert. Der Zugriff im Konto ist vom Unternehmen getrennt und die Benutzer erhalten nicht automatisch Zugriff im Unternehmen, wenn das Konto importiert wird.
* Die Ressourcen innerhalb des Kontos werden nicht geändert. Benutzer mit den richtigen Zugriffsberechtigungen können weiterhin Nutzungsinformationen für die Ressourcen in dem Konto anzeigen.

Um vorhandene Konten in ein Unternehmen zu importieren, ist der folgende Zugriff erforderlich:

   * In dem zu importierenden Konto müssen Sie der Kontoeigner sein oder die Rolle "Administrator" für den Abrechnungsservice in dem Konto haben.
   * Im Unternehmenskonto benötigen Sie die Rolle "Bearbeiter" oder "Administrator" für den Unternehmensservice und die Rolle "Administrator" für den Abrechnungsservice.

Führen Sie die folgenden Schritte aus, um ein vorhandenes Konto zu importieren:

1. Melden Sie sich bei Ihrem Unternehmenskonto an und wechseln Sie zu **Verwalten > Unternehmen**.
1. Klicken Sie auf **Konten**, um die Konten und Kontogruppen im Unternehmen anzuzeigen. Wählen Sie **Hinzufügen > Konto importieren** im Abschnitt "Konten" aus.
1. Wählen Sie das Konto aus, das Sie importieren möchten.

   Wenn keine Konten angezeigt werden, haben Sie wahrscheinlich nicht den richtigen Zugriff auf die vorhandenen Konten.
   {: tip}
1. Wenn Sie das Konto zu einer Kontogruppe hinzufügen möchten, wählen Sie die Kontogruppe als übergeordnetes Element aus. Das übergeordnete Element, das Sie auswählen, bestimmt, wo sich das Konto in der Unternehmenshierarchie befindet.
1. Lesen Sie die Informationen zu den Auswirkungen auf Ihr Konto und wählen Sie **Ich bin mir über die Auswirkungen auf mein Konto im Klaren** aus. Klicken Sie anschließend auf **Importieren**.

   Nachdem das Konto in das Unternehmen importiert wurde, kann es nicht mehr entfernt werden. Stellen Sie sicher, dass Sie das Konto dauerhaft in das Unternehmen verschieben möchten.
   {: important}

### Konten über die Befehlszeilenschnittstelle (CLI) importieren
{: #add-account-cli}

1. Suchen Sie die ID des Kontos, das Sie in das Unternehmen importieren möchten.

   ```
   ibmcloud account list
   ```
   {: codeblock}
1. Wenn Sie das Konto zu einer Kontogruppe hinzufügen möchten, suchen Sie die Namen und IDs der vorhandenen Kontogruppen im Unternehmen.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. Importieren Sie das Konto in das Unternehmen und geben Sie dafür die Konto-ID für den Parameter `--account ID` an. Wenn Sie keine übergeordnete Kontogruppe angeben, wird das Konto direkt unter dem Unternehmen hinzugefügt.

   ```
   ibmcloud enterprise account-import --account-id ID
   [--parent-account-group ACCOUNT_GROUP_NAME | --parent-account-group-id ACCOUNT_GROUP_ID]
   ```
   {: codeblock}

### Konten über die Anwendungsprogrammierschnittstelle (API) importieren
{: #add-account-api}

Wenn Sie ein vorhandenes Konto in das Unternehmen importieren möchten, rufen Sie die <!-- [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#import-an-account-into-an-enterprise){: external}--> Enterprise Management API auf, wie dies in der folgenden Beispielanforderung dargestellt ist. Ersetzen Sie das IAM-Token (IAM = Identity and Access Management) und die ID-Variablen von {{site.data.keyword.Bluemix_notm}} durch die Werte aus Ihrem Unternehmen.

```
curl -X PUT \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID/import/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" -H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID"
}'
```
{: codeblock}

## Neue Konten erstellen
{: #create-accounts}

Sie können neue Konten in Ihrem Unternehmen erstellen. Die Konten werden als nutzungsabhängige Konten erstellt und die Nutzung wird dem Unternehmen in Rechnung gestellt. Um ein Konto zu erstellen, benötigen Sie eine Zugriffsrichtlinie mit der Rolle "Bearbeiter" oder "Administrator" für den Unternehmensservice.

1. Klicken Sie im Dashboard für das Unternehmen auf **Konten**, um die Konten und Kontogruppen im Unternehmen anzuzeigen.
1. Wählen Sie **Hinzufügen > Konto erstellen** im Abschnitt "Konten" aus.
1. Geben Sie einen Namen für das Konto ein, der innerhalb des Unternehmens eindeutig ist. Da es sich um eines von vielen Konten handelt, hilft Ihnen ein eindeutiger, beschreibender Name, den Zweck des Kontos auf einen Blick zu erkennen.
1. Wenn Sie einen anderen Benutzer als den Kontoeigner zuordnen möchten, geben Sie die betreffende IBMid im Feld **Eigner** ein. Der Kontoeigner hat vollständigen Zugriff für die Verwaltung des Kontos.
1. Wenn Sie das Konto zu einer Kontogruppe hinzufügen möchten, wählen Sie die Kontogruppe als übergeordnetes Element aus. Das übergeordnete Element, das Sie auswählen, bestimmt, wo sich das Konto in der Unternehmenshierarchie befindet.
1. Klicken Sie auf **Erstellen**.

Nachdem Sie das Konto erstellt haben, kann sich der Kontoeigner bei dem Konto anmelden, um andere Benutzer einzuladen und deren Zugriff zu verwalten.

### Konten über die Befehlszeilenschnittstelle (CLI) erstellen
{: #create-accounts-cli}

1. Wenn Sie das Konto zu einer Kontogruppe hinzufügen möchten, suchen Sie die Namen und IDs der vorhandenen Kontogruppen.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. Erstellen Sie das Konto, indem Sie den folgenden Befehl ausführen. Wenn Sie keine übergeordnete Kontogruppe angeben, wird das Konto direkt unter dem Unternehmen hinzugefügt. Wenn Sie einen anderen Benutzer zum Kontoeigner machen wollen, geben Sie die entsprechende IBMid für die Option `-- owner` an.

   ```
   ibmcloud enterprise account-create NAME
   [--parent-account-group ACCOUNT_GROUP_NAME] [--owner USER_ID]
   ```
   {: codeblock}

### Konten über die Anwendungsprogrammierschnittstelle (API) erstellen
{: #create-account-api}

Wenn Sie ein neues Konto im Unternehmen erstellen möchten, rufen Sie die Enterprise Management API wie in der folgenden Beispielanforderung auf und ersetzen Sie das IAM-Token und ID-Variablen durch die Werte von Ihrem Unternehmen ersetzen. <!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-a-new-account-in-an-enterprise){: external}. -->

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/accounts \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID",
  "name": "Sample Account",
  "owner_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}
