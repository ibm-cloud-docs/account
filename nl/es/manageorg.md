---

copyright:
  years: 2015, 2019
lastupdated: "2019-01-28"

keywords: account owner, user roles, manage account, orgs, spaces

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# Actualización de organizaciones y espacios
{: #orgupdates}

Como propietario de la cuenta de {{site.data.keyword.Bluemix}} o gestor de organización, puede realizar tareas de gestión a nivel de organización y de espacio. Estas tareas incluyen renombrar una organización o espacio, asignar o actualizar roles de usuario de Cloud Foundry, gestionar dominios y visualizar detalles de cuota de organización.
{:shortdesc}

Vaya a **Gestionar > Cuenta** y seleccione **Organizaciones de Cloud Foundry**.

Solo puede ver los recursos de una única organización a la vez. Si es miembro de varias organizaciones, puede conmutar entre organizaciones desde el enlace de preferencias de cuenta de usuario en la barra de menús de la consola.
{: tip}

  * Para cambiar el nombre de la organización, pulse en el icono Acciones ![icono Acción](../icons/action-menu-icon.svg) de la organización que desea volver a nombrar y seleccione **Renombrar**.
    {: #orgrename}

    Los cambios que realice se aplicarán a todos los usuarios de la organización.

  * Para suprimir una organización, póngase en contacto con el [Soporte](/docs/get-support?topic=get-support-getting-customer-support).
    {: #deleteorgs}

    Cuando se suprime una organización, todos los espacios y recursos de la misma también se suprimen. Esta acción no se puede revertir.

  * Para suprimir un espacio, seleccione la organización en la que se ha asignado el espacio. A continuación, pulse en el icono Acciones ![icono Acción](../icons/action-menu-icon.svg) y seleccione **Suprimir**.

    Cuando suprime un espacio, también se suprimen todos los recursos y usuarios incluidos.

  * Para editar los roles de usuario en el nivel de organización, pulse en el icono Acciones ![icono Acción](../icons/action-menu-icon.svg) y seleccione **Usuarios**.
    {: #listmembers}

    En función de como desea modificar los permisos de usuario, seleccione o desmarque el recuadro de selección de un rol específico. Los roles que puede asignar a nivel de organización son Gestor, Gestor de facturación y Auditor. Para obtener más información, consulte [Roles de Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles).

  * Para editar roles de usuario en un espacio específico, seleccione la organización en la que se ha asignado el espacio. A continuación, pulse en el nombre del espacio.

    En función de como desea modificar los permisos de usuario, seleccione o desmarque el recuadro de selección de un rol específico. Los roles que puede asignar a nivel de espacio son Gestor, Desarrollador y Auditor. Para obtener más información, consulte [Roles de Cloud Foundry](/docs/iam?topic=iam-cfaccess#cfroles).

  * Para gestionar los dominios, pulse el icono Acciones ![icono Acción](../icons/action-menu-icon.svg) de la organización correspondiente y seleccione **Dominios**.
    {: #managedomains}

    Como propietario de cuenta o gestor de organización, puede ver el dominio del sistema y añadir dominios personalizados para aplicaciones que están incluidas dentro una organización y sus espacios. Si es un gestor de espacios, esta página mostrará una lista de solo lectura de los dominios asignados al espacio.

    Si añade un dominio personalizado, debe configurar el servidor DNS para resolver el dominio personalizado para que apunte al dominio del sistema de {{site.data.keyword.Bluemix_notm}}. De este modo, cuando {{site.data.keyword.Bluemix_notm}} recibe una solicitud para el dominio personalizado, se direcciona correctamente a la app. El dominio del sistema siempre está disponible en un espacio y también se pueden asignar dominios personalizados a un espacio. Las apps creadas en el espacio pueden utilizar cualquiera de los dominios listados para dicho espacio. Para obtener más información sobre cómo crear y utilizar dominios personalizados, consulte [Gestión de dominios](/docs/apps?topic=creating-apps-update-domain).

  * Para gestionar todas las cuotas asignadas de una organización, haga clic en el icono Acciones ![icono Acción](../icons/action-menu-icon.svg) de la organización correspondiente y seleccione **Cuotas**.
    {: #managequota}

    Desde aquí, puede visualizar los detalles de la cuenta del número de apps, la cantidad de memoria, el número de servicios y los detalles del plan. La cuota representa los límites de recursos para la organización que está asignada cuando se crea la organización. Los recursos disponibles para una organización varían en función de si tiene una cuenta gratuita o una cuenta facturable. Cualquier aplicación o servicio incluido en un espacio de la organización contribuye al uso de la cuota asignada.

    Para cambiar la cuota asignada a una organización debe crear un caso de soporte. Para obtener más información, consulte [Cómo trabajar con casos de soporte](/docs/get-support?topic=get-support-open-case).

    Para visualizar los detalles de la cuota en el nivel de espacio de cada ubicación, pulse en el icono Acciones ![icono Acción](../icons/action-menu-icon.svg) de la organización correspondiente y seleccione **Cuotas**. A continuación, expanda cada fila según convenga.
