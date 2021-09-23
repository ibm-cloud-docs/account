---



copyright:

  years: 2015，2021

lastupdated: "2021-09-22"

keywords: dedicated ID, public IBMid, IBMid, public IAM service

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}


# Connecting a dedicated ID to your public IBMid
{: #connect_dedicated_id}

To log in to a dedicated cloud where a public IAM service is available, you must log in to the {{site.data.keyword.Bluemix_notm}} CLI with your public IBMid instead of the dedicated ID.
{: shortdesc}

```
  $ ibmcloud login -a https://api.{dedicated_env}.cloud.ibm.com
  API endpoint: https://api.{dedicated_env}.cloud.ibm.com

  Public IAM token service is available in the dedicated environment.
  Log in with your public IBMid, or use '--no-iam' to log in as a dedicated user only.

  Email>
```

If your dedicated ID is already connected to the public IBMid, it authenticates and logs in:

```
  Authenticating...
  OK

  Connected to dedicated user my_dedicated_id
```

However, if your dedicated ID is not connected to the public IBMid, you are prompted to manually connect to the public IBMid:

```
  You are logging with an IBMid that isn't associated with any dedicated user.
  To set up the connection, input the credentials of the dedicated user.

  Choose a credential type:
  1. User name and password
  2. One-time code. You can get one at https://login.{dedicated_env}.cloud.ibm.com/passcode)
  Enter a number>
```

Select an option to input the credentials for the dedicated ID. After successful authentication, your dedicated ID is connected to your public IBMid.

## Force logging in to local UAA server
{: #force_login}

To force logging in to the UAA server with a dedicated ID, specify the `--no-iam` option in `ibmcloud login` command:

```
  $ ibmcloud login --no-iam
```

## Disconnect your dedicated ID from the public IBMid
{: #disconnect_id}

You can use `ibmcloud iam dedicated-id-disconnect` to disconnect public IBMid with connected dedicated ID.

```
  $ ibmcloud iam dedicated-id-disconnect
  Do you really want to disconnect my_dedicated_id from public IBMid? (Y/N)> y
  Disconnecting dedicated user my_dedicated_id from public IBMid...
  OK

  Logging out...
  OK
```
