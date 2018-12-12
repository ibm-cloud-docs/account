---



copyright:

  years: 2016, 2018
lastupdated: "2017-10-31"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:note: .note}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} Standard Account Limited Release
{: #betaintro}

The {{site.data.keyword.Bluemix}} Standard Account Limited Release introduces a new free account, which offers a new way to work in the Public {{site.data.keyword.Bluemix_notm}}. A Standard account never expires, unlike a 30-day {{site.data.keyword.Bluemix_notm}} trial. You can continue to work on your {{site.data.keyword.Bluemix_notm}} applications without any concerns about time restrictions. 
{:shortdesc}

Users in the London and Dallas regions are eligible for a Standard account. If you aren't in either of those regions, you can still create a Standard account by asking a friend for an invite or reaching out to our sales team at sales@bluemix.net. As a Standard account owner, you can invite friends and colleagues to participate.  

## Introducing the {{site.data.keyword.Bluemix_notm}} Standard account
{: #standardaccount}

You might be wondering what is different in a Standard account as compared to a trial account. The following tables summarize the key details about an {{site.data.keyword.Bluemix_notm}} Standard account. 

|What's new in a Standard account? |    
|-----------------|
| The account never expires. |
| Cloud Foundry applications can access up to 256 MB of free, instantaneous runtime memory. |
| You can access free Lite plans for in-demand Watson services like Conversation, Internet of Things Platform, Cloudant NoSQLDB. For more information, see [What’s available](/docs/pricing/standard_account.html#whatsavailable). |
| Your applications sleep if there's no development activity for 10 days. |
| Your service instances are deleted after 30 days of inactivity. |
{:caption="Table 1. What's new in a Standard account" caption-side="top"}

|What's not changing when a trial account is converted? | 
|-----------------|
|The account is free - you don't need a credit card. |
|You can continue to use your Lite plan instances. |
|Your organization, spaces, and associated team member access settings stay the same. One organization can be transferred to your new account. |
|The level of {{site.data.keyword.Bluemix_notm}} Support stays the same. |
{:caption="Table 2. What's not changing" caption-side="top"}

If your trial account doesn't convert, a message explains why. You might have more than one organization in your existing trial account or apps that cannot be transferred. You can take the appropriate action and then try to convert the account again.
{: note}

When you own a Standard account, you can invite team members to collaborate in your organization and spaces, view your usage, create spaces, update your account profile, and manage your organization.

## Lite plans
{: #liteplans}
   
Lite plans, which are also available in a Pay-As-You-Go account, are structured as a free quota. You can work on your projects worry free, without the risk of generating an accidental bill. The quota might operate for a specific time period, for example, a month, or on a one-off usage basis. Here are some examples of Lite plan quotas:

<ul>
<li>Maximum number of registered devices.</li>
<li>Maximum number of application bindings.</li>
<li>Encrypted data storage limit, for example, 1 GB.</li>
<li>Provisioned throughput capacity.</li>
</ul> 

In a Standard account, you can use anything in the {{site.data.keyword.Bluemix_notm}} catalog that has a Lite plan. Lite plans are easy to find. By default, when you access the catalog, all services with a Lite plan are displayed and identified with a Lite tag ![Lite tag](../icons/Lite.svg). Select a service to view the quota details for the associated Lite plan.

## What’s available in a Standard account?
{: #whatsavailable}

With a Standard account, your Cloud Foundry apps can access up to a maximum of 256 MB of instantaneous runtime memory. If you exceed your allocated quota, you can stop some of the apps to free up runtime memory. You can also work with a Kubernetes cluster with 2 CPU and 4-GB RAM. 

You can use any service in the {{site.data.keyword.Bluemix_notm}} catalog that has a Lite plan. However, you can provision only one instance per Lite plan. During the Standard Account Limited Release, the following services offer a Lite plan:

<ul>
<li>{{site.data.keyword.prf_hublong}}</li>
<li>{{site.data.keyword.mobilepushfull}}</li>
<li>{{site.data.keyword.cloudantfull}}</li>
<li>{{site.data.keyword.conversationfull}}</li>
<li>{{site.data.keyword.iot_full}}</li>
<li>{{site.data.keyword.languagetranslatorfull}}</li>
<li>{{site.data.keyword.personalityinsightsfull}}</li>
<li>{{site.data.keyword.toneanalyzerfull}}</li>
</ul>

Some services are not available in all {{site.data.keyword.Bluemix_notm}} regions. For more information, see [Services by region](/docs/services/services_region.html#services_region).

We are adding to this list of services so stay tuned!

### Quota limits

When quota limits are reached, your application is stopped or your service is disabled. If the Lite plan specifies that the quota is provided monthly, the resource usage is reset on the first of every month when you can resume working with the service. When you are approaching a quota limit, or are at the quota limit, you receive a notification email. 

You can provision one instance per Lite plan. 

These limitations apply to a Standard account only. At any time, you can upgrade to a Pay-As-You-Go or a Subscription account. You pay only for what you use beyond the free allowances. For more information about Pay-As-You-Go and Subscription accounts, see [Account types](/docs/accounts/account-types.html).
{: note}

## Efficiency features
{: #devactivity}

To help you manage your resources {{site.data.keyword.Bluemix_notm}} includes efficiency features that are based on development activity and usage.

### App auto sleep

Your apps will go to sleep after 10 days of development inactivity. This helps when you want to work on a new app because you won't be close to the 256-MB memory quota limit. 

To wake up your apps, start working on them again in the Cloud Foundry command line or the {{site.data.keyword.Bluemix_notm}} console. 
 
 Here’s a list of all commands that wake up your app:
  * `cf push`
  * `cf restate`
  * `cf restart`
  * `cf ssh`
  * `cf scale`
  * `cf stop`
  * `cf start`
  * `cf create-route`
  * `cf map-route`
  * `cf unmap-route`
  * `cf delete-route`
  * `cf enable-ssh`
  * `cf disable-ssh`

For command usage details, see [Cloud Foundry commands](/docs/cli/reference/cfcommands/index.html).

If your app is already enabled for SSH, you can't use the `cf enable-ssh` and `cf disable-sh` commands to wake up your app. 
{: note}

### Garbage collection

Your Lite plan services are deleted if there isn’t any activity on them for 30 days. You don't need to delete inactive instances when you want to create a new one. 
 
## Participating in the Standard Account Limited Release
{: #lgainvitation}

You can ask a friend with a Standard account for an invite or reach out to our sales team at sales@bluemix.net. We would love to have you try it out!

If you receive an invitation from a friend or an {{site.data.keyword.Bluemix_notm}} seller, your exclusive invite is sent to the email address you provide. When you receive the invite, complete the instructions in the email to register for a Standard account. 
