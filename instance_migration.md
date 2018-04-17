---

copyright:

  years: 2017, 2018

lastupdated: "2018-04-17"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}

# Migrating Cloud Foundry service instances to a resource group
{: #migrate}

As services move from using Cloud Foundry orgs, spaces, and roles to using Cloud Identity and Access Management (IAM) and resource groups, you will be notified on your dashboard. When a service moves off Cloud Foundry, you are prompted to migrate your existing service instances that belong to an org and space into a [resource group](/docs/account/resourcegroups.html#rgs). 

When you migrate existing Cloud Foundry service instances to a resource group, the group assignment that you make can't be changed after the migration is final. So, you must be sure of your decision about how you want to organize resources in the account before you migrate. This might mean that you need to create one or more resource groups, if you have a paid account, before migrating.
{: tip}

## Why migrate my service instances?

Services that support using Cloud IAM have several benefits including the ability to connect to apps and services in any Cloud Foundry space, which allows you to connect apps and services from different regions. In addition, each instance managed by Cloud IAM belongs to a resource group, and resource groups are not scoped by region, so you can provision apps and services from different regions into the same resource group. You also have the ability to use fine-grained access control down to an individual instance.
 

## How does migration work?

Migrating a service instance from a Cloud Foundry org and space into a resource group creates a new linked service instance in the resource group. The original instance in the Cloud Foundry org and space becomes an [alias](/docs/cfapps/connecting_apps.html#what_is_alias).

You can migrate your service instances one at a time when you are notified on the dashboard by an icon associated with your Cloud Foundry service instance, or the message on the service details page that can take you directly to the wizard that walks you through the process. Before you migrate, make a decision about how you want to organize your resources, then you can choose an eligible service instance by using the **Actions** menu on the dashboard, and selecting **Migrate to a resource group**. You select a resource group to migrate the instance to during the process. After you have successfully migrated an instance, you see it reflected in the Services section of your dashboard. The alias remains in the Cloud Foundry section of the dashbaord. 
