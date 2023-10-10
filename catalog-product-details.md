---


copyright:
  years: 2021, 2023
lastupdated: "2023-10-09"

keywords: onboard software, catalog details, software, catalog entry, about, product page, catalog listing

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Defining your product details
{: #cm-catalog-details}

When you publish your product to the catalog, users with access to your private catalog can view a tile with the product name, logo, and other details that you add during onboarding. To help users easily find your product in the catalog, you can specify specific keywords and filters that apply to your product.
{: shortdesc}


## Providing catalog entry details
{: #cm-catalog-entry}

Complete the following steps to define or update your catalog entry details. A catalog entry is displayed as a tile in the catalog that shows a title, short description, common filters, and a logo. Additionally, the filters and keywords that you define enable users to quickly locate your catalog entry.

1. Click **Manage** > **Catalogs** > **Private catalogs** in the {{site.data.keyword.cloud}} console.
1. Click the name of the private catalog that contains the product that you want to add details for.
1. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Edit** in the row that contains the product.
1. In the Product overview section, click **Edit** to add or update any of the following items:

   Product name
   :   Add a name for your product

   Category
   :   Select a category. This is a required field that you set during initial onboarding, but can change if needed. You can find all of the available category values by using the [`ibmcloud catalog offering category-options`](/docs/cli?topic=cli-manage-catalogs-plugin#category-options-offering) command.

   Filters
   :   Choose from the set of filters on compliance, delivery method, deployment target, pricing plan, and more. These filters are used to help users quickly find products relevant to their business needs.

   Industry
   :   Add up to five industry filters to target your product to specific users.

   Programmatic name
   :   This name is automatically generated based on your product's name that you imported to your private catalog. It is used when managing your product in the CLI or API.

   Logo
   :   Provide an image URL, or upload an SVG or PNG image from your computer. Make sure that your product or company logo image is an SVG or PNG file that's a square image that is roughly sized at 32 x 32 pixels and does not appear blurry or pixelated.

   Keywords
   :   Provide relevant keywords that enable your product to appear in search results when users search for the product.

   Short description
   :   Provide a short description to help users learn about and evaluate your product quickly from the tile in the catalog.

   Catalog ID
   :   This field is automatically populated, and you cannot change it.

   Product ID:
   :   This field is automatically populated, and you cannot change it.
cc
   Documentation URL
   :   Provide the link to your product's public documentation.

   Provider name
   :   Add a provider name, such as your company name, that displays when this product is shared from a private catalog. This name is not displayed if you publish to the {{site.data.keyword.cloud_notm}} catalog. Users can filter the catalog by the provider of a product. When you onboard a product to a private catalog, the provider name is set to `Community` by default. However, you can customize this field to display your company or organization name.

   Delivery method
   :   Select the delivery method for your product. The available delivery methods depend on the product type.

   Product type
   :   Select the product type. Examples of the product type are deployable architecture, module, or software.

   The preview of your catalog entry updates in real time as you update the fields that display in the catalog entry, such as the product name, short description, and logo.
   {: tip}

1. Review your catalog entry preview by clicking **View catalog entry**. When you're happy with your changes, click **Save**.

## Adding product page information
{: #cm-catalog-about}

When users select your product from the catalog, they can review more details, including a list of features and supporting media. These details are displayed on the About page for your product.

Complete the following steps to add information to your product's About page:

1. Click **Actions...** > **Edit product page**.
1. Add or edit the following information:

   * Click **Description**. Using common language, provide a unique description that includes the benefits and what your product can do for potential users. This description helps users understand why and how they can use your product.
   * Click **Features**. Showcase your product’s attributes that deliver value and differentiate it in the market. You want the information to be visually scannable by providing a descriptive title and one or two sentences for each feature.
   * Click **Media**. Add links to high-quality images or videos that show off your product. For example, provide an introductory walkthrough video or an illustration that shows user benefits or differences between certain features. The supported options are images, videos in MP4 or WebM file format, and videos hosted on YouTube or Vimeo.

1. Click **Update**.
