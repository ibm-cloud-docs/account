---

copyright:
  years: 2023
lastupdated: "2023-09-22"

keywords: catalog, private catalogs, IAM access, Schematics service, cross accounts, target account, projects

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Setting up a target account
{: #catalog-cross-validation}

If you want to use a different account to validate your product and run security and compliance scans, you can add a target account. You can add a target account by using an {{site.data.keyword.cloud_notm}} API key or a trusted profile ID. In addition, you can link your private catalog with a project, allowing the project to create the resources in the target account rather than having them created directly by the catalog. 
{: shortdesc}

You might want to use a target account for the following reasons:

- Prevent the account with the product from becoming cluttered with resources that are created and deleted as part of the onboarding process
- Allow users to complete onboarding when they might not have authorization to create resources in the account that contains the product

## Before you begin
{: #catalog-cross-begin}

1. Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.
1. Make sure that you have the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management) or have the catalog administrator complete this task.
1. Set up [service-to-service authorization](/docs/account?topic=account-catalog-catalog-service-authorization).
1. If you want to use an {{site.data.keyword.cloud_notm}} API key, [create an API key](/docs/account?topic=account-userapikey&interface=ui#create_user_key) for the target account.
1. If you want to use a trusted profile ID, see [Creating trusted profiles](/docs/account?topic=account-create-trusted-profile&interface=ui).
1. If you want to link a private catalog with a project, you must have a catalog and a project created. For more information on creating a private catalog, see [Customizing the IBM Cloud catalog and private catalogs for users in your account](/docs/account?topic=account-restrict-by-user&interface=ui). For more information on creating a project, see [Creating a project](/docs/secure-enterprise?topic=secure-enterprise-setup-project&interface=ui).

## Using an {{site.data.keyword.cloud_notm}} API key
{: #target-api-key}

You can add a target account by using an API key. Alternatively, if you would like to add a trusted profile ID, see [Using a trusted profile](/docs/account?topic=account-catalog-cross-validatione&interface=ui#target-trusted-profile).

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage > Catalogs > Private catalogs** to access your private catalogs.
1. Select the private catalog that you want to add a target account to.
1. Click **Actions...** > **Edit catalog details** > **Add** to add a target account.
1. Select **{{site.data.keyword.cloud_notm}} API key** as the method.
1. Create a programmatic name of the target account.
1. Create a display name for the target account. The display name appears as a target account option for users that are onboarding products.
1. Enter the API key for the target account. If you need an API key, see [Create an API key](/docs/account?topic=account-userapikey&interface=ui#create_user_key).
1. Click the checkbox to indicate that you set up service authorization for Schematics and Catalog Management.
1. Click **Add** > **Update**.

Users can now use the added target account to validate and add scans to any product version in the private catalog.

## Using a trusted profile
{: #target-trusted-profile}

If you want to use a trusted profile, you need to update your trusted profile to include the private catalog's CRN as a trust relationship. If you need to create a trusted profile, see [Creating trusted profiles](/docs/account?topic=account-create-trusted-profile&interface=ui).

### Updating a trusted profile
{: #update-create-profile}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage > Catalogs > Private catalogs** to access your private catalogs.
1. Select the private catalog that you want to add a target account to.
1. Click **Actions...** > **Edit catalog details** to find the `Catalog CRN`.
1. Copy the `Catalog CRN`.
1. Click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) > **Manage** > **Access (IAM)** > **Trusted profiles** to access your existing trusted profile.
1. Select the trusted profile that you want to use.
1. Click **{{site.data.keyword.cloud_notm}} services** > **Add**.
1. Enter the CRN and click **Save**.
1. Click **Details** to find the `Profile ID` of the trusted profile.
1. Copy the `Profile ID`. You use the ID to add a target account to your private catalog.

You linked the private catalog to the trusted profile as a trust relationship and are ready to add a target account.

### Adding a target account
{: #target-account-trusted}

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage > Catalogs > Private catalogs** to access your private catalogs.
1. Select the private catalog that you want to add a target account to.
1. Click **Actions...** > **Edit catalog details** > **Add** to add a target account.
1. Select **Trusted profile ID** as the method.
1. Create a unique programmatic name for the target account.
1. Create a display name for the target account. The display name appears as a target account option for users that are onboarding products.
1. Enter the profile ID of the trusted profile. If you do not have the profile ID, see [Updating a trusted profile](/docs/account?topic=account-catalog-cross-validatione&interface=ui#update-create-profile).
1. Click the checkbox to indicate that you set up service authorization for Schematics and Catalog Management.
1. Click the checkbox to indicate that you created a trusted profile and added the catalog CRN as a trust relationship.
1. Click **Add** > **Update**.

Users can now use the added target account to validate and add scans to any product version in the private catalog.

## Using an {{site.data.keyword.cloud_notm}} project ID
{: #target-project-id}

You can configure a target account for a private catalog with a project. If you link your catalog to a project, you can synchronize the status between them, for example, when you create a new software with a specific version in your catalog, a configuration is created in your project with the same version. After you link your catalog with a project, you can validate your version either in Catalog management, or in Projects, but you only need to validate it once. 

You must have a private catalog and a project created before you can configure a target account and link your catalog to a project. For more information on creating a private catalog, see [Customizing the IBM Cloud catalog and private catalogs for users in your account](/docs/account?topic=account-restrict-by-user&interface=ui). For more information on creating a project, see [Creating a project](/docs/secure-enterprise?topic=secure-enterprise-setup-project&interface=ui).
{: note}

To add a target account by using a project ID, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage > Catalogs > Private catalogs** to access your private catalogs.
1. Select the private catalog that you want to add a target account to.
1. Click **Actions... > Edit catalog details > Add** to add a target account.
1. Select **{{site.data.keyword.cloud_notm}} project** as the method.
1. Provide a programmatic name for the target account.
1. Provide a display name for the target account. The target account display name appears as an option for users who are validating a product version.
1. Enter the project ID.

   To find your project ID, in the {{site.data.keyword.cloud_notm}} console, go to the **Navigation menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") and select **Projects**. Select your project and go to the Manage tab where you can find and copy your project ID.
   {: note}

1. Click the checkbox to indicate that you set up service authorization for Projects and Catalog Management.
1. Select **{{site.data.keyword.cloud_notm}} API key** or **Trusted profile** as the authentication method for the target account that will be used by the project when it runs.
1. Enter the API key for the target account, or the trusted profile ID based on what you selected as the authentication method in the previous step.

   To find your trusted profile ID, in the {{site.data.keyword.cloud_notm}} console, go to **Manage > Access (IAM)**, and select **Trusted profiles**. Select your trusted profile and click **Details** to find and copy your trusted profile ID.
   {: note}

1. Click the checkbox to indicate that you set up service authorization for Schematics and Catalog Management. If you selected a trusted profile as the authentication method for the target account, you must click the checkbox to indicate that you created a trusted profile and added the catalog CRN as a trust relationship.
1. Click **Add > Update**.

