---

copyright:
  years: 2015, 2019
lastupdated: "2019-08-06"

keywords: troubleshoot account, account problem, account support, account help, account error, access error, login error, error message

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


# Fehlerbehebung für den Zugriff auf {{site.data.keyword.Bluemix_notm}}
{: #accessing}

Allgemeine Probleme beim Zugriff auf {{site.data.keyword.Bluemix}} können sein, dass es Schwierigkeiten bei der Anmeldung bei {{site.data.keyword.Bluemix_notm}} gibt oder sich ein Konto dauerhaft im Wartestatus befindet. In vielen Fällen können Sie diese Probleme durch Ausführen weniger einfacher Schritte beheben.
{:shortdesc}


## Warum ist mein Kennwort nicht korrekt?
{: #ts_logintobm}
{: troubleshoot}

Sie müssen über ein gültiges Kennwort verfügen, das Ihrer IBMid-ID oder SoftLayer-ID zugeordnet ist, um sich bei der {{site.data.keyword.Bluemix_notm}}-Konsole anzumelden.

Wenn Sie versuchen, sich bei {{site.data.keyword.Bluemix_notm}} anzumelden, wird die folgende Fehlernachricht angezeigt:
{: tsSymptoms}

`Das eingegebene Kennwort ist nicht korrekt.`

Das Kennwort, das Sie für die Anmeldung bei {{site.data.keyword.Bluemix_notm}} verwendet haben, ist nicht gültig.
{: tsCauses}

Verwenden Sie eine der folgenden Optionen:
{: tsResolve}
 * Rufen Sie die [Profilseite von 'Meine IBM' ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://myibm.ibm.com/dashboard/){: new_window} auf, um sich zu vergewissern, dass Sie ein gültiges Kennwort verwenden.
 * Falls Sie Ihr Kennwort vergessen haben, klicken Sie auf **Kennwort vergessen**, um Ihr Kennwort zurückzusetzen.
 * Wenn Sie Ihre IBMid vergessen haben oder weiterhin Probleme mit dem Kennwort vorliegen, suchen Sie auf der Site 'Worldwide IBM Registration Helpdesk' nach Hilfe.

Wenn Sie sich bei {{site.data.keyword.Bluemix_notm}} anmelden und der Anmeldeprozess aus irgendeinem Grund unterbrochen wird, z. B. durch das Zurücksetzen des Kennworts, kehren Sie zur Konsole zurück und starten Sie den Anmeldeprozess erneut.
{: tip}


## Warum wurde meine IBMid oder E-Mail-Adresse nicht erkannt?
{: #ts_old_username}
{: troubleshoot}

Für eine erfolgreiche Anmeldung bei der {{site.data.keyword.Bluemix_notm}}-Konsole müssen Sie sicherstellen, dass Sie über eine IBMid-Authentifizierung für jedes Konto verfügen. 

Wenn Sie sich bei der Konsole anmelden, wird die folgende Nachricht angezeigt:
{: tsSymptoms}

`Diese IBMid oder E-Mail-Adresse wurde nicht erkannt.`

Sie haben versucht, sich bei der Konsole anzumelden, jedoch keine gültige IBMid verwendet. Beispielsweise haben Sie keine vollständig qualifizierte E-Mail-Adresse für die IBMid eingegeben oder versucht, einen Benutzernamen mit dem zugehörigen Kennwort zu verwenden.
{: tsCauses}

Sie müssen über eine gültige IBMid und ein Kennwort verfügen, um sich bei {{site.data.keyword.Bluemix_notm}} anmelden zu können.

 * Geben Sie eine vollständig qualifizierte E-Mail-Adresse für die IBMid ein.
 {: tsResolve}
 * Wenn Sie ein SoftLayer-Benutzer mit einer SoftLayer-ID sind, müssen Sie in jedem Konto, auf das Sie zugreifen können, zur IBMid-Authentifizierung wechseln, bevor Sie sich anmelden können. Weitere Informationen finden Sie unter [Zur IBMid wechseln](/docs/account?topic=account-unifyingaccounts).


## Warum ist meine IBMid keinen {{site.data.keyword.Bluemix_notm}}-Konten zugeordnet?
{: #ts_unabletologin}
{: troubleshoot}

Wenn Sie sich bei {{site.data.keyword.Bluemix_notm}} anmelden, wird die folgende Nachricht angezeigt:
{: tsSymptoms}

`Sie sind auf diese Seite gelangt, weil Ihre Authentifizierung erfolgreich war; allerdings ist diese IBMid keinem {{site.data.keyword.Bluemix_notm}}-Konto zugeordnet.`

Sie haben sich über die [{{site.data.keyword.Bluemix_notm}}-Konsole](https://{DomainName}){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") mit einer gültigen IBMid angemeldet, es ist jedoch kein {{site.data.keyword.Bluemix_notm}}-Konto für Sie erstellt.
{: tsCauses}

Führen Sie den Registrierungsprozess durch, um ein {{site.data.keyword.Bluemix_notm}}-Konto zu erstellen.
{: tsResolve}


## Warum wird die Konsole nicht geöffnet, wenn ich mich mit meiner IBMid anmelde?
{: #ts_login_stalls}
{: troubleshoot}

Wenn Sie sich mit Ihrer IBMid anmelden, wird eine Nachricht über die erfolgreiche Anmeldung angezeigt, die {{site.data.keyword.Bluemix_notm}}-Konsole wird jedoch nicht erneut aufgerufen.
{: tsSymptoms}

Verwenden Sie eine der folgenden Optionen:
{: tsResolve}
 * Schließen Sie Ihren Browser, löschen Sie Cookies sowie den Inhalt des Cache und versuchen Sie erneut, sich anzumelden.
 * Melden Sie sich über die [{{site.data.keyword.Bluemix_notm}}-Konsole](https://{DomainName}){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") an.


## Warum wurde meine IBMid-Anmeldung nicht abgeschlossen?
{: #ts_login_ibmid}
{: troubleshoot}

Wenn Sie sich bei {{site.data.keyword.Bluemix_notm}} anmelden und die Authentifizierung Ihrer IBMid nicht vollständig ausgeführt wird, möglicherweise ein Problem mit dem Service vor.

Wenn Sie sich bei {{site.data.keyword.Bluemix_notm}} anmelden, wird die Authentifizierung mit der IBMid nicht vollständig abgeschlossen.
{: tsSymptoms}

Möglicherweise besteht ein Problem beim Service für die IBMid-Authentifizierung.
{: tsCauses}

Stellen Sie sicher, dass Sie sich bei [IBM](https://idaas.iam.ibm.com/idaas/mtfim/sps/authsvc?PolicyId=urn:ibm:security:authentication:asf:basicldapuser){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") anmelden können. Ist dies der Fall, handelt es sich um ein Anwendungsproblem und Sie können die Anmeldung über die Konsole zu einem späteren Zeitpunkt erneut versuchen. Wenn Sie sich nicht bei dieser Seite anmelden können, wenden Sie sich an den [IBMid-Help-Desk ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}.  
{: tsResolve}


## Warum kann ich mich nicht sofort anmelden, nachdem ich eine Registrierung für ein Konto durchgeführt habe?
{: #ts_accntpding}
{: troubleshoot}

Falls sich Ihr Konto noch im Wartestatus befindet, können Sie sich nicht bei {{site.data.keyword.Bluemix_notm}} anmelden.

Nach der Registrierung für ein {{site.data.keyword.Bluemix_notm}}-Konto können Sie sich möglicherweise nicht bei {{site.data.keyword.Bluemix_notm}} anmelden.
{: tsSymptoms}

Bei der Registrierung für ein {{site.data.keyword.Bluemix_notm}}-Konto erhalten Sie eine E-Mail mit einem Bestätigungs-Link. Sie müssen auf diesen Link klicken, um die Registrierung zu bestätigen. Wenn Sie die Registrierung nicht bestätigen, bleibt Ihr Konto im Wartestatus.
{: tsCauses}

Die Bestätigungs-E-Mail wird an die E-Mail-Adresse gesendet, die Ihrer IBMid zugeordnet ist. Überprüfen Sie Ihren Posteingang und Ihren Spamordner. Wenn Sie die Bestätigungs-E-Mail nicht erhalten haben, rufen Sie die [{{site.data.keyword.Bluemix_notm}} Anmeldeseite](https://cloud.ibm.com/){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") auf und versuchen Sie, sich anzumelden. Die folgende Nachricht wird angezeigt:
{: tsResolve}

```
Zum Abschluss Ihrer Registrierung müssen Sie Ihren E-Mail-Eingang überprüfen.
Die E-Mail ist nicht vorhanden? Erneut senden.
```
{:screen}

Klicken Sie auf **Erneut senden**, damit eine weitere Bestätigungs-E-Mail an die E-Mail-Adresse gesendet wird, die Ihrer IBMid zugeordnet ist. Falls es weiterhin nicht möglich ist, die Registrierung abzuschließen, wenden Sie sich an den [{{site.data.keyword.Bluemix_notm}} Support](/docs/get-support?topic=get-support-getting-customer-support).  

## Warum werden Konsolenseiten nicht geladen?
{: #ts_err}
{: troubleshoot}

Wenn Sie die {{site.data.keyword.Bluemix_notm}}-Konsole verwenden, kann es vorkommen, dass Sie eine Konsolenseite nicht laden können. Stattdessen werden möglicherweise die Fehlernachrichten BXNUI0001E oder BXNUI0016E angezeigt. 

Es wird möglicherweise eine der folgenden Fehlernachrichten angezeigt:
{: tsSymptoms}

`BXNUI0001E: Die Seite wurde nicht geladen, weil von {{site.data.keyword.Bluemix_notm}} nicht erkannt wurde, ob eine Sitzung vorhanden ist.`

`BXNUI0016E: Die Apps und Services wurden nicht abgerufen, da eine {{site.data.keyword.Bluemix_notm}}-Seite nicht geladen wurde.`

Führen Sie nach Bedarf eine oder mehrere der folgenden Aktionen aus:
{: tsResolve}

  * Aktualisieren Sie den Browser oder starten Sie ihn erneut.
  * Melden Sie sich bei {{site.data.keyword.Bluemix_notm}} ab und anschließend wieder an.
  * Verwenden Sie den persönlichen Browsing-Modus des Browsers.
  * Löschen Sie Cookies und den Inhalt des Browser-Cache.
  * Verwenden Sie einen anderen Browser. Informationen zu den Versionen der Browser, die von {{site.data.keyword.Bluemix_notm}} unterstützt werden, finden Sie in den [{{site.data.keyword.Bluemix_notm}}-Voraussetzungen](/docs/overview?topic=overview-prereqs-platform).
  * Wenn Sie die Cloud Foundry-Befehlszeilenschnittstelle installiert haben, geben Sie den Befehl `ibmcloud cf apps` ein, um anzuzeigen, ob die App aktiv ist.

## Wie kann ich auf Infrastrukturservices in meinem Konto zugreifen?
{: #troubleshoot-infrastructure-access}
{: troubleshoot}

Wenn Sie versuchen, auf Infrastrukturabschnitte in der IBM Cloud-Konsole zuzugreifen, wird die folgende Nachricht angezeigt:
{: tsSymptoms}

`Diese Seite kann nicht geladen werden, da das Infrastrukturkonto nicht vollständig als IBM Cloud-Konto konfiguriert ist. `

Für die Anzeige dieser Nachricht gibt es mehrere mögliche Gründe:
{: tsCauses}

* Sie verfügen über ein [Lite-Konto](/docs/account?topic=account-accounts#liteaccount), das den Zugriff auf Infrastrukturservices nicht zulässt.
* Das Konto ist nicht mit einem Infrastrukturkonto verbunden.


Zur Behebung dieses Problems müssen Sie ein Upgrade auf ein Konto mit nutzungsabhängiger Abrechnung oder ein Abonnementkonto durchführen. Weitere Informationen finden Sie in [Upgrade für Konto durchführen](/docs/account?topic=account-upgrading-account).
{: tsResolve}
