---

copyright:

  years: 2018
lastupdated: "2018-07-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Hiérarchie de compte
{: #overview}

Votre compte {{site.data.keyword.Bluemix}} inclut plusieurs composants et systèmes interagissant les uns avec les autres. Le diagramme et les explications ci-dessous présentent chaque composant et ont pour but de vous aider à comprendre comment certains composants sont liés, ou connectés, et comment l'accès fonctionne au sein du compte. 

![{{site.data.keyword.Bluemix_notm}} Diagramme du compte](images/account_diagram.svg "{{site.data.keyword.Bluemix_notm}} Diagramme du compte")

Pour avoir une vue de plus grande taille du diagramme, [cliquez ici](https://console.stage1.bluemix.net/docs/api/content/account/images/account_diagram.svg).

Le diagramme présente deux principaux concepts s'appliquant aux composants de la hiérarchie de compte qu'il est important de bien connaître. L'utilisation de lignes continues et de lignes pointillées indique que certains composants sont inclus dans d'autres. Par exemple, les utilisateurs sont ajoutés à des groupes d'accès ou à des organisations Cloud Foundry. Toutefois, certains composants interagissent avec d'autres afin de fournir l'accès à un élément et non une adhésion à ce dernier. Par exemple, les utilisateurs se voient accorder l'accès à des groupes de ressources mais ne sont pas membres d'un groupe de ressources comme ils le sont d'un groupe d'accès. Ces concepts sont également présentés dans les sections suivantes.

<dl>
<dt>Utilisateurs</dt>
<dd>Les utilisateurs sont invités dans le compte et se voient accorder l'accès à différentes ressources du compte.</dd>
<dt>ID de service</dt>
<dd>Un ID de service identifie un service ou une application de la même façon qu'un ID utilisateur identifie un utilisateur. Vous pouvez utiliser un ID de service que vous créez pour permettre à une application située hors d'{{site.data.keyword.Bluemix_notm}} d'accéder à vos services {{site.data.keyword.Bluemix_notm}}. Vous pouvez affecter des règles d'accès spécifiques à l'ID de service qui limitent les droits d'utilisation à des services spécifiques ou bien combiner des droits d'accès à différents services. Les ID de service n'étant pas liés à un utilisateur spécifique, si un utilisateur quitte une organisation et est supprimé du compte, l'ID de service est conservé de sorte que votre application ou service reste fonctionnel. Pour plus d'informations, voir [Création et utilisation des ID de service](/docs/iam/serviceid.html#serviceids).</dd>
<dt>Ressources ou instances de service</dt>
<dd>Les services dans {{site.data.keyword.Bluemix_notm}} s'appuient sur un groupe de ressources ou sur Cloud Foundry. Les instances de service pouvant être ajoutées à un groupe de ressources et gérées via l'utilisation d'{{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) sont appelées des ressources. Les instances de service ajoutées à des espaces et à des organisations Cloud Foundry ont un autre système de gestion lorsqu'ils utilisent des rôles Cloud Foundry. Pour plus d'informations, voir [Qu'est-ce qu'une ressource ?](/docs/resources/acct_resources.html#resource)</dd>
<dt>Clés d'API</dt>
<dd>Une clé d'interface de programmation (clé d'API) est un code unique transmis à une interface de programmation (API) afin d'identifier l'application ou l'utilisateur appelant. Certaines clés d'API de plateforme sont associées aux identités d'utilisateur et certaines clés d'API peuvent être créées pour les ID de service. Pour plus d'informations, voir [Gestion des clés d'API](/docs/iam/apikeys.html#manapikey).</dd>
<dt>Groupes d'accès</dt>
<dd>Vous pouvez créer un groupe d'accès pour organiser un ensemble d'utilisateurs et d'ID de service dans une seule entité et faciliter l'affectation de droits d'accès. Vous pouvez affecter une seule règle au groupe au lieu d'affecter individuellement le même accès plusieurs fois pour chaque utilisateur ou ID de service. Pour plus d'informations, voir [Configuration de groupes d'accès](/docs/iam/groups.html#groups).</dd>
<dt>Groupes de ressources</dt>
<dd>Un groupe de ressources permet d'organiser vos ressources de compte en regroupements personnalisables de manière à pouvoir affecter rapidement des accès utilisateur à plusieurs ressources à la fois. Chaque ressource de compte gérée à l'aide du contrôle d'accès IAM appartient à un groupe de ressources de votre compte. Les utilisateurs ne sont pas ajoutés aux groupes de ressources mais ils peuvent accéder aux ressources qui s'y trouvent ou peuvent gérer le groupe de ressources. Les utilisateurs disposant de l'accès permettant de gérer le groupe de ressources peuvent créer des instances dans le groupe, gérer les autorisations permettant à d'autres utilisateurs d'utiliser le groupe ou modifier le nom du groupe en fonction du rôle IAM affecté. Pour plus d'informations, voir [Gestion des groupes de ressources](/docs/resources/resourcegroups.html#rgs) et [Meilleures pratiques en matière d'organisation des ressources dans un groupe de ressources](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).</dd>
<dt>Organisations Cloud Foundry</dt>
<dd>En tant que propriétaire de compte ou responsable de l'organisation, vous pouvez ajouter des organisations et des espaces depuis la page Organisations Cloud Foundry dans la console. Les services prenant en charge l'utilisation des espaces et des organisations Cloud Foundry sont ajoutés à un espace et une organisation lorsque vous les créez à partir du catalogue. Les organisations contiennent des utilisateurs, des domaines et des quotas. Dans chaque organisation, des espaces contenant des instances de service sont ajoutés. Pour plus d'informations, voir [Ajout d'organisations et d'espaces](/docs/account/orgs_spaces.html#orgsspacesusers).</dd>
<dt>Espaces Cloud Foundry</dt>
<dd>Dans une organisation, vous pouvez utiliser des espaces pour regrouper un ensemble d'applications, de services et d'utilisateurs. Les espaces sont liés à une région spécifique dans {{site.data.keyword.Bluemix_notm}}. Vous pouvez créer des espaces dans une organisation en fonction du cycle de vie de distribution. Par exemple, vous pouvez créer un espace dev en tant qu'environnement de développement, un espace test en tant qu'environnement de test et un espace production en tant qu'environnement de production. Ensuite, vous pouvez associer vos applications à des espaces. Pour plus d'informations, voir [Ajout d'organisations et d'espaces](/docs/account/orgs_spaces.html#orgsspacesusers).</dd>
</dl>

Un autre aspect important du diagramme est la description des trois types de système de gestion d'accès que vous pouvez utiliser pour accorder aux utilisateurs du compte l'accès aux ressources de ce dernier. 

* Les [rôles d'accès](/docs/iam/users_roles.html#iamusermanrol) IAM permettent d'accorder aux utilisateurs l'accès à toutes les ressources appartenant à un groupe de ressources. Ces rôles d'accès sont également utilisés pour permettre aux utilisateurs de gérer les groupes de ressources et de créer des instances de service qui seront affectées à un groupe de ressources.
* Les [rôles d'organisation et d'espace](/docs/iam/cfaccess.html#cfroles) Cloud Foundry permettent d'accorder aux utilisateurs l'accès à toute instance de service se trouvant dans un espace Cloud Foundry.
* Les droits du [portail client](/docs/customer-portal/cpwhatis.html#customerportal_whatisCP) de l'infrastructure permettent d'accorder aux utilisateurs des [droits](/docs/iam/infrastructureaccess.html#infrapermission) granulaires pour l'accès au portail client ainsi qu'aux fonctions qui s'y trouvent (factures, facturation, configuration d'IaaS, surveillance d'IaaS, achat d'IaaS et support, par exemple). L'accès au périphérique est une opération distincte gérée à partir du périphérique lui-même.
