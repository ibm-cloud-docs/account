---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Changement de la propriété de ressources privées

Vous pouvez modifier la propriété d'un compte avec l'interface de ligne de commande. Une fois que vous avez créé et personnalisé les ressources privées de votre catalogue, vous pouvez transférer la propriété de ces ressources à quelqu'un d'autre. Une fois le transfert de propriété effectué, vous ne pourrez pas voir la ressource depuis votre compte. Le changement de la propriété d'un compte ne peut être annulé, agissez donc avec précaution.
{:shortdesc: .shortdesc}

## Comment modifier le propriétaire d'une ressource de catalogue ?

Pour changer le propriétaire d'une ressource, avec l'[interface de ligne de commande](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_settings), utilisez la commande suivante :

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
