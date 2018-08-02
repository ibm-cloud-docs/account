---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Managing access to the catalog
{: #find-access}

As an account owner, you might want to assign access by using an IAM policy to allow users in your account the ability to control the visibility of private services added to the account catalog or public services that have been created in the account. By default, only the account owner has the ability to complete these tasks.

## How do I delegate access as an account owner?
{: #get-access}

If you're an account owner, you can give access to a user in your account through the Identity and Access UI by assigning an access policy. To ensure the user has the necessary access, select the **Global Catalog** resource and the **Administrator** role for the access policy.

You might want to grant other permissions to users in your account by using the `viewer` and `editor` Identity and Access Management (IAM) roles. Review the following table to learn more about what each IAM role allows a user to do within the context of working with the catalog for your account.

| Platform management role | Description of actions |
|:-----------------|:-----------------|
| Viewer | Can see private services, even if the account hasn't been included, but cannot make changes. |
| Editor | Can make changes to object metadata but cannot change visibility. |
| Administrator | Can change object metadata or visibility.  |
{: caption="Table 1. Example platform management roles and actions for the catalog service" caption-side="top"}

For step-by-step instructions on assigning access to users in your account, go to the [Access to resources](/docs/iam/mngiam.html#iammanidaccser#resourceaccess) documentation.

## How do I check if I have access?

When you are added to another person's account, they might delegate certain levels of access to you so that you can view private resources that have been added to the account. The account owner might also delegate the ability for you manage who sees public resources in the account catalog. You do not have this access by default. The account owner must grant you an IAM role that enables you to have access to complete these account resource management tasks.

You can use the CLI or the Identity and Access UI to determine whether you have access to enable specific users to view a private resource that has been added to the account.

To use the Identity and Access UI, complete the following steps:

1. Go to **Manage** > **Security** > **Identity and Access**, and then click **Users**.
2. Click your name from the Users list.
3. In the **Access Policies** section, you can view your assigned access policies. You must have the Cloud IAM administrator role for the catalog resource in your account to update the list that includes accounts to see private resources in the catalog.

To use the [ibmcloud CLI](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_iam), complete the following steps:

Enter the following command with your user name `ibmcloud iam user-policies <your-username>` to find whether you're an administrator of accounts you selected in the CLI. If you aren't an administrator for your account, these commands return an error that says you're not authorized.
{: tip}
