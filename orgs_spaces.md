---

copyright:
  years: 2015, 2022
lastupdated: "2022-01-31"

keywords: account, add orgs, add spaces, cloud foundry orgs

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:external: target="_blank" .external}
{:help: data-hd-content-type='help'} 
{:support: data-reuse='support'}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}
{:javascript: .ph data-hd-programlang='javascript'}

# Creating orgs and spaces
{: #orgsspacesusers}

As an {{site.data.keyword.Bluemix}} account owner, you can add Cloud Foundry orgs and spaces to your account. Only account owners can create new Cloud Found orgs. If you're an organization manager, you can manage the orgs in the account after they are created.
{: shortdesc}

## Cloud Foundry org concepts
{: #cf-org-concepts}

Orgs enable collaboration among users and facilitate the logical grouping of project resources in the following ways:

   * You can group a set of spaces, apps, services, domains, routes, and users together in orgs.
   * You can manage the user access to the orgs and spaces on an individual basis.

Orgs can span multiple regions, and they are defined by the following items:

Spaces
:   A subgroup within an org that you can use to organize applications, services, and users. Spaces are tied to a specific region in {{site.data.keyword.Bluemix_notm}}.

Users
:   The role with basic permission in orgs and spaces. You must be assigned to an org before you can be granted other permissions to the spaces within the org. For more details, see [Cloud Foundry access](/docs/account?topic=account-mngcf).

Domains
:   Provide the route on the internet that is allocated to the org. A route has a subdomain and a domain. A subdomain is typically the application name. A domain might be a system domain or a custom domain that you registered for your application. If you add a custom domain, you must configure your DNS server to resolve your custom domain to point to the {{site.data.keyword.Bluemix_notm}} system domain. In this way, when {{site.data.keyword.Bluemix_notm}} receives a request for your custom domain, it can properly route it to your application.

Quota
:   Represents the resources that are available to an org, including the number of services and the amount of memory that can be allocated for use by the org. Quotas are assigned when orgs are created. Any application or service in a space within an org contributes to the usage of the quota. With Pay-As-You-Go or Subscription accounts, you can adjust your quota for Cloud Foundry applications and containers as the needs of your org change.

In a Subscription account, the quota is a user-defined limit that initiates spending notifications.
{: tip}

## Managing Cloud Foundry orgs and spaces 
{: #manage-orgs-spaces}
{: ui} 

You can manage Cloud Foundry orgs and spaces by going to **Manage** > **Account** in the {{site.data.keyword.cloud_notm}} console, and selecting **Account resources** > **Cloud Foundry orgs**.

## Creating orgs in the console
{: #createorg}
{: help} 
{: support}
{: ui}

If you have a billable account, you can add as many orgs as you need. Lite accounts can have only one org, which is already created in your account. Orgs can't be deleted after you add them.

1. In the console, go to **Manage** > **Account**, and select **Account resources** > **Cloud Foundry orgs**. Click **Create**.
2. Enter an org name. The name must be unique in {{site.data.keyword.Bluemix_notm}}.

   If the org name is already in use by another {{site.data.keyword.Bluemix_notm}} Public, Dedicated, or Local user, you must specify a different name.
3. Click **Add**.

After you add the org, you're automatically assigned the Organization Manager permission, so you can edit the org name, add users, and create or delete spaces in the org.

You can assign the following [Cloud Foundry roles](/docs/account?topic=account-mngcf#cfroles) to users in an org. All users who are invited to the account are assigned the auditor role by default.

* Organization manager
* Organization billing manager
* Organization auditor

## Creating spaces in the console
{: #spaceinfo}
{: help} 
{: support}
{: ui}

Within an organization, you can use spaces to group a set of applications, services, and users. Spaces are defined within a single {{site.data.keyword.Bluemix_notm}} region. You can create spaces in an org based on the delivery lifecycle. For example, you can create a `dev` space as a development environment, a `test` space as a testing environment, and a `production` space as a production environment. Then, you can associate your apps with spaces.

To add a space to an org, complete the following steps.

1. On the Cloud Foundry Orgs page in the console, click the name of the org that you want to add a space to.
2. Click **Add a space**.
3. Select a region and enter a name.
4. Click **Save**.

After you add users to an org, you can grant them permissions to the spaces. Similar to orgs, spaces also have a set of [Cloud Foundry roles](/docs/account?topic=account-mngcf#cfroles) with specific permissions that are assigned to team members:

* Space manager
* Space developer
* Space auditor

A user must be assigned at least one of the permissions in the space.
{: tip}

## Creating orgs by using the CLI
{: #create-org-cli}
{: cli}

You can create an organization by using the {{site.data.keyword.Bluemix}} Command Line Interface. For detailed information about managing accounts, users in an account, and the org, space, and roles of public Cloud Foundry environments, see [Managing accounts, users, and Cloud Foundry orgs](/docs/cli?topic=cli-ibmcloud_commands_account#ibmcloud_account_org).

1. Log in, and select the account.

   ```bash
   ibmcloud login
   ```
   {: codeblock}

2. Create an organization by running the [`ibmcloud account org-create`](/docs/cli?topic=cli-ibmcloud_commands_account#ibmcloud_account_org_create) command, where `ORG_NAME` is the name of the organization to be created, and `-r, --region REGION` is the region name. 

   ```bash
   ibmcloud account org-create ORG_NAME [-r, --region REGION]
   ```
   {: codeblock}


   For example, the following command creates an organization that is named `IBM`.

   ```bash
   ibmcloud account org-create IBM
   ```
   {: codeblock}

   If `REGION` is not specified, the name is default to current region.

This operation can be run only by the account owner. 
{: note}
     
## Creating spaces by using the CLI
{: #create-space-cli}
{: cli}

You can also create spaces by using the {{site.data.keyword.Bluemix}} CLI.

1. Log in, and select the account.

   ```bash
   ibmcloud login
   ```
   {: codeblock}

2. Create an organization by running the [`ibmcloud account space-create`](/docs/cli?topic=cli-ibmcloud_commands_account#ibmcloud_account_space_create) command, where `-o` is the organization, and `-q` is the quota to assign to the newly created space. 

   ```bash
   ibmcloud account space-create SPACE [-o ORG] [-q SPACE_QUOTA]
   ```
   {: codeblock}
   
## Creating orgs by using the Cloud Foundry API
{: #create-org-api}
{: api}

You can create an organization by calling the Cloud Foundry API. For detailed information about how to use it, see [Create an Organization](http://v3-apidocs.cloudfoundry.org/version/3.97.0/index.html#create-an-organization){: external}. Check the following sample request, where `my-organization` is the name of your organization:

```curl
curl "https://api.example.org/v3/organizations" \
  -X POST \
  -H "Authorization: bearer [token]" \
  -H "Content-Type: application/json" \
  -d '{ "name": "my-organization" }'
```
{: codeblock}
{: curl}

## Creating spaces by using the Cloud Foundry API
{: #create-space-api}
{: api}

You can also create spaces by calling the Cloud Foundry API. For detailed information about how to use it, see [Create a Space](http://v3-apidocs.cloudfoundry.org/version/3.97.0/index.html#create-a-space){: external}. Check the following sample request, where `my-space`is the name of your space:

```curl
curl "https://api.example.org/v3/spaces" \
  -X POST \
  -H "Authorization: bearer [token]" \
  -H "Content-Type: application/json" \
  -d '{
    "name": "my-space",
    "relationships": {
      "organization": {
        "data": {
          "guid": "[org-guid]"
        }
      }
    }
  }'

```
{: codeblock}
{: curl}



