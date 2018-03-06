---

copyright:

  years: 2017, 2018
lastupdated: "2017-12-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 对帐户中的用户隐藏公共资源
{: #exclude}

如果您是帐户的管理员，那么可以选择通过使用 `bx` [命令行界面](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_catalog_entry_visibility_set)将帐户中的每个人添加到排除列表，从而对此人隐藏公共资源。
{:shortdesc: .shortdesc}

**注：**在目录中隐藏项并不会从 Cloud Foundry CLI 或通过全局导航（例如，财务、移动、Watson 和 Web 应用程序）提供的服务供应列表中除去该项。

## 如何知道自己是否具有访问权？
{: #find-access}

您可以使用 CLI 或 Identity and Access UI 来确定自己是否有权允许用户查看已添加到帐户的专用资源。如果您是帐户所有者，那么可以通过在 Identity and Access Management UI 中分配访问策略，向您帐户中的用户授予访问权。有关更多信息，请参阅[管理对帐户的访问权](access.html)。

## 步骤 1：查找资源
{: #find-resource}

输入 `bx catalog search <service-id or service-name>` 以搜索资源。将 service-id 或 service-name 替换为资源名称或标识。查找要在返回的信息中隐藏的服务的标识或名称。

## 步骤 2：获取该服务的详细信息

输入 `bx catalog service <service-id or service-name>`. 使用此命令并利用在上一个命令中找到的内容来检查资源的更多详细信息。借助返回的信息，可以查看层次结构，其中会显示资源中各项的子资源。

## 步骤 3：隐藏资源
{: #vis-exc}

输入以下命令以阻止帐户查看公共资源。

`bx catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

在 excludes 标志后，可以添加与帐户关联的电子邮件或帐户标识的逗号分隔列表。

运行此命令后，隐藏资源的过程需要 30 分钟。30 分钟后，请注销并重新登录到帐户以查看隐藏的资源。

**注：**隐藏的条目在 UI 和 bx CLI 中不可用。隐藏的条目仍然会在 Cloud Foundry 市场中显示，但无法通过 Cloud Foundry 供应隐藏的套餐。已排除帐户的管理员仍可以查看该资源。

## 从排除列表中除去帐户
{: #remove-exclude}

输入以下命令以从排除列表中除去帐户标识或电子邮件。

`bx catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`

## 管理子对象可视性的示例
{: #child}

您可以管理所有资源的可视性。每个子资源都具有其单独的可视性特征。

在此示例中，可以从公共 Cloudant 服务中排除帐户。

如果输入 `bx catalog service cloudant`，那么可以查看资源的子代。

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

查找对象的标识并使用 `bx catalog entry-visibility-set <resource-id> --excludes-add<account-id or account-email>` 来排除帐户。

有关可视性工作方式的更多信息，请参阅 [API 文档](https://console.bluemix.net/apidocs/682)。
