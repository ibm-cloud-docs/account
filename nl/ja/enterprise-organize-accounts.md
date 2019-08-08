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

# エンタープライズ内のアカウントの編成
{: #enterprise-organize}

アカウント・グループを使用して、{{site.data.keyword.Bluemix}} エンタープライズ内の関連するアカウントを編成します。アカウント・グループ内にアカウント・グループをネストすることで、複数の層からなるエンタープライズ階層を作成できます。必要な場合、アカウント・グループ間でアカウントを移動して再編成できます。
{:shortdesc}

例えば、次の図は、アカウント・グループをネストしてセットアップできる 4 層のエンタープライズを表しています。まず、エンタープライズを親とする 2 つのアカウント・グループを作成します。次に、それらのアカウント・グループのいずれかを親とする 2 つの追加アカウント・グループを作成できます。アカウント・グループがどの層にあるのかに関係なく、アカウント・グループ内でアカウントを自由に移動できます。ただし、アカウント・グループを移動することはできません。

![4 つのエンタープライズ層を示す図。最上位の層はエンタープライズであり、アカウント・グループの 2 つの層を含んでいます。アカウント・グループはアカウントを含んでいます。](images/enterprise-hierarchy.svg "アカウント・グループの追加によって作成されたエンタープライズ層。")

エンタープライズの編成方法が、使用コストの追跡方法に影響することに注意してください。詳しくは、『[エンタープライズを使用した請求および使用量の一元管理](/docs/billing-usage?topic=billing-usage-enterprise)』を参照してください。
{: tip}

## アカウント・グループの作成
{: #create-account-group}

アカウント・グループを作成するには、エンタープライズ・アカウント内のエンタープライズ・サービスに対する管理者またはエディターの役割が必要です。

1. エンタープライズ・ダッシュボードで**「アカウント」**をクリックして、エンタープライズ内のアカウントおよびアカウント・グループを表示します。
1. 「アカウント・グループ」セクションで**「作成」**をクリックします。
1. アカウント・グループの名前を入力します。このグループに含まれる予定のアカウントを反映する名前を付けてください。アカウントの編成例については、『[エンタープライズの使用方法](/docs/account?topic=account-enterprise#enterprise-use-cases)』を参照してください。
1. 自分以外のエンタープライズ・ユーザーをこのアカウント・グループの 1 次連絡先にする場合、そのユーザーの IBMid を**「連絡先」**メニューから選択します。連絡先として割り当てたいユーザーがエンタープライズ内にない場合は、まずそのユーザーをエンタープライズ・アカウントに招待してください。アカウント・グループの作成後に連絡先を変更することはできません。詳しくは、[ユーザーの招待](/docs/iam?topic=iam-iamuserinv)を参照してください。

   アカウント・グループ内またはアカウント・グループのアカウント内で追加のアクセス権限を持たないという点で、連絡先はアカウント所有者とは異なります。連絡先として選択したユーザーは、アカウント・グループのすべての問題のフォーカル・ポイントとしての役割を担います。例えば、財務担当者がアカウント・グループの使用コストが予想外に高いことに気付いた場合にアカウント・グループの連絡先に通知するといったことが考えられます。


1. このアカウント・グループをエンタープライズ階層の別の部分に配置する場合は、別の親を選択します。

  アカウント・グループは、作成した場所から削除することも、移動することもできません。
  {: note}
1. **「作成」**をクリックします。

エンタープライズ階層に新しい層を作成するには、アカウント・グループ内に新規アカウント・グループを作成します。エンタープライズ内に既に存在するアカウントをアカウント・グループに移動することができ、アカウント・グループ内でアカウントをインポートまたは作成することもできます。アカウントのインポートおよび作成について詳しくは、『[エンタープライズへのアカウントの追加](/docs/account?topic=account-enterprise-add)』を参照してください。

### CLI を使用したアカウント・グループの作成
{: #create-account-groups-cli}

次のコマンドを実行してアカウント・グループを作成します。別のアカウント・グループ内にアカウント・グループをネストするには、`--parent-account-group` オプションでアカウント・グループの名前を指定します。別のユーザーをアカウント・グループの連絡先にするには、`--primary-contact-id` オプションでそのユーザーの IBMid を指定します。

```
ibmcloud enterprise account-group-create NAME
[--parent-account-group ACCOUNT_GROUP_NAME] [--primary-contact-id USER_ID]
```
{: codeblock}

### API を使用したアカウント・グループの作成
{: #create-account-groups-api}

Enterprise Management API を呼び出すことによって、エンタープライズ内にアカウント・グループをプログラマチックに作成できます。

以下のサンプル要求は、エンタープライズ・レベルのすぐ下にアカウント・グループを 1 つ作成します。API を呼び出す際、ID 変数を実際のエンタープライズの値に置き換えてください。別のアカウント・グループ内にアカウント・グループをネストするには、`crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID` という形式で、クラウド・リソース名 (CRN) でアカウント・グループの ID を指定します。

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

## エンタープライズ内でのアカウントの移動
{: #move-accounts}

エンタープライズ内の任意の場所にアカウントを移動できます。例えば、アカウントを下位アカウント・グループから親アカウント・グループに移動したり、エンタープライズのすぐ下に移動したりできます。アカウントはエンタープライズ内でのみ移動できます。別のエンタープライズに移動したり、スタンドアロン・アカウントになるようにエンタープライズから除去したりすることはできません。

アカウントを移動するには、エンタープライズ・アカウント内の請求処理サービスに対する管理者役割と、エンタープライズ全体に対して、または、現行アカウント・グループとターゲット・アカウント・グループの両方に対して、エディターまたは管理者の役割が必要です。

1. エンタープライズ・ダッシュボードで**「アカウント」**をクリックします。
1. 「アカウント」セクションで、アカウントの行にあるアクション・アイコンをクリックし、**「アカウントの移動」**を選択します。
1. アカウントの新しい親を選択し、**「保存」**をクリックします。

### CLI を使用したアカウントの移動
{: #move-accounts-cli}

1. エンタープライズ内のすべてのアカウントをリストして、アカウント名と ID を見つけます。

   ```
   ibmcloud enterprise accounts --recursive
   ```
   {: codeblock}
1. アカウントをアカウント・グループに移動する場合は、そのアカウント・グループの名前と ID を見つけます。

   ```
   ibmcloud enterprise account-groups
   ```
   {: codeblock}
1. 新しい親を関連するオプションで指定して、アカウントを移動します。

   アカウントをアカウント・グループに移動するには、`--parent-account-group` オプションでアカウント・グループ名を指定します。

   ```
   ibmcloud enterprise account-move -n NAME --parent-account-group ACCOUNT_GROUP_NAME
   ```
   {: codeblock}

   アカウントをエンタープライズのすぐ下に移動するには、`--parent-enterprise` オプションを指定します。

   ```
   ibmcloud enterprise account-move -n NAME --parent-enterprise
   ```
   {: codeblock}

### API を使用したアカウントの移動
{: #move-account-api}

以下のサンプル要求に示すように、Enterprise Management API を呼び出すことによって、アカウントを移動できます。その際、IAM トークンおよび ID 変数は実際のエンタープライズの値に置き換えてください。

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
