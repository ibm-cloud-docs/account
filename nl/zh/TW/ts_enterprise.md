---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-18"

keywords: troubleshoot enterprise, enterprise problem, account problem, enterprise support, enterprise help, error message

subcollection: account
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# 企業的疑難排解
{: #enterprise_help}

管理企業時的一般問題可能包括，當您嘗試套用訂閱或特性碼時，或當您嘗試將帳戶新增至企業時所發生的問題。在許多情況下，您可以遵循一些簡單的步驟，從這些問題回復。


## 為何無法檢視整個企業？
{: #troubleshoot-view-enterprise}
{: troubleshoot}

如果您看不到整個企業，則可能需要檢查您獲指派的存取權。

您可以看到企業中的一些帳戶，但看不到整個企業階層。帳戶階層只會顯示您有權存取的帳戶，而不是整個企業帳戶。
{: tsSymptoms}

您僅獲指派企業中特定帳戶的存取權。
{: tsCauses}

若要檢查您獲指派的存取權，請完成下列步驟：
{: tsResolve}

1. 移至**管理** &gt; **存取 (IAM)** > **使用者**。
2. 選取名稱。
2. 按一下**存取原則**標籤。

請與企業擁有者聯絡，以要求正確的存取權。

如果您是企業的擁有者，請完成下列步驟，以指派使用者對整個企業的存取權：
1. 移至**管理** > **存取 (IAM)** > **使用者**。
2. 選取使用者的名稱。 
2. 按一下**存取原則** 標籤 > **指派存取權** > **指派對帳戶管理服務的存取權**。
3. 選取**企業**作為服務，然後選取企業的名稱。
4. 在企業中選取您要提供使用者存取權的帳戶群組或帳戶。例如，如果您想要使用者僅具有檢視單一帳戶的存取權，請選取該帳戶，然後將「檢視者」角色或更高的角色指派給使用者。如果您想要使用者具有可以檢視整個企業的存取權，請讓帳戶群組及帳戶選項保留空白，然後指派存取權。

## 為何無法將現有帳戶新增至企業？
{: #troubleshoot-existing-enterprise}
{: troubleshoot}

當您嘗試將現有帳戶新增至企業時，發生下列其中一個問題：
{: tsSymptoms}
* 按一下「帳戶」區段中的**新增現有帳戶**時，未列出您要新增的帳戶。
* 您無從選擇按一下**新增現有帳戶**。

您未獲指派正確的存取權。
{: tsCauses}

如果您看不到作為選項列出的現有帳戶，表示您需要現有帳戶的計費服務的「管理者」角色。
{: tsResolve}

若要將現有帳戶新增至企業，您需要企業的計費服務的「管理者」或「編輯者」角色，以及母企業或帳戶群組的企業服務的「管理者」或「編輯者」角色。

## 為何無法在企業中建立新帳戶？
{: #troubleshoot-add-enterprise}
{: troubleshoot}

您無法按一下「帳戶」區段中的**新增帳戶**。
{: tsSymptoms}

您未獲指派正確的存取權。
{: tsCauses}

若要在企業中建立帳戶，您必須具有下列存取權。
{: tsResolve}
1. 企業的計費服務的「管理者」角色。
2. 目標母企業或帳戶群組的企業服務的「管理者」或「編輯者」角色。

## 為何看不到企業訂閱？
{: #troubleshoot-viewsub-enterprise}
{: troubleshoot}

從子帳戶檢視「訂閱」頁面時，顯示下列訊息：
{: tsSymptoms}

`您似乎沒有許可權，無法檢視此帳戶的訂閱資料。請與帳戶擁有者或管理者聯絡，以要求存取權。`

下列訊息顯示在企業儀表板的「計費」區段中：

`您似乎沒有許可權，無法檢視此資訊。進一步瞭解 IAM 存取。`

僅限企業帳戶中的使用者，才能存取未來計費期間的計費及付款資訊。子帳戶中的使用者無法存取計費及付款資訊（例如訂閱），即使他們先前具有帳戶的存取權。
{: tsCauses}

若要檢視或管理計費，您需要受邀加入企業帳戶，並獲得該帳戶中「計費」服務的存取權。請與帳戶擁有者聯絡，以要求存取權。
{: tsResolve}

## 為何無法將訂閱代碼套用至我的帳戶？  
{: #troubleshoot-promo-enterprise}
{: troubleshoot}

您無法將訂閱代碼新增至您的帳戶，因為您沒有正確的存取權。  
{: tsSymptoms}

因為您是企業中的子帳戶，所以無法套用訂閱代碼。訂閱代碼必須在企業層級套用。
{: tsCauses}

請與企業的擁有者或管理者聯絡，以新增訂閱代碼。新增訂閱代碼後，它會套用至企業中的所有帳戶。如需相關資訊，請參閱[管理訂閱](/docs/billing-usage?topic=billing-usage-subscriptions)。
{: tsResolve}
