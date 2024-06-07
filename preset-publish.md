---

copyright:
  years: 2022, 2023
lastupdated: "2023-02-07"

subcollection: account

keywords: objects, private catalog, onboarding, preset configuration, object, publish preset configuration, preset

---

{{site.data.keyword.attribute-definition-list}}


# Making your preset configuration available to users
{: #publish-preset}

To make your preset configuration available to users, you must share it. You can share your preset configuration with your account, an enterprise, allowlisted accounts, or publicly to the {{site.data.keyword.cloud_notm}} catalog.
{: shortdesc}

## Before you begin
{: #before-publish-preset}

You need Editor access on the catalog that the preset configuration is in to share it. For more information, see [Assigning catalog management access](/docs/account?topic=account-catalog-access).



If you want to share your preset configuration publicly to the {{site.data.keyword.cloud_notm}} catalog, select a parent product for the preset configuration. You must have editor access to the parent product, and it must be published to the {{site.data.keyword.cloud_notm}} catalog. If you don’t select a parent, you can still share your preset configuration to your account or enterprise, but you won't be able to publish it publicly.
{: important}

## Sharing your preset configuration by using the console
{: #publish-preset-ui}
{: ui}

To share your preset configuration, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, select **Private catalogs**.
1. Select your private catalog and then select your preset configuration.
1. Click **Ready to share**.
1. Click **Share**.

    You can also click **Actions...** > **Share** to share your preset configuration.
    {: note}

1. Select your sharing preferences and then click **Share**.



## Sharing your preset configuration to your account by using the CLI
{: #publish-preset-cli}
{: cli}

Use the following steps to share your VPE to your account:

1. Share your preset configuration to your account.
   ```bash
   ibmcloud catalog object publish account [--catalog CATALOG] [--name NAME]
   ```
   {: codeblock}

   For more information about this command, enter:
   ```bash
   ibmcloud catalog object help publish account
   ```
   {: codeblock}

## Sharing your preset configuration to IBM employees by using the CLI
{: #publish-account-preset-cli}
{: cli}

1. Make your preset configuration visible to all IBM employees.
   ```bash
   ibmcloud catalog object publish ibm [--catalog CATALOG] [--name NAME]
   ```
   {: codeblock}

   For more information about this command, enter:
   ```bash
   ibmcloud catalog object help publish ibm
   ```
   {: codeblock}

## Sharing your preset configuration to all users by using the CLI
{: #publish-preset-all-cli}
{: cli}

1. Make your preset configuration visible to all {{site.data.keyword.cloud_notm}} users.
   ```bash
   ibmcloud catalog object publish public [--catalog CATALOG] [--name NAME]
   ```
   {: codeblock}

   For more information about this command, enter:
   ```bash
   ibmcloud catalog object help publish-to-public
   ```
   {: codeblock}

## Sharing your preset configuration to an access list by using the CLI
{: #publish-preset-access-cli}
{: cli}

1. Make your preset configuration visible to users in an access list.

   ```bash
   ibmcloud catalog object publish accesslist[--catalog CATALOG] [--name NAME]
   ```
   {: codeblock}

   For more information about this command, enter:
   ```bash
   ibmcloud catalog object help publish access list
   ```
   {: codeblock}
