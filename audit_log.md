---

copyright:

  years: 2018, 2025
lastupdated: "2025-01-28"

keywords: audit log, user access, account log, system events, monitor system events, user access logs

subcollection: account

---

{{site.data.keyword.attribute-definition-list}}

# Auditing system events for classic infrastructure
{: #audit-log}

If you have a classic infrastructure account, you can monitor storage replication events by viewing audit logs. Audit logs track the interactions of each user, like login attempts, port speed updates, power restarts, and interactions made by {{site.data.keyword.BluSoftlayer_notm}} infrastructure support staff.
{: shortdesc}

## Viewing your audit log in the console
{: #view-audit-log}
{: ui}

To view your audit log, go to **Manage** > **Account** in the {{site.data.keyword.cloud}} console, and select **Audit log**. The audit log initially displays the last 25 interactions that were taken by users on the account. You can view up to 200 interactions at any time. Expand the items per page menu to see more results.

### Viewing a user's access logs
{: #view-access-logs}

From the audit log page, you can also see data for each access attempt that is made by a specific user. The logs display a date and timestamp and IP address for each access attempt. Use the following steps to view a user's Access Logs.

1. Go to **Manage** > **Account** in the {{site.data.keyword.cloud_notm}} console, and select **Audit log**.
2. Then, filter for the user, select the timeframe that you want to view, and choose an object type.

The access log for each user displays the access attempts that were made by that user by date, along with the IP address from which the access attempt was made. Information within the access log is read-only.

### Granting access to the audit log
{: #grant-access-logs}

The Viewer role or higher on all account management services is required to view the audit log. For classic infrastructure permissions, a user must be assigned the Super user role.

## Viewing your audit log by using the SoftLayer API
{: #view-audit-log-api}
{: api}

You can use the SoftLayer API to view your audit log. The {{site.data.keyword.slapi_full}} is the development interface that gives developers and system administrators direct interaction with {{site.data.keyword.cloud_notm}} backend system. The {{site.data.keyword.slapi_short}} powers many of the features in the {{site.data.keyword.cloud_notm}} console, which typically means if an interaction is possible in the {{site.data.keyword.cloud_notm}} console, it can also be run in the API. Because you can programmatically interact with all portions of the {{site.data.keyword.cloud_notm}} environment within the API, you can automate tasks with {{site.data.keyword.slapi_short}}.

The {{site.data.keyword.slapi_short}} is a Remote Procedure Call system. Each call involves sending data toward an API endpoint and receiving structured data in return. The format used to send and receive data with the {{site.data.keyword.slapi_short}} depends on which implementation of the API you choose. The {{site.data.keyword.slapi_short}} currently uses SOAP, XML-RPC, or REST for data transmission.

To programmatically audit system events for classic infrastructure, call the {{site.data.keyword.slapi_short}} as shown in the following example:

```bash
https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?
                    resultLimit=0,50&
                    objectMask=mask[eventName,eventCreateDate,userType]

curl -g -u $SL_USER:$SL_APIKEY 'https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?objectMask=mask[eventName,eventCreateDate,userType]&resultLimit=0,50'

The output looks something like this, in this case just the first event in the list:

[
    {
        "eventCreateDate": "2021-03-29T14:41:55.444089-06:00",
        "eventName": "Login Successful",
        "userType": "CUSTOMER"
    }
  ]
```
{: codeblock}
{: curl}

```python
import datetime
import SoftLayer

class example():

    def __init__(self):

        self.client = SoftLayer.Client()
        debugger = SoftLayer.DebugTransport(self.client.transport)
        self.client.transport = debugger

    def recentLogs(self):
        """REST API CALL
        'https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?
            resultLimit=0,50&
            objectFilter={"eventCreateDate":{"operation":"greaterThanDate","options":[{"name":"date","value":["2018-04-18T00:00:00.0000-06:00"]}]}}'
        """
        _filter = {
            'eventCreateDate': {
                'operation': 'greaterThanDate',
                'options': [
                    {'name': 'date', 'value': [getDateString(30)]}
                ]
            }
        }
        for event in self.getAllObjects(_filter):
            printLogs(event)

    def systemLogs(self):
        """REST API CALL
        'https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?
            resultLimit=0,50&
            objectFilter={"userType":{"operation":"SYSTEM"}}'
        """
        _filter = {'userType': {'operation': 'SYSTEM'}}
        for event in self.getAllObjects(_filter):
            printLogs(event)

    def loginLogs(self):
        """REST API CALL
        https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?
            resultLimit=0,50&
            objectFilter={"eventName":{"operation":"^= Login"}}'
        """
        _filter = {
            'eventName': {
                'operation': '^= Login'
            }
        }
        for event in self.getAllObjects(_filter):
            printLogs(event)

    def allLogs(self):
        """REST API CALL
        'https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?resultLimit=0,50'
        """
        for event in self.getAllObjects(None):
            printLogs(event)


    def getAllObjects(self, _filter, limit=50, offset=0):
        """Pages through all results from the Event_Log. This might take long time."""
        notDone = True
        while notDone:
            events = self.client.call('SoftLayer_Event_Log', 'getAllObjects', filter=_filter, limit=limit, offset=offset)
            print("%s from getAllObjects, offset = %s" % (len(events), offset))

            for event in events:
                yield event
            if len(events) < limit:
                notDone = False
            offset = offset + limit
            notDone = False

    def debug(self):
        for call in self.client.transport.get_last_calls():
            print(self.client.transport.print_reproduceable(call))


def getDateString(self, delta=30):
    date_object = datetime.date.today() - datetime.timedelta(days=delta)
    return date_object.strftime("%Y-%m-%dT00:00:00.0000-06:00")

def printLogs(log):
    print("%s - %s - %s" % (log['eventName'],log['eventCreateDate'], log['userType']))

if __name__ == "__main__":
    main = example()
    main.allLogs()
    main.debug()
```
{: codeblock}
{: python}

```java
import com.google.gson.Gson;
import com.google.gson.GsonBuilder;
import com.softlayer.api.ApiClient;
import com.softlayer.api.RestApiClient;
import com.softlayer.api.ResultLimit;
import com.softlayer.api.service.event.Log;
import java.time.LocalDate;
import java.util.ArrayList;
import java.util.List;
import java.util.stream.Collectors;
public class EventLogExample {
  private final ApiClient client;
  private final Log.Service  logService;
  public EventLogExample() {
    String username = "set-me";
    String apiKey = "set-me";
    client = new RestApiClient().withCredentials(username, apiKey).withLoggingEnabled();
    logService = Log.service(client);
  }
  public static void main(String[] args) {
    EventLogExample eventLogExample = new EventLogExample();
    eventLogExample.getAllTypes();
    eventLogExample.getUserTypes();
    eventLogExample.allLogs();
    eventLogExample.loginLogs();
    eventLogExample.recentLogs();
    eventLogExample.systemLogs();
  }
  /**
   * Running GET on https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/AllEventObjectNames.json with no body
   */
  private void getAllTypes() {
    print(logService.getAllEventObjectNames());
  }
  /***
   * Running GET on https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/AllUserTypes.json with no body
   */
  private void getUserTypes() {
    print(logService.getAllUserTypes());
  }
  /***
   * Running GET on https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/AllObjects.json?resultLimit=0,50 with no body
   */
  private void systemLogs() {
    List<Log> logs=getAllEvents(false);
    String systemName="SYSTEM";
    List<Log> systemLogs = logs.stream()
            .filter(log -> systemName.equalsIgnoreCase(log.getEventName()))
            .collect(Collectors.toList());
    printEventLogs(systemLogs);
  }
  /**
   * Running GET on https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/AllObjects.json?resultLimit=0,50 with no body
   */
  private void recentLogs() {
    LocalDate daysAgo = LocalDate.now().minusDays(30);
    List<Log> logs=getAllEvents(false);
    List<Log> recentLogs = logs.stream()
            .filter(log -> log.getEventCreateDate()
                    .toZonedDateTime()
                    .toLocalDate()
                    .compareTo(daysAgo)>0)
            .collect(Collectors.toList());
    printEventLogs(recentLogs);
  }
  /**
   * Running GET on https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/AllObjects.json?resultLimit=0,50 with no body
   */
  private void loginLogs() {
    List<Log> logs=getAllEvents(false);
    String loginName="login";
    List<Log> loginLogs = logs.stream()
            .filter(log -> log
                    .getEventName()
                    .toLowerCase()
                    .contains(loginName))
            .collect(Collectors.toList());
    printEventLogs(loginLogs);
  }
  /**
   * Running GET on https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/AllObjects.json?resultLimit=0,50 with no body
   */
  private void allLogs() {
    printEventLogs(getAllEvents(false));
  }
  /**
   * Pages through all results from the Event_Log. This might take long time.
   */
  private List<Log> getAllEvents(boolean allEvents) {
    List<Log> result=new ArrayList<>();
    int limit =50;
    int offset =0;
    ResultLimit resultLimit =new ResultLimit(offset,limit);
    boolean iterateEvents=true;
    while(iterateEvents) {
      logService.setResultLimit(resultLimit);
      List<Log> logs = logService.getAllObjects();
      result.addAll(logs);
      if (logs.size() < resultLimit.limit) {
        iterateEvents = false;
      }
      offset+=limit;
      resultLimit=new ResultLimit(offset,limit);
      iterateEvents=iterateEvents&&allEvents;
    }
    return result;
  }
  void print(Object object) {
    Gson gson = new GsonBuilder().setPrettyPrinting().create();
    String json;
    json = gson.toJson(object);
    System.out.println(json);
  }
  void printEventLogs(List<Log> logs){
    for (Log event :logs) {
      System.out.println(String.format("%s - %s - %s",
                      event.getEventName(),
                      event.getEventCreateDate().getTime(),
                      event.getUserType()));
    }
  }
}
```
{: codeblock}
{: java}

```go
package main

import (
	"encoding/json"
	"fmt"
	"github.com/softlayer/softlayer-go/datatypes"
	"github.com/softlayer/softlayer-go/filter"
	"github.com/softlayer/softlayer-go/services"
	"github.com/softlayer/softlayer-go/session"
	"time"
)

// Session created using values set in the environment, or from the local configuration file (i.e. ~/.softlayer).
var sess = session.New()

// Set the limit number of events that the API retrieves in each SoftLayer_Event_Log::getAllObjects  method call.
var pagination = 50

// Set the max number of events to retrieve in each log example function.
var maxNumberOfEvents =200

func main() {

	sess.Debug = true

	//shows the all user type events
	getEventUserTypes()
	userType:="EMPLOYEE"
	//shows the events with names is a userType value
	getLogsByUserType(userType)

	//shows the all user type events
	getEventNames()
	eventName:="Authentication"
	//shows the events which names contain the eventName value
	getLogsByName(eventName)

	//shows the events created from a specific number of days ago
	daysAgo:=30
	getRecentLogs(daysAgo)

	//shows the system logs
	getSystemLogs()

	//shows the login logs
	getLoginLogs()
}

/**
Shows the Event Logs by user type.
Request URL:
GET https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?
objectFilter={"userType":{"operation":"userType"}}&
objectMask=mask[userType,eventName,eventCreateDate]&
resultLimit=0,50
*/
func getLogsByUserType(eventUserType string) {
	filter := filter.Build(filter.Path("userType").Eq(eventUserType))
	mask:="userType,eventName,eventCreateDate"
	systemEvents:=getAllEvents(filter,mask,pagination,maxNumberOfEvents)
	printLogs(systemEvents)
}

/**
Shows the Event Logs which eventName contains nameQuery value
RequestURL:
GET https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?
objectFilter={"eventName":{"operation":"^=+nameQuery"}}&
objectMask=mask[userType;eventName,eventCreateDate]&
resultLimit=0,50
*/
func
getLogsByName(nameQuery string){
	filterQuery:=fmt.Sprintf("^= %s",nameQuery)
	filter := filter.Build(filter.Path("eventName").Eq(filterQuery))
	mask:="userType;eventName,eventCreateDate"
	eventLogs :=getAllEvents(filter,mask,pagination,maxNumberOfEvents)
	printLogs(eventLogs)
}


/**
Shows the SYSTEM Logs.
Request URL:
GET https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?
objectFilter={"userType":{"operation":"SYSTEM"}}&
objectMask=mask[userType,eventName,eventCreateDate]&
resultLimit=0,50
*/
func getSystemLogs(){
	getLogsByUserType("SYSTEM")
}

/**
Shows the Login Logs
RequestURL:
GET https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?
objectFilter={"eventName":{"operation":"^=+Login"}}&
objectMask=mask[userType;eventName,eventCreateDate]&
resultLimit=0,50
*/
func getLoginLogs(){
	getLogsByName("Login")
}

/**
Shows the recent Logs, based on a number of days ago.
Request URL:
GET https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?
objectFilter={"eventCreateDate":{"operation":"greaterThanDate",
	"options":[{"name":"date","value":["2021-04-24T00:00:00.0000-06:00"]}]}}&
objectMask=mask[userType;eventName,eventCreateDate]&
resultLimit=0,50
*/
func getRecentLogs(daysAgo int){
	offsetDate :=getDateString(-daysAgo)
	filterObject:=filter.Build(filter.Path("eventCreateDate").DateAfter(offsetDate))
	mask:="userType;eventName,eventCreateDate"
	recentEvents:=getAllEvents(filterObject,mask,pagination,maxNumberOfEvents)
	printLogs(recentEvents)
}

/**
Pages through all results from the Event_Log. This might take long time.
*/
func getAllEvents(
	filter string,
	mask string,
	pagination int,
	maxNumberOfEvents int,
) (resp []datatypes.Event_Log) {
	limit:=pagination
	offset:=0
	eventsSize:=limit
	var allEvents []datatypes.Event_Log
	for eventsSize<=maxNumberOfEvents {
		events := getAllObjects(limit,offset,filter,mask)
		// return if the events are a list of empty structure like [{}]
		if events[0]==(datatypes.Event_Log{}){
			return allEvents
		}
		allEvents=append(allEvents, events...)
		eventsSize=eventsSize+pagination
	}
	return allEvents
}

/**
Request URL:
GET https://api.softlayer.com/rest/v3.1/SoftLayer_Event_Log/getAllObjects.json?
objectFilter= filter &
objectMask= mask &
resultLimit=0,50

It returns an array of Event_Log encountered.
*/
func getAllObjects(
	limit int,
	offset int,
	filter string,
	mask string,
) (resp []datatypes.Event_Log) {
	var service = services.GetEventLogService(sess)
	result, err := service.
		Limit(limit).
		Offset(offset).
		Filter(filter).
		Mask(mask).
		GetAllObjects()
	if err != nil {
		fmt.Printf("\n Unable to get Events:\n - %s\n", err)
		return
	}

	return result
}

/**
Shows the Event Logs Names.
*/
func getEventNames(){
	var service = services.GetEventLogService(sess)
	result, err := service.GetAllEventObjectNames()
	if err != nil {
		fmt.Printf("\n Unable to get Events:\n - %s\n", err)
		return
	}
	printAsJsonFormat(result)
}

/**
Shows the Event Logs User Types.
*/
func getEventUserTypes() {
	var service = services.GetEventLogService(sess)
	result, err := service.GetAllUserTypes()
	if err != nil {
		fmt.Printf("\n Unable to get User types:\n - %s\n", err)
		return
	}
	printAsJsonFormat(result)
}

/**
Gets a date offset in days determined by offsetDays value.
It returns a string date with SL API date filtering format.
*/
func getDateString(offsetDays int) (resp string) {
	years:=0
	months:=0
	days:= offsetDays
	offsetTime:=time.Now().AddDate(years,months,days)
	return fmt.Sprintf(
		"%d-%02d-%02dT00:00:00.0000-06:00",
		offsetTime.Year(),
		offsetTime.Month(),
		offsetTime.Day())
}

/**
Prints the data as format JSON.
*/
func printAsJsonFormat(data interface{}){
	jsonData, jsonErr := json.MarshalIndent(data, "", "    ")
	if jsonErr != nil {
		fmt.Println(jsonErr)
		return
	}
	println(string(jsonData))
}

/**
Prints the Event Logs.
*/
func printLogs(logs []datatypes.Event_Log){
	fmt.Printf("| %35s | %25s |%10s |\n","Event Name","Event Create Date","User Type")
	for _, log := range logs {
		if log!=(datatypes.Event_Log{}){
			fmt.Printf("| %35s ", *log.EventName)
			fmt.Printf("| %25s ", log.EventCreateDate)
			fmt.Printf("| %10s |\n", *log.UserType)
		}
	}
}
```
{: codeblock}
{: go}

To get all Events logs, use [SoftLayer_Event_Log::getAllObjects()](https://sldn.softlayer.com/reference/services/SoftLayer_Event_Log/getAllObjects/). In this case, just the first 50 events are returned by using pagination limit `resultLimit=0,50`. For more information, see [Using Result Limits in the SoftLayer API](https://sldn.softlayer.com/article/using-result-limits-softlayer-api/). A mask is shown in this example, `mask[eventName,eventCreateDate,userType]`, that restricts other local fields and limits the amount of information returned.
{: curl}

This example deals with a few ways of pulling data from `SoftLayer_Event_Log`. There can be many Logs, so by using a filter, like the `recentLogs` function, you can limit how far back you search for Events.
{: python}

This example deals with a few ways of pulling data from [SoftLayer_Event_Log](https://sldn.softlayer.com/reference/services/SoftLayer_Event_Log/). The latest version of the SoftLayer API Client for Java (`v0.3.2` at the time of publishing this example) does not support object filters in the SoftLayer API, so programmatic filters are used instead.
{: java}

This example deals with a few ways of pulling data from `SoftLayer_Event_Log`. There can be many Logs, so by using a filter, like the `getRecentLogs` function, you can limit how far back you search for Events. This example uses the `maxNumberOfEvents` value to limit the number of event logs that that are retrieved.
{: go}

For more information about the {{site.data.keyword.slapi_short}} and virtual server APIs, see the following resources in the {{site.data.keyword.sldn_full}}:
* [{{site.data.keyword.slapi_short}} Overview ![External link icon](../icons/launch-glyph.svg "External link icon")](https://sldn.softlayer.com/reference/softlayerapi/){: external}
* [Getting Started with the {{site.data.keyword.slapi_short}} ![External link icon](../icons/launch-glyph.svg "External link icon")](https://sldn.softlayer.com/article/getting-started/){: external}

For API usage examples, see the following resources:
* [Understanding and building an order by using the {{site.data.keyword.slapi_short}} order CLI](https://sldn.softlayer.com/article/understanding-ordering/){: external}
* [{{site.data.keyword.slapi_short}} Examples - Release Notes](https://sldn.softlayer.com/){: external}
* [Python examples](https://sldn.softlayer.com/python/){: external}
