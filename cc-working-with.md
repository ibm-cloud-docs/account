---
copyright:
  years: 2022, 2025
lastupdated: "2025-01-07"


keywords: carbon calculator, cloud carbon calculator, emission calculator, carbon footprint, sustainability, FAQs

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Working with {{site.data.keyword.Bluemix_notm}}'s carbon calculator
{: #what-is-cloud-calc}

Output that is provided by the carbon calculator is provided “as-is” for informational purposes only, and is based on cloud services information that is provisioned by client in client’s {{site.data.keyword.cloud_notm}} account. Output is provided in a format according to greenhouse gas (GHG) protocol standards. The data sources and tools that are used to calculate client's emissions are subject to change by IBM without notice. The client is responsible for confirming the accuracy of any calculator output for purposes of the client’s compliance with any applicable regulatory obligations or for any other purpose.
{: important}

{{site.data.keyword.cloud_notm}}'s carbon calculator displays the greenhouse gas (GHG) emissions for an account by monitoring your electricity consumption for services, resources, and the location and efficiency of your data centers. Tracking your GHG emissions is important so that you can know how much GHG emissions your account is associated with, and it helps you manage and mitigate your carbon footprint over time.

All service workloads across all sites are metered for electricity consumption or estimations based on hardware profiles. Service usage is also tracked by account, location, and over time. Data is then processed to produce a standards-based GHG emission estimate for each account per service, per location, and resource group. {{site.data.keyword.cloud_notm}} has a resilient global network of locations to host data center workloads and provides three tiers of regions: multizone regions, single-campus multizone regions, and data centers. For more information, see [IBM Cloud global data centers](https://www.ibm.com/cloud/data-centers){: external}.

The carbon calculator provides a wide range of features to track your GHG emissions:

* View total emissions by service, resource group, and location.
* View total emissions for an enterprise account.
* Filter emissions data by time period, service, or location.
* Best practices for cloud sustainability.
* Export the data as a CSV file for additional analyses.
* View emissions data by using [the API](/apidocs/carbon-calculator).

## Services
{: #work-with-services}

Emissions data is currently tracked for a subset of services, but more services are under consideration to be added.

If service data is not displayed, it might be because:
* Emissions data isn't tracked for the service.
* Data for newly added services and current quarter results are not yet available because it can take approximately two months to populate.

Emission data is available for the following services:

* {{site.data.keyword.iae_short}}                               
* {{site.data.keyword.appconfig_short}}                         
* Application Load Balancer                                     
* {{site.data.keyword.bm_is_short}}                             
* {{site.data.keyword.baremetal_short}} for Classic             
* {{site.data.keyword.blockstorageshort}}                       
* {{site.data.keyword.block_storage_is_short}}                  
* Block Storage Snapshots for VPC [New]{: tag-new}              
* Cloud HSM                                                     
* Cloud Object Storage                                          
* Cloudant                                                      
* Code Engine                                                   
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
* Db2                                                           
* Db2 Warehouse                                                 
* Dedicated Host for VPC [New]{: tag-new}                       
* Direct Link Connect                                           
* Direct Link Connect on Classic [New]{: tag-new}               
* Direct Link Dedicated                                         
* Direct Link Dedicated on Classic [New]{: tag-new}             
* {{site.data.keyword.dns_short}}                               
* {{site.data.keyword.en_short}}                                
* {{site.data.keyword.messagehub}}                              
* {{site.data.keyword.filestorage_short}}                       
* {{site.data.keyword.filestorage_vpc_short}}                   
* {{site.data.keyword.fsa10_full}}                              
* Gateway Appliance                                             
* IBM Cloud Activity Tracker                                    
* IBM Cloud Monitoring                                          
* IBM Cloud Platform - Core Services [^tabletext1]              
* IBM Log Analysis                                              
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
* {{site.data.keyword.tg_short}}                                
* VMware Solutions                                              
* {{site.data.keyword.vpn_vpc_short}}                           
* {{site.data.keyword.virtualmachinesshort}} for Classic        
* Virtual Server for VPC                                        

[^tabletext1]: Contains multiple services that are not tracked individually but are combined into one service. IBM Cloud Platform includes the following: Command line interface, Billing and usage, Identity and access management, Global catalog, Global search & tagging, Console, Cloud shell, Projects, Paywall, Schematics, and Carbon calculator.


## Before you begin
{: #carbon-calc-prereq}

Account owners, account administrators, and users with a viewer role or higher on the billing service can view and export emissions data for the entire account. An account or billing administrator role is required to grant other users access to the Billing service. For more information about assigning access, see [Assigning access to account management services](/docs/account?topic=account-account-services&interface=api#billing-acct-mgmt-api).



## IBM Cloud and sustainability
{: #cc-sustainability}

As organizations and users work together to achieve better outcomes for their business and for the environment, digital technologies are a growing source of GHG emissions. There are four areas that are the main source for GHG emissions: data centers, big data analytics, security, and internet usage. For more information about sustainability, see [IT sustainability beyond the data center](https://www.ibm.com/thought-leadership/institute-business-value/report/it-sustainability){: external}.

One use case strategy for sustainability involves ESG reporting, which uses environmental, social, and governance reporting to integrate data silos. For more information, explore [IBM Envizi](https://www.ibm.com/products/envizi){: external}.

## IBM Cloud carbon calculator methodology
{: #carbon-methodology}

{{site.data.keyword.cloud_notm}} plays a critical role for achieving {{site.data.keyword.IBM_notm}}’s energy conservation, renewable electricity procurement, and greenhouse gas (GHG) emissions reduction targets. {{site.data.keyword.cloud_notm}} is improving the estimation approach by introducing the carbon calculator, which gives you a detailed view of your cloud electricity consumption and associated GHG emissions.

{{site.data.keyword.cloud_notm}}'s carbon calculator uses data from electricity consumption, server resource utilization measurements, server and process life-cycle events, and service usage data. Based on the data, it estimates the electricity consumption and GHG emission from each account and service offering, according to the location, time period, and resource groups.

{{site.data.keyword.cloud_notm}} has a resilient global network of locations to host data center workloads and provides three tiers of regions: multizone regions, single-campus multizone regions, and data centers.

The calculation method depends on the gross electricity consumption and GHG emissions factor per location. It allocates a portion of the electricity consumption to each one of the services in a location based on the physical hosts that are being used. Then, it splits the electricity consumption per service, per location, across the tenants that are using the service based on their respective usage metrics. For Classic Infrastructure services, energy consumption is calculated by using the average power consumption for the machine on which the server is running.

Due to the high volume of flexible profiles associated with Bare Metal for Classic, profiles were onboarded in phases. Complete data is available from December 2023 on. Users that require a complete emissions report for previous months can submit a support case to request a manual calculation. When creating a support case, select the **Billing and usage** topic. For more information, see [Creating support cases](https://cloud.ibm.com/docs/account?topic=account-open-case).
{: note}

The method uses the service units of individual {{site.data.keyword.cloud_notm}} offerings to allocate electricity consumption of shared resources to a service's individual resources. The per-account electricity consumption is multiplied by the location’s Power Usage Effectiveness (PUE) and GHG emission factor to yield the accounts carbon footprint.

The goal of the calculation method is to associate electricity consumption and carbon footprint allocation for the following:

* Per client account
* Per client account and cloud service used
* Per client account, cloud service, and location where the service is running
* Per client account and resource group

The carbon calculation methodology has been independently validated by Bureau Veritas for the following key services: Virtual Private Cloud (VPC) and Virtual Servers for VPC, Cloud Object Storage, and Kubernetes Service. [View validation](https://cloud.ibm.com/media/docs/downloads/account/bureau-veritas-validation.pdf){: external}.

For a more in depth explanation about carbon calculators methodology and calculations, see [Energy and carbon quantification methodology](https://cloud.ibm.com/media/docs/downloads/account/carbon-calc-method-v4.pdf){: external}.
