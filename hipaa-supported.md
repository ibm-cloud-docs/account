---

copyright:
  years: 2018, 2021
lastupdated: "2021-06-11"

keywords: HIPAA, PHI, HITECH

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:important: .important}
{:tip: .tip}
{:note: .note}
{:term: .term}


# Enabling HIPAA support for your account
{: #enabling-hipaa}

If you're the account owner, you can enable your {{site.data.keyword.cloud}} account to be HIPAA supported. HIPAA support can be useful if you plan to include Protected Health Information (PHI) in HIPAA-enabled services.
{:shortdesc}

The US Health Insurance Portability and Accountability Act (HIPAA) and the Health Information Technology for Economic and Clinical Health (HITECH) Act define standards for handling electronic healthcare transactions and information. If you or your company is a covered entity as defined by HIPAA, you must enable the HIPAA Supported setting if you run sensitive workloads that are regulated under HIPAA and the HITECH Act. Learn more about {{site.data.keyword.Bluemix_notm}} compliance in [Compliance on the {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud/compliance){: external}.

Enabling this setting has the following effects:

* Enables you to filter on HIPAA Enabled services in the catalog
* Indicates to {{site.data.keyword.IBM_notm}} that your account stores protected health information (PHI)
* Digitally accepts the {{site.data.keyword.IBM_notm}} Business Associate Addendum (BAA) for covered entities

Enable this setting only if you or your company is a covered entity as defined by HIPAA. If you or your company is a business associate of a covered entity, [contact {{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/account/reg/us-en/signup?formid=MAIL-wcp){: external} to accept the applicable BAA. For more information about HIPAA definitions of covered entities and business associates, see the [US Department of Health & Human Services](https://www.hhs.gov/hipaa/for-professionals/covered-entities/index.html){: external} website.
{: important}

Accounts that enable the HIPAA Supported setting still have access to the full catalog of services. {{site.data.keyword.Bluemix_notm}} services typically offer multiple plans. The HIPAA Enabled label on a service can apply to all available plans or be limited to specific plans or configurations. You as the client are solely responsible for limiting PHI to HIPAA Enabled product plans and architecting in accordance with HIPAA and HITECH.

1. Go to **Manage** > **Account**, and select **Account setting** in the console.
2. For the HIPAA Supported option, click **On**.
3. Read the information about enabling this setting.

  You can't disable the setting after you enable it.
  {: important}

4. Select **Accept**, and click **Submit**.

  After you enable the HIPAA Supported setting, you can use the HIPAA Enabled tag to search the catalog for products that are HIPAA enabled.


