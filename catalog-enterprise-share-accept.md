---

copyright:
  years: 2022, 2023
lastupdated: "2023-09-14"

keywords: enterprise, share, private catalog, allowlist, account groups, share request, accept request, opt in

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Accepting share requests for private catalog products
{: #catalog-share-accept}

You can accept requests from other accounts that share products from their private catalog to your account. You can then create an instance of the product in your private catalog.
{: shortdesc}

When you accept a share request, products that are shared by the requesting account are visible in the {{site.data.keyword.cloud}} catalog for your account. When you accept the request, you are opting in to having access to future products that are shared by the same requesting account. The share request is per catalog type (Product or Virtual Private Endpoint) in an account, not for individual products.

## Before you begin
{: #prereqs-enterprise-share}

* You must be assigned the Administrator role on the Catalog Management service in the individual account itself.
* You must be assigned the Editor role for the enterprise itself if you're managing share requests that are for the enterprise.

For more information, see [Assigning users access](/docs/account?topic=account-catalog-access).

## Accepting or denying a share request by using the console
{: #ent-share-steps-accept}
{: ui}

Complete the following steps to accept a share request for a product:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Catalogs** > **Share requests**.
1. Select the catalog type for the requests that you want to manage. Possible catalog types are Product or Virtual Private Endpoint.
1. The list of share requests from other accounts to your account is displayed in the Received requests table.
1. For any requests that are in the `Pending` state, click either **Accept** or **Deny**.
   - When you click **Accept**, the request state changes from `Pending` to `Accepted`, and the product is visible in your account.
   - When you click **Deny**, the request state changes to `Denied`.
