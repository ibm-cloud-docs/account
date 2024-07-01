---

copyright:
  years: 2023
lastupdated: "2023-07-25"

keywords: troubleshoot IAM, enterprise-managed, IAM, access group, trusted profile, settings, IAM locked
subcollection: account

content-type: troubleshoot
---

{{site.data.keyword.attribute-definition-list}}

# How do I know if an IAM resource is managed by the enterprise?
{: #ts_enterprise_managed}
{: troubleshoot}

You aren't sure if an IAM resource, like an access group, trusted profile, or account setting, is enterprise-managed.
{: shortdesc}

You can't update an IAM resource in your account.
{: tsSymptoms}

Your account has enabled enterprise-managed IAM and is eligable to be assigned templated IAM resources, like access groups, trusted profiles, or account settings. Some of the actions you can usually take on an IAM resource might be blocked due to action controls set on the enterprise-managed IAM resource in your account.
{: tsCauses}

Check the IAM resource to see if it is enterprise-managed.
{: tsResolve}

**In the {{site.data.keyword.Bluemix}} console**
Use the {{site.data.keyword.Bluemix}} console to determine that an IAM resource comes from an enterprise IAM template.

1. In the {{site.data.keyword.Bluemix}} console, go to **Manage > Access (IAM)**.
1. Click **Access groups**, **Trusted profiles**, or **Settings**.
1. You can determine that an IAM resource comes from an enterprise IAM template by the [enterprise-managed]{: tag-cyan} tag on the access group, trusted profile, or account setting.

**Using the API**
You can also determine that an IAM resource comes from an enterprise IAM template by using the API.

1. Retreive an access group by calling the [IAM Access Groups API](/apidocs/iam-access-groups) or trusted profiles and settings by calling the [IAM Identity API](/apidocs/iam-identity-token-api).
1. IAM resources that return the `template` attribute in the response body are enterprise-managed.

For more information, see [Opting-in to enterprise-managed IAM](/docs/secure-enterprise?topic=secure-enterprise-enterprise-managed-opt-in&interface=ui) and [How enterprise-managed IAM access works](/docs/secure-enterprise?topic=secure-enterprise-access-enterprises&interface=ui#how-enterprise-iam).
