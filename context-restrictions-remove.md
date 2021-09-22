---

copyright:

  years: 2021

lastupdated: "2021-09-23"

keywords: remove restrictions, delete restrictions, delete network access, delete context based restrictions, remove network access, rule, context, network access rule, network zone

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:pre: .pre}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Removing context-based restrictions
{: #context-restrictions-remove}

By removing context-based restrictions, you delete restrictions that are defined by the contexts in a rule. Deleting rules removes context-based restrictions from the given resource, and requests from any context are allowed if the user has the correct permissions.
{: shortdesc}

## Removing a rule
{: #context-restrictions-remove-rules}

You can remove a rule on your cloud resources by completing the following steps: 
1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Context-based restrictions**, and select **Rules**.
2. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") in the row that contains the rule, and click **Remove**.

## Removing a network zone
{: #network-zones-remove}

Removing a network zone removes the set of allowed network locations from which an access request is created. If a network zone is added to a rule, you can't remove it. 

To remove a network zone, complete the following steps: 
1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Network-based access**, and select **Network zones**.
2. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") in the row that contains the network zone, and click **Remove**.
