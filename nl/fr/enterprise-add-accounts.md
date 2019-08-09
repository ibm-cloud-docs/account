---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, add account, import account, create account

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Ajout de comptes à une entreprise
{: #enterprise-add}

Vous pouvez faire évoluer votre entreprise en y ajoutant des comptes {{site.data.keyword.Bluemix}} supplémentaires. Pour cela, vous pouvez importer des comptes existants qui ne se trouvent pas dans une autre entreprise ou vous pouvez créer de nouveaux comptes dans votre entreprise.
{:shortdesc}

Une fois que votre entreprise a plusieurs comptes, vous pouvez rassembler les comptes liés dans des groupes. Pour plus d'informations, voir [Organisation des comptes dans une entreprise](/docs/account?topic=account-enterprise-organize).

## Importation de comptes existants
{: #add-accounts}

Vous pouvez importer des comptes existants dans une entreprise. Une fois que vous avez importé un compte, il ne peut pas être retiré et chaque compte ne peut faire partie que d'une seule entreprise. Si vous importez un compte Lite ou d'essai, il est automatiquement converti en [compte Paiement à la carte](/docs/account?topic=account-accounts).

L'importation d'un compte dans l'entreprise a les conséquences suivantes :
* La facturation du compte est désormais gérée par l'entreprise. Après la transition, les utilisateurs du compte ne peuvent pas accéder aux informations de facturation et de paiement, comme les factures, les paiements ou les abonnements, pour les périodes de facturation futures. Pour afficher ou gérer la facturation, les utilisateurs doivent être invités à rejoindre le compte de l'entreprise et ils doivent disposer de l'accès au service Facturation dans ce compte. Pour plus d'informations, voir [Gestion centrale de la facturation et de l'utilisation avec les entreprises](/docs/billing-usage?topic=billing-usage-enterprise).
* Les utilisateurs et les droits d'accès dans le compte ne sont pas modifiés. L'accès au sein du compte est séparé de l'entreprise et les utilisateurs n'obtiennent pas automatiquement l'accès dans l'entreprise lors de l'importation du compte.
* Les ressources dans le compte ne sont pas changées. Les utilisateurs disposant des droits d'accès corrects peuvent continuer de consulter les informations d'utilisation concernant les ressources du compte.

Pour importer des comptes existants dans une entreprise, l'accès suivant est requis :

   * Dans le compte à importer, vous devez être propriétaire du compte ou disposer du rôle Administrateur sur le service Facturation dans le compte.
   * Dans le compte d'entreprise, vous devez avoir le rôle Editeur ou Administrateur sur le service Entreprise et le rôle Administrateur sur le service Facturation.

Pour importer un compte existant, procédez comme suit :

1. Connectez-vous à votre compte d'entreprise puis sélectionnez **Gérer > Entreprise**.
1. Cliquez sur **Comptes** pour afficher les comptes et les groupes de comptes de l'entreprise. Dans la section Comptes, sélectionnez **Ajouter > Importer le compte**.
1. Sélectionnez le compte à importer.

   Si aucun compte ne s'affiche, il est fort probable que vous ne disposiez pas de l'accès correct aux comptes existants.
   {: tip}
1. Si vous souhaitez ajouter le compte à un groupe de comptes, sélectionnez ce dernier afin qu'il soit le parent du compte. Le parent que vous sélectionnez détermine l'emplacement du compte dans la hiérarchie d'entreprise.
1. Consultez les informations sur les conséquences pour votre compte puis sélectionnez **Je comprends l'impact sur mon compte**. Cliquez ensuite sur **Importer**.

   Une fois que le compte est importé dans l'entreprise, il ne peut pas être retiré. Soyez donc sûr de vouloir déplacer de manière définitive le compte dans l'entreprise.
   {: important}

### Importation de comptes à l'aide de l'interface de ligne de commande
{: #add-account-cli}

1. Rechercher l'ID du compte à importer dans l'entreprise.

   ```
   ibmcloud account list
   ```
   {: codeblock}
1. Si vous souhaitez ajouter le compte dans un groupe de comptes, recherchez les noms et les ID des groupes de comptes existants dans l'entreprise.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. Importer le compte dans l'entreprise, en spécifiant l'ID de compte pour le paramètre `--account ID`. Si vous ne spécifiez pas de groupe de comptes parent, le compte est ajouté directement sous l'entreprise.

   ```
   ibmcloud enterprise account-import --account-id ID
   [--parent-account-group ACCOUNT_GROUP_NAME | --parent-account-group-id ACCOUNT_GROUP_ID]
   ```
   {: codeblock}

### Importation de comptes à l'aide de l'API
{: #add-account-api}

Pour importer un compte existant dans l'entreprise, appelez l'API <!-- [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#import-an-account-into-an-enterprise){: external}--> Enterprise Management, comme cela est présenté dans la demande exemple suivante. Remplacez le jeton {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) et les variables d'ID par les valeurs de votre entreprise.

```
curl -X PUT \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID/import/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" -H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID"
}'
```
{: codeblock}

## Création de nouveaux comptes
{: #create-accounts}

Vous pouvez créer des comptes dans votre entreprise. Les comptes créés sont des comptes Paiement à la carte et l'utilisation est facturée à l'entreprise. Pour créer un compte, vous avez besoin d'une règle d'accès avec le rôle Editeur ou Administrateur sur le service Entreprise.

1. Dans le tableau de bord d'entreprise, cliquez sur **Comptes** pour afficher les comptes et les groupes de comptes dans l'entreprise.
1. Dans la section Comptes, sélectionnez **Ajouter > Créer un compte**.
1. Entrez un nom pour le compte qui est unique au sein de l'entreprise. Etant donné qu'il s'agit d'un compte parmi un grand nombre, un nom unique et descriptif vous permet de voir rapidement le rôle d'un compte.
1. Si vous souhaitez définir un autre utilisateur comme propriétaire de compte, entrez son IBMid dans la zone **Propriétaire**. Le propriétaire de compte a un accès complet au compte.
1. Si vous souhaitez ajouter le compte à un groupe de comptes, sélectionnez ce dernier afin qu'il soit le parent du compte. Le parent que vous choisissez détermine l'emplacement du compte dans la hiérarchie d'entreprise.
1. Cliquez sur **Créer**.

Une fois que vous avez créé le compte, le propriétaire du compte peut se connecter au compte pour inviter d'autres utilisateurs et gérer l'accès.

### Création de comptes à l'aide de l'interface de ligne de commande
{: #create-accounts-cli}

1. Si vous souhaitez ajouter le compte à un groupe de comptes, recherchez les noms et les ID des groupes de comptes existants.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. Créez le compte en exécutant la commande suivante. Si vous ne spécifiez pas de groupe de comptes parent, le compte est ajouté directement sous l'entreprise. Pour faire en sorte qu'un autre utilisateur soit le propriétaire du compte, indiquez son IBMid dans l'option `--owner`.

   ```
   ibmcloud enterprise account-create NAME
   [--parent-account-group ACCOUNT_GROUP_NAME] [--owner USER_ID]
   ```
   {: codeblock}

### Création de compte à l'aide de l'API
{: #create-account-api}

Pour créer un compte dans l'entreprise, appelez l'API Enterprise Management, comme cela est présenté dans la demande exemple suivante, en remplaçant le jeton IAM et les variables d'ID par les valeurs de votre entreprise. <!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-a-new-account-in-an-enterprise){: external}. -->

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/accounts \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID",
  "name": "Sample Account",
  "owner_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}
