---

copyright:

  years: 2015, 2018
lastupdated: "2018-03-19"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Actualización de organizaciones y espacios
{: #orgupdates}

Como propietario de cuenta o gestor de organización, puede realizar tareas de gestión a nivel de organización y de espacio. Estas tareas incluyen renombrar una organización o espacio, asignar o actualizar roles de usuario de Cloud Foundry, gestionar dominios y visualizar detalles de cuota de organización. 
{:shortdesc}

Para gestionar sus organizaciones desde la consola de {{site.data.keyword.Bluemix}}, pulse **Gestionar > Cuenta > Organizaciones de Cloud Foundry**. Solo puede ver los recursos de una organización a la vez. Si es miembro de varias organizaciones, puede conmutar entre organizaciones desde el enlace de preferencias de cuenta de usuario en la barra de menús de la consola.

## Cambiar el nombre de las organizaciones
{: #orgrename}

Complete los pasos siguientes para renombrar su organización. Tenga en cuenta que los cambios que realice se aplicarán a todos los usuarios de la organización.

1. Pulse **Gestionar** > **Cuenta** > **Organizaciones de Cloud Foundry**.
2. Pulse el icono Acciones de la organización que desea renombrar y seleccione **Renombrar**.  
3. Especifique el nuevo nombre y pulse **Guardar**.

## Supresión de organizaciones y espacios
{: #deleteorgs}

### Supresión de una organización

Para suprimir una organización, póngase en contacto con el [Soporte](/docs/get-support/howtogetsupport.html). Cuando se suprime una organización, todos los espacios y recursos de la misma también se suprimen. Asegúrese de tener en cuenta que las operaciones de supresión no se pueden revertir. 

### Supresión de un espacio

Cuando suprime un espacio, también se suprimen todos los recursos y usuarios incluidos. Complete los siguientes pasos para suprimir un espacio:

1. Pulse **Gestionar** > **Cuenta** > **Organizaciones de Cloud Foundry**.
2. Pulse la organización en la que se ha asignado el espacio.
3. Pulse el icono Acciones y seleccione **Suprimir**.
4. Confirme que desea suprimir el espacio escribiendo el nombre del espacio en el campo y pulse **Suprimir**.

## Edición de roles de usuario
{: #listmembers}

Los roles que puede asignar a nivel de organización son Gestor, Gestor de facturación y Auditor. Los roles que puede asignar a nivel de espacio son Gestor, Desarrollador y Auditor. Para obtener una descripción detallada de los roles, consulte [Roles de Cloud Foundry](/docs/iam/cfaccess.html#cfroles).

### Edición de roles de usuario a nivel de organización

Complete los pasos siguientes para editar los roles de usuario de una organización específica:

1. Pulse **Gestionar** > **Cuenta** > **Organizaciones de Cloud Foundry**.
2. Pulse el icono Acciones y seleccione **Usuarios**.
3. En función de como desea modificar los permisos de usuario, seleccione o desmarque el recuadro de selección de un rol específico.
4. Confirme los cambios pulsando **Guardar**. 

### Edición de roles de usuario a nivel de espacio

Siga los siguientes pasos para editar los roles de usuario de un espacio específico:

1. Pulse **Gestionar** > **Cuenta** > **Organizaciones de Cloud Foundry**.
2. Pulse la organización en la que se ha asignado el espacio.
3. Pulse el nombre del espacio.
4. En función de como desea modificar los permisos de usuario, seleccione o desmarque el recuadro de selección de un rol específico.
5. Confirme los cambios pulsando **Guardar**.

## Gestión de dominios
{: #managedomains}

Como propietario de cuenta o gestor de organización, puede ver el dominio del sistema y añadir dominios personalizados para aplicaciones que están incluidas dentro una organización y sus espacios. Como gestor de espacios, el separador **Dominios** es una lista de solo lectura de los dominios asignados al espacio.

1. Pulse **Gestionar** &gt; **Cuenta** &gt; **Organizaciones de Cloud Foundry**.
2. Pulse el icono Acciones de la organización y seleccione **Dominios**.

Si añade un dominio personalizado, debe configurar el servidor DNS para resolver el dominio personalizado para que apunte al dominio del sistema de {{site.data.keyword.Bluemix_notm}}. De este modo, cuando {{site.data.keyword.Bluemix_notm}} recibe una solicitud para el dominio personalizado, se direcciona correctamente a la app. El dominio del sistema siempre está disponible en un espacio y también se pueden asignar dominios personalizados a un espacio. Las apps creadas en un espacio pueden utilizar cualquiera de los dominios listados para ese espacio. Para obtener más información sobre cómo crear y utilizar dominios personalizados, consulte [Utilización de un dominio personalizado](/docs/apps/updapps.html#domain).

## Gestión de cuotas
{: #managequota}

Puede visualizar la cuota utilizada y asignada de una organización. La cuota representa los límites de recursos de la organización, que se asigna cuando se crea la organización. Los recursos disponibles para una organización varían en función de si tiene una cuenta gratuita o una cuenta facturable. Cualquier aplicación o servicio incluido en un espacio de la organización contribuye al uso de la cuota asignada.

Para ver la cuota utilizada y asignada a una organización, realice los pasos siguientes:

1. Pulse **Gestionar** &gt; **Cuenta** &gt; **Organizaciones de Cloud Foundry**.
2. Pulse el icono Acciones de la organización específica y seleccione **Cuotas**.

   De forma predeterminada, se mostrará la página de cuota de **Cloud Foundry**. Desde aquí, puede visualizar los detalles de la cuota de los recursos siguientes:
 
   * El número de apps
   * La cantidad de memoria 
   * El número de servicios 
   * Detalles del plan 

3. Expanda los detalles de región para ver la cuota a nivel de espacio. 

Para cambiar la cuota asignada para una organización debe abrir una incidencia de soporte. Para obtener más información, consulte [Obtención de soporte al cliente](/docs/get-support/howtogetsupport.html#getting-customer-support). 

