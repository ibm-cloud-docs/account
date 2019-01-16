---


copyright:

  years: 2018
lastupdated: "2018-11-29"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:tip: .tip}
{:note: .note}


# Configuración de la seguridad de inicio de sesión
{: #login-settings}

Con el acceso autorizado puede configurar una seguridad adicional para el inicio de sesión. Puede seleccionar una caducidad de contraseña y configurar preguntas y respuesta de seguridad, la autenticación de multifactores (MFA) de código de acceso de un solo uso basada en tiempo (TOTP) y las opciones de autenticación externas.  
{:shortdesc}

Un propietario de cuenta puede requerir la MFA de IBMid en una cuenta de la que es miembro. La MFA de IBMid altera temporalmente cualquier otro valor de MFA del usuario. Por ejemplo, cuando se establece la MFA de IBMid, se le solicita una MFA de TOTP asociada con el IBMid en lugar de preguntas de seguridad o uno de los métodos de autenticación externa.
{: note}

Puede ver las siguientes opciones de seguridad y habilitarlas o inhabilitarlas solo si el administrador le proporciona acceso. Vaya al icono **{{site.data.keyword.avatar}}** ![Icono Avatar ](../icons/i-avatar-icon.svg) > **Perfil y valores** y seleccione **Valores de inicio de sesión**.

## Configuración de preguntas de seguridad
{: #security-questions}

Para configurar las preguntas de seguridad:
1. En la consola, vaya al icono **{{site.data.keyword.avatar}}** ![icono Avatar ](../icons/i-avatar-icon.svg) > **Perfil y valores** y seleccione **Valores de inicio de sesión**.
2. Pulse **Editar**. 
3. Seleccione las preguntas que desee y respóndalas. Debe utilizar tres opciones de preguntas de seguridad.
4. Pulse en **Guardar** cuando haya terminado.  
5. Para asegurarse, se marca el recuadro `Sí` para que se activen las preguntas de seguridad. Si selecciona el recuadro `Sí` es posible que se le solicite que vuelva a iniciar sesión.  

Puede configurar respuestas de las tres preguntas de seguridad para obtener una autenticación adicional en el inicio de sesión. Debe configurar las preguntas de seguridad y las respuestas para que el administrador pueda habilitar este requisito de la MFA.

Debe ser el propietario de la cuenta o disponer del valor de inicio de sesión gestionado por el usuario para que el administrador de la cuenta active y desactive las preguntas de seguridad.
{: note}

## Configuración de la caducidad de una contraseña
{: #password-expiration}

Para establecer el tiempo durante el que desea utilizar la contraseña actual, seleccione una opción de caducidad para su contraseña en la sección **Caducidad de la contraseña**.

La caducidad de la contraseña se establece en "nunca" de forma predeterminada. Cuando registre una cuenta, no se le solicitará que cambie la contraseña. Si establece un período de caducidad para la contraseña, se le notificará sobre la caducidad de la misma mediante un correo electrónico 14 y 7 días antes y el mismo día en que la contraseña caduca.

Esta opción solo está disponible para los usuarios que inicien sesión con un ID de SoftLayer. Para actualizar la caducidad de la contraseña, debe ser el propietario de la cuenta, o el administrador de la cuenta debe habilitar un valor de inicio de sesión gestionado por el usuario en la página de detalles del usuario de IAM.
{: note}

## Configuración de la autenticación TOTP
{: #MFA}

Para configurar la autenticación TOTP, pulse en **Configurar**. 

La MFA de TOTP añade una capa de seguridad adicional a su cuenta solicitando un código de acceso TOTP además del ID y la contraseña estándar durante el inicio de sesión. Debe configurar la autenticación TOTP antes de que el administrador de la cuenta pueda habilitar este requisito de la MFA.

Es posible que se le solicite un código de acceso de uso único basado en tiempo si el valor de TOTP del usuario no está configurado y habilitado. Esto se debe a que un propietario de la cuenta puede activar la MFA del IBMid para una cuenta a la que tenga acceso. Este tipo de MFA se aplica a cada usuario de la cuenta cuando el valor se activa y se le solicita que lo utilice. Para obtener más información, consulte [Tipos de autenticación de multifactores.](/docs/iam/mfatypes.html#types).


## Configuración de opciones de autenticación externas
{: #third-party-MFA}

El usuario y el administrador de la cuenta pueden solicitar la autenticación por teléfono o Symantec por un coste mensual. Para solicitar la autenticación externa, debe tener permisos para añadir infraestructura de servicios. Para saber si la autenticación externa está habilitada, vaya al icono **{{site.data.keyword.avatar}}** ![icono Avatar](../icons/i-avatar-icon.svg) > **Perfil y valores** y seleccione **Valores de inicio de sesión**. Si la MFA por teléfono está inhabilitada, pulse en **Ir a los detalles de usuario**. Este enlace le llevará a la misma página que la de los pasos para configurar la autenticación de symantec y la autenticación por teléfono.  

### Configuración de la autenticación de Symantec

Si el administrador de la cuenta decide solicitar la protección de identidad de Symantec, deberá trabajar con el administrador para ayudarle a completar el pedido proporcionando el ID de la credencial:

1. Vaya a [VIP de Symantec](https://vip.symantec.com/).
2. Pulse **Descargar**. 
3. Obtenga el ID de la credencial y proporcione el ID al administrador para completar el pedido. 

Cuando el administrador solicite y habilite la opción, podrá utilizar la app para la autenticación del inicio de sesión.

### Configuración de la autenticación por teléfono

Si el administrador de la cuenta decide solicitar la protección de identidad por teléfono, deberá configurarla cuando el administrador la solicite. Después, el administrador podrá habilitarla para que la utilice. Cuando el administrador haya solicitado la autenticación por teléfono, siga los pasos siguientes para configurarla:

1. Vaya a **Gestionar** > **Acceso (IAM)**.
2. Pulse en **Usuarios** y seleccione el nombre de la lista.
3. En la página **Detalles de usuario** en la sección **Gestionar inicio de sesión de usuarios**, pulse en el icono **Editar**![icono Editar](../icons/icon_write.svg) en la fila **Autenticación por teléfono**.
4. Siga las indicaciones para configurar la autenticación por teléfono.

Cuando haya configurado la autenticación por teléfono, el administrador de cuenta podrá habilitar la opción para que se le solicite el tipo de MFA que desea durante el inicio de sesión.


 

