---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, create account group, organize accounts, move accounts

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Organisation des comptes dans une entreprise
{: #enterprise-organize}

Utilisez des groupes de comptes afin d'organiser les comptes liés dans votre entreprise {{site.data.keyword.Bluemix}}. Vous pouvez créer une hiérarchie d'entreprise multi-niveaux en imbriquant des groupes de comptes dans un groupe de comptes. Si nécessaire, vous pouvez effectuer une réorganisation en déplaçant des comptes entre des groupes.
{:shortdesc}

Par exemple, le diagramme suivant présente une entreprise à quatre niveaux que vous pouvez configurer en imbriquant des groupes de comptes. Créez tout d'abord deux groupes de comptes ayant l'entreprise comme parent. Créez ensuite deux groupes de comptes supplémentaires ayant un de ces groupes de comptes comme parent. Vous pouvez déplacer des comptes en toute liberté dans les groupes de comptes, quel que soit le niveau dans lequel ils se trouvent. Toutefois, il n'est pas possible de déplacer les groupes de comptes.

![Diagramme présentant quatre niveaux d'entreprise. Le premier niveau est celui de l'entreprise, qui contient deux niveaux de groupes de comptes. Ensuite, le groupe de comptes contient des comptes.](images/enterprise-hierarchy.svg "Les niveaux d'entreprise sont créés en ajoutant des groupes de comptes."){: caption="Figure 1. Hiérarchie d'entreprise à quatre niveaux" caption-side="bottom"}

N'oubliez pas que le mode d'organisation de votre entreprise a des conséquences sur le mode de suivi des coûts d'utilisation. Pour plus d'informations, voir [Gestion centrale de la facturation et de l'utilisation avec les entreprises](/docs/billing-usage?topic=billing-usage-enterprise).
{: tip}

## Création de groupes de comptes
{: #create-account-group}

Pour créer un groupe de comptes, vous devez disposer du rôle Administrateur ou Editeur sur le service Entreprise dans le compte correspondant.

1. Dans le tableau de bord d'entreprise, cliquez sur **Comptes** pour afficher les comptes et les groupes de comptes de l'entreprise.
1. Dans la section Groupes de comptes, cliquez sur **Créer**.
1. Entrez un nom pour le groupe de comptes défini en fonction des comptes de ce dernier. Voir [Comment puis-je utiliser une entreprise ?](/docs/account?topic=account-enterprise#enterprise-use-cases) pour obtenir des exemples d'organisation de compte.
1. Si vous souhaitez qu'un utilisateur d'entreprise soit le principal contact pour le groupe de comptes, sélectionnez son IBMid dans le menu **Contact**. Si un utilisateur que vous souhaitez définir comme contact n'est pas dans l'entreprise, invitez-le tout d'abord à rejoindre le compte d'entreprise. Une fois le groupe de comptes créé, il n'est pas possible de changer le contact. Voir [Invitation d'utilisateurs](/docs/iam?topic=iam-iamuserinv) pour plus d'informations.

   Le contact est différent d'un propriétaire de compte. Effectivement, il n'a pas d'accès supplémentaire au groupe de comptes ou à ses comptes. L'utilisateur que vous sélectionnez comme contact a le rôle de coordinateur pour tout problème de groupe de comptes. Par exemple, si un responsable financier remarque que les coûts d'utilisation du groupe de comptes sont étonnamment élevés, il peut envoyer une notification au contact du groupe de comptes.


1. Si vous souhaitez que le groupe de comptes se trouve dans une autre partie de votre hiérarchie d'entreprise, sélectionnez un autre parent.

  Les groupes de comptes ne peuvent pas être supprimés ou déplacés.
  {: note}
1. Cliquez sur **Créer**.

Pour créer un nouveau niveau dans votre hiérarchie d'entreprise, créez de nouveaux groupes de comptes dans le groupe de comptes. Vous pouvez déplacer des comptes se trouvant déjà dans l'entreprise dans le groupe de comptes ou vous pouvez importer ou créer des comptes dans ce dernier. Pour plus d'informations sur l'importation et la création de comptes, voir [Ajout de comptes à une entreprise](/docs/account?topic=account-enterprise-add).

### Création de groupes de comptes à l'aide de l'interface de ligne de commande
{: #create-account-groups-cli}

Créez un groupe de comptes en exécutant la commande suivante. Pour imbriquer un groupe de comptes dans un autre groupe de comptes, spécifiez le nom du groupe dans l'option `--parent-account-group`. Si vous souhaitez qu'un autre utilisateur soit le contact du groupe de comptes, indiquez son IBMid dans l'option `--primary-contact-id`.

```
ibmcloud enterprise account-group-create NAME
[--parent-account-group ACCOUNT_GROUP_NAME] [--primary-contact-id USER_ID]
```
{: codeblock}

### Création de groupes de comptes à l'aide de l'API
{: #create-account-groups-api}

Vous pouvez créer à l'aide d'un programme un groupe de comptes dans l'entreprise en appelant l'API Enterprise Management.

La demande exemple suivante crée un groupe de comptes directement sous le niveau de l'entreprise. Lorsque vous appelez l'API, remplacez les variables d'ID par les valeurs de votre entreprise. Pour imbriquer le groupe de comptes dans un autre groupe de comptes, indiquez son ID dans le nom CRN au format suivant : `crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID`.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/account-groups \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID",
  "name": "Sample Account Group",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

Pour plus d'informations sur l'API, voir [API Enterprise Management](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-account-group){: external}.

## Déplacement de comptes au sein de l'entreprise
{: #move-accounts}

Vous pouvez déplacer des comptes à tout emplacement dans votre entreprise. Par exemple, vous pouvez déplacer un compte d'un groupe de comptes inférieur dans son groupe de comptes parent ou vous pouvez le déplacer directement sous l'entreprise. Les comptes peuvent être déplacés uniquement dans l'entreprise. Ils ne peuvent pas être déplacés dans une autre entreprise ou être retirés de l'entreprise afin de devenir un compte autonome.

Pour déplacer un compte, vous devez disposer du rôle Administrateur sur le service Facturation dans le compte d'entreprise et du rôle Editeur ou Administrateur sur l'ensemble de l'entreprise ou sur les groupes de comptes actuel et cible.

1. Dans le tableau de bord d'entreprise, cliquez sur **Comptes**.
1. Dans la section Comptes, cliquez sur l'icône Actions dans la ligne du compte puis sélectionnez **Déplacer le compte**.
1. Sélectionnez le nouveau parent pour le compte puis cliquez sur **Sauvegarder**.

### Déplacement d'un compte à l'aide de l'interface de ligne de commande
{: #move-accounts-cli}

1. Rechercher l'ID et le nom de compte en répertoriant tous les comptes de votre entreprise.

   ```
   ibmcloud enterprise accounts --recursive
   ```
   {: codeblock}
1. En cas de déplacement du compte dans un groupe de comptes, rechercher l'ID et le nom du groupe de comptes.

   ```
   ibmcloud enterprise account-groups
   ```
   {: codeblock}
1. Déplacer le compte en spécifiant le nouveau parent dans l'option liée.

   Pour déplacer le compte dans un groupe de comptes, spécifiez le nom du groupe de comptes dans l'option `--parent-account-group`.

   ```
   ibmcloud enterprise account-move -n NAME --parent-account-group ACCOUNT_GROUP_NAME
   ```
   {: codeblock}

   Pour déplacer le compte directement sous l'entreprise, indiquez l'option `--parent-enterprise`.

   ```
   ibmcloud enterprise account-move -n NAME --parent-enterprise
   ```
   {: codeblock}

### Déplacement de comptes à l'aide de l'API
{: #move-account-api}

Vous pouvez déplacer un compte en appelant l'API Enterprise Management, comme cela est présenté dans la demande exemple suivante. Remplacez le jeton IAM et les variables d'ID par les valeurs de votre entreprise.

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_1"",
}'
```
{: codeblock}

Pour plus d'informations sur l'API, voir
[API
Enterprise Management](https://{DomainName}/apidocs/enterprise-apis/enterprise#move-an-account-with-the-enterprise){: external}.
