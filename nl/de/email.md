---

copyright:

  years: 2015, 2018
lastupdated: "2018-11-28"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# E-Mail-Vorgaben festlegen
{: #email-prefs}

Abhängig vom jeweiligen {{site.data.keyword.Bluemix}}-Kontotyp können Sie auswählen, ob Sie E-Mail-Benachrichtigungen zu geplanten und ungeplanten Ereignissen der {{site.data.keyword.Bluemix}}-Plattform oder zu ungeplanten Ergeinissen, Wartungsarbeiten und Ankündigungen der Infrastruktur erhalten möchten. Darüber hinaus können Sie Benachrichtigungsabonnements für Ereignisse der klassischen Infrastruktur festlegen.
{: shortdesc}

## Plattformbenachrichtigungen festlegen
{: #setting-platform-notifications}

Wenn Sie ein Lite-Kontoeigner sind, können Sie auswählen, ob Sie E-Mail-Benachrichtigungen über ungeplante Ereignisse auf der {{site.data.keyword.Bluemix}}-Plattform wie beispielsweise Ausfälle und geplante Ereignisse wie beispielsweise Wartungen erhalten möchten. Wenn Sie Benachrichtigungen für die {{site.data.keyword.Bluemix_notm}}-Plattform festlegen, erhalten Sie ausschließlich E-Mail-Benachrichtigungen, die der {{site.data.keyword.Bluemix_notm}}-Plattform zugeordnet sind. Sie erhalten keine E-Mail-Benachrichtigungen zu Ereignissen, die {{site.data.keyword.Bluemix_notm}}-Services zugeordnet sind. 

Sie können E-Mail-Benachrichtigungen der Plattform nur für Ihr Profil festlegen, nicht für das Konto. Mit anderen Worten: Wenn Sie zu einem anderen Konto wechseln, beziehen sich alle von Ihnen vorgenommenen Aktualisierungen der Plattformbenachrichtigungen auf Ihr Profil, nicht auf das Konto, zu dem Sie gewechselt haben. 

Wenn Sie die Option auswählen, mit der Sie Benachrichtigungen zu ungeplanten Plattformereignissen erhalten, erhalten Sie nur E-Mails zu Problemen, die einen Ausfall verursachen können (Priorität 1). Sie können zu jedem beliebigen Zeitpunkt alle geplanten und ungeplanten Ereignisse über die Seite [Status ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/status){: new_window} anzeigen. 

1. Rufen Sie das Avatarsymbol ![Avatarsymbol](../icons/i-avatar-icon.svg) &gt; **Profil und Einstellungen** auf. 
2. Klicken Sie auf **Benachrichtigungen**. 
3. Wählen Sie für jede Kategorie, die Sie aktualisieren möchten, aus, ob Sie Plattformbenachrichtigungen erhalten möchten. 

  Standardmäßig sind alle {{site.data.keyword.Bluemix_notm}}-Plattformbenachrichtigungen inaktiviert.
  {: tip}

4. Klicken Sie auf **Speichern**. 

## Infrastrukturbenachrichtigungen festlegen

Wenn Sie Eigner eines nutzungsabhängigen Kontos oder eines Abonnementkontos sind, können Sie auswählen, ob Sie E-Mail-Benachrichtigungen der {{site.data.keyword.Bluemix_notm}}-Infrastruktur zu ungeplanten Ereignissen, Wartungsarbeiten und Ankündigungen erhalten möchten. Infrastrukturbenachrichtigungen beziehen sich auf das Konto, zu dem Sie gewechselt haben. Sie können zu einem anderen Konto wechseln und Benachrichtigungen für dieses Konto verwalten. 

1. Rufen Sie das Avatarsymbol ![Avatarsymbol](../icons/i-avatar-icon.svg) &gt; **Profil und Einstellungen** auf. 
2. Klicken Sie auf **Benachrichtigungen**. 
3. Wählen Sie für jede Kategorie, die Sie aktualisieren möchten, aus, ob Sie Infrastrukturbenachrichtigungen erhalten möchten. 

  Standardmäßig sind alle {{site.data.keyword.Bluemix_notm}}-Infrastrukturbenachrichtigungen inaktiviert.
  {: tip}

4. Klicken Sie auf **Speichern**. 

## Benutzerbenachrichtigungen einrichten
{: #setting-user-notifications}

Das Festlegen von Benutzerbenachrichtigungen ist nur für Ressourcen der klassischen Infrastruktur verfügbar. Als Kontoeigner können Sie Benachrichtigungsabonnements für Benutzer in Ihrem Konto festlegen. Die Abonnements gelten für eine bestimmte Gruppe von Entwicklerservices wie z. B. {{site.data.keyword.autoscaling}} und Raid Alert Monitoring. Wenn der Benutzer einen Service abonniert, erhält er E-Mails zu diesem Service.   

Benutzer in Ihrem Konto erhalten Benachrichtigungen für die folgenden Typen wichtiger operativer Ereignisse: 

  * Ungeplante Infrastrukturprobleme oder -ausfälle: Probleme, die zu einem Ausfall auf der Basis bestimmter Bedingungen für bestimmte Kunden führen könnten. 
  * Geplanter Service oder geplanter Wartungsservice: Dies sind Wartungsaktivitäten, die zur Aufrechterhaltung eines optimalen Status für den Infrastrukturbetrieb erforderlich sind. 
  * Sicherheitslücken: Der betroffene Bereich wird isoliert. Eine Programmkorrektur zum Schließen der Sicherheitslücke wird erstellt und getestet, um sicherzustellen, dass keine zugehörigen Funktionen betroffen sind.  
  * Geöffnete Supportfälle: Benutzer erhalten Alerts zu Fällen, die für ihr Konto geöffnet sind. 

Der Zeitpunkt der Benachrichtigung ist davon abhängig, ob es sich um ein ungeplantes, geplantes oder termingesteuertes Ereignis handelt. Die {{site.data.keyword.BluSoftlayer_notm}}-Infrastrukturrichtlinie gibt vor, dass Probleme so schnell wie möglich behoben werden müssen, um das Risiko weiterer Probleme mit einer größeren Auswirkung zu verhindern oder zu begrenzen. Selbst planmäßige Wartungen werden bisweilen mit einer nur kurzfristigen Vorabbenachrichtigung durchgeführt. 

Führen Sie die folgenden Schritte aus, um Abonnementbenachrichtigungen für die Benutzer einzurichten:  

  1. Rufen Sie **Verwalten > Konto** auf und wählen Sie **Benachrichtigungen** aus.  
  2. Wählen Sie einen Service in der Tabelle aus.  
  3. Wählen Sie in der Spalte 'Abonniert' **Ja** für den Benutzer aus, der Benachrichtigungen erhalten möchte.  

    Klicken Sie auf **Filtern** und filtern Sie anhand des Vornamens, des Nachnamens oder des Benutzernamens, um den gewünschten Benutzer ohne großen Aufwand zu finden.
    {: tip}

