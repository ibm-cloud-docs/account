---

copyright:

  years: 2020, 2022

lastupdated: "2022-10-26"

keywords: restrict service id, block users from creating service id, restrict service id creation

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Restricting users from creating service IDs
{: #restrict-service-id-create}

By default, all members of an account can create service IDs. However, access can be restricted so that only members with the correct access can create service IDs by using the Service ID creation setting. For more information about Service IDs, see [Creating and working with service IDs](/docs/account?topic=account-serviceids).
{: shortdesc}

## Enabling the restriction to create service IDs in the console
{: #enable-restrict-create-serviceid-ui}

To enable the setting to restrict users from creating service IDs, you must have the following assigned access:

* An IAM policy with the `Administrator`, `Operator`, or `Editor` role on the [IAM Identity Service](/docs/account?topic=account-account-services#identity-service-account-management).

If you enable the Service ID creation setting, users in your account require specific access to create service IDs, including the account owner. To restrict who can create service IDs, use the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Access (IAM)**, and select **Settings**.
1. In the Account section, enable the **Service ID creation** setting.
1. Click **Yes** to confirm.

Now that the setting is enabled to restrict users from creating service IDs, you can assign the required access to enable specific users to continue creating service IDs. Remember, the account owner is also required to be assigned this explicit access.
{: important}

## Assigning access to create service IDs with restrictions enabled in the console
{: #assign-access-create-service-id-restrict}

If the Service ID creation setting is enabled, only users, including the account owner, assigned the `Service ID creator` role on the IAM Identity Service can create service IDs.

The quickest way to assign a group of users the required access for creating service IDs is to create an access group and assign the group the required role. For more information about assigning access policies, see [Setting up access groups](/docs/account?topic=account-groups).
{: tip}
