---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise settings, manage enterprise, view enterprise, rename enterprise

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Unternehmen verwalten
{: #enterprise-settings}

Über das Dashboard Ihres {{site.data.keyword.Bluemix}}-Unternehmens können Sie Unternehmensdetails anzeigen, allgemeine Aktionen ausführen (z. B. Konten hinzufügen und Benutzer einladen) und Abrechnungsinformationen anzeigen. Sie können Ihr Unternehmen auch über das Dashboard, über die Befehlszeilenschnittstelle oder die API umbenennen.
{:shortdesc}

Zum Verwalten von Unternehmenseinstellungen benötigen Sie die Rolle "Administrator" oder "Bearbeiter" für den Unternehmensservice im Unternehmenskonto.
{: tip}

## Unternehmen in der Konsole verwalten
{: #enterprise-manage}

Um das Dashboard für das Unternehmen anzuzeigen, rufen Sie **Verwalten > Unternehmen** auf. Das Dashboard bietet einen Überblick über Konten, Benutzer und Abonnementguthaben in Ihrem Unternehmen. Das Dashboard verfügt über Quick Links, über die Sie die folgenden allgemeinen Aktionen ausführen können:
   * [Neue oder vorhandene Konten zu Ihrem Unternehmen hinzufügen](/docs/account?topic=account-enterprise-add)
   * [Benutzer für Unternehmenskonto einladen](/docs/iam?topic=iam-iamuserinv)
   * [Abonnementguthaben anzeigen und verwalten](/docs/billing-usage?topic=billing-usage-subscriptions)

Außerdem können Sie Ihr Unternehmen umbenennen, indem Sie im Abschnitt "Unternehmensdetails" auf **Umbenennen** klicken.

## Unternehmen über die Befehlszeilenschnittstelle verwalten
{: #enterprise-manage-cli}

* Sie können Unternehmensinformationen wie den Namen, die Domäne, den Eigner sowie das Erstellungs- und Aktualisierungsdatum anzeigen.

  ```
  ibmcloud enterprise show
  ```
  {: codeblock}
* Benennen Sie das Unternehmen um, indem Sie den neuen Namen bei der Option `-n` im folgenden Befehl angeben.

   ```
   ibmcloud enterprise update -n NEW_NAME
   ```
   {:codeblock}

## Unternehmen über die API verwalten
{: #enterprise-manage-api}

Sie können ein Unternehmen über das Programm aktualisieren, indem Sie die Unternehmensverwaltungs-API aufrufen, wie in der folgenden Beispielanforderung dargestellt. Sie können den Unternehmensnamen oder die Domäne aktualisieren, indem Sie die neuen Werte für den API-Aufruf übergeben. Detaillierte Informationen zur API finden Sie in der [Dokumentation zur Unternehmensverwaltung-API](https://{DomainName}/apidocs/enterprise-apis/enterprise#update-an-enterprise){: external}.

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID" \
-H "Authorization: $IAM_TOKEN" \
-H 'Content-Type: application/json' \
-d '{
  "name": "Brand New Sample Enterprise",
  "domain": "new.example.com"
}'
```
