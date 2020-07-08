---

copyright:
  years: 2017, 2020
lastupdated: "2020-06-10"

keywords: create connection, connect a service, bind, alias

subcollection: account

---

{:shortdesc: .shortdesc}

# Managing connections
{: #connect_app}

You can connect a service to an existing or new {{site.data.keyword.Bluemix}} application from the Connections tab on your service dashboard. You can add more connections or delete connections from the Connections tab.
{: shortdesc}

However, when you connect a service instance that is managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) to an application, an alias of the service that is managed by IAM is automatically created in the corresponding space with the connection information that you specified. This alias is represented as a service instance of your IAM-managed service.
{:shortdesc}

## What is an alias?
{: #what_is_alias}

An alias is a connection between your IAM-managed service within a resource group and an application within an org or a space. In the {{site.data.keyword.Bluemix_notm}} console, the connection (alias) is represented as a service instance. You can manage your alias by modifying the service instance that represents your connection.

Aliases are like symlinks that hold references to remote resources and enable interoperability and reuse of an instance across the platform. For example, you can create an instance of a service in a resource group and then reuse it from any available region by creating an alias in an org or space in those regions.

The following rules apply to aliases:

* There's no extra charge for an alias, but each alias counts against your quota in your organization.
* You can create only one alias per space in the {{site.data.keyword.Bluemix_notm}} console. However, more than one alias per space can be created by using the {{site.data.keyword.Bluemix_notm}} CLI. For more information, see [Working with resources and resource groups](/docs/cli?topic=cli-ibmcloud_commands_resource).
* You can create multiple connections between your IAM-managed service and any application in any space, organization, and region in the same account if you have permission.
* Multiple connections that are made in the same space to different apps from an IAM-managed service instance use the same alias.
* Unbinding an IAM-managed service instance *doesn't* delete the service instance that represents the alias.
* Deleting the application that your IAM-managed service instance is connected to *doesn't* delete the instance that represents the alias.
* Deleting an IAM-managed service instance *deletes* the service instance that represents the alias.

## Creating a connection (alias) between an IAM-managed service and an app
{: #creating_alias}

To connect your IAM-managed service instance to an application:

1. Go to your dashboard.

2. Click the name of your app to open the app details view.

3. Click **Connect existing** and choose from your existing app. Or click **Create connection** to create an app to connect to.

4. Specify the **Access Role for connection**. This value sets the IAM service access role. For more information, see [IAM access](/docs/account?topic=account-userroles).

5. Optionally, you can provide a **Service ID for connection** by either allowing IAM to generate a unique value for you, or by providing an existing service ID. For more information, see [Creating and working with service IDs](/docs/account?topic=account-serviceids).

6. Click **Create**.

## Viewing an alias
{: #view_alias}

After you create a connection between an IAM-managed service and an app, the alias is displayed on the Connections tab of the connected app. Additionally, the alias is displayed as a running service instance on your resource list, and contains a Connections tab only when you open it.

1. Go to the your resource list.
2. From the **Application Services** table, click the name of the service instance to open the service details view. If it has a Connections tab only, it's an alias.

## Deleting an alias
{: #delete_alias}

The easiest way to delete the alias is to delete the IAM-managed service instance. However, you can maintain your IAM-managed service instance and instead delete the alias directly.

1. Go to the your resource list.
2. From the **Application Services** table, click the name of the service instance to open the service details view. If it has a Connections tab only, it's an alias.
3. Delete the instance.

## Creating a connection between multiple services
{: #multiple_services}

For more information, see [Using services in another service](/docs/account?topic=account-s2s_binding).
