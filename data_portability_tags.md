---

copyright:
  years: 2024
lastupdated: "2024-11-06"

keywords: tags, dora, data portability, Global Search and Tagging

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Understanding data portability for Global Search and Tagging
{: #data-portability}

Data portability involves a set of tools and procedures that enable customers to export metadata stored within IBM Cloud Global Search and Tagging service. It includes procedures to export all tags associated to the customer resources.
{: shortdesc}

## Responsibilities
{: #data-portability-responsibilities}

{{site.data.keyword.Bluemix_notm}} services provide interfaces and instructions to guide the customer in copying and storing the service customer content, including the related configuration, in their selected location.

The customer is responsible for the use of the exported data and configuration for data portability to other infrastructures, which includes:

- The planning and execution for setting up alternative infrastructure on different cloud providers or on-premises software that provide similar capabilities to the {{site.data.keyword.IBM_notm}} services.
- The planning and execution for the porting of the required application code on the alternative infrastructure, including the adaptation of customer's application code, deployment automation, and so on.
- The conversion of the exported data and configuration to the format that's required by the alternative infrastructure and adapted applications.


## Data export procedures
{: #data-portability-procedures}

Global Search and Tagging provides the mechanisms to export your content that's uploaded, stored, and processed when you use the service.

```sh
ibmcloud resources --output json | jq -r '["CRN","RESOURCE NAME", "TAGS", "ACCESS TAGS"], ["---","-------------","---","-----------"], (.items[] | [.crn, .name, (.tags | join(",")), (.access_tags | join(","))]) | @csv' > report.csv
```

## Exported data formats
{: #data-portability-data-formats}

Global Search and Tagging supports the following data format and schema of the exported data, configuration, and application:

### CSV file
{: #portability-csv}

This file contains 4 columns indicating the CRN, the name, the user tags, and the access tags for each resource.

## Data ownership
{: #data-portability-ownership}

All exported data is classified as customer content. Apply the full customer ownership and licensing rights, as stated in the [IBM Cloud Service Agreement](https://www.ibm.com/terms/?id=Z126-6304_WS).
