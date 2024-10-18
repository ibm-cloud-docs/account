---

copyright:
  years: 2021, 2024
lastupdated: "2024-09-26"

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

## Installing the {{site.data.keyword.cloud_notm}} Catalog command-line plug-in
{: #install-command-line-cli}
{: cli}

Install the {{site.data.keyword.cloud_notm}} Catalog plug-in to manage private catalogs, manage your offerings, and explore products in the {{site.data.keyword.cloud_notm}} catalog.

1. Install the {{site.data.keyword.cloud_notm}} Catalog command-line plug-in.
    ```sh
    ibmcloud plugin install catalogs-management
    ```
    {: pre}

1. Verify that you can use the catalogs-management command-line plug-in by listing all supported commands. The command prefix to work with the catalogs-management command-line plug-in is `ibmcloud catalog`.
    ```sh
    ibmcloud catalog help
    ```
    {: pre}

    Example output 
    ```text
    NAME:
    ibmcloud catalog - Manage catalog

    USAGE:
    ibmcloud catalog command [arguments...] [command options]

    COMMANDS:
    account                Account commands
    blocklist              Add the targeted account to the blocklist of the specified service
    create                 Create a new catalog. It will use the currently targeted group.
    delete                 Delete a catalog
    entry                  Get a catalog entry
    entry-copy             Create duplicate of existing entry, with ability to change key fields.
    entry-create           Create a new catalog entry(catalog admin of an account only)
    entry-delete           Delete a catalog entry(catalog admin of an account only)
    entry-update           Update an existing catalog entry(catalog admin or editor of an account only)
    entry-visibility       Get the visibility for a catalog entry(catalog admin of an account only)
    entry-visibility-set   Update the visibility of an existing catalog entry (catalog admin of an account only)
    filter                 View and Modify account and catalog filters.
    get                    Get catalog details
    install                Install a software version.
    list                   List catalogs
    locations              Get Choice Subset of Regions in Choice of Format
    netrc                  Create or refresh the token in your .netrc file. This token is used by Terraform when referencing modules in the catalog.
    object                 View and modify objects.
    offering               View and Modify offering.
    pricing                Get pricing information for catalog offerings
    search                 search the public catalog for published offerings. This includes managed services, software, and software published from your own account.
    service                Show details of a service catalog entry
    service-marketplace    List service offerings in the marketplace
    target-account         Manage catalog target accounts.
    utility                Utility commands
    help, h                Show help

    Enter 'ibmcloud catalog help [command]' for more information about a command
        ```
    {: screen}

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

You must verify collaborator status if you are trying to publish a module from an approved IBM repository into the public catalog. To verify collaborator status in the approved repo, you must provide your personal access token.

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
