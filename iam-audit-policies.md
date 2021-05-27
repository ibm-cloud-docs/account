---

copyright:

  years: 2021

lastupdated: "2021-05-27"

keywords: auditing IAM policies, last permit information, restore policies

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Auditing access policies
{: #iam-audit-policies}

To reduce the number of policies in the account and keep only the minimum access that is required for each user, you can identify the infrequently used access policies and remove them.
{:shortdesc}

IAM captures authorization information for each policy. This information includes the last time the policy was used to grant a permit and a running count of its use. Every access policy in {{site.data.keyword.cloud}} is soft deleted and kept in the system for up to 10 days. During this time period, you can list and restore them at any time.

## Listing policies with last permit information
{: #iam-audit-policies-list}

List all account policies including last permit information that is sorted by count or last used. The policy metadata can be retrieved by using the [IAM Policy Management API](/apidocs/iam-policy-management#policy-data-enrichment).

```
curl -X GET https://iam.cloud.ibm.com/v1/policies?account_id=<>&format=include_last_permit&sort=-last_modified_at \
  -H 'Authorization: Bearer $TOKEN' \
  -H 'Content-Type: application/json'
```
{: codeblock}
{: curl}

```
ListPoliciesOptions options = new ListPoliciesOptions.Builder()
    .accountId(exampleAccountId)
    .iamId(exampleUserId)
    .format("include_last_permit")
    .build();

Response<PolicyList> response = service.listPolicies(options).execute();
PolicyList policyList = response.getResult();

System.out.println(policyList);
```
{: codeblock}
{: java}

```
const params = {
  accountId: exampleAccountId,
  iamId: exampleUserId,
  format: 'include_last_permit',
};

iamPolicyManagementService.listPolicies(params)
  .then(res => {
    console.log('listPolicies() result:\n' + JSON.stringify(res.result, null, 2));
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```
policy_list = iam_policy_management_service.list_policies(
  account_id=example_account_id, iam_id=example_user_id, format='include_last_permit'
).get_result()

print(json.dumps(policy_list, indent=2))
```
{: codeblock}
{: python}

```
options := iamPolicyManagementService.NewListPoliciesOptions(
  exampleAccountID,
)
options.SetIamID(exampleUserID)
options.SetFormat("include_last_permit")

policyList, response, err := iamPolicyManagementService.ListPolicies(options)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(policyList, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

* `format=include_last_permit`: Include the last permit information for each policy.
* `sort=-last_modified_at`: Sort in ascending ("-") date order. In other words, the policies with the least amount of permits are listed first.

The format of the response is represented in JSON.

```
{
    "policies": [
        {
            "id": "45b226ac-490d-47f3-a785-990e0c729d93",
            "type": "access",
            "subjects": [...],
            "roles": [...],
            "resources": [...],
            ...
            "last_modified_at": "2021-04-09T14:36:30.505Z",
            "last_modified_by_id": "IBMid-310000JVN5",
            "last_permit_at": null,       <-- IAM has no record of this policy ever granting a permit decision 
            "last_permit_frequency": 0,
            "state": "active"
        },
        {
            "id": "11155157-afb3-4792-9ebd-b1f5547be224",
            "type": "access",
            "subjects": [...],
            "roles": [...],
            "resources": [...],
            ...
            "last_modified_at": "2019-05-09T15:28:07.045Z",
            "last_modified_by_id": "IAM",
            "last_permit_at": "2021-04-20T19:45:44.058Z",
            "last_permit_frequency": 137,  <-- it has been used this many times since IAM started keeping track
            "state": "active"
        },
...
```
{: codeblock}

## Deleting unused policies
{: #iam-audit-policies-delete}

You identified one or more policies that have not been used to grant access in a while.

```
curl -X DELETE https://iam.cloud.ibm.com/v1/policies/{examplePolicyId} \
    -H 'Authorization: Bearer $TOKEN'
```
{: codeblock}
{: curl}

```
DeletePolicyOptions options = new DeletePolicyOptions.Builder()
    .policyId(examplePolicyId)
    .build();

service.deletePolicy(options).execute();
```
{: codeblock}
{: java}

```
const params = {
  policyId: examplePolicyId,
};

iamPolicyManagementService.deletePolicy(params)
  .then(res => {
    console.log('deletePolicy() response status code: ' + res.status);
  })
  .catch(err => {
    console.warn(err)
  });
```
{: codeblock}
{: javascript}

```
response = iam_policy_management_service.delete_policy(
  policy_id=example_policy_id
).get_result()

print(json.dumps(response, indent=2))
```
{: codeblock}
{: python}

```
options := iamPolicyManagementService.NewDeletePolicyOptions(
  examplePolicyID,
)

response, err := iamPolicyManagementService.DeletePolicy(options)
if err != nil {
  panic(err)
}
```
{: codeblock}
{: go}

For more information, see [Delete a policy by ID](/apidocs/iam-policy-management#delete-policy).

The policy is deleted and no longer included for authorization evaluations. IAM keeps a copy of all deleted policies for 10 days.
{: note}

## Restoring deleted policies
{: #iam-audit-policies-restore}

You found out that a policy that was recently deleted is needed. In that case, you can follow these steps to restore the policies.

1. List deleted policies in the account and sort by the last modified time.

    ```
    curl -X GET https://iam.cloud.ibm.com/v1/policies?account_id=<>&state=deleted&sort=last_modified_at \
      -H 'Authorization: Bearer $TOKEN' \
      -H 'Content-Type: application/json'
    ```
    {: codeblock}
    {: curl}

    ```
    ListPoliciesOptions options = new ListPoliciesOptions.Builder()
          .accountId(exampleAccountId)
          .iamId(exampleUserId)
          .state("deleted")
          .sort("last_modified_at")
          .build();

    Response<PolicyList> response = service.listPolicies(options).execute();
    PolicyList policyList = response.getResult();

    System.out.println(policyList);
    ```
    {: codeblock}
    {: java}

    ```
    const params = {
      accountId: exampleAccountId,
      iamId: exampleUserId,
      sort: 'last_modified_at',
      state: 'deleted'
    };

    iamPolicyManagementService.listPolicies(params)
      .then(res => {
          console.log('listPolicies() result:\n' + JSON.stringify(res.result, null, 2));
      })
      .catch(err => {
          console.warn(err)
      });
    ```
    {: codeblock}
    {: javascript}

    ```
    policy_list = iam_policy_management_service.list_policies(
      account_id=example_account_id, iam_id=example_user_id, state='deleted', sort='last_modified_at'
    ).get_result()

    print(json.dumps(policy_list, indent=2))
    ```
    {: codeblock}
    {: python}

    ```
    options := iamPolicyManagementService.NewListPoliciesOptions(
      exampleAccountID,
    )
    options.SetIamID(exampleUserID)
    options.SetSort("last_modified_at")
    options.SetState("deleted")

    policyList, response, err := iamPolicyManagementService.ListPolicies(options)
    if err != nil {
      panic(err)
    }
    b, _ := json.MarshalIndent(policyList, "", "  ")
    fmt.Println(string(b))
    ```
    {: codeblock}
    {: go}

    The format of the response is represented in JSON.

    ```
    {
        "policies": [
            {
                "id": examplePolicyId1,
                "type": "access",
                "subjects": [...],
                "roles": [...],
                "resources": [...],
                ...
                "last_modified_at": "2021-04-09T14:36:30.505Z",
                "last_modified_by_id": "IBMid-310000JVN5",
                "last_permit_at": null,
                "last_permit_frequency": 0,
                "state": "deleted"  <-- deleted policy
            },
            {
                "id": examplePolicyId2,
                "type": "access",
                "subjects": [...],
                "roles": [...],
                "resources": [...],
                ...
                "last_modified_at": "2019-05-09T15:28:07.045Z",
                "last_modified_by_id": "IAM",
                "last_permit_at": "2021-04-20T19:45:44.058Z",
                "last_permit_frequency": 137,
                "state": "deleted"  <-- deleted policy
            },
    ...
    ```
    {: codeblock}

2. With the previously retrieved policy ID, you can restore the policy:

    ```
    curl -X PATCH 'https://iam.cloud.ibm.com/v1/policies/{examplePolicyId}' \
      -H 'Authorization: Bearer $TOKEN' \
      -H 'Content-Type: application/json' \
      -H 'If-Match: $ETAG' \
      -d '{"state": "active"}'
    ```
    {: codeblock}
    {: curl}

    ```
    PatchPolicyOptions patchPolicyOptions = new PatchPolicyOptions.Builder()
            .policyId(examplePolicyId)
            .ifMatch(examplePolicyEtag)
            .state("active")
            .build();

    Response<Policy> response = service.patchPolicy(patchPolicyOptions).execute();
    Policy policy = response.getResult();

    System.out.println(policy);
    ```
    {: codeblock}
    {: java}

    ```
    const params = {
      policyId: examplePolicyId,
      ifMatch: examplePolicyETag,
      state: 'active'
    };

    iamPolicyManagementService.patchPolicy(params)
      .then(res => {
        console.log(JSON.stringify(res.result, null, 2));
      })
      .catch(err => {
        console.warn(err)
      });
    ```
    {: codeblock}
    {: javascript}

    ```
    policy = iam_policy_management_service.patch_policy(
      policy_id=example_policy_id,
      if_match=example_updated_policy_etag,
      state='active'
    ).get_result()

    print(json.dumps(policy, indent=2))
    ```
    {: codeblock}
    {: python}

    ```
    options := iamPolicyManagementService.NewPatchPolicyOptions(
      examplePolicyID,
      examplePolicyETag,
    )

    options.SetState("active")

    policy, response, err := iamPolicyManagementService.PatchPolicy(options)
    if err != nil {
      panic(err)
    }
    b, _ := json.MarshalIndent(policy, "", "  ")
    fmt.Println(string(b))
    ```
    {: codeblock}
    {: go}

    The format of the response is represented in JSON.

    ```
    {
        "id": examplePolicyId,
        "type": "access",
        "subjects": [...],
        "roles": [...],
        "resources": [...],
        ...
        "last_modified_at": "2021-04-09T14:36:30.505Z",
        "last_modified_by_id": "IBMid-310000JVN5",
        "last_permit_at": null,
        "last_permit_frequency": 0,
        "state": "active"  <-- policy is active again
    }
    ```
    {: codeblock}

    For more information, see [Restore a deleted policy by ID](/apidocs/iam-policy-management#patch-policy).
