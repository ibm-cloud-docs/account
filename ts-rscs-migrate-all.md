---

copyright:

  years: 2015, 2026
lastupdated: "2026-11-11"

keywords: troubleshooting services, troubleshooting resources, service problems, resource problems, migrate, migration error, migrate all services

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I migrate all services to a resource group? 
{: #ts_service_migration}
{: troubleshoot}

You can't migrate some {{site.data.keyword.cloud_notm}} services to a resource group because they don't support IAM. Look for the Migrate icon to check eligibility.
{: shortdesc}

You're unable to migrate certain services.  
{: tsSymptoms}

Services that can't be added to resource groups and aren't managed by using Identity and Access Management (IAM) can't be migrated. If a service is not eligible, there isn't an option for migration. 
{: tsCauses}

Check the services to confirm they're eligible for migration. You receive a notification and a **Migrate** icon ![Migrate icon](../icons/migrate.svg "Migrate this service instance to a resource group") is displayed to indicate if a service is eligible for migration.
{: tsResolve}
