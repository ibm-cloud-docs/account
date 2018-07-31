---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Changing private resource ownership

You can change account ownership with the command line interface. After you've created and customized private resources in your catalog, you can transfer ownership of those resources to someone else. After you transfer ownership, you won't be able to see the resource from your account. Changing account ownership cannot be undone, so exercise caution.
{:shortdesc: .shortdesc}

## How to change the owner of a catalog resource

To change the owner of a resource, with the [CLI](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_settings) use the following command:

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
