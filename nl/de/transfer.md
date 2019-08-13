---

copyright:
  years: 2019
lastupdated: "2019-07-31"

keywords: change owner, transfer account, transfer account ownership, switch owner, transfer owner

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Eigentumsrecht für Ihr Konto übertragen
{: #transfer}

Sie können Ihr gesamtes {{site.data.keyword.cloud}}-Konto an einen anderen Eigner übertragen, indem Sie das Unternehmensprofil aktualisieren. Wenn Sie eine Konto von einem anderen Eigner übertragen müssen, erstellen Sie einen Supportfall mit Ihren Unternehmensinformationen.
{:shortdesc}

Nur Konten mit nutzungsabhängiger Abrechnung oder Abonnementkonten können übertragen werden.

Sie können das Eigentumsrecht für einzelne Ressourcen innerhalb Ihres Kontos übertragen, indem Sie den Befehl `ibmcloud catalog` verwenden. Weitere Informationen finden Sie in [Eigentumsrecht für eine private Ressource übertragen](/docs/account?topic=account-include#owners).
{: tip}

## Konto übertragen, dessen Eigner Sie sind
{: #transfer-own}

Wenn Sie der Kontoeigner sind und sich bei Ihrem Konto anmelden können, können Sie mithilfe der folgenden Schritte das Eigentumsrecht für Ihr Konto übertragen.

1. Rufen Sie in der Konsole **Verwalten > Konto** auf und wählen Sie **Unternehmensprofil** aus.
1. Klicken Sie auf **Profilaktualisierung anfordern**.
1. Aktualisieren Sie das Kontoprofil mit den Informationen des neuen Eigners.
1. Klicken Sie auf **Aktualisierungsanforderung übergeben**.

Das {{site.data.keyword.cloud_notm}}-Team überprüft die Änderungen, bevor diese wirksam werden.

## Konto von einem anderen Eigner übertragen
{: #transfer-lost}

Wenn der Eigner eines Kontos das Unternehmen verlässt und Sie das Konto übertragen müssen, müssen Sie einen neuen Eigner auswählen und dann einen Supportfall öffnen, um eine Übertragung anzufordern.  

Der neue Eigner muss ein Benutzer in dem betreffenden Konto sein und darf nicht der Eigner eines anderen {{site.data.keyword.cloud_notm}}-Kontos sein. Wenn sich der Benutzer nicht im Konto befindet, kann er von einem anderen Benutzer eingeladen werden oder Sie können in dem Supporfall, den Sie erstellt haben, anfordern, dass der Benutzer zum Konto hinzugefügt wird. Wenn der Benutzer bereits Eigner eines {{site.data.keyword.cloud_notm}}-Kontos ist, können Sie anfordern, dass das aktuelle Konto dieses Benutzers an einen anderen Benutzer übertragen oder storniert wird. 

Im Supportfall zum Anfordern einer Kontoübertragung müssen Sie ein offizielles Dokument Ihres Unternehmens anfügen, das die nachfolgend aufgeführten Informationen enthält. 
- Offizieller Briefkopf des Unternehmens
- Satzung des Unternehmens, falls zutreffend
- Erklärung, dass die betreffende Person nicht mehr zum Unternehmen gehört
- Erklärung, dass das Konto an einen neuen Eigner übertragen werden soll
- Vor- und Nachname des neuen Kontoeigners
- E-Mail-Adresse und Telefonnummer des neuen Kontoeigners
- Unterschrift einer Führungskraft des Unternehmens
- Kontonummer des zu übertragenden Kontos

   Wenn Sie beim Konto angemeldet sind, finden Sie die Kontonummer in der {{site.data.keyword.cloud_notm}}-Menüleiste neben dem Kontonamen. Beispiel: "1234567 - IBM". Dabei ist die Kontonummer 1234567.
   {: tip}

   ![Screenshot der Kontoauswahl in der Menüleiste der Konsole. Kontoname und Kontonummer werden angezeigt. Sie können das aktuelle Konto auswählen, um eine Liste anderer Konten aufzurufen, auf die Sie zugreifen können.](images/account-faq.svg "In der Kontoauswahl werden der Kontoname und die Kontonummer angezeigt. Sie können das aktuelle Konto auswählen, um eine Liste anderer Konten aufzurufen, auf die Sie zugreifen können.")

Zur Erstellung des Supportfalls rufen Sie **Support** auf und klicken Sie auf **Fall erstellen**. Hängen Sie das offizielle Anforderungsdokument an den Fall an, bevor Sie ihn übergeben.
