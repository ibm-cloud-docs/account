---

copyright:

  years: 2019

lastupdated: "2023-06-17"

keywords: service iam roles, service iam actions, account management roles, iam roles

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}


# IAM roles and actions
{: #iam-service-roles-actions}

It is important to understand how to effectively assign access for users to work with products and take specific account management actions within your account to follow the principle of least privilege and minimize the number of policies that you have to manage. The following tables provide information about the access roles and the actions mapped to each by the {{site.data.keyword.cloud}} services.
{: shortdesc}

The following tables provide data from the individual IAM-enabled services that are available from the {{site.data.keyword.cloud_notm}} catalog as well as the  account management services that enable you to assign others the ability to work with users, access groups, support cases, and more in the account. If you don't see a platform roles or service roles table, then that means that particular service doesn't use those types of roles.

Each service has custom actions that they define and map to platform and service roles that you can use to assign access by creating an IAM access policy. If you are trying to assign access and an existing role doesn't fit your needs, you can create a [custom role](/docs/account?topic=account-custom-roles) that combines any number of actions that are available for a given service.

For more information about assigning access for each service, check out the documentation for the service that you're using.

<!-- Everything is deleted after this line. -->
## Statum KPI
{: #3p-amberoon-xaas-statumkpi-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `3p-amberoon-xaas-statumkpi` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 1. Platform roles - Statum KPI" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="3p-amberoon-xaas-statumkpi"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table1}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `3p-amberoon-xaas-statumkpi.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 1. Service actions - Statum KPI" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="3p-amberoon-xaas-statumkpi"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table1}

## ViziVault Platform
{: #3p-anontech-xaas-vizivault-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `3p-anontech-xaas-vizivault` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 2. Platform roles - ViziVault Platform" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="3p-anontech-xaas-vizivault"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table2}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `3p-anontech-xaas-vizivault.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 2. Service actions - ViziVault Platform" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="3p-anontech-xaas-vizivault"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table2}

## Cognitive View
{: #3p-cognitiveview-xaas-cognitiveview-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `3p-cognitiveview-xaas-cognitiveview` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 3. Platform roles - Cognitive View" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="3p-cognitiveview-xaas-cognitiveview"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table3}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `3p-cognitiveview-xaas-cognitiveview.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 3. Service actions - Cognitive View" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="3p-cognitiveview-xaas-cognitiveview"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table3}

## SimpleCloud
{: #3p-summusrender-xaas-simplecl0ud-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `3p-summusrender-xaas-simplecl0ud` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 4. Platform roles - SimpleCloud" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="3p-summusrender-xaas-simplecl0ud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table4}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `3p-summusrender-xaas-simplecl0ud.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 4. Service actions - SimpleCloud" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="3p-summusrender-xaas-simplecl0ud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table4}

## VPC+ DRaaS (VPC+ Disaster Recovery as a Service)
{: #3p-wanclds-draas-vpcplus-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `3p-wanclds-draas-vpcplus` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 5. Platform roles - VPC+ DRaaS (VPC+ Disaster Recovery as a Service)" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="3p-wanclds-draas-vpcplus"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table5}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `3p-wanclds-draas-vpcplus.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 5. Service actions - VPC+ DRaaS (VPC+ Disaster Recovery as a Service)" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="3p-wanclds-draas-vpcplus"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table5}

## Watson OpenScale
{: #aiopenscale-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `aiopenscale` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 6. Platform roles - Watson OpenScale" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="aiopenscale"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table6}

| Role | Description |
| ----- | :----- |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 6. Service roles - Watson OpenScale" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="aiopenscale"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table6}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `aiopenscale.dashboard.view` | View OpenScale | Administrator, Editor, Operator, Viewer |
| `aiopenscale.dashboard.edit` | Edit OpenScale | Administrator, Editor, Writer |
| `aiopenscale.dashboard.administer` | Administer OpenScale | Administrator |
{: caption="Table 6. Service actions - Watson OpenScale" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="aiopenscale"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table6}

## API Gateway
{: #api-gateway-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `api-gateway` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 7. Platform roles - API Gateway" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="api-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table7}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 7. Service roles - API Gateway" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="api-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table7}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `api-gateway.dashboard.view` |  | Administrator, Editor, Operator |
| `api-gateway.api.view` |  | Manager, Reader, Writer |
| `api-gateway.api.create` |  | Manager, Writer |
| `api-gateway.api.edit` |  | Manager, Writer |
| `api-gateway.api.delete` |  | Manager, Writer |
| `api-gateway.api.share` |  | Manager |
{: caption="Table 7. Service actions - API Gateway" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="api-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table7}

## API Connect
{: #apiconnect-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `apiconnect` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 8. Platform roles - API Connect" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="apiconnect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table8}

| Role | Description |
| ----- | :----- |
| API Developer | As an API Developer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Api Administrator | As an Api Administrator, you can perform all platform actions except for managing the account and assigning access policies. |
| Community Manager | As a Community Manager, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 8. Service roles - API Connect" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="apiconnect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table8}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `apiconnect.instance.admin` | apiconnect.instance.admin | Administrator |
| `apiconnect.admin.manage` | Enables API Connect administrators to create provider orgs, manage gateways, and adjust other settings for the environment. | Administrator, Api Administrator, Editor, Manager |
| `apiconnect.instance.view` | apiconnect.instance.view | API Developer, Administrator, Api Administrator, Community Manager, Editor, Manager, Operator, Reader, Viewer, Writer |
| `apiconnect.instance.manage-community` | apiconnect.instance.manage-community | Community Manager, Operator |
| `apiconnect.instance.api-admin` | apiconnect.instance.api-admin | Api Administrator, Editor, Manager |
| `apiconnect.instance.develop` | apiconnect.instance.develop | API Developer, Writer |
{: caption="Table 8. Service actions - API Connect" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="apiconnect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table8}

## App ID
{: #appid-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `appid` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 9. Service roles - App ID" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="appid"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table9}

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
| `appid.mgmt.get.settings` | Retrieve instance settings | Manager, Reader, Writer |
| `appid.mgmt.set.settings` | Set instance settings | Manager, Writer |
{: caption="Table 9. Service actions - App ID" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="appid"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table9}

## App Configuration
{: #apprapp-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `apprapp` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 10. Platform roles - App Configuration" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="apprapp"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table10}

| Role | Description |
| ----- | :----- |
| Client SDK | Role to manage Client SDK |
| Config Operator | As a Config Operator, you can toggle the feature state. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 10. Service roles - App Configuration" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="apprapp"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table10}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `apprapp.dashboard.view` | Dashboard view | Administrator, Config Operator, Editor, Manager, Operator, Reader, Writer |
| `apprapp.collections.list` | List collections | Administrator, Client SDK, Config Operator, Manager, Reader, Writer |
| `apprapp.collections.create` | Create collections | Administrator, Manager |
| `apprapp.collections.update` | Update collections | Administrator, Manager |
| `apprapp.collections.delete` | Delete collections  | Administrator, Manager |
| `apprapp.features.list` | List features | Administrator, Config Operator, Manager, Reader, Writer |
| `apprapp.features.create` | Create Features | Administrator, Manager |
| `apprapp.features.update` | Update features | Administrator, Manager |
| `apprapp.features.delete` | Delete features | Administrator, Manager |
| `apprapp.segments.list` | List segments | Administrator, Config Operator, Manager, Reader, Writer |
| `apprapp.segments.update` | Update segments | Administrator, Manager, Writer |
| `apprapp.segments.create` | Create segments | Administrator, Manager, Writer |
| `apprapp.segments.delete` | Delete segments | Administrator, Manager, Writer |
| `apprapp.features.patch` | Patch features | Administrator, Writer |
| `apprapp.features.toggle` | Toggle feature | Administrator, Config Operator, Manager, Writer |
| `apprapp.properties.list` | List properties | Config Operator, Manager, Reader, Writer |
| `apprapp.properties.update` | Update properties | Administrator, Manager |
| `apprapp.properties.create` | Create properties | Administrator, Manager |
| `apprapp.properties.delete` | Delete properties | Administrator, Manager |
| `apprapp.properties.patch` | Patch properties | Administrator, Writer |
| `apprapp.environments.create` | Create environments | Administrator, Manager |
| `apprapp.environments.update` | Update environments | Administrator, Manager |
| `apprapp.environments.delete` | Delete environments | Administrator, Manager |
| `apprapp.environments.list` | List environments | Administrator, Config Operator, Manager, Reader, Writer |
| `apprapp.instances.export` | Export instance resources to a JSON | Administrator, Manager |
| `apprapp.instances.import` | Import instance resources from a JSON | Administrator, Manager |
| `apprapp.gitconfigs.create` | Create git configuration | Administrator, Manager |
| `apprapp.gitconfigs.update` | Update git configurations | Administrator, Manager |
| `apprapp.gitconfigs.delete` | Delete GIT configuration | Administrator, Manager |
| `apprapp.gitconfigs.view` | GET a GIT configuration | Administrator, Config Operator, Manager, Reader, Writer |
| `apprapp.gitconfigs.promote` | Promote configuration | Manager |
| `apprapp.usage.create` | Usage posting | Administrator, Client SDK, Config Operator, Manager, Reader, Viewer, Writer |
| `apprapp.sse.view` | SSE connect | Client SDK, Config Operator, Manager, Reader, Writer |
| `apprapp.encryptionconfigs.create` | Create Encryption configuration for data encryption using key management services | Administrator, Manager |
| `apprapp.encryptionconfigs.list` | List Encryption configurations for data encryption using key management services | Administrator, Config Operator, Editor, Manager, Reader, Viewer, Writer |
| `apprapp.originconfigs.update` | Update origin configuration for allowlisting CORS policy for Browser clients SDKs | Administrator, Manager |
| `apprapp.originconfigs.list` | List origin configuration for allowlisting CORS policy for Browser clients SDKs | Administrator, Config Operator, Editor, Manager, Reader, Viewer, Writer |
| `apprapp.gitconfigs.restore` | Restore configuration | Manager |
| `apprapp.integrations.create` | Create a integration between App Configuration and an external service | Administrator, Manager |
| `apprapp.integrations.list` | List integrations between App Configuration and external services | Administrator, Config Operator, Editor, Manager, Reader, Viewer, Writer |
| `apprapp.integrations.delete` | Delete the integration between App Configuration and an external service | Administrator, Manager |
| `apprapp.workflowconfigs.create` | Create workflow configuration for service now integration for CR approval | Administrator, Manager |
| `apprapp.workflowconfigs.update` | Update workflow configuration for service now integration for CR approval | Administrator, Manager |
| `apprapp.workflowconfigs.list` | List the workflow configuration for service now integration for CR approval | Administrator, Config Operator, Editor, Manager, Reader, Viewer, Writer |
| `apprapp.workflowconfigs.delete` | Delete the workflow configuration for service now integration for CR approval | Administrator, Manager |
| `apprapp.changerequest.create` | API endpoint to listen to service-now events | Administrator, Manager |
{: caption="Table 10. Service actions - App Configuration" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="apprapp"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table10}

## Activity Tracker
{: #atracker-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `atracker` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 11. Platform roles - Activity Tracker" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table11}

| Role | Description |
| ----- | :----- |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 11. Service roles - Activity Tracker" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table11}

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
{: tab-title="Actions"}
{: tab-group="atracker"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table11}

## Bespoken Automated Testing For IVR and Chat
{: #automated-testing-and-monitoring-for-voice-and-chat-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `automated-testing-and-monitoring-for-voice-and-chat` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 12. Platform roles - Bespoken Automated Testing For IVR and Chat" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="automated-testing-and-monitoring-for-voice-and-chat"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table12}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `automated-testing-and-monitoring-for-voice-and-chat.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 12. Service actions - Bespoken Automated Testing For IVR and Chat" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="automated-testing-and-monitoring-for-voice-and-chat"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table12}

## Billing
{: #billing-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `billing` for the service name.

No supported roles.
## Blockchain Platform 2.0
{: #blockchain-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `blockchain` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 14. Service roles - Blockchain Platform 2.0" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="blockchain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table14}

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
{: caption="Table 14. Service actions - Blockchain Platform 2.0" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="blockchain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table14}

## Cloud Foundry for Custom Domain
{: #cf4customdomain-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cf4customdomain` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 15. Service roles - Cloud Foundry for Custom Domain" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="cf4customdomain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table15}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `cf4customdomain.newdashboard.view` | View information in the new dashboard | Manager, Reader, Writer |
{: caption="Table 15. Service actions - Cloud Foundry for Custom Domain" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="cf4customdomain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table15}

## Cloud Foundry Enterprise Environment
{: #cfaas-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cfaas` for the service name.

No supported roles.
## Cloud Object Storage
{: #cloud-object-storage-roles}

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
{: caption="Table 17. Service roles - Cloud Object Storage" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="cloud-object-storage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table17}

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
| `cloud-object-storage.bucket.get_object_lock_configuration` | Get Object Lock Configuration from the bucket. | Manager, Reader, Writer |
| `cloud-object-storage.bucket.put_object_lock_configuration` | Set Object Lock Configuration from the bucket. | Manager, Writer |
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
| `cloud-object-storage.object.get_object_lock_retention` | Get object lock retention settings on the object. | Manager, Reader, Writer |
| `cloud-object-storage.object.put_object_lock_retention_version` | Set object lock retention version settings on the object. | Manager, Object Writer, Writer |
| `cloud-object-storage.object.get_object_lock_retention_version` | Get object lock retention version settings on the object. | Manager, Reader, Writer |
| `cloud-object-storage.object.get_object_lock_legal_hold` | Get object lock legal hold state on the object. | Manager, Reader, Writer |
| `cloud-object-storage.object.put_object_lock_retention` | Set object lock retention settings on the object. | Manager, Object Writer, Writer |
| `cloud-object-storage.object.put_object_lock_legal_hold` | Set object lock legal hold state on the object. | Manager, Object Writer, Writer |
| `cloud-object-storage.object.put_object_lock_legal_hold_version` | Set object lock legal hold version state on the object. | Manager, Object Writer, Writer |
| `cloud-object-storage.object.get_object_lock_legal_hold_version` | Get object lock legal hold version state on the object. | Manager, Reader, Writer |
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
{: caption="Table 17. Service actions - Cloud Object Storage" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="cloud-object-storage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table17}

## Cloudant
{: #cloudantnosqldb-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cloudantnosqldb` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 18. Platform roles - Cloudant" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="cloudantnosqldb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table18}

| Role | Description |
| ----- | :----- |
| Checkpointer | As a checkpointer, you have permissions to write local documents enabling checkpoint writes. Checkpoints are local documents optionally created during replication recording their state. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Monitor | As a monitor, you have permissions to get information about specified databases, list databases, monitor indexing and replication, view data volume usage and view provisioned and current throughput. |
| Reader | As a reader, you can perform read-only actions within a service, such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 18. Service roles - Cloudant" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="cloudantnosqldb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table18}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `cloudantnosqldb.db.any` | Perform any database action | Manager |
| `cloudantnosqldb.activity-tracker-event-types.read` | Access list of configured activity tracker event types for a service instance | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `cloudantnosqldb.activity-tracker-event-types.write` | Update list of configured activity tracker event types for a service instance | Administrator, Manager, Operator |
| `cloudantnosqldb.sapi.lastactivity` | Access last activity time for account | Manager |
| `cloudantnosqldb.sapi.usercors` | Update CORS settings for a service instance | Administrator, Manager |
| `cloudantnosqldb.sapi.apikeys` | Generate Cloudant API keys for a service instance | Manager |
| `cloudantnosqldb.sapi.userccmdiagnostics` | Access current and maximum allowed throughput values | Manager |
| `cloudantnosqldb.sapi.supportattachments` | View attachments on support tickets for user | Manager |
| `cloudantnosqldb.sapi.supporttickets` | View support tickets for user | Manager |
| `cloudantnosqldb.sapi.userinfo` | Retrieve basic user infomation for this user | Administrator, Editor, Manager, Operator, Viewer |
| `cloudantnosqldb.users-database-info.read` | Read users' database info | Manager |
| `cloudantnosqldb.users-database.create` | Create users' databases | Manager |
| `cloudantnosqldb.users-database.delete` | Delete users' databases | Manager |
| `cloudantnosqldb.users.read` | Read from users' databases | Manager |
| `cloudantnosqldb.users.write` | Write to users' databases | Manager |
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
| `cloudantnosqldb.data-document.write` | Create, update, and delete normal documents in a database | Manager, Writer |
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
{: caption="Table 18. Service actions - Cloudant" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="cloudantnosqldb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table18}

## IBM Cloud Shell
{: #cloudshell-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cloudshell` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 19. Platform roles - IBM Cloud Shell" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="cloudshell"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table19}

| Role | Description |
| ----- | :----- |
| Cloud Developer | As a cloud developer, you can create Cloud Shell environments to manage IBM Cloud resources and develop applications for IBM Cloud (Web Preview enabled). |
| Cloud Operator | As a cloud operator, you can create Cloud Shell environments to manage IBM Cloud resources. |
| File Manager | As a file manager, you can create Cloud Shell environments to manage IBM Cloud resources and manage files in your workspace (File Upload and File Download enabled). |
{: row-headers}
{: caption="Table 19. Service roles - IBM Cloud Shell" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="cloudshell"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table19}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `cloudshell.account-settings.update` | The ability to update Cloud Shell account settings. | Administrator |
| `cloudshell.server.create` | The ability to create Cloud Shell environments. | Administrator, Cloud Developer, Cloud Operator, File Manager |
| `cloudshell.server.preview-web` | The ability to preview web applications in Cloud Shell (Web Preview enabled). | Administrator, Cloud Developer |
| `cloudshell.server.manage-file` | The ability to manage files in the Cloud Shell workspace (File Upload and File Download enabled). | Administrator, File Manager |
{: caption="Table 19. Service actions - IBM Cloud Shell" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="cloudshell"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table19}

## Code Engine
{: #codeengine-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `codeengine` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 20. Platform roles - Code Engine" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="codeengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table20}

| Role | Description |
| ----- | :----- |
| Compute Environment Administrator | Can manage Code Engine Compute Environments. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 20. Service roles - Code Engine" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="codeengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table20}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `codeengine.dashboard.view` | View Dashboard | Administrator, Editor, Operator |
| `codeengine.tenant.read` | View project details | Manager, Reader, Writer |
| `codeengine.tenant.entities.create` | Create project contents, such as applications, job definitions, and jobs | Manager, Writer |
| `codeengine.tenant.entities.update` | Modify existing items already contained by a project, such as applications, jobs, or job definitions.  This does not include the ability to create or delete these items. | Manager, Writer |
| `codeengine.tenant.entities.delete` | Delete existing items from within a project | Manager, Writer |
| `codeengine.tenant.entities.read` | List and view existing items within a project | Manager, Reader, Writer |
| `codeengine.computeenvironment.create` | Allows you to create a Code Engine Compute Environment. | Compute Environment Administrator |
| `codeengine.computeenvironment.delete` | Allows you to delete compute environments. | Compute Environment Administrator |
| `codeengine.computeenvironment.projects.create` | Allows you to create projects in this compute environment. | Manager, Writer |
| `codeengine.computeenvironment.projects.delete` | Allows you to delete projects in this compute environment. | Manager, Writer |
{: caption="Table 20. Service actions - Code Engine" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="codeengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table20}

## Cognos Dashboard
{: #cognos-dashboard-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cognos-dashboard` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 21. Platform roles - Cognos Dashboard" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="cognos-dashboard"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table21}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 21. Service roles - Cognos Dashboard" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="cognos-dashboard"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table21}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `cognos-dashboard.dashboard.author` | Author Dashboard | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
{: caption="Table 21. Service actions - Cognos Dashboard" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="cognos-dashboard"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table21}

## IBM Cloud Compliance and Security Center
{: #compliance-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `compliance` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 22. Platform roles - IBM Cloud Compliance and Security Center" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="compliance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table22}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 22. Service roles - IBM Cloud Compliance and Security Center" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="compliance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table22}

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
| `compliance.posture-management.attachments-create` | Create Attachments | Administrator, Editor |
| `compliance.posture-management.attachments-update` | Update Attachments | Administrator, Editor |
| `compliance.posture-management.attachments-read` | Read Attachments | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.attachments-delete` | Delete Attachments | Administrator, Editor |
| `compliance.posture-management.control-libraries-create` | Add New Control Libraries | Administrator, Editor |
| `compliance.posture-management.control-libraries-read` | Read Control Libraries | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.control-libraries-update` | Update Control Libraries | Administrator, Editor |
| `compliance.posture-management.control-libraries-delete` | Delete Control Libraries | Administrator, Editor |
| `compliance.posture-management.scans-create` | Add New Scans | Administrator, Editor |
| `compliance.posture-management.scans-read` | Read Scans | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.scans-update` | Update Scans | Administrator, Editor |
| `compliance.posture-management.scans-delete` | Delete Scans | Administrator, Editor |
| `compliance.posture-management.reports-read` | View results | Administrator, Editor, Operator |
| `compliance.posture-management.profiles-compare` | Compare profiles | Administrator, Editor, Operator, Viewer |
| `compliance.posture-management.attachments-upgrade` | Upgrade attachments | Administrator, Editor |
{: caption="Table 22. Service actions - IBM Cloud Compliance and Security Center" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="compliance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table22}

## Consult with IBM Cloud Garage
{: #consult-with-icg-wes-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `consult-with-icg-wes` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 23. Platform roles - Consult with IBM Cloud Garage" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="consult-with-icg-wes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table23}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 23. Service roles - Consult with IBM Cloud Garage" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="consult-with-icg-wes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table23}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `consult-with-icg-wes.dashboard.view` | The ability to view your provisioned Consult with IBM Garage services in the dashboard. | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
{: caption="Table 23. Service actions - Consult with IBM Cloud Garage" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="consult-with-icg-wes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table23}

## Container Registry
{: #container-registry-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `container-registry` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 24. Service roles - Container Registry" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="container-registry"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table24}

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
{: caption="Table 24. Service actions - Container Registry" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="container-registry"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table24}

## Kubernetes Service
{: #containers-kubernetes-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `containers-kubernetes` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 25. Platform roles - Kubernetes Service" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="containers-kubernetes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table25}

| Role | Description |
| ----- | :----- |
| Compliance Management | Allows Security and Compliance Center to access your cluster to setup, run, and fetch compliance results. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 25. Service roles - Kubernetes Service" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="containers-kubernetes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table25}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `containers-kubernetes.cluster.create` | Users such as cluster or account administrators can create and delete clusters or set up cluster-wide features like service endpoints or managed add-ons. | Administrator, Compliance Management |
| `containers-kubernetes.cluster.read` | Users such as auditors or billing can see cluster details but not modify the infrastructure. | Administrator, Editor, Operator, Viewer |
| `containers-kubernetes.cluster.operate` | Users such as reliability or DevOps engineers can add worker nodes and troubleshoot infrastructure such as reloading a worker node. They cannot create, delete, change credentials, or set up cluster-wide features. | Administrator, Operator |
| `containers-kubernetes.cluster.update` | Users such as developers can bind service, work with Ingress resources, and set up log forwarding for their apps but cannot modify the infrastructure. | Administrator, Editor |
| `containers-kubernetes.kube.read` | Users get read access to most Kubernetes resources in the namespace, but not to certain resources like roles, role bindings, or secrets. Corresponds to the RBAC view cluster role, which can be scoped to a namespace. | Reader |
| `containers-kubernetes.kube.write` | Users get read and write access to most Kubernetes resources in the namespace, but not to certain resources like roles or role bindings. Corresponds to the RBAC edit cluster role, which can be scoped to a namespace. | Writer |
| `containers-kubernetes.kube.manage` | When scoped to one namespace: Users can read and write to all Kubernetes resources in the namespace, but not to objects that apply across namespaces, the namespace resource quota, or the namespace itself. Corresponds to the RBAC admin cluster role to that namespace. When scoped to all namespaces in the cluster (by leaving the previous namespace field empty): Users can read and write to all Kubernetes resources in all namespaces in the cluster and work with objects that apply across namespaces, like top pods, top nodes, or creating an Ingress resource to make apps publicly available. Corresponds to the RBAC cluster-admin cluster role. | Manager |
{: caption="Table 25. Service actions - Kubernetes Service" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="containers-kubernetes"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table25}

## Context-Based Restrictions
{: #context-based-restrictions-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `context-based-restrictions` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 26. Platform roles - Context-Based Restrictions" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="context-based-restrictions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table26}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `context-based-restrictions.zone.create` | Network Zone Create | Administrator, Editor |
| `context-based-restrictions.zone.read` | Network Zone Read | Administrator, Editor, Viewer |
| `context-based-restrictions.zone.update` | Network Zone Update | Administrator, Editor |
| `context-based-restrictions.zone.delete` | Network Zone Delete | Administrator, Editor |
| `context-based-restrictions.account-settings.read` | View context-based restriction account settings | Administrator, Editor, Viewer |
| `context-based-restrictions.account-settings.update` | Update context-based restriction account settings | Administrator |
{: caption="Table 26. Service actions - Context-Based Restrictions" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="context-based-restrictions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table26}

## Continuous Delivery
{: #continuous-delivery-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `continuous-delivery` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can modify the Authorized Users list. |
| Editor | As an editor, you can create, view, update, change the plan for, and delete instances of the Continuous Delivery service. |
| Operator | As an operator, you can view instances of the Continuous Delivery service. |
{: row-headers}
{: caption="Table 27. Platform roles - Continuous Delivery" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="continuous-delivery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table27}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 27. Service roles - Continuous Delivery" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="continuous-delivery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table27}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `continuous-delivery.dashboard.view` | View instances of the Continuous Delivery service. | Administrator, Editor, Operator |
| `continuous-delivery.instance.add-auth-users` | Add entries to the Authorized Users list on the Manage tab of a Continuous Delivery service instance. | Administrator, Manager, Writer |
| `continuous-delivery.instance.remove-auth-users` | Remove entries from the Authorized Users list on the Manage tab of a Continuous Delivery service instance. | Administrator, Manager, Writer |
| `continuous-delivery.instance.config-auth-users` | Configure authorized users. | Administrator, Manager |
{: caption="Table 27. Service actions - Continuous Delivery" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="continuous-delivery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table27}

## Converlistics
{: #converlistics-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `converlistics` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 28. Platform roles - Converlistics" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="converlistics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table28}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `converlistics.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 28. Service actions - Converlistics" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="converlistics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table28}

## Watson Assistant
{: #conversation-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `conversation` for the service name.

| Role | Description |
| ----- | :----- |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 29. Platform roles - Watson Assistant" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="conversation"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table29}

| Role | Description |
| ----- | :----- |
| Logs Reader | As a logs reader, you can view user conversations and analytics. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Version Maker | As a Version Maker, you will be able to create or delete versions of your assistant. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 29. Service roles - Watson Assistant" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="conversation"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table29}

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
| `conversation.logs.read` | Can view skill analytics and access user conversation logs. | Logs Reader, Manager |
| `conversation.assistant.list` | Can list assistant or skill | Manager, Reader, Viewer, Writer |
| `conversation.assistant.default` | Default access for Assistant | Manager, Reader, Viewer, Writer |
| `conversation.environment.write` | Can rename, edit, or delete an environment | Manager, Writer |
| `conversation.environment.read` | Can open and view an environment | Manager, Reader, Writer |
| `conversation.release.write` | Can create or delete a Release for an Assistant | Manager, Version Maker, Writer |
{: caption="Table 29. Service actions - Watson Assistant" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="conversation"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table29}

## IBM Cloud Pak for Data
{: #cp4d-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `cp4d` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 30. Platform roles - IBM Cloud Pak for Data" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="cp4d"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table30}

| Role | Description |
| ----- | :----- |
| CloudPak Data Engineer | Create or view governance artifacts. |
| CloudPak Data Scientist | Find data in catalogs and use data in projects. |
| CloudPak Data Steward | Create or view governance artifacts and curate data into catalogs. |
| Governance Artifacts Administrator | Manage governance artifacts |
| Manager | Manage catalogs, governance artifacts, categories, and workflow. |
| Reporting Administrator | Manage reports on Watson Knowledge Catalog data. |
{: row-headers}
{: caption="Table 30. Service roles - IBM Cloud Pak for Data" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="cp4d"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table30}

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
| `cp4d.project.manage` | Manage projects | Manager |
| `cp4d.deployment-space.manage` | Manage deployment space | Manager |
| `cp4d.glossary.admin` | Manage governance artifacts | Governance Artifacts Administrator |
{: caption="Table 30. Service actions - IBM Cloud Pak for Data" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="cp4d"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table30}

## Db2 Warehouse
{: #dashdb-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `dashdb` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 31. Platform roles - Db2 Warehouse" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="dashdb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table31}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 31. Service roles - Db2 Warehouse" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="dashdb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table31}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `dashdb.console.access` | dashdb.console.access | Manager, Writer |
| `dashdb.console.manage-users` | Allows management of users for database access such as creating new users or assign and IAM user or service id to a database user. | Administrator, Manager |
| `dashdb.console.monitor` | Allows viewing of metrics and information that allow you to understand the resources your database is using or workload it is running. | Administrator, Manager, Operator, Viewer, Writer |
| `dashdb.console.scale` | scale operation | Administrator, Editor, Operator |
| `dashdb.console.backup` | backup operation | Administrator, Editor, Operator |
| `dashdb.console.restore` | restore operation | Administrator, Editor, Operator |
| `dashdb.console.settings` | set configuration | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/configuration` | Get deployment configuration | Administrator, Editor, Operator, Viewer |
| `dashdb.console.view-settings` | view database settings | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/regions` | Read discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/task_infos/:task_id` | Read a Task metadata | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/backups/:backup_id` | Read a backup | Administrator, Editor, Operator, Viewer |
| `DELETE /v4/:platform/backups/:backup_id` | Delete a backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v4/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data` | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/tasks` | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/task_infos` | Read all deployment tasks metadata | Administrator, Editor, Operator, Viewer |
| `GET /v4/:platform/deployments/:deployment_id/backups` | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/backups` | Create an on-demand backup | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/remotes` | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| `DELETE /v4/:platform/deployments/:deployment_id/management/database_connections` | Kill all database connections | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/configuration` | Update deployment configuration | Administrator, Editor, Operator |
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
| `POST /v4/:platform/deployments/:deployment_id/inplace_restores` | Perform in place database restore | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/groups/member` | Update scaling member configuration | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id/adminpassword` | Update admin password | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id/locked` | Update user locked state | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/describe_updates` | Get db updates | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/db_updates` | Create db update | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/users/:user_id/password` | Update password | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/check_updates` | Check deployment for available updates | Administrator, Editor, Operator, Viewer |
| `PATCH /v4/:platform/deployments/:deployment_id/billable` | Set billable annotation to true | Administrator, Editor, Operator |
| `PATCH /v4/:platform/deployments/:deployment_id/migrated` | Set migration flag to false | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/dr_take_over` | dr_take_over | Administrator, Editor, Operator |
| `GET /v4/:platform/deployments/:deployment_id/get_dr` | get_dr | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id/configuration` | Get deployment configuration | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/deployables` | Read Deployables | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/regions` | Read discover available regions | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/tasks/:task_id` | Read a Task | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/task_infos/:task_id` | Read a Task metadata | Administrator, Editor, Operator, Viewer |
| `GET /v5/:platform/backups/:backup_id` | Read a backup | Administrator, Editor, Operator, Viewer |
| `DELETE /v5/:platform/backups/:backup_id` | Delete a backup | Administrator, Editor, Operator |
| `GET /v5/:platform/deployments/:deployment_id` | Read a Deployment | Administrator, Editor, Operator, Viewer |
| `PATCH /v5/:platform/deployments/:deployment_id` | Update a Deployment | Administrator, Editor, Operator |
| `GET /v5/:platform/deployables/:deployable_id/groups` | Read deployable group | Administrator, Editor, Operator, Viewer |
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
{: caption="Table 31. Service actions - Db2 Warehouse" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="dashdb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table31}

## Db2 on Cloud
{: #dashdb-for-transactions-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `dashdb-for-transactions` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 32. Platform roles - Db2 on Cloud" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="dashdb-for-transactions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table32}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
{: row-headers}
{: caption="Table 32. Service roles - Db2 on Cloud" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="dashdb-for-transactions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table32}

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
| `POST /v4/:platform/deployments/:deployment_id/rebalance` | rebalance tablespaces | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/reducemax` | reclaim disk space | Administrator, Editor, Operator, Viewer |
| `POST /v4/:platform/deployments/:deployment_id/configure_iks_worker` | Configure bare metal and dedicated virtual machine | Administrator, Editor, Operator, Viewer |
| `POST /hyperwarp_messages` | hyperwarp subscriber endpoint | Administrator, Editor, Operator |
| `POST /v4/:platform/deployments/:deployment_id/hibernate` | Hibernate the target instance | Administrator, Editor, Operator |
| `DELETE /v4/:platform/deployments/:deployment_id/hibernate` | Reactivate the target hibernating instance. | Administrator, Editor, Operator |
{: caption="Table 32. Service actions - Db2 on Cloud" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="dashdb-for-transactions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table32}

## IBM Data Replication on Cloud
{: #data-replication-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `data-replication` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 33. Platform roles - IBM Data Replication on Cloud" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="data-replication"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table33}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 33. Service roles - IBM Data Replication on Cloud" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="data-replication"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table33}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `data-replication.replications.retrieve` | data-replication.replications.retrieve | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `data-replication.replications.create` | Create replication | Manager, Writer |
| `data-replication.replications.operate` | Operate Replication | Manager, Writer |
| `data-replication.replications.delete` | Delete Replication | Manager, Writer |
| `data-replication.replications.update` | Update Replication | Manager, Writer |
{: caption="Table 33. Service actions - IBM Data Replication on Cloud" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="data-replication"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table33}

## Watson Studio
{: #data-science-experience-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `data-science-experience` for the service name.

No supported roles.
## Data Store for Memcache
{: #data-store-for-memcache-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `data-store-for-memcache` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
{: row-headers}
{: caption="Table 35. Platform roles - Data Store for Memcache" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="data-store-for-memcache"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table35}

| Role | Description |
| ----- | :----- |
| Manager | null |
| Reader | null |
| Writer | null |
{: row-headers}
{: caption="Table 35. Service roles - Data Store for Memcache" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="data-store-for-memcache"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table35}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `data-store-for-memcache.keys.create` |  | Administrator, Manager |
| `data-store-for-memcache.keys.read` |  | Manager, Reader, Writer |
| `data-store-for-memcache.keys.update` |  | Manager, Writer |
| `data-store-for-memcache.keys.delete` |  | Manager |
| `data-store-for-memcache.keys.encode` |  | Manager, Writer |
| `data-store-for-memcache.keys.decode` |  | Manager, Writer |
{: caption="Table 35. Service actions - Data Store for Memcache" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="data-store-for-memcache"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table35}

## Data Virtualization
{: #data-virtualization-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `data-virtualization` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 36. Platform roles - Data Virtualization" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="data-virtualization"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table36}

| Role | Description |
| ----- | :----- |
| DataAccess (For Service to Service Authorization Only) | Used for Service to Service authorization.  Do not choose this role for service credential generation. |
| Manager (For generated service credentials only) | This role is only enabled for generated service credentials.  Using this role will grant the generated Service ID Manager access. |
{: row-headers}
{: caption="Table 36. Service roles - Data Virtualization" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="data-virtualization"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table36}

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
{: caption="Table 36. Service actions - Data Virtualization" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="data-virtualization"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table36}

## Netezza Performance Server
{: #data-warehouse-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `data-warehouse` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 37. Platform roles - Netezza Performance Server" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="data-warehouse"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table37}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 37. Service roles - Netezza Performance Server" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="data-warehouse"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table37}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `data-warehouse.dashboard.view` | The capability to view the service instance details page | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `data-warehouse.database.connect` | The  action describes who can connect to the database | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `data-warehouse.database.admin` | The role defines people with admin privileges on the database | Administrator, Manager |
{: caption="Table 37. Service actions - Netezza Performance Server" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="data-warehouse"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table37}

## Databases for DataStax
{: #databases-for-cassandra-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-cassandra` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 38. Platform roles - Databases for DataStax" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="databases-for-cassandra"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table38}

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
{: caption="Table 38. Service actions - Databases for DataStax" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="databases-for-cassandra"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table38}

## Databases for Elasticsearch
{: #databases-for-elasticsearch-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-elasticsearch` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 39. Platform roles - Databases for Elasticsearch" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="databases-for-elasticsearch"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table39}

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
{: caption="Table 39. Service actions - Databases for Elasticsearch" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="databases-for-elasticsearch"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table39}

## Databases for EDB
{: #databases-for-enterprisedb-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-enterprisedb` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 40. Platform roles - Databases for EDB" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="databases-for-enterprisedb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table40}

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
{: caption="Table 40. Service actions - Databases for EDB" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="databases-for-enterprisedb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table40}

## Databases for etcd
{: #databases-for-etcd-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-etcd` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 41. Platform roles - Databases for etcd" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="databases-for-etcd"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table41}

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
{: caption="Table 41. Service actions - Databases for etcd" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="databases-for-etcd"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table41}

## Databases for MongoDB
{: #databases-for-mongodb-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-mongodb` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 42. Platform roles - Databases for MongoDB" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="databases-for-mongodb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table42}

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
{: caption="Table 42. Service actions - Databases for MongoDB" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="databases-for-mongodb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table42}

## Databases for MySQL
{: #databases-for-mysql-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-mysql` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 43. Platform roles - Databases for MySQL" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="databases-for-mysql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table43}

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
{: caption="Table 43. Service actions - Databases for MySQL" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="databases-for-mysql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table43}

## Databases for PostgreSQL
{: #databases-for-postgresql-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-postgresql` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 44. Platform roles - Databases for PostgreSQL" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="databases-for-postgresql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table44}

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
{: caption="Table 44. Service actions - Databases for PostgreSQL" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="databases-for-postgresql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table44}

## Databases for Redis
{: #databases-for-redis-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `databases-for-redis` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 45. Platform roles - Databases for Redis" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="databases-for-redis"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table45}

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
{: caption="Table 45. Service actions - Databases for Redis" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="databases-for-redis"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table45}

## IBM Knowledge Catalog for Watson Data and AI
{: #datacatalog-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `datacatalog` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 46. Platform roles - IBM Knowledge Catalog for Watson Data and AI" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="datacatalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table46}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 46. Service roles - IBM Knowledge Catalog for Watson Data and AI" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="datacatalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table46}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `datacatalog` |  | Administrator |
| `datacatalog.catalog.create` |  | Administrator, Manager, Writer |
{: caption="Table 46. Service actions - IBM Knowledge Catalog for Watson Data and AI" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="datacatalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table46}

## DataStage
{: #datastage-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `datastage` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 47. Platform roles - DataStage" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="datastage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table47}

| Role | Description |
| ----- | :----- |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 47. Service roles - DataStage" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="datastage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table47}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `datastage.dashboard.view` | DataStage dashboard view | Administrator, Editor, Operator, Reader |
{: caption="Table 47. Service actions - DataStage" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="datastage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table47}

## Direct Link
{: #directlink-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `directlink` for the service name.

No supported roles.
## Direct Link Connect
{: #directlink.connect-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `directlink.connect` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 49. Platform roles - Direct Link Connect" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="directlink.connect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table49}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `directlink.connect.view` | View | Administrator, Editor, Operator, Viewer |
| `directlink.connect.edit` | Edit | Administrator, Editor |
{: caption="Table 49. Service actions - Direct Link Connect" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="directlink.connect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table49}

## Direct Link Dedicated
{: #directlink.dedicated-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `directlink.dedicated` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 50. Platform roles - Direct Link Dedicated" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="directlink.dedicated"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table50}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `directlink.dedicated.view` | View | Administrator, Editor, Operator, Viewer |
| `directlink.dedicated.edit` | Edit | Administrator, Editor |
{: caption="Table 50. Service actions - Direct Link Dedicated" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="directlink.dedicated"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table50}

## Discovery
{: #discovery-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `discovery` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 51. Service roles - Discovery" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="discovery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table51}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `PUT /discovery` | Update existing resources | Manager, Writer |
| `POST /discovery` | Create new resources | Manager, Writer |
| `DELETE /discovery` | Delete resources | Manager, Writer |
| `PATCH /discovery` | Make partial update to resources | Manager, Writer |
| `GET /discovery` | Retrieve resources | Manager, Reader, Writer |
{: caption="Table 51. Service actions - Discovery" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="discovery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table51}

## Dizzion DaaS
{: #dizziondaas-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `dizziondaas` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 52. Platform roles - Dizzion DaaS" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="dizziondaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table52}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `dizziondaas.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 52. Service actions - Dizzion DaaS" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="dizziondaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table52}

## DNS Services
{: #dns-svcs-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `dns-svcs` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 53. Platform roles - DNS Services" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="dns-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table53}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 53. Service roles - DNS Services" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="dns-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table53}

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
{: caption="Table 53. Service actions - DNS Services" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="dns-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table53}

## Dynamic Dashboard Embedded
{: #dynamic-dashboard-embedded-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `dynamic-dashboard-embedded` for the service name.

| Role | Description |
| ----- | :----- |
| null | null |
| null | null |
| null | null |
{: row-headers}
{: caption="Table 54. Service roles - Dynamic Dashboard Embedded" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="dynamic-dashboard-embedded"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table54}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `dynamic-dashboard-embedded.instances.write` |  | null, null, null |
{: caption="Table 54. Service actions - Dynamic Dashboard Embedded" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="dynamic-dashboard-embedded"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table54}

## ibm-cloud-for-education
{: #education-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `education` for the service name.

No supported roles.
## IBM Cloud Platform Enterprise Service
{: #enterprise-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `enterprise` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | Administrators can update the enterprise, create accounts and account groups, move accounts between account groups, import existing accounts, and view usage reports. |
| Editor | Editors can update the enterprise, create accounts and account groups, view usage reports, and import accounts. |
| Operator | Operators can view the enterprise, account groups, and accounts. |
| Viewer | Viewers can view the enterprise, account groups, and accounts. |
{: row-headers}
{: caption="Table 56. Platform roles - IBM Cloud Platform Enterprise Service" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="enterprise"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table56}

| Role | Description |
| ----- | :----- |
| Usage Report Viewer | Usage report viewers can view the usage reports for the entire enterprise, an account group and its accounts, or a specific account. |
{: row-headers}
{: caption="Table 56. Service roles - IBM Cloud Platform Enterprise Service" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="enterprise"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table56}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `enterprise.enterprise.create` |  | Administrator |
| `enterprise.enterprise.update` |  | Administrator, Editor |
| `enterprise.enterprise.retrieve` |  | Administrator, Editor, Operator, Usage Report Viewer, Viewer |
| `enterprise.enterprise.import` |  | Administrator, Editor |
| `enterprise.enterprise.retrieve-usage-report` |  | Administrator, Editor, Usage Report Viewer |
| `enterprise.enterprise.attach-config-rules` |  | Administrator |
| `enterprise.enterprise.detach-config-rules` |  | Administrator |
| `enterprise.enterprise.update-config-rules` |  | Administrator |
| `enterprise.enterprise.attach-templates` |  | Administrator |
| `enterprise.enterprise.detach-templates` |  | Administrator |
| `enterprise.enterprise.update-templates` |  | Administrator |
| `enterprise.account-group.create` |  | Administrator, Editor |
| `enterprise.account-group.update` |  | Administrator, Editor |
| `enterprise.account-group.delete` |  | Administrator, Editor |
| `enterprise.account-group.retrieve` |  | Administrator, Editor, Operator, Usage Report Viewer, Viewer |
| `enterprise.account-group.retrieve-usage-report` |  | Administrator, Editor, Usage Report Viewer |
| `enterprise.account-group.attach-config-rules` |  | Administrator |
| `enterprise.account-group.detach-config-rules` |  | Administrator |
| `enterprise.account-group.update-config-rules` |  | Administrator |
| `enterprise.account-group.attach-templates` |  | Administrator |
| `enterprise.account-group.detach-templates` |  | Administrator |
| `enterprise.account-group.update-templates` |  | Administrator |
| `enterprise.account.create` |  | Administrator, Editor |
| `enterprise.account.update` |  | Administrator, Editor |
| `enterprise.account.move` |  | Administrator |
| `enterprise.account.delete` |  | Administrator, Editor |
| `enterprise.account.retrieve` |  | Administrator, Editor, Operator, Usage Report Viewer, Viewer |
| `enterprise.account.retrieve-usage-report` |  | Administrator, Editor, Usage Report Viewer |
| `enterprise.account.attach-config-rules` |  | Administrator |
| `enterprise.account.detach-config-rules` |  | Administrator |
| `enterprise.account.update-config-rules` |  | Administrator |
| `enterprise.account.attach-templates` |  | Administrator |
| `enterprise.account.detach-templates` |  | Administrator |
| `enterprise.account.update-templates` |  | Administrator |
{: caption="Table 56. Service actions - IBM Cloud Platform Enterprise Service" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="enterprise"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table56}

## License and Entitlement
{: #entitlement-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `entitlement` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 57. Platform roles - License and Entitlement" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="entitlement"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table57}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `entitlement.entitlement.write` |  | Administrator, Editor |
| `entitlement.entitlement.write-admin` |  | Administrator |
{: caption="Table 57. Service actions - License and Entitlement" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="entitlement"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table57}

## Event Notifications
{: #event-notifications-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `event-notifications` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 58. Platform roles - Event Notifications" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="event-notifications"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table58}

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
{: caption="Table 58. Service roles - Event Notifications" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="event-notifications"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table58}

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
| `event-notifications.integrations.create` | This action is to create an integration. For example BYOK integration with EN. | Administrator, Event Source Manager, Manager |
| `event-notifications.integrations.update` | This action is to update an already  created integration with EN | Administrator, Event Source Manager, Manager |
| `event-notifications.integrations.read` | This action is to get an already-created integration | Administrator, Event Source Manager, Manager |
| `event-notifications.integrations.list` | This action is to list all integrations with EN | Administrator, Event Source Manager, Manager |
| `event-notifications.integrations.delete` | This action is to delete integration | Event Source Manager, Manager |
{: caption="Table 58. Service actions - Event Notifications" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="event-notifications"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table58}

## IBM Cloud Functions
{: #functions-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `functions` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 59. Service roles - IBM Cloud Functions" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="functions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table59}

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
{: caption="Table 59. Service actions - IBM Cloud Functions" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="functions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table59}

## Globalization Pipeline
{: #g11n-pipeline-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `g11n-pipeline` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 60. Platform roles - Globalization Pipeline" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="g11n-pipeline"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table60}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 60. Service roles - Globalization Pipeline" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="g11n-pipeline"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table60}

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
{: caption="Table 60. Service actions - Globalization Pipeline" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="g11n-pipeline"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table60}

## GhoST API
{: #ghost-api-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `ghost-api` for the service name.

No supported roles.
## GhoST Tagging Service
{: #ghost-tags-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `ghost-tags` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 62. Platform roles - GhoST Tagging Service" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="ghost-tags"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table62}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `ghost-tags.create-access-tag` | The ability to create access management tags in an account | Administrator |
| `ghost-tags.delete-access-tag` | The ability to delete access management tags in an account | Administrator |
{: caption="Table 62. Service actions - GhoST Tagging Service" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="ghost-tags"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table62}

## Global Catalog
{: #globalcatalog-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `globalcatalog` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | Administrators can change object metadata or visibility for private services added to the account and can restrict the visibility of a public service. |
| Editor | Editors can change object metadata, but can’t change visibility for private services added to the account. |
| Operator | Operators can view private services added to the account. |
| Viewer | Viewers can view private services added to the account. |
{: row-headers}
{: caption="Table 63. Platform roles - Global Catalog" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="globalcatalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table63}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `globalcatalog.is.admin` | Is Admin | Administrator |
| `globalcatalog.is.editor` | Is Editor | Editor |
| `globalcatalog.is.viewer` | Is Viewer | Operator, Viewer |
{: caption="Table 63. Service actions - Global Catalog" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="globalcatalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table63}

## Personal Catalog
{: #globalcatalog-collection-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `globalcatalog-collection` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 64. Platform roles - Personal Catalog" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="globalcatalog-collection"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table64}

| Role | Description |
| ----- | :----- |
| IBMOperation | (Internal) - IBM Use only |
| Publisher | You can publish offerings that are approved by IBM and that are in a private catalog to which you're assigned the viewer role. |
{: row-headers}
{: caption="Table 64. Service roles - Personal Catalog" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="globalcatalog-collection"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table64}

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
{: caption="Table 64. Service actions - Personal Catalog" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="globalcatalog-collection"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table64}

## Instance Management
{: #globalcatalog-instance-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `globalcatalog-instance` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 65. Platform roles - Instance Management" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="globalcatalog-instance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table65}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `globalcatalog-instance.dashboard.view` | View Dashboard | Administrator, Editor, Operator, Viewer |
{: caption="Table 65. Service actions - Instance Management" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="globalcatalog-instance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table65}

## HPCaaS from Rescale
{: #hpcaas-from-rescale-prod-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `hpcaas-from-rescale-prod` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
| Editor | null |
| Operator | null |
{: row-headers}
{: caption="Table 66. Platform roles - HPCaaS from Rescale" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="hpcaas-from-rescale-prod"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table66}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `hpcaas-from-rescale-prod.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 66. Service actions - HPCaaS from Rescale" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="hpcaas-from-rescale-prod"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table66}

## Hyper Protect Virtual Server
{: #hpvs-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `hpvs` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 67. Platform roles - Hyper Protect Virtual Server" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="hpvs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table67}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 67. Service roles - Hyper Protect Virtual Server" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="hpvs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table67}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `hpvs.dashboard.view` | Can view the dashboard | Administrator, Editor, Manager, Operator, Reader, Writer |
{: caption="Table 67. Service actions - Hyper Protect Virtual Server" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="hpvs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table67}

## Hyper Protect Crypto Services
{: #hs-crypto-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `hs-crypto` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 68. Platform roles - Hyper Protect Crypto Services" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="hs-crypto"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table68}

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
{: caption="Table 68. Service roles - Hyper Protect Crypto Services" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="hs-crypto"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table68}

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
{: caption="Table 68. Service actions - Hyper Protect Crypto Services" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="hs-crypto"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table68}

## Hyper Protect DBaaS for MongoDB 
{: #hyperp-dbaas-mongodb-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `hyperp-dbaas-mongodb` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 69. Service roles - Hyper Protect DBaaS for MongoDB " caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="hyperp-dbaas-mongodb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table69}

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
| `hyperp-dbaas-mongodb.backups.list` | List backup files | Manager, Reader, Writer |
| `hyperp-dbaas-mongodb.backups.configuration.update` | Update backup configuration | Manager |
| `hyperp-dbaas-mongodb.backups.configuration.read` | Show backup configuration | Manager, Reader, Writer |
{: caption="Table 69. Service actions - Hyper Protect DBaaS for MongoDB " caption-side="top"}
{: tab-title="Actions"}
{: tab-group="hyperp-dbaas-mongodb"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table69}

## Hyper Protect DBaaS for PostgreSQL
{: #hyperp-dbaas-postgresql-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `hyperp-dbaas-postgresql` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 70. Service roles - Hyper Protect DBaaS for PostgreSQL" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="hyperp-dbaas-postgresql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table70}

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
| `hyperp-dbaas-postgresql.backups.list` | List backup files | Manager, Reader, Writer |
| `hyperp-dbaas-postgresql.backups.configuration.update` | Update backup configuration | Manager |
| `hyperp-dbaas-postgresql.backups.configuration.read` | Show backup configuration | Manager, Reader, Writer |
{: caption="Table 70. Service actions - Hyper Protect DBaaS for PostgreSQL" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="hyperp-dbaas-postgresql"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table70}

## IAM Access Management
{: #iam-access-management-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iam-access-management` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 71. Platform roles - IAM Access Management" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="iam-access-management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table71}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `iam-access-management.settings.read` | Read Access Management account settings | Administrator, Editor, Viewer |
| `iam-access-management.user-access-list.read` | Read User Access list | Administrator, Editor |
| `iam-access-management.insight.get` | Read Access Policy insights | Administrator, Editor |
| `iam-access-management.settings.update` | Update Access Management account settings | Administrator |
{: caption="Table 71. Service actions - IAM Access Management" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="iam-access-management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table71}

## Role Management
{: #iam-access-management.customRole-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iam-access-management.customRole` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 72. Platform roles - Role Management" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="iam-access-management.customRole"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table72}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `iam-access-management.customRole.create` | The ability to create custom roles. | Administrator |
| `iam-access-management.customRole.update` | The ability to edit and update custom roles. | Administrator, Editor |
| `iam-access-management.customRole.delete` | The ability to delete a custom role. | Administrator |
| `iam-access-management.customRole.read` | Retrieve custom roles | Administrator, Editor, Operator, Viewer |
{: caption="Table 72. Service actions - Role Management" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="iam-access-management.customRole"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table72}

## AM Insights
{: #iam-access-management.insight-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iam-access-management.insight` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 73. Platform roles - AM Insights" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="iam-access-management.insight"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table73}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `iam-access-management.insight.get` | Read Access Management insights | Administrator, Editor |
{: caption="Table 73. Service actions - AM Insights" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="iam-access-management.insight"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table73}

## IAM Access Groups
{: #iam-groups-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iam-groups` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can view, create, edit, and delete access groups including adding or removing users from the groups. You can also assign access to the group and manage access for others to work with access groups. |
| Editor | As an editor, you can view, create, edit, and delete access groups including adding or removing users from the groups. |
| Viewer | As a viewer, you can view access groups and its members. |
{: row-headers}
{: caption="Table 74. Platform roles - IAM Access Groups" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="iam-groups"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table74}

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
{: caption="Table 74. Service actions - IAM Access Groups" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="iam-groups"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table74}

## IAM Identity Service
{: #iam-identity-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iam-identity` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | An Administrator can view, update and delete service IDs and API keys. |
| Editor | An Editor can view and update service IDs and API keys. |
| Operator | An Operator can view, update and delete service IDs and API keys. |
| Viewer | A Viewer can view service IDs and API keys. |
{: row-headers}
{: caption="Table 75. Platform roles - IAM Identity Service" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="iam-identity"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table75}

| Role | Description |
| ----- | :----- |
| Service ID creator | Can create service IDs when the account setting to restrict service ID creation is enabled. |
| User API key creator | Can create API keys when the account setting to restrict API key creation is enabled. |
{: row-headers}
{: caption="Table 75. Service roles - IAM Identity Service" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="iam-identity"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table75}

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
| `iam-identity.profile.get_session` | Get sessions associated to a Trusted Profile. | Administrator, Operator |
| `iam-identity.profile.revoke_session` | Revoke sessions associated to Trusted Profile | Administrator, Operator |
| `iam-identity.profile.linkToResource` | Link a trusted profile to a resource | Administrator, Editor, Operator |
| `iam-identity.idp.get` | Get the details of an existing Identity Provider configuration. | Administrator, Editor, Operator |
| `iam-identity.idp.list` | List Identity Provider configurations. | Administrator, Editor, Operator |
| `iam-identity.idp.create` | Create a new Identity Provider configuration. | Administrator, Operator |
| `iam-identity.idp.update` | Update an existing Identity Provider configuration. | Administrator, Editor, Operator |
| `iam-identity.idp.delete` | Delete an Identity Provider configuration. | Administrator, Operator |
| `iam-identity.idp.test` | Test an Identity Provider configuration. | Administrator, Editor, Operator |
| `iam-identity.idp.metadata` | Get the metadata of an identity provider | Administrator, Editor, Operator |
| `iam-identity.account.get` | Get the account configuration. | Administrator, Editor, Operator, Viewer |
| `iam-identity.account.create` | Create a new account configuration. | Administrator, Operator |
| `iam-identity.account.update` | Update an existing account configuration. | Administrator, Editor, Operator |
| `iam-identity.account.create` | Create a new account configuration. | Administrator, Operator |
| `iam-identity.account.update` | Update an existing account configuration. | Administrator, Editor, Operator |
| `iam-identity.account.enable_idp` | Enable an Identity Provider configuration for the account. | Administrator, Editor, Operator |
| `iam-identity.account.disable_idp` | Disable an Identity Provider configuration for the account. | Administrator, Editor, Operator |
| `iam-identity.account.delete` | Delete an account configuration. | Administrator, Operator |
| `iam-identity.session.manage` | Manage the user sessions of an account. | Administrator |
| `iam-identity.crnmapping.create` | Create a CRN mapping for an account | Administrator |
| `iam-identity.crnmapping.read` | Read CRN mappings of an account | Administrator |
| `iam-identity.crnmapping.delete` | Delete a CRN mapping for an account | Administrator |
| `iam-identity.activity.get` | Get authentication activity information | Administrator, Editor, Operator, Viewer |
| `iam-identity.report.create` | Trigger report creation for an account | Administrator |
| `iam-identity.report.get` | Get a report for an account | Administrator |
| `iam-identity.mfa-status.get` | Get MFA Enrollment Status | Administrator |
{: caption="Table 75. Service actions - IAM Identity Service" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="iam-identity"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table75}

## Identity and Access Management
{: #iam-svcs-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iam-svcs` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 76. Platform roles - Identity and Access Management" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="iam-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table76}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `iam-svcs.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 76. Service actions - Identity and Access Management" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="iam-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table76}

## Analytics Engine
{: #ibmanalyticsengine-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `ibmanalyticsengine` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 77. Platform roles - Analytics Engine" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="ibmanalyticsengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table77}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 77. Service roles - Analytics Engine" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="ibmanalyticsengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table77}

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
{: caption="Table 77. Service actions - Analytics Engine" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="ibmanalyticsengine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table77}

## IBM Cloud Platform
{: #ibmcloud-platform-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `ibmcloud-platform` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
| Editor | null |
| Operator | null |
| Viewer | null |
{: row-headers}
{: caption="Table 78. Platform roles - IBM Cloud Platform" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="ibmcloud-platform"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table78}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `ibmcloud-platform.osbbroker.create` |  | Administrator, Editor |
| `ibmcloud-platform.osbbroker.update` |  | Administrator, Editor, Operator |
| `ibmcloud-platform.osbbroker.retrieve` |  | Administrator, Editor, Operator, Viewer |
| `ibmcloud-platform.osbbroker.delete` |  | Administrator, Editor |
{: caption="Table 78. Service actions - IBM Cloud Platform" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="ibmcloud-platform"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table78}

## Cloud Internet Services
{: #internet-svcs-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `internet-svcs` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 79. Service roles - Cloud Internet Services" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="internet-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table79}

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
{: caption="Table 79. Service actions - Cloud Internet Services" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="internet-svcs"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table79}

## Internet of Things Platform
{: #iotf-service-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `iotf-service` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 80. Platform roles - Internet of Things Platform" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="iotf-service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table80}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `iotf-service.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 80. Service actions - Internet of Things Platform" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="iotf-service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table80}

## Infrastructure Service
{: #is-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is` for the service name.

No supported roles.
## Regional Backup as a Service for VPC
{: #is.backup-policy-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.backup-policy` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can create, manage, retrieve and delete backup polices and plans, including assigning access policies to other users. |
| Editor | As an editor, you can create, manage, retrieve and delete backup polices and plans except for managing the account and assigning access policies. |
| Operator | As an operator, you can manage and operate backup polices and plans. |
| Viewer | As a viewer, you can retrieve backup polices and plans but you can't modify them. |
{: row-headers}
{: caption="Table 82. Platform roles - Regional Backup as a Service for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.backup-policy"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table82}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.backup-policy.dashboard.view` |  | Administrator, Editor, Operator |
| `is.backup-policy.backup-policy.create` | IAM action to create backup policy | Administrator, Editor |
| `is.backup-policy.backup-policy.read` | IAM action for reading a policy | Administrator, Editor, Operator, Viewer |
| `is.backup-policy.backup-policy.list` | IAM action for listing all backup policy in an account | Administrator, Editor, Operator, Viewer |
| `is.backup-policy.backup-policy.update` | IAM action for Updating Backup Policy | Administrator, Editor |
| `is.backup-policy.backup-policy.delete` | IAM action for deleting a backup policy | Administrator, Editor |
{: caption="Table 82. Service actions - Regional Backup as a Service for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.backup-policy"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table82}

## Bare Metal Server for VPC
{: #is.bare-metal-server-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.bare-metal-server` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all functions of an editor and can also assign access policies to other users. |
| Editor | As an editor, you can view, create, edit, delete, update, and perform operator actions on a bare metal server. |
| Operator | As an operator, you can view and perform actions (such as restart) on a bare metal server. |
| Viewer | As a viewer, you can view bare metal servers, but not modify them. |
{: row-headers}
{: caption="Table 83. Platform roles - Bare Metal Server for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.bare-metal-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table83}

| Role | Description |
| ----- | :----- |
| Bare Metal Advanced Network Operator | As an advanced network operator, you will be permitted access to modify IP Spoofing and Infrastructure NAT on bare metal interfaces |
| Bare Metal Console Admin | As a console admin, you will be able to access the bare metal server console. |
{: row-headers}
{: caption="Table 83. Service roles - Bare Metal Server for VPC" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="is.bare-metal-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table83}

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
{: caption="Table 83. Service actions - Bare Metal Server for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.bare-metal-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table83}

## Dedicated Host for VPC
{: #is.dedicated-host-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.dedicated-host` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 84. Platform roles - Dedicated Host for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.dedicated-host"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table84}

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
{: caption="Table 84. Service actions - Dedicated Host for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.dedicated-host"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table84}

## Virtual Private Endpoint for VPC
{: #is.endpoint-gateway-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.endpoint-gateway` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator you can create, delete, update and view endpoint gateway service instances, and assign access policies to other users. Administrators can also bind and unbind an endpoint gateway to a reserved IP address. |
| Editor | As an editor you can create, delete, update and view endpoint gateway service instance. Editors can also bind and unbind an endpoint gateway to a reserved IP address. |
| Operator | As an operator you can bind and unbind an endpoint gateway service instance to a reserved IP address. You can also view the properties of endpoint gateways but you cannot modify them. |
| Viewer | 	As a viewer you can view the properties of endpoint gateway service instances, but you cannot modify them. |
{: row-headers}
{: caption="Table 85. Platform roles - Virtual Private Endpoint for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.endpoint-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table85}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.endpoint-gateway.endpoint-gateway.read` | View Endpoint Gateway | Administrator, Editor, Operator, Viewer |
| `is.endpoint-gateway.endpoint-gateway.create` | Create Endpoint Gateway | Administrator, Editor |
| `is.endpoint-gateway.endpoint-gateway.delete` | Delete Endpoint Gateway | Administrator, Editor |
| `is.endpoint-gateway.endpoint-gateway.update` | Update Endpoint Gateway | Administrator, Editor |
| `is.endpoint-gateway.endpoint-gateway.list` | List Endpoint Gateways | Administrator, Editor, Operator, Viewer |
| `is.endpoint-gateway.endpoint-gateway.operate` | Operate Endpoint Gateway | Administrator, Editor, Operator |
{: caption="Table 85. Service actions - Virtual Private Endpoint for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.endpoint-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table85}

## Floating IP for VPC
{: #is.floating-ip-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.floating-ip` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 86. Platform roles - Floating IP for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.floating-ip"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table86}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.floating-ip.floating-ip.create` |  | Administrator, Editor |
| `is.floating-ip.floating-ip.delete` |  | Administrator, Editor |
| `is.floating-ip.floating-ip.update` |  | Administrator, Editor |
| `is.floating-ip.floating-ip.operate` |  | Administrator, Editor, Operator |
| `is.floating-ip.floating-ip.read` |  | Administrator, Editor, Operator, Viewer |
| `is.floating-ip.floating-ip.list` |  | Administrator, Editor, Operator, Viewer |
{: caption="Table 86. Service actions - Floating IP for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.floating-ip"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table86}

## IBM Cloud Flow Logs for VPC
{: #is.flow-log-collector-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.flow-log-collector` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 87. Platform roles - IBM Cloud Flow Logs for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.flow-log-collector"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table87}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.flow-log-collector.flow-log-collector.read` | As an administrator, an editor, an operator or a viewer, you can view the details of a flow log collector | Administrator, Editor, Operator, Viewer |
| `is.flow-log-collector.flow-log-collector.update` | As an administrator or an editor, you can update a flow log collector | Administrator, Editor |
| `is.flow-log-collector.flow-log-collector.operate` | As an administrator, an editor or an operator, you can operate on a flow log collector | Administrator, Editor, Operator |
| `is.flow-log-collector.flow-log-collector.create` | As an administrator or an editor, you can create a flow log collector | Administrator, Editor |
| `is.flow-log-collector.flow-log-collector.delete` | As an administrator or an editor, you can delete a flow log collector | Administrator, Editor |
| `is.flow-log-collector.flow-log-collector.list` | List Flow Log Collectors | Administrator, Editor, Operator, Viewer |
{: caption="Table 87. Service actions - IBM Cloud Flow Logs for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.flow-log-collector"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table87}

## Image Service for VPC
{: #is.image-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.image` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 88. Platform roles - Image Service for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.image"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table88}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 88. Service roles - Image Service for VPC" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="is.image"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table88}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.image.image.list` | List Images | Administrator, Editor, Operator, Viewer |
| `is.image.image.read` | Read Images | Administrator, Editor, Operator, Viewer |
| `is.image.image.create` | Create Images | Administrator, Editor |
| `is.image.image.update` | Update Images | Administrator, Editor |
| `is.image.image.delete` | Delete Images | Administrator, Editor |
| `is.image.image.provision` | Provision Images | Administrator, Editor, Operator |
| `is.image.image.operate` | Operate on Custom Images | Administrator, Editor, Operator |
| `is.image.image.export` | Export on Custom Images | Administrator, Editor |
| `is.image.image.obsolete` | Set an image status to obsolete | Administrator, Editor, Manager, Writer |
| `is.image.image.deprecate` | Set an image status to deprecated | Administrator, Editor, Manager, Writer |
{: caption="Table 88. Service actions - Image Service for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.image"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table88}

## Virtual Server for VPC
{: #is.instance-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.instance` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 89. Platform roles - Virtual Server for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.instance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table89}

| Role | Description |
| ----- | :----- |
| Console Administrator | As a console administrator, you can access the virtual server instance console., This role only provides console access and must be combined with another role that has operator access to the virtual server such as Operator, Editor or Administrator. |
| IP Spoofing Operator | As the IP spoofing operator, you can enable or disable the IP spoofing check on virtual server instances. This role should only be granted if necessary.  |
{: row-headers}
{: caption="Table 89. Service roles - Virtual Server for VPC" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="is.instance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table89}

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
{: caption="Table 89. Service actions - Virtual Server for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.instance"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table89}

## Auto Scale for VPC
{: #is.instance-group-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.instance-group` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 90. Platform roles - Auto Scale for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.instance-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table90}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.instance-group.instance-group.read` | Read an Instance Group | Administrator, Editor, Operator, Viewer |
| `is.instance-group.instance-group.create` | Create an Instance Group | Administrator, Editor |
| `is.instance-group.instance-group.update` | Update an Instance Group | Administrator, Editor |
| `is.instance-group.instance-group.delete` | Delete an Instance Group | Administrator, Editor |
| `is.instance-group.instance-group.list` | List Instance Groups | Administrator, Editor, Operator, Viewer |
{: caption="Table 90. Service actions - Auto Scale for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.instance-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table90}

## SSH Key for VPC
{: #is.key-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.key` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 91. Platform roles - SSH Key for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.key"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table91}

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
{: caption="Table 91. Service actions - SSH Key for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.key"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table91}

## Load Balancer for VPC
{: #is.load-balancer-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.load-balancer` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 92. Platform roles - Load Balancer for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.load-balancer"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table92}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.load-balancer.load-balancer.view` | View load balancers | Administrator, Editor, Operator, Viewer |
| `is.load-balancer.load-balancer.manage` |  | Administrator, Editor |
| `is.load-balancer.load-balancer.operate` | Operator permissions for load balancers | Administrator, Editor, Operator |
{: caption="Table 92. Service actions - Load Balancer for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.load-balancer"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table92}

## Network ACL
{: #is.network-acl-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.network-acl` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 93. Platform roles - Network ACL" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.network-acl"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table93}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.network-acl.network-acl.read` |  | Administrator, Editor, Operator, Viewer |
| `is.network-acl.network-acl.create` |  | Administrator, Editor |
| `is.network-acl.network-acl.update` |  | Administrator, Editor |
| `is.network-acl.network-acl.delete` |  | Administrator, Editor |
| `is.network-acl.network-acl.list` |  | Administrator, Editor, Operator, Viewer |
| `is.network-acl.network-acl.operate` |  | Administrator, Editor, Operator |
{: caption="Table 93. Service actions - Network ACL" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.network-acl"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table93}

## Placement Groups for VPC
{: #is.placement-group-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.placement-group` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 94. Platform roles - Placement Groups for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.placement-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table94}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.placement-group.dashboard.view` | View Dashboard | Administrator, Editor, Operator |
| `is.placement-group.placement-group.create` | Create a virtual instance placement group | Administrator, Editor |
| `is.placement-group.placement-group.update` | Update the name of a virtual instance placement group | Administrator, Editor |
| `is.placement-group.placement-group.delete` | Delete a virtual instance placement group | Administrator, Editor |
| `is.placement-group.placement-group.operate` | Add or remove an instance to or from a placement group | Administrator, Editor, Operator |
| `is.placement-group.placement-group.read` | View the details of a virtual instance placement group | Administrator, Editor, Operator, Viewer |
| `is.placement-group.placement-group.list` | List all placements groups associated for this account | Administrator, Editor, Operator, Viewer |
{: caption="Table 94. Service actions - Placement Groups for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.placement-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table94}

## Public Gateway
{: #is.public-gateway-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.public-gateway` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 95. Platform roles - Public Gateway" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.public-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table95}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.public-gateway.public-gateway.read` |  | Administrator, Editor, Operator, Viewer |
| `is.public-gateway.public-gateway.create` |  | Administrator, Editor |
| `is.public-gateway.public-gateway.update` |  | Administrator, Editor |
| `is.public-gateway.public-gateway.delete` |  | Administrator, Editor |
| `is.public-gateway.public-gateway.list` |  | Administrator, Editor, Operator, Viewer |
| `is.public-gateway.public-gateway.operate` |  | Administrator, Editor, Operator |
{: caption="Table 95. Service actions - Public Gateway" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.public-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table95}

## Security Group for VPC
{: #is.security-group-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.security-group` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 96. Platform roles - Security Group for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.security-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table96}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.security-group.security-group.create` |  | Administrator, Editor |
| `is.security-group.security-group.read` |  | Administrator, Editor, Operator, Viewer |
| `is.security-group.security-group.update` |  | Administrator, Editor |
| `is.security-group.security-group.delete` |  | Administrator, Editor |
| `is.security-group.security-group.operate` |  | Administrator, Editor, Operator |
{: caption="Table 96. Service actions - Security Group for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.security-group"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table96}

## Block Storage Snapshots for VPC
{: #is.snapshot-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.snapshot` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can create, view, list, modify, delete and restore block storage snapshots, including assigning access policies to other users. |
| Editor | As an editor, you can create, view, list, modify, delete and restore block storage snapshots, except for assigning access policies to other users. |
| Operator | As an operator, you can view, list and restore block storage snapshots, but you can't modify them. |
| Viewer | As a viewer, you can view and list block storage snapshots, but you can't modify them. |
{: row-headers}
{: caption="Table 97. Platform roles - Block Storage Snapshots for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.snapshot"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table97}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.snapshot.snapshot.create` | This action allows the user to create block storage snapshots. | Administrator, Editor |
| `is.snapshot.snapshot.read` | This action allows the user to view block storage snapshots , but not modify them. | Administrator, Editor, Operator, Viewer |
| `is.snapshot.snapshot.list` | This action allows the user to list snapshot resources. | Administrator, Editor, Operator, Viewer |
| `is.snapshot.snapshot.update` | This action allows the user to modify block storage snapshots. | Administrator, Editor |
| `is.snapshot.snapshot.delete` | This action allows the user to delete block storage snapshots. | Administrator, Editor |
| `is.snapshot.snapshot.restore` | This action allows the user to restore block storage snapshots. | Administrator, Editor, Operator |
| `is.snapshot.snapshot.operate` | Operate a snapshot | Administrator, Editor, Operator |
| `is.snapshot.snapshot-clone.create` | Create clones of block storage snapshots for fast restoration | Administrator, Editor |
| `is.snapshot.clone.read` | View the clones of block storage snapshots | Administrator, Editor, Operator, Viewer |
| `is.snapshot.snapshot-clone.delete` | Delete clones of block storage snapshots | Administrator, Editor |
{: caption="Table 97. Service actions - Block Storage Snapshots for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.snapshot"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table97}

## Subnet
{: #is.subnet-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.subnet` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 98. Platform roles - Subnet" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.subnet"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table98}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.subnet.subnet.create` |  | Administrator, Editor |
| `is.subnet.subnet.read` |  | Administrator, Editor, Operator, Viewer |
| `is.subnet.subnet.update` |  | Administrator, Editor |
| `is.subnet.subnet.delete` |  | Administrator, Editor |
| `is.subnet.subnet.list` |  | Administrator, Editor, Operator, Viewer |
| `is.subnet.subnet.operate` |  | Administrator, Editor, Operator |
{: caption="Table 98. Service actions - Subnet" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.subnet"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table98}

## Virtual Network Interface
{: #is.virtual-network-interface-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.virtual-network-interface` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As a Virtual Network Interface administrator, you can Read, List, Attach, Detach, Create, Update, and Delete Virtual Network resources on the account and provide policies to other users on the account. |
| Editor | As a Virtual Network Interface editor, you can Read, List, Attach, Detach, Create, Update, and Delete Virtual Network resources. |
| Operator | As a Virtual Network Interface operator, you can Read, List, Attach, and Detach Virtual Network resources. |
| Viewer | As a Virtual Network Interface viewer, you can Read, and List Virtual Network resources. |
{: row-headers}
{: caption="Table 99. Platform roles - Virtual Network Interface" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.virtual-network-interface"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table99}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.virtual-network-interface.virtual-network-interface.read` | Read Virtual Network Interface | Administrator, Editor, Operator, Viewer |
| `is.virtual-network-interface.virtual-network-interface.list` | List Virtual Network Interfaces | Administrator, Editor, Operator, Viewer |
| `is.virtual-network-interface.virtual-network-interface.update` | Update Virtual Network Interface | Administrator, Editor |
| `is.virtual-network-interface.virtual-network-interface.operate` | Operate Virtual Network Interfaces | Administrator, Editor, Operator |
| `is.virtual-network-interface.virtual-network-interface.create` | Create Virtual Network Interface | Administrator, Editor |
| `is.virtual-network-interface.virtual-network-interface.delete` | Delete Virtual Network Interface | Administrator, Editor |
{: caption="Table 99. Service actions - Virtual Network Interface" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.virtual-network-interface"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table99}

## Block Storage for VPC
{: #is.volume-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.volume` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 100. Platform roles - Block Storage for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.volume"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table100}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.volume.profile.view` |  | Administrator, Editor, Operator, Viewer |
| `is.volume.volume.create` |  | Administrator, Editor |
| `is.volume.volume.list` |  | Administrator, Editor, Operator, Viewer |
| `is.volume.volume.read` |  | Administrator, Editor, Operator, Viewer |
| `is.volume.volume.update` |  | Administrator, Editor |
| `is.volume.volume.delete` |  | Administrator, Editor |
| `is.volume.volume.operate` | Operate a volume | Administrator, Editor, Operator |
{: caption="Table 100. Service actions - Block Storage for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.volume"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table100}

## Virtual Private Cloud
{: #is.vpc-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.vpc` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 101. Platform roles - Virtual Private Cloud" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.vpc"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table101}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.vpc.vpc.read` | View a Virtual Private Cloud (VPC) | Administrator, Editor, Operator, Viewer |
| `is.vpc.vpc.create` | Create a Virtual Private Cloud (VPC) | Administrator, Editor |
| `is.vpc.vpc.delete` | Delete a Virtual Private Cloud (VPC) | Administrator, Editor |
| `is.vpc.vpc.update` | Update a Virtual Private Cloud (VPC) | Administrator, Editor |
| `is.vpc.vpc.list` | List Virtual Private Clouds (VPC) | Administrator, Editor, Operator, Viewer |
| `is.vpc.vpc.operate` | Operate a Virtual Private Clouds (VPC) | Administrator, Editor, Operator |
| `is.vpc.routing-table.list` | List Routing Tables | Administrator, Editor, Operator, Viewer |
| `is.vpc.routing-table.read` | Read Routes/Details of Routing Table | Administrator, Editor, Operator, Viewer |
| `is.vpc.routing-table.create` | Create a Route Table | Administrator, Editor |
| `is.vpc.routing-table.update` | Update Routing Table and Routes | Administrator, Editor |
| `is.vpc.routing-table.delete` | Delete Route Table | Administrator, Editor |
| `is.vpc.routing-table.operate` | Configure Subnet Attachment to Route Table | Administrator, Editor, Operator |
{: caption="Table 101. Service actions - Virtual Private Cloud" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.vpc"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table101}

## VPN for VPC
{: #is.vpn-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.vpn` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 102. Platform roles - VPN for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.vpn"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table102}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `is.vpn.vpn.create` |  | Administrator, Editor |
| `is.vpn.vpn.update` |  | Administrator, Editor |
| `is.vpn.vpn.delete` |  | Administrator, Editor |
| `is.vpn.vpn.read` |  | Administrator, Editor, Operator, Viewer |
| `is.vpn.vpn.list` |  | Administrator, Editor, Operator, Viewer |
| `is.vpn.dashboard.view` |  | Administrator, Editor, Operator, Viewer |
{: caption="Table 102. Service actions - VPN for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.vpn"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table102}

## VPN Server for VPC
{: #is.vpn-server-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `is.vpn-server` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 103. Platform roles - VPN Server for VPC" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="is.vpn-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table103}

| Role | Description |
| ----- | :----- |
| VPN Client | Users of the VPN server need this role to connect to the VPN server |
{: row-headers}
{: caption="Table 103. Service roles - VPN Server for VPC" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="is.vpn-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table103}

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
{: caption="Table 103. Service actions - VPN Server for VPC" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="is.vpn-server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table103}

## IBM Key Protect
{: #kms-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `kms` for the service name.

| Role | Description |
| ----- | :----- |
| KeyPurge | Role for purging key. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| ReaderPlus | As a reader plus, you can perform read-only actions within Key Protect such as viewing service-specific resources. You can also access key material for standard keys. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 104. Service roles - IBM Key Protect" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="kms"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table104}

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
| `kms.secrets-with-policy-overrides.create` | Create an encryption key with policy overrides. | Manager |
{: caption="Table 104. Service actions - IBM Key Protect" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="kms"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table104}

## Knowledge Studio
{: #knowledge-studio-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `knowledge-studio` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 105. Platform roles - Knowledge Studio" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="knowledge-studio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table105}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 105. Service roles - Knowledge Studio" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="knowledge-studio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table105}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `knowledge-studio.dashboard.view` |  | Administrator, Editor, Manager, Reader, Viewer, Writer |
{: caption="Table 105. Service actions - Knowledge Studio" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="knowledge-studio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table105}

## Language Translator
{: #language-translator-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `language-translator` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 106. Service roles - Language Translator" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="language-translator"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table106}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `GET /language-translator` |  | Manager, Reader, Writer |
| `POST /language-translator` |  | Manager, Reader, Writer |
| `DELETE /language-translator` |  | Manager, Writer |
{: caption="Table 106. Service actions - Language Translator" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="language-translator"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table106}

## IBM Log Analysis with LogDNA
{: #logdna-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `logdna` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 107. Platform roles - IBM Log Analysis with LogDNA" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="logdna"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table107}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you can manage resources, configure views, dashboards and alerts, export data, search, filter, and view all data. |
| Reader | As a reader, you can perform read-only actions such as monitor data through views and dashboards. |
| Standard Member | As a member, you can configure views, dashboards and alerts, export data, search, filter, and view all data. |
{: row-headers}
{: caption="Table 107. Service roles - IBM Log Analysis with LogDNA" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="logdna"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table107}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `logdna.dashboard.view` | View LogDNA Dashboard | Administrator, Manager, Reader, Standard Member |
| `logdna.dashboard.read` | Access LogDNA dashboard without any edit permission | Reader |
| `logdna.dashboard.member` | Access LogDNA dashboard with limited edit capabilities | Standard Member |
| `logdna.dashboard.manage` | Access and manage LogDNA dashboard without any limitation | Administrator, Manager |
{: caption="Table 107. Service actions - IBM Log Analysis with LogDNA" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="logdna"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table107}

## IBM Cloud Activity Tracker with LogDNA
{: #logdnaat-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `logdnaat` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 108. Platform roles - IBM Cloud Activity Tracker with LogDNA" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="logdnaat"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table108}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you can manage resources, configure views, dashboards and alerts, export data, search, filter, and view all data. |
| Reader | As a reader, you can perform read-only actions such as monitor data through views and dashboards. |
| Standard member | As a member, you can configure views, dashboards and alerts, export data, search, filter, and view all data. |
{: row-headers}
{: caption="Table 108. Service roles - IBM Cloud Activity Tracker with LogDNA" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="logdnaat"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table108}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `logdnaat.dashboard.view` | View LogDNA Dashboard | Administrator, Manager, Reader, Standard member |
| `logdnaat.dashboard.read` | Access LogDNA dashboard without any edit permission | Reader |
| `logdnaat.dashboard.member` | Access LogDNA dashboard with limited edit capabilities | Standard member |
| `logdnaat.dashboard.manage` | Access and manage LogDNA dashboard without any limitation | Administrator, Manager |
{: caption="Table 108. Service actions - IBM Cloud Activity Tracker with LogDNA" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="logdnaat"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table108}

## Managed Solutions
{: #managed-solutions-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `managed-solutions` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 109. Platform roles - Managed Solutions" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="managed-solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table109}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 109. Service roles - Managed Solutions" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="managed-solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table109}

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
{: caption="Table 109. Service actions - Managed Solutions" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="managed-solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table109}

## Master Data Connect
{: #mdm-oc-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `mdm-oc` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 110. Platform roles - Master Data Connect" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="mdm-oc"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table110}

| Role | Description |
| ----- | :----- |
| Configurator Manager | As a Configurator Manager, you can perform manage actions in the Configurator microservice. |
| Configurator Reader | As a Configurator Reader, you can perform read actions in the Configurator microservice. |
| Data Engineer | As a Data Engineer you have full access to all microservices. |
| Data Manager | As a Data Manager, you can perform read, write and manage actions in the Data microservice. |
| Data Reader | As a Data Reader, you can perform read only actions in the Data microservice. |
| Data Steward | As a Data Steward, you can add or delete rules from the matching microservice. |
| Data Writer | As a Data Writer, you can perform read and write actions in the Data microservice. |
| Entity Viewer | As a Entity Viewer you can perform read actions in both the model and data microservice. |
| Job Reader | As a Job Reader, you can perform read actions in the Job microservice. |
| Job Writer | As a Job Writer, you can perform read and write actions in the Job microservice. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Matching Manager | As a Matching Manager, you can perform read, write and manage actions in the Matching microservice. |
| Matching Reader | As a Matching Reader, you can perform read actions in the Matching microservice. |
| Matching Writer | As a Matching Writer, you can perform read and write actions in the Matching microservice. |
| Model Manager | As a Model Manager, you can perform manage actions in the Model microservice. |
| Model Reader | As a Model Reader, you can perform read actions in the Model microservice. |
| Model Writer | As a Model Writer you can perform write actions in the Model microservice. |
| Pair Analysis Reader | As a Pair Analysis Reader, you can perform read actions in the Pair Analysis microservice. |
| Pair Analysis Writer | As a Pair Analysis Writer, you can perform read and write actions in the Pair Analysis microservice. |
| Publisher User | As a Publisher User you can perform manage actions in the data and model service. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 110. Service roles - Master Data Connect" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="mdm-oc"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table110}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `mdm-oc.dashboard.view` | View Dashboard | Administrator, Configurator Manager, Configurator Reader, Data Engineer, Data Manager, Data Reader, Data Steward, Data Writer, Editor, Entity Viewer, Job Reader, Job Writer, Manager, Matching Manager, Matching Reader, Matching Writer, Model Manager, Model Reader, Model Writer, Operator, Pair Analysis Reader, Pair Analysis Writer, Publisher User, Reader, Viewer, Writer |
| `mdm-oc.data.read` | Read access to the Master Data Management Data microservice. | Administrator, Data Engineer, Data Manager, Data Reader, Data Steward, Data Writer, Editor, Entity Viewer, Manager, Operator, Publisher User, Reader, Viewer, Writer |
| `mdm-oc.data.write` | Write access to the Master Data Management Data microservice. | Administrator, Data Engineer, Data Manager, Data Steward, Data Writer, Manager, Publisher User, Writer |
| `mdm-oc.data.manage` | Manage access to the Master Data Management Data microservice. | Administrator, Data Engineer, Data Manager, Manager, Publisher User |
| `mdm-oc.matching.read` | Read access to the Master Data Management Matching microservice. | Administrator, Data Engineer, Data Steward, Editor, Entity Viewer, Manager, Matching Manager, Matching Reader, Matching Writer, Operator, Reader, Viewer, Writer |
| `mdm-oc.matching.write` | Write access to the Master Data Management Matching microservice. | Administrator, Data Engineer, Data Steward, Manager, Matching Manager, Matching Writer, Writer |
| `mdm-oc.matching.manage` | Manage access to the Master Data Management Matching microservice. | Administrator, Data Engineer, Manager, Matching Manager |
| `mdm-oc.model.read` | Read access to the Master Data Management Model microservice. | Administrator, Data Engineer, Data Steward, Editor, Entity Viewer, Manager, Model Manager, Model Reader, Model Writer, Operator, Publisher User, Reader, Viewer, Writer |
| `mdm-oc.model.write` | Write access to the Master Data Management Model microservice. | Administrator, Data Engineer, Manager, Model Manager, Model Writer, Publisher User, Writer |
| `mdm-oc.configurator.read` | Read access to the Master Data Management Configurator microservice. | Administrator, Configurator Manager, Configurator Reader, Data Engineer, Editor, Manager, Operator, Viewer, Writer |
| `mdm-oc.configurator.manage` | Manage access to the Master Data Management Configurator microservice. | Administrator, Configurator Manager, Data Engineer, Manager |
| `mdm-oc.pairs-analysis.read` | Read access to the Master Data Management Pair Analysis microservice. | Administrator, Data Engineer, Data Steward, Editor, Manager, Operator, Pair Analysis Reader, Pair Analysis Writer, Reader, Viewer, Writer |
| `mdm-oc.pairs-analysis.write` | Write access to the Master Data Management Pair Analysis microservice. | Administrator, Data Engineer, Data Steward, Manager, Pair Analysis Writer, Writer |
| `mdm-oc.job.write` | Write access to the Master Data Management Job microservice. | Administrator, Data Engineer, Job Writer, Manager, Publisher User, Writer |
| `mdm-oc.job.read` | Read access to the Master Data Management Job microservice. | Administrator, Data Engineer, Data Steward, Editor, Entity Viewer, Job Reader, Job Writer, Manager, Operator, Publisher User, Reader, Viewer, Writer |
| `mdm-oc.model.manage` | Manage access to the Master Data Management Model microservice. | Administrator, Data Engineer, Manager, Model Manager, Publisher User |
| `mdm-oc.matching.datasteward` | Data Steward access to the Master Data Management. | Administrator, Data Engineer, Data Steward, Manager |
{: caption="Table 110. Service actions - Master Data Connect" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="mdm-oc"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table110}

## Event Streams
{: #messagehub-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `messagehub` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 111. Service roles - Event Streams" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="messagehub"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table111}

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
{: caption="Table 111. Service actions - Event Streams" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="messagehub"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table111}

## Messages for RabbitMQ
{: #messages-for-rabbitmq-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `messages-for-rabbitmq` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions (including making configuration changes and managing credentials) except for managing the account and assigning access policies. |
| Operator | As an operator, you can view database instances and make configuration changes including managing database credentials. |
| Viewer | As a viewer, you can view database instances but you can't make configuration changes. |
{: row-headers}
{: caption="Table 112. Platform roles - Messages for RabbitMQ" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="messages-for-rabbitmq"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table112}

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
{: caption="Table 112. Service actions - Messages for RabbitMQ" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="messages-for-rabbitmq"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table112}

## Metrics Router
{: #metrics-router-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `metrics-router` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 113. Platform roles - Metrics Router" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="metrics-router"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table113}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `metrics-router.target.read` | Read target | Administrator, Editor, Operator, Viewer |
| `metrics-router.target.create` | Create target | Administrator, Editor |
| `metrics-router.target.update` | Update target | Administrator, Editor |
| `metrics-router.target.delete` | Delete target | Administrator, Editor |
| `metrics-router.target.list` | List the targets | Administrator, Editor, Operator, Viewer |
| `metrics-router.route.read` | Read route | Administrator, Editor, Operator, Viewer |
| `metrics-router.route.create` | Create route | Administrator, Editor |
| `metrics-router.route.update` | Update route | Administrator, Editor |
| `metrics-router.route.delete` | Delete route | Administrator, Editor |
| `metrics-router.route.list` | List routes | Administrator, Editor, Operator, Viewer |
| `metrics-router.onboarding.modify` | Modify onboarding for services only. | Administrator |
| `metrics-router.onboarding.get` | Get onboarding for services only. | Administrator, Editor, Operator, Viewer |
| `metrics-router.onboarding.delete` | Delete onboarding for services only. | Administrator |
| `metrics-router.setting.update` | Update Metrics Router setting | Administrator |
| `metrics-router.setting.get` | Get Metrics Router setting | Administrator, Editor, Operator, Viewer |
{: caption="Table 113. Service actions - Metrics Router" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="metrics-router"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table113}

## Migration Services for IBM Cloud
{: #migrationtool-from-wanclds-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `migrationtool-from-wanclds` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 114. Platform roles - Migration Services for IBM Cloud" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="migrationtool-from-wanclds"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table114}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `migrationtool-from-wanclds.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 114. Service actions - Migration Services for IBM Cloud" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="migrationtool-from-wanclds"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table114}

## Minio
{: #minio-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `minio` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 115. Platform roles - Minio" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="minio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table115}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `minio.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 115. Service actions - Minio" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="minio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table115}

## IBM Cloud Monitoring Service
{: #monitoring-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `monitoring` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 116. Platform roles - IBM Cloud Monitoring Service" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="monitoring"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table116}

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
{: caption="Table 116. Service actions - IBM Cloud Monitoring Service" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="monitoring"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table116}

## IBM MQ
{: #mqcloud-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `mqcloud` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 117. Platform roles - IBM MQ" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="mqcloud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table117}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 117. Service roles - IBM MQ" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="mqcloud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table117}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `mqcloud.instance.use` | Accessing an MQ on Cloud service instance | Administrator, Editor, Manager, Viewer, Writer |
{: caption="Table 117. Service actions - IBM MQ" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="mqcloud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table117}

## Natural Language Understanding
{: #natural-language-understanding-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `natural-language-understanding` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 118. Platform roles - Natural Language Understanding" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="natural-language-understanding"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table118}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 118. Service roles - Natural Language Understanding" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="natural-language-understanding"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table118}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `natural-language-understanding.dashboard.view` |  | Administrator, Editor, Operator |
| `GET /natural-language-understanding` |  | Manager, Reader, Writer |
| `POST /natural-language-understanding` |  | Manager, Reader, Writer |
| `DELETE /natural-language-understanding` |  | Manager, Reader, Writer |
| `PUT /natural-language-understanding` | PUT /natural-language-understanding | Manager, Reader, Writer |
{: caption="Table 118. Service actions - Natural Language Understanding" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="natural-language-understanding"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table118}

## NeuralSeek
{: #neuralseek-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `neuralseek` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 119. Platform roles - NeuralSeek" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="neuralseek"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table119}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `neuralseek.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 119. Service actions - NeuralSeek" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="neuralseek"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table119}

## Partner Center
{: #partner-portal-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `partner-portal` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 120. Platform roles - Partner Center" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="partner-portal"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table120}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `partner-portal.dashboard.view` | View Dashboard | Administrator, Editor, Viewer |
| `partner-portal.dashboard.edit` | Enabled for testing only | Administrator, Editor |
{: caption="Table 120. Service actions - Partner Center" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="partner-portal"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table120}

## Personality Insights
{: #personality-insights-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `personality-insights` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
| Editor | null |
| Operator | null |
{: row-headers}
{: caption="Table 121. Platform roles - Personality Insights" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="personality-insights"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table121}

| Role | Description |
| ----- | :----- |
| Manager | null |
| Reader | null |
| Writer | null |
{: row-headers}
{: caption="Table 121. Service roles - Personality Insights" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="personality-insights"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table121}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `personality-insights.dashboard.view` |  | Administrator, Editor, Operator |
| `GET /personality-insights` |  | Manager, Reader, Writer |
| `POST /personality-insights` |  | Manager, Reader, Writer |
{: caption="Table 121. Service actions - Personality Insights" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="personality-insights"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table121}

## Planning Analytics
{: #planning-analytics-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `planning-analytics` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 122. Platform roles - Planning Analytics" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="planning-analytics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table122}

| Role | Description |
| ----- | :----- |
| Planning Analytics User | Planning Analytics User |
{: row-headers}
{: caption="Table 122. Service roles - Planning Analytics" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="planning-analytics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table122}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `planning-analytics.dashboard.view` | View Dashboard | Administrator, Editor, Operator, Viewer |
| `planning-analytics.access` | Planning Analytics Access | Administrator, Planning Analytics User |
{: caption="Table 122. Service actions - Planning Analytics" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="planning-analytics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table122}

## Watson Machine Learning
{: #pm-20-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `pm-20` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 123. Platform roles - Watson Machine Learning" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="pm-20"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table123}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you can perform all actions on the WML instance this role is being assigned. |
{: row-headers}
{: caption="Table 123. Service roles - Watson Machine Learning" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="pm-20"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table123}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `pm-20.instances.admin` |  | Administrator |
| `pm-20.instances.write` |  | Editor, Manager, Writer |
{: caption="Table 123. Service actions - Watson Machine Learning" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="pm-20"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table123}

## Portworx Enterprise
{: #portworx-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `portworx` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 124. Platform roles - Portworx Enterprise" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="portworx"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table124}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `portworx.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 124. Service actions - Portworx Enterprise" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="portworx"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table124}

## Portworx Test
{: #portworx-test-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `portworx-test` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 125. Platform roles - Portworx Test" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="portworx-test"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table125}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `portworx-test.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 125. Service actions - Portworx Test" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="portworx-test"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table125}

## PowerAI
{: #power-ai-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `power-ai` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | null |
| Editor | null |
| Operator | null |
{: row-headers}
{: caption="Table 126. Platform roles - PowerAI" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="power-ai"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table126}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `power-ai.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 126. Service actions - PowerAI" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="power-ai"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table126}

## Power Systems Virtual Server
{: #power-iaas-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `power-iaas` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 127. Service roles - Power Systems Virtual Server" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="power-iaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table127}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `power-iaas.dashboard.view` |  | Manager, Reader |
| `power-iaas.cloud-instance.modify` |  | Manager |
| `power-iaas.cloud-instance.read` |  | Manager, Reader |
{: caption="Table 127. Service actions - Power Systems Virtual Server" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="power-iaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table127}

## HDM Workload Migrator
{: #primaryio-hdm-workload-migrator-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `primaryio-hdm-workload-migrator` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 128. Platform roles - HDM Workload Migrator" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="primaryio-hdm-workload-migrator"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table128}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `primaryio-hdm-workload-migrator.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 128. Service actions - HDM Workload Migrator" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="primaryio-hdm-workload-migrator"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table128}

## Privileged Access Gateway
{: #privileged-access-gateway-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `privileged-access-gateway` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 129. Platform roles - Privileged Access Gateway" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="privileged-access-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table129}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 129. Service roles - Privileged Access Gateway" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="privileged-access-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table129}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `privileged-access-gateway.dashboard.view` |  | Administrator, Editor, Operator |
| `privileged-access-gateway.certificate.create` | this action is going to create a user certificate for the user that is needed to login to the session | Manager, Writer |
| `privileged-access-gateway.public.ca.key` | retrieves the public CA key  | Manager, Reader, Writer |
| `privileged-access-gateway.ssh.login` | ssh login | Manager, Writer |
| `privileged-access-gateway.kube.login` | kube login action that allows users to get kube config details of a cluster  | Manager, Writer |
| `privileged-access-gateway.rdp.login` | privileged-access-gateway.ssh.login | Manager, Writer |
| `privileged-access-gateway.session.list.all` | List All  Active Sessions | Manager |
| `privileged-access-gateway.instance.upgrade` | Perform a software update of the gateway associated an instance. | Administrator, Editor, Operator |
{: caption="Table 129. Service actions - Privileged Access Gateway" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="privileged-access-gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table129}

## Product Lifecycle
{: #product-lifecycle-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `product-lifecycle` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 130. Platform roles - Product Lifecycle" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="product-lifecycle"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table130}

| Role | Description |
| ----- | :----- |
| Lifecycle Approver | Approvers can approve or reject workflow tasks |
{: row-headers}
{: caption="Table 130. Service roles - Product Lifecycle" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="product-lifecycle"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table130}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `product-lifecycle.dashboard.view` |  | Administrator, Editor, Operator |
| `product-lifecycle.offering.create` | Create an onboarding offering in the account | Administrator, Editor |
| `product-lifecycle.offering.edit` | Edit an onboarding offering in the account. | Administrator, Editor |
| `product-lifecycle.review.complete` | Complete (accept or reject) a review | Lifecycle Approver |
| `product-lifecycle.offering.read` | Read values of an offering | Administrator, Editor, Lifecycle Approver |
| `product-lifecycle.registration.read` | Read onboarding registration | Administrator, Editor, Lifecycle Approver |
| `product-lifecycle.registration.create` | Create onboarding registration | Administrator, Editor |
{: caption="Table 130. Service actions - Product Lifecycle" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="product-lifecycle"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table130}

## Project
{: #project-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `project` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 131. Platform roles - Project" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="project"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table131}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `project.notifications.write` | The ability to send project notifications. | Administrator |
| `project.notifications.read` | The ability to read project notifications. | Administrator, Editor, Operator, Viewer |
| `project.notifications.delete` | The ability to delete project notifications. | Administrator |
| `project.config.delete` | The ability to delete a project config. | Administrator |
| `project.config.approve` | The ability to approve a project config. | Administrator, Editor |
| `project.config.create` | The ability to create a project config. | Administrator, Editor |
| `project.config.deploy` | The ability to deploy a project config. | Administrator, Editor |
| `project.config.destroy-resources` | The ability to destroy project config resources. | Administrator, Editor |
| `project.config.edit` | The ability to edit a project config. | Administrator, Editor, Operator |
| `project.config.force-approve` | The ability to force approve a project config. | Administrator |
| `project.config.retrieve` | The ability to view a project config. | Administrator, Editor, Operator, Viewer |
| `project.config.validate` | The ability to validate a project config. | Administrator, Editor, Operator |
{: caption="Table 131. Service actions - Project" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="project"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table131}

## PX-Backup By Portworx
{: #px-backup-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `px-backup` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 132. Platform roles - PX-Backup By Portworx" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="px-backup"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table132}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `px-backup.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 132. Service actions - PX-Backup By Portworx" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="px-backup"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table132}

## Quantum Services
{: #quantum-computing-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `quantum-computing` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 133. Service roles - Quantum Services" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="quantum-computing"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table133}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `quantum-computing.program.read` | Read a program definition | Manager, Reader |
| `quantum-computing.program.delete` | Delete a program | Manager, Writer |
| `quantum-computing.job.create` | Create a job to run a program | Manager, Writer |
| `quantum-computing.job.read` | User ability to read a job | Manager, Reader |
| `quantum-computing.job.delete` | Delete a Job | Manager, Writer |
| `quantum-computing.job.cancel` | Cancel a Job | Manager, Writer |
| `quantum-computing.device.read` | Read information about a quantum device | Manager, Reader |
| `quantum-computing.user.logout` | Clears authorization cache | Manager, Reader, Writer |
| `quantum-computing.job.update` | Update a job. | Manager, Writer |
| `quantum-computing.instance.configuration.read` | Instance configuration read | Manager |
| `quantum-computing.instance.configuration.update` | Instance configuration update | Manager |
| `quantum-computing.instance.usage.read` | Instance usage read | Manager, Reader, Writer |
{: caption="Table 133. Service actions - Quantum Services" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="quantum-computing"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table133}

## Raxak Protect
{: #raxak-protect-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `raxak-protect` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 134. Platform roles - Raxak Protect" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="raxak-protect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table134}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `raxak-protect.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 134. Service actions - Raxak Protect" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="raxak-protect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table134}

## Robin CNS
{: #robin-storage-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `robin-storage` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 135. Platform roles - Robin CNS" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="robin-storage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table135}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `robin-storage.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 135. Service actions - Robin CNS" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="robin-storage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table135}

## IBM Cloud Satellite
{: #satellite-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `satellite` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 136. Platform roles - IBM Cloud Satellite" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="satellite"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table136}

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
{: caption="Table 136. Service roles - IBM Cloud Satellite" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="satellite"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table136}

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
| `satellite.config-cluster.attach` | attach cluster to a cluster group | Administrator, Manager, Satellite Cluster Creator |
| `satellite.config-cluster.read` | read cluster list for for an org or details about a given cluster | Administrator, Manager, Reader |
| `satellite.link.create` | Create Link instance for the Satellite Location.  | Administrator |
| `satellite.config-organization.read` | allow to access the organization info | Administrator, Deployer, Manager, Reader, Satellite Cluster Creator |
| `satellite.config-organization.manage` | allow to read the org_key for an organization | Manager |
| `satellite.resource.get` | read resource under a cluster or from a cluster group | Administrator, Manager, Reader |
| `satellite.api.globalaccess` | global access satellite api for special users | Administrator, Manager |
| `satellite.config-cluster.register` | register cluster to the satellite config | Administrator, Manager, Satellite Cluster Creator |
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
{: caption="Table 136. Service actions - IBM Cloud Satellite" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="satellite"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table136}

## Satellite Infrastructure Services 
{: #satellite-iaas-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `satellite-iaas` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 137. Platform roles - Satellite Infrastructure Services " caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="satellite-iaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table137}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Satellite IS Request Handler | Satellite IS Request Handler |
{: row-headers}
{: caption="Table 137. Service roles - Satellite Infrastructure Services " caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="satellite-iaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table137}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `satellite-iaas.dashboard.view` |  | Administrator, Editor, Operator |
| `satellite-iaas.request.create` | Create a location request | Administrator, Manager, Satellite IS Request Handler |
| `satellite-iaas.request.update` | Update Satellite request | Satellite IS Request Handler |
| `satellite-iaas.request.delete` | Delete Location Request | Satellite IS Request Handler |
{: caption="Table 137. Service actions - Satellite Infrastructure Services " caption-side="top"}
{: tab-title="Actions"}
{: tab-group="satellite-iaas"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table137}

## Schematics
{: #schematics-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `schematics` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 138. Platform roles - Schematics" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="schematics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table138}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 138. Service roles - Schematics" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="schematics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table138}

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
| `schematics.settings-agent.delete` | Unregister the Schematics Agent configuration setting | Manager |
| `schematics.settings-agent.update` | Update the Schematics Agent configuration setting | Manager, Writer |
| `schematics.settings-agent.read` | Read Schematics Agent configuration setting | Manager, Reader, Writer |
| `schematics.settings-agent.register` | Register the schematics agent instance | Manager |
| `schematics.settings-agent.create` | Create the schematics agent instance | Manager |
{: caption="Table 138. Service actions - Schematics" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="schematics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table138}

## Secrets Manager
{: #secrets-manager-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `secrets-manager` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 139. Platform roles - Secrets Manager" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="secrets-manager"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table139}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions, such as managing secret groups, configuring secret engines, and managing secrets policies. |
| Reader | As a reader, you can perform read-only actions within Secrets Manager, such as viewing service-specific resources. Readers can access only the metadata that is associated with a secret. |
| SecretsReader | As a secrets reader, you can perform read-only actions, and you can also access the secret data that is associated with a secret. A secrets reader can't create secrets or modify the value of an existing secret. |
| Writer | As a writer, you have permissions beyond the secrets reader role, including the ability to create and edit secrets. Writers can't create secret groups, manage the rotation policies of a secret, or configure secrets engines. |
{: row-headers}
{: caption="Table 139. Service roles - Secrets Manager" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="secrets-manager"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table139}

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
| `secrets-manager.secret-versions.list` | List secret versions. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.endpoints.view` | Get service instance endpoints. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.vault-token.create` | Create a Vault token. | Manager |
| `secrets-manager.notifications-registration.create` | Register a Secrets Manager instance as a source in Event Notifications. | Manager |
| `secrets-manager.notifications-registration.read` | Get the registration details between a Secrets Manager and Event Notifications instance. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.notifications-registration.delete` | Unregister or remove a Secrets Manager instance as a source in Event Notifications. | Manager |
| `secrets-manager.notifications-registration.test` | Send a test event to the registered Event Notifications service instance. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.secret.revoke` | Revoke a secret | Manager |
| `secrets-manager.secret-lock.create` | Create a lock on a secret version to prevent it from being updated or deleted. | Manager, Writer |
| `secrets-manager.secret-lock.delete` | Delete a secret lock. | Manager |
| `secrets-manager.secret-locks.list` | List the locks that exist for secret and its versions. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.locks.list` | List the locks that are exist in your service instance. | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.secret-action.create` | Create a secret action | Manager, Writer |
| `secrets-manager.secret-version.create` | Create a new secret version.	 | Manager, Writer |
| `secrets-manager.secret-version.read` | View the details of a secret version.	 | Manager, SecretsReader, Writer |
| `secrets-manager.secret-version-metadata.read` | View the metadata of a secret version.	 | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.secret-version-action.create` | Create a secret version action.	 | Manager, Writer |
| `secrets-manager.configuration.create` | Create a new configuration	 | Manager |
| `secrets-manager.configuration-action.create` | Create a new configuration action	 | Manager |
| `secrets-manager.configurations.list` | List configurations	 | Manager, Reader, Writer |
| `secrets-manager.configuration.read` | View the details of a configuration.	 | Manager |
| `secrets-manager.configuration.update` | Update a configuration | Manager |
| `secrets-manager.configuration.delete` | Delete a configuration | Manager |
| `secrets-manager.secret-locks.create` | Create secret locks. | Manager, Writer |
| `secrets-manager.secret-locks.delete` | Delete secret locks. | Manager |
| `secrets-manager.secret-version-locks.create` | Create secret version locks.	 | Manager, Writer |
| `secrets-manager.secret-version-locks.list` | List secret version locks | Manager, Reader, SecretsReader, Writer |
| `secrets-manager.secret-version-locks.delete` | Delete secret version locks. | Manager |
| `secrets-manager.secrets-locks.list` | List secrets locks. | Manager, Reader, SecretsReader, Writer |
{: caption="Table 139. Service actions - Secrets Manager" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="secrets-manager"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table139}

## Simulated Instruments Analytics API
{: #sia-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `sia` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 140. Platform roles - Simulated Instruments Analytics API" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="sia"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table140}

| Role | Description |
| ----- | :----- |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 140. Service roles - Simulated Instruments Analytics API" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="sia"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table140}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `sia.dashboard.view` |  | Administrator, Editor, Operator |
| `sia.instrument.read` |  | Reader |
{: caption="Table 140. Service actions - Simulated Instruments Analytics API" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="sia"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table140}

## Skytap On IBM Cloud
{: #skytap-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `skytap` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 141. Platform roles - Skytap On IBM Cloud" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="skytap"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table141}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `skytap.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 141. Service actions - Skytap On IBM Cloud" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="skytap"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table141}

## Software Billing
{: #software-billing-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `software-billing` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 142. Platform roles - Software Billing" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="software-billing"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table142}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `software-billing.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 142. Service actions - Software Billing" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="software-billing"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table142}

## Speech to Text
{: #speech-to-text-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `speech-to-text` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 143. Platform roles - Speech to Text" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="speech-to-text"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table143}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 143. Service roles - Speech to Text" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="speech-to-text"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table143}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `speech-to-text.dashboard.view` |  | Administrator, Editor, Operator |
| `GET /speech-to-text` |  | Manager, Reader, Writer |
| `POST /speech-to-text` |  | Manager, Writer |
| `DELETE /speech-to-text` |  | Manager, Writer |
| `HEAD /speech-to-text` |  | Manager, Reader, Writer |
| `PUT /speech-to-text` |  | Manager, Writer |
{: caption="Table 143. Service actions - Speech to Text" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="speech-to-text"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table143}

## sql-query
{: #sql-query-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `sql-query` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 144. Service roles - sql-query" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="sql-query"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table144}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `sql-query.api.submit` | Submit SQL jobs that read and write data, including catalog metadata , such as table definitions. | Manager, Writer |
| `sql-query.api.getalljobs` | Retrieve a list of recent job submissions and their outcome status. | Manager, Reader, Writer |
| `sql-query.api.getjobinfo` | Retrieve the detailed status of a job based on provided jobid. | Manager, Reader, Writer |
| `sql-query.api.managecatalog` | Manage the catalog and indexes. For example, submit DDL statements to create, alter and drop tables, views and indexes. | Manager |
| `sql-query.api.readcatalog` | Introspect the catalog. For example, list the definitions of tables, views and indexes. | Manager, Reader, Writer |
{: caption="Table 144. Service actions - sql-query" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="sql-query"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table144}

## streaming-analytics
{: #streaming-analytics-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `streaming-analytics` for the service name.

| Role | Description |
| ----- | :----- |
| null | null |
| null | null |
{: row-headers}
{: caption="Table 145. Service roles - streaming-analytics" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="streaming-analytics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table145}

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
{: caption="Table 145. Service actions - streaming-analytics" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="streaming-analytics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table145}

## Support Center
{: #support-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `support` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | View, search, create, and update support cases |
| Editor | View, search, create, and update support cases |
| Viewer | View and search support cases |
{: row-headers}
{: caption="Table 146. Platform roles - Support Center" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="support"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table146}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `support.case.create` | The ability to create a case. | Administrator, Editor |
| `support.case.update` | The ability to update a case. | Administrator, Editor |
| `support.case.read` | The ability to search cases. | Administrator, Editor, Viewer |
| `support.case.list` | The ability to view cases. | Administrator, Editor, Viewer |
{: caption="Table 146. Service actions - Support Center" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="support"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table146}

## IBM Cloud Monitoring with Sysdig
{: #sysdig-monitor-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `sysdig-monitor` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions according to the resource for which this role is assigned, including assigning access policies to other users and managing Sysdig team membership. |
{: row-headers}
{: caption="Table 147. Platform roles - IBM Cloud Monitoring with Sysdig" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="sysdig-monitor"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table147}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role.  You are a member of every Sysdig Team with administrative permissions and are able to create, delete and configure all team definitions. |
| Reader | As a reader, you have read access to the environment within the defined Sysdig Team scope, but cannot create, edit or delete dashboards, alerts or other content. |
| Supertenant Metrics Publisher | This role permits IBM services to publish platform metrics to Sysdig |
| Writer | As a writer, you have read and write access to the environment within the defined Sysdig Team scope and can create, edit and delete dashboards, alerts and other content. |
{: row-headers}
{: caption="Table 147. Service roles - IBM Cloud Monitoring with Sysdig" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="sysdig-monitor"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table147}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `sysdig-monitor.launch.user` | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. | Administrator, Manager, Writer |
| `sysdig-monitor.launch.admin` | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. | Administrator, Manager |
| `sysdig-monitor.launch.viewer` | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.secure.manager` | Admin for Sysdig Secure | Administrator |
| `sysdig-monitor.secure.user` | User for Sysdig Secure | Administrator |
| `sysdig-monitor.secure.viewer` | Viewer for Sysdig Secure | Administrator |
| `sysdig-monitor.agent-installation.read` | Agent Installation (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.agent.cli.agent-network-calls-to-remote-pods` | Agent CLI (network calls) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.agent.cli.agent-status` | Agent CLI (agent status) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.agent.cli.view` | Agent CLI (view) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.agent.cli.view-configuration` | Agent CLI (view configuration) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.alert-events.edit` | Alert Events (edit) | Administrator, Manager, Writer |
| `sysdig-monitor.alert-events.read` | Alert Events (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.alerts.edit` | Alerts (edit) | Administrator, Manager, Writer |
| `sysdig-monitor.alerts.read` | Alerts (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.api-token.edit` | API Token (edit) | Administrator, Manager, Writer |
| `sysdig-monitor.api-token.read` | API Token (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.captures.edit` | Captures (edit) | Administrator, Manager, Writer |
| `sysdig-monitor.captures.read` | Captures (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.captures.view` | Captures (view) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.custom-events.edit` | Custom Events (edit) | Administrator, Manager, Writer |
| `sysdig-monitor.custom-events.read` | Custom Events (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.dashboard-metrics-data.read` | Dashboard metrics (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.dashboards.edit` | Dashboards (edit) | Administrator, Manager, Writer |
| `sysdig-monitor.dashboards.read` | Dashboards (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.datastream.read` | Datastream (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.downtimes.read` | Downtimes (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.events-forwarder.read` | Events Forwarder (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.explore.edit` | Explore (edit) | Administrator, Manager |
| `sysdig-monitor.explore.read` | Explore (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.file-storage-config.read` | File Storage Config (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.global.notification-channels.read` | Global Notification Channels (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.groupings.edit` | Groupings (edit) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.groupings.read` | Groupings (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.helmsrenderer.read` | Helms Renderer (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.infrastructure.read` | Infrastructure (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.integrations.read` | Integrations (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.manual-integrations.edit` | Manual Integrations (edit) | Administrator, Manager, Writer |
| `sysdig-monitor.manual-integrations.read` | Manual Integrations (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.memberships.edit` | Memberships (edit) | Administrator |
| `sysdig-monitor.memberships.read` | Memberships (read) | Administrator |
| `sysdig-monitor.metrics-data.read` | Metrics data (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.metrics-descriptors.read` | Metrics descriptors (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.notification-channels.edit` | Notification Channels (edit) | Administrator, Manager, Writer |
| `sysdig-monitor.notification-channels.read` | Notification Channels (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.overviews.read` | Overviews (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.promcat.integrations.edit` | PromCat Integrations (edit) | Administrator, Manager, Writer |
| `sysdig-monitor.promcat.integrations.read` | PromCat Integrations (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.promcat.integrations.validate` | PromCat Integrations (validate) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.promql-metadata.read` | PromQL Metadata (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.providers.read` | Providers (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.spotlight.read` | Spotlight (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.sysdig-storage.read` | Sysdig Storage (read) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.team.sharing.groupings.toggle` | Team Sharing Toggle | Administrator, Manager |
| `sysdig-monitor.teams.manage` | Teams (manage) | Administrator, Manager |
| `sysdig-monitor.teams.read` | Teams (read) | Administrator |
| `sysdig-monitor.token.view` | Token (view) | Administrator, Manager, Reader, Writer |
| `sysdig-monitor.users.read` | Users (read) | Administrator |
| `sysdig-monitor.system-role.admin` | System administrator role | Administrator, Manager |
| `sysdig-monitor.platform-metrics.publish` | Permit publishing of platform metrics to Sysdig | Supertenant Metrics Publisher |
{: caption="Table 147. Service actions - IBM Cloud Monitoring with Sysdig" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="sysdig-monitor"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table147}

## IBM Cloud Security
{: #sysdig-secure-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `sysdig-secure` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 148. Platform roles - IBM Cloud Security" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="sysdig-secure"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table148}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 148. Service roles - IBM Cloud Security" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="sysdig-secure"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table148}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `sysdig-secure.launch.admin` | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. | Administrator, Manager |
| `sysdig-secure.launch.user` | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. | Administrator, Manager, Writer |
| `sysdig-secure.launch.viewer` | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. | Administrator, Manager, Reader, Writer |
{: caption="Table 148. Service actions - IBM Cloud Security" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="sysdig-secure"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table148}

## Text to Speech
{: #text-to-speech-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `text-to-speech` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 149. Platform roles - Text to Speech" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="text-to-speech"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table149}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 149. Service roles - Text to Speech" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="text-to-speech"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table149}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `text-to-speech.dashboard.view` |  | Administrator, Editor, Operator |
| `GET /text-to-speech` |  | Manager, Reader, Writer |
| `POST /text-to-speech` |  | Manager, Writer |
| `DELETE /text-to-speech` |  | Manager, Writer |
| `HEAD /text-to-speech` |  | Manager, Reader, Writer |
| `PUT /text-to-speech` |  | Manager, Writer |
{: caption="Table 149. Service actions - Text to Speech" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="text-to-speech"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table149}

## Toolchain
{: #toolchain-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `toolchain` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 150. Platform roles - Toolchain" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="toolchain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table150}

| Role | Description |
| ----- | :----- |
| PipelineRunner | Run Tekton or Classic pipelines. |
{: row-headers}
{: caption="Table 150. Service roles - Toolchain" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="toolchain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table150}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `toolchain.dashboard.view` | View instances of the Toolchain service. | Administrator, Editor, Operator |
| `toolchain.instance.read-properties` | Read toolchain properties. | Administrator, Editor, Viewer |
| `toolchain.instance.update-properties` | Update toolchain properties. | Administrator, Editor |
| `toolchain.instance.create-bindings` | Add a tool integration to a toolchain within a resource group. | Administrator, Editor |
| `toolchain.instance.delete-bindings` | Remove a tool integration from a toolchain within a resource group. | Administrator, Editor |
| `toolchain.instance.list-bindings` | View the tool integrations that are contained in a toolchain within a resource group. | Administrator, Editor, Viewer |
| `toolchain.pipeline-run.create` | Run the selected pipeline. | Administrator, Editor, Operator, PipelineRunner, Viewer |
{: caption="Table 150. Service actions - Toolchain" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="toolchain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table150}

## Transit Gateway
{: #transit-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `transit` for the service name.

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
{: row-headers}
{: caption="Table 151. Service roles - Transit Gateway" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="transit"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table151}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `transit.transit.manage` | Transit service manager | Manager |
{: caption="Table 151. Service actions - Transit Gateway" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="transit"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table151}

## Transit Gateway
{: #transit.gateway-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `transit.gateway` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 152. Platform roles - Transit Gateway" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="transit.gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table152}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `transit.gateway.view` | The ability to view transit gateways and connections. | Administrator, Editor, Operator, Viewer |
| `transit.gateway.edit` | The ability to create, change, view and delete transit gateways and connections. | Administrator, Editor |
{: caption="Table 152. Service actions - Transit Gateway" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="transit.gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table152}

## IBM Cloud Platform User Management Service
{: #user-management-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `user-management` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can view, invite, and update users. You can also view and update user profile settings. |
| Editor | As an editor, you can view, invite, and update users. You can also view and update profile settings. |
| Operator | As an operator, you can view users in the account and view profile settings. |
| Viewer | As a viewer, you can view users in the account and view profile settings. |
{: row-headers}
{: caption="Table 153. Platform roles - IBM Cloud Platform User Management Service" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="user-management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table153}

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
| `user-management.user-setting.update` |  | Administrator, Editor |
| `user-management.user-setting.retrieve` |  | Administrator, Editor, Operator, Viewer |
{: caption="Table 153. Service actions - IBM Cloud Platform User Management Service" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="user-management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table153}

## VMware Solutions on VPC
{: #vmware-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `vmware` for the service name.

No supported roles.
## VMware Solutions
{: #vmware-solutions-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `vmware-solutions` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 155. Platform roles - VMware Solutions" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="vmware-solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table155}

| Role | Description |
| ----- | :----- |
| Director Backup User | As a backup user within the vCloud Director console, you can manage Veeam backup jobs. |
| Director Catalog Author | As a catalog author within the vCloud Director console, you can create and publish catalogs. |
| Director Console User | As a console user within the vCloud Director console, you can view the VM state, properties, and use the Guest OS. |
| Director Full Viewer | As a full viewer within the vCloud Director console, you have All View Access to every component in vCloud Director. |
| Director Network Admin | As a network administrator within the vCloud Director console, you can create, view, edit, delete the subnet, the static route, and troubleshoot routing. |
| Director Security Admin | As a security administrator within the vCloud Director console, you can view and edit the edge firewall or view and edit the distributed firewall. |
| Director vApp Author | As a vApp author within the vCloud Director console, you can use catalogs and create vApps. |
| Director vApp User | As a vApp user within the vCloud Director console, you can use existing vApps. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 155. Service roles - VMware Solutions" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="vmware-solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table155}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `vmware-solutions.instances.create` | Create IBM Cloud for VMware Solutions instances | Administrator, Manager |
| `vmware-solutions.instances.delete` | Delete IBM Cloud for VMware Solutions instances | Administrator, Manager |
| `vmware-solutions.instances.view` | List or view IBM Cloud for VMware Solutions instances | Administrator, Director Backup User, Director Catalog Author, Director Console User, Director Full Viewer, Director Network Admin, Director Security Admin, Director vApp Author, Director vApp User, Editor, Manager, Operator, Reader, Viewer, Writer |
| `vmware-solutions.instances.update` | Update IBM Cloud for VMware Solutions instances | Administrator, Editor, Manager, Writer |
| `vmware-solutions.account.update` | Update account settings for IBM Cloud for VMware Solutions | Administrator, Manager |
| `vmware-solutions.directorsite.administrator` | Director Administrator | Administrator |
| `vmware-solutions.directorsite.vappauthor` | Director vApp Author | Director vApp Author |
| `vmware-solutions.directorsite.vappuser` | Director vApp User | Director vApp User |
| `vmware-solutions.directorsite.fullviewer` | Director Full Viewer | Director Full Viewer |
| `vmware-solutions.directorsite.catalogauthor` | Director Catalog Author | Director Catalog Author |
| `vmware-solutions.directorsite.writer` | Director Writer | Writer |
| `vmware-solutions.directorsite.manager` | Director Manager | Manager |
| `vmware-solutions.directorsite.reader` | Director Reader | Reader |
| `vmware-solutions.directorsite.networkadmin` | Director Network Admin | Director Network Admin |
| `vmware-solutions.directorsite.consoleuser` | Director Console User | Director Console User |
| `vmware-solutions.directorsite.securityadmin` | Director Security Admin | Director Security Admin |
| `vmware-solutions.directorsite.backupuser` | Director Backup User | Director Backup User |
| `vmware-solutions.directorsite.editor` | Director Editor | Editor |
| `vmware-solutions.directorsite.viewer` | Viewer in Director | Viewer |
| `vmware-solutions.directorsite.operator` | Director Operator | Operator |
{: caption="Table 155. Service actions - VMware Solutions" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="vmware-solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table155}

## VMware Cloud Director
{: #vmware.directorsite-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `vmware.directorsite` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 156. Platform roles - VMware Cloud Director" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="vmware.directorsite"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table156}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| VMwaaS Director Backup User | As a backup user within the vCloud Director console, you can manage Veeam backup jobs. |
| VMwaaS Director Catalog Author | As a catalog author within the vCloud Director console, you can create and publish catalogs. |
| VMwaaS Director Console User | As a console user within the vCloud Director console, you can view the VM state, properties, and use the Guest OS. |
| VMwaaS Director Full Viewer | As a full viewer within the vCloud Director console, you have All View Access to every component in vCloud Director. |
| VMwaaS Director Network Admin | As a network administrator within the vCloud Director console, you can create, view, edit, delete the subnet, the static route, and troubleshoot routing. |
| VMwaaS Director Security Admin | As a security administrator within the vCloud Director console, you can view and edit the edge firewall or view and edit the distributed firewall. |
| VMwaaS Director vApp Author | As a vApp author within the vCloud Director console, you can use catalogs and create vApps. |
| VMwaaS Director vApp User | As a vApp user within the vCloud Director console, you can use existing vApps. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 156. Service roles - VMware Cloud Director" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="vmware.directorsite"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table156}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `vmware.directorsite.infrastructure.create` | Create vCloud Director | Administrator, Editor |
| `vmware.directorsite.infrastructure.delete` | Delete a single-tenant VMware Director instance | Administrator, Editor |
| `vmware.directorsite.infrastructure.view` | View a single-tenant VMware Director instance | Administrator, Editor, Operator, Viewer |
| `vmware.directorsite.infrastructure.update` | Update a single-tenant VMware Director instance | Administrator, Editor, Operator |
| `vmware.directorsite.director.create` | Create Director virtual datacenters | Administrator, Editor, Manager |
| `vmware.directorsite.director.delete` | Delete Director virtual datacenters | Administrator, Editor, Manager |
| `vmware.directorsite.director.update` | Edit Director virtual datacenters | Administrator, Editor, Manager, Operator, Writer |
| `vmware.directorsite.director.view` | View Director virtual datacenters | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| `vmware.directorsite.director.account` | Reset the Director Admin password | Administrator, Manager |
| `vmware.directorsite.administrator` | Director Administrator | Administrator |
| `vmware.directorsite.editor` | Director Editor | Editor |
| `vmware.directorsite.operator` | Director Operator | Operator |
| `vmware.directorsite.viewer` | Viewer in Director | Viewer |
| `vmware.directorsite.manager` | Director Manager | Manager |
| `vmware.directorsite.writer` | Director Writer | Writer |
| `vmware.directorsite.reader` | Director Reader | Reader |
| `vmware.directorsite.fullviewer` | Director Full Viewer | VMwaaS Director Full Viewer |
| `vmware.directorsite.vappauthor` | Director vApp Author | VMwaaS Director vApp Author |
| `vmware.directorsite.vappuser` | Director vApp User | VMwaaS Director vApp User |
| `vmware.directorsite.catalogauthor` | Director Catalog Author | VMwaaS Director Catalog Author |
| `vmware.directorsite.networkadmin` | Director Network Admin | VMwaaS Director Network Admin |
| `vmware.directorsite.consoleuser` | Director Console User | VMwaaS Director Console User |
| `vmware.directorsite.backupuser` | Director Backup User | VMwaaS Director Backup User |
| `vmware.directorsite.securityadmin` | Director Security Admin | VMwaaS Director Security Admin |
{: caption="Table 156. Service actions - VMware Cloud Director" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="vmware.directorsite"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table156}

## Organization Virtual Data Center
{: #vmware.vdc-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `vmware.vdc` for the service name.

No supported roles.
## Voice Agent with Watson
{: #voiceagent-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `voiceagent` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 158. Platform roles - Voice Agent with Watson" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="voiceagent"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table158}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 158. Service roles - Voice Agent with Watson" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="voiceagent"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table158}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `voiceagent.agent.manage` | Manage all aspects of a Voice Agent with Watson instance. | Manager, Reader, Writer |
| `voiceagent.agent.view` | View configurations for all agents of a Voice Agent with Watson instance. | Reader |
| `voiceagent.usage.view` | View usage for all agents of a Voice Agent with Watson instance. | Reader |
| `voiceagent.log.view` | View all failure logs for all agents of a Voice Agent with Watson instance. | Reader |
| `voiceagent.sms.send` | Use the SMS gateway API to send SMS messages for a Voice Agent with Watson instance. | Administrator, Editor, Manager, Operator, Writer |
| `voiceagent.voice.inbound` | Authenticate inbound calls for a Voice Agent with Watson instance using SIPS. | Manager, Writer |
| `voiceagent.voice.outbound` | Use the outbound calling API to start outbound calls for a Voice Agent with Watson instance. | Manager, Writer |
{: caption="Table 158. Service actions - Voice Agent with Watson" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="voiceagent"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table158}

## WebSphere Application Server
{: #websphereappsvr-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `websphereappsvr` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 159. Platform roles - WebSphere Application Server" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="websphereappsvr"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table159}

| Action | Description | Roles |
| ----- | :----- | :----- |
| `websphereappsvr.dashboard.view` |  | Administrator, Editor, Operator |
{: caption="Table 159. Service actions - WebSphere Application Server" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="websphereappsvr"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table159}

## Annotator for Clinical Data
{: #wh-acd-roles}

Review the available platform and service roles and the actions mapped to each to help you assign access. If you're using the CLI or API to assign access, use `wh-acd` for the service name.

| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 160. Platform roles - Annotator for Clinical Data" caption-side="top"}
{: tab-title="Platform roles"}
{: tab-group="wh-acd"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the platform role name and the column headers identify the specific information available about each role."}
{: #platform-roles-table160}

| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 160. Service roles - Annotator for Clinical Data" caption-side="top"}
{: tab-title="Service roles"}
{: tab-group="wh-acd"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers provide the service role name and the column headers identify the specific information available about each role."}
{: #service-roles-table160}

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
{: caption="Table 160. Service actions - Annotator for Clinical Data" caption-side="top"}
{: tab-title="Actions"}
{: tab-group="wh-acd"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table provides the available actions for the service, descriptions of each, and the roles that each action are mapped to."}
{: #actions-table160}

