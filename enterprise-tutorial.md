---

copyright:
  years: 2019, 2021
lastupdated: "2021-06-11"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, enterprise users, enterprise access, enterprise tutorial

subcollection: account

content-type: tutorial
completion-time: 10m

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}
{:tutorial: .tutorial}
{:step: data-tutorial-type='step'}

# Setting up an enterprise
{: #enterprise-tutorial}
{: toc-content-type="tutorial"}
{: toc-completion-time="10m"}

This tutorial walks you through how to set up an enterprise by department so you can manage and track usage costs for multiple {{site.data.keyword.Bluemix}} accounts. By completing this tutorial, you learn how to create an enterprise, add accounts and organize them in account groups, invite users, and explore subscriptions.
{:shortdesc}

The tutorial uses a fictitious company that is called *Example Corp* that wants to create an enterprise with the following structure. As you complete the tutorial, adapt each step to match your organization's accounts and desired structure.

![A four-tier enterprise that groups accounts according to department in an organization. For example, account groups are named Marketing, Development, and Sales. The account groups contain accounts for teams within those departments. For example, the Sales account group contains accounts for Direct, Online, and Enablement.](images/enterprise-by-dept.svg "An enterprise that organizes accounts according to department in the organization."){: caption="Figure 1. An enterprise that is organized by department" caption-side="bottom"}

## Before you begin
{: #setting-prereqs}

Read [What is an enterprise?](/docs/account?topic=account-what-is-enterprise) to learn the basic principles of how account management, billing, resources, and user and access management work in an enterprise.

Verify that you have the required access in a Subscription account, which serves as the base account from which you create the enterprise. To create an enterprise, you must be the account owner or have the Administrator role on the Billing account management service.

Creating an enterprise from an account and importing existing accounts cannot be undone. This tutorial is provided as an example of the steps you can follow to set up an enterprise by department, but you should carefully plan your enterprise structure around your organization's needs.
{:important}

## Create the enterprise
{: #create_enterprise_tutorial}
{: step}

Enterprises are created from an existing Subscription account. When you create the enterprise, the account is added to the enterprise hierarchy. Billing transitions to being managed by the enterprise, but its users and resources remain the same and are completely unaffected. For a complete description of account impacts, see [Creating an enterprise](/docs/account?topic=account-create-enterprise).

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Enterprise**, and click **Create**.
2. Enter the name of your company, such as Example Corp, to identify your enterprise.
3. Enter your company's domain, such as `examplecorp.com`.
4. Review the information about the impact to your account, and select **I understand the impact to my account**. Then, click **Create**. The account is now permanently part of the enterprise and can't be removed.

After your enterprise is created, you are directed to the enterprise dashboard. From here, you can view the enterprise details, accounts, users, and billing information. Go to the **Accounts** page to view your enterprise structure, where you see the following accounts:
  * An enterprise account with the same name as your enterprise. This account is used for enterprise management.
  * The account that you created the enterprise from. Users can continue working with resources in the account unaffected.

## Create an enterprise structure with account groups
{: #account_groups_tutorial}
{: step}

Use account groups to [organize related accounts](/docs/account?topic=account-enterprise-organize). The second and third tier of the Example Corp. enterprise hierarchy contain the Marketing, Development, Sales, Design, and Engineering account groups. Complete the following steps to create the account groups:

1. From the enterprise dashboard, click **Accounts** to view accounts and account groups in the enterprise.
2. In the account group section, click **Create**.
3. Enter the account group name, such as `Marketing`.
4. In the contact field, enter the IBMid for the user that you want to be the main contact for the account group. Because an account group can't contain any resources, it doesn't have an owner like an account.
5. Select **Example Corp** as the parent account.
6. Click **Create**.

Repeat the steps to create the Sales, Development, Design, and Engineering account groups. When you create the Design and Engineering account groups, make sure that you add Development as the parent account group.

## Import existing accounts
{: #existing_accounts_tutorial}
{: step}

Now that you created an enterprise structure, you can import an existing account to the enterprise. When you import an account, it is permanently added to the enterprise. Like when you create an enterprise, billing for the imported accounts transitions to being managed by the enterprise, but its users and resources remain the same. For details, see [Importing existing accounts](/docs/account?topic=account-enterprise-add#add-accounts).

To import an existing account, the following access is required:

* Within the account to be imported, you must be the account owner or have the Administrator role on the Enterprise and Billing account management services within the account.
* Within the enterprise account, you need the Editor or Administrator role on the Enterprise service and the Administrator role on the Billing service.

Complete the following steps to import the example UX-UI account to the Design account group:
1. From the enterprise dashboard, click **Accounts** to view the accounts and account groups in the enterprise.
2. In the Accounts section, click **Add** > **Import account**.
3. Select **UX-UI** from the **Account** list.

  If no accounts are displayed, you likely don't have the correct access in any existing accounts.
  {: tip}

4. Select **Design** as the parent of the UX-UI account. This determines where in the enterprise hierarchy the account exists.
5. Review the information about the impacts to your account, and select **I understand the impact to my account**. Then, click **Import**.

Repeat the steps to import more accounts.

## Create new accounts
{: #create-accounts_tutorial}
{: step}

You can create new accounts within your enterprise. The accounts are created as Pay-As-You-Go accounts, and usage is billed to the enterprise. To create an account, you need an access policy with the Editor or Administrator role on the Enterprise service.

Complete the following steps to create the example Web account in your enterprise:

1. From the Enterprise dashboard, click **Accounts** to view the accounts and account groups in the enterprise.
1. In the Accounts section, select **Add** > **Create account**.
1. Enter `Web` as the name of the account.
1. If you want to assign a different user as the account owner, enter their IBMid in the **Owner** field. The account owner has full access to manage the account.
1. Select **Marketing** as the parent of this account.
1. Click **Create**.

After you create the account, the account owner can log in to the account to invite other users and manage their access.

Repeat the steps to create more accounts. As an example, the Example Corp enterprise has the following child account and parent account group hierarchy.

| Child | Parent |
| ----- | -------|
| Print | Marketing |
| Frontend | Engineering |
| Backend | Engineering |
| Direct | Sales |
| Online | Sales |
| Enablement | Sales |
{:caption="Table 1. Child account and parent account group hierarchy" caption-side="top"}

## Explore subscriptions
{: #explore-sub_tutorial}
{: step}

You can explore subscriptions in the enterprise from the enterprise dashboard. Any existing subscriptions from accounts that are imported into the enterprise are moved to the enterprise account and added to the enterprise [credit pool](/docs/billing-usage?topic=billing-usage-enterprise#credit-pool).

1. Go back to the Enterprise dashboard by clicking **Dashboard**. In the Billing section, you can view available credit, remaining credit, and subscription expiration dates.
1. To view details about all subscriptions in the enterprise, click **View subscriptions**.

   In the Platform subscription section, you can view the subscription start date, end date, starting credit and available credit. To add more credit, you can purchase additional subscriptions and apply the subscription code.

## Invite users to manage your enterprise
{: #invite-enterprise-users-tutorial}
{: step}

In a large organization like Example Corp., there are likely other people who you want to give access to manage the enterprise so they can do their jobs. In this case, you want to give department leads of the Marketing, Development, and Sales account groups access to manage their accounts and resource usage, and you want the Example Corp. financial officer to have access to view the entire enterprise's billing and usage. To give other users access, you invite them to the enterprise account and assign them the appropriate access. 

First, invite the department leads and assign them access.

1. Go to the Enterprise dashboard by clicking **Manage** > **Enterprise**. In the Users section, click **Invite users**.
1. Enter the email address of the user you want to invite, such as `jsmith@example.com`.
1. Expand the **Manually assign users access** section.
1. Select **Account management**
1. Select **Enterprise**. 
1. Select the **Example Corp** enterprise.
1. Select the first account group, **Marketing**. Leave the account selection blank. This scopes the access to only the particular account group.
1. Select the **Editor** role.
1. Click **Add**.
1. Click **Invite**.

Invite the other two department leads by clicking **Invite users** again and assigning the Editor access role for their department's respective account groups. Then, invite the financial officer and follow the same steps, but don't select an account group, and assign the **Usage Report Viewer** access instead. 

With the Usage Report Viewer role, the financial officer can see usage from all accounts but can't create, import, or otherwise organize accounts. You then need to provide them access to billing in the enterprise.

1. From the Users page, click the name of the user from the list.
1. Click the **Access policies** tab, and then **Assign access**.
1. Click **Assign access to account management services**.
1. Select the Billing service, and then select the Administrator role.
1. Click **Assign**.

## Assign users in child accounts access to create resources
{: #users_create_resources}
{: step}

Before you begin, make sure that you switch to the account where you want to create the resource. In this case, switch to the *Print* account. If you want users in your account to create resources from the catalog and assign them to a resource group, you must assign two types of access policies.
* Assign one access policy with viewer role or higher on the resource group.
* Assign one access policy with editor or administrator role on the service.

Complete the following steps to assign the required access:

1. In the console, go to **Manage** > **Access (IAM)**, and select **Users**.
2. Click the user's name from the list.
3. Click **Access policies** > **Assign access**.
4. Select the service that you want to assign the user access to.
    * If you want the user to be able to create any service, select **All Identity and Access enabled services**.
    * If you want to assign the user access to a specific service, select it from the list. 
5. Select the resource group that you want to assign the user access to.
6. Select the region.
7. Select the viewer role or higher from the list of platform access roles. 
8. (Optional) Select the reader role or higher from the list of service access roles. 
6. Select the viewer role or higher from the list of resource group access roles.
7. Click **Add**.
8. Review the access summary, and click **Assign**. 

## View usage from all accounts
{: #usage_tutorial}
{: step}

1. Log in to the Example Corp enterprise account.
2. Go to **Manage** > **Billing and usage**, and select **Usage**.

   The Usage page displays the costs for all usage in your enterprise, which is broken down by account and account group. Usage information for classic infrastructure services is not included for the current billing period. For more information, see [Viewing usage for your classic infrastructure resources](/docs/billing-usage?topic=billing-usage-infra-usage).
3. Click **Marketing** in the table to view usage within the account group. Similar to the enterprise level, usage is broken down by the account and account group.
4. To view usage by resource, go to the account level by clicking through account groups in the table or selecting the account from the **Enterprise** menu. Costs are shown for each type of resource that was used during the time frame.

Repeat the steps to view usage for the Development, Sales, Design, and Engineering account groups.

   From the enterprise account, you can't view usage data for the resource plan or instance because it requires access within the account. Click **Switch to the account** to view data for the account. You need billing access to the resources and services in the account. See [Viewing your usage](/docs/billing-usage?topic=billing-usage-viewingusage) for more information.

Data is shown in the enterprise account only for usage that is incurred by accounts in the enterprise. To view usage from before an account was added to the enterprise, log in to that account and select the relevant timeframe.
{: note}

## Next steps
{: #enterprise-next-steps}

Now that you learned the basics of how to set up an enterprise, you can continue to add accounts, account groups, and users as your teams and cloud workloads grow. For more information, see [Managing your enterprise](/docs/account?topic=account-enterprise-settings).
