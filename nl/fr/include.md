---

copyright:

  years: 2017, 2018
lastupdated: "2018-05-22"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Ajout de comptes à votre ressource privée
{: #include}

Toute ressource privée que vous créez est restreinte par défaut. Si vous êtes administrateur du compte, vous pouvez désigner les personnes qui peuvent voir votre ressource en les ajoutant à une liste d'inclusion depuis l'[interface  de ligne de commande](/docs/cli/reference/bluemix_cli/bx_cli.html#ibmcloud_catalog_entry_visibility_set) `ibmcloud`.
{:shortdesc: .shortdesc}

## Comment savoir si j'ai accès ?
{: #find-access}

Vous pouvez utiliser l'interface de ligne de commande ou l'interface utilisateur Identity and Access pour déterminer si vous avez le droit d'autoriser des utilisateurs spécifiques à afficher une ressource privée qui a été ajoutée au compte. Si vous êtes propriétaire d'un compte, vous pouvez donner l'accès à votre compte à un utilisateur via l'interface utilisateur Identity and Access Management en affectant une règle d'accès. Pour plus d'informations, voir [Gestion de l'accès au catalogue](access.html).

## Etape 1 : Trouver votre ressource
{: #find-resource}

Entrez `ibmcloud catalog service <service-id or service-name>`. Remplacez service-id ou service-name par votre ID ou nom de ressource. Les informations retournées vous permettent de voir la hiérarchie, qui affiche les ressources enfant des éléments de votre ressource.

## Etape 2 : Définir la visibilité en incluant un compte
{: #vis-inc}

Entrez la commande suivante pour autoriser un compte à afficher votre ressource privée.

`ibmcloud catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

Après l'indicateur includes-add, vous pouvez ajouter, en séparant les différents éléments par des virgules, une liste d'adresses e-mail ou d'ID, associés à vos comptes.

Une fois la commande exécutée, le processus d'inclusion de la ressource prend environ 30 minutes. Une fois cette durée écoulée, déconnectez-vous de votre compte puis reconnectez-vous pour voir la ressource incluse.

## Retrait d'un compte de la liste d'inclusions
{: #remove-exclude}

Entrez la commande suivante pour retirer un compte de la liste d'inclusions.

`ibmcloud catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## Gestion de la visibilité des objets enfant
{: #child-vis}

Vous pouvez gérer la visibilité de votre ressource ou de ses enfants.

Une liste d'inclusions vide signifie que seuls les administrateurs de votre compte peuvent voir ce dernier. Votre compte doit figurer sur la liste d'inclusions pour tous les membres du compte pour qu'il soit visible.

Par exemple, si vous entrez `ibmcloud catalog service <your_service>`, vous pouvez voir les enfants de la ressource.

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

Vous pouvez obtenir l'ID de ressource pour le déploiement enfant puis inclure un compte en utilisant la commande suivante : `ibmcloud catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`.

Les enfants d'un objet peuvent hériter de la visibilité d'une façon complexe. Si l'objet enfant est privé, il dispose de sa propre configuration de visibilité. Toutefois, si l'objet enfant est défini sur public, il hérite de la visibilité de son parent. La définition d'une visibilité sur un objet enfant privé risque de restreindre sa visibilité plus que le parent.

Pour plus d'informations sur le fonctionnement de la visibilité, voir [Catalog API](https://console.bluemix.net/apidocs/682).
