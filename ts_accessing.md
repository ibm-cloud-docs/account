---

copyright:
  years: 2015, 2019
lastupdated: "2019-06-03"

keywords: troubleshoot account, account problem, account support, account help, account error, access error, login error, error message

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


# Troubleshooting for accessing {{site.data.keyword.Bluemix_notm}}
{: #accessing}

General problems with accessing {{site.data.keyword.Bluemix}} might include difficulties logging in to {{site.data.keyword.Bluemix_notm}} or an account that is in a pending state. In many cases, you can recover from these problems by following a few easy steps.
{:shortdesc}


## Why is my password incorrect?
{: #ts_logintobm}
{: troubleshoot}

You must have a valid password that's associated with your IBMid or SoftLayer ID to log in to the {{site.data.keyword.Bluemix_notm}} console.

When you try to log in to {{site.data.keyword.Bluemix_notm}}, the following error message is displayed:
{: tsSymptoms}

`The password that you entered is not correct.`

The password that you used to log in to {{site.data.keyword.Bluemix_notm}} isn't valid.
{: tsCauses}

Use one of the following options:
{: tsResolve}
 * Go to the [My IBM profile page ![External link icon](../icons/launch-glyph.svg "External link icon")](https://myibm.ibm.com/dashboard/){: new_window} to confirm that you're using a valid password.
 * If you forgot your password, click **Forgot your password** to reset your password.
 * If you forgot your IBMid or continue to have problems with your password, contact the Worldwide IBM Registration Help Desk for help.

If you sign in to {{site.data.keyword.Bluemix_notm}} and the log in process is disrupted for any reason, like resetting your password, return to the console and start the log in process again.
{: tip}


## Why was my IBMid or email not recognized?
{: #ts_old_username}
{: troubleshoot}

To successfully log into your email, you would have to make sure you have IBMid authentication for each account.

When you log in to the {{site.data.keyword.Bluemix_notm}} console, the following message is displayed:
{: tsSymptoms}

`We didn't recognize this IBMid or email.`

You tried to log in to the console, but didn't use a valid IBMid. For example, you didn't enter a fully qualified email address for the IBMid, or you tried to use a previous username and password.
{: tsCauses}

You must have a valid IBMid and password to log in to {{site.data.keyword.Bluemix_notm}}.

 * Enter a fully qualified email address for the IBMid.
 {: tsResolve}
 * If you're a SoftLayer user with a SoftLayer ID, you must switch to IBMid authentication in each account that you have access to before you can log in. For more information, see [Switching to IBMid](/docs/account?topic=account-unifyingaccounts).


## Why is my IBMid not associated with any {{site.data.keyword.Bluemix_notm}} accounts?
{: #ts_unabletologin}
{: troubleshoot}

When you log in to {{site.data.keyword.Bluemix_notm}}, the following message is displayed:
{: tsSymptoms}

`You have reached this page because your authentication was successful, however, this IBMid is not associated with any {{site.data.keyword.Bluemix_notm}} accounts.`

You logged in from the [{{site.data.keyword.Bluemix_notm}} console](https://{DomainName}){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon") with a valid IBMid, but you don't have an {{site.data.keyword.Bluemix_notm}} account created.
{: tsCauses}

To create an {{site.data.keyword.Bluemix_notm}} account, follow the sign up process.
{: tsResolve}


## Why doesn't the console open when I log in with my IBMid?
{: #ts_login_stalls}
{: troubleshoot}

When you get a login success message, but you don't return to the console.

When you log in using your IBMid, a login success message is displayed, but you don't return to the [{{site.data.keyword.Bluemix_notm}} console](https://{DomainName}){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon").
{: tsSymptoms}

Use one of the following options:
{: tsResolve}
 * Close your browser, clear the cache and cookies, then try to log in again.
 * Log in from the [{{site.data.keyword.Bluemix_notm}} console](https://{DomainName}){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon").


## Why didn't my IBMid login complete?
{: #ts_login_ibmid}
{: troubleshoot}

If you log in to {{site.data.keyword.Bluemix_notm}} and the authentication of your IBMid doesn't complete, then there might be a problem with the service.

When you log in to {{site.data.keyword.Bluemix_notm}}, authenticating with IBMid doesn't complete.
{: tsSymptoms}

There might be a problem with the IBMid authentication service.
{: tsCauses}

Make sure you can log in to [IBM](https://idaas.iam.ibm.com/idaas/mtfim/sps/authsvc?PolicyId=urn:ibm:security:authentication:asf:basicldapuser){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon"). if you can, it is an application problem and you can try logging in to the console again later. If you can't log in to that page, contact the [IBMid help desk ![External link icon](../icons/launch-glyph.svg "External link icon")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}.  
{: tsResolve}


## Why can't I log in immediately after I register an account?
{: #ts_accntpding}
{: troubleshoot}

If your account is still pending, you won't be able to log in to {{site.data.keyword.Bluemix_notm}}.

After you register for an {{site.data.keyword.Bluemix_notm}} account, you might not be able to log in to {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

When you register for an {{site.data.keyword.Bluemix_notm}} account, you receive an email that includes a confirmation link. You must click this link to confirm your registration. If you don't confirm your registration, your account remains in a pending state.
{: tsCauses}

The confirmation email is sent to the email address that is associated with your IBMid. Check your inbox and your spam folder. If you haven't received the confirmation email, go to the [{{site.data.keyword.Bluemix_notm}} login page](https://cloud.ibm.com/){: new_window} ![External link icon](../icons/launch-glyph.svg "External link icon") and try to log in. The following message is displayed:
{: tsResolve}

```
To complete your registration, check your email.
Can't find the email? Resend
```
{:screen}

Click **Resend** to send another confirmation email to the email address that is associated with your IBMid. If you still can't complete your registration, contact [{{site.data.keyword.Bluemix_notm}} support](/docs/get-support?topic=get-support-getting-customer-support).  

## Why do I encounter console pages that don't load?
{: #ts_err}
{: troubleshoot}

When you use the {{site.data.keyword.Bluemix_notm}} console, you might not be able to load a console page. Instead, you might see error messages BXNUI0001E or BXNUI0016E.

You might see one of the following error messages:
{: tsSymptoms}

`BXNUI0001E: The page wasn't loaded because {{site.data.keyword.Bluemix_notm}} didn't detect whether a session exists.`

`BXNUI0016E: The apps and services weren't retrieved because an {{site.data.keyword.Bluemix_notm}} page didn't load.`

Complete one or more of the following actions, as necessary:
{: tsResolve}

  * Refresh or restart your browser.
  * Log out of {{site.data.keyword.Bluemix_notm}} and log in again.
  * Use the private browsing mode of your browser.
  * Clear the cookies and the cache of the browser.
  * Use a different browser. For information about the versions of the browsers that are supported by {{site.data.keyword.Bluemix_notm}}, see [{{site.data.keyword.Bluemix_notm}} prerequisites](/docs/overview?topic=overview-prereqs-platform).
  * If you installed the Cloud Foundry command line interface, enter the `ibmcloud cf apps` command to see whether your app is running.

## How can I access infrastructure services in my account?
{: #troubleshoot-infrastructure-access}
{: troubleshoot}

When you attempt to access infrastructure sections of the IBM Cloud console, you see a message that states:
{: tsSymptoms}

`This page can't be loaded because your infrastructure account is not fully configured as an IBM Cloud account.`

There are multiple reasons why you might see this error message:
{: tsCauses}

* You have a [Lite account](/docs/account?topic=account-accounts#liteaccount), which does not allow access to infrastructure services.
* Your account is not linked to an infrastructure account.


To resolve this issue, you must upgrade to a Pay-As-You-Go or Subscription account. For information, see [Upgrading your account](/docs/account?topic=account-upgrading-account).
{: tsResolve}
