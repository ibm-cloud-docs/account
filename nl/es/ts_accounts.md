---

copyright:

  years: 2015, 2018

lastupdated: "2018-07-16"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Resolución de problemas de gestión de cuentas
{: #managingaccounts}

Los problemas generales con la gestión de la cuenta pueden incluir que distintas
apps compartan el mismo nombre de dominio o que los administradores no puedan ver
todas las organizaciones. En muchos de los casos, puede solucionar estos problemas siguiendo unos sencillos pasos.
{:shortdesc}

## No es posible acceder a otra región diferente de {{site.data.keyword.Bluemix_notm}}
{: #nosecondreg}

Puede recibir un mensaje de error al intentar crear una nueva región de {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Es probable que esto ocurra por estar utilizando una cuenta Lite, que únicamente soporta el desarrollo en una región pública. La región pública de {{site.data.keyword.Bluemix_notm}} en la que desea trabajar se elige cuando se configura la cuenta por primera vez.
{: tsCauses}

Si tiene una cuenta Lite, puede actualizarla a una cuenta facturable para acceder a más regiones. Vaya a la página **Gestionar > Facturación y utilización > Facturación** en la consola y, a continuación, pulse **Añadir tarjeta de crédito**. En la página **Facturación**, también puede comprobar si tiene una cuenta Lite.
{: tsResolve}

## No es posible crear una nueva organización
{: #nosecondorg}

Puede recibir un mensaje de error al intentar crear una nueva organización.
{: tsSymptoms}

Es probable que esto ocurra por estar utilizando una cuenta Lite, que únicamente da soporte al desarrollo en una organización. La organización la crea cuando configura la cuenta por primera vez.
{: tsCauses}

Si tiene una cuenta Lite, puede actualizarla a una cuenta facturable para acceder a más organizaciones. Vaya a la página **Gestionar > Facturación y utilización > Facturación** en la consola y, a continuación, pulse **Añadir tarjeta de crédito**. En la página **Facturación**, también puede comprobar si tiene una cuenta Lite.
{: tsResolve}

## No es posible crear la instancia de plan Lite
{: #nosecondlite}

Puede recibir el siguiente mensaje de error al intentar crear una instancia de plan Lite:
{: tsSymptoms}

`No es posible aprovisionar una nueva instancia de Lite`

Hay un límite de una instancia de plan Lite para mantener estos planes gratuitos.
{: tsCauses}

Es posible crear instancias adicionales del servicio seleccionando uno de los planes de servicios facturables, que también están disponibles en las cuentas facturables. Para actualizar a una cuenta facturable desde la consola, vaya a la página **Gestionar > Facturación y utilización > Facturación ** y, a continuación, pulse **Añadir tarjeta de crédito**.
{: tsResolve}

Si no desea actualizar la cuenta Lite y ya no está utilizando la instancia de servicio Lite existente, puede suprimir dicha instancia de plan Lite desde el panel de control y, a continuación, crear una nueva instancia.

## Se ha excedido la concesión de memoria de tiempo de ejecución
{: #noruntimemem}

No puede desplegar apps y aparece un error que indica que ha superado el límite de memoria de su organización.
{: tsSymptoms}

En una cuenta Lite, sus apps de Cloud Foundry pueden utilizar hasta 256 MB de memoria de tiempo de ejecución instantánea. En las cuentas facturables, hay un límite de 2 GB de memoria.
{: tsCauses}

Si está utilizando una cuenta Lite, puede obtener memoria adicional actualizando a una cuenta facturable. Vaya a la página **Gestionar > Facturación y utilización > Facturación** en la consola y, a continuación, pulse **Añadir tarjeta de crédito**.
{: tsResolve}

Si no desea actualizar la cuenta Lite y tiene apps desocupadas, puede suprimirlas para liberar memoria de tiempo de ejecución.

## La cuenta está inactiva
{: #ts_accnt_inactive}

No puede crear una app en {{site.data.keyword.Bluemix_notm}} si la cuenta está inactiva. Debe ponerse en contacto con el equipo de soporte para solucionar este problema.

Cuando intenta crear una app en {{site.data.keyword.Bluemix_notm}}, ve el siguiente mensaje de error:
{: tsSymptoms}

`BXNUI0096E: La app no se ha creado. La cuenta está inactiva porque se ha cancelado o suspendido.`

El estado de la cuenta de {{site.data.keyword.Bluemix_notm}} pasa a ser inactivo si la cuenta se cancela o se suspende.
{: tsCauses}

Para volver a activar la cuenta, póngase en contacto con el [equipo de soporte de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://ibm.biz/bluemixsupport.com){: new_window}. Incluya la siguiente información en el correo electrónico:
{: tsResolve}

  * El IBMid que utiliza para iniciar la sesión en {{site.data.keyword.Bluemix_notm}}.
  * El nombre de la organización en la que se está creando la app. Esta información puede ayudar al equipo de soporte a determinar si se le han asignado los roles o pertenencia a grupos correctos en la organización.

## No se pueden añadir usuarios a una organización
{: #ts_adduser}

Puede invitar a más de un usuario a trabajar en la misma organización. Solo puede invitar usuarios a su organización si es el propietario de la cuenta o si es gestor de la organización.

No ve el enlace **Invitar a un nuevo usuario** en la sección **Gestionar organizaciones**.
{: tsSymptoms}

Únicamente los siguientes usuarios de {{site.data.keyword.Bluemix_notm}}
pueden invitar a usuarios a una organización:
{: tsCauses}
  * El propietario de la cuenta de la organización
  * Gestores de la organización

**Nota:** Todos los gestores de la organización pueden añadir, modificar y eliminar los usuarios que ya están en la organización.

Si no puede invitar usuarios a su organización, póngase en contacto con el gestor de la organización. Para identificar el gestor de la organización, siga estos pasos:
{: tsResolve}

  1. Desde la barra de menús, pulse **Gestionar > Cuenta > Organizaciones**.
  2. Vaya a la organización y consulte la información sobre el gestor de la organización en el separador **USUARIOS**.  

## No se da soporte al registro por lotes de usuarios
{: #ts_batchregistration}

Cuando registre usuarios para {{site.data.keyword.Bluemix_notm}},
debe registrar cada usuario por separado.

{{site.data.keyword.Bluemix_notm}} no ofrece la posibilidad de registrar varios usuarios a la vez.
{: tsSymptoms}

{{site.data.keyword.Bluemix_notm}} no da soporte al registro por lotes de usuarios. Para registrar usuarios para {{site.data.keyword.Bluemix_notm}}, debe registrar cada usuario por separado.
{: tsCauses}

Para registrar varios usuarios para {{site.data.keyword.Bluemix_notm}},
siga los pasos siguientes para cada usuario:
{: tsResolve}

  1. Pulse **REGISTRARSE** en la consola de {{site.data.keyword.Bluemix_notm}}.
  2. Complete los pasos siguiendo el asistente.

## No hay espacio asociado a la organización actual
{: #ts_no_space}

No puede crear una app si no hay ningún espacio asociado a la organización actual.

Cuando intenta crear una app en {{site.data.keyword.Bluemix_notm}}, ve el siguiente mensaje de error:
{: tsSymptoms}

`BXNUI0097E: Para poder añadir una app, al menos un espacio debe estar asociado con la organización y la región. En el Panel de control, pulse Crear un espacio. Cuando se cree el espacio, vuélvalo a intentar.`

Las apps de {{site.data.keyword.Bluemix_notm}} se deben crear en un espacio de la organización.
{: tsCauses}

Para crear un espacio, utilice uno de estos métodos:
{: tsResolve}

  * Desde la barra de menús, pulse **Gestionar > Cuenta > Organizaciones**. A continuación, seleccione la organización en la que desea crear el espacio y pulse **Crear un espacio**.
  * En la interfaz de línea de mandatos Cloud Foundry, escriba `cf create-space <space_name> -o <organization_name>`.


## Las apps comparten el mismo nombre de dominio
{: #ts_domain_diff}

Puede que observe que varias apps comparten el mismo URL en {{site.data.keyword.Bluemix_notm}}.

Este problema puede producirse cuando se asigna la misma ruta de URL a distintas apps de un espacio.
{: tsCauses}

Por ejemplo, supongamos que envía la app myApp1 a {{site.data.keyword.Bluemix_notm}} y establece el dominio en "mynewapp.stage1.mybluemix.net". Luego envía otra app myApp2 al mismo espacio y establece una de sus rutas de URL en "mynewapp.stage1.mybluemix.net". Ahora la ruta está correlacionada a ambas apps.

Este es el comportamiento soportado de {{site.data.keyword.Bluemix_notm}} y puede utilizar este procedimiento para conseguir un tiempo de inactividad cero para la actualización de la app. Para obtener más información, consulte [Utilización del despliegue azul-verde para reducir el tiempo de inactividad y el riesgo ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](https://docs.cloudfoundry.org/devguide/deploy-apps/blue-green.html){: new_window}.
{: tsResolve}


## Los administradores no pueden ver todas las organizaciones utilizando la interfaz de usuario de {{site.data.keyword.Bluemix_notm}}
{: #ts_ui_org}

Como administrador, al utilizar la interfaz de usuario de {{site.data.keyword.Bluemix_notm}}, no puede visualizar todas las organizaciones para administrarlas. Puede visualizar y administrar únicamente aquellas organizaciones a las que pertenezca.

Como administrador, no puede ver todas las organizaciones utilizando la interfaz de usuario de {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Se trata de una limitación de la interfaz de usuario de {{site.data.keyword.Bluemix_notm}}.
{: tsCauses}

Puede utilizar mandatos como `cf orgs`, `cf create-org` y `cf delete-org` desde la interfaz de línea de mandatos de Cloud Foundry para gestionar todas las organizaciones. Para ver una lista completa de mandatos de cf, especifique `cf help`.
{: tsResolve}

## La tarjeta de crédito no se puede agregar
{: #ts_addcc}

No puede enviar información de su tarjeta de crédito para convertir la cuenta Lite en una cuenta de pago.

El botón **Enviar** de la página Añadir tarjeta de crédito está inhabilitado.
{: tsSymptoms}

El problema se produce cuando no se ha rellenado la página Añadir tarjeta de crédito con información correcta.
{: tsCauses}


Siga estos pasos:
{: tsResolve}

  1. En la página Añadir tarjeta de crédito, rellene los campos necesarios de las secciones: información de contacto, dirección de contacto y dirección de facturación.
  2. Seleccione **He leído y acepto los términos y condiciones de IBM**, luego pulse **Enviar**. Se muestra la sección **Seleccionar un método de pago**.
  3. Escriba el número de tarjeta de crédito, la fecha de caducidad y el código de seguridad de su tarjeta. Luego pulse **Enviar**.
