---

copyright:

  years: 2017, 2018
lastupdated: "2017-12-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Masquage d'une ressource publique de votre compte pour les utilisateurs
{: #exclude}

Si vous êtes administrateur d'un compte, vous pouvez choisir de masquer une ressource publique dans votre compte pour tous les utilisateurs en ajoutant ces derniers à une liste d'exclusions avec l'[interface de ligne de commande](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_catalog_entry_visibility_set) `bx`.
{:shortdesc: .shortdesc}

**Remarque :** le masquage d'un élément dans le catalogue ne retire pas ce dernier de l'interface de ligne de commande Cloud Foundry ou des listes de mise à disposition des services disponibles via la navigation globale (Finances, Mobile, Watson ou Applications Web, par exemple).

## Comment savoir si j'ai accès ?
{: #find-access}

Vous pouvez utiliser l'interface de ligne de commande ou l'interface utilisateur Identity and Access pour déterminer si vous avez le droit d'autoriser des utilisateurs spécifiques à afficher une ressource privée qui a été ajoutée au compte. Si vous êtes propriétaire d'un compte, vous pouvez donner l'accès à votre compte à un utilisateur via l'interface utilisateur Identity and Access Management en affectant une règle d'accès. Pour plus d'informations, voir [Gestion de l'accès au catalogue](access.html).

## Etape 1 : Trouver une ressource
{: #find-resource}

Entrez `bx catalog search <service-id or service-name>` pour rechercher une ressource. Remplacez service-id ou service-name par un ID ou un nom de ressource. Trouvez l'ID ou le nom du service que vous voulez masquer dans les informations qui sont retournées.

## Etape 2 : Obtenir les détails du service

Entrez `bx catalog service <service-id or service-name>`. En utilisant ce que vous avez trouvé dans la commande précédente, servez-vous de cette commande pour examiner la ressource plus en détail. Les informations retournées vous permettent de voir la hiérarchie, qui affiche les ressources enfant des éléments de votre ressource.

## Etape 3 : Masquer la ressource
{: #vis-exc}

Entrez la commande suivante pour empêcher votre compte de voir une ressource publique.

`bx catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

Après l'indicateur excludes, vous pouvez ajouter, en séparant les différents éléments par des virgules, une liste d'adresses e-mail ou d'ID de compte, associés à vos comptes.

Une fois la commande exécutée, le processus de masquage de la ressource prend environ 30 minutes. Une fois cette durée écoulée, déconnectez-vous de votre compte puis reconnectez-vous pour voir la ressource masquée.

**Remarque :** les entrées que vous masquez ne sont pas disponibles depuis l'interface utilisateur et l'interface de ligne de commande bx. Les entrées masquées sont toujours visibles sur Cloud Foundry Marketplace, mais un plan masqué ne peut pas être provisionné depuis Cloud Foundry. Les administrateurs des comptes exclus peuvent toujours voir la ressource.

## Retrait d'un compte de la liste d'exclusions
{: #remove-exclude}

Entrez la commande suivante pour retirer un ID de compte ou une adresse e-mail de la liste d'exclusions.

`bx catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`

## Gestion de la visibilité des objets enfant - exemple
{: #child}

Vous pouvez gérer la visibilité de toutes vos ressources. Chaque ressource enfant dispose de caractéristiques de visibilité individuelles.

Dans cet exemple, vous pouvez exclure un compte du service Cloudant public.

Si vous entrez `bx catalog service cloudant`, vous pouvez voir les enfants de la ressource.

```
ID                 cloudant
Name               cloudantnosqldb
Kind               service
Provider           IBM
Tags               data_management, ibm_created, ibm_dedicated_public, lite
Active             true
Description        Cloudant NoSQL DB is a fully managed data layer designed for modern web and mobile applications that leverages a flexible JSON schema. Cloudant is built upon and compatible with Apache CouchDB and accessible through a secure HTTPS API, which scales as your application grows. Cloudant is ISO27001 and SOC2 Type 1 certified, and all data is stored in triplicate across separate physical nodes in a cluster for HA/DR within a data center.
Bindable           true
RC Compatible      false
RC Provisionable   false
Children           Name                                          Kind         ID                                               Location
                   lite                                          plan         cloudant-lite
                   |__lite-eu-gb                             deployment   cloudant-lite:eu-gb                          eu-gb
                   |  |__lite-alias-eu-gb                    alias        cloudant-lite:alias:eu-gb                    eu-gb
                   |__lite-us-south                          deployment   cloudant-lite:us-south                       us-south
                      |__lite-alias-us-south                 alias        cloudant-lite:alias:us-south                 us-south
                   standard                                      plan         cloudant-standard
                   |__standard-eu-gb                         deployment   cloudant-standard:eu-gb                      eu-gb
                   |  |__standard-alias-eu-gb                alias        cloudant-standard:alias:eu-gb                eu-gb
                   |__standard-us-south                      deployment   cloudant-standard:us-south                   us-south
                      |__standard-alias-us-south             alias        cloudant-standard:alias:us-south             us-south
```

Trouvez l'ID d'un objet et excluez un compte avec `bx catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

Pour plus d'informations sur le fonctionnement de la visibilité, voir [Catalog API](https://console.bluemix.net/apidocs/682).
