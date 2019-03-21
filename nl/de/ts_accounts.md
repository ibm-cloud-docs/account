---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-13"

keywords: troubleshoot account, account problem, account support, account help, org error, resource error, error message

subcollection: account
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Fehlerbehebung für die Verwaltung von Konten
{: #managingaccounts}

Allgemeine Probleme bei der Verwaltung Ihres Kontos können sein, dass verschiedene Apps denselben Domänennamen verwenden oder Administratoren nicht alle Organisationen anzeigen können. In vielen Fällen können Sie diese Probleme durch Ausführen weniger einfacher Schritte beheben.
{:shortdesc}


## Warum kann ich nicht auf einen anderen {{site.data.keyword.Bluemix_notm}}-Standort zugreifen?
{: #nosecondreg}
{: troubleshoot}

Sie können keinen neuen Standort erstellen, da Ihr Kontotyp dies nicht zulässt.

Sie erhalten eine Fehlernachricht, wenn Sie versuchen, einen neuen {{site.data.keyword.Bluemix_notm}}-Standort zu erstellen.
{: tsSymptoms}

Dies liegt wahrscheinlich daran, dass Sie ein Lite-Konto verwenden, das die Entwicklung an nur einem öffentlichen Standort unterstützt.
{: tsCauses}

Wenn Sie auf weitere Standorte zugreifen möchten, müssen Sie ein Upgrade auf ein kostenpflichtiges Konto durchführen. Rufen Sie **Verwalten > Abrechnung und Nutzung** auf und wählen Sie **Zahlungen** aus.
{: tsResolve}


## Warum kann ich keine neue Organisation erstellen?
{: #nosecondorg}
{: troubleshoot}

Sie versuchen, mehr als eine Organisation zu erstellen, verfügen aber über ein Lite-Konto.  

Sie erhalten eine Fehlernachricht, wenn Sie versuchen, eine neue Organisation zu erstellen.
{: tsSymptoms}

Dies liegt wahrscheinlich daran, dass Sie ein Lite-Konto verwenden, das die Entwicklung in nur einer Organisation unterstützt.
{: tsCauses}

Wenn Sie eine neue Organisation erstellen möchten, müssen Sie ein Upgrade auf ein kostenpflichtiges Konto durchführen. Rufen Sie **Verwalten > Abrechnung und Nutzung** auf und wählen Sie **Upgrades** aus.
{: tsResolve}


## Warum kann ich keine neue Instanz eines Lite-Plans erstellen?
{: #nosecondlite}
{: troubleshoot}

Sie versuchen, eine zusätzliche Instanz zu erstellen, verfügen aber über ein Lite-Konto.

Sie erhalten die folgende Fehlernachricht, wenn Sie versuchen, eine neue Instanz eines Lite-Plans zu erstellen:
{: tsSymptoms}

`Fehler beim Erstellen einer neuen Lite-Instanz`

Es gilt eine Begrenzung von einer Instanz pro Lite-Plan, damit diese Pläne weiterhin kostenfrei angeboten werden können.
{: tsCauses}

Sie können weitere Instanzen des Service erstellen, indem Sie einen der abrechenbaren Servicepläne auswählen, die unter den gebührenpflichtigen Konten verfügbar sind. Wenn Sie ein Upgrade auf ein kostenpflichtiges Konto über die Konsole durchführen möchten, rufen Sie **Verwalten > Abrechnung und Nutzung** auf und wählen Sie **Upgrades** aus.
{: tsResolve}

Wenn Sie kein Upgrade für ein Lite-Konto durchführen möchten und Ihre vorhandene Lite-Serviceinstanz nicht mehr verwenden, können Sie die vorhandene Lite-Planinstanz über das Dashboard löschen und dann eine neue Instanz erstellen.


## Wie wurde das zulässige Laufzeitspeicherkontingent überschritten?
{: #noruntimemem}
{: troubleshoot}

Sie haben die zulässige Speichermenge für Ihr Konto überschritten.

Sie können keine Apps bereitstellen und erhalten eine Fehlermeldung, dass Sie die Speicherbegrenzung Ihrer Organisation überschritten haben.
{: tsSymptoms}

Bei einem Lite-Konto können Ihre Cloud Foundry-Apps bis zu 256 MB des sofort verfügbaren Laufzeitspeichers verwenden. Für kostenpflichtige Konten gilt eine Speicherbegrenzung von 2 GB.
{: tsCauses}

Wenn Sie mit einem Lite-Konto arbeiten, können Sie weiteren Speicher durch ein Upgrade auf ein kostenpflichtiges Konto erhalten. Rufen Sie **Verwalten > Abrechnung und Nutzung** auf und wählen Sie **Upgrades** aus.
{: tsResolve}

Wenn Sie kein Upgrade für ein Lite-Konto durchführen möchten, aber über inaktive Apps verfügen, können Sie diese löschen, um etwas Laufzeitspeicher freizugeben.


## Warum ist mein Konto inaktiv?
{: #ts_accnt_inactive}
{: troubleshoot}

Wenn Ihr Konto inaktiv ist, können Sie keine App in {{site.data.keyword.Bluemix_notm}} erstellen. Wenden Sie sich zur Lösung dieses Problems an das Support-Team.

Beim Erstellen einer App in {{site.data.keyword.Bluemix_notm}} wird die folgenden Fehlernachricht angezeigt:
{: tsSymptoms}

`BXNUI0096E: Die App wurde nicht erstellt. Ihr Konto ist inaktiv, da es storniert oder ausgesetzt wurde.`

Der Status Ihres {{site.data.keyword.Bluemix_notm}}-Kontos verändert sich in 'Inaktiv', wenn es storniert oder ausgesetzt wurde.
{: tsCauses}

Wenn Sie das Konto reaktivieren möchten, öffnen Sie einen Fall im [Support Center](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link"). Geben Sie für Ihren Fall die folgenden Informationen an:
{: tsResolve}

  * Die IBMid, mit der Sie sich bei {{site.data.keyword.Bluemix_notm}} anmelden.
  * Der Name der Organisation, in der Ihre App erstellt wird. Mithilfe dieser Informationen kann das Support-Team feststellen, ob Ihnen die richtigen Rollen bzw. die richtige Zugehörigkeit in Ihrer Organisation zugewiesen wurden.


## Warum kann ich keine Benutzer zu einer Organisation hinzufügen?
{: #ts_adduser}
{: troubleshoot}

Sie können nur dann Benutzer in Ihre Organisation einladen, wenn Sie der Kontoeigner sind oder wenn Sie sowohl ein Manager als auch ein Mitglied der Organisation sind.

Sie können den Link **Neuen Benutzer einladen** im Abschnitt **Organisation verwalten** nicht anzeigen.
{: tsSymptoms}

Nur die folgenden {{site.data.keyword.Bluemix_notm}}-Benutzer können Benutzer zu einer Organisation einladen:
{: tsCauses}
  * Der Kontoeigner der Organisation
  * Organisationsmanager, die gleichzeitig Mitglieder - nicht Collaborators - der Organisation sind

In {{site.data.keyword.Bluemix_notm}} können Sie entweder ein Mitglied oder ein Collaborator einer Organisation sein:

<dl><dt>Collaborator</dt>
<dd>Sie sind ein Collaborator einer Organisation, wenn Sie bereits über ein {{site.data.keyword.Bluemix_notm}}-Konto verfügen und von einer anderen Person in die Organisation eingeladen werden.</dd>
<dt>Mitglied</dt>
<dd>Sie sind ein Mitglied einer Organisation, wenn Sie nicht über ein {{site.data.keyword.Bluemix_notm}}-Konto verfügen, jedoch von einer anderen Person in die Organisation eingeladen werden und sich über die Einladung bei {{site.data.keyword.Bluemix_notm}} registrieren.</dd>
</dl>

Sie können keine Benutzer in Ihre Organisation einladen, wenn Sie ein Collaborator der Organisation sind, selbst dann nicht, wenn Sie als Organisationsmanager zugewiesen sind.

Alle Organisationsmanager, einschließlich Collaborators in einer Organisation, können Benutzer hinzufügen, ändern und entfernen, die bereits in der Organisation sind.
{: note}

Wenn Sie keine Benutzer in Ihre Organisation einladen können und hierfür eine andere Rolle benötigen, bitten Sie den zuständigen Organisationsmanager, Ihre Rolle zu ändern. Führen Sie die folgenden Schritte aus, um festzustellen, wer Ihr Organisationsmanager ist:
{: tsResolve}

  1. Klicken Sie in der Menüleiste der Konsole auf **Verwalten > Konto** und wählen Sie **Ansprechpartner im Unternehmen** aus.
  2. Wechseln Sie zu Ihrer Organisation und zeigen Sie die Informationen zum Organisationsmanager in der Registerkarte **Benutzer** an.  

Wenn Sie keine Benutzer einladen können, weil Sie ein Collaborator, aber kein Mitglied sind, müssen Sie Ihr vorheriges {{site.data.keyword.Bluemix_notm}}-Konto löschen. Anschließend müssen Sie als Mitglied der Organisation in das Konto eingeladen werden. Führen Sie die folgenden Schritte aus, um Ihr vorheriges Konto zu löschen und als Mitglied in das Konto eingeladen zu werden:

  1. Wenden Sie sich an den [{{site.data.keyword.Bluemix_notm}} Support ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window}, um einen Supportfall zu öffnen und das Löschen Ihres Kontos anzufordern. Wenn Sie über Daten verfügen, die Ihrem alten Konto zugeordnet sind, die jedoch gesichert und in das neue Konto übernommen werden sollen, dann geben Sie die entsprechenden Informationen in Ihrer E-Mail an.
  2. Nachdem Ihr Konto gelöscht wurde, bitten Sie einen Benutzer mit der Rolle eines Organisationsmanagers, Sie als Organisationsmanager in die Organisation einzuladen. Führen Sie dann von der Einladung aus eine Registrierung für {{site.data.keyword.Bluemix_notm}} durch.


## Warum sind meiner Organisation keine Bereiche zugeordnet?
{: #ts_no_space}
{: troubleshoot}

Wenn Ihrer momentanen Organisation kein Bereich zugeordnet ist, können Sie keine App erstellen.

Beim Erstellen einer App wird die folgende Fehlernachricht angezeigt:
{: tsSymptoms}

`BXNUI0097E: Bevor Sie eine App hinzufügen können, muss Ihrer Organisation und Ihrer Region mindestens ein Bereich zugeordnet sein. Klicken Sie auf dem Dashboard auf die Option 'Bereich erstellen'. Wiederholen Sie den Vorgang, wenn der Bereich erstellt worden ist. `

Apps müssen innerhalb eines Bereichs unter Ihrer Organisation erstellt werden.
{: tsCauses}

Verwenden Sie eine der folgenden Methoden, um einen Bereich zu erstellen:
{: tsResolve}

  * Klicken Sie in der Menüleiste der Konsole auf **Verwalten > Konto** und wählen Sie **Organisationen** aus. Wählen Sie anschließend die Organisation aus, in der Sie den Bereich erstellen möchten und klicken Sie auf **Bereich erstellen**.
  * Geben Sie in der {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle Folgendes ein: `ibmcloud account space-create <space_name> -o <organization_name>`.


## Warum verwenden einige Apps einen Domänennamen gemeinsam?
{: #ts_domain_diff}
{: troubleshoot}

Es kann vorkommen, dass in {{site.data.keyword.Bluemix_notm}} eine URL von mehreren Apps gemeinsam genutzt wird.

Dieses Problem kann auftreten, wenn Sie unterschiedlichen Apps in einem Bereich dieselbe URL-Route zuweisen.
{: tsCauses}

Beispiel: Sie übertragen die App 'myApp1' per Push-Operation an {{site.data.keyword.Bluemix_notm}} und legen als Domäne `mynewapp.us-east.cf.appdomain.cloud` fest. Anschließend übertragen Sie eine weitere App mit dem Namen 'myApp2' per Push-Operation in denselben Bereich und legen für eine der URL-Routen den Namen `mynewapp.us-east.cf.appdomain.cloud` fest. Die Route ist jetzt beiden Apps zugeordnet.

Hierbei handelt es sich um ein unterstütztes Verhalten; Sie können dieses Verfahren verwenden, um beim Upgrade einer App Ausfallzeiten vollständig zu vermeiden. Weitere Informationen finden Sie in [Ausfallzeiten vermeiden](/docs/overview?topic=overview-zero-downtime).
{: tsResolve}


## Warum können Administratoren nicht alle Organisationen über die Konsole anzeigen?
{: #ts_ui_org}
{: troubleshoot}

Als Administrator können Sie nicht jede Organisation zur Verwaltung anzeigen, wenn Sie die {{site.data.keyword.Bluemix_notm}}-Konsole verwenden. Sie können nur die Organisationen anzeigen und verwalten, zu denen Sie gehören.

Als Administrator können Sie nicht alle Organisationen über die Konsole anzeigen.
{: tsSymptoms}

Hierbei handelt es sich um eine Einschränkung der Konsole.
{: tsCauses}

Sie können Befehle wie z. B. `ibmcloud account orgs` und `ibmcloud account org-create` über die {{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle verwenden, um alle Organisationen zu verwalten. Geben Sie `ibmcloud account help` ein, um eine vollständige Liste der Befehle zu erhalten.
{: tsResolve}


## Warum kann ich meine Kreditkarteninformationen nicht hinzufügen?
{: #ts_addcc}
{: troubleshoot}

Sie können Ihre Kreditkarteninformationen nicht senden, um für Ihr Lite-Konto ein Upgrade auf ein kostenpflichtiges Konto durchzuführen.

Die Schaltfläche **Senden** auf der Seite 'Kreditkarte hinzufügen' ist inaktiviert.
{: tsSymptoms}

Dieses Problem tritt auf, wenn Sie auf der Seite 'Kreditkarte hinzufügen' die Informationen nicht korrekt eingegeben haben.
{: tsCauses}

Führen Sie die folgenden Schritte aus:
{: tsResolve}

  1. Füllen Sie auf der Seite 'Kreditkarte hinzufügen' alle erforderlichen Felder aus.
  2. Wählen Sie das Kontrollkästchen unter **Ich habe die allgemeinen Geschäftsbedingungen von IBM gelesen und stimme ihnen zu** aus und klicken Sie auf **Senden**.
