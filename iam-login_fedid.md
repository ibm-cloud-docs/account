---

copyright:

  years: 2015，2021

lastupdated: "2021-09-24"

keywords: federated ID, password, enterprise SSO, single sign-on ID, API key login, one-time passcode login, temporary credential, to login, logging in, trusted profiles

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:curl: .ph data-hd-programlang='curl'}
{:go: .ph data-hd-programlang='go'}
{:javascript: .ph data-hd-programlang='javascript'}
{:java: .ph data-hd-programlang='java'}
{:python: .ph data-hd-programlang='python'}
{:ruby: .ph data-hd-programlang='ruby'}
{:ui: .ph data-hd-interface='ui'}
{:cli: .ph data-hd-interface='cli'}
{:api: .ph data-hd-interface='api'}

# Logging in with a federated ID
{: #federated_id}

As a federated user that uses a corporate or enterprise single sign-on ID, you can log in to {{site.data.keyword.Bluemix}} from the console by using a federated ID and password. You can also log in from the command-line interface (CLI) by using a one-time passcode or an API key.
{: shortdesc}

By using federated IDs, you don't need to set up new login credentials specific to {{site.data.keyword.cloud_notm}}, for example, by using IBMid. Instead, users in your organization can easily log in to {{site.data.keyword.cloud_notm}} with their organization credentials through your identity provider (IdP). 

When a user logs in, the user gets an IAM token, which is a temporary credential that expires after 1 hour. After that time, the token must be refreshed to secure the connection and to continue accessing account resources to which they are assigned access. For more information about using federated IDs, see [Setting up your {{site.data.keyword.cloud_notm}} account](/docs/account?topic=account-account-getting-started).

## Using the console to log in
{: #login_console}
{: ui}

Use the following steps to log in to the {{site.data.keyword.cloud_notm}} console: 

1. Go to the [{{site.data.keyword.cloud_notm}} login page](cloud.ibm.com/login).
2. Enter your ID, and click **Continue**. 
3. Enter your password.

After you log in, you are directed to the {{site.data.keyword.cloud_notm}} dashboard, which provides a variety of development, account management, and infrastructure widgets.

## Using trusted profiles to log in to the console
{: #login_console_trustedprofile}
{: ui}

Account administrators use trusted profiles to manage specific access for account users. Each profile includes a different set of access policies that map to the roles or actions that you need to be productive. For example a developer may use access group membership to do their daily work, but at some point during the week they may need to do some operations work in production environments. In this case the developer would authenticate themselves and then take explicit action to assume a trusted profile that has the access policies they need to do operations work in production.

Complete the following steps to log in by using a trusted profile:

1. Go to the [{{site.data.keyword.cloud_notm}} login page](cloud.ibm.com/login).
2. Enter your IBMid, or if you are using single sign-on (SSO), enter your company email address, and click **Continue**. 
3. Enter your password.
4. Click **Select** to select the trusted profile that your account administrator created for you.

## Using the CLI to log in
{: #usingthecli_login}
{: cli} 

You choose to use either a one-time passcode or an API key to log in by using the CLI. You can find details based on whether you're using the {{site.data.keyword.cloud_notm}}, Cloud Foundry, or OpenShift CLI in the following sections.


### Using a one-time passcode to log in with the CLI
{: #onetime_passcode}

When you use the one-time passcode option to log in with a federated ID, you specify the single-sign on (SSO) parameter to get a one-time passcode, which you then enter at login.

Because a one-time passcode retrieves code from the {{site.data.keyword.Bluemix_notm}} console, it causes the use of a federated ID in your automation script to fail. Avoid trouble by using the API key option with an automated script.
{: tip}

#### From the {{site.data.keyword.Bluemix_notm}} CLI
{: #login_cli}

You can use two different methods to log in with the CLI. For the first method, use the following steps:

1. Specify the `--sso` option with the `ibmcloud login` command.
2. Follow the URL in the prompt to get the one-time passcode.
3. Copy and paste the passcode value in the CLI as your input.

```bash
ibmcloud login --sso
API endpoint: https://cloud.ibm.com

Get One Time Code from https://identity-2.us-south.iam.cloud.ibm.com/identity/passcode to proceed.
Open the URL in the default browser? [Y/n]>
One Time Code >
Authenticating...
OK

```
{: codeblock}

If you're already logged in to the console, you can use the following steps:

1. In the {{site.data.keyword.Bluemix_notm}} console, click the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") > **Log in to CLI and API**. 
2. Copy the information for the {{site.data.keyword.Bluemix_notm}} CLI into the CLI. 

#### From the Cloud Foundry CLI
{: #login_cf_cli}

You can use two different methods to log in with the Cloud Foundry CLI. For the first method, use the following steps:

1. Specify the `--sso` option with the `cf login` command.
2. Follow the URL in the prompt to get the one-time passcode.
3. Copy and paste the passcode value in the CLI as your input.

```bash
cf login -a https://api.us-south.cf.cloud.ibm.com --sso

API endpoint: https://api.us-south.cf.cloud.ibm.com

One Time Code (Get one at https://login.us-south.cf.cloud.ibm.com/UAALoginServerWAR/passcode)>
Authenticating...
OK

```
{: codeblock}

If you're already logged in to the console, you can use the following steps:

1. In the {{site.data.keyword.cloud_notm}} console, click the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") > **Log in to CLI and API**. 
2. Copy the information for the Cloud Foundry CLI and paste into the CLI. 

#### From the OpenShift CLI
{: #openshift_cli}

You can log in with a one-time passcode by using the following steps:

1. Log in to the console, and from the console, click the **{{site.data.keyword.avatar}}** icon ![Avatar icon](../icons/i-avatar-icon.svg "Avatar") > **Log in to CLI and API**. 
2. Copy the information for the OpenShift CLI and paste into the CLI.

### Using an API key in the CLI for authentication
{: #api_key}

The required API key is the {{site.data.keyword.Bluemix_notm}} API key that is used to authenticate with the {{site.data.keyword.Bluemix_notm}} platform, not the classic infrastructure API key, or {{site.data.keyword.Bluemix_notm}} service API key.

1. Create an API key with the [`ibmcloud iam api-key-create` command](/docs/cli?topic=cli-ibmcloud_commands_iam#ibmcloud_iam_api_key_create). Use the `--file` option to generate an API key file instead of showing the key in the command window:

   ```bash
   ibmcloud iam api-key-create NAME [-d DESCRIPTION] [--file FILE]

   ```
   {: codeblock}

2. Log in with the API key. You can use the API key with the {{site.data.keyword.Bluemix_notm}} CLI in any of the following ways:

    * Call the API key directly:

      ```bash
      ibmcloud login --apikey <api_key_string>

      ```
      {: codeblock}

    * Call the API key with the key file:

      ```bash
      ibmcloud login --apikey @key_file_name

      ```
      {: codeblock}

    * Set an environment variable. Additionally, you can also set an environment variable on your system. For example, IBMCLOUD_API_KEY=api_key_string, where `api_key_string` is the custom value of the API key. After the environment variable is set, you can simply specify `ibmcloud login` from the CLI.

   For Windows 10 PowerShell, you want to use `'@key_file_name'` with single quotation marks around the key file name.
   {: tip}

   To log in by using the Cloud Foundry CLI, specify `apikey` as the username and the API key string as the password:

    ```bash
    cf login -a https://api.us-south.cf.cloud.ibm.com

    API endpoint: https://api.us-south.cf.cloud.ibm.com

    Email> apikey

    Password>
    Authenticating...
    OK

    ```
    {: codeblock}

## Using an API key to get an IAM token for authentication
{: #using_apikey}
{: api} 

You can use an API key to get an IAM token to access your {{site.data.keyword.Bluemix_notm}} services. For example, you can run the following curl command to use an API key named `MY_APIKEY` to get an IAM token: 

```bash
curl -X POST 'https://iam.cloud.ibm.com/identity/token' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=urn:ibm:params:oauth:grant-type:apikey&apikey=MY_APIKEY'

```
{: codeblock}

For more information, see [Creating an IAM access token for a user or service ID by using an API key](https://cloud.ibm.com/apidocs/iam-identity-token-api#gettoken-apikey). 
