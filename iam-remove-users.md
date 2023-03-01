---

copyright:

  years: 2018, 2023

lastupdated: "2023-02-21"

keywords: remove user, delete user

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Removing users from an account
{: #remove}

When you remove a user from an account, the user can no longer log in to the console, switch to your account, or access account resources. Removing a user from an account doesn't delete the IBMid for the user.
{: shortdesc}

Only account owners and users with the correct access can remove others. If you use a service ID to authenticate, you can't remove users from the account. The following access is required for removing users from an account:

* An Identity and access management (IAM) policy for the User management account management service with the Administrator role assigned and be the Cloud Foundry org manager if the user belongs to a Cloud Foundry org.
* If you have classic infrastructure in your account, a user must have an IAM policy for the User management account management service with the Administrator role assigned, be the Cloud Foundry org manager if the user belongs to a Cloud Foundry org, and be an ancestor of the user in the classic infrastructure user hierarchy with the Manage user classic infrastructure permission assigned.

As an alternative to removing a user from your account, you can assign them an access policy with a temporary time-based condition. This way, the user can log in to the console and view the account in their account list, but can't access resources in the account before the policy begins or after the policy expires. For more information, see [Creating a temporary time-based condition](/docs/account?topic=account-iam-time-based&interface=api#iam-time-based-temp-api).

## Removing a user from an account in the console
{: #remove-user-acount-ui}
{: ui}

To remove a user from an account, complete the following steps:

1. In the {{site.data.keyword.cloud}} console, click **Manage** > **Access (IAM)**, and select **Users**.
2. From the row of the user that you want to remove, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Remove user**.

Any resources that are created by the user remain in the account, but any {{site.data.keyword.cloud_notm}} API keys that the user created are removed. The user no longer has access to work with the resources they created. The account owner or an administrator for the service or service instance can assign other users to work with the resources, or delete them from the account.

If you get an error message that states a classic infrastructure user can't be removed, make sure that any descendants in the user hierarchy for that user are [assigned a new parent](/docs/account?topic=account-iam-user-setting#update-parent), [disabled in the account](/docs/account?topic=account-status), or deleted. Then, you can try again.
{: tip}


## Removing a user from an account by using the CLI
{: #remove-user-acount-cli}
{: cli}

To remove a user from an account, run the following command:

```bash
ibmcloud account user-remove USER_ID [-c ACCOUNT_ID] [-f, --force]
```
{: codeblock}

For command options, see [Managing accounts, users, and Cloud Foundry orgs](https://cloud.ibm.com/docs/cli?topic=cli-ibmcloud_commands_account#ibmcloud_account_user_remove) CLI commands.

## Removing a user from an account by using the API
{: #remove-user-acount-api}
{: api}

To remove a user from an account, call the [User Management API](https://cloud.ibm.com/apidocs/user-management?code=java#remove-user) as shown in the following sample request. Replace variables with the user's IAM ID. You must use a user token for authorization. Service IDs can't remove users from an account.

```bash
curl -X DELETE https://user-management.cloud.ibm.com/v2/accounts/987d4cfd77b04e9b9e1a6asdcc861234/users/IBMid-1000000000 -H 'Authorization: Bearer <IAM_TOKEN>' -H 'Content-Type: application/json'
```
{: codeblock}
{: curl}

```java
RemoveUserOptions removeUserOptions = new RemoveUserOptions.Builder()
  .accountId(accountId)
  .iamId(deleteUserId)
  .build();

service.removeUser(removeUserOptions).execute();
```
{: codeblock}
{: java}

```javascript
const params = {
  accountId: accountId,
  iamId: deleteUserId,
};

userManagementAdminService.removeUser(params)
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
response = user_management_admin_service.remove_user(
  account_id=account_id,
  iam_id=delete_user_id,
).get_result()

print(json.dumps(response, indent=2))
```
{: codeblock}
{: python}

```go
removeUserOptions := userManagementService.NewRemoveUserOptions(
  accountID,
  deleteUserID,
)

response, err := userManagementAdminService.RemoveUser(removeUserOptions)
if err != nil {
  panic(err)
}
```
{: codeblock}
{: go}
