---

copyright:

  years: 2015, 2018
lastupdated: "2018-03-08"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Organisationen und Bereiche erstellen
{: #orgsspacesusers}

Als Kontoeigner können Sie Ihre Organisationen und Bereiche über die Seite 'Organisationen verwalten' in der {{site.data.keyword.Bluemix}}-Konsole verwalten. Organisationsmanager können ferner die Seite 'Organisationen verwalten' verwenden, um beliebige Organisationen, für die sie als Manager festgelegt sind, zu verwalten.
{:shortdesc}

Klicken Sie zum Verwalten von Organisationen und Bereichen auf **Verwalten** &gt; **Konto** &gt; **Cloud Foundry-Organisationen**. 


## Organisationen erstellen
{: #createorg}

Organisationen können mehrere Regionen umfassen und sind durch folgende Elemente definiert:

<dl>
<dt>Benutzer</dt>
<dd>Die Rolle mit Basisberechtigungen in Organisationen und Bereichen. Sie müssen einer Organisation zugewiesen sein, bevor Ihnen weitere Berechtigungen für Bereiche innerhalb der Organisation erteilt werden können. Detaillierte Informationen hierzu finden Sie unter [Benutzer und Rollen](/docs/iam/users_roles.html#userrolesinfo).</dd>
<dt>Domänen</dt>
<dd>Stellen die Route im Internet bereit, die der Organisation zugeordnet ist. Eine Route hat eine Unterdomäne und eine Domäne. Eine Unterdomäne ist in der Regel der Anwendungsname. Eine Domäne kann eine Systemdomäne oder eine angepasste Domäne sein, die Sie für Ihre Anwendung registriert haben. Siehe den Abschnitt zum Thema [Angepasste Domänen verwalten](/docs/account/manageorg.html#managedomains).<br/>
<p>**Hinweis:** Wenn Sie eine angepasste Domäne hinzufügen, müssen Sie Ihren DNS-Server so konfigurieren, dass er Ihre angepasste Domäne in einen Verweis auf die {{site.data.keyword.Bluemix_notm}}-Systemdomäne auflöst. Auf diese Weise kann {{site.data.keyword.Bluemix_notm}} eine aus Ihrer angepassten Domäne empfangene Anforderung ordnungsgemäß an Ihre Anwendung weiterleiten.</p></dd>
<dt>Kontingent</dt>
<dd>Stellt die für die Organisation verfügbaren Ressourcen dar, einschließlich der Anzahl der Services und der Speicherkapazität, die für die Verwendung durch Ihre Organisation zugeordnet werden können. Kontingente werden bei der Erstellung von Organisationen zugeordnet. Jede Anwendung oder jeder Service in einem Bereich einer Organisation trägt zur Nutzung des Kontingents bei. Sowohl mit dem nutzungsabhängigen Konto als auch dem Abonnementkonto können Sie Ihr Kontingent für Cloud Foundry-Anwendungen und -Container anpassen, sobald sich die Anforderungen für Ihre Organisation ändern. Siehe den Abschnitt zum Thema [Kontingent verwalten](/docs/account/manageorg.html#managequota).</dd>
</dl>

In einem Abonnementkonto ist das Kontingent eine benutzerdefinierte Begrenzung, die Benachrichtigungen über Ausgaben auslöst.
{: tip}

In {{site.data.keyword.Bluemix_notm}} können Sie Organisationen verwenden, um die Onlinezusammenarbeit zwischen den Benutzern zu ermöglichen und die logische Gruppierung von Projektressourcen auf folgende Weise zu erleichtern:

   * Sie können eine Reihe von Bereichen, Apps, Services, Domänen, Routen und Benutzern in Organisationen zusammen gruppieren. 
   * Sie können den Zugriff auf die Bereiche und Organisationen auf Benutzerbasis verwalten. 

Wenn Sie eine Organisation erstellen, muss ihr Name in {{site.data.keyword.Bluemix_notm}} eindeutig sein. Falls der Organisationsname bereits von einem anderen Benutzer von {{site.data.keyword.Bluemix_notm}} Public, Dedicated oder Local verwendet wird, müssen Sie einen neuen Namen angeben. Nachdem Sie die Organisation erstellt haben, wird Ihnen automatisch die Berechtigung *Organisationsmanager* zugeordnet, die es Ihnen ermöglicht, den Organisationsnamen zu bearbeiten, Benutzer hinzuzufügen und Bereiche in der Organisation zu erstellen oder zu löschen. Wenn Sie über ein gebührenpflichtiges Konto verfügen, können Sie so viele Organisationen erstellen, wie Sie brauchen. Ein Lite-Konto lässt jedoch nur eine Organisation zu.  

Sie können Unterstützung anfordern, wenn Sie eine Organisation löschen müssen. Wenn Sie eine Organisation löschen, werden alle Bereiche, Anwendungen und Services innerhalb der Organisation gelöscht.

Die folgenden [Benutzerrollen](/docs/iam/users_roles.html#userrolesinfo) können Benutzern in einer Organisation zugeordnet werden. Allen Benutzern, die zu dem Konto eingeladen werden, wird standardmäßig die Rolle "Auditor" zugewiesen.

   * Organisationsmanager
   * Abrechnungsmanager der Organisation
   * Organisationsauditor

Sie können eine Organisation erstellen, indem Sie die folgenden Schritte ausführen:

1. Klicken Sie auf **Verwalten** &gt; **Konto** &gt; **Cloud Foundry-Organisationen**.
2. Klicken Sie auf **Neue Cloud Foundry-Organisation hinzufügen**.
3. Geben Sie den Namen der Organisation ein.
4. Klicken Sie auf **Hinzufügen**.


## Bereiche erstellen
{: #spaceinfo}

Innerhalb einer Organisation können Sie Bereiche verwenden, um eine Reihe von Anwendungen, Services und Benutzern zu gruppieren. Bereiche sind an eine bestimmte Region in {{site.data.keyword.Bluemix_notm}} gebunden.

Nachdem Sie Benutzer zu einer Organisation hinzugefügt haben, können Sie ihnen Berechtigungen für die Bereiche erteilen. Ähnlich wie Organisationen verfügen Bereiche über eine Reihe von [Benutzerrollen](/docs/iam/users_roles.html#userrolesinfo) mit bestimmten Berechtigungen, die Teammitgliedern zugeordnet sind:

  * Bereichsmanager
  * Bereichsentwickler
  * Bereichsauditor

Einem Benutzer muss mindestens eine der Berechtigungen im Bereich zugeordnet sein.
{: tip}

Sie können in Ihrer Organisation Bereiche erstellen, z. B. einen Bereich *dev* als Entwicklungsumgebung, einen Bereich *test* als Testumgebung und einen Bereich *production* als Produktionsumgebung. Anschließend können Sie Ihre Apps den Bereichen zuordnen. Führen Sie die folgenden Schritte aus, um einen Bereich zu erstellen:

1. Klicken Sie auf **Verwalten** &gt; **Konto** &gt; **Cloud Foundry-Organisationen**.
2. Ermitteln Sie die Organisation, der Sie einen Bereich hinzufügen möchten, und wählen Sie **Details anzeigen** aus.
4. Klicken Sie auf **Cloud Foundry-Bereich hinzufügen**.
5. Geben Sie den Bereichsnamen ein.
6. Klicken Sie auf **Hinzufügen**.
