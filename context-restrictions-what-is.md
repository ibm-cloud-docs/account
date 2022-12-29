---

copyright:
  years: 2021, 2022
lastupdated: "2022-12-14"

keywords: Context based restriction, rule, context, network zone, IBM Cloud restrictions, IBM Cloud context restriction, IBM Cloud access, access control, resource access, Cloud Foundry, endpoint type

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# What are context-based restrictions?
{: #context-restrictions-whatis}

Context-based restrictions give account owners and administrators the ability to define and enforce access restrictions for {{site.data.keyword.cloud}} resources based on a rule's criteria. The criteria include the network location of access requests, the endpoint type from where the request is sent, and sometimes the API that the request tries to access. These restrictions work with traditional IAM policies, which are based on identity, to provide an extra layer of protection. Since both IAM policies and context-based restrictions enforce access, context-based restrictions offer protection even in the face of compromised or mismanaged credentials.
{: shortdesc}

For an example scenario on creating context-based restrictions, follow the tutorial for [Leveraging context-based restrictions to secure your resources](/docs/account?topic=account-context-restrictions-tutorial).

![A diagram that shows how context-based restrictions work.](images/CBR-diagram.svg){: caption="Figure 1. A diagram that shows how context-based restrictions work." caption-side="bottom"}

## Rules
{: #restriction-rules}
{: #context-restrictions-rule-whatis}

A rule associates an {{site.data.keyword.cloud_notm}} resource with a set of contexts:
* The cloud resource is specified by resource attributes similar to IAM access policies.
* A context is a combination of network zones and endpoint types.

The contexts that you configure define the restrictions for the associated resources.

The necessary resource attributes in context-based restrictions rules are `accountId` and `serviceName`. Rules must be scoped to an account and a specific service.
{: note}

Context-based restriction rules are applied by the following logic:
* Access is granted by a rule only when at least one of the rule's contexts allows access.
* If multiple rules are applicable to a particular resource, access is granted only when all applicable rules allow access.
* If no rules are applicable to a particular resource, access is determined exclusively by IAM policies.

Unlike IAM policies, context-based restrictions don't assign access. Context-based restrictions check that an access request comes from an allowed context that you configure.
{: note}

### Rule enforcement
{: #rule-enforcement}

You can decide how you want to enforce a rule upon creation and update the rule enforcement at any time.

Enabled
:   Enforce the rule. Depending on the service that you select, monitoring denied access attempts through {{site.data.keyword.at_short}} might be available. Review each service's documentation to learn about how they integrate with context-based restrictions.

Disabled
:   No restrictions apply to your account resources. Select this option if you're not ready to enable the rule.

Report-only
:   Depending on the service that you select, you can monitor how the rule affects access without enforcing it. With report-only mode, all attempts to access resources in the account are logged in {{site.data.keyword.at_short}}. Monitoring is recommended for 30 days before you enforce the rule. Review each service's documentation to learn about how they integrate with context-based restrictions.

You can monitor the impact of your enabled and report-only rules. For more information, see [Monitoring context-based restrictions](/docs/account?topic=account-cbr-monitor).
{: tip}

### Defining the scope of a rule
{: #rule-scope}

Define the APIs that you want to protect to narrow the scope of a rule's restrictions. This way, you can specify granular protections for different APIs that have distinct access requirements.

For example, you might create a rule that targets a data plane API so that it is only accessible from a Kubernetes cluster, or wherever your compute infrastructure exists. Then, you can create a rule that targets your control plane API that interacts with the cloud console so that it is only accessible from behind your organization's VPN.

Only some services support the ability to scope a rule by API.
{: preview}

With some services, you can restrict the actions of all APIs on your resources by default, which includes all current and future APIs that the service might support. Or, select specific APIs. For example, [Kubernetes](/docs/containers?topic=containers-cbr&interface=ui#cbr-overview) has custom service APIs that you can restrict access to based on the context of the request. Review each service's documentation to learn more about how they integrate with context-based restrictions.

You can also skip APIs to restrict all operations on the service that you select.
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
* Service references, which allow access from other {{site.data.keyword.Bluemix}} services.

#### IP addresses
{: #ip-attribute}

Customers can specify the IP addresses they know that they want to be able to send traffic from. Anything outside of the specified IP addresses is denied.

#### VPCs
{: #vpc-attribute}

If you have apps that are deployed in a VPC that need access to a context-based restricted resource, you can include the VPC IP addresses in your network zone. To do so, select the target VPC in your network zone and add that network zone to your rule. This way, you don’t have to find the IP addresses that the VPC uses. Resources that are contacted see that the request is coming from a set of allowed IP addresses.

#### Service references
{: #service-attribute}

A service reference represents the network locations of a service or service instance. Including a service reference in a network zone adds the IP addresses associated with the service to your allowlist without requiring you to know the service's underlying IP addresses. Service references are helpful since the network locations of cloud services are unknown to the context-based restriction administrator and can change over time.

The following is a list of services that you can add to a network zone as a service reference:
| Service       | Service type |
|---------------|--------------|
| All Account Management services | Account Management |
| IAM Access Groups Service  | Account Management |
| IAM User Management | Account Management |
| Cloud {{site.data.keyword.block_storage_is_short}} | IAM-enabled |
| [Cloud {{site.data.keyword.cos_short}}](/docs/cloud-object-storage?topic=cloud-object-storage-setting-a-firewall) | IAM-enabled |
| [{{site.data.keyword.codeengineshort}}](/docs/codeengine?topic=codeengine-cbr) | IAM-enabled |
| {{site.data.keyword.dl_short}} | IAM-enabled |
| [{{site.data.keyword.messagehub}}](/docs/EventStreams?topic=EventStreams-restrict_access#configuring_cbr) | IAM-enabled |
| [{{site.data.keyword.containershort}}](/docs/containers?topic=containers-cbr&interface=ui) | IAM-enabled |
| [VPC Infrastructure Services](/docs/vpc?topic=vpc-cbr&interface=cli#network-zone) | IAM-enabled |
{: caption="Table 1. Services that are compatible with service references." caption-side="top"}

Refer to each service offering's documentation for more information about which services to add as a service reference for the service offering that you target in a rule.
{: important}


### Endpoint types
{: #context-restrictions-endpint-type}

An endpoint type represents the connection over which an access request is received. It corresponds to the endpoint that receives the connection. You can allow access from all endpoint types that are supported by the service or specific service endpoint types.

The three common endpoint types are as follows:
* Public endpoints can accept requests from anywhere.
* Private endpoints are available for most requests, that originate from within {{site.data.keyword.cloud}}.
* Direct endpoints are used in Bring-Your-Own-IP scenarios, generally for requests, that originate from resources within VPCs.

Some endpoint types might not be supported by the selected service.
{: note}

## Access requirements
{: cbr-access-reqs}

To complete rule actions, you must be assigned an IAM policy on the target service. To complete network zone actions, you must be assigned an IAM policy on the context-based restrictions service.

To create a context-based restriction for a service, you must be assigned an IAM policy with the Administrator role the service you are creating a rule against. For example, if you want to create a rule to protect a **Key Protect** instance, you must be assigned the Administrator role on the **Key Protect** service and the Viewer role or higher on the Context-based restrictions** service.

The Viewer role on the Context-based restrictions service authorizes you to add network zones to your rule.
{: tip}

### Context-based restrictions roles and actions
{: cbr-access-reqs-cbr-restrict}

To manage network zones, you must be assigned an IAM policy with a specific role for the Context-based restrictions account management service. The following table shows the possible access roles and actions for account management.

| Roles         | Actions                                                                                                |
|---------------|--------------------------------------------------------------------------------------------------------|
| Viewer        | View network zones|
| Editor        | View network zones   \n  \n Create network zones   \n  \n Update network zones   \n  \n Remove network zones  |
| Administrator | View network zones   \n  \n Create network zones   \n  \n Update network zones   \n  \n Remove network zones |
{: caption="Table 2. Roles and actions for the Context-based restrictions service" caption-side="top"}

For more information, see [Actions and roles for account management services](/docs/account?topic=account-account-services&interface=ui).

You can also use network zones to restrict access at the account level. To set account-level restrictions by using network zones, go to **Manage** > **IAM** > **Settings** in the {{site.data.keyword.cloud_notm}} console and enter the name of your network zone.
{: note}

### Target service roles and actions
{: #cbr-access-reqs-target-service}

To manage rules, you must be assigned an IAM policy with the Administrator role for the service that you are creating the rule against. The following table shows the possible access roles and actions for services.

| Roles         | Actions                                                                                                |
|---------------|--------------------------------------------------------------------------------------------------------|
| Viewer        | View rules |
| Editor        | View rules |
| Administrator | View rules   \n  \n Create rules   \n  \n Update rules   \n  \n Remove rules |
{: caption="Table 3. Roles and example actions for target service" caption-side="top"}


## Services integrated with context-based restrictions
{: #cbr-adopters}

Specific {{site.data.keyword.Bluemix_notm}} services are integrated with context-based restrictions, and only these services can apply rules to their resources. The way that rules apply to individual services is determined by the service, so be sure to review the documentation for each service to understand how context-based restrictions apply.

You can create context-based restrictions for the following services if you are granted the correct access on the service:

| Service       | Service type | Scope to APIs | `service_name` |
|---------------|--------------|---------------|----------------|
| IAM Access Groups Service  | Account Management | No | `iam-groups` |
| IAM Access Management Service | Account Management | No | `iam-access-management` |
| IAM Identity Service  | Account Management | No | `iam-identity`|
| IAM User Management | Account Management | No | `user-management` |
| [Cloud {{site.data.keyword.cos_short}}](/docs/cloud-object-storage?topic=cloud-object-storage-setting-a-firewall) | IAM-enabled | No | `cloud-object-storage` |
| [{{site.data.keyword.codeengineshort}}](/docs/codeengine?topic=codeengine-cbr) | IAM-enabled | No | `codeengine` |
| [{{site.data.keyword.registryshort}}](/docs/Registry?topic=Registry-iam&interface=ui#iam_cbr) | IAM-enabled | No | `container-registry` |
| [{{site.data.keyword.databases-for-cassandra}}](/docs/cloud-databases?topic=cloud-databases-cbr) | IAM-enabled | Yes | `databases-for-cassandra` |
| [{{site.data.keyword.databases-for-enterprisedb}}](/docs/cloud-databases?topic=cloud-databases-cbr) | IAM-enabled | Yes | `databases-for-enterprisedb` |
| [{{site.data.keyword.databases-for-elasticsearch}}](/docs/cloud-databases?topic=cloud-databases-cbr) | IAM-enabled | Yes | `databases-for-elasticsearch` |
| [{{site.data.keyword.databases-for-etcd}}](/docs/cloud-databases?topic=cloud-databases-cbr) | IAM-enabled | Yes | `databases-for-etcd` |
| [{{site.data.keyword.databases-for-mongodb}}](/docs/cloud-databases?topic=cloud-databases-cbr) | IAM-enabled | Yes | `databases-for-mongodb` |
| [{{site.data.keyword.databases-for-mysql}}](/docs/cloud-databases?topic=cloud-databases-cbr) | IAM-enabled | Yes | `databases-for-mysql` |
| [{{site.data.keyword.databases-for-postgresql}}](/docs/cloud-databases?topic=cloud-databases-cbr) | IAM-enabled | Yes | `databases-for-postgresql` |
| [{{site.data.keyword.databases-for-redis}}](/docs/cloud-databases?topic=cloud-databases-cbr) | IAM-enabled | Yes | `databases-for-redis` |
| [{{site.data.keyword.messagehub}}](/docs/EventStreams?topic=EventStreams-restrict_access#configuring_cbr) | IAM-enabled | No | `messagehub` |
| [{{site.data.keyword.keymanagementserviceshort}}](/docs/key-protect?topic=key-protect-access-control-with-cbr) | IAM-enabled | No | `kms` |
| [{{site.data.keyword.containershort}}](/docs/containers?topic=containers-cbr&interface=ui) | IAM-enabled | Yes | `containers-kubernetes` |
| [{{site.data.keyword.messages-for-rabbitmq}}](/docs/cloud-databases?topic=cloud-databases-cbr)  | IAM-enabled | Yes | `messages-for-rabbitmq` |
| [{{site.data.keyword.secrets-manager_short}}](/docs/secrets-manager?topic=secrets-manager-access-control-cbr) | IAM-enabled | No | `secrets-manager` |
{: caption="Table 4. Services that are compatible with context-based restrictions." caption-side="top"}


Context-based restrictions that are defined for IAM-enabled services do not apply to platform actions like create or delete. For more information, see [IAM roles and actions](/docs/account?topic=account-iam-service-roles-actions).
{: important}

Check back regularly to see what services are added as more services integrate with context-based restrictions.
{: note}
