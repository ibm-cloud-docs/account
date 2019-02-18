---

copyright:

  years: 2017, 2019
lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Adding accounts to your private resource
{: #include}

Any {{site.data.keyword.Bluemix}} private resource that you create is restricted by default. If you're an administrator for the account, you can choose who can view your resource by adding the user to an inclusion list.
{:shortdesc: .shortdesc}

You can use the {{site.data.keyword.Bluemix}} [command-line interface (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) or console to determine whether you have access to allow users to view a private resource that was added to the account. If you're an account owner, you can give access to a user in your account from the console by assigning an access policy. For more information, see [Managing access to your account](/docs/account?topic=account-find-access).

## Finding your resource
{: #find-resource}

Run the `ibmcloud catalog service <service-id or service-name>` command. Replace the service-id or service-name variables with your resource name or ID. Use the information that is returned to view the hierarchy, which shows the child resources of the items in your resource.

## Setting the visibility by including an account
{: #vis-inc}

Run the following command to allow an account to see your private resource.

`ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

After the includes-add flag, you can add a comma-separated list of emails or IDs associated with accounts.

After you run the command, the process to include the resource takes approximately 30 minutes. After 30 minutes, log out and back in to your account to see the included resource.

## Removing an account from the inclusion list
{: #remove-exclude}

Run the following command to remove an account from the includes list.

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## Example: Managing the visibility of child objects
{: #child-vis}

You can manage the visibility of your resource or its children. An empty includes list means that only the account administrators can view it. Your account must be included in the inclusion list for all members of the account to view it.

The following example shows how you can run the the `ibmcloud catalog service cloudant` command to view the children of a Cloudant service instance.

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

You can get the resource ID for the child deployment, and then include an account by running the following command:

`ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`

The children of an object can inherit visibility in complex ways. If the child object is private, it has its own visibility configuration. However, if the child object is set to public, it inherits the visibility of its parent. Setting visibility on a private child object might restrict its visibility to more than the parent. For more information about how visibility works, see the [Catalog API docs](https://{DomainName}/apidocs/globalcatalog).

## Transferring ownership of a private resource
{: #owners}

If you leave your project or organization, you might want to transfer ownership of your account to someone else.
{:shortdesc}

After you transfer ownership, you can no longer view the resource from your account. Make sure you want to transfer ownership, because this action can't be undone.
{: important}

You can use the [{{site.data.keyword.Bluemix}} command-line interface (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) to transfer ownership of a private resource. Run the following command:

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
