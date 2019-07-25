---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, enterprise users, enterprise access, enterprise tutorial

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Getting started with an enterprise
{: #enterprise-tutorial}

In this tutorial, you create an enterprise for a fictitious company called *Example Corp* that wants to track their usage costs by department. By completing this tutorial, you learn how to model your enterprise structure by department, set up account groups, add existing accounts and users, and explore subscriptions.
{:shortdesc}

![A four-tier enterprise that groups accounts according to department in an organization. For example, account groups are named Marketing, Development, and Sales. The account groups contain accounts for teams within those departments. For example, the Sales account group contains accounts for Direct, Online, and Enablement.](images/enterprise-by-dept.svg "An enterprise that organizes accounts according to department in the organization."){: caption="Figure 1. An enterprise that is organized by department" caption-side="bottom"}

## Before you begin
{: #setting-prereqs}

To create an [{{site.data.keyword.Bluemix_notm}} enterprise](/docs/account?topic=account-enterprise), you must be the account owner or have the Administrator role on the Billing account management service in a Subscription account.

Creating an enterprise from an account and importing existing accounts cannot be undone. This tutorial is provided as an example of the steps you can follow to set up an enterprise by department, but you should carefully plan your enterprise structure around your organization's needs.
{:important}

## Step 1. Create the enterprise
{: #create_enterprise_tutorial}

1. Go to **Manage** > **Enterprise**, and click **Create**.
2. Enter the name of your company, Example Corp, to identify your enterprise.
3. Enter `example.com` as the domain name.
4. Review the information about the impact to your account, and select **I understand the impact to my account**. Then, click **Create**. The account is now permanently part of the enterprise and can't be removed.

After your enterprise is created, you are directed to the enterprise dashboard. From here, you can view the enterprise details, accounts, users, and billing information. To view the account that you used to create the enterprise, go to the **Accounts** page.

## Step 2. Create an enterprise structure with account groups
{: #account_groups_tutorial}

Your company, Example Corp, uses account groups to organize related accounts. The second and third tier of the enterprise hierarchy contain the Marketing, Development, Sales, Design, and Engineering account groups. Complete the following steps to create the account groups:

1. From the enterprise dashboard, click **Accounts** to view accounts and account groups in the enterprise.
2. In the account group section, click **Create**.
3. Enter `Marketing` for the account group name.
4. In the contact field, enter the IBMid for the user that you want to be the main contact for the account group. Because an account group can't contain any resources, it doesn't have an owner like an account.
5. Select **Example Corp** as the parent account.
6. Click **Create**.

Repeat the steps to create the Sales, Development, Design, and Engineering account groups. When you create the Design and Engineering account groups, make sure that you add Development as the parent account.

## Step 3. Import existing accounts
{: #existing_accounts_tutorial}

Now that you created an enterprise and the structure for account groups, you can import an existing account to the enterprise. To import an existing account, the following access is required:

* Within the account to be imported, you must be the account owner or have the Administrator role on the Enterprise and Billing account management services within the account.
* Within the enterprise account, you need the Editor or Administrator role on the Enterprise service and the Administrator role on the Billing service.

Complete the following steps to import the existing UX-UI account to the Design account group:
1. From the enterprise dashboard, click **Accounts** to view the accounts and account groups in the enterprise.
2. In the Accounts section, click **Add** > **Import account**.
3. Select **UX-UI** from the **Account** list.

  If no accounts are displayed, you likely don't have the correct access in any existing accounts.
  {: tip}

4. Select **Design** as the parent of the UX-UI account. This determines where in the enterprise hierarchy the account exists.
5. Review the information about the impacts to your account, and select **I understand the impact to my account**. Then, click **Import**.

Repeat the steps to import the Content account.

## Step 4. Create new accounts
{: #create-accounts_tutorial}

You can create new accounts within your Example Corp enterprise. The accounts are created as Pay-As-You-Go accounts, and usage is billed to the enterprise. To create an account, you need an access policy with the Editor or Administrator role on the Enterprise service.

Complete the following steps to create the Web account in your enterprise:

1. From the Enterprise dashboard, click **Accounts** to view the accounts and account groups in the enterprise.
1. In the Accounts section, select **Add** > **Create account**.
1. Enter `Web` as the name of the account.
1. If you want to assign a different user as the account owner, enter their IBMid in the **Owner** field. The account owner has full access to manage the account.
1. Select **Marketing** as the parent of this account.
1. Click **Create**.

After you create the account, the account owner can log in to the account to invite other users and manage their access.

Repeat the steps to add Print, Frontend, Backend, Direct, Online, and Enablement accounts. Review the following table to see the child account and parent account group hierarchy.

| Child | Parent |
| ----- | -------|
| Print | Marketing |
| Frontend | Engineering |
| Backend | Engineering |
| Direct | Sales |
| Online | Sales |
| Enablement | Sales |
{:caption="Table 1. Child account and parent account group hierarchy" caption-side="top"}

## Step 5. Explore subscriptions
{: #explore-sub_tutorial}

In this example, some accounts that were imported to the Example Corp enterprise included existing subscriptions. You can explore subscriptions in the enterprise from the enterprise dashboard.

1. Go back to the Enterprise dashboard by clicking **Dashboard**. In the Billing section, you can view available credit, remaining credit, and subscription expiration dates.
1. To view details about all subscriptions in the enterprise, click **View subscriptions**.

   In the Platform subscription section, you can view the subscription start date, end date, starting credit and available credit. To add more credit, you can purchase additional subscriptions and apply the subscription code.

## Step 6. Assign users in child accounts access to create resources
{: #users_create_resources}

Before you begin, make sure that you switch to the account where you want to create the resource. In this case, switch to the *Print* account. If you want users in your account to create resources from the catalog and assign them to a resource group, you must assign two types of access policies.
* Assign one access policy with Viewer role or higher on the resource group.
* Assign one access policy with Editor or Administrator role on the service.

Complete the following steps to assign the required access:

1. Go to **Manage** > **Access (IAM)**, and select **Users**.
2. Select a user name from the list.
3. Click the **Access policies** tab > **Assign access**.
4. Click **Assign access within a resource group**.
5. Select the resource group that you want to assign the user access to.
6. Select the Viewer role or higher on the resource group.
7. Select the service that you want to assign the user access to.
  * If you want the user to be able to provision any service, select **All services**.
  * If you want to assign the user specific access, select a service from the list. The user has access only to the service selected.
8. Select the Editor or Administrator role.
9. Click **Assign**.

## Step 7. View usage from all accounts
{: #usage_tutorial}

1. Log in to the Example Corp enterprise account.
2. Go to **Manage > Billing and usage**, and select **Usage**.

   The Usage page displays the costs for all usage in your enterprise, which is broken down by account and account group. Usage information for classic infrastructure services is not included for the current billing period. For more information, see [Viewing usage for your classic infrastructure resources](/docs/billing-usage?topic=billing-usage-infra-usage).
3. Click **Marketing** in the table to view usage within the account group. Similar to the enterprise level, usage is broken down by the account and account group.
4. To view usage by resource, go to the account level by clicking through account groups in the table or selecting the account from the **Enterprise** menu. Costs are shown for each type of resource that was used during the time frame.

Repeat the steps to view usage for the Development, Sales, Design, and Engineering account groups.

   From the enterprise account, you can't view usage data for the resource plan or instance because it requires access within the account. Click **Switch to the account** to view data for the account. You need billing access to the resources and services in the account. See [Viewing your usage](/docs/billing-usage?topic=billing-usage-viewingusage) for more information.

Data is shown in the enterprise account only for usage that is incurred by accounts in the enterprise. To view usage from before an account was added to the enterprise, log in to that account and select the relevant time frame.
{: note}
