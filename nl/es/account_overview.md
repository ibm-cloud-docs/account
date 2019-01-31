---

copyright:

  years: 2019
lastupdated: "2019-01-21"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Jerarquía de cuentas
{: #overview}

Su cuenta de {{site.data.keyword.Bluemix}} incluye varios componentes y sistemas que interactúan. Obtener una idea sobre cómo determinados componentes están conectados y cómo funciona el acceso en toda su cuenta. 
{:shortdesc}

<a href="https://console.bluemix.net/docs/api/content/account/images/account_diagram.svg">
  <img src="images/account_diagram.svg" alt="diagrama de cuenta">
</a>

Dentro del diagrama, hay dos conceptos principales correspondiente a la jerarquía de cuentas que debe comprender. El uso de líneas continuas y de líneas de puntos ayuda a mostrar que algunos componentes están contenidos dentro de otros; por ejemplo, los usuarios se añaden a grupos de usuarios o a organizaciones de Cloud Foundry. Sin embargo, algunos componentes interactúan con otros para ofrecer acceso en lugar de pertenencia a grupo. Por ejemplo, se otorga a los usuarios acceso a grupos de recursos, pero no son miembros de un grupo de recursos del mismo modo que lo son de los grupos de acceso. Estos conceptos se explican en las secciones siguientes.

<dl>
<dt>Usuarios</dt>
<dd>Se invita a los usuarios a la cuenta y se les otorga acceso a los recursos de la cuenta.</dd>
<dt>ID de servicio</dt>
<dd>Un ID de servicio identifica un servicio o una aplicación de forma similar a cómo un ID de usuario identifica un usuario. Puede utilizar un ID de servicio que cree para habilitar una aplicación fuera del acceso de {{site.data.keyword.Bluemix_notm}} a sus servicios de {{site.data.keyword.Bluemix_notm}}. Puede asignar políticas de acceso específicas al ID de servicio que restrinjan permisos para utilizar servicios específicos, o incluso combinar permisos para acceder a servicios distintos. Puesto que los ID de servicio no están vinculados a un usuario específico, si un usuario abandona una organización y se suprime de la cuenta, el ID de servicio seguirá garantizando que su aplicación o servicio permanece activo y en ejecución. Para obtener más información, consulte [Cómo crear y trabajar con ID de servicio](/docs/iam/serviceid.html#serviceids).</dd>
<dt>Instancias de servicio o recursos</dt>
<dd>Los servicios de {{site.data.keyword.Bluemix_notm}} se pueden basar en grupo de recursos o en Cloud Foundry. Las instancias de servicio que se pueden añadir a un grupo de recursos y gestionar mediante {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) se denominan recursos. Las instancias de servicio que se añaden a organizaciones y espacios de Cloud Foundry tienen otro sistema de gestión de acceso mediante el uso de roles de Cloud Foundry. Para obtener más información, consulte [¿Qué es un recurso?](/docs/resources/acct_resources.html#resource)</dd>
<dt>Claves de API</dt>
<dd>Una clave de API es un código exclusivo que se pasa a una API para identificar al usuario o la aplicación que la llama. Puede utilizar las claves de API de la plataforma, que están asociadas con las identidades de usuario, y crear otras claves de API para los ID de servicio. Para obtener más información, consulte [Comprensión de claves de API](/docs/iam/apikeys.html#manapikey).</dd>
<dt>Grupos de acceso</dt>
<dd>Puede crear un grupo de acceso para organizar un conjunto de usuarios e ID de servicio en una sola entidad, lo que le facilita la asignación de permisos. Puede asignar una única política al grupo en lugar de asignar el mismo acceso varias veces por usuario individual o ID de servicio. Para obtener más información, consulte el apartado [Configuración de grupos de acceso](/docs/iam/groups.html#groups).</dd>
<dt>Grupos de recursos</dt>
<dd>Puede utilizar un grupo de recursos para organizar sus recursos de cuenta en agrupaciones personalizables para que pueda asignar accesos de usuario rápidamente a más de un recurso a la vez. Cualquier recurso de cuenta que se gestione mediante el control de acceso de IAM pertenece a un grupo de recursos dentro de su cuenta. Los usuarios no se añaden a grupos de recursos, sino que se les otorga acceso a los recursos que contienen o bien pueden gestionar el grupo de recursos. Los usuarios a los que se otorga acceso para gestionar el grupo de recursos pueden crear nuevas instancias dentro del grupo, gestionar el acceso de otros usuarios para que trabajen con el grupo o editar el nombre del grupo en función de rol de IAM asignado. Para obtener más información, consulte [Gestión de grupos de recursos](/docs/resources/resourcegroups.html#rgs) y [Prácticas recomendadas para organizar recursos en grupos de recursos](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).</dd>
<dt>Organizaciones de Cloud Foundry</dt>
<dd>Como propietario de una cuenta o gestor de la organización, puede añadir organizaciones y espacios desde la página Organizaciones de Cloud Foundry de la consola. Los servicios que permiten utilizar organizaciones y espacios de Cloud Foundry se añaden a una organización o espacio cuando se crean desde el catálogo. Las organizaciones contienen usuarios, dominios y cuotas. Dentro de cada organización se añaden espacios, que contienen las instancias de servicio. Para obtener más información, consulte [Adición de organizaciones y espacios](/docs/account/orgs_spaces.html#orgsspacesusers).</dd>
<dt>Espacios de Cloud Foundry</dt>
<dd>En el seno de una organización, podrá utilizar espacios para agrupar un conjunto de aplicaciones, servicios y usuarios. Los espacios están vinculados a una región específica en {{site.data.keyword.Bluemix_notm}}. Puede crear espacios en una organización en función del ciclo de vida de entrega. Por ejemplo, puede crear un espacio dev como entorno de desarrollo, un espacio test como entorno de prueba y un espacio production como entorno de producción. Luego puede asociar sus apps a los espacios. Para obtener más información, consulte [Adición de organizaciones y espacios](/docs/account/orgs_spaces.html#orgsspacesusers).</dd>
</dl>

Otro aspecto importante del diagrama anterior es la representación de los tres tipos de sistemas de gestión de acceso que puede utilizar para otorgar a los usuarios de la cuenta acceso a los recursos de la misma. 

  * Puede utilizar los [roles de acceso](/docs/iam/users_roles.html#iamusermanrol) para otorgar a los usuarios acceso a todos los recursos pertenecientes a un grupo de recursos. También puede proporcionar a los usuarios acceso para gestionar grupos de recursos y crear nuevas instancias de servicio que se asignan a un grupo de recursos.
  * Puede utilizar los [roles de organización y de espacio](/docs/iam/cfaccess.html#cfroles) de Cloud Foundry para otorgar a los usuarios acceso a cualquier instancia de servicio que resida en un espacio de Cloud Foundry.
  * Puede utilizar permisos de infraestructura clásica para otorgar a los usuarios [permisos](/docs/iam/infrastructureaccess.html#infrapermission) más detallados a la infraestructura clásica. Puede asignar el acceso de dispositivo y el acceso de subred VPN por separado.
