---

copyright:

  years: 2015, 2018
lastupdated: "2018-01-23"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}

# Trabajo con organizaciones
Como propietario de una cuenta o como un gestor de una organización, puede realizar tareas de gestión de la organización como, por ejemplo, cambiar el nombre de la misma, suprimir la organización, suprimir un espacio, actualizar la organización, actualizar roles de espacio y gestionar dominios o cuotas.
{:shortdesc}

Para gestionar sus organizaciones desde la consola de {{site.data.keyword.Bluemix}}, pulse **Gestionar > Cuenta > Organizaciones de Cloud Foundry**. Sólo puede ver los recursos de una organización cada vez. Si es miembro de varias organizaciones, puede conmutar entre organizaciones desde el enlace de preferencias de cuenta de usuario en la barra de menús de la consola.

## Cambiar el nombre de las organizaciones
{: #orgrename}

Siga los pasos siguientes para cambiar el nombre de la organización:
1. Pulse **Gestionar** > **Cuenta** > **Organizaciones de Cloud Foundry**.
2. Determine qué organización desea renombrar y pulse **Ver detalles**.
3. Pulse **Editar organización de Cloud Foundry**.
4. Pulse **Editar** junto al nombre de la organización.
5. Escriba el nuevo nombre de la organización, y pulse **Guardar**.

## Supresión de organizaciones y espacios
{: #deleteorgs}

### Supresión de una organización

Cuando se suprime una organización, todos los espacios, apps y servicios dentro de la organización se suprimen. Asegúrese de tener en cuenta que las operaciones de supresión no se pueden revertir. Debe ponerse en contacto con el equipo de soporte para suprimir una organización.

### Supresión de un espacio

Complete los siguientes pasos para suprimir un espacio:

1. Pulse **Gestionar** > **Cuenta** > **Organizaciones de Cloud Foundry**.
2. Seleccione la organización que desea editar y pulse **Ver detalles**.
3. Determine qué espacio desea suprimir y pulse **Editar espacio**.
4. Pulse **Suprimir espacio de Cloud Foundry**.

## Edición de roles de usuario
{: #listmembers}

### Edición de roles de usuarios para una organización específica 

Siga los siguientes pasos para editar los roles de usuario de una organización específica:

1. Pulse **Gestionar** > **Cuenta** > **Organizaciones de Cloud Foundry**.
2. Determine qué organización desea editar y pulse **Ver detalles** y luego **Editar organización**.
4. Puede ver los miembros de su organización y sus roles en el separador **USUARIOS**.

### Edición de roles de usuarios para un espacio específico

Siga los siguientes pasos para editar los roles de usuario de un espacio específico:

1. Pulse **Gestionar** > **Cuenta** > **Organizaciones de Cloud Foundry**.
2. Seleccione la organización para la que desea ver los miembros y pulse **Ver detalles**.
3. Determine qué espacio desea editar y pulse **Editar espacio**.
4. Puede ver los miembros de su espacio y sus roles en el separador **USUARIOS**.

## Gestión de cuota
{: #managequota}

Como propietario de cuenta o gestor de organización de {{site.data.keyword.Bluemix_notm}}, puede ver la cuota utilizada y asignada para una organización. La cuota representa los límites de recursos para la organización que está asignada cuando se crea la organización. Los recursos disponibles para una organización varían en función de si tiene una cuenta gratuita o una cuenta facturable. Cualquier aplicación o servicio de un espacio de la organización contribuye al uso de la cuota asignada.

Para ver la cuota utilizada y asignada a una organización, realice los pasos siguientes:

1. Pulse **Gestionar** &gt; **Cuenta** &gt; **Organizaciones de Cloud Foundry**.
2. Identifique la organización para la que desea ver la cuota y pulse **Ver detalles**.
3. Pulse **Editar organización**.
4. Si tiene espacios definidos en más de una región, seleccione la región específica que desee ver.
5. Pulse **CUOTA**. 
6. De forma predeterminada, se abrirá la página de cuota de **Cloud Foundry**. Puede ver los detalles de la cuota para los siguientes recursos:
 * MEMORIA
 * SERVICIOS
 * PLAN
 * PRECIO
7. Pulse **Contenedores** para ver la asignación de cuota de contenedor utilizada y disponible. La asignación de contenedor varía en función del plan de precios. Puede ver los detalles de la cuota para los siguientes recursos:
 * MEMORIA
 * IP PÚBLICA
 * COMPARTICIONES DE ARCHIVOS
8. Pulse **Servidores virtuales** para ver las máquinas virtuales.

Los contenedores no están disponibles en la región Sídney de {{site.data.keyword.Bluemix_notm}}. 
{: tip}

Para obtener más información sobre los contenedores, consulte [Cuota](/docs/containers/container_planning.html#container_planning_quota) en la documentación de Contenedores.
Para cambiar la cuota asignada para una organización, debe abrir una incidencia de soporte. Para obtener más información sobre la apertura de una incidencia de soporte, consulte [Obtención de soporte al cliente](/docs/get-support/howtogetsupport.html#getting-customer-support). 

## Gestión de dominios
{: #managedomains}

Como propietario de cuenta de {{site.data.keyword.Bluemix_notm}} o gestor de organización, puede ver el dominio del sistema y añadir dominios personalizados para aplicaciones que están incluidas dentro una organización y sus espacios. Como gestor de espacios, el separador **Dominios** para un espacio es una lista de solo lectura de los dominios asignados al espacio.

1. Pulse **Gestionar** &gt; **Cuenta** &gt; **Organizaciones de Cloud Foundry**.
2. Identifique la organización para la que desea ver o editar los dominios.
3. Seleccione **Ver detalles** para esa organización.
4. Pulse **Editar organización**.
5. Pulse **DOMINIOS**.

Si añade un dominio personalizado, debe configurar el servidor DNS para resolver el dominio personalizado para que apunte al dominio del sistema de {{site.data.keyword.Bluemix_notm}}. De este modo, cuando {{site.data.keyword.Bluemix_notm}} recibe una solicitud para el dominio personalizado, puede direccionarlo correctamente a la app. El dominio del sistema siempre está disponible en un espacio y también se pueden asignar dominios personalizados a un espacio. Las apps creadas en un espacio pueden utilizar cualquiera de los dominios listados para ese espacio. Para obtener más información sobre cómo crear y utilizar dominios personalizados, consulte [Utilización de un dominio personalizado](/docs/apps/updapps.html#domain).
