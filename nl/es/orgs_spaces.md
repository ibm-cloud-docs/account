---

copyright:

  years: 2015, 2018
lastupdated: "2018-01-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Creación de organizaciones y espacios
{: #orgsspacesusers}

Como propietario de la cuenta, puede gestionar las organizaciones y los espacios desde la página Gestionar organizaciones en la consola de {{site.data.keyword.Bluemix}}. Los gestores de organizaciones también pueden utilizar la página Gestionar organizaciones para gestionar todas las organizaciones en las que se han establecido como gestor.
{:shortdesc}

Para gestionar organizaciones y espacios, pulse **Gestionar** &gt; **Cuenta** &gt; **Organizaciones de Cloud Foundry**. 


## Creación de organizaciones
{: #createorg}

Las organizaciones pueden abarcar varias regiones y se definen por los siguientes elementos:

<dl>
<dt>Usuarios</dt>
<dd>El rol con permiso básico en las organizaciones y los espacios. Debe asignarse previamente a una organización
para que se le puedan otorgar otros permisos a los espacios en el seno de la organización. Para ver información detallada,
consulte [Usuarios y roles](/docs/iam/users_roles.html#userrolesinfo).</dd>
<dt>Dominios</dt>
<dd>Proporciona la ruta en Internet que se asigna a la organización. Una ruta tiene un subdominio y un dominio. Un subdominio suele ser el nombre de la app. Un dominio puede ser un dominio del sistema o un dominio personalizado que ha registrado para la aplicación. Consulte [Gestión de dominios personalizados](/docs/account/manageorg.html#managedomains).<br/>
<p>**Nota:** Si añade un dominio personalizado, debe configurar el servidor DNS para resolver el dominio personalizado para que apunte al dominio del sistema de {{site.data.keyword.Bluemix_notm}}. De este modo, cuando {{site.data.keyword.Bluemix_notm}} recibe una solicitud para el dominio personalizado, puede direccionarlo correctamente a la app.</p></dd>
<dt>Cuota</dt>
<dd>Representa recursos disponibles para una organización, incluido el número de servicios y la cantidad de memoria que se puede asignar para que la utilice la organización. Las cuotas se asignan cuando se crean organizaciones. Cualquier aplicación o servicio en un espacio de una organización contribuye al uso de la cuota asignada. Con las cuentas de Pago según uso o Suscripción, puede ajustar su cuota para los contenedores y apps de Cloud Foundry a medida que cambien las necesidades de su organización. Consulte [Gestión de cuota](/docs/account/manageorg.html#managequota).</dd>
</dl>

En la cuenta de Suscripción, la cuota es un límite definido por el usuario que desencadena notificaciones de gastos.
{: tip}

En {{site.data.keyword.Bluemix_notm}},
puede utilizar organizaciones para habilitar la colaboración entre usuarios y para facilitar la agrupación lógica de recursos del proyecto de las maneras siguientes:

   * Puede agrupar un conjunto de espacios, apps, servicios, dominios, rutas y usuarios conjuntamente en organizaciones. 
   * Puede gestionar el acceso a los espacios y a las organizaciones usuario a usuario. 

Cuando se crea una organización, el nombre debe ser exclusivo en {{site.data.keyword.Bluemix_notm}}. Si el nombre de la organización ya lo utiliza otro usuario local, dedicado o público de {{site.data.keyword.Bluemix_notm}}, debe especificar un nuevo nombre. Después de crear la organización, se le asigna automáticamente el permiso *Gestor de organización*, lo que le permite editar el nombre de la organización, añadir usuarios y crear o suprimir espacios en la organización.

Utilice el mandato [`bx iam org-delete`](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_iam_org_delete) para suprimir organizaciones. Cuando se suprime una organización, todos los espacios, apps y servicios dentro de la organización se suprimen.

Los siguientes [roles de usuario](/docs/iam/users_roles.html#userrolesinfo) pueden asignarse a usuarios en una organización. A todos los usuarios invitados a la cuenta se les asigna el rol de Auditor de forma predeterminada.

   * Gestor de organización
   * Gestor de facturación de organización
   * Auditor de organización

Puede crear una organización completando los siguientes pasos:

1. Pulse **Gestionar** &gt; **Cuenta** &gt; **Organizaciones de Cloud Foundry**.
2. Pulse **Añadir una nueva organización de Cloud Foundry**.
3. Escriba el nombre de la organización.
4. Pulse **Añadir**.

<!-- Add info on Manage infrastructure option under a space -->

## Creación de espacios
{: #spaceinfo}

En el seno de una organización, podrá utilizar espacios para agrupar un conjunto de apps, servicios y usuarios. Los espacios están vinculados a una región específica en {{site.data.keyword.Bluemix_notm}}.

Tras añadir usuarios a una organización, puede otorgarles permisos a los espacios. Similar a las organizaciones, los espacios también tienen un conjunto de [roles de usuario](/docs/iam/users_roles.html#userrolesinfo) que se pueden asignar a los miembros del equipo:

  * Gestor de espacio
  * Desarrollador de espacio
  * Auditor de espacio

A un usuario se le puede asignar como mínimo uno de los permisos en el espacio.
{: tip}

Puede crear espacios en la organización; por ejemplo, un espacio *dev* como entorno de desarrollo, un espacio *test* como entorno de prueba y un espacio *production* como entorno de producción. Luego puede asociar sus apps a los espacios. Complete los siguientes pasos para crear un espacio:

1. Pulse **Gestionar** &gt; **Cuenta** &gt; **Organizaciones de Cloud Foundry**.
2. Determine la organización a la que desea añadir un espacio y seleccione **Ver detalles**.
4. Pulse **Añadir un espacio de Cloud Foundry**.
5. Especifique el nombre de espacio.
6. Pulse **Añadir**.
