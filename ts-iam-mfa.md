---

copyright:
  years: 2021
lastupdated: "2021-10-29"

keywords: troubleshoot MFA, multifactor authentication, verification method, authentication factor, reset MFA

subcollection: account

content-type: troubleshoot


---

{{site.data.keyword.attribute-definition-list}}

# How can I reset my MFA factors?
{: #troubleshoot-MFA}
{: troubleshoot}

If at least one account that you are a member of enables MFA, you must use an authentication factor, in addition to your username and password, to securely log in to {{site.data.keyword.cloud}}. You might want to update or reset your authentication methods if the email address or phone number that you use to authenticate to the {{site.data.keyword.Bluemix}} console changes or becomes inaccessible. 
{: shortdesc}

I can't log in because I'm prompted to enter an authentication factor that I can't access. 
{: tsSymptoms}

One or more of the authentication factors that you use are inaccessible. For example, if one of your authentication factors sends you an one-time passcode by way of SMS, but your phone number has changed, then you need to reset your MFA factors. 
{: tsCauses}

1. Go to the [Verification methods and authentication factors](https://iam.cloud.ibm.com/mysecurity){: external} page. 
{: tsResolve}

2. Validate your identity with two different verification methods. 
3. Click **Show accounts**.
4. Take note of the Authentication setting for each account. 
   1. If the account uses MFA for **IBMid users**, work with the [IBMid help desk](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: external} to reset your authentication factors. 
   1. If the account uses MFA for **All users**, you can reset your authentication factors on the Verification methods and authentication factors page. 


For more information, see [Managing verification methods and MFA factors](/docs/account?topic=account-verification-authentication). 

