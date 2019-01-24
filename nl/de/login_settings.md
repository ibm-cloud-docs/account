---


copyright:

  years: 2018
lastupdated: "2018-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}


# Anmeldesicherheit einrichten
{: #login-settings}

Mit der entsprechenden Zugriffsberechtigung können Sie zusätzliche Sicherheit für die Anmeldung einrichten. Sie können Sicherheitsfragen und -antworten festlegen, ein Ablaufdatum für Kennwörter auswählen, die Mehrfaktorauthentifizierung (MFA) mit zeitbasiertem einmaligem Kenncode (Time-based One-time Passcode, TOTP) einrichten und Optionen für die externe Authentifizierung festlegen.   
{:shortdesc}

Ein Kontoeigner kann festlegen, dass die Mehrfaktorauthentifizierung (MFA) mit einer IBMid für ein Konto erforderlich ist, dessen Mitglied Sie sind. Die Mehrfaktorauthentifizierung (MFA) mit einer IBMid setzt alle anderen MFA-Einstellungen des Benutzers außer Kraft. Beispiel: Wenn die Mehrfaktorauthentifizierung mit einer IBMid festgelegt ist, werden Sie zur Eingabe einer TOTP-MFA aufgefordert, die Ihrer IBMid zugeordnet ist, nicht zur Beantwortung von Sicherheitsfragen oder zur Verwendung einer externen Authentifizierungsmethode.
{: note}

Die folgenden Sicherheitsoptionen können Sie nur dann anzeigen und aktivieren bzw. inaktivieren, wenn der Administrator Ihnen die entsprechenden Zugriffsberechtigungen erteilt. Rufen Sie das Symbol **{{site.data.keyword.avatar}}** ![Avatarsymbol](../icons/i-avatar-icon.svg) > **Profil und Einstellungen** auf und wählen Sie **Anmeldeeinstellungen** aus. 

## Sicherheitsfragen einrichten
{: #security-questions}

Gehen Sie wie folgt vor, um die Sicherheitsfragen einzurichten: 
1. Rufen Sie in der Konsole das Symbol **{{site.data.keyword.avatar}}** ![Avatarsymbol](../icons/i-avatar-icon.svg) > **Profil und Einstellungen** auf und wählen Sie **Anmeldeeinstellungen** aus. 
2. Klicken Sie auf **Bearbeiten**.  
3. Wählen Sie die gewünschten Fragen aus und geben Sie die Antwort ein. Sie müssen drei Sicherheitsfragenoptionen verwenden. 
4. Klicken Sie auf **Speichern**, sobald dieser Schritt abgeschlossen ist.   
5. Stellen Sie sicher, dass das Kontrollkästchen `Ja` für die Sicherheitsfragen aktiviert ist, die aktiviert werden sollen. Wenn Sie das Kontrollkästchen `Ja` aktivieren, werden Sie möglicherweise dazu aufgefordert, sich erneut an Ihrem Konto anzumelden.   

Sie können Antworten auf drei Sicherheitsfragen für die zusätzliche Authentifizierung bei der Anmeldung einrichten. Sie müssen die Sicherheitsfragen und -antworten einrichten, bevor der Administrator diese MFA-Anforderung für Sie aktivieren kann. 

Zum Aktivieren bzw. Inaktivieren von Sicherheitsfragen müssen Sie der Kontoeigner sein oder der Kontoadministrator muss die Einstellung für die benutzerverwaltete Anmeldung für Sie aktivieren.
{: note}

## Ablaufdatum für ein Kennwort festlegen
{: #password-expiration}

Wenn Sie den Zeitraum festlegen möchten, während dessen Sie das aktuelle Kennwort verwenden möchten, wählen Sie eine Option für das Ablaufen des Kennworts im Abschnitt **Ablaufen der Kennwortgültigkeit** aus. 

Standardmäßig lautet die Einstellung für das Ablaufen des Kennworts 'nie'. Wenn Sie eine Registrierung für ein Konto durchführen, müssen Sie Ihr Kennwort nie ändern. Wenn Sie einen Zeitraum für das Ablaufen des Kennworts festlegen, werden Sie per E-Mail über das Ablaufen Ihres Kennworts benachrichtigt, und zwar 14 Tage vor Ablauf, 7 Tage vor Ablauf und am festgelegten Tag des Kennwortablaufs. 

Diese Option ist nur für Benutzer verfügbar, die sich mit einer SoftLayer-ID anmelden. Wenn Sie die Einstellung für das Ablaufen des Kennworts aktualisieren möchten, müssen Sie der Kontoeigner sein oder der Kontoadministrator muss die Einstellung für die benutzerverwaltete Anmeldung auf der IAM-Benutzerdetailseite für Sie aktivieren.
{: note}

## TOTP-Authentifizierung einrichten
{: #MFA}

Klicken Sie zum Einrichten der TOTP-Authentifizierung auf **Einrichten**.  

Durch TOTP-MFA wird eine zusätzliche Sicherheitsebene zu Ihrem Konto hinzugefügt, da bei der Anmeldung zusätzlich zur standardmäßig abgefragten ID mit zugehörigem Kennwort ein TOTP-Kenncode erforderlich ist. Sie müssen die TOTP-Authentifizierung einrichten, bevor der Kontoadministrator diese MFA-Anforderung für Sie aktivieren kann. 

Sie werden möglicherweise auch aufgefordert, einen zeitbasierten einmaligen Kenncode einzugeben, wenn die TOTP-Einstellung für den Benutzer nicht eingerichtet und aktiviert ist. Der Grund hierfür ist, dass ein Kontoeigner möglicherweise die Mehrfaktorauthentifizierung mit einer IBMid für ein Konto aktiviert hat, auf das Sie zugreifen können. Diese Art der Mehrfaktorauthentifizierung gilt für jeden Benutzer im Konto, wenn diese Einstellung aktiviert ist, und die Verwendung ist obligatorisch. Weitere Informationen finden Sie in [Arten der Mehrfaktorauthentifizierung](/docs/iam/mfatypes.html#types). 


## Optionen für die externe Authentifizierung einrichten
{: #third-party-MFA}

Sie oder der zuständige Kontoadministrator können die Symantec-Authentifizierung oder die telefongestützte Authentifizierung für eine monatliche Gebühr bestellen. Damit Sie die externe Authentifizierung bestellen können, müssen Sie über die Infrastrukturberechtigungen zum Hinzufügen von Services verfügen. Wenn Sie feststellen möchten, ob eine externe Authentifizierung aktiviert ist, rufen Sie das Symbol **{{site.data.keyword.avatar}}** ![Avatarsymbol](../icons/i-avatar-icon.svg) > **Profil und Einstellungen** auf und wählen Sie **Anmeldeeinstellungen** aus. Ist die telefongestützte MFA inaktiviert, klicken Sie auf **Zu 'Benutzerdetails'**. Mit diesem Link wird dieselbe Seite aufgerufen wie mit den Schritten für das Einrichten der Symantec-Authentifizierung und der telefongestützten Authentifizierung.   

### Symantec-Authentifizierung einrichten

Wenn der Kontoadministrator Symantec Identity Protection bestellt, benötigt er von Ihnen Ihre Berechtigungsnachweis-ID, damit er die Bestellung vervollständigen kann. 

1. Rufen Sie [Symantec VIP](https://vip.symantec.com/) auf. 
2. Klicken Sie auf **Download**.  
3. Rufen Sie Ihre Berechtigungsnachweis-ID ab und leiten Sie sie an den Administrator weiter, damit die Bestellung abgeschlossen werden kann.  

Nachdem der Administrator die Option bestellt und aktiviert hat, können Sie die App für die Anmeldeauthentifizierung verwenden. 

### Telefongestützte Authentifizierung einrichten

Wenn der Kontoadministrator telefongestützten Identitätsschutz bestellt, müssen Sie diesen Schutz anschließend einrichten. Danach kann der Administrator die Option aktivieren, damit Sie den Schutz verwenden können. 
Nachdem der Administrator die telefongestützte Authentifizierung bestellt hat, führen Sie die folgenden Schritte aus, um den Schutz einzurichten: 

1. Rufen Sie **Verwalten** > **Zugriff (IAM)** auf. 
2. Klicken Sie auf **Benutzer** und wählen Sie Ihren Namen in der Liste aus. 
3. Klicken Sie auf der Seite **Benutzerdetails** im Abschnitt **Anmeldung des Benutzers verwalten** auf das Symbol **Bearbeiten** ![Bearbeitungssymbol](../icons/icon_write.svg) für die Zeile **Telefongestützte Authentifizierung**. 
4. Gehen Sie den Eingabeaufforderungen entsprechend vor, um die telefongestützte Authentifizierung einzurichten. 

Nachdem Sie die telefongestützte Authentifizierung eingerichtet haben, kann der Kontoadministrator die Option aktivieren, damit Sie bei der Anmeldung zu den entsprechenden Schritten für diese Art der Mehrfaktorauthentifizierung aufgefordert werden. 


 

