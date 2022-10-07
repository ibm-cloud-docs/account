---

copyright:
  years: 2022
lastupdated: "2022-10-07"

keywords: classic infrastructure, account owner, second account owner, two account owners, alternative account owner, trusted profile

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Setting an alternative account owner
{: #classic-infra-owner}

As the owner of an account with classic infrastructure, you can set a [trusted profile](/docs/account?topic=account-create-trusted-profile) as the alternative account owner. The alternative account owner has the highest level of classic infrastructure permissions and more capabilities. An alternative account owner ensures that you always have a secure way to manage account ownership if the primary account owner leaves your organization or isn't available.
{: shortdesc}

Only accounts with classic infrastructure can set an alternative account owner.
{: preview}

## Granting alternative account owner access
{: #grant-alt-owner}

Alternative account owner access grants the following assignments:
- Administrator and manager roles on All Identity and Access enabled services
- Administrator role on All Account Management services
- A classic infrastructure flag that indicates the trusted profile is the alternative account owner

You can set only one trusted profile as the alternative account owner. A trusted profile with alternative account owner access can't be modified after creation.

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

The trusted profile with alternative account owner access is indicated by `alt owner` in the trusted profiles table.

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
