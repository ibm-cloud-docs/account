---


copyright:
  years: 2020, 2021
lastupdated: "2021-04-13"

keywords: license, entitlement, software, passport advantage, cloud pak, binding a license, PPA, part number

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:pre: .pre}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:download: .download}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:ruby: .ph data-hd-programlang='ruby'}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}

# Assigning software licenses to your account
{: #software-license}

To install software products in {{site.data.keyword.cloud}}, the license for the software must be assigned to your account. You're entitled to install a specific version of the software for a specific period of time, for example, one year. Licenses, which are also referred to as entitlements, are purchased and acquired through {{site.data.keyword.IBM}} Passport Advantage. 
{: shortdesc}

## Acquiring a license 
{: #acquire-license}

In most cases, someone in a procurement or financial role in your organization works with an {{site.data.keyword.cloud_notm}} sales representative to purchase the license through [{{site.data.keyword.IBM_notm}} Passport Advantage](https://www.ibm.com/software/passportadvantage/index.html){: external}. A part number is associated with the license for the software product to be used in {{site.data.keyword.cloud_notm}}. The person acquiring the license is not typically the same person who installs the software in the {{site.data.keyword.cloud_notm}} account. After a sales representative acquires the license through the Software Quote Order tool, it must be assigned to each account that requires entitlement for use of the software in {{site.data.keyword.cloud_notm}}. 

## Assigning licenses to an account
{: #assign-license}
{: ui}

When you assign licenses to your account, all users with access to your account can use them to install the software to which the licenses apply. If the procurement focal is not the owner of the account to which the license must be assigned, they must be assigned the administrator role on the [License and entitlement account management service](/docs/account?topic=account-account-services#license-entitlement-management). 

Complete the following steps to assign a license to an account:
1. Log in to the console and go to **Manage** > **Account**.
2. Click **Licenses**. 
1. If you don't have any licenses assigned to the account, click **Check {{site.data.keyword.IBM_notm}} Passport Advantage** to find all the licenses that are tied to your IBMid. If you have existing licenses, click **Assign** to assign more licenses to the account.

You can unassign a license from the account. Note, however, any {{site.data.keyword.bplong_notm}} workspaces in which the license is used will be impacted. 
{: important}

## Assigning licenses to an account by using the API
{: #assign-license-api}
{: api}

When you assign licenses to your account, all users with access to your account can use them to install the software to which the licenses apply. If the procurement focal is not the owner of the account to which the license must be assigned, they must be assigned the administrator role on the [License and entitlement account management service](/docs/account?topic=account-account-services#license-entitlement-management). 

To assign a license to an account, call the [Catalog Management API](https://cloud.ibm.com/apidocs/resource-catalog/private-catalog?code=java#create-license-entitlement){: external} as shown in the following example request:

```java
String name = "{name}";
CreateLicenseEntitlementOptions createOptions = new CreateLicenseEntitlementOptions.Builder().name(name).build();
Response<LicenseEntitlement> response = service.createLicenseEntitlement(createOptions).execute();
System.out.println(response.getResult());
```
{: codeblock}
{: java}

```javascript
name = "{name}";
response = await service.createLicenseEntitlement({ 'name': name } );
console.log(response);
```
{: codeblock}
{: javascript}

```python
name = "{name}"
response = self.service.create_license_entitlement(name=name)
print(response)
```
{: codeblock}
{: python}

```go
createOptions := service.NewCreateLicenseEntitlementOptions()
createOptions.SetName("{name}")
_, response, _ := service.CreateLicenseEntitlement(createOptions)
fmt.Println(response)
```
{: codeblock}
{: go}

You can unassign a license from the account. Note, however, any {{site.data.keyword.bplong_notm}} workspaces in which the license is used will be impacted. 
{: important}
