---

copyright:
  years: 2022, 2023
lastupdated: "2023-10-09"

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

* You must be assigned the Publisher role on the Catalog Management service in the individual account itself.
* If you're managing share requests that are for the enterprise, you must be assigned the following roles:
   * Viewer role for the enterprise itself.
   * Publisher role on the Catalog Management service for the enterprise. (The Publisher role is a new role.)

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

When you accept a request, products that are shared by the requesting account are visible in the {{site.data.keyword.cloud_notm}} catalog for your account. In addition, the account that sent this request is able to see your account name.
{: note}
