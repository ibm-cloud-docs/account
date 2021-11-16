---

copyright:

  years: 2021

lastupdated: "2021-11-15"

keywords: troubleshooting software, troubleshooting resources, software, operator, private registry, Red Hat, Quay

subcollection: account

content-type: troubleshoot

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Why can't I pull an Operator bundle from my private registry?
{: #ts-swinstance-registry}
{: troubleshoot}

If you can't pull an Operator bundle from a private registry when you try to onboard it, check that you are using a supported private registry.
{: shortdesc}

When you try to pull an Operator bundle from a private registry, the following error message is displayed:
{: tsSymptoms}

`An unsupported private registry cannot be used to pull an Operator bundle.`

This problem occurs if the Operator bundle is in a private registry that {{site.data.keyword.cloud}} cannot contact.
{: tsCauses}

Move your Operator bundle to a support registry and try to pull the bundle again. The supported registries are [Red Hat Quay.io](https://quay.io/){: external} and [Red Hat registry](https://registry.connect.redhat.com){: external}.
{: tsResolve}
