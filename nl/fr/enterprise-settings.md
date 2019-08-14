---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise settings, manage enterprise, view enterprise, rename enterprise

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Gestion de votre entreprise
{: #enterprise-settings}

A partir du tableau de bord de votre entreprise {{site.data.keyword.Bluemix}}, vous pouvez consulter les détails de l'entreprise, effectuer des actions communes (ajout de comptes et invitation d'utilisateurs, par exemple) et afficher les informations de facturation. Vous pouvez également renommer votre entreprise sur le tableau de bord ou en utilisant l'interface de ligne de commande ou l'API.
{:shortdesc}

Pour gérer les paramètres de l'entreprise, vous devez disposer du rôle Administrateur ou Editeur sur le service Entreprise dans le compte d'entreprise.
{: tip}

## Gestion de votre entreprise dans la console
{: #enterprise-manage}

Pour afficher le tableau de bord de votre entreprise, accédez à **Gérer > Entreprise**. Le tableau de bord inclut une présentation des comptes, des utilisateurs et du crédit d'abonnement de votre entreprise. Il inclut des liens rapides vous permettant d'effectuer les actions communes suivantes :
   * [Ajout de nouveaux comptes ou de comptes existants à votre entreprise](/docs/account?topic=account-enterprise-add)
   * [Invitation d'utilisateurs à rejoindre le compte d'entreprise](/docs/iam?topic=iam-iamuserinv)
   * [Consultation et gestion du crédit d'abonnement](/docs/billing-usage?topic=billing-usage-subscriptions)

Vous pouvez également renommer votre entreprise en cliquant sur **Renommer** dans la section Détails de l'entreprise.

## Gestion de votre entreprise à partir de l'interface de ligne de commande
{: #enterprise-manage-cli}

* Afficher les informations d'entreprise, comme le nom, le domaine, le propriétaire ainsi que les dates de création et de mise à jour.

  ```
  ibmcloud enterprise show
  ```
  {: codeblock}
* Renommer l'entreprise en indiquant le nouveau nom dans l'option `-n` de la commande suivante.

   ```
   ibmcloud enterprise update -n NEW_NAME
   ```
   {:codeblock}

## Gestion de votre entreprise à l'aide de l'API
{: #enterprise-manage-api}

Vous pouvez mettre à jour une entreprise à l'aide d'un programme en appelant l'API Enterprise Management API, comme cela est présenté dans la demande exemple suivante. 
Vous pouvez mettre à jour le nom d'entreprise ou le domaine en transmettant les nouvelles valeurs sur l'appel d'API. Pour plus d'informations sur l'API, voir la [documentation de l'API Enterprise Management](https://{DomainName}/apidocs/enterprise-apis/enterprise#update-an-enterprise){: external}.

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID" \
-H "Authorization: $IAM_TOKEN" \
-H 'Content-Type: application/json' \
-d '{
  "name": "Brand New Sample Enterprise",
  "domain": "new.example.com"
}'
```
