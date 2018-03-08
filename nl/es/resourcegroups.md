---



copyright:

  years: 2017, 2018
lastupdated: "2018-02-08"


---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Gestionar grupos de recursos
{: #rgs}

Un grupo de recursos es una manera de organizar sus recursos de cuenta en agrupaciones personalizables, para que pueda asignar accesos de usuario rápidamente a más de un recurso a la vez. Cualquier recurso de cuenta gestionado utilizando el control de acceso de la Gestión de identidad y acceso de {{site.data.keyword.Bluemix}} pertenece a un grupo de recursos dentro de su cuenta. Los servicios de Cloud Foundry permanecen asignados a organizaciones o espacios y no se pueden añadir a un grupo de recursos.

Para empezar a gestionar sus grupos de recursos, vaya a **Gestionar** &gt; **Cuenta** &gt; **Grupos de recursos** en la consola de {{site.data.keyword.Bluemix}}. Desde ahí puede ver sus grupos de recursos, renombrarlos y crear nuevos grupos de recursos.

## Visualización de recursos dentro de grupos de recursos

Para ver fácilmente los recursos que contiene un grupo de recursos, filtre por grupo de recursos desde su panel de control.

## Creación de un grupo de recursos

Si tiene una cuenta de Pago según uso o de Suscripción, puede crear varios grupos de recursos para gestionar fácilmente la cuota y ver el uso de facturación de un conjunto de recursos. También puede agrupar recursos para facilitarles la asignación de acceso a los usuarios a más de una instancia a la vez.

Si tiene una cuenta Lite o una prueba de 30 días, no puede crear grupos de recursos adicionales pero puede renombrar su grupo de recursos predeterminado. 

Cada grupo de recursos es gratuito, sin embargo, las conexiones entre un grupo de recursos y una organización o espacio de Cloud Foundry se tienen en cuenta en su cuota de cuenta. Para obtener más información, consulte [¿Qué es un alias?](/docs/cfapps/connecting_apps.html#what_is_alias)
{: tip}

1. Vaya a **Gestionar** &gt; **Cuenta** &gt; **Grupos de recursos**.
2. Pulse **Crear un grupo de recursos**.
3. Especifique un nombre para su grupo de recursos.
4. Pulse **Añadir**.

## Cómo renombrar un grupo de recursos

Su primer grupo de recursos se crea y se llama `Default`. Puede actualizar el nombre de este grupo o cualquier otro grupo que cree.

1. Vaya a **Gestionar** &gt; **Cuenta** &gt; **Grupos de recursos**.
2. Pulse **Renombrar**.
3. Especifique un nombre exclusivo y pulse **Guardar**.

## Gestión de grupos de recursos utilizando la CLI de {{site.data.keyword.Bluemix_notm}}

La CLI de {{site.data.keyword.Bluemix_notm}} tiene varios mandatos que soportan la gestión de recursos. Para obtener más información, consulte [Mandatos para gestionar grupos de recursos y recursos](/docs/cli/reference/bluemix_cli/bx_cli.html#commands-for-managing-resource-groups-and-resources).

## Gestión del acceso a sus grupos de recursos

Cloud IAM le ofrece la flexibilidad de proporcionar acceso de usuario preciso a recursos en su cuenta. Puede utilizar Cloud IAM para asignar políticas a usuarios, que proporcionan acceso de usuario a todos los recursos de un grupo de recursos, a un único tipo de servicio dentro de un grupo de recursos o a una instancia de servicio individual en su cuenta. Proporcionar acceso a los usuarios a los recursos en un grupo de recursos no les da acceso para gestionar el grupo de recursos en sí mismo. Puede establecer accesos para las capacidades de ver, editar y gestionar el grupo de recursos actual por separado.

Para obtener más información sobre la gestión del acceso a grupos de recursos, consulte [Gestión del acceso IAM](/docs/iam/mngiam.html#iammanidaccser).
