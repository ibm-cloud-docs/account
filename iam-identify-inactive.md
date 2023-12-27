---

copyright:
  years: 2022
lastupdated: "2023-12-27"

keywords: inactive identity, inactive identities, inactive, inactive users, inactive service IDs, inactive trusted profiles, inactive API keys

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Identifying inactive identities
{: #id-inactive-identities}

Identities are considered inactive when they haven't logged in or been in use in 30 days. You can review which users, service IDs, trusted profiles, and API keys in your account are inactive. You might want to remove inactive identities if they are no longer needed. Removing access for inactive identities can reduce the risk of unauthorized access to your IBM Cloud resources and help you manage access more efficiently. To manage inactive identities, you must be assigned the Administrator role on the IAM Identity Service.
{: shortdesc}

When you delete an identity from the table, for example a user, and click **Update report**, it takes a few minutes for a new report to exclude the deleted user.
{: note}

## Managing inactive identities in the console
{: #manage-inactive-identities}
{: ui}

To view inactive identities in the console, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Access (IAM)**, and select **Inactive identities**.
2. Click **Update report** to view the most recent report of the inactive identities in your account.

   Only the most recent report is available. Reports older than a day are deleted when generating a new report.
   {: note}

3. Select a tab to review a list of inactive identities.
4. To delete inactive identities that are no longer in use, click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") > **Remove**.

Before you delete an identity, confirm that they are inactive for at least 30 days.
{: note}

To learn more about the implications of removing or deleting identities in your account, review the following documentation:
   - [Removing users from an account](/docs/account?topic=account-remove&interface=ui)
   - [Deleting service IDs](/docs/account?topic=account-serviceids&interface=ui#delete_serviceid)
   - [Removing trusted profiles](/docs/account?topic=account-trusted-profile-remove)
   - [Deleting an API key](/docs/account?topic=account-userapikey&interface=ui#delete_user_key)
   - [Deleting an API key for a service ID](/docs/account?topic=account-serviceidapikeys&interface=ui#delete_service_key)


## Managing inactive identities by using the API
{: #manage-inactive-identities-api}
{: api}

To view inactive identities by using the [IAM Identity Services API](/apidocs/iam-identity-token-api#create-report), complete the following steps:

1. Get your account ID, which you'll need in later steps. Go to the [Account settings](/account/settings) page in the console to view your account ID. The account ID is a 32 character, unique account identifier.

1. Trigger the inactive identities report for your account.

   ```sh
   curl -X POST 'https://iam.test.cloud.ibm.com/v1/activity/accounts/ACCOUNT_ID/report' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json'
   ```
   {: codeblock}
   {: curl}


   ```java
   CreateReportOptions createReportOptions = new CreateReportOptions.Builder()
    .accountId(accountId)
    .build();

   Response<ReportReference> response = service.createReport(createReportOptions).execute();
   ReportReference reportReference = response.getResult();

   reportReferenceValue = reportReference.getReference();

   System.out.println(reportReferenceValue);
   ```
   {: codeblock}
   {: java}


   ```javascript
   const params = {
   accountId: accountId,
   type: 'inactive',
   duration: '120',
   };

   try {
   const res = await iamIdentityService.createReport(params);
   reportReference = res.reference;
   console.log(JSON.stringify(res.result, null, 2));
   } catch (err) {
   console.warn(err);
   }
   ```
   {: codeblock}
   {: javascript}

   ```python
   create_report_response = iam_identity_service.create_report(
   account_id=account_id,
   type="inactive",
   duration="120",
   ).get_result()

   print(json.dumps(create_report_response, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   createReportOptions := iamIdentityService.NewCreateReportOptions(accountID)
   createReportOptions.SetType("inactive")
   createReportOptions.SetDuration("120")

   report, response, err := iamIdentityService.CreateReport(createReportOptions)
   if err != nil {
   panic(err)
   }
   b, _ := json.MarshalIndent(report, "", "  ")
   fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}

1. Get the inactive identities report.

   ```sh
   curl -X GET 'https://iam.test.cloud.ibm.com/v1/activity/accounts/ACCOUNT_ID/report/REFERENCE' -H 'Authorization: Bearer TOKEN' -H 'Content-Type: application/json'
   ```
   {: codeblock}
   {: curl}

   ```java
   GetReportOptions getReportOptions = new GetReportOptions.Builder()
      .accountId(accountId)
      .reference(reportReferenceValue)
      .build();

   Response<Report> response = service.getReport(getReportOptions).execute();
   Report fetchedReport = response.getResult();

   System.out.println(fetchedReport);
   ```
   {: codeblock}
   {: java}

   ```javascript
   const params = {
   accountId: accountId,
   reference: 'latest',
   };

   try {
   const res = await iamIdentityService.getReport(params);
   console.log(JSON.stringify(res.result, null, 2));
   } catch (err) {
   console.warn(err);
   }
   ```
   {: codeblock}
   {: javascript}

   ```python
   get_report_response = iam_identity_service.get_report(
   account_id=account_id, reference="latest"
   ).get_result()

   print(json.dumps(get_report_response, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
   getReportOptions := iamIdentityService.NewGetReportOptions(accountID, "latest")

   report, response, err := iamIdentityService.GetReport(getReportOptions)
   if err != nil {
   panic(err)
   }
   b, _ := json.MarshalIndent(report, "", "  ")
   fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}

   Take note of the IAM IDs for inactive users.
   {: tip}

4. To delete inactive users that are no longer in use, call the [User Management API](/apidocs/user-management#remove-user).

   ```sh
   curl -X DELETE https://user-management.cloud.ibm.com/v2/accounts/987d4cfd77b04e9b9e1a6asdcc861234/users/IBMid-1000000000 -H 'Authorization: Bearer <IAM_TOKEN>' -H 'Content-Type: application/json'
   ```
   {: codeblock}
   {: curl}

   ```java
   RemoveUserOptions removeUserOptions = new RemoveUserOptions.Builder()
   .accountId(accountId)
   .iamId(deleteUserId)
   .build();

   Response<Void> response = userManagementService.removeUser(removeUserOptions).execute();
   ```
   {: codeblock}
   {: java}

   ```javascript
   const params = {
   accountId: accountId,
   iamId: deleteUserId,
   };

   try {
   await userManagementAdminService.removeUser(params);
   } catch (err) {
   console.warn(err);
   }
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

   Before you delete an identity, confirm that they are inactive for at least 30 days.
   {: note}

To learn more about the implications of removing or deleting identities in your account, review the following documentation:
   - [Removing users from an account](/docs/account?topic=account-remove)
   - [Deleting service IDs](/docs/account?topic=account-serviceids&interface=ui#delete_serviceid)
   - [Removing trusted profiles](/docs/account?topic=account-trusted-profile-remove)
   - [Deleting an API key](/docs/account?topic=account-userapikey#delete_user_key)
   - [Deleting an API key for a service ID](/docs/account?topic=account-serviceidapikeys#delete_service_key)
