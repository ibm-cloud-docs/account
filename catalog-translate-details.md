---


copyright:

  years: 2022, 2025
lastupdated: "2025-01-28"

keywords: onboard software, catalog details, software, catalog entry, about, product page, catalog listing, translation, internationalization, localization, CLI

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Translating product details by using the CLI
{: #translate-product-details}

When you onboard software, you can translate certain details about your product by using the [{{site.data.keyword.cloud}} CLI plug-in](/docs/cli?topic=cli-manage-catalogs-plugin). Run the `get-translations` command to download the language files. Then, edit those files to include your specific translations and upload them using the `upload-translations` command. For more information, see [Getting started with the {{site.data.keyword.cloud_notm}} CLI](/docs/cli?topic=cli-getting-started).
{: shortdesc}

## What product details can you translate? 
{: #cm-translate-what}

The following information about your product can be translated: 
* Product name
* Short and long description 
* Support process
* Media captions
* Feature titles and descriptions 
* Readme file

## Downloading translation files
{: #cm-download-translations}

Run the `get-translations` command to download the language `.json` files. 

   ```bash
   ibmcloud catalog offering get-translations -c CATALOG_NAME -o PRODUCT_NAME --languages en,de,ja
   ```
   {: codeblock}

### Command options
{: #cm-translate-options}

-c
:   Specify the catalog name or ID.

-o
:   Specify the product name or ID. 

--zip (optional)
:   Downloads the translation files as a `.zip` file. 

--languages
:   Provide a comma-separated list of languages to translate. If no languages are specified, all of them are downloaded. Valid options are `de`, `en`, `es`, `fr`, `it`, `ja`, `ko`, `pt-BR`, `zh-Hans`, and `zh-Hant`. 

Edit the default values in each translation file with your specific translations for each language. 

## Uploading translation files
{: #cm-upload-translations}

Run the `upload-translations` command to upload your translation files. 

An English translation is required to upload other translations.
{: note}

   ```bash
   ibmcloud catalog offering upload-translations -c CATALOG_NAME -o PRODUCT_NAME --language-files en.json,de.json,ja.json
   ```
   {: codeblock}

### Command options
{: #cm-upload-options}

-c
:   Specify the catalog name or ID.

-o
:   Specify the product name or ID. 

--language-files
:   Provide a comma-separated list of language files to upload. If no languages are specified, all of the available language files are uploaded. Valid options are `de.json`, `en.json`, `es.json`, `fr.json`, `it.json`, `ja.json`, `ko.json`, `pt-BR.json`, `zh-Hans.json`, and `zh-Hant.json`. 
