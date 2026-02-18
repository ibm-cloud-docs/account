---

copyright:

  years: 2018, 2026
lastupdated: "2026-02-18"

keywords:

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}



# Activity tracking events for account management
{: #at_events_am}



{{site.data.keyword.cloud_notm}} services, such as account management, generate activity tracking events.
{: shortdesc}

Activity tracking events report on activities that change the state of a service in {{site.data.keyword.cloud_notm}}. You can use the events to investigate abnormal activity and critical actions and to comply with regulatory audit requirements.

You can use {{site.data.keyword.atracker_full_notm}}, a platform service, to route auditing events in your account to destinations of your choice by configuring targets and routes that define where activity tracking events are sent. For more information, see [About {{site.data.keyword.atracker_full_notm}}](/docs/atracker?topic=atracker-about).

You can use {{site.data.keyword.logs_full_notm}} to visualize and alert on events that are generated in your account and routed by {{site.data.keyword.atracker_full_notm}} to an {{site.data.keyword.logs_full_notm}} instance.

## Locations where activity tracking events are sent by {{site.data.keyword.atracker_full_notm}}
{: #atracker-locations-am}



Account management sends activity tracking events by {{site.data.keyword.atracker_full_notm}} in the regions that are indicated in the following table.

| Dallas (`us-south`) | Washington (`us-east`)  | Toronto (`ca-tor`) | Sao Paulo (`br-sao`) |
|---------------------|-------------------------|-------------------|----------------------|
| [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Americas locations" caption-side="top"}
{: #atracker-table-1}
{: tab-title="Americas"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: row-headers}

| Tokyo (`jp-tok`)    | Sydney (`au-syd`) |  Osaka (`jp-osa`) | Chennai (`in-che`) |
|---------------------|------------------|------------------|--------------------|
| [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Asia Pacific locations" caption-side="top"}
{: #atracker-table-2}
{: tab-title="Asia Pacific"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: row-headers}

| Frankfurt (`eu-de`)  | London (`eu-gb`) | Madrid (`eu-es`) |
|---------------------------------------------------------------|---------------------|------------------|
| [Yes]{: tag-green} | [No]{: tag-red} | [No]{: tag-red} |
{: caption="Regions where activity tracking events are sent in Europe locations" caption-side="top"}
{: #atracker-table-3}
{: tab-title="Europe"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: row-headers}

## Launching {{site.data.keyword.logs_full_notm}} from the Observability page
{: #log-launch-standalone-am}



For information on launching the {{site.data.keyword.logs_full_notm}} UI, see [Launching the UI in the {{site.data.keyword.logs_full_notm}} documentation.](/docs/cloud-logs?topic=cloud-logs-instance-launch)


## Events for managing accounts
{: #account_management_events}

The following table lists the actions that generate an event:

| Action                               | Description |
|--------------------------------------|-------------|
| `billing.account.create`             | An event is generated when you create an account after the account ID is assigned to the account. |
| `billing.account.update`             | An event is generated when you update information about the account.  |
| `billing.account.active`             | An event is generated when you verify the account, that is, an event is generated when the account becomes active. |
| `billing.account-subscription.create` | An event is generated when you create a [Subscription account](/docs/account?topic=account-accounts#subscription-account). |
{: caption="Actions that generate account management events" caption-side="top"}

## Events for managing account usage reports
{: #at_events_acc_mgt_account_reporst}

These events are generated when a user looks at usage information in the account. For example, the user can look at usage data through the **Manage > Billing and usage > Usage** section, or request an export of the data. Also, users can request usage information through the CLI or by making direct [API calls](/apidocs/metering-reporting#introduction).

### Events for managing single account usage reports
{: #at_events_acc_mgt_account_reporst_std}

The following table lists the actions that generate an event:

| Action                                               | Description |
|------------------------------------------------------|-------------|
| `billing.account-summary.read`                       | An event is generated when a user views the account level summary usage page that is displayed by default. |
| `billing.account-summary.download`                   | An event is generated when a user requests a **summary** export of the data in csv format from the account level summary usage page. |
| `billing.account-usage-report.read`                  | An event is generated when a user views the usage data that is displayed after the user configures a time frame, a resource group, or both in the default account level summary usage page. This event is also generated when a user views the instances usage data page. |
| `billing.account-instances-usage-report.download`    | An event is generated when a user requests an **instances** export of the data in csv format from the account level summary usage page. |
{: caption="Actions that generate account management events" caption-side="top"}

### Events for managing enterprise usage reports
{: #at_events_acc_mgt_reporst_enterprise}

The following table lists the actions that generate an event:

| Action                                               | Description |
|------------------------------------------------------|-------------|
| `billing.enterprise-usage-report.read`               | An event is generated when a user views the enterprise account level summary usage page that is displayed by default. |
| `billing.enterprise-usage-report.download`          | An event is generated when a user requests a **summary** export of the data in csv format from the enterprise account level summary usage page.  |
| `billing.enterprise-instances-usage-report.download` | An event is generated when a user requests an **instances** export of the data in csv format from the enterprise account level summary usage page. |
{: caption="Actions that generate account management events" caption-side="top"}

## Events for managing IAM account settings
{: #at_events_acc_mgt_acc_iam}

The following table lists the actions that are generated when an account setting that is controlled from the **Manage > Access (IAM) > Settings** dashboard is modified:

| Action                                     | Description |
|--------------------------------------------|-------------|
| `iam-identity.accountsettings.update`      | An event is generated when an initiator modifies 1 or more of the following account settings: `Multifactor authentication (MFA)`, `Restrict API key creation`, `Restrict service ID creation`, and `Restrict IP address access`. |
| `iam-groups.account-settings.update` | An event is generated when an initiator modifies the account setting `Public access group`. |
| `billing.account-traits.update`      | An event is generated when an initiator modifies the account setting `Restrict user list visibility`. |
{: caption="Actions that generate events when the account settings are changed" caption-side="top"}

The following table lists the `requestData` fields that report the configuration changes:

| Action                                                         | Description |
|----------------------------------------------------------------|-------------|
| `requestData.public_access_enabled`                            | Reports the boolean value that is set when the `Public access group` setting is modified. |
| `requestData.request_body.old_mfa_traits`                      | Reports the original value for the `Multifactor authentication (MFA)` setting. Valid values are `NONE`, `TOTP`, `TOTP4ALL`, `LEVEL1`, `LEVEL2`, `LEVEL3`   \n  \n This field is set to `NONE` when MFA is not enabled in the account, and all users log in by using a standard ID and password.   \n  \n This field is set to `TOTP` when the account requires MFA for non-federated users only users with an IBMid. Users are required an ID, password, and a time-based one-time passcode to log in.   \n  \n This field is set to `TOTP4ALL` when the account requires MFA for all users with an IBMid.   \n  \n This field is set to `LEVEL1` to enable MFA for all users (IBMid & supported IdPs) when you choose the method `email-based MFA`. Users must authenticate by using a security passcode that is sent via email.     \n  \n This field is set to `LEVEL2` to enable MFA for all users (IBMid & supported IdPs) when you choose the method `TOTP MFA`. Users authenticate by using a time-based one-time passcode (TOTP) that uses the current time of day as an authentication factor.   \n  \n This field is set to `LEVEL3` to enable MFA for all users (IBMid & supported IdPs) when you choose the method `Security key MFA`. Users authenticate by using a hardware security key that generates a six-digit numerical code. |
| `requestData.request_body.new_mfa_traits`                      | Reports the new value for the `Multifactor authentication (MFA)` setting. |
| `requestData.request_body.old_restrict_create_platform_apikey` | Reports the original value for the `Restrict API key creation` setting.   \n Valid values: `NOT_RESTRICTED` and `RESTRICTED` |
| `requestData.request_body.new_restrict_create_platform_apikey` | Reports the new value for the `Restrict API key creation` setting.   \n Valid values: `NOT_RESTRICTED` and `RESTRICTED` |
| `requestData.request_body.old_restrict_create_service_id`      | Reports the original value for the `Restrict service ID creation` setting.   \n Valid values: `NOT_RESTRICTED` and `RESTRICTED` |
| `requestData.request_body.new_restrict_create_service_id`      | Reports the new value for the `Restrict service ID creation` setting.   \n Valid values: `NOT_RESTRICTED` and `RESTRICTED` |
| `requestData.request_body.old_allowed_ip_addresses`            | Reports the original value for the `Restrict IP address access` setting.   \n Valid values: `NOT_RESTRICTED` and `RESTRICTED` |
| `requestData.request_body.new_allowed_ip_addresses`            | Reports the new value for the `Restrict IP address access` setting.   \n Valid values: `NOT_RESTRICTED` and `RESTRICTED` |
| `requestData.team_directory_enabled`                           | Reports the boolean value that is set when the `Restrict user list visibility` setting is modified. |
{: caption="Actions that generate events when the account settings are changed" caption-side="top"}

The following table lists the `deprecated` actions that generate an event when an account setting that is controlled from the **Manage > Access (IAM) > Settings** dashboard is modified:

| Action                               | Description |
|--------------------------------------|-------------|
| `billing.account-traits.update`      | An event is generated when an account setting is modified. |
| `billing.account-mfa.set-on`         | An event is generated when the `Account Login` setting sets on multifactor authentication in the account. |
| `billing.account-mfa.set-off`        | An event is generated when the `Account Login` setting sets off multifactor authentication in the account. |
{: caption="Actions that generate events when the account settings are changed" caption-side="top"}

## Events for managing organizations
{: #at_events_acc_mgt_org}

The following table lists the actions that generate an event:

| Action                               | Description |
|--------------------------------------|-------------|
| `billing.account-org.create`         | An event is generated when you add an organization to the account. |
{: caption="Actions that generate events" caption-side="top"}

## Events for managing tags
{: #at_events_acc_mgt_resources}

The following table lists the actions that generate an event:

| Action                                          | Description |
|-------------------------------------------------|-------------|
| `global-search-tagging.tag.create`              | An event is generated when you create a tag. The tag type is included in the requestData object. |
| `global-search-tagging.tag.delete`              | An event is generated when you delete a tag in your account.  |
| `global-search-tagging.tags.delete`             | An event is generated when you delete all the tags that are not attached to resources in your account.  |
| `<service-name>.tag.attach`                     | An event is generated when you associate a tag to a resource. |
| `<service-name>.tag.detach`                     | An event is generated when you remove a tag from a resource.  |
{: caption="Actions that generate events" caption-side="top"}

When an access tag is created, you get an event with `global-search-tagging.tag.create`.

When an access tag is attached to a resource you get the event `<service-name>.tag.attach`.

## Events for managing users
{: #at_events_acc_mgt_users}

The following table lists the actions that generate an event:

| Action                               | Description |
|--------------------------------------|-------------|
| `user-management.user.invite`        | An event is generated when you invite a user to the account. |
| `user-management.user.resend-invite` | An event is generated when you resend a invite to a user for the account. |
| `user-management.cloud-user.list`    | An event is generated when you retrieve users from the account. |
| `user-management.user.read`          | An event is generated when you retrieve a user's information from the account. |
| `billing.user.active`                | An event is generated when a user, that has received an email invitation to join an account, verifies the email address. |
| `user-management.user.update`        | An event is generated when log in configurations are modified for a user from the {{site.data.keyword.cloud_notm}} UI. |
| `user-management.user-realm.update`  | An event is generated when you update a user's IBM ID. |
| `user-management.user.delete`        | An event is generated when you remove a user from the account. |
| `user-management.user-setting.read`  | An event is generated when you retrieve the user's login configuration settings: User one-time passcode authentication ,Require MFA security questions at login, User-managed login or Setting up security questions |
| `user-management.user-setting.update` | An event is generated when you update the user's login configuration settings: User one-time passcode authentication ,Require MFA security questions at login, User-managed login or Setting up security questions |
{: caption="Actions that generate events" caption-side="top"}

### Inviting a user to an account
{: #acc_invite_user}

Separate events are generated for this asynchronous activity: one showing a pending invitation and one showing the completion or failure of the invitation.

* A pending invitation event would contain the following values for the action, outcome and message fields.

```json
"action": "user-management.user.invite",
"outcome": "pending",
"message": "IAM User Management: invite user -pending"
```
{: codeblock}

* A completed invitation event would contain the following values for the action, outcome and message fields.

```json
"action": "user-management.user.invite",
"outcome": "success",
"message": "IAM User Management: invite user"
``` 
{: codeblock}

### Deleting a user from an account
{: #acc_delete_user}

Separate events are generated for asynchronous delete users requests: one showing a pending deletion and one showing the completion or failure of the delete.

* A pending delete user event would contain the following values for the action, outcome and message fields.

```json
"action": "user-management.user.delete",
"outcome": "pending",
"message": " IAM User Management: delete user IBMid-Example -pending"
``` 
{: codeblock}

* A completed delete user event would contain the following values for the action, outcome and message fields.

```json
"action": "user-management.user.delete",
"outcome": "success",
"message": " IAM User Management: delete user IBMid-Example"
```
{: codeblock}

## Events for carbon calculator
{: #at_events_carbon_calculator}

The following table lists the actions that generate an event:

| Action                               | Description |
|--------------------------------------|-------------|
| `carbon-calculator.carbon-emissions.list`        | Request to get the carbon emissions for a given account. |
| `carbon-calculator.services.list`        | Request the list the services for which carbon emissions can be fetch. |
| `carbon-calculator.locations.list`        | Request the list of location from where carbon emissions can be fetch. |
{: caption="Actions that generate events" caption-side="top"}

## Analyzing account management activity tracking events
{: #at_events_am_analyze}



### User management events
{: #at_events_analyze_3}

This section explains events that are generated when you manage users from the **Manage > Access (IAM) > Users** dashboard.

When you analyze user management events, `target.name` is set to the user ID of the user on which the action is requested.

#### Modify the status of a user
{: #at_events_analyze_3_1}

When you modify the status of a user by selecting a user, clicking **Edit** in the **Details** section, and changing the **User status**, you get the following event:
* Event with action `user-management.user.update` that reports a request in the account to modify the user's properties.

For example, see the `action` field for the event `user-management.user.update`:

```json
"action": "user-management.user.update",
"message": "User management service: update user"
"initiator": {
    "id": "IBMid-12345",
    "typeURI": "service/security/account/user",
    "name": "example@ibm.com",
    "host": {
      "agent": "",
      "address": "...",
      "addressType": "IPv4"
    },
    "credential": {
      "type": "token"
    }
  },
  "target": {
    "id": "crn:v1:bluemix:public:user-management:global:a/account1234:::",
    "typeURI": "user-management/user",
    "name": "IBMid-12345",
    "host": {
      "address": "user-management.cloud.ibm.com"
    }
}

```
{: screen}

#### Restrict IP addresses
{: #at_events_analyze_3_2}

When you configure IP address restrictions from the **IP address restrictions** section, you get 1 event with action `user-management.user-setting.update`.

For example, see the `requestData` field for the event `user-management.user-setting.update`:

```json
{
    "action": "user-management.user-setting.update",
    "message": "IAM User Management: update user-setting user@company.com",
    "requestData": {
        "totalNumberChanges": 1,
        "update": [
            {
                "ips_added": [
                    {
                        "address": "241.211.116.250",
                        "addressType": "IPv4"
                    },
                    {
                        "address": "89.78.194.127",
                        "addressType": "IPv4"
                    },
                    {
                        "address": "40.190.11.111",
                        "addressType": "IPv4"
                    },
                    {
                        "address": "246.140.117.83",
                        "addressType": "IPv4"
                    },
                ],
                "updateType": "allowed_ip_addresses changes"
            }
        ]
    }
}
```
{: screen}

#### Manage user's login
{: #at_events_analyze_3_3}

When you modify information about a user's login from the **Manage > Access (IAM) > Users > User Details** section, you get 1 event with action `user-management.user-setting.update`.

See the sample of the `requestData` field when the **User-managed login** property is disabled:

```json
{
    "action": "user-management.user-setting.update",
    "message": "IAM User Management: update user-setting user@company.com",
    "requestData": {
        "totalNumberChanges": 1,
        "update": [
            {
                "initialValue": true,
                "newValue": false,
                "updateType": "self_manage update"
            }
        ]
    }
}
```
{: screen}

See the sample of the `requestData` field when the **User one-time passcode authentication** property is enabled. The `requestData.2FA` field is set to `true`.

```json
{
    "action": "user-management.user-setting.update",
    "message": "IAM User Management: update user-setting user@company.com",
    "requestData": {
        "totalNumberChanges": 1,
        "update": [
            {
                "initialValue": false,
                "newValue": true,
                "updateType": "2FA update"
            },
        ]
    }
}
```
{: screen}

See the sample of the `requestData` field when the **Require MFA security questions at login:** property is enabled. The `requestData.security_questions_setup` field is set to `true`.

```json
{
    "action": "user-management.user-setting.update",
    "message": "IAM User Management: update user-setting user@company.com",
    "requestData": {
        "totalNumberChanges": 1,
        "update": [
            {
                "initialValue": false,
                "newValue": true,
                "updateType": "security_questions_setup update"
            }
        ]
    }
}
```
{: screen}

#### User accepts an account invitation
{: #at_events_analyze_accept_invitation}

When a user accepts an account invitation, you get the following event:
* Event with action `user-management.user-invitation.accept` that reports which user accepted the account invitation.

See the sample of the `responseData` field when the user accepts the invitation:

```json
    "action": "user-management.user-invitation.accept",
    "message": "IBM User Management: accept user invitation to account Joe Test's Account",
    "responseData": {
        "update": [
            {
                "initialValue": "BSS-3f6af42016b440e087025542cbd9cb91",
                "newValue": "IBMid-663003Z105",
                "updateType": "IAM ID Update during Accept"
            }
        ]
    }
```
{: screen}

#### requestData fields
{: #at_events_analyze_3_reqdata}

The following table lists *requestData* fields that you can find in events that are generated when user details are modified from the **Users** dashboard:

| Field | Type | Description |
|-------|------|-------------|
| `2FA`                      | Boolean         | Defines the MFA requirements for users in the account.   \n This field is set to `true` when MFA is enabled for users.  |
| `allowed_ip_addresses`     | String          | List of IP addresses from where a user is allowed to access account resources. |
| `ips_added` | String | The new IP adresses that are added to the `allowed_ip_addresses`. |
| `ips_removed` | String | The IP adresses that are removed from the `allowed_ip_addresses`. |
| `iam_id`                   | String          | Defines the IBM ID of the user whose settings are being modified. |
| `initialValue` | String | The original value for a specific user setting. Not applicable for `allowed_ip_addresses`. |
| `newValue` | String | The new value for a specific user setting. Not applicable for `allowed_ip_addresses`. |
| `updateType` | String | The specific user setting that is updated. |
| `security_questions_setup` | Boolean         | Defines when a user requires security questions to log in to the account.   \n This field is set to `true` to indicate that questions are required.  |
| `self_manage`              | Boolean         | Defines whether a user can configure his log in settings on how to log in to the account.    \n This field is set to `true` to allow a user to set password expiration, turn on security questions for login, and define allowed IP addresses for log in to {{site.data.keyword.cloud_notm}} and from classic infrastructure API calls.  |
| `totalNumberChanges` | The number of settings updated. |
{: caption="User management requestData fields" caption-side="top"}

### Events for managing account usage reports
{: #at_events_analyze_4}

This section explains events that are generated when a user looks at the information that is provided through the  **Manage > Billing and usage > Usage** section, or request an export of the data.

You can get events with `reason.reasonCode = 404` that are generated when there is no usage data available for the request. The `severity` is set to normal.
{: note}

#### requestData fields
{: #at_events_analyze_4_reqdata}

The following table lists the fields that are available through the `requestData` field in the events with actions `billing.account-summary.read`, `billing.account-summary.download`, and `billing.account-instances-usage-report.download`:

| Field | Type | Description | Status |
|-------|------|-------------|--------|
| `month` | String | Indicates the month that the user selects to view usage data. | Included always in the event |
{: caption="Account usage summary requestData fields" caption-side="top"}

The following table lists the fields that are available through the `requestData` field in the events with actions `billing.account-usage-report.read`:

| Field               | Type      | Description | Status |
|---------------------|-----------|-------------|--------|
| `month`             | String    | Indicates the month that the user selects to view usage data. |  Included always in the event |
| `usage_report_type` | String    | Indicates the type of report.   \n Valid values are `instances` and `rollup`.|  Included always in the event |
| `sub_account_id`    | String    | Indicates the sub-account ID. | Optional |
| `resource_group`    | String    | Indicates the resource group. | Optional   \n Included if the user filters data by resource group. |
| `organization_id`   | String    | Indicates the organization ID. | Optional |
| `daily`             | Boolean   | Indicates the frequency of the report. | Optional |
{: caption="Account usage requestData fields" caption-side="top"}

The following table lists the fields that are available through the `requestData` field in the events with actions `billing.enterprise-usage-report.read` and `billing.enterprise-usage-report.download`:

| Field               | Type      | Description | Status |
|---------------------|-----------|-------------|--------|
| `month`             | String    | Indicates the month that the user selects to view usage data. |  Included always in the event |
| `children`          | Boolean   | Indicates whether the usage is aggregated at account level. | Included always in the event |
| `enterprise_id`     | String    | Indicates the ID of the enterprise. |  Included always in the event |
| `account_id`        | String    | Indicates the sub-account ID that is requested in the report. | Optional |
| `account_group_id`  | String    | Indicates the account group when a user selects one. | Optional   \n Included if the user filters data by selecting 1 account group. |
{: caption="Enterprise usage requestData fields" caption-side="top"}

The following table lists the fields that are available through the `requestData` field in the events with actions `billing.enterprise-instances-usage-report.download`:

| Field               | Type      | Description | Status |
|---------------------|-----------|-------------|--------|
| `month`             | String    | Indicates the month that the user selects to view usage data. |  Included always in the event |
| `enterprise_id`     | String    | Indicates the ID of the enterprise. |  Included always in the event |
| `account_id`        | String    | Indicates the the sub-account IDs that is requested in the report. | Optional |
| `account_group_id`  | String    | Indicates the account group when a user selects one. | Optional   \n Included if the user filters data by selecting 1 account group. |
{: caption="Enterprise instances usage requestData fields" caption-side="top"}

### Account IAM settings events (Deprecated)
{: #at_events_analyze_1}

This section explains events that are generated when you configure the IAM account settings from the **Access (IAM) > Settings** dashboard.

#### Configuring MFA
{: #at_events_analyze_1_1}

When you set on MFA in your account by configuring the **Account Login** section in the **Access (IAM) > Settings** dashboard, you get 2 events:
* Event with action `billing.account-traits.update` that reports the type of MFA that is configured in the account in the `requestData.mfa` field.
* Event with action `billing.account-mfa.set-on` that indicates that MFA is enabled in the account.

When you set off MFA, you get the following 2 events:
* Event with action `billing.account-traits.update` that reports the type of MFA that is configured in the account in the `requestData.mfa` field.
* Event with action `billing.account-mfa.set-off` that indicates that MFA is disabled in the account.

For example, see the `requestData` field for the event `billing.account-traits.update`:

```json
"action": "billing.account-traits.update",
"message": "Billing service: update account traits",
"requestData": {
    "mfa": "",
    "origin": "BSS"
}
```
{: screen}

#### Configuring user list visibility restriction
{: #at_events_analyze_1_2}

When you modify the *User list visibility restriction* IAM account setting in the **Manage > Access (IAM) > Settings** dashboard, you get 1 event with action `billing.account-traits.update`.

For example, see the `requestData` field for the event `billing.account-traits.update`:

```json
"action": "billing.account-traits.update",
"message": "Billing service: update account traits",
"requestData": {
    "origin": "BSS",
    "team_directory_enabled": false
}
```
{: screen}

#### requestData fields
{: #at_events_analyze_1_reqdata}

The following table lists *requestData* fields that you can find in events that are generated when the IAM account settings are modified from the **Access (IAM) > Settings** dashboard:

| Field | Type | Description |
|-------|------|-------------|
| `team_directory_enabled`   | Boolean         | Defines the status of the *User list visibility restriction* IAM account setting.   \n When it is set to `true`, users in your account can view other users from the Users page. |
| `mfa`                      | String          | Defines the MFA method that is required for users to log in to the account.   \n Valid values are *TOTP*, and *TOTP4ALL*   \n This field is set to `TOTP` when the account requires MFA for non-federated users only. Users are required an ID, password, and a time-based one-time passcode to log in.   \n This field is set to `TOTP4ALL` when the account requires MFA for all users.  \n All users by requiring an ID, password, and a time-based one-time passcode.   \n When this field is empty, MFA is not enabled in the account, and all users log in by using a standard ID and password. |
{: caption="Account IAM settings requestData fields" caption-side="top"}
