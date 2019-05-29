---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-29"

keywords: troubleshoot account, account problem, account support, account help, org error, resource error, error message

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

# Troubleshooting for managing accounts
{: #managingaccounts}

General problems with managing your account might include different apps that have the same domain name, or administrators can't view all organizations. In many cases, you can recover from these problems by following a few easy steps.
{:shortdesc}


## Why can't I access a different {{site.data.keyword.Bluemix_notm}} location?
{: #nosecondreg}
{: troubleshoot}

You're unable to create a new location because your account type doesn't allow it.

You receive an error message when you try to create a new {{site.data.keyword.Bluemix_notm}} location.
{: tsSymptoms}

This is likely because you're using a Lite account, which supports development in one public location only. For more information about Lite account features, see [Lite account](/docs/account?topic=account-accounts#liteaccount).
{: tsCauses}

To access more locations, upgrade to a billable account. Go to **Manage > Account**, and select **Account settings**. In the Account upgrade section, select your upgrade option.
{: tsResolve}


## Why can't I create a new organization?
{: #nosecondorg}
{: troubleshoot}

You try to create more than one org, and you have a Lite account.  

You receive an error message when you try to create a new organization.
{: tsSymptoms}

You're likely seeing this error because you're using a Lite account, which supports development in one organization only. For more information about Lite account features, see [Lite account](/docs/account?topic=account-accounts#liteaccount).
{: tsCauses}

To create a new org, upgrade to a billable account. Go to **Manage > Billing and usage**, and select **Payments**.
{: tsResolve}


## Why can't I create a new Lite plan instance?
{: #nosecondlite}
{: troubleshoot}

You try to create an extra instance, but you have a Lite account.

You receive the following error message when you try to create a new Lite plan instance:
{: tsSymptoms}

`Unable to provision new Lite instance`

There's a limit of one instance per Lite plan instance to ensure that these plans stay free. For more information about Lite account features, see [Lite account](/docs/account?topic=account-accounts#liteaccount).
{: tsCauses}

You can create more instances of the service by selecting one of the billable service plans, which are available in the billable accounts. To upgrade to a billable account from the console, go to **Manage > Account**, and select **Account settings**.
{: tsResolve}

If you don't want to upgrade from a Lite account and are no longer using your existing Lite service instance, you can delete the existing Lite plan instance from the dashboard and then create a new instance.


## How did I exceed the runtime memory allowance?
{: #noruntimemem}
{: troubleshoot}

You've gone over the allowed memory for your account.

You're unable to deploy apps, and an error states that you've exceeded your organization's memory limit.
{: tsSymptoms}

In a Lite account, your Cloud Foundry apps can use up to 256 MB of instantaneous runtime memory. In billable accounts, there's a 2 GB memory limit.
{: tsCauses}

If you're using a Lite account, you can get more memory by upgrading to a billable account. Go to **Manage > Account**, and select **Account settings**. For more information about Lite account features, see [Lite account](/docs/account?topic=account-accounts#liteaccount).
{: tsResolve}

If you don't want to upgrade from a Lite account but have some idle apps, you can delete them to free up some runtime memory.


## Why is my account inactive?
{: #ts_accnt_inactive}
{: troubleshoot}

You can't create an app in {{site.data.keyword.Bluemix_notm}} if your account is inactive. You must contact the support team to fix this problem.

When you try to create an app in {{site.data.keyword.Bluemix_notm}}, the following error message is displayed:
{: tsSymptoms}

`BXNUI0096E: The app wasn't created. Your account is inactive because it was canceled or suspended.`

The status of your {{site.data.keyword.Bluemix_notm}} account becomes inactive when the account is canceled or suspended.
{: tsCauses}

To reactivate your account, open a case from the [support center](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon"). Include the following information in your case:
{: tsResolve}

  * The IBMid that you use to log in to {{site.data.keyword.Bluemix_notm}}.
  * The name of the organization in which your app is being created. This information can help the support team determine whether you're assigned the correct roles or membership in your organization.


## Why can't I add users to an org?
{: #ts_adduser}
{: troubleshoot}

You can invite users to your organization only if you're the account owner, or if you're both a manager and a member of the organization.

You can't see the **Invite a New User** link in your **Manage Organizations** section.
{: tsSymptoms}

Only the following {{site.data.keyword.Bluemix_notm}} users can invite users to an organization:
{: tsCauses}
  * The account owner of the organization
  * Organization managers who are also members, not collaborators, of the organization

In {{site.data.keyword.Bluemix_notm}}, you can be either a member or a collaborator of an organization:

<dl><dt>Collaborator</dt>
<dd>You are a collaborator of an organization if you already have an {{site.data.keyword.Bluemix_notm}} account, and someone else invites you to the organization.</dd>
<dt>Member</dt>
<dd>You are a member of an organization if you don't have an {{site.data.keyword.Bluemix_notm}} account, but then someone invites you to the organization and you sign up for {{site.data.keyword.Bluemix_notm}} from the invitation.</dd>
</dl>

You can't invite users to your organization if you're a collaborator of the organization, even if you're assigned as an organization manager.

All organization managers, including collaborators in an organization, can add, modify, and remove users that are already in the organization.
{: note}

If you can't invite users to your organization and need a different role to do so, contact your organization manager to change your role. To identify your organization manager, complete the following steps:
{: tsResolve}

  1. From the console menu bar, click **Manage > Account**, and select **Company contacts**.
  2. Go to your organization, and view the information of organization manager on the **USERS** tab.  

If you can't invite users because you're a collaborator and not a member, you must delete your previous {{site.data.keyword.Bluemix_notm}} account and then be invited to join the account as a member of the organization. To delete your previous account and join the account as a member, complete the following steps:

  1. Contact [{{site.data.keyword.Bluemix_notm}} Support ![External link icon](../icons/launch-glyph.svg "External link icon")](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} to open a support case and request that your account be deleted. If you have data that is associated with your old account that you want to save and move to the new account, include this information in your email.
  2. After your account is deleted, have a user with the organization manager role invite you to the organization as an organization manager. Then, sign up for {{site.data.keyword.Bluemix_notm}} from the invitation.


## Why are no spaces associated with my current org?
{: #ts_no_space}
{: troubleshoot}

You can't create an app if no space is associated with your current organization.

When you try to create an app the following error message is displayed:
{: tsSymptoms}

`BXNUI0097E: Before you can add an app, at least one space must be associated with your organization and region. On the Dashboard, click Create a Space. When the space is created, try again.`

Apps must be created in a space under your organization.
{: tsCauses}

To create a space, use one of the following methods:
{: tsResolve}

  * From the console menu bar, click **Manage > Account**. Expand **Account resources** and click **Cloud Foundry orgs**.
  Then, select the organization in which you want to create the space, and click **Add a space**.
  * In the {{site.data.keyword.Bluemix_notm}} command line interface, type `ibmcloud account space-create <space_name> -o <organization_name>`.


## Why do some apps share a domain name?
{: #ts_domain_diff}
{: troubleshoot}

You might notice that several apps share a URL in {{site.data.keyword.Bluemix_notm}}.

This problem might happen when you assign the same URL route for different apps in a space.
{: tsCauses}

For example, you push the myApp1 app to {{site.data.keyword.Bluemix_notm}} and set the domain to `mynewapp.us-east.cf.appdomain.cloud`. Then, you push another myApp2 app to the same space and set one of its URL routes to `mynewapp.us-east.cf.appdomain.cloud`. The route is now mapped to both apps.

This behavior is supported, and you can use this practice to achieve zero downtime for your app upgrade. For more information, see [How to ensure zero downtime](/docs/overview?topic=overview-zero-downtime).
{: tsResolve}


## Why can't administrators use the console to view all orgs?
{: #ts_ui_org}
{: troubleshoot}

As an administrator, you can't display every organization to administer them when you use the {{site.data.keyword.Bluemix_notm}} console. You can display and administer only those organizations to which you belong.

As an administrator, you can't view all the organizations from the console.
{: tsSymptoms}

This behavior is a limitation of the console.
{: tsCauses}

You can use commands such as `ibmcloud account orgs` and `ibmcloud account org-create` from the {{site.data.keyword.Bluemix_notm}} command line interface to manage all the organizations. For a full list of commands, enter `ibmcloud account help`.
{: tsResolve}


## Why can't I submit the form to add my credit card information?
{: #ts_addcc}
{: troubleshoot}

You can't submit your credit card information to upgrade your Lite account to a billable account.

The **Submit** button on the Add credit card page is disabled.
{: tsSymptoms}

This problem happens when your information isn't completed correctly on the Add credit card page.
{: tsCauses}

Complete the following steps:
{: tsResolve}

  1. On the Add credit card page, complete all the required fields.
  2. Select **I have read and agree to IBM's Terms and Conditions**, then click **Submit**.

## How do I add a credit card when the option is unavailable through the console?
{: #ts_ccibm}
{: troubleshoot}

You want to enter a credit card to pay for {{site.data.keyword.Bluemix_notm}} services, but the option doesn't appear.

When you try to enter your credit card information, you see the following message:
{: tsSymptoms}

`Your payments are managed through IBM.com. To view your payments and maintain your billing, you can visit the IBM.com portal which contains everything for your IBMid account.`

You click **Explore** to access the ibm.com website, but you don't see a location to enter your credit card information.

We securely process credit card transactions through the {{site.data.keyword.Bluemix_notm}} console. However, in some countries, we must take additional steps to ensure the integrity of the credit card data. Those credit card requests are completed through the ibm.com website. Both methods ensure that your credit card information is securely processed.   
{: tsCauses}

To provide your credit card information for payment, complete the following steps:
{: tsResolve}

  1. Go to [ibm.com ![External link icon](../icons/launch-glyph.svg "External link icon")](http://www.ibm.com){: new_window} and log in with the same IBMid and password that you use to log in to {{site.data.keyword.Bluemix_notm}}.
  1. Click the Avatar icon ![Avatar icon](../icons/i-avatar-icon.svg), and select **Billing**.
  1. Click **Manage payment method**.
  1. Enter your credit card information, and click **Register**.

The information will be verified and added to your {{site.data.keyword.Bluemix_notm}} account as your payment method for any charges.
