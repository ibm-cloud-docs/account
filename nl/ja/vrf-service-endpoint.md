---

copyright:
  years: 2019
lastupdated: "2019-07-01"

keywords: VRF, virtual routing and forwarding, service endpoint, private network

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# VRF およびサービス・エンドポイントの有効化
{: #vrf-service-endpoint}

デフォルトでは、アカウント内のリソースへは {{site.data.keyword.Bluemix}} パブリック・ネットワークを介して接続します。VRF (Virtual Routing and Forwarding) を有効にして、ご使用のアカウントおよびそのリソースのすべての IP ルーティングを別個のルーティング・テーブルに移すことができます。VRF が有効になったら、次に、パブリック・ネットワークを使用せずにリソースに直接接続するように {{site.data.keyword.Bluemix_notm}} サービス・エンドポイントを有効にすることができます。
{:shortdesc}

Virtual Routing and Forwarding および {{site.data.keyword.Bluemix_notm}} サービス・エンドポイントを有効にするには、有料アカウントが必要です。

## VRF の有効化
{: #vrf}

VRF は、ルーティング・テーブルの複数のインスタンスがルーターに存在して同時に機能することを可能にします。VRF を有効にすると、ご使用のアカウント用に別個のルーティング・テーブルが作成され、アカウントのリソースとの間の接続は {{site.data.keyword.Bluemix_notm}} ネットワーク上で別個にルーティングされます。VRF はアカウント・レベルで有効になるため、このネットワーク変更はすべてのリソースに影響します。VRF テクノロジーおよびそれがアカウントのネットワーク・ルーティングに与える影響について詳しくは、[{{site.data.keyword.Bluemix_notm}} での Virtual Routing and Forwarding](/docs/resources?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud) を参照してください。

VRF を有効にすると、アカウントのネットワーキングは永久に変更されます。アカウントおよびリソースへの影響を理解しておく必要があります。VRF を有効にした後に無効化することはできません。
{: important}

VRF を有効にするには、それを要請するためのサポート Case を作成します。

1. コンソールで**「サポート」**に進み、**「Case の作成」**をクリックします。
1. サポート・タイプとして**「アカウントおよびアクセス」**を選択します。
1. **「サブジェクト」**フィールドに `Private networking question` と入力します。
1. **「説明」**フィールドに次のメッセージを入力します。その際、_enter your account number_ (アカウント番号を入力) をご使用の {{site.data.keyword.Bluemix_notm}} アカウント番号に置き換えてください。

   `We are requesting that account *enter your account number* is moved to its own VRF. We understand the risks and approve the change. Please reply back with the scheduled window(s) of time where this change will be made so we can prepare for the migration.` (アカウント *アカウント番号を入力* を独自の VRF に移行することを要請します。リスクについて理解しており、変更に同意します。移行に向けた準備ができるように、この変更が行われる時間をスケジュールしてお知らせください。)

{{site.data.keyword.Bluemix_notm}} ネットワーク・エンジニアリング・チームは、この Case の所有者に連絡して、アカウントのネットワーキングを VRF に変換する時間をスケジュールします。変換プロセス中は、アカウント内のリソースへの接続がパケット・ロスのために不安定になることがあります。アカウントの複雑さに応じて、変換には 15 分から 30 分ほどかかります。アカウントにレガシー {{site.data.keyword.BluDirectLink}} 接続がある場合は、さらに時間がかかる可能性があります。


## サービス・エンドポイントの有効化
{: #service-endpoint}

アカウント内で {{site.data.keyword.Bluemix_notm}} サービス・エンドポイントが有効になっている場合、リソースを作成するときに、プライベート・ネットワーク・エンドポイントを公開することを選択できます。そうすると、このエンドポイントに、パブリック・ネットワークではなく {{site.data.keyword.Bluemix_notm}} プライベート・ネットワークを介して直接接続できるようになります。プライベート・ネットワーク・エンドポイントを使用するリソースはインターネットでルーティング可能な IP アドレスを持たないため、これらのリソースへの接続の安全性が高まります。詳しくは、[プライベート・ネットワーク接続のためのサービス・エンドポイント](/docs/resources?topic=resources-service-endpoints)を参照してください。

サービス・エンドポイントを有効にするには、その前にアカウントで VRF が有効にされている必要があります。
{: note}

CLI からサービス・エンドポイントを有効にするには、バージョン 0.13 以降の [{{site.data.keyword.Bluemix_notm}} CLI](/docs/cli?topic=cloud-cli-getting-started) が必要です。

1.  アカウントでサービス・エンドポイントが既に有効になっているかどうかを確認します。

    ```
    ibmcloud account show
    ```
    {: codeblock}

    以下の例のように「`サービス・エンドポイントが有効`」が `false` の場合、サービス・エンドポイントは有効になっていません。

    ```
    Retrieving account Mia Example's Account of m.example@example.com...
    OK

    アカウント ID:                             abc123d0bc2edefthyufffc9b5ca318   
    現在のターゲット・アカウント:              true   
    リンクされている SoftLayer アカウント:     0123456   
    サービス・エンドポイントが有効:            false  
    ```
    {: screen}
1. 次のコマンドを実行して、サービス・エンドポイントを有効にします。

   ```
   ibmcloud account update --service-endpoint-enable true
   ```
   {: codeblock}

   この変更が有効になるまでに数分かかることがあります。コマンドが完了したら、検証のために `ibmcloud account show` コマンドを再実行できます。

    アカウントで VRF が有効になっていない場合、このコマンドを実行すると、有効にするための Case を作成するように促すプロンプトが出されます。サポート Case を作成するには、`y` を入力します。アカウントで VRF が有効になった後、コマンドを再実行して、アカウントでサービス・エンドポイント接続を有効にします。

    ```
    サービス・エンドポイントはリンクされた Softlayer アカウント 1008967 で使用可能ではありません。
    続行するには、まず VRF (Virtual Routing and Forwarding) を有効にしてください。
    VRF について詳しくは、https://cloud.ibm.com/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html を参照してください。

    有効にするためのチケットをオープンしますか?[y/N]> y
    チケット 70729615 が正常にオープンされました。リンク https://control.softlayer.com/support/tickets/70729876 に従って詳細を確認し、チケットの状況を追跡してください。このチケットを表示するには、ログインする必要があります。
    アカウント ID:    1008967
    チケット:         Private Network Question
    ```
    {: screen}


サービス・エンドポイントが有効になった後、{{site.data.keyword.Bluemix_notm}} プライベート・ネットワークを介して接続するリソースを作成できます。サービス・エンドポイントをサポートするサービスのリストと詳細については、[プライベート・ネットワーク・エンドポイントのセットアップ](/docs/resources?topic=resources-private-network-endpoints)を参照してください。
