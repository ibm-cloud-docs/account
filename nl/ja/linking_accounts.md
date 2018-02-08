---



copyright:

  years: 2015, 2018
lastupdated: "2018-01-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# {{site.data.keyword.Bluemix_notm}} アカウントと SoftLayer アカウントのリンク
{: #unifyingaccounts}

{{site.data.keyword.Bluemix}} アカウントと SoftLayer アカウントをリンクして、結合されたリソースを活用することができます。
{: shortdesc}

{{site.data.keyword.Bluemix_notm}} アカウントと Softlayer アカウントをリンクすると、単一の {{site.data.keyword.Bluemix_notm}} 請求書を受け取ることになります。 既存の {{site.data.keyword.Bluemix_notm}} アカウントがある場合、インフラストラクチャー・リソースに対する {{site.data.keyword.Bluemix_notm}} からの請求は、両方のアカウントをリンクした後に開始される新しい請求処理サイクルで有効になります。

{{site.data.keyword.Bluemix_notm}} でリンクされるアカウントはすべて、従量課金 (PAYG) アカウントでなければなりません。 新しい従量課金 (PAYG) アカウントを作成するか、既存の従量課金 (PAYG) アカウントをリンクするか、または既存のトライアル・アカウントをリンクできます (既存のトライアル・アカウントは、従量課金 (PAYG) アカウントにアップグレードされます)。サブスクリプション・アカウントはリンクできません。
{: tip}

アカウントをリンクするには、SoftLayer アカウントのマスター・ユーザーでなければなりません。

アカウントがリンクされると、以下のようになります。

* SoftLayer と {{site.data.keyword.Bluemix_notm}} アカウントの両方にアクセスするために、IBM ID 資格情報を使用する必要があります。
* 既存の SoftLayer 割引は、{{site.data.keyword.Bluemix_notm}} の料金全体に適用されます。
* 米国ドル (USD) 単位の 1 つの請求書を受け取ります。
* インフラストラクチャー・リソースの使用量は、{{site.data.keyword.Bluemix_notm}} コンソールでモニターできます。

アカウントをリンクした後は、リンク解除することはできません。  

マスター・ユーザーは、{{site.data.keyword.Bluemix_notm}} アカウントと SoftLayer アカウントをリンクするために、以下の手順を実行します。

 1. {{site.data.keyword.Bluemix_notm}} カスタマー・ポータルから、**「{{site.data.keyword.Bluemix_notm}} アカウントのリンク (Link a Bluemix Account)」**をクリックします。
 2. SoftLayer アカウントと {{site.data.keyword.Bluemix_notm}} アカウントをリンクする場合のご利用条件を読み、同意します。
 3. 要求されたら、{{site.data.keyword.Bluemix_notm}} アカウントに関連付けられている E メール・アドレスを指定します。 {{site.data.keyword.Bluemix_notm}} アカウントを持っていない場合は、使用する E メール・アドレスを指定し、{{site.data.keyword.Bluemix_notm}} への招待の手順に従ってアカウントを作成します。

アカウントをリンクすると、SoftLayer コンソールのメニュー・バーで**「{{site.data.keyword.Bluemix_notm}} に進む」**が選択可能になります。 このリンクをクリックすると、{{site.data.keyword.Bluemix_notm}} ログイン・ページに移動します。

## アカウントがリンクされている場合の {{site.data.keyword.Bluemix_notm}} 使用量に対する請求処理
{: #linkedbilling}

{{site.data.keyword.Bluemix_notm}} と SoftLayer の請求アカウントをリンクすると、次の請求処理サイクルは、単一の {{site.data.keyword.Bluemix_notm}} 請求書で請求されます。


{{site.data.keyword.Bluemix_notm}} の使用量サイクルは暦月ベースであるため、アカウントは毎月、課金契約に設定された請求日に請求されます。 SoftLayer では、使用量サイクルは、SoftLayer の使用を開始したときから始まるため、毎月、SoftLayer アカウントを登録したときと同じ日に請求されます。 

アカウントがリンクされると、{{site.data.keyword.Bluemix_notm}} の使用量の測定は、引き続き現行月のサイクルを対象として行われ、その使用量の料金は {{site.data.keyword.Bluemix_notm}} の請求書で請求されます。翌月の初めから、{{site.data.keyword.Bluemix_notm}} と SoftLayer の課金が、{{site.data.keyword.Bluemix_notm}} 請求書で結合されるようになります。

例えば、2017年 4 月 16 日にアカウントをリンクした場合、4 月の使用量については {{site.data.keyword.Bluemix_notm}} の請求書を受け取ります。 アカウントをリンクしたタイミングによっては、SoftLayer 使用量に対して別個の請求書を受け取ることがあります。 その後、5 月中の結合された使用量の料金が、{{site.data.keyword.Bluemix_notm}} アカウントから請求されます。

![IBM Cloud アカウントと SoftLayer アカウントのリンクの要約](images/IBMCloudSoftLayerBill.svg)

請求書がリンクされた後には、{{site.data.keyword.Bluemix_notm}} 請求書には、使用した各リソースに対する別個の料金がリストされます。

## API ベースの {{site.data.keyword.Bluemix_notm}} サービス
{: #api-based-services}

以下のリストに含まれているサービスは、アプリケーション・コードを使用して実行するようにセットアップできます。
これらのサービスのすべてのプランが、リンクされたアカウントで使用できるわけではありません。 リンクされたアカウントで使用できるのは、従量課金 (PAYG) アカウント用に有効になっているプランのみです。 ただし、個別に請求される個別の {{site.data.keyword.Bluemix_notm}} アカウントがある場合には、これらのすべてのサービスのすべてのプランを使用できます。

* {{site.data.keyword.alchemyapishort}}
* {{site.data.keyword.alertnotificationshort}}
* {{site.data.keyword.sparks}}
* {{site.data.keyword.appseccloudshort}}
* {{site.data.keyword.blockchain}}
* {{site.data.keyword.cloudant}}
* {{site.data.keyword.conceptinsightsshort}}
* {{site.data.keyword.iotmapinsights_short}}
* {{site.data.keyword.dashdbshort}}
* {{site.data.keyword.dialogshort}}
* {{site.data.keyword.documentconversionshort}}
* {{site.data.keyword.twittershort}}
* {{site.data.keyword.weather_short}}
* {{site.data.keyword.iotdriverinsights_short}}
* {{site.data.keyword.geospatialshort_Geospatial}}
* {{site.data.keyword.graphshort}}
* {{site.data.keyword.iotelectronics}}
* {{site.data.keyword.languagetranslationshort}}
* {{site.data.keyword.messagehub}}
* {{site.data.keyword.mqa}}
* {{site.data.keyword.mobileappbuilder_short}}
* {{site.data.keyword.mql}}
* {{site.data.keyword.nlclassifiershort}}
* {{site.data.keyword.objectstorageshort}}
* {{site.data.keyword.personalityinsightsshort}}
* {{site.data.keyword.presenceinsightsshort}}
* {{site.data.keyword.relationshipextractionshort}}
* {{site.data.keyword.retrieveandrankshort}}
* {{site.data.keyword.servicediscoveryshort}}
* {{site.data.keyword.speechtotextshort}}
* {{site.data.keyword.sqldb}}
* {{site.data.keyword.streaminganalyticsshort}}
* {{site.data.keyword.texttospeechshort}}
* {{site.data.keyword.toneanalyzershort}}
* {{site.data.keyword.tradeoffanalyticsshort}}
* {{site.data.keyword.visualinsightsshort}}
* {{site.data.keyword.visualrecognitionshort}}
* {{site.data.keyword.workflow}}
* {{site.data.keyword.workloadscheduler}}

