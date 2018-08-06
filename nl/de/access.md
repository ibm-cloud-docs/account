---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Zugriff auf den Katalog verwalten
{: #find-access}

Als Kontoeigner kann es hilfreich sein, Zugriff mithilfe einer IAM-Richtlinie (IAM = Identity and Access Management) zuzuordnen, um es Benutzern in Ihrem Konto zu ermöglichen, die Sichtbarkeit von privaten Services, die zum Kontokatalog hinzugefügt wurden, oder von öffentlichen Services, die im Konto erstellt wurden, zu steuern. Standardmäßig können diese Aufgaben nur vom Kontoeigner ausgeführt werden.

## Wie kann ich als Kontoeigner Zugriff delegieren?
{: #get-access}

Als Kontoeigner können Sie einem Benutzer in Ihrem Konto über die IAM-Benutzerschnittstelle Zugriff erteilen, indem Sie eine Zugriffsrichtlinie zuordnen. Stellen Sie sicher, dass der Benutzer über den erforderlichen Zugriff verfügt, indem Sie die globale Katalogressource**** und die Rolle **Administrator** für die Zugriffsrichtlinie auswählen.

Bei Bedarf können Sie Benutzern in Ihrem Konto über die IAM-Rollen `Anzeigeberechtigter (Viewer)` und `Editor` weitere Berechtigungen erteilen. In der folgenden Tabelle finden Sie weitere Informationen zu den Möglichkeiten, die die einzelnen IAM-Rollen Benutzern bei der Arbeit mit dem Katalog für Ihr Konto eröffnen.

| Plattformmanagementrolle | Beschreibung von Aktionen |
|:-----------------|:-----------------|
| Viewer (Anzeigeberechtigter) | Private Services anzeigen, auch wenn das Konto nicht einbezogen wurde. Änderungen sind nicht möglich. |
| Editor (Bearbeiter) | Objektmetadaten ändern. Änderungen an der Sichtbarkeit sind nicht möglich. |
| Administrator | Objektmetadaten oder Sichtbarkeit ändern.  |
{: caption="Tabelle 1. Beispielrollen und Aktionen des Plattformmanagements für den Katalogservice" caption-side="top"}

Schrittweise Anweisungen für das Zuordnen von Zugriff für Benutzer in Ihrem Konto finden Sie unter [Zugriff auf Ressourcen](/docs/iam/mngiam.html#iammanidaccser#resourceaccess).

## Wie kann ich feststellen, ob ich über Zugriff verfüge?

Wenn Sie zum Konto eines anderen hinzugefügt wurden, wurden möglicherweise bestimmte Zugriffsebenen an Sie delegiert, sodass Ihnen private Ressourcen angezeigt werden, die dem Konto hinzugefügt wurden. Der Kontoeigner kann auch die Möglichkeit zum Verwalten der Benutzer an Sie delegieren, denen öffentliche Ressourcen im Kontokatalog angezeigt werden. Dieser Zugriff ist Ihnen nicht standardmäßig zugeordnet. Der Kontoeigner müssen Ihnen eine IAM-Rolle zuordnen, die Ihnen den Zugriff zum Ausführen dieser Aufgaben des Kontoressourcenmanagements ermöglicht.

Über die Befehlszeilenschnittstelle oder die IAM-Benutzerschnittstelle können Sie ermitteln, ob Sie über den erforderlichen Zugriff verfügen, um dafür zu sorgen, dass bestimmten Benutzern eine private Ressource angezeigt wird, die dem Konto hinzugefügt wurde.

Führen Sie die folgenden Schritte aus, um mit der IAM-Benutzerschnittstelle zu arbeiten:

1. Rufen Sie **Verwalten** > **Sicherheit** > **Identität und Zugriff** auf und klicken Sie dann auf **Benutzer**.
2. Klicken Sie in der Benutzerliste auf Ihren Namen.
3. Im Bereich **Zugriffsrichtlinie** können Sie Ihre zugeordneten Zugriffsrichtlinien anzeigen. Sie müssen über die Cloud IAM-Administratorrolle für die Katalogressource in Ihrem Konto verfügen, um die Einschlussliste mit den Konten, die private Ressourcen im Katalog anzeigen können, aktualisieren zu können.

Führen Sie die folgenden Schritte aus, um mit der [Benutzerschnittstelle für IBM Cloud (ibmcloud)](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_iam) zu arbeiten:

Geben Sie den Befehl `ibmcloud iam user-policies <your-username>` mit Ihrem Benutzernamen ein, um herauszufinden, ob Sie als Administrator von Konten eingesetzt wurden, die Sie in der Befehlszeilenschnittstelle ausgewählt haben. Wenn Sie nicht über die Administratorrolle für Ihr Konto verfügen, wird von diesen Befehlen ein Fehler zu fehlenden Berechtigungen zurückgegeben.
{: tip}
