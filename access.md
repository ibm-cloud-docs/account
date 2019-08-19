---

copyright:
  years: 2017, 2019
lastupdated: "2019-07-31"

keywords: user access, IBM Cloud account access, account owner, delegating access, confirming access

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Managing user access to the catalog
{: #find-access}

As an {{site.data.keyword.Bluemix}} account owner, you can assign, delegate, and confirm users access to the catalog by using an {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) policy. You can control the visibility of private services that are added to the account catalog or public services that are created in the account. By default, only the account owner can complete these tasks.

## Delegating access
{: #get-access}

You can delegate access on your account to control what users can see and to control how much authority those users have. For example, some information might only be appropriate for one user to read and analyze, whereas another might be given the authority to edit that information. To delegate account access to another user in the account, complete the following steps.

1. Click **Manage** > **Access (IAM)**.
2. Click **Access starts with the user** on the landing page.
3. Select a user on your account.
4. Click **Access policies**.
5. Click **Assign access**. Then, click **Assign account management services**.
6. Select the **Global Resource Catalog** from the Services list and the **Administrator** role from the Select roles list.

To grant other permissions, use the Viewer and Editor roles. Review the following table to learn more about what each IAM role allows a user to do within the context of working with the catalog for your account.

| Platform Management Role | Actions                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| Viewer                   | Can view private services, but can't change them                                                            |
| Editor                   | Can change object metadata, but can't change visibility for private services                                |
| Administrator            | Can change object metadata or visibility for private services, and restrict visibility of a public service  |
{: caption="Table 1. Example platform management roles and actions for the catalog" caption-side="top"}

For more information about assigning access to users, see [Assigning access to account management services](/docs/iam?topic=iam-account-services).

## Confirming your access
{: #confirm-access}

When you're added to another person's account, account administrators might delegate levels of access to you so that you can view private resources that are added to the account. The account owner might also delegate for who can view public resources in the account catalog. You don't have this access by default. The account owner must grant you an IAM role that so you can have access to complete these account resource management tasks.

You can use the {{site.data.keyword.Bluemix_notm}} console or the command-line interface (CLI) to determine whether you have access to enable specific users to view a private resource in the account.

To use the console, complete the following steps:

  1. Go to **Manage > Access (IAM)**.
  2. Click your name from the Users list.
  3. Click the **Access Policies** tab, where you can view your assigned access policies. You must have the Cloud IAM administrator role for the catalog resource in your account to update the list that includes accounts to see private resources in the catalog.


To use the [CLI](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_iam#ibmcloud_commands_iam), run the `ibmcloud iam user-policies <your-user-name>` command. The command returns an error if you aren't an administrator for the account.
