---

copyright:

  years: 2017, 2018
lastupdated: "2017-11-21"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Gestión del acceso al catálogo
{: #find-access}

Como propietario de cuenta, es posible que desee asignar acceso mediante una política IAM para permitir a los usuarios de su cuenta controlar la visibilidad de los servicios privados añadidos al catálogo de la cuenta o los servicios públicos que se han creado en la cuenta. De forma predeterminada, solo el propietario de la cuenta puede para completar estas tareas.

## ¿Cómo delego el acceso como propietario de cuenta?
{: #get-access}

Si es propietario de la cuenta, puede dar acceso a un usuario a su cuenta a través de la interfaz de usuario de identidad y acceso asignando una política de acceso. Para garantizar que el usuario tenga el acceso necesario, seleccione el recurso **Catálogo global** y el rol **Administrador** para la política de acceso.

Puede que desee otorgar permisos a otros usuarios de la cuenta mediante los roles `visor` y `editor` de Identity and Access Management (IAM). Revise la tabla siguiente para obtener más información sobre qué permite cada rol IAM a un usuario dentro del contexto de trabajar con el catálogo para su cuenta.

| Rol de gestión de plataforma | Descripción de acciones |
|:-----------------|:-----------------|
| Visor | Puede ver los servicios privados, aunque la cuenta no se haya incluido, pero no puede realizar cambios. |
| Editor | Puede hacer cambios en los metadatos de objeto pero no puede cambiar la visibilidad. |
| Administrador | Puede cambiar la visibilidad y los metadatos de objeto.  |
{: caption="Tabla 1. Roles y acciones de gestión de plataforma de ejemplo para el servicio de catálogo" caption-side="top"}

Para obtener instrucciones detalladas sobre la asignación de acceso a los usuarios en su cuenta, vaya a la documentación de [Acceso a recursos](/docs/iam/mngiam.html#iammanidaccser#resourceaccess).


## ¿Cómo puedo comprobar si tengo acceso?

Cuando se le añade a la cuenta de otra persona, pueden delegarle ciertos niveles de acceso, de forma que pueda ver recursos privados que se han añadido a la cuenta. El propietario de la cuenta también puede delegarle la capacidad de gestionar quién ve los recursos públicos en el catálogo de la cuenta. De forma predeterminada, no tiene este acceso. El propietario de la cuenta debe otorgarle un rol de IAM que le permita tener acceso para realizar estas tareas de gestión de recursos de la cuenta.

Puede utilizar la CLI o la interfaz de usuario de identidad y acceso para determinar si tiene acceso para permitir a los usuarios ver un recurso privado que se ha añadido a la cuenta.

Para utilizar la interfaz de usuario de identidad y acceso, siga estos pasos:

1. Vaya a **Gestionar** > **Seguridad** > **Identidad y acceso** y luego pulse **Usuarios**.
2. Pulse su nombre de la lista Usuarios.
3. En la sección **Políticas de acceso**, puede ver sus políticas de acceso asignadas. Debe tener el rol de administrador de Cloud IAM para el recurso de catálogo en su cuenta para actualizar la lista que incluye cuentas para ver recursos privados en el catálogo.

Para utilizar la [CLI de bx](/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_iam), siga estos pasos:

Especifique el siguiente mandato con el nombre de usuario `bx iam user-policies <your-username>` para saber si es un administrador de cuentas que ha seleccionado en la CLI. Si no es un administrador de su cuenta, estos mandatos devuelven un error que dice que no está autorizado.
{: tip}
