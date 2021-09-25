---

copyright:

  years: 2018, 2021

lastupdated: "2021-09-24"

keywords: dynamic rules,access groups,specific identity attributes,identity provider,federated ID,

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}
{:terraform: .ph data-hd-interface='terraform'} 
{:ui: .ph data-hd-interface='ui'}

# Creating dynamic rules for access groups
{: #rules}

You can create dynamic rules to automatically add federated users to access groups based on specific identity attributes. When your users log in with a federated ID, the data from the identity provider (IdP) dynamically maps your users to an access group based on the rules that you set.
{: shortdesc}

Users already have specific identity information within your company's domain, and when they log in with a federated ID, this data can be passed through by using SAML assertions. The SAML assertions or attribute statements that are configured within the IdP provide the data that is used to create each rule. For example, you might have a true or false attribute statement that defines users as a manager. This information can be used to add all users who are managers to a specific access group for managers that you created in your {{site.data.keyword.Bluemix}} account. For more information, see the tutorial about how to [Control access to cloud resources](https://developer.ibm.com/tutorials/use-iam-access-groups-to-effectively-manage-access-to-your-cloud-resources/){: external} and an [Example rule](/docs/account?topic=account-rules#example).

Only users who are already invited to the account can be mapped to access groups by using dynamic rules.
{: note}

## Setting up rules by using the console
{: #setup_rules}
{: ui}

Dynamic rules are created by setting conditions that must be matched by the data that is configured within the IdP and passed in with a user's federated ID during login. You can add more than one condition for a rule. All conditions set in the rule must be met for a user to be added to an access group. 

To create a rule, follow these steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Access Groups**.
2. Select the name of the access group that you want to create a rule for to open the group details page.
3. Select **Dynamic rules**.
4. Click **Add rule**.
5. Enter the information from your IdP that is dynamically provided for you on the Add rule page. The following list provides details for each required field.

You can think of an access group rule as a key:value pair. The key is what you add in the **`**Add users when** field, and the value is what you enter in the **Values** field. 
{: tip}

Name
:   Enter a custom name for your rule that helps you remember what type of users that you are adding to an access group.

Identity provider
:   Enter the URI for your IdP. This is the SAML "entityId" field, which is sometimes referred to as the issuer ID, for the IdP as part of the federation configuration for onboarding with IBMid.

Expiration (in hours)
:   Use this option to provide extra security by setting a time limit for the assigned access. Each user must log in every 24 hours to refresh their access, but you can set the access to expire in as little as an hour's time. Group membership is revoked after this time period expires.

Add users when
:   The attribute statement name must be entered in this field. This value is specific to your IdP.

Comparator
:   Use the **Contains** option when the attribute statement has an array type. And, you can enter more than one value to be matched by using the **In** option.

Value
:   Enter the attribute value for the attribute statement that the rule is comparing against.

Users added to access groups by using dynamic rules don't display as group members on the users list for the access group. To check a specific user's membership to an access group, you can select that user's name from the account **Users** page, and then click **Access groups**.
{: note}

## Setting up rules by using Terraform
{: #setup_rules_terraform}
{: terraform}

Dynamic rules are created by setting conditions that must be matched by the data that is configured within the IdP and passed in with a user's federated ID during login. You can add more than one condition for a rule. All conditions set in the rule must be met for a user to be added to an access group. 

To create a rule by using Terraform, follow these steps:

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to create dynamic rules for access groups by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

   The following example creates a new dynamic rule for an access group by using the `ibm_iam_access_group_dynamic_rule` resource, where `name` is a unique name to identify the dynamic rule. 

   ```terraform
    resource "ibm_iam_access_group_dynamic_rule" "rule1" {
      name              = "newrule"
      access_group_id   = "AccessGroupId-dsnd4bvsaf"
      expiration        = 4
      identity_provider = "test-idp.com"
      conditions {
        claim    = "blueGroups"
        operator = "CONTAINS"
        value    = "\"test-bluegroup-saml\""
      }
    }
   ```
   {: codeblock}
   
   For more information, see the argument reference details in the [Terraform documentation](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_access_group_dynamic_rule) page.
3. Initialize the Terraform CLI.

   ```terraform
   terraform init
   ```
   {: pre}
   
4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to create the dynamic rule.

   ```terraform
   terraform plan
   ```
   {: pre}

5. Create the dynamic rule.

   ```terraform
   terraform apply
   ```
   {: pre}

## Example rule
{: #example}

The following example includes values for each of the fields on the **Add rule** page. In this rule, users who are identified as managers within the federated IdP are mapped to an {{site.data.keyword.Bluemix_notm}} access group that has specific access set for only managers.

| Field                           | Value                           |
|---------------------------------|---------------------------------|
| Name                            | Manager group rule              |
| Identity provider               | `https://idp.example.org/SAML2` |
| Expiration (in hours)           | 12                              |
| Add users when (attribute name) | isManager                       |
| Comparator                      | Equals                          |
| Value                           | true                            |
{: caption="Table 1. Example dynamic rule for access groups" caption-side="top"}
