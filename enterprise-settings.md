---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise settings, manage enterprise, view enterprise, rename enterprise

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Managing your enterprise
{: #enterprise-settings}

From the dashboard of your {{site.data.keyword.Bluemix}} enterprise, you can view enterprise details, take common actions such as adding accounts and inviting users, and view billing information. You can also rename your enterprise on the dashboard or using the CLI or API.
{:shortdesc}

To manage enterprise settings, you need the Administrator or Editor role on the Enterprise service in the enterprise account.
{: tip}

## Managing your enterprise in the console
{: #enterprise-manage}

To view your enterprise dashboard, go to **Manage > Enterprise**. The dashboard provides an overview of accounts, users, and subscription credit in your enterprise. The dashboard has quick links so that you can perform the following common actions:
   * [Add new or existing accounts to your enterprise](/docs/account?topic=account-enterprise-add)
   * [Invite users to the enterprise account](/docs/iam?topic=iam-iamuserinv)
   * [View and manage subscription credit](/docs/billing-usage?topic=billing-usage-subscriptions)

Also, you can rename your enterprise by clicking **Rename** in the Enterprise details section.

## Managing your enterprise by using the API
{: #enterprise-manage-api}

You can programmatically update an enterprise by calling the Enterprise Management API as shown in the following sample request. You can update the enterprise name or domain by passing the new values on the API call. For detailed information about the API, see the [Enterprise Management API documentation](https://{DomainName}/apidocs/enterprise-apis/enterprise#update-an-enterprise){: external}.

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID" \
-H "Authorization: $IAM_TOKEN" \
-H 'Content-Type: application/json' \
-d '{
  "name": "Brand New Sample Enterprise",
  "domain": "new.example.com"
}'
```
