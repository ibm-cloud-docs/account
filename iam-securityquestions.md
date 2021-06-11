---

copyright:

  years: 2018, 2021

lastupdated: "2021-06-11"

keywords: security questions, MFA, multifactor authentication, login security

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}

# Enabling MFA security questions for a user
{: #questions}

As an administrator with the correct access, you can enable the option for a user to be prompted for security questions and answers at login. This type of multifactor authentication (MFA) is required only for the account where the setting is enabled. This type of multifactor authentication (MFA) is required only for the account where the setting is enabled unlike ID-based MFA. For more information, see [Types of multifactor authentication](/docs/account?topic=account-types).
{:shortdesc}

## Before you begin
{: #security-question-access}

If you have any of the following types of access, you can update this setting for other users in your account:

* Editor or higher role on the User management service
* You are an ancestor in the classic infrastructure hierarchy for the user and you have the Manage users classic infrastructure permission assigned

## Enabling security questions
{: #enable-security-question}

To turn on this MFA option for a user, the user must set up [security questions](#security-questions-setup) and answers from the profile Login settings page.
{: note}

1. In the {{site.data.keyword.cloud}} console, click **Manage** > **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the **User details** page in the **Manage user's login** section, set the **Require MFA security questions at login** option to on.

You can manage this setting for yourself if you have the User-managed login setting enabled on your User details page.
{: tip}

## Setting up security questions
{: #security-questions-setup}

You can set up answers to three security questions for extra authentication at login. You must set up your security questions and answers before your administrator can enable this MFA requirement for you.

To set up your security questions:
1. From the console, go to Go to **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") > **Profile and settings**, and select **Login settings**.
2. Click **Set up**.

   If you previously set up security questions, click **Edit**.
3. Select the questions that you want to have and answer them. You must use three security question options.
4. Click **Save** when you're finished.  
5. Select the **Yes** checkbox for the security questions to be enabled. Selecting this option might prompt you to sign in to your account again.  

   If this option isn't selected, you don't have access to turn on security questions. You must be the account owner or have the User-managed login setting that is enabled for you by your account administrator to turn security questions on and off. Contact your account owner or administrator to get access.
   {: note}
