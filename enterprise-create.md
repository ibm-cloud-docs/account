---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, multiple account

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Creating an enterprise
{: #create-enterprise}

You create an {{site.data.keyword.Bluemix}} enterprise from an existing Subscription account. The account that you use to create the enterprise is permanently added to the enterprise.
{:shortdesc}

## Before you begin
{: #create-prereqs}

To create an [{{site.data.keyword.Bluemix_notm}} enterprise](/docs/account?topic=account-enterprise), you must be the account owner or have the Administrator role on the Billing account management service in a Subscription account.

The Subscription account that you use to create the enterprise is permanently moved into the enterprise. Moving the account into the enterprise has the following impacts:
* Billing for the account transitions to being [managed by the enterprise](/docs/billing-usage?topic=billing-usage-enterprise). After the transition, users in the account can't access billing and payment information, such as invoices, payments, or subscriptions, for future billing periods. To view or manage billing, users need to be invited to the enterprise account and be given access to the Billing service in that account.
* Users and access permissions within the account are not changed. Access within the account is separate from the enterprise, and users don't automatically get access within the enterprise when the account is added. However, as previously mentioned, billing information is no longer available within the account regardless of access permissions.
* Resources within the account are not changed. Users with the correct access permissions can continue to view usage information for resources in the account.

If you don't have a Subscription account, you can upgrade your account as described in [Upgrading your account](/docs/account?topic=account-upgrading-account).

## Creating an enterprise in the console
{: #create-console}

1. Go to **Manage > Enterprise**, and click **Create**.
1. Enter a unique name to identify your enterprise. Typically, the name reflects your company or organization, such as `My organization's enterprise`. You can edit the enterprise name later if needed.
1. If your company or organization has an associated domain name, enter it in the **Domain** field. You can specify any domain or subdomain format, such as `example.com` or `my.example.com`.
1. Review the information about the impact to your account, and select **I understand the impact to my account**. Then, click **Create**.

   After the account is added to the enterprise, it can't be removed. Be sure you want to permanently move the account to an enterprise.
   {: important}

After a few moments, your enterprise is created, and you can view the enterprise dashboard. Your IBMid is listed as the contact. The contact serves as a focal point for any enterprise concerns, such as billing or usage questions. You're also assigned as the enterprise account owner, so you can invite additional users to manage the enterprise.

Click **Accounts** to view your enterprise hierarchy, which contains two accounts.

* The enterprise account, which is where you invite users and grant access to manage the enterprise.
* The account that you used to create the enterprise. Its users and resources remain the same, but billing is now managed by the enterprise.

## Creating an enterprise by using the CLI
{: #create-cli}

1. Log in, and select the account.

   ```
   ibmcloud login
   ```
   {:codeblock}
1. Create the enterprise by running the following command, where `NAME` is a unique name to identify the enterprise.

   ```
   ibmcloud enterprise create NAME [-d, --domain DOMAIN_NAME] [--primary-contact-id PRIMARY_CONTACT_USER_ID]
   ```
   {:codeblock}

   For example, the following command creates an enterprise that is named `Example Corp Enterprise` with the `examplecorp.com` domain.

   ```
   ibmcloud enterprise create "Example Corp Enterprise" -d examplecorp.com
   ```
   {:codeblock}

   By default, the enterprise is created with the currently logged-in user in the following roles:
      * The contact for the enterprise, which identifies a focal person to notify with enterprise-related concerns
      * The owner of the enterprise account, which has full access to manage the enterprise account

   You can specify the IBMid for a different user on the `--primary-contact-id` option. The same user is assigned to both roles.
1. Review the impact to your account, and confirm that you want to continue by entering `y`.
   ```
   Account abcde12345fghij67890 will be incorporated into enterprise My new enterprise
   (which cannot be undone). Do you want to proceed? [y/N]> y
   ```

After the enterprise is created, two new IDs are displayed. The first ID is associated with the enterprise, and the second ID identifies the enterprise account, which you use to manage the enterprise.

```
ID:                      09876jihgf54321edcba   
Enterprise Account ID:   edcba12345jihgf67890
```

The account that you used to create the enterprise is now a part of the enterprise. Run the [`ibmcloud enterprise accounts`](/docs/cli?topic=cloud-cli-ibmcloud_enterprise#ibmcloud_enterprise_accounts) command to view the two accounts in your enterprise: the enterprise account, and the account you used to create the enterprise.

## Creating an enterprise by using the API
{: #create-api}

You can programmatically create an enterprise by calling the Enterprise Management API as shown in the following sample request. For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-enterprise){: external}.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/enterprises \
-H "Authorization: Bearer <Token>" \
-H 'Content-Type: application/json' \
-d '{
  "source_account_id": "a1b2c32a5ea94809a9840f5e23c362d",
  "name": "Sample Enterprise",
  "domain": "example.com",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

## Next steps
{: #create-next-steps}

Build out your enterprise structure by adding more existing accounts or creating new accounts within your enterprise. For more information, see [Adding accounts to your enterprise](/docs/account?topic=account-enterprise-add).

You can also invite additional users to the enterprise account so that they can help manage the enterprise. For example, you might want to invite a financial officer to manage billing and track usage costs, and invite department leads to administer accounts. See [Inviting users](/docs/iam?topic=iam-iamuserinv) for more information about how to invite users.
