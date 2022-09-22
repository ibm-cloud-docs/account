---

copyright:

  years: 2021, 2022

lastupdated: "2022-09-22"

keywords: update network access, network access rule, network zone

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Updating context-based restrictions
{: #context-restrictions-update}

You can update context rules at any time by providing a new description, which helps identifying the purpose of the rule, or selecting a new list of resources and network environments.
{: shortdesc}

To update a context-based restrictions rule, you must be assigned the administrator role on the account management service.

## Updating rules
{: #context-restrictions-update-rules}
{: ui}

To edit the context-based restrictions on your cloud resources, complete the following steps.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Context-based restrictions**, and select **Rules**.
1. To update the scope of resources for the restriction, you can select **All resources** or **Specific resources** based on the available attributes, such as resource group or location. Then, click **Apply** or **Continue**.
1. Click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit") in the summary panel to update an existing context.
   1. Update the allowed endpoint types.
      - Set the toggle to No to allow all service supported endpoint types.
      - Set the toggle to Yes to allow only specific endpoint types.
   1. Update the nework zones.
      - Select new network zones.
      - Deselct network zones to remove them.
1. Then, click **Apply**.
1. Click the **Remove** icon ![Remove icon](../icons/delete.svg "Remove") in the summary panel to remove a context.
1. Configure a new context by selecting all endpoints or a specific endpoint, and by selecting your network zones. Then, click **Add**.
1. Click **Apply** or **Continue**.
1. Provide a new description for your rule. Click **Apply** to update the description, or click **Continue**.
1. To update the enforcement of a rule, click the **Edit** icon ![Edit icon](../icons/edit-tagging.svg "Edit"). You can **Enable**, **Disable**, or set the rule to **Report-only**.
1. Click **Apply** to finish.

## Updating rules by using the CLI
{: #context-restrictions-update-rules-cli}
{: cli}

To update the context-based restrictions on your cloud resources, use the [ibmcloud cbr rule-update](/docs/account?topic=cli-cbr-plugin&interface=cli#cbr-cli-rule-update-command) command. The following example updates description, allowed endpoint type, and network zone for a rule with the ID `30fd58c9b75f40e854b89c432318b4a2`.

```sh
ibmcloud cbr rule-update 30fd58c9b75f40e854b89c432318b4a2 --description 'Example rule description' --service-name kms --context-attributes endpointType=private --zone-id 93de8d3f588ab2c457ff576c364d1145
```
{: pre}

## Updating rules by using the API
{: #context-restrictions-update-rules-api}
{: api}

To update restrictions to your cloud resources by creating rules, call the [Context-based restrictions API](/apidocs/context-based-restrictions?code=node#replace-rule). The following example replaces a rule with an updated version.

```sh
curl -X PUT --location --header "Authorization: Bearer {iam_token}" --header "Accept: application/json" --header "If-Match: {if_match}" --header "Content-Type: application/json" --data '{ "description": "this is an example of rule", "resources": [ { "attributes": [ { "name": "accountId", "value": "12ab34cd56ef78ab90cd12ef34ab56cd" }, { "name": "serviceName", "value": "kms" } ] } ], "contexts": [ { "attributes": [ { "name": "networkZoneId", "value": "76921bd873115033bd2a0909fe081b45" } ] } ], "enforcement_mode": "disabled" }' "{base_url}/v1/rules/{rule_id}"
```
{: codeblock}
{: curl}

```java
RuleContextAttribute ruleContextAttributeModel = new RuleContextAttribute.Builder()
  .name("networkZoneId")
  .value("76921bd873115033bd2a0909fe081b45")
  .build();
RuleContext ruleContextModel = new RuleContext.Builder()
  .attributes(new java.util.ArrayList<RuleContextAttribute>(java.util.Arrays.asList(ruleContextAttributeModel)))
  .build();
ResourceAttribute resourceAttributeModel = new ResourceAttribute.Builder()
  .name("accountId")
  .value("12ab34cd56ef78ab90cd12ef34ab56cd")
  .build();
Resource resourceModel = new Resource.Builder()
  .attributes(new java.util.ArrayList<ResourceAttribute>(java.util.Arrays.asList(resourceAttributeModel)))
  .build();
ReplaceRuleOptions replaceRuleOptions = new ReplaceRuleOptions.Builder()
  .ruleId("testString")
  .ifMatch("testString")
  .description("this is an example of rule")
  .enforcementMode("disabled")
  .contexts(new java.util.ArrayList<RuleContext>(java.util.Arrays.asList(ruleContextModel)))
  .resources(new java.util.ArrayList<Resource>(java.util.Arrays.asList(resourceModel)))
  .build();

Response<OutRule> response = contextBasedRestrictionsService.replaceRule(replaceRuleOptions).execute();
OutRule outRule = response.getResult();

System.out.println(outRule);
```
{: codeblock}
{: java}

```javascript
// Request models needed by this operation.

// RuleContextAttribute
const ruleContextAttributeModel = {
  name: 'networkZoneId',
  value: '76921bd873115033bd2a0909fe081b45',
};

// RuleContext
const ruleContextModel = {
  attributes: [ruleContextAttributeModel],
};

// ResourceAttribute
const resourceAttributeModel = {
  name: 'accountId',
  value: '12ab34cd56ef78ab90cd12ef34ab56cd',
};

// Resource
const resourceModel = {
  attributes: [resourceAttributeModel],
};

const params = {
  ruleId: 'testString',
  ifMatch: 'testString',
  contexts: [ruleContextModel],
  resources: [resourceModel],
  description: 'this is an example of rule',
  enforcementMode: 'disabled',
};

contextBasedRestrictionsService.replaceRule(params)
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
rule_context_attribute_model = {
  'name': 'networkZoneId',
  'value': '76921bd873115033bd2a0909fe081b45',
}

rule_context_model = {
  'attributes': [rule_context_attribute_model],
}

resource_attribute_model = {
  'name': 'accountId',
  'value': '12ab34cd56ef78ab90cd12ef34ab56cd',
}

resource_model = {
  'attributes': [resource_attribute_model],
}

out_rule = context_based_restrictions_service.replace_rule(
  rule_id='testString',
  if_match='testString',
  contexts=[rule_context_model],
  resources=[resource_model],
  description='this is an example of rule',
  enforcement_mode='disabled'
).get_result()

print(json.dumps(out_rule, indent=2))
```
{: codeblock}
{: python}

```go
ruleContextAttributeModel := &contextbasedrestrictionsv1.RuleContextAttribute{
  Name: core.StringPtr("networkZoneId"),
  Value: core.StringPtr("76921bd873115033bd2a0909fe081b45"),
}

ruleContextModel := &contextbasedrestrictionsv1.RuleContext{
  Attributes: []contextbasedrestrictionsv1.RuleContextAttribute{*ruleContextAttributeModel},
}

resourceAttributeModel := &contextbasedrestrictionsv1.ResourceAttribute{
  Name: core.StringPtr("accountId"),
  Value: core.StringPtr("12ab34cd56ef78ab90cd12ef34ab56cd"),
}

resourceModel := &contextbasedrestrictionsv1.Resource{
  Attributes: []contextbasedrestrictionsv1.ResourceAttribute{*resourceAttributeModel},
}

replaceRuleOptions := contextBasedRestrictionsService.NewReplaceRuleOptions(
  "testString",
  "testString",
)
replaceRuleOptions.SetDescription("this is an example of rule")
replaceRuleOptions.SetContexts([]contextbasedrestrictionsv1.RuleContext{*ruleContextModel})
replaceRuleOptions.SetResources([]contextbasedrestrictionsv1.Resource{*resourceModel})
replaceRuleOptions.SetEnforcementMode(contextbasedrestrictionsv1.ReplaceRuleOptionsEnforcementModeDisabledConst)

outRule, response, err := contextBasedRestrictionsService.ReplaceRule(replaceRuleOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(outRule, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}

## Updating network zones
{: #network-zones-update}
{: ui}

You can modify the list of allowed locations where an access request can originate. A set of one or more network locations can be specified by IP addresses (individual addresses, ranges, or subnets), VPCs, or service references. You can update a network zone that is used in a rule, or integrate the new updated network zones into your rules later.

1. In the {{site.data.keyword.cloud_notm}} console, click **Manage** > **Context-based restrictions**, and select **Network zones**.
1. Select the **Actions** icon ![Actions icon](../icons/action-menu-icon.svg "Actions") on the network zone that you want to update, and select **Edit**.
1. You can update your zone name and description.
1. You can edit the list of allowed IP addresses where an access request can originate. Include exceptions in the deny list, if necessary.
1. You can add or remove allowed VPCs.
1. You can add or remove service references. Select a service to associate its IP addresses with your network zone.
1. Click **Next** to review your new configuration.
1. To apply changes, click **Update**.

## Updating network zones by using the CLI
{: #network-zones-update-cli}
{: cli}

To update a network zone, complete the following steps.

1. Retrieve the zone ID for the network zone that you want to update by using the [ibmcloud cbr zones](/docs/account?topic=cli-cbr-plugin&interface=cli#cbr-cli-zones-command) command to list all zones in the account.

    ```sh
    ibmcloud cbr zones
    ```
    {: pre}

1. Update the network zone by using the [ibmcloud cbr zone-update](/docs/account?topic=cli-cbr-plugin&interface=cli#cbr-cli-zone-update-command) command. The following example updates the zone name, allowed addresses, and excluded addresses for a network zone with the ID `65810ac762004f22ac19f8f8edf70a34`.
    ```sh
    ibmcloud cbr zone-update 65810ac762004f22ac19f8f8edf70a34 --name 'Example Zone Name' --addresses 166.22.23.0-166.22.23.108 --excluded 166.22.23.100
    ```
    {: pre}

## Updating network zones by using the API
{: #network-zones-update-api}
{: api}

To update a network zone, complete the following steps.

1. Retrieve the zone ID for the network zone that you want to update by listing the network zones in the account.

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


2.  Update the network zone by using the [ReplaceZone](/apidocs/context-based-restrictions?code=go#replace-zone) method.

    ```sh
    curl -X PUT --location --header "Authorization: Bearer {iam_token}" --header "Accept: application/json" --header "If-Match: {if_match}" --header "Content-Type: application/json" --data '{ "name": "an example of zone", "description": "this is an example of zone", "account_id": "12ab34cd56ef78ab90cd12ef34ab56cd", "addresses": [ { "type": "ipAddress", "value": "169.23.56.234" }, { "type": "ipRange", "value": "169.23.22.0-169.23.22.255" }, { "type": "vpc", "value": "crn:v1:bluemix:public:is:us-south:a/12ab34cd56ef78ab90cd12ef34ab56cd::vpc:r134-d98a1702-b39a-449a-86d4-ef8dbacf281e" } ] }' "{base_url}/v1/zones/{zone_id}"
    ```
    {: codeblock}
    {: curl}

    ```java
    AddressIPAddress addressModel = new AddressIPAddress.Builder()
      .type("ipAddress")
      .value("169.23.56.234")
      .build();
    ReplaceZoneOptions replaceZoneOptions = new ReplaceZoneOptions.Builder()
      .zoneId("testString")
      .ifMatch("testString")
      .name("an example of zone")
      .accountId("12ab34cd56ef78ab90cd12ef34ab56cd")
      .description("this is an example of zone")
      .addresses(new java.util.ArrayList<Address>(java.util.Arrays.asList(addressModel)))
      .build();

    Response<OutZone> response = contextBasedRestrictionsService.replaceZone(replaceZoneOptions).execute();
    OutZone outZone = response.getResult();

    System.out.println(outZone);
    ```
    {: codeblock}
    {: java}

    ```javascript
    // Request models needed by this operation.

    // AddressIPAddress
    const addressModel = {
      type: 'ipAddress',
      value: '169.23.56.234',
    };

    const params = {
      zoneId: 'testString',
      ifMatch: 'testString',
      name: 'an example of zone',
      accountId: '12ab34cd56ef78ab90cd12ef34ab56cd',
      addresses: [addressModel],
      description: 'this is an example of zone',
    };

    contextBasedRestrictionsService.replaceZone(params)
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
    address_model = {
      'type': 'ipAddress',
      'value': '169.23.56.234',
    }

    out_zone = context_based_restrictions_service.replace_zone(
      zone_id='testString',
      if_match='testString',
      name='an example of zone',
      account_id='12ab34cd56ef78ab90cd12ef34ab56cd',
      addresses=[address_model],
      description='this is an example of zone'
    ).get_result()

    print(json.dumps(out_zone, indent=2))
    ```
    {: codeblock}
    {: python}

    ```go
    addressModel := &contextbasedrestrictionsv1.AddressIPAddress{
      Type: core.StringPtr("ipAddress"),
      Value: core.StringPtr("169.23.56.234"),
    }

    replaceZoneOptions := contextBasedRestrictionsService.NewReplaceZoneOptions(
      "testString",
      "testString",
    )
    replaceZoneOptions.SetName("an example of zone")
    replaceZoneOptions.SetAccountID("12ab34cd56ef78ab90cd12ef34ab56cd")
    replaceZoneOptions.SetDescription("this is an example of updated zone")
    replaceZoneOptions.SetAddresses([]contextbasedrestrictionsv1.AddressIntf{addressModel})

    outZone, response, err := contextBasedRestrictionsService.ReplaceZone(replaceZoneOptions)
    if err != nil {
      panic(err)
    }
    b, _ := json.MarshalIndent(outZone, "", "  ")
    fmt.Println(string(b))
    ```
    {: codeblock}
    {: go}
