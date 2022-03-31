---

copyright:

  years: 2018, 2022

lastupdated: "2022-03-31"

keywords: specific IP addresses, IP addresses, restrict IP access, IP address access, allow IP access

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Allowing specific IP addresses 
{: #ips}

By default, all IP addresses can be used to log in to the {{site.data.keyword.cloud}} console and access classic infrastructure APIs. You can specify which IP addresses have access and all other IP addresses are restricted. You can specify this access at the user level or at the account level. Currently, only public IP addresses are supported. 
{: shortdesc}

If an IP address restriction is defined for both the account and the user, the IP address needs to match both specifications to be able to generate an IAM token.
{: important}

## Allowing specific IP addresses for a user
{: #ips_user}
{: ui}

If you have the following assigned access, you can update the restricted IP addresses for another user:

* An IAM policy with the Editor or higher role on the User management service.
* You are an ancestor in the classic infrastructure hierarchy for the user and you have the Manage users classic infrastructure permission assigned

If you have the User-managed login setting that is enabled on your User details page, you can manage this setting for yourself.
{: tip}

To restrict a user to using only specific IP addresses, complete the following steps:
1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Users**.
2. Select a user from the list.
3. From the User details page, go to the **IP address restrictions** section.
4. For **Cloud platform**, enter the IP addresses. The IP addresses listed are the only ones from which this user can log in to {{site.data.keyword.Bluemix}}.
5. For **Classic infrastructure**, enter the IP addresses. The IP addresses listed are the only ones from which the user can call a classic infrastructure API.

      You can enter a single IP address `17.5.7.8`, an IP address range `17.5.7.8 - 17.5.9.5`, or IP subnets `17.5.7.8.0/16`, or a [network zone](/docs/account?topic=account-context-restrictions-whatis#network-zones-whatis) `networkZoneName`. Make sure to use IPv4 or IPv6 addresses, and to separate multiple values with a comma. If there is already an IP address restriction that exists, the resource overrides the restriction.
      {: note}

6. Click **Save**. 

To enter a classic infrastructure IP address, the user must have already created a classic infrastructure API key.
{: note}


## Allowing specific IP addresses for an account 
{: #ips_account}
{: ui}

If you have the following assigned access, you can update the restricted IP addresses for an account:

* An IAM policy with the Editor, Operator, or Administrator role on the IAM identity service.

To restrict all users to using only specific IP addresses, complete the following steps:
1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** &gt; **Access (IAM)**, and select **Settings**.
1. From the Account restrictions section, turn on the **IP address access** setting. 
1. Enter the IP addresses. The IP addresses listed are the only ones from which users in the account can log in to {{site.data.keyword.Bluemix}}.
   You can enter a single IP address `17.5.7.8`, an IP address range `17.5.7.8 - 17.5.9.5`, or IP subnets `17.5.7.8.0/16`, or a [network zone](/docs/account?topic=account-context-restrictions-whatis#network-zones-whatis) `networkZoneName`. Make sure to use IPv4 or IPv6 addresses, and to separate multiple values with a comma. If there is already an IP address restriction that exists, the resource overrides the restriction.
   {: note}

1. Click **Save**. 

## Allowing specific IP addresses for an account by using Terraform
{: #ips_account_terraform}
{: terraform}

If you have the following assigned access, you can update the restricted IP addresses for an account:

* An IAM policy with the Editor, Operator, or Administrator role on the IAM identity service.

To restrict all users to using only specific IP addresses, complete the following steps:

1. In your Terraform configuration file, find the Terraform code that you used to create the `iam_account_settings_instance`.
2. Enter the IP addresses that you want to restrict all users to using. The IP addresses listed are the only ones from which users in the account can log in to {{site.data.keyword.Bluemix}}.
   ```terraform
    resource "ibm_iam_account_settings" "iam_account_settings_instance" {
      allowed_ip_addresses = "17.5.7.8, 17.5.7.8 - 17.5.9.5, 17.5.7.8.0/16"
   }
   ```
   {: pre}

3. Create a Terraform execution plan.
   ```bash
   terraform plan
   ```
   {: pre}

4. Update the allowed IP addressees in the account. Note that this process might take a few minutes to complete.
   ```bash
   terraform apply
   ```
   {: pre}

For more information, see the [Terraform documentation](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_account_settings#allowed_ip_addresses). 

You can enter a single IP address `17.5.7.8`, an IP address range `17.5.7.8 - 17.5.9.5`, or IP subnets `17.5.7.8.0/16`, or a [network zone](/docs/account?topic=account-context-restrictions-whatis#network-zones-whatis) `networkZoneName`. Make sure to use IPv4 or IPv6 addresses, and to separate multiple values with a comma. If there is already an IP address restriction that exists, the resource overrides the restriction. 
{: note}

