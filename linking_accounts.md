---



copyright:

  years: 2015, 2018
lastupdated: "2018-01-30"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Linking your {{site.data.keyword.Bluemix_notm}} and SoftLayer accounts
{: #unifyingaccounts}

You can link your {{site.data.keyword.Bluemix}} and SoftLayer accounts to make use of the combined resources. 
{: shortdesc}

When you link your {{site.data.keyword.Bluemix_notm}} and Softlayer accounts, you will receive a single {{site.data.keyword.Bluemix_notm}} invoice. If you have an existing {{site.data.keyword.Bluemix_notm}} account, the billing through {{site.data.keyword.Bluemix_notm}} for infrastructure resources takes effect for the new billing cycle that starts after the accounts are linked.

All linked accounts in {{site.data.keyword.Bluemix_notm}} must be Pay-As-You-Go accounts. You can create a new Pay-As-You-Go account, link an existing Pay-As-You-Go account, or link an existing trial account, which is then upgraded to a Pay-As-You-Go account. You cannot link Subscription accounts.
{: tip}

You must be a master user in the SoftLayer account to link accounts.

When your accounts are linked:

* You must use your IBMid credentials to access both your SoftLayer and your {{site.data.keyword.Bluemix_notm}} accounts.
* Any existing SoftLayer discounts are applied across {{site.data.keyword.Bluemix_notm}} charges.
* You will receive one invoice in United States dollars (USD).
* You can monitor the usage of your infrastructure resources in the {{site.data.keyword.Bluemix_notm}} console.

After you link your accounts, they cannot be unlinked.  

As a master user, complete the following steps to link your {{site.data.keyword.Bluemix_notm}} and SoftLayer accounts:

 1. From the {{site.data.keyword.Bluemix_notm}} Customer Portal, click **Link a {{site.data.keyword.Bluemix_notm}} Account**.
 2. Read and accept the terms for linking SoftLayer and {{site.data.keyword.Bluemix_notm}} accounts.
 3. When requested, provide the email address that is associated with your {{site.data.keyword.Bluemix_notm}} account. If you don't have a {{site.data.keyword.Bluemix_notm}} account, provide the email address that you want to use, follow the instructions to be invited to {{site.data.keyword.Bluemix_notm}} and create an account.

After you link your accounts, **Go to {{site.data.keyword.Bluemix_notm}}** is available in the SoftLayer console menu bar. Clicking this link takes you to the {{site.data.keyword.Bluemix_notm}} login page.

## Billing for {{site.data.keyword.Bluemix_notm}} usage when accounts are linked
{: #linkedbilling}

After you've linked your {{site.data.keyword.Bluemix_notm}} and SoftLayer billing accounts, the next billing cycle will be charged in a single {{site.data.keyword.Bluemix_notm}} bill.

Your {{site.data.keyword.Bluemix_notm}} usage cycle is on a calendar month basis, so your account is billed each month on the billing day that was established for your charge agreement. With SoftLayer, your usage cycle begins from when you started with SoftLayer, so you are billed each month on the same day of the month as when you signed up for your SoftLayer account. 

When your accounts are linked, your {{site.data.keyword.Bluemix_notm}} usage continues to be measured for the current month's cycle, and you are billed for that usage on a {{site.data.keyword.Bluemix_notm}} invoice. Starting on the first of the next month, your {{site.data.keyword.Bluemix_notm}} and SoftLayer charges are combined on your {{site.data.keyword.Bluemix_notm}} invoice.

For example, if you linked your accounts on 16 April 2017, you get a {{site.data.keyword.Bluemix_notm}} invoice for your April usage. Depending on when you linked your accounts, you might get a separate bill for your SoftLayer usage. Then, your combined usage during May is billed through your {{site.data.keyword.Bluemix_notm}} account.

![Linking IBM Cloud and SoftLayer accounts summary](images/IBMCloudSoftLayerBill.svg)

After your bills are linked, your {{site.data.keyword.Bluemix_notm}} invoice lists the different charges for each resource that you have used.

## API-based {{site.data.keyword.Bluemix_notm}} services
{: #api-based-services}

The following list contains the services that you can set up to run with your application code. Not all plans for these services are available for use with linked accounts. Only the plans enabled for Pay-As-You-Go accounts are available to use with linked accounts. However, if you have a separate {{site.data.keyword.Bluemix_notm}} account that's billed separately, you can use any plan for any of these services.

* {{site.data.keyword.alertnotificationshort}}
* {{site.data.keyword.sparks}}
* {{site.data.keyword.appseccloudshort}}
* {{site.data.keyword.blockchain}}
* {{site.data.keyword.cloudant}}
* {{site.data.keyword.iotmapinsights_short}}
* {{site.data.keyword.dashdbshort}}
* {{site.data.keyword.weather_short}}
* {{site.data.keyword.iotdriverinsights_short}}
* {{site.data.keyword.geospatialshort_Geospatial}}
* {{site.data.keyword.iotelectronics}}
* {{site.data.keyword.languagetranslationshort}}
* {{site.data.keyword.messagehub}}
* {{site.data.keyword.nlclassifiershort}}
* {{site.data.keyword.objectstorageshort}}
* {{site.data.keyword.personalityinsightsshort}}
* {{site.data.keyword.servicediscoveryshort}}
* {{site.data.keyword.speechtotextshort}}
* {{site.data.keyword.sqldb}}
* {{site.data.keyword.streaminganalyticsshort}}
* {{site.data.keyword.texttospeechshort}}
* {{site.data.keyword.toneanalyzershort}}
* {{site.data.keyword.visualrecognitionshort}}
* {{site.data.keyword.workloadscheduler}}

