---

copyright:
  years: 2021, 2022
lastupdated: "2022-02-18"

keywords: enterprise, organize accounts, account group, change contact, account group contact

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Updating the account group contact
{: #update-account-group-contact}

You can update the contact for any account group within your enterprise. The contact is different from an account owner in that they don't have any additional access within the account group or its accounts. The user that you select as a contact acts as a focal point for any account group issues. For example, if a financial officer notices that the account group's usage costs are unexpectedly high, they might notify the account group contact.
{: shortdesc}

To update an account group contact, you need the Administrator or Editor role on the Enterprise service in the enterprise account. For more information, see [Assigning access for enterprise management](/docs/secure-enterprise?topic=secure-enterprise-assign-access-enterprise).

## Updating the account group contact in the console
{: #update-account-group-contact-ui}
{: ui}

To update the contact for an account group, complete the following steps. If a user that you want to assign as the contact isn't in the enterprise, first invite the user to the enterprise account. See [Inviting users](/docs/account?topic=account-iamuserinv) for more information.

1. In the {{site.data.keyword.cloud}} console, click **Manage** > **Enterprise** > **Accounts**.
1. In the **Account groups** section, click the **Actions** icon ![Actions icon](../icons/actions-icon-vertical.svg "Actions") in the row for the account group, and select **Edit**.
1. Select the new contact for the account group, and click **Save**.

## Updating the account group contact using the CLI
{: #update-account-group-contact-cli}
{: cli}

This action can be done only through the UI, API, or SDKs. To see the steps, switch to the UI or API instructions.


## Updating the account group contact using the API
{: #update-account-group-contact-api}
{: api}

To update the primary contact for the account group, call the [Enterprise Management API](/apidocs/enterprise-apis/enterprise#update-account-group){: external} as shown in the following sample request. Replace the IAM token and ID variables with the values from your enterprise.

1. If a user that you want to assign as the contact isn't in the enterprise, first invite the user to the enterprise account. See [Inviting users](/docs/account?topic=account-iamuserinv) for more information.

1. Update the primary contact by passing the IAM ID of the user you want to be the new primary contact for the enterprise.

   ```bash
    curl -X PATCH \
    "https://enterprise.cloud.ibm.com/v1/account-groups/$ACCOUNT_GROUP_ID" \
    -H "Authorization: Bearer <IAM_Token>" \
    -H 'Content-Type: application/json' \
    -d '{
    "primary_contact_iam_id": "enterpriseAccountIamId"
     }'
   ```
{: codeblock}
{: curl}

```java
UpdateAccountGroupOptions updateAccountGroupOptions = new UpdateAccountGroupOptions.Builder()
    .accountGroupId(accountGroupId)
    .name("Updated Example Account Group")
    .primaryContactIamId(enterpriseAccountIamId)
    .build();

Response<Void> response = service.updateAccountGroup(updateAccountGroupOptions).execute();
```
{: codeblock}
{: java}

```javascript
const params = {
  accountGroupId: accountGroupId,
  name: 'Updated Example Account Group',
  primaryContactIamId: enterpriseAccountIamId,
};

enterpriseManagementService.updateAccountGroup(params)
  .then(res => {
    done();
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
response = enterprise_management_service.update_account_group(
  account_group_id=account_group_id,
  name='Updated Example Account Group',
  primary_contact_iam_id=enterprise_account_iam_id,
)
```
{: codeblock}
{: python}

```go
updateAccountGroupOptions := enterpriseManagementService.NewUpdateAccountGroupOptions(
  accountGroupID,
)
updateAccountGroupOptions.SetName("Updated Example Account Group")
updateAccountGroupOptions.SetPrimaryContactIamID(enterpriseAccountIamID)

response, err := enterpriseManagementService.UpdateAccountGroup(updateAccountGroupOptions)
if err != nil {
  panic(err)
}
```
{: codeblock}
{: go}
