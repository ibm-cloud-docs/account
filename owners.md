---

copyright:

  years: 2017, 2018
lastupdated: "2018-11-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:important: .important}

# Transferring ownership of a private resource

If you leave your project or organization, you might want to transfer ownership of your account to someone else.
{:shortdesc}

After you transfer ownership, you can no longer view the resource from your account. Make sure you want to transfer ownership, because this action can't be undone.
{: important}

You can use the [{{site.data.keyword.Bluemix}} command-line interface (CLI)](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_settings) to transfer ownership of a private resource. Run the following command:

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
