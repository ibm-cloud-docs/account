---

copyright:

  years: 2019, 2021

lastupdated: "2021-09-13"

keywords: cir, impacting event, services, advanced customer support

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Customer Incident Report
{: #cir}

{{site.data.keyword.Bluemix}} works hard to maintain high availability of infrastructure and cloud services. If you're impacted by any event that disrupts your service delivery, a Customer Incident Report (CIR) can be provided. A CIR provides information about how services are impacted and how an issue is getting resolved.
{: shortdesc}

After you create a support case, you can view updates about your impacting event from the Manage cases page. For more information, see [Managing your support cases](/docs/account?topic=account-managing-support-cases). If the scope of an impacting event is of a larger enterprise-wide scope, a CIR is provided upon request.
{: note}


## Details about the Customer Incident Report (CIR)
{: #details-customer-incident-report}

A CIR is provided for larger, enterprise-level issues. They are updates that provide a Root Cause Analysis (RCA) which is the process for determining the underlying cause of a Customer Impacting Event (CIE). Smaller issues that don't affect {{site.data.keyword.Bluemix_notm}} at an enterprise level don't provide an RCA or CIR. The Advanced Customer Support (ACS) team that mitigates the issue still provides updates, but they're not a formal RCA.

Larger enterprise-wide issues are events that typically impact multiple user environments or regions. Due to the scope and impact of enterprise issues, {{site.data.keyword.Bluemix_notm}} requires a thorough RCA and the CIR is a summary report for the findings of the investigation.

RCA investigations are complex and involve program review, feedback from product specialists, multiple inter-related cloud services, and vendor discussions. If the CIR can't be delivered within the Service Level Objective (SLO), an interim CIR is provided within the five business day SLO. For more information about SLO, see [Case severity and initial response times](/docs/account?topic=account-support-case-severity).

The CIR is a point-in-time document that is intended to convey a specific set of information about an impacting incident. The interim CIR document provides the current findings of the ongoing RCA, the next investigative steps, and a timeline for the next expected update. Depending on the complexity of the issue, more than one interim CIR might be required before the final version is available. The Service team (SRE) determines when the CIR is available. Customers with follow-up questions about a specific detail of the incident, or its impact on their environment, need to ask those questions in a support case.

The following image shows the process for receiving a CIR.

![Flowchart for receiving customer incident report updates.](images/CIRimage.png "Customer incident report flowchart"){: caption="Workflow for getting customer incident report updates." caption-side="bottom"}


## Requesting a Customer Incident Report (CIR)
{: #requesting-customer-incident-report}

A CIR must be requested within 30 days of an impacting event by using one of the following methods:

* Create a case that requests a CIR
* Request a CIR within the case description
* Update your case with a request for a CIR

To create a case, go to [Create a case](/unifiedsupport/cases/add), or to update your case, go to the [Manage cases page](/unifiedsupport/cases).

After the ACS team receives your request for a CIR, they will initiate the CIR process if the issue was caused by a CIE. When it's available, your CIR is provided with a PDF copy that is attached to your support case.
