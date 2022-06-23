---

copyright:

  years: 2022

lastupdated: "2022-06-22"

keywords: context-based restrictions, enabled, disabled, report-only, monitor, monitor cbr, cbr, activity tracker, cbr events, context-based restrictions events, denied access

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Monitoring context-based restrictions
{: #cbr-monitor}

Context-based restrictions protect your resources by denying access to identities that don't satisfy context requirements, such as making access requests from the network zones and endpoint types that you define. You can enable context-based restrictions upon creation, or choose to set the rule to report-only mode. Use {{site.data.keyword.cloudaccesstrailshort}} to monitor enabled rules, and report-only rules to view how the rule affects your users, applications, and workflows without enforcing the rule. 
{: shortdesc}

## Before you begin
{: #before-monitor-cbr}

You must provision an instance of the {{site.data.keyword.cloudaccesstrailshort}} service in the Frankfurt (eu-de) region to monitor events for context-based restrictions. For more information, see [Provisioning an instance](/docs/activity-tracker?topic=activity-tracker-provision).

## Determining how rules would affect access by using report-only mode
{: #report-only-access}

It can be difficult to predict exactly how your rules might affect users, applications, and workflows. At first, you might create rules that are too stringent and break your workflows. Or, they are too accessible and might allow more users than you intend to access your resources. The recommendation is to first set your rule to report-only mode for at least 30 days before you enable it so that you can monitor the rule's impact.

Complete the following steps to view how rules affect your users' and applications' access in report-only mode by using {{site.data.keyword.cloudaccesstrailshort}}:

1. In the {{site.data.keyword.cloud_notm}} console, go to the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Observability** > **{{site.data.keyword.cloudaccesstrailshort}}**. 
1. Click **Open dashboard** on the dashboard that you use to monitor context-based restrictions. 
1. Use the search field to narrow the results to report-only context-based restrictions events.
   1. To view potentially blocked access requests, search for `action:context-based-restrictions.policy.eval responseData.isEnforced:==false responseData.decision:Deny`. 
      * `isEnforced:==false` indicates that the rule is in report-only mode. 
      * `responseData.decision:Deny` indicates that, if you enable the rule, this access request is blocked. 

      Evaluate whether this access flow is supposed to be denied, or whether you need to update your rule to allow access so that your workflows don't break. 
      {: tip}

   1. To view potentially allowed access requests, search for `action:context-based-restrictions.policy.eval responseData.isEnforced:==false responseData.decision:Permit`.
      * `isEnforced:==false` indicates that the rule is in report-only mode. 
      * `responseData.decision:Permit` indicates that, if you enable the rule, this access request is allowed.

      Evaluate whether this access flow is supposed to be allowed, or whether you need to update your rule to deny access so that your resources are protected. 
      {: tip}

## Determining how enabled rules affect access
{: #enabled-access}

When you enable a rule, some users, applications, and workflows might be affected. If your users or applications can't access something that they previously had access to, you can search in {{site.data.keyword.cloudaccesstrailshort}} and view what rules are denying the requests. You can further refine the search by filtering on the subject or resource to identify the implicated rule, which is represented by the `target id`. Then, you can update the rule to allow access so that your workflows don't break. For more information, see [Updating context-based restrictions](/docs/account?topic=account-context-restrictions-update). 

Complete the following steps to view how enabled rules affect your users' and applications' access by using {{site.data.keyword.cloudaccesstrailshort}}:

1. In the {{site.data.keyword.cloud_notm}} console, go to the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg "Menu") > **Observability** > **{{site.data.keyword.cloudaccesstrailshort}}**. 
1. Click **Open dashboard** on the dashboard that you use to monitor context-based restrictions. 
1. Use the search field to narrow the results to enabled context-based restrictions events.
   1. To view blocked access request, search for `action:context-based-restrictions.policy.eval responseData.isEnforced:==true responseData.decision:Deny`. 
      * `isEnforced:==true` indicates that the rule is enabled and enforced. 
      * `responseData.decision:Deny` indicates that the access request is blocked. 
    
   1. If you have a specific resource that you are protecting with a context-based restriction, you can see whether access to the resource is blocked by searching for `action:context-based-restrictions.policy.eval  responseData.decision:Deny responseData.isEnforced:==true <CRN OR UNIQUE ID OF THE RESOURCE>`. 

### Examples 
{: #cbr-monitor-example}

A context-based restriction rule that protects `Example service` has the following identifying attributes in Activity Tracker:

| Attribute    | Value      | Description |
|---------------|------------|-----------|
| action        | `context-based-restrictions.policy.eval` |
| initiator ID | `iam-ServiceId-21271d73-adae-410d-820b-7a582b0066fc` | The unique ID of the protected service. |
| initiator name  | `Example service` | The name of the protected service. |
| target ID| `crn:v1:staging:public:context-based-restrictions:global:a/9bb3ea01633c4d828080de16ce34ea70::rule:b9fadacd4fbe034d7aafcd1659063aaa` | The unique ID of the rule that rendered the allow or deny decision. |
| requestData | `ipAddress`, `resource`, `subject` | Contains the details of the resource that the requester is trying to access, the identity of the requester and from what IP address they are requesting access.|
| responseData | `decision`, `isEnforced` | The decision and enforcement mode. When `isEnforced=false`, the rule is in report-only mode. |
| correlationId | `4a03eafdefed4f059dc9cad29d28513cxacml` | Used for debug interactions and tracing the request with support. |
{: caption="Table 1. Sample context-based restriction attributes and values in Activity Tracker" caption-side="top"}
