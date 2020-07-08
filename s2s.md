---

copyright:
  years: 2015, 2019
lastupdated: "2019-12-11"

keywords: service authorization, service instance's access, connect service to app

subcollection: account

---
 
{:shortdesc: .shortdesc}
{:tip: .tip}
{:note: .note}
{:important: .important}

# Connecting services to a Cloud Foundry app
{: #s2s_binding}

To use a service in a Cloud Foundry app, you must create a connection or bind that service to the app.
{: shortdesc}

To connect a service to your app by starting from the details page for a specific service, complete the following steps:

You can also create connections from your app to the service. Select your app from the My resources page, go to the **Connections** menu, and select the service.
{: note}

1. On the My resources page, click **Services** and select the service that you want to access. The service details page is displayed.
2. Click **Connections** in the navigation.
3. Click **Create connection**.
4. Click **Connect** for the row of the app that you want to create the connection for.
5. Select an access role to assign to the connection. This role defines the allowable actions that can be performed by the app accessing the service.
6. Optional: Select, create, or auto-generate a service ID for the app to use to access the service. This service ID is assigned the access role that you selected in the previous step, and if you do not select an option, one is generated.
7. Optional: Add configuration parameters in JSON format.
8. Click **Connect & restage app**.


If you want to restrict an app's access to the service instance, click **Connections** in the navigation pane and then click **Unbind** in the menu for the connected application to remove the service binding.
{: tip}
