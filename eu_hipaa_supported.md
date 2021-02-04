---

copyright:
  years: 2018, 2021
lastupdated: "2021-02-04"

keywords: GDPR, HIPAA, data security, PHI, europe, ACS 

subcollection: account

---

{:shortdesc: .shortdesc}
{:important: .important}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}

# Enabling EU and HIPAA supported settings
{: #eu-hipaa-supported}

If you're the account owner, you can enable your {{site.data.keyword.cloud}} account to be EU supported and HIPAA supported. You might choose to enable the EU Supported setting, for example, if you use resources to process personal data for European citizens. And you might choose to enable the HIPAA Supported setting if you plan to include Protected Health Information (PHI) in HIPAA-enabled services.
{:shortdesc}


## Enabling the EU Supported setting
{: #bill_eusupported}

Enabling the EU supported setting limits Advanced Customer Support (ACS) that is provided by {{site.data.keyword.Bluemix_notm}} support team members in the European Union region. However, {{site.data.keyword.Bluemix_notm}} processing activities might be performed by teams that are outside of the EU region. Global teams can be contacted when issues aren't resolved by the ACS teams in the EU. The global teams are always contacted at the instruction of the EU support team and only when there's no impact to the security or privacy of your data.

By enabling this setting, EU supported services have strict access controls to ensure the data you store and process is restricted and controlled by the IBM support team in the EU region. If {{site.data.keyword.Bluemix_notm}} experts that are outside of the European region need access to this data, an EU support team member reviews the access request. The EU support team member provides necessary access to the global cloud expert only to the requested system, and only for a specific timeframe after which access is revoked. Throughout this process, your data is always protected.

  1. In the {{site.data.keyword.Bluemix_notm}} console, go to **Manage > Account**, and select **Account settings**.
  2. Click **On**.
  3. Read the information about enabling the setting, and select **I understand and agree to these terms**.
  4. Click **On**.

   After you enable the setting, you can use the EU Supported filter option to search the catalog for products that have EU-supported pricing plans.


## Enabling the HIPAA Supported setting
{: #enabling-hipaa}

The US Health Insurance Portability and Accountability Act (HIPAA) and the Health Information Technology for Economic and Clinical Health (HITECH) Act define standards for handling electronic healthcare transactions and information. If you or your company is a covered entity as defined by HIPAA, you must enable the HIPAA Supported setting if you run sensitive workloads that are regulated under HIPAA and the HITECH Act. Learn more about {{site.data.keyword.Bluemix_notm}} compliance in [Compliance on the {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud/compliance){: external}.

Enabling this setting has the following effects:

* Enables you to filter on HIPAA Enabled services in the catalog
* Indicates to IBM that your account stores protected health information (PHI)
* Digitally accepts the IBM Business Associate Addendum (BAA) for covered entities

Enable this setting only if you or your company is a covered entity as defined by HIPAA. If you or your company is a business associate of a covered entity, [contact {{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/account/reg/us-en/signup?formid=MAIL-wcp){: external} to accept the applicable BAA. For more information about HIPAA definitions of covered entities and business associates, see the [US Department of Health & Human Services](https://www.hhs.gov/hipaa/for-professionals/covered-entities/index.html){: external} website.
{: important}

Accounts that enable the HIPAA Supported setting still have access to the full catalog of services. {{site.data.keyword.Bluemix_notm}} services typically offer multiple plans. The HIPAA Enabled label on a service can apply to all available plans or be limited to specific plans or configurations. You as the client are solely responsible for limiting PHI to HIPAA Enabled product plans and architecting in accordance with HIPAA and HITECH.

1. Go to **Manage > Account**, and select **Account setting** in the console.
2. For the HIPAA Supported option, click **On**.
3. Read the information about enabling this setting.

  You can't disable the setting after you enable it.
  {: note}

4. Select **Accept**, and click **Submit**.

  After you enable the setting, you can use the HIPAA Enabled tag to search the catalog for products that are HIPAA enabled.
