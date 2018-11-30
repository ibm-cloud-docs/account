---

copyright:

  years: 2018

lastupdated: "2018-11-15" 

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:tip: .tip}
{:important: .important}


# Enabling EU and HIPAA supported settings
{: #eu-hipaa-supoorted}

If you're the account owner, you can enable your account to be EU supported and HIPAA supported. You might choose to enable the EU Supported setting, for example, if you use resources to process personal data for European citizens. And you might choose to enable the HIPAA Supported setting if you plan to include Protected Health Information (PHI) in HIPAA-enabled services. 
{:shortdesc}


## Enabling the EU Supported setting
{: #bill_eusupported}

Enabling the EU supported setting limits Level 1 and Level 2 support that is provided by {{site.data.keyword.Bluemix_notm}} support team members in the European Union region. However, {{site.data.keyword.Bluemix_notm}} processing activities might be performed by teams that are outside of the EU region. Global teams can be contacted when issues aren't resolved by the Level 1 or Level 2 support teams in the EU. The global teams are always contacted at the instruction of the EU support team and only when there's no impact to the security or privacy of your data.

By enabling this setting, EU supported services have strict access controls to ensure the data you store and process is restricted and controlled by the IBM support team in the EU region. If {{site.data.keyword.Bluemix_notm}} experts that are outside of the European region need access to this data, an EU support team member reviews the access request. The EU support team member provides necessary access to the global cloud expert only to the requested system, and only for a specific time frame after which access is revoked. Throughout this process, your data is always protected.

  1. In the {{site.data.keyword.Bluemix_notm}} console, go to **Manage > Account**, and select **Account settings**.
  2. Click **On**.
  3. Read the information about enabling the setting, and select **I understand and agree to these terms**.
  4. Click **On**.

  After you enable the EU Supported setting, you can use the `EU Supported` tag to search the catalog for offerings that have EU-supported plans. 
  {: tip}


## Enabling the HIPAA Supported setting
{: #enabling-hipaa}

You can choose to enable the HIPAA Supported setting to run sensitive workloads that are regulated under the US Health Insurance Portability and Accountability Act (HIPAA). By enabling this setting, you're indicating that your account processes PHI that might be subject to HIPAA. 

1. Go to **Manage > Account**, and select **Account setting** in the console.
2. For the HIPAA Supported option, click **On**. 
3. Read the information about enabling this setting. 

  You can't disable it after you enable it.
  {: important}
   
4. Select **Accept**, and click **Submit**. 

  After you enable the HIPAA Supported setting, you can use the `HIPAA Enabled` tag to search the catalog for offerings that are HIPAA enabled. Also, {{site.data.keyword.Bluemix_notm}} warns you if you select to create an offering that isn't HIPAA enabled.
  {: tip}