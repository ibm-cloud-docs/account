---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-29"

keywords: create account, IBMid, sign up for account, sign up

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Inscription à {{site.data.keyword.Bluemix_notm}}
{: #signup}

Vous pouvez vous inscrire à un compte {{site.data.keyword.Bluemix}} avec votre IBMid existant ou créer un nouvel IBMid. Si votre société est enregistrée de manière à utiliser un ID fédéré de connexion unique (SSO), inscrivez-vous plutôt avec cet ID fédéré.
{:shortdesc}

| ID d'inscription | Détails |    
|-----------------|---------|
|IBMid existant   | Si vous possédez déjà un IBMid, inscrivez-vous à {{site.data.keyword.Bluemix_notm}} avec les données d'identification existantes que vous utilisez pour recevoir les autres produits et services IBM. |
|Nouvel IBMid        | Si vous ne possédez pas encore d'IBMid, vous en créerez un lors de votre inscription. Un IBMid vous permet d'utiliser un seul et même nom d'utilisateur pour vous connecter à tous les services et produits IBM, y compris {{site.data.keyword.Bluemix_notm}}. |
|ID fédéré     | Si votre société a déjà demandé à enregistrer auprès d'IBM les données d'identification de l'utilisateur du domaine de votre société, vous pouvez vous inscrire à {{site.data.keyword.Bluemix_notm}} à l'aide des données d'identification dont vous vous servez déjà pour la connexion de votre société. Vous devez entrer un numéro de téléphone lorsque vous vous inscrivez. |
{:caption="Tableau 1. Option d'ID pour l'inscription à {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Inscription avec un IBMid nouveau ou existant
{: #signup-ibmid}

Si vous ne faites pas partie d'une société qui utilise des ID fédérés, vous vous inscrirez à {{site.data.keyword.Bluemix_notm}} à l'aide d'un IBMid.

1. Accédez à la [page de connexion {{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com/){: new_window} ![Icône de lien externe](../icons/launch-glyph.svg "Icône de lien externe"), puis cliquez sur **Créer un compte {{site.data.keyword.Bluemix_notm}}**.
1. Entrez l'adresse électronique de votre IBMid. Si vous ne disposez pas d'un IBMid existant, un ID est créé d'après l'adresse électronique que vous entrez.
1. Entrez vos informations dans les autres zones, puis cliquez sur **Créer un compte**.
1. Confirmez votre compte en cliquant sur le lien contenu dans le courrier électronique de confirmation envoyé à l'adresse électronique fournie.

En cas de problème lors de la connexion à votre  nouveau compte, voir [Identification et résolution des incidents liés à l'accès à {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-accessing) pour obtenir de l'aide.

## Inscription avec un ID fédéré
{: #signup-federated}

Un ID fédéré est un ID présent dans le domaine d'une société qui est enregistré auprès d'IBM de sorte que le domaine et les données d'identification de l'utilisateur puissent être utilisés pour accéder aux applications Web IBM. Vous pouvez vous inscrire à {{site.data.keyword.Bluemix_notm}} avec un ID fédéré uniquement si votre société est déjà enregistrée auprès d'IBM. L'enregistrement du domaine d'une société auprès d'IBM permet aux utilisateurs de se connecter pour recevoir des produits et des services IBM en utilisant leurs données d'identification d'utilisateur de société existantes. L'authentification est alors gérée par le fournisseur d'identité de votre société à l'aide de SSO.

IBM utilise le langage Security Assertion Markup Language 2.0 (SAML 2.0) pour cette fédération d'identité. SAML 2.0 est une version standard pour l'échange de données d'authentification entre des domaines de sécurité. Il s'agit d'un protocole de type XML qui utilise un jeton de sécurité contenant des assertions pour transmettre des informations entre les organisations "fournisseur d'identité" et la "partie utilisatrice IBM", connue sous l'appellation "fournisseur de services".

Pour plus d'informations sur l'enregistrement de votre société pour obtenir un ID fédéré, voir [IBMid Enterprise Federation Adoption Guide![Icône de lien externe](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window}. Un sponsor IBM, tel qu'un représentant du client ou un service de conseil, est requis lorsque vous demandez à enregistrer des ID fédérés.

### Connexion à l'aide d'un ID fédéré
{: #login-federated}

Lorsque vous vous connectez à la console {{site.data.keyword.Bluemix_notm}} avec un ID fédéré, vous êtes invité à vous connecter via la page de connexion de votre société. Si vous vous connectez via une interface de ligne de commande, vous devrez fournir des paramètres supplémentaires spécifiques pour vous authentifier. Pour plus d'informations, voir [Connexion à l'aide d'un ID fédéré](/docs/iam?topic=iam-federated_id).
