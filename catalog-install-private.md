---

copyright:
  years: 2020, 2021
lastupdated: "2021-04-13"

keywords: catalog, catalogs, private catalogs, install software, software product, deployment target

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:javascript: .ph data-hd-programlang='javascript'}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}

# Installing software from a private catalog
{: #install-sw}

You can install software that's been added to a private catalog if you're the catalog owner or you have the required access to it. 
{: shortdesc} 

## Before you begin
{: #prereq-installsw}

To complete this task, you need to be assigned the following roles:

* Viewer role on the catalog management service
* Administrator and manager roles on the cluster
* Viewer role on all resource groups. Select **No service access**, a resource group name, then the role, and repeat for each resource group.

For more information, see [Assigning catalog management access](/docs/account?topic=account-catalog-access).

## Installing software by using the console
{: #installsw-console}
{: ui}

1. Click **Catalog** in the console menu bar.
2. Select the name of the catalog from the list of catalogs. 
1. Click **Private** > the software type that you want to install.
1. Select a cluster, and enter one of the following values:

   * A namespace if your deployment target is IBM Kubernetes Service. 
   * A project name if your deployment target is Red Hat OpenShift. 
   
  You can install software to clusters that are deployed to classic {{site.data.keyword.cloud}} infrastructure. Installing software to clusters that are deployed to {{site.data.keyword.cloud_notm}} Virtual Private Cloud is currently not supported.
  {: note}
  
1. Click **Install**.

## Installing software by using the API
{: #installsw-api}
{: api}

To install sowftware that's been added to a private catalog, call the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog#install-version){: external} as shown in the following example request: 

```java
String authRefreshToken = "{authRefreshToken}";
String versionLocator = "{versionLocator}";
InstallVersionOptions installOptions = new InstallVersionOptions.Builder().xAuthRefreshToken(authRefreshToken).versionLocatorId(versionLocator).build();
Response<Void> response = service.installVersion(installOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
versionLocator = "{versionLocator}";
authRefreshToken = "{authRefreshToken}";
response = await service.installVersion({ 'versionLocatorId': versionLocator, 'xAuthRefreshToken': authRefreshToken });
console.log(response);
```
{: codeblock}
{: javascript}

```python
authRefreshToken="{authRefreshToken}"
versionLocator = "{versionLocator}"
response = self.service.install_version(version_locator_id=versionLocator, x_auth_refresh_token=authRefreshToken)
print(response)
```
{: codeblock}
{: python}

```go
versionLocator := "{versionLocator}"
authRefreshToken := "{authRefreshToken}"
installOptions := service.NewInstallVersionOptions(versionLocator, authRefreshToken)
response, _ := service.InstallVersion(installOptions)
fmt.Println(response)
```
{: codeblock}
{: go}

The [pre-install](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=go#preinstall-version) is only necessary for offerings where cluster configuration is required.
{: note}
