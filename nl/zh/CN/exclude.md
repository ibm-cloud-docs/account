---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-28"

keywords: hide resource, limit viewer, exclude user, hide service

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}


# 对用户隐藏公共资源
{: #exclude}

作为 {{site.data.keyword.Bluemix}} 帐户管理员，您可以对有权访问帐户的用户隐藏公共资源。您可以隐藏资源，使敏感信息对未经授权的用户隐藏，或者某些信息可能只需要由有限数量的人员访问。
{:shortdesc}

在目录中隐藏资源并不会从 Cloud Foundry 命令行界面 (CLI) 或通过 {{site.data.keyword.Bluemix_notm}} 控制台导航（例如，财务、移动、Watson 和 Web 应用程序）提供的产品类别列表中除去该资源。
{: note}

您可以使用 {{site.data.keyword.Bluemix}} [命令行界面 (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) 或控制台来确定自己是否有权允许用户查看已添加到帐户的专用资源。如果您是帐户所有者，那么可以通过在控制台中分配访问策略，向您帐户中的用户授予访问权。有关更多信息，请参阅[管理对帐户的访问权](/docs/account?topic=account-find-access)。

## 查找资源
{: #find-resource-exc}

运行 `ibmcloud catalog search <service-id or service-name>` 命令以搜索资源。将 service-id 或 service-name 变量替换为资源名称或标识。使用返回的信息来查找要隐藏的服务的标识或名称。

## 获取资源的详细信息

运行 `ibmcloud catalog service <service-id or service-name>` 命令。使用此命令并利用通过运行先前命令返回的信息，可检查有关资源的更多详细信息。借助返回的信息，可以查看层次结构，其中会显示资源中各项的子资源。

## 隐藏资源
{: #vis-exc}

运行以下命令以阻止帐户中的用户查看公共资源。

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

在 excludes 标志后，可以添加与帐户关联的电子邮件或帐户标识的逗号分隔列表。

运行此命令后，隐藏资源的过程大约需要 30 分钟。30 分钟后，请注销并重新登录到帐户以查看隐藏的资源。

隐藏的条目无法通过控制台或 CLI 使用。但被排除帐户的管理员仍可以查看该资源。
{: note}

## 从排除列表中除去帐户
{: #remove-exclude}

运行以下命令以从排除列表中除去帐户标识或电子邮件。

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`


## 示例：管理子对象的可视性
{: #child}

您可以管理所有资源的可视性。每个子资源都具有其单独的可视性特征。此示例显示了可以如何从 Cloudant 服务中排除帐户。

运行 `ibmcloud catalog service cloudant` 命令以查看资源的所有子代。

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

查找对象的标识并运行 `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>` 命令来排除帐户。

有关可视性工作方式的更多信息，请参阅[目录 API 文档](https://{DomainName}/apidocs/globalcatalog)。
