---



copyright:

  years: 2016, 2018
lastupdated: "2017-10-13"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}}-Standardkonto (begrenztes Release)
{: #betaintro}

Mit dem {{site.data.keyword.Bluemix}}-Standardkonto (begrenztes Release) wird ein neues kostenfreies Konto eingeführt, das die Möglichkeit bietet, in {{site.data.keyword.Bluemix_notm}} Public zu arbeiten. Für ein Standardkonto gilt kein Ablaufdatum, im Gegensatz zum {{site.data.keyword.Bluemix_notm}}-Testkonto mit einer Gültigkeit von 30 Tagen. Sie können die Arbeit mit den {{site.data.keyword.Bluemix_notm}}-Anwendungen fortsetzen, ohne sich um Zeitbegrenzungen zu kümmern. 
{:shortdesc}

Für Benutzer in den Regionen 'Vereintes Königreich' und 'USA (Süden)' steht ein Standardkonto zur Verfügung. Wenn Sie sich nicht in einer dieser Regionen befinden, können Sie dennoch ein Standardkonto erstellen, indem Sie einen Freund um eine Einladung bitten oder indem Sie sich unter CloudDigitalSales@us.ibm.com an das Vertriebsteam wenden. Wenn Sie über ein Standardkonto verfügen, können Sie Freunde und Kollegen einladen, sodass auch sie teilnehmen können.  

## {{site.data.keyword.Bluemix_notm}}-Standardkonto - Einführung
{: #standardaccount}

Sicher interessiert es Sie, welche Unterschiede zwischen einem Standardkonto und einem Testkonto bestehen. Die folgende Tabelle enthält eine Zusammenfassung der wichtigen Details zu einem {{site.data.keyword.Bluemix_notm}}-Standardkonto. 

|Neuerungen bei einem Standardkonto |    
|-----------------|
| Für das Konto existiert kein Ablaufdatum. |
| Cloud Foundry-Anwendungen können auf bis zu 256 MB an freiem, sofort verfügbarem Laufzeitspeicher zugreifen. |
| Sie können auf kostenfreie Lite-Pläne für gefragte Watson-Services wie Conversation, Internet of Things Platform und Cloudant NoSQLDB zugreifen. Weitere Informationen finden Sie unter [Merkmale und Leistungen](/docs/pricing/standard_account.html#whatsavailable). |
| Ihre Anwendungen werden in den Ruhemodus versetzt, falls über einen Zeitraum von 10 Tagen keine Entwicklungsaktivität stattfindet. |
| Ihre Serviceinstanzen werden nach einem Inaktivitätszeitraum von 30 Tagen gelöscht. |
{:caption="Tabelle 1. Neuerungen in einem Standardkonto" caption-side="top"}

|Was bleibt nach dem Konvertieren eines Testkontos unverändert? | 
|-----------------|
|Das Konto ist kostenfrei - Sie benötigen keine Kreditkarte. |
|Sie können weiterhin die Instanzen Ihres Lite-Plans verwenden. |
|Die Organisation, Bereiche und zugehörige Zugriffseinstellungen für Teammitglieder bleiben unverändert. Eine Organisation kann an das neue Konto übertragen werden. |
|Die {{site.data.keyword.Bluemix_notm}}-Support-Stufe bleibt unverändert. |
{:caption="Tabelle 2. Was bleibt unverändert?" caption-side="top"}

**Hinweis**: Wenn Ihr Testkonto nicht konvertiert werden kann, erhalten Sie eine Nachricht mit einer Erläuterung zur Ursache. Möglicherweise enthält das bestehende Testkonto mehr als eine Organisation oder Apps, die nicht übertragen werden können. Sie können die entsprechende Maßnahme ausführen und dann die Konvertierung des Kontos erneut versuchen.

Wenn Sie über ein Standardkonto verfügen, können Sie Teammitglieder zur Zusammenarbeit in Ihrer Organisation und den zugehörigen Bereichen einladen, Ihre Nutzungsinformationen anzeigen, Bereiche erstellen, Ihr Kontoprofil aktualisieren und Ihre Organisation verwalten.

## Lite-Pläne
{: #liteplans}
   
Lite-Pläne, die auch in einem nutzungsabhängigen Konto verfügbar sind, sind mit kostenfreien Kontingenten strukturiert. Sie können an Ihren Projekten arbeiten, ohne sich darüber Gedanken zu machen, versehentlich Kosten zu generieren. Das Kontingent kann über einen bestimmten Zeitraum hinweg gültig sein, z . B. für einen Monat, oder auf einer Einzelnutzungsbasis. Beispiele für Kontingente im Rahmen eines Lite-Plans:

<ul>
<li>Maximale Anzahl registrierter Geräte.</li>
<li>Maximale Anzahl von Anwendungsbindungen.</li>
<li>Grenzwert für den verschlüsselten Datenspeicher, z. B. 1 GB.</li>
<li>Bereitgestellte Durchsatzkapazität.</li>
</ul> 

In einem Standardkonto können Sie alle Angebote des {{site.data.keyword.Bluemix_notm}}-Katalogs nutzen, für die ein Lite-Plan vorgesehen ist. Lite-Pläne sind einfach zu finden. Beim Aufrufen des Katalogs werden standardmäßig alle Services mit einem Lite-Plan angezeigt und mit einem Lite-Tag ![Lite-Tag](../icons/Lite.svg) gekennzeichnet. Wählen Sie einen Service aus, um die Kontingentdetails für den zugehörigen Lite-Plan anzuzeigen.

## Was ist mit einem Standardkonto verfügbar?
{: #whatsavailable}

Mit einem Standardkonto können Ihre Cloud Foundry-Apps auf maximal 256 MB sofort verfügbaren Laufzeitspeicher zugreifen. Wenn das zugeordnete Kontingent überschritten wird, können Sie einige der Apps stoppen, um Laufzeitspeicher freizugeben. Sie haben auch die Möglichkeit, mit einem Kubernetes-Cluster mit 2 CPUs und 4 GB RAM arbeiten. 

Sie können alle Services im {{site.data.keyword.Bluemix_notm}}-Katalog nutzen, für die ein Lite-Plan vorgesehen ist. Es kann jedoch nur jeweils eine Instanz pro Lite-Plan bereitgestellt werden. Während der begrenzten Verfügbarkeit des Standardkontos (Standard Account Limited Release) wird für die folgenden Services ein Lite-Plan angeboten:

<ul>
<li>{{site.data.keyword.prf_hublong}}</li>
<li>{{site.data.keyword.mobilepushfull}}</li>
<li>{{site.data.keyword.cloudantfull}}</li>
<li>{{site.data.keyword.conversationfull}}</li>
<li>{{site.data.keyword.iot_full}}</li>
<li>{{site.data.keyword.languagetranslatorfull}}</li>
<li>{{site.data.keyword.personalityinsightsfull}}</li>
<li>{{site.data.keyword.toneanalyzerfull}}</li>
</ul>

Manche Services sind nicht in allen {{site.data.keyword.Bluemix_notm}}-Regionen verfügbar. Weitere Informationen finden Sie unter [Services nach Region](/docs/services/services_region.html#services_region).

Zu dieser Liste werden weitere Services hinzugefügt, bleiben Sie also dran!

### Grenzwerte des Kontingents

Wenn die Grenzwerte des Kontingents erreicht sind, wird die Anwendung gestoppt oder der Service wird inaktiviert. Wenn im Lite-Plan angegeben ist, dass das Kontingent auf monatlicher Basis bereitgestellt wird, wird die Ressourcennutzung am ersten Tag jedes Monats zurückgesetzt und Sie können die Arbeit mit dem Service fortsetzen. Wenn ein Kontingentgrenzwert erreicht oder fast erreicht ist, erhalten Sie eine Benachrichtigungs-E-Mail. 

Sie können 1 Instanz pro Lite-Plan bereitstellen. 

**Hinweis**: Diese Einschränkungen gelten nur für ein Standardkonto. Sie können jederzeit ein Upgrade auf ein nutzungsabhängiges Konto oder ein abonnementbasiertes Konto durchführen. Kosten fallen nur für die Nutzung an, die über die kostenfreien Kontingente hinausgeht. Weitere Informationen zu nutzungsabhängigen Konten und Abonnementkonten finden Sie unter [Kontotypen](/docs/accounts/account-types.html).

## Optimierungsfeatures
{: #devactivity}

Neue Optimierungsfeatures, die auf Entwicklungsaktivitäten und dem Einsatz in der Entwicklungsumgebung basieren, unterstützen Sie beim Ressourcenmanagement.

### Automatischer Ruhemodus für Apps

Ihre Apps werden in den Ruhemodus versetzt, falls über einen Zeitraum von 10 Tagen keine Entwicklungsaktivität stattfindet. Dies ist nützlich, wenn Sie an einer neuen App arbeiten möchten, da Sie auf diese Weise den Grenzwert von 256 MB für das Speicherkontingent nicht so schnell erreichen. 

Wenn Sie die Apps erneut aktivieren möchten, beginnen Sie in der Cloud Foundry-Befehlszeile oder der {{site.data.keyword.Bluemix_notm}}-Konsole erneut mit der Bearbeitung der Apps. 
 
 In der folgenden Liste sind alle Befehle aufgeführt, mit denen die App aktiviert wird:
  * cf push
  * cf restate
  * cf restart
  * cf ssh
  * cf scale
  * cf stop
  * cf start
  * cf create-route
  * cf map-route
  * cf unmap-route
  * cf delete-route
  * cf enable-ssh
  * cf disable-ssh

Weitere Informationen zur Verwendung der Befehle finden Sie unter [Cloud Foundry-Befehle](/docs/cli/reference/cfcommands/index.html).

 **Hinweis**: Wenn die App bereits für SSH aktiviert ist, kann sie mit den Befehlen `cf enable-ssh` und `cf disable-sh` nicht aktiviert werden. 

### Garbage-Collection

Ihre Lite-Plan-Services werden gelöscht, wenn über einen Zeitraum von 30 Tagen keine Aktivität dafür stattfindet. Auf diese Weise müssen Sie keine inaktiven Instanzen löschen, wenn Sie eine neue Instanz erstellen möchten. 
 
## Teilnahme am begrenzten Release des Standardkontos
{: #lgainvitation}

Sie können einen Freund, der bereits ein Standardkonto besitzt, bitten, Sie einzuladen, oder Sie können sich unter CloudDigitalSales@us.ibm.com an das Vertriebsteam wenden. Nutzen Sie die Gelegenheit, das Produkt zu testen!

Wenn Sie eine Einladung von einem Freund oder einem {{site.data.keyword.Bluemix_notm}}-Verkäufer erhalten, wird die exklusive Einladung an die von Ihnen angegebene E-Mail-Adresse gesendet. Nachdem Sie die Einladung erhalten haben, führen Sie die Anweisungen in der E-Mail aus, um eine Registrierung für ein Standardkonto durchzuführen. 
