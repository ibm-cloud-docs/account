---

copyright:
  years: 2015, 2019
lastupdated: "2019-05-28"

keywords: account, upgrade, account settings, IBM Cloud account, Lite account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:faq: data-hd-content-type='faq'}
{:tip: .tip}

# FAQs
{: #accountfaqs}

## How do I create an account?
{: #create-account}
{: faq}

Go to [{{site.data.keyword.Bluemix}}](https://cloud.ibm.com){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon"), and click **Create an {{site.data.keyword.Bluemix_notm}} account** to create a Lite account that never expires. See [Lite account](/docs/account?topic=account-liteaccount#liteaccount) for more details about the included features.


## How do I resolve errors that occur when creating my account?
{: #account-error}
{: faq}

If you are able to log in to an {{site.data.keyword.Bluemix_notm}} account, go to [Support](https://test.cloud.ibm.com/unifiedsupport/supportcenter) and choose one of the following options.

* If you have advanced or premium support, click **Live chat** to talk to an {{site.data.keyword.Bluemix_notm}} support representative.
* Create a support case by clicking **Create a case** from the _Need more help_ section.

   After you open the case, an email notification is sent to you. Follow the instructions for further communication.

If you can't log into an {{site.data.keyword.Bluemix_notm}} account, [create an account request](https://watson.service-now.com/x_ibmwc_open_case_app.do#!/create){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon").

## What is Cloud Foundry?
{: #cloud-foundry}
{: faq}

Cloud Foundry is an open source platform as a service (PaaS) option available through {{site.data.keyword.Bluemix_notm}} Public for building and deploying applications on the cloud. Cloud Foundry organizations and spaces are used to organize resources and apps available within specific regions.

For more information about managing orgs and spaces, see [Adding orgs and spaces](/docs/account?topic=account-orgsspacesusers#orgsspacesusers). And, if you’re interested in learning more about how to provide access to resources in a Cloud Foundry space, see [Cloud Foundry access](/docs/iam?topic=iam-cfaccess#cfaccess).


## Can I move an org to another account?
{: #move-org-diff-account}
{: faq}

Currently, you can't move an org to a different account. However, you can recreate the org with the same credentials in a different account to mimic this functionality. For more information, see [Adding orgs and spaces](https://cloud.ibm.com/docs/account?topic=account-orgsspacesusers#createorg).


## Which Cloud Foundry regions can I use?
{: #whichregions}
{: faq}

In a Lite account, you can work in only one region. In a Pay-As-You-Go or Subscription account, you can access all available regions.


## What's a Lite pricing plan for services?
{: #whatisliteplan}
{: faq}

A Lite plan is a free quota-based service plan. You can use a service Lite plan to build an app without incurring any charges. A Lite plan might be offered on a monthly cycle that is renewed each month or on a one-off usage basis. You can have one instance per Lite plan service. Lite pricing plans are offered in all accounts. For more information about Lite accounts, see [Account types](/docs/account?topic=account-accounts#accounts).


## What happens when my Lite plan instance reaches the monthly quota?
{: #monthlyquota}
{: faq}

Reaching any quota limit for Lite plan instances suspends the service for that month. Quota limits are per org, not per instance. New instances that are created in the same org reflect any usage from previous instances. The quota limits reset on the first of every month.

You can check your usage by going to **Manage > Billing and usage** and selecting **Usage**. For more information, see [Viewing your usage](/docs/billing-usage?topic=billing-usage-viewingusage).

## How do I delete a service from my account?
{: #accounts-service-removal}
{: faq}

If you want to stop or delete a service, you can do so from the resource list. Learn more in [Navigating the {{site.data.keyword.Bluemix_notm}} console](/docs/overview?topic=overview-ui).

## How many resource groups, orgs, or spaces can I create?
{: #resourcelimit}
{: faq}

If you have a billable account, there's no limit to the number of resource groups, orgs, or spaces that you can create within your account. However, if you have a Lite account, you're limited to one org and one resource group.

## How do I upgrade or convert my account type?
{: #changeacct}
{: faq}

To upgrade your Lite account, go to [Account settings](https://{DomainName}/account/settings). In the Account Upgrade section, click **Add credit card** to upgrade to a Pay-As-You-Go account, or click **Upgrade** for a Subscription account. You can also apply a promotional feature code to convert your Lite account to a trial account on the Account settings page.

To convert between Pay-As-You-Go and Subscription account types, contact [{{site.data.keyword.Bluemix_notm}} Sales ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}.

If you're not sure of your current account type, you can find it on the Account settings page. Learn more in [Upgrading your account](/docs/account?topic=account-upgrading-account).

## If I upgrade my Lite account, can I continue to use my existing instances?
{: #nochange}
{: faq}

Yes, when you upgrade to a billable account, you can continue to use the instances you created with your Lite account.

## How do I update my credit card?
{: #updatepayment}
{: faq}

Updating your credit card is just like adding a new one. Go to [Payments](https://{DomainName}/billing/payments), and in the Add Payment Method section, enter the billing information for your new card, then click **Add credit card**.

To switch to a different payment method, select **Pay with Other** and then click **Submit change request**. A support case to change your payment method will be created for you.

## How do I change my email notification settings?
{: #change-email-prefs}
{: faq}

You can change which email notifications you receive for planned events, unplanned events, and announcements in your profile settings.
1. Go to [Notifications](https://cloud.ibm.com/user/notifications) in your profile settings.
1. Select whether to receive email notifications for each type of event.

For classic infrastructure services, account owners can also subscribe users to notifications from those services by going to **Manage > Account > Notifications**.

For more information, see [Setting email preferences](/docs/account?topic=account-email-prefs).

## How do I reset my password?
{: #reset-password}
{: faq}

To reset your account password, go to the Avatar icon ![Avatar icon](../icons/i-avatar-icon.svg) **> Profile and settings**. Then, click **Change or reset** from the Account user information tile.

To reset your VPN password, complete the following steps:

  1. Go to **Manage > Access (IAM)**, and select **Users**.
  2. Select the user.
  3. From the VPN subnets section, click the Edit icon ![Edit icon](../icons/icon_write.svg) to enter a new VPN password.
  5. Click **Apply**.

## How do I cancel my account?
{: #cancelaccount}
{: faq}

We're sad to see you go! If there's any way we can assist you with your account before you go, reach out to us by contacting support.

If you do decide to leave, how you cancel your account depends on your account type. You can check your account type by going to [Account settings](https://cloud.ibm.com/account/settings) and looking under _Account Type_.

* For Pay-As-You-Go or Subscription accounts, the quickest way to cancel your account is to contact us through [live chat](https://{DomainName}/unifiedsupport/supportcenter) or by calling 1-866-325-0045 and selecting the third option. Alternatively, you can open a support case.
* To cancel a Lite account, go to [Account settings](https://cloud.ibm.com/account/settings) and click **Deactivate account**.

## How do I delete my account?
{: #deleteaccount}
{: faq}

Contact [{{site.data.keyword.Bluemix_notm}} Support ![External link icon](../icons/launch-glyph.svg)](https://{DomainName}/unifiedsupport/supportcenter){: new_window} to open a support case and request to delete your account. If you have data that is associated with your old account that you want to move to a new account, include this information in your email.

## How can I remove my personal data from {{site.data.keyword.Bluemix_notm}}?
{: #remove-pi}
{: faq}

To understand how IBM handles your personal information, see the [IBM Privacy Statement ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/privacy/){: new_window}. In the Your Rights section, review the information about what you can request to remove. Click the link in the section to submit a request to remove your personal information.

## Why is my account deactivated?
{: #account-deactivated}
{: faq}

Your account might be deactivated for the following reasons:

- For trial accounts, the trial period ended. To reactivate your account, log in to your account and upgrade it to a Pay-As-You-Go account.
- An authorized user canceled the account.
- The account is suspended. At the discretion of IBM, accounts that violate the acceptable usage behaviors of the {{site.data.keyword.Bluemix_notm}} services can be disabled without notice. Some services can be restored if users correct their usage behaviors after they're notified of the offensive action.

If you believe your account was deactivated in error, contact support by calling 1-866-325-0045 and selecting the third option.

## How do I get support?
{: #contactsupport}
{: faq}

Click **Support** from the console menu bar to go to the Support Center. Learn more about support in [Getting support](/docs/get-support?topic=get-support-support-plans).

## Can I sign up for a free trial?
{: #freetrial}
{: faq}

{{site.data.keyword.Bluemix_notm}} trial accounts are available for faculty and students at accredited academic institutions. To qualify for a trial account, go to [Harness the Power of IBM ![External link icon](../icons/launch-glyph.svg)](https://onthehub.com/ibm/){: new_window} and validate your institution credentials.

## After I link my account, how do I log in?
{: #al_login}
{: faq}

After you link your account, use your IBMid to log in to the {{site.data.keyword.Bluemix}} console.

## After I link my account, what's the impact on my support?
{: #al_support}
{: faq}

After you link your account, you keep the same level of support when you add {{site.data.keyword.Bluemix_notm}} platform to your account.

## Are there other ways to get help with linking my account?
{: #al_morehelp}
{: faq}

  1. See the [Steps to Link your IaaS and PaaS Accounts blog](https://www.ibm.com/blogs/bluemix/2018/03/follow-steps-link-iaas-paas-accounts/){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon") for helpful information.
  2. From the {{site.data.keyword.BluSoftlayer_full}} customer portal, open a **Sales Live Chat** to ask account questions.
  3. Open a ticket from the customer portal. Select **Support** > **Add ticket** and then, in the **Subject** field, select **Accounting Request** to route your account question to the correct support team.

## How do I link my account if I have several accounts?
{: #al_multacct}
{: faq}

If you have multiple SoftLayer accounts, you must link the accounts that have a matching {{site.data.keyword.Bluemix_notm}} platform account, and an accompanying IBMid.

If you don't have a matching {{site.data.keyword.Bluemix_notm}} platform account, and an accompanying IBMid account, a new SoftLayer account can be created to link the accounts.

## Are there incentives for linking my accounts?
{: #al_incent}
{: faq}

When you link your accounts, you can use a $200 promotional credit to try {{site.data.keyword.Bluemix_notm}} services.

To learn more about the $200 promotional credit, see [Pay-As-You-Go account](/docs/account?topic=account-accounts#paygo).

## What does adding {{site.data.keyword.Bluemix_notm}} platform services to my SoftLayer account mean?
{: #al_owaffslacct}
{: faq}

It means that your account has access to all {{site.data.keyword.Bluemix_notm}} platform offerings. After you add the {{site.data.keyword.Bluemix_notm}} platform offering to your account, your account master must enable the user to have access to the offering.

For more information about being an account master, see [Working with users](/docs/iam?topic=iam-iamuserinv#iamuserinv).

## How does linking accounts impact my SoftLayer Master Account ID?
{: #al_howaffslmastacct}
{: faq}

You can still use the ID for your SoftLayer account to sign in to the customer portal because the {{site.data.keyword.Bluemix_notm}} console is accessible with IBMids.

## How can I view accounts that I own?
{: #accounts-owned}
{: faq}

The IBM Cloud console header lists all accounts that are affiliated with your login ID, including those you own. You can view your role in each account on the [Users](https://{DomainName}/iam/users) page.

You can also find your accounts from the CLI by running the `ibmcloud account list` command.

## How do I switch between multiple accounts?
{: #switch-between-accounts}
{: faq}

If you have more than one account, you can click your account name to select another account that you have access to.  

![Account switcher screen capture.](images/account-faq.svg "Account switcher screen capture")

## Can I make someone else the account owner?
{: #switch-account-owners}
{: faq}

You can transfer ownership of individual resources within your account to someone else by using the `ibmcloud catalog` command. To learn more, see [Transferring ownership of a private resource](/docs/account?topic=account-include#owners).

Transferring ownership of your entire account requires additional help from support. To get help, [contact support](/docs/get-support?topic=get-support-getting-customer-support).

## Does {{site.data.keyword.Bluemix_notm}} support batch registration of users?
{: #batch-registration}
{:faq}

When you register users for {{site.data.keyword.Bluemix_notm}}, you must register each user individually. {{site.data.keyword.Bluemix_notm}} doesn't support batch registration of users.

Go to [{{site.data.keyword.Bluemix}}](https://cloud.ibm.com){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon"), and click **Create an {{site.data.keyword.Bluemix_notm}} account**. Then, complete the account registration form for each individual user.

## What are tags?
{: #know-about-tags}
{: faq}

You can use tags to organize and view resources across your account by filtering tags from your resource list. For more information, see [Working with tags](/docs/resources?topic=resources-tag).

## Who can view the tags in an account?
{: #tags-visibility-account}
{: faq}

Tags are visible throughout your account. If you have permission to see a resource, you can view all tags that are attached. For more information, see [Granting users access to tag resources](/docs/resources?topic=resources-access#access).

## What permissions do I need to add or remove tags?
{: #permissions-add-remove-tags}
{: faq}

You must have at least the Editor for IAM-enabled resources or the developer role in a Cloud Foundry space on a resource to add or remove tags on that resource. For more information, see [Granting users access to tag resources](/docs/resources?topic=resources-access#access).

## Can I delete my tag?
{: # delete-tag}
{: faq}

Before you can delete a tag, you must remove it from all resources. If you still can't delete it, the tag might be attached to a resource that you don't have permission to view. The same tag can be attached to several resources by different users in the same billing account. Users don't have the same visibility on all resources on the account.

## Can I rename a tag?
{: #rename-tag}
{: faq}

You can't edit the name of a tag. To rename a tag, remove it and reassign the resource with a new tag.
