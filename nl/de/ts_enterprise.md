---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-18"

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

## Warum kann ich dem Unternehmen kein bestehendes Konto hinzufügen?
{: #troubleshoot-existing-enterprise}
{: troubleshoot}

Wenn Sie versuchen, ein bestehendes Konto zum Unternehmen hinzuzufügen, tritt eines der folgenden Probleme auf:
{: tsSymptoms}
* Wenn Sie im Abschnitt "Konto" auf **Vorhandenes Konto hinzufügen** klicken, wird das Konto, das Sie hinzufügen möchten, nicht aufgelistet.
* Sie haben nicht die Möglichkeit, auf **Vorhandenes Konto hinzufügen** zu klicken.

Ihnen wurden nicht die richtigen Zugriffsrechte zugewiesen.
{: tsCauses}

Wenn Sie das vorhandene Konto, das als Option aufgelistet ist, nicht sehen können, benötigen Sie die Administratorrolle für den Abrechnungsservice des vorhandenen Kontos.
{: tsResolve}

Wenn Sie dem Unternehmen ein vorhandenes Konto hinzufügen möchten, benötigen Sie die Rolle "Administrator" oder "Bearbeiter" für den Abrechnungsservice des Unternehmens sowie die Rolle "Administrator" oder "Bearbeiter" für den Unternehmensservice für das übergeordnete Unternehmen oder die Kontogruppe.

## Warum kann ich kein neues Konto im Unternehmen erstellen?
{: #troubleshoot-add-enterprise}
{: troubleshoot}

Sie können im Abschnitt "Konto" nicht auf **Konto hinzufügen** klicken.
{: tsSymptoms}

Ihnen wurden nicht die richtigen Zugriffsrechte zugewiesen.
{: tsCauses}

Um ein Konto im Unternehmen erstellen zu können, müssen Sie über den folgenden Zugriff verfügen.
{: tsResolve}
1. Rolle "Administrator" für den Abrechnungsservice des Unternehmens.
2. Rolle "Administrator" oder "Bearbeiter" für den Unternehmensservice für das betreffende übergeordnete Unternehmen oder die Kontogruppe.

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

Von einem untergeordneten Konto im Unternehmen können keine Abonnementcodes angewendet werden. Abonnementcodes müssen auf Unternehmensebene angewendet werden.
{: tsCauses}

Bitten Sie den Eigner oder Administrator des Unternehmens, den Abonnementcode hinzuzufügen. Wenn der Abonnementcode hinzugefügt wird, gilt er für alle Konten im Unternehmen. Weitere Informationen finden Sie in [Abonnements verwalten](/docs/billing-usage?topic=billing-usage-subscriptions).
{: tsResolve}
