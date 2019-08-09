---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, create account group, organize accounts, move accounts

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 在企业中组织帐户
{: #enterprise-organize}

在 {{site.data.keyword.Bluemix}} 企业中使用帐户组来组织相关帐户。您可以通过在帐户组中嵌套帐户组来创建多层企业层次结构。如果需要，可以通过在帐户组之间移动帐户来进行重组。
{:shortdesc}

例如，下图描绘了四层企业，可通过嵌套帐户组进行设置。首先，创建两个以企业作为父代的帐户组。然后，可以创建另外两个帐户组，并以先前创建的其中一个帐户组作为其父代。您可以在帐户组中自由地移动帐户，无论这些帐户处于哪个层。但是，不能移动帐户组。

![显示四个企业层的图。顶层是企业，其中包含两层帐户组。帐户组进而包含帐户。](images/enterprise-hierarchy.svg "企业层是通过添加帐户组创建的。")

请记住，组织企业的方式会影响跟踪使用成本的方式。有关更多信息，请参阅[集中管理企业的计费和使用情况](/docs/billing-usage?topic=billing-usage-enterprise)。
{: tip}

## 创建帐户组
{: #create-account-group}

要创建帐户组，您需要在企业帐户中具有对企业服务的管理员或编辑者角色。

1. 在企业仪表板中，单击**帐户**以查看企业中的帐户和帐户组。
1. 在“帐户组”部分中，单击**创建**。
1. 输入帐户组的名称，名称应能反映组中将包含的帐户。有关可以如何组织帐户的示例，请参阅[如何使用企业？](/docs/account?topic=account-enterprise#enterprise-use-cases)。
1. 如果您希望除您自己以外的其他企业用户成为帐户组的主要联系人，请从**联系人**菜单中选择其 IBM 标识。如果要分配为联系人的用户不在企业中，请首先邀请该用户加入企业帐户。创建帐户组后即无法更改联系人。有关更多信息，请参阅[邀请用户](/docs/iam?topic=iam-iamuserinv)。


   联系人与帐户所有者不同，因为联系人在帐户组或其帐户中没有其他任何访问权。您选择作为联系人的用户充当任何帐户组问题的主要联系人。例如，如果财务管理人员注意到帐户组的使用成本过高，那么他们可能会通知该帐户组的联系人。


1. 如果希望帐户组位于企业层次结构的其他部分中，请选择其他父代。

  无法删除帐户组，也无法将其从创建位置移到其他位置。
  {: note}
1. 单击**创建**。

要在企业层次结构中创建新的层，请在帐户组中创建新的帐户组。可以将企业中已存在的帐户移入帐户组，也可以在帐户组中导入或创建帐户。有关导入和创建帐户的更多信息，请参阅[向企业添加帐户](/docs/account?topic=account-enterprise-add)。

### 使用 CLI 创建帐户组
{: #create-account-groups-cli}

通过运行以下命令来创建帐户组。要将一个帐户组嵌套到另一个帐户组中，请在 `--parent-account-group` 选项上指定父帐户组的名称。如果希望其他用户成为帐户组的联系人，请在 `--primary-contact-id` 选项上指定该用户的 IBM 标识。

```
ibmcloud enterprise account-group-create NAME
[--parent-account-group ACCOUNT_GROUP_NAME] [--primary-contact-id USER_ID]
```
{: codeblock}

### 使用 API 创建帐户组
{: #create-account-groups-api}

您可以通过调用企业管理 API 以编程方式在企业中创建帐户组。

以下样本请求在企业级别正下方创建帐户组。调用 API 时，请将标识变量替换为企业中的值。要将一个帐户组嵌套到另一个帐户组中，请在云资源名称 (CRN) 中指定父帐户组的标识，格式如下：`crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID`。

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/account-groups \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID",
  "name": "Sample Account Group",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-account-group){: external}.-->

## 在企业中移动帐户
{: #move-accounts}

您可以将帐户移至企业中的任意位置。例如，可以将帐户从较低级别的帐户组移入其父帐户组，也可以移至企业正下方。帐户只能在企业中进行移动。帐户不能移至其他企业，也不能从企业中除去而成为独立帐户。

要移动帐户，您需要在企业帐户中具有对计费服务的管理员角色，以及对整个企业或对当前和目标帐户组的编辑者或管理员角色。

1. 在企业仪表板中，单击**帐户**。
1. 在“帐户”部分中，单击帐户所在行中的“操作”图标，然后选择**移动帐户**。
1. 为帐户选择新父代，然后单击**保存**。

### 使用 CLI 移动帐户
{: #move-accounts-cli}

1. 通过列出企业中的所有帐户来查找帐户名称和标识。

   ```
   ibmcloud enterprise accounts --recursive
   ```
   {: codeblock}
1. 如果要将帐户移至帐户组，请查找帐户组名称和标识。

   ```
   ibmcloud enterprise account-groups
   ```
   {: codeblock}
1. 通过在相关选项上指定新父代来移动帐户。

   要将帐户移动到帐户组，请在 `--parent-account-group` 选项上指定帐户组名。

   ```
   ibmcloud enterprise account-move -n NAME --parent-account-group ACCOUNT_GROUP_NAME
   ```
   {: codeblock}

   要将帐户移至企业正下方，请指定 `--parent-enterprise` 选项。

   ```
   ibmcloud enterprise account-move -n NAME --parent-enterprise
   ```
   {: codeblock}

### 使用 API 移动帐户
{: #move-account-api}

您可以如以下样本请求中所示，通过调用企业管理 API 来移动帐户。将 IAM 令牌和标识变量替换为企业中的值。

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_1"",
}'
```
{: codeblock}

<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#move-an-account-with-the-enterprise){: external}. -->
