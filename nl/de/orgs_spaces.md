---

copyright:

  years: 2015, 2019
lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Organisationen und Bereiche hinzufügen
{: #orgsspacesusers}

Als {{site.data.keyword.Bluemix}}-Kontoeigner können Sie Organisationen und Bereiche zu Ihrem Konto hinzufügen. Als Organisationsmanager können Sie die Organisationen im Konto verwalten. Rufen Sie **Verwalten** > **Konto** auf und wählen Sie **Cloud Foundry-Organisationen** aus.
{:shortdesc}

Sie können Organisationen verwenden, um die Onlinezusammenarbeit zwischen den Benutzern zu ermöglichen und die logische Gruppierung von Projektressourcen auf folgende Weise zu erleichtern:

   * Sie können eine Reihe von Bereichen, Apps, Services, Domänen, Routen und Benutzern in Organisationen zusammen gruppieren.
   * Sie können den Benutzerzugriff auf die Organisationen und Bereiche auf individueller Basis verwalten.

## Organisationen hinzufügen
{: #createorg}

Organisationen können mehrere Regionen umfassen und sind durch folgende Elemente definiert:

<dl>
<dt>Benutzer</dt>
<dd>Die Rolle mit Basisberechtigungen in Organisationen und Bereichen. Sie müssen einer Organisation zugewiesen sein, bevor Ihnen weitere Berechtigungen für Bereiche innerhalb der Organisation erteilt werden können. Weitere Informationen finden Sie unter [Benutzer und Rollen](/docs/iam?topic=iam-userroles).</dd>
<dt>Domänen</dt>
<dd>Geben Sie die Route im Internet an, die der Organisation zugeordnet ist. Eine Route enthält eine Unterdomäne und eine Domäne. Bei einer Unterdomäne handelt es sich normalerweise um den Anwendungsnamen. Eine Domäne kann eine Systemdomäne oder eine angepasste Domäne sein, die Sie für Ihre Anwendung registriert haben.<br/>
<p>Wenn Sie eine angepasste Domäne hinzufügen möchten, müssen Sie Ihren DNS-Server so konfigurieren, dass er auf die {{site.data.keyword.Bluemix_notm}}-Systemdomäne verweist. Auf diese Weise kann {{site.data.keyword.Bluemix_notm}} eine aus Ihrer angepassten Domäne empfangene Anforderung ordnungsgemäß an Ihre Anwendung weiterleiten.</p></dd>
<dt>Kontingent</dt>
<dd>Stellt die für die Organisation verfügbaren Ressourcen dar, einschließlich der Anzahl der Services und der Speicherkapazität, die für die Verwendung durch Ihre Organisation zugeordnet werden können. Kontingente werden beim Erstellen von Organisationen zugewiesen. Jede Anwendung oder jeder Service in einem Bereich einer Organisation trägt zur Nutzung des Kontingents bei. Sowohl mit dem nutzungsabhängigen Konto als auch dem Abonnementkonto können Sie Ihr Kontingent für Cloud Foundry-Anwendungen und -Container anpassen, sobald sich die Anforderungen für Ihre Organisation ändern.</dd>
</dl>

In einem Abonnementkonto ist das Kontingent eine benutzerdefinierte Begrenzung, die Benachrichtigungen über Ausgaben auslöst.
{: tip}

Wenn Sie eine Organisation hinzufügen, muss ihr Name in {{site.data.keyword.Bluemix_notm}} eindeutig sein. Falls der Organisationsname bereits von einem anderen Benutzer von {{site.data.keyword.Bluemix_notm}} Public, Dedicated oder Local verwendet wird, müssen Sie einen neuen Namen angeben. Nachdem Sie die Organisation hinzugefügt haben, wird Ihnen automatisch die Berechtigung eines Organisationsmanagers zugeordnet, die es Ihnen ermöglicht, den Organisationsnamen zu bearbeiten, Benutzer hinzuzufügen und Bereiche in der Organisation zu erstellen oder zu löschen. Wenn Sie über ein gebührenpflichtiges Konto verfügen, können Sie so viele Organisationen hinzufügen, wie Sie benötigen. Ein Lite-Konto lässt jedoch nur eine einzige Organisation zu.

Die folgenden [Benutzerrollen](/docs/iam?topic=iam-userroles) können Benutzern in einer Organisation zugeordnet werden. Allen Benutzern, die zu dem Konto eingeladen werden, wird standardmäßig die Rolle 'Auditor' zugewiesen.

   * Organisationsmanager
   * Abrechnungsmanager der Organisation
   * Organisationsauditor

Führen Sie die folgenden Schritte aus, um eine Organisation hinzuzufügen:

  1. Klicken Sie auf **Organisation hinzufügen**.
  2. Geben Sie den Namen der Organisation ein.  
  3. Klicken Sie auf **Hinzufügen**.

<!-- Add info on Manage infrastructure option under a space -->

## Bereiche hinzufügen
{: #spaceinfo}

Innerhalb einer Organisation können Sie Bereiche verwenden, um eine Reihe von Anwendungen, Services und Benutzern zu gruppieren. Bereiche sind an eine bestimmte Region in {{site.data.keyword.Bluemix_notm}} gebunden. Sie können auf der Basis des Bereitstellungslebenszyklus Bereiche in einer Organisation erstellen. Sie können z. B. einen Bereich `dev` als Entwicklungsumgebung, einen Bereich `test` als Testumgebung und einen Bereich `production` als Produktionsumgebung erstellen. Anschließend können Sie Ihre Apps den Bereichen zuordnen.

Nachdem Sie Benutzer zu einer Organisation hinzugefügt haben, können Sie ihnen Berechtigungen für die Bereiche erteilen. Ähnlich wie Organisationen verfügen Bereiche über eine Reihe von [Cloud Foundry-Rollen](/docs/iam?topic=iam-cfroles) mit bestimmten Berechtigungen, die Teammitgliedern zugeordnet sind:

  * Bereichsmanager
  * Bereichsentwickler
  * Bereichsauditor

Einem Benutzer muss mindestens eine der Berechtigungen im Bereich zugeordnet sein.
{: tip}

Führen Sie die folgenden Schritte aus, um einen Bereich hinzuzufügen:

  1. Klicken Sie auf den Namen der Organisation, der Sie einen Bereich hinzufügen möchten.
  2. Klicken Sie auf **Bereich hinzufügen**.
  3. Wählen Sie eine Region aus und geben Sie einen Namen ein.
  4. Klicken Sie auf **Speichern**.
