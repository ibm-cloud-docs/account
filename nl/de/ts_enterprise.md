---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: troubleshoot enterprise, enterprise problem, account problem, enterprise support, enterprise help, error message

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

# Fehlerbehebung bei einem Unternehmen
{: #enterprise_help}

Zu den allgemeinen Problemstellungen bei der Verwaltung Ihres Unternehmens gehören auch Probleme, die auftreten, wenn Sie versuchen, Abonnementcodes oder Feature-Codes anzuwenden, oder wenn Sie versuchen, dem Unternehmen ein Konto hinzuzufügen. In vielen Fällen können Sie diese Probleme durch Ausführen weniger einfacher Schritte beheben.

## Warum kann ich nicht das gesamte Unternehmen anzeigen?
{: #troubleshoot-view-enterprise}
{: troubleshoot}

Wenn Sie nicht das gesamte Unternehmen anzeigen können, müssen Sie möglicherweise prüfen, welcher Zugriff Ihnen zugewiesen wurde.

Sie können einen Teil der Konten im Unternehmen sehen, aber nicht die gesamte Unternehmenshierarchie. In der Kontenhierarchie werden nur die Konten angezeigt, auf die Sie Zugriff haben, nicht das gesamte Unternehmenskonto.
{: tsSymptoms}

Sie haben nur auf bestimmte Konten im Unternehmen Zugriff.
{: tsCauses}

Führen Sie die folgenden Schritte aus, um zu prüfen, über welchen Zugriff Sie verfügen:
{: tsResolve}

1. Rufen Sie **Verwalten** &gt; **Zugriff (IAM)** > **Benutzer** auf.
2. Wählen Sie Ihren Namen aus.
2. Klicken Sie auf die Registerkarte **Zugriffsrichtlinien**.

Wenden Sie sich an den Unternehmenseigner, um den korrekten Zugriff anzufordern.

Wenn Sie der Eigner des Unternehmens sind, führen Sie die folgenden Schritte aus, wenn Sie einem Benutzer Zugriff auf das gesamte Unternehmen erteilen wollen:
1. Rufen Sie **Verwalten** > **Zugriff (IAM)** > **Benutzer** auf.
2. Wählen Sie den Namen des Benutzers aus.
2. Klicken Sie auf die Registerkarte **Zugriffsrichtlinien** > **Zugriff zuweisen** > **Zugriff auf Kontoverwaltungsservices zuweisen**.
3. Wählen Sie **Unternehmen** als Service aus und wählen Sie den Namen Ihres Unternehmens aus.
4. Wählen Sie die Kontogruppe oder das Konto im Unternehmen aus, auf das Sie dem Benutzer Zugriff geben möchten. Wenn Sie beispielsweise möchten, dass ein Benutzer Zugriff auf nur ein bestimmtes Konto erhalten soll, wählen Sie das Konto aus und weisen Sie dem Benutzer die Rolle "Anzeigeberechtigter" (oder höher) zu. Wenn Sie einen Benutzer berechtigen möchten, das gesamte Unternehmen anzuzeigen, lassen Sie die Kontogruppe und die Kontoauswahl leer und weisen Sie den Zugriff zu.

## Warum kann ich ein vorhandenes Konto nicht in das Unternehmen importieren?
{: #troubleshoot-existing-enterprise}
{: troubleshoot}

Wenn Sie versuchen, ein vorhandenes Konto in das Unternehmen zu importieren, tritt eines der folgenden Probleme auf:
{: tsSymptoms}
* Wenn Sie im Abschnitt "Konto" auf **Vorhandenes Konto hinzufügen** klicken, wird das Konto, das Sie hinzufügen möchten, nicht aufgelistet.
* Sie haben nicht die Möglichkeit, auf **Konto importieren** zu klicken.

Ihnen wurden nicht die korrekten Zugriffsberechtigungen zugewiesen oder das Konto kommt für einen Import nicht infrage.
{: tsCauses}

Wenn das vorhandene Konto, das importiert werden soll, nicht angezeigt wird, benötigen Sie die Administratorrolle für den Abrechnungsservice des vorhandenen Kontos.
{: tsResolve}

Wenn die Option **Konto importieren** nicht verfügbar ist, vergewissern Sie sich, dass Sie über die Rolle eines Administrators oder eines Bearbeiters für den Abrechnungsservice des Unternehmens und über die Rolle eines Administrators oder eines Bearbeiters für den Unternehmensservice des übergeordneten Unternehmens bzw. der übergeordneten Kontogruppe verfügen. 

Wenn es sich bei dem zu importierenden Konto um eine nutzungsabhängiges Konto handelt und sie es nicht importieren können, obwohl Sie über die erforderlichen Zugriffsberechtigungen verfügen, kommt das Konto möglicherweise nicht für den Import in das Unternehmen infrage. Einige nutzungsabhängige Konten können nicht direkt in ein Unternehmen importiert werden, wie z. B. zahlreiche nutzungsabhängige Konten, deren Abrechnung in US-Dollar (USD) erfolgt. Wenden Sie sich an den [{{site.data.keyword.Bluemix_notm}}-Vertrieb ](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Symbol für externen Link](../icons/launch-glyph.svg), um das Konto in ein Abonnementkonto zu konvertieren, und importieren Sie es dann in das Unternehmen. 

## Warum kann ich kein neues Konto im Unternehmen erstellen?
{: #troubleshoot-add-enterprise}
{: troubleshoot}

Sie können im Abschnitt "Konto" nicht auf **Konto hinzufügen** klicken.
{: tsSymptoms}

Ihnen wurden nicht die richtigen Zugriffsrechte zugewiesen.
{: tsCauses}

Um ein Konto im Unternehmen erstellen zu können, müssen Sie über die folgenden Zugriffsberechtigungen verfügen.
{: tsResolve}
1. Administratorrolle für den Abrechnungsservice des Unternehmens.
2. Administrator- oder Bearbeiterrolle für den Unternehmensservice für das betreffende übergeordnete Unternehmen oder die übergeordnete Kontogruppe.

## Warum kann ich die Unternehmensabonnements nicht sehen?
{: #troubleshoot-viewsub-enterprise}
{: troubleshoot}

Wenn Sie die Seite "Abonnements" von einem untergeordneten Konto anzeigen möchten, wird die folgende Nachricht angezeigt:
{: tsSymptoms}

`Sie verfügen offenbar nicht über die Berechtigung zum Anzeigen der Abonnementdaten für dieses Konto. Wenden Sie sich an den Kontoeigner oder Administrator, um Zugriff anzufordern.`

Die folgende Nachricht wird im Abschnitt "Abrechnung" im Dashboard für das Unternehmen angezeigt:

`Sie verfügen offenbar nicht über die Berechtigung zum Anzeigen dieser Informationen. Weitere Informationen zum IAM-Zugriff aufrufen.`

Der Zugriff auf Abrechnungs- und Zahlungsinformationen für zukünftige Abrechnungszeiträume ist auf die Benutzer im Unternehmenskonto beschränkt. Benutzer in einem untergeordneten Konto können nicht auf Abrechnungs- und Zahlungsinformationen zugreifen (wie z. B. Abonnements), selbst wenn sie zuvor Zugriff auf das Konto hatten.
{: tsCauses}

Um die Abrechnung anzuzeigen oder zu verwalten, müssen Sie für das Unternehmenskonto eingeladen werden und Zugriff auf den Abrechnungsservice in diesem Konto erhalten. Wenden Sie sich an den Kontoeigner, um den Zugriff anzufordern.
{: tsResolve}

## Warum kann ich einen Abonnementcode nicht auf mein Konto anwenden?  
{: #troubleshoot-promo-enterprise}
{: troubleshoot}

Sie können Ihrem Konto keinen Abonnementcode hinzufügen, da Sie nicht über den richtigen Zugriff verfügen.  
{: tsSymptoms}

Da es sich bei Ihrem Konto um ein untergeordnetes Konto des Unternehmens handelt, können Sie keine Abonnementcodes anwenden. Abonnementcodes müssen auf Unternehmensebene angewendet werden.
{: tsCauses}

Bitten Sie den Eigner oder Administrator des Unternehmens, den Abonnementcode hinzuzufügen. Wenn der Abonnementcode hinzugefügt wird, gilt er für alle Konten im Unternehmen. Weitere Informationen finden Sie in [Abonnements verwalten](/docs/billing-usage?topic=billing-usage-subscriptions).
{: tsResolve}
