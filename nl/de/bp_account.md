---

copyright:

  years: 2018
lastupdated: "2018-10-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Bewährte Verfahren für das Einrichten Ihres Kontos
{: #account_setup}

Bewährte Verfahren liefern die Grundbausteine für den Erfolg, bevor Sie überhaupt mit der Erstellung von Ressourcen beginnen. Wenn Sie bereit sind, Apps in den Produktionsbetrieb zu überführen und eine Umgebung für Ihre Entwickler einzurichten, machen Sie sich zum Einrichten Ihres Kontos mit dem Inhalt der folgenden Abschnitte vertraut.
{:shortdesc}

Die folgenden bewährten Verfahren konzentrieren sich auf die Verwendung IAM-fähiger Services. Gegenwärtig sind nicht alle Services in {{site.data.keyword.cloud}} IAM-fähig. Wenn eine Serviceinstanz in Ihrem Konto zu einer Cloud Foundry-Organisation und einem solchen Bereich gehört, gelten IAM-Richtlinien, Ressourcengruppen und Zugriffsgruppen nicht für sie. Sie können trotzdem Cloud Foundry-Organisationen und -Bereiche (Spaces) wie auch Ressourcengruppen in Ihrem Konto verwenden, aber Sie müssen Benutzern den Zugriff auf diese Ressourcen separat zuweisen. Informationen zum Arbeiten mit Cloud Foundry-Organisationen und Bereichen finden Sie unter [Organisationen und Bereiche hinzufügen](/docs/account/orgs_spaces.html#orgsspacesusers).
{: tip}

## Was ist eine gute Strategie für Ressourcengruppen?
{: #resource-group-strategy}

Da es sich bei einer Ressourcengruppe um einen logischen Container für Ressourcen handelt, ist die Verwendung einer Ressourcengruppe pro Projektumgebung ein guter Ausgangspunkt. Mit dieser Strategie können Administratoren die Ressourcennutzung auf Projektumgebungsebene steuern und anzeigen. Ein typisches Projekt verfügt beispielsweise über Umgebungen für die Entwicklung, das Testen und die Produktion. Daher hätte ein Projekt mit dem Namen `CustApp` die folgenden Ressourcengruppen:

* CustApp-Dev
* CustApp-Test
* CustApp-Prod

Dann kann Benutzern Zugriff erteilt werden. Ein Entwickler verfügt zum Beispiel im Normalfall über recht weitreichende Zugriffsrechte für die Entwicklungsressourcengruppe und über einen sehr viel enger gefassten oder sogar keinen Zugriff auf die Produktionsressourcengruppe.

Wenn Sie über ein Konto mit nutzungsabhängiger Zahlung oder ein Abonnementkonto verfügen, können Sie zusätzliche Ressourcengruppen erstellen: 

1. Rufen Sie **Verwalten** &gt; **Konto** &gt; **Ressourcengruppen** auf.
2. Klicken Sie auf **Ressourcengruppe erstellen**.
3. Geben Sie den Namen für Ihre Ressourcengruppe ein.
4. Klicken Sie auf **Hinzufügen**.

## Ressourcengruppen einrichten
{: #setting-up-rgs}

Ressourcengruppen dienen als logische Container zum Organisieren Ihrer IAM-fähigen Ressourcen. Alle Service, die unter Verwendung der IAM-Zugriffssteuerung verwaltet werden, gehören zu einer Ressourcengruppe. Die Zuweisung einer Ressource zu ihrer Ressourcengruppe erfolgt bei ihrer Erstellung aus dem Katalog. Die Ressourcengruppenzuordnung kann nicht geändert werden, nachdem sie erst einmal eingerichtet wurde. Daher ist es wichtig, dass Sie einige Ihrer Ressourcengruppen zum jetzigen Zeitpunkt einrichten.

Wenn Sie über ein Testkonto oder ein Lite-Konto verfügen, sind Sie auf die Verwendung der Standardressourcengruppe beschränkt und können keine weiteren Ressourcengruppen erstellen.
{: tip}

## Ressourcen zu einer Ressourcengruppe hinzufügen
{: #adding-resources}

Wenn Sie eine IAM-fähige Ressource aus dem Katalog erstellen, müssen Sie die Ressourcengruppe auswählen, der Sie sie zuweisen möchten. Nachdem eine Ressource erstellt worden ist, kann die Ressourcengruppe, der sie zugewiesen ist, nicht mehr geändert werden. Wenn in dieser Phase ein Fehler gemacht wird, müssen Sie die Ressource löschen und eine neue erstellen.

### Erforderlicher Zugriff zum Hinzufügen einer Ressource zu einer Ressourcengruppe
{: #rg_access}

Der {{site.data.keyword.cloud_notm}}-Kontoeigner kann Ressourcen zu jeder beliebigen Ressourcengruppe hinzufügen. Die übrigen Benutzer können dies nur, wenn ihnen zuvor über eine IAM-Zugriffsrichtlinie Zugriff erteilt wurde. Benutzern müssen mindestens zwei Plattformmanagementrollen zugewiesen werden, damit sie Ressourcen zu einer Ressourcengruppe hinzufügen können:

* Die Rolle eines Anzeigeberechtigten ('Viewer') oder höher für die Ressourcengruppe selbst
* Die Rolle eines Bearbeiters ('Editor') oder höher für die Ressource oder den Service

Führen Sie zum Hinzufügen einer Ressource zu einer Ressourcengruppe die folgenden Schritte aus:

1. Rufen Sie **Verwalten** &gt; **Konto** &gt; **Ressourcengruppen** auf.
2. Klicken Sie für für die Ressourcengruppe, zu der Sie Ressourcen hinzufügen wollen, im Menü auf das Symbol 'Weitere Aktionen' ![Symbol 'Weitere Aktionen'](../icons/overflow-menu.svg), und wählen Sie **Ressourcen hinzufügen** aus.
3. Wenn Sie zum Katalog weitergeleitet werden, wählen Sie die Ressource aus, die Sie hinzufügen wollen.
4. Wählen Sie die Ressourcengruppe aus, der Sie die Ressource zuweisen wollen.
5. Klicken Sie auf **Erstellen**.

Sie können immer direkt zum Katalog wechseln, um Ressourcen zu erstellen und diese dann einer Ressourcengruppe zuzuordnen.
{: tip} 

Weitere Informationen finden Sie in [Bewährte Verfahren für das Organisieren von Ressourcen in einer Ressourcengruppe](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).

## Nächste Schritte

Richten Sie Zugriffsgruppen für die Benutzer und Service-IDs ein, die denselben Zugriff auf Ressourcen und Ressourcengruppen in Ihrem Konto benötigen. Sie können eine sehr geringe Anzahl von Zugriffsrichtlinien zuweisen, wodurch Sie Zeit sparen. Weitere Informationen enthält [Bewährte Verfahren für die Zuweisung von Zugriff](/docs/iam/bp_access.html).

Weitere Informationen zum Einrichten von Benutzern und Teams in Ihrem Konto finden Sie in [Bewährte Verfahren für das Organisieren von Benutzern, Teams und Apps](/docs/tutorials/users-teams-applications.html#best-practices-for-organizing-users-teams-applications).
