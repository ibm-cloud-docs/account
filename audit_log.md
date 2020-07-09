---

copyright:
  years: 2018, 2020
lastupdated: "2020-06-10"

keywords: audit log, user access, account log, system events, monitor system events, user access logs

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}


# Auditing system events for classic infrastructure 
{: #audit-log}

If you have a classic infrastructure account, you can monitor storage replication events by viewing audit logs. Audit logs track the interactions of each user, like login attempts, port speed updates, power restarts, and interactions made by {{site.data.keyword.BluSoftlayer_notm}} infrastructure support staff.
{:shortdesc}


## Viewing your audit log
{: #view-audit-log}

To view your audit log, go to **Manage > Account** in the {{site.data.keyword.cloud_notm}} console, and select **Audit log**. The audit log initially displays the last 25 interactions that were taken by users on the account. You can view up to 200 interactions at any time. Expand the items per page menu to see more results.

### Viewing a user's access logs
{: #view-access-logs}

From the audit log page, you can also see data for each access attempt that is made by a specific user. The logs display a date and time stamp and IP address for each access attempt. Use the following steps to view a user's Access Logs.

1. In the console, go to **Manage > Account**, and select **Audit log**.
2. Then, filter for the user, select the timeframe that you want to view, and choose an object type.  

The access log for each user displays the access attempts that were made by that user by date, along with the IP address from which the access attempt was made. Information within the access log is read-only.

### Granting access to the audit log
{: #grant-access-logs}

The Viewer role or higher on all account management services is required to view the audit log. For classic infrastructure permissions, a user must be assigned the Super user role. 
