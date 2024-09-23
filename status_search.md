---

copyright:

  years: 2018, 2021

lastupdated: "2021-11-18"

keywords: status page, status query, incident, maintenance, search query

subcollection: get-support

---

{{site.data.keyword.attribute-definition-list}}

# Advanced status search
{: #adv-search}

You can search across all tabs on the [Status page](/status), but did you know that you can build URL search values by using query parameters from outside the console?
{: shortdesc}

The following list includes examples of URL search options:

* Load the page with the Status tab selected: `console.cloud.ibm.com/status?selected=status`
* Load the page with the Planned maintenance tab selected: `console.cloud.ibm.com/status?selected=maintenance`
* Load the page with the Security bulletin tab selected: `console.cloud.ibm.com/status?selected=security`
* Load the page with the Announcements tab selected: `console.cloud.ibm.com/status?selected=announcement`
* Load the page with a search query entered: `console.cloud.ibm.com/status?selected=<selected>&query=<query>`
* Land on the page with filters selected. For example, you can set the geographic location to North America by using the following URL search: `console.cloud.ibm.com/status?selected=status&region=na`

* Use unique notification identifiers as a search parameter to go directly to the details for the notification. For example, `query=INC1000001` targets items with the ID: `INC1000001`. In this example, `INC1000001` is the case number for a maintenance notification.

## URL query filters:
{: #url-query}

The following table provides information on URL query filters that you can use to search across all tabs on the status page. 

| URL Query Parameter | Description                                                                                                                         | Values                      |
|---------------------|-------------------------------------------------------------------------------------------------------------------------------------|-----------------------------|
| `?type`             | A filter that applies only to the Status tab. Use the `?type` query to filter the Status tab by incidents or maintenance.           | `=incident`, `=maintenance` |
| `?region`           | Filter the page by geographic location.                                                                                             | `=na`, `=eu`, `=sa`, `=ap`  |
| `?component`        | Filter the page by {{site.data.keyword.Bluemix_notm}} components. For example, you might filter by a service you are interested in. | Applies to most global catalog IDs; for example, `?component=iotf-service` filters the page and display events that affect Internet of Things Platform |
{: caption="Table 1. URL query filters" caption-side="top"}

You can always use the **Filter by** filters, and then copy or bookmark the URL query that is generated. The filters are displayed in your URL and can help you build future queries.
{: tip}
