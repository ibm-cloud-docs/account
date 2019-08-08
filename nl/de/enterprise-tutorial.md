---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, enterprise users, enterprise access, enterprise tutorial

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Einführung in Unternehmen
{: #enterprise-tutorial}

Dieses Lernprogramm führt Sie durch das Einrichten eines Unternehmens (Enterprise) nach Abteilung, damit Sie die Nutzungskosten für mehrere {{site.data.keyword.Bluemix}}-Konten verwalten und verfolgen können. Wenn Sie dieses Lernprogramm ausführen, erfahren Sie, wie Sie ein Unternehmen erstellen, Konten hinzufügen und diese in Kontogruppen organisieren, Benutzer einladen und Abonnements durchsuchen können.
{:shortdesc}

Im Lernprogramm wird eine fiktive Firma mit dem Namen *Example Corp* verwendet, die ein Unternehmen mit der im Folgenden beschriebenen Struktur erstellen möchte. Wenn Sie das Lernprogramm ausführen, passen Sie jeden Schritt an die Konten Ihres Unternehmens und die gewünschte Struktur an.

![Ein Unternehmen mit vier Ebenen, das die Konten nach Abteilung in einer Organisation gruppiert. Kontogruppen erhalten Bezeichnungen wie beispielsweise 'Marketing', 'Development' und 'Sales'. Die Kontogruppen enthalten Konten für Teams innerhalb dieser Abteilungen. Die Kontogruppe 'Sales' enthält z. B. Konten für ?'Direct', 'Online' und 'Enablement'.](images/enterprise-by-dept.svg "Ein Unternehmen, das Konten nach Abteilung in der Organisation organisiert.")

## Vorbereitende Schritte
{: #setting-prereqs}

Der Abschnitt [Was ist ein Unternehmen?](/docs/account?topic=account-enterprise) enthält grundlegende Informationen dazu, wie die Kontoverwaltung, Abrechnung, Ressourcen sowie das Benutzer- und Zugriffsmanagement in einem Unternehmen funktionieren.

Stellen Sie sicher, dass Sie über den erforderlichen Zugriff in einem Abonnementkonto verfügen, das als Basiskonto dient, von dem aus Sie das Unternehmen erstellen. Um ein Unternehmen zu erstellen, müssen Sie der Kontoeigner sein oder über die Rolle "Administrator" für den Abrechnungskontoverwaltungsservice verfügen.

Das Erstellen eines Unternehmens aus einem Konto und das Importieren vorhandener Konten kann nicht rückgängig gemacht werden. Dieses Lernprogramm zeigt beispielhaft die Schritte, die Sie ausführen können, um ein Unternehmen nach Abteilung zu konfigurieren, aber Sie sollten Ihre Unternehmensstruktur sorgfältig für die Anforderungen Ihrer Organisation planen.
{:important}

## Schritt 1. Unternehmen erstellen
{: #create_enterprise_tutorial}

Unternehmen werden aus einem vorhandenen Abonnementkonto erstellt. Wenn Sie das Unternehmen erstellen, wird das Konto zur Unternehmenshierarchie hinzugefügt. Die Abrechnung für das Konto geht an das Unternehmen über, aber die zugehörigen Benutzer und Ressourcen bleiben gleich und sind nicht betroffen. Eine vollständige Beschreibung der Auswirkungen auf das Konto finden Sie unter [Unternehmen erstellen](/docs/account?topic=account-create-enterprise).

1. Rufen Sie **Verwalten** > **Unternehmen** auf und klicken Sie auf **Erstellen**.
2. Geben Sie den Namen Ihres Unternehmens ein (z. B. 'Example Corp'), um Ihr Unternehmen anzugeben.
3. Geben Sie die Domäne Ihres Unternehmens ein (z. B. `examplecorp.com`).
4. Lesen Sie die Informationen zu den Auswirkungen auf Ihr Konto und wählen Sie **Ich bin mir über die Auswirkungen auf mein Konto im Klaren** aus. Klicken Sie anschließend auf **Erstellen**. Das Konto ist jetzt fester Bestandteil des Unternehmens und kann nicht entfernt werden.

Wenn Ihr Unternehmen erstellt wurde, werden Sie zum Dashboard für das Unternehmen geleitet. Von hier aus können Sie die Unternehmensdetails, die Konten, die Benutzer und die Abrechnungsinformationen anzeigen. Rufen Sie die Seite **Konten** auf, um Ihre Unternehmensstruktur anzuzeigen, in der die folgenden Konten angezeigt werden:
  * Ein Unternehmenskonto mit demselben Namen wie Ihr Unternehmen. Dieses Konto wird für das Unternehmensmanagement verwendet.
  * Das Konto, aus dem Sie das Unternehmen erstellt haben. Die Benutzer können weiterhin problemlos mit den Ressourcen in dem Konto arbeiten.

## Schritt 2. Unternehmensstruktur mit Kontogruppen erstellen
{: #account_groups_tutorial}

Sie können Kontogruppen verwenden, um zusammengehörige Konten zu organisieren. Die zweite und dritte Ebene der Unternehmenshierarchie von 'Example Corp.' enthält die Kontogruppen 'Marketing', 'Development', 'Sales', 'Design' und 'Engineering'. Führen Sie die folgenden Schritte aus, um die Kontogruppen zu erstellen:

1. Klicken Sie im Dashboard für das Unternehmen auf **Konten**, um die Konten und Kontogruppen im Unternehmen anzuzeigen.
2. Klicken Sie im Abschnitt "Kontogruppe" auf **Erstellen**.
3. Geben Sie den Namen der Kontogruppe ein, z. B. `Marketing`.
4. Geben Sie im Kontaktfeld die IBMid für den Benutzer ein, den Sie als primären Kontakt für die Kontogruppe verwenden möchten. Da eine Kontogruppe keine Ressourcen enthalten kann, verfügt sie nicht über einen Eigner wie ein Konto.
5. Wählen Sie **Example Corp** als übergeordnetes Konto aus.
6. Klicken Sie auf **Erstellen**.

Wiederholen Sie die Schritte zum Erstellen der Kontogruppen 'Sales', 'Development', 'Design' und 'Engineering'. Wenn Sie die Kontogruppen für 'Design' und 'Engineering' erstellen, stellen Sie sicher, dass Sie 'Development' als übergeordnete Kontogruppe hinzufügen.

## Schritt 3. Vorhandene Konten importieren
{: #existing_accounts_tutorial}

Nachdem Sie nun eine Unternehmensstruktur erstellt haben, können Sie ein vorhandenes Konto in das Unternehmen importieren. Wenn Sie ein Konto importieren, wird es dem Unternehmen permanent hinzugefügt. Wie beim Erstellen eines Unternehmens geht die Abrechnung für die importierten Konten an das Unternehmen über, aber die zugehörigen Benutzer und Ressourcen bleiben gleich. Details hierzu finden Sie unter [Vorhandene Konten importieren](/docs/account?topic=account-enterprise-add#add-accounts).

Der folgende Zugriff ist erforderlich, um ein vorhandenes Konto zu importieren:

* In dem zu importierenden Konto müssen Sie der Kontoeigner sein oder die Rolle "Administrator" für den Unternehmens- und Abrechnungskontoverwaltungsservice in dem Konto haben.
* Im Unternehmenskonto benötigen Sie die Rolle "Bearbeiter" oder "Administrator" für den Unternehmensservice und die Rolle "Administrator" für den Abrechnungsservice.

Führen Sie die folgenden Schritte aus, um das UX-UI-Beispielkonto in die Kontogruppe 'Design' zu importieren:
1. Klicken Sie im Dashboard für das Unternehmen auf **Konten**, um die Konten und Kontogruppen im Unternehmen anzuzeigen.
2. Klicken Sie im Abschnitt "Konten" auf **Hinzufügen** > **Konto importieren**.
3. Wählen Sie in der Liste **Konten** den Eintrag **UX-UI** aus.

  Wenn keine Konten angezeigt werden, haben Sie wahrscheinlich nicht den richtigen Zugriff auf die vorhandenen Konten.
  {: tip}

4. Wählen Sie **Design** als übergeordnetes Element des UX-UI-Kontos aus. Dies bestimmt, wo sich das Konto in der Unternehmenshierarchie befindet.
5. Lesen Sie die Informationen zu den Auswirkungen auf Ihr Konto und wählen Sie **Ich bin mir über die Auswirkungen auf mein Konto im Klaren** aus. Klicken Sie anschließend auf **Importieren**.

Wiederholen Sie die Schritte, um weitere Konten zu importieren.

## Schritt 4. Neue Konten erstellen
{: #create-accounts_tutorial}

Sie können neue Konten in Ihrem Unternehmen erstellen. Die Konten werden als nutzungsabhängige Konten erstellt und die Nutzung wird dem Unternehmen in Rechnung gestellt. Um ein Konto zu erstellen, benötigen Sie eine Zugriffsrichtlinie mit der Rolle "Bearbeiter" oder "Administrator" für den Unternehmensservice.

Führen Sie die folgenden Schritte aus, um das Beispielwebkonto in Ihrem Unternehmen zu erstellen:

1. Klicken Sie im Dashboard für das Unternehmen auf **Konten**, um die Konten und Kontogruppen im Unternehmen anzuzeigen.
1. Wählen Sie **Hinzufügen** > **Konto erstellen** aus.
1. Geben Sie `Web` als Namen für das Konto ein.
1. Wenn Sie einen anderen Benutzer als den Kontoeigner zuordnen möchten, geben Sie die betreffende IBMid im Feld **Eigner** ein. Der Kontoeigner hat vollständigen Zugriff für die Verwaltung des Kontos.
1. Wählen Sie **Marketing** als übergeordnetes Element dieses Kontos aus.
1. Klicken Sie auf **Erstellen**.

Nachdem Sie das Konto erstellt haben, kann sich der Kontoeigner bei dem Konto anmelden, um andere Benutzer einzuladen und deren Zugriff zu verwalten.

Wiederholen Sie die Schritte, um weitere Konten zu erstellen. Zum Beispiel hat das Unternehmen 'Example Corp' die folgende Hierarchie aus untergeordneten und übergeordneten Konten.

| Untergeordnetes Konto | Übergeordnetes Konto |
| ----- | -------|
| Print | Marketing |
| Frontend | Engineering |
| Backend | Engineering |
| Direct | Sales |
| Online | Sales |
| Enablement | Sales |
{:caption="Tabelle 1. Hierarchie aus untergeordneten und übergeordneten Konten" caption-side="top"}

## Schritt 5. Abonnements erkunden
{: #explore-sub_tutorial}

Sie können Abonnements im Unternehmen über das Dashboard für das Unternehmen erkunden. Alle vorhandenen Abonnements von Konten, die in das Unternehmen importiert werden, werden in das Unternehmenskonto verschoben und dem [Guthabenpool](/docs/billing-usage?topic=billing-usage-enterprise#credit-pool) des Unternehmens hinzugefügt.

1. Klicken Sie auf **Dashboard**, um wieder das Dashboard für das Unternehmen aufzurufen. Im Abschnitt "Abrechnung" können Sie verfügbare Guthaben, übrige Guthaben und Abonnementablaufdaten anzeigen.
1. Wenn Sie Details zu allen Abonnements im Unternehmen anzeigen möchten, klicken Sie auf **Abonnements anzeigen**.

   Im Abschnitt "Plattformabonnement" können Sie das Startdatum, das Enddatum, das Startguthaben und das verfügbare Guthaben des Abonnements anzeigen. Wenn Sie weiteres Guthaben hinzufügen möchten, können Sie zusätzliche Abonnements erwerben und den Abonnementcode anwenden.

## Schritt 6. Benutzern in untergeordneten Konten den Zugriff zum Erstellen von Ressourcen zuweisen
{: #users_create_resources}

Bevor Sie beginnen, stellen Sie sicher, dass Sie zu dem Konto wechseln, in dem Sie die Ressource erstellen möchten. Wechseln Sie in diesem Fall zu dem Konto *Print*. Wenn Sie möchten, dass Benutzer in Ihrem Konto Ressourcen aus dem Katalog erstellen und sie einer Ressourcengruppe zuweisen können, müssen Sie zwei Typen von Zugriffsrichtlinien zuweisen.
* Weisen Sie eine Zugriffsrichtlinie mit der Rolle "Anzeigeberechtigter" oder einer Rolle mit noch weitergehenden Berechtigungen für die Ressourcengruppe zu.
* Weisen Sie eine Zugriffsrichtlinie mit der Rolle "Bearbeiter" oder "Administrator" für den Service zu.

Führen Sie die folgenden Schritte aus, um den erforderlichen Zugriff zuzuweisen:

1. Rufen Sie **Verwalten** > **Zugriff (IAM)** auf und wählen Sie dann **Benutzer** aus.
2. Wählen Sie einen Benutzernamen aus der Liste aus.
3. Klicken Sie auf die Registerkarte **Zugriffsrichtlinien** > **Zugriff zuweisen**.
4. Klicken Sie auf **Zugriff in einer Ressourcengruppe zuweisen**.
5. Wählen Sie die Ressourcengruppe aus, der Sie den Benutzerzugriff zuweisen wollen.
6. Wählen Sie die Rolle "Anzeigeberechtigter" oder höher für die Ressourcengruppe aus.
7. Wählen Sie den Service aus, dem Sie den Benutzerzugriff zuweisen wollen.
  * Wenn der Benutzer in der Lage sein soll, jeden beliebigen Service bereitzustellen, wählen Sie **Alle Services** aus.
  * Wenn Sie dem Benutzer einen spezifischen Zugriff zuweisen möchten, wählen Sie einen Service aus der Liste aus. Der Benutzer hat nur Zugriff auf den ausgewählten Service.
8. Wählen Sie die Rolle "Bearbeiter" oder "Administrator" aus.
9. Klicken Sie auf **Zuweisen**.

## Schritt 7. Nutzung von allen Konten anzeigen
{: #usage_tutorial}

1. Melden Sie sich bei dem Unternehmenskonto "Example Corp " an.
2. Rufen Sie **Verwalten > Abrechnung und Nutzung** auf und wählen Sie **Nutzung** aus.

   Auf der Seite "Nutzung" werden die Kosten für die gesamte Nutzung in Ihrem Unternehmen angezeigt, aufgeschlüsselt nach Konto und Kontogruppe. Nutzungsinformationen für klassische Infrastrukturservices sind für den aktuellen Abrechnungszeitraum nicht enthalten. Weitere Informationen finden Sie unter [Nutzung für Ressourcen der klassischen Infrastruktur anzeigen](/docs/billing-usage?topic=billing-usage-infra-usage).
3. Klicken Sie in der Tabelle auf **Marketing**, um die Nutzung innerhalb der Kontogruppe anzuzeigen. Ähnlich wie bei der Unternehmensebene wird die Nutzung nach Konto und Kontogruppe aufgegliedert.
4. Wenn Sie die Nutzung nach Ressource anzeigen möchten, rufen Sie die Kontoebene auf, indem Sie sich in der Tabelle durch die Kontogruppen klicken oder das Konto im Menü **Unternehmen** auswählen. Es werden die Kosten für jeden Ressourcentyp angezeigt, der innerhalb des Zeitrahmens genutzt wurde.

Wiederholen Sie die Schritte zum Anzeigen der Nutzung der Kontogruppen 'Development', 'Sales', 'Design' und 'Engineering'.

   Über das Unternehmenskonto können Sie die Nutzungsdaten für den Ressourcenplan oder die Instanz nicht anzeigen, da ein Zugriff innerhalb des Kontos erforderlich ist. Klicken Sie auf **Zum Konto wechseln**, um Daten für das Konto anzuzeigen. Sie benötigen den Abrechnungszugriff auf die Ressourcen und Services im Konto. Weitere Informationen finden Sie unter [Nutzung anzeigen](/docs/billing-usage?topic=billing-usage-viewingusage).

Daten werden im Unternehmenskonto nur für die Nutzung angezeigt, die durch Konten im Unternehmen anfällt. Um die Nutzung für den Zeitraum anzuzeigen, bevor ein Konto zum Unternehmen hinzugefügt wurde, melden Sie sich bei diesem Konto an und wählen Sie den entsprechenden Zeitraum aus.
{: note}
