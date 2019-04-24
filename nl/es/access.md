---

copyright:
  years: 2017, 2019
lastupdated: "2019-01-28"

keywords: user access, IBM Cloud account access, account owner

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Gestión del acceso de usuario al catálogo
{: #find-access}

Como propietario de la cuenta de {{site.data.keyword.Bluemix}} puede asignar a los usuarios acceso al catálogo utilizando una política de Identity and Access Management (IAM) de {{site.data.keyword.Bluemix_notm}}. Puede controlar la visibilidad de los servicios privados que se añaden al catálogo de cuenta o a los servicios públicos creados en la cuenta. De forma predeterminada, solo el propietario de la cuenta puede realizar estas tareas.

## Delegación de acceso
{: #get-access}

Puede delegar el acceso a la cuenta para controlar lo que pueden ver los usuarios y la cantidad de autoridad que tienen. Por ejemplo, es posible que parte de la información solo sea adecuada para que un usuario la lea y analice, mientras que otro usuario distinto podría tener autoridad para editar dicha información. Para delegar a la cuenta el acceso a otro usuario de la cuenta, realice los pasos siguientes.

1. Pulse en **Gestionar** > **Acceso (IAM)**.
2. Pulse en **El acceso comienza por el usuario** en la página de destino.
3. Seleccione un usuario de la cuenta.
4. Pulse **Políticas de acceso**.
5. Pulse **Asignar acceso**. A continuación, pulse en **Asignar servicios de gestión de cuentas**.
6. Seleccione el **Catálogo de recursos global** en la lista Servicios y el rol **Administrador** de la lista Seleccionar roles.

Para otorgar otros permisos, utilice los roles Visor y Editor. Revise la tabla siguiente para obtener más información sobre qué permite cada rol IAM a un usuario dentro del contexto de trabajar con el catálogo para su cuenta.

| Rol de gestión de plataforma | Acciones                                                                                                     |
|--------------------------|-------------------------------------------------------------------------------------------------------------|
| Visor                   | Puede ver los servicios privados, pero no puede cambiarlos                                                            |
| Editor                   | Puede cambiar los metadatos del objeto, pero no puede cambiar la visibilidad de los servicios privados                                |
| Administrador            | Puede cambiar los metadatos de objeto o la visibilidad de los servicios privados y restringir la visibilidad de un servicio público  |
{: caption="Tabla 1. Roles y acciones de gestión de plataforma de ejemplo para el catálogo" caption-side="top"}

Para obtener más información sobre la asignación de acceso a los usuarios, consulte [Asignación de acceso a los servicios de gestión de cuentas](/docs/iam?topic=iam-account-services).

## Confirmación del acceso
{: #confirm-access}

Cuando se le añade a la cuenta de otra persona, pueden delegarle niveles de acceso, de forma que pueda ver recursos privados que se han añadido a la cuenta. El propietario de la cuenta también puede delegar quién ve los recursos públicos en el catálogo de la cuenta. De forma predeterminada, no tiene este acceso. El propietario de la cuenta debe otorgarle un rol de IAM que le permita tener acceso para realizar estas tareas de gestión de recursos de la cuenta.

Puede utilizar la consola de {{site.data.keyword.Bluemix_notm}} o la interfaz de línea de mandatos (CLI) para determinar si tiene acceso para habilitar usuarios específicos y visualizar un recurso privado en la cuenta.

Para utilizar la consola, realice los pasos siguientes:

  1. Vaya a **Gestionar > Acceso (IAM)**.
  2. Pulse su nombre de la lista Usuarios.
  3. Pulse el separador **Políticas de acceso**, donde puede ver sus políticas de acceso asignadas. Debe tener el rol de administrador de Cloud IAM para el recurso de catálogo en su cuenta para actualizar la lista que incluye cuentas para ver recursos privados en el catálogo.


Para utilizar la [CLI](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_iam#ibmcloud_commands_iam), ejecute el mandato `ibmcloud iam user-policies <your-user-name>`. El mandato devuelve un error si no es un administrador de la cuenta.
