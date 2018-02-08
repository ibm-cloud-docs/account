---

copyright:

  years: 2015, 2018
lastupdated: "2018-01-23"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Mit Organisationen arbeiten
Als Kontoeigner oder Organisationsmanager können Sie Management-Tasks für die Organisation, wie das Umbenennen der Organisation, das Löschen einer Organisation oder eines Bereichs, das Aktualisieren von Organisations- oder Bereichsrollen und das Verwalten von Kontingenten und Domänen, durchführen.
{:shortdesc}

Klicken Sie zum Verwalten Ihrer Organisationen in der {{site.data.keyword.Bluemix}}-Konsole auf **Verwalten > Konto > Cloud Foundry-Organisationen**. Sie können immer nur die Ressourcen einer Organisation anzeigen. Wenn Sie ein Mitglied mehrerer Organisationen sind, können Sie in der Menüleiste der Konsole über den Link mit den Benutzerkontovorgaben zwischen den Organisationen umschalten.

## Organisationen umbenennen
{: #orgrename}

Führen Sie die folgenden Schritte aus, um Ihre Organisation umzubenennen:
1. Klicken Sie auf **Verwalten** > **Konto** > **Cloud Foundry-Organisationen**.
2. Legen Sie die Organisation fest, die Sie umbenennen möchten, und klicken Sie auf **Details anzeigen**.
3. Klicken Sie auf **Cloud Foundry-Organisation bearbeiten**.
4. Klicken Sie neben dem Namen der Organisation auf **Bearbeiten**.
5. Geben Sie den neuen Organisationsnamen ein und klicken Sie auf **Speichern**.

## Organisationen und Bereiche löschen
{: #deleteorgs}

### Organisation löschen

Wenn Sie eine Organisation löschen, werden alle Bereiche, Anwendungen und Services innerhalb der Organisation gelöscht. Beachten Sie hierbei unbedingt, dass das Löschen von Operationen nicht rückgängig gemacht werden kann. 

### Bereich löschen

Führen Sie die folgenden Schritte aus, um einen Bereich zu löschen:

1. Klicken Sie auf **Verwalten** > **Konto** > **Cloud Foundry-Organisationen**.
2. Wählen Sie die Organisation aus, die bearbeitet werden soll, und klicken Sie auf **Details anzeigen**.
3. Ermitteln Sie den Bereich, den Sie löschen möchten, und klicken Sie auf **Bereich bearbeiten**.
4. Klicken Sie auf **Cloud Foundry-Bereich löschen**. 

## Benutzerrollen bearbeiten
{: #listmembers}

### Benutzerrollen für eine bestimmte Organisation bearbeiten 

Führen Sie die folgenden Schritte aus, um die Benutzerrollen für eine bestimmte Organisation zu bearbeiten:

1. Klicken Sie auf **Verwalten** > **Konto** > **Cloud Foundry-Organisationen**.
2. Legen Sie die Organisation fest, die Sie bearbeiten möchten, und klicken Sie auf **Details anzeigen** und dann auf **Organisation bearbeiten**.
4. Sie können die Mitglieder Ihrer Organisation und deren Rollen auf der Registerkarte **Benutzer** anzeigen.

### Benutzerrollen für einen bestimmten Bereich bearbeiten

Führen Sie die folgenden Schritte aus, um die Benutzerrollen für einen bestimmten Bereich zu bearbeiten:

1. Klicken Sie auf **Verwalten** > **Konto** > **Cloud Foundry-Organisationen**.
2. Wählen Sie die Organisation aus, deren Mitglieder Sie anzeigen möchten, und klicken Sie auf **Details anzeigen**.
3. Ermitteln Sie den Bereich, den Sie bearbeiten möchten, und klicken Sie auf **Bereich bearbeiten**.
4. Sie können die Mitglieder Ihres Bereichs und deren Rollen auf der Registerkarte **Benutzer** anzeigen.

## Kontingent verwalten
{: #managequota}

Als {{site.data.keyword.Bluemix_notm}}-Kontoeigner oder -Organisationsmanager können Sie das verwendete und zugeordnete Kontingent für eine Organisation anzeigen. Das Kontingent stellt die Ressourcengrenzen für die Organisation dar, die beim Erstellen der Organisation zugeordnet wird. Die Ressourcen, die für eine Organisation verfügbar sind, variieren abhängig davon, ob Sie über ein kostenloses Konto oder ein gebührenpflichtiges Konto verfügen. Jede Anwendung oder jeder Service in einem Bereich der Organisation trägt zur Nutzung des zugeordneten Kontingents bei.

Führen Sie die folgenden Schritte aus, um das verwendete und zugeordnete Kontingent für eine Organisation anzuzeigen:

1. Klicken Sie auf **Verwalten** &gt; **Konto** &gt; **Cloud Foundry-Organisationen**.
2. Ermitteln Sie die Organisation, deren Kontingent Sie anzeigen möchten, und klicken Sie auf **Details anzeigen**.
3. Klicken Sie auf **Organisation bearbeiten**.
4. Wenn Bereiche in mehreren Regionen definiert wurden, dann wählen Sie die Region aus, die Sie anzeigen möchten.
5. Klicken Sie auf **Kontingent**. 
6. Standardmäßig wird die Kontingentseite **Cloud Foundry** geöffnet. Sie können die Kontingentdetails für die folgenden Ressourcen anzeigen:
 * SPEICHER
 * SERVICES
 * PLAN
 * PREIS
7. Klicken Sie auf **Container**, um die verwendete und verfügbare Containerkontingentzuordnung anzuzeigen. Die Containerzuordnung variiert abhängig von Ihrem Preistarif. Sie können die Kontingentdetails für die folgenden Ressourcen anzeigen:
 * SPEICHER
 * ÖFFENTLICHE IP
 * DATEIFREIGABEN
8. Klicken Sie auf **Virtuelle Server**, um die virtuellen Maschinen anzuzeigen.

In der {{site.data.keyword.Bluemix_notm}}-Region 'Sydney' stehen keine Container zur Verfügung. 
{: tip}

Weitere Informationen zu Containern finden Sie unter dem Thema [Kontingent](/docs/containers/container_planning.html#container_planning_quota) in der Dokumentation zu Containern.
Um das Kontingent zu ändern, das einer Organisation zugeordnet ist, müssen Sie ein Support-Ticket öffnen. Weitere Informationen zum Öffnen eines Support-Tickets finden Sie unter dem Thema [Kundenunterstützung abrufen](/docs/get-support/howtogetsupport.html#getting-customer-support). 

## Domänen verwalten
{: #managedomains}

Als {{site.data.keyword.Bluemix_notm}}-Kontoeigner oder -Organisationsmanager können Sie die Systemdomäne anzeigen und angepasste Domänen für Anwendungen hinzufügen, die innerhalb einer Organisation und ihren Bereichen erstellt werden. Als Bereichsmanager enthält Ihre Registerkarte **Domänen** für einen Bereich eine schreibgeschützte Liste der Domänen, die dem Bereich zugeordnet sind.

1. Klicken Sie auf **Verwalten** &gt; **Konto** &gt; **Cloud Foundry-Organisationen**.
2. Ermitteln Sie die Organisation, für die Sie Domänen anzeigen oder bearbeiten möchten.
3. Wählen Sie **Details anzeigen** für diese Organisation aus.
4. Klicken Sie auf **Organisation bearbeiten**.
5. Klicken Sie auf **Domänen**.

Wenn Sie eine angepasste Domäne hinzufügen möchten, müssen Sie Ihren DNS-Server so konfigurieren, dass er auf die {{site.data.keyword.Bluemix_notm}}-Systemdomäne verweist. Auf diese Weise kann {{site.data.keyword.Bluemix_notm}} eine aus Ihrer angepassten Domäne empfangene Anforderung ordnungsgemäß an Ihre App weiterleiten. Die Systemdomäne ist für einen Bereich immer verfügbar und angepasste Domänen können auch einem Bereich zugeordnet sein. In einem Bereich erstellte Anwendungen können eine der Domänen verwenden, die für diesen Bereich aufgelistet sind. Weitere Informationen zum Erstellen und Verwenden angepasster Domänen finden Sie unter [Angepasste Domäne verwenden](/docs/apps/updapps.html#domain).
