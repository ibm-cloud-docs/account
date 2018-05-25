---

copyright:

  years: 2017, 2018

lastupdated: "2018-04-26"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}
{:gif: data-image-type='gif'}
{:tip: .tip}

# Migración de instancias de servicio de Cloud Foundry a un grupo de recursos
{: #migrate}

Cuando los servicios pasen de utilizar roles, espacios y organizaciones de Cloud Foundry a utilizar Cloud Identity and Access Management (IAM) y grupos de recursos, podrá migrar las instancias de servicio de Cloud Foundry a un [grupo de recursos](/docs/account/resourcegroups.html#rgs). La migración de instancias de servicio a un grupo de recursos tiene varios beneficios, incluido un control de acceso más granular utilizando roles de IAM y conectando instancias de servicio a apps y servicios de distintas regiones.

Cuando un servicio deje Cloud Foundry, se le solicitará mediante un mensaje en el panel de control que migre a instancias de servicio existentes. Puede identificar los servicios que están listos para que los migre el icono ![Migrar esta instancia de servicio a un grupo de recursos](images/migrate.svg "Migrar esta instancia de servicio a un grupo de recursos").
{:shortdesc}

Cuando migre instancias de servicio de Cloud Foundry a un grupo de recursos, no podrá cambiar el grupo que haya seleccionado una vez la migración se haya completado. Por lo tanto, asegúrese de planificar cómo desea organizar los recursos en la cuenta antes de realizar la migración. Esto puede requerir que cree uno o varios grupos de recursos, si dispone de una cuenta facturable, antes de realizar la migración. Puede intentar organizar los recursos en grupos de recursos de la misma forma que ha organizado recursos en los espacios de Cloud Foundry.
{: tip}

## ¿Por qué migrar instancias de servicio?

Los servicios que ofrecen soporte al control de acceso y organización de IAM Cloud en grupos de recursos disponen de varios beneficios, como la capacidad de conectarse a apps y servicios en cualquier espacio de Cloud Foundry, lo que permite conexiones en apps y servicios de distintas regiones. Para crear la conexión, puede crear un alias de una instancia desde un grupo de recursos en un espacio de Cloud Foundry. Cuando realice la migración, la conexión se establecerá automáticamente convirtiendo su instancia de servicio de Cloud Foundry original en un alias y creando una instancia enlazada a un grupo de recursos de su elección.

![Enlace de una instancia de servicio a un espacio de Cloud Foundry para crear un alias](images/alias.svg "Enlace de una instancia de servicio a un espacio de Cloud Foundry para crear un alias")

Asimismo, cada instancia gestionada por Cloud IAM pertenece a un grupo de recursos. Los grupos de recursos no se tratan por regiones, por lo que puede proporcionar apps y servicios de distintas regiones en el mismo grupo de recursos. También puede aprovechar el control de acceso granular en un nivel de instancia individual.

## ¿Quién puede migrar instancias de servicio?
{: #whocanmigrate}

Los usuarios deben tener acceso específico para migrar instancias de servicio de Cloud Foundry a un grupo de recursos:

* El usuario debe tener el rol de desarrollador en el espacio de Cloud Foundry o el rol de gestor de la organización de Cloud Foundry en la organización a la que pertenece la instancia.
* El usuario debe tener al menos el rol de IAM Visor para gestionar el grupo de recursos al que se va a migrar la instancia.
* El usuario debe tener al menos el rol de IAM Editor en el servicio.

Para obtener más información sobre la asignación del acceso correcto, consulte [Acceso de Cloud Foundry](/docs/iam/cfaccess.html#cfaccess) y [Acceso de IAM](/docs/iam/users_roles.html#platformrolestable).

Para comprobar qué acceso tiene, en la barra de menús pulse **Gestionar** &gt; **Seguridad** &gt; **Identidad y acceso** y pulse **Usuarios**. A continuación, pulse en su nombre y revise las **Políticas de acceso** de los roles IAM asignados y el **Acceso de Cloud Foundry** para ver a qué organizaciones tiene acceso y los roles de Cloud Foundry que tiene asignados.
{: tip}


## ¿Cómo funciona la migración?

Cuando migra una instancia de servicio desde un espacio y organización de Cloud Foundry a un grupo de recursos, se crea en el grupo de recursos una nueva instancia de servicio enlazada. La instancia original de la organización y el espacio de Cloud Foundry pasa a ser un [alias](/docs/cfapps/connecting_apps.html#what_is_alias). El alias se tendrá en cuenta en relación con la cuota de su organización, pero se le facturará por el uso de la instancia de servicio en el grupo de recurso.

![Migración de una instancia de servicio de Cloud Foundry a un grupo de recursos](images/migration.gif){: gif}

Puede migrar sus instancias de servicio de una en una cuando se lo notifique en el panel de control el icono ![Migrar esta instancia de servicios a un grupo de recursos](images/migrate.svg "Migrar esta instancia de servicio a un grupo de recursos") asociado a su instancia de servicio de Cloud Foundry.

1. Abra el menú **Más acciones**.
2. Seleccione **Migrar a un grupo de recursos** para empezar.
3. Seleccione un grupo de recursos.
4. Pulse **Migrar** y la instancia se migrará.
5. Como solo puede migrar una instancia a la vez, puede continuar migrando instancias elegibles cuando haya realizado la migración de la primera.

Cuando haya migrado una instancia correctamente, la verá reflejada en la sección Servicio del panel de control. El alias permanecerá en la sección de Cloud Foundry del panel de control. Puede utilizar el ![Icono de enlace](images/link.svg "Icono de enlace que representa un alias") en la sección de Cloud Foundry del panel de control para identificar los alias.

## Resolución de problemas

Si se le presentan problemas al migrar instancias de servicio de Cloud Foundry, consulte [Resolución de problemas de migración de instancias de servicio](/docs/troubleshoot/ts_migration.html).
