---

copyright:

  years: 2015, 2021
lastupdated: "2021-03-10"

keywords: search, find, search for instance, search for resource

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:download: .download}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}


# Searching for resources
{: #searching-for-resources}

You can search for resources from anywhere in the {{site.data.keyword.cloud}} console. Enter the resource or tag in the search field from the console menu bar. You can also use the {{site.data.keyword.Bluemix_notm}} command-line interface (CLI) to search across your resources. The CLI searches for distributed applications and service instances across locations and data centers.
{:shortdesc}

## Refining your search results
{: #results}
{: ui}

<dl>
<dt>View all resource results</dt>
<dt>View all catalog results</dt>
<dd>Use this option to view a filtered catalog search. The first five results are displayed by name. If you want a more detailed search criteria for catalog entries, such as searching the description, you can click this link and get a filtered catalog results view. This option helps you find the offerings that you want to create faster. This appears if it matches to a catalog result. This field doesn't appear if your search query starts with `tag:`.</dd>
<dt>Search support cases</dt>
<dd>Use this option to filter by your open support cases across the platform, including infrastructure resources. This shows up at the end of the search if you search for anything, including if you search by `tag:`.</dd>
<dt>Search in IBM Cloud docs</dt>
<dd>Use this option to get a filtered search of the documentation. This shows up at the end of the search if you search for anything, including if you search by `tag:`.</dd>
</dl>

Press the Forward Slash key (/) to navigate your cursor to the search field.
{: tip}


## Searching with the CLI
{: #searching-cl}
{: cli}

You can also search across all your resources by using Lucene query syntax, with a single command by using the {{site.data.keyword.Bluemix_notm}} CLI, starting with version 0.6.7.


You can search for the following attributes:

<dl>
<dt>`name`</dt>
<dd> The user-defined name of the resource.</dd>
<dt>`region`</dt>
<dd>The geographical location where the resource is provisioned. The allowed values are, for example, `us-south`, `us-east`, `au-syd`, `eu-gb`, `eu-de`, and `jp-tok`.</dd>
<dt>`service_name`</dt>
<dd>The name of the service as it appears in the Name column of the output of `ibmcloud catalog service-marketplace`.</dd>
<dt>`family`</dt>
<dd>The cloud component to which your resource belongs. The allowed values are `cloud_foundry`, `containers`, `vmware`, `resource_controller`, `is` or `ims`.</dd>
<dt>`organization_id`</dt>
<dd>The Cloud Foundry organization GUID.</dd>
<dt>`doc.space_id`</dt>
<dd>The Cloud Foundry space GUID.</dd>
<dt>`doc.resource_group_id`</dt>
<dd>The ID of the resource group.</dd>
<dt>`type`</dt>
<dd>The resource type. The allowed values are: `k8-cluster`, `k8-location`, `namespace`, `cf-service-instance`, `cf-user-provided-service-instance`, `cf-organization`, `cf-service-binding`, `cf-space`, `cf-application`, `resource-instance`, `resource-alias`, `resource-binding`, `resource-group`, `vmware-solutions`, `vpc`, `volume`, `vpn`, `load-balancer`, `security-group`, `key`, `image`, `subnet`, `public-gateway`, `floating-ip`, `network-acl`, `flow-log-collector`, `instance`, `instance-group`, `dedicated-host`, `endpoint-gateway`, `cloud-object-storage-infrastructure`, `block-storage`, `file-storage`, `cloud-backup`, `cdn-powered-by-akamai`, `direct-link-cloud-exchange`, `direct-link-cloud-connect`, `direct-link-colocation`, `direct-link-network-service-provider`, `hardware-firewall`, `hardware-firewall-dedicated`, `fortigate-security-appliance-1gb`, `fortigate-security-appliance-10gb`,  `virtual-router-appliance-copy`, `network-gateway-byoa`, `network-gateway-juniper-vsrx`, `ibm-cloud-load-balancer`, `virtual-server`, `bare-metal`.</dd>
<dt>`creation_date`</dt>
<dd>The date on which the resource is created.</dd>
<dt>`modification_date`</dt>
<dd> The last modification date of the resource.</dd>
<dt>`tags`</dt>
<dd>The tags that have been attached to the resource </dd>
<dt>`tagReferences.tag.name`</dt>
<dd>The tags that have been attached to a classic infrastructure resource. Requires you to specify `-p classic-infrastructure` parameter. </dd>  
<dt>`_objectType:`</dt>
<dd>The object type of the classic infrastructure resource. Allowed values are: `SoftLayer_Virtual_DedicatedHost`, `SoftLayer_Hardware`, `SoftLayer_Network_Application_Delivery_Controller`, `SoftLayer_Network_Subnet_IpAddress`, `SoftLayer_Network_Vlan`, `SoftLayer_Network_Vlan_Firewall`, `SoftLayer_Virtual_Guest`. Requires you to specify `-p classic-infrastructure` parameter. </dd> 
  
  The usage of `-p classic-infrastructure` for _objectType `SoftLayer_Virtual_DedicatedHost`, `SoftLayer_Network_Vlan_Firewall`, `SoftLayer_Virtual_Guest` and `SoftLayer_Hardware` (for the classic infrastructure bare metal servers only) is deprecated since now they are searcheable as all other not classic infrastructure resources.
  </dl>


### Searching for classic infrastructure resources
To search for classic infrastructure resources, the string must be contained within double quotation marks (") in order for an exact match for the query string to be returned. 

In addition, if you enter a search term that includes a hyphen (-) and you don't surround the string with a double quotation marks ("), the search will not return an exact match. Hyphens within the string are used to break the term into multiple strings.


### Search examples
{: #resource-name}

The following examples can help you search for account resources.

When the `-p classic-infrastucture` parameter is not specified search spans across all resources but classic infrastructure resources with `_objectType` `SoftLayer_Network_Application_Delivery_Controller`, `SoftLayer_Network_Subnet_IpAddress`, `SoftLayer_Network_Vlan` or `SoftLayer_Hardware` (excluding bare metal servers).

* To search for all your resources named `ABC`, enter the following command:

    `ibmcloud resource search ‘name:ABC’`

* To search for all Cloud Foundry applications whose name starts with `my`, enter the following command:

    `ibmcloud resource search 'name:my* AND type:cf-application'`

* To search for all service instances of Message Hub, enter the following command:

    `ibmcloud resource search 'service_name:messagehub'`

* To search for all resources in either the `a07181ca-f917-4ee6-af22-b2c0c2a2d5d7` Cloud Foundry organization or the `c900d9671b235c00461c5e311a8aeced` resource group in the `us-south` region, enter the following command:

    `ibmcloud resource search (organization_id:a07181ca-f917-4ee6-af22-b2c0c2a2d5d7 OR doc.resource_group_id:c900d9671b235c00461c5e311a8aeced) AND 'region:us-south'`

* To search for resources that are not classic infrastructure that were created between 16 May 2020 and 20 May 2020, enter the following command:

    `ibmcloud resource search "creation_date:[2020-05-16T00:00:00Z TO 2020-05-20T00:00:00Z]"`
     

* To search for resources that are not classic infrastructure whose name starts with "my", ordered by type, enter the following command:

    `ibmcloud resource search 'name:my*' -s type`
    
* To search for resources that are not classic infrastructure and have been tagged with `MyTag`, enter the following command:

    `ibmcloud resource search 'tags:MyTag'`
    
* To search for all classic infrastructure virtual servers whose fully qualified domain name is `MyVM`, enter the following command:

    `ibmcloud resource search “doc.fullyQualifiedDomainName:MyVM AND service_name:virtual-server”`

* To search for all classic infrastructure resources that have been tagged with `MyTag`, enter the following command:

    `ibmcloud resource search 'tagReferences.tag.name:MyTag' -p classic-infrastructure`
    
* To search for all classic infrastructure of type `SoftLayer_Network_Vlan`

    `ibmcloud resource search '_objectType:SoftLayer_Network_Vlan' -p classic-infrastructure`
  
