---

copyright:

  years: 2017, 2019
lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}


# Masquage d'une ressource publique pour les utilisateurs
{: #exclude}

En tant qu'administrateur de votre compte {{site.data.keyword.Bluemix}}, vous pouvez masquer une ressource publique à tous les utilisateurs ayant accès au compte. Vous pouvez également masquer des ressources afin que certaines informations sensibles ne soient pas visibles des utilisateurs non autorisés. De plus, l'accès à certaines informations doit être restreint à un nombre défini de personnes.
{:shortdesc}

Le masquage d'une ressource dans le catalogue ne retire pas cet élément de l'interface CLI Cloud Foundry ou de la liste des catégories d'offre disponible dans la navigation de la console {{site.data.keyword.Bluemix_notm}} (Finance, Mobile, Watson et Applications Web, par exemple).
{: note}

Vous pouvez utiliser la console ou l'interface de ligne de commande (CLI) {{site.data.keyword.Bluemix}} [](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) afin de déterminer si vous avez le droit d'autoriser des utilisateurs à voir une ressource privée ajoutée au compte. Si vous êtes propriétaire d'un compte, vous pouvez accorder l'accès à votre compte à un utilisateur à partir de la console en affectant une règle d'accès. Pour plus d'informations, voir [Gestion de l'accès à votre compte](/docs/account?topic=account-find-access).

## Recherche d'une ressource
{: #find-resource}

Exécutez la commande `ibmcloud catalog search <service-id or service-name>` pour rechercher une ressource. Remplacez les variables service-id ou service-name par un ID ou un nom de ressource. Utilisez les informations renvoyées pour trouver l'ID ou le nom du service à masquer.

## Obtention des détails de la ressource

Exécutez la commande `ibmcloud catalog service <service-id or service-name>`. En utilisant les informations renvoyées suite à l'exécution de la commande précédente, utilisez cette commande pour examiner de manière détaillée la ressource. Les informations renvoyées vous permettent de voir la hiérarchie, qui affiche les ressources enfant des éléments de votre ressource.

## Masquage de la ressource
{: #vis-exc}

Exécutez la commande suivante pour empêcher les utilisateurs de votre compte de voir une ressource publique.

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

Après l'indicateur excludes, vous pouvez ajouter, en séparant les différents éléments par des virgules, une liste d'adresses e-mail ou d'ID de compte, associés à vos comptes.

Une fois la commande exécutée, le processus de masquage de la ressource dure environ 30 minutes. Une fois cette durée écoulée, déconnectez-vous de votre compte puis reconnectez-vous pour voir la ressource masquée.

Les entrées que vous masquez ne sont pas disponibles dans la console ou l'interface CLI. Les administrateurs des comptes exclus peuvent toujours voir la ressource.
{: note}

## Retrait d'un compte de la liste d'exclusion
{: #remove-exclude}

Exécutez la commande suivante pour retirer un ID de compte ou une adresse e-mail de la liste d'exclusion.

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`


## Exemple : Gestion de la visibilité des objets enfant
{: #child}

Vous pouvez gérer la visibilité de toutes vos ressources. Chaque ressource enfant dispose de caractéristiques de visibilité individuelles. Cet exemple présente comment vous pouvez exclure un compte du service Cloudant.

Exécutez la commande `ibmcloud catalog service cloudant` pour voir tous les enfants de la ressource.

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

Recherchez l'ID d'un objet et excluez un compte en utilisant la commande `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

Pour plus d'informations sur le fonctionnement de la visibilité, voir la [documentation de l'API Catalog](https://{DomainName}/apidocs/globalcatalog).
