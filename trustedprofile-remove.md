---

copyright:

  years: 2021

lastupdated: "2021-07-26"

keywords: trusted profile, federated users, compute resources, granting access, remove trusted profile

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

# Removing trusted profiles
{: #trusted-profile-remove}

When you remove trusted profiles, compute resources and federated users are unlinked from the profile and can no longer apply the trusted profile identity.
{: shortdesc}

To remove trusted profiles, you must be assigned the administrator or operator role within the account.

When you remove trusted profiles, you revoke all active sessions. Users are immediately logged out and the removed profiles are no longer available to connect to the target account.
{: note}

## Removing trusted profiles in the console
{: #remove-tp-console}

1. To see the full list of trusted profiles in your account, go to **Manage** > **Access (IAM)** in the {{site.data.keyword.cloud_notm}} console, and select **Trusted profiles**.
2. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg) next to the trusted profile you want to remove, and select **Remove**.
