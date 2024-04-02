---

copyright:

  years: 2021, 2024

lastupdated: "2024-04-02"

keywords: trusted profile, generating IAM token, compute resource, kubernetes cluster, virtual server

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Generating an IAM token for a compute resource
{: #trusted-profile-iam-token}

You can request an Identity and Access Management (IAM) token for a trusted profile that represents your compute resource. The IAM access token is suitable for use as a bearer token in calls that require user or service credentials.
{: shortdesc}

To generate IAM tokens for your compute resources, you must be at least an administrator on **All Identity and Access enabled services** within the account.

## {{site.data.keyword.containershort_notm}}
{: #kub-token}

For {{site.data.keyword.containerlong}}, you don't need to take steps to generate an IAM token from a compute resource (CR) token. The token generation is done automatically by the service for new clusters that run Kubernetes version 1.21 or later. Trusted profiles are not supported for earlier versions of Kubernetes. See [Authorizing pods in your cluster to IBM Cloud services with IAM trusted profiles](/docs/containers?topic=containers-pod-iam-identity) for more information.

## {{site.data.keyword.openshiftshort}}
{: #rhos-token}

Give application pods that run in your {{site.data.keyword.openshiftlong}} cluster access to IBM Cloud services by creating a trusted profile. For more information, see [Authorizing pods in your cluster to IBM Cloud services with IAM trusted profiles](/docs/openshift?topic=openshift-pod-iam-identity&interface=ui).

## {{site.data.keyword.vsi_is_short}}
{: #vsi-token}

{{site.data.keyword.vsi_is_short}} uses different APIs for token creation. For more information, see [Using a trusted profile to call IAM-enabled services](/docs/vpc?topic=vpc-imd-trusted-profile-metadata).
