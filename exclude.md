---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-28"

keywords: hide resource, limit viewer, exclude user, hide service

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}


# Hiding a public resource from users
{: #exclude}

As an administrator for your {{site.data.keyword.Bluemix}} account, you can hide a public resource from users who have access to the account. You might hide resources to keep sensitive information hidden from non-authorized users, or some information might only need to be accessed by a finite number of people.
{:shortdesc}

Hiding a resource in the catalog does not remove it from the Cloud Foundry command-line interface (CLI) or from the offering category list that's available from the {{site.data.keyword.Bluemix_notm}} console navigation, such as Finance, Mobile, Watson, and Web Apps.
{: note}

You can use the {{site.data.keyword.Bluemix}} [command-line interface (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) or console to determine whether you have access to allow users to view a private resource that was added to the account. If you're an account owner, you can give access to a user in your account from the console by assigning an access policy. For more information, see [Managing access to your account](/docs/account?topic=account-find-access).

## Finding a resource
{: #find-resource-exc}

Run the `ibmcloud catalog search <service-id or service-name>` command to search for a resource. Replace the service-id or service-name variables with a resource name or ID. Use the information that's returned to find the ID or name of the service that you want to hide.

## Getting the details of the resource

Run the `ibmcloud catalog service <service-id or service-name>` command. Using the information that's returned from running the previous command, use this command to examine more details about the resource. With the information that is returned, you can view the hierarchy, which shows the child resources of the items in your resource.

## Hiding the resource
{: #vis-exc}

Run the following command to prevent users in your account from viewing a public resource.

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

You can add a comma-separated list of emails or account ID associated with accounts after the excludes flag.

After you run the command, the process to hide the resource takes approximately 30 minutes. After 30 minutes, log out and log back in to your account to see the hidden resource.

Entries that you hide aren't available from the console or the CLI. Admins of the excluded account can still view the resource.
{: note}

## Removing an account from the exclusion list
{: #remove-exclude}

Run the following command to remove an account ID or email from the exclusion list.

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`


## Example: Managing the visibility of child objects
{: #child}

You can manage the visibility of all your resources. Each child resource has its individual visibility characteristics. This example shows how you can exclude an account from the Cloudant service.

Run the `ibmcloud catalog service cloudant` command to view all the children of the resource.

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

Find the ID for an object and exclude an account by running the `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>` command.

For more information about how visibility works, see the [catalog API docs](https://{DomainName}/apidocs/globalcatalog).
