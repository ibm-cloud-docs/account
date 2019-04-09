---

copyright:
  years: 2015, 2018
lastupdated: "2018-11-28"

keywords: troubleshoot account, account problem, account support, account help, account error, access error, login error, error message

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


# Resolución de problemas de acceso a {{site.data.keyword.Bluemix_notm}}
{: #accessing}

Algunos de los problemas generales de acceso a {{site.data.keyword.Bluemix}} incluyen dificultades al iniciar una sesión en {{site.data.keyword.Bluemix_notm}} o que una cuenta se haya bloqueado en estado pendiente. En muchos de los casos, puede solucionar estos problemas siguiendo unos sencillos pasos.
{:shortdesc}


## ¿Por qué no es correcta mi contraseña?
{: #ts_logintobm}
{: troubleshoot}

Debe tener una contraseña válida que esté asociada a su IBMid o ID de SoftLayer para poder iniciar sesión en la consola de {{site.data.keyword.Bluemix_notm}}.

Cuando intenta iniciar una sesión en {{site.data.keyword.Bluemix_notm}}, aparece el siguiente mensaje de error:
{: tsSymptoms}

`La contraseña introducida no es correcta.`

La contraseña que ha utilizado para iniciar sesión en {{site.data.keyword.Bluemix_notm}} no son válidos.
{: tsCauses}

Utilice una de las opciones siguientes:
{: tsResolve}
 * Vaya a la página [Mi perfil de IBM ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://myibm.ibm.com/dashboard/){: new_window} para confirmar que utiliza una contraseña válida.
 * Si ha olvidado su contraseña, pulse **¿Ha olvidado su contraseña?** para restablecer la contraseña.
 * Si ha olvidado el IBMid o sigue teniendo problemas con su contraseña, póngase en contacto con el centro de atención al cliente de registro de IBM a nivel mundial para obtener ayuda.

Si inicia sesión en {{site.data.keyword.Bluemix_notm}} y el proceso se interrumpe por cualquier motivo como, por ejemplo, al restablecer la contraseña, vuelva a la consola e inicie el proceso de inicio de sesión de nuevo.
{: tip}


## ¿Por qué no se han reconocido mi IBMid o mi correo electrónico?
{: #ts_old_username}
{: troubleshoot}

Para iniciar sesión correctamente en el correo electrónico, deberá asegurarse de que tiene la autenticación de IBMid para cada cuenta.

Cuando inicia sesión en la consola de {{site.data.keyword.Bluemix_notm}} aparece el siguiente mensaje:
{: tsSymptoms}

`No hemos reconocido este IBMid o correo electrónico.`

Ha intentado iniciar sesión en la consola pero no ha utilizado un IBMid válido. Por ejemplo, no ha especificado una dirección de correo electrónico completa para el IBMid o ha intentado utilizar un nombre de usuario y contraseña anteriores.
{: tsCauses}

Debe tener un IBMid y contraseña válidos para poder iniciar una sesión en {{site.data.keyword.Bluemix_notm}}.

 * Especifique una dirección de correo electrónico completa para el IBMid.
 {: tsResolve}
 * Si es un usuario de SoftLayer con un ID de SoftLayer, debe cambiar a la autenticación del IBMid en cada cuenta a la que tenga acceso antes de poder iniciar una sesión. Para obtener más información, consulte [Cambio a un IBMid](/docs/account?topic=account-unifyingaccounts).


## ¿Por qué mi IBMid no está asociado con ninguna cuenta de {{site.data.keyword.Bluemix_notm}}?
{: #ts_unabletologin}
{: troubleshoot}

Cuando inicia sesión en {{site.data.keyword.Bluemix_notm}}, aparece el siguiente mensaje:
{: tsSymptoms}

`Ha llegado a esta página porque la autenticación ha sido satisfactoria; sin embargo, este IBMid no está asociado a ninguna cuenta de {{site.data.keyword.Bluemix_notm}}.`

Ha iniciado sesión en la [consola de {{site.data.keyword.Bluemix_notm}} console](https://{DomainName}){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo") co un IBMid válido, pero aún no ha creado una cuenta de {{site.data.keyword.Bluemix_notm}}.
{: tsCauses}

Para crear una cuenta de {{site.data.keyword.Bluemix_notm}}, siga el proceso de registro.
{: tsResolve}


## ¿Por qué no se abre la consola cuando inicio sesión con mi IBMid?
{: #ts_login_stalls}
{: troubleshoot}

Cuando obtiene un mensaje de inicio de sesión correcto, pero no vuelve a la consola.

Cuando inicia sesión utilizando su IBMid, se muestra un mensaje de inicio de sesión correcto, pero no vuelve a la [consola de {{site.data.keyword.Bluemix_notm}}](https://{DomainName}){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo").
{: tsSymptoms}

Utilice una de las opciones siguientes:
{: tsResolve}
 * Cierre el navegador, borre la memoria caché y las cookies y luego intente de nuevo iniciar la sesión.
 * Inicie sesión desde la [consola de {{site.data.keyword.Bluemix_notm}}](https://{DomainName}){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo").


## ¿Por qué no se ha completado mi inicio de sesión de IBMid?
{: #ts_login_ibmid}
{: troubleshoot}

Si inicia sesión en {{site.data.keyword.Bluemix_notm}} y la autenticación del IBMid no se completa, es posible que haya un problema con el servicio.

Cuando inicia una sesión en {{site.data.keyword.Bluemix_notm}}, la autenticación con IBMid no se completa.
{: tsSymptoms}

Es posible que haya un problema con el servicio de autenticación de IBMid.
{: tsCauses}

Asegúrese de que puede iniciar sesión en [IBM](https://idaas.iam.ibm.com/idaas/mtfim/sps/authsvc?PolicyId=urn:ibm:security:authentication:asf:basicldapuser){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo"). Si puede hacerlo, entonces se trata de un problema en la aplicación y puede intentar iniciar sesión de nuevo en la consola más adelante. Si no puede iniciar una sesión en esa página, póngase en contacto con el [centro de atención al cliente de IBMid ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/ibmid/myibm/help/us/helpdesk.html){: new_window}.  
{: tsResolve}


## ¿Por qué no puedo iniciar sesión inmediatamente después de registrar una cuenta?
{: #ts_accntpding}
{: troubleshoot}

Si la cuenta está pendiente, no puede iniciar una sesión en {{site.data.keyword.Bluemix_notm}}.

Después de registrarse para una cuenta de Lite de {{site.data.keyword.Bluemix_notm}}, es posible que no pueda iniciar sesión en {{site.data.keyword.Bluemix_notm}}. Se visualiza el mensaje siguiente:
{: tsSymptoms}

<code>Su cuenta está pendiente. Debe esperar hasta 24 horas a recibir una confirmación por correo electrónico y debe comprobar la carpeta spam. Si transcurrido este tiempo no ha recibido la confirmación por correo electrónico, póngase en contacto con el <a href="https://ibm.biz/ibmcloudsupport" target="_blank">Soporte de {{site.data.keyword.Bluemix_notm}}</a>.</code>

Cuando registra una cuenta Lite de {{site.data.keyword.Bluemix_notm}}, recibe un correo electrónico que incluye un enlace en el que debe pulsar para confirmar el registro.  
{: tsCauses}

El correo electrónico de confirmación se envía a la dirección de correo electrónico asociada con el IBMid. Consulte la bandeja de entrada de la carpeta spam. Si no ha recibido el correo electrónico de confirmación, póngase en contacto con el [Soporte de {{site.data.keyword.Bluemix_notm}}](/docs/get-support?topic=get-support-getting-customer-support).  
{: tsResolve}


## ¿Por qué hay páginas de la consola que no se cargan?
{: #ts_err}
{: troubleshoot}

Cuando utilice la consola de {{site.data.keyword.Bluemix_notm}}, es posible que no pueda cargar una página de consola. En su lugar verá los mensajes de error BXNUI0001E o BXNUI0016E.

Es posible que vea uno de los mensajes de error siguientes:
{: tsSymptoms}

`BXNUI0001E: La página no se ha cargado porque {{site.data.keyword.Bluemix_notm}} no ha detectado si existe una sesión.`

`BXNUI0016E: Las apps y servicios no se han recuperado porque no se ha cargado una página de {{site.data.keyword.Bluemix_notm}}.`

Lleve a cabo una o varias de estas acciones si es necesario:
{: tsResolve}

  * Renueve o reinicie el navegador.
  * Finalice la sesión de {{site.data.keyword.Bluemix_notm}} y vuélvala a iniciar.
  * Utilice la modalidad de navegación privada del navegador.
  * Borre las cookies y la memoria caché del navegador.
  * Utilice otro navegador. Para obtener información sobre las versiones de los navegadores a las que da soporte {{site.data.keyword.Bluemix_notm}}, consulte [Requisitos previos de {{site.data.keyword.Bluemix_notm}}](/docs/overview?topic=overview-prereqs-platform).
  * Si ha instalado la interfaz de línea de mandatos Cloud Foundry, escriba el mandato `ibmcloud cf apps` para ver si la app se está ejecutando.
