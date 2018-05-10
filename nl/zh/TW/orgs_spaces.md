---

copyright:

  years: 2015, 2018
lastupdated: "2018-03-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# 新增組織及空間
{: #orgsspacesusers}

身為帳戶擁有者，您可以從 {{site.data.keyword.Bluemix}} 主控台的「Cloud Foundry 組織」頁面中新增組織及空間。如果您是組織管理員，則也可以使用「Cloud Foundry 組織」頁面來管理組織。
{:shortdesc}

您可以使用組織來啟用使用者之間的協同作業，以及使用下列方式促進專案資源的邏輯分組：

   * 您可以一組空間、應用程式、服務、網域、路徑及使用者一起分組成為組織。 
   * 您可以根據個別基準來管理使用者對組織及空間的存取權。 

## 新增組織
{: #createorg}

組織可以跨越多個地區，而且是由下列項目所定義：

<dl>
<dt>使用者</dt>
<dd>組織及空間中具有基本許可權的角色。您必須先被指派給組織，才能獲授與組織內空間的其他許可權。如需詳細資料，請參閱[使用者及角色](/docs/iam/users_roles.html#userrolesinfo)。</dd>
<dt>網域</dt>
<dd>提供網際網路上配置給組織的路徑。路徑具有一個子網域及一個網域。子網域一般是應用程式名稱。網域可能是系統網域，或您針對應用程式所登錄的自訂網域。請參閱[管理自訂網域](/docs/account/manageorg.html#managedomains)。<br/>
<p>**附註：**如果您新增自訂網域，則必須配置 DNS 伺服器來解析自訂網域，以指向 {{site.data.keyword.Bluemix_notm}} 系統網域。使用此方式，{{site.data.keyword.Bluemix_notm}} 接到您的自訂網域的要求時，可以將它適當地遞送至您的應用程式。</p></dd>
<dt>配額</dt>
<dd>代表組織可用的資源，包括可配置供組織使用的服務數目及記憶體量。建立組織時，會指派配額。組織空間中的任何應用程式或服務都會使用配額。使用「隨收隨付制」或「訂閱」帳戶，您可以在組織需要變更時，調整 Cloud Foundry 應用程式及容器的配額。請參閱[管理配額](/docs/account/manageorg.html#managequota)。</dd>
</dl>

在「訂閱」帳戶中，配額是起始消費通知的使用者定義限制。
{: tip}

新增組織時，名稱在 {{site.data.keyword.Bluemix_notm}} 中必須是唯一的。如果另一位 {{site.data.keyword.Bluemix_notm}}「公用」、「專用」或「本端」使用者已使用此組織名稱，則您必須指定新的名稱。新增組織之後，您會自動獲指派「組織管理員」許可權，這可讓您編輯組織名稱、新增使用者，以及在組織中建立或刪除空間。如果您具有計費帳戶，則可以新增所需數目的組織。不過，在精簡帳戶中，您只能有一個組織。 

下列[使用者角色](/docs/iam/users_roles.html#userrolesinfo)可以指派給組織中的使用者。依預設，受邀加入帳戶的所有使用者都會獲指派審核員角色。

   * 組織管理員
   * 組織帳單管理員
   * 組織審核員

請完成下列步驟，以新增組織：

1. 按一下**管理** &gt; **帳戶** &gt; **Cloud Foundry 組織**。
2. 按一下**新增組織**。
3. 輸入組織名稱。 
4. 按一下**新增**。

<!-- Add info on Manage infrastructure option under a space -->

## 新增空間
{: #spaceinfo}

在組織內，您可以使用空間來群組一組應用程式、服務及使用者。在 {{site.data.keyword.Bluemix_notm}} 中，空間關聯於特定地區。您可以根據交付生命週期，在組織中建立空間。例如，您可以建立 `dev` 空間作為開發環境、`test` 空間作為測試環境，以及 `production` 空間作為正式作業環境。然後，您可以建立應用程式與空間的關聯。

將使用者新增至組織之後，即可將空間的許可權授與他們。與組織類似，空間也會有一組[使用者角色](/docs/iam/users_roles.html#userrolesinfo)，其具有指派給團隊成員的特定許可權：

  * 空間管理員
  * 空間開發人員
  * 空間審核員

使用者必須至少獲指派空間中的一個許可權。
{: tip}

請完成下列步驟，以新增空間：

1. 按一下**管理** &gt; **帳戶** &gt; **Cloud Foundry 組織**。
2. 按一下您要新增空間的組織名稱。
4. 按一下**新增空間**。
5. 選取地區並輸入名稱。
6. 按一下**儲存**。
