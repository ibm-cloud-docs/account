---

copyright:
  years: 2023, 2025
lastupdated: "2025-07-02"

keywords: catalog, private catalogs, IAM access, Schematics service, cross accounts, target account, projects

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Setting up a target account for validation
{: #catalog-cross-validation}

If you want to use a different account to validate your product and run security and compliance scans, you can link a target account to your private catalog. You can give your catalog access to a target account by using an {{site.data.keyword.cloud_notm}} API key or trusted profile. In addition, you can link your private catalog with a project. Linking a private catalog to a project authorizes the project to create the resources in the target account rather than having them created directly by the catalog.
{: shortdesc}

Trusted profiles are the preferred method of authentication because you can securely grant access without the need for key rotation.

If you link your private catalog with a project, you still need an {{site.data.keyword.cloud_notm}} API key or a trusted profile ID to enable access.
{: note}

You might want to use a target account to validate software for the following reasons:

- Prevent the account with the product from becoming cluttered with resources that are created and deleted as part of the onboarding process
- Allow users to complete onboarding when they might not have authorization to create resources in the account that contains the product

## Before you begin
{: #catalog-cross-begin}

- Verify that you're using a Pay-As-You-Go or Subscription account. See [Viewing your account type](/docs/account?topic=account-account_settings#view-acct-type) for more details.
- Make sure that you have the [administrator role on the catalog management service](/docs/account?topic=account-account-services#catalog-management-account-management) or have the catalog administrator complete this task.
- Set up [service-to-service authorization](/docs/account?topic=account-catalog-service-authorization).
- If you want to link a private catalog with a project, you must have a catalog and a project created. For more information on creating a private catalog, see [Customizing the IBM Cloud catalog and private catalogs for users in your account](/docs/account?topic=account-restrict-by-user&interface=ui). For more information on creating a project, see [Creating a project](/docs/secure-enterprise?topic=secure-enterprise-setup-project&interface=ui).

## Using an {{site.data.keyword.cloud_notm}} API key
{: #target-api-key}

You can use an API key to give your private catalog access to validate your product and run security and compliance scans in a target account.

Alternatively, use a trusted profile to eliminate the need for key rotation. For more information, see [Using a trusted profile](/docs/account?topic=account-catalog-cross-validation#target-trusted-profile).
{: tip}



1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage > Catalogs > Private catalogs** to access your private catalogs.
1. Select the private catalog that you want to add a target account to.
1. Click **Actions...** > **Edit catalog details** > **Add** to add a target account.
1. Select **{{site.data.keyword.cloud_notm}} API key** as the method.
1. Create a programmatic name of the target account.
1. Create a display name for the target account. The display name appears as a target account option for users that are onboarding products.
1. Enter the API key from the target account. If you need an API key, see [Create an API key](/docs/account?topic=account-userapikey&interface=ui#create_user_key).
1. Select the checkbox to indicate that you set up service authorization for Schematics and Catalog Management.
1. Click **Add** > **Update**.

Users can now use the added target account to validate and add scans to any product version in the private catalog.

## Using a trusted profile
{: #target-trusted-profile}

You can use a trusted profile to authorize your private catalog to validate your product and run security and compliance scans in a target account.

### Creating a trusted profile in the target account
{: #catalog-create-profile}

Retrieve the CRN associated with your private catalog. You need this to establish trust with the trusted profile in the target account. Then, create the trusted profile in the target account where you want to validate your product and run security and compliance scans.

#### Getting the private catalog CRN
{: #catalog-get-crn}

1. In the {{site.data.keyword.cloud_notm}} console, navigate to the account where you have your private catalogs by clicking the account switcher and selecting the correct account.
1. Go to **Manage > Catalogs > Private catalogs** to access your private catalogs.
1. Select the private catalog that you want to validate in a target account.
1. Click **Actions...** > **Edit catalog details** to find the `Catalog CRN`.
1. Copy the `Catalog CRN`.

#### Creating the trusted profile
{: #catalog-create-tp}

1. In the {{site.data.keyword.cloud_notm}} console, navigate to the account where you want to validate your product by clicking the account switcher and selecting the correct account.
1. Click the **Menu** icon ![Menu icon](../icons/icon_hamburger.svg) > **Manage** > **Access (IAM)** > **Trusted profiles**.
1. Click **Create**.
1. Enter a name for the trusted profile, such as the name of your private catalog.
1. Enter a description, such as `This trusted profile authorizes a private catalog in another account to validate a product and run security and compliance scans in this account`. Then, click **Continue**.
1. Select **{{site.data.keyword.cloud}} services** and enter the `Catalog CRN` that you copied.

   {{site.data.keyword.cloud_notm}} services, like the Catalog Management service, are static identities that don't use conditions to establish trust. Instead, you establish trust by using the CRN to create a direct link between the profile and a service instance.
   {: note}

1. Click **Continue**.
1. [Assign access to the trusted profile](/docs/account?topic=account-create-trusted-profile&interface=ui#tp-access) with at least the Viewer role on the Schematic service and resource groups in the account.

   To determine any other necessary permissions for your specific use case, look at the template to see what resources it creates. For example, if the template creates VPC resources, then the trusted profile requires permission to create those VPC resources as well.
   {: tip}

   1. Select the **Schematics** service.
   1. Select **All resources** > **Next**.
   1. Select the Viewer roles and click **Next**.
   1. Click **Add**.
   1. Assign another policy with **Resource group only** and a particular resource group that is selected as well as a resource group access role assigned. Repeat this type of policy for each available resource group in the account.
      1. Select **Resource group only** > **Next**.
      1. Click **Add a condition** and select the Resource group attribute.
      1. Select a resource group and click **Next**.
      1. Select the Viewer role and click **Next**.
      1. Click **Add** and repeat these steps for all resource groups in the account.
1. Click **Create**.
1. Click **Details** and copy the Profile ID.

Now that you linked the private catalog in one account to the trusted profile in the target account, you are ready to add the target account to your private catalog.

### Adding a target account to your private catalog
{: #target-account-trusted}

The trusted profile that gives your private catalog access to create validation resources in the target account is set up. Now, add the target account to your private catalog by entering your trusted profile details so that the catalog can assume the profile and access the target account.

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage > Catalogs > Private catalogs** to access your private catalogs.
1. Select the private catalog that you want to connect to the target account where you can validate products.
1. Click **Actions...** > **Edit catalog details** > **Add** to add a target account.
1. Select **Trusted profile ID** as the method.
1. Create a unique programmatic name for the target account.
1. Create a display name for the target account. The display name appears as a target account option for users that are onboarding products.
1. Enter the profile ID of the trusted profile. If you do not have the profile ID, see [Creating the trusted profile](/docs/account?topic=account-catalog-cross-validation#target-trusted-profile).
1. Select the checkbox to indicate that you set you service authorization for Schematics and Catalog Management.
1. Select the checkbox to indicate that you created a trusted profile and added the catalog CRN as a trust relationship.
1. Click **Add** > **Update**.

Users can now use the added target account to validate and add scans to any product version in the private catalog.

## Linking an {{site.data.keyword.cloud_notm}} project ID (Optional)
{: #target-project-id}

You can configure a target account for a private catalog with a project. If you link your catalog to a project, you can synchronize the status between them. For example, when you create a new software with a specific version in your catalog, a configuration is created in your project with the same version. After you link your catalog with a project, you can validate your version either in Catalog management, or in Projects, but you need to validate it only once.

You must have a private catalog and a project that is created before you can configure a target account and link your catalog to a project. For more information on creating a private catalog, see [Customizing the IBM Cloud catalog and private catalogs for users in your account](/docs/account?topic=account-restrict-by-user&interface=ui). For more information on creating a project, see [Creating a project](/docs/secure-enterprise?topic=secure-enterprise-setup-project&interface=ui).
{: note}

To add a target account by using a project ID, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage > Catalogs > Private catalogs** to access your private catalogs.
1. Select the private catalog that you want to add a target account to.
1. Click **Actions... > Edit catalog details > Add** to add a target account.
1. Select **{{site.data.keyword.cloud_notm}} project** as the method.
1. Provide a programmatic name for the target account.
1. Provide a display name for the target account. The target account display name appears as an option for users who are validating a product version.
1. Select a project.

   If you don't have a project to select, click **Create an {{site.data.keyword.cloud_notm}} project**.
   {: tip}

1. Select the checkbox to indicate that you set up service authorization for Projects and Catalog Management.
1. Select an authentication method that the project can use to access the target account. If you don't have authentication set up yet, see [Using an {{site.data.keyword.cloud_notm}} API key](/docs/account?topic=account-catalog-cross-validation#target-api-key) or [Using a trusted profile](/docs/account?topic=account-catalog-cross-validation#target-trusted-profile).
1. Enter the API key or the trusted profile ID based on what you selected as the authentication method in the previous step.

   To find your trusted profile ID, click **Manage > Access (IAM)**, and select **Trusted profiles**. Select your trusted profile and click **Details** to find and copy your trusted profile ID.
   {: tip}

1. Select the checkbox to indicate that you set up service authorization for Schematics and Catalog Management. If you selected a trusted profile as the authentication method for your target account, you must select the checkbox to indicate that you created a trusted profile and added the catalog CRN as a trust relationship.
1. Click **Add > Update**.
