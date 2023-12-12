---

copyright:
  years: 2023
lastupdated: "2023-12-12"

keywords: catalog, private catalogs, IAM access, Schematics service, cross accounts, target account

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Setting up authorization for validation in a target account
{: #catalog-service-authorization}

When onboarding software to a private catalog, you are required to validate the software and provide proof for any security and compliance claims by adding scans. You can choose to complete these steps in an account other than the account that contains your product, which is known as a target account. Before you can use a target account for validation, you must set up a service to service authorization. The authorization must grant the Schematics service in the target account access to the catalog management service in the account that contains your product.
{: shortdesc}

You might want to use a target account to validate software for the following reasons:

- Prevent the account with the product from becoming cluttered with resources that are created and deleted as part of the onboarding process
- Allow users to complete onboarding when they might not have authorization to create resources in the account that contains the product

## Before you begin
{: #prereq-auth}

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.

1. Verify that you have the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management) or have the catalog administrator set up authorization.

## Setting up authorization
{: #catalog-auth-step}

Set up an authorization in the account that contains your product. The authorization grants the Schematics service in another account access to your product.

In a service to service authorization, the source service is the service that needs access to the target service. The source service is the Schematics service in another account, which needs access to the catalog management service in the account that contains your product. The authorization allows Schematics to fetch the source URL from your product's version.

### Getting the source account ID
{: #account-id-cm}

1. Log in to the {{site.data.keyword.cloud_notm}} account where you want to validate your product.
1. Go to **Manage > Account > Account settings**.
1. Copy the 32 character account ID.

Save the account ID for the next steps in creating the authorization.

### Creating the authorization
{: #cm-schematics-auth}

1. Use the account switcher to go to the account that contains your product.
1. Go to **Manage** > **Access (IAM)** > **Authorizations** > **Create**.
1. Select **Another account** for the source account.
1. Enter the 32 character account ID that you copied in [Getting the source account ID](/docs/account?topic=account-catalog-service-authorization#account-id-cm).
1. Select **Schematics** for the source service.
1. Select **Catalog management** for the target service.
1. Limit access to a specific catalog by selecting **Resources based on selected attributes** > **Catalog**. Then, choose your catalog from the Value menu. Move on to the next step if you want to grant access to all of your catalogs.
1. Select **Viewer** for platform access.
1. Click **Authorize** to finalize the authorization.

Now, the Schematics service in the target account has Viewer access to the catalog in the account that contains your product. This allows Schematics to fetch the source URL from your product's version. Next, you are ready to give your catalog permissions to create the Schematics workspace in the target account by [Setting up a target account for validation](/docs/account?topic=account-catalog-cross-validation&interface=ui). Then, you can add the target account to your catalog for validation and security and compliance center scans.
