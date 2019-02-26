---

copyright:

  years: 2017, 2019
lastupdated: "2019-01-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Ajout de comptes à votre ressource privée
{: #include}

Toute ressource privée {{site.data.keyword.Bluemix}} que vous créez est restreinte par défaut. Si vous êtes administrateur du compte, vous pouvez choisir qui peut voir vos ressources en ajoutant l'utilisateur à une liste d'inclusion.
{:shortdesc: .shortdesc}

Vous pouvez utiliser la console ou l'interface de ligne de commande (CLI) {{site.data.keyword.Bluemix}} [](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) afin de déterminer si vous avez le droit d'autoriser des utilisateurs à voir une ressource privée ajoutée au compte. Si vous êtes propriétaire d'un compte, vous pouvez donner accès à votre compte à un utilisateur à partir de la console en affectant une règle d'accès. Pour plus d'informations, voir [Gestion de l'accès à votre compte](/docs/account?topic=account-find-access).

## Recherche de ressources
{: #find-resource}

Exécutez la commande `ibmcloud catalog service <service-id or service-name>`. Remplacez les variables service-id ou service-name par votre ID ou votre nom de ressource. Les informations renvoyées vous permettent de voir la hiérarchie, qui affiche les ressources enfant des éléments de votre ressource.

## Définition de la visibilité en incluant un compte
{: #vis-inc}

Exécutez la commande suivante pour autoriser un compte à voir votre ressource privée.

`ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

Après l'indicateur includes-add, vous pouvez ajouter, en séparant les différents éléments par des virgules, une liste d'adresses e-mail ou d'ID, associés à vos comptes.

Une fois la commande exécutée, le processus d'inclusion de la ressource dure environ 30 minutes. Une fois cette durée écoulée, déconnectez-vous de votre compte puis reconnectez-vous pour voir la ressource incluse.

## Retrait d'un compte de la liste d'inclusion
{: #remove-exclude}

Exécutez la commande suivante pour retirer un compte de la liste d'inclusions.

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## Exemple : Gestion de la visibilité des objets enfant
{: #child-vis}

Vous pouvez gérer la visibilité de votre ressource ou de ses enfants. Une liste d'inclusion vide signifie que seuls les administrateurs de compte peuvent voir ce dernier. Votre compte doit figurer dans la liste d'inclusion pour que tous les membres du compte puissent le voir.

L'exemple suivant présente comment vous pouvez exécuter la commande `ibmcloud catalog service cloudant` pour afficher les enfants d'une instance de service Cloudant.

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

Vous pouvez obtenir l'ID de ressource pour le déploiement enfant puis inclure un compte en exécutant la commande suivante :

`ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`

Les enfants d'un objet peuvent hériter de la visibilité d'une façon complexe. Si l'objet enfant est privé, il dispose de sa propre configuration de visibilité. Toutefois, si l'objet enfant est défini sur public, il hérite de la visibilité de son parent. La définition d'une visibilité sur un objet enfant privé risque de restreindre sa visibilité au-delà du parent. Pour plus d'informations sur le fonctionnement de la visibilité, voir la [documentation de l'API Catalog](https://{DomainName}/apidocs/globalcatalog).

## Transfert de la propriété d'une ressource privée
{: #owners}

Si vous quittez votre projet ou votre organisation, vous pouvez souhaiter transférer la propriété de votre compte à un autre utilisateur.
{:shortdesc}

Une fois le transfert de propriété effectué, vous ne pouvez plus voir la ressource depuis votre compte. Vous devez être sûr de vouloir effectuer cette action car elle ne peut pas être annulée.
{: important}

Vous pouvez utiliser l'[interface de ligne de commande (CLI) {{site.data.keyword.Bluemix}}](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_cli) pour transférer la propriété d'une ressource privée. Exécutez la commande suivante :

`ibmcloud catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
