---

copyright:

  years: 2015, 2020

lastupdated: "2020-06-02"

keywords: troubleshooting services, troubleshooting resources, service problems, resource problems, resource group, move resource, reassign resource, reassign instance

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I assign my resource to a new resource group? 
{: #ts_service_instance}
{: troubleshoot}

You can't reassign an {{site.data.keyword.Bluemix}} resource to a different resource group after it has already been created.
{: shortdesc}

You don't have the option to move a resource from one resource group to another.
{: tsSymptoms}

Resources can't be moved after they are assigned to a resource group. Your resource group selection at the time of creating the instance is final and can't be changed in the platform.
{: tsCauses}

To correct this issue, you can delete the resource and create a new instance of it from the catalog. This way, you can be sure to assign the new instance to the correct resource group.
{: tsResolve}
