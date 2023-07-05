---

copyright:
  years: 2023
lastupdated: "2023-07-05"

keywords: catalog, private catalogs, IAM access, Schematics service, cross accounts, target account

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Setting up authorization for target account support
{: #catalog-service-authorization}

When onboarding software to a private catalog, you are required to validate the software and provide proof for any security and compliance claims by adding scans. You can choose to complete these steps in an account other than the account that contains your product also known as a target account. Before you can use a target account, you must set up authorization.
{: shortdesc}

You might want to use a target account for the following reasons:

- prevent the account that contains the product from becoming cluttered with resources that are being created and deleted as part of the validation and scanning processes

- allow users to complete onboarding when they might not have authorization to create resources in the account that contains the product

## Before you begin
{: #prereq-auth}

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.

1. Verify that you have the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management) or have the catalog administrator set up authorization.

## Setting up authorization
{: #catalog-auth-step}

1. Log in to the {{site.data.keyword.cloud_notm}} account that contains the product.
1. Go to **Manage** > **Access (IAM)** > **Authorizations** > **Create**.
1. For source account, select **This account** to indicate that you are giving access to the account with the product.
1. For source service, select **Schematics**. You can leave **All resources** selected.
1. For target service, select **Catalog management**.
1. If you want to grant access to all your catalogs, you can move on to the next step. If you want to limit access to a specific catalog, select **Resources based on selected attributes** > **Catalog** and then choose your catalog from the `Value` menu.
1. For platform access, select **Viewer**.
1. Click **Authorize** to finalize the authorization.

You are ready to add a target account for validation and security and compliance center scans. For more information, see [Using cross account support for validation](/docs/account?topic=account-catalog-cross-validation&interface=ui).
