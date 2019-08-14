---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: troubleshoot enterprise, enterprise problem, account problem, enterprise support, enterprise help, error message

subcollection: account
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Traitement des incidents liés à une entreprise
{: #enterprise_help}

Les problèmes généraux liés à la gestion de votre entreprise peuvent inclure les problèmes survenant lorsque vous tentez d'appliquer des codes de fonction ou d'abonnement ou lorsque vous tentez d'ajouter un compte à l'entreprise. Dans de nombreux cas, ces problèmes peuvent être résolus en quelques opérations simples.

## Pourquoi ne puis-je pas afficher l'ensemble de l'entreprise ?
{: #troubleshoot-view-enterprise}
{: troubleshoot}

Si vous ne voyez pas l'ensemble de l'entreprise, il peut être nécessaire de vérifier l'accès qui vous est affecté.

Vous pouvez voir quelques comptes de l'entreprise mais non l'ensemble de la hiérarchie de l'entreprise. La hiérarchie des comptes affiche uniquement les comptes auxquels vous avez accès et non l'ensemble des comptes de l'entreprise.
{: tsSymptoms}

Vous disposez d'un accès à certains comptes de l'entreprise uniquement.
{: tsCauses}

Pour savoir quel est l'accès qui vous est affecté, procédez comme suit :
{: tsResolve}

1. Accédez à **Gérer** &gt; **Accès (IAM)** > **Utilisateurs**.
2. Sélectionnez votre nom.
2. Cliquez sur l'onglet **Règles d'accès**.

Contactez le propriétaire de l'entreprise afin de demander l'accès correct.

Si vous êtes propriétaire de l'entreprise, procédez comme suit pour affecter un accès utilisateur à l'ensemble de l'entreprise :
1. Accédez à **Gérer** > **Accès (IAM)** > **Utilisateurs**.
2. Sélectionnez le nom de l'utilisateur.
2. Cliquez sur l'onglet **Règles d'accès**, sélectionnez **Affecter un accès** > **Affecter l'accès aux services de gestion des comptes**.
3. Sélectionnez **Entreprise** comme service puis choisissez le nom de votre entreprise.
4. Sélectionnez le groupe de comptes ou le compte dans l'entreprise auquel vous souhaitez que l'utilisateur ait accès. Par exemple, si vous souhaitez qu'un utilisateur dispose d'un accès lui permettant de consulter un seul compte, sélectionnez le compte et affectez à l'utilisateur le rôle Afficheur ou un rôle supérieur. Si vous souhaitez qu'un utilisateur dispose d'un accès lui permettant d'afficher l'ensemble de l'entreprise, laissez les sélections de compte et de groupe de comptes vides puis affectez l'accès.

## Pourquoi ne puis-je pas importer un compte existant dans l'entreprise ?
{: #troubleshoot-existing-enterprise}
{: troubleshoot}

Lorsque vous tentez d'importer un compte existant dans l'entreprise, l'un des problèmes suivants se produit :
{: tsSymptoms}
* Lorsque vous cliquez sur **Ajouter un compte** dans la section Compte, le compte que vous souhaitez ajouter n'est pas répertorié.
* Vous n'avez pas la possibilité de cliquer sur **Importer le compte**.

Vous ne disposez pas des droits appropriés ou le compte n'est pas éligible pour importation.
{: tsCauses}

Si vous ne pouvez pas voir le compte existant que vous voulez importer, vous devez disposer du rôle Administrateur sur le service de facturation du compte existant.
{: tsResolve}

Si l'option **Importer le compte** n'est pas disponible, vérifiez que vous disposez du rôle Administrateur ou Editeur sur le service Facturation de l'entreprise et du rôle
Administrateur ou Editeur sur le service Entreprise pour l'entreprise parent ou le groupe de compte.

Si le compte que vous voulez importer est un compte Pay-As-You-Go et que vous ne pouvez toujours pas l'importer après avoir vérifiez que vous disposez des droits requis, il est possible que le compte ne soit pas éligible pour importation dans l'entreprise. 
Certains comptes Pay-As-You-Go ne peuvent pas être importés directement dans une entreprise, tels la plupart des comptes Pay-As-You-Go facturés en dollars américains (USD). 
Contactez le service [Ventes {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}
![Icône de lien externe](../icons/launch-glyph.svg) pour convertir le compte en compte d'abonnement, puis l'importer dans l'entreprise.

## Pourquoi ne puis-je pas créer de nouveau compte dans l'entreprise ?
{: #troubleshoot-add-enterprise}
{: troubleshoot}

Vous ne pouvez pas cliquer sur **Ajouter un compte** dans la section Comptes.
{: tsSymptoms}

L'accès correct ne vous est pas affecté.
{: tsCauses}

Pour créer un compte dans l'entreprise, vous devez disposer de l'accès suivant.
{: tsResolve}
1. Rôle Administrateur sur le service Facturation de l'entreprise.
2. Rôle Administrateur ou Editeur sur le service Entreprise pour l'entreprise parent ou le groupe de comptes cible.

## Pourquoi ne puis-je pas voir les abonnements d'entreprise ?
{: #troubleshoot-viewsub-enterprise}
{: troubleshoot}

Lorsque vous tentez d'afficher une page Abonnements à partir d'un compte enfant, le message suivant s'affiche :
{: tsSymptoms}

`Looks like you don't have permission to view subscription data for this account. Contact your account owner or administrator to request access.`

Le message suivant s'affiche dans la section Facturation du tableau de bord de votre entreprise :

`Looks like you don't have permission to view this information. Learn more about IAM access.`

L'accès aux informations de facturation et de paiement pour les périodes de facturation futures est restreint aux utilisateurs du compte d'entreprise. Les utilisateurs d'un compte enfant ne peuvent pas accéder aux informations de facturation et de paiement (abonnements, par exemple) même s'ils avaient précédemment accès au compte.
{: tsCauses}

Pour consulter ou gérer la facturation, vous devez être invité à rejoindre le compte d'entreprise et l'accès au service Facturation du compte doit vous être accordé. Pour demander l'accès, contactez le propriétaire du compte.
{: tsResolve}

## Pourquoi ne puis-je pas appliquer de code d'abonnement à mon compte ?  
{: #troubleshoot-promo-enterprise}
{: troubleshoot}

Vous ne pouvez pas ajouter de code d'abonnement à votre compte car vous ne disposez pas de l'accès correct.  
{: tsSymptoms}

Etant donné que votre compte est un compte enfant dans l'entreprise, vous ne pouvez pas appliquer de codes d'abonnement. De tels codes doivent être appliqués au niveau de l'entreprise.
{: tsCauses}

Contactez le propriétaire ou l'administrateur de l'entreprise pour ajouter le code d'abonnement. Une fois cette action effectuée, le code s'applique à tous les comptes de l'entreprise. Pour plus d'informations, voir [Gestion des abonnements](/docs/billing-usage?topic=billing-usage-subscriptions).
{: tsResolve}
