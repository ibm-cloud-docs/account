---



copyright:

  years: 2016, 2018
lastupdated: "2018-01-11"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Zur IBMid wechseln
Für die Authentifizierung in SoftLayer wird jetzt eine IBMid verwendet, die eine einzige Anmeldung bei allen {{site.data.keyword.Bluemix}}-Komponenten ermöglicht. Für vorhandene SoftLayer-Konten wird ein Wechsel zur IBMid-Authentifizierung ermöglicht. Ein Migrationsassistent führt Sie durch diese Umstellung.
{:shortdesc}

Sie können diesen Wechsel zur IBMid jederzeit abbrechen, solange der Prozess noch nicht abgeschlossen ist. Bei jeder Anmeldung wird jedoch die Aufforderung zum Wechsel zur IBMid angezeigt. Jedes SoftLayer-Konto, das mit einem {{site.data.keyword.Bluemix_notm}}-Konto verknüpft werden soll, muss zu einer eindeutigen IBMid mit einer eindeutigen E-Mail-Adresse gehören.

Führen Sie folgende Schritte aus, um von Ihrem bisherigen SoftLayer-Konto zu einer IBMid zu wechseln:
1. Melden Sie sich bei Ihrem SoftLayer-Konto an und klicken Sie auf **OK**, wenn die Eingabeaufforderung zum Wechseln zu einem IBMid angezeigt wird.

   Wenn Sie ein Masterbenutzer sind und keine Eingabeaufforderung zum Wechseln zur IBMid im {{site.data.keyword.slportal}} angezeigt wird, dann wenden Sie sich an den [IBM Support](/docs/get-support/howtogetsupport.html#getting-customer-support), um Hilfe zu erhalten.

   Falls Sie bereits angemeldet sind und bei der Eingabeaufforderung auf **Später** geklickt haben, jedoch in der aktuellen Sitzung zur IBMid-Authentifizierung wechseln möchten, rufen Sie die Seite für die Bearbeitung des Benutzerprofils auf und klicken Sie auf **Zu IBM ID wechseln**.

2. Befolgen Sie die Anweisungen im Assistenten, um Ihre IBMid zu erstellen.

   Geben Sie eine E-Mail-Adresse ein, die aktuell nicht von einer IBMid verwendet wird. Diese E-Mail-Adresse wird als Benutzername für die neue IBMid verwendet; an diese Adresse wird Ihr Registrierungscode gesendet, nachdem die IBMid erstellt wurde. Sie können die E-Mail-Adresse, die der IBMid zugeordnet ist, zu einem späteren Zeitpunkt aktualisieren, jedoch nicht den Benutzernamen ändern.

3. Wenn Sie Ihren Registrierungscode erhalten, klicken Sie auf den Link in der E-Mail oder kopieren Sie die URL in einen Browser und geben Sie Ihren Registrierungscode ein.

   Der Registrierungscode ist sieben Tage lang gültig und kann nur einmal verwendet werden.

4. Nachdem Sie Ihren Registrierungscode übergeben haben, melden Sie sich mit Ihrer IBMid am Kundenportal an.

   Wechseln Sie bei der Eingabeaufforderung 'Kontoanmeldung' in den Abschnitt für die **Kontoanmeldung mit IBMid** und klicken Sie auf **Mit IBM ID anmelden**. Verwenden Sie nicht die Felder **Benutzername** und **Kennwort**, die Sie zuvor mit Ihrer SoftLayer-ID verwendet haben.

Wenn Sie ein neuer Kunde sind, werden Sie beim Überprüfen Ihrer Bestellung nach Ihrer vorhandenen IBMid gefragt oder zum Erstellen einer neuen IBMid aufgefordert.
  * Zur Verwendung einer bestehenden IBMid geben Sie den Benutzernamen oder die E-Mail-Adresse der IBMid ein, falls diese eindeutig ist (also nicht von mehreren IBMids gemeinsam genutzt wird).

  * Geben Sie zum Erstellen einer neuen IBMid eine E-Mail-Adresse ein, die noch nicht von einer IBMid verwendet wird. Diese E-Mail-Adresse ist der Benutzername für die IBMid; an diese Adresse wird Ihr Registrierungscode gesendet, nachdem die IBMid erstellt wurde. Sie können die E-Mail-Adresse, die der IBMid zugeordnet ist, zu einem späteren Zeitpunkt aktualisieren, jedoch nicht den Benutzernamen ändern.

Informationen zur Lösung von Problemen, die bei der Anmeldung mit Ihrer IBMid auftreten könnten, finden Sie unter [Fehlerbehebung für den Zugriff auf {{site.data.keyword.Bluemix_notm}}](/docs/get-support/ts_accessing.html#accessing).

## Benutzerkonten für die IBMid-Authentifizierung aktivieren
{: #link_accounts_resellers}

In einigen Fällen muss ein Reseller oder Distributor aktivieren, dass die IBMid-Authentifizierung für ein Konto verwendet werden kann, bevor ein Benutzer zu einer IBMid wechseln kann.

  * Die Authentifizierung mit der IBMid ist für jedes vorhandene Benutzerkonto erforderlich, das mit einem {{site.data.keyword.Bluemix_notm}}-Konto verknüpft werden soll. Anschließend muss jeder Benutzer den Prozess abschließen, um mithilfe des Migrationsassistenten zu einer IBMid zu wechseln, wie im vorherigen Abschnitt beschrieben. Wenden Sie sich an den [IBM Support](/docs/get-support/howtogetsupport.html#getting-customer-support), um ein vorhandenes SoftLayer-Konto für die Verwendung der IBMid-Authentifizierung zu aktivieren.

  * Um sicherzustellen, dass neue Benutzerkonten mit einer IBMid erstellt werden, muss das Attribut `CREATE_NEW_ACCOUNT_WITH_IBMid_AUTHENTICATION` auf das direkte Masterbenutzerkonto festgelegt werden. Wenden Sie sich an den [ IBM Support ](/docs/get-support/howtogetsupport.html#getting-customer-support) oder Ihren Anbieter, um das Attribut für Ihre Konten festzulegen.  

## IBMid-Benutzerkonten verknüpfen
{: #link_user_accounts}

Nachdem die Benutzerkonten zur IBMid-Authentifizierung gewechselt haben, können Reseller und Distributoren SoftLayer- und {{site.data.keyword.Bluemix_notm}}-Konten verknüpfen, um die kombinierten Infrastruktur- und Plattformressourcen zu nutzen. Lesen Sie unbedingt die folgenden wichtigen Hinweise:

  * Der Masterbenutzer des Kontos, das verknüpft wird, muss eine IBMid haben.
  * Jedes Benutzerkonto, das mit einem {{site.data.keyword.Bluemix_notm}}-Konto verknüpft wird, muss zu einer eindeutigen IBMid mit einer eindeutigen E-Mail-Adresse gehören. Auch wenn eine einzelne IBMid mehreren SoftLayer-Konten zugeordnet sein kann, müssen Sie die Masterbenutzer für jedes Konto in eine jeweils eindeutige IBMid ändern. Wenden Sie sich an den [IBM SoftLayer-Support ![Symbol für externen Link](../icons/launch-glyph.svg)](https://knowledgelayer.softlayer.com/topic/support){: new_window}, um den Masterbenutzer für ein SoftLayer-Konto zu ändern.
  * Wenn Sie einem verknüpften Konto neue Benutzer hinzufügen, müssen Sie sie sowohl dem SoftLayer-Konto als auch dem {{site.data.keyword.Bluemix_notm}}-Konto hinzufügen, damit sie Zugriff auf alle Funktionen in der einheitlichen Konsole erhalten.

Führen Sie die folgenden Schritte aus, um jedes Konto mit einem {{site.data.keyword.Bluemix_notm}}-Konto zu verknüpfen:
1. Um eine Verknüpfung mit einem vorhandenen {{site.data.keyword.Bluemix_notm}}-Konto zu erstellen oder um ein neues zu erstellen, melden Sie sich als Masterbenutzer beim Kundenportal an und klicken auf den {{site.data.keyword.Bluemix_notm}}-Link.

   Die IBMid, die der Masterbenutzer des Kontos ist, muss der Eigner des {{site.data.keyword.Bluemix_notm}}-Kontos sein, zu dem die Verknüpfung hergestellt wird.

2. Befolgen Sie die Eingabeaufforderungen im Assistenten und fügen Sie die Benutzer im SoftLayer-Konto dem {{site.data.keyword.Bluemix_notm}}-Konto hinzu.
3. Nachdem Sie das Konto verknüpft haben, informieren Sie die Endbenutzer der einzelnen Konten darüber, dass sie zur IBMid migrieren müssen. Dabei sollte das im vorherigen Abschnitt beschriebene Verfahren verwendet werden.

Migrieren Sie nur Endbenutzerkonten auf die IBMid. Migrieren Sie keine Brandkonten. Dies sind übergeordnete Konten für Endbenutzerkonten und enthalten keine Ressourcen. Brandkontenbenutzer, die zur IBMid migrieren, können sich anschließend nicht mehr beim BAP (Brand Agent Portal) anmelden.
{: tip}  

## Nutzung von Mehrfaktorauthentifizierung in verknüpften Konten
{: #2fa}

Wenn Sie über ein verknüpftes Konto verfügen, können Sie auf der Seite **Einstellungen** von Identity and Access die Mehrfaktorauthentifizierung für Ihr Konto aktivieren (/docs/iam/mfa.html). Diese Authentifizierung wird auch als 'Zwei-Faktor-Authentifizierung' bezeichnet und stellt eine Sicherheitsstufe für den Zugriff auf Ihr Konto bereit, die über das Standardverfahren mit erforderlicher IBMid und zugehörigem Kennwort hinausgeht. Die Mehrfaktorauthentifizierung für Ihr Konto wird auf alle Ressourcen in Ihrem verknüpften {{site.data.keyword.Bluemix_notm}}-Konto angewendet. Wenn sie für Ihr Konto aktiviert ist, gilt sich auch für alle Benutzer, die zu Ihrem Konto hinzugefügt wurden. Im Abschnitt [Mehrfaktorauthentifizierung aktivieren](/docs/iam/mfa.html) können Sie sich darüber informieren, wann diese Art der Authentifizierung für Sie sinnvoll sein kann.

Die Mehrfaktorauthentifizierung erfolgt nicht pro IBMid. Sie erfolgt weiterhin pro Konto. Wenn eine IBMid mehreren Konten zugeordnet ist und Sie zwischen den Konten wechseln, müssen Sie Ihre Identität bei jedem Wechsel zu einem anderen Konto bestätigen, für das eine Zwei-Faktor-Authentifizierung erforderlich ist. Dies gilt auch, wenn das vorherige Konto und das neue Konto beide mit demselben Mechanismus für die Zwei-Faktor-Authentifizierung konfiguriert sind.

<!-- Above section is for MFA release 1/2018. Commented out section here has old content.
If you enabled two-factor authentication for your existing SoftLayer account, you are still required to enter your security code when logging in to the {{site.data.keyword.Bluemix_notm}} console. However, the two-factor authentication applies only to the resources in your Infrastructure account. You might be able to do various actions to the resources in your {{site.data.keyword.Bluemix_notm}} account without doing two-factor authentication.
Two-factor authentication is not per IBMid. It is still per account. When an IBMid is associated with multiple accounts, and you switch between accounts, you must confirm your identity every time you switch to a different account that requires two-factor authentication. This is true even if the prior account and the new account are both configured with the same two-factor authentication mechanism.
-->

