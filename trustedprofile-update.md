---

copyright:

  years: 2021

lastupdated: "2021-07-26"

keywords: trusted profile, federated users, granting access, update trusted profile, compute resource

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:pre: .pre}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Updating trusted profiles
{: #trusted-profile-update}

You can update the permissions or redefine the trust relationship of the trusted profiles at any time. To update trusted profiles, go to **Manage** > **Access (IAM)** in the console and select **Trusted profiles**. Then, select the name of the trusted profile that you want to update. 
{: shortdesc}

To update trusted profiles, you must be assigned the administrator, operator, or editor role within the account.
{: note}

## Updating trusted profiles in the console
{: #updating-tp-console}

To see the full list of trusted profiles in your account, go to **Manage** > **Access (IAM)** in the {{site.data.keyword.cloud}} console, and select **Trusted profiles**.

### Describe your profile better
{: #description}

Click the name of the trusted profile that you want to update, and select **Actions** > **Edit**. Enter the new name and description, and click **Apply**.

### Redefine the trust relationship
{: #trust}

After the trusted profile is created, you can build trust with both federated users and compute resources in the same trusted profile.

1. Click the name of the trusted profile that you want to update.
2. Click **Add** to add new condition to the existing trust relationship. To edit an existing condition, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Edit** next to the trust relationship you want to update.
  * Click **Add new condition** and repeat as needed to add more conditions.
  * To remove a condition, click the **Close** icon ![Close icon](../icons/close-icon.svg "Close") next to the existing condition.
3. Click **Save** to apply all added conditions to your trusted profile.
  
### Assign access policies
{: #access-policies}

1. Click the name of the trusted profile that you want to update.
2. Click the **Access policies** tab.
3. To assign new access policies, click **Assign access**. To edit existing access policies, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Edit** next to the access policy you want to update.
  * You can select your resources based on resource attributes and any combination of roles to assign.
  * Click **Add** and repeat as needed to add more access.
  * Click **Assign** to assign all added access to your trusted profile.

### Update session limits
{: #session-limit-tp}

1. Click the name of the trusted profile that you want to update.
2. In the federated users section, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") next to the identity provider (IdP) row that you want to update.
3. In hours, add or subtract how long federated users can use this profile before their session expires.
4. Click **Save**. 

