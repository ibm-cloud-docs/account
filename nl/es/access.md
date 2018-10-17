---

copyright:

  years: 2017, 2018
lastupdated: "2018-10-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Gestión del acceso al catálogo
{: #find-access}

Como propietario de una cuenta, puede asignar acceso utilizando una política de IAM. Esto permite a los usuarios controlar la visibilidad de los servicios privados añadidos al catálogo de la cuenta o los servicios públicos que se crean en la cuenta. De forma predeterminada, solo el propietario de la cuenta puede realizar estas tareas.

## ¿Cómo delego el acceso como propietario de cuenta?
{: #get-access}

Como propietario de la cuenta, puede dar acceso a la cuenta asignando una política de acceso a un usuario mediante la interfaz de usuario de Identity and Access. Para garantizar el acceso necesario para el usuario, seleccione el recurso **Catálogo global** y el rol **Administrador** para la política de acceso.

Para otorgar otros permisos, utilice los roles `visor` y `editor` de Identity and Access Management (IAM). Revise la tabla siguiente para obtener más información sobre qué permite cada rol IAM a un usuario dentro del contexto de trabajar con el catálogo para su cuenta.

| Rol de gestión de plataforma | Descripción de acciones |
|:-----------------|:-----------------|
| Visor | Puede ver los servicios privados, pero no puede realizar cambios. |
| Editor | Puede hacer cambios en los metadatos de objeto pero no puede cambiar la visibilidad. |
| Administrador | Puede cambiar la visibilidad y los metadatos de objeto.  |
{: caption="Tabla 1. Roles y acciones de gestión de plataforma de ejemplo para el servicio de catálogo" caption-side="top"}

Para obtener instrucciones detalladas sobre la asignación de acceso a los usuarios en su cuenta, vaya a la documentación de [Acceso a recursos](/docs/iam/mngiam.html#iammanidaccser#resourceaccess).

## ¿Cómo puedo comprobar si tengo acceso?

Cuando se le añade a la cuenta de otra persona, pueden delegarle niveles de acceso, de forma que pueda ver recursos privados que se han añadido a la cuenta. El propietario de la cuenta también puede delegar quién ve los recursos públicos en el catálogo de la cuenta. De forma predeterminada, no tiene este acceso. El propietario de la cuenta debe otorgarle un rol de IAM que le permita tener acceso para realizar estas tareas de gestión de recursos de la cuenta.

Puede utilizar la CLI o la interfaz de usuario de identidad y acceso para determinar si tiene acceso para permitir a los usuarios ver un recurso privado que se ha añadido a la cuenta.

Para utilizar la interfaz de usuario de identidad y acceso, siga estos pasos:

1. Vaya a **Gestionar** > **Acceso (IAM)** y pulse **Usuarios**.
2. Pulse su nombre de la lista Usuarios.
3. Pulse el separador **Políticas de acceso**, donde puede ver sus políticas de acceso asignadas. Debe tener el rol de administrador de Cloud IAM para el recurso de catálogo en su cuenta para actualizar la lista que incluye cuentas para ver recursos privados en el catálogo.

Para utilizar la [CLI de {{site.data.keyword.Bluemix_notm}}](/docs/cli/reference/ibmcloud/bx_cli.html#ibmcloud_commands_iam), siga estos pasos:

Especifique el siguiente mandato con el nombre de usuario `ibmcloud iam user-policies <your-username>` para saber si es un administrador de cuentas que ha seleccionado en la CLI. Si no es un administrador de su cuenta, estos mandatos devuelven un error que dice que no está autorizado.
{: tip}
