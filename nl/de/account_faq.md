---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-13"

keywords: account, upgrade, account settings, IBM Cloud account, Lite account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:tip: .tip}

# Häufig gestellte Fragen (FAQs)
{: #accountfaqs}

## Wie erstelle ich ein Konto?
{: #create-account}
{: faq}

Rufen Sie [{{site.data.keyword.Bluemix}}](https://cloud.ibm.com){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") auf und klicken Sie auf **{{site.data.keyword.Bluemix_notm}}-Konto erstellen**, um ein Lite-Konto zu erstellen, das nicht abläuft. Weitere Details zu den enthaltenen Features finden Sie in [Lite-Konto](/docs/account?topic=account-liteaccount#liteaccount).


## Wie kann ich Fehler beheben, die bei der Erstellung meines Kontos auftreten?
{: #account-error}
{: faq}

Wenn Sie sich bei einem {{site.data.keyword.Bluemix_notm}}-Konto anmelden können, rufen Sie das [Support Center](https://test.cloud.ibm.com/unifiedsupport/supportcenter) auf und wählen Sie eine der folgenden Optionen aus.

* Wenn Sie über Advanced Support oder Premium Support verfügen, klicken Sie auf **Live chat**, um mit einem {{site.data.keyword.Bluemix_notm}}-Ansprechpartner zu sprechen.
* Erstellen Sie einen Supportfall, indem Sie auf die Option **Fall erstellen** im Abschnitt _Sie benötigen weitere Hilfe?_ klicken.

   Nachdem Sie den Fall erstellt haben, wird Ihnen eine E-Mail-Benachrichtigung gesendet. Folgen Sie zur weiteren Kommunikation den entsprechenden Anweisungen.

Wenn Sie sich nicht bei einem {{site.data.keyword.Bluemix}}-Konto anmelden können, [Erstellen Sie eine Kontoanforderung](https://watson.service-now.com/x_ibmwc_open_case_app.do#!/create){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link").

## Was ist Cloud Foundry?
{: #cloud-foundry}
{: faq}

Cloud Foundry ist eine über {{site.data.keyword.Bluemix_notm}} Public verfügbare quelloffene PaaS-Option (PaaS - Platform as a Service), mit der Anwendungen in der Cloud erstellt und bereitgestellt werden können. Cloud Foundry-Organisationen und -Bereiche werden verwendet, um Ressourcen und Apps in bestimmten Regionen zu organisieren.

Weitere Informationen zum Verwalten von Organisationen und Bereichen finden Sie unter [Organisationen und Bereiche hinzufügen](/docs/account?topic=account-orgsspacesusers#orgsspacesusers). Wenn Sie Zugriff auf Ressourcen in einem Cloud Foundry-Bereich erteilen wollen, finden Sie weitere Informationen unter [Cloud Foundry-Zugriff](/docs/iam?topic=iam-cfaccess#cfaccess).


## Kann ich eine Organisation in ein anderes Konto versetzen?
{: #move-org-diff-account}
{: faq}

Es ist derzeit nicht möglich, eine Organisation in ein anderes Konto zu versetzen. Sie können die Organisation jedoch mit denselben Berechtigungsnachweisen in einem anderen Konto erneut erstellen und so diese Funktionalität nachahmen. Weitere Informationen finden Sie in [Organisationen und Bereiche hinzufügen](https://cloud.ibm.com/docs/account?topic=account-orgsspacesusers#createorg).


## Welche Cloud Foundry-Regionen kann ich verwenden?
{: #whichregions}
{: faq}

Bei einem Lite-Konto können Sie nur in einer Region arbeiten. In einem nutzungsabhängigen Konto oder Abonnementkonto können Sie auf alle verfügbaren Regionen zugreifen.


## Was ist ein Lite-Preisstrukturplan für Services?
{: #whatisliteplan}
{: faq}

Ein Lite-Plan ist ein Serviceplan mit kostenfreiem Kontingent. Sie können einen Lite-Planservice verwenden, um eine App ohne Gebühren zu erstellen. Ein Lite-Plan kann in monatlichen Zyklen, die jeden Monat erneuert werden, oder für eine einmalige Gebühr angeboten werden. Pro Lite-Planservice können Sie über eine Instanz verfügen. Lite-Preisstrukturpläne werden in allen Konten angeboten. Weitere Informationen zu Lite-Konten finden Sie in [Kontotypen](/docs/account?topic=account-accounts#accounts).


## Was passiert, wenn meine Lite-Planinstanz das monatliche Kontingent erreicht?
{: #monthlyquota}
{: faq}

Wenn ein Grenzwert für das Kontingent für die Lite-Planinstanzen erreicht wird, wird der Service für diesen Monat ausgesetzt. Grenzwerte für Kontingente gelten für die gesamte Organisation, nicht nur für die Instanz. Neue Instanzen, die in derselben Organisation erstellt werden, spiegeln die Nutzung bereits vorhandener Instanzen wider. Die Grenzwerte für Kontingente werden am ersten Tag jedes Monats zurückgesetzt.

Sie können die Nutzung überprüfen, indem Sie **Verwalten > Abrechnung und Nutzung** aufrufen und **Nutzung** auswählen. Weitere Informationen finden Sie unter [Nutzung anzeigen](/docs/billing-usage?topic=billing-usage-viewingusage).

## Wie kann ich einen Service aus meinem Konto löschen?
{: #accounts-service-removal}
{: faq}

Wenn Sie einen Service stoppen oder löschen möchten, können Sie dies über die Ressourcenliste tun. Weitere Informationen finden Sie in [Navigation in der {{site.data.keyword.Bluemix_notm}}-Konsole](/docs/overview?topic=overview-ui).

## Wie viele Ressourcengruppen, Organisationen oder Bereiche kann ich erstellen?
{: #resourcelimit}
{: faq}

Wenn Sie über ein gebührenpflichtiges Konto verfügen, gibt es keinen Grenzwert für die Anzahl von Ressourcengruppen, Organisationen oder Bereichen, die Sie in Ihrem Konto erstellen können. Bei einem Lite-Konto sind Sie jedoch auf eine Organisation und eine Ressourcengruppe beschränkt.

## Wie kann ich ein Upgrade meines Kontotyps durchführen oder den Kontotyp umwandeln?
{: #changeacct}
{: faq}

* Für ein Upgrade von einem Lite-Konto auf ein nutzungsabhängiges oder Abonnementkonto rufen Sie [Kontoeinstellungen](https://{DomainName}/account/settings) auf.
  * Für ein Upgrade auf ein nutzungsabhängiges Konto klicken Sie auf **Kreditkarte hinzufügen**.
  * Für ein Upgrade auf ein Abonnementkonto klicken Sie auf **Upgrade**.
* Zum Konvertieren zwischen einem nutzungsabhängigen und einem Abonnementkonto wenden Sie sich an den [{{site.data.keyword.Bluemix_notm}} Vertrieb ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}.

Den aktuellen Kontotyp finden Sie auf der Seite mit den Kontoeinstellungen.

Weitere Informationen finden Sie in [Upgrade für das Konto durchführen](/docs/account?topic=account-upgrading-account).

## Kann ich meine vorhandenen Instanzen weiterhin verwenden, wenn ich ein Upgrade für mein Lite-Konto durchführe?
{: #nochange}
{: faq}

Ja, Sie können ein Upgrade auf ein gebührenpflichtiges Konto durchführen und die Instanzen, die Sie mit Ihrem Lite-Konto erstellt haben, weiter verwenden.

## Wie aktualisiere ich meine Kreditkartendaten?
{: #updatepayment}
{: faq}

Sie können die Zahlungsmethode, die Ihrem Konto zugeordnet ist, aktualisieren, indem Sie in der Konsole [Zahlungen](https://cloud.ibm.com/billing/payments) aufrufen. Geben Sie unter 'Zahlungsmethode hinzufügen' die Rechnungsinformationen für Ihre neue Karte ein und klicken Sie auf **Kreditkarte hinzufügen**.

Wenn Sie zu einer anderen Zahlungsmethode wechseln möchten, wählen Sie die Option für eine **Andere Zahlungsmethode** aus und klicken Sie auf **Änderungsanforderung senden**. Ein Supportfall zum Ändern Ihrer Zahlungsmethode wird für Sie erstellt.

## Wie ändere ich meine Einstellungen für die E-Mail-Benachrichtigung?
{: #change-email-prefs}
{: faq}

In Ihren Profileinstellungen können Sie ändern, welche E-Mail-Benachrichtigungen Sie für geplante Ereignisse, ungeplante Ereignisse und Ankündigungen erhalten möchten.
1. Wechseln Sie in Ihren Profileinstellungen zu [Ankündigungen](https://cloud.ibm.com/user/notifications).
1. Wählen Sie für jeden Ereignistyp aus, ob Sie E-Mail-Benachrichtigungen erhalten möchten.

Bei klassischen Infrastrukturservices können Kontoeigner auch für Benutzer Abonnements für diese Services einrichten, indem **Verwalten > Konto > Benachrichtigungen** aufgerufen wird.

Weitere Informationen finden Sie in [E-Mail-Vorgaben festlegen](/docs/account?topic=account-email-prefs).

## Wie kann ich mein Kennwort zurücksetzen?
{: #reset-password}
{: faq}

Zum Zurücksetzen Ihres Kontokennworts rufen Sie das Avatarsymbol ![Avatarsymbol](../icons/i-avatar-icon.svg) und **> Profil und Einstellungen** auf. Klicken Sie dann auf **Ändern oder zurücksetzen** in der Kachel mit den Kontobenutzerinformationen.

Führen Sie die folgenden Schritte aus, um Ihr VPN-Kennwort zurückzusetzen:

  1. Rufen Sie **Verwalten > Zugriff (IAM)** auf und wählen Sie **Benutzer** aus.
  2. Wählen Sie den Benutzer aus.
  3. Klicken Sie im Abschnitt zu den VPN-Teilnetzen auf das Bearbeitungssymbol ![Symbol 'Bearbeiten'](../icons/icon_write.svg), um ein neues VPN-Kennwort einzugeben.
  5. Klicken Sie auf **Anwenden**.

## Wie kann ich mein Konto kündigen?
{: #cancelaccount}
{: faq}

Schade, dass Sie schon gehen! Wenn wir Ihnen mit Ihrem Konto behilflich sein können, wenden Sie sich an unseren Support.

Wenn Sie Ihr Konto beenden möchten, ist das weitere Vorgehen von Ihrem Kontotyp abhängig. Sie können Ihren Kontotyp überprüfen, indem Sie in den [Kontoeinstellungen](https://cloud.ibm.com/account/settings) die Einstellung _Kontotyp_ aufrufen.

* Für nutzungsabhängige Konten oder Abonnementkonten besteht die schnellste Möglichkeit, das Konto zu stornieren, darin, über den [Live-Chat](https://{DomainName}/unifiedsupport/supportcenter) Kontakt aufzunehmen oder die Telefonnummer 1-866-325-0045 anzurufen und Option 3 auszuwählen. Alternativ dazu können Sie auch einen Supportfall öffnen.
* Zum Stornieren eines Lite-Kontos rufen Sie [Kontoeinstellungen](https://cloud.ibm.com/account/settings) auf und klicken Sie auf **Konto inaktivieren**.

## Wie kann ich mein Konto löschen?
{: #deleteaccount}
{: faq}

Wenden Sie sich an [{{site.data.keyword.Bluemix_notm}} Support ![Symbol für externen Link](../icons/launch-glyph.svg)](https://{DomainName}/unifiedsupport/supportcenter){: new_window}, um einen Supportfall für das Löschen Ihres Kontos zu öffnen. Wenn Sie über Daten verfügen, die Ihrem alten Konto zugeordnet sind, die jedoch in ein neues Konto übernommen werden sollen, dann geben Sie die entsprechenden Informationen in Ihrer E-Mail an.

## Warum ist mein Konto inaktiviert?
{: #account-deactivated}
{: faq}

Ihr Konto kann aus den folgenden Gründen inaktiviert werden:

- Bei einem Testkonto kann es sein, dass der Testzeitraum beendet wurde. Zum Reaktivieren Ihres Kontos melden Sie sich bei Ihrem Konto an und führen Sie ein Upgrade auf ein nutzungsabhängiges Konto durch.
- Ein berechtigter Benutzer hat das Konto storniert.
- Das Konto wurde ausgesetzt. IBM kann Konten von Benutzern, die gegen die allgemeinen Nutzungsrichtlinien für die {{site.data.keyword.Bluemix_notm}}-Services verstoßen, ohne Vorankündigung inaktivieren. Bestimmte Services können wiederhergestellt werden, wenn die Benutzer ihr Nutzungsverhalten ändern, nachdem sie über ihren Verstoß informiert wurden.

Wenn Sie glauben, dass Ihr Konto aufgrund eines Fehlers inaktiviert wurde, wenden Sie sich an den Support unter 1-866-325-0045 und wählen Sie die dritte Option aus.

## Wie erhalte ich Unterstützung?
{: #contactsupport}
{: faq}

Klicken Sie auf **Support** in der Menüleiste der Konsole, um das Support Center aufzurufen. Weitere Informationen zum Support finden Sie in [Unterstützung anfordern](/docs/get-support?topic=get-support-support-plans).

## Kann ich eine Registrierung für eine kostenfreie Testversion durchführen?
{: #freetrial}
{: faq}

Für Fakultätsmitglieder und Studierende akkreditierter akademischer Einrichtungen sind {{site.data.keyword.Bluemix_notm}}-Testkonten erhältlich. Um sich für ein solches Testkonto zu qualifizieren, rufen Sie die Seite [Nutzen Sie das Potenzial von IBM ![Symbol für externen Link](../icons/launch-glyph.svg)](https://onthehub.com/ibm/){: new_window} auf und validieren Sie die Berechtigungsnachweise für Ihre Einrichtung.

## Wie melde ich mich an, nachdem ich mein Konto verknüpft habe?
{: #al_login}
{: faq}

Nach dem Verknüpfen Ihres Kontos melden Sie sich mit Ihrer IBMid bei der {{site.data.keyword.Bluemix}}-Konsole an.

## Wie wirkt sich das Verknüpfen meines Kontos auf meinen Support aus?
{: #al_support}
{: faq}

Nach dem Verknüpfen Ihres Kontos ändert sich an Ihrem Support-Level nichts, wenn Sie die {{site.data.keyword.Bluemix_notm}}-Plattform zu Ihrem Konto hinzufügen.

## Gibt es andere Möglichkeiten, Hilfe beim Verknüpfen meines Kontos zu erhalten?
{: #al_morehelp}
{: faq}

  1. Der Blog [Schritte zum Verknüpfen Ihrer IaaS- und PaaS-Konten](https://www.ibm.com/blogs/bluemix/2018/03/follow-steps-link-iaas-paas-accounts/){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") enthält nützliche Informationen.
  2. Öffnen Sie im {{site.data.keyword.BluSoftlayer_full}}-Kundenportal einen **Live-Chat mit dem Vertriebsteam**, Fragen zum Konto zu stellen.
  3. Öffnen Sie ein Ticket über das Kundenportal. Wählen Sie **Support** > **Ticket hinzufügen** aus und wählen Sie dann im Feld **Subjekt** die Option **Kontoanfrage** aus, um Ihre Frage zum Konto an das richtige Support-Team zu adressieren.

## Wie verknüpfe ich mein Konto, wenn ich mehrere Konten haben?
{: #al_multacct}
{: faq}

Wenn Sie über mehrere SoftLayer-Konten verfügen, müssen Sie die Konten verknüpfen, für die es ein übereinstimmendes {{site.data.keyword.Bluemix_notm}}-Plattformkonto und eine zugehörige IBMid gibt.

Wenn es kein übereinstimmendes {{site.data.keyword.Bluemix_notm}}-Plattformkonto und kein zugehöriges IBMid-Konto gibt, kann ein neues SoftLayer-Konto erstellt werden, um die Konten zu verknüpfen.

## Gibt es Kaufanreize für das Verknüpfen meiner Konten?
{: #al_incent}
{: faq}

Wenn Sie Ihre Konten verknüpfen, erhalten Sie im Rahmen einer Werbeaktion eine Gutschrift von $ 200 zum Ausprobieren der {{site.data.keyword.Bluemix_notm}}-Services.

Weitere Informationen zu der Werbeaktion mit einer Gutschrift von $ 200 finden Sie unter [Nutzungsabhängiges Konto](/docs/account?topic=account-accounts#paygo).

## Was bedeutet es, {{site.data.keyword.Bluemix_notm}}-Plattformservices zu meinem SoftLayer-Konto hinzuzufügen?
{: #al_owaffslacct}
{: faq}

Es bedeutet, dass Ihr Konto Zugriff auf alle {{site.data.keyword.Bluemix_notm}} Platform-Angebote hat. Nachdem Sie das {{site.data.keyword.Bluemix_notm}}-Platform-Angebot zu Ihrem Konto hinzugefügt haben, muss der Master des Kontos dem Benutzer Zugriff auf das Angebot erteilen.

Weitere Informationen für Master von Konten finden Sie in [Mit Benutzern arbeiten](/docs/iam?topic=iam-iamuserinv#iamuserinv).

## Wie wirkt sich das Verknüpfen von Konten auf meine SoftLayer-Masterkonto-ID aus?
{: #al_howaffslmastacct}
{: faq}

Sie können die ID weiterhin für Ihr SoftLayer-Konto verwenden, um sich beim Kundenportal anzumelden, da auf die {{site.data.keyword.Bluemix_notm}}-Konsole über IBMids zugegriffen werden kann.

## Wie kann ich Konten anzeigen, deren Eigner ich bin?
{: #accounts-owned}
{: faq}

Im Header der IBM Cloud-Konsole sind alle Konten aufgeführt, die Ihrer Anmelde-ID zugeordnet sind. Hierzu gehören auch die Konten, deren Eigner Sie sind. Sie können Ihre Rolle im jeweiligen Konto auf der Seite [Benutzer](https://{DomainName}/iam/users) anzeigen.

Sie können Ihre Konten auch auflisten, indem Sie den Befehl `ibmcloud account list` über die Befehlszeilenschnittstelle ausführen. 

## Wie kann ich zwischen mehreren Konten wechseln?
{: #switch-between-accounts}
{: faq}

Wenn Sie über mehrere Konten verfügen, können Sie auf einen der Kontonamen klicken, um ein anderes Konto auszuwählen, auf das Sie zugreifen können.  

![Screenshot zum Wechseln von Konten](images/account-faq.svg "Screenshot zum Wechseln von Konten")

## Kann ich eine andere Person als Kontoeigner angeben?
{: #switch-account-owners}
{: faq}

Sie können das Eigentumsrecht für einzelne Ressourcen innerhalb Ihres Kontos an eine andere Person übertragen, indem Sie den Befehl `ibmcloud catalog` verwenden. Weitere Informationen finden Sie in [Eigentumsrecht für eine private Ressource übertragen](/docs/account?topic=account-include#owners).

Zur Übertragung des Eigentumsrechts für Ihre gesamtes Konto benötigen Sie zusätzliche Unterstützung des Support-Teams. [Wenden Sie sich an den Support](/docs/get-support?topic=get-support-getting-customer-support), um Unterstützung anzufordern. 

## Unterstützt {{site.data.keyword.Bluemix_notm}} die Registrierung von Benutzern mithilfe einer Batchoperation?
{: #batch-registration}
{:faq}

Wenn Sie Benutzer für {{site.data.keyword.Bluemix_notm}} registrieren, müssen Sie für jeden Benutzer eine individuelle Registrierung vornehmen. {{site.data.keyword.Bluemix_notm}} unterstützt die Registrierung von Benutzern anhand einer Batchoperation nicht.

Rufen Sie [{{site.data.keyword.Bluemix}}](https://cloud.ibm.com){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") auf und klicken Sie auf **{{site.data.keyword.Bluemix_notm}}-Konto erstellen**. Füllen Sie dann das Kontoregistrierungsformular für jeden einzelnen Benutzer aus.

## Was sind Tags?
{: #know-about-tags}
{: faq}

Mithilfe von Tags können Sie Ressourcen in Ihrem Konto organisieren und anzeigen, indem Sie in der Ressourcenliste Tags zum Filtern verwenden. Weitere Informationen finden Sie in [Mit Tags arbeiten](/docs/resources?topic=resources-tag).

## Wer kann die Tags in einem Konto anzeigen?
{: #tags-visibility-account}
{: faq}

Tags sind im gesamten Konto sichtbar. Wenn Sie über die Berechtigung zum Anzeigen einer Ressource verfügen, können Sie alle zugeordneten Tags anzeigen. Weitere Informationen finden Sie in [Benutzern Zugriff zum Hinzufügen und Entfernen von Ressourcentags erteilen](/docs/resources?topic=resources-access#access).

## Welche Berechtigungen benötige ich zum Hinzufügen oder Entfernen von Tags?
{: #permissions-add-remove-tags}
{: faq}

Sie benötigen für eine Ressource mindestens die Rolle eines Bearbeiters für IAM-fähige Ressourcen oder die Entwicklerrolle in einem Cloud Foundry-Bereich, um Tags zu dieser Ressource hinzuzufügen oder von dieser zu entfernen. Weitere Informationen finden Sie in [Benutzern Zugriff zum Hinzufügen und Entfernen von Ressourcentags erteilen](/docs/resources?topic=resources-access#access).

## Kann ich einen eigenen Tag löschen?
{: # delete-tag}
{: faq}

Bevor Sie einen Tag löschen können, müssen Sie ihn von allen Ressourcen entfernen. Falls Sie den Tag dennoch nicht löschen können, ist er möglicherweise einer Ressource zugeordnet, für deren Anzeige Sie nicht berechtigt sind. Derselbe Tag kann von verschiedenen Benutzern im selben Abrechnungskonto mehreren Ressourcen zugeordnet werden. Nicht alle Benutzer im Konto verfügen über dieselben Anzeigeberechtigungen für alle Ressourcen.

## Kann ich einen Tag umbenennen?
{: #rename-tag}
{: faq}

Der Name eines Tags kann nicht bearbeitet werden. Wenn Sie einen Tag umbenennen möchten, entfernen Sie ihn und weisen Sie der Ressource einen neuen Tag zu.  
