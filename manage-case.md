---

copyright:
  years: 2019, 2024
lastupdated: "2024-12-09"

keywords: create case, manage case, open case, start case, ticket

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Managing your support cases
{: #managing-support-cases}

Each support case is assigned a unique number and severity level based on the details in the case description. You can use the case number to track the progress of your reported issue, leave feedback, or update the support case. Updates and feedback are recorded in the case notes, which you can find by selecting the specific support case. You can also add users in your account to a watchlist so they can receive alerts about a case. For more information, see [Updating your support case's watchlist](/docs/account?topic=account-managing-support-cases&interface=ui#contact-watchlist).
{: shortdesc}

To view and manage your support cases, go to the [Manage cases page](/unifiedsupport/cases). If you're a classic infrastructure user, and you don't see a listing of a previous case, click **View classic infrastructure cases**.

You can also view your IBM support cases on the Manage cases page, but they can only be managed in the [IBM support portal](https://www.ibm.com/mysupport/s/){: external}. Access for viewing these cases is controlled in the IBM support portal. For more information about access, see [Managing Your Support Account Access](https://www.ibm.com/mysupport/s/article/Managing-Your-Support-Account-Access?language=en_US){: external}.
{: note}

## Searching for support cases
{: #search-options}
{: ui}

From the Manage cases page, you can filter by case status and search for all of your support cases by using query parameters in the search bar. All parameters can be used together and entered in any order. You can also filter cases by selecting **All cases**, **My cases**, and **Watchlist cases**.

See the following table for details about the search parameters:

| Parameter | Option | Rule |
|-----------|--------|------|
| `number` | target case number | This parameter can't be used with other parameters. When the `number` parameter is used, all of the other parameters and options ignored. The `number` parameter doesn't autofill the search. You must use the whole case number to start the search. |
| `sort` | number  \n subject  \n severity  \n updatedAt | Only one of the `sort` options can be used at one time. You can use the `~` prefix to reverse the sorting order. |
| `status` | new  \n inProgress  \n waitingOnClient  \n resolutionProvided  \n resolved  \n closed | Any number of options can be used. The available options can be entered as `status:new,inProgress` or as `status:new status:inProgress`. |
| `page` | target page to view | If you have several results from your search that spans multiple pages, you can view your results from any result page. For example, to view page 5 out of 10, use `page:5`. |
| `pageSize`  | 10  \n 25  \n 50  \n 100  | The size of that page to be viewed. The page size refers to the number of results that you want to load. |
{: caption="Search query parameters and options" caption-side="top"}

If you enter a term without a parameter, the search results are shown for the support case number and the case subject.
{: note}

### Query and URL examples
{: #search-query-examples}
{: ui}

You can enter search queries in the search bar by stating a parameter and option separated by a colon (:) or you can use parameters in a URL to go directly to a specific case or group of cases on the Manage cases page.

To use parameters in the URL, add a question mark (?) to the end of the URL. Then, set your parameter equal to the option you select. You can also separate additional parameters with an ampersand (&).

To search for a case by keyword, you can enter the word in the search bar without a parameter. To search for a keyword with the URL, use `search` as a parameter and set it equal to your keyword, for example, `search=server`.
{: tip}

#### Searching by case number
{: #search-case-number}

Enter the following to search support cases by case number:

Query
:   `number:CS1234567`

URL
:   `https://cloud.ibm.com/unifiedsupport/cases?number=CS1234567`

#### Searching with multiple parameters
{: #search-mult-parameters}

You might want to search for both new and in progress support cases, limit the results to 25 per page, and displayed by severity. You also know that the case that you're looking for isn't going to be within the first couple of pages, so you want to start on page 5. Enter the following search query:

Query
:   `status:new,inProgress page:5 pageSize:25 sort:severity`

URL
:   `https://cloud.ibm.com/unifiedsupport/cases?status=new&status=inProgress&pageSize=25&sort=severity`

#### Searching for resolved cases
{: #search-resolved}

Enter the following query to view all of the resolved cases based on when they were last updated:

Query
:   `sort:~updatedAT status:resolved`

URL
:   `https://cloud.ibm.com/unifiedsupport/cases?sort=~updatedAT&status=resolved`


## Viewing support cases by using the API
{: #viewing-case-api}
{: api}

You can programmatically view a support case by using the API as shown in the following sample request. For more information, see the [Case Management API](/apidocs/case-management#createcase){: external}.

To view a case, see the following samples:

```curl
curl -X GET 'https://support-center.cloud.ibm.com/case-management/v1/cases/{case_number}?fields=number,updated_at,resources' -H 'Authorization: TOKEN' \
```
{: codeblock}
{: curl}

```java
GetCaseOptions getCaseOptions = new GetCaseOptions.Builder()
  .caseNumber(caseNumber)
  .addFields(GetCaseOptions.Fields.DESCRIPTION)
  .addFields(GetCaseOptions.Fields.STATUS)
  .addFields(GetCaseOptions.Fields.SEVERITY)
  .addFields(GetCaseOptions.Fields.CREATED_BY)
  .build();

Response<Case> response = service.getCase(getCaseOptions).execute();
Case xCase = response.getResult();

System.out.println(xCase);
```
{: codeblock}
{: java}

```javascript
const fieldsToReturn = [
  CaseManagementV1.GetCaseConstants.Fields.DESCRIPTION,
  CaseManagementV1.GetCaseConstants.Fields.STATUS,
  CaseManagementV1.GetCaseConstants.Fields.SEVERITY,
  CaseManagementV1.GetCaseConstants.Fields.CREATED_BY,
];

const params = {
  caseNumber: caseNumber,
  fields: fieldsToReturn,
};

caseManagementService.getCase(params)
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
fields_to_return = [
  GetCaseEnums.Fields.DESCRIPTION,
  GetCaseEnums.Fields.STATUS,
  GetCaseEnums.Fields.SEVERITY,
  GetCaseEnums.Fields.CREATED_BY,
]

case = case_management_service.get_case(
  case_number=case_number,
  fields=fields_to_return
).get_result()

print(json.dumps(case, indent=2))
```
{: codeblock}
{: python}

```go
getCaseOptions := caseManagementService.NewGetCaseOptions(
  caseNumber,
)
getCaseOptions.SetFields([]string{
  casemanagementv1.GetCaseOptionsFieldsDescriptionConst,
  casemanagementv1.GetCaseOptionsFieldsStatusConst,
  casemanagementv1.GetCaseOptionsFieldsSeverityConst,
  casemanagementv1.GetCaseOptionsFieldsCreatedByConst,
})

caseVar, response, err := caseManagementService.GetCase(getCaseOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(caseVar, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}


## Updating support cases by using the API
{: #updating-case-api}
{: api}

The following sample request shows how to programmatically update a support case. For more information, see the [Case Management API](/apidocs/case-management#createcase){: external}.

```curl
curl -X PUT '/case-management/v1/cases/{case_number}/status' -H 'Authorization: TOKEN' -d '{
  "action": "resolve",
  "comment": "The issue is resolved. Thank you!",
  "resolution_code": 1
}'
```
{: codeblock}
{: curl}

```java
ResolvePayload statusPayloadModel = new ResolvePayload.Builder()
  .action("resolve")
  .comment("The problem has been resolved.")
  .resolutionCode(1)
  .build();
UpdateCaseStatusOptions updateCaseStatusOptions = new UpdateCaseStatusOptions.Builder()
  .caseNumber(caseNumber)
  .statusPayload(statusPayloadModel)
  .build();

Response<Case> response = service.updateCaseStatus(updateCaseStatusOptions).execute();
Case xCase = response.getResult();

System.out.println(xCase);
```
{: codeblock}
{: java}

```javascript
const statusPayloadModel = {
  action: 'resolve',
  comment: 'The problem has been resolved.',
  resolution_code: 1,
};

const params = {
  caseNumber: caseNumber,
  statusPayload: statusPayloadModel,
};

caseManagementService.updateCaseStatus(params)
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
status_payload_model = {
  'action': 'resolve',
  'comment': 'The problem has been resolved.',
  'resolution_code': 1,
}

case = case_management_service.update_case_status(
  case_number=case_number,
  status_payload=status_payload_model
).get_result()

print(json.dumps(case, indent=2))
```
{: codeblock}
{: python}

```go
statusPayloadModel := &casemanagementv1.ResolvePayload{
  Action:         core.StringPtr("resolve"),
  Comment:        core.StringPtr("The problem has been resolved."),
  ResolutionCode: core.Int64Ptr(int64(1)),
}

updateCaseStatusOptions := caseManagementService.NewUpdateCaseStatusOptions(
  caseNumber,
  statusPayloadModel,
)

caseVar, response, err := caseManagementService.UpdateCaseStatus(updateCaseStatusOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(caseVar, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

## Adding comments to support cases by using the API
{: #comment-case-api}
{: api}

The following sample request shows how to programmatically add a comment to a support case. For more information, see the [Case Management API](/apidocs/case-management#createcase){: external}.

```curl
curl -X PUT '/case-management/v1/cases/{case_number}/comments' -H 'Authorization: TOKEN' -d '{
  "comment": "Test comment api"
}'
```
{: codeblock}
{: curl}

```java
AddCommentOptions addCommentOptions = new AddCommentOptions.Builder()
  .caseNumber(caseNumber)
  .comment("This is an example comment.")
  .build();

Response<Comment> response = service.addComment(addCommentOptions).execute();
Comment comment = response.getResult();

System.out.println(comment);
```
{: codeblock}
{: java}

```javascript
const params = {
  caseNumber: caseNumber,
  comment: 'This is an example comment,',
};

caseManagementService.addComment(params)
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
comment = case_management_service.add_comment(
  case_number=case_number,
  comment='This is an example comment.'
).get_result()

print(json.dumps(comment, indent=2))
```
{: codeblock}
{: python}

```go
addCommentOptions := caseManagementService.NewAddCommentOptions(
  caseNumber,
  "This is an example comment.",
)

comment, response, err := caseManagementService.AddComment(addCommentOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(comment, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

## Support case status types
{: #search-case-status}

When your response to an update in your support case is needed, the status is displayed as `Waiting on client`. If you don't provide a response within seven days, the status is updated to `Resolved`. The case is then closed if there's still no response after seven more days. For a description of each status type, see the following table:

| Status              | Description |
|---------------------|------------|
| New                 | A created case not yet viewed by a support engineer. |
| In progress         | A case that is under review. |
| Waiting on client   | The support engineer has submitted an inquiry on the case that needs the user's response. |
| Resolution provided | The support engineer provided a resolution that the user needs to perform. |
| Resolved            | The support case is considered finished and ready to be closed. |
| Closed              | Case is closed by a support engineer and can't be reopened. |
{: caption="Support case status types" caption-side="top"}

## Escalating support cases
{: #escalation}

You can use the escalation process to surface critical issues and voice your concern about a support case. When a case is escalated, the {{site.data.keyword.Bluemix_notm}} support team reviews the information in the support case and responds with appropriate updates. For information about case severity, see [Case severity and initial response times](/docs/account?topic=account-support-case-severity).

To escalate a case, complete the following steps:

1. Contact {{site.data.keyword.Bluemix_notm}} Support by chat or by phone.
   * Click **Chat with {{site.data.keyword.IBM_notm}}** in the [Support Center](/unifiedsupport/supportcenter){: external} to connect with a support agent
   * Connect by phone using the number in the [Support Center](/unifiedsupport/supportcenter){: external}.
1. Provide your existing case number and a request to escalate the case.
1. Provide the justification an escalation and explain the business impact of your problem or issue.

Basic support plans: If you have a Basic support plan, access to support is through cases only. If your support inquiry requires a more immediate response, consider upgrading to a Premium or Advanced support plan so you assign a severity level to a case. To upgrade your support plan, contact a [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/cloud?contactmodule){: external} representative.

## Updating your support case's watchlist
{: #contact-watchlist}

You can update which users in your account can receive notifications about your support case by adding them to the watchlist. Users can be added to the watchlist when you [create a support case](/docs/account?topic=account-open-case) or after the support case is created.
{: shortdesc}

By default, account users don't have access to create, update, search, or view cases. The account owner must provide users access by assigning an Identity and Access Management (IAM) access policy. For more information, see [Assigning user access for working with support cases](/docs/account?topic=account-access#access).

To ensure that users are notified about updates to an existing support case that you created, complete the following steps to add them to the watchlist.

1. From the {{site.data.keyword.cloud_notm}} console menu bar, click the **Help** icon ![Help icon](../icons/help.svg "Help") > **Support center**.
1. Select the support case from the Recent support cases tile.
1. From the Watchlist section, click the **Settings** icon ![Settings icon](../icons/settings.svg "Settings").
1. Select users that are in the account to add to the watchlist.

   Users that are added to the watchlist must be a member of the account in which the case was created. For more information about assigning users access to your account, see [Adding users to your case management access group](/docs/account?topic=account-access&interface=ui#iam-managed).
   {: note}
