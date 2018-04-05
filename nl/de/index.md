---

copyright:

  years: 2015, 2018
lastupdated: "2018-03-12"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Kontotypen
{: #accounts}

Wenn Sie sich für {{site.data.keyword.Bluemix}} entscheiden, entstehen Ihnen zunächst keine Kosten. Sie können unter drei unterschiedlichen Kontotypen wählen: Lite-Konto, nutzungsabhängiges Konto und Abonnementkonto. Sie können jeden der Kontotypen verwenden, um Ihre Arbeit mit {{site.data.keyword.Bluemix_notm}} zu beginnen - wählen Sie einfach den für Ihre Anforderungen am besten geeigneten Kontotyp aus.
{:shortdesc}

## Kontovergleich
{: #compare}

Die folgende Tabelle enthält einen Vergleich von Lite-Konto, nutzungsabhängigem Konto und Abonnementkonto. Weitere Informationen zu den einzelnen Konten finden Sie in den folgenden Abschnitten.

|  | Lite  | Nutzungsabhängig | Abonnement |
|--------------------|--------------------|--------------------|--------------------|
| **Zugriff auf kostenlosen Cloud Foundry-Speicher** | 256 MB | 512 MB | 512 MB |
| **Zugriff auf [Lite-Servicepläne ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/catalog/?search=label:lite){: new_window}** | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Zugriff auf alle kostenlosen Pläne** |  | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Zugriff auf den gesamten Katalog** |  | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Keine zeitlichen Begrenzungen** | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Kostenfreiheitsgarantie** | ![Funktion verfügbar](../icons/icon_enabled.svg) |  |  |
| **Preisgestaltung auf Verhandlungsbasis** |  |  | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Eignung für Schulung oder Erstellung von POCs** | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |  |
| **Eignung für den Produktionseinsatz** |  | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
{: caption="Tabelle 1. Vergleich von {{site.data.keyword.Bluemix_notm}}-Konten" caption-side="top"}

## Lite-Konto
{: #liteaccount}

Registrieren Sie sich für ein kostenloses Lite-Konto, um mit ausgewählten gebührenfreien Plänen Apps zu entwickeln und Services zu nutzen. Diese Lite-Pläne werden mit einem Lite-Tag ![Lite-Tag](../icons/Lite.svg) in der {{site.data.keyword.Bluemix_notm}}-Konsole angezeigt. Ihr Lite-Konto gilt unbefristet und Ihre Kreditkarte wird nicht benötigt.

Sie haben Zugriff auf eine einzelne Ressourcengruppe, die für Sie erstellt wurde und den Namen `Default` (Standard) trägt. Alle Serviceinstanzen, die von {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) verwaltet werden, werden dieser Ressourcengruppe automatisch hinzugefügt. Sie können den Namen dieser Ressourcengruppe jederzeit ändern. Detaillierte Schritte finden Sie unter [Ressourcengruppe umbenennen](/docs/account/resourcegroups.html#renaming-a-resource-group).

Jede Ressourcengruppe ist kostenfrei. Wenn Sie eine Verbindung zwischen einem von IAM verwalteten Service und einer Cloud Foundry-App erstellen, erstellen Sie einen Aliasnamen, der eine Serviceinstanz ist, die zu Ihrem Kontingent zählt. Weitere Informationen finden Sie unter [Was ist ein Aliasname?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

### Merkmale und Leistungen

Ein Lite-Konto umfasst das nachfolgend beschriebene Angebot. Die folgende Liste enthält die wichtigsten Merkmale:

   * Das Konto ist kostenfrei - Sie benötigen keine Kreditkarte.
   * Für das Konto existiert kein Ablaufdatum.
   * Sie können eine Organisation in einer {{site.data.keyword.Bluemix_notm}}-Region verwenden.
   * {{site.data.keyword.Bluemix_notm}} Basic Support ist kostenlos. Basic Support wird für Nicht-Produktionsumgebungen oder -Workloads bereitgestellt, bei denen keine konventionellen Prioritäten verwendet und spezielle Reaktionszeiten vereinbart werden.
   * Sie erhalten E-Mail-Benachrichtigungen über Ihren Kontostatus und Ihre Kontingentbeschränkungen.
   * Ihre Cloud Foundry-Apps können auf bis zu 256 MB an freiem, sofort verfügbarem Laufzeitspeicher zugreifen.
   * Sie können eine Instanz jedes Service im [{{site.data.keyword.Bluemix_notm}}-Katalog einrichten![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window}, für den ein Lite-Plan besteht.
   * Nach 10 Tagen ohne Entwicklungstätigkeit werden Ihre Apps inaktiviert. Sie können mit der Arbeit an neuen Apps beginnen, ohne sich Gedanken über begrenzten Speicher machen zu müssen.
   * Nach 30 Tagen ohne Entwicklungstätigkeit werden Ihre Serviceinstanzen mit den Lite-Plänen gelöscht. Das heißt, Sie müssen sich nicht um das Löschen inaktiver Instanzen kümmern, bevor Sie neue Instanzen erstellen.

### Upgrade für Konto durchführen

Wenn Sie Ihre Umgebung später ausbauen möchten, führen Sie ein Upgrade auf ein nutzungsabhängiges Konto durch und zahlen Sie nur das, was Sie über die Gratisleistungen hinaus nutzen. Nach dem Upgrade können Sie die mit Ihrem Lite-Konto erstellten Instanzen weiterhin verwenden. Rufen Sie in der Konsole die Seite **Verwalten** > **Abrechnung und Nutzung** > **Abrechnung** auf und klicken Sie auf **Kreditkarte hinzufügen**. 

## Gebührenpflichtige Konten
{: #billableacts}

In der folgenden Tabelle werden die verschiedenen Kontotypen und ihre Gebührenmodelle aufgelistet.

|Kontotyp |	Art der Gebührenabrechnung |
|------------------|-----------------------|
|Nutzungsabhängig |	Kosten werden auf der Grundlage Ihrer Nutzung der {{site.data.keyword.Bluemix_notm}}-Berechnungen und -Services in Rechnung gestellt. |
|Abonnement | Sie können einen monatlichen Rabatt auf der Basis einer verbindlichen Mindestausgabeverpflichtung erhalten. |
| {{site.data.keyword.Bluemix_dedicated_notm}} | Jahresvertrag |
|{{site.data.keyword.Bluemix_local_notm}} |	Jahresvertrag |
{:caption="Tabelle 2. Gebührenpflichtige {{site.data.keyword.Bluemix_notm}}-Konten und Gebühren" caption-side="top"}

Wenn Sie Ihr gebührenpflichtiges {{site.data.keyword.Bluemix_notm}}-Konto mit einem SoftLayer-Konto verknüpfen, werden Ihre kombinierten Gebühren ab dem Ersten des folgenden Monats über die {{site.data.keyword.Bluemix_notm}}-Rechnung abgerechnet. Weitere Informationen finden Sie unter [Guthaben anzeigen](/docs/billing-usage/viewing_usage.html#credits).
{: tip}

### Nutzungsabhängiges Konto

Mit einem nutzungsabhängigen Konto können Sie mehrere Ressourcengruppen erstellen, um Kontingente ohne großen Aufwand zu verwalten und um Informationen zu Abrechnung und Nutzung für eine Gruppe von Ressourcen anzuzeigen. Ihnen stehen zusätzliche kostenlose Laufzeit- und Serviceleistungen zur Verfügung. Wenn Sie in Ihrer Nutzung über die gebührenfreien Leistungen hinausgehen, erhalten Sie eine {{site.data.keyword.Bluemix_notm}}-Rechnung für den Monat. Die Rechnung wird in USD ausgestellt und enthält die Details zu Ihren Ressourcengebühren.

In vielen Ländern und Regionen können Sie sich für ein nutzungsabhängiges Konto über die {{site.data.keyword.Bluemix_notm}}-Konsole anmelden. Akzeptieren Sie nach der Angabe Ihrer Abrechnungs- und Kreditkarteninformationen die Vertragsbedingungen und übergeben Sie Ihre Anforderung. Anschließend wird Ihre Kreditkarte geprüft. Sie erhalten außerdem eine Bestätigungs-E-Mail zu den Kontoinformationen. Einige Minuten nach Empfang der Bestätigungs-E-Mail können Sie zur Konsole zurückkehren, um mit der Erstellung Ihrer Apps fortzufahren. 

Wenn Ihre Onlineanforderung für Ihr Land oder Ihre Region nicht verarbeitet werden kann, wenden Sie sich an den [{{site.data.keyword.Bluemix_notm}}-Support](https://ibm.biz/bluemixsupport){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg). Klicken Sie nach der Anmeldung beim {{site.data.keyword.Bluemix_notm}}-Serviceportal auf **Unterstützung anfordern** und wählen Sie die Option für Abrechnung, Konto oder Anmeldung**** aus.

Sie können Ihr Konto für nutzungsabhängige Zahlung jederzeit in ein Abonnementkonto konvertieren. Weitere Informationen erhalten Sie über den [{{site.data.keyword.Bluemix_notm}}-Vertrieb](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg).
{: tip}

### Abonnementkonto

Mit einem Abonnementkonto können Sie mehrere Ressourcengruppen erstellen, um Kontingente ohne großen Aufwand zu verwalten und um Informationen zu Abrechnung und Nutzung für eine Gruppe von Ressourcen anzuzeigen.

Sie verpflichten sich zu einem Mindestausgabebetrag pro Monat und erhalten einen Abonnementrabatt, der auf diese Mindestgebühr angewendet wird. Außerdem müssen Sie jede Nutzung bezahlen, die über den Mindestausgabebetrag hinausgeht.

Wenden Sie sich an den [{{site.data.keyword.Bluemix_notm}}-Vertrieb](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg), um sich für ein Abonnementkonto anzumelden oder um weitere Informationen zu Abonnementgebühren und -nachlässen zu erhalten.

### {{site.data.keyword.Bluemix_dedicated_notm}}-Konto

Bei {{site.data.keyword.Bluemix_dedicated_notm}} müssen Sie sich für eine Mindestlaufzeit von einem Jahr anmelden.

   * VPN-Anbindung zurück zu Ihrer Infrastruktur
   * Vollständige redundante Umgebung in einem {{site.data.keyword.BluSoftLayer_notm}}-Rechenzentrum
   * Alle unterstützten Laufzeiten (IBM Java Liberty, Node.js sowie integrierte Open-Source-Laufzeiten)
   * Alle dedizierten Services, die Sie ausgewählt haben, und alle öffentlichen {{site.data.keyword.Bluemix_notm}}-Services
   * Standard-{{site.data.keyword.Bluemix_notm}}-Unterstützung

Es können auch optionale Elemente wie z. B. SoftLayer DirectLink oder Premium-Support-Optionen bestellt werden. Weitere Informationen erhalten Sie vom [{{site.data.keyword.Bluemix_notm}}-Vertrieb ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg).

Die monatlichen Kosten während dieser Laufzeit sind von den von Ihnen gewünschten dedizierten Services plus einem Abonnementkonto abhängig, mit dem Sie auf alle öffentlichen Services zugreifen können. Die Nutzungsgebühren der Services in {{site.data.keyword.Bluemix_notm}} Public werden auf der Grundlage Ihrer Abonnementkontovereinbarung berechnet. Sie erhalten für sämtliche Services, die Sie über die Abonnementvereinbarung hinaus nutzen, eine Rechnung. Für Informationen zu Ihrer Vereinbarung wenden Sie sich an Ihren zugewiesenen IBM Kundenbeauftragten oder an den [{{site.data.keyword.Bluemix_notm}}-Vertrieb](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg).

### {{site.data.keyword.Bluemix_local_notm}}-Konto

Bei {{site.data.keyword.Bluemix_local_notm}} müssen Sie sich für eine Mindestlaufzeit von einem Jahr anmelden.

   * Eine Zustellungsfunktion, die als Relay bezeichnet wird, mit deren Hilfe IBM eine Verbindung zu Ihrer lokalen Bereitstellung herstellen und Aktualisierungen automatisch und unterbrechungsfrei übermitteln kann
   * Alle unterstützten Laufzeiten (IBM Java Liberty, Node.js sowie integrierte Open-Source-Laufzeiten)
   * Alle lokalen Services, die Sie ausgewählt haben, und Zugriff auf alle öffentlichen {{site.data.keyword.Bluemix_notm}}-Services
   * Standard-{{site.data.keyword.Bluemix_notm}}-Unterstützung

Die monatlichen Kosten während dieser Laufzeit sind von den von Ihnen gewünschten lokalen Services plus einem Abonnementkonto abhängig, mit dem Sie auf alle öffentlichen Services zugreifen können. Die Nutzungsgebühren der Services in {{site.data.keyword.Bluemix_notm}} Public werden auf der Grundlage Ihrer Abonnementkontovereinbarung berechnet. Sie erhalten für sämtliche Services, die Sie über die Abonnementvereinbarung hinaus nutzen, eine Rechnung. Für Informationen zu Ihrer Vereinbarung wenden Sie sich an Ihren zugewiesenen IBM Kundenbeauftragten oder an den [{{site.data.keyword.Bluemix_notm}}-Vertrieb](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg).

## Testkonto
{: #trial}

Testkonten sind in allen Regionen verfügbar. Der 30-Tage-Testzeitraum bietet Ihnen die Möglichkeit zum Schnelleinstieg für das Entwickeln von Apps und das Nutzen der Services in {{site.data.keyword.Bluemix_notm}}.

Wenn Sie sich für einen kostenfreien Test mit Ihrer {{site.data.keyword.Bluemix_notm}}-ID registrieren, wird Ihr Konto gebührenfrei mit den folgenden Ressourcen ausgestattet:

  * Maximal 2 GB Speicher
  * 10 Services
  * 1 SSL-Zertifikat

Sie haben außerdem Zugriff auf eine einzelne Ressourcengruppe, die für Sie erstellt wurde und den Namen `Default` (Standard) trägt. Alle von IAM verwalteten Serviceinstanzen werden automatisch zu dieser Ressourcengruppe hinzugefügt. Sie können den Namen dieser Ressourcengruppe jederzeit ändern. Detaillierte Schritte finden Sie unter [Ressourcengruppe umbenennen](/docs/account/resourcegroups.html#renaming-a-resource-group).

Jede Ressourcengruppe ist kostenfrei. Wenn Sie eine Verbindung zwischen einem von IAM verwalteten Service und einer Cloud Foundry-App erstellen, erstellen Sie einen Aliasnamen, der eine Serviceinstanz ist, die zu Ihrem Kontingent zählt. Weitere Informationen finden Sie unter [Was ist ein Aliasname?](/docs/cfapps/connecting_apps.html#what_is_alias).
{: tip}

### Möglichkeiten am Ende des kostenlosen Testzeitraums
{: #trialend}

Ihr kostenloser Testzeitraum läuft 30 Tage nach Ihrer Registrierung ab; dann werden die Apps in Ihrem Konto gestoppt. Sie können sich zwar nicht für ein weiteres {{site.data.keyword.Bluemix_notm}}-Konto registrieren, aber Sie können weiterhin auf Ihr Konto und die Konten zugreifen, für die Sie eingeladen wurden.

Zum erneuten Starten Ihrer Anwendungen müssen Sie Ihr Konto in ein gebührenpflichtiges Konto umwandeln - also entweder Ihre Kreditkarteninformationen für ein nutzungsabhängiges Konto angeben oder ein Konto vom Typ 'Abonnement' erstellen. Anschließend können Sie mit der Verwendung der kostenlosen Rechen- und Serviceressourcen fortfahren. Sie zahlen nur für die Nutzung von Services, Containern und Laufzeiten, die nicht durch die kostenlosen Monatsleistungen abgedeckt sind.

  * Um ein Upgrade auf ein nutzungsabhängiges Konto durchzuführen, rufen Sie in der Konsole die Seite **Verwalten** > **Abrechnung und Nutzung** > **Abrechnung** auf und klicken Sie auf **Kreditkarte hinzufügen**.
  * Informationen zum Anmelden eines Abonnementkontos erhalten Sie vom [{{site.data.keyword.Bluemix_notm}}-Vertrieb](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg).

Wenn Sie Ihr Konto nach Ablauf des kostenlosen Testzeitraums nicht umwandeln, werden Ihre Apps und Services nach 30 Tagen entfernt. Ihr Konto wird jedoch nicht gelöscht und Sie können sich jederzeit anmelden und Ihr Konto in ein gebührenpflichtiges Konto umwandeln. Außerdem erhalten Sie E-Mail-Benachrichtigungen, die Sie daran erinnern, ein gebührenpflichtiges Konto einzurichten, damit Ihre App-Einstellungen und Servicekonfigurationen nicht verloren gehen. Wenn Sie diese Benachrichtigungen von {{site.data.keyword.Bluemix_notm}} nicht empfangen möchten, können Sie das Abonnement jederzeit beenden.

Wenn Sie Ihr Konto umwandeln, werden Ihre kostenlosen Leistungen auf diejenigen begrenzt, die normalerweise von jedem Service bereitgestellt werden. Die kostenlosen Leistungen sind keine Leistungen mit unbegrenzter Nutzung mehr, die von vielen IBM Services während der kostenlosen Testperiode angeboten werden.

