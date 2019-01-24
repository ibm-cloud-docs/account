---



copyright:

  years: 2017, 2018
lastupdated: "2018-11-19"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Plan ändern
{: #changing}

Sie können den {{site.data.keyword.Bluemix}}-Serviceplan ändern, wenn Planänderungen für den jeweiligen Service aktiviert sind. Der Plan kann beispielsweise geändert werden, um ein Upgrade durchzuführen oder um zu einem Plan mit weniger Features zu wechseln. Der Plan kann über das Dashboard der Serviceinstanz geändert werden.
{: shortdesc}

Sind Sie auf der Suche nach Details zum Upgrade Ihres Kontotyps? Der Abschnitt [Wie kann ich ein Upgrade meines Kontotyps durchführen oder den Kontotyp ändern?](/docs/account/account_faq.html#changeacct) enthält weitere Informationen hierzu.
{: tip}

Das Ändern der Servicepläne ist nur für bestimmte Services möglich. Wenn Planänderungen für den Service aktiviert sind, wird im Serviceinstanzdashboard die Option **Plan** im Navigationsbereich angezeigt. Für jeden Service müssen unterschiedliche weitere Schritte ausgeführt werden, wenn Sie Ihren Plan ändern.

1. Klicken Sie im Dashboard der Serviceinstanz auf **Plan**. Normalerweise können Sie ein Upgrade oder eine Herabstufung für Ihren Plan vornehmen.
2. Nach dem Ändern des Plans müssen Sie zusätzliche Schritte ausführen. Die Schritte variieren abhängig von der Art der Planänderung und vom Service. Wenn Sie beispielsweise Ihren Plan reduziert haben, müssen Sie möglicherweise ein erneutes Staging für Ihre App durchführen. Oder wenn Sie für Ihren Plan ein Upgrade durchgeführt haben, müssen Sie möglicherweise ein erneutes Staging für Ihre App und weitere Aktionen durchführen.

Für ein erneutes Staging Ihrer App rufen Sie die Ressourcenliste auf und suchen Sie nach der App, an die der Service gebunden ist. Klicken Sie auf das Menüsymbol ![Menüsymbol](../icons/icon_hamburger.svg) ** und dann auf Ressourcenliste**. Wählen Sie im Menü 'App' die Option **Anwendung erneut starten** aus.

Die weiteren Aktionen des nächsten Schritts hängen vom Service ab. In der folgenden Tabelle sind bestimmte Aktionen aufgeführt.

|Service |	Informationen|
|--------|-------------|
|Presence Insights 	|Wenn Sie einen Lite-Plan verwenden und das kostenfreie Kontingent überschreiten, wird die Nachricht 403 angezeigt oder protokolliert, um anzugeben, dass Sie nicht mehr über die entsprechende Berechtigung verfügen und dass Ihre Serviceinstanz inaktiviert ist. Darüber hinaus werden POST-Aufrufe der REST-API mit der Antwort 403 zurückgewiesen. <br/><br/>Wenn der Service inaktiviert wurde, weil Sie das kostenfreie Kontingent überschritten haben, können Sie ein Upgrade von einem Lite-Plan auf einen kostenpflichtigen Plan durchführen. Ihr Service wird innerhalb von zwei Stunden erneut aktiviert.<br/><br/>Wenn Sie einen kostenpflichtigen Plan verwenden, können Sie eine Herabstufung auf einen Lite-Plan durchführen, vorausgesetzt, Ihre Nutzungsrate für Ereignisse und Gesamtspeicher bleibt innerhalb des Lite-Kontingents für diese Posten.<br/><br/>Wenn Sie ein Upgrade oder eine Herabstufung des Plans vornehmen, müssen Sie kein erneutes Staging und keinen Neustart für Ihre Apps durchführen.|
{:caption="Tabelle 1. Nächste Schritte zur Änderung eines Plans" caption-side="top"}


## Plan über die Befehlszeilenschnittstelle ändern
{: #changing_command_line}

Optional können Sie den Serviceplan auch über die Befehlszeilenschnittstelle ändern, indem Sie den folgenden Befehl eingeben:

```
cf update-service <Servicename> [-p <neuer Plan>]
```
