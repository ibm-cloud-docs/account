---

copyright:
  years: 2015, 2019
lastupdated: "2019-06-19"

keywords: account, add orgs, add spaces, cloud foundry orgs

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Organisationen und Bereiche hinzufügen
{: #orgsspacesusers}

Als {{site.data.keyword.Bluemix}}-Kontoeigner können Sie Organisationen und Bereiche zu Ihrem Konto hinzufügen. Als Organisationsmanager können Sie die Organisationen im Konto verwalten. 
{:shortdesc}

## Konzepte für Cloud Foundry-Organisationen
{: #cf-org-concepts}

Sie können Organisationen und Bereiche von Cloud Foundry verwalten, indem Sie **Verwalten** > **Konto** aufrufen und **Kontoressourcen > Cloud Foundry-Organisationen** auswählen.

Organisationen ermöglichen die Onlinezusammenarbeit zwischen den Benutzern und erleichtern die logische Gruppierung von Projektressourcen auf folgende Weise:

   * Sie können eine Reihe von Bereichen, Apps, Services, Domänen, Routen und Benutzern in Organisationen zusammen gruppieren.
   * Sie können den Benutzerzugriff auf die Organisationen und Bereiche auf individueller Basis verwalten.

Organisationen können mehrere Regionen umfassen und sind durch folgende Elemente definiert:

<dl>
<dt>Bereiche</dt>
<dd>Eine Untergruppe innerhalb eines Unternehmens, die Sie zum Verwalten von Anwendungen, Services und Benutzern verwenden können. Bereiche sind an eine bestimmte Region in {{site.data.keyword.Bluemix_notm}} gebunden. </dd>
<dt>Benutzer</dt>
<dd>Die Rolle mit Basisberechtigungen in Organisationen und Bereichen. Sie müssen einer Organisation zugeordnet sein, bevor Ihnen innerhalb der Organisation weitere Berechtigungen erteilt werden können. Weitere Informationen finden Sie unter [Cloud Foundry-Zugriff](/docs/iam?topic=iam-cfaccess).</dd>
<dt>Domänen</dt>
<dd>Geben Sie die Route im Internet an, die der Organisation zugeordnet ist. Eine Route enthält eine Unterdomäne und eine Domäne. Bei einer Unterdomäne handelt es sich normalerweise um den Anwendungsnamen. Eine Domäne kann eine Systemdomäne oder eine angepasste Domäne sein, die Sie für Ihre Anwendung registriert haben.<br/>
<p>Wenn Sie eine angepasste Domäne hinzufügen möchten, müssen Sie Ihren DNS-Server so konfigurieren, dass er auf die {{site.data.keyword.Bluemix_notm}}-Systemdomäne verweist. Auf diese Weise kann {{site.data.keyword.Bluemix_notm}} eine aus Ihrer angepassten Domäne empfangene Anforderung ordnungsgemäß an Ihre Anwendung weiterleiten.</p></dd>
<dt>Kontingent</dt>
<dd>Stellt die für die Organisation verfügbaren Ressourcen dar, einschließlich der Anzahl der Services und der Speicherkapazität, die für die Verwendung durch Ihre Organisation zugeordnet werden können. Kontingente werden beim Erstellen von Organisationen zugewiesen. Jede Anwendung oder jeder Service in einem Bereich einer Organisation trägt zur Nutzung des Kontingents bei. Sowohl mit dem nutzungsabhängigen Konto als auch dem Abonnementkonto können Sie Ihr Kontingent für Cloud Foundry-Anwendungen und -Container anpassen, sobald sich die Anforderungen für Ihre Organisation ändern.</dd>
</dl>

In einem Abonnementkonto ist das Kontingent eine benutzerdefinierte Begrenzung, die Benachrichtigungen über Ausgaben auslöst.
{: tip}

## Organisationen hinzufügen
{: #createorg}

Falls Sie über ein gebührenpflichtiges Konto verfügen, können Sie so viele Organisationen hinzufügen, wie erforderlich. Lite-Konten können nur eine einzige Organisation aufweisen; diese ist in Ihrem Konto bereits erstellt.

1. Rufen Sie **Verwalten** > **Konto** auf und wählen Sie **Kontoressourcen > Cloud Foundry-Organisationen** aus. Klicken Sie auf **Erstellen**.
2. Geben Sie einen Organisationsnamen ein. Der Name muss in {{site.data.keyword.Bluemix_notm}} eindeutig sein.

   Wenn der Organisationsname bereits von einem anderen öffentlichen, dedizierten oder lokalen {{site.data.keyword.Bluemix_notm}}-Benutzer verwendet wird, müssen Sie einen anderen Namen angeben.
3. Klicken Sie auf **Hinzufügen**.

Nach dem Hinzufügen der Organisation wird Ihnen automatisch die Berechtigung eines Organisationsmanagers zugewiesen, sodass Sie den Namen der Organisation bearbeiten, Benutzer hinzufügen und Bereiche in der Organisation erstellen oder löschen können.

Sie können Benutzern in einer Organisation folgende [Cloud Foundry-Rollen](/docs/iam?topic=iam-cfaccess#cfroles) zuweisen. Die Auditorrolle wird allen Benutzern, die in das Konto eingeladen wurden, standardmäßig zugewiesen.

   * Organisationsmanager
   * Abrechnungsmanager der Organisation
   * Organisationsauditor

## Bereiche hinzufügen
{: #spaceinfo}

Innerhalb einer Organisation können Sie Bereiche verwenden, um eine Reihe von Anwendungen, Services und Benutzern zu gruppieren. Bereiche werden innerhalb einer einzigen {{site.data.keyword.Bluemix_notm}}-Region definiert. Sie können auf der Basis des Bereitstellungslebenszyklus Bereiche in einer Organisation erstellen. Sie können z. B. einen Bereich `dev` als Entwicklungsumgebung, einen Bereich `test` als Testumgebung und einen Bereich `production` als Produktionsumgebung erstellen. Anschließend können Sie Ihre Apps den Bereichen zuordnen.

Führen Sie folgende Schritte aus, um einer Organisation einen Bereich hinzuzufügen.

1. Klicken Sie auf der Seite der Cloud Foundry-Organisationen auf den Namen der Organisation, der Sie einen Bereich hinzufügen wollen.
2. Klicken Sie auf **Bereich hinzufügen**.
3. Wählen Sie eine Region aus und geben Sie einen Namen ein.
4. Klicken Sie auf **Speichern**.

Nachdem Sie Benutzer zu einer Organisation hinzugefügt haben, können Sie ihnen Berechtigungen für die Bereiche erteilen. Ähnlich wie Organisationen verfügen Bereiche über eine Reihe von [Cloud Foundry-Rollen](/docs/iam?topic=iam-cfaccess#cfroles) mit bestimmten Berechtigungen, die Teammitgliedern zugeordnet sind:

  * Bereichsmanager
  * Bereichsentwickler
  * Bereichsauditor

Einem Benutzer muss mindestens eine der Berechtigungen im Bereich zugeordnet sein.
{: tip}
