---

copyright:

  years: 2019, 2025
lastupdated: "2025-11-05"

keywords: change owner, transfer account, transfer account ownership, switch owner, transfer owner, classic infrastructure, account owner, second account owner, two account owners, alternative account owner, trusted profile

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Updating account ownership
{: #transfer}

You can update your {{site.data.keyword.cloud}} account's ownership and transfer your account to a different owner by creating a support case with information about the new owner. You can transfer only Pay-As-You-Go or Subscription accounts. If you're the owner of an account with classic infrastructure, you can also set a [trusted profile](/docs/account?topic=account-create-trusted-profile) as the alternative account owner. The alternative account owner has the highest level of classic infrastructure permissions and more capabilities. An alternative account owner helps ensure that you always have a secure way to manage account ownership. For example, if the primary account owner leaves your organization or isn't available.
{: shortdesc}

Every {{site.data.keyword.cloud_notm}} account must have a valid account owner. Accounts without a valid account owner are subject to suspension and possible termination.
{: note}

## Transferring an account that you own
{: #transfer-own}

As the account owner, you can transfer the account ownership only by creating a support case. The new owner must be an existing user within the account. If the person that you want to own the account isn't an existing user, [invite them to the account](/docs/account?topic=account-iamuserinv) before you create the support case.

To create the support case, click the **Help** icon ![Help icon](../icons/help.svg "Help") > **Support center** from the console menu bar, and click **Create a case**. In the case description, include the full name and IBMid of the user that is to be the new account owner. {{site.data.keyword.cloud_notm}} Support completes the ownership change as directed by the account owner.

When you transfer your account to a new owner, the previous account owner is automatically removed from the account. The new owner can invite the account's previous owner back to the transferred account as necessary. To help ensure the security of the account, {{site.data.keyword.cloud_notm}} Support cannot modify the account's user list.
{: note}

## Transferring an account from another owner
{: #transfer-lost}

If the owner of an account leaves the company and there is a need to transfer the account, a new owner must be identified. Then, create a support case to request a transfer.

The new owner must have an IBMid or be a user of the account. If the user does not have an IBMid, the new owner must create the IBMid and be added to the account by another user.

In the support case to request an account transfer, you must attach an official document from your company that contains the following information.
- Your official company letterhead
- Your company's article of incorporation, if applicable
- A statement that the individual is no longer associated with your company
- An explanation that you want the account owner to be changed to a new owner
- The given name and surname of the new account owner
- The email address and phone number of the new account owner
- A signature of an executive at your company
- The account number of the account to transfer

To create the support case, click the **Help** icon ![Help icon](../icons/help.svg "Help") > **Support center** from the console menu bar, and click **Create a case**. Attach the official request document to the case before you submit it.

When the ownership is transferred to the new owner, the previous account owner is automatically removed from that account, and the new owner has full access to the account. The new owner needs to invite the account's previous owner to the account if they still need access.
{: note}

When you're logged in to the account, you can find the account number in the {{site.data.keyword.cloud_notm}} menu bar next to the account name. For example, you might see `1234567 - IBM`, where the account number is 1234567.

![A screen capture of the account selector in the console menu bar. The account selector displays the account name and account number, and you select the current account to display a list of other accounts that you can access.](images/account-switcher.svg "The account selector displays the account name and account number, and you select the current account to display a list of other accounts that you can access."){: caption="How to switch between trusted profiles and accounts" caption-side="bottom"}

## Granting alternative account owner access
{: #grant-alt-owner}
{: support}
{: help}

Alternative account owner access grants the following assignments:

- Administrator and manager roles on All Identity and Access enabled services
- Administrator role on All Account Management services
- A classic infrastructure flag that indicates the trusted profile is the alternative account owner

You can set only one trusted profile as the alternative account owner. A trusted profile with alternative account owner access can't be modified after creation. If you create another alternative account owner, an error occurs. For more information, see [troubleshooting](/docs/account?topic=account-ts_alt-owner).
{: important}

To set a trusted profile as the alternative account owner, complete the following steps.

1. Go to **Manage** > **Access (IAM)** in the {{site.data.keyword.cloud_notm}} console.
1. Select **Trusted profiles**.
1. Click **Create**.
1. Set the **Alternative account owner access** toggle to **Yes**.
1. Click **Continue**.
1. Define which federated users can apply the trusted profile. For more information, see [Establishing trust with federated users](/docs/account?topic=account-create-trusted-profile&interface=ui#create-profile-federated-ui).
1. Click **Continue**.
1. Review the policies and permissions that the trusted profile is assigned.
1. Click **Create**.

The `alt owner` label indicates the trusted profile with alternative account owner access in the trusted profiles table.

Users with the administrator, operator, or editor role on the IAM Identity service can grant or revoke access to the trusted profile at any time by [updating the trust relationship](/docs/account?topic=account-trusted-profile-update&interface=ui#trust).
{: note}

## Differentiating between the account owner and the alternative account owner
{: #acct-owner-table}

The alternative account owner doesn't replace the account owner, but they share some of the same privileges.

Every {{site.data.keyword.cloud_notm}} account must have a valid account owner. Accounts without a valid account owner are subject to suspension and possible termination. For more information, see [Transferring ownership of your account](/docs/account?topic=account-transfer&interface=ui).
{: note}

The following table shows the difference between the account owner and the alternative account owner:

| Privileges | Account owner       | Alternative account owner |
|---------------------|---------------------------|------|
| Full access to all resources |![Checkmark icon](../icons/checkmark-icon.svg) | ![Checkmark icon](../icons/checkmark-icon.svg)|
| Assign access to others | ![Checkmark icon](../icons/checkmark-icon.svg) | ![Checkmark icon](../icons/checkmark-icon.svg)|
| Update the account owner | ![Checkmark icon](../icons/checkmark-icon.svg) |  |
| View all users | ![Checkmark icon](../icons/checkmark-icon.svg) | ![Checkmark icon](../icons/checkmark-icon.svg)|
| Set user visibility | ![Checkmark icon](../icons/checkmark-icon.svg) | ![Checkmark icon](../icons/checkmark-icon.svg)|
| Billing responsibility | ![Checkmark icon](../icons/checkmark-icon.svg) |  |
| Owner notifications | ![Checkmark icon](../icons/checkmark-icon.svg) |  |
| Default email | ![Checkmark icon](../icons/checkmark-icon.svg) |  |
{: row-headers}
{: class="comparison-table"}
{: caption="Account owner and alternative account owner comparison." caption-side="bottom"}
