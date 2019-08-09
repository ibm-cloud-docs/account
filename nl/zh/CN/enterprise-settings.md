---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, enterprise settings, manage enterprise, view enterprise, rename enterprise

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 管理企业
{: #enterprise-settings}

在 {{site.data.keyword.Bluemix}} 企业的仪表板中，可以查看企业详细信息，执行添加帐户和邀请用户等常用操作，以及查看计费信息。您还可以在仪表板上或者使用 CLI 或 API 对企业重命名。
{:shortdesc}

要管理企业设置，您需要在企业帐户中具有对企业服务的管理员或编辑者角色。
{: tip}

## 在控制台中管理企业
{: #enterprise-manage}

要查看企业仪表板，请转至**管理 > 企业**。仪表板提供了企业中的帐户、用户和预订信用值的概述。仪表板具有快速链接，以便您可以执行以下常用操作：
   * [向企业添加新帐户或现有帐户](/docs/account?topic=account-enterprise-add)
   * [邀请用户加入企业帐户](/docs/iam?topic=iam-iamuserinv)
   * [查看和管理预订信用值](/docs/billing-usage?topic=billing-usage-subscriptions)

此外，还可以通过在“企业详细信息”部分中单击**重命名**对企业重命名。

## 通过 CLI 管理企业
{: #enterprise-manage-cli}

* 查看企业信息，例如名称、域、所有者以及创建和更新日期。

  ```
  ibmcloud enterprise show
  ```
  {: codeblock}
* 通过在以下命令中的 `-n` 选项上指定新名称，对企业重命名。

   ```
   ibmcloud enterprise update -n NEW_NAME
   ```
   {:codeblock}

## 使用 API 管理企业
{: #enterprise-manage-api}

您可以如以下样本请求中所示，通过调用企业管理 API 以编程方式更新企业。可以通过在 API 调用中传递新值来更新企业名称或域。<!--For detailed information about the API, see the [Enterprise Management API documentation](https://{DomainName}/apidocs/enterprise-apis/enterprise#update-an-enterprise){: external}.-->


```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID" \
-H "Authorization: $IAM_TOKEN" \
-H 'Content-Type: application/json' \
-d '{
  "name": "Brand New Sample Enterprise",
  "domain": "new.example.com"
}'
```
