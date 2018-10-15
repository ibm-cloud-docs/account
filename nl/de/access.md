---

copyright:

  years: 2017, 2018
lastupdated: "2018-10-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Zugriff auf den Katalog verwalten
{: #find-access}

Als Kontoeigner können Sie Zugriffsberechtigungen mithilfe einer IAM-Richtlinie zuweisen. Dies ermöglicht es Benutzern, die Sichtbarkeit privater Services, die zum Kontokatalog hinzugefügt werden, oder öffentlicher Services, die im Konto erstellt werden, zu steuern. Standardmäßig kann nur der Kontoeigner diese Aufgaben ausführen.

## Wie kann ich als Kontoeigner Zugriff delegieren?
{: #get-access}

Als Kontoeigner können Sie Zugriff auf das Konto gewähren, indem Sie über die Identity and Access-Benutzerschnittstelle einem Benutzer eine Zugriffsrichtlinie zuweisen. Stellen Sie den erforderlichen Zugriff für den Benutzer sicher, indem Sie die Ressource **Globaler Katalog** und die Rolle **Administrator** für die Zugriffsrichtlinie auswählen.

Mithilfe der IAM-Rollen (Identity and Access Management) `Anzeigeberechtigter` und `Bearbeitungsberechtigter` können Sie weitere Berechtigungen erteilen. In der folgenden Tabelle finden Sie weitere Informationen zu den Möglichkeiten, die die einzelnen IAM-Rollen Benutzern bei der Arbeit mit dem Katalog für Ihr Konto eröffnen.

| Plattformmanagementrolle | Beschreibung von Aktionen |
|:-----------------|:-----------------|
| Viewer (Anzeigeberechtigter) | Private Services anzeigen, jedoch keine Änderungen vornehmen. |
| Editor (Bearbeiter) | Objektmetadaten ändern. Änderungen an der Sichtbarkeit sind nicht möglich. |
| Administrator | Objektmetadaten oder Sichtbarkeit ändern.  |
{: caption="Tabelle 1. Beispielrollen und Aktionen des Plattformmanagements für den Katalogservice" caption-side="top"}

Schrittweise Anweisungen für das Zuordnen von Zugriff für Benutzer in Ihrem Konto finden Sie unter [Zugriff auf Ressourcen](/docs/iam/mngiam.html#iammanidaccser#resourceaccess).

## Wie kann ich feststellen, ob ich über Zugriff verfüge?

Wenn Sie zum Konto einer anderen Person hinzugefügt werden, werden möglicherweise bestimmte Zugriffsebenen an Sie delegiert, sodass Sie private Ressourcen anzeigen können, die zum Konto hinzugefügt werden. Der Kontoeigner kann auch die Möglichkeit zum Anzeigen öffentlicher Ressourcen im Kontokatalog delegieren. Standardmäßig verfügen Sie nicht über diese Zugriffsberechtigung. Der Kontoeigner muss Ihnen eine IAM-Rolle zuweisen, die Ihnen den Zugriff zum Ausführen dieser Aufgaben des Kontoressourcenmanagements ermöglicht.

Über die Befehlszeilenschnittstelle oder die IAM-Benutzerschnittstelle können Sie ermitteln, ob Sie über den erforderlichen Zugriff verfügen, um dafür zu sorgen, dass bestimmten Benutzern eine private Ressource angezeigt wird, die dem Konto hinzugefügt wird.

Führen Sie die folgenden Schritte aus, um mit der IAM-Benutzerschnittstelle zu arbeiten:

1. Rufen Sie **Verwalten** > **Zugriff (IAM)** auf und klicken Sie dann auf **Benutzer**.
2. Klicken Sie in der Benutzerliste auf Ihren Namen.
3. Klicken Sie auf die Registerkarte **Zugriffsrichtlinien**, auf der Sie die zugewiesenen Zugriffsrichtlinien anzeigen können. Sie müssen über die Cloud IAM-Administratorrolle für die Katalogressource in Ihrem Konto verfügen, um die Einschlussliste mit den Konten, die private Ressourcen im Katalog anzeigen können, aktualisieren zu können.

Führen Sie die folgenden Schritte aus, um die [{{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_iam) zu verwenden:

Geben Sie den Befehl `ibmcloud iam user-policies <your-username>` mit Ihrem Benutzernamen ein, um herauszufinden, ob Sie als Administrator von Konten eingesetzt wurden, die Sie in der Befehlszeilenschnittstelle ausgewählt haben. Wenn Sie nicht über die Administratorrolle für Ihr Konto verfügen, wird von diesen Befehlen ein Fehler zu fehlenden Berechtigungen zurückgegeben.
{: tip}
