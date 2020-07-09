---

copyright:

  years: 2015, 2020
lastupdated: "2020-05-28"

keywords: service key, api key, bind, credential

subcollection: account

---

{:shortdesc: .shortdesc}
{:note: .note}
{:tip: .tip}


# Adding and viewing credentials
{: #service_credentials}

You can generate a new set of credentials for times when you want to manually connect an app or external consumer to an {{site.data.keyword.Bluemix}} service.
{: shortdesc} 

For example, if you're trying to bind an AWS app to a Watson service, you need to generate a new credential that can be used to bind them together. After your credential is created, you can [manually add](/docs/apps?topic=apps-credentials_overview) it to your {{site.data.keyword.Bluemix_notm}} app or other [external consumer](/docs/account?topic=account-externalapp) to connect your service.

To manually add credentials to your apps, refer to the documentation for the type of app or compute option that you are using.
{: tip}

## Adding a credential when binding an IAM-enabled service
{: #IAM}

Services that are managed by {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) can generate a resource key, also known as a credential. Credentials are service-specific and vary based on how each service defines the credentials they need to generate. A credential might contain a user name, password, host name, port, and a URL.

However, while the contents of each credential is unique to the service that generates it, all services managed by IAM require that new credentials include an IAM Service access role. Some services might generate more data that requires parameters to be passed in. For example, a service might require you to input a language parameter to set the default language that is returned in the resource key that is generated.

Complete the following steps to add a credential to a service that is managed by IAM:

1. From the My resources page, select the name of the service to open the service details page. Then, select the Credentials tab, and click **New Credential +**.
2. From the Add New Credential dialog, provide a **Name**.
3. Specify the role. This value sets the IAM service access role. For more information, see: [IAM Access](/docs/account?topic=account-userroles)
4. Optionally, you can provide a Service ID by either allowing IAM to generate a unique value for you, or by providing an existing Service ID. For more information, see: [Creating and working with service IDs](/docs/account?topic=account-serviceids)
5. Optionally, you can provide more parameters as a valid JSON object that contains service-specific configuration parameters, provided either inline or in a file.

  Most services don't require extra parameters, and for services that do, each service defines its own unique list of parameters. For a list of supported configuration parameters, see the documentation for the particular service offering.
  {: note}
6. Click **Add** to generate the new service credential.

## Adding a credential when binding a Cloud Foundry service
{: #cf_credential}

Cloud Foundry services can generate a service key, also known as a credential. Credentials are service-specific and vary based on how each service defines the credentials they need to generate. A service credential might contain a user name, password, host name, port, and a URL.

However, the contents of each credential is unique to the service that generates it. Some services might generate extra data that requires parameters to be passed in. For example, a service might require you to input a language parameter to set the default language that is returned in the service key that is generated.

Complete the following steps to add a Cloud Foundry credential:

1. From the service details page, select the Credentials tab, and click **New Credential +**.
2. From the Add New Credential dialog, provide a **Name**.
3. Optionally, you can provide more parameters as a valid JSON object that contains service-specific configuration parameters, provided either inline or in a file.

  Most services don't require extra parameters, and for services that do, each service defines its own unique list of parameters. For a list of supported configuration parameters, see the documentation for the particular service offering.
  {: note}
4. Click **Add** to generate the new service credential.

## Viewing a credential
{: #viewing-credentials}

After a credential is created for a service, it can be viewed at any time for users that need the API key value. However, all users must have the correct level of access to see the details of a credential including the API key value. The access of the user must be equal to or greater than that of the service credential. For example, if the credential has the IAM service role `Writer`, then the user trying to view the credential must have the IAM service role `Writer` or `Manager` for that particular service assigned. When a user doesn't have the correct access, details such as the API key value are redacted.

To view an existing service credential for a service, complete the following steps:

1. From the My resources page, select the name of the service to open the service details page. 
2. Click **Service credentials**
3. Expand **View credentials** on the row for an existing credential.


