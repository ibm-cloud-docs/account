---
copyright:

 years: 2023, 2025
lastupdated: "2025-09-22"

keywords: carbon calculator, cloud carbon calculator, emission calculator, carbon footprint, sustainability, FAQs

subcollection: account

content-type: faq

---

{{site.data.keyword.attribute-definition-list}}

# FAQ for {{site.data.keyword.cloud_notm}} Carbon calculator
{: #carboncalcfaqs}

FAQ for {{site.data.keyword.cloud}} Carbon calculator might include questions on how to find guidance on accessing emissions reports, understanding how emissions are calculated, supported services, to use data with ESG tools like IBM Envizi, and providing feedback. To find all FAQ for {{site.data.keyword.cloud_notm}}, see our [FAQ library](/docs/faqs).
{: shortdesc}

## Why can't I see my emissions data?
{: #carboncalc-emissions}
{: faq}

You might not be able to view your accounts emissions data because you don't have the correct access or the service doesn't have enough data. For access, account owners, account administrators, and users with a viewer role or higher on the billing service can view and export emissions data for the entire account. Supported services must have at least 30 days of data to be viewed on the carbon calculator.



If you're still having issues to view data, [create a support case](/unifiedsupport/cases/form) in the {{site.data.keyword.cloud_notm}} Support Center.

## How do you calculate the emissions?
{: #calculate-emissions}
{: faq}

The total emissions are calculated by comparing the energy-related usage with data center energy sources. Emissions from key greenhouse gases are measured in metric tons of carbon dioxide-equivalent (kgCO~2~e). You can download the total emissions data in CSV format. View the total emissions widget on the [Carbon Calculator](/billing/carbon-calculator) page in the console.


## Can I view emissions for all services on my account?
{: #service-emissions}
{: faq}

Emissions data is currently tracked for a subset of services, but more services are under consideration to be added. Emission data is currently available for the following services:

* {{site.data.keyword.iae_short}}                               
* {{site.data.keyword.appconfig_short}}                         
* Application Load Balancer                                     
* {{site.data.keyword.bm_is_short}}                             
* {{site.data.keyword.baremetal_short}} for Classic             
* {{site.data.keyword.blockstorageshort}}                       
* {{site.data.keyword.block_storage_is_short}}                  
* Cloud HSM                                                     
* Cloud Object Storage                                          
* Cloudant                                                      
* {{site.data.keyword.registryshort}}                           
* {{site.data.keyword.contdelivery_short}}                      
* Data Engine (previously SQL Query)                            
* {{site.data.keyword.databases-for-elasticsearch}}             
* {{site.data.keyword.databases-for-enterprisedb}}              
* {{site.data.keyword.databases-for-etcd}}                      
* {{site.data.keyword.databases-for-mongodb}}                   
* {{site.data.keyword.databases-for-mysql}}                     
* {{site.data.keyword.databases-for-postgresql}}                
* {{site.data.keyword.databases-for-redis}}                     
* {{site.data.keyword.datastageshort}}                          
* Db2 Warehouse                                                 
* {{site.data.keyword.dns_short}}                               
* {{site.data.keyword.en_short}}                                
* {{site.data.keyword.messagehub}}                              
* {{site.data.keyword.filestorage_short}}                       
* {{site.data.keyword.filestorage_vpc_short}}                   
* {{site.data.keyword.fsa10_full}}                              
* Gateway Appliance                                             
* IBM Cloud Monitoring                                          
* {{site.data.keyword.keymanagementserviceshort}}               
* {{site.data.keyword.containershort_notm}}                     
* {{site.data.keyword.loadbalancer_short}} for Classic          
* {{site.data.keyword.messages-for-rabbitmq}}                   
* MQ                                                            
* Network Load Balancer                                         
* SAP on Classic Infrastructure                                 
* SAP on VMware                                                 
* {{site.data.keyword.satelliteshort}}                          
* {{site.data.keyword.secrets-manager_short}}                   
* {{site.data.keyword.compliance_short}}                        
* Security and Compliance Center Workload Protection            
* VMware Solutions                                              
* {{site.data.keyword.vpn_vpc_short}}                           
* {{site.data.keyword.virtualmachinesshort}} for Classic        
* Virtual Server for VPC                                        

Because emissions are reported after the close of each billing cycle, data for newly added services and current quarter results take about two months to populate.
{: note}

## How do I use this data with Envizi or other third party ESG reporting tools?
{: #emission-tools}
{: faq}

IBM Envizi is a robust data management foundation that is designed to create a single, trusted data source for all your ESG reporting and opportunity identification. Use ESG reporting to meet compliance and reporting requirements. For more information, see [IBM Envizi ESG Suite](https://www.ibm.com/products/envizi){: external}.

Envizi integration currently requires creation of a custom connector. Reach out to your {{site.data.keyword.cloud_notm}} representative for more information.

## How do I submit feedback on Carbon Calculator?
{: #cc-feedback}
{: faq}

Talk to your customer success manager (CSM) or create case on support center. When you open a support case, choose billing and usage topics and subtopics, but specify carbon calculator in the case description.



## How do I view the carbon emissions factor of my data center?
{: #carbon-intensity}
{: faq}

In the carbon calculator, on the locations widget, you can hover over the location of their data center to see the carbon emissions factor. For more information, see [Working with IBM Cloud carbon calculator](/docs/account?topic=account-what-is-cloud-calc).



## How is greenhouse gas (GHG) measured?
{: #GHG-measure}
{: faq}

{{site.data.keyword.cloud_notm}} plays a critical role in for achieving IBM’s energy conservation, renewable electricity procurement, and GHG emissions reduction targets. {{site.data.keyword.Bluemix_notm}} is improving the estimation approach by introducing the carbon calculator, which gives you a detailed view of your cloud electricity consumption and associated GHG emissions. For more information, see [{{site.data.keyword.cloud_notm}} carbon calculator methodology](/docs/account?topic=account-what-is-cloud-calc#carbon-methodology).

## What methodology does {{site.data.keyword.cloud_notm}} carbon calculator use?
{: #methodology-use}
{: faq}

{{site.data.keyword.cloud_notm}} carbon calculator uses data from electricity consumption, measurement of the usage of server resources, server and process lifecycle events, and service usage data. Based on the data, it estimates the electricity consumption and GHG emission from each account and service offerings, according to the location, time period, and resource groups. For more information, see [{{site.data.keyword.cloud_notm}} carbon calculator methodology](/docs/account?topic=account-what-is-cloud-calc#carbon-methodology).

## Who can view the carbon calculator data?
{: #view-data}
{: faq}

Account owners, account administrators, and users with a viewer role or higher on the billing service can view and export emissions data for the entire account. An account or billing administrator role is required to grant other users access to the Billing service. For more information about assigning access, see [Billing](/docs/account?topic=account-account-services&interface=api#billing-acct-mgmt-api).

## How to view the Power Virtual Server data on carbon calculator?
{: #view-power-virtual-server}
{: faq}

On the [Carbon calculator](https://cloud.ibm.com/billing/carbon-calculator){: external} interface, from the **Filter by server** list, select the **Power Virtual Server** option.

## Why is the data for my workspace not displayed in the carbon calculator?
{: #data-workspace-display}
{: faq}

Only data from Power10 or later workspaces is used to calculate the carbon emissions. If your workspace is on Power9 or previous versions, the data is not displayed on the carbon calculator.

## Why am I not able to see the data for my workspace in the carbon calculator?
{: #data-workspace-carbon-calculator}
{: faq}

If your workspace is on Power9 or previous versions, the data is not displayed on the carbon calculator. Also, you must have the permissions or roles to view the data on the carbon calculator. For more information about assigning access, see [Billing](/docs/account?topic=account-account-services&interface=api#billing-acct-mgmt-api).

## How do I to track GHG emissions for my account in the carbon calculator?
{: #track-GHG-emissions}
{: faq}

To view emissions data for your account, you must be assigned the viewer or higher role on the billing service to view and export the emissions data for the entire account. For more information, see [Account tracking emissions with carbon calculator](/docs/account?topic=account-tracking-emissions-account).

## How do I to extract GHG emissions data through API?
{: #extract-GHG-emissions}
{: faq}

For extracting emissions data through API, see [Carbon calculator API](https://cloud.ibm.com/apidocs/carbon-calculator){: external}.
