---

copyright:

  years: 2015, 2018
lastupdated: "2018-05-21"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Organisationen und Bereiche aktualisieren
{: #orgupdates}

Als Kontoeigner oder Organisationsmanager können Sie Management-Tasks auf der Organisationsebene und der Bereichsebene ausführen. Zu diesen Tasks gehören die Umbenennung einer Organisation oder eines Bereichs, die Zuweisung oder Aktualisierung von Cloud Foundry-Benutzerrollen, die Verwaltung von Domänen und die Anzeige von Details zum Organisationskontingent. 
{:shortdesc}

Klicken Sie zum Verwalten Ihrer Organisationen in der {{site.data.keyword.Bluemix}}-Konsole auf **Verwalten > Konto > Cloud Foundry-Organisationen**. Sie können immer nur die Ressourcen einer Organisation anzeigen. Wenn Sie ein Mitglied mehrerer Organisationen sind, können Sie in der Menüleiste der Konsole über den Link mit den Benutzerkontovorgaben zwischen den Organisationen umschalten.

## Organisationen umbenennen
{: #orgrename}

Führen Sie die folgenden Schritte aus, um Ihre Organisation umzubenennen. Beachten Sie, dass alle Änderungen, die Sie vornehmen, für alle Benutzer in der Organisation gelten.

1. Klicken Sie auf **Verwalten** > **Konto** > **Cloud Foundry-Organisationen**.
2. Klicken Sie auf das Symbol 'Aktionen' der Organisation, die Sie umbenennen möchten, und wählen Sie **Umbenennen** aus.  
3. Geben Sie den neuen Namen ein und klicken Sie auf **Speichern**.

## Organisationen und Bereiche löschen
{: #deleteorgs}

### Organisation löschen

Wenden Sie sich an den [-Support](/docs/get-support/howtogetsupport.html), um eine Organisation zu löschen. Beim Löschen einer Organisation werden alle Bereiche und Ressourcen in der Organisation ebenfalls gelöscht. Beachten Sie hierbei unbedingt, dass das Löschen von Operationen nicht rückgängig gemacht werden kann. 

### Bereich löschen

Wenn Sie einen Bereich löschen, werden alle darin enthaltenen Ressourcen und Benutzer ebenfalls gelöscht. Führen Sie die folgenden Schritte aus, um einen Bereich zu löschen:

1. Klicken Sie auf **Verwalten** > **Konto** > **Cloud Foundry-Organisationen**.
2. Klicken Sie auf die Organisation, in der der Bereich zugewiesen wird.
3. Klicken Sie auf das Symbol 'Aktionen' und wählen Sie **Löschen** aus.
4. Bestätigen Sie, dass der Bereich gelöscht werden soll, indem Sie den Bereichsnamen in das Feld eingeben und auf **Löschen** klicken.

## Benutzerrollen bearbeiten
{: #listmembers}

Die Rollen, die Sie auf Organisationsebene zuweisen können, sind 'Manager', 'Abrechnungsmanager' und 'Auditor'. Die Rollen, die Sie auf Bereichsebene zuweisen können, sind 'Manager', 'Entwickler' und 'Auditor'. Nähere Beschreibungen der Rollen finden Sie unter [Cloud Foundry-Rollen](/docs/iam/cfaccess.html#cfroles).

### Benutzerrollen auf Organisationsebene bearbeiten

Führen Sie die folgenden Schritte aus, um die Benutzerrollen für eine bestimmte Organisation zu bearbeiten:

1. Klicken Sie auf **Verwalten** > **Konto** > **Cloud Foundry-Organisationen**.
2. Klicken Sie auf das Symbol 'Aktionen' und wählen Sie **Benutzer** aus.
3. Je nachdem, wie Sie die Benutzerberechtigungen ändern wollen, aktivieren oder inaktivieren Sie das Kontrollkästchen einer bestimmten Rolle.
4. Bestätigen Sie Ihre Änderungen, indem Sie auf **Speichern** klicken. 

### Benutzerrollen auf Bereichsebene bearbeiten

Führen Sie die folgenden Schritte aus, um die Benutzerrollen für einen bestimmten Bereich zu bearbeiten:

1. Klicken Sie auf **Verwalten** > **Konto** > **Cloud Foundry-Organisationen**.
2. Klicken Sie auf die Organisation, in der der Bereich zugewiesen wird.
3. Klicken Sie auf den Namen des Bereichs.
4. Je nachdem, wie Sie die Benutzerberechtigungen ändern wollen, aktivieren oder inaktivieren Sie das Kontrollkästchen einer bestimmten Rolle.
5. Bestätigen Sie Ihre Änderungen, indem Sie auf **Speichern** klicken.

## Domänen verwalten
{: #managedomains}

Als Kontoeigner oder Organisationsmanager können Sie die Systemdomäne anzeigen und angepasste Domänen für Anwendungen hinzufügen, die innerhalb einer Organisation und ihren Bereichen erstellt werden. Als Bereichsmanager enthält die Registerkarte **Domänen** eine schreibgeschützte Liste der Domänen, die dem Bereich zugeordnet sind.

1. Klicken Sie auf **Verwalten** &gt; **Konto** &gt; **Cloud Foundry-Organisationen**.
2. Klicken Sie auf das Symbol 'Aktionen' der Organisation und wählen Sie **Domänen** aus.

Wenn Sie eine angepasste Domäne hinzufügen möchten, müssen Sie Ihren DNS-Server so konfigurieren, dass er auf die {{site.data.keyword.Bluemix_notm}}-Systemdomäne verweist. Auf diese Weise wird eine von {{site.data.keyword.Bluemix_notm}} aus Ihrer angepassten Domäne empfangene Anforderung ordnungsgemäß an Ihre App weitergeleitet. Die Systemdomäne ist für einen Bereich immer verfügbar und angepasste Domänen können auch einem Bereich zugeordnet sein. In einem Bereich erstellte Anwendungen können eine der Domänen verwenden, die für diesen Bereich aufgelistet sind. Weitere Informationen zum Erstellen und Verwenden angepasster Domänen finden Sie unter [Angepasste Domäne verwenden](/docs/apps/updapps.html#domain).

## Kontingent verwalten
{: #managequota}

Sie können das verwendete und zugeordnete Kontingent für eine Organisation anzeigen. Das Kontingent stellt die Ressourcengrenzen für die Organisation dar, die beim Erstellen der Organisation zugeordnet wird. Die Ressourcen, die für eine Organisation verfügbar sind, variieren abhängig davon, ob Sie über ein kostenloses Konto oder ein gebührenpflichtiges Konto verfügen. Jede Anwendung oder jeder Service in einem Bereich der Organisation trägt zur Nutzung des zugeordneten Kontingents bei.

Führen Sie die folgenden Schritte aus, um das verwendete und zugeordnete Kontingent für eine Organisation anzuzeigen:

1. Klicken Sie auf **Verwalten** &gt; **Konto** &gt; **Cloud Foundry-Organisationen**.
2. Klicken Sie auf das Symbol 'Aktionen' der jeweiligen Organisation und wählen Sie **Kontingente** aus.

   Standardmäßig wird die Kontingentseite **Cloud Foundry** angezeigt. Hier können Sie die Kontingentdetails für die folgenden Ressourcen anzeigen:
 
   * Die Anzahl der Apps.
   * Die Speicherkapazität. 
   * Die Anzahl der Services. 
   * Plandetails. 

3. Erweitern Sie die Zeilen, um für jede Region die Kontingentdetails auf Bereichsebene anzuzeigen.  

Um das Kontingent zu ändern, das einer Organisation zugeordnet ist, müssen Sie ein Support-Ticket öffnen. Weitere Informationen finden Sie unter [Kundenunterstützung abrufen](/docs/get-support/howtogetsupport.html#getting-customer-support). 

