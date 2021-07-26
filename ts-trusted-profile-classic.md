---

copyright:
  years: 2021
lastupdated: "2021-07-26"

keywords: troubleshoot trusted profile, classic infrastructure, trusted profile application

subcollection: account

content-type: troubleshoot


---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Why can't I use Classic Infrastructure or the Softlayer API when I log in to {{site.data.keyword.cloud}} by applying a trusted profile?
{: #troubleshoot-trusted-profile-classic}
{: troubleshoot}

You need to log in to an account without applying a trusted profile.
{: shortdesc}

When I try to log in by applying a trusted profile, the following error message is displayed:
{: tsSymptoms}

`The Classic Infrastructure and Softlayer API is not available.`
   
The Classic Infrastructure and Softlayer API is not currently enabled for users that log in to {{site.data.keyword.cloud_notm}} by applying a trusted profile. 
{: tsCauses}

If you need to use Classic Infrastructure or Softlayer permissions, log out and log back in without applying a trusted profile by clicking **Continue** on the trusted profiles landing page.
{: tsResolve}