---

copyright:
  years: 2021, 2022
lastupdated: "2022-07-21"

keywords: Context based restriction, rule, context, network zone, IBM Cloud restrictions, IBM Cloud context restriction, IBM Cloud access, access control, resource access, Cloud Foundry, endpoint type

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# What are context-based restrictions?
{: #context-restrictions-whatis}

Context-based restrictions give account owners and administrators the ability to define and enforce access restrictions for {{site.data.keyword.cloud}} resources based on the network location of access requests. These restrictions work with traditional IAM policies, which are based on identity, to provide an extra layer of protection. Since both IAM access and context-based restrictions enforce access, context-based restrictions offer protection even in the face of compromised or mismanaged credentials.
{: shortdesc}

For an example scenario on creating context-based restrictions, follow the tutorial for [Leveraging context-based restrictions to secure your resources](/docs/account?topic=account-context-restrictions-tutorial).

![A diagram that shows how context-based restrictions work.](images/CBR-diagram.svg){: caption="Figure 1. A diagram that shows how context-based restrictions work." caption-side="bottom"}

## Rules
{: #restriction-rules}
{: #context-restrictions-rule-whatis}

A rule associates an {{site.data.keyword.cloud}} resource with a set of contexts: 
* The cloud resource is specified by resource attributes similar to IAM access policies.
* A context is a combination of network zones and endpoint types.

The contexts that you configure define the restrictions for the associated resources.

The required resource attributes in context-based restrictions rules are `accountId` and `serviceName`. Rules must be scoped to an account and a specific service.
{: note}

Context-based restriction rules are applied by the following logic:
* Access is granted by a rule only when at least one of the rule's contexts allows access.
* If multiple rules are applicable to a particular resource, access is granted only when all applicable rules allow access.
* If no rules are applicable to a particular resource, access is determined exclusively by IAM policies.

Unlike IAM policies, context-based restrictions don't assign access. Context-based restrictions check that an access request comes from an allowed context that you configure. 
{: note}

To manage rules, you must be assigned a specific role for the context-based restriction account management service: 
| Roles         | Actions                                                                                                |
|---------------|--------------------------------------------------------------------------------------------------------|
| Viewer        | View rules   |
| Editor        | View rules   |
| Operator      | View rules   |
| Administrator | View rules   \n  \n Create rules   \n  \n Update rules   \n  \n Remove rules  |
{: caption="Table 1. Roles and example actions for rules" caption-side="top"}

For more information, see [Actions and roles for account management services](/docs/account?topic=account-account-services&interface=ui).

### Rule enforcement 
{: #rule-enforcement}

You can decide how you want to enforce a rule upon creation and update the rule enforcement at any time.
* **Enable**: Enforce the rule. Denied access attempts are reported in {{site.data.keyword.at_short}}.
* **Disable**: No restrictions apply to your account resources. Select this option if you're not ready to enable the rule. 
* **Report-only**: Monitor how the rule affects users without enforcing it. All attempts to access resources in the account are logged in {{site.data.keyword.at_short}}. Monitoring is recommended for 30 days before you enforce the rule.

You can monitor the impact of your enabled and report-only rules. For more information, see [Monitoring context-based restrictions](/docs/account?topic=account-cbr-monitor). 
{: tip}

## Contexts 
{: #restriction-context}

Contexts define where your resource can be accessed. A context is made up of the allowed endpoint types and network zones that you configure. 

* If a context includes network zones, then access is granted only when the request is created from within one of those zones.
* If a context includes service endpoint types, then access is granted only when the request is received over a connection that matches one of those types.
* If a context includes multiple restrictions, for example, both zones and endpoint types, then all restrictions must be satisfied for access to be granted.

### Network zone
{: #network-zones-whatis}

A network zone represents an allowlist of IP addresses where an access request is created. It defines a set of one or more network locations that are specified by the following attributes:
* IP addresses, which include individual addresses, ranges, or subnets.
* VPCs
* Service references, which allow access from other {{site.data.keyword.cloud}} services. 

#### IP addresses
{: #ip-attribute}

Customers can specify the IP addresses they know that they want to be able to send traffic from. Anything outside of the specified IP addresses is denied. 

#### VPCs
{: #vpc-attribute}

If you have apps that are deployed in a VPC that need access to a context-based restricted resource, you can include the VPC IP addresses in your network zone. To do so, you can select the target VPC in your network zone, and add that network zone to your rule. This way, you don’t have to find the IP addresses that the VPC uses. Resources that are contacted see that the request is coming from a set of allowed IP addresses.

#### Service references
{: #service-attribute}

A service reference represents the network locations of a service or service-instance. Including a service reference to a network zone adds the IP addresses associated with the service to your allowlist without requiring you to know their underlying IP addresses. This is helpful since the network locations of cloud services are unknown to the context-based restriction administrator, and can change over time.

To manage network zones, you must be assigned a specific role for the context-based restriction account management service: 
| Roles         | Actions                                                                                                |
|---------------|--------------------------------------------------------------------------------------------------------|
| Viewer        | View network zones                                               |
| Editor        | View network zones   \n  \n Create network zones   \n  \n Update network zones   \n  \n Remove network zones  |
| Administrator | View network zones   \n  \n Create network zones   \n  \n Update network zones   \n  \n Remove network zones  |
{: caption="Table 2. Roles and example actions for network zones" caption-side="top"}

For more information, see [Actions and roles for account management services](/docs/account?topic=account-account-services&interface=ui#account-management-actions-roles).

You can also use network zones to restrict access at the account level. To set account level restrictions by using network zones, go to **Manage** > **IAM** > **Settings** in the {{site.data.keyword.cloud_notm}} console and enter the name of your network zone.
{: note}

### Endpoint types
{: #context-restrictions-endpint-type}

An endpoint type represents the connection over which an access request is received. It corresponds to the endpoint that receives the connection. You can allow access from all endpoint types that are supported by the service or specific service endpoint types.

The three common endpoint types are as follows:
* Public endpoints can accept requests from anywhere.
* Private endpoints are available for most requests, that originate from within {{site.data.keyword.cloud}}.
* Direct endpoints are used in Bring-Your-Own-IP scenarios, generally for requests, that originate from resources within VPCs.

Some endpoint types might not be supported by the selected service.
{: note}

## Services integrated with context-based restrictions
{: #cbr-adopters}

Specific {{site.data.keyword.Bluemix_notm}} services are integrated with context-based restrictions, and only these services can apply rules to their resources. The way that rules apply to individual services is determined by the service, so be sure to review the documentation for each service to understand how context-based restrictions apply.

You can create context-based restrictions for the following services if you are granted the correct access on the service:

| Service       | Service type |
|---------------|---------------|
| IAM Access Groups Service  | Account Management |
| IAM Access Management Service | Account Management |
| IAM Identity Service  | Account Management |
| IAM User Management | Account Management |
| {{site.data.keyword.cos_full_notm}} | IAM-enabled |
| {{site.data.keyword.codeengineshort}} | IAM-enabled |
| {{site.data.keyword.registryshort}} | IAM-enabled |
| {{site.data.keyword.keymanagementserviceshort}} | IAM-enabled |
{: caption="Table 3. Services that are compatible with context-based restrictions." caption-side="top"}

Context-based restrictions defined for IAM-enabled services do not apply to platform actions like provision or deprovision actions. For more information, see [IAM roles and actions](/docs/account?topic=account-iam-service-roles-actions). 
{: important}

Check back regularly to see what services are added as more services integrate with context-based restrictions.
{: note} 
