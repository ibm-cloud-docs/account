---

copyright:
  years: 2021, 2023
lastupdated: "2023-10-23"

keywords: account, publish, private catalog, allowlist, external

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Publishing products to specific accounts
{: #catalog-other-publish}

If you don't want your product to be publicly available to all users in the {{site.data.keyword.cloud}} catalog but you do want certain accounts to be able to access your product, you can publish your product to specific allowlisted accounts if your product is [approved for publishing](/docs/sell?topic=sell-sw-publish&interface=ui#sw-request-approval).
{: shortdesc}

A different process is used if you want to share your product with users in your own enterprise or account or to enterprises to which you have the Editor role or higher already assigned, and it does not require approval for publishing. For more information, see [Sharing private catalog products](/docs/account?topic=account-catalog-share&interface=ui).

## Before you begin
{: #prereqs-share-enterprise}

1. Ensure that your product is [approved to publish](/docs/sell?topic=sell-sw-publish&interface=ui#sw-request-approval).

1. You must be assigned the Administrator role for the Catalog Management account management service in the same account as your product. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

1. Verify that at least one version of your product is in the `ready` state.

1. Retrieve the ID of the account that you want to publish to. For more information, see [Can I view my account ID, account type, and account number?](/docs/account?topic=account-accountfaqs#account-details).

   If you don't have access to the account, a user that does have access must share the ID with you.
   {: important}

## Publishing products to specific accounts by using the console
{: #other-publish-steps}
{: ui}

When you publish your product to specific accounts, the accounts are added to a list of IDs that are granted access to your product also known as the allowlist. Any ID that is not included in the allowlist can't access your product.

To manage the allowlist and publish your product to specific accounts, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Catalogs** > **Private catalogs**.
1. Select the private catalog where your product is located.
1. Select the product that you want to publish.
1. Click **Actions...** > **Publish**.
1. Select **Publish to a set of accounts**.
1. Select **Publish to other accounts**.
1. Click **Add accounts** > **Account**.
1. Enter the ID of the account that you want to publish your product to.

   If you are already a member of the account that you want to publish to, you can click **Add your accounts** to choose from a list.
   {: tip}

1. Click **Add** > **Publish**.

## Verifying collaborator status
{: #other-publish-verify}
{: ui}

When you publish a product to the {{site.data.keyword.cloud_notm}} catalog or to all IBM accounts, you must enter your personal access token so that your collaborator status in the repo is verified.

You must have the following minimum access to the corresponding repo for the product that you are publishing:
- Access to the repo
- Read org and team membership
- User email address

You must be a collaborator in the repos.

Your user email address must match the email address for the personal access token.

## Publishing products to specific accounts by using the CLI
{: #other-publish-steps-cli}
{: cli}

To publish your product to specific accounts, run the [ibmcloud catalog offering publish allowlist](/docs/cli?topic=cli-manage-catalogs-plugin#publish-offering-allowllist). To run the command, you must include the catalog ID where the product is located, the product name or ID, and the account IDs that you would like to add to the allowlist.

When you publish your product to specific accounts, the accounts are added to a list of IDs that are granted access to your product also known as the allowlist. Any ID that is not included in the allowlist cannot access your product.
{: note}

```bash
ibmcloud catalog offering publish allowlist [--catalog CATALOG][--offering OFFERING][--account-ids ACCOUNT-IDS].
```
{: codeblock}

### Example command
{: #other-publish-example}

Add the account ID `1` to the allowlist for the product `Product` that is located in the `A` private catalog.

```bash
ibmcloud catalog offering publish allowlist --catalog A --offering Product --account-ids 1
```
{: codeblock}
