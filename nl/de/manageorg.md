---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: account owner, user roles, manage account, orgs, spaces

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# Organisationen und Bereiche aktualisieren
{: #orgupdates}

Als {{site.data.keyword.Bluemix}}-Kontoeigner oder -Organisationsmanager können Sie Verwaltungstasks auf der Organisationsebene und der Bereichsebene ausführen. Zu diesen Tasks gehören die Umbenennung einer Organisation oder eines Bereichs, die Zuweisung oder Aktualisierung von Cloud Foundry-Benutzerrollen, die Verwaltung von Domänen und die Anzeige von Details zum Organisationskontingent.
{:shortdesc}

Wechseln Sie zu **Verwalten > Konto** und wählen Sie **Cloud Foundry-Organisationen** aus.

Sie können jeweils nur die Ressourcen einer einzelnen Organisation anzeigen. Wenn Sie ein Mitglied mehrerer Organisationen sind, können Sie in der Menüleiste der Konsole über den Link mit den Benutzerkontovorgaben zwischen den Organisationen umschalten.
{: tip}

  * Klicken Sie zum Umbenennen einer Organisation auf das Aktionssymbol ![Aktionssymbol](../icons/action-menu-icon.svg) für die Organisation, die umbenannt werden soll, und wählen Sie **Umbenennen** aus.
    {: #orgrename}

    Alle Änderungen, die Sie vornehmen, gelten für alle Benutzer in der Organisation.

  * Wenden Sie sich an den [-Support](/docs/get-support?topic=get-support-getting-customer-support), um eine Organisation zu löschen.
    {: #deleteorgs}

    Beim Löschen einer Organisation werden alle Bereiche und Ressourcen in der Organisation ebenfalls gelöscht. Diese Aktion kann nicht rückgängig gemacht werden.

  * Wählen Sie zum Löschen eines Bereichs die Organisation aus, in der der Bereich zugewiesen ist. Klicken Sie dann auf das Aktionssymbol ![Aktionssymbol](../icons/action-menu-icon.svg) und wählen Sie **Löschen** aus.

    Wenn Sie einen Bereich löschen, werden alle darin enthaltenen Ressourcen und Benutzer ebenfalls gelöscht.

  * Klicken Sie zum Bearbeiten von Benutzerrollen auf der Organisationsebene auf das Aktionssymbol ![Aktionssymbol](../icons/action-menu-icon.svg) und wählen Sie **Benutzer** aus.
    {: #listmembers}

    Je nachdem, wie Sie die Benutzerberechtigungen ändern wollen, aktivieren oder inaktivieren Sie das Kontrollkästchen einer bestimmten Rolle. Die Rollen, die Sie auf Organisationsebene zuweisen können, sind 'Manager', 'Abrechnungsmanager' und 'Auditor'. Weitere Informationen finden Sie in [Cloud Foundry-Rollen](/docs/iam?topic=iam-cfaccess#cfroles).

  * Klicken Sie zum Bearbeiten von Benutzerrollen für einen bestimmten Bereich auf die Organisation, in der der Bereich zugewiesen ist. Klicken Sie dann auf den Namen des Bereichs.

    Je nachdem, wie Sie die Benutzerberechtigungen ändern wollen, aktivieren oder inaktivieren Sie das Kontrollkästchen einer bestimmten Rolle. Die Rollen, die Sie auf Bereichsebene zuweisen können, sind 'Manager', 'Entwickler' und 'Auditor'. Weitere Informationen finden Sie in [Cloud Foundry-Rollen](/docs/iam?topic=iam-cfaccess#cfroles).

  * Klicken Sie zum Verwalten Ihrer Domänen auf das Aktionssymbol ![Aktionssymbol](../icons/action-menu-icon.svg) für die entsprechende Organisation und wählen Sie **Domänen** aus.
    {: #managedomains}

    Als Kontoeigner oder Organisationsmanager können Sie die Systemdomäne anzeigen und angepasste Domänen für Anwendungen hinzufügen, die innerhalb einer Organisation und ihren Bereichen erstellt werden. Wenn Sie Bereichsmanager sind, wird auf dieser Seite eine schreibgeschützte Liste der Domänen angezeigt, die dem Speicherbereich zugeordnet sind.

    Wenn Sie eine angepasste Domäne hinzufügen möchten, müssen Sie Ihren DNS-Server so konfigurieren, dass er auf die {{site.data.keyword.Bluemix_notm}}-Systemdomäne verweist. Auf diese Weise wird eine von {{site.data.keyword.Bluemix_notm}} aus Ihrer angepassten Domäne empfangene Anforderung ordnungsgemäß an Ihre App weitergeleitet. Die Systemdomäne ist für einen Bereich immer verfügbar und angepasste Domänen können auch einem Bereich zugeordnet sein. In einem Bereich erstellte Anwendungen können eine beliebige der Domänen verwenden, die für diesen Bereich aufgelistet sind. Weitere Informationen zum Erstellen und Verwenden angepasster Domänen finden Sie in [Ihre Domänen verwalten](/docs/apps?topic=creating-apps-update-domain#update-domain).

  * Klicken Sie zum Verwalten der zugeordneten Kontingente für eine Organisation auf das Aktionssymbol ![Aktionssymbol](../icons/action-menu-icon.svg) für die entsprechende Organisation und wählen Sie **Kontingente** aus.
    {: #managequota}

    Hier können Sie die Kontingentdetails für die Anzahl der Apps, die Speichermenge, die Anzahl der Services und die Plandetails anzeigen. Das Kontingent stellt die Ressourcengrenzwerte für die Organisation dar, die bei der Erstellung der Organisation zugeordnet werden. Die Ressourcen, die für eine Organisation verfügbar sind, variieren abhängig davon, ob Sie über ein kostenfreies Konto oder ein gebührenpflichtiges Konto verfügen. Jede Anwendung oder jeder Service in einem Bereich der Organisation trägt zur Nutzung des zugeordneten Kontingents bei.

    Wenn Sie das Kontingent ändern möchten, das einer Organisation zugeordnet ist, müssen Sie einen Supportfall erstellen. Weitere Informationen finden Sie in [Mit Supportfällen arbeiten](/docs/get-support?topic=get-support-open-case).

    Klicken Sie zum Anzeigen der Kontingentdetails auf der Bereichsebene für die einzelnen Standorte auf das Aktionssymbol ![Aktionssymbol](../icons/action-menu-icon.svg) für die entsprechende Organisation und wählen Sie **Kontingente** aus. Erweitern Sie dann die einzelnen Zeilen entsprechend.
