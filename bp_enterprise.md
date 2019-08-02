---

copyright:
  years: 2019
lastupdated: "2019-07-23"

keywords: enterprise, enterprise resources, enterprise account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Best practices for setting up an enterprise
{: #enterprise-best-practices}

These best practices provide you with the basic building blocks for setting up an {{site.data.keyword.cloud}} enterprise.
{:shortdesc}

## Organizing accounts according to how you want to track billing
{: #organize-enterprise-usage}

A key benefit of {{site.data.keyword.cloud_notm}} enterprises is that they enable you to centrally view and manage billing and usage across multiple accounts. This capability's usefulness is dependent on your enterprise structure, because usage data is aggregated by each account group and account. Create account groups for projects that function under a common budget. For examples, see [How can I use an enterprise?](/docs/account?topic=account-enterprise#enterprise-use-cases).

The enterprise administrator or your financial officer might not be familiar with each individual account or account group. To make it easier to identify their purpose, give each account and account group a human-readable name. If your company uses billing codes, you can also incorporate them into the name. For example, instead of a `devteam` account group with `fed ui` and `be api` accounts, create the `Development - A2B3` account group with `Front-end UI team` and `Back-end API team` accounts.

An enterprise user with Administrator or Editor access can edit the enterprise and account group names, but they can't change account names. To edit an account name, a user must be in the account itself.
{:tip}

Because you have a unified view of all usage that's organized by your account groups and accounts, you can charge back usage costs to the associated teams. For more information, see [Recovering costs for enterprise usage](/docs/billing-usage?topic=billing-usage-enterprise-usage#enterprise-cost-recovery).

## Creating a consistent enterprise hierarchy
{: #accounts-vs-groups}

When you set up your enterprise, you create an enterprise hierarchy that reflects your company or organization. As you create accounts and account groups, plan a consistent scheme for how your company uses the following enterprise layers:
- Resource groups and Cloud Foundry orgs and spaces within an account
- Accounts within an account group
- Account groups within the enterprise

For example, your company might create accounts for each team, with resource groups or Cloud Foundry orgs within the account for development, testing, and production environments. Another company might have distinct accounts for each environment, which are grouped into account groups for each team.

However you choose to structure your enterprise, be as consistent as possible to simplify enterprise management. Because it's easy to create and keep track of new accounts, it can be tempting to create lots of separate accounts as users request them. However, each account introduces additional management overhead. As you plan how to structure your enterprise, keep in mind the following points.
- For each account that you create, users must be invited and their access must be managed separately.
- An inconsistent structure can make it harder to determine who to give access within each account and which teams are using resources.
- Users can collaborate on resources and services only within an account. Resources can't be moved between accounts.

## Working with resources in an enterprise
{: #child-resources-enterprise}

In the enterprise, create resources only in child accounts that you import or create within the enterprise. Although it's possible to create resources within the enterprise account, it's not best practice for the following reasons:
 - The enterprise account is always a direct child of the enterprise and can't be moved, so you won't have the flexibility to change how usage is reported for the resources.
 - The enterprise account contains the users and access for managing the enterprise and its billing, so only users with those responsibilities should be added to the account.

Users within each account in the enterprise can create, use, and collaborate on resources just as you can in a stand-alone account. For details, see [Working with resources and services](/docs/resources?topic=resources-resource). Enterprise users can't directly work with resources within child accounts, but they can monitor the resource types and plans that are used in each account by viewing their usage. For more information, see [Viewing usage in an enterprise](/docs/billing-usage?topic=billing-usage-enterprise-usage).

## Setting up access policies in an enterprise
{: #access-enterprise}

As always, follow the best practice for assigning the minimal number of access policies and levels of access. This enables you to spend less time assigning access to users and more time focusing on developing in {{site.data.keyword.cloud_notm}}, while ensuring that you don't provide too much access to users who don't need it.

Access groups are a useful tool for assigning access to a group of users and service IDs that all need the same access. By using access groups, you can streamline access management by assigning the minimal number of access policies to groups of users.  As an example, if you have five users that you want to manage all of the billing and account management-related tasks for the enterprise, then you can combine them into an access group that is called `Administrators`. In the access group, you can assign two policies: one with the administrator role on the Billing account management service and one with the administrator role on all account management services in the account. As users change job responsibilities or teams, you can add or remove users from the access group instead of adding or removing the same policies from the individual users.
