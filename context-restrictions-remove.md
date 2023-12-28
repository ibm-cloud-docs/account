---

copyright:

  years: 2021, 2023

lastupdated: "2023-12-27"

keywords: remove restrictions, delete restrictions, delete network access, delete context based restrictions, remove network access, rule, context, network access rule, network zone

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Removing context-based restrictions
{: #context-restrictions-remove}

By removing context-based restrictions, you delete restrictions that are defined by the contexts in a rule. Deleting rules removes context-based restrictions from the given resource, and requests from any context are allowed if the user has the correct permissions.
{: shortdesc}

## Removing a rule
{: #context-restrictions-remove-rules}
{: ui}

You can remove a rule on your cloud resources by completing the following steps:
1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Context-based restrictions**, and select **Rules**.
2. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") in the row that contains the rule, and click **Remove**.

## Removing a rule by using the CLI
{: #context-restrictions-remove-rules-cli}
{: cli}

You can remove a rule on your cloud resources by completing the following steps:

1. Retrieve the rule ID for the rule that you want to delete by using the [context-based restrictions rules](/docs/account?topic=account-cbr-plugin&interface=cli#cbr-cli-rules-command) command. You can narrow the results of the list by specifying attributes as command options.

   ```sh
   ibmcloud cbr rules --serviceName "iam-identity"
   ```
   {: pre}

1. Delete the rule for the specified rule ID by using the [cbr rule-delete](/docs/account?topic=account-cbr-plugin&interface=cli#cbr-cli-rule-delete-command) command.

   ```sh
   ibmcloud cbr rule-delete 30fd58c9b75f40e854b89c432318b4a2
   ```
   {: pre}

## Removing a rule by using the API
{: #context-restrictions-remove-rules-api}
{: api}

You can remove a rule on your cloud resources by completing the following steps:

1. Retrieve the rule ID for the rule that you want to delete by using the [context-based-restrictions list rules](/apidocs/context-based-restrictions#list-rules) method.

   ```sh
   curl -X GET --location --header "Authorization: Bearer {iam_token}" --header "Accept: application/json" "{base_url}/v1/rules?account_id={account_id}"
   ```
   {: codeblock}
   {: curl}

   ```java
   ListRulesOptions listRulesOptions = new ListRulesOptions.Builder()
   .accountId("testString")
   .build();

   Response<OutRulePage> response = contextBasedRestrictionsService.listRules(listRulesOptions).execute();
   OutRulePage outRulePage = response.getResult();

   System.out.println(outRulePage);
   ```
   {: codeblock}
   {: java}

   ```javascript
    const params = {
      accountId: 'testString',
    };

    contextBasedRestrictionsService.listRules(params)
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
   out_rule_page = context_based_restrictions_service.list_rules(
      account_id='testString'
    ).get_result()

    print(json.dumps(out_rule_page, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
    listRulesOptions := contextBasedRestrictionsService.NewListRulesOptions(
      "testString",
    )

    ruleList, response, err := contextBasedRestrictionsService.ListRules(listRulesOptions)
    if err != nil {
      panic(err)
    }
    b, _ := json.MarshalIndent(ruleList, "", "  ")
    fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}

1. Delete the rule for the specified rule ID.

   ```sh
   curl -X DELETE --location --header "Authorization: Bearer {iam_token}" "{base_url}/v1/rules/{rule_id}"
   ```
   {: codeblock}
   {: curl}

   ```java
   DeleteRuleOptions deleteRuleOptions = new DeleteRuleOptions.Builder()
     .ruleId("testString")
     .build();

   Response<Void> response = contextBasedRestrictionsService.deleteRule(deleteRuleOptions).execute();
   ```
   {: codeblock}
   {: java}

   ```javascript
    const params = {
      ruleId: 'testString',
    };

    contextBasedRestrictionsService.deleteRule(params)
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
    response = context_based_restrictions_service.delete_rule(
      rule_id='testString'
    )
   ```
   {: codeblock}
   {: python}

   ```go
    deleteRuleOptions := contextBasedRestrictionsService.NewDeleteRuleOptions(
      "testString",
    )

    response, err := contextBasedRestrictionsService.DeleteRule(deleteRuleOptions)
    if err != nil {
      panic(err)
    }
    if response.StatusCode != 204 {
      fmt.Printf("\nUnexpected response status code received from DeleteRule(): %d\n", response.StatusCode)
    }
   ```
   {: codeblock}
   {: go}

## Removing a network zone
{: #network-zones-remove}
{: ui}

Removing a network zone removes the set of allowed network locations from which an access request is created. If a network zone is added to a rule, you first have to remove the zone from the rule. See [Updating context-based restrictions](/docs/account?topic=account-context-restrictions-update) for more information about removing a zone from a rule. Then, complete the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, go to **Manage** > **Context-based restrictions**, and select **Network zones**.
2. Click the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") in the row that contains the network zone, and click **Remove**.

## Removing a network zone by using the CLI
{: #network-zones-remove-cli}
{: cli}

Removing a network zone removes the set of allowed network locations from which an access request is created. If a network zone is added to a rule, you first have to remove the zone from the rule. For more information about removing a zone from a rule, see [Updating context-based restrictions](/docs/account?topic=account-context-restrictions-update) . Then, complete the following steps:

1. Retrieve the zone ID for the network zone that you want to delete by using the [contxt-based restrictions zones](/docs/account?topic=account-cbr-plugin&interface=cli#cbr-cli-zones-command) command. You can narrow the results of the list by specifying the name of the zone.

   ```sh
   ibmcloud cbr zones --name "Example zone"
   ```
   {: pre}

1. Delete the network zone for the specified zone ID by using the [cbr zone-delete](/docs/account?topic=account-cbr-plugin&interface=cli#cbr-cli-zone-delete-command) command.

   ```sh
   ibmcloud cbr zone-delete 65810ac762004f22ac19f8f8edf70a34
   ```
   {: pre}

## Removing a network zone by using the API
{: #network-zones-remove-api}
{: api}

Removing a network zone removes the set of allowed network locations from which an access request is created. If a network zone is added to a rule, you first have to remove the zone from the rule. See [Updating context-based restrictions](/docs/account?topic=account-context-restrictions-update) for more information about removing a zone from a rule. Then, complete the following steps:

1. Retrieve the rule ID for the rule that you want to delete by using the [Context-based restrictions list zones](/apidocs/context-based-restrictions#list-zones) method.

   ```sh
   curl -X GET --location --header "Authorization: Bearer {iam_token}" --header "Accept: application/json" "{base_url}/v1/zones?account_id={account_id}"
   ```
   {: codeblock}
   {: curl}

   ```java
   ListZonesOptions listZonesOptions = new ListZonesOptions.Builder()
   .accountId("testString")
   .build();

   Response<OutZonePage> response = contextBasedRestrictionsService.listZones(listZonesOptions).execute();
   OutZonePage outZonePage = response.getResult();

   System.out.println(outZonePage);
   ```
   {: codeblock}
   {: java}

   ```javascript
    const params = {
      accountId: 'testString',
    };

    contextBasedRestrictionsService.listZones(params)
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
    out_zone_page = context_based_restrictions_service.list_zones(
      account_id='testString'
    ).get_result()

    print(json.dumps(out_zone_page, indent=2))
   ```
   {: codeblock}
   {: python}

   ```go
    listZonesOptions := contextBasedRestrictionsService.NewListZonesOptions(
      "testString",
    )

    outZonePage, response, err := contextBasedRestrictionsService.ListZones(listZonesOptions)
    if err != nil {
      panic(err)
    }
    b, _ := json.MarshalIndent(outZonePage, "", "  ")
    fmt.Println(string(b))
   ```
   {: codeblock}
   {: go}

1. Delete the network zone for the specified zone ID.

   ```sh
   curl -X DELETE --location --header "Authorization: Bearer {iam_token}" "{base_url}/v1/zones/{zone_id}"
   ```
   {: codeblock}
   {: curl}

   ```java
    DeleteZoneOptions deleteZoneOptions = new DeleteZoneOptions.Builder()
      .zoneId("testString")
      .build();

    Response<Void> response = contextBasedRestrictionsService.deleteZone(deleteZoneOptions).execute();
   ```
   {: codeblock}
   {: java}

   ```javascript
    const params = {
      zoneId: 'testString',
    };

    contextBasedRestrictionsService.deleteZone(params)
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
    response = context_based_restrictions_service.delete_zone(
      zone_id='testString'
    )
   ```
   {: codeblock}
   {: python}

   ```go
    deleteZoneOptions := contextBasedRestrictionsService.NewDeleteZoneOptions(
      "testString",
    )

    response, err := contextBasedRestrictionsService.DeleteZone(deleteZoneOptions)
    if err != nil {
      panic(err)
    }
    if response.StatusCode != 204 {
      fmt.Printf("\nUnexpected response status code received from DeleteZone(): %d\n", response.StatusCode)
    }
   ```
   {: codeblock}
   {: go}
