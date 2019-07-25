---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, add account, import account, create account

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Adding accounts to an enterprise
{: #enterprise-add}

You can build out your enterprise by adding more {{site.data.keyword.Bluemix}} accounts to it. To add accounts, you can import existing accounts that aren't in another enterprise, or you can create new accounts within your enterprise.
{:shortdesc}

After your enterprise has multiple accounts, you can organize related accounts by using account groups. For more information, see in [Organizing accounts in an enterprise](/docs/account?topic=account-enterprise-organize).

## Importing existing accounts
{: #add-accounts}

You can import existing accounts into an enterprise. After you import an account, it can't be removed, and each account can be a part of only one enterprise. If you import a Lite or trial account, it's automatically upgraded to a [Pay-As-You-Go account](/docs/account?topic=account-accounts).

Importing an account to the enterprise has the following impacts:
* Billing for the account transitions to being managed by the enterprise. After the transition, users in the account can't access billing and payment information, such as invoices, payments, or subscriptions, for future billing periods. To view or manage billing, users need to be invited to the enterprise account and be given access to the Billing service in that account. See [Centrally manage billing and usage with enterprises](/docs/billing-usage?topic=billing-usage-enterprise) for more information.
* Users and access permissions within the account are not changed. Access within the account is separate from the enterprise, and users don't automatically get access within the enterprise when the account is imported.
* Resources within the account are not changed. Users with the correct access permissions can continue to view usage information for resources in the account.

To import existing accounts into an enterprise, the following access is required:

   * Within the account to be imported, you must be the account owner or have the Administrator role on the Billing service within the account.
   * Within the enterprise account, you need the Editor or Administrator role on the Enterprise service and the Administrator role on the Billing service.

To import an existing account, complete the following steps:

1. Log in to your enterprise account, and go to **Manage > Enterprise**.
1. Click **Accounts** to view the accounts and account groups in the enterprise. In the Accounts section, select **Add > Import account**.
1. Select the account that you want to import.

   If no accounts are displayed, you likely don't have the correct access in any existing accounts.
   {: tip}
1. If you want to add the account to an account group, select the account group to be its parent. The parent that you select determines where in the enterprise hierarchy the account exists.
1. Review the information about impacts to your account, and select **I understand the impact to my account**. Then, click **Import**.

   After the account is imported to the enterprise, it can't be removed. Be sure you want to permanently move the account to the enterprise.
   {: important}


### Importing accounts by using the API
{: #add-account-api}

To import an existing account to the enterprise, call the <!--[Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#import-an-account-into-an-enterprise){: external}--> as shown in the following sample request. Replace the {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) token and ID variables with the values from your enterprise.

```
curl -X PUT \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID/import/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" -H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID"
}'
```
{: codeblock}

## Creating new accounts
{: #create-accounts}

You can create new accounts within your enterprise. The accounts are created as Pay-As-You-Go accounts, and usage is billed to the enterprise. To create an account, you need an access policy with the Editor or Administrator role on the Enterprise service.

1. From the Enterprise dashboard, click **Accounts** to view accounts and account groups in the enterprise.
1. In the Accounts section, select **Add > Create account**.
1. Enter a name for the account that's unique within the enterprise. Because it's one of many accounts, a unique, descriptive name helps you understand the purpose of the account at a glance.
1. If you want to assign a different user as the account owner, enter their IBMid in the **Owner** field. The account owner has full access to manage the account.
1. If you want to add the account to an account group, select the account group to be its parent. The parent that you choose determines where in the enterprise hierarchy the account exists.
1. Click **Create**.

After you create the account, the account owner can log in to the account to invite other users and manage their access.

### Creating accounts by using the API
{: #create-account-api}

To create a new account in the enterprise, call the Enterprise Management API as shown in the following sample request, replacing the IAM token and ID variables with the values from your enterprise. <!--For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-a-new-account-in-an-enterprise){: external}-->.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/accounts \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID",
  "name": "Sample Account",
  "owner_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}
