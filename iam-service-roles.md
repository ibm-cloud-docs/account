---

copyright:

  years: 2019

lastupdated: "2020-07-08"

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

It is important to understand what roles assign different levels of access when you're assigning access in your account. The following tables provide information about the access roles and the actions mapped to each by the {{site.data.keyword.cloud_notm}} services. 
{: shortdesc}

<!-- Everything is deleted after this line. -->
## API Connect
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 1. Service Roles - API Connect" caption-side="top"}
{: #roles-table1}
{: tab-title="Roles"}
{: tab-group="API Connect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| apiconnect.instance.view |  | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| apiconnect.instance.admin |  | Administrator, Editor, Manager |
| apiconnect.instance.edit |  | Administrator, Editor, Manager, Operator, Writer |
{: row-headers}
{: caption="Table 1. Service Actions - API Connect" caption-side="top"}
{: #roles-table1}
{: tab-title="Actions"}
{: tab-group="API Connect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## API Gateway
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 2. Service Roles - API Gateway" caption-side="top"}
{: #roles-table2}
{: tab-title="Roles"}
{: tab-group="API Gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| api-gateway.dashboard.view |  | Administrator, Editor, Operator |
| api-gateway.api.view |  | Manager, Reader, Writer |
| api-gateway.api.create |  | Manager, Writer |
| api-gateway.api.edit |  | Manager, Writer |
| api-gateway.api.delete |  | Manager, Writer |
| api-gateway.api.share |  | Manager |
{: row-headers}
{: caption="Table 2. Service Actions - API Gateway" caption-side="top"}
{: #roles-table2}
{: tab-title="Actions"}
{: tab-group="API Gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Actifio GO
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 3. Service Roles - Actifio GO" caption-side="top"}
{: #roles-table3}
{: tab-title="Roles"}
{: tab-group="Actifio GO"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| actifio-go.dashboard.view |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 3. Service Actions - Actifio GO" caption-side="top"}
{: #roles-table3}
{: tab-title="Actions"}
{: tab-group="Actifio GO"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Analytics Engine
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
{: row-headers}
{: caption="Table 4. Service Roles - Analytics Engine" caption-side="top"}
{: #roles-table4}
{: tab-title="Roles"}
{: tab-group="Analytics Engine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| ibmae.cluster.createlogconfig |  | Administrator, Editor, Manager, Writer |
| ibmae.cluster.customize |  | Administrator, Editor, Manager, Writer |
| ibmae.cluster.deletelogconfig |  | Administrator, Editor, Manager, Writer |
| ibmae.cluster.read |  | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| ibmae.cluster.resize |  | Administrator, Editor, Manager, Writer |
| ibmae.cluster.resetpassword |  | Administrator, Manager |
| ibmae.cluster.updatePrivateEndpointWhitelist |  | Administrator, Editor, Manager, Writer |
| ibmae.cluster.viewpassword |  | Administrator, Editor, Manager, Writer |
{: row-headers}
{: caption="Table 4. Service Actions - Analytics Engine" caption-side="top"}
{: #roles-table4}
{: tab-title="Actions"}
{: tab-group="Analytics Engine"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Annotator for Clinical Data
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 5. Service Roles - Annotator for Clinical Data" caption-side="top"}
{: #roles-table5}
{: tab-title="Roles"}
{: tab-group="Annotator for Clinical Data"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| wh-acd.dashboard.view |  | Administrator, Editor, Operator |
| GET /wh-acd |  | Manager, Reader, Writer |
| PUT /wh-acd |  | Manager, Writer |
| POST /wh-acd |  | Manager, Writer |
| DELETE /wh-acd |  | Manager |
{: row-headers}
{: caption="Table 5. Service Actions - Annotator for Clinical Data" caption-side="top"}
{: #roles-table5}
{: tab-title="Actions"}
{: tab-group="Annotator for Clinical Data"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## App ID
| Role | Description |
| ----- | :----- |
| Reader | Reader |
| Writer | Writer |
| Manager | Manager |
{: row-headers}
{: caption="Table 6. Service Roles - App ID" caption-side="top"}
{: #roles-table6}
{: tab-title="Roles"}
{: tab-group="App ID"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| appid.mgmt.set.sender.details.cd |  | Manager, Writer |
| appid.mgmt.get.sender.details.cd |  | Manager, Reader, Writer |
| appid.mgmt.set.redirect.uris |  | Manager, Writer |
| appid.mgmt.get.redirect.uris |  | Manager, Reader, Writer |
| appid.mgmt.set.idps |  | Manager, Writer |
| appid.mgmt.get.idps |  | Manager, Reader, Writer |
| appid.mgmt.get.recent.activities |  | Manager, Reader, Writer |
| appid.mgmt.get.ui.config |  | Manager, Reader, Writer |
| appid.mgmt.set.ui.config |  | Manager, Writer |
| appid.mgmt.get.user.profile.config |  | Manager, Reader, Writer |
| appid.mgmt.set.user.profile.config |  | Manager, Writer |
| appid.mgmt.get.cd.users |  | Manager, Reader, Writer |
| appid.mgmt.add.cd.user |  | Manager, Writer |
| appid.mgmt.set.cd.user |  | Manager, Writer |
| appid.mgmt.delete.cd.user |  | Manager, Writer |
| appid.mgmt.get.email.template |  | Manager, Reader, Writer |
| appid.mgmt.update.email.template |  | Manager, Writer |
| appid.mgmt.delete.email.template |  | Manager, Writer |
| appid.mgmt.get.saml.metadata |  | Manager, Reader, Writer |
| appid.mgmt.post.saml.logo |  | Manager, Writer |
| appid.mgmt.resend.notification.cd |  | Manager, Writer |
| appid.mgmt.get.tokens.configuration |  | Manager, Reader, Writer |
| appid.mgmt.set.tokens.configuration |  | Manager, Writer |
| appid.mgmt.cd.sign.up |  | Manager, Writer |
| appid.mgmt.cd.sign.up.result |  | Manager, Writer |
| appid.mgmt.cd.forgot.password |  | Manager, Writer |
| appid.mgmt.cd.forgot.password.result |  | Manager, Writer |
| appid.mgmt.cd.change.password |  | Manager, Writer |
| appid.mgmt.get.cd.actions.urls |  | Manager, Reader, Writer |
| appid.mgmt.get.cd.action.url |  | Manager, Reader, Writer |
| appid.mgmt.update.cd.action.url |  | Manager, Writer |
| appid.mgmt.del.cd.action.url |  | Manager, Writer |
| appid.mgmt.bulk.cd.users |  | Manager, Writer |
| appid.mgmt.get.cd.password.policy |  | Manager, Reader, Writer |
| appid.mgmt.update.cd.password.policy |  | Manager, Writer |
| appid.mgmt.delete.profile |  | Manager, Writer |
| appid.mgmt.get.profile |  | Manager, Reader, Writer |
| appid.mgmt.update.profile |  | Manager, Writer |
| appid.mgmt.get.profiles |  | Manager, Reader, Writer |
| appid.mgmt.revoke.refresh.token |  | Manager, Writer |
| appid.mgmt.nominate.user |  | Manager, Writer |
| appid.mgmt.update.cd.get.email.dispatcher |  | Manager, Reader, Writer |
| appid.mgmt.update.cd.set.email.dispatcher |  | Manager, Writer |
| appid.mgmt.update.cd.post.email.dispatcher.test |  | Manager, Writer |
| appid.mgmt.add.application |  | Manager, Writer |
| appid.mgmt.delete.application |  | Manager, Writer |
| appid.mgmt.update.application |  | Manager, Writer |
| appid.mgmt.get.applications |  | Manager, Reader, Writer |
| appid.mgmt.get.application |  | Manager, Reader, Writer |
| appid.mgmt.export.cd.users |  | Manager |
| appid.mgmt.import.cd.users |  | Manager |
| appid.mgmt.get.capture.runtime.activity |  | Manager, Reader, Writer |
| appid.mgmt.update.capture.runtime.activity |  | Manager, Writer |
| appid.mgmt.get.mfa.channels |  | Manager, Reader, Writer |
| appid.mgmt.get.mfa.channel |  | Manager, Reader, Writer |
| appid.mgmt.update.mfa.channel |  | Manager, Writer |
| appid.mgmt.update.mfa.config |  | Manager, Writer |
| appid.mgmt.get.mfa.config |  | Manager, Reader, Writer |
| appid.mgmt.get.advanced.password.management |  | Manager, Reader, Writer |
| appid.mgmt.set.advanced.password.management |  | Manager, Writer |
| appid.mgmt.get.sso.config |  | Manager, Reader, Writer |
| appid.mgmt.update.sso.config |  | Manager, Writer |
| appid.mgmt.post.sso.logout |  | Manager, Writer |
| appid.mgmt.cd.post.sms.dispatcher.test |  | Manager, Writer |
| appid.mgmt.remove.cd.user |  | Manager, Writer |
| appid.mgmt.get.cd.userinfo |  | Manager, Reader, Writer |
| appid.mgmt.get.cd.rate.config |  | Manager, Reader, Writer |
| appid.mgmt.update.cd.rate.config |  | Manager, Writer |
| appid.mgmt.import.profiles |  | Manager |
| appid.mgmt.export.profiles |  | Manager |
| appid.mgmt.add.scope |  | Manager, Writer |
| appid.mgmt.get.scopes |  | Manager, Reader, Writer |
| appid.mgmt.delete.scope |  | Manager, Writer |
| appid.mgmt.add.role |  | Manager, Writer |
| appid.mgmt.get.role |  | Manager, Reader, Writer |
| appid.mgmt.update.role |  | Manager, Writer |
| appid.mgmt.delete.role |  | Manager, Writer |
| appid.mgmt.get.user.roles |  | Manager, Reader, Writer |
| appid.mgmt.update.user.roles |  | Manager, Writer |
| appid.mgmt.get.webhook.config |  | Manager, Reader, Writer |
| appid.mgmt.update.webhook.config |  | Manager, Writer |
| appid.mgmt.update.webhook.active |  | Manager, Writer |
| appid.mgmt.test.webhook.config |  | Manager, Writer |
| appid.mgmt.del.totp.channel |  | Manager, Writer |
{: row-headers}
{: caption="Table 6. Service Actions - App ID" caption-side="top"}
{: #roles-table6}
{: tab-title="Actions"}
{: tab-group="App ID"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Billing
No supported roles.
{: row-headers}
{: caption="Table 7. Service Roles - Billing" caption-side="top"}
{: #roles-table7}
{: tab-title="Roles"}
{: tab-group="Billing"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

No supported actions.
{: row-headers}
{: caption="Table 7. Service Actions - Billing" caption-side="top"}
{: #roles-table7}
{: tab-title="Actions"}
{: tab-group="Billing"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Block Storage for VPC
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 8. Service Roles - Block Storage for VPC" caption-side="top"}
{: #roles-table8}
{: tab-title="Roles"}
{: tab-group="Block Storage for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.volume.profile.view |  | Administrator, Editor, Operator, Viewer |
| is.volume.volume.create |  | Administrator, Editor |
| is.volume.volume.list |  | Administrator, Editor, Operator, Viewer |
| is.volume.volume.read |  | Administrator, Editor, Operator, Viewer |
| is.volume.volume.update |  | Administrator, Editor |
| is.volume.volume.delete |  | Administrator, Editor |
{: row-headers}
{: caption="Table 8. Service Actions - Block Storage for VPC" caption-side="top"}
{: #roles-table8}
{: tab-title="Actions"}
{: tab-group="Block Storage for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Blockchain Platform
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 9. Service Roles - Blockchain Platform" caption-side="top"}
{: #roles-table9}
{: tab-title="Roles"}
{: tab-group="Blockchain Platform"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| blockchain.components.create | Can create (provision) Orderes/CAs/Peers | Manager |
| blockchain.components.remove | Can remove imported Orderes/CAs/Peers | Manager, Writer |
| blockchain.components.import | Can import external Orderes/CAs/Peers | Manager, Writer |
| blockchain.components.export | Can export any Orderes/CAs/Peers | Manager, Reader, Writer |
| blockchain.optools.restart | Can restart the UI server | Manager |
| blockchain.optools.logs | Can change logging settings of the UI | Manager |
| blockchain.optools.view | Can view the UI & logs as well as run any GET api | Manager, Reader, Writer |
| blockchain.notifications.manage | Can add/remove UI notifications | Manager, Writer |
| blockchain.components.delete | Can remove provisioned Orderes/CAs/Peers | Manager |
| blockchain.signaturecollection.manage | Can add/remove signature collections | Manager, Writer |
| blockchain.optools.settings | Can change UI settings | Manager |
| blockchain.components.manage | Can manage admin certs on Peers/Orderers as well as enroll ids on CAs | Manager, Writer |
| blockchain.instance.link | Can associate an IBM Blockchain Platform service instance with a cluster | Manager |
| blockchain.instance.view | Can get the status of the an IBM Blockchain Platform service instance | Manager, Reader, Writer |
| blockchain.optools.redeploy | Can redeploy an IBM Blockchain Platform service instance | Manager |
{: row-headers}
{: caption="Table 9. Service Actions - Blockchain Platform" caption-side="top"}
{: #roles-table9}
{: tab-title="Actions"}
{: tab-group="Blockchain Platform"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Catalog Management
| Role | Description |
| ----- | :----- |
| Administrator | You can set filters in the IBM Cloud catalog that apply to all users in an account. You can also create, update, or delete private catalogs, publish IBM-approved offerings, and assign user access. |
| Publisher | You can publish offerings that are approved by IBM and that are in a private catalog to which you're assigned the viewer role. |
| Editor | You can create, update, or delete private catalogs and set filters for the IBM Cloud catalog that apply at the private catalog level. You can also view account-level filters, but you can?t modify them. |
| Viewer | You can view the filtered offerings in the IBM Cloud catalog and the filter settings, but you can?t modify the settings. You can view private catalogs, but you can't modify them. |
| Operator | You can view the filtered offerings in the IBM Cloud catalog and the filter settings, but you can?t modify the settings. You can view private catalogs, but you can't modify them. |
{: row-headers}
{: caption="Table 10. Service Roles - Catalog Management" caption-side="top"}
{: #roles-table10}
{: tab-title="Roles"}
{: tab-group="Catalog Management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| globalcatalog-collection.instance.promote | Publish item to public, assuming also has viewer access. | Administrator, Publisher |
| globalcatalog-collection.operation.approve | This action approves the publishing of items to public. Only IBM can use this action. | Publisher |
| globalcatalog-collection.account.manage | This action manages account level settings, e.g. Hiding the public catalog from the account members. | Administrator |
| globalcatalog-collection.test.hasrole | internal use - has role test | Editor, Operator, Viewer |
{: row-headers}
{: caption="Table 10. Service Actions - Catalog Management" caption-side="top"}
{: #roles-table10}
{: tab-title="Actions"}
{: tab-group="Catalog Management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Certificate Manager
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 11. Service Roles - Certificate Manager" caption-side="top"}
{: #roles-table11}
{: tab-title="Roles"}
{: tab-group="Certificate Manager"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| cloudcerts.certificate.import | Re/Import a certificate and its private key. | Manager |
| cloudcerts.certificate.delete | Delete a certificate | Manager |
| cloudcerts.certificate.read | Retrieve a certificate, its private key, and its intermediate certificate if present | Manager, Writer |
| cloudcerts.certificate.update | Update the name and description of a certificate | Manager, Writer |
| cloudcerts.certificates.list | Retrieve a list of all certificates and their associated metadata or perform a search for certificates | Manager, Reader, Writer |
| cloudcerts.notifications.publickey | Retrieve the public key for Callback URL notifications | Manager, Reader, Writer |
| cloudcerts.certificate.order | Order/Renew a certificate | Manager |
| cloudcerts.certificate-metadata.read | Retrieve the metadata of a certificate | Manager, Reader, Writer |
| cloudcerts.notifications-channel.update | Update the endpoint or state of a notification channel | Manager |
| cloudcerts.notifications-channel.list | Retrieve all notification channels | Manager, Reader, Writer |
| cloudcerts.notifications-channel.delete | Delete a notification channel | Manager |
| cloudcerts.notifications-channel.test | Test a notification channel | Manager, Reader, Writer |
| cloudcerts.notifications-channel.create | Create a new notification channel. | Manager |
{: row-headers}
{: caption="Table 11. Service Actions - Certificate Manager" caption-side="top"}
{: #roles-table11}
{: tab-title="Actions"}
{: tab-group="Certificate Manager"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Cloud Foundry Enterprise Environment
No supported roles.
{: row-headers}
{: caption="Table 12. Service Roles - Cloud Foundry Enterprise Environment" caption-side="top"}
{: #roles-table12}
{: tab-title="Roles"}
{: tab-group="Cloud Foundry Enterprise Environment"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

No supported actions.
{: row-headers}
{: caption="Table 12. Service Actions - Cloud Foundry Enterprise Environment" caption-side="top"}
{: #roles-table12}
{: tab-title="Actions"}
{: tab-group="Cloud Foundry Enterprise Environment"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## CloudAMQP
| Role | Description |
| ----- | :----- |
| Operator | Operator |
| Administrator | Administrator |
| Editor | Editor |
{: row-headers}
{: caption="Table 13. Service Roles - CloudAMQP" caption-side="top"}
{: #roles-table13}
{: tab-title="Roles"}
{: tab-group="CloudAMQP"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| cldamqp.dashboard.view |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 13. Service Actions - CloudAMQP" caption-side="top"}
{: #roles-table13}
{: tab-title="Actions"}
{: tab-group="CloudAMQP"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Cloudant
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Monitor | As a Monitor, you have permissions to get information about specified databases, list databases, monitor indexing and replication, view data volume usage and view provisioned and current throughput. |
| Checkpointer | As a Checkpointer, you have permissions to write _local documents enabling checkpoint writes. checkpoints are local documents optionally creaded during replicaton recording their state. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 14. Service Roles - Cloudant" caption-side="top"}
{: #roles-table14}
{: tab-title="Roles"}
{: tab-group="Cloudant"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| cloudantnosqldb.db.any | Perform any database action | Manager |
| cloudantnosqldb.activity-tracker-event-types.read | Access list of configured activity tracker event types for a service instance | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
| cloudantnosqldb.activity-tracker-event-types.write | Update list of configured activity tracker event types for a service instance | Administrator, Manager, Operator |
| cloudantnosqldb.sapi.lastactivity | Access last activity time for account | Manager |
| cloudantnosqldb.sapi.usercors | Update CORS settings for a service instance | Manager |
| cloudantnosqldb.sapi.apikeys | Generate Cloudant API keys for a service instance | Manager |
| cloudantnosqldb.sapi.userccmdiagnostics | Access current and maximum allowed throughput values | Manager |
| cloudantnosqldb.sapi.supportattachments | View attachments on support tickets for user | Manager |
| cloudantnosqldb.sapi.supporttickets | View support tickets for user | Manager |
| cloudantnosqldb.sapi.userinfo | Retrieve basic user infomation for this user | Administrator, Editor, Manager, Operator, Viewer |
| cloudantnosqldb.users-database-info.read | Read _users database info | Manager |
| cloudantnosqldb.users-database.create | Create users databases | Manager |
| cloudantnosqldb.users-database.delete | Delete users databases | Manager |
| cloudantnosqldb.users.read | Read from users databases | Manager |
| cloudantnosqldb.users.write | Write to users databases | Manager |
| cloudantnosqldb.database.create | Create databases | Manager |
| cloudantnosqldb.database.delete | Delete databases | Manager |
| cloudantnosqldb.sapi.userplan | Retrieve and update instance plan settings | Administrator, Editor, Manager, Operator, Viewer |
| cloudantnosqldb.sapi.usage-data-volume | View instance data usage | Administrator, Editor, Manager, Monitor, Operator, Viewer |
| cloudantnosqldb.sapi.usage-requests | View instance requests usage | Manager |
| cloudantnosqldb.account-active-tasks.read | View active tasks for instance | Manager, Monitor |
| cloudantnosqldb.sapi.db-security | Allow update of database security | Manager |
| cloudantnosqldb.session.write | Write _session endpoint | Manager, Reader, Writer |
| cloudantnosqldb.session.read | Read _session endpoint | Manager, Reader, Writer |
| cloudantnosqldb.session.delete | Delete _session endpoint | Manager, Reader, Writer |
| cloudantnosqldb.iam-session.write | Write _iam_session endpoint | Manager, Reader, Writer |
| cloudantnosqldb.iam-session.read | Read _iam_session endpoint | Manager, Reader, Writer |
| cloudantnosqldb.iam-session.delete | Delete _iam_session endpoint | Manager, Reader, Writer |
| cloudantnosqldb.account-db-updates.read | Read db_updates feed | Manager, Reader, Writer |
| cloudantnosqldb.any-document.read | Read any documents in a normal database | Manager, Reader, Writer |
| cloudantnosqldb.database-info.read | Read /db/ database info | Manager, Monitor, Reader, Writer |
| cloudantnosqldb.account-dbs-info.read | Read _dbs_info endpoint | Manager, Monitor, Reader, Writer |
| cloudantnosqldb.replicator-database-info.read | Read _replicator database info | Manager |
| cloudantnosqldb.replicator-database.create | Create _replicator databases | Manager |
| cloudantnosqldb.replicator-database.delete | Delete _replicator databases | Manager |
| cloudantnosqldb.replication.write | Write to _replicator databases | Manager |
| cloudantnosqldb.replication.read | Read from _replicator databases | Manager |
| cloudantnosqldb.replication-scheduler.read | Read from replication _scheduler endpoints | Manager, Monitor |
| cloudantnosqldb.account-up.read | View _up | Manager, Monitor |
| cloudantnosqldb.account-uuids.read | Generate doc ID UUIDs | Manager, Writer |
| cloudantnosqldb.data-document.write | Create, update and delete normal documents in a database | Manager, Writer |
| cloudantnosqldb.local-document.write | Write _local documents | Checkpointer, Manager, Writer |
| cloudantnosqldb.design-document.write | Write _design documents | Manager |
| cloudantnosqldb.cluster-membership.read | View cluster membership | Manager |
| cloudantnosqldb.database-security.read | Read database security definitions | Manager |
| cloudantnosqldb.database-security.write | Write database security definitions | Manager |
| cloudantnosqldb.database-shards.read | View database shard metadata | Manager, Monitor |
| cloudantnosqldb.capacity-throughput.read | Read current provisioned throughput | Administrator, Editor, Manager, Monitor, Operator, Viewer |
| cloudantnosqldb.capacity-throughput.write | Update provisioned throughput capacity | Administrator, Editor, Manager |
| cloudantnosqldb.current-throughput.read | Read current request throughput | Manager, Monitor |
| cloudantnosqldb.limits-throughput.read | Read throughput limits for current Plan | Manager |
| cloudantnosqldb.account-all-dbs.read | List all databases | Manager, Monitor, Reader, Writer |
| cloudantnosqldb.account-deleted-dbs.list | List deleted databases | Manager, Monitor |
| cloudantnosqldb.account-deleted-dbs.restore | Restore deleted database | Manager |
| cloudantnosqldb.account-deleted-dbs.delete | Delete deleted database | Manager |
| cloudantnosqldb.account-meta-info.read | View account metadata | Manager, Monitor, Reader, Writer |
| cloudantnosqldb.database-ensure-full-commit.execute | Call _ensure_full_commit endpoint | Manager, Writer |
| cloudantnosqldb.account-search-analyze.execute | Call _search_analyze endpoint | Manager, Reader, Writer |
| cloudantnosqldb.couchdbextension-instance.read | View metadata of an Extension for Apache CouchDB instance | Manager |
| cloudantnosqldb.couchdbextension-instance.write | Make changes to an Extension for Apache CouchDB instance | Manager |
{: row-headers}
{: caption="Table 14. Service Actions - Cloudant" caption-side="top"}
{: #roles-table14}
{: tab-title="Actions"}
{: tab-group="Cloudant"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Compare and Comply
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 15. Service Roles - Compare and Comply" caption-side="top"}
{: #roles-table15}
{: tab-title="Roles"}
{: tab-group="Compare and Comply"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| compare-comply.dashboard.view |  | Administrator, Editor, Operator |
| GET /compare-comply |  | Manager, Reader, Writer |
| POST /compare-comply |  | Manager, Reader, Writer |
| PUT /compare-comply |  | Manager, Reader, Writer |
| DELETE /compare-comply |  | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 15. Service Actions - Compare and Comply" caption-side="top"}
{: #roles-table15}
{: tab-title="Actions"}
{: tab-group="Compare and Comply"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Consult with IBM Garage
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 16. Service Roles - Consult with IBM Garage" caption-side="top"}
{: #roles-table16}
{: tab-title="Roles"}
{: tab-group="Consult with IBM Garage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| consult-with-icg-wes.dashboard.view |  | Administrator, Editor, Manager, Operator, Reader, Viewer, Writer |
{: row-headers}
{: caption="Table 16. Service Actions - Consult with IBM Garage" caption-side="top"}
{: #roles-table16}
{: tab-title="Actions"}
{: tab-group="Consult with IBM Garage"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Container Registry
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Service Configuration Reader | The ability to read services configuration for Governance management. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
{: row-headers}
{: caption="Table 17. Service Roles - Container Registry" caption-side="top"}
{: #roles-table17}
{: tab-title="Roles"}
{: tab-group="Container Registry"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| container-registry.exemption.manager | Create an exemption for a security issue. List your exemptions for security issues. Delete an exemption for a security issue. List the types of security issues that you can exempt. | Manager |
| container-registry.image.push | Push a container image. Sign a container image. Import IBM software that is downloaded from IBM Passport Advantage Online. Restore a deleted container image from the trash. Create a new container image that refers to a source image. | Manager, Writer |
| container-registry.image.pull | Pull a container image. Inspect the signature for a container image. Create a new image that refers to a source image. | Manager, Reader, Writer |
| container-registry.namespace.create | Add a namespace. | Manager, Writer |
| container-registry.namespace.delete | Remove a namespace. | Manager, Writer |
| container-registry.image.delete | Delete one or more container images. Remove a tag, or tags, from each specified container image in IBM Cloud Container Registry. Delete the signature for a container image. Clean up your namespaces by retaining only images that meet your criteria. Set a policy to clean up your namespaces by retaining only container images that meet your criteria. | Manager, Writer |
| container-registry.namespace.list | List your namespaces. | Manager, Reader |
| container-registry.image.list | List your container images. Display the container images that are in the trash. | Manager, Reader, Service Configuration Reader |
| container-registry.image.vulnerabilities | View a vulnerability assessment report for your container image. | Manager, Reader, Service Configuration Reader |
| container-registry.image.inspect | Display details about a specific container image. | Manager, Reader |
| container-registry.image.build | Build a container image. | Manager, Writer |
| container-registry.quota.get | Display your current quotas for traffic and storage, and usage information against those quotas. | Manager, Reader, Writer |
| container-registry.quota.set | Modify the specified quota. | Manager |
| container-registry.plan.get | Display your pricing plan. | Manager |
| container-registry.plan.set | Upgrade to the standard plan. | Manager |
| container-registry.registrytoken.get | Retrieve the specified token from the registry. | Administrator |
| container-registry.registrytoken.delete | Remove one or more specified tokens. | Administrator |
| container-registry.registrytoken.bulkdelete | Delete multiple registry tokens. | Administrator |
| container-registry.registrytoken.list | Display all tokens that exist for your IBM Cloud account. | Administrator |
| container-registry.auth.set | Enable IAM policy enforcement. | Manager |
| container-registry.retention.analyze | Clean up your namespaces by retaining only container images that meet your criteria. Set a policy to clean up your namespaces by retaining only container images that meet your criteria. | Manager, Reader |
| container-registry.retention.get | Get an image retention policy. | Manager, Reader |
| container-registry.retention.set | Set a policy to clean up your namespaces by retaining only container images that meet your criteria. | Manager, Writer |
| container-registry.retention.list | List the image retention policies for your account. | Manager, Reader |
{: row-headers}
{: caption="Table 17. Service Actions - Container Registry" caption-side="top"}
{: #roles-table17}
{: tab-title="Actions"}
{: tab-group="Container Registry"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Continuous Delivery
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can view instances of the Continuous Delivery service. |
| Administrator | As an administrator, you can modify the Authorized Users list. |
| Editor | As an editor, you can create, view, update, change the plan for, and delete instances of the Continuous Delivery service. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 18. Service Roles - Continuous Delivery" caption-side="top"}
{: #roles-table18}
{: tab-title="Roles"}
{: tab-group="Continuous Delivery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| continuous-delivery.dashboard.view | View instances of the Continuous Delivery service. | Administrator, Editor, Operator |
| continuous-delivery.instance.add-auth-users | Add entries to the Authorized Users list on the Manage tab of a Continuous Delivery service instance. | Administrator, Manager, Writer |
| continuous-delivery.instance.remove-auth-users | Remove entries from the Authorized Users list on the Manage tab of a Continuous Delivery service instance. | Administrator, Manager, Writer |
| continuous-delivery.instance.config-auth-users | Configure authorized users. | Administrator, Manager |
{: row-headers}
{: caption="Table 18. Service Actions - Continuous Delivery" caption-side="top"}
{: #roles-table18}
{: tab-title="Actions"}
{: tab-group="Continuous Delivery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## DNS Services
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 19. Service Roles - DNS Services" caption-side="top"}
{: #roles-table19}
{: tab-title="Roles"}
{: tab-group="DNS Services"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| dns-svcs.dashboard.view |  | Administrator, Editor, Operator |
| dns-svcs.zones.read |  | Manager, Reader, Writer |
| dns-svcs.zones.update |  | Manager, Writer |
| dns-svcs.zones.manage |  | Manager |
| dns-svcs.resource-records.manage |  | Manager |
| dns-svcs.resource-records.update |  | Manager, Writer |
| dns-svcs.resource-records.read |  | Manager, Reader, Writer |
| dns-svcs.acls.manage |  | Manager |
| dns-svcs.acls.update |  | Manager, Writer |
| dns-svcs.acls.read |  | Manager, Reader, Writer |
| dns-svcs.permitted-networks.manage |  | Manager |
| dns-svcs.permitted-networks.update |  | Manager, Writer |
| dns-svcs.permitted-networks.read |  | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 19. Service Actions - DNS Services" caption-side="top"}
{: #roles-table19}
{: tab-title="Actions"}
{: tab-group="DNS Services"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Db2
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 20. Service Roles - Db2" caption-side="top"}
{: #roles-table20}
{: tab-title="Roles"}
{: tab-group="Db2"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| dashdb-for-transactions.console.access | Allows users to view the Db2 Console. | Manager |
| dashdb-for-transactions.console.manage-users | Allows management of users for database access such as creating new users or assign and IAM user or service id to a database user. | Administrator, Manager |
| dashdb-for-transactions.console.monitor | Allows viewing of metrics and information that allow you to understand the resources your database is using or workload it is running. | Administrator, Editor, Operator, Viewer |
| dashdb-for-transactions.console.scale | scale operation | Administrator, Editor, Operator |
| dashdb-for-transactions.console.backup | backup operation | Administrator, Editor, Operator |
| dashdb-for-transactions.console.restore | restore operation | Administrator, Editor, Operator |
| dashdb-for-transactions.console.settings | set configuration | Administrator, Editor, Operator |
| dashdb-for-transactions.console.view-settings | view database settings | Administrator, Editor, Operator, Viewer |
| GET /v4/:platform/deployables | Read Deployables | Administrator, Editor, Operator, Viewer |
| GET /v4/:platform/regions | Read discover available regions | Administrator, Editor, Operator, Viewer |
| GET /v4/:platform/tasks/:task_id | Read a Task | Administrator, Editor, Operator, Viewer |
| GET /v4/:platform/backups/:backup_id | Read a backup | Administrator, Editor, Operator, Viewer |
| GET /v4/:platform/deployments/:deployment_id | Read a Deployment | Administrator, Editor, Operator, Viewer |
| PATCH /v4/:platform/deployments/:deployment_id | Update a Deployment | Administrator, Editor, Operator |
| GET /v4/:platform/deployables/:deployable_id/groups | Read deployable group | Administrator, Editor, Operator, Viewer |
| GET /v4/:platform/deployments/:deployment_id/point_in_time_recovery_data | Read all deployment point-in-time-recovery data | Administrator, Editor, Operator, Viewer |
| GET /v4/:platform/deployments/:deployment_id/tasks | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| GET /v4/:platform/deployments/:deployment_id/backups | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| POST /v4/:platform/deployments/:deployment_id/backups | Create an on-demand backup | Administrator, Editor, Operator |
| GET /v4/:platform/deployments/:deployment_id/remotes | Read all deployment remotes | Administrator, Editor, Operator, Viewer |
| DELETE /v4/:platform/deployments/:deployment_id/management/database_connections | Kill all database connections | Administrator, Editor, Operator |
| PATCH /v4/:platform/deployments/:deployment_id/configuration | Update deployment configuration | Administrator, Editor, Operator |
| GET /v4/:platform/deployments/:deployment_id/configuration/schema | Read deployment configuration schema | Administrator, Editor, Operator, Viewer |
| GET /v4/:platform/deployments/:deployment_id/groups | Read Groups | Administrator, Editor, Operator, Viewer |
| PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id | Update a group | Administrator, Editor, Operator |
| POST /v4/:platform/deployments/:deployment_id/users | Create a Db2 database user | Administrator |
| GET /v4/:platform/deployments/:deployment_id/users/:user_id | Read a Db2 database user | Administrator, Editor, Operator, Viewer |
| PATCH /v4/:platform/deployments/:deployment_id/users/:user_id | Update a Db2 database user | Administrator |
| DELETE /v4/:platform/deployments/:deployment_id/users/:user_id | Remove a Db2 database user | Administrator |
| GET /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling | Read autoscaling configuration | Administrator, Editor, Operator, Viewer |
| PATCH /v4/:platform/deployments/:deployment_id/groups/:group_id/autoscaling | Update autoscaling configuration | Administrator, Editor, Operator |
| GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| GET /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type | Read deployment user connections | Administrator, Editor, Operator, Viewer |
| POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections | Create deployment user connection | Administrator, Editor, Operator, Viewer |
| POST /v4/:platform/deployments/:deployment_id/users/:user_id/connections/:endpoint_type | Create deployment user connection | Administrator, Editor, Operator, Viewer |
| GET /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses | Read whitelisted IP addresses | Administrator, Editor, Operator, Viewer |
| POST /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses | Create whitelisted IP addresses | Administrator, Editor, Operator |
| DELETE /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses/:ip_address_id | Remove a whitelisted IP address | Administrator, Editor, Operator |
| PUT /v4/:platform/deployments/:deployment_id/whitelists/ip_addresses | Bulk add whitelist IP addresses | Administrator, Editor, Operator |
| GET /2017-12/:platform/tasks/:task_id | Read a task | Administrator, Editor, Operator, Viewer |
| GET /2017-12/:platform/backups/:backup_id | Read a backup | Administrator, Editor, Operator, Viewer |
| GET /2017-12/:platform/deployments/:deployment_id | Read a deployment | Administrator, Editor, Operator, Viewer |
| DELETE /2017-12/:platform/deployments/:deployment_id | Remove a deployment | Administrator, Editor, Operator |
| GET /2017-12/:platform/deployments/:deployment_id/tasks | Read all deployment tasks | Administrator, Editor, Operator, Viewer |
| GET /2017-12/:platform/deployments/:deployment_id/backups | Read all deployment backups | Administrator, Editor, Operator, Viewer |
| POST /2017-12/:platform/clusters/:cluster_id/deployments | Create a deployment | Administrator, Editor, Operator |
| POST /v4/:platform/deployments/:deployment_id/inplace_restores | Perform in place database restore | Administrator, Editor, Operator |
| PATCH /v4/:platform/deployments/:deployment_id/groups/member | Update scaling member configuration | Administrator, Editor, Operator |
| PATCH /v4/:platform/deployments/:deployment_id/users/:user_id/adminpassword | Update admin password | Administrator, Editor, Operator |
| PATCH /v4/:platform/deployments/:deployment_id/users/:user_id/locked | Update user locked state | Administrator, Editor, Operator |
| POST /v4/:platform/deployments/:deployment_id/describe_updates | Get db updates | Administrator, Editor, Operator, Viewer |
| POST /v4/:platform/deployments/:deployment_id/db_updates | Create db update | Administrator, Editor, Operator |
| PATCH /v4/:platform/deployments/:deployment_id/users/:user_id/password | Update password | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 20. Service Actions - Db2" caption-side="top"}
{: #roles-table20}
{: tab-title="Actions"}
{: tab-group="Db2"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Db2 Warehouse
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 21. Service Roles - Db2 Warehouse" caption-side="top"}
{: #roles-table21}
{: tab-title="Roles"}
{: tab-group="Db2 Warehouse"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| dashdb.console.access |  | Manager, Writer |
{: row-headers}
{: caption="Table 21. Service Actions - Db2 Warehouse" caption-side="top"}
{: #roles-table21}
{: tab-title="Actions"}
{: tab-group="Db2 Warehouse"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Direct Link
No supported roles.
{: row-headers}
{: caption="Table 22. Service Roles - Direct Link" caption-side="top"}
{: #roles-table22}
{: tab-title="Roles"}
{: tab-group="Direct Link"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

No supported actions.
{: row-headers}
{: caption="Table 22. Service Actions - Direct Link" caption-side="top"}
{: #roles-table22}
{: tab-title="Actions"}
{: tab-group="Direct Link"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Direct Link Dedicated
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 23. Service Roles - Direct Link Dedicated" caption-side="top"}
{: #roles-table23}
{: tab-title="Roles"}
{: tab-group="Direct Link Dedicated"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| directlink.dedicated.view | View | Administrator, Editor, Operator, Viewer |
| directlink.dedicated.edit | Edit | Administrator, Editor |
{: row-headers}
{: caption="Table 23. Service Actions - Direct Link Dedicated" caption-side="top"}
{: #roles-table23}
{: tab-title="Actions"}
{: tab-group="Direct Link Dedicated"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Discovery
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 24. Service Roles - Discovery" caption-side="top"}
{: #roles-table24}
{: tab-title="Roles"}
{: tab-group="Discovery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| PUT /discovery | Update existing resources | Manager, Writer |
| POST /discovery | Create new resources | Manager, Writer |
| DELETE /discovery | Delete resources | Manager, Writer |
| PATCH /discovery | Make partial update to resources | Manager, Writer |
| GET /discovery | Retrieve resources | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 24. Service Actions - Discovery" caption-side="top"}
{: #roles-table24}
{: tab-title="Actions"}
{: tab-group="Discovery"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## ElephantSQL
| Role | Description |
| ----- | :----- |
| Operator | Operator |
| Administrator | Administrator |
| Editor | Editor |
{: row-headers}
{: caption="Table 25. Service Roles - ElephantSQL" caption-side="top"}
{: #roles-table25}
{: tab-title="Roles"}
{: tab-group="ElephantSQL"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| esql.dashboard.view |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 25. Service Actions - ElephantSQL" caption-side="top"}
{: #roles-table25}
{: tab-title="Actions"}
{: tab-group="ElephantSQL"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Enterprise
| Role | Description |
| ----- | :----- |
| Administrator | Administrators can update the enterprise, create accounts and account groups, move accounts between account groups, import existing accounts, and view usage reports. |
| Editor | Editors can update the enterprise, create accounts and account groups, view usage reports, and import accounts. |
| Operator | Operators can view the enterprise, account groups, and accounts. |
| Viewer | Viewers can view the enterprise, account groups, and accounts. |
| Usage Report Viewer | Usage report viewers can view the usage reports for the entire enterprise, an account group and its accounts, or a specific account. |
{: row-headers}
{: caption="Table 26. Service Roles - Enterprise" caption-side="top"}
{: #roles-table26}
{: tab-title="Roles"}
{: tab-group="Enterprise"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| enterprise.enterprise.create |  | Administrator |
| enterprise.enterprise.update |  | Administrator, Editor |
| enterprise.enterprise.retrieve |  | Administrator, Editor, Operator, Usage Report Viewer, Viewer |
| enterprise.enterprise.import |  | Administrator, Editor |
| enterprise.enterprise.system-update |  |  |
| enterprise.enterprise.retrieve-usage-report |  | Administrator, Editor, Usage Report Viewer |
| enterprise.enterprise.attach-config-rules |  | Administrator |
| enterprise.enterprise.detach-config-rules |  | Administrator |
| enterprise.enterprise.update-config-rules |  | Administrator |
| enterprise.account-group.create |  | Administrator, Editor |
| enterprise.account-group.update |  | Administrator, Editor |
| enterprise.account-group.retrieve |  | Administrator, Editor, Operator, Usage Report Viewer, Viewer |
| enterprise.account-group.retrieve-usage-report |  | Administrator, Editor, Usage Report Viewer |
| enterprise.account-group.attach-config-rules |  | Administrator |
| enterprise.account-group.detach-config-rules |  | Administrator |
| enterprise.account-group.update-config-rules |  | Administrator |
| enterprise.account.create |  | Administrator, Editor |
| enterprise.account.update |  | Administrator, Editor |
| enterprise.account.move |  | Administrator |
| enterprise.account.retrieve |  | Administrator, Editor, Operator, Usage Report Viewer, Viewer |
| enterprise.account.retrieve-usage-report |  | Administrator, Editor, Usage Report Viewer |
| enterprise.account.attach-config-rules |  | Administrator |
| enterprise.account.detach-config-rules |  | Administrator |
| enterprise.account.update-config-rules |  | Administrator |
{: row-headers}
{: caption="Table 26. Service Actions - Enterprise" caption-side="top"}
{: #roles-table26}
{: tab-title="Actions"}
{: tab-group="Enterprise"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Event Streams
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 27. Service Roles - Event Streams" caption-side="top"}
{: #roles-table27}
{: tab-title="Roles"}
{: tab-group="Event Streams"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| messagehub.topic.read | Allow an app to read messages from all topics, or if applied to a named topic, then just that single topic. | Manager, Reader, Writer |
| messagehub.topic.write | Allow an app to write messages to all topics, or if applied to a named topic, then just that single topic. | Manager, Writer |
| messagehub.topic.manage | Allow an app or user to create or delete topic. If applied to a named topic, then only topics of that name can be created or deleted. | Manager |
| messagehub.cluster.read | Allow an app to connect to a service instance and read its state, including listing consumer groups, topics and offsets and describing consumer groups, topics and broker configurations. | Manager, Reader, Writer |
| messagehub.group.read | Allow an app to join and commit offsets in a consumer group. | Manager, Reader, Writer |
| messagehub.group.manage | Allow an app or user to delete a Consumer Group. If applied to a group ID, then only the consumer group with that ID can be deleted. | Manager |
| messagehub.txnid.write | Allow an app to produce messages transactionally. | Manager, Writer |
| messagehub.schema.read | Read a schema/schema version | Manager, Reader, Writer |
| messagehub.schema.write | Create a schema/schema version | Manager, Writer |
| messagehub.schema.manage | Delete a schema/schema version | Manager |
| messagehub.cluster.manage | Manage the configuration of an Event Streams instance | Manager |
{: row-headers}
{: caption="Table 27. Service Actions - Event Streams" caption-side="top"}
{: #roles-table27}
{: tab-title="Actions"}
{: tab-group="Event Streams"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Floating IP for VPC
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 28. Service Roles - Floating IP for VPC" caption-side="top"}
{: #roles-table28}
{: tab-title="Roles"}
{: tab-group="Floating IP for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.floating-ip.floating-ip.create |  | Administrator, Editor |
| is.floating-ip.floating-ip.delete |  | Administrator, Editor |
| is.floating-ip.floating-ip.update |  | Administrator, Editor |
| is.floating-ip.floating-ip.operate |  | Administrator, Editor, Operator |
| is.floating-ip.floating-ip.read |  | Administrator, Editor, Operator, Viewer |
| is.floating-ip.floating-ip.list |  | Administrator, Editor, Operator, Viewer |
{: row-headers}
{: caption="Table 28. Service Actions - Floating IP for VPC" caption-side="top"}
{: #roles-table28}
{: tab-title="Actions"}
{: tab-group="Floating IP for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Functions
| Role | Description |
| ----- | :----- |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 29. Service Roles - Functions" caption-side="top"}
{: #roles-table29}
{: tab-title="Roles"}
{: tab-group="Functions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| functions.namespaces.read |  | Manager, Reader, Writer |
| functions.namespaces.delete |  | Manager |
| functions.namespaces.update |  | Manager |
| functions.entities.create |  | Manager, Writer |
| functions.entities.update |  | Manager, Writer |
| functions.entities.delete |  | Manager, Writer |
| functions.entities.read |  | Manager, Reader, Writer |
| functions.entities.activate |  | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 29. Service Actions - Functions" caption-side="top"}
{: #roles-table29}
{: tab-title="Actions"}
{: tab-group="Functions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Global Resource Catalog
| Role | Description |
| ----- | :----- |
| Administrator | Administrators can change object metadata or visibility for private services added to the account and can restrict the visibility of a public service. |
| Editor | Editors can change object metadata, but can?t change visibility for private services added to the account. |
| Viewer | Viewers can view private services added to the account. |
| Operator | Operators can view private services added to the account. |
{: row-headers}
{: caption="Table 30. Service Roles - Global Resource Catalog" caption-side="top"}
{: #roles-table30}
{: tab-title="Roles"}
{: tab-group="Global Resource Catalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| globalcatalog.is.admin | Is Admin | Administrator |
| globalcatalog.is.editor | Is Editor | Editor |
| globalcatalog.is.viewer | Is Viewer | Operator, Viewer |
{: row-headers}
{: caption="Table 30. Service Actions - Global Resource Catalog" caption-side="top"}
{: #roles-table30}
{: tab-title="Actions"}
{: tab-group="Global Resource Catalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Globalization Pipeline
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 31. Service Roles - Globalization Pipeline" caption-side="top"}
{: #roles-table31}
{: tab-title="Roles"}
{: tab-group="Globalization Pipeline"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| g11n-pipeline.dashboard.view |  | Administrator, Editor, Operator |
| g11n-pipeline.user.create-user |  | Manager |
| g11n-pipeline.document.delete-document |  | Manager |
| g11n-pipeline.document-translation-request.create-translation-request |  | Manager |
| g11n-pipeline.bundle.update-resource-entry-info |  | Manager, Writer |
| g11n-pipeline.translation-request.get-translation-requests |  | Manager, Writer |
| g11n-pipeline.document.create-document |  | Manager |
| g11n-pipeline.bundle.get-resource-strings |  | Manager, Reader, Writer |
| g11n-pipeline.xliff-document.update-documents-with-xliff |  | Manager, Writer |
| g11n-pipeline.user.update-user |  | Manager |
| g11n-pipeline.bundle.update-resource-entries |  | Manager, Writer |
| g11n-pipeline.translation-request.get-tr-resource-entry-info |  | Manager, Writer |
| g11n-pipeline.xliff.update-bundles-with-xliff |  | Manager, Writer |
| g11n-pipeline.bundle.upload-resource-entries |  | Manager |
| g11n-pipeline.document.get-document-list |  | Manager, Writer |
| g11n-pipeline.document-translation-request.get-tr-document-segment-info |  | Manager, Writer |
| g11n-pipeline.xliff.get-xliff-from-tr |  | Manager, Writer |
| g11n-pipeline.document-translation-request.update-translation-request |  | Manager |
| g11n-pipeline.document-translation-request.get-document-translation-request |  | Manager, Writer |
| g11n-pipeline.config.put-translation-config |  | Manager |
| g11n-pipeline.xliff-document.get-xliff-from-document-tr |  | Manager, Writer |
| g11n-pipeline.user.get-users |  | Manager |
| g11n-pipeline.config.put-mt-service-binding |  | Manager |
| g11n-pipeline.translation-request.update-translation-request |  | Manager |
| g11n-pipeline.document-translation-request.get-document-translation-requests |  | Manager, Writer |
| g11n-pipeline.user.get-user |  | Manager, Writer |
| g11n-pipeline.document-translation-request.get-tr-document-segments |  | Manager, Writer |
| g11n-pipeline.translation-request.get-tr-resource-entries |  | Manager, Writer |
| g11n-pipeline.document-translation-request.delete-document-translation-request |  | Manager |
| g11n-pipeline.bundle.delete-bundle |  | Manager |
| g11n-pipeline.bundle.get-resource-entry-info |  | Manager, Writer |
| g11n-pipeline.bundle.get-bundle-list |  | Manager, Writer |
| g11n-pipeline.bundle.create-bundle |  | Manager |
| g11n-pipeline.bundle.get-bundle-info |  | Manager, Reader, Writer |
| g11n-pipeline.bundle.update-bundle |  | Manager |
| g11n-pipeline.translation-request.get-tr-bundle-info |  | Manager, Writer |
| g11n-pipeline.config.get-all-mt-service-bindings |  | Manager |
| g11n-pipeline.service-instance.get-service-instance-info |  | Manager, Writer |
| g11n-pipeline.xliff.get-xliff-from-bundles |  | Manager, Writer |
| g11n-pipeline.config.delete-mt-service-binding |  | Manager |
| g11n-pipeline.config.get-translation-config |  | Manager |
| g11n-pipeline.user.delete-user |  | Manager |
| g11n-pipeline.document-translation-request.get-tr-document-info |  | Manager, Writer |
| g11n-pipeline.config.get-mt-service-binding |  | Manager |
| g11n-pipeline.config.delete-translation-config |  | Manager |
| g11n-pipeline.xliff-document.get-xliff-from-documents |  | Manager, Writer |
| g11n-pipeline.config.get-all-translation-configs |  | Manager, Writer |
| g11n-pipeline.translation-request.delete-translation-request |  | Manager |
| g11n-pipeline.translation-request.get-translation-request |  | Manager, Writer |
| g11n-pipeline.translation-request.create-translation-request |  | Manager |
| g11n-pipeline.bundle.get-bundle-info-full |  | Manager, Writer |
| g11n-pipeline.bundle.get-bundle-list-all |  | Manager |
| g11n-pipeline.bundle.get-resource-strings-all |  | Manager, Writer |
| g11n-pipeline.user.get-user-all |  | Manager |
| g11n-pipeline.bundle.update-resource-strings-src |  | Manager |
| g11n-pipeline.bundle.update-resource-entry-info-src |  | Manager |
| g11n-pipeline.document.get-document-content |  | Manager, Reader, Writer |
| g11n-pipeline.document.get-document-meta-data |  | Manager, Reader, Writer |
| g11n-pipeline.document.get-document-meta-data-full |  | Manager, Writer |
| g11n-pipeline.document.get-document-segments |  | Manager, Writer |
| g11n-pipeline.document.update-document-meta-data |  | Manager |
| g11n-pipeline.document.get-segment-info |  | Manager, Writer |
| g11n-pipeline.document.upload-document-content |  | Manager |
| g11n-pipeline.document.update-segment-translation |  | Manager, Writer |
{: row-headers}
{: caption="Table 31. Service Actions - Globalization Pipeline" caption-side="top"}
{: #roles-table31}
{: tab-title="Actions"}
{: tab-group="Globalization Pipeline"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## HPCaaS from Rescale
| Role | Description |
| ----- | :----- |
| Operator | Operator |
| Administrator | Administrator |
| Editor | Editor |
{: row-headers}
{: caption="Table 32. Service Roles - HPCaaS from Rescale" caption-side="top"}
{: #roles-table32}
{: tab-title="Roles"}
{: tab-group="HPCaaS from Rescale"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| hpcaas-from-rescale-prod.dashboard.view |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 32. Service Actions - HPCaaS from Rescale" caption-side="top"}
{: #roles-table32}
{: tab-title="Actions"}
{: tab-group="HPCaaS from Rescale"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Hyper Protect Crypto Services
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 33. Service Roles - Hyper Protect Crypto Services" caption-side="top"}
{: #roles-table33}
{: tab-title="Roles"}
{: tab-group="Hyper Protect Crypto Services"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| hs-crypto.dashboard.view | View the dashboard | Administrator, Editor, Operator |
| hs-crypto.instances.read | Get Instance API endpoint info | Administrator, Editor, Manager, Reader, Viewer, Writer |
| hs-crypto.secrets.list | Retrieve a list of encryption keys. | Administrator, Editor, Manager, Reader, Viewer, Writer |
| hs-crypto.secrets.wrap | Retrieve a list of encryption keys. | Administrator, Editor, Manager, Reader, Viewer, Writer |
| hs-crypto.secrets.unwrap | Unwrap an encryption key. | Administrator, Editor, Manager, Reader, Viewer, Writer |
| hs-crypto.secrets.create | Create an encryption key. | Administrator, Editor, Manager, Writer |
| hs-crypto.secrets.read | Retrieve an encryption key. | Administrator, Editor, Manager, Writer |
| hs-crypto.secrets.delete | Delete an encryption key. | Administrator, Manager |
| hs-crypto.secrets.rotate | Rotate an encryption key. | Administrator, Editor, Manager, Writer |
| hs-crypto.instances.manage | Manage instance via TKE. | Administrator, Manager |
| hs-crypto.ep11.use | Use the GREP11 Interface for Hyper Protect Crypto Services | Administrator, Editor, Manager, Reader, Viewer, Writer |
| hs-crypto.importtoken.create | Allow creation of secure import tokens | Manager, Writer |
| hs-crypto.importtoken.read | Allow retrieval of secure import tokens | Manager, Writer |
| hs-crypto.policies.read | Retrieve policies for an encryption key | Manager |
| hs-crypto.policies.write | Set policies for an encryption key | Manager |
| hs-crypto.instancepolicies.read | Retrieve instance level policies | Manager |
| hs-crypto.instancepolicies.write | Add or update instance level policies | Manager |
| hs-crypto.secrets.setkeyfordeletion | Set or prepare an encryption key for deletion | Manager, Writer |
| hs-crypto.secrets.unsetkeyfordeletion | Unset an encryption key for deletion | Manager, Writer |
| hs-crypto.secrets.readmetadata | Retrieve the details of an encryption key | Manager, Reader, Writer |
| hs-crypto.secrets.rewrap | Rewrap an encryption key | Manager, Reader, Writer |
| hs-crypto.registrations.list | Retrieve a list of registrations | Manager, Reader, Writer |
| hs-crypto.secrets.listkeyversions | Retrieve a list of versions that are associated with an encryption key | Manager, Reader, Writer |
| hs-crypto.registrations.listforkey | Retrieve a list of registrations for a given encryption key | Manager, Reader, Writer |
| hs-crypto.registrations.deactivate | Move a suspended registration to the deactivated state | Manager, Reader, Writer |
| hs-crypto.registrations.create | Create a registration between an encryption key and a cloud resource | Manager, Reader, Writer |
| hs-crypto.registrations.write | Replace an existing registration | Manager, Reader, Writer |
| hs-crypto.registrations.merge | Update the details of an existing registration | Manager, Reader, Writer |
| hs-crypto.registrations.delete | Delete a registration | Manager, Reader, Writer |
| hs-crypto.secrets.disable | Disable operations for an encryption key | Manager |
| hs-crypto.secrets.enable | Enable operations for an encryption key | Manager |
| hs-crypto.secrets.restore | Restore a previously deleted encryption key | Manager |
| hs-crypto.secrets.eventack | Acknowledge a key lifecycle event | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 33. Service Actions - Hyper Protect Crypto Services" caption-side="top"}
{: #roles-table33}
{: tab-title="Actions"}
{: tab-group="Hyper Protect Crypto Services"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Hyper Protect DBaaS for MongoDB
| Role | Description |
| ----- | :----- |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 34. Service Roles - Hyper Protect DBaaS for MongoDB" caption-side="top"}
{: #roles-table34}
{: tab-title="Roles"}
{: tab-group="Hyper Protect DBaaS for MongoDB"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| hyperp-dbaas-mongodb.clusters.read | Get the detailed information about a database cluster | Manager, Reader, Writer |
| hyperp-dbaas-mongodb.logging.enable | Enable sending database logs and audit logs to the user's service instance of IBM Log Analysis with LogDNA | Manager, Writer |
| hyperp-dbaas-mongodb.monitoring.enable | Enable sending database metrics to a user-specified organization and space in the IBM Cloud Monitoring service | Manager, Writer |
| hyperp-dbaas-mongodb.users.list | List all database users | Manager, Reader, Writer |
| hyperp-dbaas-mongodb.users.read | Get the detailed information about a database user | Manager, Reader, Writer |
| hyperp-dbaas-mongodb.databases.list | List all databases | Manager, Reader, Writer |
| hyperp-dbaas-mongodb.logs.list | List database log files and audit log files | Manager, Reader, Writer |
| hyperp-dbaas-mongodb.logs.read | Download a database log file or an audit log file | Manager |
{: row-headers}
{: caption="Table 34. Service Actions - Hyper Protect DBaaS for MongoDB" caption-side="top"}
{: #roles-table34}
{: tab-title="Actions"}
{: tab-group="Hyper Protect DBaaS for MongoDB"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Hyper Protect DBaaS for PostgreSQL
| Role | Description |
| ----- | :----- |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 35. Service Roles - Hyper Protect DBaaS for PostgreSQL" caption-side="top"}
{: #roles-table35}
{: tab-title="Roles"}
{: tab-group="Hyper Protect DBaaS for PostgreSQL"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| hyperp-dbaas-postgresql.clusters.read | Get the detailed information about a database cluster | Manager, Reader, Writer |
| hyperp-dbaas-postgresql.logging.enable | Enable sending database logs and audit logs to the user's service instance of IBM Log Analysis with LogDNA | Manager, Writer |
| hyperp-dbaas-postgresql.monitoring.enable | Enable sending database metrics to a user-specified organization and space in the IBM Cloud Monitoring service | Manager, Writer |
| hyperp-dbaas-postgresql.users.list | List all database users | Manager, Reader, Writer |
| hyperp-dbaas-postgresql.users.read | Get the detailed information about a database user | Manager, Reader, Writer |
| hyperp-dbaas-postgresql.databases.list | List all databases | Manager, Reader, Writer |
| hyperp-dbaas-postgresql.logs.list | List database log files and audit log files | Manager, Reader, Writer |
| hyperp-dbaas-postgresql.logs.read | Download a database log file or an audit log file | Manager |
{: row-headers}
{: caption="Table 35. Service Actions - Hyper Protect DBaaS for PostgreSQL" caption-side="top"}
{: #roles-table35}
{: tab-title="Actions"}
{: tab-group="Hyper Protect DBaaS for PostgreSQL"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Hyper Protect Virtual Server
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 36. Service Roles - Hyper Protect Virtual Server" caption-side="top"}
{: #roles-table36}
{: tab-title="Roles"}
{: tab-group="Hyper Protect Virtual Server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| hpvs.dashboard.view |  | Administrator, Editor, Manager, Operator, Reader, Writer |
{: row-headers}
{: caption="Table 36. Service Actions - Hyper Protect Virtual Server" caption-side="top"}
{: #roles-table36}
{: tab-title="Actions"}
{: tab-group="Hyper Protect Virtual Server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## IAM Access Groups Service
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can view, create, edit, and delete access groups including adding or removing users from the groups. You can also assign access to the group and manage access for others to work with access groups. |
| Editor | As an editor, you can view, create, edit, and delete access groups including adding or removing users from the groups. |
| Viewer | As a viewer, you can view access groups and its members. |
| Service Configuration Reader | The ability to read services configuration for Governance management. |
{: row-headers}
{: caption="Table 37. Service Roles - IAM Access Groups Service" caption-side="top"}
{: #roles-table37}
{: tab-title="Roles"}
{: tab-group="IAM Access Groups Service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| iam-groups.groups.create | Create an access group | Administrator, Editor |
| iam-groups.groups.read | Get an access group | Administrator, Editor, Viewer |
| iam-groups.groups.update | Update an access group | Administrator, Editor |
| iam-groups.groups.delete | Delete an access group | Administrator, Editor |
| iam-groups.groups.list | List access groups | Administrator, Editor, Viewer |
| iam-groups.members.add | Add members to an access group | Administrator, Editor |
| iam-groups.members.read | Check membership in an access group | Administrator, Editor, Viewer |
| iam-groups.members.delete | Delete member from an access group | Administrator, Editor |
| iam-groups.members.list | List access group members | Administrator, Editor, Viewer |
| iam-groups.rules.create | Create rule for an access group | Administrator, Editor |
| iam-groups.rules.read | Get an access group rule | Administrator, Editor, Viewer |
| iam-groups.rules.update | Update an access group rule | Administrator, Editor |
| iam-groups.rules.delete | Delete an access group rule | Administrator, Editor |
| iam-groups.rules.list | List access group rules | Administrator, Editor, Viewer |
| iam-groups.groups.audit | View access groups audit data | Administrator, Editor, Viewer |
| iam-groups.account-settings.read | View access groups account settings | Administrator, Editor, Viewer |
| iam-groups.account-settings.update | Update access groups account settings | Administrator |
{: row-headers}
{: caption="Table 37. Service Actions - IAM Access Groups Service" caption-side="top"}
{: #roles-table37}
{: tab-title="Actions"}
{: tab-group="IAM Access Groups Service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## IAM Identity Service
| Role | Description |
| ----- | :----- |
| Viewer | A Viewer can view service IDs and API keys. |
| Editor | An Editor can view and update service IDs and API keys. |
| Administrator | An Administrator can view, update and delete service IDs and API keys. |
| Operator | An Operator can view, update and delete service IDs and API keys. |
{: row-headers}
{: caption="Table 38. Service Roles - IAM Identity Service" caption-side="top"}
{: #roles-table38}
{: tab-title="Roles"}
{: tab-group="IAM Identity Service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| iam-identity.serviceid.get | Get the details of an existing service ID. | Administrator, Editor, Operator, Viewer |
| iam-identity.serviceid.create | Create a new service ID. | Administrator, Operator |
| iam-identity.serviceid.update | Update the details of an existing service ID. | Administrator, Editor, Operator |
| iam-identity.serviceid.delete | Delete a service ID. | Administrator, Operator |
| iam-identity.apikey.manage | actiondescription.iam-identity.apikey.manage | Administrator |
| iam-identity.apikey.get | Get the details of an existing API key. | Administrator, Editor, Operator |
| iam-identity.apikey.list | List API keys based on properties. | Administrator, Editor, Operator |
| iam-identity.apikey.create | Create a new API key. | Administrator, Operator |
| iam-identity.apikey.update | Update the details of an existing API key. | Administrator, Editor, Operator |
| iam-identity.apikey.delete | Delete an API key. | Administrator, Operator |
| iam-identity.idp.get | actiondescription.iam-identity.idp.get | Administrator, Editor, Operator |
| iam-identity.idp.list | actiondescription.iam-identity.idp.list | Administrator, Editor, Operator |
| iam-identity.idp.create | actiondescription.iam-identity.idp.create | Administrator, Operator |
| iam-identity.idp.update | actiondescription.iam-identity.idp.update | Administrator, Editor, Operator |
| iam-identity.idp.delete | actiondescription.iam-identity.idp.delete | Administrator, Operator |
| iam-identity.idp.test | actiondescription.iam-identity.idp.test | Administrator, Editor, Operator |
| iam-identity.account.get | actiondescription.iam-identity.account.get | Administrator, Editor, Operator |
| iam-identity.account.create | actiondescription.iam-identity.account.create | Administrator, Operator |
| iam-identity.account.update | actiondescription.iam-identity.account.update | Administrator, Editor, Operator |
| iam-identity.account.enable_idp | actiondescription.iam-identity.account.enable_idp | Administrator, Editor, Operator |
| iam-identity.account.disable_idp | actiondescription.iam-identity.account.disable_idp | Administrator, Editor, Operator |
| iam-identity.account.delete | actiondescription.iam-identity.account.delete | Administrator, Operator |
{: row-headers}
{: caption="Table 38. Service Actions - IAM Identity Service" caption-side="top"}
{: #roles-table38}
{: tab-title="Actions"}
{: tab-group="IAM Identity Service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## IBM Cloud Activity Tracker with LogDNA
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you can manage resources, configure views, dashboards and alerts, export data, search, filter, and view all data. |
| Reader | As a reader, you can perform read-only actions such as monitor data through views and dashboards. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Standard member | As a member, you can configure views, dashboards and alerts, export data, search, filter, and view all data. |
{: row-headers}
{: caption="Table 39. Service Roles - IBM Cloud Activity Tracker with LogDNA" caption-side="top"}
{: #roles-table39}
{: tab-title="Roles"}
{: tab-group="IBM Cloud Activity Tracker with LogDNA"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| logdnaat.dashboard.view | View LogDNA Dashboard | Administrator, Manager, Reader, Standard member |
| logdnaat.dashboard.read | Access LogDNA dashboard without any edit permission | Reader |
| logdnaat.dashboard.member | Access LogDNA dashboard with limited edit capabilities | Standard member |
| logdnaat.dashboard.manage | Access and manage LogDNA dashboard without any limitation | Administrator, Manager |
{: row-headers}
{: caption="Table 39. Service Actions - IBM Cloud Activity Tracker with LogDNA" caption-side="top"}
{: #roles-table39}
{: tab-title="Actions"}
{: tab-group="IBM Cloud Activity Tracker with LogDNA"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## IBM Cloud Data Shield
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 40. Service Roles - IBM Cloud Data Shield" caption-side="top"}
{: #roles-table40}
{: tab-title="Roles"}
{: tab-group="IBM Cloud Data Shield"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| data-shield.dashboard.view |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 40. Service Actions - IBM Cloud Data Shield" caption-side="top"}
{: #roles-table40}
{: tab-title="Actions"}
{: tab-group="IBM Cloud Data Shield"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## IBM Cloud Monitoring with Sysdig
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 41. Service Roles - IBM Cloud Monitoring with Sysdig" caption-side="top"}
{: #roles-table41}
{: tab-title="Roles"}
{: tab-group="IBM Cloud Monitoring with Sysdig"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| sysdig-monitor.launch.viewer |  | Administrator, Manager, Reader, Writer |
| sysdig-monitor.launch.user |  | Administrator, Manager, Writer |
| sysdig-monitor.launch.admin |  | Administrator, Manager |
{: row-headers}
{: caption="Table 41. Service Actions - IBM Cloud Monitoring with Sysdig" caption-side="top"}
{: #roles-table41}
{: tab-title="Actions"}
{: tab-group="IBM Cloud Monitoring with Sysdig"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## IBM Cognos Dashboard Embedded
| Role | Description |
| ----- | :----- |
| Manager | Manager |
| Reader | Reader |
| Writer | Writer |
{: row-headers}
{: caption="Table 42. Service Roles - IBM Cognos Dashboard Embedded" caption-side="top"}
{: #roles-table42}
{: tab-title="Roles"}
{: tab-group="IBM Cognos Dashboard Embedded"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| dynamic-dashboard-embedded.instances.write |  | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 42. Service Actions - IBM Cognos Dashboard Embedded" caption-side="top"}
{: #roles-table42}
{: tab-title="Actions"}
{: tab-group="IBM Cognos Dashboard Embedded"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## IBM Log Analysis with LogDNA
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you can manage resources, configure views, dashboards and alerts, export data, search, filter, and view all data. |
| Reader | As a reader, you can perform read-only actions such as monitor data through views and dashboards. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Standard Member | As a member, you can configure views, dashboards and alerts, export data, search, filter, and view all data. |
{: row-headers}
{: caption="Table 43. Service Roles - IBM Log Analysis with LogDNA" caption-side="top"}
{: #roles-table43}
{: tab-title="Roles"}
{: tab-group="IBM Log Analysis with LogDNA"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| logdna.dashboard.view | View LogDNA Dashboard | Administrator, Manager, Reader, Standard Member |
| logdna.dashboard.read | Access LogDNA dashboard without any edit permission | Reader |
| logdna.dashboard.member | Access LogDNA dashboard with limited edit capabilities | Standard Member |
| logdna.dashboard.manage | Access and manage LogDNA dashboard without any limitation | Administrator, Manager |
{: row-headers}
{: caption="Table 43. Service Actions - IBM Log Analysis with LogDNA" caption-side="top"}
{: #roles-table43}
{: tab-title="Actions"}
{: tab-group="IBM Log Analysis with LogDNA"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Image Service for VPC
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 44. Service Roles - Image Service for VPC" caption-side="top"}
{: #roles-table44}
{: tab-title="Roles"}
{: tab-group="Image Service for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.image.image.list |  | Administrator, Editor, Operator, Viewer |
| is.image.image.read |  | Administrator, Editor, Operator, Viewer |
| is.image.image.create |  | Administrator, Editor |
| is.image.image.update |  | Administrator, Editor |
| is.image.image.delete |  | Administrator, Editor |
| is.image.image.provision |  | Administrator, Editor, Operator |
| is.image.image.operate | Operate on Custom Images | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 44. Service Actions - Image Service for VPC" caption-side="top"}
{: #roles-table44}
{: tab-title="Actions"}
{: tab-group="Image Service for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Infrastructure Service
No supported roles.
{: row-headers}
{: caption="Table 45. Service Roles - Infrastructure Service" caption-side="top"}
{: #roles-table45}
{: tab-title="Roles"}
{: tab-group="Infrastructure Service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

No supported actions.
{: row-headers}
{: caption="Table 45. Service Actions - Infrastructure Service" caption-side="top"}
{: #roles-table45}
{: tab-title="Actions"}
{: tab-group="Infrastructure Service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Internet Services
| Role | Description |
| ----- | :----- |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Service Configuration Reader | The ability to read services configuration for Governance management. |
{: row-headers}
{: caption="Table 46. Service Roles - Internet Services" caption-side="top"}
{: #roles-table46}
{: tab-title="Roles"}
{: tab-group="Internet Services"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| internet-svcs.zones.read | View all zone settings but can't modify them. | Manager, Reader, Service Configuration Reader, Writer |
| internet-svcs.zones.update | Modify all zone settings but can't create or delete them. | Manager, Writer |
| internet-svcs.zones.manage | View, Modify, Create, and Delete all zone settings. | Manager |
| internet-svcs.reliability.read | View all Reliability settings but can't modify them. | Manager, Reader, Service Configuration Reader, Writer |
| internet-svcs.reliability.update | Modify all Reliability settings except for pools and monitors. | Manager, Writer |
| internet-svcs.reliability.manage | View, Modify, Create, and Delete all Reliability settings except for pools and monitors. | Manager |
| internet-svcs.security.read | View all Security settings except for instance level firewall rules. | Manager, Reader, Service Configuration Reader, Writer |
| internet-svcs.security.update | Modify all Security settings except for instance level firewall rules. | Manager, Writer |
| internet-svcs.security.manage | View, Modify, Create, and Delete all Security settings except for instance level firewall rules. | Manager |
| internet-svcs.performance.read | View all Performance settings but can't modify them. | Manager, Reader, Service Configuration Reader, Writer |
| internet-svcs.performance.update | Modify all Performance settings but cannot create or delete. | Manager, Writer |
| internet-svcs.performance.manage | View, Modify, Create, and Delete all Performance settings. | Manager |
{: row-headers}
{: caption="Table 46. Service Actions - Internet Services" caption-side="top"}
{: #roles-table46}
{: tab-title="Actions"}
{: tab-group="Internet Services"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Internet of Things Platform
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 47. Service Roles - Internet of Things Platform" caption-side="top"}
{: #roles-table47}
{: tab-title="Roles"}
{: tab-group="Internet of Things Platform"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| iotf-service.dashboard.view |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 47. Service Actions - Internet of Things Platform" caption-side="top"}
{: #roles-table47}
{: tab-title="Actions"}
{: tab-group="Internet of Things Platform"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Key Protect
| Role | Description |
| ----- | :----- |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| ReaderPlus | As a reader plus, you can perform read-only actions within Key Protect such as viewing service-specific resources. You can also access key material for standard keys. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 48. Service Roles - Key Protect" caption-side="top"}
{: #roles-table48}
{: tab-title="Roles"}
{: tab-group="Key Protect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| kms.secrets.create | Create an encryption key. | Manager, Writer |
| kms.secrets.read | Retrieve an encryption key. | Manager, ReaderPlus, Writer |
| kms.secrets.list | Retrieve a list of encryption keys. | Manager, Reader, ReaderPlus, Writer |
| kms.secrets.delete | Delete an encryption key. | Manager |
| kms.secrets.wrap | Unwrap an encryption key. | Manager, Reader, ReaderPlus, Writer |
| kms.secrets.unwrap | Wrap an encryption key. | Manager, Reader, ReaderPlus, Writer |
| kms.secrets.rotate | Rotate an encryption key. | Manager, Writer |
| kms.lockers.read | Read lockers | Manager, Writer |
| kms.lockers.create | Create lockers | Manager, Writer |
| kms.lockers.list | List lockers | Manager, Writer |
| kms.policies.read | Retrieve policies for an encryption key. | Manager |
| kms.policies.write | Set policies for an encryption key. | Manager |
| kms.secrets.rewrap | Rewrap an encryption key. | Manager, Reader, ReaderPlus, Writer |
| kms.importtoken.read | Retrieve an import token. | Manager, Writer |
| kms.importtoken.create | Create an import token. | Manager, Writer |
| kms.registrations.list | Retrieve a list of registrations. | Manager, Reader, ReaderPlus, Writer |
| kms.registrations.listforkey | Retrieve a list of registrations for a given encryption key. | Manager, Reader, ReaderPlus, Writer |
| kms.registrations.delete | Delete a registration. | Manager, Reader, ReaderPlus, Writer |
| kms.registrations.merge | Update the details of an existing registration. | Manager, Reader, ReaderPlus, Writer |
| kms.registrations.write | Replace an existing registration. | Manager, Reader, ReaderPlus, Writer |
| kms.registrations.create | Create a registration between an encryption key and a cloud resource. | Manager, Reader, ReaderPlus, Writer |
| kms.registrations.deactivate | Move a suspended registration to the deactivated state | Manager, Reader, ReaderPlus, Writer |
| kms.instancepolicies.read | Retrieve instance level policies. | Manager |
| kms.instancepolicies.write | Add or update instance level policies. | Manager |
| kms.secrets.setkeyfordeletion | Set or prepare an encryption key for deletion. | Manager, Writer |
| kms.secrets.unsetkeyfordeletion | Unset an encryption key for deletion. | Manager, Writer |
| kms.secrets.readmetadata | Retrieve the details of an encryption key. | Manager, Reader, ReaderPlus, Writer |
| kms.secrets.listkeyversions | Retrieve a list of versions that are associated with an encryption key. | Manager, Reader, ReaderPlus, Writer |
| kms.keyversions.list | Retrieve a list of versions that are associated with an encryption key. | Manager, Reader, ReaderPlus, Writer |
| kms.secrets.restore | Restore a previously deleted encryption key. | Manager |
| kms.secrets.disable | Disable operations for an encryption key. | Manager |
| kms.secrets.enable | Enable operations for an encryption key. | Manager |
| kms.secrets.eventack | Acknowledge a key lifecycle event | Manager, Reader, ReaderPlus, Writer |
{: row-headers}
{: caption="Table 48. Service Actions - Key Protect" caption-side="top"}
{: #roles-table48}
{: tab-title="Actions"}
{: tab-group="Key Protect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Knowledge Catalog
| Role | Description |
| ----- | :----- |
| Administrator | Administrator |
| Manager | Manager |
| Writer | Writer |
{: row-headers}
{: caption="Table 49. Service Roles - Knowledge Catalog" caption-side="top"}
{: #roles-table49}
{: tab-title="Roles"}
{: tab-group="Knowledge Catalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| datacatalog |  | Administrator |
| datacatalog.catalog.create |  | Administrator, Manager, Writer |
{: row-headers}
{: caption="Table 49. Service Actions - Knowledge Catalog" caption-side="top"}
{: #roles-table49}
{: tab-title="Actions"}
{: tab-group="Knowledge Catalog"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Knowledge Studio
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 50. Service Roles - Knowledge Studio" caption-side="top"}
{: #roles-table50}
{: tab-title="Roles"}
{: tab-group="Knowledge Studio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| knowledge-studio.dashboard.view |  | Administrator, Editor, Manager, Reader, Viewer, Writer |
{: row-headers}
{: caption="Table 50. Service Actions - Knowledge Studio" caption-side="top"}
{: #roles-table50}
{: tab-title="Actions"}
{: tab-group="Knowledge Studio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Kubernetes Service
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
{: row-headers}
{: caption="Table 51. Service Roles - Kubernetes Service" caption-side="top"}
{: #roles-table51}
{: tab-title="Roles"}
{: tab-group="Kubernetes Service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| containers-kubernetes.cluster.create | Users such as cluster or account administrators can create and delete clusters or set up cluster-wide features like service endpoints or managed add-ons. | Administrator |
| containers-kubernetes.cluster.read | Users such as auditors or billing can see cluster details but not modify the infrastructure. | Administrator, Editor, Operator, Viewer |
| containers-kubernetes.cluster.operate | Users such as reliability or DevOps engineers can add worker nodes and troubleshoot infrastructure such as reloading a worker node. They cannot create, delete, change credentials, or set up cluster-wide features. | Administrator, Operator |
| containers-kubernetes.cluster.update | Users such as developers can bind service, work with Ingress resources, and set up log forwarding for their apps but cannot modify the infrastructure. | Administrator, Editor |
| containers-kubernetes.kube.read | Users get read access to most Kubernetes resources in the namespace, but not to certain resources like roles, role bindings, or secrets. Corresponds to the RBAC view cluster role, which can be scoped to a namespace. | Reader |
| containers-kubernetes.kube.write | Users get read and write access to most Kubernetes resources in the namespace, but not to certain resources like roles or role bindings. Corresponds to the RBAC edit cluster role, which can be scoped to a namespace. | Writer |
| containers-kubernetes.kube.manage | When scoped to one namespace: Users can read and write to all Kubernetes resources in the namespace, but not to objects that apply across namespaces, the namespace resource quota, or the namespace itself. Corresponds to the RBAC admin cluster role to that namespace. When scoped to all namespaces in the cluster (by leaving the previous namespace field empty): Users can read and write to all Kubernetes resources in all namespaces in the cluster and work with objects that apply across namespaces, like top pods, top nodes, or creating an Ingress resource to make apps publicly available. Corresponds to the RBAC cluster-admin cluster role. | Manager |
{: row-headers}
{: caption="Table 51. Service Actions - Kubernetes Service" caption-side="top"}
{: #roles-table51}
{: tab-title="Actions"}
{: tab-group="Kubernetes Service"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Language Translator
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 52. Service Roles - Language Translator" caption-side="top"}
{: #roles-table52}
{: tab-title="Roles"}
{: tab-group="Language Translator"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| GET /language-translator |  | Manager, Reader, Writer |
| POST /language-translator |  | Manager, Reader, Writer |
| DELETE /language-translator |  | Manager, Writer |
{: row-headers}
{: caption="Table 52. Service Actions - Language Translator" caption-side="top"}
{: #roles-table52}
{: tab-title="Actions"}
{: tab-group="Language Translator"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## License and Entitlement
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 53. Service Roles - License and Entitlement" caption-side="top"}
{: #roles-table53}
{: tab-title="Roles"}
{: tab-group="License and Entitlement"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| entitlement.entitlement.write |  | Administrator, Editor |
| entitlement.entitlement.write-admin |  | Administrator |
{: row-headers}
{: caption="Table 53. Service Actions - License and Entitlement" caption-side="top"}
{: #roles-table53}
{: tab-title="Actions"}
{: tab-group="License and Entitlement"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Load Balancer for VPC
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 54. Service Roles - Load Balancer for VPC" caption-side="top"}
{: #roles-table54}
{: tab-title="Roles"}
{: tab-group="Load Balancer for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.load-balancer.load-balancer.view |  | Administrator, Editor, Viewer |
| is.load-balancer.load-balancer.manage |  | Administrator, Editor |
{: row-headers}
{: caption="Table 54. Service Actions - Load Balancer for VPC" caption-side="top"}
{: #roles-table54}
{: tab-title="Actions"}
{: tab-group="Load Balancer for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## MQ
| Role | Description |
| ----- | :----- |
| Administrator | Administrator |
| Operator | Operator |
| Editor | Editor |
| Viewer | Viewer |
| Reader | Reader |
| Writer | Writer |
| Manager | Manager |
{: row-headers}
{: caption="Table 55. Service Roles - MQ" caption-side="top"}
{: #roles-table55}
{: tab-title="Roles"}
{: tab-group="MQ"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| mqcloud.instance.use |  | Administrator, Editor, Operator, Viewer |
| mqcloud.qm.admin |  | Administrator, Manager |
| mqcloud.qm.app1 |  | Editor, Operator, Writer |
| mqcloud.qm.app2 |  | Reader, Viewer |
{: row-headers}
{: caption="Table 55. Service Actions - MQ" caption-side="top"}
{: #roles-table55}
{: tab-title="Actions"}
{: tab-group="MQ"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Machine Learning
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Writer | As a writer, you can perform all actions on the WML instance this role is being assigned. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
{: row-headers}
{: caption="Table 56. Service Roles - Machine Learning" caption-side="top"}
{: #roles-table56}
{: tab-title="Roles"}
{: tab-group="Machine Learning"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| pm-20.instances.admin |  | Administrator |
| pm-20.instances.write |  | Editor, Manager, Writer |
{: row-headers}
{: caption="Table 56. Service Actions - Machine Learning" caption-side="top"}
{: #roles-table56}
{: tab-title="Actions"}
{: tab-group="Machine Learning"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Mass Data Migration
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
{: row-headers}
{: caption="Table 57. Service Roles - Mass Data Migration" caption-side="top"}
{: #roles-table57}
{: tab-title="Roles"}
{: tab-group="Mass Data Migration"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| mass-data-migration.dashboard.view |  | Administrator, Editor, Operator |
| mass-data-migration.order.place | Can place order | Manager, Writer |
{: row-headers}
{: caption="Table 57. Service Actions - Mass Data Migration" caption-side="top"}
{: #roles-table57}
{: tab-title="Actions"}
{: tab-group="Mass Data Migration"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Mobile Foundation
No supported roles.
{: row-headers}
{: caption="Table 58. Service Roles - Mobile Foundation" caption-side="top"}
{: #roles-table58}
{: tab-title="Roles"}
{: tab-group="Mobile Foundation"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

No supported actions.
{: row-headers}
{: caption="Table 58. Service Actions - Mobile Foundation" caption-side="top"}
{: #roles-table58}
{: tab-title="Actions"}
{: tab-group="Mobile Foundation"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Monitoring
| Role | Description |
| ----- | :----- |
| Editor | Editor |
| Operator | Operator |
| Administrator | Administrator |
| Viewer | Viewer |
{: row-headers}
{: caption="Table 59. Service Roles - Monitoring" caption-side="top"}
{: #roles-table59}
{: tab-title="Roles"}
{: tab-group="Monitoring"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| monitoring.domain.write |  | Administrator, Editor, Operator |
| monitoring.domain.render |  | Administrator, Editor, Operator, Viewer |
| monitoring.domain.find |  | Administrator, Editor, Operator, Viewer |
| monitoring.domain.alarm_write |  | Administrator, Editor |
| monitoring.domain.alarm_read |  | Administrator, Editor, Viewer |
| monitoring.domain.notify_write |  | Administrator, Editor |
| monitoring.domain.notify_read |  | Administrator, Editor, Viewer |
| monitoring.domain.dashboard_write |  | Administrator, Editor, Operator |
| monitoring.domain.dashboard_read |  | Administrator, Editor, Viewer |
| monitoring.domain.uptime_write |  | Administrator, Editor |
| monitoring.domain.uptime_read |  | Administrator, Editor, Viewer |
{: row-headers}
{: caption="Table 59. Service Actions - Monitoring" caption-side="top"}
{: #roles-table59}
{: tab-title="Actions"}
{: tab-group="Monitoring"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Natural Language Classifier
| Role | Description |
| ----- | :----- |
| Manager | Manager |
| Writer | Writer |
| Reader | Reader |
| Administrator | Administrator |
| Viewer | Viewer |
| Editor | Editor |
{: row-headers}
{: caption="Table 60. Service Roles - Natural Language Classifier" caption-side="top"}
{: #roles-table60}
{: tab-title="Roles"}
{: tab-group="Natural Language Classifier"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| GET /natural-language-classifier |  | Administrator, Editor, Manager, Reader, Viewer, Writer |
| POST /natural-language-classifier |  | Administrator, Editor, Manager, Reader, Viewer, Writer |
| DELETE /natural-language-classifier |  | Administrator, Editor, Manager, Reader, Viewer, Writer |
{: row-headers}
{: caption="Table 60. Service Actions - Natural Language Classifier" caption-side="top"}
{: #roles-table60}
{: tab-title="Actions"}
{: tab-group="Natural Language Classifier"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Natural Language Understanding
| Role | Description |
| ----- | :----- |
| Operator | Operator |
| Administrator | Administrator |
| Editor | Editor |
| Manager | Manager |
| Writer | Writer |
| Reader | Reader |
{: row-headers}
{: caption="Table 61. Service Roles - Natural Language Understanding" caption-side="top"}
{: #roles-table61}
{: tab-title="Roles"}
{: tab-group="Natural Language Understanding"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| natural-language-understanding.dashboard.view |  | Administrator, Editor, Operator |
| GET /natural-language-understanding |  | Manager, Reader, Writer |
| POST /natural-language-understanding |  | Manager, Reader, Writer |
| DELETE /natural-language-understanding |  | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 61. Service Actions - Natural Language Understanding" caption-side="top"}
{: #roles-table61}
{: tab-title="Actions"}
{: tab-group="Natural Language Understanding"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Network ACL
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 62. Service Roles - Network ACL" caption-side="top"}
{: #roles-table62}
{: tab-title="Roles"}
{: tab-group="Network ACL"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.network-acl.network-acl.read |  | Administrator, Editor, Operator, Viewer |
| is.network-acl.network-acl.create |  | Administrator, Editor |
| is.network-acl.network-acl.update |  | Administrator, Editor |
| is.network-acl.network-acl.delete |  | Administrator, Editor |
| is.network-acl.network-acl.list |  | Administrator, Editor, Operator, Viewer |
| is.network-acl.network-acl.operate |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 62. Service Actions - Network ACL" caption-side="top"}
{: #roles-table62}
{: tab-title="Actions"}
{: tab-group="Network ACL"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Personality Insights
| Role | Description |
| ----- | :----- |
| Operator | Operator |
| Administrator | Administrator |
| Editor | Editor |
| Manager | Manager |
| Writer | Writer |
| Reader | Reader |
{: row-headers}
{: caption="Table 63. Service Roles - Personality Insights" caption-side="top"}
{: #roles-table63}
{: tab-title="Roles"}
{: tab-group="Personality Insights"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| personality-insights.dashboard.view |  | Administrator, Editor, Operator |
| GET /personality-insights |  | Manager, Reader, Writer |
| POST /personality-insights |  | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 63. Service Actions - Personality Insights" caption-side="top"}
{: #roles-table63}
{: tab-title="Actions"}
{: tab-group="Personality Insights"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Portworx Enterprise
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 64. Service Roles - Portworx Enterprise" caption-side="top"}
{: #roles-table64}
{: tab-title="Roles"}
{: tab-group="Portworx Enterprise"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| portworx.dashboard.view |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 64. Service Actions - Portworx Enterprise" caption-side="top"}
{: #roles-table64}
{: tab-title="Actions"}
{: tab-group="Portworx Enterprise"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Power Systems Virtual Server
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 65. Service Roles - Power Systems Virtual Server" caption-side="top"}
{: #roles-table65}
{: tab-title="Roles"}
{: tab-group="Power Systems Virtual Server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| power-iaas.dashboard.view |  | Manager, Reader |
| power-iaas.cloud-instance.modify |  | Manager |
| power-iaas.cloud-instance.read |  | Manager, Reader |
{: row-headers}
{: caption="Table 65. Service Actions - Power Systems Virtual Server" caption-side="top"}
{: #roles-table65}
{: tab-title="Actions"}
{: tab-group="Power Systems Virtual Server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## PowerAI
| Role | Description |
| ----- | :----- |
| Operator | Operator |
| Administrator | Administrator |
| Editor | Editor |
{: row-headers}
{: caption="Table 66. Service Roles - PowerAI" caption-side="top"}
{: #roles-table66}
{: tab-title="Roles"}
{: tab-group="PowerAI"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| power-ai.dashboard.view |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 66. Service Actions - PowerAI" caption-side="top"}
{: #roles-table66}
{: tab-title="Actions"}
{: tab-group="PowerAI"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Project Coligo
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 67. Service Roles - Project Coligo" caption-side="top"}
{: #roles-table67}
{: tab-title="Roles"}
{: tab-group="Project Coligo"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| knative.dashboard.view | View Dashboard | Administrator, Editor, Operator |
| knative.tenant.read | View project details | Manager, Reader, Writer |
| knative.tenant.entities.create | Create project contents, such as applications, job definitions, and jobs | Manager, Writer |
| knative.tenant.entities.update | Modify existing items already contained by a project, such as applications, jobs, or job definitions.  This does not include the ability to create or delete these items. | Manager, Writer |
| knative.tenant.entities.delete | Delete existing items from within a project | Manager, Writer |
| knative.tenant.entities.read | List and view existing items within a project | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 67. Service Actions - Project Coligo" caption-side="top"}
{: #roles-table67}
{: tab-title="Actions"}
{: tab-group="Project Coligo"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Public Gateway for VPC
| Role | Description |
| ----- | :----- |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 68. Service Roles - Public Gateway for VPC" caption-side="top"}
{: #roles-table68}
{: tab-title="Roles"}
{: tab-group="Public Gateway for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.public-gateway.public-gateway.read |  | Administrator, Editor, Operator, Viewer |
| is.public-gateway.public-gateway.create |  | Administrator, Editor |
| is.public-gateway.public-gateway.update |  | Administrator, Editor |
| is.public-gateway.public-gateway.delete |  | Administrator, Editor |
| is.public-gateway.public-gateway.list |  | Administrator, Editor, Operator, Viewer |
| is.public-gateway.public-gateway.operate |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 68. Service Actions - Public Gateway for VPC" caption-side="top"}
{: #roles-table68}
{: tab-title="Actions"}
{: tab-group="Public Gateway for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Push Notifications
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
{: row-headers}
{: caption="Table 69. Service Roles - Push Notifications" caption-side="top"}
{: #roles-table69}
{: tab-title="Roles"}
{: tab-group="Push Notifications"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| imfpush.dashboard.view |  | Administrator, Editor |
| imfpush.application.list |  | Manager, Reader, Writer |
| imfpush.application.delete |  | Manager |
| imfpush.device.list |  | Manager, Reader, Writer |
| imfpush.application.update |  | Manager |
| imfpush.device.create |  | Manager, Writer |
| imfpush.device.update |  | Manager, Writer |
| imfpush.device.delete |  | Manager |
| imfpush.messages.send |  | Manager, Writer |
| imfpush.messages.send |  | Manager, Writer |
| imfpush.messages.delete |  | Manager |
| imfpush.messages.list |  | Manager, Reader, Writer |
| imfpush.subscriptions.create |  | Manager, Writer |
| imfpush.subscriptions.delete |  | Manager |
| imfpush.subscriptions.list |  | Manager, Reader, Writer |
| imfpush.tags.create |  | Manager, Writer |
| imfpush.tags.update |  | Manager, Writer |
| imfpush.tags.delete |  | Manager |
| imfpush.tags.list |  | Manager, Reader, Writer |
| imfpush.webhooks.create |  | Manager, Writer |
| imfpush.webhooks.update |  | Manager, Writer |
| imfpush.webhooks.delete |  | Manager |
| imfpush.webhooks.list |  | Manager, Reader, Writer |
| imfpush.status.update |  | Manager, Writer |
| imfpush.channels.create | Channel creation | Manager, Writer |
| imfpush.channels.update | Channel update | Manager, Writer |
| imfpush.channels.delete | Channel delete | Manager |
| imfpush.channels.list | Channels list | Manager, Reader, Writer |
| imfpush.channelgroups.create | Channelgroup create | Manager, Writer |
| imfpush.channelgroups.update | Channelgroup update | Manager, Writer |
| imfpush.channelgroups.delete | Channelgroup delete | Manager |
| imfpush.channelgroups.list | Channelgroup list | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 69. Service Actions - Push Notifications" caption-side="top"}
{: #roles-table69}
{: tab-title="Actions"}
{: tab-group="Push Notifications"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Raxak Protect
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 70. Service Roles - Raxak Protect" caption-side="top"}
{: #roles-table70}
{: tab-title="Roles"}
{: tab-group="Raxak Protect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| raxak-protect.dashboard.view |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 70. Service Actions - Raxak Protect" caption-side="top"}
{: #roles-table70}
{: tab-title="Actions"}
{: tab-group="Raxak Protect"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Role management
| Role | Description |
| ----- | :----- |
| Administrator | Administrators can create, edit, update, and delete custom roles. |
| Editor | Editors can edit and update custom roles. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 71. Service Roles - Role management" caption-side="top"}
{: #roles-table71}
{: tab-title="Roles"}
{: tab-group="Role management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| iam-access-management.customRole.create | The ability to create custom roles. | Administrator |
| iam-access-management.customRole.update | The ability to edit and update custom roles. | Administrator, Editor |
| iam-access-management.customRole.delete | The ability to delete a custom role. | Administrator |
{: row-headers}
{: caption="Table 71. Service Actions - Role management" caption-side="top"}
{: #roles-table71}
{: tab-title="Actions"}
{: tab-group="Role management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## SQL Query
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 72. Service Roles - SQL Query" caption-side="top"}
{: #roles-table72}
{: tab-title="Roles"}
{: tab-group="SQL Query"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| sql-query.api.submit | Submit SQL jobs that read and write data, including catalog metadata , such as table definitions. | Manager, Writer |
| sql-query.api.getalljobs | Retrieve a list of recent job submissions and their outcome status. | Manager, Reader, Writer |
| sql-query.api.getjobinfo | Retrieve the detailed status of a job based on provided jobid. | Manager, Reader, Writer |
| sql-query.api.managecatalog | Manage the catalog and indexes. For example, submit DDL statements to create, alter and drop tables, views and indexes. | Manager |
| sql-query.api.readcatalog | Introspect the catalog. For example, list the definitions of tables, views and indexes. | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 72. Service Actions - SQL Query" caption-side="top"}
{: #roles-table72}
{: tab-title="Actions"}
{: tab-group="SQL Query"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## SSH Key for VPC
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 73. Service Roles - SSH Key for VPC" caption-side="top"}
{: #roles-table73}
{: tab-title="Roles"}
{: tab-group="SSH Key for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.key.key.list |  | Administrator, Editor, Operator, Viewer |
| is.key.key.create |  | Administrator, Editor |
| is.key.key.delete |  | Administrator, Editor |
| is.key.key.read |  | Administrator, Editor, Operator, Viewer |
| is.key.key.update |  | Administrator, Editor |
| is.key.artifactattachment.create |  | Administrator, Editor |
| is.key.artifactattachment.update |  | Administrator, Editor |
| is.key.artifactattachment.delete |  | Administrator, Editor |
| is.key.userdata.list |  | Administrator, Editor, Operator |
| is.key.userdata.create |  | Administrator, Editor |
| is.key.userdata.delete |  | Administrator, Editor |
| is.key.userdata.read |  | Administrator, Editor, Operator, Viewer |
| is.key.artifactattachment.read |  | Administrator, Editor, Operator, Viewer |
| is.key.key.operate | Operate on Key | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 73. Service Actions - SSH Key for VPC" caption-side="top"}
{: #roles-table73}
{: tab-title="Actions"}
{: tab-group="SSH Key for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Schematics
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 74. Service Roles - Schematics" caption-side="top"}
{: #roles-table74}
{: tab-title="Roles"}
{: tab-group="Schematics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| schematics.workspace.create |  | Manager |
| schematics.workspace.update |  | Manager, Writer |
| schematics.workspace.delete |  | Manager |
| schematics.workspace.read | Read workspace details | Manager, Reader, Writer |
| schematics.presets.create | Create new presets for the Account | Manager |
| schematics.presets.update | Update the preset values | Manager, Writer |
| schematics.presets.delete | Delete the preset from Account | Manager |
| schematics.presets.read | Read the preset variable, value and metadata | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 74. Service Actions - Schematics" caption-side="top"}
{: #roles-table74}
{: tab-title="Actions"}
{: tab-group="Schematics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Security Advisor
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 75. Service Roles - Security Advisor" caption-side="top"}
{: #roles-table75}
{: tab-title="Roles"}
{: tab-group="Security Advisor"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| security-advisor.dashboard.view |  | Administrator, Editor, Operator |
| security-advisor.findings.read |  | Manager, Reader, Writer |
| security-advisor.findings.write |  | Manager, Writer |
| security-advisor.findings.delete |  | Manager |
| security-advisor.findings.update |  | Manager, Writer |
| security-advisor.metadata.read |  | Manager, Reader, Writer |
| security-advisor.metadata.delete |  | Manager |
| security-advisor.metadata.write |  | Manager |
| security-advisor.metadata.update |  | Manager |
| security-advisor.data.post |  | Manager, Writer |
| security-advisor.data.get |  | Manager, Reader, Writer |
| security-advisor.analytics.post |  | Manager, Writer |
| security-advisor.custom-solution.read |  | Manager, Reader, Writer |
| security-advisor.custom-solution.write |  | Manager |
| security-advisor.custom-solution.update |  | Manager |
| security-advisor.custom-solution.delete |  | Manager |
| security-advisor.partner-solution.read |  | Manager, Reader, Writer |
| security-advisor.partner-solution.write |  | Manager |
| security-advisor.partner-solution.update |  | Manager |
| security-advisor.partner-solution.delete |  | Manager |
| security-advisor.network-insights.enable |  | Manager |
| security-advisor.network-insights.disable |  | Manager |
| security-advisor.activity-insights.enable |  | Manager |
| security-advisor.activity-insights.disable |  | Manager |
| security-advisor.insights-cos.create |  | Manager |
| security-advisor.notification-channels.read |  | Manager, Reader, Writer |
| security-advisor.notification-channels.create |  | Manager |
| security-advisor.notification-channels.delete |  | Manager |
| security-advisor.notification-channels.update |  | Manager |
| security-advisor.accounts.list |  | Reader |
| security-advisor.config-insights.scan | Invoke Config Advisor Scan | Manager |
| security-advisor.insights.read | Fetch  the list of supported insights | Manager, Reader, Writer |
| security-advisor.network-insights-cos.create | Add cos bucket details for insights | Manager |
| security-advisor.activity-insights-cos.create | Add cos bucket details for activity insights | Manager |
| security-advisor.network-insights-cos.delete | Delete cos bucket details for network insights | Manager |
| security-advisor.activity-insights-cos.delete | Delete cos bucket details for activity insights | Manager |
{: row-headers}
{: caption="Table 75. Service Actions - Security Advisor" caption-side="top"}
{: #roles-table75}
{: tab-title="Actions"}
{: tab-group="Security Advisor"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Security Group for VPC
| Role | Description |
| ----- | :----- |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 76. Service Roles - Security Group for VPC" caption-side="top"}
{: #roles-table76}
{: tab-title="Roles"}
{: tab-group="Security Group for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.security-group.security-group.create |  | Administrator, Editor |
| is.security-group.security-group.read |  | Administrator, Editor, Operator, Viewer |
| is.security-group.security-group.update |  | Administrator, Editor |
| is.security-group.security-group.delete |  | Administrator, Editor |
| is.security-group.security-group.operate |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 76. Service Actions - Security Group for VPC" caption-side="top"}
{: #roles-table76}
{: tab-title="Actions"}
{: tab-group="Security Group for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Skytap On IBM Cloud
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 77. Service Roles - Skytap On IBM Cloud" caption-side="top"}
{: #roles-table77}
{: tab-title="Roles"}
{: tab-group="Skytap On IBM Cloud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| skytap.dashboard.view |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 77. Service Actions - Skytap On IBM Cloud" caption-side="top"}
{: #roles-table77}
{: tab-title="Actions"}
{: tab-group="Skytap On IBM Cloud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Speech to Text
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
{: row-headers}
{: caption="Table 78. Service Roles - Speech to Text" caption-side="top"}
{: #roles-table78}
{: tab-title="Roles"}
{: tab-group="Speech to Text"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| speech-to-text.dashboard.view |  | Administrator, Editor, Operator |
| GET /speech-to-text |  | Manager, Reader, Writer |
| POST /speech-to-text |  | Manager, Writer |
| DELETE /speech-to-text |  | Manager, Writer |
| HEAD /speech-to-text |  | Manager, Reader, Writer |
| PUT /speech-to-text |  | Manager, Writer |
{: row-headers}
{: caption="Table 78. Service Actions - Speech to Text" caption-side="top"}
{: #roles-table78}
{: tab-title="Actions"}
{: tab-group="Speech to Text"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Streaming Analytics
| Role | Description |
| ----- | :----- |
| Manager | Manager |
| Writer | Writer |
{: row-headers}
{: caption="Table 79. Service Roles - Streaming Analytics" caption-side="top"}
{: #roles-table79}
{: tab-title="Roles"}
{: tab-group="Streaming Analytics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| streaming-analytics.instances.query |  | Manager |
| streaming-analytics.instances.read |  | Manager, Writer |
| streaming-analytics.instances.update |  | Manager |
| streaming-analytics.instances.start |  | Manager, Writer |
| streaming-analytics.jobs.query |  | Manager, Writer |
| streaming-analytics.jobs.create |  | Manager, Writer |
| streaming-analytics.jobs.read |  | Manager, Writer |
| streaming-analytics.jobs.delete |  | Manager, Writer |
| streaming-analytics.builds.query |  | Manager, Writer |
| streaming-analytics.builds.create |  | Manager, Writer |
| streaming-analytics.builds.read |  | Manager, Writer |
| streaming-analytics.builds.delete |  | Manager, Writer |
| streaming-analytics.artifacts.query |  | Manager, Writer |
| streaming-analytics.artifacts.read |  | Manager, Writer |
| streaming-analytics.artifacts.download |  | Manager, Writer |
{: row-headers}
{: caption="Table 79. Service Actions - Streaming Analytics" caption-side="top"}
{: #roles-table79}
{: tab-title="Actions"}
{: tab-group="Streaming Analytics"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Subnet
| Role | Description |
| ----- | :----- |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 80. Service Roles - Subnet" caption-side="top"}
{: #roles-table80}
{: tab-title="Roles"}
{: tab-group="Subnet"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.subnet.subnet.create |  | Administrator, Editor |
| is.subnet.subnet.read |  | Administrator, Editor, Operator, Viewer |
| is.subnet.subnet.update |  | Administrator, Editor |
| is.subnet.subnet.delete |  | Administrator, Editor |
| is.subnet.subnet.list |  | Administrator, Editor, Operator, Viewer |
| is.subnet.subnet.operate |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 80. Service Actions - Subnet" caption-side="top"}
{: #roles-table80}
{: tab-title="Actions"}
{: tab-group="Subnet"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Support Center
| Role | Description |
| ----- | :----- |
| Administrator | View, search, create, and update support cases |
| Editor | View, search, create, and update support cases |
| Viewer | View and search support cases |
{: row-headers}
{: caption="Table 81. Service Roles - Support Center" caption-side="top"}
{: #roles-table81}
{: tab-title="Roles"}
{: tab-group="Support Center"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| support.case.create |  | Administrator, Editor |
| support.case.update |  | Administrator, Editor |
| support.case.read |  | Administrator, Editor, Viewer |
| support.case.list |  | Administrator, Editor, Viewer |
{: row-headers}
{: caption="Table 81. Service Actions - Support Center" caption-side="top"}
{: #roles-table81}
{: tab-title="Actions"}
{: tab-group="Support Center"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Text to Speech
| Role | Description |
| ----- | :----- |
| Operator | Operator |
| Administrator | Administrator |
| Editor | Editor |
| Manager | Manager |
| Writer | Writer |
| Reader | Reader |
{: row-headers}
{: caption="Table 82. Service Roles - Text to Speech" caption-side="top"}
{: #roles-table82}
{: tab-title="Roles"}
{: tab-group="Text to Speech"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| text-to-speech.dashboard.view |  | Administrator, Editor, Operator |
| GET /text-to-speech |  | Manager, Reader, Writer |
| POST /text-to-speech |  | Manager, Writer |
| DELETE /text-to-speech |  | Manager, Writer |
| HEAD /text-to-speech |  | Manager, Reader, Writer |
| PUT /text-to-speech |  | Manager, Writer |
{: row-headers}
{: caption="Table 82. Service Actions - Text to Speech" caption-side="top"}
{: #roles-table82}
{: tab-title="Actions"}
{: tab-group="Text to Speech"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Tone Analyzer
| Role | Description |
| ----- | :----- |
| Operator | Operator |
| Administrator | Administrator |
| Editor | Editor |
| Manager | Manager |
| Writer | Writer |
| Reader | Reader |
{: row-headers}
{: caption="Table 83. Service Roles - Tone Analyzer" caption-side="top"}
{: #roles-table83}
{: tab-title="Roles"}
{: tab-group="Tone Analyzer"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| tone-analyzer.dashboard.view |  | Administrator, Editor, Operator |
| GET /tone-analyzer |  | Manager, Reader, Writer |
| POST /tone-analyzer |  | Manager, Reader, Writer |
{: row-headers}
{: caption="Table 83. Service Actions - Tone Analyzer" caption-side="top"}
{: #roles-table83}
{: tab-title="Actions"}
{: tab-group="Tone Analyzer"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Toolchain
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 84. Service Roles - Toolchain" caption-side="top"}
{: #roles-table84}
{: tab-title="Roles"}
{: tab-group="Toolchain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| toolchain.dashboard.view | View instances of the Toolchain service. | Administrator, Editor, Operator |
| toolchain.instance.read-properties | Read toolchain properties. | Administrator, Editor, Viewer |
| toolchain.instance.update-properties | Update toolchain properties. | Administrator, Editor |
| toolchain.instance.create-bindings | Add a tool integration to a toolchain within a resource group. | Administrator, Editor |
| toolchain.instance.delete-bindings | Remove a tool integration from a toolchain within a resource group. | Administrator, Editor |
| toolchain.instance.list-bindings | View the tool integrations that are contained in a toolchain within a resource group. | Administrator, Editor, Viewer |
{: row-headers}
{: caption="Table 84. Service Actions - Toolchain" caption-side="top"}
{: #roles-table84}
{: tab-title="Actions"}
{: tab-group="Toolchain"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Transit Gateway
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
{: row-headers}
{: caption="Table 85. Service Roles - Transit Gateway" caption-side="top"}
{: #roles-table85}
{: tab-title="Roles"}
{: tab-group="Transit Gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| transit.transit.manage | Transit service manager | Manager |
{: row-headers}
{: caption="Table 85. Service Actions - Transit Gateway" caption-side="top"}
{: #roles-table85}
{: tab-title="Actions"}
{: tab-group="Transit Gateway"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## User Management
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can view, invite, and update users. You can also view and update user profile settings. |
| Editor | As an editor, you can view, invite, and update users. You can also view and update profile settings. |
| Operator | As an operator, you can view users in the account and view profile settings. |
| Viewer | As a viewer, you can view users in the account and view profile settings. |
{: row-headers}
{: caption="Table 86. Service Roles - User Management" caption-side="top"}
{: #roles-table86}
{: tab-title="Roles"}
{: tab-group="User Management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| user-management.email.retrieve |  |  |
| user-management.user.create |  | Administrator, Editor |
| user-management.user.update |  | Administrator, Editor |
| user-management.user.system-update |  |  |
| user-management.user.state-change |  | Administrator, Editor |
| user-management.user.system-state-change |  |  |
| user-management.user.register |  |  |
| user-management.user.verify |  |  |
| user-management.user.delete |  | Administrator, Editor |
| user-management.user.retrieve |  | Administrator, Editor, Operator, Viewer |
| user-management.invitation-email.create |  | Administrator, Editor |
| user-management.preference.update |  | Administrator, Editor |
| user-management.preference.retrieve |  | Administrator, Editor, Operator, Viewer |
| user-management.user-linkage.create |  |  |
| user-management.user-linkage.update |  |  |
| user-management.user-linkage.delete |  |  |
| user-management.user-linkage.retrieve |  | Administrator, Editor, Operator, Viewer |
| user-management.user-setting.update |  | Administrator, Editor |
| user-management.user-setting.retrieve |  | Administrator, Editor, Operator, Viewer |
| user-management.user.replace-iam-id |  | Administrator, Editor |
{: row-headers}
{: caption="Table 86. Service Actions - User Management" caption-side="top"}
{: #roles-table86}
{: tab-title="Actions"}
{: tab-group="User Management"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## VMware Solutions
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 87. Service Roles - VMware Solutions" caption-side="top"}
{: #roles-table87}
{: tab-title="Roles"}
{: tab-group="VMware Solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| vmware-solutions.instances.create | Create IBM Cloud for VMware Solutions instances | Administrator |
| vmware-solutions.instances.delete | Delete IBM Cloud for VMware Solutions instances | Administrator |
| vmware-solutions.instances.view | List or view IBM Cloud for VMware Solutions instances | Administrator, Editor, Operator, Viewer |
| vmware-solutions.instances.update | Update IBM Cloud for VMware Solutions instances | Administrator, Editor |
| vmware-solutions.account.update | Update account settings for IBM Cloud for VMware Solutions | Administrator |
{: row-headers}
{: caption="Table 87. Service Actions - VMware Solutions" caption-side="top"}
{: #roles-table87}
{: tab-title="Actions"}
{: tab-group="VMware Solutions"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## VPN for VPC
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 88. Service Roles - VPN for VPC" caption-side="top"}
{: #roles-table88}
{: tab-title="Roles"}
{: tab-group="VPN for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.vpn.vpn.create |  | Administrator, Editor |
| is.vpn.vpn.update |  | Administrator, Editor |
| is.vpn.vpn.delete |  | Administrator, Editor |
| is.vpn.vpn.read |  | Administrator, Editor, Operator, Viewer |
| is.vpn.vpn.list |  | Administrator, Editor, Operator, Viewer |
| is.vpn.dashboard.view |  | Administrator, Editor, Operator, Viewer |
{: row-headers}
{: caption="Table 88. Service Actions - VPN for VPC" caption-side="top"}
{: #roles-table88}
{: tab-title="Actions"}
{: tab-group="VPN for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Virtual Private Cloud
| Role | Description |
| ----- | :----- |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 89. Service Roles - Virtual Private Cloud" caption-side="top"}
{: #roles-table89}
{: tab-title="Roles"}
{: tab-group="Virtual Private Cloud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.vpc.vpc.read |  | Administrator, Editor, Operator, Viewer |
| is.vpc.vpc.create |  | Administrator, Editor |
| is.vpc.vpc.delete |  | Administrator, Editor |
| is.vpc.vpc.update |  | Administrator, Editor |
| is.vpc.vpc.list |  | Administrator, Editor, Operator, Viewer |
| is.vpc.vpc.operate |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 89. Service Actions - Virtual Private Cloud" caption-side="top"}
{: #roles-table89}
{: tab-title="Actions"}
{: tab-group="Virtual Private Cloud"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Virtual Server for VPC
| Role | Description |
| ----- | :----- |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 90. Service Roles - Virtual Server for VPC" caption-side="top"}
{: #roles-table90}
{: tab-title="Roles"}
{: tab-group="Virtual Server for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| is.instance.instance.list |  | Administrator, Editor, Operator, Viewer |
| is.instance.instance.create |  | Administrator, Editor |
| is.instance.instance.read |  | Administrator, Editor, Operator, Viewer |
| is.instance.instance.update |  | Administrator, Editor |
| is.instance.instance.delete |  | Administrator, Editor |
| is.instance.instance.operate | As an administrator, an editor or an operator, you can operate on a virtual server instance | Administrator, Editor, Operator |
| is.instance.instance-template.read | View an Instance Template  | Administrator, Editor, Operator, Viewer |
| is.instance.instance-template.create | Create an Instance Template | Administrator, Editor |
| is.instance.instance-template.update | Update an Instance Template | Administrator, Editor |
| is.instance.instance-template.delete | Delete an Instance Template | Administrator, Editor |
{: row-headers}
{: caption="Table 90. Service Actions - Virtual Server for VPC" caption-side="top"}
{: #roles-table90}
{: tab-title="Actions"}
{: tab-group="Virtual Server for VPC"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Visual Recognition
| Role | Description |
| ----- | :----- |
| Manager | Manager |
| Writer | Writer |
| Reader | Reader |
{: row-headers}
{: caption="Table 91. Service Roles - Visual Recognition" caption-side="top"}
{: #roles-table91}
{: tab-title="Roles"}
{: tab-group="Visual Recognition"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| GET /watson-vision-combined |  | Manager, Reader, Writer |
| POST /watson-vision-combined |  | Manager, Writer |
| DELETE /watson-vision-combined |  | Manager, Writer |
{: row-headers}
{: caption="Table 91. Service Actions - Visual Recognition" caption-side="top"}
{: #roles-table91}
{: tab-title="Actions"}
{: tab-group="Visual Recognition"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Voice Agent with Watson
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
{: row-headers}
{: caption="Table 92. Service Roles - Voice Agent with Watson" caption-side="top"}
{: #roles-table92}
{: tab-title="Roles"}
{: tab-group="Voice Agent with Watson"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| voiceagent.agent.manage | Manage all aspects of a Voice Agent with Watson instance. | Manager, Reader, Writer |
| voiceagent.agent.view | View configurations for all agents of a Voice Agent with Watson instance. | Reader |
| voiceagent.usage.view | View usage for all agents of a Voice Agent with Watson instance. | Reader |
| voiceagent.log.view | View all failure logs for all agents of a Voice Agent with Watson instance. | Reader |
| voiceagent.sms.send | Use the SMS gateway API to send SMS messages for a Voice Agent with Watson instance. | Administrator, Editor, Manager, Operator, Writer |
| voiceagent.voice.inbound | Authenticate inbound calls for a Voice Agent with Watson instance using SIPS. | Manager, Writer |
| voiceagent.voice.outbound | Use the outbound calling API to start outbound calls for a Voice Agent with Watson instance. | Manager, Writer |
{: row-headers}
{: caption="Table 92. Service Actions - Voice Agent with Watson" caption-side="top"}
{: #roles-table92}
{: tab-title="Actions"}
{: tab-group="Voice Agent with Watson"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Watson Assistant
| Role | Description |
| ----- | :----- |
| Manager | As a manager, you have permissions beyond the writer role to complete privileged actions as defined by the service. In addition, you can create and edit service-specific resources. |
| Writer | As a writer, you have permissions beyond the reader role, including creating and editing service-specific resources. |
| Reader | As a reader, you can perform read-only actions within a service such as viewing service-specific resources. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 93. Service Roles - Watson Assistant" caption-side="top"}
{: #roles-table93}
{: tab-title="Roles"}
{: tab-group="Watson Assistant"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| GET /conversation |  | Manager, Reader, Writer |
| POST /conversation |  | Manager, Reader, Writer |
| DELETE /conversation |  | Manager, Reader, Writer |
| PATCH /conversation |  | Manager, Reader, Writer |
| PUT /conversation |  | Manager, Reader, Writer |
| conversation.assistant.legacy | Can perform authoring methods for a workspace through v1 APIs. | Manager |
| conversation.skill.write | Can rename, edit, or delete a skill. | Manager, Writer |
| conversation.skill.read | Can open and view a skill. | Manager, Reader, Writer |
| conversation.assistant.write | Can rename, edit, or delete an assistant. | Manager, Writer |
| conversation.assistant.read | Can open and view an assistant. | Manager, Reader, Writer |
| conversation.logs.read | Can view skill analytics and access user conversation logs. | Manager |
| conversation.assistant.list | Can list assistant or skill | Manager, Reader, Viewer, Writer |
| conversation.assistant.default | Default access for Assistant | Manager, Reader, Viewer, Writer |
{: row-headers}
{: caption="Table 93. Service Actions - Watson Assistant" caption-side="top"}
{: #roles-table93}
{: tab-title="Actions"}
{: tab-group="Watson Assistant"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Watson OpenScale
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
| Viewer | As a viewer, you can view service instances, but you can't modify them. |
{: row-headers}
{: caption="Table 94. Service Roles - Watson OpenScale" caption-side="top"}
{: #roles-table94}
{: tab-title="Roles"}
{: tab-group="Watson OpenScale"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| aiopenscale.dashboard.view |  | Administrator, Editor, Operator, Viewer |
{: row-headers}
{: caption="Table 94. Service Actions - Watson OpenScale" caption-side="top"}
{: #roles-table94}
{: tab-title="Actions"}
{: tab-group="Watson OpenScale"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## Watson Studio
No supported roles.
{: row-headers}
{: caption="Table 95. Service Roles - Watson Studio" caption-side="top"}
{: #roles-table95}
{: tab-title="Roles"}
{: tab-group="Watson Studio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

No supported actions.
{: row-headers}
{: caption="Table 95. Service Actions - Watson Studio" caption-side="top"}
{: #roles-table95}
{: tab-title="Actions"}
{: tab-group="Watson Studio"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

## WebSphere Application Server
| Role | Description |
| ----- | :----- |
| Operator | As an operator, you can perform platform actions required to configure and operate service instances, such as viewing a service's dashboard. |
| Administrator | As an administrator, you can perform all platform actions based on the resource this role is being assigned, including assigning access policies to other users. |
| Editor | As an editor, you can perform all platform actions except for managing the account and assigning access policies. |
{: row-headers}
{: caption="Table 96. Service Roles - WebSphere Application Server" caption-side="top"}
{: #roles-table96}
{: tab-title="Roles"}
{: tab-group="WebSphere Application Server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers."}

| Action | Description | Roles |
| ----- | :----- | :----- |
| websphereappsvr.dashboard.view |  | Administrator, Editor, Operator |
{: row-headers}
{: caption="Table 96. Service Actions - WebSphere Application Server" caption-side="top"}
{: #roles-table96}
{: tab-title="Actions"}
{: tab-group="WebSphere Application Server"}
{: class="simple-tab-table"}
{: summary="Use the tab buttons to change the context of the table. This table has row and column headers. The row headers identify the service."}

