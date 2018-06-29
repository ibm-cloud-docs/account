---

copyright:

  years: 2015, 2018

lastupdated: "2018-05-02"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Fehlerbehebung für den Zugriff auf {{site.data.keyword.Bluemix_notm}}
{: #accessing}

Allgemeine Probleme beim Zugriff auf {{site.data.keyword.Bluemix}} können sein, dass es Schwierigkeiten bei der Anmeldung bei {{site.data.keyword.Bluemix_notm}} gibt oder sich ein Konto dauerhaft im Wartestatus befindet. In vielen Fällen können Sie diese Probleme durch Ausführen weniger einfacher Schritte beheben.
{:shortdesc}

## Falsches Kennwort
{: #ts_logintobm}

Sie müssen über ein gültiges Kennwort verfügen, das Ihrer IBMid zugeordnet ist, um sich bei der {{site.data.keyword.Bluemix_notm}}-Konsole anzumelden.

Sie müssen über ein gültiges Kennwort verfügen, das Ihrer IBMid oder ID eines verknüpften Kontos zugeordnet ist, um sich über das [{{site.data.keyword.slportal}}](https://control.softlayer.com) anzumelden.

Wenn Sie versuchen, sich bei {{site.data.keyword.Bluemix_notm}} anzumelden, wird die folgende Fehlernachricht angezeigt:
{: tsSymptoms}

`Das eingegebene Kennwort ist nicht korrekt.`

Das Kennwort für die Anmeldung bei {{site.data.keyword.Bluemix_notm}} ist ungültig.
{: tsCauses}

Verwenden Sie eine der folgenden Lösungen:
{: tsResolve}
 * Geben Sie das richtige Kennwort ein. Um zu prüfen, ob Ihre IBMid und das Kennwort gültig sind, können Sie auf die Seite 'Mein IBM Profil' wechseln. Klicken Sie dort auf **Anmelden** und geben Sie Ihre IBMid und das Kennwort auf der Anmeldeseite ein.
 * Falls Sie Ihr Kennwort vergessen haben, klicken Sie auf **Kennwort vergessen**, um Ihr Kennwort zurückzusetzen. Rufen Sie anschließend erneut die [{{site.data.keyword.Bluemix_notm}}-Konsole](https://console.{DomainName}) oder das [{{site.data.keyword.slportal}}](https://control.softlayer.com) auf und melden Sie sich erneut an.
 * Wenn Sie Ihre IBMid vergessen haben oder weiterhin Probleme mit dem Kennwort vorliegen, suchen Sie auf der Site 'Worldwide IBM Registration Helpdesk' nach Hilfe.
 * Um eine gültige IBMid und ein gültiges Kennwort anzufordern, rufen Sie die Seite 'Mein IBM Profil' auf und klicken Sie dann auf **Registrieren**.

**Hinweis:** Falls Sie sich auf der Seite für die Anmeldung bei IBM befinden und der Anmeldeprozess aus irgendeinem Grund unterbrochen wird (beispielsweise beim Zurücksetzen Ihres Kennworts), rufen Sie erneut die [{{site.data.keyword.Bluemix_notm}}-Konsole](https://console.{DomainName}) oder das [{{site.data.keyword.slportal}}](https://control.softlayer.com) auf und beginnen Sie den Anmeldeprozess erneut.


## Ungültige Anmeldeberechtigungsnachweise
{: #ts_login_invalid_credentials}

Wenn Sie sich mit Ihrer IBMid anmelden, wird die folgende Nachricht angezeigt:
{: tsSymptoms}

`Es wurden falsche Anmeldeberechtigungsnachweise angegeben. Falls Ihrem Konto eine IBMid zugeordnet ist, melden Sie sich bitte hier an.`

* Sie haben zur Verwendung einer IBMid gewechselt, aber versucht, sich über das [{{site.data.keyword.slportal}}](https://control.softlayer.com) mit Ihrem vorherigen Benutzernamen und Kennwort anzumelden.
{: tsCauses}

* Sie haben versucht, sich über das [{{site.data.keyword.slportal}}](https://control.softlayer.com)anzumelden, aber Ihre IBMid und das zugehörige Kennwort in den Feldern für den Benutzernamen und das Kennwort eingegeben.

Klicken Sie in der Nachricht auf den Link **hier** oder wechseln Sie zum Abschnitt für die Kontoanmeldung mit IBMid und klicken Sie auf **Mit IBMid anmelden**.
{: tsResolve}

Verwenden Sie nicht die Felder **Benutzername** und **Kennwort**, die Sie für Ihre vorherige ID verwendet haben.


## Nicht erkannte IBMid oder E-Mail-Adresse
{: #ts_old_username}

Wenn Sie sich bei der {{site.data.keyword.Bluemix_notm}}-Konsole anmelden, wird die folgende Nachricht angezeigt:
{: tsSymptoms}

`Diese IBMid oder E-Mail wurde nicht erkannt.`

Sie haben versucht, sich bei der {{site.data.keyword.Bluemix_notm}}-Konsole anzumelden, jedoch keine gültige IBMid verwendet. Beispielsweise haben Sie keine vollständig qualifizierte E-Mail-Adresse für die IBMid eingegeben oder versucht, einen Benutzernamen mit dem zugehörigen Kennwort zu verwenden.
{: tsCauses}

Sie müssen über eine gültige IBMid und ein Kennwort verfügen, um sich bei {{site.data.keyword.Bluemix_notm}} anmelden zu können.

 * Stellen Sie sicher, dass Sie eine vollständig qualifizierte E-Mail-Adresse für die IBMid eingeben.
 {: tsResolve}
 * Falls Sie einen {{site.data.keyword.BluSoftlayer_full}}-Benutzer mit einer {{site.data.keyword.BluSoftlayer_full}}-ID verwenden, müssen Sie für jedes Konto, auf das Sie zugreifen können, im {{site.data.keyword.slportal}} zur IBMid-Authentifizierung wechseln, bevor Sie sich mit der IBMid-Authentifizierung anmelden können.
 Weitere Informationen finden Sie unter [Zur IBMid wechseln](/docs/account/softlayerlink.html).


## IBMid ist keinem IBM Cloud-Konto zugeordnet
{: #ts_login_noswitch}

Wenn Sie sich mit Ihrer IBMid anmelden, wird die folgende Nachricht angezeigt:
{: tsSymptoms}

`Sie sind auf diese Seite gelangt, weil Ihre Authentifizierung erfolgreich war; allerdings ist diese IBMid keinem IBM Cloud-Konto zugeordnet. Wenn Sie dies für einen Fehler halten, wenden Sie sich an Ihren Kontoeigner oder Masterbenutzer.`

Sie haben sich über das [{{site.data.keyword.slportal}}](https://control.softlayer.com) mit einer gültigen IBMid angemeldet, aber sie konnten nicht vom {{site.data.keyword.slportal}} zur IBMid-Authentifizierung wechseln.
{: tsCauses}

Führen Sie die folgenden Prüfungen durch:
{: tsResolve}
 * Lassen Sie von Ihrem Masterbenutzer oder Kontoadministrator überprüfen, ob Sie zur IBMid-Authentifizierung wechseln können.
 * Stellen Sie sicher, dass Sie den Schritt für den Wechsel zur IBMid ausgeführt haben. Weitere Informationen finden Sie unter [Zur IBMid wechseln](/docs/account/softlayerlink.html).
 * Stellen Sie sicher, dass Sie die Aktionen ausgeführt haben, die in der E-Mail für die **Zuordnung der Benutzer-ID zu einer IBMid** beschrieben sind. Überprüfen Sie Ihren Posteingang und Ihren Ordner für Junk-Mail. Um die E-Mail erneut abzurufen, weil sie beispielsweise abgelaufen ist, wechseln Sie im {{site.data.keyword.slportal}} auf die Seite für die Bearbeitung des Benutzerprofils und klicken Sie auf **E-Mail erneut senden**. Setzen Sie sich alternativ mit dem [{{site.data.keyword.Bluemix_notm}}-Support ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://ibm.biz/bluemixsupport.com){: new_window} in Verbindung.

**Hinweis:** Falls Sie Ihre IBMid direkt über IBMid erstellt haben, erhalten Sie zwei E-Mails, die Sie verarbeiten müssen. Eine E-Mail stammt von der IBMid-Registrierung, die andere von {{site.data.keyword.Blu_full}}. Stellen Sie sicher, dass Sie die Aktionen ausführen, die in beiden E-Mails aufgeführt sind.

Je nachdem, wie Ihr Konto eingerichtet wurde, können einige dieser Anmeldeoptionen auf Sie zutreffen:
 * {{site.data.keyword.BluSoftlayer_notm}}-Benutzer mit {{site.data.keyword.BluSoftlayer_full}}-IDs müssen sich über das [{{site.data.keyword.slportal}}](https://control.softlayer.com) anmelden.
 * {{site.data.keyword.BluSoftlayer_notm}}-Benutzer mit einer IBMid und mit oder ohne verknüpftes {{site.data.keyword.Bluemix_notm}}-Konto können sich über das [{{site.data.keyword.slportal}}](https://control.softlayer.com) anmelden, um das {{site.data.keyword.slportal}} zu öffnen, oder über die [{{site.data.keyword.Bluemix_notm}}-Konsole](https://console.{DomainName}), um das Infrastruktur-Dashboard zu öffnen.


## IBMid ist keinem {{site.data.keyword.Bluemix_notm}}-Konto zugeordnet
{: #ts_unabletologin}

Wenn Sie sich bei {{site.data.keyword.Bluemix_notm}} anmelden, wird die folgende Nachricht angezeigt:
{: tsSymptoms}

`Sie sind auf diese Seite gelangt, weil Ihre Authentifizierung erfolgreich war; allerdings ist diese IBMid keinem {{site.data.keyword.Bluemix_notm}}-Konto zugeordnet.`

Sie haben sich über die [{{site.data.keyword.Bluemix_notm}}-Konsole](https://console.{DomainName}) mit einer gültigen IBMid angemeldet, aber es wurde noch kein {{site.data.keyword.Bluemix_notm}}-Konto erstellt.
{: tsCauses}

Führen Sie den Anmeldeprozess durch, um ein {{site.data.keyword.Bluemix_notm}}-Konto zu erstellen.
{: tsResolve}

Je nachdem, wie Ihr Konto eingerichtet wurde, können einige dieser Anmeldeoptionen auf Sie zutreffen:
 * {{site.data.keyword.Bluemix_notm}}-Benutzer ohne verknüpftes SoftLayer-Konto müssen sich über die {{site.data.keyword.Bluemix_notm}}-Konsole anmelden.
 * {{site.data.keyword.Bluemix_notm}}-Benutzer mit verknüpftem SoftLayer-Konto können sich über die [{{site.data.keyword.Bluemix_notm}}-Konsole](https://console.{DomainName}) oder das [{{site.data.keyword.slportal}}](https://control.softlayer.com) anmelden.


## Konsole wird nicht geöffnet
{: #ts_login_stalls}

Wenn Sie sich mit Ihrer IBMid anmelden, wird eine Nachricht über die erfolgreiche Anmeldung ausgegeben, aber die [{{site.data.keyword.Bluemix_notm}}-Konsole](https://console.{DomainName}) oder das [{{site.data.keyword.slportal}}](https://control.softlayer.com) nicht erneut angezeigt.
{: tsSymptoms}

Verwenden Sie eine der folgenden Lösungen:
{: tsResolve}
 * Schließen Sie Ihren Browser, löschen Sie Cookies sowie den Inhalt des Cache und versuchen Sie erneut, sich anzumelden.
 * Stellen Sie sicher, dass Sie zur Anmeldung die [{{site.data.keyword.Bluemix_notm}}-Konsole](https://console.{DomainName}) oder das [{{site.data.keyword.slportal}}](https://control.softlayer.com) und nicht direkt den Service für die IBMid-Authentifizierung verwenden.


## Anmeldung mit IBMid wird nicht vollständig ausgeführt
{: #ts_login_ibmid}

Wenn Sie sich bei {{site.data.keyword.Bluemix_notm}} anmelden, wird die Authentifizierung mit der IBMid nicht vollständig abgeschlossen.
{: tsSymptoms}

Möglicherweise besteht ein Problem beim Service für die IBMid-Authentifizierung.
{: tsCauses}

Prüfen Sie, ob Sie sich bei der [IBM Homepage ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/us-en/){: new_window} anmelden können. Falls das klappt, handelt es sich hier um ein Anwendungsproblem, und Sie können es zu einem späteren Zeitpunkt erneut versuchen. Wenn Sie sich nicht bei dieser Seite anmelden können, wenden Sie sich an den [Help-Desk ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}.
{: tsResolve}


## Konto ist im Wartestatus
{: #ts_accntpding}

Falls sich Ihr Konto im Wartestatus befindet, können Sie sich nicht bei {{site.data.keyword.Bluemix_notm}} anmelden.

Wenn Sie sich für ein {{site.data.keyword.Bluemix_notm}}-Testkonto registriert haben, kann es vorkommen, dass Sie sich nicht an {{site.data.keyword.Bluemix_notm}} anmelden können. Die folgende Nachricht wird angezeigt:
{: tsSymptoms}

<code>Ihr Konto befindet sich im Zustand 'Anstehend'. Es kann bis zu 24 Stunden dauern, bis Sie eine Bestätigungs-E-Mail für Ihr Konto erhalten. Überprüfen Sie außerdem Ihren Spamordner. Wenn Sie trotzdem keine E-Mail-Bestätigung erhalten haben, wenden Sie sich an den <a href="http://ibm.biz/bluemixsupport.com" target="_blank">{{site.data.keyword.Bluemix_notm}}-Support</a>.</code>

Wenn Sie sich für ein {{site.data.keyword.Bluemix_notm}}-Testkonto registriert haben, erhalten Sie eine Bestätigungs-E-Mail. Sie müssen auf den Link in dieser Bestätigungs-E-Mail klicken, um den Registrierungsprozess abzuschließen.
{: tsCauses}

Die Bestätigungs-E-Mail wird an die E-Mail-Adresse gesendet, die Sie angegeben haben. Überprüfen Sie Ihren Posteingang und Ihren Spamordner. Falls Sie die Bestätigungs-E-Mail nicht erhalten haben, setzen Sie sich mit dem [{{site.data.keyword.Bluemix_notm}}-Support ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](http://ibm.biz/bluemixsupport.com){: new_window} in Verbindung.  
{: tsResolve}

## Laden einer {{site.data.keyword.Bluemix_notm}}-Seite nicht möglich
{: #ts_err}

Wenn Sie die {{site.data.keyword.Bluemix_notm}}-Konsole verwenden, kann es vorkommen, dass Sie eine Konsolenseite nicht laden können. Stattdessen können die Fehlernachrichten BXNUI0001E oder BXNUI0016E angezeigt werden.

Während der Verwendung der {{site.data.keyword.Bluemix_notm}}-Konsole kann eine der folgenden Fehlernachrichten angezeigt werden:
{: tsSymptoms}

`BXNUI0001E: Die Seite wurde nicht geladen, weil von {{site.data.keyword.Bluemix_notm}} nicht erkannt wurde, ob eine Sitzung vorhanden ist.`

`BXNUI0016E: Die Apps und Services wurden nicht abgerufen, da eine {{site.data.keyword.Bluemix_notm}}-Seite nicht geladen wurde.`

Führen Sie nach Bedarf eine oder mehrere der folgenden Aktionen aus:
{: tsResolve}

  * Aktualisieren Sie den Browser oder starten Sie ihn erneut.
  * Melden Sie sich bei {{site.data.keyword.Bluemix_notm}} ab und anschließend wieder an.
  * Verwenden Sie den persönlichen Browsing-Modus des Browsers.
  * Löschen Sie Cookies und den Inhalt des Browser-Cache.
  * Verwenden Sie einen anderen Browser. Informationen zu den Versionen der Browser, die von {{site.data.keyword.Bluemix_notm}} unterstützt werden, finden Sie in den [{{site.data.keyword.Bluemix_notm}}-Voraussetzungen](/docs/overview/prereqs.html#prereqs).
  * Wenn Sie die cf-Befehlszeilenschnittstelle installiert haben, geben Sie den Befehl `cf apps` ein, um anzuzeigen, ob die App aktiv ist.
