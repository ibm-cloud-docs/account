---

copyright:
  years: 2019
lastupdated: "2019-08-05"

keywords: enterprise, enterprise resources, enterprise account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Bewährte Verfahren für die Einrichtung von Unternehmen
{: #enterprise-best-practices}

Die hier beschriebenen bewährten Verfahren liefern die Grundbausteine für das Einrichten eines {{site.data.keyword.cloud}}-Unternehmens.
{:shortdesc}

## Konten nach dem gewünschten Verfahren zur Abrechnungsverfolgung organisieren
{: #organize-enterprise-usage}

Ein wesentlicher Vorteil von {{site.data.keyword.cloud_notm}}-Unternehmen besteht darin, dass sie es ermöglichen, die Abrechnung und Nutzung über mehrere Konten hinweg zentral anzuzeigen und zu verwalten. Diese Funktionalität ist von Ihrer Unternehmensstruktur abhängig, da die Nutzungsdaten von jeder Kontogruppe und jedem Konto aggregiert werden. Sie können Kontogruppen für Projekte erstellen, die im Rahmen eines gemeinsamen Budgets durchgeführt werden. [Wie kann ich ein Unternehmen verwenden?](/docs/account?topic=account-enterprise#enterprise-use-cases) enthält Beispiele hierzu. 

Der Unternehmensadministrator oder Ihr Finanzverantwortlicher ist möglicherweise nicht mit jedem einzelnen Konto oder jeder Kontogruppe vertraut. Geben Sie jedem Konto und jeder Kontogruppe daher einen aussagefähigen Namen, damit ihr Zweck leichter zu erkennen ist. Wenn Ihr Unternehmen Abrechnungscodes verwendet, können Sie diese auch in den Namen aufnehmen. Beispiel: Anstelle einer Kontogruppe `devteam` mit den Konten `fed ui` und `be api` erstellen Sie eine Kontogruppe `Development - A2B3` mit den Konten `Front-end UI team` und `Back-end API team`.

Ein Unternehmensbenutzer mit Administrator- oder Bearbeiterzugriff kann die Namen des Unternehmens und der Kontogruppen bearbeiten, aber die Kontonamen können nicht geändert werden. Um einen Kontonamen zu bearbeiten, muss ein Benutzer selbst im Konto enthalten sein.
{:tip}

Da Sie eine einheitliche Sicht der gesamten Nutzung haben, die nach Ihren Kontogruppen und Konten organisiert ist, können Sie die Nutzungskosten an die zugehörigen Teams zurückbelasten. Weitere Informationen finden Sie unter [Kosten für die Unternehmensnutzung einziehen](/docs/billing-usage?topic=billing-usage-enterprise-usage#enterprise-cost-recovery).

## Konsistente Unternehmenshierarchie erstellen
{: #accounts-vs-groups}

Wenn Sie Ihr Unternehmen einrichten, erstellen Sie eine Unternehmenshierarchie, die Ihre Firma oder Ihre Organisation widerspiegelt. Wenn Sie Konten und Kontogruppen erstellen, planen Sie ein konsistentes Schema für die Art und Weise, wie Ihr Unternehmen die folgenden Unternehmensebenen verwendet:
- Ressourcengruppen und Cloud-Foundry-Organisationen und -Bereiche innerhalb eines Kontos
- Konten innerhalb einer Kontogruppe
- Kontogruppen innerhalb des Unternehmens

Beispielsweise kann Ihre Firma Konten für jedes Team erstellen - mit Ressourcengruppen oder Cloud Foundry-Organisationen innerhalb des Kontos für Entwicklungs-, Test- und Produktionsumgebungen. Eine andere Firma verfügt möglicherweise über unterschiedliche Konten für jede Umgebung, die in Kontogruppen für jedes Team gruppiert sind.

Wie immer Sie Ihr Unternehmen strukturieren - tun Sie dies möglichst konsistent, um das Unternehmensmanagement zu vereinfachen. Da es einfach ist, neue Konten zu erstellen und zu verfolgen, besteht eine gewisse Gefahr, dass sehr viele separate Konten erstellt werden, wenn die Benutzer dies anfordern. Dabei ist zu beachten, dass jedes zusätzliche Konto den Verwaltungsaufwand erhöht. Beachten Sie deshalb beim Planen der Struktur Ihres Unternehmens die folgenden Punkte:
- Für jedes Konto, das Sie erstellen, müssen Benutzer eingeladen werden und ihr Zugriff muss separat verwaltet werden.
- Bei einer inkonsistenten Struktur kann es schwieriger sein festzustellen, wer innerhalb jedes Kontos Zugriff hat und welche Teams Ressourcen nutzen.
- Benutzer können Ressourcen und Services nur innerhalb eines einzelnen Kontos gemeinsam nutzen. Ressourcen können nicht zwischen Konten verschoben werden.

## Zugriffsrichtlinien in einem Unternehmen einrichten
{: #access-enterprise}

Wenden Sie ein bewährtes Verfahren an, um die minimale Anzahl von Zugriffsrichtlinien und Zugriffsebenen zuzuweisen. Auf diese Weise benötigen Sie weniger Zeit, um Benutzern den Zugriff zuzuweisen, und Sie haben mehr Zeit für die Entwicklung in {{site.data.keyword.cloud_notm}}. Gleichzeitig stellen Sie sicher, dass Sie die Zugriffsrechte nicht vielen Benutzern erteilen, die diese gar nicht benötigen.

Zugriffsgruppen sind ein nützliches Tool für das Zuweisen von Zugriffsrechten für eine Gruppe von Benutzern und Service-IDs, die alle denselben Zugriff benötigen. Durch die Verwendung von Zugriffsgruppen können Sie die Zugriffsverwaltung rationalisieren, indem Sie Gruppen von Benutzern die minimale Anzahl von Zugriffsrichtlinien zuweisen. Beispiel: Wenn 5 Benutzer vorhanden sind, die alle Aufgaben im Zusammenhang mit der Abrechnung und der Kontoverwaltung für das Unternehmen übernehmen sollen, können Sie diese zu einer Zugriffsgruppe mit dem Namen `Administratoren` hinzufügen. In der Zugriffsgruppe können Sie zwei Richtlinien zuweisen: eine mit der Administratorrolle für den Abrechnungskontoverwaltungsservice und eine mit der Administratorrolle für alle Kontoverwaltungsservices im Konto. Wenn Benutzer ihre Zuständigkeiten oder Teams wechseln, können Sie Benutzer aus der Zugriffsgruppe hinzufügen oder entfernen, anstatt immer dieselben Richtlinien für einzelne Benutzer hinzuzufügen oder zu entfernen. [Zugriffsberechtigungen für das Unternehmen zuweisen](/docs/iam?topic=iam-assign-access-enterprise) enthält weitere Informationen hierzu. 

## Mit Ressourcen in einem Unternehmen arbeiten
{: #child-resources-enterprise}

Erstellen Sie Ressourcen nur in untergeordneten Konten, die Sie im Unternehmen importieren oder erstellen. Auch wenn es möglich ist, Ressourcen innerhalb des Unternehmenskontos zu erstellen, empfiehlt sich dies aus den folgenden Gründen eher nicht:
 - Das Unternehmenskonto ist dem Unternehmen immer direkt untergeordnet und kann nicht verschoben werden, sodass Sie nicht flexibel ändern können, wie die Nutzung für die Ressourcen gemeldet wird.
 - Das Unternehmenskonto enthält die Benutzer und den Zugriff für die Verwaltung des Unternehmens und der Abrechnung, sodass dem Konto nur die Benutzer mit diesen Zuständigkeiten hinzugefügt werden sollten.

Benutzer innerhalb jedes Kontos im Unternehmen können Ressourcen erstellen, verwenden und mit anderen Benutzern gemeinsam nutzen, so wie dies in einem eigenständigen Konto möglich ist. Weitere Informationen finden Sie unter [Mit Ressourcen und Services arbeiten](/docs/resources?topic=resources-resource). Die Benutzer eines Unternehmens können nicht direkt mit Ressourcen in untergeordneten Konten arbeiten, aber sie können die Ressourcentypen und -pläne überwachen, die in jedem Konto verwendet werden, indem sie ihre Nutzung anzeigen. Weitere Informationen finden Sie unter [Nutzung in einem Unternehmen anzeigen](/docs/billing-usage?topic=billing-usage-enterprise-usage).


