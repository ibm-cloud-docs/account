---

copyright:

  years: 2017, 2019
lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Benutzerzugriff auf den Katalog verwalten
{: #find-access}

Als {{site.data.keyword.Bluemix}}-Kontoeigner können Sie Benutzern den Zugriff auf den Katalog zuweisen, indem Sie eine IAM-Richtlinie (Identity and Access Management) in {{site.data.keyword.Bluemix_notm}} verwenden. Auf diese Weise können Sie die Anzeige privater Services, die zum Kontokatalog hinzugefügt werden, oder öffentlicher Services, die im Konto erstellt werden, steuern. Standardmäßig kann nur der Kontoeigner diese Aufgaben ausführen.

## Zugriff delegieren
{: #get-access}

Sie können den Zugriff auf Ihr Konto delegieren, um zu steuern, was für Benutzer sichtbar ist und welche Berechtigungen diese Benutzer erhalten sollen. So sollten z. B. einige Benutzer bestimmte Informationen nur lesen und analysieren können, andere Benutzer könnten dagegen die Berechtigung zum Bearbeiten dieser Informationen erhalten. Führen Sie die folgenden Schritte aus, um den Kontozugriff an einen anderen Benutzer im Konto zu delegieren.

1. Klicken Sie auf **Verwalten** > **Zugriff (IAM)**.
2. Klicken Sie auf **Zugriffsverwaltung beginnt beim Benutzer** auf der Landing-Page.
3. Wählen Sie eine Benutzer in Ihrem Konto aus.
4. Klicken Sie auf **Zugriffsrichtlinien**.
5. Klicken Sie auf **Zugriff zuweisen**. Klicken Sie dann auf **Zugriff auf Kontoverwaltungsservices zuweisen**.
6. Wählen Sie den **Katalog mit globalen Ressourcen** in der Serviceliste und die Rolle **Administrator** in der Rollenauswahlliste aus.

Verwenden Sie die Rollen eines Anzeigeberechtigten und eines Bearbeiters, um weitere Berechtigungen zu erteilen. In der folgenden Tabelle finden Sie weitere Informationen zu den Möglichkeiten, die die einzelnen IAM-Rollen Benutzern bei der Arbeit mit dem Katalog für Ihr Konto eröffnen.

| Plattformmanagementrolle | Aktionen                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| Anzeigeberechtigter                   | Private Services anzeigen, nicht jedoch ändern                                                            |
| Bearbeiter                   | Objektmetadaten ändern, nicht jedoch die Sichtbarkeit privater Services                                |
| Administrator            | Objektmetadaten oder Sichtbarkeit privater Services ändern, Sichtbarkeit eines öffentlichen Service einschränken  |
{: caption="Tabelle 1. Beispiele für Plattformmanagementrollen und -aktionen für den Katalog" caption-side="top"}

Weitere Informationen zum Zuweisen von Zugriffsberechtigungen für Benutzer finden Sie in [Zugriff auf Kontoverwaltungsservices zuweisen](/docs/iam?topic=iam-account-services). 

## Zugriff bestätigen
{: #confirm-access}

Wenn Sie zum Konto einer anderen Person hinzugefügt werden, können Kontoadministratoren Zugriffsebenen an Sie delegieren, sodass Sie private Ressourcen anzeigen können, die zum Konto hinzugefügt werden. Der Kontoeigner kann auch die Möglichkeit zum Anzeigen öffentlicher Ressourcen im Kontokatalog delegieren. Standardmäßig verfügen Sie nicht über diese Zugriffsberechtigung. Der Kontoeigner muss Ihnen eine IAM-Rolle zuweisen, die Ihnen den Zugriff zum Ausführen dieser Aufgaben des Kontoressourcenmanagements ermöglicht.

Über die {{site.data.keyword.Bluemix_notm}}-Konsole oder die Befehlszeilenschnittstelle (CLI) können Sie ermitteln, ob Sie über die erforderliche Zugriffsberechtigung verfügen, um bestimmten Benutzern das Anzeigen einer privaten Ressource im Konto zu ermöglichen.

Führen Sie die folgenden Schritte aus, um die Konsole zu verwenden:

  1. Rufen Sie **Verwalten > Zugriff (IAM)** auf.
  2. Klicken Sie in der Benutzerliste auf Ihren Namen.
  3. Klicken Sie auf die Registerkarte **Zugriffsrichtlinien**, auf der Sie die zugewiesenen Zugriffsrichtlinien anzeigen können. Sie müssen über die Cloud IAM-Administratorrolle für die Katalogressource in Ihrem Konto verfügen, um die Einschlussliste mit den Konten, die private Ressourcen im Katalog anzeigen können, aktualisieren zu können.


Führen Sie zur Verwendung der [Befehlszeilenschnittstelle](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_iam#ibmcloud_commands_iam) den Befehl `ibmcloud iam user-policies <your-user-name>` aus. Der Befehl gibt einen Fehler zurück, wenn Sie kein Administrator für das Konto sind.
