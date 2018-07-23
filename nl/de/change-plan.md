---



copyright:

  years: 2017, 2018
lastupdated: "2018-07-17"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Plan ändern
{: #changing}

Sie können Ihren Serviceplan im Serviceinstanzdashboard von {{site.data.keyword.Bluemix}} ändern, falls diese Funktion für den betreffenden Service aktiviert ist.
{: shortdesc}

Im Abschnitt [Wie führe ich ein Upgrade meines Kontotyps durch oder wie ändere ich meinen Kontotyp?](/docs/account/account_faq.html#changeacct) finden Sie detaillierte Informationen zur Durchführung eines Upgrades für Ihren Kontotyp.
{: tip}

Nur bestimmte Services ermöglichen Ihnen das Ändern des Serviceplans. Wenn Planänderungen für den Service aktiviert sind, wird im Serviceinstanzdashboard die Option **Plan** im Navigationsbereich angezeigt. Für jeden Service müssen unterschiedliche weitere Schritte ausgeführt werden, wenn Sie Ihren Plan ändern.

1. Klicken Sie zum Ändern Ihres Plans im Serviceinstanzdashboard auf **Plan**. Normalerweise können Sie ein Upgrade oder eine Herabstufung für Ihren Plan vornehmen.
2. Nach dem Ändern des Plans müssen Sie eine Reihe weiterer Schritte ausführen. Die Schritte variieren abhängig von der Art der Planänderung und vom Service. Wenn Sie beispielsweise Ihren Plan reduziert haben, müssen Sie möglicherweise ein erneutes Staging für Ihre App durchführen. Oder wenn Sie für Ihren Plan ein Upgrade durchgeführt haben, müssen Sie möglicherweise ein erneutes Staging für Ihre App und weitere Aktionen durchführen.<br/><br/>Für ein erneutes Staging Ihrer App rufen Sie das {{site.data.keyword.Bluemix_notm}}-Dashboard auf und suchen Sie nach der App, an die der Service gebunden ist. Wählen Sie im Menü 'App' die Option **Anwendung erneut starten** aus.<br/><br/>Die weiteren Aktionen des nächsten Schritts hängen vom Service ab. In der folgenden Tabelle sind bestimmte Aktionen aufgeführt.

|Service |	Informationen|
|--------|-------------|
|Presence Insights 	|Wenn Sie einen Lite-Plan verwenden und das kostenfreie Kontingent überschreiten, wird die Nachricht 403 angezeigt oder protokolliert, um anzugeben, dass Sie nicht mehr über die entsprechende Berechtigung verfügen und dass Ihre Serviceinstanz inaktiviert ist. Außerdem werden POST-Aufrufe der REST-API mit der Antwort 403 zurückgewiesen.<br/><br/>Wenn der Service inaktiviert wurde, weil Sie das kostenfreie Kontingent überschritten haben, können Sie ein Upgrade von einem Lite-Plan auf einen Paid-Plan durchführen. Ihr Service wird innerhalb von zwei Stunden erneut aktiviert.<br/><br/>Wenn Sie einen Paid-Plan verwenden, können Sie eine Herabstufung auf einen Lite-Plan durchführen, vorausgesetzt, Ihre Nutzungsrate für Ereignisse und Gesamtspeicher bleibt innerhalb des Lite-Kontingents für diese Posten.<br/><br/>Wenn Sie ein Upgrade oder eine Herabstufung des Plans vornehmen, müssen Sie kein erneutes Staging und keinen Neustart für Ihre Apps durchführen.|
{:caption="Tabelle 1. Nächste Schritte zur Änderung eines Plans" caption-side="top"}

## Plan über die Befehlszeilenschnittstelle ändern
{: #changing_command_line}

Optional können Sie den Serviceplan auch über die Befehlszeilenschnittstelle ändern, indem Sie den folgenden Befehl eingeben:
```
cf update-service <Servicename> [-p <neuer Plan>]
```
