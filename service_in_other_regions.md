---

copyright:

  years: 2015, 2026
lastupdated: "2026-02-04"

keywords: service availability, service location, using services across regions

subcollection: account

---

{{site.data.keyword.attribute-definition-list}} 

# Using services in another region
{: #cross_region_service}

If you have a service instance that is created and bound to apps in one region, you can use this service instance in another region by one of the following methods:
{: shortdesc}

* Use the service credentials to configure your app instance directly. See [Connecting services to apps](/docs/account?topic=account-service_credentials) for details.
* Create a user-provided service as a bridge.

To use a service instance that exists in another region, complete the following steps:

1. To switch to the region where the service instance exists, click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list**. Then, expand the **LOCATION** menu and select the region.

2. Retrieve the credentials and the connection parameters from the VCAP_SERVICES environment variable of the service instance in the region where the service exists. Complete the following steps:
   1. In the {{site.data.keyword.cloud_notm}} Dashboard, click **View all** on your apps tile. The Overview page is displayed.
   2. In the navigation pane, click **Credentials**. The *VCAP_SERVICES* environment variable details are displayed. Record the JSON content for the service instance.

3. Switch to the region where you want to use the service instance. Click the **Navigation Menu** icon ![Navigation Menu icon](../icons/icon_hamburger.svg "Menu") > **Resource list**. Then, expand the **LOCATION** menu and select the region where you want to use the service instance.

4. Create a user-provided service instance by using the credentials and connection parameters that you recorded from the *VCAP_SERVICES* environment variable.

5. Configure your application to use the service credentials. You can do this by setting environment variables or updating your application's configuration file:

   **Using environment variables:**
   
   ```bash
   export SERVICE_USERNAME="appuser"
   export SERVICE_PASSWORD="sec123"
   export SERVICE_URL="https://api.example.com"
   ```
   {: pre}

   **Using a configuration file (example for Node.js):**
   
   ```json
   {
     "service": {
       "username": "appuser",
       "password": "sec123",
       "url": "https://api.example.com"
     }
   }
   ```
   {: codeblock}

   Then, reference these credentials in your application code to connect to the service in the other region.
