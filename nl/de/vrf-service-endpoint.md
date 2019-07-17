---

copyright:
  years: 2019
lastupdated: "2019-07-01"

keywords: VRF, virtual routing and forwarding, service endpoint, private network

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# VRF und Serviceendpunkte aktivieren
{: #vrf-service-endpoint}

Standardmäßig werden Verbindungen zu den Ressourcen in Ihrem Konto über das öffentliche Netz von {{site.data.keyword.Bluemix}} hergestellt. Durch das Aktivieren von VRF (Virtual Routing and Forwarding) können Sie das IP-Routing für Ihr Konto und alle zugehörigen Ressourcen in eine separate Routing-Tabelle verlagern. Wenn VRF aktiviert ist, können Sie {{site.data.keyword.Bluemix_notm}}-Serviceendpunkte aktivieren, um direkte Verbindungen zu Ressourcen herzustellen, ohne das öffentliche Netz zu verwenden.
{:shortdesc}

Für die Aktivierung von VRF und {{site.data.keyword.Bluemix_notm}}-Serviceendpunkten benötigen Sie ein Abrechnungskonto. 

## VRF aktivieren
{: #vrf}

Mit VRF können mehrere Instanzen einer Routing-Tabelle in einem Router vorhanden sein und gleichzeitig ausgeführt werden. Wenn Sie VRF aktivieren, wird eine separate Routing-Tabelle für Ihr Konto erstellt und die Verbindungen zu und von den Ressourcen Ihres Kontos werden separat im {{site.data.keyword.Bluemix_notm}}-Netz weitergeleitet. VRF wird auf der Kontoebene aktiviert, sodass alle Ressourcen von dieser Netzänderung betroffen sind. Weitere Informationen zur VRF-Technologie und deren Auswirkungen auf das Netzrouting in Ihrem Konto finden Sie in [Virtual Routing and Forwarding (VRF) in {{site.data.keyword.Bluemix_notm}}](/docs/resources?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud).

Das Aktivieren von VRF ändert den Netzbetrieb für Ihr Konto permanent. Stellen Sie sicher, dass Ihnen die Auswirkungen auf Ihr Konto und die Ressourcen bekannt sind. Nach dem Aktivieren von VRF ist keine Inaktivierung möglich.
{: important}

Erstellen Sie zum Aktivieren von VRF einen Supportfall mit Ihrer Anforderung. 

1. Rufen Sie in der Konsole die Option **Support** auf und klicken Sie auf **Fall erstellen**. 
1. Wählen Sie **Konto und Zugriff** als Unterstützungstyp aus. 
1. Geben Sie im Feld **Subjekt** `Frage zum privaten Netz` ein. 
1. Geben Sie im Feld **Beschreibung** die folgende Nachricht ein und ersetzen Sie dabei _Kontonummer eingeben_ durch Ihre {{site.data.keyword.Bluemix_notm}}-Kontonummer. 

   `Das Konto *Kontonummer eingeben* soll in ein eigenes VRF verschoben werden. Die Risiken sind bekannt und der Änderung wird zugestimmt. Bitte teilen Sie uns das bzw. die geplante(n) Zeitfenster mit, in dem/denen diese Änderung vorgenommen wird, damit die Migration entsprechend vorbereitet werden kann. `

Das {{site.data.keyword.Bluemix_notm}}-Netzentwicklerteam setzt sich mit dem Eigner des Falls in Verbindung, um einen Zeitraum zu planen, in dem der Netzbetrieb Ihres Kontos in VRF konvertiert wird. Während des Konvertierungsprozesses können Verbindungen zu Ressourcen in Ihrem Konto aufgrund von Paketverlusten instabil werden. Die Konvertierung nimmt etwa 15 bis 30 Minuten in Anspruch, abhängig von der Komplexität des Kontos. Wenn in Ihrem Konto traditionelle {{site.data.keyword.BluDirectLink}}-Verbindungen vorhanden sind, ist möglicherweise mehr Zeit erforderlich. 


## Serviceendpunkte aktivieren
{: #service-endpoint}

Wenn {{site.data.keyword.Bluemix_notm}}-Serviceendpunkte in Ihrem Konto aktiviert sind, können Sie beim Erstellen einer Ressource festlegen, dass ein Endpunkt des privaten Netzes zugänglich gemacht wird. Es ist dann möglich, eine direkte Verbindung zu diesem Endpunkt über das private {{site.data.keyword.Bluemix_notm}}-Netz herzustellen, nicht über das öffentliche Netz. Da Ressourcen, die Endpunkte des privaten Netzes verwenden, nicht über Internet-Routing-fähige IP-Adressen verfügen, sind Verbindungen zu diesen Ressourcen sicherer. Weitere Informationen finden Sie in [Serviceendpunkte für private Netzverbindungen](/docs/resources?topic=resources-service-endpoints).

Bevor Sie Serviceendpunkte aktivieren können, muss VRF für Ihr Konto aktiviert sein.
{: note}

Für die Aktivierung von Serviceendpunkten über die Befehlszeilenschnittstelle benötigen Sie Version 0.13 oder eine höhere Version der [{{site.data.keyword.Bluemix_notm}}-Befehlszeilenschnittstelle](/docs/cli?topic=cloud-cli-getting-started). 

1.  Überprüfen Sie, ob Serviceendpunkten in Ihrem Konto bereits aktiviert sind.

    ```
    ibmcloud account show
    ```
    {: codeblock}

    Wenn für `Serviceendpunkt aktiviert` die Einstellung `false` festgelegt ist, wie im folgenden Beispiel dargestellt, sind keine Serviceendpunkte aktiviert. 

    ```
    Abrufen des Kontos Mia Example's Account of m.example@example.com...
    OK

    Konto-ID:                     abc123d0bc2edefthyufffc9b5ca318   
    Aktuell vorgesehenes Konto:   true   
    Verknüpftes-SoftLayer-Konto:  0123456   
    Serviceendpunkt aktiviert:    false  
    ```
    {: screen}
1. Aktivieren Sie Serviceendpunkte, indem Sie den folgenden Befehl ausführen. 

   ```
   ibmcloud account update --service-endpoint-enable true
   ```
   {: codeblock}

   Es kann einige Minuten dauern, bis diese Änderung wirksam wird. Nach dem Abschluss des Befehls können Sie den Befehl `ibmcloud account show` zur Verifizierung erneut ausführen. 

    Wenn VRF für Ihr Konto nicht aktiviert ist, bewirkt die Ausführung dieses Befehls, dass Sie dazu aufgefordert werden, einen Supportfall zu erstellen, um VRF zu aktivieren. Geben Sie `y` ein, um den Supportfall zu erstellen. Führen Sie nach der Aktivierung von VRF für das Konto den Befehl erneut aus, um die Serviceendpunktkonnektivität im Konto zu aktivieren. 

    ```
    Der Serviceendpunkt ist im verknüpften SoftLayer-Konto 1008967 nicht verfügbar.
    Zuerst VRF (Virtual Routing and Forwarding) aktivieren, um den Vorgang fortzusetzen.
    Weitere Informationen zu VRF finden Sie hier: https://cloud.ibm.com/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html.

    Möchten Sie ein Ticket öffnen, um diese Funktion zu aktivieren? y/N]> y
    Ticket 70729615 wurde erfolgreich geöffnet. Rufen Sie den Link https://control.softlayer.com/support/tickets/70729876 auf, um die Details zu überprüfen und den Status des Tickets zu verfolgen. Sie müssen sich anmelden, um dieses Ticket anzuzeigen.
    Konto-ID:      1008967
    Ticket:        Frage zum privaten Netz
    ```
    {: screen}


Nach dem Aktivieren der Serviceendpunkte können Sie Ressourcen erstellen, für die Verbindungen über das private {{site.data.keyword.Bluemix_notm}}-Netz hergestellt werden. Eine Liste der Services, die Serviceendpunkte unterstützen, sowie weitere Informationen finden Sie in [Endpunkte für private Netze einrichten](/docs/resources?topic=resources-private-network-endpoints). 
