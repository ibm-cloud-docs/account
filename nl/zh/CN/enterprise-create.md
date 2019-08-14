---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, multiple account

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# 创建企业
{: #create-enterprise}

您可以通过现有预订帐户创建 {{site.data.keyword.Bluemix}} 企业。用于创建企业的帐户将永久添加到企业中。
{:shortdesc}

## 开始之前
{: #create-prereqs}

要创建 [{{site.data.keyword.Bluemix_notm}} 企业](/docs/account?topic=account-enterprise)，您必须是帐户所有者，或在预订帐户中具有对缴费帐户管理服务的管理员角色。

用于创建企业的预订帐户将永久移入企业。将帐户移入企业具有以下影响：
* 帐户的计费会转换为[由企业进行管理](/docs/billing-usage?topic=billing-usage-enterprise)。转换之后，帐户中的用户即无法访问未来结算周期的帐单和付款信息，例如发票、付款或预订。要使这些用户能够查看或管理计费，需要邀请他们加入企业帐户，并在该帐户中向其授予对计费服务的访问权。
* 帐户中的用户和访问许可权不会更改。帐户中的访问权与企业相分离，并且在添加帐户时，用户并不会自动获得企业中的访问权。但是，如前所述，计费信息在帐户中不再可用，不管有怎样的访问许可权。
* 帐户中的资源不会更改。具有正确访问许可权的用户可以继续查看帐户中资源的使用情况信息。

如果您没有预订帐户，那么可以如[升级帐户](/docs/account?topic=account-upgrading-account)中所述对帐户升级。

## 在控制台中创建企业
{: #create-console}

1. 转至**管理 > 企业**，然后单击**创建**。
1. 输入用于标识企业的唯一名称。通常，名称应反映您的公司或组织，例如`我的组织的企业`。如果需要，您日后可以编辑企业名称。
1. 如果公司或组织有关联的域名，请在**域**字段中输入该域名。您可以指定任何域或子域格式，例如 `example.com` 或 `my.example.com`。
1. 查看有关帐户所受影响的信息，然后选择**我了解对帐户的影响**。然后，单击**创建**。

   将帐户添加到企业后，即无法将其除去。请确保要将帐户永久移至企业。
   {: important}

片刻之后，您的企业即会创建完成，然后您可以查看企业仪表板。您的 IBM 标识将作为联系人列出。联系人充当任何企业问题（例如，计费或使用情况问题）的主要联系人。此外，还会将您分配为企业帐户所有者，因此您可以邀请其他用户来管理企业。

单击**帐户**以查看企业层次结构，其中包含两个帐户。

* 企业帐户，用于邀请用户加入并向其授予访问权来管理企业。
* 用于创建企业的帐户。此帐户的用户和资源保持相同，但计费现在由企业进行管理。

## 使用 CLI 创建企业
{: #create-cli}

1. 登录并选择帐户。

   ```
ibmcloud login
```
   {:codeblock}
1. 通过运行以下命令来创建企业，其中 `NAME` 是用于标识企业的唯一名称。

   ```
   ibmcloud enterprise create NAME [-d, --domain DOMAIN_NAME] [--primary-contact-id PRIMARY_CONTACT_USER_ID]
   ```
   {:codeblock}

   例如，以下命令使用 `examplecorp.com` 域创建名为 `Example Corp Enterprise` 的企业。

   ```
   ibmcloud enterprise create "Example Corp Enterprise" -d examplecorp.com
   ```
   {:codeblock}

   缺省情况下，将使用具有以下角色的当前已登录用户来创建企业：
      * 企业的联系人，标识向其通知企业相关问题的主要联系人
      * 企业帐户的所有者，具有管理企业帐户的完全访问权

   您可以在 `--primary-contact-id` 选项上指定其他用户的 IBM 标识。可为同一用户同时分配这两个角色。
1. 查看对您帐户的影响，并输入 `y` 以确认您要继续。
   ```
   Account abcde12345fghij67890 will be incorporated into enterprise My new enterprise
   (which cannot be undone). Do you want to proceed? [y/N]> y
   ```

创建企业后，将显示两个新标识。第一个标识与企业相关联，第二个标识用于标识企业帐户，该帐户用于管理企业。

```
ID:                      09876jihgf54321edcba   
Enterprise Account ID:   edcba12345jihgf67890
```

现在，用于创建企业的帐户已成为企业的一部分。运行 [`ibmcloud enterprise accounts`](/docs/cli?topic=cloud-cli-ibmcloud_enterprise#ibmcloud_enterprise_accounts) 命令可查看企业中的两个帐户：企业帐户和用于创建企业的帐户。

## 使用 API 创建企业
{: #create-api}

您可以如以下样本请求中所示，通过调用企业管理 API 以编程方式创建企业。有关 API 的详细信息，请参阅[企业管理 API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-enterprise){: external}。

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/enterprises \
-H "Authorization: Bearer <Token>" \
-H 'Content-Type: application/json' \
-d '{
  "source_account_id": "a1b2c32a5ea94809a9840f5e23c362d",
  "name": "Sample Enterprise",
  "domain": "example.com",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

## 后续步骤
{: #create-next-steps}

通过添加更多现有帐户或在企业中创建新帐户来扩建企业结构。有关更多信息，请参阅[向企业添加帐户](/docs/account?topic=account-enterprise-add)。

您还可以邀请其他用户加入企业帐户，以便他们能够帮助管理企业。例如，您可能希望邀请财务管理人员来管理计费并跟踪使用成本，邀请部门负责人来管理帐户。有关如何邀请用户的更多信息，请参阅[邀请用户](/docs/iam?topic=iam-iamuserinv)。
