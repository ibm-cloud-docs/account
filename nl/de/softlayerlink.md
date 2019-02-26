---

copyright:

  years: 2016, 2019

lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Zur IBMid wechseln und Konten verknüpfen
{: #unifyingaccounts}

Eine IBMid ist eine einzelne ID, die Sie für die Anmeldung an Ihrem {{site.data.keyword.Bluemix}}-Konto für den Zugriff auf und den Kauf von Infrastruktur-, Service- und Anwendungsfeatures verwenden. Alle neuen Konten erhalten automatisch eine IBMid und vorhandene SoftLayer-Konten, mit Ausnahme von föderierten SAML-Konten, werden für den Wechsel zur IBMid-Authentifizierung aktiviert.
{:shortdesc}

## Zur IBMid wechseln
{: #switchtoIBMid}

Sie können diesen Wechsel zur IBMid jederzeit abbrechen, solange der Prozess noch nicht abgeschlossen ist. Bei jeder Anmeldung wird jedoch die Aufforderung zum Wechsel zur IBMid angezeigt. Jedes SoftLayer-Konto, das mit einem {{site.data.keyword.Bluemix_notm}}-Konto verknüpft werden soll, muss zu einer eindeutigen IBMid mit einer eindeutigen E-Mail-Adresse gehören.

Für den Wechsel von Ihrem bisherigen SoftLayer-Konto zu einer IBMid müssen Sie eine IBMid erstellen und diese anschließend mithilfe Ihres Registrierungscodes bestätigen.

### IBMid und Registrierungscode anfordern
{: #reqIBMidandregcode}

1. Melden Sie sich bei Ihrem SoftLayer-Konto an und klicken Sie auf **OK**, wenn die Eingabeaufforderung zum Wechseln zu einer IBMid angezeigt wird.

   Wenn Sie ein Masterbenutzer sind und keine Eingabeaufforderung zum Wechseln zur IBMid im Kundenportal angezeigt wird, wenden Sie sich an den IBM Support, um Hilfe zu erhalten. Weitere Informationen zur Kontaktaufnahme mit IBM Support erhalten Sie unter [Unterstützung anfordern](/docs/get-support?topic=get-support-getting-customer-support).

   Falls Sie bereits angemeldet sind und bei der Eingabeaufforderung auf **Später** geklickt haben, jedoch in der aktuellen Sitzung zur IBMid-Authentifizierung wechseln möchten, rufen Sie die Seite für die Bearbeitung des Benutzerprofils auf und klicken Sie auf **Zu IBM ID wechseln**.

2. Befolgen Sie die Anweisungen im Assistenten, um Ihre IBMid zu erstellen.

   Geben Sie eine E-Mail-Adresse ein, die derzeit nicht von einer IBMid verwendet wird. Diese E-Mail-Adresse wird als Benutzername für die neue IBMid verwendet. An diese Adresse wird auch Ihr Registrierungscode gesendet, nachdem die IBMid erstellt wurde. Sie können die E-Mail-Adresse, die der IBMid zugeordnet ist, zu einem späteren Zeitpunkt aktualisieren, jedoch nicht den Benutzernamen ändern.

### IBMid mit dem Registrierungscode bestätigen
{: #confIBMiduseregcode}

1. Wenn Sie Ihren Registrierungscode erhalten, klicken Sie auf den Link in der E-Mail oder kopieren Sie die URL in einen Browser und geben Sie Ihren Registrierungscode ein. Der Registrierungscode ist sieben Tage lang gültig und kann nur einmal verwendet werden.

2. Nachdem Sie Ihren Registrierungscode übergeben haben, melden Sie sich mit Ihrer IBMid am Kundenportal an.

   Wechseln Sie bei der Eingabeaufforderung 'Kontoanmeldung' in den Abschnitt für die **Kontoanmeldung mit IBMid** und klicken Sie auf **Mit IBM ID anmelden**. Verwenden Sie nicht die Felder **Benutzername** und **Kennwort**, die Sie zuvor mit Ihrer SoftLayer-ID verwendet haben.

Wenn Sie ein neuer Kunde sind, werden Sie beim Überprüfen Ihrer Bestellung nach Ihrer vorhandenen IBMid gefragt oder zum Erstellen einer neuen IBMid aufgefordert.
  * Zur Verwendung einer bestehenden IBMid geben Sie den Benutzernamen oder die E-Mail-Adresse der IBMid ein, falls diese nicht von mehreren IBMids gemeinsam genutzt wird.
  * Geben Sie zum Erstellen einer neuen IBMid eine E-Mail-Adresse ein, die noch nicht von einer IBMid verwendet wird. Diese E-Mail-Adresse ist der Benutzername für die IBMid; an diese Adresse wird Ihr Registrierungscode gesendet, nachdem die IBMid erstellt wurde. Sie können die E-Mail-Adresse, die der IBMid zugeordnet ist, zu einem späteren Zeitpunkt aktualisieren, jedoch nicht den Benutzernamen ändern.

Informationen zur Lösung von Problemen, die bei der Anmeldung mit Ihrer IBMid auftreten könnten, finden Sie unter [Fehlerbehebung für den Zugriff auf {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-accessing).


## IBMid-Konten verknüpfen
{: #link_accounts}

Nachdem die Konten auf IBMid-Konten umgestellt wurden, können Sie SoftLayer- und {{site.data.keyword.Bluemix_notm}}-Konten verknüpfen, um die kombinierten IaaS- (Infrastructure as a Service) und PaaS-Ressourcen (Platform as a Service) zu nutzen. Anschließend können Sie mit einer einzigen Anmeldung auf IaaS-Ressourcen und PaaS-Ressourcen zugreifen. Dank dem Verknüpfen Ihrer Konten erhalten Sie eine gemeinsame Abrechnung für alle verwendeten PaaS- und IaaS-Ressourcen. Sie können Ihr eigenes Konto oder, wenn Sie ein Masterbenutzer sind, Ihre Benutzerkonten verknüpfen.

### Ihr IBMid-Konto verknüpfen
{: #link_user_account}

Wenn Sie Kunde der klassischen Infrastruktur sind und außerdem über PaaS-Konten in {{site.data.keyword.Bluemix_notm}} verfügen oder diese erstellen, können Sie IaaS und PaaS verknüpfen, um eine Gesamtansicht Ihrer Konten zu erhalten. Führen Sie die folgenden Schritte aus, um Ihre Konten zu verknüpfen:
1. Melden Sie sich an Ihrem SoftLayer-Konto an.
2. Klicken Sie auf der Seite 'Konto - Zusammenfassung' auf **Neu! Bluemix-Konto verknüpfen**.
3. Überprüfen Sie die Nutzungsbedingungen und bestätigen Sie, dass Sie ihnen zustimmen.
4. Führen Sie einen der folgenden abschließenden Schritte aus, je nachdem, wie Ihr Konto eingerichtet ist:
  * Wenn Ihre IBMid über ein zugeordnetes {{site.data.keyword.Bluemix_notm}}-Konto verfügt, werden Sie zu einer Berechtigungsseite weitergeleitet und anschließend zurück zum letzten Bestätigungsschritt.
  * Wenn Ihnen kein {{site.data.keyword.Bluemix_notm}}-Konto zugeordnet ist, werden Sie aufgefordert, ein neues zu erstellen.

Häufig gestellte Fragen und Antworten zum Verknüpfen Ihres Kontos finden Sie unter [FAQs](/docs/account?topic=account-al_login).

### IBMid-Benutzerkonten verknüpfen
{: #link_customer_accounts}

Nachdem Ihre Benutzerkonten zur Authentifizierung mit IBMid gewechselt haben, können Reseller und Distributoren ihre eigenen Benutzerkonten verknüpfen. Zum Verknüpfen von Kundenkonten müssen Sie ein SoftLayer-Masterbenutzer sein. Die IBMid, die der Masterbenutzer des Kontos ist, muss der Eigner des {{site.data.keyword.Bluemix_notm}}-Plattformkontos sein, zu dem die Verknüpfung hergestellt wird.

Das Verknüpfen der Konten kann nicht rückgängig gemacht werden.
{: note}

Lesen Sie unbedingt die folgenden wichtigen Hinweise zum Verknüpfen von Konten:

  * Der Masterbenutzer des SoftLayer-Kontos, das verknüpft wird, muss eine IBMid haben.
  * Jedes Benutzerkonto, das mit einem {{site.data.keyword.Bluemix_notm}}-Konto verknüpft wird, muss zu einer eindeutigen IBMid mit einer eindeutigen E-Mail-Adresse gehören. Auch wenn eine einzelne IBMid mehreren SoftLayer-Konten zugeordnet sein kann, müssen Sie die Masterbenutzer für jedes Konto in eine jeweils eindeutige IBMid ändern. Fordern Sie Unterstützung an, um den Masterbenutzer für ein SoftLayer-Konto zu ändern. Weitere Informationen finden Sie in [Unterstützung für {{site.data.keyword.Bluemix_notm}}-Infrastruktur anfordern](/docs/customer-portal?topic=customer-portal-customerportal_support).
  * Wenn Sie einem verknüpften Konto neue Benutzer hinzufügen, müssen Sie sie sowohl dem SoftLayer-Konto als auch dem {{site.data.keyword.Bluemix_notm}}-Konto hinzufügen, damit sie Zugriff auf alle Funktionen in der einheitlichen Konsole erhalten.
  * Wenn Sie über ein Markenkonto verfügen, das BAP (Brand Agent Portal) verwendet, und Unterstützung beim Verknüpfen Ihres Kontos benötigen, wenden Sie sich per E-Mail (softlayer_revenue_services_team@wwpdl.vnet.ibm.com) an das Revenue Services-Team.

Führen Sie die folgenden Schritte aus, um jedes SoftLayer-Konto mit einem vorhandenen {{site.data.keyword.Bluemix_notm}}-Plattformkonto zu verknüpfen oder ein neues Konto zu erstellen:

   1. Melden Sie sich beim Kundenportal mit Ihrer Masterbenutzerkonto-ID an.
   2. Klicken Sie im Kundenportal auf **Bluemix-Konto verknüpfen**.
   3. Lesen und akzeptieren Sie die Bedingungen für das Verknüpfen von SoftLayer- und {{site.data.keyword.Bluemix_notm}}-Konten.
   4. Befolgen Sie die Eingabeaufforderungen im Assistenten und fügen Sie die Benutzer im SoftLayer-Konto dem {{site.data.keyword.Bluemix_notm}}-Konto hinzu.
   5. Führen Sie bei entsprechender Aufforderung eine der folgenden Aktionen aus:
     * Wenn Sie bereits über ein {{site.data.keyword.Bluemix_notm}}-Konto verfügen, geben Sie die E-Mail-Adresse des Kontos an, um die Konten zu verknüpfen.
     * Wenn Sie nicht über ein {{site.data.keyword.Bluemix_notm}}-Konto verfügen, geben Sie die von Ihnen gewünschte E-Mail-Adresse an, befolgen Sie die Anweisungen für die Einladung zu {{site.data.keyword.Bluemix_notm}} und erstellen Sie ein Konto.
   6. Nachdem Sie das Konto verknüpft haben, informieren Sie die Endbenutzer der einzelnen Konten darüber, dass sie zur IBMid migrieren müssen. Dabei sollte das im vorherigen Abschnitt [Zur IBMid wechseln](#switchtoIBMid) beschriebene Verfahren befolgt werden.

      Migrieren Sie nur Endbenutzerkonten auf IBMid. Migrieren Sie keine Markenkonten. Hierbei handelt es sich um übergeordnete Konten für Endbenutzerkonten, die keine Ressourcen enthalten. Benutzer von Markenkonten, die zur IBMid migrieren, können sich anschließend nicht mehr beim BAP (Brand Agent Portal) anmelden.
      {: important}

Beachten Sie die folgenden Änderungen nach der Verknüpfung Ihrer Konten:

  * Sie melden sich nun bei der [{{site.data.keyword.Bluemix}}-Konsole ![Symbol für externen Link](../icons/launch-glyph.svg)](https://cloud.ibm.com){: new_window} an.
  * Für den Zugriff sowohl auf das SoftLayer- als auch auf das {{site.data.keyword.Bluemix_notm}}-Konto müssen Sie Ihre IBMid-Berechtigungsnachweise verwenden.
  * Alle bestehenden SoftLayer-Rabatte werden auf alle {{site.data.keyword.Bluemix_notm}}-Gebühren angewandt.
  * Sie erhalten nur eine Rechnung; diese ist in USD ausgestellt. Wenn Sie über ein bestehendes {{site.data.keyword.Bluemix_notm}}-Konto verfügen, erfolgt die Rechnungsstellung für Infrastrukturressourcen über {{site.data.keyword.Bluemix_notm}} ab dem neuen Abrechnungszyklus, der nach dem Verknüpfen der Konten beginnt. Weitere Informationen finden Sie unter [Konsolidierte Rechnungsstellung für verknüpfte Konten](/docs/customer-portal?topic=customer-portal-unifybillaccounts).
  * Sie können die Nutzung Ihrer Ressourcen der klassischen Infrastruktur in der {{site.data.keyword.Bluemix_notm}}-Konsole überwachen.

## Nutzung von Mehrfaktorauthentifizierung in verknüpften Konten
{: #2fa}

Wenn Sie über ein verknüpftes Konto verfügen, können Sie auf der Seite **Einstellungen** von {{site.data.keyword.Bluemix_notm}} IAM die Mehrfaktorauthentifizierung (MFA) für Ihr Konto aktivieren. Diese Authentifizierung wird auch als 'Zwei-Faktor-Authentifizierung' bezeichnet und stellt eine Sicherheitsstufe für den Zugriff auf Ihr Konto bereit, die über das Standardverfahren mit erforderlicher IBMid und zugehörigem Kennwort hinausgeht. Die Mehrfaktorauthentifizierung für Ihr Konto wird auf alle Ressourcen in Ihrem verknüpften {{site.data.keyword.Bluemix_notm}}-Konto angewendet. Wenn sie für Ihr Konto aktiviert ist, gilt sich auch für alle Benutzer, die zu Ihrem Konto hinzugefügt wurden.

Andere Mehrfaktorauthentifizierungsmethoden erfolgen nicht pro IBMid. Sie erfolgen pro Konto. Wenn eine IBMid mehreren Konten zugeordnet ist und Sie zwischen den Konten wechseln, müssen Sie Ihre Identität bei jedem Wechsel zu einem anderen Konto, für das eine Zwei-Faktor-Authentifizierung erforderlich ist, bestätigen. Dies gilt auch, wenn das vorherige Konto und das neue Konto beide mit demselben Mechanismus für die Zwei-Faktor-Authentifizierung konfiguriert sind.

Wenn Sie zuvor die [Zwei-Faktor-Authentifizierung (2FA) im Kundenportal](/docs/customer-portal?topic=customer-portal-customerportal_2fa) für Ihre Ressourcen der klassischen Infrastruktur aktiviert haben und dann die MFA-Einstellung für das {{site.data.keyword.Bluemix_notm}}-Konto aktivieren, überschreibt letztere die 2FA im Kundenportal. Dies bedeutet, dass Sie die 2FA, die Sie im Kundenportal erworben haben, zugunsten der MFA-Einstellung inaktivieren können.
