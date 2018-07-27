---

copyright:

  years: 2015, 2018

lastupdated: "2018-07-09"

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

También debe tener una contraseña válida que esté asociada con su IBMid o ID de cuenta enlazada para iniciar sesión a través del [portal de clientes](https://control.softlayer.com).

Cuando intenta iniciar una sesión en {{site.data.keyword.Bluemix_notm}}, aparece el siguiente mensaje de error:
{: tsSymptoms}

`La contraseña introducida no es correcta.`

La contraseña que ha utilizado para iniciar sesión en {{site.data.keyword.Bluemix_notm}} no son válidos.
{: tsCauses}

Utilice una de las soluciones siguientes:
{: tsResolve}
 * Escriba la contraseña correcta. Para comprobar si su IBMid y contraseña son válidos, puede ir a la página Mi perfil de IBM, pulsar **Iniciar sesión** y especificar el IBMid y la contraseña en la página Iniciar sesión.
 * Si ha olvidado su contraseña, pulse **¿Ha olvidado su contraseña?** para restablecer la contraseña. A continuación, vuelva a la [consola de {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) o al [portal de clientes](https://control.softlayer.com) e inicie sesión de nuevo.
 * Si ha olvidado el IBMid o sigue teniendo problemas con su contraseña, póngase en contacto con el centro de atención al cliente de registro de IBM a nivel mundial para obtener ayuda.
 * Para obtener un IBMid y una contraseña válidos, vaya a la página Mi perfil de IBM y pulse **Registro**.

**Nota:** Si está en la página de inicio de sesión en IBM y el proceso de inicio de sesión se interrumpe por cualquier motivo (por ejemplo, al restablecer su contraseña), vuelva a la [consola de {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) o al [portal de clientes](https://control.softlayer.com) e inicie el proceso de inicio de sesión de nuevo.


## Credenciales de inicio de sesión no válidas
{: #ts_login_invalid_credentials}

Cuando inicia sesión con su IBMid, aparece el siguiente mensaje:
{: tsSymptoms}

`Se han proporcionado credenciales de inicio de sesión no válidas. Si tiene un IBMid asociado a su cuenta, inicie la sesión aquí`

* Ha cambiado a un IBMid, pero ha intentado iniciar sesión a través del [portal de clientes](https://control.softlayer.com) utilizando su nombre de usuario y contraseña anteriores.
{: tsCauses}

* Ha intentado iniciar la sesión a través del [portal de clientes](https://control.softlayer.com), pero ha especificado su IBMid y su contraseña en los campos Nombre de usuario y Contraseña.

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
 * Si es un usuario de SoftLayer con un ID de SoftLayer, debe cambiar a la autenticación del IBMid en el portal de clientes en cada cuenta a la que tenga acceso antes de poder iniciar una sesión utilizando la autenticación del IBMid.
 Para obtener más información, consulte [Cambio a un IBMid](/docs/account/softlayerlink.html).


## El IBMid no está asociada a ninguna cuenta de IBM Cloud
{: #ts_login_noswitch}

Cuando inicia sesión con su IBMid, aparece el siguiente mensaje:
{: tsSymptoms}

`Ha llegado a esta página porque la autenticación ha sido satisfactoria; sin embargo, este IBMid no está asociado con ninguna cuenta de IBM Cloud. Si cree que esto es un error, póngase en contacto con el Propietario de la cuenta o el Usuario maestro.`

Ha iniciado una sesión desde el [portal de clientes](https://control.softlayer.com) con un IBMid válido, pero no ha cambiado a la autenticación de IBMid desde el portal de cliente.
{: tsCauses}

Siga los pasos siguientes según proceda:
{: tsResolve}
 * Póngase en contacto con el usuario maestro o con el administrador para comprobar que puede cambiar a la autenticación con IBMid.
 * Asegúrese de haber llevado a cabo el paso de cambio a IBMid. Consulte [Cambio a un IBMid](/docs/account/softlayerlink.html).
 * Asegúrese de seguir las acciones del correo electrónico **Asociar su ID de usuario con un IBMid**. Consulte la bandeja de entrada y la carpeta de correo basura para buscar el correo electrónico. Para recuperar el correo electrónico, por ejemplo si ha caducado, vaya a la página Editar perfil de usuario del portal de clientes y pulse **Reenviar correo electrónico**. Como alternativa, póngase en contacto con el [equipo de soporte de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://ibm.biz/bluemixsupport.com){: new_window}.

En función de cómo se haya configurado su cuenta, se podrán aplicar algunas de estas opciones de inicio de sesión:
 * Los usuarios de SoftLayer con ID de SoftLayer deben iniciar sesión a través del [portal de clientes](https://control.softlayer.com).
 * Los usuarios de SoftLayer con un IBMid y con o sin una cuenta de {{site.data.keyword.Bluemix_notm}} enlazada pueden iniciar sesión a través del [portal de clientes](https://control.softlayer.com) para abrir el portal de clientes o a través de la [consola de {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) para abrir el panel de control de Infraestructura.


## El IBMid no está asociada a ninguna cuenta de {{site.data.keyword.Bluemix_notm}}
{: #ts_unabletologin}

Cuando inicia sesión en {{site.data.keyword.Bluemix_notm}}, aparece el siguiente mensaje:
{: tsSymptoms}

`Ha llegado a esta página porque la autenticación ha sido satisfactoria; sin embargo, este IBMid no está asociado a ninguna cuenta de {{site.data.keyword.Bluemix_notm}}.`

Ha iniciado sesión en la [consola de {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) con un IBMid válido pero aún no ha creado una cuenta de {{site.data.keyword.Bluemix_notm}}.
{: tsCauses}

Para crear una cuenta de {{site.data.keyword.Bluemix_notm}}, siga el proceso de registro.
{: tsResolve}

En función de cómo se haya configurado su cuenta, se podrán aplicar algunas de estas opciones de inicio de sesión:
 * Los usuarios de {{site.data.keyword.Bluemix_notm}} sin una cuenta enlazada deben iniciar sesión a través de la consola de {{site.data.keyword.Bluemix_notm}}.
 * Los usuarios de {{site.data.keyword.Bluemix_notm}} con una cuenta enlazada pueden iniciar la sesión a través de la [consola de {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) o el [portal de clientes](https://control.softlayer.com).


## La consola no se abre
{: #ts_login_stalls}

Cuando inicia una sesión utilizando su IBMid, se muestra un mensaje de inicio de sesión correcto, pero no vuelve a la [consola de {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) ni al [portal de clientes](https://control.softlayer.com)
{: tsSymptoms}

Utilice una de las soluciones siguientes:
{: tsResolve}
 * Cierre el navegador, borre la memoria caché y las cookies y luego intente de nuevo iniciar la sesión.
 * Asegúrese de iniciar la sesión desde la [consola de {{site.data.keyword.Bluemix_notm}}](https://console.{DomainName}) o el [portal de clientes](https://control.softlayer.com), en lugar de hacerlo directamente desde el servicio de autenticación de IBMid.


## El inicio de sesión con IBMid no se completa
{: #ts_login_ibmid}

Cuando inicia una sesión en {{site.data.keyword.Bluemix_notm}}, la autenticación con IBMid no se completa.
{: tsSymptoms}

Es posible que haya un problema con el servicio de autenticación de IBMid.
{: tsCauses}

Compruebe si puede iniciar sesión en la [página de inicio de IBM ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/us-en/){: new_window}. Si puede, entonces es un problema de aplicación y puede intentarlo más tarde. Si no puede iniciar sesión en esa página, póngase en contacto con el [centro de atención al cliente ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}.
{: tsResolve}


## La cuenta está pendiente
{: #ts_accntpding}

Si la cuenta está pendiente, no puede iniciar una sesión en {{site.data.keyword.Bluemix_notm}}.

Después de registrarse para una cuenta de Lite de {{site.data.keyword.Bluemix_notm}}, es posible que no pueda iniciar sesión en {{site.data.keyword.Bluemix_notm}}. Se visualiza el mensaje siguiente:
{: tsSymptoms}

<code>Su cuenta está pendiente. Debe esperar hasta 24 horas a recibir una confirmación por correo electrónico y debe comprobar la carpeta spam. Si transcurrido este tiempo no ha recibido la confirmación por correo electrónico, póngase en contacto con el <a href="http://ibm.biz/bluemixsupport.com" target="_blank">Soporte de {{site.data.keyword.Bluemix_notm}}</a>.</code>

Después de registrarse para una cuenta de Lite de {{site.data.keyword.Bluemix_notm}}, recibirá un correo electrónico de confirmación. Debe pulsar el enlace del correo electrónico de confirmación para completar el proceso de registro.
{: tsCauses}

El correo electrónico de confirmación se envía a la dirección de correo electrónico que ha especificado. Consulte la bandeja de entrada de la carpeta spam. Si no ha recibido el correo electrónico de confirmación, póngase en contacto con el [Soporte de {{site.data.keyword.Bluemix_notm}}![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](http://ibm.biz/bluemixsupport.com){: new_window}.  
{: tsResolve}

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
  * Utilice otro navegador. Para obtener información sobre las versiones de los navegadores a las que da soporte {{site.data.keyword.Bluemix_notm}}, consulte [Requisitos previos de {{site.data.keyword.Bluemix_notm}}](/docs/overview/prereqs.html#prereqs).
  * Si ha instalado la interfaz de línea de mandatos Cloud Foundry, escriba el mandato `cf apps` para ver si la app se está ejecutando.
