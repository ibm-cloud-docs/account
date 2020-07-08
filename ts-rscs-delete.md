---

copyright:

  years: 2015, 2020

lastupdated: "2020-06-02"

keywords: troubleshooting services, troubleshooting resources, service problems, delete service, delete instance, delete service instance

subcollection: account

---


{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Why can't I delete my service instance?
{: #ts_service_broker}
{: troubleshoot}

You might receive an error message if you try to delete a service instance that is already deleted from the cloud controller.
{:shortdesc}

When you try to delete a service instance, the following error message is displayed:
{: tsSymptoms}

`Gateway timeout`

This problem happens if the service instance is already deleted from the cloud controller.
{: tsCauses}

Create a service instance with the same service name, and connect it to your applications. Then, you can delete the service instance and the applications that use the service.   
{: tsResolve}

