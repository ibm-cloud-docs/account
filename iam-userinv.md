---

copyright:

  years: 2015, 2023

lastupdated: "2023-01-20"

keywords: invite, invite users, invitation access, vpn-only user

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# Inviting users to an account
{: #iamuserinv}

Use {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) to invite users, cancel invitations, or resend a pending invitation. You can invite a single user or multiple users.
{: shortdesc}

All users must accept an invitation to become an active user within a new account. [Learn more.](#pending-invitations)
{: important}

## Watch and learn
{: #watch-iam-invite}
{: ui}

![IBM Cloud console guide: Inviting users to the account](https://www.kaltura.com/p/1773841/sp/177384100/embedIframeJs/uiconf_id/27941801/partner_id/1773841?iframeembed=true&entry_id=1_ea3b5fz1){: video output="iframe" data-script="#invite-transcript" id="mediacenterplayer" frameborder="0" width="560" height="315" allowfullscreen webkitallowfullscreen mozAllowFullScreen}

### Video transcript
{: #invite-transcript}
{: notoc}
{: ui}

Welcome back to another installment of the IBM Cloud Console Guide. In this video, we’ll be talking about how to invite users to your IBM Cloud account.

Inviting users to your IBM Cloud account is simple. Click on “Manage”, and then click “Access (IAM).” Then, click on the “Users” tab on the left menu, and click on the blue “Invite Users” button.

Once you are on the “Invite Users” page, you can invite users to your account by typing in their email address in the text box (Cursor moves to Enter email addresses text box).

On this page, you can also add users to access groups. In the “Add users to access groups” section, you will see the access groups that you have created. To add a user to one or more access groups, click the “Add” button to the right of the appropriate access group.

If you need to assign access to classic infrastructure permissions or Cloud Foundry resources, you can do this in the “Assign users additional access section”, which is found just below the access group section. Click on the additional access you would like to assign (clicks Classic infrastructure tile, selects Super user radio button), and then click on the blue “Add” button (then, clicks "Invite" button).

You can manage existing users and their access from the users menu. Click on “Users” in the Access (IAM) left menu. From here, you can see all of the users in your account.

To manage access for existing users, simply click on the user’s name and you will have access to their user details, access groups, access policies, classic infrastructure, and Cloud Foundry access. From here, you can make changes to access permissions as needed (Clicks "Assign access" button from the Access policies tab to show how additional IAM access can be assigned for the selected user).

## Before you begin
{: #invite-access}

To invite users and manage outstanding invitations, you must have at least one of the following types of access. Only users can invite others. If you use a service ID to authenticate, you can't invite new users to the account.

* Account owner
* Cloud Foundry organization manager
* An IAM access policy with the Editor role or higher on the user management account management service
* The Manage Users classic infrastructure permission to add users

Depending on your access level, you can invite new users and assign all or just some types of access. For example, if you're not the account owner, but you're a Cloud Foundry organization manager, you can invite users and assign only Cloud Foundry access.
{: note}

Before you can invite users by using Terraform, make sure that you have completed the following:
{: terraform}

- Install the Terraform CLI and configure the {{site.data.keyword.cloud_notm}} Provider plug-in for Terraform. For more information, see the tutorial for [Getting started with Terraform on {{site.data.keyword.cloud}}](/docs/ibm-cloud-provider-for-terraform?topic=ibm-cloud-provider-for-terraform-getting-started). The plug-in abstracts the {{site.data.keyword.cloud_notm}} APIs that are used to complete this task.
- Create a Terraform configuration file that is named `main.tf`. In this file, you add arguments by using HashiCorp Configuration Language. For more information, see the [Terraform documentation](https://www.terraform.io/docs/language/index.html){: external}.
{: terraform}


## Inviting users in the console
{: #invitations}
{: help}
{: support}
{: ui}

To invite users, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Users**.
1. Click **Invite users**.
1. Specify the email addresses of the users. If you are inviting more than one user with a single invitation, they are all assigned the same access.

   You can restrict membership to your account based on the domain of the users that are invited. This way, only users from a specific domain can be invited to the account. For more information, see [Restrict user domains for account invitations](/docs/account?topic=account-restrict-acct-invite).
   {: note}

1. Add one or more of the access options that you manage. You must assign at least one access option. For any access options that you don't add and configure, the default value of **No access** is assigned. Depending on the options that you are authorized to manage, you can assign the following types of access:

   * Add users to access groups. Click **Add** for each access group that you want the users to belong to.
   * Assign users individual IAM access policies, Cloud Foundry roles, or classic infrastructure permissions.
      * Select **Cloud Foundry**, choose an organization, then select a region to select a specific space, and assign a space role. An organization and space role are both required to add the access assignment to the invite.
      * Select **Classic infrastructure**, and then choose from the three permission sets.
      * Select a group of services like **All Identity and Access enabled services**, **All Account management services**, and **All IAM Account Management services**, or a specific service. Next, you can scope the access to the entire account or just one resource group. Then, select all roles that apply. To view what actions are mapped to each role, click the numbers listed next to each role.

         Some services support the use of advanced operators to grant access to resources that satisfy specific naming conventions. See [Assigning access by using wildcard policies](/docs/account?topic=account-wildcard) for more information.

      * Select **Account management**, and then choose from the all account management services option or select a specific service. Then, select all roles that apply.
1. Select **Add** to save the access assignment to the invitation.
1. After you add all the necessary access assignments, click **Invite**.

You can cancel an invitation for any users that are shown in a Processing or Pending state in the Status column of the [Users page](/iam/users). If an invited user did not receive an invitation, you can resend the invitation to any user in a Pending state. You can add more policies and permissions only after a user accepts the invitation.
{: note}

## Adding VPN-only users
{: #add-vpn-only}
{: ui}

Any user with the following permissions can add a VPN-only user:

- For Cloud Foundry, you must have the Manager organization role.
- For classic infrastructure, you must have the Manage Users permission on the account.
- For IAM access, you must have the Administrator or Editor role on the user management account management service.

To add a VPN-only user, use the following steps:

1. On the Users page, click **Add VPN-only user**.
1. Enter the personal information details for the user.
1. Click **Save**.

## Inviting users by using the CLI
{: #cli-invite}
{: cli}

To invite users by using the CLI, run the following command:

```sh
ibmcloud account user-invite USER_EMAIL [-o ORG [--org-role ORG_ROLE] [-s SPACE, --space-role SPACE_ROLE]]
```
{: codeblock}

By using the CLI, you can choose to assign Cloud Foundry access or no access and work on assigning access later. For more information about the command parameters, see [**`ibmcloud account user-invite`**](/docs/cli?topic=cli-ibmcloud_commands_account#ibmcloud_account_user_invite).

## Inviting users by using the API
{: #api-invite}
{: api}

You can use the [API](https://cloud.ibm.com/apidocs/user-management#invite-users){: external} to invite users in bulk. All users that are included in a single invitation are assigned the same access. When you invite users by using the API, you enter emails in a comma-separated list with each entry that is surrounded by quotations. This example assigns access by adding the user to an access group.

``` bash
curl -X POST https://user-management.cloud.ibm.com/v2/accounts/987d4cfd77b04e9b9e1a6asdcc861234/users -H 'Authorization: Bearer <IAM_TOKEN>'
  -H 'Content-Type: application/json' -d '{
      "users": [
      {
        "email": "cloud_api_example_member@ibm.com",
        "account_role": "Member"
      }],
      "iam_policy": [{
        "type": "access",
        "roles": [{
          "role_id": "crn:v1:bluemix:public:iam::::role:Viewer"
        }],
        "resources": [{
          "attributes": [{
              "name": "accountId",
              "value": "987d4cfd77b04e9b9e1a6asdcc861234"
            },
            {
              "name": "resourceType",
              "value": "resource-group"
            },
            {
              "name": "resource",
              "value": "2c7449dd871049c29ec3a53853ce123e"
            }
          ]
        }]
      }],
      "access_groups":[
        "AccessGroupId-******-0f54-4d4f-89c2-e5fdc0b9a28c",
        "AccessGroupId-******-3087-4395-a382-a8e8ff9ccc23"
      ]
    }'
```
{: codeblock}
{: curl}

```java
InviteUser inviteUserModel = new InviteUser.Builder()
        .email(memberEmail)
        .accountRole("Member")
        .build();

Role roleModel = new Role.Builder()
        .roleId(viewerRoleId)
        .build();

Attribute attributeModel = new Attribute.Builder()
        .name("accountId")
        .value(accountId)
        .build();

Attribute attributeModel2 = new Attribute.Builder()
        .name("resourceGroupId")
        .value("*")
        .build();

Resource resourceModel = new Resource.Builder()
        .addAttributes(attributeModel)
        .addAttributes(attributeModel2)
        .build();

InviteUserIamPolicy inviteUserIamPolicyModel = new InviteUserIamPolicy.Builder()
        .type("access")
        .addRoles(roleModel)
        .addResources(resourceModel)
        .build();

InviteUsersOptions inviteUsersOptions = new InviteUsersOptions.Builder()
        .accountId(accountId)
        .addUsers(inviteUserModel)
        .addIamPolicy(inviteUserIamPolicyModel)
        .addAccessGroups(accessGroupId)
        .build();

Response<InvitedUserList> response = adminService.inviteUsers(inviteUsersOptions).execute();
InvitedUserList invitedUserList = response.getResult();

System.out.println(invitedUserList);
```
{: codeblock}
{: java}

```javascript
const inviteUserModel = {
  email: memberEmail,
  account_role: 'Member',
};

const roleModel = {
  role_id: viewerRoleId,
};

const attributeModel = {
  name: 'accountId',
  value: accountId,
};

const attributeModel2 = {
  name: 'resourceGroupId',
  value: '*',
};

const resourceModel = {
  attributes: [attributeModel, attributeModel2],
};

const inviteUserIamPolicyModel = {
  type: 'access',
  roles: [roleModel],
  resources: [resourceModel],
};

const params = {
  accountId: accountId,
  users: [inviteUserModel],
  iamPolicy: [inviteUserIamPolicyModel],
  accessGroups: [accessGroupId],
};

userManagementAdminService.inviteUsers(params)
  .then(res => {
    deleteUserId = res.result.resources[0].id;
    console.log(JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```python
invite_user_model = {
  'email': member_email,
  'account_role': 'Member'
}

role_model = {'role_id': viewer_role_id}

attribute_model = {'name': 'accountId', 'value': account_id}

attribute_model2 = {'name': 'resourceGroupId', 'value': '*'}

resource_model = {'attributes': [attribute_model, attribute_model2]}

invite_user_iam_policy_model = {
  'type': 'access',
  'roles': [role_model],
  'resources': [resource_model]
}

invite_user_response = user_management_admin_service.invite_users(
  account_id=account_id,
  users=[invite_user_model],
  iam_policy=[invite_user_iam_policy_model],
  access_groups=[access_group_id]
).get_result()

print(json.dumps(invite_user_response, indent=2))
```
{: codeblock}
{: python}

```go
inviteUserModel := &usermanagementv1.InviteUser{
  Email:       &memberEmail,
  AccountRole: core.StringPtr("Member"),
}

roleModel := &usermanagementv1.Role{
  RoleID: &viewerRoleID,
}

attributeModel := &usermanagementv1.Attribute{
  Name:  core.StringPtr("accountId"),
  Value: &accountID,
}

attributeModel2 := &usermanagementv1.Attribute{
  Name:  core.StringPtr("resourceGroupId"),
  Value: core.StringPtr("*"),
}

resourceModel := &usermanagementv1.Resource{
  Attributes: []usermanagementv1.Attribute{*attributeModel, *attributeModel2},
}

inviteUserIamPolicyModel := &usermanagementv1.InviteUserIamPolicy{
  Type:      core.StringPtr("access"),
  Roles:     []usermanagementv1.Role{*roleModel},
  Resources: []usermanagementv1.Resource{*resourceModel},
}

inviteUsersOptions := &usermanagementv1.InviteUsersOptions{
  AccountID:    &accountID,
  Users:        []usermanagementv1.InviteUser{*inviteUserModel},
  IamPolicy:    []usermanagementv1.InviteUserIamPolicy{*inviteUserIamPolicyModel},
  AccessGroups: []string{accessGroupID},
}

invitedUserList, response, err := userManagementAdminService.InviteUsers(inviteUsersOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(invitedUserList, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

You can assign access to a group of services. To assign access to **All Identity and Access enabled services**, specify `serviceType` for the `name` attribute, and use the `value` `service`. To assign access to **All Account Management services**, specify `serviceType` for the `name` attribute, and use the `value` `platform_service`. To assign access to the subset of account management services **All IAM Account Management services**, specify `service_group_id` for the `name` attribute, and use the `value` `IAM`.
{: tip}

## Inviting users by using Terraform
{: #terraform-invite}
{: terraform}

You can invite users to your {{site.data.keyword.cloud_notm}} account by using Terraform.

1. Create an argument in your `main.tf` file. The following example invites users by using the `ibm_iam_user_invite` resource, where `users` are the list of user email IDs to invite.

   ```terraform
   resource "ibm_iam_user_invite" "invite_user" {
    users = ["test@in.ibm.com"]
   }
   ```
   {: codeblock}

   For more information, see the argument reference details on the [Terraform Identity and Access Management (IAM)](https://registry.terraform.io/providers/IBM-Cloud/ibm/latest/docs/resources/iam_user_invite){: external} page.

1. Provision the resources from the `main.tf` file. For more information, see [Provisioning Infrastructure with Terraform](https://www.terraform.io/cli/run){: external}.

   1. Run `terraform plan` to generate a Terraform execution plan to preview the proposed actions.

      ```terraform
      terraform plan
      ```
      {: pre}

   1. Run `terraform apply` to create the resources that are defined in the plan.

      ```terraform
      terraform apply
      ```
      {: pre}


## Canceling or resending pending invitations
{: #pending-invitations}
{: ui}

After inviting new users to join your account, {{site.data.keyword.cloud_notm}} requires all except VPN-only users to accept the invitation to become an active user in your account.

The invitation expires after 30 days. New users to {{site.data.keyword.cloud_notm}} can accept an invitation only by using the invitation link that they received through email.
{: note}

You can cancel an invitation for any users that are shown in a Processing or Pending state in the Status column of the [Users page](/iam/users). If an invited user did not receive an invitation, you can resend the invitation to any user in a Pending state.

1. Go to the [Users page](/iam/users).
1. Locate the row for the user in `Processing` or `Pending` state.
1. Click the **Actions** icon ![More Actions icon](../icons/action-menu-icon.svg "Actions"), then choose to **Resend invite** or **Cancel invite**.

## Accepting invitations in the console
{: #accepting-invitations-ui}
{: ui}

If the invited user is already a member of {{site.data.keyword.cloud_notm}}, they receive an invitation link in their notifications and by email. On the [Notifications page](https://cloud.ibm.com/user/notifications){: external}, users can use the search field to locate an invitation or filter by the notification type called `account`. For more information, see [Managing invitation notifications](/docs/account?topic=account-email-prefs#managing-invitation-notifications) and [Viewing notifications](/docs/get-support?topic=get-support-viewing-notifications).

## Accepting invitations by using the CLI
{: #cli-accepting}
{: cli}

If the invited user is already a member of {{site.data.keyword.cloud_notm}}, they can accept invitations by using the CLI. In the following [**`ibmcloud login`**](/docs/cli?topic=cli-ibmcloud_cli#ibmcloud_login) command, the `ACCOUNT_ID` is the ID of the targeted account that the user is invited to join.

```sh
ibmcloud login -c ACCOUNT_ID --accept
```
{: codeblock}

## Accepting invitations by using the API
{: #api-accepting}
{: api}

If the invited user is already a member of {{site.data.keyword.cloud_notm}}, they can accept invitations by using the API. In the following example, the `ACCOUNT_ID` is the ID of the targeted account that the user is invited to join and the `IAM_TOKEN` belongs to the invitee.

```curl
curl -X POST \
  'https://iam.cloud.ibm.com/v2/users/accept' \
  --header 'Authorization: Bearer <IAM_TOKEN>' \
  --header 'Content-Type: application/json' \
  --data-raw '{
    "account_id": "<ACCOUNT ID>"
  }
```
{: codeblock}
