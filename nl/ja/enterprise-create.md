---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, multiple account

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# エンタープライズの作成
{: #create-enterprise}

既存のサブスクリプション・アカウントから {{site.data.keyword.Bluemix}} エンタープライズを作成します。エンタープライズの作成に使用するアカウントは、エンタープライズに永久に追加されます。
{:shortdesc}

## 始める前に
{: #create-prereqs}

[{{site.data.keyword.Bluemix_notm}} エンタープライズ](/docs/account?topic=account-enterprise)を作成するには、アカウント所有者であるか、サブスクリプション・アカウント内の請求アカウント管理サービスに対する管理者役割を持っている必要があります。

エンタープライズの作成に使用するサブスクリプション・アカウントは、エンタープライズに永久に移動されます。アカウントをエンタープライズに移動すると、以下の影響があります。
* そのアカウントに対する請求は[エンタープライズによる管理](/docs/billing-usage?topic=billing-usage-enterprise)に移行します。この移行の後、アカウント内のユーザーは、以降の請求対象期間の請求および支払情報 (請求書、支払い、サブスクリプションなど) にアクセスできません。ユーザーが請求情報を表示または管理するには、エンタープライズ・アカウントに招待され、そのアカウント内の請求処理サービスへのアクセス権限を付与される必要があります。
* アカウント内のユーザーおよびアクセス許可は変更されません。アカウント内のアクセス権限はエンタープライズから分離されていて、アカウントの追加時にエンタープライズ内のアクセス権限がユーザーに自動的に付与されることはありません。ただし、前述のように、アクセス許可に関係なく、アカウント内で請求情報を使用することはできなくなります。
* アカウント内のリソースは変更されません。適切なアクセス許可を持つユーザーは、引き続きアカウント内のリソースの使用量情報を表示できます。

サブスクリプション・アカウントをお持ちでない場合、『[アカウントのアップグレード](/docs/account?topic=account-upgrading-account)』で説明されているように、ご使用のアカウントをアップグレードできます。

## コンソールでのエンタープライズの作成
{: #create-console}

1. **「管理」 > 「エンタープライズ」**と移動し、**「作成」**をクリックします。
1. エンタープライズを識別する固有の名前を入力します。通常、会社または組織を反映する名前にします (例: `My organization's enterprise`)。必要な場合、後でエンタープライズ名を編集できます。
1. 会社または組織にドメイン・ネームが関連付けられている場合は、それを**「ドメイン」**フィールドに入力します。任意のドメインまたはサブドメイン形式を指定できます (例: `example.com` や `my.example.com` など)。
1. アカウントへの影響に関する情報を確認し、**「アカウントに対する影響を理解しました (I understand the impact to my account)」**を選択します。 次に、**「作成」**をクリックします。 

   アカウントがエンタープライズに追加された後でそれを削除することはできません。アカウントをエンタープライズに永久に移動してもよいことを確認してください。
   {: important}

しばらくすると、エンタープライズが作成され、エンタープライズ・ダッシュボードを表示できるようになります。ご使用の IBMid が連絡先としてリストされます。この連絡先は、請求や使用量に関する質問など、エンタープライズに関するすべての問題のフォーカル・ポイントとなります。エンタープライズ・アカウント所有者も自分に割り当てられるため、エンタープライズを管理するための追加ユーザーを招待できます。

**「アカウント」** をクリックして、エンタープライズ階層を表示します。これには次の 2 つのアカウントが含まれます。

* エンタープライズ・アカウント: ここで、ユーザーを招待し、エンタープライズを管理するためのアクセス権限を付与します。
* エンタープライズを作成するために使用したアカウント。このアカウントのユーザーおよびリソースは同じままですが、請求はエンタープライズによって管理されるようになりました。

## CLI を使用したエンタープライズの作成
{: #create-cli}

1. ログインし、アカウントを選択します。

   ```
   ibmcloud login
   ```
   {:codeblock}
1. 次のコマンドを実行してエンタープライズを作成します。ここで、`NAME` はエンタープライズを識別する固有の名前です。

   ```
   ibmcloud enterprise create NAME [-d, --domain DOMAIN_NAME] [--primary-contact-id PRIMARY_CONTACT_USER_ID]
   ```
   {:codeblock}

   例えば、次のコマンドでは、`Example Corp Enterprise` という名前で、`examplecorp.com` ドメインのエンタープライズが作成されます。

   ```
   ibmcloud enterprise create "Example Corp Enterprise" -d examplecorp.com
   ```
   {:codeblock}

   デフォルトでは、現在ログインしているユーザーに以下の役割を持たせてエンタープライズが作成されます。
      * エンタープライズ関連の問題について通知する中心人物を示す、エンタープライズの連絡先
      * エンタープライズ・アカウントを管理するための全アクセス権限を持つ、エンタープライズ・アカウントの所有者

   `--primary-contact-id` オプションで、別のユーザーの IBMid を指定できます。両方の役割に同じユーザーが割り当てられます。
1. アカウントへの影響を確認し、`y` を入力して続行することを確認します。
   ```
   Account abcde12345fghij67890 will be incorporated into enterprise My new enterprise
   (which cannot be undone). Do you want to proceed? [y/N]> y
   ```

エンタープライズが作成されると、2 つの新しい ID が表示されます。1 番目の ID はエンタープライズに関連付けられていて、2 番目の ID はエンタープライズの管理に使用するエンタープライズ・アカウントを識別します。

```
ID:                      09876jihgf54321edcba   
Enterprise Account ID:   edcba12345jihgf67890
```

これで、エンタープライズの作成に使用したアカウントはエンタープライズの一部になりました。エンタープライズ内の 2 つのアカウント (エンタープライズ・アカウントと、エンタープライズの作成に使用したアカウント) を表示するには、[`ibmcloud enterprise accounts`](/docs/cli?topic=cloud-cli-ibmcloud_enterprise#ibmcloud_enterprise_accounts) コマンドを実行します。

## API を使用したエンタープライズの作成
{: #create-api}

以下のサンプル要求に示すように、Enterprise Management API を呼び出すことによって、プログラマチックにエンタープライズを作成できます。<!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-enterprise){: external}.-->

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

## 次のステップ
{: #create-next-steps}

既存アカウントをさらに追加するか、エンタープライズ内で新規アカウントを作成することによって、エンタープライズを大きくします。詳しくは、『[エンタープライズへのアカウントの追加](/docs/account?topic=account-enterprise-add)』を参照してください。

エンタープライズの管理に役立つように、追加のユーザーをエンタープライズ・アカウントに招待することもできます。例えば、請求管理および使用コスト追跡のために財務担当者を招待したり、アカウント管理のために部門リーダーを招待したりできます。 ユーザーを招待する方法について詳しくは、『[ユーザーの招待](/docs/iam?topic=iam-iamuserinv)』を参照してください。
