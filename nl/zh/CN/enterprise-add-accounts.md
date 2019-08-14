---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise, add account, import account, create account

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 向企业添加帐户
{: #enterprise-add}

您可以通过向企业添加更多 {{site.data.keyword.Bluemix}} 帐户来扩建企业。要添加帐户，可以导入不位于其他企业中的现有帐户，也可以在企业中创建新帐户。
{:shortdesc}

企业有多个帐户后，可以使用帐户组来组织相关帐户。有关更多信息，请参阅[在企业中组织帐户](/docs/account?topic=account-enterprise-organize)。

## 导入现有帐户
{: #add-accounts}

您可以将现有帐户导入到企业。导入帐户后，即无法将其除去，并且每个帐户只能属于一个企业。如果导入轻量或试用帐户，那么会自动将其升级为[现收现付帐户](/docs/account?topic=account-accounts)。

将帐户导入企业具有以下影响：
* 帐户的计费会转换为由企业进行管理。转换之后，帐户中的用户即无法访问未来结算周期的帐单和付款信息，例如发票、付款或预订。要使这些用户能够查看或管理计费，需要邀请他们加入企业帐户，并在该帐户中向其授予对计费服务的访问权。有关更多信息，请参阅[集中管理企业的计费和使用情况](/docs/billing-usage?topic=billing-usage-enterprise)。
* 帐户中的用户和访问许可权不会更改。帐户中的访问权与企业相分离，并且在导入帐户时，用户并不会自动获得企业中的访问权。
* 帐户中的资源不会更改。具有正确访问许可权的用户可以继续查看帐户中资源的使用情况信息。

要将现有帐户导入到企业，需要以下访问权：

   * 在要导入的帐户中，您必须是帐户所有者，或在帐户中具有对计费服务的管理员角色。
   * 在企业帐户中，您需要具有对企业服务的编辑者或管理员角色以及对计费服务的管理员角色。

要导入现有帐户，请完成以下步骤：

1. 登录到企业帐户，然后转至**管理 > 企业**。
1. 单击**帐户**以查看企业中的帐户和帐户组。在“帐户”部分中，选择**添加 > 导入帐户**。
1. 选择要导入的帐户。

   如果未显示任何帐户，说明您可能在任何现有帐户中都没有正确的访问权。
  {: tip}
1. 如果要将帐户添加到帐户组，请选择要作为其父代的帐户组。您选择的父代将确定该帐户在企业层次结构中的位置。
1. 查看有关帐户所受影响的信息，然后选择**我了解对帐户的影响**。然后，单击**导入**。

   将帐户导入到企业后，即无法将其除去。请确保要将帐户永久移至企业。
   {: important}

### 使用 CLI 导入帐户
{: #add-account-cli}

1. 查找要导入到企业的帐户的标识。

   ```
ibmcloud account list
```
   {: codeblock}
1. 如果要将帐户添加到帐户组，请在企业中查找现有帐户组的名称和标识。

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. 将帐户导入到企业，并为 `--account ID` 参数指定帐户标识。如果未指定父帐户组，那么帐户将添加到企业正下方。

   ```
   ibmcloud enterprise account-import --account-id ID
   [--parent-account-group ACCOUNT_GROUP_NAME | --parent-account-group-id ACCOUNT_GROUP_ID]
   ```
   {: codeblock}

### 使用 API 导入帐户
{: #add-account-api}

要将现有帐户导入到企业，请如以下样本请求中所示调用[企业管理 API](https://{DomainName}/apidocs/enterprise-apis/enterprise#import-an-account-into-an-enterprise){: external}。将 {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) 令牌和标识变量替换为企业中的值。

```
curl -X PUT \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID/import/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" -H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID"
}'
```
{: codeblock}

## 创建新帐户
{: #create-accounts}

您可以在企业中创建新帐户。帐户将创建为现收现付帐户，并且使用量将计入企业。要创建帐户，您需要具有对企业服务的编辑者或管理员角色的访问策略。

1. 在企业仪表板中，单击**帐户**以查看企业中的帐户和帐户组。
1. 在“帐户”部分中，选择**添加 > 创建帐户**。
1. 输入帐户的名称，该名称应在企业中唯一。因为这是众多帐户中的一个帐户，所以唯一的描述性名称可帮助您一眼就了解帐户的用途。
1. 如果要将其他用户分配为帐户所有者，请在**所有者**字段中输入其 IBM 标识。帐户所有者具有管理帐户的完全访问权。
1. 如果要将帐户添加到帐户组，请选择要作为其父代的帐户组。您选择的父代将确定该帐户在企业层次结构中的位置。
1. 单击**创建**。

创建帐户后，帐户所有者可以登录到该帐户以邀请其他用户并管理其访问权。

### 使用 CLI 创建帐户
{: #create-accounts-cli}

1. 如果要将帐户添加到帐户组，请查找现有帐户组的名称和标识。

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. 通过运行以下命令来创建帐户。如果未指定父帐户组，那么帐户将添加到企业正下方。要使其他用户成为帐户所有者，请在 `--owner` 选项上指定其 IBM 标识。

   ```
   ibmcloud enterprise account-create NAME
   [--parent-account-group ACCOUNT_GROUP_NAME] [--owner USER_ID]
   ```
   {: codeblock}

### 使用 API 创建帐户
{: #create-account-api}

要在企业中创建新帐户，请如以下样本请求中所示调用企业管理 API，并将 IAM 令牌和标识变量替换为企业中的值。
有关 API 的详细信息，请参阅[企业管理 API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-a-new-account-in-an-enterprise){: external}。

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/accounts \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID",
  "name": "Sample Account",
  "owner_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}
