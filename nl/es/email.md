---

copyright:
  years: 2015, 2019
lastupdated: "2019-06-19"

keywords: platform notifications, email notifications, IBM Cloud notifications, notification preferences, email preferences, user notifications, infrastructure notifications

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:note: .note}
{:screen: .screen}
{:new_window: target="_blank"}


# Configuración de las preferencias de correo electrónico
{: #email-prefs}

En función del tipo de cuenta de {{site.data.keyword.Bluemix}}, puede seleccionar si desea recibir notificaciones de correo electrónico sobre sucesos no planificados de la plataforma {{site.data.keyword.Bluemix}} o notificaciones de correo electrónico de infraestructura sobre sucesos no planificados, mantenimiento y anuncios. También puede optar por establecer suscripciones de notificación para sucesos de infraestructura clásica.
{: shortdesc}

## Establecimiento de notificaciones de plataforma
{: #setting-platform-notifications}

Si es el propietario de una cuenta Lite, puede seleccionar si desea recibir notificaciones de correo electrónico sobre sucesos no planificados de la plataforma {{site.data.keyword.Bluemix}}, como paradas, y sobre sucesos planificados, como los de mantenimiento. Cuando establece notificaciones de la plataforma {{site.data.keyword.Bluemix_notm}}, únicamente recibe notificaciones de correo electrónico asociadas a la plataforma {{site.data.keyword.Bluemix_notm}}. No recibirá notificaciones de correo electrónico sobre sucesos asociados con los servicios de {{site.data.keyword.Bluemix_notm}}.

Puede establecer notificaciones de correo electrónico solo para su perfil, no para la cuenta. En otras palabras, si cambia a otra cuenta, las actualizaciones de notificación de la plataforma que realice abarcarán su perfil y no la cuenta a la que ha cambiado.

Si selecciona recibir sucesos de plataforma no planificados, obtendrá correos electrónicos sobre los problemas que pueden provocar una interrupción (Sev 1). En cualquier momento, puede ver todos los sucesos planificados y no planificados de la página [Estado ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/status){: new_window}.

1. Vaya al icono Avatar ![icono Avatar](../icons/i-avatar-icon.svg) &gt; **Perfil y valores**.
2. Pulse **Notificaciones**.
3. Seleccione si desea recibir notificaciones de plataforma para cada una de las categorías que desea actualizar.

  Todas las notificaciones de plataforma de {{site.data.keyword.Bluemix_notm}} están desactivadas de forma predeterminada.
  {: tip}

4. Pulse **Guardar**.

## Establecimiento de notificaciones de infraestructura

Si es el propietario de una cuenta de Pago según uso o de Suscripción, puede elegir si desea recibir notificaciones por correo electrónico relacionados con la infraestructura de {{site.data.keyword.Bluemix_notm}} sobre sucesos no planificados, mantenimiento y anuncios. Las notificaciones de infraestructura abarcan la cuenta a la que ha cambiado. Puede cambiar a otra cuenta y gestionar notificaciones para dicha cuenta.

1. Vaya al icono Avatar ![icono Avatar](../icons/i-avatar-icon.svg) &gt; **Perfil y valores**.
2. Pulse **Notificaciones**.
3. Seleccione si desea recibir notificaciones de infraestructura para cada una de las categorías que desea actualizar.

  Todas las notificaciones de infraestructura de {{site.data.keyword.Bluemix_notm}} están activadas de forma predeterminada.
  {: tip}

4. Pulse **Guardar**.

## Configuración de notificaciones de usuario
{: #setting-user-notifications}

Solo es posible establecer notificaciones de usuario en los recursos de infraestructura clásica. Si es un propietario de cuenta, puede establecer suscripciones de notificaciones para los usuarios de su cuenta. Las suscripciones son para un conjunto específico de servicios de desarrollador como {{site.data.keyword.autoscaling}} y Raid Alert Monitoring. Cuando el usuario se suscribe a un servicio, recibe correos electrónicos sobre dicho servicio.  

Los usuarios de la cuenta reciben notificaciones de los siguientes tipos de sucesos operativos importantes:

  * Problemas o paradas de infraestructura no planificados: Problemas que podrían causar una interrupción en determinadas condiciones para clientes específicos.
  * Mantenimiento o servicio planificado: Mantenimiento necesario para que la infraestructura siga funcionando en estado óptimo.
  * Vulnerabilidades de seguridad: El área afectada está aislada. Se crea un parche para cerrar la vulnerabilidad y se realizan pruebas para garantizar que no esté afectada ninguna función colateral.
  * Casos de soporte abiertos: Alerta a los usuarios de los casos abiertos en su cuenta.

La hora de la notificación varía en función de si el suceso está o no planificado. La política de la infraestructura de {{site.data.keyword.BluSoftlayer_notm}} es remediar problemas lo antes posible para eliminar o minimizar el riesgo de más problemas al desarrollar lo que podría tener un mayor impacto. A veces incluso el mantenimiento planificado se realiza con solo una notificación brevemente avanzada.

Para configurar notificaciones de suscripción para los usuarios, complete los pasos siguientes:

  1. Vaya a **Gestionar > Cuenta** y seleccione **Notificaciones**.
  2. Seleccione un servicio de la tabla.
  3. En la columna Suscrito, seleccione **Sí** para el usuario que desea recibir notificaciones.

    Para encontrar el usuario fácilmente, pulse en **Filtrar** y filtre por nombre, apellido o nombre de usuario.
    {: tip}
