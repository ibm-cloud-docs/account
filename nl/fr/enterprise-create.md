---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, multiple account

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Création d'une entreprise
{: #create-enterprise}

La création d'une entreprise {{site.data.keyword.Bluemix}} s'effectue à partir d'un compte Abonnement existant. Le compte utilisé pour la création de l'entreprise est ajouté définitivement à l'entreprise.
{:shortdesc}

## Avant de commencer
{: #create-prereqs}

Pour créer une entreprise [{{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-enterprise), vous devez être propriétaire du compte ou disposer du rôle Administrateur sur le service de gestion des comptes Facturation dans un compte Abonnement.

Le compte Abonnement que vous utilisez pour créer l'entreprise est déplacé définitivement dans l'entreprise. Le déplacement du compte dans l'entreprise a les conséquences suivantes :
* La facturation du compte est désormais [gérée par l'entreprise](/docs/billing-usage?topic=billing-usage-enterprise). Après la transition, les utilisateurs du compte ne peuvent pas accéder aux informations de facturation et de paiement, comme les factures, les paiements ou les abonnements, concernant les périodes de facturation futures. Pour afficher ou gérer la facturation, les utilisateurs doivent être invités à rejoindre le compte de l'entreprise et ils doivent disposer de l'accès au service Facturation dans ce compte.
* Les utilisateurs et les droits d'accès dans le compte ne sont pas modifiés. L'accès au sein du compte est séparé de l'entreprise et les utilisateurs n'obtiennent pas automatiquement l'accès dans l'entreprise lors de l'ajout du compte. Toutefois, comme mentionné précédemment, les informations de facturation ne sont plus disponibles dans le compte, quels que soient les droits d'accès.
* Les ressources dans le compte ne sont pas changées. Les utilisateurs disposant des droits d'accès corrects peuvent continuer de consulter les informations d'utilisation concernant les ressources du compte.

Si vous ne disposez pas d'un compte Abonnement, vous pouvez mettre à niveau votre compte comme cela est décrit dans [Mise à niveau de votre compte](/docs/account?topic=account-upgrading-account).

## Création d'une entreprise dans la console
{: #create-console}

1. Accédez à **Gérer > Entreprise** puis cliquez sur **Créer**.
1. Entrez un nom unique permettant d'identifier votre entreprise. Généralement, le nom dépend de votre société ou de votre organisation, comme `L'entreprise de mon organisation`. Vous pouvez éditer le nom d'entreprise ultérieurement, si nécessaire.
1. Si votre société ou votre organisation a un nom de domaine associé, entrez-le dans la zone **Domaine**. Vous pouvez spécifier tout format de domaine ou de sous-domaine, tel `example.com` ou `my.example.com`.
1. Consultez les informations sur les conséquences pour votre compte puis sélectionnez **Je comprends l'impact sur mon compte**. Cliquez ensuite sur **Créer**.

   Une fois que le compte est ajouté à l'entreprise, il ne peut pas être retiré. Soyez donc sûr de vouloir déplacer de manière définitive le compte dans une entreprise.
   {: important}

Après quelques instants, votre entreprise est créée et vous pouvez consulter le tableau de bord de l'entreprise. Votre IBMid est répertorié en tant que contact. Le contact a la fonction de coordinateur pour toute question concernant l'entreprise, comme les questions relatives à la facturation ou à l'utilisation. Vous êtes également le propriétaire du compte d'entreprise, vous pouvez donc inviter d'autres utilisateurs à gérer l'entreprise.

Cliquez sur **Comptes** pour afficher la hiérarchie de votre entreprise qui contient deux comptes.

* Le compte d'entreprise à partir duquel vous invitez des utilisateurs et accordez l'accès permettant de gérer l'entreprise.
* Le compte utilisé pour créer l'entreprise. Ses utilisateurs et ses ressources restent identiques mais la facturation est désormais gérée par l'entreprise.

## Création d'une entreprise à l'aide de l'interface de ligne de commande
{: #create-cli}

1. Connectez-vous et sélectionnez le compte.

   ```
   ibmcloud login
   ```
   {:codeblock}
1. Créez l'entreprise en exécutant la commande suivante, où `NAME` est un nom unique permettant d'identifier l'entreprise.

   ```
   ibmcloud enterprise create NAME [-d, --domain DOMAIN_NAME] [--primary-contact-id PRIMARY_CONTACT_USER_ID]
   ```
   {:codeblock}

   Par exemple, la commande suivante crée une entreprise nommée `Example Corp Enterprise` avec le domaine `examplecorp.com`.

   ```
   ibmcloud enterprise create "Example Corp Enterprise" -d examplecorp.com
   ```
   {:codeblock}

   Par défaut, l'entreprise est créée avec l'utilisateur actuellement connecté ayant les rôles suivants :
      * Le contact de l'entreprise, qui identifie un coordinateur auquel envoyer des notifications concernant des problèmes liés à l'entreprise
      * Le propriétaire du compte d'entreprise, qui dispose d'un accès complet lui permettant de gérer le compte d'entreprise

   Vous pouvez spécifier l'IBMid pour un autre utilisateur dans l'option `--primary-contact-id`. Les deux rôles sont affectés au même utilisateur.
1. Consultez les conséquences sur votre compte et confirmez que vous souhaitez continuer en entrant `y`.
   ```
   Account abcde12345fghij67890 will be incorporated into enterprise My new enterprise
   (which cannot be undone). Do you want to proceed? [y/N]> y
   ```

Une fois que l'entreprise est créée, deux nouveaux ID s'affichent. Le premier est associé à l'entreprise, et le deuxième identifie le compte d'entreprise, que vous utilisez pour gérer l'entreprise.

```
ID:                      09876jihgf54321edcba   
Enterprise Account ID:   edcba12345jihgf67890
```

Le compte utilisé pour la création de l'entreprise fait désormais partie de cette dernière. Exécutez la commande [`ibmcloud enterprise accounts`](/docs/cli?topic=cloud-cli-ibmcloud_enterprise#ibmcloud_enterprise_accounts) pour afficher les deux comptes de votre entreprise : le compte d'entreprise et le compte utilisé pour la création de l'entreprise.

## Création d'une entreprise à l'aide de l'API
{: #create-api}

Vous pouvez créer une entreprise à l'aide d'un programme en appelant l'API Enterprise Management API, comme cela est présenté dans la demande exemple suivante. <!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-enterprise){: external}.-->

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/enterprises \
-H "Authorization: Bearer <Token>" \
-H 'Content-Type: application/json' \
-d '{
  "source_account_id": "a1b2c32a5ea94809a9840f5e23c362d",
  "name": "Sample Enterprise",
  "domain": "example.com",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

## Etapes suivantes
{: #create-next-steps}

Faites évoluer la structure de votre entreprise en ajoutant des comptes existants supplémentaires ou en créant de nouveaux comptes dans votre entreprise. Pour plus d'informations, voir la rubrique présentant l'[ajout de comptes à votre entreprise](/docs/account?topic=account-enterprise-add).

Vous pouvez également inviter des utilisateurs supplémentaires à rejoindre le compte d'entreprise afin qu'ils puissent gérer l'entreprise. Par exemple, vous pouvez inviter un responsable financier à gérer la facturation et à effectuer le suivi des coûts d'utilisation et inviter les responsables des différents services à gérer les comptes. Pour savoir comment inviter des utilisateurs, voir [Invitation d'utilisateurs](/docs/iam?topic=iam-iamuserinv).
