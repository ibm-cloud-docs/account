---

copyright:

  years: 2015, 2022
lastupdated: "2022-05-09"

keywords: search, find, search for instance, search for resource

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Searching for resources
{: #searching-for-resources}

You can search for resources from anywhere in the {{site.data.keyword.cloud}} console. Enter the resource or tag in the search field from the console menu bar. You can also use the {{site.data.keyword.Bluemix_notm}} command-line interface (CLI) to search across your resources. The CLI searches for distributed applications and service instances across locations and data centers. [The Global Search and Tagging - Search API](https://cloud.ibm.com/apidocs/search) supports searching for resources as well. 
{: shortdesc}

## Refining your search results
{: #results}
{: ui}

View all resource results

View all catalog results
:   Use this option to view a filtered catalog search. The first five results are displayed by name. If you want a more detailed search criteria for catalog entries, such as searching the description, you can click this link and get a filtered catalog results view. This option helps you find the offerings that you want to create faster. This appears if it matches to a catalog result. This field doesn't appear if your search query starts with `tag:`.

Search support cases
:   Use this option to filter by your open support cases across the platform, including infrastructure resources. This shows up at the end of the search if you search for anything, including if you search by `tag:`.

Search in {{site.data.keyword.cloud_notm}} docs
:   Use this option to get a filtered search of the documentation. This shows up at the end of any search, including if you search by `tag:`.


Press the Forward Slash key (/) to navigate your cursor to the search field.
{: tip}


## Searching with the CLI
{: #searching-cl}
{: cli}

You can also search across all your resources by using Lucene query syntax, with a single command by using the {{site.data.keyword.Bluemix_notm}} CLI, starting with version 0.6.7.


You can search for the following attributes:


`name`
:   The user-defined name of the resource.

`region`
:   The geographical location where the resource is created. The allowed values are, for example, `us-south`, `us-east`, `au-syd`, `eu-gb`, `eu-de`, and `jp-tok`.

`service_name`
:   The name of the service as it appears in the Name column of the output of `ibmcloud catalog service-marketplace`.

`family`
:   The cloud component to which your resource belongs. The allowed values are: `cloud_foundry`, `containers`, `container-registry`, `vmware`, `resource_controller`, `is`, `atracker`, `ims`, `iam`.

`organization_id`
:   The Cloud Foundry organization GUID.

`doc.space_id`
:   The Cloud Foundry space GUID.

`doc.resource_group_id`
:   The ID of the resource group.

`type`
:   The resource type. The allowed values are: `k8-cluster`, `k8-location`, `namespace`, `cf-service-instance`, `cf-user-provided-service-instance`, `cf-organization`, `cf-service-binding`, `cf-space`, `cf-application`, `resource-instance`, `resource-alias`, `resource-binding`, `resource-group`, `vmware-solutions`, `vpc`, `volume`, `vpn`, `load-balancer`, `security-group`, `key`, `image`, `subnet`, `public-gateway`, `floating-ip`, `network-acl`, `flow-log-collector`, `instance`, `instance-group`, `dedicated-host`, `endpoint-gateway`, `snapshot`, `share`, `backup-policy`, `vpn-server`, `placement-group`, `route`, `target`, `cloud-object-storage-infrastructure`, `block-storage`, `file-storage`, `cloud-backup`, `cdn-powered-by-akamai`, `direct-link-cloud-exchange`, `direct-link-cloud-connect`, `direct-link-colocation`, `direct-link-network-service-provider`, `hardware-firewall`, `hardware-firewall-dedicated`, `fortigate-security-appliance-1gb`, `fortigate-security-appliance-10gb`,  `virtual-router-appliance-copy`, `network-gateway-byoa`, `network-gateway-juniper-vsrx`, `ibm-cloud-load-balancer`, `virtual-server`, `bare-metal`, `citrix-virtual-app-desktop`, `bare-metal-server`, `serviceid`.

`creation_date`
:   The date on which the resource is created.

`modification_date`
:   The last modification date of the resource.

`tags`
:   The tags that have been attached to the resource.

`tagReferences.tag.name`
:   The tags that have been attached to a classic infrastructure resource. Requires you to specify `-p classic-infrastructure` parameter.

`_objectType:`
:   The object type of the classic infrastructure resource. Allowed values are: `SoftLayer_Virtual_DedicatedHost`, `SoftLayer_Hardware`, `SoftLayer_Network_Application_Delivery_Controller`, `SoftLayer_Network_Subnet_IpAddress`, `SoftLayer_Network_Vlan`, `SoftLayer_Network_Vlan_Firewall`, `SoftLayer_Virtual_Guest`. Requires you to specify `-p classic-infrastructure` parameter.


The usage of `-p classic-infrastructure` for _objectType `SoftLayer_Virtual_DedicatedHost`, `SoftLayer_Network_Vlan_Firewall`, `SoftLayer_Virtual_Guest` and `SoftLayer_Hardware` (for the classic infrastructure bare metal servers only) is deprecated since now they are searchable as all other not classic infrastructure resources.
{: note}


### Searching for classic infrastructure resources
{: #search-classic-infra-resources}

To search for classic infrastructure resources, the string must be contained within double quotation marks (") in order for an exact match for the query string to be returned. 

In addition, if you enter a search term that includes a hyphen (-) and you don't surround the string with a double quotation mark ("), the search will not return an exact match. Hyphens within the string are used to break the term into multiple strings.


### Search examples
{: #resource-name}

The following examples can help you search for account resources.

When the `-p classic-infrastucture` parameter is not specified search spans across all resources but classic infrastructure resources with `_objectType` `SoftLayer_Network_Application_Delivery_Controller`, `SoftLayer_Network_Subnet_IpAddress`, or `SoftLayer_Hardware` (excluding bare metal servers).

* To search for all your resources named `ABC`, enter the following command:

    ```bash
    ibmcloud resource search ‘name:ABC’
    ```
    {: codeblock}

* To search for all Cloud Foundry applications whose name starts with `my`, enter the following command:

    ```bash
    ibmcloud resource search 'name:my* AND type:cf-application'
    ```
    {: codeblock}

* To search for all service instances of Message Hub, enter the following command:

    ```bash
    ibmcloud resource search 'service_name:messagehub'
    ```
    {: codeblock}

* To search for all resources in either the `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` Cloud Foundry organization or the `c900d9671b235c00461c5e311a8aeced` resource group in the `us-south` region, enter the following command:

    ```bash
    ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'
    ```
    {: codeblock}

* To search for resources that are not classic infrastructure that were created between 16 May 2020 and 20 May 2020, enter the following command:

    ```bash
    ibmcloud resource search "creation_date:[2020-05-16T00:00:00Z TO 2020-05-20T00:00:00Z]"
    ```
    {: codeblock}
     

* To search for resources that are not classic infrastructure whose name starts with "my", ordered by type, enter the following command:

    ```bash
    ibmcloud resource search 'name:my*' -s type
    ```
    {: codeblock}
    
* To search for resources that are not classic infrastructure and have been tagged with `MyTag`, enter the following command:

    ```bash
    ibmcloud resource search 'tags:MyTag'
    ```
    {: codeblock}
    
* To search for all classic infrastructure virtual servers whose fully qualified domain name is `MyVM`, enter the following command:

    ```bash
    ibmcloud resource search “doc.fullyQualifiedDomainName:MyVM AND service_name:virtual-server”
    ```
    {: codeblock}

* To search for all classic infrastructure resources that have been tagged with `MyTag`, enter the following command:

    ```bash
    ibmcloud resource search 'tagReferences.tag.name:MyTag' -p classic-infrastructure
    ```
    {: codeblock}
    
* To search for all classic infrastructure of type `SoftLayer_Network_Vlan`

    ```bash
    ibmcloud resource search '_objectType:SoftLayer_Network_Vlan' -p classic-infrastructure
    ```
    {: codeblock}
  
## Search by using the API
{: #searching-api}
{: api}

To search for resources, call [The Global Search and Tagging - Search API](https://cloud.ibm.com/apidocs/search#search). The following example searches for all resources with tag "project:myproject" attached. 

Use the `SearchOptions.Builder` to create a `SearchOptions` object that contains the parameter values for the `search` method.
{: java}

Instantiate the `SearchOptions` struct and set the fields to provide parameter values for the `Search` method.
{: go}

```bash
curl -X POST -H "Authorization: {iam_token}" -H "Accept: application/json" -H "Content-Type: application/json" -d '{"query": "tags:project\\:myproject OR access_tags:project\\:myproject", "fields": ["*"]}' "api.global-search-tagging.cloud.ibm.com/v3/resources/search"
```
{: codeblock}
{: curl}

```java
SearchOptions searchOptions = new SearchOptions.Builder()
  .query("GST-sdk-*")
  .fields(new java.util.ArrayList<String>(java.util.Arrays.asList("*")))
  .searchCursor(searchCursor)
  .build();

Response<ScanResult> response = service.search(searchOptions).execute();
ScanResult scanResult = response.getResult();

System.out.println(scanResult);
```
{: codeblock}
{: java}

```javascript
const params = {
  query: 'GST-sdk-*',
  fields: ['*'],
  searchCursor: searchCursor,
};

globalSearchService.search(params)
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
response = global_search_service.search(query='GST-sdk-*',
                    fields=['*'])
scan_result = response.get_result()

print(json.dumps(scan_result, indent=2))
```
{: codeblock}
{: python}

```go
searchOptions := globalSearchService.NewSearchOptions()
searchOptions.SetLimit(10)
searchOptions.SetQuery("GST-sdk-*")
searchOptions.SetFields([]string{"*"})

scanResult, response, err := globalSearchService.Search(searchOptions)
if err != nil {
  panic(err)
}
b, _ := json.MarshalIndent(scanResult, "", "  ")
fmt.Println(string(b))
```
{: codeblock}
{: go}
