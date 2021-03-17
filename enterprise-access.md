---

copyright:

  years: 2019, 2020

lastupdated: "2020-06-10"

keywords: enterprise access, user access, roles, permissions, IAM, child account, invite users

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# User management for enterprises
{: #enterprise-access-management}

{{site.data.keyword.cloud}} enterprises are valuable for large companies or organizations that need to group a set of accounts while still maintaining a separation and isolation between the accounts for different departments or teams. The management of users and their access to resources in each account remains entirely separate even when the accounts are added and organized in an enterprise. 
{:shortdesc}

See [What is an enterprise?](/docs/account?topic=account-what-is-enterprise) for more information about enterprises.

The user list for each child account in an enterprise is accessible only to users in that child account. This means the users who are invited to the enterprise and the users who are invited to the accounts within the enterprise remain entirely separate. This is beneficial because you can add multiple accounts to an enterprise and organize them as needed into account groups, but keep the user lists restricted from other accounts. 

In most cases, you want to add only the users to your enterprise account that need the ability to manage the enterprise. Depending on the role the user is assigned on the [Enterprise account management service](/docs/account?topic=account-account-services#enterprise-account-management), they have varying levels of access for managing the enterprise. For example, a user assigned the Administrator role on the Enterprise service can rename the enterprise, update the domain, view usage, create accounts, and more. However, a user with the viewer or operator role is limited to viewing the accounts and account groups hierarchy for the enterprise.

Inviting users to the enterprise account doesn't provide access to manage any of the child accounts within the enterprise or their resources. If you add a user to an enterprise account that contains a number of accounts, those users do not automatically have access to manage those accounts as far as user management, billing, and more. The enterprise account users also don't have access to any resources in other accounts within the enterprise. 

If you want a user to manage the enterprise and have access to resources within child accounts, you must invite them to both accounts. Assigning access policies in the enterprise account allows the user to manage the enterprise. And, assigning access policies within the child account allows the user to manage specific resources or complete account management tasks within that account only.
{: note}

For information about assigning access to users in an enterprise, see [Assigning enterprise access](/docs/account?topic=account-assign-access-enterprise).





