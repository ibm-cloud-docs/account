---

copyright:
  years: 2015, 2019
lastupdated: "2019-06-19"

keywords: account, add orgs, add spaces, cloud foundry orgs

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Adición de organizaciones y espacios
{: #orgsspacesusers}

Como propietario de la cuenta de {{site.data.keyword.Bluemix}}, puede añadir organizaciones y espacios a la misma. Si es un gestor de la organización, puede gestionar las organizaciones en la cuenta. 
{:shortdesc}

## Conceptos sobre las organizaciones de Cloud Foundry
{: #cf-org-concepts}

Para gestionar organizaciones y espacios de Cloud Foundry, vaya a **Gestionar** > **Cuenta** y seleccione **Recursos de cuenta > Organizaciones de Cloud Foundry**.

Las organizaciones permiten la colaboración entre usuarios y facilitan la agrupación lógica de recursos del proyecto de las maneras siguientes:

   * Puede agrupar un conjunto de espacios, apps, servicios, dominios, rutas y usuarios conjuntamente en organizaciones.
   * Puede gestionar el acceso de usuario a las organizaciones y espacios de forma individual.

Las organizaciones pueden abarcar varias regiones y se definen por los siguientes elementos:

<dl>
<dt>Espacios</dt>
<dd>Un subgrupo de una organización que puede utilizar para organizar aplicaciones, servicios y usuarios. Los espacios están vinculados a una región específica en {{site.data.keyword.Bluemix_notm}}. </dd>
<dt>Usuarios</dt>
<dd>El rol con permiso básico en las organizaciones y los espacios. Debe estar asignado a una organización para que se le puedan otorgar otros permisos a los espacios en la organización. Para obtener más detalles, consulte [Acceso a Cloud Foundry](/docs/iam?topic=iam-cfaccess).</dd>
<dt>Dominios</dt>
<dd>Proporcione la ruta en Internet que se asigna a la organización. Una ruta tiene un subdominio y un dominio. Un subdominio suele ser el nombre de la aplicación. Un dominio puede ser un dominio del sistema o un dominio personalizado que ha registrado para la aplicación.<br/>
<p>Si añade un dominio personalizado, debe configurar el servidor DNS para resolver el dominio personalizado para que apunte al dominio del sistema de {{site.data.keyword.Bluemix_notm}}. De este modo, cuando {{site.data.keyword.Bluemix_notm}} recibe una solicitud para el dominio personalizado, puede direccionarlo correctamente a la aplicación.</p></dd>
<dt>Cuota</dt>
<dd>Representa recursos disponibles para una organización, incluido el número de servicios y la cantidad de memoria que se puede asignar para que la utilice la organización. Cualquier aplicación o servicio en un espacio de una organización contribuye al uso de la cuota asignada. Con las cuentas de Pago según uso o Suscripción, puede ajustar su cuota para los contenedores y aplicaciones de Cloud Foundry a medida que cambien las necesidades de su organización.</dd>
</dl>

En la cuenta de Suscripción, la cuota es un límite definido por el usuario que desencadena notificaciones de gastos.
{: tip}

## Adición de organizaciones
{: #createorg}

Si tiene una cuenta facturable, puede añadir tantas organizaciones como necesite. Las cuentas Lite solo pueden tener una organización, que ya está creada en la cuenta.

1. Vaya a **Gestionar** > **Cuenta** y seleccione **Recursos de cuenta > Organizaciones de Cloud Foundry**. Pulse **Crear**.
2. Escriba un nombre de organización. El nombre debe ser exclusivo en {{site.data.keyword.Bluemix_notm}}.

   Si el nombre de la organización ya lo utiliza otro usuario local, dedicado o público de {{site.data.keyword.Bluemix_notm}}, debe especificar otro nombre.
3. Pulse **Añadir**.

Después de añadir la organización, se le asigna automáticamente el permiso Gestor de organización, lo que le permite editar el nombre de la organización, añadir usuarios y crear o suprimir espacios en la organización.

Puede asignar los siguientes [roles de Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles) a los usuarios de una organización. A todos los usuarios invitados a la cuenta se les asigna el rol de auditor de forma predeterminada.

   * Gestor de organización
   * Gestor de facturación de organización
   * Auditor de organización

## Adición de espacios
{: #spaceinfo}

En el seno de una organización, podrá utilizar espacios para agrupar un conjunto de aplicaciones, servicios y usuarios. Los espacios se definen dentro de una sola región de {{site.data.keyword.Bluemix_notm}}. Puede crear espacios en una organización en función del ciclo de vida de entrega. Por ejemplo, puede crear un espacio `dev` como entorno de desarrollo, un espacio `test` como entorno de prueba y un espacio `production` como entorno de producción. Luego puede asociar sus apps a los espacios.

Para añadir un espacio a una organización, siga estos pasos.

1. En la página organizaciones de Cloud Foundry, pulse el nombre de la organización a la que desea añadir un espacio.
2. Pulse **Añadir un espacio**.
3. Seleccione una región y especifique un nombre.
4. Pulse **Guardar**.

Tras añadir usuarios a una organización, puede otorgarles permisos a los espacios. Similar a las organizaciones, los espacios también tienen un conjunto de [roles de Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles) que se pueden asignar a los miembros del equipo:

  * Gestor de espacio
  * Desarrollador de espacio
  * Auditor de espacio

A un usuario se le puede asignar como mínimo uno de los permisos en el espacio.
{: tip}
