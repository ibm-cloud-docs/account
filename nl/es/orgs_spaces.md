---

copyright:

  years: 2015, 2018
lastupdated: "2018-03-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Adición de organizaciones y espacios
{: #orgsspacesusers}

Como propietario de la cuenta, puede añadir organizaciones y espacios desde la página Organizaciones de Cloud Foundry en la consola de {{site.data.keyword.Bluemix}}. Si es un gestor de organización, también puede utilizar la página Organizaciones de Cloud Foundry para gestionar sus organizaciones.
{:shortdesc}

Puede utilizar organizaciones para habilitar la colaboración entre usuarios y facilitar la agrupación lógica de recursos del proyecto de las maneras siguientes:

   * Puede agrupar un conjunto de espacios, apps, servicios, dominios, rutas y usuarios conjuntamente en organizaciones. 
   * Puede gestionar el acceso de usuario a las organizaciones y espacios de forma individual. 

## Adición de organizaciones
{: #createorg}

Las organizaciones pueden abarcar varias regiones y se definen por los siguientes elementos:

<dl>
<dt>Usuarios</dt>
<dd>El rol con permiso básico en las organizaciones y los espacios. Debe estar asignado a una organización para que se le puedan otorgar otros permisos a los espacios en la organización. Para obtener más detalles, consulte [Usuarios y roles](/docs/iam/users_roles.html#userrolesinfo).</dd>
<dt>Dominios</dt>
<dd>Proporciona la ruta en Internet que se asigna a la organización. Una ruta tiene un subdominio y un dominio. Un subdominio suele ser el nombre de la app. Un dominio puede ser un dominio del sistema o un dominio personalizado que ha registrado para la aplicación. Consulte [Gestión de dominios personalizados](/docs/account/manageorg.html#managedomains).<br/>
<p>**Nota:** Si añade un dominio personalizado, debe configurar el servidor DNS para resolver el dominio personalizado para que apunte al dominio del sistema de {{site.data.keyword.Bluemix_notm}}. De este modo, cuando {{site.data.keyword.Bluemix_notm}} recibe una solicitud para el dominio personalizado, puede direccionarlo correctamente a la app.</p></dd>
<dt>Cuota</dt>
<dd>Representa recursos disponibles para una organización, incluido el número de servicios y la cantidad de memoria que se puede asignar para que la utilice la organización. Cualquier aplicación o servicio en un espacio de una organización contribuye al uso de la cuota asignada. Con las cuentas de Pago según uso o Suscripción, puede ajustar su cuota para los contenedores y apps de Cloud Foundry a medida que cambien las necesidades de su organización. Consulte [Gestión de cuota](/docs/account/manageorg.html#managequota).</dd>
</dl>

En la cuenta de Suscripción, la cuota es un límite definido por el usuario que desencadena notificaciones de gastos.
{: tip}

Cuando añade una organización, el nombre debe ser exclusivo en {{site.data.keyword.Bluemix_notm}}. Si el nombre de la organización ya lo utiliza otro usuario local, dedicado o público de {{site.data.keyword.Bluemix_notm}}, debe especificar uno nuevo. Después de añadir la organización, se le asigna automáticamente el permiso Gestor de organización, que le permite editar el nombre de la organización, añadir usuarios y crear o suprimir espacios de la organización. Si tiene una cuenta facturable, puede añadir tantas organizaciones como desee. Sin embargo, en una cuenta Lite solo podrá tener una organización. 

Los [roles de usuario](/docs/iam/users_roles.html#userrolesinfo) siguientes pueden asignarse a usuarios en una organización. A todos los usuarios invitados a la cuenta se les asigna el rol de auditor de forma predeterminada.

   * Gestor de organización
   * Gestor de facturación de organización
   * Auditor de organización

Complete los pasos siguientes para añadir una organización:

1. Pulse **Gestionar** &gt; **Cuenta** &gt; **Organizaciones de Cloud Foundry**.
2. Pulse **Añadir una organización**.
3. Escriba el nombre de la organización. 
4. Pulse **Añadir**.

<!-- Add info on Manage infrastructure option under a space -->

## Adición de espacios
{: #spaceinfo}

En el seno de una organización, podrá utilizar espacios para agrupar un conjunto de apps, servicios y usuarios. Los espacios están vinculados a una región específica en {{site.data.keyword.Bluemix_notm}}. Puede crear espacios en una organización en función del ciclo de vida de entrega. Por ejemplo, puede crear un espacio `dev` como entorno de desarrollo, un espacio `test` como entorno de prueba y un espacio `production` como entorno de producción. Luego puede asociar sus apps a los espacios.

Tras añadir usuarios a una organización, puede otorgarles permisos a los espacios. Similar a las organizaciones, los espacios también tienen un conjunto de [roles de usuario](/docs/iam/users_roles.html#userrolesinfo) que se pueden asignar a los miembros del equipo:

  * Gestor de espacio
  * Desarrollador de espacio
  * Auditor de espacio

A un usuario se le puede asignar como mínimo uno de los permisos en el espacio.
{: tip}

Complete los pasos siguientes para añadir un espacio:

1. Pulse **Gestionar** &gt; **Cuenta** &gt; **Organizaciones de Cloud Foundry**.
2. Pulse el nombre de la organización en la que desea añadir un espacio.
4. Pulse **Añadir un espacio**.
5. Seleccione una región y especifique un nombre.
6. Pulse **Guardar**.
