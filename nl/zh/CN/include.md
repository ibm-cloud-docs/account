---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 向专用资源添加帐户
{: #include}

缺省情况下，您创建的任何专用资源都会受到限制。如果您是帐户的管理员，那么可以选择通过使用 {{site.data.keyword.Bluemix}} [命令行界面](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set)将用户添加到包含列表，从而使其可以查看您的资源。
{:shortdesc: .shortdesc}

## 如何知道自己是否具有访问权？
{: #find-access}

您可以使用 CLI 或 Identity and Access UI 来确定自己是否有权允许用户查看已添加到帐户的专用资源。如果您是帐户所有者，那么可以通过在 Identity and Access Management UI 中分配访问策略，向您帐户中的用户授予访问权。有关更多信息，请参阅[管理对帐户的访问权](access.html)。

## 步骤 1：查找资源
{: #find-resource}

输入 `ibmcloud catalog service <service-id or service-name>`. 将 service-id 或 service-name 替换为资源名称或标识。借助返回的信息，可以查看层次结构，其中会显示资源中各项的子资源。

## 步骤 2：通过包含帐户来设置可视性
{: #vis-inc}

输入以下命令以允许帐户查看您的专用资源。

`ibmcloud catalog entry-visibility-set <service-id> --includes-add<account-id or account-email>`

在 includes-add 标志后，可以添加与帐户关联的电子邮件或标识的逗号分隔列表。

运行此命令后，包含资源的过程需要 30 分钟。30 分钟后，请注销并重新登录到帐户以查看包含的资源。

## 从包含列表中除去帐户
{: #remove-exclude}

输入以下命令以从 `includes` 列表中除去帐户。

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove<account-id or account-email>`

## 管理子对象的可视性
{: #child-vis}

您可以管理资源或其子代的可视性。

包含列表为空意味着仅帐户管理员可以查看该列表。您的帐户必须位于包含列表中，该帐户的所有成员才可查看该列表。

例如，如果输入 `ibmcloud catalog service <your_service>`，那么可以查看资源的子代。

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

您可以获取资源标识用于子代部署，然后使用以下命令来包含帐户。`ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`.

对象的子代可以通过复杂方式来继承可视性。如果子对象是私有对象，那么它会具有自己的可视性配置。但是，如果将该子对象设置为公共，那么它会继承其父代的可视性。在专用子对象上设置可视性可能会使其可视性比父代更受限制。

有关可视性工作方式的更多信息，请参阅 [API 文档](https://console.bluemix.net/apidocs/globalcatalog)。
