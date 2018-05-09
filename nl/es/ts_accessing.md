---

copyright:

  years: 2015, 2018

lastupdated: "2017-11-10"

---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}


# Resolución de problemas de acceso a {{site.data.keyword.Bluemix_notm}}
{: #accessing}

Algunos de los problemas generales de acceso a {{site.data.keyword.Bluemix}} incluyen dificultades al iniciar una sesión en {{site.data.keyword.Bluemix_notm}} o que una cuenta se haya bloqueado en estado pendiente. En muchos de los casos, puede solucionar estos problemas siguiendo unos sencillos pasos.
{:shortdesc}

## Contraseña incorrecta
{: #ts_logintobm}

Debe tener una contraseña válida que esté asociada a su IBMid para poder iniciar sesión en la consola de {{site.data.keyword.Bluemix_notm}}.

Debe tener una contraseña válida que esté asociada con su IBMid o ID de cuenta enlazada para iniciar sesión a través del [portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com){: new_window}.

Cuando intenta iniciar una sesión en {{site.data.keyword.Bluemix_notm}}, aparece el siguiente mensaje de error:
{: tsSymptoms}

`La contraseña introducida no es correcta.`

La contraseña que ha utilizado para iniciar sesión en {{site.data.keyword.Bluemix_notm}} no son válidos.
{: tsCauses}

Utilice una de las soluciones siguientes:
{: tsResolve}
 * Escriba la contraseña correcta. Para comprobar si su IBMid y contraseña son válidos, puede ir a la página Mi perfil de IBM, pulsar **Iniciar sesión** y especificar el IBMid y la contraseña en la página Iniciar sesión.
 * Si ha olvidado su contraseña, pulse **¿Ha olvidado su contraseña?** para restablecer la contraseña. A continuación, vuelva a la [consola de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.{DomainName}){: new_window} o al [portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com){: new_window} e inicie sesión de nuevo.
 * Si ha olvidado el IBMid o sigue teniendo problemas con su contraseña, póngase en contacto con el centro de atención al cliente de registro de IBM a nivel mundial para obtener ayuda.
 * Para obtener un IBMid y una contraseña válidos, vaya a la página Mi perfil de IBM y pulse **Registro**.

Notas:
<!-- begin STAGING ONLY -->
 * Para los empleados de IBM, el IBMid puede ser distinto a su ID de intranet.
 <!-- end STAGING ONLY -->
 * Si está en la página de inicio de sesión en IBM y el proceso de inicio de sesión se interrumpe por cualquier motivo (por ejemplo, al restablecer su contraseña), vuelva a la [consola de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.{DomainName}){: new_window} o al [portal de cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com){: new_window} e inicie el proceso de inicio de sesión de nuevo.


## Credenciales de inicio de sesión no válidas
{: #ts_login_invalid_credentials}

Cuando inicia sesión con su IBMid, aparece el siguiente mensaje:
{: tsSymptoms}

`Se han proporcionado credenciales de inicio de sesión no válidas. Si tiene un IBMid asociado a su cuenta, inicie la sesión aquí`

* Ha cambiado a un IBMid, pero ha intentado iniciar sesión a través del [portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com){: new_window} utilizando su nombre de usuario y contraseña anteriores.
{: tsCauses}

* Ha intentado iniciar sesión a través del [portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com){: new_window}, pero ha especificado el ID y la contraseña de IBM en los campos Nombre de usuario y Contraseña.

Pulse **iniciar la sesión aquí** en el mensaje o vaya a la sección de inicio de sesión con cuenta de IBMid y pulse **Iniciar la sesión con IBMid**.
{: tsResolve}

No utilice los campos **Nombre de usuario** y **Contraseña** que ha utilizado con el ID anterior.


## IBMid o correo electrónico no reconocido
{: #ts_old_username}

Cuando inicia sesión en la consola de {{site.data.keyword.Bluemix_notm}} aparece el siguiente mensaje:
{: tsSymptoms}

`No hemos reconocido este IBMid o correo electrónico.`

Ha intentado iniciar la sesión en la consola {{site.data.keyword.Bluemix_notm}}, pero no ha utilizado un IBMid válido. Por ejemplo, no ha especificado una dirección de correo electrónico completa para el IBMid o ha intentado utilizar un nombre de usuario y contraseña anteriores.
{: tsCauses}

Debe tener un IBMid y contraseña válidos para poder iniciar una sesión en {{site.data.keyword.Bluemix_notm}}.

 * Asegúrese de especificar una dirección de correo electrónico completa para el IBMid.
 {: tsResolve}
 * Si es un usuario de {{site.data.keyword.BluSoftlayer_full}} con un ID de {{site.data.keyword.BluSoftlayer_full}}, debe cambiar a la autenticación del IBMid en el portal de cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} en cada cuenta a la que tenga acceso antes de poder iniciar una sesión utilizando la autenticación del IBMid.
 Para obtener más información, consulte [Cambio a un IBMid](/docs/account/softlayerlink.html#switching-to-ibmid).


## El IBMid no está asociada a ninguna cuenta de IBM Cloud
{: #ts_login_noswitch}

Cuando inicia sesión con su IBMid, aparece el siguiente mensaje:
{: tsSymptoms}

`Ha llegado a esta página porque la autenticación ha sido satisfactoria; sin embargo, este IBMid no está asociado con ninguna cuenta de IBM Cloud. Si cree que esto es un error, póngase en contacto con el Propietario de la cuenta o el Usuario maestro.`

Ha iniciado sesión en el [portal de cliente de la infraestructura de {{site.data.keyword.BluSoftlayer_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com){: new_window} con un IBMid válido, pero no ha cambiado a la autenticación del IBMid desde el portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}}.
{: tsCauses}

Siga los pasos siguientes según proceda:
{: tsResolve}
 * Póngase en contacto con el usuario maestro o con el administrador para comprobar que puede cambiar a la autenticación con IBMid.
 * Asegúrese de haber llevado a cabo el paso de cambio a IBMid. Consulte [Cambio a un IBMid](/docs/account/softlayerlink.html#switching-to-ibmid).
 * Asegúrese de seguir las acciones del correo electrónico **Asociar su ID de usuario con un IBMid**. Consulte la bandeja de entrada y la carpeta de correo basura para buscar el correo electrónico. Para recuperar el correo electrónico, por ejemplo si ha caducado, vaya a la página Editar perfil de usuario del portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} y pulse **Reenviar correo electrónico**. Como alternativa, póngase en contacto con el [equipo de soporte de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://ibm.biz/bluemixsupport.com){: new_window}.

**Nota:** si ha creado su IBMid directamente con IBMid, habrá recibido dos correos electrónicos; uno del registro de IBMid y otro de {{site.data.keyword.Blu_full}}. Asegúrese de seguir las indicaciones de ambos correos electrónicos.

En función de cómo se haya configurado su cuenta, se podrán aplicar algunas de estas opciones de inicio de sesión:
 * Los usuarios de {{site.data.keyword.BluSoftlayer_notm}} con los ID de {{site.data.keyword.BluSoftlayer_full}} deben iniciar sesión a través del [portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com){: new_window}.
 * Los usuarios de {{site.data.keyword.BluSoftlayer_notm}} con un IBMid y con o sin una cuenta de {{site.data.keyword.Bluemix_notm}} enlazada pueden iniciar sesión a través del [portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com){: new_window} para abrir el portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} o a través de la [consola de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.{DomainName}){: new_window} para abrir el panel de control de infraestructura.


## El IBMid no está asociada a ninguna cuenta de {{site.data.keyword.Bluemix_notm}}
{: #ts_unabletologin}

Cuando inicia sesión en {{site.data.keyword.Bluemix_notm}}, aparece el siguiente mensaje:
{: tsSymptoms}

`Ha llegado a esta página porque la autenticación ha sido satisfactoria; sin embargo, este IBMid no está asociado a ninguna cuenta de {{site.data.keyword.Bluemix_notm}}.`

Ha iniciado sesión en la [consola de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.{DomainName}){: new_window} con un IBMid válido, pero aún no tiene una cuenta de {{site.data.keyword.Bluemix_notm}} creada.
{: tsCauses}

Para crear una cuenta de {{site.data.keyword.Bluemix_notm}}, siga el proceso de registro.
{: tsResolve}

En función de cómo se haya configurado su cuenta, se podrán aplicar algunas de estas opciones de inicio de sesión:
 * Los usuarios de {{site.data.keyword.Bluemix_notm}} sin una cuenta enlazada deben iniciar sesión a través de la consola de {{site.data.keyword.Bluemix_notm}}.
 * Los usuarios de {{site.data.keyword.Bluemix_notm}} con una cuenta enlazada pueden iniciar sesión mediante la [consola de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.{DomainName}){: new_window} o el [portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com){: new_window}.


## La consola no se abre
{: #ts_login_stalls}

Cuando inicie sesión utilizando su IBMid, se mostrará un mensaje de inicio de sesión correcto, pero no vuelve a la [consola de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.{DomainName}){: new_window} ni al [portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com){: new_window}
{: tsSymptoms}

Utilice una de las soluciones siguientes:
{: tsResolve}
 * Cierre el navegador, borre la memoria caché y las cookies y luego intente de nuevo iniciar la sesión.
 * Asegúrese de iniciar la sesión desde la [consola de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.{DomainName}){: new_window} o el [portal del cliente de infraestructura de {{site.data.keyword.BluSoftlayer_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://control.softlayer.com){: new_window}, en lugar de directamente desde el servicio de autenticación del IBMid.


## El inicio de sesión con IBMid no se completa
{: #ts_login_ibmid}

Cuando inicia una sesión en {{site.data.keyword.Bluemix_notm}}, la autenticación con IBMid no se completa.
{: tsSymptoms}

Es posible que haya un problema con el servicio de autenticación de IBMid.
{: tsCauses}

Compruebe el estado del servicio en [IBMid ![icono de enlace externo](../icons/launch-glyph.svg "icono de enlace externo")](https://new.wind.ibmcloud.com/webapp/#/status/a1a0c5d743d94a6a9597087541564d8e){: new_window} y vuélvalo a intentar.
{: tsResolve}


## La cuenta está pendiente
{: #ts_accntpding}

Si la cuenta está pendiente, no puede iniciar una sesión en {{site.data.keyword.Bluemix_notm}}.

Después de registrarse para una cuenta de prueba de {{site.data.keyword.Bluemix_notm}}, es posible que no pueda iniciar una sesión en {{site.data.keyword.Bluemix_notm}}. Se visualiza el mensaje siguiente:
{: tsSymptoms}

<code>Su cuenta está pendiente. Debe esperar hasta 24 horas a recibir una confirmación por correo electrónico y debe comprobar la carpeta spam. Si transcurrido este tiempo no ha recibido la confirmación por correo electrónico, póngase en contacto con el <a href="http://ibm.biz/bluemixsupport.com" target="_blank">Soporte de {{site.data.keyword.Bluemix_notm}}</a>.</code>

Después de registrarse para una cuenta de prueba de {{site.data.keyword.Bluemix_notm}}, recibirá un correo electrónico de confirmación. Debe pulsar el enlace del correo electrónico de confirmación para completar el proceso de registro.
{: tsCauses}

El correo electrónico de confirmación se envía a la dirección de correo electrónico que ha especificado. Consulte la bandeja de entrada de la carpeta spam. Si no ha recibido el correo electrónico de confirmación, póngase en contacto con el [Soporte de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://ibm.biz/{{site.data.keyword.Bluemix_notm}}support.com){: new_window}.  
{: tsResolve}


<!-- begin STAGING ONLY -->

## Problema al acceder a un sitio web externo
{: #ts_bmlinkid}

Para iniciar una sesión en {{site.data.keyword.Bluemix_notm}} utilizando su ID de intranet de IBM, debe enlazar su ID de intranet con su IBMid.

Después de seleccionar **Iniciar sesión con su ID de intranet** desde la página Inicio de sesión de {{site.data.keyword.Bluemix_notm}}, podría aparecer el siguiente mensaje:
{: tsSymptoms}

`Problema accediendo al sitio web externo`

Este problema se produce cuando se inicia sesión en {{site.data.keyword.Bluemix_notm}} utilizando un ID de intranet de IBM que no está enlazado a un IBMid. Su IBMid es el identificador que se utiliza para iniciar una sesión en www.ibm.com.
{: tsCauses}

Como empleado de IBM, antes de poder iniciar sesión en {{site.data.keyword.Bluemix_notm}} utilizando su ID de intranet de IBM, debe enlazar su ID de intranet con su IBMid externo. Siga estos pasos para enlazar los dos identificadores:
{: tsResolve}

  1. En la página [Central Sign-on ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://w3-03.sso.ibm.com/tools/cso/index.jsp){: new_window}, pulse **Mis inicios de sesión**.
  2. En la página de Mis inicios de sesión, pulse **Enlazar ID**, y especifique su IBMid y contraseña en la página de inicio de sesión en {{site.data.keyword.Bluemix_notm}}. Después de esto, su ID de intranet y su IBMid estarán enlazados de forma automática.


<!-- end STAGING ONLY -->

## La página {{site.data.keyword.Bluemix_notm}} no se puede cargar
{: #ts_err}

Cuando utilice la consola de {{site.data.keyword.Bluemix_notm}}, es posible que no pueda cargar una página de consola. En su lugar verá los mensajes de error BXNUI0001E o BXNUI0016E.

Es posible que vea uno de los siguientes mensajes de error cuando utilice la consola de {{site.data.keyword.Bluemix_notm}}:
{: tsSymptoms}

`BXNUI0001E: La página no se ha cargado porque {{site.data.keyword.Bluemix_notm}} no ha detectado si existe una sesión.`

`BXNUI0016E: Las apps y servicios no se han recuperado porque no se ha cargado una página de {{site.data.keyword.Bluemix_notm}}.`

Lleve a cabo una o varias de estas acciones si es necesario:
{: tsResolve}

  * Renueve o reinicie el navegador.
  * Finalice la sesión de {{site.data.keyword.Bluemix_notm}} y vuélvala a iniciar.
  * Utilice la modalidad de navegación privada del navegador.
  * Borre las cookies y la memoria caché del navegador.
  * Utilice otro navegador. Para obtener información sobre las versiones de los navegadores a las que da soporte {{site.data.keyword.Bluemix_notm}}, consulte [Requisitos previos de {{site.data.keyword.Bluemix_notm}}](/docs/overview/whatisbluemix.html#prereqs).
  * Si ha instalado la interfaz de línea de mandatos cf, escriba el mandato `cf apps` para ver si la app se está ejecutando.
