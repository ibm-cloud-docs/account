---

copyright:
  years: 2021
lastupdated: "2021-11-17"

keywords: troubleshoot MFA, multifactor authentication, verification method, authentication factor

subcollection: account

content-type: troubleshoot


---

{{site.data.keyword.attribute-definition-list}}

# Why can't I log in with my MFA factors?
{: #troubleshoot-MFA}
{: troubleshoot}

You are required to use an authentication factor, in addition to your username and password, to securely log in to {{site.data.keyword.cloud}} if at least one account that you are a member of enables MFA. You can update or reset your authentication methods if the email address or phone number that you use to authenticate changes or becomes inaccessible by going to the [Verification methods and authentication factors](https://iam.cloud.ibm.com/mysecurity){: external} page.
{: shortdesc}

When I try to log in with an authentication factor, the following error message is displayed:
{: tsSymptoms}

`Error: Incorrect validation code.`

One or more of the authentication factors that you use are inaccessible. For example, if one of your authentication factors sends you a one-time passcode by way of SMS, but you changed your, then you need to reset your MFA factors. 
{: tsCauses}

1. Go to the [Verification methods and authentication factors](https://iam.cloud.ibm.com/mysecurity){: external} page. 
{: tsResolve}

2. Validate your identity with two different verification methods. 
3. Click **Show accounts**.
4. Take note of the Authentication setting for each account. 
   1. If the account uses MFA for **IBMid users**, work with the [IBMid help desk](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: external} to reset your authentication factors. 
   1. If the account uses MFA for **All users**, you can reset your authentication factors on the Verification methods and authentication factors page. 


For more information, see [Managing verification methods and MFA factors](/docs/account?topic=account-verification-authentication). 

