---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-13"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Kontotypen
{: #accounts}

{{site.data.keyword.Bluemix_notm}} bietet drei verschiedene Kontotypen: Lite-Konto, nutzungsabhängiges Konto und Abonnementkonto. Sobald Sie eine Registrierung durchführen, erhalten Sie ein kostenfreies Lite-Konto. Nutzungsabhängige Konten und Abonnementkonten sind die verfügbaren kostenpflichtigen Kontooptionen, mit denen jeweils unterschiedliche Features zur Verfügung stehen. Vergleichen Sie die einzelnen Kontotypen und wählen Sie das Konto aus, das für Sie am besten geeignet ist.
{:shortdesc}


## Konten im Vergleich
{: #compare}

Die folgende Tabelle enthält einen Vergleich von Lite-Konto, nutzungsabhängigem Konto und Abonnementkonto. Weitere Informationen zu den einzelnen Konten finden Sie in den folgenden Abschnitten.

|                                         | Lite               | Nutzungsabhängig      | Abonnement       |
|-----------------------------------------|--------------------|--------------------|--------------------|
| **Zugriff auf kostenfreien Cloud Foundry-Speicher** | 256 MB             | 512 MB             | 512 MB             |
| **Zugriff auf [Lite-Servicepläne ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://{DomainName}/catalog/?search=label:lite){: new_window}** | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Zugriff auf alle kostenfreien Pläne**            |                    | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Zugriff auf den gesamten {{site.data.keyword.Bluemix_notm}}-Katalog** |  | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Zugriff auf mehrere Cloud Foundry-Regionen** |               | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Keine zeitlichen Begrenzungen** | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Kostenfreiheitsgarantie**                | ![Funktion verfügbar](../icons/icon_enabled.svg) |  |         |
| **Preise mit Nachlass**                  |                    |                    | ![Funktion verfügbar](../icons/icon_enabled.svg) |
| **Eignung für Schulung oder Erstellung von POCs** | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |  |
| **Eignung für den Produktionseinsatz**        |                    | ![Funktion verfügbar](../icons/icon_enabled.svg) | ![Funktion verfügbar](../icons/icon_enabled.svg) |
{: caption="Tabelle 1. Vergleich von {{site.data.keyword.Bluemix_notm}}-Konten" caption-side="top"}


## Lite-Konto
{: #liteaccount}

Registrieren Sie sich für ein Lite-Konto, um unter Nutzung ausgewählten gebührenfreien Pläne mit der Entwicklung von Apps und Erkundung von Services zu beginnen. Diese Lite-Pläne werden mit einem Lite-Tag ![Lite-Tag](../icons/Lite.svg) in der {{site.data.keyword.Bluemix_notm}}-Konsole angezeigt. Ihr Lite-Konto gilt unbefristet und Ihre Kreditkarte wird nicht benötigt.

Sie haben Zugriff auf eine einzelne Ressourcengruppe, die für Sie erstellt wurde und den Namen `Default` (Standard) trägt. Alle Instanzen des Service, die von {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) verwaltet werden, werden dieser Ressourcengruppe automatisch hinzugefügt. Sie können den Namen dieser Ressourcengruppe jederzeit ändern. Detaillierte Schritte finden Sie unter [Ressourcengruppe umbenennen](/docs/resources?topic=resources-rgs#rename_rgs).

Jede Ressourcengruppe ist kostenfrei. Wenn Sie eine Verbindung zwischen einem von IAM verwalteten Service und einer Cloud Foundry-App erstellen, erstellen Sie einen Aliasnamen, der eine Serviceinstanz ist, die zu Ihrem Kontingent zählt. Weitere Informationen finden Sie in [Verbindungen verwalten](/docs/resources?topic=resources-connect_app).
{: tip}

### Merkmale und Leistungen
{: #lite-account-features}

Die folgende Liste enthält zentrale Features, die mit einem Lite-Konto zur Verfügung stehen:

   * Das Konto ist kostenfrei - Sie benötigen keine Kreditkarte.
   * Für das Konto existiert kein Ablaufdatum.
   * Sie können eine Organisation in einer {{site.data.keyword.Bluemix_notm}}-Region verwenden.
   * {{site.data.keyword.Bluemix_notm}} Basic Support ist kostenfrei. Basic Support wird für Nicht-Produktionsumgebungen oder -Workloads bereitgestellt, bei denen keine konventionellen Prioritäten verwendet und spezielle Reaktionszeiten vereinbart werden.
   * Sie erhalten E-Mail-Benachrichtigungen über Ihren Kontostatus und Ihre Kontingentbeschränkungen.
   * Ihre Cloud Foundry-Apps können auf bis zu 256 MB an freiem, sofort verfügbarem Laufzeitspeicher zugreifen.
   * Sie können eine Instanz jedes Service im [{{site.data.keyword.Bluemix_notm}}-Katalog einrichten![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window}, für den ein Lite-Plan besteht.
   * Nach 10 Tagen ohne Entwicklungstätigkeit werden Ihre Apps inaktiviert. Sie können Ihre Apps aktivieren, indem Sie die Arbeit an ihnen fortsetzen.
   * Nach 30 Tagen ohne Entwicklungstätigkeit werden Ihre Serviceinstanzen mit den Lite-Plänen gelöscht.

### Upgrade für Lite-Konto durchführen
{: #upgrade-lite-account}

Sie können ein Upgrade auf ein nutzungsabhängiges Konto oder ein Abonnementkonto durchführen. Weitere Informationen finden Sie in [Wie kann ich ein Upgrade meines Kontotyps durchführen oder den Kontotyp konvertieren?](/docs/account?topic=account-changeacct).

Nach dem Upgrade auf ein Konto mit nutzungsabhängiger Zahlung erhalten Sie eine Werbegutschrift in Höhe von 200 US-Dollar. Dieses Guthaben wird Ihrem Konto automatisch gutgeschrieben. Die Gutschrift von 200 US-Dollar hat eine Gültigkeit von 30 Tagen und wird automatisch mit Ihrer Rechnung verrechnet. Die Gutschrift kann nicht mit Angeboten anderer Anbieter verwendet werden.

## Nutzungsabhängiges Konto
{: #paygo}

Mit einem nutzungsabhängigen Konto können Sie mehrere Ressourcengruppen erstellen, um Kontingente ohne großen Aufwand zu verwalten und um Informationen zu Abrechnung und Nutzung für eine Gruppe von Ressourcen anzuzeigen. Die für Sie anfallenden Gebühren richten Sie nach Ihrer Nutzung von {{site.data.keyword.Bluemix_notm}}-Berechnungen und -Services. Ihnen stehen zusätzliche kostenfreie Laufzeit- und Serviceleistungen zur Verfügung. Wenn Sie in Ihrer Nutzung über die gebührenfreien Leistungen hinausgehen, erhalten Sie eine {{site.data.keyword.Bluemix_notm}}-Rechnung für den Monat. Die Rechnung ist in USD ausgestellt und enthält Detailangaben zu Ihren Ressourcengebühren.

Darüber hinaus können mit einem nutzungsabhängigen Konto optionale Features, wie z. B. Advanced Support oder Premium Support, bestellt werden. Weitere Informationen erhalten Sie vom [{{site.data.keyword.Bluemix_notm}}-Vertrieb ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg).


### Upgrade für nutzungsabhängiges Konto durchführen
{: #upgrade-to-subscription}

Wenn Sie für ein nutzungsabhängiges Konto ein Upgrade auf ein Abonnementkonto durchführen möchten, wenden Sie sich an den [{{site.data.keyword.Bluemix_notm}}-Vertrieb](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link").

## Abonnementkonto
{: #subscription-account}

Mit einem Abonnementkonto können Sie mehrere Ressourcengruppen erstellen, um Kontingente ohne großen Aufwand zu verwalten und um Informationen zu Abrechnung und Nutzung für eine Gruppe von Ressourcen anzuzeigen. Sie verpflichten sich zu einem kombinierten Mindestausgabebetrag pro Monat und erhalten einen Abonnementrabatt, der auf diese Mindestgebühr angewendet wird. Für eine Nutzung, die über die Gesamtsumme des Abonnements hinaus geht, fallen die normalen Gebühren ohne Rabatt an. Zum Anzeigen Ihres Abonnements rufen Sie **Verwalten > Abrechnung und Nutzung** auf und wählen Sie **Abonnements** aus.

Wenn Sie über ein Abonnementkonto verfügen, können Sie die meisten Services erstellen, die im [{{site.data.keyword.Bluemix_notm}}-Katalog](https://cloud.ibm.com/catalog/){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") verfügbar sind. Für einige Services gilt jedoch ein bestimmter Preisstrukturplan, gemäß dem diese Services separat erworben werden müssen.

### {{site.data.keyword.Bluemix_dedicated_notm}}-Konto
Bei {{site.data.keyword.Bluemix_dedicated_notm}} müssen Sie sich für eine Mindestlaufzeit von einem Jahr anmelden.

   * VPN-Anbindung zurück zu Ihrer Infrastruktur
   * Vollständige redundante Umgebung in einem {{site.data.keyword.BluSoftlayer_notm}}-Rechenzentrum
   * Alle unterstützten Laufzeiten ({{site.data.keyword.runtime_liberty_short}}, {{site.data.keyword.runtime_nodejs_short}} sowie integrierte Open-Source-Laufzeiten)
   * Alle dedizierten Services, die Sie ausgewählt haben, und alle öffentlichen {{site.data.keyword.Bluemix_notm}}-Services
   * Standard-{{site.data.keyword.Bluemix_notm}}-Unterstützung

Es können auch optionale Features, wie z. B. {{site.data.keyword.BluDirectLink}}, Advanced Support oder Premium Support, bestellt werden. Weitere Informationen erhalten Sie vom [{{site.data.keyword.Bluemix_notm}}-Vertrieb ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg).

Die monatlichen Kosten während dieser Laufzeit sind von den von Ihnen gewünschten dedizierten Services plus einem Abonnementkonto abhängig, mit dem Sie auf alle öffentlichen Services zugreifen können. Die Nutzungsgebühren der Services in {{site.data.keyword.Bluemix_notm}} Public werden auf der Grundlage Ihrer Abonnementkontovereinbarung berechnet. Sie erhalten für sämtliche Services, die Sie über die Abonnementvereinbarung hinaus nutzen, eine Rechnung. Für Informationen zu Ihrer Vereinbarung wenden Sie sich an Ihren zugewiesenen IBM Kundenbeauftragten oder an den [{{site.data.keyword.Bluemix_notm}}-Vertrieb](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg).
