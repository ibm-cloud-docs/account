---

copyright:
  years: 2015, 2022
lastupdated: "2022-06-03"

keywords: service authorization, service instance's access, connect service to app

subcollection: account

---
 
{{site.data.keyword.attribute-definition-list}}

# Connecting services to a Cloud Foundry app
{: #s2s_binding}

To use a service in a Cloud Foundry app, you must create a connection or bind that service to the app.
{: shortdesc}

IBM Cloud Foundry Public is deprecated. For more information, see the [Deprecation of IBM Cloud Foundry](/docs/cloud-foundry-public?topic=cloud-foundry-public-deprecation).
{: deprecated}

## Connect a service to your Cloud Foundry app in the console
{: #s2s_binding-ui}
{: ui}

To connect a service to your app by starting from the details page for a specific service, complete the following steps:

You can also create connections from your app to the service. Select your app from the Resource list page, go to the **Connections** menu, and select the service.
{: note}

1. On the Resource list page, click **Services** and select the service that you want to access. The service details page is displayed.
2. Click **Connections** in the navigation.
3. Click **Create connection**.
4. Click **Connect** for the row of the app that you want to create the connection for.
5. Select an access role to assign to the connection. This role defines the allowable actions that can be performed by the app accessing the service.
6. Optional: Select, create, or auto-generate a service ID for the app to use to access the service. This service ID is assigned the access role that you selected in the previous step, and if you do not select an option, one is generated.
7. Optional: Add configuration parameters in JSON format.
8. Click **Connect & restage app**.


If you want to restrict an app's access to the service instance, click **Connections** in the navigation pane and then click **Unbind** in the menu for the connected application to remove the service binding.
{: tip}

## Connect a service to your Cloud Foundry app by using the API
{: #s2s_binding-api}
{: api}

To connect a service to your Cloud Foundry app, call the [Cloud Foundy API](http://v3-apidocs.cloudfoundry.org/version/3.99.0/index.html#manifests){: external} as shown in the following steps. 

1. Open the manifest YAML file for for applying bulk configurations to apps and their underlying processes.
1. Create a new service bindings between the app and a service instance as shown in the following manifest example. In the service-level configuration, `name` is the name of the service instance to be bound to. `binding_name` is the name of the service binding to be created. `parameters` is a map of arbitrary key/value pairs to send to the service broker during binding. 

   ```bash
   ---
   version: 1
   applications:
   - name: app1
    buildpacks:
    - ruby_buildpack
    - java_buildpack
    env:
      VAR1: value1
      VAR2: value2
    routes:
    - route: route.example.com
    - route: another-route.example.com
    services:
    - my-service1
    - my-service2
    - name: my-service-with-arbitrary-params
      binding_name: my-binding
      parameters:
        key1: value1
        key2: value2
    stack: cflinuxfs3
    metadata:
      annotations:
        contact: "bob@example.com jane@example.com"
      labels:
        sensitive: true
    processes:
    - type: web
      command: start-web.sh
      disk_quota: 512M
      health-check-http-endpoint: /healthcheck
      health-check-type: http
      health-check-invocation-timeout: 10
      instances: 3
      memory: 500M
      timeout: 10
    - type: worker
      command: start-worker.sh
      disk_quota: 1G
      health-check-type: process
      instances: 2
      memory: 256M
      timeout: 15
   - name: app2
    env:
      VAR1: value1
    processes:
    - type: web
      instances: 1
      memory: 256M
    sidecars:
    - name: authenticator
      process_types: [ 'web', 'worker' ]
      command: bundle exec run-authenticator
      memory: 800M

    - name: upcaser
      process_types: [ 'worker' ]
      command: ./tr-server
      memory: 2G
   ```
   {: codeblock}

1. Apply changes specified in the manifest to the named app as shown in the following example request.

   ```curl
   curl "https://api.example.org/v3/spaces/[guid]/actions/apply_manifest" \
    -X POST \
    -H "Authorization: bearer [token]" \
    -H "Content-type: application/x-yaml" \
    --data-binary @/path/to/manifest.yml
   ```
   {: codeblock}
