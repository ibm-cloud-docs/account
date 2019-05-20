---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-10"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account, subscription, service bundle

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
   * Ihre Cloud Foundry-Apps können auf bis zu 256 MB an freiem, sofort verfügbarem Laufzeitspeicher pro Monat zugreifen.
   * Sie können eine Instanz jedes Service im [{{site.data.keyword.Bluemix_notm}}-Katalog einrichten![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window}, für den ein Lite-Plan besteht.
   * Nach 10 Tagen ohne Entwicklungstätigkeit werden Ihre Apps inaktiviert. Sie können Ihre Apps aktivieren, indem Sie die Arbeit an ihnen fortsetzen.
   * Nach 30 Tagen ohne Entwicklungstätigkeit werden Ihre Serviceinstanzen mit den Lite-Plänen gelöscht.

## Nutzungsabhängiges Konto
{: #paygo}

Mit einem nutzungsabhängigen Konto verfügen Sie über Zugriff auf den gesamten {{site.data.keyword.Bluemix_notm}}-Katalog, einschließlich aller kostenfreien Pläne, und Sie erhalten mit 512 MB pro Monat die doppelte Menge an freiem Laufzeitspeicher. Gebühren fallen nur für die von Ihnen genutzten abrechnungsfähigen Services an, ohne langfristige Verträge oder Verpflichtungen.

Sie können mehrere Ressourcengruppen erstellen, um Kontingente ohne großen Aufwand zu verwalten und um Informationen zu Abrechnung und Nutzung für eine Gruppe von Ressourcen anzuzeigen. Die für Sie anfallenden Gebühren richten Sie nach Ihrer Nutzung von {{site.data.keyword.Bluemix_notm}}-Berechnungen und -Services. Wenn die Nutzung das kostenfreie Laufzeit- und Servicekontingent überschreitet, erhalten Sie eine monatliche Rechnung, die Details zu den Ressourcengebühren enthält.

Darüber hinaus können Sie mit einem nutzungsabhängigen Konto Advanced oder Premium Support-Pläne bestellen, um zusätzliche Unterstützung für Ihre Produktionsworkloads zu erhalten. Weitere Informationen finden Sie in [Support-Pläne](/docs/get-support?topic=get-support-support-plans).

## Abonnementkonto
{: #subscription-account}

Mit einem Abonnementkonto können Sie mehrere Ressourcengruppen erstellen, um Kontingente ohne großen Aufwand zu verwalten und um Informationen zu Abrechnung und Nutzung für eine Gruppe von Ressourcen anzuzeigen. Sie verpflichten sich zu einem Mindestausgabebetrag pro Monat und erhalten einen Abonnementrabatt, der auf diese Mindestgebühr angewendet wird.

Beispiel: Wenn Sie sich zu einem Ausgabebetrag von $ 100 pro Monat für einen Zeitraum von 6 Monaten verpflichten, können Sie einen Rabatt von 10 % erhalten. Während der Abonnementlaufzeit fallen Nutzungsgebühren von $ 600 an, Sie bezahlen jedoch nur $ 540 dafür. Je länger die Abonnementlaufzeit, desto höher der Rabatt.

Ihre Nutzung wird von der Gesamtmenge des Abonnements subtrahiert. Selbst wenn die Nutzung von Monat zu Monat variiert, bleibt die Abrechnung vorhersehbar und konsistent. Wenn die Nutzung die Gesamtmenge des Abonnements überschreitet, fallen für die Überschreitung die regulären Gebühren ohne Rabatt an.

Wie die nutzungsabhängigen Konten ermöglicht Ihnen auch das Abonnementkonto, Advanced oder Premium Support-Pläne zu bestellen, um bei Bedarf zusätzliche Unterstützung zu erhalten. Weitere Informationen finden Sie in [Support-Pläne](/docs/get-support?topic=get-support-support-plans).

Wenn Sie über ein Abonnementkonto verfügen, können Sie die meisten Services erstellen, die im [{{site.data.keyword.Bluemix_notm}}-Katalog](https://{DomainName}/catalog){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link") verfügbar sind. Für einige Services gilt jedoch ein bestimmter Preisstrukturplan, gemäß dem diese Services separat erworben werden müssen.

### Serviceabonnementpakete
{: #service-subscriptions}

Serviceabonnementpakete bieten Zugriff und Gutschriften für eine Gruppe von Services innerhalb einer bestimmten Domäne, die für gängige Anwendungsfälle verwendet werden. Sie können Servicepakete aus den Bereichen AI, Analytics, {{site.data.keyword.blockchainfull_notm}}, Internet of Things (IoT) und Cloud-native Services auswählen. Falls die gegebenen Anforderungen mehrere Domänen betreffen, können Sie mehrere Serviceabonnementpakete erwerben.

Sie können Servicepakete zu jedem vorhandenen Kontotyp hinzufügen, auch zu Lite-Konten. In den ersten 90 Tagen ist die Nutzung auf Services innerhalb des Pakets begrenzt. Nach den ersten 90 Tagen verfügen Sie über Zugriff auf den gesamten Katalog. Serviceabonnementpakete unterliegen den Bedingungen der [{{site.data.keyword.Bluemix_notm}}-Servicebeschreibung](/docs/overview/terms-of-use?topic=overview-terms).

Serviceabonnementpakete sind nicht über die {{site.data.keyword.Bluemix_notm}}-Konsole verfügbar. Wenden Sie sich an den [{{site.data.keyword.Bluemix_notm}}-Vertrieb ![Symbol für externen Link](../icons/launch-glyph.svg "Symbol für externen Link")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}, wenn Sie weitere Informationen benötigen oder ein Servicepaket erwerben möchten.
{:tip}

Nach dem Kauf eines Serviceabonnementpakets erhalten Sie eine E-Mail mit einem Feature-Code, den Sie anwenden, um das Paket zu Ihrem Konto hinzuzufügen. Weitere Informationen zum Anwenden von Feature-Codes finden Sie in [Feature-Codes anwenden](/docs/account?topic=account-codes). Wenn das Servicepaket abläuft oder die Gutschrift verbraucht ist, können Sie die Services weiter nutzen, wobei die nutzungsabhängigen Gebühren berechnet werden.

## Upgrade für Konto durchführen
{: #upgrade-lite-account}

Wenn Sie Ihr Konto erweitern möchten, können Sie ein [Upgrade für ein Lite-Konto](/docs/account?topic=account-upgrading-account) auf ein nutzungsabhängiges Konto oder ein Abonnementkonto durchführen. Ein Upgrade für Ihr Konto bietet Ihnen die gesamte Palette des {{site.data.keyword.Bluemix_notm}}-Katalogs, zusätzliche freie Ressourcen und mehr.

Nach einem Upgrade des Lite-Kontos auf ein nutzungsabhängiges Konto erhalten Sie eine Werbegutschrift von $ 200, die automatisch für Ihr Konto angewendet wird. Die Gutschrift von $ 200 ist für einen Zeitraum von 30 Tagen gültig und die Nutzung wird automatisch vom Gutschriftsbetrag subtrahiert. Die Gutschrift kann nicht mit Angeboten anderer Anbieter verwendet werden und ist möglicherweise nicht für alle Konten verfügbar.

Wenn Sie bereits über ein nutzungsabhängiges Konto oder ein Abonnementkonto verfügen, können Sie das Konto auch in einen anderen Kontotyp konvertieren. Weitere Informationen finden Sie in [Upgrade für Konto durchführen](/docs/account?topic=account-upgrading-account).
