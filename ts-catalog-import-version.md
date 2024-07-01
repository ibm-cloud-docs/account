---

copyright:
  years: 2020, 2022
lastupdated: "2022-12-19"

keywords: troubleshoot private catalog, new version, update version, update software, root folder name, update private catalog, private catalog, software

subcollection: account

content-type: troubleshoot

---

{{site.data.keyword.attribute-definition-list}}

# Why can't I import a new version of my software?
{: #troubleshoot-import-version}
{: troubleshoot}

When you try to update software in your private catalog by importing a new version, the following error message is displayed:
{: tsSymptoms}

> The newly imported version specifies a package with a root folder name that does not match the root folder name of existing versions. These values are required to be the same.

The name of the root folder can't change from version to version. Typically this happens if you generate the TAR from GitHub directly.
{: tsCauses}

Download the files, compress in a ZIP file, and upload them with the same root folder name.
{: tsResolve}
