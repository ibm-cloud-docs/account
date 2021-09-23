---

copyright:
  years: 2019, 2021
lastupdated: "2021-09-22"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, multiple account, video

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:pre: .pre}
{:important: .important}
{:tip: .tip}
{:note: .note}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:ruby: .ph data-hd-programlang='ruby'}
{:api: .ph data-hd-interface='api'}
{:cli: .ph data-hd-interface='cli'}
{:ui: .ph data-hd-interface='ui'}
{:terraform: .ph data-hd-interface='terraform'}


# Creating an enterprise
{: #create-enterprise}

You create an {{site.data.keyword.Bluemix}} enterprise from an existing Subscription account. When an existing subscription account is used, an enterprise and an enterprise account are created. The account that you use to create the enterprise and the new enterprise account are permanently added to the enterprise, but this account does not become the parent account.
{: shortdesc}

## Before you begin
{: #create-prereqs}

To create an [{{site.data.keyword.Bluemix_notm}} enterprise](/docs/account?topic=account-what-is-enterprise), you must be the account owner or have the Administrator role on the Billing account management service in a Subscription account.

The Subscription account that you use to create the enterprise is permanently moved into the enterprise. Moving the account into the enterprise has the following impacts:
* Billing for the account transitions to being [managed by the enterprise](/docs/billing-usage?topic=billing-usage-enterprise). After the transition, users in the account can't access billing and payment information, such as invoices, payments, or subscriptions, for future billing periods. To view or manage billing, users need to be invited to the enterprise account and be given access to the Billing service in that account.
* Users and access permissions within the account are not changed. Access within the account is separate from the enterprise, and users don't automatically get access within the enterprise when the account is added. However, billing information is no longer available within the account regardless of access permissions.
* Resources within the account are not changed. Users with the correct access permissions can continue to view usage information for resources in the account.

If you don't have a Subscription account, you can upgrade your account as described in [Upgrading your account](/docs/account?topic=account-upgrading-account).

## Creating an enterprise in the console
{: #create-console}
{: ui}

1. In the {{site.data.keyword.Bluemix_notm}} console, go to **Manage > Enterprise**, and click **Create**.
1. Enter a unique name to identify your enterprise. Typically, the name reflects your company or organization, such as `My organization's enterprise`. You can edit the enterprise name later if needed.
1. If your company or organization has an associated domain name, enter it in the **Domain** field. You can specify any domain or subdomain format, such as `example.com` or `my.example.com`.
1. Review the information about the impact to your account, and select **I understand the impact to my account**. Then, click **Create**.

   After the account is added to the enterprise, it can't be removed. Be sure you want to permanently move the account to an enterprise.
   {: important}

After a few moments, your enterprise is created, and you can view the enterprise dashboard. Your IBMid is listed as the contact. The contact serves as a focal point for any enterprise concerns, such as billing or usage questions. You're also assigned as the enterprise account owner, so you can invite additional users to manage the enterprise.

Click **Accounts** to view your enterprise hierarchy, which contains two accounts.

* The enterprise account, which is where you invite users and grant access to manage the enterprise.
* The account that you used to create the enterprise. Its users and resources remain the same, but billing is now managed by the enterprise.

## Creating an enterprise by using the CLI
{: #create-cli}
{: cli}

1. Log in, and select the account.

   ```
   ibmcloud login
   ```
   {: codeblock}

1. Create the enterprise by running the [`ibmcloud enterprise create`](/docs/account?topic=cli-ibmcloud_enterprise#ibmcloud_enterprise_create) command, where `NAME` is a unique name to identify the enterprise.

   ```
   ibmcloud enterprise create NAME [-d, --domain DOMAIN_NAME] [--primary-contact-id PRIMARY_CONTACT_USER_ID]
   ```
   {: codeblock}

   For example, the following command creates an enterprise that is named `Example Corp Enterprise` with the `examplecorp.com` domain.

   ```
   ibmcloud enterprise create "Example Corp Enterprise" -d examplecorp.com
   ```
   {: codeblock}

   By default, the enterprise is created with the currently logged-in user in the following roles:
      * The contact for the enterprise, which identifies a focal person to notify with enterprise-related concerns
      * The owner of the enterprise account, which has full access to manage the enterprise account

   You can specify the IBMid for a different user on the `--primary-contact-id` option. The same user is assigned to both roles.
1. Review the impact to your account, and confirm that you want to continue by entering `y`.

   ```
   Account abcde12345fghij67890 will be incorporated into enterprise My new enterprise
   (which cannot be undone). Do you want to proceed? [y/N]> y
   ```

After the enterprise is created, two new IDs are displayed. The first ID is associated with the enterprise, and the second ID identifies the enterprise account, which you use to manage the enterprise.

```
ID:                      09876jihgf54321edcba   
Enterprise Account ID:   edcba12345jihgf67890
```

The account that you used to create the enterprise is now a part of the enterprise. Run the [`ibmcloud enterprise accounts`](/docs/account?topic=cli-ibmcloud_enterprise#ibmcloud_enterprise_accounts) command to view the two accounts in your enterprise: the enterprise account, and the account you used to create the enterprise.

## Creating an enterprise by using the API
{: #create-api}
{: api}

You can programmatically create an enterprise by calling the Enterprise Management API as shown in the following sample request. For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise){: external}.

```bash
curl -X POST "https://enterprise.cloud.ibm.com/v1/enterprises 
-H "Authorization: Bearer <IAM_Token>" 
-H 'Content-Type: application/json' 
-d '{
  "source_account_id": "a1b2c32a5ea94809a9840f5e23c362d",
  "name": "Example Enterprise",
  "domain": "example.com",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: pre}
{: curl}


```java
CreateEnterpriseOptions createEnterpriseOptions = new CreateEnterpriseOptions.Builder()
    .sourceAccountId(srcAccountId)
    .name("Example Enterprise")
    .primaryContactIamId(contactIamId)
    .build();

Response<CreateEnterpriseResponse> response = service.createEnterprise(createEnterpriseOptions).execute();
CreateEnterpriseResponse createEnterpriseResponse = response.getResult();

System.out.println(createEnterpriseResponse);
```
{: codeblock}
{: java}


```javascript
const params = {
  sourceAccountId: srcAccountId,
  name: 'Example Enterprise',
  primaryContactIamId: contactIamId,
};

enterpriseManagementService.createEnterprise(params)
  .then(res => {
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}


```python
create_enterprise_response = enterprise_management_service.create_enterprise(
  source_account_id=src_account_id,
  name='Example Enterprise',
  primary_contact_iam_id=contact_iam_id,
).get_result()

print(json.dumps(create_enterprise_response, indent=2))
```
{: codeblock}
{: python}


```go
createEnterpriseOptions := enterpriseManagementService.NewCreateEnterpriseOptions(
  srcAccountID,
  "Example Enterprise",
  contactIamID,
)

createEnterpriseResponse, response, err := enterpriseManagementService.CreateEnterprise(createEnterpriseOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(createEnterpriseResponse, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}


## Creating an enterprise by using Terraform
{: #create-terraform}
{: terraform}

You can create an enterprise by using Terraform. 

1. To install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform, follow the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.

2. Create a Terraform configuration file that is named `main.tf`. In this file, you add the configuration to create an enterprise by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.

   The following example creates an enterprise by using the `ibm_enterprise` resource, where `name` is a unique name to identify the enterprise. You must have an existing IAM ID of an enterprise primary contact in order to complete the task. 

   ```terraform
   resource "ibm_enterprise" "enterprise" {
    source_account_id = <source_account_id>
    name = <name>
    primary_contact_iam_id = <primary_contact_iam_id>
   }
   ```
   {: codeblock}

   You can specify the ID of an account that is used to create the enterprise on the `source_account_id` option. For more information, see the argument reference details on the [Terraform Enterprise Management](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/enterprise){: external} page.
  
3. Initialize the Terraform CLI.

   ```
   terraform init
   ```
   {: pre}
   
4. Create a Terraform execution plan. The Terraform execution plan summarizes all the actions that need to be run to create the enterprise.

   ```
   terraform plan
   ```
   {: pre}

5. Create the enterprise.

   ```
   terraform apply
   ```
   {: pre}

## Next steps
{: #create-next-steps}

Build out your enterprise structure by adding more existing accounts or creating new accounts within your enterprise. For more information, see [Adding accounts to your enterprise](/docs/account?topic=account-enterprise-add).

You can also invite additional users to the enterprise account so that they can help manage the enterprise. For example, you might want to invite a financial officer to manage billing and track usage costs, and invite department leads to administer accounts. See [Inviting users](/docs/account?topic=account-iamuserinv) for more information about how to invite users.
