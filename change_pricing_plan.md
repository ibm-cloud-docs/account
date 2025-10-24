---

copyright:
  years: 2017, 2025
lastupdated: "2025-10-23"

keywords: change service, switch service, service plan, pricing plan

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Switching your pricing plan
{: #changing}

You can switch the pricing plan of an {{site.data.keyword.Bluemix}} service if plan switches are enabled for the specific service. For example, you might want to switch or reduce your pricing plan. You can switch the service's pricing plan from the service instance dashboard.
{: shortdesc}

You can switch the pricing plan only for certain services. Pricing plans for some services cannot be reduced, or downgraded, to a prior plan. See the documentation for the specific service for information about what plan changes are allowed.

If the ability to switch a plan is enabled for the service, a **Plan** option is displayed on the service instance dashboard. Each service has a different set of steps to follow if you switch your plan. For more information, see section [How you're charged](/docs/account?topic=account-charges).

Are you looking for details about upgrading your account type? See [Upgrading your account](/docs/account?topic=account-upgrading-account) for more information.
{: note}

## Switching a plan in the console
{: #changing-plan-ui}
{: ui}

1. From the {{site.data.keyword.Bluemix_notm}} console, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list**, and select the service.
1. Click **Plan** in the service instance dashboard. Select the pricing plan that you want, and click **Save**.

    Some services have pricing plans that are not selectable from the Plan page. Typically, these plans aren't selectable because they require assistance from [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/solutions/cloud?contactmodule){: external} or they require a migration before you can switch plans. See the documentation for the specific service for information about the required next steps.

Depending on the type of switch you make to your plan, your next steps can vary. For example, if you reduced the pricing plan, restart your app. Or, if you switched the pricing plan, you might need to restart your app, and then take other actions.

Complete the following steps to restart your app:

1. Click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource List**, and find the app that the service is bound to.
1. From the app menu, select **Restart App**.

For more information about any further required actions, see the documentation for the specific service.

## Updating a pricing plan by using the CLI
{: #changing_command_line}
{: cli}

Complete the following steps to switch a pricing plan by using the {{site.data.keyword.Bluemix_notm}} command-line interface (CLI).

1. Check whether the service is enabled with the resource controller.

   ```
   ibmcloud catalog service <service_name>
   ```
   {: codeblock}

   The output lists `RC Compatible true`. Make a note of the ID of the plan that you want to switch to.

   ```
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. Switch the pricing plan for your service instance.

   - If the service is enabled with the resource controller, run the [`ibmcloud resource service-instance-update` command](/docs/cli?topic=cli-ibmcloud_commands_resource#ibmcloud_resource_service_instance_update).

     ```
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}


## Switching a pricing plan by using the API
{: #changing-plan-api}
{: api}

You can programmatically switch a pricing plan for a service by calling the [{{site.data.keyword.cloud_notm}} Resource Controller API](/apidocs/resource-controller/resource-controller#update-resource-instance) as shown in the following sample request. The example switches a pricing plan for an instance.

```
curl -X PATCH https://resource-controller.cloud.ibm.com/v2/resource_instances/8d7af921-b136-4078-9666-081bd8470d94 -H 'Authorization: Bearer <>' -H 'Content-Type: application/json' -d '{
    "name": "my-instance-new-binding-1",
    "resource_plan_id": "744bfc56-d12c-4866-88d5-dac9139e0e5d"
  }'
```
{: codeblock}
{: curl}

```java
Map<String, Object> parameters = new HashMap<String, Object>();
parameters.put("exampleProperty", "exampleValue");

UpdateResourceInstanceOptions updateResourceInstanceOptions = new UpdateResourceInstanceOptions.Builder()
  .id(instanceGuid)
  .name(resourceInstanceUpdateName)
  .parameters(parameters)
  .build();

Response<ResourceInstance> response = service.updateResourceInstance(updateResourceInstanceOptions).execute();
ResourceInstance resourceInstance = response.getResult();

System.out.printf("updateResourceInstance() response:\n%s\n", resourceInstance.toString());
```
{: codeblock}
{: java}

```
getAccountUsage(params)
```
{: codeblock}
{: javascript}

```python
parameters = {
    'exampleProperty': 'exampleValue'
}
resource_instance = resource_controller_service.update_resource_instance(
    id=instance_guid,
    name=resource_instance_update_name,
    parameters=parameters
).get_result()

print('\nupdate_resource_instance() response:\n',
      json.dumps(resource_instance, indent=2))
```
{: codeblock}
{: python}

```go
parameters := map[string]interface{}{"exampleProperty": "exampleValue"}
updateResourceInstanceOptions := resourceControllerService.NewUpdateResourceInstanceOptions(
  instanceGUID,
)
updateResourceInstanceOptions = updateResourceInstanceOptions.SetName(resourceInstanceUpdateName)
updateResourceInstanceOptions = updateResourceInstanceOptions.SetParameters(parameters)

resourceInstance, response, err := resourceControllerService.UpdateResourceInstance(updateResourceInstanceOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(resourceInstance, "", "  ")
fmt.Printf("\nUpdateResourceInstance() response:\n%s\n", string(b))
```
{: codeblock}
{: go}

If you want to purchase an upgraded subscription, contact [{{site.data.keyword.Bluemix_notm}} Sales](https://www.ibm.com/solutions/cloud?contactmodule){: external}.
