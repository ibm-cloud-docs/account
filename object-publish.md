---

copyright:
  years: 2021, 2022
lastupdated: "2022-12-06"

subcollection: account

keywords: objects, private catalog, onboarding, vpe objects, publish vpe objects, vpe

---

{{site.data.keyword.attribute-definition-list}}


# Sharing your Virtual Private Endpoint
{: #publish-object}

You can share your VPE with your account, allowlisted accounts, or publicly to the {{site.data.keyword.cloud_notm}} catalog. For more information, see [Sharing objects from your private catalog](/docs/account?topic=account-sharing-access-services).
{: shortdesc}

## Before you begin
{: #before-publish-object}

Before you share your object, make sure you [validate your object's data format](/docs/get-coding?topic=get-coding-vpe-onboarding-platform#validate-vpe-object).

## Sharing your VPE by using the console
{: #publish-object-ui}
{: ui}

Use the following steps to share your VPE:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Catalogs**, and select **Objects**.
1. Select your VPE.
1. Click **Ready to share**.
1. Click **Share**.

    You can also click **Actions...** > **Share** to share your VPE.
    {: note}

1. Select your sharing preferences, then, click **Share**.






## Sharing your VPE to your account by using the CLI
{: #publish-object-cli}
{: cli}

Use the following steps to share your VPE to your account:

1. Share your VPE to your account.
   ```bash
   ibmcloud catalog object publish account [--catalog CATALOG] [--name NAME]
   ```
   {: codeblock}

   For more information about this command, enter:
   ```bash
   ibmcloud catalog object help publish account
   ```
   {: codeblock}

## Sharing your VPE to IBM employees by using the CLI
{: #publish-account-cli}
{: cli}

1. Make your VPE visible to all IBM employees.
   ```bash
   ibmcloud catalog object publish ibm [--catalog CATALOG] [--name NAME]
   ```
   {: codeblock}

   For more information about this command, enter:
   ```bash
   ibmcloud catalog object help publish ibm
   ```
   {: codeblock}

## Sharing your VPE to all users by using the CLI
{: #publish-all-cli}
{: cli}

1. Make your VPE visible to all {{site.data.keyword.cloud_notm}} users.
   ```bash
   ibmcloud catalog object publish public [--catalog CATALOG] [--name NAME]
   ```
   {: codeblock}

   For more information about this command, enter:
   ```bash
   ibmcloud catalog object help publish-to-public
   ```
   {: codeblock}

## Sharing your VPE to an access list by using the CLI
{: #publish-access-cli}
{: cli}

1. Make your VPE visible to users in an access list.

   ```bash
   ibmcloud catalog object publish accesslist[--catalog CATALOG] [--name NAME]
   ```
   {: codeblock}

   For more information about this command, enter:
   ```bash
   ibmcloud catalog object help publish access list
   ```
   {: codeblock}
