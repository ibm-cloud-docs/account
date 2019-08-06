---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: troubleshoot enterprise, enterprise problem, account problem, enterprise support, enterprise help, error message

subcollection: account
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Troubleshooting for an enterprise
{: #enterprise_help}

General problems with managing your enterprise might include issues when you try to apply subscription or feature codes, or when you try to add an account to the enterprise. In many cases, you can recover from these problems by following a few easy steps.

## Why can't I view the entire enterprise?
{: #troubleshoot-view-enterprise}
{: troubleshoot}

If you are not seeing the entire enterprise, you might need to check what access you are assigned.

You can see a few of the accounts in the enterprise but not the entire enterprise hierarchy. The account hierarchy shows only accounts that you have access to, not the entire enterprise account.
{: tsSymptoms}

You are assigned access to only certain accounts in the enterprise.
{: tsCauses}

To check what access you are assigned, complete the following steps:
{: tsResolve}

1. Go to **Manage** &gt; **Access (IAM)** > **Users**.
2. Select your name.
2. Click the **Access policies** tab.

Contact the enterprise owner to request the correct access.

If you're the owner of the enterprise, complete the following steps to assign a user access to the entire enterprise:
1. Go to **Manage** > **Access (IAM)** > **Users**.
2. Select the name of the user.
2. Click the **Access policies** tab > **Assign access** > **Assign access to account management services**.
3. Select **Enterprise** as the service, and select the name of your enterprise.
4. Select the account group or account in the enterprise that you want to give the user access to. For example, if you want a user to have access to view only a single account, select the account and assign the user the Viewer role or higher. If you want a user to have access to view the entire enterprise, leave the account group and account selections blank, and assign the access.

## Why can't I import an existing account to the enterprise?
{: #troubleshoot-existing-enterprise}
{: troubleshoot}

When you try to import an existing account to enterprise, one of the following issues occurs:
{: tsSymptoms}
* When you click **Add existing account** in the Account section, the account that you want to add is not listed.
* You don't have the option to click **Import account**.

You aren't assigned the correct access, or the account isn't eligible to be imported.
{: tsCauses}

If you can't see the existing account that you want to import, you need the Administrator role on the Billing service of the existing account.
{: tsResolve}

If the **Import account** option isn't available, verify that you have the Administrator or Editor role on the Billing service of the enterprise and the Administrator or Editor role on the Enterprise service for the parent enterprise or account group.

If the account that you want to import is a Pay-As-You-Go account and you're still unable to import it after you verify you have access, the account might not be eligible to be imported into the enterprise. Some Pay-As-You-Go accounts can't be directly imported into an enterprise, such as many Pay-As-You-Go accounts that are billed in United States dollars (USD). Contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![External link icon](../icons/launch-glyph.svg) to convert the account to a Subscription account, and then import it into the enterprise.

## Why can't I create a new account in the enterprise?
{: #troubleshoot-add-enterprise}
{: troubleshoot}

You can't click **Add account** in the Account section.
{: tsSymptoms}

You aren't assigned the correct access.
{: tsCauses}

To create an account in the enterprise, you must have the following access.
{: tsResolve}
1. Administrator role on the Billing service of the enterprise.
2. Administrator or Editor role on the Enterprise service for the targeted parent enterprise or account group.

## Why can't I see the enterprise subscriptions?
{: #troubleshoot-viewsub-enterprise}
{: troubleshoot}

When you go to view the Subscriptions page from a child account, the following message is displayed:
{: tsSymptoms}

`Looks like you don't have permission to view subscription data for this account. Contact your account owner or administrator to request access.`

The following message is displayed in the Billing section on your enterprise dashboard:

`Looks like you don't have permission to view this information. Learn more about IAM access.`

Access to billing and payment information for future billing periods is restricted to users in the enterprise account. Users in a child account can't access billing and payment information, such as subscriptions, even if they previously had access in the account.
{: tsCauses}

To view or manage billing, you need to be invited to the enterprise account and given access to the Billing service in that account. Contact the account owner to request access.
{: tsResolve}

## Why can't I apply a subscription code to my account?  
{: #troubleshoot-promo-enterprise}
{: troubleshoot}

You can't add a subscription code to your account, because you don't have the correct access.  
{: tsSymptoms}

Because your account is a child account on the enterprise, you can't apply subscription codes. Subscription codes must be applied at the enterprise level.
{: tsCauses}

Contact the owner or the administrator of the enterprise to add the subscription code. When the subscription code is added, it applies to all accounts in the enterprise. For more information, see [Managing subscriptions](/docs/billing-usage?topic=billing-usage-subscriptions).
{: tsResolve}
