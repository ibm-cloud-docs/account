---

copyright:
  years: 2018, 2019
lastupdated: "2019-01-28"

keywords: resource group, account access, user access, IAM, organize

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Bewährte Verfahren für das Einrichten Ihres Kontos
{: #account_setup}

Die hier beschriebenen bewährten Verfahren liefern die Grundbausteine für den Erfolg, bevor Sie mit der Erstellung von Ressourcen beginnen. Wenn Sie bereit sind, Apps in den Produktionsbetrieb zu überführen und eine Umgebung für Ihre Entwickler einzurichten, machen Sie sich zum Einrichten Ihres Kontos mit dem Inhalt der folgenden Abschnitte vertraut.
{:shortdesc}

Die folgenden bewährten Verfahren konzentrieren sich auf die Verwendung IAM-fähiger Services. Gegenwärtig sind nicht alle Services in {{site.data.keyword.cloud}} IAM-fähig. IAM-Richtlinien, Ressourcengruppen und Zugriffsgruppen gelten nicht für Serviceinstanzen, die zu einer Cloud Foundry-Organisation und einem Cloud Foundry-Bereich gehören. Es ist dennoch möglich, sowohl Cloud Foundry-Organisationen und -Bereiche als auch Ressourcengruppen im Konto zu verwenden, Sie müssen den Benutzern den Zugriff auf diese Ressourcen jedoch separat zuweisen. Informationen zu Cloud Foundry-Organisationen und -Bereichen finden Sie in [Organisationen und Bereiche hinzufügen](/docs/account?topic=account-orgsspacesusers).
{: note}

## Was zeichnet eine gute Strategie für Ressourcengruppen aus?
{: #resource-group-strategy}

Administratoren können die Ressourcennutzung auf Projektumgebungsebene besser steuern, wenn eine Ressourcengruppe pro Projektumgebung verwendet wird. Ein typisches Projekt verfügt beispielsweise über Umgebungen für die Entwicklung, das Testen und die Produktion. Ein Projekt mit dem Namen `CustApp` würde die folgenden Ressourcengruppen umfassen:

* `CustApp-Dev`
* `CustApp-Test`
* `CustApp-Prod`

Sie können Benutzern Zugriffsberechtigungen erteilen. Ein Entwickler verfügt zum Beispiel im Normalfall über recht weitreichende Zugriffsberechtigungen für die Entwicklungsressourcengruppe und über einen sehr viel enger gefassten oder sogar keinen Zugriff auf die Produktionsressourcengruppe.

Wenn Sie über ein Konto mit nutzungsabhängiger Zahlung oder ein Abonnementkonto verfügen, können Sie weitere Ressourcengruppen erstellen:

1. Rufen Sie **Verwalten** > **Konto** auf und wählen Sie **Ressourcengruppen** im Menü **Kontoressourcen** aus.
3. Klicken Sie auf **Erstellen**.
4. Geben Sie den Namen für Ihre Ressourcengruppe ein.
5. Klicken Sie auf **Hinzufügen**.

Weitere Informationen zu dem am besten für Sie geeigneten Kontotyp finden Sie in [Kontotypen](/docs/account?topic=account-accounts).


## Ressourcengruppen einrichten
{: #setting-up-rgs}

Ressourcengruppen dienen als logische Container zum Organisieren Ihrer IAM-fähigen Ressourcen. Alle Services, die mit der Zugriffssteuerung von {{site.data.keyword.cloud_notm}} Identity and Access Management (IAM) verwaltet werden, gehören zu einer Ressourcengruppe. Die Zuweisung einer Ressource zu ihrer Ressourcengruppe erfolgt bei ihrer Erstellung aus dem Katalog. Die Ressourcengruppenzuordnung kann nicht geändert werden, nachdem sie erst einmal eingerichtet wurde. Daher ist es wichtig, dass Sie einige Ihrer Ressourcengruppen zum jetzigen Zeitpunkt einrichten.

Mit einem Lite-Konto verfügen Sie über Zugriff auf eine einzelne Ressourcengruppe, die für Sie erstellt wird. Sie können keine zusätzlichen Ressourcengruppen erstellen. Wenn Sie ein [Upgrade für Ihr Konto durchführen](/docs/account?topic=account-changeacct#changeacct), können Sie mehrere Ressourcengruppen erstellen und mit diesen arbeiten.
{: note}


## Ressourcen zu einer Ressourcengruppe hinzufügen
{: #adding-resources}

Sie können eine Ressource zu einer Ressourcengruppe hinzufügen, wenn Sie eine IAM-fähige Ressource über den Katalog erstellen. Stellen Sie bei der Auswahl der Ressource sicher, dass die Zielressourcengruppe ausgewählt ist. Nach der Erstellung einer Ressource kann ihre zugewiesene Ressourcengruppe nicht mehr geändert werden. Wenn Sie eine Ressource versehentlich der falschen Ressourcengruppe zuweisen, löschen Sie die Ressource und erstellen Sie eine neue.

### Erforderlicher Zugriff zum Hinzufügen einer Ressource zu einer Ressourcengruppe
{: #rg_access}

Als Kontoeigner können Sie Ressourcen zu jeder beliebigen Ressourcengruppe hinzufügen. Anderen Benutzern muss die entsprechende Zugriffsberechtigung mithilfe einer IAM-Zugriffsrichtlinie erteilt werden, damit diese Benutzer Ressourcen zu Ressourcengruppen hinzufügen können. Benutzern müssen mindestens zwei Plattformmanagementrollen zugewiesen werden, damit sie Ressourcen zu einer Ressourcengruppe hinzufügen können:

* Die Rolle eines Anzeigeberechtigten oder eine Rolle mit umfassenderen Berechtigungen für die Ressourcengruppe
* Die Rolle eines Bearbeiters oder eine Rolle mit umfassenderen Berechtigungen für die Ressource oder den Service

Führen Sie zum Hinzufügen einer Ressource zu einer Ressourcengruppe die folgenden Schritte aus:

1. Rufen Sie **Verwalten > Konto** auf und wählen Sie **Ressourcengruppen** aus.
2. Klicken Sie auf das Aktionssymbol ![Aktionssymbol](../icons/action-menu-icon.svg) für die Ressourcengruppe, zu der Ressourcen hinzugefügt werden sollen, und wählen Sie **Ressourcen hinzufügen** aus.
3. Nachdem Sie zum Katalog weitergeleitet wurden, wählen Sie die Ressource aus, die Sie hinzufügen möchten.
4. Wählen Sie die Ressourcengruppe aus, der Sie die Ressource zuweisen wollen.
5. Klicken Sie auf **Erstellen**.

Sie können immer direkt zum Katalog wechseln, um Ressourcen zu erstellen und diese dann einer Ressourcengruppe zuzuordnen.
{: tip}

Weitere Informationen finden Sie in [Bewährte Verfahren für das Organisieren von Ressourcen in einer Ressourcengruppe](/docs/resources?topic=resources-bp_resourcegroups).


## Ressourcen mithilfe von Tags organisieren
{: #tags}

Mithilfe von Tags können Sie Ihre Ressourcen organisieren und Nutzungskosten verfolgen. Sie können zusammengehörende Ressourcen mit Tags kennzeichnen und im gesamten Konto anzeigen, indem Sie im Dashboard anhand von Tags filtern. Tags des Typs 'Schlüssel:Wert' können Sie bei der Organisation von Entwicklungsumgebungen, Projekten, Compliance und Optimierung unterstützen.

Führen Sie die folgenden Schritte aus, um einen Tag zu einer Ressource hinzuzufügen:

1. Klicken Sie auf das Menüsymbol ![Menüsymbol](../icons/icon_hamburger.svg) > **Ressourcenliste**, um die Ressourcenliste anzuzeigen. Suchen Sie die Ressource, zu der Sie einen Tag hinzufügen möchten.
2. Wenn der Ressource bereits ein Tag zugeordnet wurde, bewegen Sie den Mauszeiger über den vorhandenen Tag und klicken Sie auf das Bearbeitungssymbol ![Bearbeitungssymbol](../icons/edit-tagging.svg). Ist der Ressource kein Tag zugeordnet, bewegen Sie den Mauszeiger über **--** in der Spalte `Tags` und klicken Sie auf **Tags hinzufügen**.
3. Geben Sie eine Namen für den Tag ein und drücken Sie die Eingabetaste nach jedem Tag, falls Sie mehrere Tags hinzufügen.
4. Wenn Sie einen Tag von einer Ressource entfernen möchten, klicken Sie auf das Symbol für 'Entfernen' ![Symbol für 'Entfernen'](../icons/close-tagging.svg) neben dem Tag.
5. Speichern Sie die Änderungen.

Weitere Informationen dazu, welche Ressourcen mit Tags gekennzeichnet werden können und wie die entsprechenden Zugriffsberechtigungen zugewiesen werden, um die Taggingfunktion an Benutzer in Ihrem Konto zu delegieren, finden Sie in [Mit Tags arbeiten](/docs/resources?topic=resources-tag).


## Nächste Schritte

Richten Sie Zugriffsgruppen für die Benutzer und Service-IDs ein, die denselben Zugriff auf Ressourcen und Ressourcengruppen in Ihrem Konto benötigen. Sie können eine sehr geringe Anzahl von Zugriffsrichtlinien zuweisen, wodurch Sie Zeit sparen. Weitere Informationen enthält [Bewährte Verfahren für die Zuweisung von Zugriff](/docs/iam?topic=iam-cfaccess).
