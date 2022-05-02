---

copyright:
  years: 2021, 2022
lastupdated: "2022-05-02"

keywords: enterprise, share, private catalog, allowlist

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Sharing products with users in your account, enterprise, or account groups
{: #catalog-enterprise-share}

As a member of an enterprise, you can share products in your private catalog with users in your account, enterprise, or account groups within your enterprise. By sharing your product, you allow anyone within the account, enterprise, or account groups to create an instance of your product. 
{: shortdesc}

## Before you begin
{: #prereqs-enterprise-share}

1. You must be assigned the following permissions. For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).
   - Editor role for the Enterprise account management service in the enterprise account.
   - Administrator role for the Catalog Management account management service in the same account as your product.
1. Verify that at least one version of your product is in the `ready` state.

## Sharing your product
{: #ent-share-steps}

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
