---

copyright:

  years: 2018
lastupdated: "2018-10-31"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Prácticas recomendadas para configurar su cuenta
{: #account_setup}

Las prácticas recomendadas ofrecen conceptos básicos para alcanzar el éxito antes de empezar a crear recursos. Si está listo para colocar las apps en producción y configurar un entorno para sus desarrolladores, examine las siguientes secciones para configurar su cuenta.
{:shortdesc}

Las siguientes prácticas recomendadas se centran en el uso de servicios habilitados para IAM. Actualmente, no todos los servicios de {{site.data.keyword.cloud}} están habilitados para IAM. Si una instancia de servicio de la cuenta pertenece a una organización y un espacio de Cloud Foundry, no se le aplican políticas de IAM, grupos de recursos ni grupos de acceso. Puede utilizar tanto organizaciones y espacios de Cloud Foundry como grupos de recursos en su cuenta, pero debe asignar a los usuarios acceso a estos recursos por separado. Para obtener información sobre cómo trabajar con organizaciones y espacios de Cloud Foundry, consulte [Adición de organizaciones y espacios](/docs/account/orgs_spaces.html#orgsspacesusers).
{: tip}

## ¿Qué es una buena estrategia de grupo de recursos?
{: #resource-group-strategy}

Puesto que un grupo de recursos es un contenedor lógico para los recursos, el uso de un grupo de recursos por entorno de proyecto es un buen punto de partida. Esta estrategia permite a los administradores controlar y ver el uso de recursos a nivel de entorno del proyecto. Por ejemplo, un proyecto típico tiene entornos de desarrollo, prueba y producción. Por lo tanto, un proyecto que denominado `CustApp` tendría los siguientes grupos de recursos:

* CustApp-Dev
* CustApp-Test
* CustApp-Prod

Luego se puede otorgar acceso a los usuarios. Por ejemplo, un desarrollador normalmente tiene derechos de acceso bastante amplios sobre el grupo de recursos de desarrollo y mucho más reducidos o no tiene acceso al grupo de recursos de producción.

Si tiene una cuenta de Pago según uso o de Suscripción, puede crear grupos de recursos adicionales: 

1. Vaya a **Gestionar** &gt; **Cuenta** &gt; **Grupos de recursos**.
2. Pulse **Crear un grupo de recursos**.
3. Especifique el nombre del grupo de recursos.
4. Pulse **Añadir**.

## Configuración de los grupos de recursos
{: #setting-up-rgs}

Los grupos de recursos son un contenedor lógico para organizar los recursos habilitados para IAM. Todos los servicios gestionados mediante el control de acceso de IAM pertenecen a un grupo de recursos. Asigna un recurso a un grupo de recursos cuando lo crea desde el catálogo. No puede cambiar la asignación del grupo de recursos después de establecerla, por lo que es importante configurar algunos de los grupos de recursos ahora.

Si tiene una cuenta de prueba o Lite, puede utilizar el grupo de recursos predeterminado y no puede crear ningún otro.
{: tip}

## Adición de recursos a un grupo de recursos
{: #adding-resources}

Cuando se crea un recurso habilitado para IAM desde el catálogo, el grupo de recursos al que desea asignarlo debe estar seleccionado. Una vez que se ha creado un recurso, no puede cambiar el grupo de recursos al que se ha asignado. Si comete un error en esta fase, tiene que suprimir el recurso y crear uno nuevo.

### Acceso necesario para añadir un recurso a un grupo de recursos
{: #rg_access}

El propietario de la cuenta de {{site.data.keyword.cloud_notm}} puede añadir recursos a cualquier grupo de recursos. Sin embargo, a otros usuarios se les debe otorgar acceso mediante una política de acceso de IAM. Hay dos roles de gestión de plataforma mínimos que se debe asignar a los usuarios para que puedan añadir recursos a un grupo de recursos:

* Rol de visor o superior sobre el propio grupo de recursos
* Rol de editor o superior sobre el recurso o servicio

Para añadir un recurso a un grupo de recursos, siga los siguientes pasos:

1. Vaya a **Gestionar** &gt; **Cuenta** &gt; **Grupos de recursos**.
2. Pulse el menú del icono Más acciones ![Icono Más acciones](../icons/overflow-menu.svg) correspondiente al grupo de recursos al que desea añadir recursos y seleccione **Añadir recursos**.
3. Cuando se le redirija al catálogo, seleccione el recurso que desea añadir.
4. Seleccione el grupo de recursos al que desea asignarlo.
5. Pulse **Crear**.

Siempre puede ir directamente al catálogo para crear recursos y asignarlos a un grupo de recursos.
{: tip} 

Para obtener más información, consulte [Prácticas recomendadas para organizar los recursos en un grupo de recursos](/docs/resources/bestpractice_rgs.html#bp_resourcegroups).

## Pasos siguientes

Configure los grupos de acceso para los usuarios y los ID de servicio que requieren el mismo acceso a recursos y grupos de recursos en su cuenta. Puede asignar un número mínimo de políticas de acceso, lo que le ahorra tiempo. Para obtener más información, consulte [Prácticas recomendadas para asignar acceso](/docs/iam/bp_access.html).

Consulte [Prácticas recomendadas para organizar usuarios, equipos y aplicaciones](/docs/tutorials/users-teams-applications.html#best-practices-for-organizing-users-teams-applications) para obtener más información sobre cómo configurar usuarios y equipos en su cuenta. 
