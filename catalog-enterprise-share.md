---

copyright:
  years: 2022, 2023
lastupdated: "2023-02-01"

keywords: enterprise, share, private catalog, allowlist

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Sharing products with users in your account, enterprise, or account groups
{: #catalog-enterprise-share}

As a member of an enterprise, you can share products in your private catalog with users in your account, enterprise, or account groups within your enterprise. By sharing your product, any user within the account, enterprise, or account groups can create an instance of your product.
{: shortdesc}

## Before you begin
{: #prereqs-enterprise-share}

1. You must be assigned the following access. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).
   - Editor role for the Enterprise account management service in the enterprise account.
   - Administrator role for the Catalog Management account management service in the same account as your product.
1. Verify that at least one version of your product is in the `ready` state.

## Sharing your product by using the console
{: #ent-share-steps}
{: ui}

When you share a product with users in your account, enterprise, or account groups, they can create instances of any version that is validated and in the `ready` state. Versions that are in the `draft` state are not shared with users. Complete the following steps to share your product:

1. In the {{site.data.keyword.cloud}} console, click **Manage** > **Catalogs** > **Private catalogs**.
1. Select the private catalog where your product is located.
1. Select the product that you want to share.
1. Click **Actions...** > **Share**.
1. Review the list of affected versions.

   If you don't see the version that you want to share, make sure that the version is in the `ready` state.
   {: tip}

1. Select one of the following options:
   - **Share to this account**.
   - **Share to this enterprise or account groups**. Then, select the enterprise or account groups within the enterprise.
1. Click **Share**.

## Sharing your product by using the CLI
{: #ent-share-cli}
{: cli}

When you share a product with users in your account, enterprise, or account groups, they can create instances of any version that is validated and in the `ready` state. Versions that are in the `draft` state are not shared with users.

Run the [`ibmcloud catalog offering publish enterprise`](/docs/cli?topic=cli-manage-catalogs-plugin#publish-offering-enterprise) command to share your product to your enterprise:

   ```bash
   ibmcloud catalog offering publish enterprise [--catalog CATALOG][--offering OFFERING]
   ```
   {: codeblock}

Run the [`ibmcloud catalog offering publish allowlist`](/docs/cli?topic=cli-manage-catalogs-plugin#publish-offering-allowllist) command to share your product to an allowlisted set of accounts:

   ```bash
   ibmcloud catalog offering publish allowlist [--catalog CATALOG][--offering OFFERING][--account-ids ACCOUNT-IDS]
   ```
   {: codeblock}

The `ibmcloud catalog offering publish allowlist` command shares your product with a set of accounts based on the account IDs listed in the command. If you add an account that is external to your enterprise or your own account, the account is added to your allowlist, but your product is not shared to that account. You must have [publishing approval for your product](/docs/sell?topic=sell-sw-publish&interface=ui#sw-request-approval) to publish it to accounts outside of your enterprise or your own account.
{: note}
