---

copyright:
  years: 2021, 2023
lastupdated: "2023-06-27"

keywords: troubleshoot account, upgrade account, upgrade issue
subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# How do I get access to upgrade my {{site.data.keyword.Bluemix_notm}} account? 
{: #ts_upgrade_cc}
{: troubleshoot}

You can't upgrade to a Pay-As-You-Go account.
{: shortdesc}

When you try to upgrade your account from the [Account settings](/account/settings) page in the {{site.data.keyword.Bluemix_notm}} console, the following message is displayed:
{: tsSymptoms}

> Looks like you don't have access to view this page. Contact the account owner for access.

To upgrade your account, you must have an access policy with the Editor role or higher on all account management services. 
{: tsCauses}

Contact the account owner to request access to upgrade your account. For more information, see [Upgrading your account](/docs/account?topic=account-upgrading-account). 
{: tsResolve}

## Requirements 
{: #requirements}

The following table outlines the requirements used in the architecture for each aspect: 

| Aspect | Requirements |
|-----| -----|
| Compute | Provide properly isolated compute resources with adequate compute capacity for the application. Remember to allow for the resource needs of the operating system and any other software needed. |
| Storage | Provide storafe that meets the application data volume and performance requirements. |
| Networking | Deploy workloads in an islolated environment and enforce information flow policies.  \n \n Provide secure and encrypted connectivity to the cloud's private network for management purposes.  \n \n Distribute resolution to support the use of hostnames instead of IP addresses. |
| Security | Protect the boundaries of the application against the Denial of Service and application-layer attacks.  \n \n If it's required, encrypt all the application data in transit and at rest to protect from unauthorized disclosure.  \n \n Encrypt all the security data and operational and audit logs to protect from unauthorized disclosure. |
| Resiliency | Support application availability targets.  \n \n Ensure availability of the application in the event of a planned and an unplanned outage.  \n \n Provide highly available compute, storage, network, and other cloud services to handle application load and performance requirements.  \n \n Provide highly available storage for security data logs and backup data.  \n \n Automate recovery tasks to minimize down time. |
| Service management | Monitor system and application health metrics and logs to detect issues that might impact the availability of the application.  \n \n Generate alerts and notifications about issues that might impact the availability of applications to trigger appropriate responses to minimize down time.  \n \n Monitor audit logs to track changes and detect potential security problems.  \n \n Provide a mechanism to identify and send notifications about issues found in the audit logs. |
{: caption="Table 1. Requirements" caption-side="bottom"}
