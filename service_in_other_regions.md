---

copyright:
  years: 2015, 2021
lastupdated: "2021-09-24"

keywords: service availability, service location, using services across regions

subcollection: account

---

{:shortdesc: .shortdesc}

# Using services in another region
{: #cross_region_service}

If you have a service instance that is created and bound to apps in one region, you can use this service instance in another region by one of the following methods:
{: shortdesc}

* Use the service credentials to configure your app instance directly. See [Connecting services to external apps](/docs/account?topic=account-externalapp) for details.
* Create a user-provided service as a bridge.

To use a service instance that exists in another region, complete the following steps:

1. To switch to the region where the service instance exists, click the **Navigation menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list**. Then, expand the **LOCATION** menu and select the region.

2. Retrieve the credentials and the connection parameters from the VCAP_SERVICES environment variable of the service instance in the region where the service exists. Complete the following steps:
   1. In the {{site.data.keyword.Bluemix_notm}} Dashboard, click **View all** on your apps tile. The Overview page is displayed.
   2. In the navigation pane, click **Credentials**. The *VCAP_SERVICES* environment variable details are displayed. Record the JSON content for the service instance.

3. Switch to the region where you want to use the service instance. Click the **Navigation menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list**. Then, expand the **LOCATION** menu and select the region where you want to use the service instance.

4. Create a user-provided service instance by using the credentials and connection parameters that you recorded from the *VCAP_SERVICES* environment variable.

5. Bind the user-provided service instance to your app by using the following command:

   ```bash
   ibmcloud service bind myapp user-provided_service_instance
   ```
   {: pre}
