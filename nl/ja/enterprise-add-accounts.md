---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, add account, import account, create account

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# エンタープライズへのアカウントの追加
{: #enterprise-add}

{{site.data.keyword.Bluemix}} アカウントをさらに追加することによって、エンタープライズを大きくすることができます。アカウントを追加するために、別のエンタープライズ内にない既存のアカウントをインポートすることも、エンタープライズ内に新規アカウントを作成することもできます。
{:shortdesc}

エンタープライズに複数のアカウントができたら、アカウント・グループを使用して関連するアカウントを編成できます。詳しくは、『[エンタープライズ内のアカウントの編成](/docs/account?topic=account-enterprise-organize)』を参照してください。

## 既存アカウントのインポート
{: #add-accounts}

既存のアカウントをエンタープライズにインポートできます。アカウントをインポートした後でそのアカウントを削除することはできず、各アカウントは 1 つのエンタープライズのみに属することができます。インポートされるのがライト・アカウントまたはトライアル・アカウントの場合、それは自動的に[従量課金 (PAYG) アカウント](/docs/account?topic=account-accounts)にアップグレードされます。

アカウントをエンタープライズにインポートすると、以下の影響があります。
* アカウントに対する請求はエンタープライズによる管理に移行します。この移行の後、アカウント内のユーザーは、以降の請求対象期間の請求および支払情報 (請求書、支払い、サブスクリプションなど) にアクセスできません。ユーザーが請求情報を表示または管理するには、エンタープライズ・アカウントに招待され、そのアカウント内の請求処理サービスへのアクセス権限を付与される必要があります。詳しくは、『[エンタープライズを使用した請求および使用量の一元管理](/docs/billing-usage?topic=billing-usage-enterprise)』を参照してください。
* アカウント内のユーザーおよびアクセス許可は変更されません。アカウント内のアクセス権限はエンタープライズから分離されていて、アカウントのインポート時にエンタープライズ内のアクセス権限がユーザーに自動的に付与されることはありません。
* アカウント内のリソースは変更されません。適切なアクセス許可を持つユーザーは、引き続きアカウント内のリソースの使用量情報を表示できます。

既存のアカウントをエンタープライズにインポートするには、以下のアクセス権限が必要です。

   * インポートされるアカウント内で、アカウント所有者であるか、アカウント内の請求処理サービスに対する管理者役割を持っている必要があります。
   * エンタープライズ・アカウント内で、エンタープライズ・サービスに対するエディターまたは管理者の役割、および請求処理サービスに対する管理者役割が必要です。

既存のアカウントをインポートするには、次のステップを実行します。

1. エンタープライズ・アカウントにログインし、**「管理」 > 「エンタープライズ」**と移動します。
1. **「アカウント」**をクリックして、エンタープライズ内のアカウントおよびアカウント・グループを表示します。「アカウント」セクションで、**「追加」 > 「アカウントのインポート」**を選択します。
1. インポートするアカウントを選択します。

   アカウントがまったく表示されない場合、既存のどのアカウント内でも適切なアクセス権限を持っていない可能性があります。
   {: tip}
1. アカウントをアカウント・グループに追加する場合は、親にするアカウント・グループを選択します。選択した親によって、このアカウントがエンタープライズ階層内のどこに存在するのかが決まります。
1. アカウントへの影響に関する情報を確認し、**「アカウントに対する影響を理解しました (I understand the impact to my account)」**を選択します。次に、**「インポート」**をクリックします。

   アカウントがエンタープライズにインポートされた後でそれを削除することはできません。アカウントをエンタープライズに永久に移動してもよいことを確認してください。
   {: important}

### CLI を使用したアカウントのインポート
{: #add-account-cli}

1. エンタープライズにインポートするアカウントの ID を見つけます。

   ```
   ibmcloud account list
   ```
   {: codeblock}
1. アカウントをアカウント・グループに追加する場合は、エンタープライズ内の既存のアカウント・グループの名前と ID を調べます。

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. `--account ID` パラメーターにアカウント ID を指定して、アカウントをエンタープライズにインポートします。親アカウント・グループを指定しない場合、アカウントはエンタープライズのすぐ下に追加されます。

   ```
   ibmcloud enterprise account-import --account-id ID
   [--parent-account-group ACCOUNT_GROUP_NAME | --parent-account-group-id ACCOUNT_GROUP_ID]
   ```
   {: codeblock}

### API を使用したアカウントのインポート
{: #add-account-api}

既存のアカウントをエンタープライズにインポートするには、以下のサンプル要求に示すように、<!-- [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#import-an-account-into-an-enterprise){: external}--> Enterprise Management API を呼び出します。その際、{{site.data.keyword.Bluemix_notm}} ID およびアクセス管理 (IAM) トークンおよび ID 変数は実際のエンタープライズの値に置き換えてください。

```
curl -X PUT \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID/import/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" -H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID"
}'
```
{: codeblock}

## 新規アカウントの作成
{: #create-accounts}

エンタープライズ内に新規アカウントを作成できます。アカウントは従量課金 (PAYG) アカウントとして作成され、使用についての請求先はエンタープライズになります。アカウントを作成するには、エンタープライズ・サービスに対するエディターまたは管理者の役割が設定されたアクセス・ポリシーが必要です。

1. エンタープライズ・ダッシュボードで**「アカウント」**をクリックして、エンタープライズ内のアカウントおよびアカウント・グループを表示します。
1. 「アカウント」セクションで、**「追加」>「アカウントの作成」**を選択します。
1. エンタープライズ内で固有のアカウント名を入力します。これは多くのアカウントの 1 つであるため、固有の記述名は、アカウントの目的を一目で理解するのに役立ちます。
1. 別のユーザーをアカウント所有者として割り当てる場合は、**「所有者」** フィールドにそのユーザーの IBMid を入力します。アカウント所有者は、アカウントを管理するための全アクセス権限を持ちます。
1. アカウントをアカウント・グループに追加する場合は、親にするアカウント・グループを選択します。選択する親によって、このアカウントがエンタープライズ階層内のどこに存在するのかが決まります。
1. **「作成」**をクリックします。

アカウント作成後、アカウント所有者は、アカウントにログインして、他のユーザーを招待し、彼らのアクセス権限を管理することができます。

### CLI を使用したアカウントの作成
{: #create-accounts-cli}

1. アカウントをアカウント・グループに追加する場合は、既存のアカウント・グループの名前と ID を調べます。

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. 次のコマンドを実行してアカウントを作成します。親アカウント・グループを指定しない場合、アカウントはエンタープライズのすぐ下に追加されます。別のユーザーをアカウント所有者にするには、そのユーザーの IBMid を `--owner` オプションで指定します。

   ```
   ibmcloud enterprise account-create NAME
   [--parent-account-group ACCOUNT_GROUP_NAME] [--owner USER_ID]
   ```
   {: codeblock}

### API を使用したアカウントの作成
{: #create-account-api}

エンタープライズ内に新規アカウントを作成するには、以下のサンプル要求に示すように、Enterprise Management API を呼び出します (その際、IAM トークンおよび ID 変数は実際のエンタープライズの値に置き換えてください)。<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-a-new-account-in-an-enterprise){: external}. -->

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
