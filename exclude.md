---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Hiding a public resource from users in your account
{: #exclude}

If you're an administrator for your account, you can hide a public resource for everyone in your account. Add the resource to an exclusion list with the `ibmcloud` [command line interface](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set).
{:shortdesc: .shortdesc}

**Note:** Hiding a resource in the catalog does not remove it from the Cloud Foundry CLI or from the service provisioning lists available through the global navigation, such as Finance, Mobile, Watson, and Web Apps.

## How do I know whether I have access?
{: #find-access}

You can use the CLI or the Identity and Access UI to determine whether you have access to allow users to view a private resource that was added to the account. If you're an account owner, you can give access to a user in your account through the Identity and Access Management UI by assigning an access policy. For more information, see [Managing access to your account](access.html).

## Step 1: Find a resource
{: #find-resource}

Enter `ibmcloud catalog search <service-id or service-name>` to search for a resource. Replace service-id or service-name with a resource name or ID. Find the ID or name of the service you want to hide in the information that returns.

## Step 2: Get the details of that service

Enter `ibmcloud catalog service <service-id or service-name>`. Using what you found in the previous command, use this command to examine more details of the resource. With the information that returns, you can see the hierarchy, which shows the child resources of the items in your resource.

## Step 3: Hide the resource
{: #vis-exc}

Enter the following command to prevent your account from seeing a public resource.

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

After the `excludes` flag, you can add a comma-separated list of emails or account ID associated with accounts.

After you run the command, the process to hide the resource takes 30 minutes. After 30 minutes, log out and back in to your account to see the hidden resource.

**Note:** Entries that you hide are not available from the UI and {{site.data.keyword.Bluemix}} CLI. The hidden entries are still visible in the Cloud Foundry marketplace, but a hidden plan cannot be provisioned from Cloud Foundry. Admins of the excluded account can still see the resource.

## Remove an account from the exclusion list
{: #remove-exclude}

Enter the following command to remove an account ID or email from the exclusion list.

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`

## Managing visibility of child objects example
{: #child}

You can manage the visibility of all your resources. Each child resource has its individual visibility characteristics.

In this example, you can exclude an account from the public Cloudant service.

If you enter `ibmcloud catalog service cloudant`, you can see the resource's children.

```
ID                 cloudant
Name               cloudantnosqldb
Kind               service
Provider           IBM
Tags               data_management, ibm_created, ibm_dedicated_public, lite
Active             true
Description        Cloudant NoSQL DB is a fully managed data layer designed for modern web and mobile applications that leverages a flexible JSON schema. Cloudant is built upon and compatible with Apache CouchDB and accessible through a secure HTTPS API, which scales as your application grows. Cloudant is ISO27001 and SOC2 Type 1 certified, and all data is stored in triplicate across separate physical nodes in a cluster for HA/DR within a data center.
Bindable           true
RC Compatible      false
RC Provisionable   false
Children           Name                                          Kind         ID                                               Location
                   lite                                          plan         cloudant-lite
                   |__lite-eu-gb                             deployment   cloudant-lite:eu-gb                          eu-gb
                   |  |__lite-alias-eu-gb                    alias        cloudant-lite:alias:eu-gb                    eu-gb
                   |__lite-us-south                          deployment   cloudant-lite:us-south                       us-south
                      |__lite-alias-us-south                 alias        cloudant-lite:alias:us-south                 us-south
                   standard                                      plan         cloudant-standard
                   |__standard-eu-gb                         deployment   cloudant-standard:eu-gb                      eu-gb
                   |  |__standard-alias-eu-gb                alias        cloudant-standard:alias:eu-gb                eu-gb
                   |__standard-us-south                      deployment   cloudant-standard:us-south                   us-south
                      |__standard-alias-us-south             alias        cloudant-standard:alias:us-south             us-south
```

Find the ID for an object and exclude an account with the `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

For more information about how visibility works, see the [API docs](https://console.bluemix.net/apidocs/682).
