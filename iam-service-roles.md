---

copyright:

  years: 2019

lastupdated: "2022-05-23"

keywords: service iam roles, service iam actions, account management roles, iam roles

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:faq: data-hd-content-type='faq'}
{:note: .note}

# IAM roles and actions
{: #iam-service-roles-actions}

It is important to understand how to effectively assign access for users to work with products and take specific account management actions within your account to follow the principle of least privilege and minimize the number of policies that you have to manage. The following tables provide information about the access roles and the actions mapped to each by the {{site.data.keyword.cloud}} services. 
{: shortdesc}

The following tables provide data from the individual IAM-enabled services that are available from the {{site.data.keyword.cloud_notm}} catalog as well as the  account management services that enable you to assign others the ability to work with users, access groups, support cases, and more in the account. If you don't see a platform roles or service roles table, then that means that particular service doesn't use those types of roles.

Each service has custom actions that they define and map to platform and service roles that you can use to assign access by creating an IAM access policy. If you are trying to assign access and an existing role doesn't fit your needs, you can create a [custom role](/docs/account?topic=account-custom-roles) that combines any number of actions that are available for a given service.

For more information about assigning access for each service, check out the documentation for the service that you're using.

<!-- Everything is deleted after this line. -->
## Statum KPI
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `3p-amberoon-xaas-statumkpi` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 1. Platform roles - Statum KPI" caption-side="top"}
{: #platform-roles-table1}
{: tab-title="Platform roles"}
{: tab-group="3p-amberoon-xaas-statumkpi"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `3p-amberoon-xaas-statumkpi.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 1. Service actions - Statum KPI" caption-side="top"}
{: #actions-table1}
{: tab-title="Actions"}
{: tab-group="3p-amberoon-xaas-statumkpi"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## ViziVault Platform
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `3p-anontech-xaas-vizivault` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 2. Platform roles - ViziVault Platform" caption-side="top"}
{: #platform-roles-table2}
{: tab-title="Platform roles"}
{: tab-group="3p-anontech-xaas-vizivault"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `3p-anontech-xaas-vizivault.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 2. Service actions - ViziVault Platform" caption-side="top"}
{: #actions-table2}
{: tab-title="Actions"}
{: tab-group="3p-anontech-xaas-vizivault"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Cognitive View
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `3p-cognitiveview-xaas-cognitiveview` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 3. Platform roles - Cognitive View" caption-side="top"}
{: #platform-roles-table3}
{: tab-title="Platform roles"}
{: tab-group="3p-cognitiveview-xaas-cognitiveview"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `3p-cognitiveview-xaas-cognitiveview.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 3. Service actions - Cognitive View" caption-side="top"}
{: #actions-table3}
{: tab-title="Actions"}
{: tab-group="3p-cognitiveview-xaas-cognitiveview"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## SimpleCloud
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `3p-summusrender-xaas-simplecl0ud` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 4. Platform roles - SimpleCloud" caption-side="top"}
{: #platform-roles-table4}
{: tab-title="Platform roles"}
{: tab-group="3p-summusrender-xaas-simplecl0ud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `3p-summusrender-xaas-simplecl0ud.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 4. Service actions - SimpleCloud" caption-side="top"}
{: #actions-table4}
{: tab-title="Actions"}
{: tab-group="3p-summusrender-xaas-simplecl0ud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## VPC+ DRaaS (VPC+ Disaster Recovery as a Service)
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `3p-wanclds-draas-vpcplus` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 5. Platform roles - VPC+ DRaaS (VPC+ Disaster Recovery as a Service)" caption-side="top"}
{: #platform-roles-table5}
{: tab-title="Platform roles"}
{: tab-group="3p-wanclds-draas-vpcplus"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `3p-wanclds-draas-vpcplus.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 5. Service actions - VPC+ DRaaS (VPC+ Disaster Recovery as a Service)" caption-side="top"}
{: #actions-table5}
{: tab-title="Actions"}
{: tab-group="3p-wanclds-draas-vpcplus"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Watson OpenScale
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `aiopenscale` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 6. Platform roles - Watson OpenScale" caption-side="top"}
{: #platform-roles-table6}
{: tab-title="Platform roles"}
{: tab-group="aiopenscale"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `aiopenscale.dashboard.view` |  | Administrator, Editor, Operator, Viewer |
{: caption="Table 6. Service actions - Watson OpenScale" caption-side="top"}
{: #actions-table6}
{: tab-title="Actions"}
{: tab-group="aiopenscale"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## API Gateway
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `api-gateway` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 7. Platform roles - API Gateway" caption-side="top"}
{: #platform-roles-table7}
{: tab-title="Platform roles"}
{: tab-group="api-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 7. Service roles - API Gateway" caption-side="top"}
{: #service-roles-table7}
{: tab-title="Service roles"}
{: tab-group="api-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `api-gateway.dashboard.view` |  | Administrator, Editor, Operator |
| `api-gateway.api.view` |  | Manager, Reader, Writer |
| `api-gateway.api.create` |  | Manager, Writer |
| `api-gateway.api.edit` |  | Manager, Writer |
| `api-gateway.api.delete` |  | Manager, Writer |
| `api-gateway.api.share` |  | Manager |
{: caption="Table 7. Service actions - API Gateway" caption-side="top"}
{: #actions-table7}
{: tab-title="Actions"}
{: tab-group="api-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## API Connect
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `apiconnect` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 8. Platform roles - API Connect" caption-side="top"}
{: #platform-roles-table8}
{: tab-title="Platform roles"}
{: tab-group="apiconnect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 8. Service roles - API Connect" caption-side="top"}
{: #service-roles-table8}
{: tab-title="Service roles"}
{: tab-group="apiconnect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `apiconnect.instance.view` | apiconnect.instance.view | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `apiconnect.instance.admin` | apiconnect.instance.admin | Administrator |
| `apiconnect.admin.manage` | Enables API Connect administrators to create provider orgs, manage gateways, and adjust other settings for the environment. | Administrator, Editor, Manager |
| `apiconnect.instance.api-admin` | apiconnect.instance.api-admin | Editor, Manager |
| `apiconnect.instance.develop` | apiconnect.instance.develop | Writer |
| `apiconnect.instance.manage-community` | apiconnect.instance.manage-community | Operator |
{: caption="Table 8. Service actions - API Connect" caption-side="top"}
{: #actions-table8}
{: tab-title="Actions"}
{: tab-group="apiconnect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## App ID
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `appid` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 9. Service roles - App ID" caption-side="top"}
{: #service-roles-table9}
{: tab-title="Service roles"}
{: tab-group="appid"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `appid.mgmt.set.sender.details.cd` | Set the sender details for emails sent to Cloud Directory users. | Manager, Writer |
| `appid.mgmt.get.sender.details.cd` | View the sender details for the emails sent to Cloud Directory users. | Manager, Reader, Writer |
| `appid.mgmt.set.redirect.uris` | Add or update post-authentication redirect URIs. | Manager, Writer |
| `appid.mgmt.get.redirect.uris` | View the post-authentication redirect URIs that are currently configured. | Manager, Reader, Writer |
| `appid.mgmt.set.idps` | Configure the identity provider options that a user has at sign in. | Manager, Writer |
| `appid.mgmt.get.idps` | View the current identity provider options that a user has when they sign in. | Manager, Reader, Writer |
| `appid.mgmt.get.recent.activities` | View recent authentication activity for an application. | Manager, Reader, Writer |
| `appid.mgmt.get.ui.config` | View the current Login Widget configuration including the color and logo. | Manager, Reader, Writer |
| `appid.mgmt.set.ui.config` | Configure the appearance of the Login Widget including the color and logo. | Manager, Writer |
| `appid.mgmt.get.user.profile.config` | Get user information from your app configuration. | Manager, Reader, Writer |
| `appid.mgmt.set.user.profile.config` | Update a user profile with the information from your app. | Manager, Writer |
| `appid.mgmt.get.cd.users` | View Cloud Directory users and their data. | Manager, Reader, Writer |
| `appid.mgmt.add.cd.user` | Create a Cloud Directory user | Manager, Writer |
| `appid.mgmt.set.cd.user` | Update a Cloud Directory user's information. | Manager, Writer |
| `appid.mgmt.delete.cd.user` | Delete a user from Cloud Directory. | Manager, Writer |
| `appid.mgmt.get.email.template` | Get your current email template configuration. | Manager, Reader, Writer |
| `appid.mgmt.update.email.template` | Update your email template configuration | Manager, Writer |
| `appid.mgmt.delete.email.template` | Delete an email template configuration. | Manager, Writer |
| `appid.mgmt.get.saml.metadata` | Get the metadata that is used to link your SAML provider. | Manager, Reader, Writer |
| `appid.mgmt.resend.notification.cd` | Resend an email to a Cloud Directory user. | Manager, Writer |
| `appid.mgmt.get.tokens.configuration` | View the current configuration of your tokens. | Manager, Reader, Writer |
| `appid.mgmt.set.tokens.configuration` | Configure the access, identity, and refresh tokens. | Manager, Writer |
| `appid.mgmt.cd.sign.up` | Start the sign up process for a new Cloud Directory user. | Manager, Writer |
| `appid.mgmt.cd.sign.up.result` | View the result of a new user sign up. | Manager, Writer |
| `appid.mgmt.cd.forgot.password` | Start the forgot password email flow for a Cloud Directory user. | Manager, Writer |
| `appid.mgmt.cd.forgot.password.result` | View whether the forgot password email was successfully sent. | Manager, Writer |
| `appid.mgmt.cd.change.password` | Start the change password email flow for a Cloud Directory user. | Manager, Writer |
| `appid.mgmt.get.cd.actions.urls` | View the action URLs that are configured for Cloud Directory. | Manager, Reader, Writer |
| `appid.mgmt.get.cd.action.url` | Get a single action URI that is configured for Cloud Directory. | Manager, Reader, Writer |
| `appid.mgmt.update.cd.action.url` | Update an action URI that is configured for Cloud Directory. | Manager, Writer |
| `appid.mgmt.del.cd.action.url` | Delete an action URI that is configured for Cloud Directory. | Manager, Writer |
| `appid.mgmt.get.cd.password.policy` | View the Cloud Directory password policy configuration in regex form | Manager, Reader, Writer |
| `appid.mgmt.update.cd.password.policy` | Update a Cloud Directory password policy in regex. | Manager, Writer |
| `appid.mgmt.delete.profile` | Delete a user profile from App ID. | Manager, Writer |
| `appid.mgmt.get.profile` | View a user profile. | Manager, Reader, Writer |
| `appid.mgmt.update.profile` | Update a user's profile. | Manager, Writer |
| `appid.mgmt.get.profiles` | Search all of your user profiles and get a count of any anonymous users. | Manager, Reader, Writer |
| `appid.mgmt.revoke.refresh.token` | Revoke a user's refresh token. | Manager, Writer |
| `appid.mgmt.nominate.user` | Create a profile for a future user. | Manager, Writer |
| `appid.mgmt.update.cd.get.email.dispatcher` | View the email provider configuration. | Manager, Reader, Writer |
| `appid.mgmt.update.cd.set.email.dispatcher` | Configure or update an email provider. | Manager, Writer |
| `appid.mgmt.update.cd.post.email.dispatcher.test` | Test the email provider configuration. | Manager, Writer |
| `appid.mgmt.add.application` | Register a new application with App ID. | Manager, Writer |
| `appid.mgmt.delete.application` | Delete an application that is registered with App ID | Manager, Writer |
| `appid.mgmt.update.application` | Update an application that is registered with App ID. | Manager, Writer |
| `appid.mgmt.get.applications` | View all of the apps that are registered with your instance of App ID. | Manager, Reader, Writer |
| `appid.mgmt.get.application` | View a specific application that is registered with App ID. | Manager, Reader, Writer |
| `appid.mgmt.export.cd.users` | Export Cloud Directory users and their information as a JSON object. | Manager |
| `appid.mgmt.import.cd.users` | Import the Cloud Directory users and their information that was exported from another instance of the service. | Manager |
| `appid.mgmt.get.capture.runtime.activity` | Get the auditing status of the tenant as a JSON object. | Manager, Reader, Writer |
| `appid.mgmt.update.capture.runtime.activity` | Update the auditing status. | Manager, Writer |
| `appid.mgmt.get.mfa.channels` | Get a list of all of the configured MFA channels. | Manager, Reader, Writer |
| `appid.mgmt.get.mfa.channel` | Get an MFA channel. | Manager, Reader, Writer |
| `appid.mgmt.update.mfa.channel` | Update an MFA channel. | Manager, Writer |
| `appid.mgmt.update.mfa.config` | Update an MFA configuration. | Manager, Writer |
| `appid.mgmt.get.mfa.config` | View the current MFA configuration. | Manager, Reader, Writer |
| `appid.mgmt.get.advanced.password.management` | View the current advanced password policy configuration. | Manager, Reader, Writer |
| `appid.mgmt.set.advanced.password.management` | Configure advanced password policies. | Manager, Writer |
| `appid.mgmt.get.sso.config` | Get the Cloud Directory SSO configuration. | Manager, Reader, Writer |
| `appid.mgmt.update.sso.config` | Update the Cloud Directory SSO configuration. | Manager, Writer |
| `appid.mgmt.post.sso.logout` | Initiate SSO logout for Cloud Directory. | Manager, Writer |
| `appid.mgmt.cd.post.sms.dispatcher.test` | Test the MFA configuration for SMS. | Manager, Writer |
| `appid.mgmt.remove.cd.user` | Delete Cloud Directory users and their profile. | Manager, Writer |
| `appid.mgmt.get.cd.userinfo` | Get a Cloud Directory user and their information. | Manager, Reader, Writer |
| `appid.mgmt.get.cd.rate.config` | Get the rate limite configuration. | Manager, Reader, Writer |
| `appid.mgmt.update.cd.rate.config` | Update the rate limit configuration. | Manager, Writer |
| `appid.mgmt.import.profiles` | Import user profiles that have been exported from another instance of App ID. | Manager |
| `appid.mgmt.export.profiles` | Export user profiles. | Manager |
| `appid.mgmt.add.scope` | Add a scope to an application. | Manager, Writer |
| `appid.mgmt.get.scopes` | Get the scopes that are associated with an application. | Manager, Reader, Writer |
| `appid.mgmt.delete.scope` | Delete a scope that is associated with an application. | Manager, Writer |
| `appid.mgmt.add.role` | Create a role. | Manager, Writer |
| `appid.mgmt.get.role` | Get a role that is associated with a scope. | Manager, Reader, Writer |
| `appid.mgmt.update.role` | Update a role. | Manager, Writer |
| `appid.mgmt.delete.role` | Delete a role. | Manager, Writer |
| `appid.mgmt.get.user.roles` | View the roles that are assigned to a specific user. | Manager, Reader, Writer |
| `appid.mgmt.update.user.roles` | Update a user's associated roles. | Manager, Writer |
| `appid.mgmt.get.webhook.config` | Get a registered extension's configuration. | Manager, Reader, Writer |
| `appid.mgmt.update.webhook.config` | Update a registered extensions configuration. | Manager, Writer |
| `appid.mgmt.update.webhook.active` | Update the status of a registered extension's configuration. | Manager, Writer |
| `appid.mgmt.test.webhook.config` | Test the configuration for a registered extension. | Manager, Writer |
| `appid.mgmt.del.totp.channel` | appid-mgmt-del-totp-channel | Manager, Writer |
| `appid.mgmt.get.application.roles` | Get application roles | Manager, Reader, Writer |
| `appid.mgmt.update.application.roles` | Update application roles | Manager, Writer |
{: caption="Table 9. Service actions - App ID" caption-side="top"}
{: #actions-table9}
{: tab-title="Actions"}
{: tab-group="appid"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## App Configuration
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `apprapp` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 10. Platform roles - App Configuration" caption-side="top"}
{: #platform-roles-table10}
{: tab-title="Platform roles"}
{: tab-group="apprapp"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Config Operator | As a Config Operator, you can toggle the feature state. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 10. Service roles - App Configuration" caption-side="top"}
{: #service-roles-table10}
{: tab-title="Service roles"}
{: tab-group="apprapp"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `apprapp.dashboard.view` | Dashboard view | Administrator, Config Operator, Editor, Manager, Operator, Reader, Writer |
| `apprapp.collections.list` | List collections | Administrator, Config Operator, Manager, Reader, Writer |
| `apprapp.collections.create` | Create collections | Administrator, Manager |
| `apprapp.collections.update` | Update collections | Administrator, Manager |
| `apprapp.collections.delete` | Delete collections  | Administrator, Manager |
| `apprapp.segments.list` | List segments | Administrator, Config Operator, Manager, Reader, Writer |
| `apprapp.segments.update` | Update segments | Administrator, Manager, Writer |
| `apprapp.segments.create` | Create segments | Administrator, Manager, Writer |
| `apprapp.segments.delete` | Delete segments | Administrator, Manager, Writer |
| `apprapp.features.toggle` | Toggle feature | Administrator, Config Operator, Manager, Writer |
| `apprapp.properties.patch` | Patch properties | Writer |
| `apprapp.environments.create` | Create environments | Administrator, Manager |
| `apprapp.environments.update` | Update environments | Administrator, Manager |
| `apprapp.environments.delete` | Delete environments | Administrator, Manager |
| `apprapp.environments.list` | List environments | Administrator, Config Operator, Manager, Reader, Writer |
| `apprapp.features.list` | List features | Administrator, Config Operator, Manager, Reader, Writer |
| `apprapp.features.create` | Create Features | Administrator, Manager |
| `apprapp.features.update` | Update features | Administrator, Manager |
| `apprapp.features.delete` | Delete features | Administrator, Manager |
| `apprapp.features.patch` | Patch features | Administrator, Writer |
| `apprapp.properties.list` | List properties | Config Operator, Manager, Reader, Writer |
| `apprapp.properties.update` | Update properties | Administrator, Manager |
| `apprapp.properties.create` | Create properties | Administrator, Manager |
| `apprapp.properties.delete` | Delete properties | Administrator, Manager |
| `apprapp.properties.patch` | Patch properties | Administrator, Writer |
| `apprapp.instances.export` | Export instance resources to a JSON | Administrator, Manager |
| `apprapp.instances.import` | Import instance resources from a JSON | Administrator, Manager |
{: caption="Table 10. Service actions - App Configuration" caption-side="top"}
{: #actions-table10}
{: tab-title="Actions"}
{: tab-group="apprapp"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Activity Tracker
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `atracker` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 11. Platform roles - Activity Tracker" caption-side="top"}
{: #platform-roles-table11}
{: tab-title="Platform roles"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 11. Service roles - Activity Tracker" caption-side="top"}
{: #service-roles-table11}
{: tab-title="Service roles"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `atracker.target.read` | read target | Administrator, Editor, Operator, Viewer |
| `atracker.target.create` | Create atracker target | Administrator, Editor |
| `atracker.target.update` | Update atracker target | Administrator, Editor |
| `atracker.target.delete` | Delete atracker target | Administrator, Editor |
| `atracker.target.list` | List the atracker targets | Administrator, Editor, Operator, Viewer |
| `atracker.route.read` | Read atracker route | Administrator, Editor, Operator, Viewer |
| `atracker.route.create` | Create atracker route | Administrator, Editor |
| `atracker.route.update` | Update atracker route | Administrator, Editor |
| `atracker.route.delete` | Delete atracker route | Administrator, Editor |
| `atracker.route.list` | List atracker routes | Administrator, Editor, Operator, Viewer |
| `atracker.endpoint.set` | Set atracker endpoint properties | Administrator |
| `atracker.endpoint.get` | Read atracker endpoint properties | Administrator, Editor, Operator, Viewer |
| `atracker.service.ingest` | Send events to Atracker | Writer |
| `atracker.setting.get` | Get Atracker setting | Administrator, Editor, Operator, Viewer |
| `atracker.setting.update` | Update Atracker setting | Administrator |
| `atracker.migration.post` | Post atracker migration | Administrator |
| `atracker.migration.get` | Get atracker migration | Administrator, Editor, Operator, Viewer |
| `atracker.migration.delete` | Delete Atracker migration | Administrator |
{: caption="Table 11. Service actions - Activity Tracker" caption-side="top"}
{: #actions-table11}
{: tab-title="Actions"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Billing
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `billing` for the service name.

No supported roles.
## Blockchain Platform 2.0
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `blockchain` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 13. Service roles - Blockchain Platform 2.0" caption-side="top"}
{: #service-roles-table13}
{: tab-title="Service roles"}
{: tab-group="blockchain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `blockchain.components.create` | Can create (provision) Orderes/CAs/Peers | Manager |
| `blockchain.components.remove` | Can remove imported Orderes/CAs/Peers | Manager, Writer |
| `blockchain.components.import` | Can import external Orderes/CAs/Peers | Manager, Writer |
| `blockchain.components.export` | Can export any Orderes/CAs/Peers | Manager, Reader, Writer |
| `blockchain.optools.restart` | Can restart the UI server | Manager |
| `blockchain.optools.logs` | Can change logging settings of the UI | Manager |
| `blockchain.optools.view` | Can view the UI & logs as well as run any GET api | Manager, Reader, Writer |
| `blockchain.notifications.manage` | Can add/remove UI notifications | Manager, Writer |
| `blockchain.components.delete` | Can remove provisioned Orderes/CAs/Peers | Manager |
| `blockchain.signaturecollection.manage` | Can add/remove signature collections | Manager, Writer |
| `blockchain.optools.settings` | Can change UI settings | Manager |
| `blockchain.components.manage` | Can manage admin certs on Peers/Orderers as well as enroll ids on CAs | Manager, Writer |
| `blockchain.instance.link` | Can associate an IBM Blockchain Platform service instance with a cluster | Manager |
| `blockchain.instance.view` | Can get the status of the an IBM Blockchain Platform service instance | Manager, Reader, Writer |
| `blockchain.optools.redeploy` | Can redeploy an IBM Blockchain Platform service instance | Manager |
{: caption="Table 13. Service actions - Blockchain Platform 2.0" caption-side="top"}
{: #actions-table13}
{: tab-title="Actions"}
{: tab-group="blockchain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Cloud Foundry Enterprise Environment
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cfaas` for the service name.

No supported roles.
## Cloud Object Storage
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cloud-object-storage` for the service name.

| Role | Description |
| ----- | :----- |
| Content Reader | As a Content Reader, one can read and list objects in the bucket. |
| Manager | As a Manager, one can create/modify/delete buckets including managing retention policy, configuring IP addresses. In addition, one can upload and download the objects in the bucket. |
| Notifications Manager | As a Notifications Manager, the service can manage (view/modify/delete) configuration for notifications on a Cloud Object Storage bucket. |
| Object Reader | As an Object Reader, one can read objects in the bucket. |
| Object Writer | As an Object Writer, one can only write objects to a bucket. |
| Reader | As a Reader, one can view bucket configuration and download the objects in the bucket. |
| Writer | As a Writer, one can create/modify/delete buckets. In addition, one can upload and download the objects in the bucket. |
{: row-headers}
{: caption="Table 15. Service roles - Cloud Object Storage" caption-side="top"}
{: #service-roles-table15}
{: tab-title="Service roles"}
{: tab-group="cloud-object-storage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `cloud-object-storage.account.get_account_buckets` | List all buckets in a service instance. | Manager, Notifications Manager, Reader, Writer |
| `cloud-object-storage.bucket.put_bucket` | Create a bucket. | Manager, Writer |
| `cloud-object-storage.bucket.post_bucket` | Internal use only - unsupported for users. | Manager, Writer |
| `cloud-object-storage.bucket.delete_bucket` | Delete a bucket. | Manager, Writer |
| `cloud-object-storage.bucket.get` | List all the objects in a bucket. | Content Reader, Manager, Reader, Writer |
| `cloud-object-storage.bucket.list_crk_id` | List the IDs of encryption root keys associated with a bucket. | Manager, Writer |
| `cloud-object-storage.bucket.head` | View bucket metadata. | Content Reader, Manager, Reader, Writer |
| `cloud-object-storage.bucket.get_versions` | Unsupported operation - used for S3 API compatibility only. | Content Reader, Manager, Reader, Writer |
| `cloud-object-storage.bucket.get_uploads` | List all active multipart uploads for a bucket. | Manager, Reader, Writer |
| `cloud-object-storage.bucket.get_acl` | Read a bucket ACL [deprecated]. | Manager |
| `cloud-object-storage.bucket.put_acl` | Create a bucket ACL [deprecated]. | Manager |
| `cloud-object-storage.bucket.get_cors` | Read CORS rules. | Manager, Reader, Writer |
| `cloud-object-storage.bucket.put_cors` | Add CORS rules to a bucket. | Manager, Writer |
| `cloud-object-storage.bucket.delete_cors` | Delete CORS rules. | Manager, Writer |
| `cloud-object-storage.bucket.get_website` | Read bucket website configuration. | Manager, Reader, Writer |
| `cloud-object-storage.bucket.put_website` | Add bucket website configuration. | Manager, Writer |
| `cloud-object-storage.bucket.delete_website` | Delete bucket website configuration. | Manager, Writer |
| `cloud-object-storage.bucket.get_versioning` | Unsupported operation - used for S3 API compatibility only. | Manager, Reader, Writer |
| `cloud-object-storage.bucket.put_versioning` | Unsupported operation - used for S3 API compatibility only. | Manager, Writer |
| `cloud-object-storage.bucket.get_fasp_connection_info` | View Aspera FASP connection information. | Manager, Reader, Writer |
| `cloud-object-storage.account.delete_fasp_connection_info` | Delete Aspera FASP connection information. | Manager, Writer |
| `cloud-object-storage.bucket.get_location` | View the location and storage class of a bucket. | Content Reader, Manager, Notifications Manager, Reader, Writer |
| `cloud-object-storage.bucket.get_lifecycle` | Read a bucket lifecycle policy. | Manager, Reader, Writer |
| `cloud-object-storage.bucket.put_lifecycle` | Create a bucket lifecycle policy. | Manager, Writer |
| `cloud-object-storage.bucket.get_activity_tracking` | Read activity tracking configuration. | Manager, Reader, Writer |
| `cloud-object-storage.bucket.put_activity_tracking` | Add activity tracking configuration. | Manager, Writer |
| `cloud-object-storage.bucket.get_metrics_monitoring` | Read metrics monitoring configuration. | Manager, Reader, Writer |
| `cloud-object-storage.bucket.put_metrics_monitoring` | Add metrics monitoring configuration. | Manager, Writer |
| `cloud-object-storage.bucket.put_protection` | Add Immutable Object Storage policy. | Manager |
| `cloud-object-storage.bucket.get_protection` | Read Immutable Object Storage policy. | Manager, Reader, Writer |
| `cloud-object-storage.bucket.put_firewall` | Add a firewall configuration. | Manager |
| `cloud-object-storage.bucket.get_firewall` | Read a firewall configuration. | Manager |
| `cloud-object-storage.bucket.put_public_access_block` | Add/Update a public access block configuration for a bucket. | Manager |
| `cloud-object-storage.bucket.delete_public_access_block` | Remove public access block configuration for a bucket. | Manager |
| `cloud-object-storage.bucket.get_public_access_block` | Retrieve public access block configuration for a bucket. | Manager |
| `cloud-object-storage.bucket.get_basic` | List objects in a bucket [deprecated]. | Manager, Notifications Manager, Reader, Writer |
| `cloud-object-storage.bucket.list_bucket_crn` | View a bucket CRN. | Manager, Reader, Writer |
| `cloud-object-storage.bucket.get_notifications` | Internal use only - unsupported for users. | Notifications Manager |
| `cloud-object-storage.bucket.put_notifications` | Internal use only - unsupported for users. | Notifications Manager |
| `cloud-object-storage.object.get` | View and download objects. | Content Reader, Manager, Object Reader, Reader, Writer |
| `cloud-object-storage.object.head` | Read an object's metadata. | Content Reader, Manager, Object Reader, Reader, Writer |
| `cloud-object-storage.object.get_version` | Unsupported operation - used for S3 API compatibility only. | Content Reader, Manager, Object Reader, Reader, Writer |
| `cloud-object-storage.object.head_version` | Unsupported operation - used for S3 API compatibility only. | Content Reader, Manager, Object Reader, Reader, Writer |
| `cloud-object-storage.object.put` | Write and upload objects. | Manager, Object Writer, Writer |
| `cloud-object-storage.object.post` | Upload an object using HTML forms [deprecated]. | Manager, Object Writer, Writer |
| `cloud-object-storage.object.post_md` | Update object metadata using HTML forms [deprecated]. | Manager, Object Writer, Writer |
| `cloud-object-storage.object.post_initiate_upload` | Initiate multipart uploads. | Manager, Object Writer, Writer |
| `cloud-object-storage.object.put_part` | Upload an object part. | Manager, Object Writer, Writer |
| `cloud-object-storage.object.copy_part` | Copy (write) an object part. | Manager, Writer |
| `cloud-object-storage.object.copy_part_get` | Copy (read) an object part. | Manager, Reader, Writer |
| `cloud-object-storage.object.post_complete_upload` | Complete a multipart upload. | Manager, Object Writer, Writer |
| `cloud-object-storage.object.copy` | Copy (write) an object from one bucket to another. | Manager, Writer |
| `cloud-object-storage.object.copy_get` | Copy (read) an object from one bucket to another. | Manager, Reader, Writer |
| `cloud-object-storage.object.get_acl` | Read object ACL [deprecated]. | Manager |
| `cloud-object-storage.object.get_acl_version` | Read object ACL Version [deprecated]. | Manager |
| `cloud-object-storage.object.put_acl` | Write object ACL [deprecated]. | Manager |
| `cloud-object-storage.object.put_acl_version` | Unsupported operation - used for S3 API compatibility only. | Manager |
| `cloud-object-storage.object.delete` | Delete an object. | Manager, Writer |
| `cloud-object-storage.object.delete_version` | Unsupported operation - used for S3 API compatibility only. | Manager, Writer |
| `cloud-object-storage.object.get_tagging` | Read object tags | Manager, Reader, Writer |
| `cloud-object-storage.object.get_tagging_version` | Read object tag versions | Manager, Reader, Writer |
| `cloud-object-storage.object.put_tagging` | Add/Update object tags | Manager, Object Writer, Writer |
| `cloud-object-storage.object.put_tagging_version` | Add/Update object tag versions | Manager, Object Writer, Writer |
| `cloud-object-storage.object.delete_tagging` | Delete object tags | Manager, Object Writer, Writer |
| `cloud-object-storage.object.delete_tagging_version` | Delete object tag versions | Manager, Object Writer, Writer |
| `cloud-object-storage.object.get_uploads` | List parts of a multi-part object upload. | Manager, Object Writer, Reader, Writer |
| `cloud-object-storage.object.delete_upload` | Abort a multipart upload. | Manager, Object Writer, Writer |
| `cloud-object-storage.object.restore` | Temporarily restore an archived object. | Manager, Writer |
| `cloud-object-storage.object.post_multi_delete` | Delete multiple objects. | Manager, Writer |
| `cloud-object-storage.object.post_legal_hold` | Add a legal hold to an object. | Manager, Writer |
| `cloud-object-storage.object.get_legal_hold` | View any legal holds on an object. | Manager, Reader, Writer |
| `cloud-object-storage.object.post_extend_retention` | Extend a retention policy. | Manager, Writer |
| `cloud-object-storage.bucket.put_quota` | Set a hard quota on a bucket. | Manager |
| `cloud-object-storage.bucket.get_quota` | Read a bucket's hard quota. | Manager, Writer |
| `cloud-object-storage.object.copy_get_version` | Copy (read) a version of an object from one bucket to another. | Content Reader, Manager, Object Reader, Reader, Writer |
| `cloud-object-storage.object.copy_part_get_version` | Copy (read) a version of an object as a part. | Content Reader, Manager, Object Reader, Reader, Writer |
| `cloud-object-storage.object.restore_version` | Temporarily restore an archived version of an object. | Manager, Writer |
| `cloud-object-storage.bucket.get_replication` | Read replication configuration of an bucket. | Manager, Reader, Writer |
| `cloud-object-storage.bucket.put_replication` | Add replication configuration to a bucket. | Manager, Writer |
| `cloud-object-storage.bucket.delete_replication` | Delete replication configuration of an bucket. | Manager, Writer |
{: caption="Table 15. Service actions - Cloud Object Storage" caption-side="top"}
{: #actions-table15}
{: tab-title="Actions"}
{: tab-group="cloud-object-storage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Cloudant
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cloudantnosqldb` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 16. Platform roles - Cloudant" caption-side="top"}
{: #platform-roles-table16}
{: tab-title="Platform roles"}
{: tab-group="cloudantnosqldb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Checkpointer | As a Checkpointer, you have permissions to write _local documents enabling checkpoint writes. checkpoints are local documents optionally created during replication recording their state. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Monitor | As a Monitor, you have permissions to get information about specified databases, list databases, monitor indexing and replication, view data volume usage and view provisioned and current throughput. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 16. Service roles - Cloudant" caption-side="top"}
{: #service-roles-table16}
{: tab-title="Service roles"}
{: tab-group="cloudantnosqldb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `cloudantnosqldb.db.any` | Perform any database action | Manager |
| `cloudantnosqldb.activity-tracker-event-types.read` | Access list of configured activity tracker event types for a service instance | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `cloudantnosqldb.activity-tracker-event-types.write` | Update list of configured activity tracker event types for a service instance | Administrator, Manager, Operator |
| `cloudantnosqldb.sapi.lastactivity` | Access last activity time for account | Manager |
| `cloudantnosqldb.sapi.usercors` | Update CORS settings for a service instance | Manager |
| `cloudantnosqldb.sapi.apikeys` | Generate Cloudant API keys for a service instance | Manager |
| `cloudantnosqldb.sapi.userccmdiagnostics` | Access current and maximum allowed throughput values | Manager |
| `cloudantnosqldb.sapi.supportattachments` | View attachments on support tickets for user | Manager |
| `cloudantnosqldb.sapi.supporttickets` | View support tickets for user | Manager |
| `cloudantnosqldb.sapi.userinfo` | Retrieve basic user infomation for this user | Administrator, Editor, Manager, Operator, Viewer |
| `cloudantnosqldb.users-database-info.read` | Read _users database info | Manager |
| `cloudantnosqldb.users-database.create` | Create users databases | Manager |
| `cloudantnosqldb.users-database.delete` | Delete users databases | Manager |
| `cloudantnosqldb.users.read` | Read from users databases | Manager |
| `cloudantnosqldb.users.write` | Write to users databases | Manager |
| `cloudantnosqldb.database.create` | Create databases | Manager |
| `cloudantnosqldb.database.delete` | Delete databases | Manager |
| `cloudantnosqldb.sapi.userplan` | Retrieve and update instance plan settings | Administrator, Editor, Manager, Operator, Viewer |
| `cloudantnosqldb.sapi.usage-data-volume` | View instance data usage | Administrator, Editor, Manager, Monitor, Operator, Viewer |
| `cloudantnosqldb.sapi.usage-requests` | View instance requests usage | Manager |
| `cloudantnosqldb.account-active-tasks.read` | View active tasks for instance | Manager, Monitor |
| `cloudantnosqldb.sapi.db-security` | Allow update of database security | Manager |
| `cloudantnosqldb.session.write` | Write _session endpoint | Manager, Reader, Writer |
| `cloudantnosqldb.session.read` | Read _session endpoint | Manager, Reader, Writer |
| `cloudantnosqldb.session.delete` | Delete _session endpoint | Manager, Reader, Writer |
| `cloudantnosqldb.iam-session.write` | Write _iam_session endpoint | Manager, Reader, Writer |
| `cloudantnosqldb.iam-session.read` | Read _iam_session endpoint | Manager, Reader, Writer |
| `cloudantnosqldb.iam-session.delete` | Delete _iam_session endpoint | Manager, Reader, Writer |
| `cloudantnosqldb.account-db-updates.read` | Read db_updates feed | Manager, Reader, Writer |
| `cloudantnosqldb.any-document.read` | Read any documents in a normal database | Manager, Reader, Writer |
| `cloudantnosqldb.database-info.read` | Read /db/ database info | Manager, Monitor, Reader, Writer |
| `cloudantnosqldb.account-dbs-info.read` | Read _dbs_info endpoint | Manager, Monitor, Reader, Writer |
| `cloudantnosqldb.replicator-database-info.read` | Read _replicator database info | Manager |
| `cloudantnosqldb.replicator-database.create` | Create _replicator databases | Manager |
| `cloudantnosqldb.replicator-database.delete` | Delete _replicator databases | Manager |
| `cloudantnosqldb.replication.write` | Write to _replicator databases | Manager |
| `cloudantnosqldb.replication.read` | Read from _replicator databases | Manager |
| `cloudantnosqldb.replication-scheduler.read` | Read from replication _scheduler endpoints | Manager, Monitor |
| `cloudantnosqldb.account-up.read` | View _up | Manager, Monitor |
| `cloudantnosqldb.account-uuids.read` | Generate doc ID UUIDs | Manager, Writer |
| `cloudantnosqldb.data-document.write` | Create, update and delete normal documents in a database | Manager, Writer |
| `cloudantnosqldb.local-document.write` | Write _local documents | Checkpointer, Manager, Writer |
| `cloudantnosqldb.design-document.write` | Write _design documents | Manager |
| `cloudantnosqldb.cluster-membership.read` | View cluster membership | Manager |
| `cloudantnosqldb.database-security.read` | Read database security definitions | Manager |
| `cloudantnosqldb.database-security.write` | Write database security definitions | Manager |
| `cloudantnosqldb.database-shards.read` | View database shard metadata | Manager, Monitor |
| `cloudantnosqldb.capacity-throughput.read` | Read current provisioned throughput | Administrator, Editor, Manager, Monitor, Operator, Viewer |
| `cloudantnosqldb.capacity-throughput.write` | Update provisioned throughput capacity | Administrator, Editor, Manager |
| `cloudantnosqldb.current-throughput.read` | Read current request throughput | Manager, Monitor |
| `cloudantnosqldb.limits-throughput.read` | Read throughput limits for current Plan | Manager |
| `cloudantnosqldb.account-all-dbs.read` | List all databases | Manager, Monitor, Reader, Writer |
| `cloudantnosqldb.account-deleted-dbs.list` | List deleted databases | Manager, Monitor |
| `cloudantnosqldb.account-deleted-dbs.restore` | Restore deleted database | Manager |
| `cloudantnosqldb.account-deleted-dbs.delete` | Delete deleted database | Manager |
| `cloudantnosqldb.account-meta-info.read` | View account metadata | Manager, Monitor, Reader, Writer |
| `cloudantnosqldb.database-ensure-full-commit.execute` | Call _ensure_full_commit endpoint | Checkpointer, Manager, Writer |
| `cloudantnosqldb.account-search-analyze.execute` | Call _search_analyze endpoint | Manager, Reader, Writer |
| `cloudantnosqldb.couchdbextension-instance.read` | View metadata of an Extension for Apache CouchDB instance | Manager |
| `cloudantnosqldb.couchdbextension-instance.write` | Make changes to an Extension for Apache CouchDB instance | Manager |
| `cloudantnosqldb.legacy-root-credential.revoke` | Revoke legacy credential tied to your instance URL | Administrator, Manager |
| `cloudantnosqldb.legacy-credentials.revoke` | Migrate instance to IAM only  | Administrator, Manager |
{: caption="Table 16. Service actions - Cloudant" caption-side="top"}
{: #actions-table16}
{: tab-title="Actions"}
{: tab-group="cloudantnosqldb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Certificate Manager
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cloudcerts` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 17. Service roles - Certificate Manager" caption-side="top"}
{: #service-roles-table17}
{: tab-title="Service roles"}
{: tab-group="cloudcerts"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `cloudcerts.certificate.import` | Re/Import a certificate and its private key. | Manager |
| `cloudcerts.certificate.delete` | Delete a certificate | Manager |
| `cloudcerts.certificate.read` | Retrieve a certificate, its private key, and its intermediate certificate if present | Manager, Writer |
| `cloudcerts.certificate.update` | Update the name and description of a certificate | Manager, Writer |
| `cloudcerts.certificates.list` | Retrieve a list of all certificates and their associated metadata or perform a search for certificates | Manager, Reader, Writer |
| `cloudcerts.notifications.publickey` | Retrieve the public key for Callback URL notifications | Manager, Reader, Writer |
| `cloudcerts.certificate.order` | Order/Renew a certificate | Manager |
| `cloudcerts.certificate-metadata.read` | Retrieve the metadata of a certificate | Manager, Reader, Writer |
| `cloudcerts.notifications-channel.update` | Update the endpoint or state of a notification channel | Manager |
| `cloudcerts.notifications-channel.list` | Retrieve all notification channels | Manager, Reader, Writer |
| `cloudcerts.notifications-channel.delete` | Delete a notification channel | Manager |
| `cloudcerts.notifications-channel.test` | Test a notification channel | Manager, Reader, Writer |
| `cloudcerts.notifications-channel.create` | Create a new notification channel. | Manager |
{: caption="Table 17. Service actions - Certificate Manager" caption-side="top"}
{: #actions-table17}
{: tab-title="Actions"}
{: tab-group="cloudcerts"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Cloud Shell
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cloudshell` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 18. Platform roles - IBM Cloud Shell" caption-side="top"}
{: #platform-roles-table18}
{: tab-title="Platform roles"}
{: tab-group="cloudshell"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Cloud Developer | As a cloud developer, you can create Cloud Shell environments to manage IBM Cloud resources and develop applications for IBM Cloud (Web Preview enabled). |
| Cloud Operator | As a cloud operator, you can create Cloud Shell environments to manage IBM Cloud resources. |
| File Manager | As a file manager, you can create Cloud Shell environments to manage IBM Cloud resources and manage files in your workspace (File Upload and File Download enabled). |
{: row-headers}
{: caption="Table 18. Service roles - IBM Cloud Shell" caption-side="top"}
{: #service-roles-table18}
{: tab-title="Service roles"}
{: tab-group="cloudshell"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `cloudshell.account-settings.update` | The ability to update Cloud Shell account settings. | Administrator |
| `cloudshell.server.create` | The ability to create Cloud Shell environments. | Administrator, Cloud Developer, Cloud Operator, File Manager |
| `cloudshell.server.preview-web` | The ability to preview web applications in Cloud Shell (Web Preview enabled). | Administrator, Cloud Developer |
| `cloudshell.server.manage-file` | The ability to manage files in the Cloud Shell workspace (File Upload and File Download enabled). | Administrator, File Manager |
{: caption="Table 18. Service actions - IBM Cloud Shell" caption-side="top"}
{: #actions-table18}
{: tab-title="Actions"}
{: tab-group="cloudshell"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Code Engine
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `codeengine` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 19. Platform roles - Code Engine" caption-side="top"}
{: #platform-roles-table19}
{: tab-title="Platform roles"}
{: tab-group="codeengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 19. Service roles - Code Engine" caption-side="top"}
{: #service-roles-table19}
{: tab-title="Service roles"}
{: tab-group="codeengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `codeengine.dashboard.view` | View Dashboard | Administrator, Editor, Operator |
| `codeengine.tenant.read` | View project details | Manager, Reader, Writer |
| `codeengine.tenant.entities.create` | Create project contents, such as applications, job definitions, and jobs | Manager, Writer |
| `codeengine.tenant.entities.update` | Modify existing items already contained by a project, such as applications, jobs, or job definitions.  This does not include the ability to create or delete these items. | Manager, Writer |
| `codeengine.tenant.entities.delete` | Delete existing items from within a project | Manager, Writer |
| `codeengine.tenant.entities.read` | List and view existing items within a project | Manager, Reader, Writer |
{: caption="Table 19. Service actions - Code Engine" caption-side="top"}
{: #actions-table19}
{: tab-title="Actions"}
{: tab-group="codeengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Cloud Compliance and Security Center
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `compliance` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 20. Platform roles - IBM Cloud Compliance and Security Center" caption-side="top"}
{: #platform-roles-table20}
{: tab-title="Platform roles"}
{: tab-group="compliance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 20. Service roles - IBM Cloud Compliance and Security Center" caption-side="top"}
{: #service-roles-table20}
{: tab-title="Service roles"}
{: tab-group="compliance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `compliance.posture-management.dashboard-view` | Access the Security and Compliance dashboard to view security and compliance posture and results. | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.controls-create` | Add a control to a profile. | Administrator, Editor |
| `compliance.posture-management.controls-read` | View the controls that you can add to a profile. | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.controls-update` | Update an existing control. | Administrator, Editor |
| `compliance.posture-management.controls-delete` | Delete a control. | Administrator, Editor |
| `compliance.posture-management.scopes-create` | Create a scope. | Administrator, Editor |
| `compliance.posture-management.scopes-update` | Edit a scope. | Administrator, Editor |
| `compliance.posture-management.scopes-read` | View scopes. | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.scopes-delete` | Delete a scope. | Administrator, Editor |
| `compliance.posture-management.credentials-create` | Create a credential. | Administrator, Editor |
| `compliance.posture-management.credentials-update` | Update a credential. | Administrator, Editor |
| `compliance.posture-management.credentials-read` | View credentials. | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.credentials-delete` | Delete a credential. | Administrator, Editor |
| `compliance.posture-management.credentialsmap-create` | Map credentials to a scope. | Administrator, Editor |
| `compliance.posture-management.credentialsmap-update` | Edit an existing credentials mapping. | Administrator, Editor |
| `compliance.posture-management.credentialsmap-read` | View credentials mappings. | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.credentialsmap-delete` | Delete a credentials mapping. | Administrator, Editor |
| `compliance.posture-management.profiles-create` | Create a profile. | Administrator, Editor |
| `compliance.posture-management.profiles-update` | Update a profile. | Administrator, Editor |
| `compliance.posture-management.profiles-read` | View profiles. | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.profiles-delete` | Delete a profile. | Administrator, Editor |
| `compliance.posture-management.validations-create` | Run a vallidation scan. | Administrator, Editor |
| `compliance.posture-management.validations-update` | Update a validation scan. | Administrator, Editor |
| `compliance.posture-management.validations-read` | View a validation scan. | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.validations-delete` | Delete a validation scan. | Administrator, Editor |
| `compliance.posture-management.collectors-create` | Create a collector. | Administrator, Editor |
| `compliance.posture-management.collectors-update` | Update a collector. | Administrator, Editor |
| `compliance.posture-management.collectors-read` | View collectors. | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.collectors-delete` | Delete a collector. | Administrator, Editor |
| `compliance.posture-management.values-create` | Add parameters to an existing goal. | Administrator, Editor |
| `compliance.posture-management.values-update` | Update the parameters of an existing goal. | Administrator, Editor |
| `compliance.posture-management.values-read` | View the parameters that are associated with a goal. | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.tenants-create` |  Create tenants | Administrator, Editor |
| `compliance.posture-management.tenants-update` |  Update tenants  | Administrator, Editor |
| `compliance.posture-management.tenants-read` | View tenants  | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.tenants-delete` | Delete tenants | Administrator, Editor |
| `compliance.posture-management.events-create` | Create an audit log for monitoring compliance activity. | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.events-view` | View audit logs. | Administrator, Editor, Operator, Viewer |
| `compliance.configuration-governance.rules-create` | Create a config rule. | Administrator, Editor |
| `compliance.configuration-governance.rules-read` | View the config rules that are available for your accounts. | Administrator, Editor, Operator, Viewer |
| `compliance.configuration-governance.rules-update` | Update an existing config rule. | Administrator, Editor |
| `compliance.configuration-governance.rules-delete` | Delete a config rule. | Administrator, Editor |
| `compliance.configuration-governance.templates-create` | Create a template. | Administrator, Editor |
| `compliance.configuration-governance.templates-read` | View the templates that are available for your accounts. | Administrator, Editor, Operator, Viewer |
| `compliance.configuration-governance.templates-update` | Update an existing template. | Administrator, Editor |
| `compliance.configuration-governance.templates-delete` | Delete a template. | Administrator, Editor |
| `compliance.configuration-governance.attachments-create` | Create an attachment between a rule and a scope. | Administrator, Editor |
| `compliance.configuration-governance.attachments-read` | View the attachments that are associated with a rule. | Administrator, Editor, Operator, Viewer |
| `compliance.configuration-governance.attachments-update` | Update a rule attachment. | Administrator, Editor |
| `compliance.configuration-governance.attachments-delete` | Delete a rule attachment. | Administrator, Editor |
| `compliance.configuration-governance.services-create` | Create a definition to enable a service for configuration governance. | Administrator, Editor |
| `compliance.configuration-governance.services-update` | Update an existing service definition. | Administrator, Editor |
| `compliance.configuration-governance.services-delete` | Delete a service definition. | Administrator, Editor |
| `compliance.configuration-governance.config-state-create` | Create configuration governance config state. | Administrator, Editor |
| `compliance.configuration-governance.config-state-read` | Read configuration governance config state. | Administrator, Editor, Operator, Viewer |
| `compliance.configuration-governance.config-state-update` | Update configuration governance config state. | Administrator, Editor |
| `compliance.configuration-governance.config-state-delete` | Delete configuration governance config state. | Administrator, Editor |
| `compliance.configuration-governance.results-create` | Create configuration governance results. | Administrator, Editor |
| `compliance.configuration-governance.results-read` | Read configuration governance results. | Administrator, Editor, Operator, Viewer |
| `compliance.configuration-governance.results-update` | Update configuration governance results. | Administrator, Editor |
| `compliance.configuration-governance.results-delete` | Delete configuration governance results. | Administrator, Editor |
| `compliance.posture-management.tags-create` | Create tags. | Administrator, Editor, Operator |
| `compliance.posture-management.tags-update` | Update tags. | Administrator, Editor, Operator |
| `compliance.posture-management.tags-delete` | Delete a tag. | Administrator, Editor, Operator |
| `compliance.posture-management.tags-read` | View tags. | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.keys-read` | Read BYOK/KYOK configuration | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.keys-write` | Edit BYOK/KYOK configuration | Administrator, Editor |
| `compliance.posture-management.keys-delete` | Enable/Disable BYOK configuration | Administrator, Editor |
| `compliance.admin.settings-read` | View Admin Settings | Administrator, Editor, Operator, Viewer |
| `compliance.admin.settings-update` | Edit Admin Settings | Administrator |
| `compliance.admin.test-event-send` | Send test events | Administrator |
| `compliance.platform.notifications.write` | To send platform notifications  | Manager, Reader, Writer |
| `compliance.posture-management.integrations-read` | Read compliance posture management integrations | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.integrations-create` | Create compliance posture management integrations | Administrator, Editor, Operator |
| `compliance.posture-management.integrations-update` | Update compliance posture management integrations | Administrator, Editor, Operator |
| `compliance.posture-management.integrations-delete` | Delete compliance posture management integrations | Administrator, Editor |
{: caption="Table 20. Service actions - IBM Cloud Compliance and Security Center" caption-side="top"}
{: #actions-table20}
{: tab-title="Actions"}
{: tab-group="compliance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Consult with IBM Cloud Garage
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `consult-with-icg-wes` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 21. Platform roles - Consult with IBM Cloud Garage" caption-side="top"}
{: #platform-roles-table21}
{: tab-title="Platform roles"}
{: tab-group="consult-with-icg-wes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 21. Service roles - Consult with IBM Cloud Garage" caption-side="top"}
{: #service-roles-table21}
{: tab-title="Service roles"}
{: tab-group="consult-with-icg-wes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `consult-with-icg-wes.dashboard.view` | The ability to view your provisioned Consult with IBM Garage services in the dashboard. | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
{: caption="Table 21. Service actions - Consult with IBM Cloud Garage" caption-side="top"}
{: #actions-table21}
{: tab-title="Actions"}
{: tab-group="consult-with-icg-wes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Container Registry
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `container-registry` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 22. Service roles - Container Registry" caption-side="top"}
{: #service-roles-table22}
{: tab-title="Service roles"}
{: tab-group="container-registry"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `container-registry.exemption.manager` | Create an exemption for a security issue. Delete an exemption for a security issue. | Manager |
| `container-registry.image.push` | Push a container image. Sign a container image. Import IBM software that is downloaded from IBM Passport Advantage Online. Restore a deleted container image from the trash. Create a new container image that refers to a source image. | Manager, Writer |
| `container-registry.image.pull` | Pull a container image. Inspect the signature for a container image. Create a new image that refers to a source image. | Manager, Reader, Writer |
| `container-registry.namespace.create` | Add a namespace. | Manager |
| `container-registry.namespace.delete` | Remove a namespace. | Manager |
| `container-registry.image.delete` | Delete one or more container images. Remove a tag, or tags, from each specified container image in IBM Cloud Container Registry. Delete the signature for a container image. Clean up your namespaces by retaining only images that meet your criteria. Set a policy to clean up your namespaces by retaining only container images that meet your criteria. | Manager, Writer |
| `container-registry.namespace.list` | List your namespaces. | Manager, Reader |
| `container-registry.image.list` | List your container images. Display the container images that are in the trash. | Manager, Reader |
| `container-registry.image.vulnerabilities` | View a vulnerability assessment report for your container image. | Manager, Reader |
| `container-registry.image.inspect` | Display details about a specific container image. | Manager, Reader |
| `container-registry.quota.get` | Display your current quotas for traffic and storage, and usage information against those quotas. | Manager, Reader, Writer |
| `container-registry.quota.set` | Modify the specified quota. | Manager |
| `container-registry.plan.get` | Display your pricing plan. | Manager |
| `container-registry.plan.set` | Upgrade to the standard plan. | Manager |
| `container-registry.auth.get` | Get Auth Configuration, such as whether IAM policy enforcement is enabled | Manager, Reader, Writer |
| `container-registry.auth.set` | Enable IAM policy enforcement. | Manager |
| `container-registry.retention.analyze` | Clean up your namespaces by retaining only container images that meet your criteria. Set a policy to clean up your namespaces by retaining only container images that meet your criteria. | Manager, Reader |
| `container-registry.retention.get` | Get an image retention policy. | Manager, Reader |
| `container-registry.retention.set` | Set a policy to clean up your namespaces by retaining only container images that meet your criteria. | Manager, Writer |
| `container-registry.retention.list` | List the image retention policies for your account. | Manager, Reader |
| `container-registry.exemption.list` | List your exemptions for security issues.  List the types of security issues that you can exempt. | Manager, Reader |
| `container-registry.settings.get` | Get Account Settings, such as whether platform metrics are enabled | Manager, Reader, Writer |
| `container-registry.settings.set` | Set Account Settings, such as whether platform metrics are enabled | Manager |
{: caption="Table 22. Service actions - Container Registry" caption-side="top"}
{: #actions-table22}
{: tab-title="Actions"}
{: tab-group="container-registry"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Kubernetes Service
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `containers-kubernetes` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 23. Platform roles - Kubernetes Service" caption-side="top"}
{: #platform-roles-table23}
{: tab-title="Platform roles"}
{: tab-group="containers-kubernetes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 23. Service roles - Kubernetes Service" caption-side="top"}
{: #service-roles-table23}
{: tab-title="Service roles"}
{: tab-group="containers-kubernetes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `containers-kubernetes.cluster.create` | Users such as cluster or account administrators can create and delete clusters or set up cluster-wide features like service endpoints or managed add-ons. | Administrator |
| `containers-kubernetes.cluster.read` | Users such as auditors or billing can see cluster details but not modify the infrastructure. | Administrator, Editor, Operator, Viewer |
| `containers-kubernetes.cluster.operate` | Users such as reliability or DevOps engineers can add worker nodes and troubleshoot infrastructure such as reloading a worker node. They cannot create, delete, change credentials, or set up cluster-wide features. | Administrator, Operator |
| `containers-kubernetes.cluster.update` | Users such as developers can bind service, work with Ingress resources, and set up log forwarding for their apps but cannot modify the infrastructure. | Administrator, Editor |
| `containers-kubernetes.kube.read` | Users get read access to most Kubernetes resources in the namespace, but not to certain resources like roles, role bindings, or secrets. Corresponds to the RBAC view cluster role, which can be scoped to a namespace. | Reader |
| `containers-kubernetes.kube.write` | Users get read and write access to most Kubernetes resources in the namespace, but not to certain resources like roles or role bindings. Corresponds to the RBAC edit cluster role, which can be scoped to a namespace. | Writer |
| `containers-kubernetes.kube.manage` | When scoped to one namespace: Users can read and write to all Kubernetes resources in the namespace, but not to objects that apply across namespaces, the namespace resource quota, or the namespace itself. Corresponds to the RBAC admin cluster role to that namespace. When scoped to all namespaces in the cluster (by leaving the previous namespace field empty): Users can read and write to all Kubernetes resources in all namespaces in the cluster and work with objects that apply across namespaces, like top pods, top nodes, or creating an Ingress resource to make apps publicly available. Corresponds to the RBAC cluster-admin cluster role. | Manager |
{: caption="Table 23. Service actions - Kubernetes Service" caption-side="top"}
{: #actions-table23}
{: tab-title="Actions"}
{: tab-group="containers-kubernetes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Context-Based Restrictions
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `context-based-restrictions` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 24. Platform roles - Context-Based Restrictions" caption-side="top"}
{: #platform-roles-table24}
{: tab-title="Platform roles"}
{: tab-group="context-based-restrictions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `context-based-restrictions.zone.create` | Network Zone Create | Administrator, Editor |
| `context-based-restrictions.zone.read` | Network Zone Read | Administrator, Editor, Viewer |
| `context-based-restrictions.zone.update` | Network Zone Update | Administrator, Editor |
| `context-based-restrictions.zone.delete` | Network Zone Delete | Administrator, Editor |
| `context-based-restrictions.account-settings.read` | View context-based restriction account settings | Administrator, Editor, Viewer |
| `context-based-restrictions.account-settings.update` | Update context-based restriction account settings | Administrator |
{: caption="Table 24. Service actions - Context-Based Restrictions" caption-side="top"}
{: #actions-table24}
{: tab-title="Actions"}
{: tab-group="context-based-restrictions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Continuous Delivery
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `continuous-delivery` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can modify the Authorized Users list. |
| Editor | As an editor, you can create, view, update, change the plan for, and delete instances of the Continuous Delivery service. |
| Operator | As an operator, you can view instances of the Continuous Delivery service. |
{: row-headers}
{: caption="Table 25. Platform roles - Continuous Delivery" caption-side="top"}
{: #platform-roles-table25}
{: tab-title="Platform roles"}
{: tab-group="continuous-delivery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 25. Service roles - Continuous Delivery" caption-side="top"}
{: #service-roles-table25}
{: tab-title="Service roles"}
{: tab-group="continuous-delivery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `continuous-delivery.dashboard.view` | View instances of the Continuous Delivery service. | Administrator, Editor, Operator |
| `continuous-delivery.instance.add-auth-users` | Add entries to the Authorized Users list on the Manage tab of a Continuous Delivery service instance. | Administrator, Manager, Writer |
| `continuous-delivery.instance.remove-auth-users` | Remove entries from the Authorized Users list on the Manage tab of a Continuous Delivery service instance. | Administrator, Manager, Writer |
| `continuous-delivery.instance.config-auth-users` | Configure authorized users. | Administrator, Manager |
{: caption="Table 25. Service actions - Continuous Delivery" caption-side="top"}
{: #actions-table25}
{: tab-title="Actions"}
{: tab-group="continuous-delivery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Watson Assistant
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `conversation` for the service name.

| Role | Description |
| ----- | :----- |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 26. Platform roles - Watson Assistant" caption-side="top"}
{: #platform-roles-table26}
{: tab-title="Platform roles"}
{: tab-group="conversation"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 26. Service roles - Watson Assistant" caption-side="top"}
{: #service-roles-table26}
{: tab-title="Service roles"}
{: tab-group="conversation"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /conversation` | Can use API endpoints to extract data from skills and assistants | Manager, Reader, Writer |
| `POST /conversation` | Can use API endpoints to create data & to use the message endpoint | Manager, Reader, Writer |
| `DELETE /conversation` | Can use API endpoints to delete data from skills and assistant | Manager, Reader, Writer |
| `PATCH /conversation` | Can use API endpoint to modify data from skills and assistant | Manager, Reader, Writer |
| `PUT /conversation` | Can use API endpoint to modify data from skills and assistant | Manager, Reader, Writer |
| `conversation.assistant.legacy` | Can perform authoring methods for a workspace through v1 APIs. | Manager |
| `conversation.skill.write` | Can rename, edit, or delete a skill. | Manager, Writer |
| `conversation.skill.read` | Can open and view a skill. | Manager, Reader, Writer |
| `conversation.assistant.write` | Can rename, edit, or delete an assistant. | Manager, Writer |
| `conversation.assistant.read` | Can open and view an assistant. | Manager, Reader, Writer |
| `conversation.logs.read` | Can view skill analytics and access user conversation logs. | Manager |
| `conversation.assistant.list` | Can list assistant or skill | Manager, Reader, Viewer, Writer |
| `conversation.assistant.default` | Default access for Assistant | Manager, Reader, Viewer, Writer |
{: caption="Table 26. Service actions - Watson Assistant" caption-side="top"}
{: #actions-table26}
{: tab-title="Actions"}
{: tab-group="conversation"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Cloud Pak for Data
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cp4d` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 27. Platform roles - IBM Cloud Pak for Data" caption-side="top"}
{: #platform-roles-table27}
{: tab-title="Platform roles"}
{: tab-group="cp4d"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| CloudPak Data Engineer | CloudPak Data Engineer |
| CloudPak Data Scientist | CloudPak Data Scientist |
| CloudPak Data Steward | CloudPak Data Steward |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reporting Administrator | Reporting Administrator |
{: row-headers}
{: caption="Table 27. Service roles - IBM Cloud Pak for Data" caption-side="top"}
{: #service-roles-table27}
{: tab-title="Service roles"}
{: tab-group="cp4d"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `cp4d.catalog.manage` | Manage catalogs
 | Administrator, Editor, Manager |
| `cp4d.governance-categories.manage` | Manage governance categories
 | Manager |
| `cp4d.governance-workflows.manage` | Manage governance workflows
 | Manager |
| `cp4d.wkc.reporting.manage` | Manage reporting | Reporting Administrator |
| `cp4d.governance-artifacts.access` | Access governance artifacts | CloudPak Data Engineer, CloudPak Data Scientist, CloudPak Data Steward |
| `cp4d.catalog.access` | Access catalogs | CloudPak Data Scientist, CloudPak Data Steward, Manager |
| `cp4d.data-protection-rules.manage` | Manage data protection rules | CloudPak Data Engineer, CloudPak Data Steward, Manager |
| `cp4d.glossary.manage` | Perform business glossary administrative tasks | Manager |
{: caption="Table 27. Service actions - IBM Cloud Pak for Data" caption-side="top"}
{: #actions-table27}
{: tab-title="Actions"}
{: tab-group="cp4d"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Db2 Warehouse
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `dashdb` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 28. Service roles - Db2 Warehouse" caption-side="top"}
{: #service-roles-table28}
{: tab-title="Service roles"}
{: tab-group="dashdb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `dashdb.console.access` |  | Manager, Writer |
{: caption="Table 28. Service actions - Db2 Warehouse" caption-side="top"}
{: #actions-table28}
{: tab-title="Actions"}
{: tab-group="dashdb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Db2 on Cloud
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `dashdb-for-transactions` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 29. Platform roles - Db2 on Cloud" caption-side="top"}
{: #platform-roles-table29}
{: tab-title="Platform roles"}
{: tab-group="dashdb-for-transactions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
{: row-headers}
{: caption="Table 29. Service roles - Db2 on Cloud" caption-side="top"}
{: #service-roles-table29}
{: tab-title="Service roles"}
{: tab-group="dashdb-for-transactions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `dashdb-for-transactions.console.access` | Allows users to view the Db2 Console. | Manager |
| `dashdb-for-transactions.console.manage-users` | Allows management of users for database access such as creating new users or assign and IAM user or service id to a database user. | Administrator, Manager |
| `dashdb-for-transactions.console.monitor` | Allows viewing of metrics and information that allow you to understand the resources your database is using or workload it is running. | Administrator, Editor, Operator, Viewer |
| `dashdb-for-transactions.console.clone` | clone operation | Administrator, Editor |
| `dashdb-for-transactions.console.scale` | scale operation | Administrator, Editor, Operator |
| `dashdb-for-transactions.console.backup` | backup operation | Administrator, Editor, Operator |
| `dashdb-for-transactions.console.restore` | restore operation | Administrator, Editor, Operator |
| `dashdb-for-transactions.console.settings` | set configuration | Administrator, Editor, Operator |
| `dashdb-for-transactions.console.view-settings` | view database settings | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a backup | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration` | Get deployment configuration | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id` | Update a group | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/users` | Create a Db2 database user | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id` | Read a Db2 database user | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id` | Update a Db2 database user | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/users/:user_id` | Remove a Db2 database user | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connection | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connection | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read whitelisted IP addresses | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create whitelisted IP addresses | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a whitelisted IP address | Administrator, Editor, Operator |
| `PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk add whitelist IP addresses | Administrator, Editor, Operator |
| `GET /2017-12/:platform/tasks/:task_id` | Read a task | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/backups/:backup_id` | Read a backup | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id` | Read a deployment | Administrator, Editor, Operator, Viewer |
| `DELETE /2017-12/:platform/deployments/:deployment_id` | Remove a deployment | Administrator, Editor, Operator |
| `GET /2017-12/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /2017-12/:platform/clusters/:cluster_id/deployments` | Create a deployment | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/inplace_restores` | Perform in place database restore | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/member` | Update scaling member configuration | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id/adminpassword` | Update admin password | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id/locked` | Update user locked state | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/describe_updates` | Get db updates | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/db_updates` | Create db update | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id/password` | Update password | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/billable` | Set billable annotation to true | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/migrated` | Set migration flag to false | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/check_updates` | Check deployment for available updates | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/dr_take_over` | dr_take_over | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/get_dr` | get_dr | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/resyncs` | resyncs | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration` | Get deployment configuration | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/regions` | Read discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/task_infos/:task_id` | Read a Task metadata | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id` | Read a backup | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/task_infos` | Read all deployment tasks metadata | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `DELETE /v5/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id` | Update a group | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/users` | Create a Db2 database user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_id` | Read a Db2 database user | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_id` | Update a Db2 database user | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/users/:user_id` | Remove a Db2 database user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connection | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connection | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read whitelisted IP addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create whitelisted IP addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a whitelisted IP address | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk add whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/inplace_restores` | Perform in place database restore | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/member` | Update scaling member configuration | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_id/adminpassword` | Update admin password | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_id/locked` | Update user locked state | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/describe_updates` | Get db updates | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/db_updates` | Create db update | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_id/password` | Update password | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/check_updates` | Check deployment for available updates | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/billable` | Set billable annotation to true | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/migrated` | Set migration flag to false | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/dr_take_over` | dr_take_over | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/get_dr` | get_dr | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/resyncs` | resyncs | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/configure_sets` | Configures db2set parameters | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/configure_sets` | Configures db2set parameters | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/configure_sets` | Retrieves configured parameters | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/configure_sets` | Retrieves configured parameters | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/task_infos` | Read all deployment tasks metadata | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/task_infos/:task_id` | Read a Task metadata
 | Administrator, Editor, Operator, Viewer |
{: caption="Table 29. Service actions - Db2 on Cloud" caption-side="top"}
{: #actions-table29}
{: tab-title="Actions"}
{: tab-group="dashdb-for-transactions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Data Replication on Cloud
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `data-replication` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 30. Platform roles - IBM Data Replication on Cloud" caption-side="top"}
{: #platform-roles-table30}
{: tab-title="Platform roles"}
{: tab-group="data-replication"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 30. Service roles - IBM Data Replication on Cloud" caption-side="top"}
{: #service-roles-table30}
{: tab-title="Service roles"}
{: tab-group="data-replication"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `data-replication.replications.retrieve` | data-replication.replications.retrieve | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `data-replication.replications.create` | Create replication | Manager, Writer |
| `data-replication.replications.operate` | Operate Replication | Manager, Writer |
| `data-replication.replications.delete` | Delete Replication | Manager, Writer |
| `data-replication.replications.update` | Update Replication | Manager, Writer |
{: caption="Table 30. Service actions - IBM Data Replication on Cloud" caption-side="top"}
{: #actions-table30}
{: tab-title="Actions"}
{: tab-group="data-replication"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Watson Studio
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `data-science-experience` for the service name.

No supported roles.
## Data Shield
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `data-shield` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 32. Platform roles - Data Shield" caption-side="top"}
{: #platform-roles-table32}
{: tab-title="Platform roles"}
{: tab-group="data-shield"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `data-shield.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 32. Service actions - Data Shield" caption-side="top"}
{: #actions-table32}
{: tab-title="Actions"}
{: tab-group="data-shield"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Data Store for Memcache
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `data-store-for-memcache` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
{: row-headers}
{: caption="Table 33. Platform roles - Data Store for Memcache" caption-side="top"}
{: #platform-roles-table33}
{: tab-title="Platform roles"}
{: tab-group="data-store-for-memcache"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | null |
| Reader | null |
| Writer | null |
{: row-headers}
{: caption="Table 33. Service roles - Data Store for Memcache" caption-side="top"}
{: #service-roles-table33}
{: tab-title="Service roles"}
{: tab-group="data-store-for-memcache"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `data-store-for-memcache.keys.create` |  | Administrator, Manager |
| `data-store-for-memcache.keys.read` |  | Manager, Reader, Writer |
| `data-store-for-memcache.keys.update` |  | Manager, Writer |
| `data-store-for-memcache.keys.delete` |  | Manager |
| `data-store-for-memcache.keys.encode` |  | Manager, Writer |
| `data-store-for-memcache.keys.decode` |  | Manager, Writer |
{: caption="Table 33. Service actions - Data Store for Memcache" caption-side="top"}
{: #actions-table33}
{: tab-title="Actions"}
{: tab-group="data-store-for-memcache"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Data Virtualization
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `data-virtualization` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 34. Platform roles - Data Virtualization" caption-side="top"}
{: #platform-roles-table34}
{: tab-title="Platform roles"}
{: tab-group="data-virtualization"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| DataAccess (For Service to Service Authorization Only) | Used for Service to Service authorization.  Do not choose this role for service credential generation. |
| Manager (For generated service credentials only) | This role is only enabled for generated service credentials.  Using this role will grant the generated Service ID Manager access. |
{: row-headers}
{: caption="Table 34. Service roles - Data Virtualization" caption-side="top"}
{: #service-roles-table34}
{: tab-title="Service roles"}
{: tab-group="data-virtualization"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `data-virtualization.console.manage-users` | Allows management of users for database access such as creating new users or assign and IAM user or service id to a database user. | Administrator |
| `data-virtualization.console.monitor` | Allows viewing of metrics and information that allow you to understand the resources your database is using or workload it is running. | Administrator, Editor, Manager (For generated service credentials only), Operator, Viewer |
| `data-virtualization.data.access` | Allows data access for other services. | DataAccess (For Service to Service Authorization Only) |
| `data-virtualization.console.scale` | scale operation | Administrator, Editor, Manager (For generated service credentials only), Operator |
| `data-virtualization.console.backup` | backup operation | Administrator, Editor, Operator |
| `data-virtualization.console.restore` | restore operation | Administrator, Editor, Operator |
| `data-virtualization.console.settings` | set configuration | Administrator, Editor, Manager (For generated service credentials only), Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration` | Get deployment configuration | Administrator, Editor, Operator, Viewer |
| `data-virtualization.console.view-settings` | view database settings | Administrator, Editor, Manager (For generated service credentials only), Operator, Viewer |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a backup | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id` | Update a group | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/users` | Create a Data Virtualization database user | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id` | Read a Data Virtualization database user | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id` | Update a Data Virtualization database user | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/users/:user_id` | Remove a Data Virtualization database user | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connection | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connection | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read whitelisted IP addresses | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create whitelisted IP addresses | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a whitelisted IP address | Administrator, Editor, Operator |
| `PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk add whitelist IP addresses | Administrator, Editor, Operator |
| `GET /2017-12/:platform/tasks/:task_id` | Read a task | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/backups/:backup_id` | Read a backup | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id` | Read a deployment | Administrator, Editor, Operator, Viewer |
| `DELETE /2017-12/:platform/deployments/:deployment_id` | Remove a deployment | Administrator, Editor, Operator |
| `GET /2017-12/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /2017-12/:platform/clusters/:cluster_id/deployments` | Create a deployment | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/member` | Update scaling member configuration | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id/locked` | Update user locked state | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/describe_updates` | Get db updates | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/db_updates` | Create db update | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/check_updates` | Check deployment for available updates | Administrator, Editor, Operator, Viewer |
{: caption="Table 34. Service actions - Data Virtualization" caption-side="top"}
{: #actions-table34}
{: tab-title="Actions"}
{: tab-group="data-virtualization"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Netezza Performance Server
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `data-warehouse` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 35. Platform roles - Netezza Performance Server" caption-side="top"}
{: #platform-roles-table35}
{: tab-title="Platform roles"}
{: tab-group="data-warehouse"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 35. Service roles - Netezza Performance Server" caption-side="top"}
{: #service-roles-table35}
{: tab-title="Service roles"}
{: tab-group="data-warehouse"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `data-warehouse.dashboard.view` | The capability to view the service instance details page | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `data-warehouse.database.connect` | The  action describes who can connect to the database | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `data-warehouse.database.admin` | The role defines people with admin privileges on the database | Administrator, Manager |
{: caption="Table 35. Service actions - Netezza Performance Server" caption-side="top"}
{: #actions-table35}
{: tab-title="Actions"}
{: tab-group="data-warehouse"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Databases for DataStax
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-cassandra` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 36. Platform roles - Databases for DataStax" caption-side="top"}
{: #platform-roles-table36}
{: tab-title="Platform roles"}
{: tab-group="databases-for-cassandra"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /2017-12/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `DELETE /2017-12/:platform/deployments/:deployment_id` | Remove a Deployment | Administrator, Editor, Operator |
| `GET /2017-12/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /2017-12/:platform/clusters/:cluster_id/deployments` | Create a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/users` | Create a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id` | Read a DeploymentUser | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id` | Update a DeploymentUser | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/users/:user_id` | Remove a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v5/:platform/capability/:capability_id` | Discover a supported capability | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type` | Create a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Update a type of user | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Delete a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses/:ip_address_id` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `task.read` | Read a Task | Administrator, Editor, Operator, Viewer |
| `backup.read` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `deployment.read` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `deployment.update` | Update a Deployment | Administrator, Editor, Operator |
| `deployment-point-in-time-recovery-data.list` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `deployment-task.list` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `deployment-backup.list` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `deployment-backup.create` | Create an on-demand backup | Administrator, Editor, Operator |
| `deployment-remote.list` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `deployment-remote.update` | Update a remote replica | Administrator, Editor, Operator |
| `deployment-remote.create` | Promote a remote replica | Administrator, Editor, Operator |
| `deployment-remote-resync.create` | Resync remote replica | Administrator, Editor, Operator |
| `deployment-database-connection.bulkdelete` | Kill all database connections | Administrator, Editor, Operator |
| `deployment-configuration.update` | Update deployment configuration | Administrator, Editor, Operator |
| `deployment-configuration-schema.read` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `deployment-network.read` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `deployment-group.list` | Read Groups | Administrator, Editor, Operator, Viewer |
| `deployment-group.update` | Update a Group | Administrator, Editor, Operator |
| `deployment-group-autoscaling.read` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `deployment-group-autoscaling.update` | Update autoscaling configuration | Administrator, Editor, Operator |
| `capability.create` | Discover a supported capability | Administrator, Editor, Operator |
| `deployment-user.create` | Create a type of user | Administrator, Editor, Operator |
| `deployment-user.read` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `deployment-user.update` | Update a type of user | Administrator, Editor, Operator |
| `deployment-user.delete` | Delete a type of user | Administrator, Editor, Operator |
| `deployment-user-connection.list` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-user-connection.create` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.list` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.create` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-ip-address.delete` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-allowlist-ip-addresses.update` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `deployment-capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
| `capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
{: caption="Table 36. Service actions - Databases for DataStax" caption-side="top"}
{: #actions-table36}
{: tab-title="Actions"}
{: tab-group="databases-for-cassandra"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Databases for Elasticsearch
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-elasticsearch` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 37. Platform roles - Databases for Elasticsearch" caption-side="top"}
{: #platform-roles-table37}
{: tab-title="Platform roles"}
{: tab-group="databases-for-elasticsearch"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /2017-12/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `DELETE /2017-12/:platform/deployments/:deployment_id` | Remove a Deployment | Administrator, Editor, Operator |
| `GET /2017-12/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /2017-12/:platform/clusters/:cluster_id/deployments` | Create a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/users` | Create a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id` | Read a DeploymentUser | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id` | Update a DeploymentUser | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/users/:user_id` | Remove a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/elasticsearch/file_syncs` | Create elasticsearch file sync | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/elasticsearch/file_syncs` | Create elasticsearch file sync | Administrator, Editor, Operator |
| `POST /v5/:platform/capability/:capability_id` | Discover a supported capability | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type` | Create a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Update a type of user | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Delete a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses/:ip_address_id` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `task.read` | Read a Task | Administrator, Editor, Operator, Viewer |
| `backup.read` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `deployment.read` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `deployment.update` | Update a Deployment | Administrator, Editor, Operator |
| `deployment-point-in-time-recovery-data.list` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `deployment-task.list` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `deployment-backup.list` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `deployment-backup.create` | Create an on-demand backup | Administrator, Editor, Operator |
| `deployment-remote.list` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `deployment-remote.update` | Update a remote replica | Administrator, Editor, Operator |
| `deployment-remote.create` | Promote a remote replica | Administrator, Editor, Operator |
| `deployment-remote-resync.create` | Resync remote replica | Administrator, Editor, Operator |
| `deployment-database-connection.bulkdelete` | Kill all database connections | Administrator, Editor, Operator |
| `deployment-configuration.update` | Update deployment configuration | Administrator, Editor, Operator |
| `deployment-configuration-schema.read` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `deployment-network.read` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `deployment-group.list` | Read Groups | Administrator, Editor, Operator, Viewer |
| `deployment-group.update` | Update a Group | Administrator, Editor, Operator |
| `deployment-group-autoscaling.read` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `deployment-group-autoscaling.update` | Update autoscaling configuration | Administrator, Editor, Operator |
| `deployment-elasticsearch-file-syncs.create` | Create elasticsearch file sync | Administrator, Editor, Operator |
| `capability.create` | Discover a supported capability | Administrator, Editor, Operator |
| `deployment-user.create` | Create a type of user | Administrator, Editor, Operator |
| `deployment-user.read` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `deployment-user.update` | Update a type of user | Administrator, Editor, Operator |
| `deployment-user.delete` | Delete a type of user | Administrator, Editor, Operator |
| `deployment-user-connection.list` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-user-connection.create` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.list` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.create` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-ip-address.delete` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-allowlist-ip-addresses.update` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `deployment-capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
| `capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
{: caption="Table 37. Service actions - Databases for Elasticsearch" caption-side="top"}
{: #actions-table37}
{: tab-title="Actions"}
{: tab-group="databases-for-elasticsearch"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Databases for EDB
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-enterprisedb` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 38. Platform roles - Databases for EDB" caption-side="top"}
{: #platform-roles-table38}
{: tab-title="Platform roles"}
{: tab-group="databases-for-enterprisedb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /2017-12/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `DELETE /2017-12/:platform/deployments/:deployment_id` | Remove a Deployment | Administrator, Editor, Operator |
| `GET /2017-12/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /2017-12/:platform/clusters/:cluster_id/deployments` | Create a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/users` | Create a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id` | Read a DeploymentUser | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id` | Update a DeploymentUser | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/users/:user_id` | Remove a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v5/:platform/capability/:capability_id` | Discover a supported capability | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type` | Create a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Update a type of user | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Delete a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses/:ip_address_id` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `databases-for-enterprisedb.emp.allow` | Allow access to EnterpriseDB Migration Portal | Administrator, Editor, Operator, Viewer |
| `task.read` | Read a Task | Administrator, Editor, Operator, Viewer |
| `backup.read` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `deployment.read` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `deployment.update` | Update a Deployment | Administrator, Editor, Operator |
| `deployment-point-in-time-recovery-data.list` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `deployment-task.list` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `deployment-backup.list` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `deployment-backup.create` | Create an on-demand backup | Administrator, Editor, Operator |
| `deployment-remote.list` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `deployment-remote.update` | Update a remote replica | Administrator, Editor, Operator |
| `deployment-remote.create` | Promote a remote replica | Administrator, Editor, Operator |
| `deployment-remote-resync.create` | Resync remote replica | Administrator, Editor, Operator |
| `deployment-database-connection.bulkdelete` | Kill all database connections | Administrator, Editor, Operator |
| `deployment-configuration.update` | Update deployment configuration | Administrator, Editor, Operator |
| `deployment-configuration-schema.read` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `deployment-network.read` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `deployment-group.list` | Read Groups | Administrator, Editor, Operator, Viewer |
| `deployment-group.update` | Update a Group | Administrator, Editor, Operator |
| `deployment-group-autoscaling.read` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `deployment-group-autoscaling.update` | Update autoscaling configuration | Administrator, Editor, Operator |
| `capability.create` | Discover a supported capability | Administrator, Editor, Operator |
| `deployment-user.create` | Create a type of user | Administrator, Editor, Operator |
| `deployment-user.read` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `deployment-user.update` | Update a type of user | Administrator, Editor, Operator |
| `deployment-user.delete` | Delete a type of user | Administrator, Editor, Operator |
| `deployment-user-connection.list` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-user-connection.create` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.list` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.create` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-ip-address.delete` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-allowlist-ip-addresses.update` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `deployment-capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
| `capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
{: caption="Table 38. Service actions - Databases for EDB" caption-side="top"}
{: #actions-table38}
{: tab-title="Actions"}
{: tab-group="databases-for-enterprisedb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Databases for etcd
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-etcd` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 39. Platform roles - Databases for etcd" caption-side="top"}
{: #platform-roles-table39}
{: tab-title="Platform roles"}
{: tab-group="databases-for-etcd"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /2017-12/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `DELETE /2017-12/:platform/deployments/:deployment_id` | Remove a Deployment | Administrator, Editor, Operator |
| `GET /2017-12/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /2017-12/:platform/clusters/:cluster_id/deployments` | Create a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/users` | Create a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id` | Read a DeploymentUser | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id` | Update a DeploymentUser | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/users/:user_id` | Remove a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v5/:platform/capability/:capability_id` | Discover a supported capability | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type` | Create a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Update a type of user | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Delete a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses/:ip_address_id` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `task.read` | Read a Task | Administrator, Editor, Operator, Viewer |
| `backup.read` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `deployment.read` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `deployment.update` | Update a Deployment | Administrator, Editor, Operator |
| `deployment-point-in-time-recovery-data.list` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `deployment-task.list` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `deployment-backup.list` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `deployment-backup.create` | Create an on-demand backup | Administrator, Editor, Operator |
| `deployment-remote.list` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `deployment-remote.update` | Update a remote replica | Administrator, Editor, Operator |
| `deployment-remote.create` | Promote a remote replica | Administrator, Editor, Operator |
| `deployment-remote-resync.create` | Resync remote replica | Administrator, Editor, Operator |
| `deployment-database-connection.bulkdelete` | Kill all database connections | Administrator, Editor, Operator |
| `deployment-configuration.update` | Update deployment configuration | Administrator, Editor, Operator |
| `deployment-configuration-schema.read` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `deployment-network.read` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `deployment-group.list` | Read Groups | Administrator, Editor, Operator, Viewer |
| `deployment-group.update` | Update a Group | Administrator, Editor, Operator |
| `deployment-group-autoscaling.read` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `deployment-group-autoscaling.update` | Update autoscaling configuration | Administrator, Editor, Operator |
| `capability.create` | Discover a supported capability | Administrator, Editor, Operator |
| `deployment-user.create` | Create a type of user | Administrator, Editor, Operator |
| `deployment-user.read` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `deployment-user.update` | Update a type of user | Administrator, Editor, Operator |
| `deployment-user.delete` | Delete a type of user | Administrator, Editor, Operator |
| `deployment-user-connection.list` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-user-connection.create` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.list` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.create` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-ip-address.delete` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-allowlist-ip-addresses.update` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `deployment-capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
| `capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
{: caption="Table 39. Service actions - Databases for etcd" caption-side="top"}
{: #actions-table39}
{: tab-title="Actions"}
{: tab-group="databases-for-etcd"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Databases for MongoDB
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-mongodb` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 40. Platform roles - Databases for MongoDB" caption-side="top"}
{: #platform-roles-table40}
{: tab-title="Platform roles"}
{: tab-group="databases-for-mongodb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /2017-12/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `DELETE /2017-12/:platform/deployments/:deployment_id` | Remove a Deployment | Administrator, Editor, Operator |
| `GET /2017-12/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /2017-12/:platform/clusters/:cluster_id/deployments` | Create a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/users` | Create a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id` | Read a DeploymentUser | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id` | Update a DeploymentUser | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/users/:user_id` | Remove a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v5/:platform/capability/:capability_id` | Discover a supported capability | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type` | Create a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Update a type of user | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Delete a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses/:ip_address_id` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `task.read` | Read a Task | Administrator, Editor, Operator, Viewer |
| `backup.read` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `deployment.read` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `deployment.update` | Update a Deployment | Administrator, Editor, Operator |
| `deployment-point-in-time-recovery-data.list` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `deployment-task.list` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `deployment-backup.list` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `deployment-backup.create` | Create an on-demand backup | Administrator, Editor, Operator |
| `deployment-remote.list` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `deployment-remote.update` | Update a remote replica | Administrator, Editor, Operator |
| `deployment-remote.create` | Promote a remote replica | Administrator, Editor, Operator |
| `deployment-remote-resync.create` | Resync remote replica | Administrator, Editor, Operator |
| `deployment-database-connection.bulkdelete` | Kill all database connections | Administrator, Editor, Operator |
| `deployment-configuration.update` | Update deployment configuration | Administrator, Editor, Operator |
| `deployment-configuration-schema.read` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `deployment-network.read` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `deployment-group.list` | Read Groups | Administrator, Editor, Operator, Viewer |
| `deployment-group.update` | Update a Group | Administrator, Editor, Operator |
| `deployment-group-autoscaling.read` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `deployment-group-autoscaling.update` | Update autoscaling configuration | Administrator, Editor, Operator |
| `capability.create` | Discover a supported capability | Administrator, Editor, Operator |
| `deployment-user.create` | Create a type of user | Administrator, Editor, Operator |
| `deployment-user.read` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `deployment-user.update` | Update a type of user | Administrator, Editor, Operator |
| `deployment-user.delete` | Delete a type of user | Administrator, Editor, Operator |
| `deployment-user-connection.list` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-user-connection.create` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.list` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.create` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-ip-address.delete` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-allowlist-ip-addresses.update` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `deployment-capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
| `capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
{: caption="Table 40. Service actions - Databases for MongoDB" caption-side="top"}
{: #actions-table40}
{: tab-title="Actions"}
{: tab-group="databases-for-mongodb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Databases for MySQL
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-mysql` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 41. Platform roles - Databases for MySQL" caption-side="top"}
{: #platform-roles-table41}
{: tab-title="Platform roles"}
{: tab-group="databases-for-mysql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /2017-12/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `DELETE /2017-12/:platform/deployments/:deployment_id` | Remove a Deployment | Administrator, Editor, Operator |
| `GET /2017-12/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /2017-12/:platform/clusters/:cluster_id/deployments` | Create a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/users` | Create a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id` | Read a DeploymentUser | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id` | Update a DeploymentUser | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/users/:user_id` | Remove a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v5/:platform/capability/:capability_id` | Discover a supported capability | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type` | Create a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Update a type of user | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Delete a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses/:ip_address_id` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `task.read` | Read a Task | Administrator, Editor, Operator, Viewer |
| `backup.read` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `deployment.read` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `deployment.update` | Update a Deployment | Administrator, Editor, Operator |
| `deployment-point-in-time-recovery-data.list` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `deployment-task.list` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `deployment-backup.list` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `deployment-backup.create` | Create an on-demand backup | Administrator, Editor, Operator |
| `deployment-remote.list` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `deployment-remote.update` | Update a remote replica | Administrator, Editor, Operator |
| `deployment-remote.create` | Promote a remote replica | Administrator, Editor, Operator |
| `deployment-remote-resync.create` | Resync remote replica | Administrator, Editor, Operator |
| `deployment-database-connection.bulkdelete` | Kill all database connections | Administrator, Editor, Operator |
| `deployment-configuration.update` | Update deployment configuration | Administrator, Editor, Operator |
| `deployment-configuration-schema.read` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `deployment-network.read` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `deployment-group.list` | Read Groups | Administrator, Editor, Operator, Viewer |
| `deployment-group.update` | Update a Group | Administrator, Editor, Operator |
| `deployment-group-autoscaling.read` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `deployment-group-autoscaling.update` | Update autoscaling configuration | Administrator, Editor, Operator |
| `capability.create` | Discover a supported capability | Administrator, Editor, Operator |
| `deployment-user.create` | Create a type of user | Administrator, Editor, Operator |
| `deployment-user.read` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `deployment-user.update` | Update a type of user | Administrator, Editor, Operator |
| `deployment-user.delete` | Delete a type of user | Administrator, Editor, Operator |
| `deployment-user-connection.list` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-user-connection.create` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.list` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.create` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-ip-address.delete` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-allowlist-ip-addresses.update` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `deployment-capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
| `capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
{: caption="Table 41. Service actions - Databases for MySQL" caption-side="top"}
{: #actions-table41}
{: tab-title="Actions"}
{: tab-group="databases-for-mysql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Databases for PostgreSQL
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-postgresql` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 42. Platform roles - Databases for PostgreSQL" caption-side="top"}
{: #platform-roles-table42}
{: tab-title="Platform roles"}
{: tab-group="databases-for-postgresql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /2017-12/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `DELETE /2017-12/:platform/deployments/:deployment_id` | Remove a Deployment | Administrator, Editor, Operator |
| `GET /2017-12/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /2017-12/:platform/clusters/:cluster_id/deployments` | Create a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/users` | Create a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id` | Read a DeploymentUser | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id` | Update a DeploymentUser | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/users/:user_id` | Remove a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/postgresql/logical_replication_slots` | Create postgresql logical replication slot | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/postgresql/logical_replication_slots/:name` | Delete postgresql logical replication slot | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/postgresql/logical_replication_slots` | Create postgresql logical replication slot | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/postgresql/logical_replication_slots/:name` | Delete postgresql logical replication slot | Administrator, Editor, Operator |
| `POST /v5/:platform/capability/:capability_id` | Discover a supported capability | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type` | Create a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Update a type of user | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Delete a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses/:ip_address_id` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `task.read` | Read a Task | Administrator, Editor, Operator, Viewer |
| `backup.read` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `deployment.read` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `deployment.update` | Update a Deployment | Administrator, Editor, Operator |
| `deployment-point-in-time-recovery-data.list` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `deployment-task.list` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `deployment-backup.list` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `deployment-backup.create` | Create an on-demand backup | Administrator, Editor, Operator |
| `deployment-remote.list` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `deployment-remote.update` | Update a remote replica | Administrator, Editor, Operator |
| `deployment-remote.create` | Promote a remote replica | Administrator, Editor, Operator |
| `deployment-remote-resync.create` | Resync remote replica | Administrator, Editor, Operator |
| `deployment-database-connection.bulkdelete` | Kill all database connections | Administrator, Editor, Operator |
| `deployment-configuration.update` | Update deployment configuration | Administrator, Editor, Operator |
| `deployment-configuration-schema.read` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `deployment-network.read` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `deployment-group.list` | Read Groups | Administrator, Editor, Operator, Viewer |
| `deployment-group.update` | Update a Group | Administrator, Editor, Operator |
| `deployment-group-autoscaling.read` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `deployment-group-autoscaling.update` | Update autoscaling configuration | Administrator, Editor, Operator |
| `deployment-postgresql-logical-replication-slot.create` | Create postgresql logical replication slot | Administrator, Editor, Operator |
| `deployment-postgresql-logical-replication-slot.delete` | Delete postgresql logical replication slot | Administrator, Editor, Operator |
| `capability.create` | Discover a supported capability | Administrator, Editor, Operator |
| `deployment-user.create` | Create a type of user | Administrator, Editor, Operator |
| `deployment-user.read` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `deployment-user.update` | Update a type of user | Administrator, Editor, Operator |
| `deployment-user.delete` | Delete a type of user | Administrator, Editor, Operator |
| `deployment-user-connection.list` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-user-connection.create` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.list` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.create` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-ip-address.delete` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-allowlist-ip-addresses.update` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `deployment-capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
| `capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
{: caption="Table 42. Service actions - Databases for PostgreSQL" caption-side="top"}
{: #actions-table42}
{: tab-title="Actions"}
{: tab-group="databases-for-postgresql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Databases for Redis
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-redis` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 43. Platform roles - Databases for Redis" caption-side="top"}
{: #platform-roles-table43}
{: tab-title="Platform roles"}
{: tab-group="databases-for-redis"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /2017-12/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `DELETE /2017-12/:platform/deployments/:deployment_id` | Remove a Deployment | Administrator, Editor, Operator |
| `GET /2017-12/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /2017-12/:platform/clusters/:cluster_id/deployments` | Create a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/users` | Create a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id` | Read a DeploymentUser | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id` | Update a DeploymentUser | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/users/:user_id` | Remove a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v5/:platform/capability/:capability_id` | Discover a supported capability | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type` | Create a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Update a type of user | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Delete a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses/:ip_address_id` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `task.read` | Read a Task | Administrator, Editor, Operator, Viewer |
| `backup.read` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `deployment.read` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `deployment.update` | Update a Deployment | Administrator, Editor, Operator |
| `deployment-point-in-time-recovery-data.list` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `deployment-task.list` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `deployment-backup.list` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `deployment-backup.create` | Create an on-demand backup | Administrator, Editor, Operator |
| `deployment-remote.list` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `deployment-remote.update` | Update a remote replica | Administrator, Editor, Operator |
| `deployment-remote.create` | Promote a remote replica | Administrator, Editor, Operator |
| `deployment-remote-resync.create` | Resync remote replica | Administrator, Editor, Operator |
| `deployment-database-connection.bulkdelete` | Kill all database connections | Administrator, Editor, Operator |
| `deployment-configuration.update` | Update deployment configuration | Administrator, Editor, Operator |
| `deployment-configuration-schema.read` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `deployment-network.read` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `deployment-group.list` | Read Groups | Administrator, Editor, Operator, Viewer |
| `deployment-group.update` | Update a Group | Administrator, Editor, Operator |
| `deployment-group-autoscaling.read` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `deployment-group-autoscaling.update` | Update autoscaling configuration | Administrator, Editor, Operator |
| `capability.create` | Discover a supported capability | Administrator, Editor, Operator |
| `deployment-user.create` | Create a type of user | Administrator, Editor, Operator |
| `deployment-user.read` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `deployment-user.update` | Update a type of user | Administrator, Editor, Operator |
| `deployment-user.delete` | Delete a type of user | Administrator, Editor, Operator |
| `deployment-user-connection.list` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-user-connection.create` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.list` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.create` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-ip-address.delete` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-allowlist-ip-addresses.update` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `deployment-capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
| `capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
{: caption="Table 43. Service actions - Databases for Redis" caption-side="top"}
{: #actions-table43}
{: tab-title="Actions"}
{: tab-group="databases-for-redis"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Knowledge Catalog for Watson Data and AI
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `datacatalog` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 44. Platform roles - IBM Knowledge Catalog for Watson Data and AI" caption-side="top"}
{: #platform-roles-table44}
{: tab-title="Platform roles"}
{: tab-group="datacatalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 44. Service roles - IBM Knowledge Catalog for Watson Data and AI" caption-side="top"}
{: #service-roles-table44}
{: tab-title="Service roles"}
{: tab-group="datacatalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `datacatalog` |  | Administrator |
| `datacatalog.catalog.create` |  | Administrator, Manager, Writer |
{: caption="Table 44. Service actions - IBM Knowledge Catalog for Watson Data and AI" caption-side="top"}
{: #actions-table44}
{: tab-title="Actions"}
{: tab-group="datacatalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## DataStage
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `datastage` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 45. Platform roles - DataStage" caption-side="top"}
{: #platform-roles-table45}
{: tab-title="Platform roles"}
{: tab-group="datastage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 45. Service roles - DataStage" caption-side="top"}
{: #service-roles-table45}
{: tab-title="Service roles"}
{: tab-group="datastage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `datastage.dashboard.view` | DataStage dashboard view | Administrator, Editor, Operator, Reader |
{: caption="Table 45. Service actions - DataStage" caption-side="top"}
{: #actions-table45}
{: tab-title="Actions"}
{: tab-group="datastage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Direct Link
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `directlink` for the service name.

No supported roles.
## Direct Link Connect
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `directlink.connect` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 47. Platform roles - Direct Link Connect" caption-side="top"}
{: #platform-roles-table47}
{: tab-title="Platform roles"}
{: tab-group="directlink.connect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `directlink.connect.view` | View | Administrator, Editor, Operator, Viewer |
| `directlink.connect.edit` | Edit | Administrator, Editor |
{: caption="Table 47. Service actions - Direct Link Connect" caption-side="top"}
{: #actions-table47}
{: tab-title="Actions"}
{: tab-group="directlink.connect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Direct Link Dedicated
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `directlink.dedicated` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 48. Platform roles - Direct Link Dedicated" caption-side="top"}
{: #platform-roles-table48}
{: tab-title="Platform roles"}
{: tab-group="directlink.dedicated"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `directlink.dedicated.view` | View | Administrator, Editor, Operator, Viewer |
| `directlink.dedicated.edit` | Edit | Administrator, Editor |
{: caption="Table 48. Service actions - Direct Link Dedicated" caption-side="top"}
{: #actions-table48}
{: tab-title="Actions"}
{: tab-group="directlink.dedicated"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Discovery
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `discovery` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 49. Service roles - Discovery" caption-side="top"}
{: #service-roles-table49}
{: tab-title="Service roles"}
{: tab-group="discovery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `PUT /discovery` | Update existing resources | Manager, Writer |
| `POST /discovery` | Create new resources | Manager, Writer |
| `DELETE /discovery` | Delete resources | Manager, Writer |
| `PATCH /discovery` | Make partial update to resources | Manager, Writer |
| `GET /discovery` | Retrieve resources | Manager, Reader, Writer |
{: caption="Table 49. Service actions - Discovery" caption-side="top"}
{: #actions-table49}
{: tab-title="Actions"}
{: tab-group="discovery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Dizzion DaaS
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `dizziondaas` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 50. Platform roles - Dizzion DaaS" caption-side="top"}
{: #platform-roles-table50}
{: tab-title="Platform roles"}
{: tab-group="dizziondaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `dizziondaas.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 50. Service actions - Dizzion DaaS" caption-side="top"}
{: #actions-table50}
{: tab-title="Actions"}
{: tab-group="dizziondaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## DNS Services
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `dns-svcs` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 51. Platform roles - DNS Services" caption-side="top"}
{: #platform-roles-table51}
{: tab-title="Platform roles"}
{: tab-group="dns-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 51. Service roles - DNS Services" caption-side="top"}
{: #service-roles-table51}
{: tab-title="Service roles"}
{: tab-group="dns-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `dns-svcs.dashboard.view` |  | Administrator, Editor, Operator |
| `dns-svcs.zones.read` |  | Manager, Reader, Writer |
| `dns-svcs.zones.update` |  | Manager, Writer |
| `dns-svcs.zones.manage` |  | Manager |
| `dns-svcs.resource-records.manage` |  | Manager |
| `dns-svcs.resource-records.update` |  | Manager, Writer |
| `dns-svcs.resource-records.read` |  | Manager, Reader, Writer |
| `dns-svcs.acls.manage` |  | Manager |
| `dns-svcs.acls.update` |  | Manager, Writer |
| `dns-svcs.acls.read` |  | Manager, Reader, Writer |
| `dns-svcs.permitted-networks.manage` |  | Manager |
| `dns-svcs.permitted-networks.update` |  | Manager, Writer |
| `dns-svcs.permitted-networks.read` |  | Manager, Reader, Writer |
{: caption="Table 51. Service actions - DNS Services" caption-side="top"}
{: #actions-table51}
{: tab-title="Actions"}
{: tab-group="dns-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Dynamic Dashboard Embedded
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `dynamic-dashboard-embedded` for the service name.

| Role | Description |
| ----- | :----- |
| null | null |
| null | null |
| null | null |
{: row-headers}
{: caption="Table 52. Service roles - Dynamic Dashboard Embedded" caption-side="top"}
{: #service-roles-table52}
{: tab-title="Service roles"}
{: tab-group="dynamic-dashboard-embedded"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `dynamic-dashboard-embedded.instances.write` |  | null, null, null |
{: caption="Table 52. Service actions - Dynamic Dashboard Embedded" caption-side="top"}
{: #actions-table52}
{: tab-title="Actions"}
{: tab-group="dynamic-dashboard-embedded"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## ibm-cloud-for-education
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `education` for the service name.

No supported roles.
## IBM Cloud Platform Enterprise Service
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `enterprise` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | Administrators can update the enterprise, create accounts and account groups, move accounts between account groups, import existing accounts, and view usage reports. |
| Editor | Editors can update the enterprise, create accounts and account groups, view usage reports, and import accounts. |
| Operator | Operators can view the enterprise, account groups, and accounts. |
| Viewer | Viewers can view the enterprise, account groups, and accounts. |
{: row-headers}
{: caption="Table 54. Platform roles - IBM Cloud Platform Enterprise Service" caption-side="top"}
{: #platform-roles-table54}
{: tab-title="Platform roles"}
{: tab-group="enterprise"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Usage Reports Viewer | As a usage reports viewer, you can view usage reports of entities under the enterprise hierarchy |
{: row-headers}
{: caption="Table 54. Service roles - IBM Cloud Platform Enterprise Service" caption-side="top"}
{: #service-roles-table54}
{: tab-title="Service roles"}
{: tab-group="enterprise"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `enterprise.enterprise.create` |  | Administrator |
| `enterprise.enterprise.update` |  | Administrator, Editor |
| `enterprise.enterprise.retrieve` | Retrieve an enterprise in IBM Cloud. | Administrator, Editor, Operator, Usage Reports Viewer, Viewer |
| `enterprise.enterprise.import` |  | Administrator, Editor |
| `enterprise.enterprise.retrieve-usage-report` |  | Administrator, Editor, Usage Reports Viewer |
| `enterprise.account-group.create` |  | Administrator, Editor |
| `enterprise.account-group.update` |  | Administrator, Editor |
| `enterprise.account-group.retrieve` | Retrieve account groups within an enterprise. | Administrator, Editor, Operator, Usage Reports Viewer, Viewer |
| `enterprise.account-group.retrieve-usage-report` | Retrieve resource usage reports of the resources in the account-group | Administrator, Editor, Usage Reports Viewer |
| `enterprise.account.create` |  | Administrator, Editor |
| `enterprise.account.update` |  | Administrator, Editor |
| `enterprise.account.move` |  | Administrator |
| `enterprise.account.retrieve` | Retrieve accounts within an enterprise. | Administrator, Editor, Operator, Usage Reports Viewer, Viewer |
| `enterprise.account.retrieve-usage-report` | Retrieve resource usage reports of the resources in the account | Administrator, Editor, Usage Reports Viewer |
| `enterprise.enterprise.attach-config-rules` | Attach config rules to an enterprise. | Administrator |
| `enterprise.enterprise.detach-config-rules` | Detach config rules from an enterprise. | Administrator |
| `enterprise.enterprise.update-config-rules` | Update config rules attached to an enterprise. | Administrator |
| `enterprise.account-group.attach-config-rules` | Attach config rules to an account group. | Administrator |
| `enterprise.account-group.detach-config-rules` | Detach config rules from an account group. | Administrator |
| `enterprise.account-group.update-config-rules` | Update config rules attached to an account group. | Administrator |
| `enterprise.account.attach-config-rules` | Attach config rules to an account within an enterprise. | Administrator |
| `enterprise.account.detach-config-rules` | Detach config rules from an account within an enterprise. | Administrator |
| `enterprise.account.update-config-rules` | Update config rules attached to an account within an enterprise. | Administrator |
| `enterprise.enterprise.attach-templates` | Attach templates to an enterprise. | Administrator |
| `enterprise.enterprise.detach-templates` | Detach templates from an enterprise. | Administrator |
| `enterprise.enterprise.update-templates` | Update templates attached to an enterprise. | Administrator |
| `enterprise.account-group.attach-templates` | Attach templates to an account group. | Administrator |
| `enterprise.account-group.detach-templates` | Detach templates from an account group. | Administrator |
| `enterprise.account-group.update-templates` | Update templates attached to an account group. | Administrator |
| `enterprise.account.attach-templates` | Attach templates to an account within an enterprise. | Administrator |
| `enterprise.account.detach-templates` | Detach templates from an account within an enterprise. | Administrator |
| `enterprise.account.update-templates` | Update templates attached to an account within an enterprise. | Administrator |
{: caption="Table 54. Service actions - IBM Cloud Platform Enterprise Service" caption-side="top"}
{: #actions-table54}
{: tab-title="Actions"}
{: tab-group="enterprise"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## License and Entitlement
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `entitlement` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 55. Platform roles - License and Entitlement" caption-side="top"}
{: #platform-roles-table55}
{: tab-title="Platform roles"}
{: tab-group="entitlement"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `entitlement.entitlement.write` |  | Administrator, Editor |
| `entitlement.entitlement.write-admin` |  | Administrator |
{: caption="Table 55. Service actions - License and Entitlement" caption-side="top"}
{: #actions-table55}
{: tab-title="Actions"}
{: tab-group="entitlement"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Event Notifications
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `event-notifications` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 56. Platform roles - Event Notifications" caption-side="top"}
{: #platform-roles-table56}
{: tab-title="Platform roles"}
{: tab-group="event-notifications"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Channel Editor | Custom role to handle subscription activities |
| Device Manager | Custom role to handle push device registration with the event-noitifications service |
| Event Notification Publisher | Custom role to send notifications |
| Event Source Manager | Custom role to handle source integration with the event-notifications service |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Status Reporter | Custom role to handle messaging api callbacks |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 56. Service roles - Event Notifications" caption-side="top"}
{: #service-roles-table56}
{: tab-title="Service roles"}
{: tab-group="event-notifications"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `event-notifications.dashboard.view` | This action is to view the dashboard | Administrator, Channel Editor, Event Source Manager, Manager, Operator, Reader, Viewer, Writer |
| `event-notifications.sources.create` | This action is to integrate a new source | Administrator, Event Source Manager, Manager |
| `event-notifications.sources.read` | This action is to get an already integrated source | Administrator, Channel Editor, Event Source Manager, Manager, Reader |
| `event-notifications.sources.update` | This action is to update an already integrated source | Administrator, Event Source Manager, Manager |
| `event-notifications.sources.delete` | This action is to delete an already integrated source | Administrator, Event Source Manager, Manager |
| `event-notifications.sources.list` | This action is to list all integrated sources in an instance | Administrator, Channel Editor, Event Source Manager, Manager, Reader |
| `event-notifications.topics.create` | This action is to create a new topic | Administrator, Manager, Writer |
| `event-notifications.topics.read` | This action is to get an already created topic | Administrator, Channel Editor, Manager, Reader, Writer |
| `event-notifications.topics.update` | This action is to update an already created topic | Administrator, Manager, Writer |
| `event-notifications.topics.delete` | This action is to delete an already created topic | Administrator, Manager |
| `event-notifications.topics.list` | This action is to list all topics in an instance | Administrator, Channel Editor, Manager, Reader, Writer |
| `event-notifications.rules.create` | This action is to create a rule under a source | Administrator, Manager, Writer |
| `event-notifications.rules.read` | This action is to get a rule in an instance | Administrator, Channel Editor, Manager, Reader, Writer |
| `event-notifications.rules.update` | This action is to update an existing rule | Administrator, Manager, Writer |
| `event-notifications.rules.delete` | This action is to delete a rule in an instance | Administrator, Manager |
| `event-notifications.rules.list` | This action is to list all rules in an instance based on the sourceID and/or topicID | Administrator, Channel Editor, Manager, Reader, Writer |
| `event-notifications.destinations.create` | This action is to create a new destination | Administrator, Manager, Writer |
| `event-notifications.destinations.read` | This action is to get a destination within an instance | Administrator, Channel Editor, Manager, Reader, Writer |
| `event-notifications.destinations.update` | This action is to update existing destination information | Administrator, Manager, Writer |
| `event-notifications.destinations.delete` | This action is to delete a destination | Administrator, Manager |
| `event-notifications.destinations.list` | This action is to list all destinations within an instance | Administrator, Channel Editor, Manager, Reader, Writer |
| `event-notifications.subscriptions.create` | This action is to create associate a destination to a topic | Administrator, Channel Editor, Manager, Writer |
| `event-notifications.subscriptions.read` | This action is to get a destination-topic mapping | Administrator, Channel Editor, Manager, Reader, Writer |
| `event-notifications.subscriptions.update` | This action is to update a destination-topic mapping | Administrator, Channel Editor, Manager, Writer |
| `event-notifications.subscriptions.delete` | This action is to delete a subscription | Administrator, Channel Editor, Manager |
| `event-notifications.subscriptions.list` | This action is to list subscriptions based on the topicID and/or destinationID | Administrator, Channel Editor, Manager, Reader, Writer |
| `event-notifications.notifications.post` | This action is to publish an event to EN | Administrator, Event Notification Publisher, Event Source Manager, Manager, Writer |
| `event-notifications.counts.get` | This action is to get counts of all entities in an instance | Channel Editor, Event Notification Publisher, Event Source Manager, Manager, Reader |
| `event-notifications.events.create` | This API is used to create a new Event | Administrator, Event Source Manager, Manager |
| `event-notifications.events.read` | This API is used to get information about an event | Event Source Manager |
| `event-notifications.events.list` | This API is used to list all events in an instance under a source | Administrator, Event Source Manager, Manager, Reader |
| `event-notifications.events.delete` | This API is used to delete an event in an instance under a source | Event Source Manager |
| `event-notifications.publickey.read` | To get public keys related to webhook encryption | Administrator, Channel Editor, Manager, Reader, Writer |
| `event-notifications.severities.create` | This API is used to create a new Event | Event Source Manager |
| `event-notifications.severities.read` | This API is used to get information about an event | Event Source Manager |
| `event-notifications.severities.list` | This API is used to list all events in an instance under a source | Administrator, Event Source Manager, Manager, Reader |
| `event-notifications.severities.delete` | This API is used to delete an event in an instance under a source | Event Source Manager |
| `event-notifications.email-status.create` | The API is used for callback from messaging service | Status Reporter |
| `event-notifications.sms-status.create` | The API is used for callback from messaging service | Status Reporter |
| `event-notifications.webhook-status.create` | The API is used for callback from messaging service | Status Reporter |
| `event-notifications.devices.create` | This API is used to register new device for push destination | Administrator, Device Manager, Manager |
| `event-notifications.devices.read` | This API is used to get registered push destination device by device_id | Administrator, Device Manager, Manager |
| `event-notifications.devices.update` | This API is used to update the push registered device for push destination | Administrator, Device Manager, Manager |
| `event-notifications.devices.delete` | This API is used to delete registered push device for push destination | Administrator, Device Manager, Manager |
| `event-notifications.devices.list` | This API is used to get all registered devices for push destination | Administrator, Manager |
| `event-notifications.tag-subscriptions.list` | The API is get subscriptions for push destination | Administrator, Manager |
| `event-notifications.tag-subscriptions.devices.list` | This Api is used to get subscriptions by device for push destination | Administrator, Device Manager, Manager |
| `event-notifications.tag-subscriptions.create` | The API is create subscription for push destination | Administrator, Device Manager, Manager |
| `event-notifications.tag-subscriptions.delete` | The API is delete subscription for push destination | Administrator, Device Manager, Manager |
| `event-notifications.channel-groups.create` | This action is to integrate a new channel group | Administrator, Device Manager, Manager |
| `event-notifications.channel-groups.read` | This action is to read a channel group | Administrator, Device Manager, Manager, Reader |
| `event-notifications.channel-groups.list` | This action is to get all channel groups | Administrator, Device Manager, Manager, Reader |
| `event-notifications.channel-groups.update` | This action is to update a channel group | Administrator, Device Manager, Manager |
| `event-notifications.channel-groups.delete` | This action is to delete a channel group | Administrator, Manager |
| `event-notifications.channels.create` | This action is to create fcm channel | Administrator, Device Manager, Manager |
| `event-notifications.channels.read` | This action is to read a channel | Administrator, Device Manager, Manager, Reader |
| `event-notifications.channels.list` | This action is to read all fcm channels | Administrator, Device Manager, Manager, Reader |
| `event-notifications.channels.update` | This action is to update fcm channel | Administrator, Device Manager, Manager |
| `event-notifications.channels.delete` | This action is to delete a fcm channel | Administrator, Manager |
{: caption="Table 56. Service actions - Event Notifications" caption-side="top"}
{: #actions-table56}
{: tab-title="Actions"}
{: tab-group="event-notifications"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Cloud Functions
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `functions` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 57. Service roles - IBM Cloud Functions" caption-side="top"}
{: #service-roles-table57}
{: tab-title="Service roles"}
{: tab-group="functions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `functions.namespaces.read` |  | Manager, Reader, Writer |
| `functions.namespaces.delete` |  | Manager |
| `functions.namespaces.update` |  | Manager |
| `functions.entities.create` |  | Manager, Writer |
| `functions.entities.update` |  | Manager, Writer |
| `functions.entities.delete` |  | Manager, Writer |
| `functions.entities.read` |  | Manager, Reader, Writer |
| `functions.entities.activate` |  | Manager, Reader, Writer |
{: caption="Table 57. Service actions - IBM Cloud Functions" caption-side="top"}
{: #actions-table57}
{: tab-title="Actions"}
{: tab-group="functions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Globalization Pipeline
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `g11n-pipeline` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 58. Platform roles - Globalization Pipeline" caption-side="top"}
{: #platform-roles-table58}
{: tab-title="Platform roles"}
{: tab-group="g11n-pipeline"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 58. Service roles - Globalization Pipeline" caption-side="top"}
{: #service-roles-table58}
{: tab-title="Service roles"}
{: tab-group="g11n-pipeline"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `g11n-pipeline.dashboard.view` |  | Administrator, Editor, Operator |
| `g11n-pipeline.user.create-user` |  | Manager |
| `g11n-pipeline.document.delete-document` |  | Manager |
| `g11n-pipeline.document-translation-request.create-translation-request` |  | Manager |
| `g11n-pipeline.bundle.update-resource-entry-info` |  | Manager, Writer |
| `g11n-pipeline.translation-request.get-translation-requests` |  | Manager, Writer |
| `g11n-pipeline.document.create-document` |  | Manager |
| `g11n-pipeline.bundle.get-resource-strings` |  | Manager, Reader, Writer |
| `g11n-pipeline.xliff-document.update-documents-with-xliff` |  | Manager, Writer |
| `g11n-pipeline.user.update-user` |  | Manager |
| `g11n-pipeline.bundle.update-resource-entries` |  | Manager, Writer |
| `g11n-pipeline.translation-request.get-tr-resource-entry-info` |  | Manager, Writer |
| `g11n-pipeline.xliff.update-bundles-with-xliff` |  | Manager, Writer |
| `g11n-pipeline.bundle.upload-resource-entries` |  | Manager |
| `g11n-pipeline.document.get-document-list` |  | Manager, Writer |
| `g11n-pipeline.document-translation-request.get-tr-document-segment-info` |  | Manager, Writer |
| `g11n-pipeline.xliff.get-xliff-from-tr` |  | Manager, Writer |
| `g11n-pipeline.document-translation-request.update-translation-request` |  | Manager |
| `g11n-pipeline.document-translation-request.get-document-translation-request` |  | Manager, Writer |
| `g11n-pipeline.config.put-translation-config` |  | Manager |
| `g11n-pipeline.xliff-document.get-xliff-from-document-tr` |  | Manager, Writer |
| `g11n-pipeline.user.get-users` |  | Manager |
| `g11n-pipeline.config.put-mt-service-binding` |  | Manager |
| `g11n-pipeline.translation-request.update-translation-request` |  | Manager |
| `g11n-pipeline.document-translation-request.get-document-translation-requests` |  | Manager, Writer |
| `g11n-pipeline.user.get-user` |  | Manager, Writer |
| `g11n-pipeline.document-translation-request.get-tr-document-segments` |  | Manager, Writer |
| `g11n-pipeline.translation-request.get-tr-resource-entries` |  | Manager, Writer |
| `g11n-pipeline.document-translation-request.delete-document-translation-request` |  | Manager |
| `g11n-pipeline.bundle.delete-bundle` |  | Manager |
| `g11n-pipeline.bundle.get-resource-entry-info` |  | Manager, Writer |
| `g11n-pipeline.bundle.get-bundle-list` |  | Manager, Writer |
| `g11n-pipeline.bundle.create-bundle` |  | Manager |
| `g11n-pipeline.bundle.get-bundle-info` |  | Manager, Reader, Writer |
| `g11n-pipeline.bundle.update-bundle` |  | Manager |
| `g11n-pipeline.translation-request.get-tr-bundle-info` |  | Manager, Writer |
| `g11n-pipeline.config.get-all-mt-service-bindings` |  | Manager |
| `g11n-pipeline.service-instance.get-service-instance-info` |  | Manager, Writer |
| `g11n-pipeline.xliff.get-xliff-from-bundles` |  | Manager, Writer |
| `g11n-pipeline.config.delete-mt-service-binding` |  | Manager |
| `g11n-pipeline.config.get-translation-config` |  | Manager |
| `g11n-pipeline.user.delete-user` |  | Manager |
| `g11n-pipeline.document-translation-request.get-tr-document-info` |  | Manager, Writer |
| `g11n-pipeline.config.get-mt-service-binding` |  | Manager |
| `g11n-pipeline.config.delete-translation-config` |  | Manager |
| `g11n-pipeline.xliff-document.get-xliff-from-documents` |  | Manager, Writer |
| `g11n-pipeline.config.get-all-translation-configs` |  | Manager, Writer |
| `g11n-pipeline.translation-request.delete-translation-request` |  | Manager |
| `g11n-pipeline.translation-request.get-translation-request` |  | Manager, Writer |
| `g11n-pipeline.translation-request.create-translation-request` |  | Manager |
| `g11n-pipeline.bundle.get-bundle-info-full` |  | Manager, Writer |
| `g11n-pipeline.bundle.get-bundle-list-all` |  | Manager |
| `g11n-pipeline.bundle.get-resource-strings-all` |  | Manager, Writer |
| `g11n-pipeline.user.get-user-all` |  | Manager |
| `g11n-pipeline.bundle.update-resource-strings-src` |  | Manager |
| `g11n-pipeline.bundle.update-resource-entry-info-src` |  | Manager |
| `g11n-pipeline.document.get-document-content` |  | Manager, Reader, Writer |
| `g11n-pipeline.document.get-document-meta-data` |  | Manager, Reader, Writer |
| `g11n-pipeline.document.get-document-meta-data-full` |  | Manager, Writer |
| `g11n-pipeline.document.get-document-segments` |  | Manager, Writer |
| `g11n-pipeline.document.update-document-meta-data` |  | Manager |
| `g11n-pipeline.document.get-segment-info` |  | Manager, Writer |
| `g11n-pipeline.document.upload-document-content` |  | Manager |
| `g11n-pipeline.document.update-segment-translation` |  | Manager, Writer |
{: caption="Table 58. Service actions - Globalization Pipeline" caption-side="top"}
{: #actions-table58}
{: tab-title="Actions"}
{: tab-group="g11n-pipeline"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## GhoST API
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `ghost-api` for the service name.

No supported roles.
## GhoST Tagging Service
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `ghost-tags` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 60. Platform roles - GhoST Tagging Service" caption-side="top"}
{: #platform-roles-table60}
{: tab-title="Platform roles"}
{: tab-group="ghost-tags"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `ghost-tags.create-access-tag` | The ability to create access management tags in an account | Administrator |
| `ghost-tags.delete-access-tag` | The ability to delete access management tags in an account | Administrator |
{: caption="Table 60. Service actions - GhoST Tagging Service" caption-side="top"}
{: #actions-table60}
{: tab-title="Actions"}
{: tab-group="ghost-tags"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Global Catalog
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `globalcatalog` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | Administrators can change object metadata or visibility for private services added to the account and can restrict the visibility of a public service. |
| Editor | Editors can change object metadata, but can?t change visibility for private services added to the account. |
| Operator | Operators can view private services added to the account. |
| Viewer | Viewers can view private services added to the account. |
{: row-headers}
{: caption="Table 61. Platform roles - Global Catalog" caption-side="top"}
{: #platform-roles-table61}
{: tab-title="Platform roles"}
{: tab-group="globalcatalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `globalcatalog.is.admin` | Is Admin | Administrator |
| `globalcatalog.is.editor` | Is Editor | Editor |
| `globalcatalog.is.viewer` | Is Viewer | Operator, Viewer |
{: caption="Table 61. Service actions - Global Catalog" caption-side="top"}
{: #actions-table61}
{: tab-title="Actions"}
{: tab-group="globalcatalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Personal Catalog
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `globalcatalog-collection` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 62. Platform roles - Personal Catalog" caption-side="top"}
{: #platform-roles-table62}
{: tab-title="Platform roles"}
{: tab-group="globalcatalog-collection"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| IBMOperation | (Internal) - IBM Use only |
| Publisher | You can publish offerings that are approved by IBM and that are in a private catalog to which you're assigned the viewer role. |
{: row-headers}
{: caption="Table 62. Service roles - Personal Catalog" caption-side="top"}
{: #service-roles-table62}
{: tab-title="Service roles"}
{: tab-group="globalcatalog-collection"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `globalcatalog-collection.instance.promote` | Publish item to public, assuming also has viewer access. | Administrator, Publisher |
| `globalcatalog-collection.operation.approve` | This action approves the publishing of items to public. Only IBM can use this action. | Publisher |
| `globalcatalog-collection.account.manage` | This action manages account level settings, e.g. Hiding the public catalog from the account members. | Administrator |
| `globalcatalog-collection.support.janitor` | (Internal) Janitor support | IBMOperation |
| `globalcatalog-collection.support.approveibm` | (Internal) - Approve publishing to IBM only | IBMOperation |
| `globalcatalog-collection.support.approvepublic` | (Internal) Approve publishing to public | IBMOperation |
| `globalcatalog-collection.support.approveshare` | (Internal) Approve publishing to Shared | IBMOperation |
| `globalcatalog-collection.config.read` | Fortress compliance - read configuration | IBMOperation |
| `globalcatalog-collection.restrictedtags.update` | Permission to set restricted tags in a product. | IBMOperation |
{: caption="Table 62. Service actions - Personal Catalog" caption-side="top"}
{: #actions-table62}
{: tab-title="Actions"}
{: tab-group="globalcatalog-collection"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Instance Management
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `globalcatalog-instance` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 63. Platform roles - Instance Management" caption-side="top"}
{: #platform-roles-table63}
{: tab-title="Platform roles"}
{: tab-group="globalcatalog-instance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `globalcatalog-instance.dashboard.view` | View Dashboard | Administrator, Editor, Operator, Viewer |
{: caption="Table 63. Service actions - Instance Management" caption-side="top"}
{: #actions-table63}
{: tab-title="Actions"}
{: tab-group="globalcatalog-instance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## HPCaaS from Rescale
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `hpcaas-from-rescale-prod` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
| Editor | null |
| Operator | null |
{: row-headers}
{: caption="Table 64. Platform roles - HPCaaS from Rescale" caption-side="top"}
{: #platform-roles-table64}
{: tab-title="Platform roles"}
{: tab-group="hpcaas-from-rescale-prod"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `hpcaas-from-rescale-prod.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 64. Service actions - HPCaaS from Rescale" caption-side="top"}
{: #actions-table64}
{: tab-title="Actions"}
{: tab-group="hpcaas-from-rescale-prod"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Hyper Protect Virtual Server
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `hpvs` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 65. Platform roles - Hyper Protect Virtual Server" caption-side="top"}
{: #platform-roles-table65}
{: tab-title="Platform roles"}
{: tab-group="hpvs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 65. Service roles - Hyper Protect Virtual Server" caption-side="top"}
{: #service-roles-table65}
{: tab-title="Service roles"}
{: tab-group="hpvs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `hpvs.dashboard.view` | Can view the dashboard | Administrator, Editor, Manager, Operator, Reader, Writer |
{: caption="Table 65. Service actions - Hyper Protect Virtual Server" caption-side="top"}
{: #actions-table65}
{: tab-title="Actions"}
{: tab-group="hpvs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Hyper Protect Crypto Services
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `hs-crypto` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 66. Platform roles - Hyper Protect Crypto Services" caption-side="top"}
{: #platform-roles-table66}
{: tab-title="Platform roles"}
{: tab-group="hs-crypto"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Certificate Manager | Managing client certificates to configure mutual TLS for EP11 workloads |
| KMS Key Purge Role | As a KMS Key Purge, the user is allowed to purge encryption keys. |
| Key Custodian - Creator | Manages Keys. For a complete key lifecycle both Creator and Deployer roles are needed. To implement separaton of duties assign Creator and Deployer role to different people. Can create keys |
| Key Custodian - Deployer | Manages Keys. For a complete key lifecycle both Creator and Deployer roles are needed. To implement separaton of duties assign Creator and Deployer role to different people. Can deploy keys |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Reader Plus | As a reader plus, you can perform read-only actions within the service such as viewing service-specific resources. You can also access key material of standard keys. |
| VMWare KMIP Manager | Allow the VMWare Solutions service to configure KMIP (activate/deactivate KMIP endpoint, manage client certificates) |
| Vault Administrator | Can manage vaults, keystores (incl. cost implications), templates, and can perform destructive lifecycle actions on managed keys. Different vaults can be used to e.g. separate teams, lines of business, or customers. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 66. Service roles - Hyper Protect Crypto Services" caption-side="top"}
{: #service-roles-table66}
{: tab-title="Service roles"}
{: tab-group="hs-crypto"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `hs-crypto.crypto.decrypt` | hs-crypto.crypto.decrypt | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.derivekey` | hs-crypto.crypto.derivekey | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.digest` | hs-crypto.crypto.digest | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.digestkey` | hs-crypto.crypto.digestkey | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.encrypt` | hs-crypto.crypto.encrypt | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.generatekey` | hs-crypto.crypto.generatekey | Manager, Writer |
| `hs-crypto.crypto.generatekeypair` | hs-crypto.crypto.generatekeypair | Manager, Writer |
| `hs-crypto.crypto.generaterandom` | hs-crypto.crypto.generaterandom | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.getattributevalue` | hs-crypto.crypto.getattributevalue | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.getmechanisminfo` | hs-crypto.crypto.getmechanisminfo | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.getmechanismlist` | hs-crypto.crypto.getmechanismlist | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.rewrapkeyblob` | hs-crypto.crypto.rewrapkeyblob | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.setattributevalue` | hs-crypto.crypto.setattributevalue | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.sign` | hs-crypto.crypto.sign | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.unwrapkey` | hs-crypto.crypto.unwrapkey | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.verify` | hs-crypto.crypto.verify | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.wrapkey` | hs-crypto.crypto.wrapkey | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.login` | hs-crypto.crypto.login | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.crypto.logout` | hs-crypto.crypto.logout | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.discovery.listservers` | hs-crypto.discovery.listservers | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.registertopic` | hs-crypto.voting.registertopic | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.listtopicsbyids` | hs-crypto.voting.listtopicsbyids | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.listtopicsbyattributes` | hs-crypto.voting.listtopicsbyattributes | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.deletetopic` | hs-crypto.voting.deletetopic | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.newpoll` | hs-crypto.voting.newpoll | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.finishpoll` | hs-crypto.voting.finishpoll | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.registerpermanentvoter` | hs-crypto.voting.registerpermanentvoter | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.listvotersbyids` | hs-crypto.voting.listvotersbyids | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.listvotersbyattributes` | hs-crypto.voting.listvotersbyattributes | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.deletevoter` | hs-crypto.voting.deletevoter | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.newvote` | hs-crypto.voting.newvote | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.getpollresults` | hs-crypto.voting.getpollresults | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.voting.registerlivevoter` | hs-crypto.voting.registerlivevoter | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.keystore.createkeystore` | hs-crypto.keystore.createkeystore | Manager |
| `hs-crypto.keystore.deletekey` | hs-crypto.keystore.deletekey | Manager, Writer |
| `hs-crypto.keystore.deletekeystore` | hs-crypto.keystore.deletekeystore | Manager |
| `hs-crypto.keystore.listkeysbyattributes` | hs-crypto.keystore.listkeysbyattributes | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.keystore.listkeysbyids` | hs-crypto.keystore.listkeysbyids | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.keystore.listkeystoresbyattributes` | hs-crypto.keystore.listkeystoresbyattributes | Manager |
| `hs-crypto.keystore.listkeystoresbyids` | hs-crypto.keystore.listkeystoresbyids | Manager |
| `hs-crypto.keystore.storenewkey` | hs-crypto.keystore.storenewkey | Manager, Writer |
| `hs-crypto.keystore.updatekey` | hs-crypto.keystore.updatekey | Manager, Writer |
| `hs-crypto.dashboard.view` | View the dashboard | Administrator, Editor, Operator |
| `hs-crypto.instances.read` | Get Instance API endpoint info | Administrator, Editor, Key Custodian - Creator, Key Custodian - Deployer, Manager, Reader, VMWare KMIP Manager, Vault Administrator, Viewer, Writer |
| `hs-crypto.secrets.list` | Retrieve a list of encryption keys. | Manager, Reader, Reader Plus, VMWare KMIP Manager, Writer |
| `hs-crypto.secrets.wrap` | Wrap an encryption key. | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.secrets.unwrap` | Unwrap an encryption key. | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.secrets.create` | Create an encryption key. | Manager, Writer |
| `hs-crypto.secrets.read` | Retrieve an encryption key. | Manager, Reader Plus, Writer |
| `hs-crypto.secrets.delete` | Delete an encryption key. | Manager |
| `hs-crypto.secrets.rotate` | Rotate an encryption key. | Manager, Writer |
| `hs-crypto.instances.manage` | Manage instance via TKE. | Manager |
| `hs-crypto.ep11.use` | Use the GREP11 Interface for Hyper Protect Crypto Services | Administrator, Editor, Manager, Reader, Reader Plus, Viewer, Writer |
| `hs-crypto.importtoken.create` | Allow creation of secure import tokens | Manager, Writer |
| `hs-crypto.importtoken.read` | Allow retrieval of secure import tokens | Manager, Writer |
| `hs-crypto.policies.read` | Retrieve policies for an encryption key | Manager |
| `hs-crypto.policies.write` | Set policies for an encryption key | Manager |
| `hs-crypto.instancepolicies.read` | Retrieve instance level policies | Manager |
| `hs-crypto.instancepolicies.write` | Add or update instance level policies | Manager |
| `hs-crypto.secrets.setkeyfordeletion` | Set or prepare an encryption key for deletion | Manager, Writer |
| `hs-crypto.secrets.unsetkeyfordeletion` | Unset an encryption key for deletion | Manager, Writer |
| `hs-crypto.secrets.readmetadata` | Retrieve the details of an encryption key | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.secrets.rewrap` | Rewrap an encryption key | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.registrations.list` | Retrieve a list of registrations | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.secrets.listkeyversions` | Retrieve a list of versions that are associated with an encryption key | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.registrations.listforkey` | Retrieve a list of registrations for a given encryption key | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.registrations.deactivate` | Move a suspended registration to the deactivated state | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.registrations.create` | Create a registration between an encryption key and a cloud resource | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.registrations.write` | Replace an existing registration | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.registrations.merge` | Update the details of an existing registration | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.registrations.delete` | Delete a registration | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.secrets.disable` | Disable operations for an encryption key | Manager |
| `hs-crypto.secrets.enable` | Enable operations for an encryption key | Manager |
| `hs-crypto.secrets.restore` | Restore a previously deleted encryption key | Manager |
| `hs-crypto.secrets.eventack` | Acknowledge a key lifecycle event | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.kmip.activate` | Activate KMIP endpoint | VMWare KMIP Manager |
| `hs-crypto.kmip.deactivate` | Deactivate KMIP endpoint | VMWare KMIP Manager |
| `hs-crypto.kmip.status` | Get Status of KMIP endpoint | VMWare KMIP Manager |
| `hs-crypto.kmip.certadd` | Add Client Certificates to KMIP endpoint for usage of mutual TLS | VMWare KMIP Manager |
| `hs-crypto.kmip.certdel` | Delete Client Certificates from KMIP endpoint for usage of mutual TLS | VMWare KMIP Manager |
| `hs-crypto.keyrings.create` | Create key rings | Manager, Writer |
| `hs-crypto.keyrings.delete` | Delete key rings | Manager |
| `hs-crypto.keyrings.list` | List key rings | Manager, Reader, Reader Plus, Writer |
| `hs-crypto.secrets.createalias` | Create key alias | Manager, Writer |
| `hs-crypto.secrets.deletealias` | Delete key alias | Manager, Writer |
| `hs-crypto.secrets.sync` | Initiate a manual synchronization request to the associated resources of a key. | Manager, Writer |
| `hs-crypto.secrets.purge` | Purge a destroyed encryption key. | KMS Key Purge Role |
| `hs-crypto.secrets.patch` | Update an encryption key | Manager |
| `hs-crypto.mtlscert-admin-key.create` | Create the administrator signature key for the certificate administrator | Certificate Manager |
| `hs-crypto.mtlscert-admin-key.update` | Update the administrator signature key for the certificate administrator | Certificate Manager |
| `hs-crypto.mtlscert-admin-key.delete` | Delete the administrator signature key of the certificate administrator | Certificate Manager |
| `hs-crypto.mtlscert-admin-key.read` | Get the administrator signature key of the certificate administrator | Certificate Manager |
| `hs-crypto.mtlscert-cert.set` | Create or update certificates by the certificate administrator | Certificate Manager |
| `hs-crypto.mtlscert-cert.list` | List all certificates that are managed by the certificate administrator | Certificate Manager |
| `hs-crypto.mtlscert-cert.read` | Get certificates by the certificate administrator | Certificate Manager |
| `hs-crypto.mtlscert-cert.delete` | Delete certificates by the certificate administrator | Certificate Manager |
| `hs-crypto.vault-keys.active-deactivate` | Deactivate an ACTIVE key | Key Custodian - Deployer |
| `hs-crypto.vault-keys.active-install` | Install an ACTIVE key | Key Custodian - Deployer, Vault Administrator |
| `hs-crypto.vault-keys.active-uninstall` | Uninstall an ACTIVE key | Key Custodian - Creator, Key Custodian - Deployer |
| `hs-crypto.vault-keys.deactivated-destroy` | Destroy a DEACTIVATED key | Vault Administrator |
| `hs-crypto.vault-keys.deactivated-install` | Install a DEACTIVATED key | Key Custodian - Creator, Key Custodian - Deployer |
| `hs-crypto.vault-keys.deactivated-reactivate` | Reactivate a DEACTIVATED key | Key Custodian - Deployer |
| `hs-crypto.vault-keys.deactivated-uninstall` | Uninstall a DEACTIVATED key | Key Custodian - Creator, Key Custodian - Deployer |
| `hs-crypto.vault-keys.destroyed-remove` | Remove a DESTROYED key from Vault | Vault Administrator |
| `hs-crypto.vault-keys.distribute` | Distribute key into assigned keystores | Key Custodian - Creator, Key Custodian - Deployer |
| `hs-crypto.vault-keys.generate` | Generate new key material | Key Custodian - Creator |
| `hs-crypto.vault-keys.preactivation-activate` | Activate a PREACTIVE key | Key Custodian - Deployer |
| `hs-crypto.vault-keys.preactivation-destroy` | Destroy a PREACTIVE key | Key Custodian - Creator, Key Custodian - Deployer |
| `hs-crypto.vault-keys.read` | Read managed key details | Key Custodian - Creator, Key Custodian - Deployer, Reader, Vault Administrator |
| `hs-crypto.vault-keys.list` | List managed keys | Administrator, Editor, Key Custodian - Creator, Key Custodian - Deployer, Manager, Reader, Vault Administrator, Viewer, Writer |
| `hs-crypto.vault-keys.write` | Write/edit managed key details | Key Custodian - Creator, Key Custodian - Deployer |
| `hs-crypto.vault-keys.delete` | Delete a managed key | Vault Administrator |
| `hs-crypto.vault-keys.write-dates` | Write key activation/expiration dates | Key Custodian - Creator, Key Custodian - Deployer |
| `hs-crypto.vault-keys.write-tags` | Write key tags | Key Custodian - Creator, Key Custodian - Deployer |
| `hs-crypto.vault-keystores.read` | Read target keystore details | Key Custodian - Creator, Key Custodian - Deployer, Reader, Vault Administrator |
| `hs-crypto.vault-keystores.list` | List target keystores | Administrator, Editor, Key Custodian - Creator, Key Custodian - Deployer, Manager, Reader, Vault Administrator, Viewer, Writer |
| `hs-crypto.vault-keystores.write` | Write/edit target keystore details | Vault Administrator |
| `hs-crypto.vault-keystores.delete` | Delete a keystore (internal) / Disconnect a keystore (external) | Vault Administrator |
| `hs-crypto.vault-key-templates.read` | Read key template details | Key Custodian - Creator, Key Custodian - Deployer, Reader, Vault Administrator |
| `hs-crypto.vault-key-templates.list` | List key templates | Administrator, Editor, Key Custodian - Creator, Key Custodian - Deployer, Manager, Reader, Vault Administrator, Viewer, Writer |
| `hs-crypto.vault-key-templates.write` | Write/Edit key templates | Key Custodian - Creator, Vault Administrator |
| `hs-crypto.vault-key-templates.delete` | Delete key templates | Vault Administrator |
| `hs-crypto.vaults.read` | Read Vault details | Key Custodian - Creator, Key Custodian - Deployer, Reader, Vault Administrator |
| `hs-crypto.vaults.list` | List Vaults | Administrator, Editor, Key Custodian - Creator, Key Custodian - Deployer, Manager, Reader, Vault Administrator, Viewer, Writer |
| `hs-crypto.vaults.write` | Write/Edit Vault details | Vault Administrator |
| `hs-crypto.vaults.delete` | Delete a Vault | Vault Administrator |
| `hs-crypto.uko.initiate-paid-upgrade` | Start billing of UKO base price (by using external keystores) | Vault Administrator |
| `hs-crypto.uko.add-paid-keystore` | Create a paid keystore (beyond free amount) | Vault Administrator |
{: caption="Table 66. Service actions - Hyper Protect Crypto Services" caption-side="top"}
{: #actions-table66}
{: tab-title="Actions"}
{: tab-group="hs-crypto"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Hyper Protect DBaaS for MongoDB 
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `hyperp-dbaas-mongodb` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 67. Service roles - Hyper Protect DBaaS for MongoDB " caption-side="top"}
{: #service-roles-table67}
{: tab-title="Service roles"}
{: tab-group="hyperp-dbaas-mongodb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `hyperp-dbaas-mongodb.clusters.read` | Get the detailed information about a database cluster | Manager, Reader, Writer |
| `hyperp-dbaas-mongodb.logging.enable` | Enable sending database logs and audit logs to the user's service instance of IBM Log Analysis with LogDNA | Manager, Writer |
| `hyperp-dbaas-mongodb.monitoring.enable` | Enable sending database metrics to a user-specified organization and space in the IBM Cloud Monitoring service | Manager, Writer |
| `hyperp-dbaas-mongodb.users.list` | List all database users | Manager, Reader, Writer |
| `hyperp-dbaas-mongodb.users.read` | Get the detailed information about a database user | Manager, Reader, Writer |
| `hyperp-dbaas-mongodb.databases.list` | List all databases | Manager, Reader, Writer |
| `hyperp-dbaas-mongodb.logs.list` | List database log files and audit log files | Manager, Reader, Writer |
| `hyperp-dbaas-mongodb.logs.read` | Download a database log file or an audit log file | Manager |
| `hyperp-dbaas-mongodb.clusters.resource.scale` | Scale cluster resources | Manager |
| `hyperp-dbaas-mongodb.clusters.tasks.list` | List the tasks running or recently run on a cluster | Manager, Reader, Writer |
| `hyperp-dbaas-mongodb.clusters.tasks.read` | Get the detailed information about a task | Manager, Reader, Writer |
| `hyperp-dbaas-mongodb.clusters.configuration.update` | Update the database configuration of your cluster | Manager |
| `hyperp-dbaas-mongodb.clusters.configuration.read` | Show the database configuration of your cluster | Manager, Reader, Writer |
| `hyperp-dbaas-mongodb.backups.cos.enable` | Enable backups to COS | Manager |
| `hyperp-dbaas-mongodb.backups.cos.disable` | Disable backups to COS | Manager |
| `hyperp-dbaas-mongodb.backups.restore` | Restore DB from backup | Manager |
| `hyperp-dbaas-mongodb.backups.cos.read` | Show COS configuration | Manager, Reader, Writer |
{: caption="Table 67. Service actions - Hyper Protect DBaaS for MongoDB " caption-side="top"}
{: #actions-table67}
{: tab-title="Actions"}
{: tab-group="hyperp-dbaas-mongodb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Hyper Protect DBaaS for PostgreSQL
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `hyperp-dbaas-postgresql` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 68. Service roles - Hyper Protect DBaaS for PostgreSQL" caption-side="top"}
{: #service-roles-table68}
{: tab-title="Service roles"}
{: tab-group="hyperp-dbaas-postgresql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `hyperp-dbaas-postgresql.clusters.read` | Get the detailed information about a database cluster | Manager, Reader, Writer |
| `hyperp-dbaas-postgresql.logging.enable` | Enable sending database logs and audit logs to the user's service instance of IBM Log Analysis with LogDNA | Manager, Writer |
| `hyperp-dbaas-postgresql.monitoring.enable` | Enable sending database metrics to a user-specified organization and space in the IBM Cloud Monitoring service | Manager, Writer |
| `hyperp-dbaas-postgresql.users.list` | List all database users | Manager, Reader, Writer |
| `hyperp-dbaas-postgresql.users.read` | Get the detailed information about a database user | Manager, Reader, Writer |
| `hyperp-dbaas-postgresql.databases.list` | List all databases | Manager, Reader, Writer |
| `hyperp-dbaas-postgresql.logs.list` | List database log files and audit log files | Manager, Reader, Writer |
| `hyperp-dbaas-postgresql.logs.read` | Download a database log file or an audit log file | Manager |
| `hyperp-dbaas-postgresql.clusters.resource.scale` | Scale cluster resources | Manager |
| `hyperp-dbaas-postgresql.clusters.tasks.list` | List the tasks running or recently run on a cluster | Manager, Reader, Writer |
| `hyperp-dbaas-postgresql.clusters.tasks.read` | Get the detailed information about a task | Manager, Reader, Writer |
| `hyperp-dbaas-postgresql.clusters.configuration.update` | Update the database configuration of your cluster | Manager |
| `hyperp-dbaas-postgresql.clusters.configuration.read` | Show the database configuration of your cluster | Manager, Reader, Writer |
| `hyperp-dbaas-postgresql.backups.cos.enable` | Enable backups to COS | Manager |
| `hyperp-dbaas-postgresql.backups.cos.disable` | Disable backups to COS | Manager |
| `hyperp-dbaas-postgresql.backups.restore` | Restore DB from backup | Manager |
| `hyperp-dbaas-postgresql.backups.cos.read` | Show COS configuration | Manager, Reader, Writer |
{: caption="Table 68. Service actions - Hyper Protect DBaaS for PostgreSQL" caption-side="top"}
{: #actions-table68}
{: tab-title="Actions"}
{: tab-group="hyperp-dbaas-postgresql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IAM Access Management
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iam-access-management` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 69. Platform roles - IAM Access Management" caption-side="top"}
{: #platform-roles-table69}
{: tab-title="Platform roles"}
{: tab-group="iam-access-management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `iam-access-management.settings.read` | Read Access Management account settings | Administrator, Editor, Viewer |
| `iam-access-management.settings.update` | Update Access Management account settings | Administrator |
{: caption="Table 69. Service actions - IAM Access Management" caption-side="top"}
{: #actions-table69}
{: tab-title="Actions"}
{: tab-group="iam-access-management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Role Management
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iam-access-management.customRole` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 70. Platform roles - Role Management" caption-side="top"}
{: #platform-roles-table70}
{: tab-title="Platform roles"}
{: tab-group="iam-access-management.customRole"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `iam-access-management.customRole.create` | The ability to create custom roles. | Administrator |
| `iam-access-management.customRole.update` | The ability to edit and update custom roles. | Administrator, Editor |
| `iam-access-management.customRole.delete` | The ability to delete a custom role. | Administrator |
| `iam-access-management.customRole.read` | Retrieve custom roles | Administrator, Editor, Operator, Viewer |
{: caption="Table 70. Service actions - Role Management" caption-side="top"}
{: #actions-table70}
{: tab-title="Actions"}
{: tab-group="iam-access-management.customRole"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IAM Access Groups
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iam-groups` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can view, create, edit, and delete access groups including adding or removing users from the groups. You can also assign access to the group and manage access for others to work with access groups. |
| Editor | As an editor, you can view, create, edit, and delete access groups including adding or removing users from the groups. |
| Viewer | As a viewer, you can view access groups and its members. |
{: row-headers}
{: caption="Table 71. Platform roles - IAM Access Groups" caption-side="top"}
{: #platform-roles-table71}
{: tab-title="Platform roles"}
{: tab-group="iam-groups"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `iam-groups.groups.create` | Create an access group | Administrator, Editor |
| `iam-groups.groups.read` | Get an access group | Administrator, Editor, Viewer |
| `iam-groups.groups.update` | Update an access group | Administrator, Editor |
| `iam-groups.groups.delete` | Delete an access group | Administrator, Editor |
| `iam-groups.groups.list` | List access groups | Administrator, Editor, Viewer |
| `iam-groups.members.add` | Add members to an access group | Administrator, Editor |
| `iam-groups.members.read` | Check membership in an access group | Administrator, Editor, Viewer |
| `iam-groups.members.delete` | Delete member from an access group | Administrator, Editor |
| `iam-groups.members.list` | List access group members | Administrator, Editor, Viewer |
| `iam-groups.rules.create` | Create rule for an access group | Administrator, Editor |
| `iam-groups.rules.read` | Get an access group rule | Administrator, Editor, Viewer |
| `iam-groups.rules.update` | Update an access group rule | Administrator, Editor |
| `iam-groups.rules.delete` | Delete an access group rule | Administrator, Editor |
| `iam-groups.rules.list` | List access group rules | Administrator, Editor, Viewer |
| `iam-groups.groups.audit` | View access groups audit data | Administrator, Editor, Viewer |
| `iam-groups.account-settings.read` | View access groups account settings | Administrator, Editor, Viewer |
| `iam-groups.account-settings.update` | Update access groups account settings | Administrator |
{: caption="Table 71. Service actions - IAM Access Groups" caption-side="top"}
{: #actions-table71}
{: tab-title="Actions"}
{: tab-group="iam-groups"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IAM Identity Service
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iam-identity` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | An Administrator can view, update and delete service IDs and API keys. |
| Editor | An Editor can view and update service IDs and API keys. |
| Operator | An Operator can view, update and delete service IDs and API keys. |
| Viewer | A Viewer can view service IDs and API keys. |
{: row-headers}
{: caption="Table 72. Platform roles - IAM Identity Service" caption-side="top"}
{: #platform-roles-table72}
{: tab-title="Platform roles"}
{: tab-group="iam-identity"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Service ID creator | Can create service IDs when the account setting to restrict service ID creation is enabled. |
| User API key creator | Can create API keys when the account setting to restrict API key creation is enabled. |
{: row-headers}
{: caption="Table 72. Service roles - IAM Identity Service" caption-side="top"}
{: #service-roles-table72}
{: tab-title="Service roles"}
{: tab-group="iam-identity"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `iam-identity.serviceid.get` | Get the details of an existing service ID. | Administrator, Editor, Operator, Viewer |
| `iam-identity.serviceid.create` | Create a new service ID. | Service ID creator |
| `iam-identity.serviceid.update` | Update the details of an existing service ID. | Administrator, Editor, Operator |
| `iam-identity.serviceid.delete` | Delete a service ID. | Administrator, Operator |
| `iam-identity.apikey.manage` | Manage the API keys of an account. | Administrator |
| `iam-identity.apikey.get` | Get the details of an existing API key. | Administrator, Editor, Operator |
| `iam-identity.apikey.list` | List API keys based on properties. | Administrator, Editor, Operator |
| `iam-identity.apikey.create` | Create a new API key. | Administrator, Operator |
| `iam-identity.apikey.update` | Update the details of an existing API key. | Administrator, Editor, Operator |
| `iam-identity.apikey.delete` | Delete an API key. | Administrator, Operator |
| `iam-identity.user-apikey.create` | Ability to create IBM Cloud API keys associated with a user identity. | User API key creator |
| `iam-identity.profile.create` | Create a new Trusted Profile. | Administrator |
| `iam-identity.profile.update` | Update the details of an existing Trusted Profile. | Administrator, Editor, Operator |
| `iam-identity.profile.delete` | Delete a Trusted Profile. | Administrator, Operator |
| `iam-identity.profile.get` | Get the details of an existing Trusted Profile. | Administrator, Editor, Operator, Viewer |
| `iam-identity.profile.linkToResource` | actiondescription.iam-identity.profile.linkToResource | Administrator, Editor, Operator |
| `iam-identity.idp.get` | Get the details of an existing Identity Provider configuration. | Administrator, Editor, Operator |
| `iam-identity.idp.list` | List Identity Provider configurations. | Administrator, Editor, Operator |
| `iam-identity.idp.create` | Create a new Identity Provider configuration. | Administrator, Operator |
| `iam-identity.idp.update` | Update an existing Identity Provider configuration. | Administrator, Editor, Operator |
| `iam-identity.idp.delete` | Delete an Identity Provider configuration. | Administrator, Operator |
| `iam-identity.idp.test` | Test an Identity Provider configuration. | Administrator, Editor, Operator |
| `iam-identity.idp.metadata` | actiondescription.iam-identity.idp.metadata | Administrator, Editor, Operator |
| `iam-identity.account.get` | Get the account configuration. | Administrator, Editor, Operator, Viewer |
| `iam-identity.account.create` | Create a new account configuration. | Administrator, Operator |
| `iam-identity.account.update` | Update an existing account configuration. | Administrator, Editor, Operator |
| `iam-identity.account.create` | Create a new account configuration. | Administrator, Operator |
| `iam-identity.account.update` | Update an existing account configuration. | Administrator, Editor, Operator |
| `iam-identity.account.enable_idp` | Enable an Identity Provider configuration for the account. | Administrator, Editor, Operator |
| `iam-identity.account.disable_idp` | Disable an Identity Provider configuration for the account. | Administrator, Editor, Operator |
| `iam-identity.account.delete` | Delete an account configuration. | Administrator, Operator |
| `iam-identity.session.manage` | Manage the user sessions of an account. | Administrator |
| `iam-identity.crnmapping.create` | actiondescription.iam-identity.crnmapping.create | Administrator |
| `iam-identity.crnmapping.read` | actiondescription.iam-identity.crnmapping.read | Administrator |
| `iam-identity.crnmapping.delete` | actiondescription.iam-identity.crnmapping.delete | Administrator |
| `iam-identity.activity.get` | actiondescription.iam-identity.activity.get | Administrator, Editor, Operator, Viewer |
| `iam-identity.report.get` | actiondescription.iam-identity.report.get | Administrator |
{: caption="Table 72. Service actions - IAM Identity Service" caption-side="top"}
{: #actions-table72}
{: tab-title="Actions"}
{: tab-group="iam-identity"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Identity and Access Management
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iam-svcs` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 73. Platform roles - Identity and Access Management" caption-side="top"}
{: #platform-roles-table73}
{: tab-title="Platform roles"}
{: tab-group="iam-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `iam-svcs.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 73. Service actions - Identity and Access Management" caption-side="top"}
{: #actions-table73}
{: tab-title="Actions"}
{: tab-group="iam-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Analytics Engine
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `ibmanalyticsengine` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 74. Platform roles - Analytics Engine" caption-side="top"}
{: #platform-roles-table74}
{: tab-title="Platform roles"}
{: tab-group="ibmanalyticsengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 74. Service roles - Analytics Engine" caption-side="top"}
{: #service-roles-table74}
{: tab-title="Service roles"}
{: tab-group="ibmanalyticsengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `ibmae.applications.create` |  | Manager, Writer |
| `ibmae.applications.delete` |  | Manager, Writer |
| `ibmae.applications.read` |  | Manager, Reader, Writer |
| `ibmae.cluster.createlogconfig` |  | Administrator, Editor, Manager, Writer |
| `ibmae.cluster.customize` |  | Administrator, Editor, Manager, Writer |
| `ibmae.cluster.deletelogconfig` |  | Administrator, Editor, Manager, Writer |
| `ibmae.cluster.read` |  | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `ibmae.cluster.resize` |  | Administrator, Editor, Manager, Writer |
| `ibmae.cluster.resetpassword` |  | Administrator, Manager |
| `ibmae.cluster.updatePrivateEndpointAllowlist` |  | Administrator, Editor, Manager, Writer |
| `ibmae.cluster.updatePrivateEndpointWhitelist` |  | Administrator, Editor, Manager, Writer |
| `ibmae.cluster.viewpassword` |  | Administrator, Editor, Manager, Writer |
| `ibmae.instance-logging.create` |  | Manager, Writer |
| `ibmae.instance-logging.delete` |  | Manager, Writer |
| `ibmae.instance-logging.patch` |  | Manager, Writer |
| `ibmae.instance-logging.read` |  | Manager, Reader, Writer |
| `ibmae.instance-logging.update` |  | Manager, Writer |
| `ibmae.instances.patch` |  | Manager, Writer |
| `ibmae.instances.read` |  | Manager, Reader, Writer |
| `ibmae.instances.update` |  | Manager, Writer |
| `ibmae.kernels.create` |  | Manager, Writer |
| `ibmae.kernels.delete` |  | Manager, Writer |
| `ibmae.kernels.read` |  | Manager, Reader, Writer |
| `ibmae.livybatch.create` |  | Manager, Writer |
| `ibmae.livybatch.delete` |  | Manager, Writer |
| `ibmae.livybatch.read` |  | Manager, Reader, Writer |
| `ibmae.sparkhistoryserver.create` |  | Manager, Writer |
| `ibmae.sparkhistoryserver.delete` |  | Manager, Writer |
| `ibmae.sparkhistoryserver.read` |  | Manager, Reader, Writer |
| `ibmae.sparkhistoryui.read` |  | Manager, Reader, Writer |
{: caption="Table 74. Service actions - Analytics Engine" caption-side="top"}
{: #actions-table74}
{: tab-title="Actions"}
{: tab-group="ibmanalyticsengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Cloud Platform
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `ibmcloud-platform` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
| Editor | null |
| Operator | null |
| Viewer | null |
{: row-headers}
{: caption="Table 75. Platform roles - IBM Cloud Platform" caption-side="top"}
{: #platform-roles-table75}
{: tab-title="Platform roles"}
{: tab-group="ibmcloud-platform"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `ibmcloud-platform.osbbroker.create` |  | Administrator, Editor |
| `ibmcloud-platform.osbbroker.update` |  | Administrator, Editor, Operator |
| `ibmcloud-platform.osbbroker.retrieve` |  | Administrator, Editor, Operator, Viewer |
| `ibmcloud-platform.osbbroker.delete` |  | Administrator, Editor |
{: caption="Table 75. Service actions - IBM Cloud Platform" caption-side="top"}
{: #actions-table75}
{: tab-title="Actions"}
{: tab-group="ibmcloud-platform"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Push Notifications
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `imfpush` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 76. Platform roles - Push Notifications" caption-side="top"}
{: #platform-roles-table76}
{: tab-title="Platform roles"}
{: tab-group="imfpush"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 76. Service roles - Push Notifications" caption-side="top"}
{: #service-roles-table76}
{: tab-title="Service roles"}
{: tab-group="imfpush"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `imfpush.dashboard.view` | View Dashboard | Administrator, Editor |
| `imfpush.application.list` | Application list | Manager, Reader, Writer |
| `imfpush.application.delete` | Application delete | Manager |
| `imfpush.device.list` | Device list | Manager, Reader, Writer |
| `imfpush.application.update` | Application update | Manager |
| `imfpush.device.create` | Device create | Manager, Writer |
| `imfpush.device.update` | Device update | Manager, Writer |
| `imfpush.device.delete` | Device delete | Manager |
| `imfpush.messages.send` | Message send | Manager, Writer |
| `imfpush.messages.send` | Message bulk send | Manager, Writer |
| `imfpush.messages.delete` | Message delete | Manager |
| `imfpush.messages.list` | Message list | Manager, Reader, Writer |
| `imfpush.subscriptions.create` | Subscription create | Manager, Writer |
| `imfpush.subscriptions.delete` | Subscription delete | Manager |
| `imfpush.subscriptions.list` | Subscription list | Manager, Reader, Writer |
| `imfpush.tags.create` | Tag create | Manager, Writer |
| `imfpush.tags.update` | Tag update | Manager, Writer |
| `imfpush.tags.delete` | Tag delete | Manager |
| `imfpush.tags.list` | Tag list | Manager, Reader, Writer |
| `imfpush.webhooks.create` | Webhook create | Manager, Writer |
| `imfpush.webhooks.update` | Webhook update | Manager, Writer |
| `imfpush.webhooks.delete` | Webhook delete | Manager |
| `imfpush.webhooks.list` | Webhook list | Manager, Reader, Writer |
| `imfpush.status.update` | Message delivery status update | Manager, Writer |
| `imfpush.channels.create` | Channel creation | Manager, Writer |
| `imfpush.channels.update` | Channel update | Manager, Writer |
| `imfpush.channels.delete` | Channel delete | Manager |
| `imfpush.channels.list` | Channels list | Manager, Reader, Writer |
| `imfpush.channelgroups.create` | Channelgroup create | Manager, Writer |
| `imfpush.channelgroups.update` | Channelgroup update | Manager, Writer |
| `imfpush.channelgroups.delete` | Channelgroup delete | Manager |
| `imfpush.channelgroups.list` | Channelgroup list | Manager, Reader, Writer |
{: caption="Table 76. Service actions - Push Notifications" caption-side="top"}
{: #actions-table76}
{: tab-title="Actions"}
{: tab-group="imfpush"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Cloud Internet Services
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `internet-svcs` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 77. Service roles - Cloud Internet Services" caption-side="top"}
{: #service-roles-table77}
{: tab-title="Service roles"}
{: tab-group="internet-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `internet-svcs.zones.read` | View all zone settings but can't modify them. | Manager, Reader, Writer |
| `internet-svcs.zones.update` | Modify all zone settings but can't create or delete them. | Manager, Writer |
| `internet-svcs.zones.manage` | View, Modify, Create, and Delete all zone settings. | Manager |
| `internet-svcs.reliability.read` | View all Reliability settings but can't modify them. | Manager, Reader, Writer |
| `internet-svcs.reliability.update` | Modify all Reliability settings except for pools and monitors. | Manager, Writer |
| `internet-svcs.reliability.manage` | View, Modify, Create, and Delete all Reliability settings except for pools and monitors. | Manager |
| `internet-svcs.security.read` | View all Security settings except for instance level firewall rules. | Manager, Reader, Writer |
| `internet-svcs.security.update` | Modify all Security settings except for instance level firewall rules. | Manager, Writer |
| `internet-svcs.security.manage` | View, Modify, Create, and Delete all Security settings except for instance level firewall rules. | Manager |
| `internet-svcs.performance.read` | View all Performance settings but can't modify them. | Manager, Reader, Writer |
| `internet-svcs.performance.update` | Modify all Performance settings but cannot create or delete. | Manager, Writer |
| `internet-svcs.performance.manage` | View, Modify, Create, and Delete all Performance settings. | Manager |
{: caption="Table 77. Service actions - Cloud Internet Services" caption-side="top"}
{: #actions-table77}
{: tab-title="Actions"}
{: tab-group="internet-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Internet of Things Platform
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iotf-service` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 78. Platform roles - Internet of Things Platform" caption-side="top"}
{: #platform-roles-table78}
{: tab-title="Platform roles"}
{: tab-group="iotf-service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `iotf-service.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 78. Service actions - Internet of Things Platform" caption-side="top"}
{: #actions-table78}
{: tab-title="Actions"}
{: tab-group="iotf-service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Infrastructure Service
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is` for the service name.

No supported roles.
## Bare Metal Server for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.bare-metal-server` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all functions of an editor and can also assign access policies to other users. |
| Editor | As an editor, you can view, create, edit, delete, update, and perform operator actions on a bare metal server. |
| Operator | As an operator, you can view and perform actions (such as restart) on a bare metal server. |
| Viewer | As a viewer, you can view bare metal servers, but not modify them. |
{: row-headers}
{: caption="Table 80. Platform roles - Bare Metal Server for VPC" caption-side="top"}
{: #platform-roles-table80}
{: tab-title="Platform roles"}
{: tab-group="is.bare-metal-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Bare Metal Advanced Network Operator | As an advanced network operator, you will be permitted access to modify IP Spoofing and Infrastructure NAT on bare metal interfaces |
| Bare Metal Console Admin | As a console admin, you will be able to access the bare metal server console. |
{: row-headers}
{: caption="Table 80. Service roles - Bare Metal Server for VPC" caption-side="top"}
{: #service-roles-table80}
{: tab-title="Service roles"}
{: tab-group="is.bare-metal-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.bare-metal-server.dashboard.view` | . | Administrator, Editor, Operator |
| `is.bare-metal-server.bare-metal-server.read` | This description will need to be re-written. | Administrator, Editor, Operator, Viewer |
| `is.bare-metal-server.bare-metal-server.list` | This description will need to be updated. | Administrator, Editor, Operator, Viewer |
| `is.bare-metal-server.bare-metal-server.update` | This description will need to be updated. | Administrator, Editor |
| `is.bare-metal-server.bare-metal-server.delete` | This description will need to be updated. | Administrator, Editor |
| `is.bare-metal-server.bare-metal-server.create` | This description will need to be updated. | Administrator, Editor |
| `is.bare-metal-server.bare-metal-server.operate` | This description will need to be updated. | Administrator, Editor, Operator |
| `is.bare-metal-server.bare-metal-server.ip-spoofing` | Bare Metal Server IP Spoofing description (crn:v1:bluemix:public:is::::serviceRole:BareMetalAdvancedNetworkOperator) | Bare Metal Advanced Network Operator |
| `is.bare-metal-server.bare-metal-server.infrastructure-nat` | Bare Metal Server Infrastructure NAT description (crn:v1:bluemix:public:is::::serviceRole:BareMetalAdvancedNetworkOperator) | Bare Metal Advanced Network Operator |
| `is.bare-metal-server.bare-metal-server.console` | . | Bare Metal Console Admin |
{: caption="Table 80. Service actions - Bare Metal Server for VPC" caption-side="top"}
{: #actions-table80}
{: tab-title="Actions"}
{: tab-group="is.bare-metal-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Dedicated Host for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.dedicated-host` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 81. Platform roles - Dedicated Host for VPC" caption-side="top"}
{: #platform-roles-table81}
{: tab-title="Platform roles"}
{: tab-group="is.dedicated-host"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.dedicated-host.dashboard.view` | View Dashboard | Administrator, Editor, Operator, Viewer |
| `is.dedicated-host.dedicated-host.list` | List Dedicated Hosts | Administrator, Editor, Operator, Viewer |
| `is.dedicated-host.dedicated-host.create` | Create a Dedicated Host | Administrator, Editor |
| `is.dedicated-host.dedicated-host.update` | Update a Dedicated Host | Administrator, Editor |
| `is.dedicated-host.dedicated-host.delete` | Delete a Dedicated Host | Administrator, Editor |
| `is.dedicated-host.dedicated-host.read` | View a Dedicated Host | Administrator, Editor, Operator, Viewer |
| `is.dedicated-host.dedicated-host.provision` | Provision an Instance on a Dedicated Host | Administrator, Editor, Operator |
| `is.dedicated-host.dedicated-host-group.create` | Create a Dedicated Host Group | Administrator, Editor |
| `is.dedicated-host.dedicated-host-group.read` | View a Dedicated Host Group | Administrator, Editor, Operator, Viewer |
| `is.dedicated-host.dedicated-host-group.update` | Update a Dedicated Host Group | Administrator, Editor |
| `is.dedicated-host.dedicated-host-group.delete` | Delete a Dedicated Host Group | Administrator, Editor |
| `is.dedicated-host.dedicated-host-group.append` | Add a Dedicated Host to a Dedicated Host Group | Administrator, Editor |
| `is.dedicated-host.dedicated-host-group.provision` | Provision an Instance to a Dedicated Host Group | Administrator, Editor, Operator |
| `is.dedicated-host.dedicated-host.operate` | Operate on a Dedicated Host | Administrator, Editor, Operator |
| `is.dedicated-host.dedicated-host-group.operate` | Operate on a Dedicated Host Group | Administrator, Editor, Operator |
| `is.dedicated-host.dedicated-host-group.list` | List Dedicated Host Groups | Administrator, Editor, Operator, Viewer |
{: caption="Table 81. Service actions - Dedicated Host for VPC" caption-side="top"}
{: #actions-table81}
{: tab-title="Actions"}
{: tab-group="is.dedicated-host"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Virtual Private Endpoint for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.endpoint-gateway` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator you can create, delete, update and view endpoint gateway service instances, and assign access policies to other users. Administrators can also bind and unbind an endpoint gateway to a reserved IP address. |
| Editor | As an editor you can create, delete, update and view endpoint gateway service instance. Editors can also bind and unbind an endpoint gateway to a reserved IP address. |
| Operator | As an operator you can bind and unbind an endpoint gateway service instance to a reserved IP address. You can also view the properties of endpoint gateways but you cannot modify them. |
| Viewer | 	As a viewer you can view the properties of endpoint gateway service instances, but you cannot modify them. |
{: row-headers}
{: caption="Table 82. Platform roles - Virtual Private Endpoint for VPC" caption-side="top"}
{: #platform-roles-table82}
{: tab-title="Platform roles"}
{: tab-group="is.endpoint-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.endpoint-gateway.endpoint-gateway.read` | View Endpoint Gateway | Administrator, Editor, Operator, Viewer |
| `is.endpoint-gateway.endpoint-gateway.create` | Create Endpoint Gateway | Administrator, Editor |
| `is.endpoint-gateway.endpoint-gateway.delete` | Delete Endpoint Gateway | Administrator, Editor |
| `is.endpoint-gateway.endpoint-gateway.update` | Update Endpoint Gateway | Administrator, Editor |
| `is.endpoint-gateway.endpoint-gateway.list` | List Endpoint Gateways | Administrator, Editor, Operator, Viewer |
| `is.endpoint-gateway.endpoint-gateway.operate` | Operate Endpoint Gateway | Administrator, Editor, Operator |
{: caption="Table 82. Service actions - Virtual Private Endpoint for VPC" caption-side="top"}
{: #actions-table82}
{: tab-title="Actions"}
{: tab-group="is.endpoint-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Floating IP for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.floating-ip` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 83. Platform roles - Floating IP for VPC" caption-side="top"}
{: #platform-roles-table83}
{: tab-title="Platform roles"}
{: tab-group="is.floating-ip"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.floating-ip.floating-ip.create` |  | Administrator, Editor |
| `is.floating-ip.floating-ip.delete` |  | Administrator, Editor |
| `is.floating-ip.floating-ip.update` |  | Administrator, Editor |
| `is.floating-ip.floating-ip.operate` |  | Administrator, Editor, Operator |
| `is.floating-ip.floating-ip.read` |  | Administrator, Editor, Operator, Viewer |
| `is.floating-ip.floating-ip.list` |  | Administrator, Editor, Operator, Viewer |
{: caption="Table 83. Service actions - Floating IP for VPC" caption-side="top"}
{: #actions-table83}
{: tab-title="Actions"}
{: tab-group="is.floating-ip"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Cloud Flow Logs for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.flow-log-collector` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 84. Platform roles - IBM Cloud Flow Logs for VPC" caption-side="top"}
{: #platform-roles-table84}
{: tab-title="Platform roles"}
{: tab-group="is.flow-log-collector"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.flow-log-collector.flow-log-collector.read` | As an administrator, an editor, an operator or a viewer, you can view the details of a flow log collector | Administrator, Editor, Operator, Viewer |
| `is.flow-log-collector.flow-log-collector.update` | As an administrator or an editor, you can update a flow log collector | Administrator, Editor |
| `is.flow-log-collector.flow-log-collector.operate` | As an administrator, an editor or an operator, you can operate on a flow log collector | Administrator, Editor, Operator |
| `is.flow-log-collector.flow-log-collector.create` | As an administrator or an editor, you can create a flow log collector | Administrator, Editor |
| `is.flow-log-collector.flow-log-collector.delete` | As an administrator or an editor, you can delete a flow log collector | Administrator, Editor |
| `is.flow-log-collector.flow-log-collector.list` | List Flow Log Collectors | Administrator, Editor, Operator, Viewer |
{: caption="Table 84. Service actions - IBM Cloud Flow Logs for VPC" caption-side="top"}
{: #actions-table84}
{: tab-title="Actions"}
{: tab-group="is.flow-log-collector"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Image Service for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.image` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 85. Platform roles - Image Service for VPC" caption-side="top"}
{: #platform-roles-table85}
{: tab-title="Platform roles"}
{: tab-group="is.image"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.image.image.list` | List Images | Administrator, Editor, Operator, Viewer |
| `is.image.image.read` | Read Images | Administrator, Editor, Operator, Viewer |
| `is.image.image.create` | Create Images | Administrator, Editor |
| `is.image.image.update` | Update Images | Administrator, Editor |
| `is.image.image.delete` | Delete Images | Administrator, Editor |
| `is.image.image.provision` | Provision Images | Administrator, Editor, Operator |
| `is.image.image.operate` | Operate on Custom Images | Administrator, Editor, Operator |
{: caption="Table 85. Service actions - Image Service for VPC" caption-side="top"}
{: #actions-table85}
{: tab-title="Actions"}
{: tab-group="is.image"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Virtual Server for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.instance` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 86. Platform roles - Virtual Server for VPC" caption-side="top"}
{: #platform-roles-table86}
{: tab-title="Platform roles"}
{: tab-group="is.instance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Console Administrator | As a console administrator, you can access the virtual server instance console., This role only provides console access and must be combined with another role that has operator access to the virtual server such as Operator, Editor or Administrator. |
| IP Spoofing Operator | As the IP spoofing operator, you can enable or disable the IP spoofing check on virtual server instances. This role should only be granted if necessary.  |
{: row-headers}
{: caption="Table 86. Service roles - Virtual Server for VPC" caption-side="top"}
{: #service-roles-table86}
{: tab-title="Service roles"}
{: tab-group="is.instance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.instance.instance.list` | List Virtual Server Instance | Administrator, Editor, Operator, Viewer |
| `is.instance.instance.create` | Create Virtual Server Instance | Administrator, Editor |
| `is.instance.instance.read` | View Virtual Server Instance | Administrator, Editor, Operator, Viewer |
| `is.instance.instance.update` | Update Virtual Server Instance | Administrator, Editor |
| `is.instance.instance.delete` | Delete Virtual Server Instance | Administrator, Editor |
| `is.instance.instance.operate` | As an administrator, an editor or an operator, you can operate on a virtual server instance | Administrator, Editor, Operator |
| `is.instance.instance-template.read` | View Virtual Server Instance Template | Administrator, Editor, Operator, Viewer |
| `is.instance.instance-template.create` | Create Virtual Server Instance Template | Administrator, Editor |
| `is.instance.instance-template.update` | Update Virtual Server Instance Template | Administrator, Editor |
| `is.instance.instance-template.delete` | Delete Virtual Server Instance Template | Administrator, Editor |
| `is.instance.instance.ip-spoofing` | IP spoofing control for Virtual Server Instance | IP Spoofing Operator |
| `is.instance.instance.console` | Access Virtual Server Instance Console | Console Administrator |
{: caption="Table 86. Service actions - Virtual Server for VPC" caption-side="top"}
{: #actions-table86}
{: tab-title="Actions"}
{: tab-group="is.instance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Auto Scale for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.instance-group` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 87. Platform roles - Auto Scale for VPC" caption-side="top"}
{: #platform-roles-table87}
{: tab-title="Platform roles"}
{: tab-group="is.instance-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.instance-group.instance-group.read` | Read an Instance Group | Administrator, Editor, Operator, Viewer |
| `is.instance-group.instance-group.create` | Create an Instance Group | Administrator, Editor |
| `is.instance-group.instance-group.update` | Update an Instance Group | Administrator, Editor |
| `is.instance-group.instance-group.delete` | Delete an Instance Group | Administrator, Editor |
| `is.instance-group.instance-group.list` | List Instance Groups | Administrator, Editor, Operator, Viewer |
{: caption="Table 87. Service actions - Auto Scale for VPC" caption-side="top"}
{: #actions-table87}
{: tab-title="Actions"}
{: tab-group="is.instance-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## SSH Key for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.key` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 88. Platform roles - SSH Key for VPC" caption-side="top"}
{: #platform-roles-table88}
{: tab-title="Platform roles"}
{: tab-group="is.key"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.key.key.list` | List SSH Keys | Administrator, Editor, Operator, Viewer |
| `is.key.key.create` | Create SSH Key | Administrator, Editor |
| `is.key.key.delete` | Delete SSH Key | Administrator, Editor |
| `is.key.key.read` | View SSH Key | Administrator, Editor, Operator, Viewer |
| `is.key.key.update` | Update SSH Key | Administrator, Editor |
| `is.key.artifactattachment.create` | Create Artifact Attachment | Administrator, Editor |
| `is.key.artifactattachment.update` | Update Artifact Attachment | Administrator, Editor |
| `is.key.artifactattachment.delete` | Delete Artifact Attachment | Administrator, Editor |
| `is.key.userdata.list` | List User Data | Administrator, Editor, Operator |
| `is.key.userdata.create` | Create User Data | Administrator, Editor |
| `is.key.userdata.delete` | Delete User Data | Administrator, Editor |
| `is.key.userdata.read` | Read User Data | Administrator, Editor, Operator, Viewer |
| `is.key.artifactattachment.read` | Read Artifact Attachment | Administrator, Editor, Operator, Viewer |
| `is.key.key.operate` | Operate on Key | Administrator, Editor, Operator |
{: caption="Table 88. Service actions - SSH Key for VPC" caption-side="top"}
{: #actions-table88}
{: tab-title="Actions"}
{: tab-group="is.key"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Load Balancer for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.load-balancer` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 89. Platform roles - Load Balancer for VPC" caption-side="top"}
{: #platform-roles-table89}
{: tab-title="Platform roles"}
{: tab-group="is.load-balancer"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.load-balancer.load-balancer.view` | View load balancers | Administrator, Editor, Operator, Viewer |
| `is.load-balancer.load-balancer.manage` |  | Administrator, Editor |
| `is.load-balancer.load-balancer.operate` | Operator permissions for load balancers | Administrator, Editor, Operator |
{: caption="Table 89. Service actions - Load Balancer for VPC" caption-side="top"}
{: #actions-table89}
{: tab-title="Actions"}
{: tab-group="is.load-balancer"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Network ACL
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.network-acl` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 90. Platform roles - Network ACL" caption-side="top"}
{: #platform-roles-table90}
{: tab-title="Platform roles"}
{: tab-group="is.network-acl"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.network-acl.network-acl.read` |  | Administrator, Editor, Operator, Viewer |
| `is.network-acl.network-acl.create` |  | Administrator, Editor |
| `is.network-acl.network-acl.update` |  | Administrator, Editor |
| `is.network-acl.network-acl.delete` |  | Administrator, Editor |
| `is.network-acl.network-acl.list` |  | Administrator, Editor, Operator, Viewer |
| `is.network-acl.network-acl.operate` |  | Administrator, Editor, Operator |
{: caption="Table 90. Service actions - Network ACL" caption-side="top"}
{: #actions-table90}
{: tab-title="Actions"}
{: tab-group="is.network-acl"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Placement Groups for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.placement-group` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 91. Platform roles - Placement Groups for VPC" caption-side="top"}
{: #platform-roles-table91}
{: tab-title="Platform roles"}
{: tab-group="is.placement-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.placement-group.dashboard.view` | View Dashboard | Administrator, Editor, Operator |
| `is.placement-group.placement-group.create` | Create a virtual instance placement group | Administrator, Editor |
| `is.placement-group.placement-group.update` | Update the name of a virtual instance placement group | Administrator, Editor |
| `is.placement-group.placement-group.delete` | Delete a virtual instance placement group | Administrator, Editor |
| `is.placement-group.placement-group.operate` | Add or remove an instance to or from a placement group | Administrator, Editor, Operator |
| `is.placement-group.placement-group.read` | View the details of a virtual instance placement group | Administrator, Editor, Operator, Viewer |
| `is.placement-group.placement-group.list` | List all placements groups associated for this account | Administrator, Editor, Operator, Viewer |
{: caption="Table 91. Service actions - Placement Groups for VPC" caption-side="top"}
{: #actions-table91}
{: tab-title="Actions"}
{: tab-group="is.placement-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Public Gateway
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.public-gateway` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 92. Platform roles - Public Gateway" caption-side="top"}
{: #platform-roles-table92}
{: tab-title="Platform roles"}
{: tab-group="is.public-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.public-gateway.public-gateway.read` |  | Administrator, Editor, Operator, Viewer |
| `is.public-gateway.public-gateway.create` |  | Administrator, Editor |
| `is.public-gateway.public-gateway.update` |  | Administrator, Editor |
| `is.public-gateway.public-gateway.delete` |  | Administrator, Editor |
| `is.public-gateway.public-gateway.list` |  | Administrator, Editor, Operator, Viewer |
| `is.public-gateway.public-gateway.operate` |  | Administrator, Editor, Operator |
{: caption="Table 92. Service actions - Public Gateway" caption-side="top"}
{: #actions-table92}
{: tab-title="Actions"}
{: tab-group="is.public-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Security Group for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.security-group` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 93. Platform roles - Security Group for VPC" caption-side="top"}
{: #platform-roles-table93}
{: tab-title="Platform roles"}
{: tab-group="is.security-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.security-group.security-group.create` |  | Administrator, Editor |
| `is.security-group.security-group.read` |  | Administrator, Editor, Operator, Viewer |
| `is.security-group.security-group.update` |  | Administrator, Editor |
| `is.security-group.security-group.delete` |  | Administrator, Editor |
| `is.security-group.security-group.operate` |  | Administrator, Editor, Operator |
{: caption="Table 93. Service actions - Security Group for VPC" caption-side="top"}
{: #actions-table93}
{: tab-title="Actions"}
{: tab-group="is.security-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Block Storage Snapshots for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.snapshot` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can create, view, list, modify, delete and restore block storage snapshots, including assigning access policies to other users. |
| Editor | As an editor, you can create, view, list, modify, delete and restore block storage snapshots, except for assigning access policies to other users. |
| Operator | As an operator, you can view, list and restore block storage snapshots, but you can't modify them. |
| Viewer | As a viewer, you can view and list block storage snapshots, but you can't modify them. |
{: row-headers}
{: caption="Table 94. Platform roles - Block Storage Snapshots for VPC" caption-side="top"}
{: #platform-roles-table94}
{: tab-title="Platform roles"}
{: tab-group="is.snapshot"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.snapshot.snapshot.create` | This action allows the user to create block storage snapshots. | Administrator, Editor |
| `is.snapshot.snapshot.read` | This action allows the user to view block storage snapshots , but not modify them. | Administrator, Editor, Operator, Viewer |
| `is.snapshot.snapshot.list` | This action allows the user to list snapshot resources. | Administrator, Editor, Operator, Viewer |
| `is.snapshot.snapshot.update` | This action allows the user to modify block storage snapshots. | Administrator, Editor |
| `is.snapshot.snapshot.delete` | This action allows the user to delete block storage snapshots. | Administrator, Editor |
| `is.snapshot.snapshot.restore` | This action allows the user to restore block storage snapshots. | Administrator, Editor, Operator |
| `is.snapshot.snapshot.operate` | Operate a snapshot | Administrator, Editor, Operator |
| `is.snapshot.clone.create` | Create clones of block storage snapshots for fast restoration | Administrator, Editor |
| `is.snapshot.clone.read` | View the clones of block storage snapshots | Administrator, Editor, Operator, Viewer |
| `is.snapshot.clone.delete` | Delete clones of block storage snapshots | Administrator, Editor |
{: caption="Table 94. Service actions - Block Storage Snapshots for VPC" caption-side="top"}
{: #actions-table94}
{: tab-title="Actions"}
{: tab-group="is.snapshot"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Subnet
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.subnet` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 95. Platform roles - Subnet" caption-side="top"}
{: #platform-roles-table95}
{: tab-title="Platform roles"}
{: tab-group="is.subnet"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.subnet.subnet.create` |  | Administrator, Editor |
| `is.subnet.subnet.read` |  | Administrator, Editor, Operator, Viewer |
| `is.subnet.subnet.update` |  | Administrator, Editor |
| `is.subnet.subnet.delete` |  | Administrator, Editor |
| `is.subnet.subnet.list` |  | Administrator, Editor, Operator, Viewer |
| `is.subnet.subnet.operate` |  | Administrator, Editor, Operator |
{: caption="Table 95. Service actions - Subnet" caption-side="top"}
{: #actions-table95}
{: tab-title="Actions"}
{: tab-group="is.subnet"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Block Storage for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.volume` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 96. Platform roles - Block Storage for VPC" caption-side="top"}
{: #platform-roles-table96}
{: tab-title="Platform roles"}
{: tab-group="is.volume"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.volume.profile.view` |  | Administrator, Editor, Operator, Viewer |
| `is.volume.volume.create` |  | Administrator, Editor |
| `is.volume.volume.list` |  | Administrator, Editor, Operator, Viewer |
| `is.volume.volume.read` |  | Administrator, Editor, Operator, Viewer |
| `is.volume.volume.update` |  | Administrator, Editor |
| `is.volume.volume.delete` |  | Administrator, Editor |
| `is.volume.volume.operate` | Operate a volume | Administrator, Editor, Operator |
{: caption="Table 96. Service actions - Block Storage for VPC" caption-side="top"}
{: #actions-table96}
{: tab-title="Actions"}
{: tab-group="is.volume"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Virtual Private Cloud
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.vpc` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 97. Platform roles - Virtual Private Cloud" caption-side="top"}
{: #platform-roles-table97}
{: tab-title="Platform roles"}
{: tab-group="is.vpc"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.vpc.vpc.read` | View a Virtual Private Cloud (VPC) | Administrator, Editor, Operator, Viewer |
| `is.vpc.vpc.create` | Create a Virtual Private Cloud (VPC) | Administrator, Editor |
| `is.vpc.vpc.delete` | Delete a Virtual Private Cloud (VPC) | Administrator, Editor |
| `is.vpc.vpc.update` | Update a Virtual Private Cloud (VPC) | Administrator, Editor |
| `is.vpc.vpc.list` | List Virtual Private Clouds (VPC) | Administrator, Editor, Operator, Viewer |
| `is.vpc.vpc.operate` | Operate a Virtual Private Clouds (VPC) | Administrator, Editor, Operator |
{: caption="Table 97. Service actions - Virtual Private Cloud" caption-side="top"}
{: #actions-table97}
{: tab-title="Actions"}
{: tab-group="is.vpc"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## VPN for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.vpn` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 98. Platform roles - VPN for VPC" caption-side="top"}
{: #platform-roles-table98}
{: tab-title="Platform roles"}
{: tab-group="is.vpn"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.vpn.vpn.create` |  | Administrator, Editor |
| `is.vpn.vpn.update` |  | Administrator, Editor |
| `is.vpn.vpn.delete` |  | Administrator, Editor |
| `is.vpn.vpn.read` |  | Administrator, Editor, Operator, Viewer |
| `is.vpn.vpn.list` |  | Administrator, Editor, Operator, Viewer |
| `is.vpn.dashboard.view` |  | Administrator, Editor, Operator, Viewer |
{: caption="Table 98. Service actions - VPN for VPC" caption-side="top"}
{: #actions-table98}
{: tab-title="Actions"}
{: tab-group="is.vpn"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## VPN Server for VPC
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.vpn-server` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 99. Platform roles - VPN Server for VPC" caption-side="top"}
{: #platform-roles-table99}
{: tab-title="Platform roles"}
{: tab-group="is.vpn-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| VPN Client | Users of the VPN server need this role to connect to the VPN server |
{: row-headers}
{: caption="Table 99. Service roles - VPN Server for VPC" caption-side="top"}
{: #service-roles-table99}
{: tab-title="Service roles"}
{: tab-group="is.vpn-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.vpn-server.dashboard.view` | View Dashboard | Administrator, Editor, Operator, Viewer |
| `is.vpn-server.vpn-server.create` | Create VPN server
 | Administrator, Editor |
| `is.vpn-server.vpn-server.delete` | Delete VPN server
 | Administrator, Editor |
| `is.vpn-server.vpn-server.operate` | Operate VPN server
 | Administrator, Editor, Operator |
| `is.vpn-server.vpn-server.read` | View VPN server
 | Administrator, Editor, Operator, Viewer |
| `is.vpn-server.vpn-server.update` | Update VPN server
 | Administrator, Editor |
| `is.vpn-server.vpn-server.connect` | Connect to VPN server | VPN Client |
{: caption="Table 99. Service actions - VPN Server for VPC" caption-side="top"}
{: #actions-table99}
{: tab-title="Actions"}
{: tab-group="is.vpn-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Key Protect
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `kms` for the service name.

| Role | Description |
| ----- | :----- |
| KeyPurge | Role for purging key. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| ReaderPlus | As a reader plus, you can perform read-only actions within Key Protect such as viewing service-specific resources. You can also access key material for standard keys. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 100. Service roles - IBM Key Protect" caption-side="top"}
{: #service-roles-table100}
{: tab-title="Service roles"}
{: tab-group="kms"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `kms.secrets.create` | Create an encryption key. | Manager, Writer |
| `kms.secrets.read` | Retrieve an encryption key. | Manager, ReaderPlus, Writer |
| `kms.secrets.list` | Retrieve a list of encryption keys. | Manager, Reader, ReaderPlus, Writer |
| `kms.secrets.delete` | Delete an encryption key. | Manager |
| `kms.secrets.wrap` | Wrap an encryption key. | Manager, Reader, ReaderPlus, Writer |
| `kms.secrets.unwrap` | Unwrap an encryption key. | Manager, Reader, ReaderPlus, Writer |
| `kms.secrets.rotate` | Rotate an encryption key. | Manager, Writer |
| `kms.lockers.read` | Read lockers | Manager, Writer |
| `kms.lockers.create` | Create lockers | Manager, Writer |
| `kms.lockers.list` | List lockers | Manager, Writer |
| `kms.policies.read` | Retrieve policies for an encryption key. | Manager |
| `kms.policies.write` | Set policies for an encryption key. | Manager |
| `kms.secrets.rewrap` | Rewrap an encryption key. | Manager, Reader, ReaderPlus, Writer |
| `kms.importtoken.read` | Retrieve an import token. | Manager, Writer |
| `kms.importtoken.create` | Create an import token. | Manager, Writer |
| `kms.registrations.list` | Retrieve a list of registrations. | Manager, Reader, ReaderPlus, Writer |
| `kms.registrations.listforkey` | Retrieve a list of registrations for a given encryption key. | Manager, Reader, ReaderPlus, Writer |
| `kms.registrations.delete` | Delete a registration. | Manager, Reader, ReaderPlus, Writer |
| `kms.registrations.merge` | Update the details of an existing registration. | Manager, Reader, ReaderPlus, Writer |
| `kms.registrations.write` | Replace an existing registration. | Manager, Reader, ReaderPlus, Writer |
| `kms.registrations.create` | Create a registration between an encryption key and a cloud resource. | Manager, Reader, ReaderPlus, Writer |
| `kms.registrations.deactivate` | Move a suspended registration to the deactivated state | Manager, Reader, ReaderPlus, Writer |
| `kms.instancepolicies.read` | Retrieve instance level policies. | Manager |
| `kms.instancepolicies.write` | Add or update instance level policies. | Manager |
| `kms.secrets.setkeyfordeletion` | Set or prepare an encryption key for deletion. | Manager, Writer |
| `kms.secrets.unsetkeyfordeletion` | Unset an encryption key for deletion. | Manager, Writer |
| `kms.secrets.readmetadata` | Retrieve the details of an encryption key. | Manager, Reader, ReaderPlus, Writer |
| `kms.secrets.listkeyversions` | Retrieve a list of versions that are associated with an encryption key. | Manager, Reader, ReaderPlus, Writer |
| `kms.keyversions.list` | Retrieve a list of versions that are associated with an encryption key. | Manager, Reader, ReaderPlus, Writer |
| `kms.secrets.restore` | Restore a previously deleted encryption key. | Manager |
| `kms.secrets.disable` | Disable operations for an encryption key. | Manager |
| `kms.secrets.enable` | Enable operations for an encryption key. | Manager |
| `kms.secrets.eventack` | Acknowledge a key lifecycle event | Manager, Reader, ReaderPlus, Writer |
| `kms.instance.readipwhitelistport` | Retrieve port associated with instance level ip whitelist policy. | Manager |
| `kms.instance.readallowedipport` | Retrieve port associated with instance level allowed IP policy. | Manager |
| `kms.secrets.sync` | Initiate a manual data synchronization request to the associated resources of a key. | Manager, Writer |
| `kms.secrets.createalias` | Create an alias for an encryption key. | Manager, Writer |
| `kms.secrets.deletealias` |  Delete an alias for an encryption key. | Manager, Writer |
| `kms.keyrings.list` | Retrieve a list of key rings in the instance. | Manager, Reader, ReaderPlus, Writer |
| `kms.keyrings.create` | Create a key ring in the instance. | Manager, Writer |
| `kms.keyrings.delete` | Delete a key ring in the instance. | Manager |
| `kms.secrets.purge` | Purge an encryption key. | KeyPurge |
| `kms.secrets.patch` | Patch attributes of an encryption key. | Manager |
{: caption="Table 100. Service actions - IBM Key Protect" caption-side="top"}
{: #actions-table100}
{: tab-title="Actions"}
{: tab-group="kms"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Knowledge Studio
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `knowledge-studio` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 101. Platform roles - Knowledge Studio" caption-side="top"}
{: #platform-roles-table101}
{: tab-title="Platform roles"}
{: tab-group="knowledge-studio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 101. Service roles - Knowledge Studio" caption-side="top"}
{: #service-roles-table101}
{: tab-title="Service roles"}
{: tab-group="knowledge-studio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `knowledge-studio.dashboard.view` |  | Administrator, Editor, Manager, Reader, Viewer, Writer |
{: caption="Table 101. Service actions - Knowledge Studio" caption-side="top"}
{: #actions-table101}
{: tab-title="Actions"}
{: tab-group="knowledge-studio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Language Translator
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `language-translator` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 102. Service roles - Language Translator" caption-side="top"}
{: #service-roles-table102}
{: tab-title="Service roles"}
{: tab-group="language-translator"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /language-translator` |  | Manager, Reader, Writer |
| `POST /language-translator` |  | Manager, Reader, Writer |
| `DELETE /language-translator` |  | Manager, Writer |
{: caption="Table 102. Service actions - Language Translator" caption-side="top"}
{: #actions-table102}
{: tab-title="Actions"}
{: tab-group="language-translator"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Log Analysis with LogDNA
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `logdna` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 103. Platform roles - IBM Log Analysis with LogDNA" caption-side="top"}
{: #platform-roles-table103}
{: tab-title="Platform roles"}
{: tab-group="logdna"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you can manage resources, configure views, dashboards and alerts, export data, search, filter, and view all data. |
| Reader | As a reader, you can perform read-only actions such as monitor data through views and dashboards. |
| Standard Member | As a member, you can configure views, dashboards and alerts, export data, search, filter, and view all data. |
{: row-headers}
{: caption="Table 103. Service roles - IBM Log Analysis with LogDNA" caption-side="top"}
{: #service-roles-table103}
{: tab-title="Service roles"}
{: tab-group="logdna"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `logdna.dashboard.view` | View LogDNA Dashboard | Administrator, Manager, Reader, Standard Member |
| `logdna.dashboard.read` | Access LogDNA dashboard without any edit permission | Reader |
| `logdna.dashboard.member` | Access LogDNA dashboard with limited edit capabilities | Standard Member |
| `logdna.dashboard.manage` | Access and manage LogDNA dashboard without any limitation | Administrator, Manager |
{: caption="Table 103. Service actions - IBM Log Analysis with LogDNA" caption-side="top"}
{: #actions-table103}
{: tab-title="Actions"}
{: tab-group="logdna"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Cloud Activity Tracker with LogDNA
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `logdnaat` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 104. Platform roles - IBM Cloud Activity Tracker with LogDNA" caption-side="top"}
{: #platform-roles-table104}
{: tab-title="Platform roles"}
{: tab-group="logdnaat"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you can manage resources, configure views, dashboards and alerts, export data, search, filter, and view all data. |
| Reader | As a reader, you can perform read-only actions such as monitor data through views and dashboards. |
| Standard member | As a member, you can configure views, dashboards and alerts, export data, search, filter, and view all data. |
{: row-headers}
{: caption="Table 104. Service roles - IBM Cloud Activity Tracker with LogDNA" caption-side="top"}
{: #service-roles-table104}
{: tab-title="Service roles"}
{: tab-group="logdnaat"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `logdnaat.dashboard.view` | View LogDNA Dashboard | Administrator, Manager, Reader, Standard member |
| `logdnaat.dashboard.read` | Access LogDNA dashboard without any edit permission | Reader |
| `logdnaat.dashboard.member` | Access LogDNA dashboard with limited edit capabilities | Standard member |
| `logdnaat.dashboard.manage` | Access and manage LogDNA dashboard without any limitation | Administrator, Manager |
{: caption="Table 104. Service actions - IBM Cloud Activity Tracker with LogDNA" caption-side="top"}
{: #actions-table104}
{: tab-title="Actions"}
{: tab-group="logdnaat"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Managed Solutions
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `managed-solutions` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 105. Platform roles - Managed Solutions" caption-side="top"}
{: #platform-roles-table105}
{: tab-title="Platform roles"}
{: tab-group="managed-solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 105. Service roles - Managed Solutions" caption-side="top"}
{: #service-roles-table105}
{: tab-title="Service roles"}
{: tab-group="managed-solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `managed-solutions.overview.view` | View the Managed Solutions dashboard. | Administrator, Editor, Operator, Viewer |
| `managed-solutions.support.view-dashboard` | View the Support Dashboard. | Administrator, Editor, Operator, Viewer |
| `managed-solutions.onboarding.link-services` | Link Managed Solutions to your IBM Cloud Account. | Administrator |
| `managed-solutions.sap-landscapes.view` | View SAP Landscapes | Administrator, Editor, Operator, Reader, Viewer |
| `managed-solutions.support.view` | View Support Artifacts | Administrator, Editor, Operator, Viewer |
| `managed-solutions.support.manage` | Add/Edit Support Cases | Administrator, Editor, Operator |
| `managed-solutions.sap-systems.view` | View SAP Systems | Administrator, Editor, Operator, Viewer |
| `managed-solutions.sap-servers.view` | View SAP Servers | Administrator, Editor, Operator, Viewer |
| `managed-solutions.health-alerts.view` | View Health Alerts | Administrator, Editor, Operator, Viewer |
| `managed-solutions.support.manage-settings` | Managed Support Settings | Administrator |
| `managed-solutions.oracle-applications.view` | View Oracle Applications | Viewer |
| `managed-solutions.support.manage-change-approvers` | Manages who can approve cases for a solution. | Administrator, Manager |
| `managed-solutions.support.manage-subscriptions` | Manage Support API Subscriptions | Administrator, Editor |
| `managed-solutions.platform.view` | Allows access to view Managed Solutions that are not IAM enabled. | Administrator, Editor, Operator, Viewer |
| `managed-solutions.solution.view` | View Managed Solutions, but not necessarily data associated with the solutions. | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `managed-solutions.support.manage-cases` | Managed Support Cases for a Solution | Manager, Writer |
| `managed-solutions.solution.enable-iam` | Allows enable Access Control (IAM) for Solutions. | Administrator, Editor |
| `managed-solutions.support.view-cases` | Allows viewing support cases for a solution. | Manager, Reader, Writer |
| `managed-solutions.platform.operate` | Allows access to operate Managed Solutions that are not IAM enabled. | Administrator, Editor, Operator |
| `managed-solutions.platform.administrate` | Perform administrative functions on non-IAM enabled solutions. | Administrator |
| `managed-solutions.sap-instances.view` | View SAP Instances | Administrator, Editor, Operator, Viewer |
| `managed-solutions.health.view-alerts` | View Alerts | Manager, Reader, Writer |
| `managed-solutions.core.manage-host-credentials` | Manage credentials on the host. | Administrator, Manager |
{: caption="Table 105. Service actions - Managed Solutions" caption-side="top"}
{: #actions-table105}
{: tab-title="Actions"}
{: tab-group="managed-solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Mass Data Migration
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `mass-data-migration` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 106. Platform roles - Mass Data Migration" caption-side="top"}
{: #platform-roles-table106}
{: tab-title="Platform roles"}
{: tab-group="mass-data-migration"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 106. Service roles - Mass Data Migration" caption-side="top"}
{: #service-roles-table106}
{: tab-title="Service roles"}
{: tab-group="mass-data-migration"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `mass-data-migration.dashboard.view` |  | Administrator, Editor, Operator |
| `mass-data-migration.order.place` | Can place order | Manager, Writer |
{: caption="Table 106. Service actions - Mass Data Migration" caption-side="top"}
{: #actions-table106}
{: tab-title="Actions"}
{: tab-group="mass-data-migration"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Event Streams
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `messagehub` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 107. Service roles - Event Streams" caption-side="top"}
{: #service-roles-table107}
{: tab-title="Service roles"}
{: tab-group="messagehub"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `messagehub.topic.read` | Allow an app to read messages from all topics, or if applied to a named topic, then just that single topic. | Manager, Reader, Writer |
| `messagehub.topic.write` | Allow an app to write messages to all topics, or if applied to a named topic, then just that single topic. | Manager, Writer |
| `messagehub.topic.manage` | Allow an app or user to create or delete topic. If applied to a named topic, then only topics of that name can be created or deleted. | Manager |
| `messagehub.cluster.read` | Allow an app to connect to a service instance and read its state, including listing consumer groups, topics and offsets and describing consumer groups, topics and broker configurations. | Manager, Reader, Writer |
| `messagehub.group.read` | Allow an app to join and commit offsets in a consumer group. | Manager, Reader, Writer |
| `messagehub.group.manage` | Allow an app or user to delete a Consumer Group. If applied to a group ID, then only the consumer group with that ID can be deleted. | Manager |
| `messagehub.txnid.write` | Allow an app to produce messages transactionally. | Manager, Writer |
| `messagehub.schema.read` | Read a schema/schema version | Manager, Reader, Writer |
| `messagehub.schema.write` | Create a schema/schema version | Manager, Writer |
| `messagehub.schema.manage` | Delete a schema/schema version | Manager |
| `messagehub.cluster.manage` | Manage the configuration of an Event Streams instance | Manager |
| `messagehub.config.read` | Configuration Information Point API access | Manager, Reader, Writer |
{: caption="Table 107. Service actions - Event Streams" caption-side="top"}
{: #actions-table107}
{: tab-title="Actions"}
{: tab-group="messagehub"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Messages for RabbitMQ
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `messages-for-rabbitmq` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 108. Platform roles - Messages for RabbitMQ" caption-side="top"}
{: #platform-roles-table108}
{: tab-title="Platform roles"}
{: tab-group="messages-for-rabbitmq"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /2017-12/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `DELETE /2017-12/:platform/deployments/:deployment_id` | Remove a Deployment | Administrator, Editor, Operator |
| `GET /2017-12/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /2017-12/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /2017-12/:platform/clusters/:cluster_id/deployments` | Create a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/users` | Create a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id` | Read a DeploymentUser | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id` | Update a DeploymentUser | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/users/:user_id` | Remove a DeploymentUser | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/regions` | Read Discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/remotes` | Update a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/promotion` | Promote a remote replica | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/remotes/resync` | Resync remote replica | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v5/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration/schema` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/network` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/groups` | Read Groups | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id` | Update a Group | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/groups/:group_id/autoscaling` | Update autoscaling configuration | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Read Whitelisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Create a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id` | Remove a Whitelisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/whitelists/ip_addresses` | Bulk whitelist IP addresses | Administrator, Editor, Operator |
| `POST /v5/:platform/capability/:capability_id` | Discover a supported capability | Administrator, Editor, Operator |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type` | Create a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Update a type of user | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id` | Delete a type of user | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/users/:user_type/:user_id/connections/:endpoint_type` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `POST /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `DELETE /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses/:ip_address_id` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `PUT /v5/:platform/deployments/:deployment_id/allowlists/ip_addresses` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id/capability/:capability_id` | Read a capability | Administrator, Editor, Operator, Viewer |
| `task.read` | Read a Task | Administrator, Editor, Operator, Viewer |
| `backup.read` | Read a Backup | Administrator, Editor, Operator, Viewer |
| `deployment.read` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `deployment.update` | Update a Deployment | Administrator, Editor, Operator |
| `deployment-point-in-time-recovery-data.list` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `deployment-task.list` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `deployment-backup.list` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `deployment-backup.create` | Create an on-demand backup | Administrator, Editor, Operator |
| `deployment-remote.list` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `deployment-remote.update` | Update a remote replica | Administrator, Editor, Operator |
| `deployment-remote.create` | Promote a remote replica | Administrator, Editor, Operator |
| `deployment-remote-resync.create` | Resync remote replica | Administrator, Editor, Operator |
| `deployment-database-connection.bulkdelete` | Kill all database connections | Administrator, Editor, Operator |
| `deployment-configuration.update` | Update deployment configuration | Administrator, Editor, Operator |
| `deployment-configuration-schema.read` | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| `deployment-network.read` | Read deployment network | Administrator, Editor, Operator, Viewer |
| `deployment-group.list` | Read Groups | Administrator, Editor, Operator, Viewer |
| `deployment-group.update` | Update a Group | Administrator, Editor, Operator |
| `deployment-group-autoscaling.read` | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| `deployment-group-autoscaling.update` | Update autoscaling configuration | Administrator, Editor, Operator |
| `capability.create` | Discover a supported capability | Administrator, Editor, Operator |
| `deployment-user.create` | Create a type of user | Administrator, Editor, Operator |
| `deployment-user.read` | Read a type of user | Administrator, Editor, Operator, Viewer |
| `deployment-user.update` | Update a type of user | Administrator, Editor, Operator |
| `deployment-user.delete` | Delete a type of user | Administrator, Editor, Operator |
| `deployment-user-connection.list` | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-user-connection.create` | Create deployment user connections | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.list` | Read Allowlisted IP Addresses | Administrator, Editor, Operator, Viewer |
| `deployment-ip-address.create` | Create a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-ip-address.delete` | Remove a Allowlisted IP Addresses | Administrator, Editor, Operator |
| `deployment-allowlist-ip-addresses.update` | Bulk allowlist IP addresses | Administrator, Editor, Operator |
| `deployment-capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
| `capability.read` | Read a capability | Administrator, Editor, Operator, Viewer |
{: caption="Table 108. Service actions - Messages for RabbitMQ" caption-side="top"}
{: #actions-table108}
{: tab-title="Actions"}
{: tab-group="messages-for-rabbitmq"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Migration Services for IBM Cloud
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `migrationtool-from-wanclds` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 109. Platform roles - Migration Services for IBM Cloud" caption-side="top"}
{: #platform-roles-table109}
{: tab-title="Platform roles"}
{: tab-group="migrationtool-from-wanclds"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `migrationtool-from-wanclds.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 109. Service actions - Migration Services for IBM Cloud" caption-side="top"}
{: #actions-table109}
{: tab-title="Actions"}
{: tab-group="migrationtool-from-wanclds"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Mobile Foundation
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `mobile-foundation` for the service name.

No supported roles.
## IBM Cloud Monitoring Service
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `monitoring` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 111. Platform roles - IBM Cloud Monitoring Service" caption-side="top"}
{: #platform-roles-table111}
{: tab-title="Platform roles"}
{: tab-group="monitoring"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `monitoring.domain.write` |  | Administrator, Editor, Operator |
| `monitoring.domain.render` |  | Administrator, Editor, Operator, Viewer |
| `monitoring.domain.find` |  | Administrator, Editor, Operator, Viewer |
| `monitoring.domain.alarm_write` |  | Administrator, Editor |
| `monitoring.domain.alarm_read` |  | Administrator, Editor, Viewer |
| `monitoring.domain.notify_write` |  | Administrator, Editor |
| `monitoring.domain.notify_read` |  | Administrator, Editor, Viewer |
| `monitoring.domain.dashboard_write` |  | Administrator, Editor, Operator |
| `monitoring.domain.dashboard_read` |  | Administrator, Editor, Viewer |
| `monitoring.domain.uptime_write` |  | Administrator, Editor |
| `monitoring.domain.uptime_read` |  | Administrator, Editor, Viewer |
{: caption="Table 111. Service actions - IBM Cloud Monitoring Service" caption-side="top"}
{: #actions-table111}
{: tab-title="Actions"}
{: tab-group="monitoring"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM MQ
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `mqcloud` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 112. Platform roles - IBM MQ" caption-side="top"}
{: #platform-roles-table112}
{: tab-title="Platform roles"}
{: tab-group="mqcloud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 112. Service roles - IBM MQ" caption-side="top"}
{: #service-roles-table112}
{: tab-title="Service roles"}
{: tab-group="mqcloud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `mqcloud.instance.use` | Accessing an MQ on Cloud service instance | Administrator, Editor, Manager, Viewer, Writer |
{: caption="Table 112. Service actions - IBM MQ" caption-side="top"}
{: #actions-table112}
{: tab-title="Actions"}
{: tab-group="mqcloud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Natural Language Classifier
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `natural-language-classifier` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
| Editor | null |
| Viewer | null |
{: row-headers}
{: caption="Table 113. Platform roles - Natural Language Classifier" caption-side="top"}
{: #platform-roles-table113}
{: tab-title="Platform roles"}
{: tab-group="natural-language-classifier"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | null |
| Reader | null |
| Writer | null |
{: row-headers}
{: caption="Table 113. Service roles - Natural Language Classifier" caption-side="top"}
{: #service-roles-table113}
{: tab-title="Service roles"}
{: tab-group="natural-language-classifier"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /natural-language-classifier` |  | Administrator, Editor, Manager, Reader, Viewer, Writer |
| `POST /natural-language-classifier` |  | Administrator, Editor, Manager, Reader, Viewer, Writer |
| `DELETE /natural-language-classifier` |  | Administrator, Editor, Manager, Reader, Viewer, Writer |
{: caption="Table 113. Service actions - Natural Language Classifier" caption-side="top"}
{: #actions-table113}
{: tab-title="Actions"}
{: tab-group="natural-language-classifier"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Natural Language Understanding
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `natural-language-understanding` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 114. Platform roles - Natural Language Understanding" caption-side="top"}
{: #platform-roles-table114}
{: tab-title="Platform roles"}
{: tab-group="natural-language-understanding"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 114. Service roles - Natural Language Understanding" caption-side="top"}
{: #service-roles-table114}
{: tab-title="Service roles"}
{: tab-group="natural-language-understanding"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `natural-language-understanding.dashboard.view` |  | Administrator, Editor, Operator |
| `GET /natural-language-understanding` |  | Manager, Reader, Writer |
| `POST /natural-language-understanding` |  | Manager, Reader, Writer |
| `DELETE /natural-language-understanding` |  | Manager, Reader, Writer |
| `PUT /natural-language-understanding` | PUT /natural-language-understanding | Manager, Reader, Writer |
{: caption="Table 114. Service actions - Natural Language Understanding" caption-side="top"}
{: #actions-table114}
{: tab-title="Actions"}
{: tab-group="natural-language-understanding"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## NeuVector Container Security Platform
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `neuvector-container-security` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 115. Platform roles - NeuVector Container Security Platform" caption-side="top"}
{: #platform-roles-table115}
{: tab-title="Platform roles"}
{: tab-group="neuvector-container-security"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `neuvector-container-security.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 115. Service actions - NeuVector Container Security Platform" caption-side="top"}
{: #actions-table115}
{: tab-title="Actions"}
{: tab-group="neuvector-container-security"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Partner Center
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `partner-portal` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 116. Platform roles - Partner Center" caption-side="top"}
{: #platform-roles-table116}
{: tab-title="Platform roles"}
{: tab-group="partner-portal"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `partner-portal.dashboard.view` | View Dashboard | Administrator, Editor, Viewer |
| `partner-portal.dashboard.edit` | Enabled for testing only | Administrator, Editor |
{: caption="Table 116. Service actions - Partner Center" caption-side="top"}
{: #actions-table116}
{: tab-title="Actions"}
{: tab-group="partner-portal"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Personality Insights
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `personality-insights` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
| Editor | null |
| Operator | null |
{: row-headers}
{: caption="Table 117. Platform roles - Personality Insights" caption-side="top"}
{: #platform-roles-table117}
{: tab-title="Platform roles"}
{: tab-group="personality-insights"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | null |
| Reader | null |
| Writer | null |
{: row-headers}
{: caption="Table 117. Service roles - Personality Insights" caption-side="top"}
{: #service-roles-table117}
{: tab-title="Service roles"}
{: tab-group="personality-insights"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `personality-insights.dashboard.view` |  | Administrator, Editor, Operator |
| `GET /personality-insights` |  | Manager, Reader, Writer |
| `POST /personality-insights` |  | Manager, Reader, Writer |
{: caption="Table 117. Service actions - Personality Insights" caption-side="top"}
{: #actions-table117}
{: tab-title="Actions"}
{: tab-group="personality-insights"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Watson Machine Learning
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `pm-20` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 118. Platform roles - Watson Machine Learning" caption-side="top"}
{: #platform-roles-table118}
{: tab-title="Platform roles"}
{: tab-group="pm-20"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you can perform all actions on the WML instance this role is being assigned. |
{: row-headers}
{: caption="Table 118. Service roles - Watson Machine Learning" caption-side="top"}
{: #service-roles-table118}
{: tab-title="Service roles"}
{: tab-group="pm-20"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `pm-20.instances.admin` |  | Administrator |
| `pm-20.instances.write` |  | Editor, Manager, Writer |
{: caption="Table 118. Service actions - Watson Machine Learning" caption-side="top"}
{: #actions-table118}
{: tab-title="Actions"}
{: tab-group="pm-20"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Portworx Enterprise
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `portworx` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 119. Platform roles - Portworx Enterprise" caption-side="top"}
{: #platform-roles-table119}
{: tab-title="Platform roles"}
{: tab-group="portworx"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `portworx.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 119. Service actions - Portworx Enterprise" caption-side="top"}
{: #actions-table119}
{: tab-title="Actions"}
{: tab-group="portworx"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## PowerAI
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `power-ai` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
| Editor | null |
| Operator | null |
{: row-headers}
{: caption="Table 120. Platform roles - PowerAI" caption-side="top"}
{: #platform-roles-table120}
{: tab-title="Platform roles"}
{: tab-group="power-ai"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `power-ai.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 120. Service actions - PowerAI" caption-side="top"}
{: #actions-table120}
{: tab-title="Actions"}
{: tab-group="power-ai"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Power Systems Virtual Server
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `power-iaas` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 121. Service roles - Power Systems Virtual Server" caption-side="top"}
{: #service-roles-table121}
{: tab-title="Service roles"}
{: tab-group="power-iaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `power-iaas.dashboard.view` |  | Manager, Reader |
| `power-iaas.cloud-instance.modify` |  | Manager |
| `power-iaas.cloud-instance.read` |  | Manager, Reader |
{: caption="Table 121. Service actions - Power Systems Virtual Server" caption-side="top"}
{: #actions-table121}
{: tab-title="Actions"}
{: tab-group="power-iaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## HDM Workload Migrator
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `primaryio-hdm-workload-migrator` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 122. Platform roles - HDM Workload Migrator" caption-side="top"}
{: #platform-roles-table122}
{: tab-title="Platform roles"}
{: tab-group="primaryio-hdm-workload-migrator"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `primaryio-hdm-workload-migrator.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 122. Service actions - HDM Workload Migrator" caption-side="top"}
{: #actions-table122}
{: tab-title="Actions"}
{: tab-group="primaryio-hdm-workload-migrator"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Product Lifecycle
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `product-lifecycle` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 123. Platform roles - Product Lifecycle" caption-side="top"}
{: #platform-roles-table123}
{: tab-title="Platform roles"}
{: tab-group="product-lifecycle"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Lifecycle Approver | Approvers can approve or reject workflow tasks |
{: row-headers}
{: caption="Table 123. Service roles - Product Lifecycle" caption-side="top"}
{: #service-roles-table123}
{: tab-title="Service roles"}
{: tab-group="product-lifecycle"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `product-lifecycle.dashboard.view` |  | Administrator, Editor, Operator |
| `product-lifecycle.offering.create` | Create an onboarding offering in the account | Administrator, Editor |
| `product-lifecycle.offering.edit` | Edit an onboarding offering in the account. | Administrator, Editor |
| `product-lifecycle.review.complete` | Complete (accept or reject) a review | Lifecycle Approver |
| `product-lifecycle.offering.read` | Read values of an offering | Administrator, Editor, Lifecycle Approver |
| `product-lifecycle.registration.read` | Read onboarding registration | Administrator, Editor, Lifecycle Approver |
| `product-lifecycle.registration.create` | Create onboarding registration | Administrator, Editor |
{: caption="Table 123. Service actions - Product Lifecycle" caption-side="top"}
{: #actions-table123}
{: tab-title="Actions"}
{: tab-group="product-lifecycle"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## PX-Backup By Portworx
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `px-backup` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 124. Platform roles - PX-Backup By Portworx" caption-side="top"}
{: #platform-roles-table124}
{: tab-title="Platform roles"}
{: tab-group="px-backup"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `px-backup.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 124. Service actions - PX-Backup By Portworx" caption-side="top"}
{: #actions-table124}
{: tab-title="Actions"}
{: tab-group="px-backup"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Quantum Services
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `quantum-computing` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 125. Service roles - Quantum Services" caption-side="top"}
{: #service-roles-table125}
{: tab-title="Service roles"}
{: tab-group="quantum-computing"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `quantum-computing.program.create` | Create a quantum program | Manager, Writer |
| `quantum-computing.program.read` | Read a program definition | Manager, Reader |
| `quantum-computing.program.delete` | Delete a program | Manager, Writer |
| `quantum-computing.job.create` | Create a job to run a program | Manager, Writer |
| `quantum-computing.job.read` | User ability to read a job | Manager, Reader |
| `quantum-computing.job.delete` | Delete a Job | Manager, Writer |
| `quantum-computing.program.update` | Update a program | Manager, Writer |
| `quantum-computing.job.cancel` | Cancel a Job | Manager, Writer |
| `quantum-computing.device.read` | Read information about a quantum device | Manager, Reader |
| `quantum-computing.user.logout` | Clears authorization cache | Manager, Reader, Writer |
{: caption="Table 125. Service actions - Quantum Services" caption-side="top"}
{: #actions-table125}
{: tab-title="Actions"}
{: tab-group="quantum-computing"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Raxak Protect
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `raxak-protect` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 126. Platform roles - Raxak Protect" caption-side="top"}
{: #platform-roles-table126}
{: tab-title="Platform roles"}
{: tab-group="raxak-protect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `raxak-protect.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 126. Service actions - Raxak Protect" caption-side="top"}
{: #actions-table126}
{: tab-title="Actions"}
{: tab-group="raxak-protect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Robin CNS
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `robin-storage` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 127. Platform roles - Robin CNS" caption-side="top"}
{: #platform-roles-table127}
{: tab-title="Platform roles"}
{: tab-group="robin-storage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `robin-storage.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 127. Service actions - Robin CNS" caption-side="top"}
{: #actions-table127}
{: tab-title="Actions"}
{: tab-group="robin-storage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Cloud Satellite
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `satellite` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 128. Platform roles - IBM Cloud Satellite" caption-side="top"}
{: #platform-roles-table128}
{: tab-title="Platform roles"}
{: tab-group="satellite"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Deployer | This role allow the user to deploy satellite-config managed contents to managed clusters |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Satellite Cluster Creator | As a Satellite Cluster Creator you have the ability create new Red Hat OpenShift on IBM Cloud OpenShift Clusters in the Satellite Location |
| Satellite Link Administrator | The Satellite Link Administrator is able to create, edit, update, and delete Satellite Link Endpoints and Sources |
| Satellite Link Source Access Controller | Allows the subject to enable access to Link Endpoint from a Link Source |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 128. Service roles - IBM Cloud Satellite" caption-side="top"}
{: #service-roles-table128}
{: tab-title="Service roles"}
{: tab-group="satellite"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `satellite.dashboard.view` |  | Administrator, Editor, Operator |
| `satellite.config-configuration.create` | create configuration for the satellite config. You can create one or more configurations for your org. | Administrator, Manager |
| `satellite.config-configuration.read` | list all the configurations for your org, or get details about one configuration | Manager, Reader |
| `satellite.config-configuration.update` | updates fields in configuration | Manager, Writer |
| `satellite.config-configuration.delete` | delete a configuration | Administrator, Manager |
| `satellite.config-configuration.manageversion` | change your configuration version | Manager, Writer |
| `satellite.config-subscription.create` | create a subscription for a configuration | Deployer, Manager |
| `satellite.config-subscription.read` | read subscriptions for your org | Deployer, Manager, Reader |
| `satellite.config-subscription.update` | update subscription name and other relevant fields | Deployer, Manager |
| `satellite.config-subscription.delete` | delete a subscription | Deployer, Manager |
| `satellite.config-subscription.setversion` | set the configuration version on this subscription | Deployer, Manager |
| `satellite.config-cluster.attach` | attach cluster to a cluster group | Administrator, Manager |
| `satellite.config-cluster.read` | read cluster list for for an org or details about a given cluster | Administrator, Manager, Reader |
| `satellite.link.create` | Create Link instance for the Satellite Location.  | Administrator |
| `satellite.config-organization.read` | allow to access the organization info | Administrator, Deployer, Manager, Reader, Satellite Cluster Creator |
| `satellite.config-organization.manage` | allow to read the org_key for an organization | Manager |
| `satellite.resource.get` | read resource under a cluster or from a cluster group | Administrator, Manager, Reader |
| `satellite.api.globalaccess` | global access satellite api for special users | Administrator, Manager |
| `satellite.config-cluster.register` | register cluster to the satellite config | Administrator, Manager |
| `satellite.config-cluster.detach` | detach cluster | Administrator, Manager |
| `satellite.config-clustergroup.read` | read cluster group for all its resources | Administrator, Manager, Reader |
| `satellite.config-clustergroup.manage` | create or delete a cluster group | Administrator, Manager |
| `satellite.location.create` | create satellite location to be added to the existing locations | Administrator |
| `satellite.location.read` | read satellite location | Administrator, Editor, Operator, Satellite Cluster Creator, Satellite Link Administrator, Viewer |
| `satellite.location.update` | edit an existing satellite location information | Administrator, Editor, Operator |
| `satellite.location.delete` | delete a satellite location belonged to you | Administrator, Operator |
| `satellite.config-clustergroup.setversion` | set the configuration version on this cluster group | Administrator, Deployer, Manager |
| `satellite.resource.servicelevelread` | Service level read of resources | Administrator, Manager |
| `satellite.link.get` | Get configuration and status of a Link instance. | Administrator, Editor, Operator, Satellite Link Administrator, Viewer |
| `satellite.link.delete` | Delete a Link instance of a Satellite Location.  | Administrator, Operator |
| `satellite.link-endpoints.list` | List all Link Endpoints of a Satellite Location. | Administrator, Editor, Operator, Satellite Link Administrator, Viewer |
| `satellite.link-endpoints.create` | Create a Link Endpoint with specified configuration. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.link-endpoints.get` | Get configuration and status of a Link Endpoint. | Administrator, Editor, Operator, Satellite Link Administrator, Viewer |
| `satellite.link-endpoints.update` | Modify configuration of a Link Endpoint. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.link-endpoints.delete` | Delete a Link Endpoint. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.link-endpoint-certs.get` | Get certificate/key of a Link Endpoint. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.link-endpoint-certs.upload` | Upload certificate/key for a Link Endpoint. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.link-endpoint-certs.delete` | Delete certificate/key of a Link Endpoint. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.link-sources.list` | List all ACL Sources of a Link instance. | Administrator, Editor, Operator, Satellite Link Administrator, Viewer |
| `satellite.link-sources.create` | Create a ACL Source for a Link instance. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.link-sources.delete` | Delete a ACL Source of a Link instance. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.link-endpoint-sources.list` | List ACL Sources used by a Link Endpoint.  | Administrator, Editor, Operator, Satellite Link Administrator, Viewer |
| `satellite.link-endpoint-sources.update` | Update ACL Sources enable/disable state of a Link Endpoint. | Administrator, Editor, Operator, Satellite Link Source Access Controller |
| `satellite.link-sources.update` | Modify IP address/subnets list of a ACL Source configured for the specified Link instance. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.config-cluster.update` | Update cluster registration | Manager |
| `satellite.location.cluster-create` | Enables the user to create Red Hat OpenShift on IBM Cloud clusters in the Satellite Location | Administrator, Satellite Cluster Creator |
| `satellite.link-endpoints.import` | Import Endpoint from previous export. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.link-endpoints.export` | Export Endpoint configuration to an archive file. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.link-source-endpoints.list` | List Source status for all Endpoints. | Administrator, Editor, Operator, Satellite Link Administrator |
| `satellite.link-source-endpoints.update` | Update Source status for listed Endpoints. | Administrator, Editor, Operator, Satellite Link Source Access Controller |
{: caption="Table 128. Service actions - IBM Cloud Satellite" caption-side="top"}
{: #actions-table128}
{: tab-title="Actions"}
{: tab-group="satellite"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Satellite Infrastructure Services 
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `satellite-iaas` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 129. Platform roles - Satellite Infrastructure Services " caption-side="top"}
{: #platform-roles-table129}
{: tab-title="Platform roles"}
{: tab-group="satellite-iaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Satellite IS Request Handler | Satellite IS Request Handler |
{: row-headers}
{: caption="Table 129. Service roles - Satellite Infrastructure Services " caption-side="top"}
{: #service-roles-table129}
{: tab-title="Service roles"}
{: tab-group="satellite-iaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `satellite-iaas.dashboard.view` |  | Administrator, Editor, Operator |
| `satellite-iaas.request.create` | Create a location request | Administrator, Manager, Satellite IS Request Handler |
| `satellite-iaas.request.update` | Update Satellite request | Satellite IS Request Handler |
| `satellite-iaas.request.delete` | Delete Location Request | Satellite IS Request Handler |
{: caption="Table 129. Service actions - Satellite Infrastructure Services " caption-side="top"}
{: #actions-table129}
{: tab-title="Actions"}
{: tab-group="satellite-iaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Schematics
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `schematics` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 130. Platform roles - Schematics" caption-side="top"}
{: #platform-roles-table130}
{: tab-title="Platform roles"}
{: tab-group="schematics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 130. Service roles - Schematics" caption-side="top"}
{: #service-roles-table130}
{: tab-title="Service roles"}
{: tab-group="schematics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `schematics.workspace.create` |  | Manager |
| `schematics.workspace.update` |  | Manager, Writer |
| `schematics.workspace.delete` |  | Manager |
| `schematics.workspace.read` | Read workspace details | Manager, Reader, Writer |
| `schematics.presets.create` | Create new presets for the Account | Manager |
| `schematics.presets.update` | Update the preset values | Manager, Writer |
| `schematics.presets.delete` | Delete the preset from Account | Manager |
| `schematics.presets.read` | Read the preset variable, value and metadata | Manager, Reader, Writer |
| `schematics.action.create` | Create an Action definition | Manager |
| `schematics.action.update` | Update the Action definition | Manager, Writer |
| `schematics.action.read` | Read the Action definition | Manager, Reader, Writer |
| `schematics.action.delete` | Delete the Action definition | Manager |
| `schematics.settings-kms.discover` | Discover KMS instances for Schematics settings | Administrator |
| `schematics.settings-kms.read` | Read the Schematics KMS settings | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `schematics.settings-kms.update` | Update the Schematics KMS settings | Administrator |
| `schematics.environment.create` | Create an Environment | Manager |
| `schematics.environment.update` | Update the Environment | Manager, Writer |
| `schematics.environment.delete` | Delete an Environment | Manager |
| `schematics.environment.read` | Read the Environment details | Manager, Reader, Writer |
| `schematics.agents.read` | Work with agent jobs | Operator |
| `schematics.settings-connection.read` | Read the connection settings for external data or template | Manager, Reader, Writer |
| `schematics.settings-connection.create` | Create connection settings for external data and template | Manager |
| `schematics.settings-connection.update` | Update connection settings for external data and template | Manager, Writer |
| `schematics.settings-connection.delete` | Delete the connection settings for external data and template | Manager |
| `schematics.datasets.create` | Create new datasets for the Account | Manager |
| `schematics.datasets.update` | Update the dataset values | Manager, Writer |
| `schematics.datasets.delete` | Delete the dataset from Account | Manager |
| `schematics.datasets.read` | Read the dataset variable, value and metadata | Manager, Reader, Writer |
{: caption="Table 130. Service actions - Schematics" caption-side="top"}
{: #actions-table130}
{: tab-title="Actions"}
{: tab-group="schematics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Secrets Manager
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `secrets-manager` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 131. Platform roles - Secrets Manager" caption-side="top"}
{: #platform-roles-table131}
{: tab-title="Platform roles"}
{: tab-group="secrets-manager"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions, such as managing secret groups, configuring secret engines, and managing secrets policies. |
| Reader | As a reader, you can perform read-only actions within Secrets Manager, such as viewing service-specific resources. Readers can access only the metadata that is associated with a secret. |
| SecretsReader | As a secrets reader, you can perform read-only actions, and you can also access the secret data that is associated with a secret. A secrets reader can't create secrets or modify the value of an existing secret. |
| Writer | As a writer, you have permissions beyond the secrets reader role, including the ability to create and edit secrets. Writers can't create secret groups, manage the rotation policies of a secret, or configure secrets engines. |
{: row-headers}
{: caption="Table 131. Service roles - Secrets Manager" caption-side="top"}
{: #service-roles-table131}
{: tab-title="Service roles"}
{: tab-group="secrets-manager"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `secrets-manager.dashboard.view` | View the Secrets Manager dashboard. | Administrator, Editor, Operator |
| `secrets-manager.secret-group.create` | Create secret groups to organize your secrets for access control. | Manager |
| `secrets-manager.secret-group.update` | Update a secret group. | Manager |
| `secrets-manager.secret-group.delete` | Delete a secret group. | Manager |
| `secrets-manager.secret-group.read` | View the details of a secret group. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.secret-groups.list` | List the secret groups in your instance. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.secret.create` | Create a secret. | Manager, Writer |
| `secrets-manager.secret.import` | Import a secret. | Manager, Writer |
| `secrets-manager.secret.read` | View the details of a secret. | Manager, SecretsReader, Writer |
| `secrets-manager.secret.delete` | Delete a secret. | Manager |
| `secrets-manager.secrets.list` | List the secrets in your instance. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.secret.rotate` | Rotate a secret. | Manager, Writer |
| `secrets-manager.secret-metadata.update` | Update a secret. | Manager, Writer |
| `secrets-manager.secret-metadata.read` | View the metadata of a secret. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.secret-policies.set` | Set secret policies. | Manager |
| `secrets-manager.secret-policies.get` | Get secret policies. | Manager |
| `secrets-manager.secret-engine-config.set` | Set secrets engine configuration. | Manager |
| `secrets-manager.secret-engine-config.get` | Get secrets engine configuration. | Manager |
| `secrets-manager.endpoints.view` | Get service instance endpoints. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.secret-versions.list` | List secret versions. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.vault-token.create` | Create a Vault token. | Manager |
| `secrets-manager.notifications-registration.create` | Register a Secrets Manager instance as a source in Event Notifications. | Manager |
| `secrets-manager.notifications-registration.read` | Get the registration details between a Secrets Manager and Event Notifications instance. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.notifications-registration.delete` | Unregister or remove a Secrets Manager instance as a source in Event Notifications. | Manager |
| `secrets-manager.notifications-registration.test` | Send a test event to the registered Event Notifications service instance. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.secret.revoke` | Revoke a secret | Manager |
{: caption="Table 131. Service actions - Secrets Manager" caption-side="top"}
{: #actions-table131}
{: tab-title="Actions"}
{: tab-group="secrets-manager"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Security Advisor
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `security-advisor` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 132. Platform roles - Security Advisor" caption-side="top"}
{: #platform-roles-table132}
{: tab-title="Platform roles"}
{: tab-group="security-advisor"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 132. Service roles - Security Advisor" caption-side="top"}
{: #service-roles-table132}
{: tab-title="Service roles"}
{: tab-group="security-advisor"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `security-advisor.dashboard.view` |  | Administrator, Editor, Operator |
| `security-advisor.findings.read` |  | Manager, Reader, Writer |
| `security-advisor.findings.write` |  | Manager, Writer |
| `security-advisor.findings.delete` |  | Manager |
| `security-advisor.findings.update` |  | Manager, Writer |
| `security-advisor.metadata.read` |  | Manager, Reader, Writer |
| `security-advisor.metadata.delete` |  | Manager |
| `security-advisor.metadata.write` |  | Manager |
| `security-advisor.metadata.update` |  | Manager |
| `security-advisor.data.post` |  | Manager, Writer |
| `security-advisor.data.get` |  | Manager, Reader, Writer |
| `security-advisor.analytics.post` |  | Manager, Writer |
| `security-advisor.custom-solution.read` |  | Manager, Reader, Writer |
| `security-advisor.custom-solution.write` |  | Manager |
| `security-advisor.custom-solution.update` |  | Manager |
| `security-advisor.custom-solution.delete` |  | Manager |
| `security-advisor.partner-solution.read` |  | Manager, Reader, Writer |
| `security-advisor.partner-solution.write` |  | Manager |
| `security-advisor.partner-solution.update` |  | Manager |
| `security-advisor.partner-solution.delete` |  | Manager |
| `security-advisor.network-insights.enable` |  | Manager |
| `security-advisor.network-insights.disable` |  | Manager |
| `security-advisor.activity-insights.enable` |  | Manager |
| `security-advisor.activity-insights.disable` |  | Manager |
| `security-advisor.insights-cos.create` |  | Manager |
| `security-advisor.notification-channels.read` |  | Manager, Reader, Writer |
| `security-advisor.notification-channels.create` |  | Manager |
| `security-advisor.notification-channels.delete` |  | Manager |
| `security-advisor.notification-channels.update` |  | Manager |
| `security-advisor.accounts.list` | Get the list of all SA accounts | Manager, Reader, Writer |
| `security-advisor.findings.list` | List all findings | Manager, Reader, Writer |
| `security-advisor.metadata.list` | List all metadata | Manager, Reader, Writer |
| `security-advisor.notification-channels.list` | List all alert channels | Manager, Reader, Writer |
| `security-advisor.partner-solution.list` | List all partner integrations | Manager, Reader, Writer |
| `security-advisor.custom-solution.list` | List all direct connections | Manager, Reader, Writer |
| `security-advisor.network-insights-cos.create` | Add cos bucket details for insights | Manager |
| `security-advisor.network-insights-cos.delete` | Delete cos bucket details for network insights | Manager |
| `security-advisor.activity-insights-cos.create` | Add cos bucket details for activity insights | Manager |
| `security-advisor.activity-insights-cos.delete` | Delete cos bucket details for activity insights | Manager |
| `security-advisor.activity-insights-config.test` | Test activity insights configuration | Manager, Writer |
| `security-advisor.insights.read` | Fetch  the list of supported insights | Manager, Reader, Writer |
| `security-advisor.keys.delete` | Delete BYOK configurations | Manager |
| `security-advisor.keys.read` | Read BYOK/KYOK configurations | Manager, Reader, Writer |
| `security-advisor.keys.write` | Create BYOK configuration | Manager |
| `security-advisor.activity-insights-cos.read` | Read cos bucket details for activity insights | Manager, Reader, Writer |
| `security-advisor.network-insights-cos.read` | Read cos bucket details for network insights | Manager, Reader, Writer |
| `security-advisor.activity-insights-configuration.read` | Read configuration details for activity insights | Manager, Reader, Writer |
| `security-advisor.network-insights-configuration.read` | Read configuration details for network insights | Manager, Reader, Writer |
| `security-advisor.activity-insights-configuration.udpate` | Update configuration details for activity insights | Manager |
| `security-advisor.network-insights-configuration.udpate` | Update configuration details for network insights | Manager |
{: caption="Table 132. Service actions - Security Advisor" caption-side="top"}
{: #actions-table132}
{: tab-title="Actions"}
{: tab-group="security-advisor"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Simulated Instruments Analytics API
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `sia` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 133. Platform roles - Simulated Instruments Analytics API" caption-side="top"}
{: #platform-roles-table133}
{: tab-title="Platform roles"}
{: tab-group="sia"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 133. Service roles - Simulated Instruments Analytics API" caption-side="top"}
{: #service-roles-table133}
{: tab-title="Service roles"}
{: tab-group="sia"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `sia.dashboard.view` |  | Administrator, Editor, Operator |
| `sia.instrument.read` |  | Reader |
{: caption="Table 133. Service actions - Simulated Instruments Analytics API" caption-side="top"}
{: #actions-table133}
{: tab-title="Actions"}
{: tab-group="sia"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Skytap On IBM Cloud
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `skytap` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 134. Platform roles - Skytap On IBM Cloud" caption-side="top"}
{: #platform-roles-table134}
{: tab-title="Platform roles"}
{: tab-group="skytap"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `skytap.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 134. Service actions - Skytap On IBM Cloud" caption-side="top"}
{: #actions-table134}
{: tab-title="Actions"}
{: tab-group="skytap"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Speech to Text
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `speech-to-text` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 135. Platform roles - Speech to Text" caption-side="top"}
{: #platform-roles-table135}
{: tab-title="Platform roles"}
{: tab-group="speech-to-text"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 135. Service roles - Speech to Text" caption-side="top"}
{: #service-roles-table135}
{: tab-title="Service roles"}
{: tab-group="speech-to-text"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `speech-to-text.dashboard.view` |  | Administrator, Editor, Operator |
| `GET /speech-to-text` |  | Manager, Reader, Writer |
| `POST /speech-to-text` |  | Manager, Writer |
| `DELETE /speech-to-text` |  | Manager, Writer |
| `HEAD /speech-to-text` |  | Manager, Reader, Writer |
| `PUT /speech-to-text` |  | Manager, Writer |
{: caption="Table 135. Service actions - Speech to Text" caption-side="top"}
{: #actions-table135}
{: tab-title="Actions"}
{: tab-group="speech-to-text"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## sql-query
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `sql-query` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 136. Service roles - sql-query" caption-side="top"}
{: #service-roles-table136}
{: tab-title="Service roles"}
{: tab-group="sql-query"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `sql-query.api.submit` | Submit SQL jobs that read and write data, including catalog metadata , such as table definitions. | Manager, Writer |
| `sql-query.api.getalljobs` | Retrieve a list of recent job submissions and their outcome status. | Manager, Reader, Writer |
| `sql-query.api.getjobinfo` | Retrieve the detailed status of a job based on provided jobid. | Manager, Reader, Writer |
| `sql-query.api.managecatalog` | Manage the catalog and indexes. For example, submit DDL statements to create, alter and drop tables, views and indexes. | Manager |
| `sql-query.api.readcatalog` | Introspect the catalog. For example, list the definitions of tables, views and indexes. | Manager, Reader, Writer |
{: caption="Table 136. Service actions - sql-query" caption-side="top"}
{: #actions-table136}
{: tab-title="Actions"}
{: tab-group="sql-query"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## streaming-analytics
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `streaming-analytics` for the service name.

| Role | Description |
| ----- | :----- |
| null | null |
| null | null |
{: row-headers}
{: caption="Table 137. Service roles - streaming-analytics" caption-side="top"}
{: #service-roles-table137}
{: tab-title="Service roles"}
{: tab-group="streaming-analytics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `streaming-analytics.instances.query` |  | null |
| `streaming-analytics.instances.read` |  | null, null |
| `streaming-analytics.instances.update` |  | null |
| `streaming-analytics.instances.start` |  | null, null |
| `streaming-analytics.jobs.query` |  | null, null |
| `streaming-analytics.jobs.create` |  | null, null |
| `streaming-analytics.jobs.read` |  | null, null |
| `streaming-analytics.jobs.delete` |  | null, null |
| `streaming-analytics.builds.query` |  | null, null |
| `streaming-analytics.builds.create` |  | null, null |
| `streaming-analytics.builds.read` |  | null, null |
| `streaming-analytics.builds.delete` |  | null, null |
| `streaming-analytics.artifacts.query` |  | null, null |
| `streaming-analytics.artifacts.read` |  | null, null |
| `streaming-analytics.artifacts.download` |  | null, null |
{: caption="Table 137. Service actions - streaming-analytics" caption-side="top"}
{: #actions-table137}
{: tab-title="Actions"}
{: tab-group="streaming-analytics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Support Center
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `support` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | View, search, create, and update support cases |
| Editor | View, search, create, and update support cases |
| Viewer | View and search support cases |
{: row-headers}
{: caption="Table 138. Platform roles - Support Center" caption-side="top"}
{: #platform-roles-table138}
{: tab-title="Platform roles"}
{: tab-group="support"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `support.case.create` |  | Administrator, Editor |
| `support.case.update` |  | Administrator, Editor |
| `support.case.read` |  | Administrator, Editor, Viewer |
| `support.case.list` |  | Administrator, Editor, Viewer |
{: caption="Table 138. Service actions - Support Center" caption-side="top"}
{: #actions-table138}
{: tab-title="Actions"}
{: tab-group="support"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Cloud Monitoring with Sysdig
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `sysdig-monitor` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 139. Platform roles - IBM Cloud Monitoring with Sysdig" caption-side="top"}
{: #platform-roles-table139}
{: tab-title="Platform roles"}
{: tab-group="sysdig-monitor"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 139. Service roles - IBM Cloud Monitoring with Sysdig" caption-side="top"}
{: #service-roles-table139}
{: tab-title="Service roles"}
{: tab-group="sysdig-monitor"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `sysdig-monitor.launch.user` |  | Administrator, Manager, Writer |
| `sysdig-monitor.launch.admin` |  | Administrator, Manager |
| `sysdig-monitor.launch.viewer` |  | Administrator, Manager, Reader, Writer |
{: caption="Table 139. Service actions - IBM Cloud Monitoring with Sysdig" caption-side="top"}
{: #actions-table139}
{: tab-title="Actions"}
{: tab-group="sysdig-monitor"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Text to Speech
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `text-to-speech` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 140. Platform roles - Text to Speech" caption-side="top"}
{: #platform-roles-table140}
{: tab-title="Platform roles"}
{: tab-group="text-to-speech"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 140. Service roles - Text to Speech" caption-side="top"}
{: #service-roles-table140}
{: tab-title="Service roles"}
{: tab-group="text-to-speech"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `text-to-speech.dashboard.view` |  | Administrator, Editor, Operator |
| `GET /text-to-speech` |  | Manager, Reader, Writer |
| `POST /text-to-speech` |  | Manager, Writer |
| `DELETE /text-to-speech` |  | Manager, Writer |
| `HEAD /text-to-speech` |  | Manager, Reader, Writer |
| `PUT /text-to-speech` |  | Manager, Writer |
{: caption="Table 140. Service actions - Text to Speech" caption-side="top"}
{: #actions-table140}
{: tab-title="Actions"}
{: tab-group="text-to-speech"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Tone Analyzer
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `tone-analyzer` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
| Editor | null |
| Operator | null |
{: row-headers}
{: caption="Table 141. Platform roles - Tone Analyzer" caption-side="top"}
{: #platform-roles-table141}
{: tab-title="Platform roles"}
{: tab-group="tone-analyzer"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | null |
| Reader | null |
| Writer | null |
{: row-headers}
{: caption="Table 141. Service roles - Tone Analyzer" caption-side="top"}
{: #service-roles-table141}
{: tab-title="Service roles"}
{: tab-group="tone-analyzer"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `tone-analyzer.dashboard.view` |  | Administrator, Editor, Operator |
| `GET /tone-analyzer` |  | Manager, Reader, Writer |
| `POST /tone-analyzer` |  | Manager, Reader, Writer |
{: caption="Table 141. Service actions - Tone Analyzer" caption-side="top"}
{: #actions-table141}
{: tab-title="Actions"}
{: tab-group="tone-analyzer"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Toolchain
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `toolchain` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 142. Platform roles - Toolchain" caption-side="top"}
{: #platform-roles-table142}
{: tab-title="Platform roles"}
{: tab-group="toolchain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `toolchain.dashboard.view` | View instances of the Toolchain service. | Administrator, Editor, Operator |
| `toolchain.instance.read-properties` | Read toolchain properties. | Administrator, Editor, Viewer |
| `toolchain.instance.update-properties` | Update toolchain properties. | Administrator, Editor |
| `toolchain.instance.create-bindings` | Add a tool integration to a toolchain within a resource group. | Administrator, Editor |
| `toolchain.instance.delete-bindings` | Remove a tool integration from a toolchain within a resource group. | Administrator, Editor |
| `toolchain.instance.list-bindings` | View the tool integrations that are contained in a toolchain within a resource group. | Administrator, Editor, Viewer |
{: caption="Table 142. Service actions - Toolchain" caption-side="top"}
{: #actions-table142}
{: tab-title="Actions"}
{: tab-group="toolchain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Transit Gateway
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `transit` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
{: row-headers}
{: caption="Table 143. Service roles - Transit Gateway" caption-side="top"}
{: #service-roles-table143}
{: tab-title="Service roles"}
{: tab-group="transit"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `transit.transit.manage` | Transit service manager | Manager |
{: caption="Table 143. Service actions - Transit Gateway" caption-side="top"}
{: #actions-table143}
{: tab-title="Actions"}
{: tab-group="transit"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Transit Gateway
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `transit.gateway` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 144. Platform roles - Transit Gateway" caption-side="top"}
{: #platform-roles-table144}
{: tab-title="Platform roles"}
{: tab-group="transit.gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `transit.gateway.view` | The ability to view transit gateways and connections. | Administrator, Editor, Operator, Viewer |
| `transit.gateway.edit` | The ability to create, change, view and delete transit gateways and connections. | Administrator, Editor |
{: caption="Table 144. Service actions - Transit Gateway" caption-side="top"}
{: #actions-table144}
{: tab-title="Actions"}
{: tab-group="transit.gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## IBM Cloud Platform User Management Service
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `user-management` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can view, invite, and update users. You can also view and update user profile settings. |
| Editor | As an editor, you can view, invite, and update users. You can also view and update profile settings. |
| Operator | As an operator, you can view users in the account and view profile settings. |
| Viewer | As a viewer, you can view users in the account and view profile settings. |
{: row-headers}
{: caption="Table 145. Platform roles - IBM Cloud Platform User Management Service" caption-side="top"}
{: #platform-roles-table145}
{: tab-title="Platform roles"}
{: tab-group="user-management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `user-management.user.create` |  | Administrator, Editor |
| `user-management.user.update` |  | Administrator, Editor |
| `user-management.user.state-change` |  | Administrator, Editor |
| `user-management.user.delete` | Remove user from account | Administrator, Editor |
| `user-management.user.retrieve` |  | Administrator, Editor, Operator, Viewer |
| `user-management.invitation-email.create` |  | Administrator, Editor |
| `user-management.preference.update` |  | Administrator, Editor |
| `user-management.preference.retrieve` |  | Administrator, Editor, Operator, Viewer |
| `user-management.user-linkage.retrieve` |  | Administrator, Editor, Operator, Viewer |
| `user-management.user-setting.update` |  | Administrator, Editor |
| `user-management.user-setting.retrieve` |  | Administrator, Editor, Operator, Viewer |
| `user-management.user.replace-iam-id` |  | Administrator, Editor |
{: caption="Table 145. Service actions - IBM Cloud Platform User Management Service" caption-side="top"}
{: #actions-table145}
{: tab-title="Actions"}
{: tab-group="user-management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## VMware Solutions
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `vmware-solutions` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 146. Platform roles - VMware Solutions" caption-side="top"}
{: #platform-roles-table146}
{: tab-title="Platform roles"}
{: tab-group="vmware-solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `vmware-solutions.instances.create` | Create IBM Cloud for VMware Solutions instances | Administrator |
| `vmware-solutions.instances.delete` | Delete IBM Cloud for VMware Solutions instances | Administrator |
| `vmware-solutions.instances.view` | List or view IBM Cloud for VMware Solutions instances | Administrator, Editor, Operator, Viewer |
| `vmware-solutions.instances.update` | Update IBM Cloud for VMware Solutions instances | Administrator, Editor |
| `vmware-solutions.account.update` | Update account settings for IBM Cloud for VMware Solutions | Administrator |
{: caption="Table 146. Service actions - VMware Solutions" caption-side="top"}
{: #actions-table146}
{: tab-title="Actions"}
{: tab-group="vmware-solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Voice Agent with Watson
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `voiceagent` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 147. Platform roles - Voice Agent with Watson" caption-side="top"}
{: #platform-roles-table147}
{: tab-title="Platform roles"}
{: tab-group="voiceagent"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 147. Service roles - Voice Agent with Watson" caption-side="top"}
{: #service-roles-table147}
{: tab-title="Service roles"}
{: tab-group="voiceagent"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `voiceagent.agent.manage` | Manage all aspects of a Voice Agent with Watson instance. | Manager, Reader, Writer |
| `voiceagent.agent.view` | View configurations for all agents of a Voice Agent with Watson instance. | Reader |
| `voiceagent.usage.view` | View usage for all agents of a Voice Agent with Watson instance. | Reader |
| `voiceagent.log.view` | View all failure logs for all agents of a Voice Agent with Watson instance. | Reader |
| `voiceagent.sms.send` | Use the SMS gateway API to send SMS messages for a Voice Agent with Watson instance. | Administrator, Editor, Manager, Operator, Writer |
| `voiceagent.voice.inbound` | Authenticate inbound calls for a Voice Agent with Watson instance using SIPS. | Manager, Writer |
| `voiceagent.voice.outbound` | Use the outbound calling API to start outbound calls for a Voice Agent with Watson instance. | Manager, Writer |
{: caption="Table 147. Service actions - Voice Agent with Watson" caption-side="top"}
{: #actions-table147}
{: tab-title="Actions"}
{: tab-group="voiceagent"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## WebSphere Application Server
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `websphereappsvr` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 148. Platform roles - WebSphere Application Server" caption-side="top"}
{: #platform-roles-table148}
{: tab-title="Platform roles"}
{: tab-group="websphereappsvr"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `websphereappsvr.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 148. Service actions - WebSphere Application Server" caption-side="top"}
{: #actions-table148}
{: tab-title="Actions"}
{: tab-group="websphereappsvr"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

## Annotator for Clinical Data
Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `wh-acd` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 149. Platform roles - Annotator for Clinical Data" caption-side="top"}
{: #platform-roles-table149}
{: tab-title="Platform roles"}
{: tab-group="wh-acd"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 149. Service roles - Annotator for Clinical Data" caption-side="top"}
{: #service-roles-table149}
{: tab-title="Service roles"}
{: tab-group="wh-acd"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `wh-acd.dashboard.view` | View Dashboard | Administrator, Editor, Operator |
| `GET /wh-acd` | ACD Dev Deadbolt API GET | Manager, Reader, Writer |
| `PUT /wh-acd` | ACD Dev Deadbolt API PUT | Manager, Writer |
| `POST /wh-acd` | ACD Dev Deadbolt API POST | Manager, Writer |
| `DELETE /wh-acd` | ACD Dev Deadbolt API DELETE | Manager |
| `wh-acd.cartridge.manage` | Cartridge manage | Manager, Writer |
| `wh-acd.flows.manage` | Manage flows | Manager, Writer |
| `wh-acd.profiles.manage` | Manage profiles | Manager, Writer |
| `wh-acd.analyze` | Analyze | Manager, Reader, Writer |
{: caption="Table 149. Service actions - Annotator for Clinical Data" caption-side="top"}
{: #actions-table149}
{: tab-title="Actions"}
{: tab-group="wh-acd"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}

