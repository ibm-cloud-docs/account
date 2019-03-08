---

copyright:
  years: 2015, 2019
lastupdated: "2019-02-13"

keywords: troubleshoot account, account problem, account support, account help, org error, resource error, error message

subcollection: account
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Resolución de problemas de gestión de cuentas
{: #managingaccounts}

Los problemas generales con la gestión de la cuenta pueden incluir que distintas
apps tienen el mismo nombre de dominio o que los administradores no puedan ver
todas las organizaciones. En muchos de los casos, puede solucionar estos problemas siguiendo unos sencillos pasos.
{:shortdesc}


## ¿Por qué no puedo acceder a una ubicación de {{site.data.keyword.Bluemix_notm}} distinta?
{: #nosecondreg}
{: troubleshoot}

No puede crear una nueva ubicación porque el tipo de cuenta que tiene no lo permite.

Puede recibir un mensaje de error al intentar crear una nueva ubicación de {{site.data.keyword.Bluemix_notm}}.
{: tsSymptoms}

Es probable que esto ocurra por estar utilizando una cuenta Lite, que únicamente soporta el desarrollo en una ubicación pública.
{: tsCauses}

Para acceder a más ubicaciones, actualice a una cuenta facturable. Vaya a **Gestionar > Facturación y uso** y seleccione **Pagos**.
{: tsResolve}


## ¿Por qué no puedo crear una nueva organización?
{: #nosecondorg}
{: troubleshoot}

Está intentando crear más de una organización y tiene una cuenta Lite.  

Puede recibir un mensaje de error al intentar crear una nueva organización.
{: tsSymptoms}

Es probable que esto ocurra por estar utilizando una cuenta Lite, que únicamente soporta el desarrollo en una organización.
{: tsCauses}

Para crear una nueva organización, actualice a una cuenta facturable. Vaya a **Gestionar > Facturación y uso** y seleccione **Actualizaciones**.
{: tsResolve}


## ¿Por qué no puedo crear una nueva instancia del plan Lite?
{: #nosecondlite}
{: troubleshoot}

Está intentando crear una instancia adicional y tiene una cuenta Lite.

Puede recibir el siguiente mensaje de error al intentar crear una nueva instancia de plan Lite:
{: tsSymptoms}

`No es posible suministrar una nueva instancia de Lite`

Hay un límite de una instancia por instancia del plan lite para garantizar que estos planes continúan siendo gratuitos.
{: tsCauses}

Se pueden crear más instancias del servicio seleccionando uno de los planes de servicios facturables, que también están disponibles en las cuentas facturables. Para actualizar a una cuenta facturable desde la consola, vaya a **Gestionar > Facturación y uso** y seleccione **Actualizaciones**.
{: tsResolve}

Si no desea actualizar la cuenta Lite y ya no está utilizando la instancia de servicio Lite existente, puede suprimir dicha instancia de plan Lite desde el panel de control y, a continuación, crear una nueva instancia.


## ¿Cómo he superado la concesión de memoria de tiempo de ejecución?
{: #noruntimemem}
{: troubleshoot}

Ha superado la memoria permitida para su cuenta.

No puede desplegar apps y aparece un error que indica que ha superado el límite de memoria de su organización.
{: tsSymptoms}

En una cuenta Lite, sus apps de Cloud Foundry pueden utilizar hasta 256 MB de memoria de tiempo de ejecución instantánea. En las cuentas facturables, hay un límite de 2 GB de memoria.
{: tsCauses}

Si está utilizando una cuenta Lite, puede obtener más memoria actualizando a una cuenta facturable. Vaya a **Gestionar > Facturación y uso** y seleccione **Actualizaciones**.
{: tsResolve}

Si no desea actualizar la cuenta Lite y tiene apps desocupadas, puede suprimirlas para liberar memoria de tiempo de ejecución.


## ¿Por qué está inactiva mi cuenta?
{: #ts_accnt_inactive}
{: troubleshoot}

No puede crear una app en {{site.data.keyword.Bluemix_notm}} si la cuenta está inactiva. Debe ponerse en contacto con el equipo de soporte para solucionar este problema.

Cuando intenta crear una app en {{site.data.keyword.Bluemix_notm}}, aparece el siguiente mensaje de error:
{: tsSymptoms}

`BXNUI0096E: La app no se ha creado. La cuenta está inactiva porque se ha cancelado o suspendido.`

El estado de la cuenta de {{site.data.keyword.Bluemix_notm}} pasa a ser inactivo si la cuenta se cancela o se suspende.
{: tsCauses}

Para volver a activar la cuenta, abra un caso en el [centro de soporte](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo"). Incluya la información siguiente:
{: tsResolve}

  * El IBMid que utiliza para iniciar la sesión en {{site.data.keyword.Bluemix_notm}}.
  * El nombre de la organización en la que se está creando la app. Esta información puede ayudar al equipo de soporte a determinar si se le han asignado los roles o pertenencia a grupos correctos en la organización.


## ¿Por qué no puedo añadir usuarios a una organización?
{: #ts_adduser}
{: troubleshoot}

Puede invitar a usuarios a la organización solo si es el propietario de la cuenta o si es gestor y miembro de la organización.

No ve el enlace **Invitar a un nuevo usuario** en la sección **Gestionar organizaciones**.
{: tsSymptoms}

Únicamente los siguientes usuarios de {{site.data.keyword.Bluemix_notm}}
pueden invitar a usuarios a una organización:
{: tsCauses}
  * El propietario de la cuenta de la organización
  * Los gestores de la organización que también son miembros, y no colaboradores, de la misma

En {{site.data.keyword.Bluemix_notm}}, puede ser o bien un miembro o bien un colaborador de una organización:

<dl><dt>Colaborador</dt>
<dd>Puede ser colaborador de una organización si ya dispone de una cuenta de {{site.data.keyword.Bluemix_notm}} y alguien le invita a la organización.</dd>
<dt>Miembro</dt>
<dd>Puede ser miembro de una organización si no dispone de una cuenta de {{site.data.keyword.Bluemix_notm}}, pero alguien le invita a la organización y se registra en {{site.data.keyword.Bluemix_notm}} a partir de la invitación.</dd>
</dl>

No puede invitar a usuarios a su organización si es colaborador, incluso si se le ha asignado como gestor de la organización.

Todos los gestores de la organización, incluidos los que son colaboradores, pueden añadir, modificar y eliminar los usuarios que ya están en la organización.
{: note}

Si no puede invitar a usuarios a su organización y necesita otro rol para hacerlo, póngase en contacto con el gestor de la organización
para cambiar el rol. Para identificar el gestor de la organización, siga estos pasos:
{: tsResolve}

  1. En la barra de menús, pulse **Gestionar > Cuenta** y pulse **Contactos de la empresa**.
  2. Vaya a la organización y consulte la información sobre el gestor de la organización en el separador **USUARIOS**.  

Si no puede invitar a usuarios porque es colaborador y no un miembro, debe suprimir la cuenta anterior de {{site.data.keyword.Bluemix_notm}} y luego se le debe invitar como un miembro de la organización. Para suprimir la cuenta anterior y unirse a la cuenta como miembro, siga estos pasos:

  1. Póngase en contacto con el [equipo de soporte de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/unifiedsupport/supportcenter){: new_window} para abrir una incidencia de soporte y solicitar que se suprima la cuenta. Si tiene datos asociados con su antigua cuenta que desea guardar y moverlos the una nueva cuenta, incluya es información en el correo.
  2. Una vez haya suprimido la cuenta, pida a un usuario con el rol de gestor de la organización que le invite a la misma como gestor de la organización. Luego, inicie sesión en {{site.data.keyword.Bluemix_notm}} desde la invitación.


## ¿Por qué no hay espacios asociados con mi organización actual?
{: #ts_no_space}
{: troubleshoot}

No puede crear una app si no hay ningún espacio asociado a la organización actual.

Cuando intenta crear una app, aparece el mensaje de error siguiente:
{: tsSymptoms}

`BXNUI0097E: Para poder añadir una app, al menos un espacio debe estar asociado con la organización y la región. En el Panel de control, pulse Crear un espacio. Cuando se cree el espacio, vuélvalo a intentar.`

Las apps se deben crear en un espacio de la organización.
{: tsCauses}

Para crear un espacio, utilice uno de estos métodos:
{: tsResolve}

  * En la barra de menús, pulse **Gestionar > Cuenta** y pulse **Organizaciones**. A continuación, seleccione la organización en la que desea crear el espacio y pulse **Crear un espacio**.
  * En la interfaz de línea de mandatos {{site.data.keyword.Bluemix_notm}}, escriba `ibmcloud account space-create <space_name> -o <organization_name>`.


## ¿Por qué algunas apps comparten un nombre de dominio?
{: #ts_domain_diff}
{: troubleshoot}

Puede que observe que varias apps comparten un URL en {{site.data.keyword.Bluemix_notm}}.

Este problema puede producirse cuando se asigna la misma ruta de URL a distintas apps de un espacio.
{: tsCauses}

Por ejemplo, supongamos que envía la app myApp1 a {{site.data.keyword.Bluemix_notm}} y establece el dominio en `mynewapp.us-east.cf.appdomain.cloud`. Luego envía otra app myApp2 al mismo espacio y establece una de sus rutas de URL en `mynewapp.us-east.cf.appdomain.cloud`. Ahora la ruta está correlacionada a ambas apps.

Este es el comportamiento soportado y puede utilizar este procedimiento para conseguir un tiempo de inactividad cero para la actualización de la app. Para obtener más información, consulte [Cómo garantizar un tiempo de inactividad zero](/docs/overview?topic=overview-zero-downtime).
{: tsResolve}


## ¿Por qué los administradores no pueden utilizar la consola para ver todas las organizaciones?
{: #ts_ui_org}
{: troubleshoot}

Como administrador, no puede visualizar todas las organizaciones para administrarlas cuando utiliza la consola de {{site.data.keyword.Bluemix_notm}}. Puede visualizar y administrar únicamente aquellas organizaciones a las que pertenezca.

Como administrador, no puede ver todas las organizaciones desde la consola.
{: tsSymptoms}

Se trata de una limitación de la consola.
{: tsCauses}

Puede utilizar mandatos como `ibmcloud account orgs` e `ibmcloud account org-create` desde la interfaz de línea de mandatos de {{site.data.keyword.Bluemix_notm}} para gestionar todas las organizaciones. Para ver una lista completa de mandatos, especifique `ibmcloud account help`.
{: tsResolve}


## ¿Por qué no puedo añadir la información de mi tarjeta de crédito?
{: #ts_addcc}
{: troubleshoot}

No puede enviar información de su tarjeta de crédito para actualizar la cuenta Lite en una cuenta de pago.

El botón **Enviar** de la página Añadir tarjeta de crédito está inhabilitado.
{: tsSymptoms}

Este problema sucede cuando no se ha especificado la información correcta en la página Añadir tarjeta de crédito.
{: tsCauses}

Siga estos pasos:
{: tsResolve}

  1. En la página Añadir tarjeta de crédito, complete todos los campos necesarios.
  2. Seleccione **He leído y acepto los términos y condiciones de IBM**, luego pulse **Enviar**.
