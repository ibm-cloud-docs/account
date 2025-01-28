---

copyright:

  years: 2021, 2025
lastupdated: "2025-01-28"

keywords: troubleshooting software, troubleshooting resources, software, operator, private registry, Red Hat, Quay

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I pull an Operator bundle from my private registry?
{: #ts-swinstance-registry}
{: troubleshoot}

If you can't pull an Operator bundle from a private registry when you try to add it to your private catalog, check that you are using a supported private registry.
{: shortdesc}

When you try to pull an Operator bundle from a private registry, the following error message is displayed:
{: tsSymptoms}

> An unsupported private registry cannot be used to pull an Operator bundle.

This problem occurs if the Operator bundle is in a private registry that {{site.data.keyword.cloud}} cannot contact.
{: tsCauses}

Move your Operator bundle to a support registry and try to pull the bundle again. The supported registries are [Red Hat Quay.io](https://quay.io/){: external} and [Red Hat registry](https://catalog.redhat.com/){: external}.
{: tsResolve}
