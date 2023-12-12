---

copyright:
  years: 2023
lastupdated: "2023-12-12"

keywords: enterprise, share, private catalog, allowlist, account groups, share request, opt in, visibility

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Visibility of products in public and private catalogs
{: #catalog-share-overview}

Learn about managing and sharing products from your private catalog and using products that are available in the {{site.data.keyword.cloud}} catalog. Learn why some product tiles are not visible to you, depending on your IAM access and the state of product versions.
{: shortdesc}

When you use {{site.data.keyword.cloud_notm}} products (deployable architectures, Helm charts, Operators, VSI images, VMware images), you typically use them from the {{site.data.keyword.cloud_notm}} catalog, where you can filter and search the product tiles that you want to work with.

When you create, edit, or manage software products, you do this from a private catalog. You share your product from a private catalog. You don't share catalogs or versions of a product.

Catalog access is governed with [IAM](/iam/roles){: external}. Users who have Editor, Viewer, or Administrator IAM access to the Catalog Management service can see and manage all versions of a product in their private catalog.

If you are logged in to an account that has a private catalog, the [Catalog menu](/catalog){: external} includes all catalogs that you have viewer or higher permissions for. When you select a private catalog, you can see all versions for a product tile.

You can specify who can see your particular product by sharing a product from your private catalog with other accounts, enterprise groups, enterprises, and to the {{site.data.keyword.cloud_notm}} catalog.

![The Catalog menu shows all catalogs that you have permissions to see and work with.](images/private-catalog-share-diagram.png){: caption="Figure 1. The Catalog menu shows all catalogs that you have permissions to see and work with." caption-side="bottom"}

The {{site.data.keyword.cloud_notm}} catalog includes products that are published to the {{site.data.keyword.IBM}} public cloud, as well as products that are shared with you directly from private catalogs. The product tiles that are visible to you include products that have one or more versions that are in either the `ready` or `pre-release` state.

![The IBM Cloud catalog includes product tiles that are either public or shared with you from a private catalog.](images/private-catalog-share-visibility-public.png){: caption="Figure 2. The IBM Cloud catalog includes product tiles that are either public or shared with you from a private catalog." caption-side="bottom"}
