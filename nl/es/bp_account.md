---

copyright:
  years: 2018, 2019
lastupdated: "2019-01-28"

keywords: resource group, account access, user access, IAM, organize

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Prácticas recomendadas para configurar su cuenta
{: #account_setup}

Las prácticas recomendadas ofrecen conceptos básicos para alcanzar el éxito antes de empezar a crear recursos. Si está listo para colocar las apps en producción y configurar un entorno para sus desarrolladores, examine las siguientes secciones para configurar su cuenta.
{:shortdesc}

Las siguientes prácticas recomendadas se centran en el uso de servicios habilitados para IAM. Actualmente, no todos los servicios de {{site.data.keyword.cloud}} están habilitados para IAM. Las políticas de IAM, los grupos de recursos y los grupos de acceso no se aplican a las instancias de servicio que pertenecen a una organización o espacio de Cloud Foundry. Puede utilizar tanto organizaciones y espacios de Cloud Foundry como grupos de recursos en su cuenta, pero debe asignar a los usuarios acceso a estos recursos por separado. Para obtener información sobre organizaciones y espacios de Cloud Foundry, consulte [Adición de organizaciones y espacios](/docs/account?topic=account-orgsspacesusers).
{: note}

## ¿Qué es una buena estrategia de grupo de recursos?
{: #resource-group-strategy}

Los administradores pueden tener un mejor control del uso de recursos en el nivel de entorno de proyecto si se utiliza un grupo de recursos por entorno de proyecto. Por ejemplo, un proyecto típico tiene entornos de desarrollo, prueba y producción. Un proyecto que se denomina `CustApp` tendría los siguientes grupos de recursos:

* `CustApp-Dev`
* `CustApp-Test`
* `CustApp-Prod`

Puede otorgar acceso a los usuarios. Por ejemplo, un desarrollador normalmente tiene permisos de acceso bastante amplios sobre el grupo de recursos de desarrollo y mucho más reducidos o no tiene acceso al grupo de recursos de producción.

Si tiene una cuenta de Pago según uso o de Suscripción, puede crear grupos de recursos adicionales:

1. Vaya a **Gestionar** > **Cuenta** y seleccione **Grupos de recursos** del menú **Recursos de cuenta**.
3. Pulse **Crear**.
4. Especifique el nombre del grupo de recursos.
5. Pulse **Añadir**.

Para obtener información sobre qué tipo de cuenta funcionará mejor, consulte [Tipos de cuenta](/docs/account?topic=account-accounts).


## Configuración de los grupos de recursos
{: #setting-up-rgs}

Los grupos de recursos son un contenedor lógico para organizar los recursos habilitados para IAM. Todos los servicios gestionados utilizando el control de acceso de Identity and Access Management (IAM) de {{site.data.keyword.cloud_notm}} pertenecen a un grupo de recursos. Asigna un recurso a un grupo de recursos cuando lo crea desde el catálogo. No puede cambiar la asignación del grupo de recursos después de establecerla, por lo que es importante configurar algunos de los grupos de recursos ahora.

Si tiene una cuenta Lite, tiene acceso a un único grupo de recursos creado automáticamente. No puede crear grupos de recursos adicionales. Considere la posibilidad de [actualizar su cuenta](/docs/account?topic=account-changeacct#changeacct) para crear y trabajar con varios grupos de recursos.
{: note}


## Adición de recursos a un grupo de recursos
{: #adding-resources}

Puede añadir un recurso a un grupo de recursos cuando cree un recurso habilitado para IAM desde el catálogo. Cuando seleccione el recurso, asegúrese de que se selecciona un grupo de recursos de destino. Una vez se haya creado un grupo de recursos, no puede cambiar el grupo de recursos asignado. Si accidentalmente asigna un recurso al grupo de recursos incorrecto, suprímalo y cree uno nuevo.

### Acceso necesario para añadir un recurso a un grupo de recursos
{: #rg_access}

Como propietario de una cuenta, puede añadir recursos a cualquier grupo de recursos. A otros usuarios se les debe otorgar acceso mediante una política de acceso de IAM para añadir recursos al grupo de recursos. Hay dos roles de gestión de plataforma mínimos que se debe asignar a los usuarios para que puedan añadir recursos a un grupo de recursos:

* Rol de visor o superior en el grupo de recursos
* Rol de editor o superior sobre el recurso o servicio

Para añadir un recurso a un grupo de recursos, siga los siguientes pasos:

1. Vaya a **Gestionar > Cuenta** y seleccione **Grupos de recursos**.
2. Pulse en el icono de Acciones ![Icono de acciones](../icons/action-menu-icon.svg) correspondiente al grupo de recursos al que desea añadir recursos y seleccione **Añadir recursos**.
3. Cuando se le redirija al catálogo, seleccione el recurso que desea añadir.
4. Seleccione el grupo de recursos al que desea asignarlo.
5. Pulse **Crear**.

Siempre puede ir directamente al catálogo para crear recursos y asignarlos a un grupo de recursos.
{: tip}

Para obtener más información, consulte [Prácticas recomendadas para organizar los recursos en un grupo de recursos](/docs/resources?topic=resources-bp_resourcegroups).


## Cómo utilizar etiquetas para organizar recursos
{: #tags}

Utilice etiquetas para organizar los recursos y realizar un seguimiento de los costes de uso. Puede etiquetar los recursos relacionados y visualizarlos en toda la cuenta filtrando por etiquetas desde el panel de control. Los pares de etiquetas Key:value pueden ayudarle a organizar los entornos de desarrollo, los proyectos, la conformidad y la optimización.

Para añadir una etiqueta a un recurso, siga estos pasos:

1. Pulse en el icono de Menú ![icono Menú](../icons/icon_hamburger.svg) > **Lista de recursos** para ver la lista de recursos. Busque el recurso que desea etiquetar.
2. Si el recurso ya tiene una etiqueta, pase el cursor por encima de la etiqueta existente y pulse en el icono Editar ![icono Editar](../icons/edit-tagging.svg). Si el recurso no tiene ninguna etiqueta, pase el curso por **--** en la columna `Etiquetas` y pulse en **Añadir etiquetas**.
3. Escriba un nombre para la etiqueta y pulse la tecla Intro después de añadir cada etiqueta si añade más de una.
4. Para eliminar una etiqueta del recurso, pulse en el icono Eliminar ![icono Eliminar](../icons/close-tagging.svg) junto a la etiqueta.
5. Guarde los cambios.

Para obtener más información sobre qué recursos se pueden etiquetar y cómo asignar acceso para delegar la funcionalidad de etiquetado a los usuarios de su cuenta, consulte [Cómo trabajar con etiquetas](/docs/resources?topic=resources-tag).


## Pasos siguientes

Configure los grupos de acceso para los usuarios y los ID de servicio que requieren el mismo acceso a recursos y grupos de recursos en su cuenta. Puede asignar un número mínimo de políticas de acceso, lo que le ahorra tiempo. Para obtener más información, consulte [Prácticas recomendadas para asignar acceso](/docs/iam?topic=iam-cfaccess).
