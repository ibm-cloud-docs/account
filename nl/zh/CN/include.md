---

copyright:
  years: 2017, 2019
lastupdated: "2019-06-19"

keywords: add user, share resource, private resource, share catalog, find resource, set visibility

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# 向专用资源添加帐户
{: #include}

缺省情况下，您创建的任何 {{site.data.keyword.Bluemix}} 专用资源都会受到限制。如果您是帐户的管理员，那么可以通过向包含列表添加用户来选择谁可以查看您的资源。
您还可以转移专用资源的所有权。
{:shortdesc}

您可以使用 {{site.data.keyword.Bluemix}} [命令行界面 (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) 或控制台来确定自己是否有权允许用户查看已添加到帐户的专用资源。如果您是帐户所有者，那么可以通过在控制台中分配访问策略，向您帐户中的用户授予访问权。有关更多信息，请参阅[管理对帐户的访问权](/docs/account?topic=account-find-access)。

## 查找资源
{: #find-resource-inc}

运行 `ibmcloud catalog service <service-id or service-name>` 命令。将 service-id 或 service-name 变量替换为资源名称或标识。使用返回的信息来查看层次结构，该层次结构显示资源中各项的子资源。

## 通过包含帐户来设置可视性
{: #vis-inc}

运行以下命令以允许帐户查看您的专用资源。

```
ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>
```
{:codeblock}

在 includes-add 标志后，可以添加与帐户关联的电子邮件或标识的逗号分隔列表。

运行此命令后，包含资源的过程大约需要 30 分钟。30 分钟后，请注销并重新登录到帐户以查看包含的资源。

## 从包含列表中除去帐户
{: #remove-include}

运行以下命令以从包含列表中除去帐户。

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## 示例：管理子对象的可视性
{: #child-vis}

您可以管理资源或其子代的可视性。包含列表为空意味着仅帐户管理员可以查看该资源。您的帐户必须位于包含列表中，该帐户的所有成员才可查看该资源。

以下示例显示了如何运行 `ibmcloud catalog service cloudant` 命令来查看 Cloudant 服务实例的子代。

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

您可以获取子代部署的资源标识，然后通过运行以下命令来包含帐户：

```
ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>
```
{:codeblock}

对象的子代可以通过复杂方式来继承可视性。如果子对象是私有对象，那么它会具有自己的可视性配置。但是，如果将该子对象设置为公共，那么它会继承其父代的可视性。在专用子对象上设置可视性可能会使其可视性比父代更受限制。有关可视性工作方式的更多信息，请参阅[目录 API 文档](https://{DomainName}/apidocs/globalcatalog)。

## 转移专用资源的所有权
{: #owners}

如果您离开项目或组织，您可能希望将您帐户中的资源的所有权转移给其他某个人。


转移所有权后，您无法再查看您帐户中的资源。确保您确实希望转移所有权，因为此操作无法撤销。
{: important}

您可以使用 [{{site.data.keyword.Bluemix}} 命令行界面 (CLI)](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) 来转移专用资源的所有权。运行以下命令：

```
ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>
```
{:codeblock}
