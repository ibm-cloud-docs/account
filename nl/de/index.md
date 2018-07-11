---

copyright:

  years: 2015, 2018
lastupdated: "2018-06-26"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Kontotypen
{: #accounts}

Sie können zwischen den drei folgenden {{site.data.keyword.Bluemix}}-Kontotypen wählen: dem Lite-Konto, dem nutzungsabhängigen Konto und dem Abonnementkonto. Sie können jeden der Kontotypen verwenden, um Ihre Arbeit mit {{site.data.keyword.Bluemix_notm}} zu beginnen - wählen Sie den für Ihre Anforderungen am besten geeigneten Kontotyp aus.
{:shortdesc}

## Konten im Vergleich
{: #compare}

Die folgende Tabelle enthält einen Vergleich von Lite-Konto, nutzungsabhängigem Konto und Abonnementkonto. Weitere Informationen zu den einzelnen Konten finden Sie in den folgenden Abschnitten.

|  | Lite  | Nutzungsabhängig | Abonnement |
|--------------------|--------------------|--------------------|--------------------|
| **Zugriff auf kostenlosen Cloud Foundry-Speicher** | 256 MB | 512 MB | 512 MB |
| **Zugriff auf [Lite-Servicepläne ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://console.bluemix.net/catalog/?search=label:lite){: new_window}** | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Zugriff auf alle kostenlosen Pläne** |  | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Zugriff auf den gesamten {{site.data.keyword.Bluemix_notm}}-Katalog** |  | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Zugriff auf mehrere Cloud Foundry-Regionen** |  | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Keine zeitlichen Begrenzungen** | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Kostenfreiheitsgarantie** | ![Funktion verfügbar](../icons/icon_enabled.svg) |  |  |
| **Preise mit Nachlass** |  |  | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Eignung für Schulung oder Erstellung von POCs** | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |  |
| **Eignung für den Produktionseinsatz** |  | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
{: caption="Tabelle 1. Vergleich von {{site.data.keyword.Bluemix_notm}}-Konten" caption-side="top"}

## Lite-Konto
{: #liteaccount}

Registrieren Sie sich für ein Lite-Konto, um unter Nutzung ausgewählten gebührenfreien Pläne mit der Entwicklung von Apps und Erkundung von Services zu beginnen. Diese Lite-Pläne werden mit einem Lite-Tag ![Lite-Tag](../icons/Lite.svg) in der {{site.data.keyword.Bluemix_notm}}-Konsole angezeigt. Ihr Lite-Konto gilt unbefristet und Ihre Kreditkarte wird nicht benötigt.

Sie haben Zugriff auf eine einzelne Ressourcengruppe, die für Sie erstellt wurde und den Namen `Default` (Standard) trägt. Alle Serviceinstanzen, die von {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) verwaltet werden, werden dieser Ressourcengruppe automatisch hinzugefügt. Sie können den Namen dieser Ressourcengruppe jederzeit ändern. Detaillierte Schritte finden Sie unter [Ressourcengruppe umbenennen](/docs/resources/resourcegroups.html#renaming-a-resource-group).

Jede Ressourcengruppe ist kostenfrei. Wenn Sie eine Verbindung zwischen einem von IAM verwalteten Service und einer Cloud Foundry-App erstellen, erstellen Sie einen Aliasnamen, der eine Serviceinstanz ist, die zu Ihrem Kontingent zählt. Weitere Informationen finden Sie unter [Was ist ein Aliasname?](/docs/resources/connecting_apps.html#what_is_alias).
{: tip}

### Merkmale und Leistungen

Die folgende Liste enthält zentrale Features, die mit einem Lite-Konto zur Verfügung stehen:

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
{: #upgrade-to-paygo}

Wenn Sie Ihre Umgebung ausbauen möchten, können Sie für Ihr Lite-Konto ein Upgrade auf ein nutzungsabhängiges Konto oder ein Abonnementkonto durchführen. 

  * Rufen Sie für ein Upgrade auf ein nutzungsabhängiges Konto **Verwalten** > **Abrechnung und Nutzung** > **Abrechnung** in der Konsole auf und klicken Sie auf **Kreditkarte hinzufügen**.
  * Rufen Sie für ein Upgrade auf ein Abonnementkonto **Verwalten** > **Abrechnung und Nutzung** > **Abrechnung** in der Konsole auf und klicken Sie auf **Weitere Informationen**.


## Nutzungsabhängiges Konto
{: #paygo}

Mit einem nutzungsabhängigen Konto können Sie mehrere Ressourcengruppen erstellen, um Kontingente ohne großen Aufwand zu verwalten und um Informationen zu Abrechnung und Nutzung für eine Gruppe von Ressourcen anzuzeigen. Die für Sie anfallenden Gebühren richten Sie nach Ihrer Nutzung von {{site.data.keyword.Bluemix_notm}}-Berechnungen und -Services. Ihnen stehen zusätzliche kostenlose Laufzeit- und Serviceleistungen zur Verfügung. Wenn Sie in Ihrer Nutzung über die gebührenfreien Leistungen hinausgehen, erhalten Sie eine {{site.data.keyword.Bluemix_notm}}-Rechnung für den Monat. Die Rechnung ist in USD ausgestellt und enthält Detailangaben zu Ihren Ressourcengebühren.

Wenn Sie Ihr Konto mit nutzungsabhängiger Zahlung mit einem SoftLayer-Konto verknüpfen, werden Ihre kombinierten Gebühren ab dem Ersten des Folgemonats über die {{site.data.keyword.Bluemix_notm}}-Rechnung abgerechnet.
{: tip}

Über die {{site.data.keyword.Bluemix_notm}}-Konsole können Sie ein Upgrade auf ein Konto mit nutzungsabhängiger Zahlung durchführen. Geben Sie zunächst Ihre Abrechnungs- und Kreditkarteninformationen an, akzeptieren Sie dann die Vertragsbedingungen und übergeben Sie anschließend die Anforderung. Es wird eine Überprüfung Ihrer Kreditkarte durchgeführt. Außerdem erhalten Sie eine Bestätigungs-E-Mail zu den Kontoinformationen. Einige Minuten nach Empfang der Bestätigungs-E-Mail können Sie zur Konsole zurückkehren, um mit der Erstellung Ihrer Apps fortzufahren. Wenn Ihre Onlineanforderung für Ihr Land oder Ihre Region nicht verarbeitet werden kann, wenden Sie sich an den [{{site.data.keyword.Bluemix_notm}}-Support](/docs/get-support/howtogetsupport.html).

Nach dem Upgrade auf ein Konto mit nutzungsabhängiger Zahlung erhalten Sie eine Werbegutschrift in Höhe von 200 US-Dollar, die Sie nutzen können, ohne dass hierfür weitere Aktionen ausgeführt werden müssen. Die Gutschrift von 200 US-Dollar hat eine Gültigkeit von 30 Tagen und wird automatisch mit Ihrer Rechnung verrechnet. Die Gutschrift kann nicht mit Angeboten anderer Anbieter verwendet werden. 

### Upgrade für Konto durchführen
{: #upgrade-to-subscription}

Für Ihr Konto mit nutzungsabhängiger Zahlung können Sie jederzeit ein Upgrade auf ein Abonnementkonto durchführen. Weitere Informationen erhalten Sie über den [{{site.data.keyword.Bluemix_notm}}-Vertrieb](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg).

## Abonnementkonto

Mit einem Abonnementkonto können Sie mehrere Ressourcengruppen erstellen, um Kontingente ohne großen Aufwand zu verwalten und um Informationen zu Abrechnung und Nutzung für eine Gruppe von Ressourcen anzuzeigen. Sie verpflichten sich zu einem Mindestausgabebetrag pro Monat und erhalten einen Abonnementrabatt, der auf diese Mindestgebühr angewendet wird. Außerdem müssen Sie jede Nutzung bezahlen, die über den Mindestausgabebetrag hinausgeht.

Wenn Sie Ihr Abonnementkonto mit einem SoftLayer-Konto verknüpfen, werden Ihre kombinierten Gebühren ab dem Ersten des Folgemonats über die {{site.data.keyword.Bluemix_notm}}-Rechnung abgerechnet.
{: tip}

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

