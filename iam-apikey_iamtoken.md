---

copyright:
  years: 2018, 2021
lastupdated: "2020-02-24"

keywords: IAM token, token, API key, generate token, access token, temporary credential

subcollection: account


---


{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:help: data-hd-content-type='help'} 
{:support: data-reuse='support'}

# Generating an {{site.data.keyword.Bluemix_notm}} IAM token by using an API key
{: #iamtoken_from_apikey}
{: help} 
{: support}

Generate an {{site.data.keyword.Bluemix}} Identity and Access Management (IAM) token by using either your IAM API key or a service ID's API key. {{site.data.keyword.Bluemix_notm}} APIs can be accessed only by users who are authorized by an assigned IAM role. Each user who is calling the API must pass credentials for the API to authenticate.
{:shortdesc}

You can generate an IAM token by using either your [{{site.data.keyword.Bluemix_notm}} API key](/docs/account?topic=account-userapikey#userapikey) or a [service ID's API key](/docs/account?topic=account-serviceidapikeys). The API key is a permanent credential that can be reused if you don't lose the API key value or delete the API key in the account. This process is also used if you are developing an application that needs to work with other {{site.data.keyword.Bluemix_notm}} services. You must use a service ID API key to get an access token to be passed to each of the {{site.data.keyword.Bluemix_notm}} services.

An access token is a temporary credential that expires after 1 hour at the latest. After the acquired token expires, you must generate a new token to continue calling {{site.data.keyword.Bluemix_notm}} or service APIs, and you can perform only actions that are allowed by your level of assigned access within all accounts. Use the response property `expires_in` in the API response to identify the length of time that your specific access token is valid.
{: note}

### ID token
{: #post_id_token}

Use the following `curl` command to generate an IAM token by using an API key.

```
POST https://iam.cloud.ibm.com/identity/token
```
{: codeblock}

### Headers
{: #header}

  - Content-Type: application/x-www-form-urlencoded
  - Accept: application/json


### Parameters
{: #parameters}

  - grant_type=urn:ibm:params:oauth:grant-type:apikey
  - apikey=*[API key]*

```
curl -k -X POST \
  --header "Content-Type: application/x-www-form-urlencoded" \
  --header "Accept: application/json" \
  --data-urlencode "grant_type=urn:ibm:params:oauth:grant-type:apikey" \
  --data-urlencode "apikey=<apikey>" \
  "https://iam.cloud.ibm.com/identity/token"
```
{: codeblock}

The following sample is the expected response:

### Response
{: #response}

```
{
  "access_token": "eyJhbGciOiJIUz......sgrKIi8hdFs",
  "refresh_token": "SPrXw5tBE3......KBQ+luWQVY=",
  "token_type": "Bearer",
  "expires_in": 3600,
  "expiration": 1473188353
}
```
{: codeblock}

An IAM token is valid for up to 60 minutes, and it is subject to change. When a token expires, you must generate a new one. Use the property `expires_in` for the expiration of the IAM token that you have just created.
{: note}
