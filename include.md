---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Adding accounts to your private resource
{: #include}

Any private resource that you create is restricted by default. If you're an administrator for the account, you can choose who can see your resource by adding them to an inclusion list with the {{site.data.keyword.Bluemix}} [command line interface](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set).
{:shortdesc: .shortdesc}

## How do I know whether I have access?
{: #find-access}

You can use the CLI or the Identity and Access UI to determine whether you have access to allow users to view a private resource that was added to the account. If you're an account owner, you can give access to a user in your account through the Identity and Access Management UI by assigning an access policy. For more information, see [Managing access to your account](access.html).

## Step 1: Find your resource
{: #find-resource}

Enter `ibmcloud catalog service <service-id or service-name>`. Replace service-id or service-name with your resource name or ID. With the information that returns, you can see the hierarchy, which shows the child resources of the items in your resource.

## Step 2: Set the visibility by including an account
{: #vis-inc}

Enter the following command to allow an account to see your private resource.

`ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

After the includes-add flag, you can add a comma-separated list of emails or IDs associated with accounts.

After you run the command, the process to include the resource takes 30 minutes. After 30 minutes, log out and back in to your account to see the included resource.

## Remove an account from the inclusion list
{: #remove-exclude}

Enter the following command to remove an account from the `includes` list.

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## Managing visibility of child objects
{: #child-vis}

You can manage the visibility of your resource or its children.

An empty includes list means that only your account administrators can see it. Your account must be on the inclusion list for all members of the account to see it.

For example, if you enter `ibmcloud catalog service <your_service>`, you can see the resource's children.

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

You can get the resource ID for the child deployment and then include an account by using the following command. `ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`.

The children of an object can inherit visibility in complex ways. If the child object is private, it has its own visibility configuration. However, if the child object is set to public, it inherits the visibility of its parent. Setting visibility on a private child object might restrict its visibility more than the parent.

For more information about how visibility works, see the [API docs](https://console.bluemix.net/apidocs/682).
