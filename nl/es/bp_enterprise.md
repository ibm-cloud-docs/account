---

copyright:
  years: 2019
lastupdated: "2019-08-05"

keywords: enterprise, enterprise resources, enterprise account

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}


# Prácticas recomendadas para configurar una empresa
{: #enterprise-best-practices}

Estas prácticas recomendadas ofrecen conceptos básicos para configurar una empresa de {{site.data.keyword.cloud}}.
{:shortdesc}

## Organización de cuentas según la forma en que desea realizar un seguimiento de la facturación
{: #organize-enterprise-usage}

Una ventaja clave de las {{site.data.keyword.cloud_notm}} empresas es que le permiten ver y gestionar de forma centralizada la facturación y el uso de varias cuentas. La utilidad de esta característica depende de la estructura de la empresa, ya que los datos de uso se agregan por cada grupo de cuenta y cada cuenta. Cree grupos de cuentas para proyectos que funcionen bajo un presupuesto común. Consulte [¿Cómo puedo utilizar una empresa?](/docs/account?topic=account-enterprise#enterprise-use-cases) para ver los ejemplos.

Es posible que el administrador de empresa o el responsable de finanzas no estén familiarizados con cada cuenta o grupo de cuentas individuales. Para facilitar la identificación de su propósito, asigne a cada cuenta y grupo de cuentas un nombre descriptivo. Si la empresa utiliza códigos de facturación, también puede incorporarlos en el nombre. Por ejemplo, en lugar del grupo de cuentas `devteam` con las cuentas `fed ui` y `be api`, cree el grupo de cuentas `Development - A2B3` con las cuentas `Front-end UI team` y `Back-end API team`.

Un usuario de empresa con acceso de Administrador o Editor puede editar los nombres de empresa y de grupo de cuentas, pero no puede cambiar los nombres de cuenta. Para editar un nombre de cuenta, el usuario debe estar en la propia cuenta.
{:tip}

Dado que tiene una vista unificada de todo el uso que está organizado según sus grupos de cuentas y cuentas, puede cargar los costes de uso a los equipos asociados. Para obtener más información, consulte [Recuperación de costes para utilizarlos en la empresa](/docs/billing-usage?topic=billing-usage-enterprise-usage#enterprise-cost-recovery).

## Creación de una jerarquía de empresa coherente
{: #accounts-vs-groups}

Al configurar la empresa, cree una jerarquía de empresa que refleje su empresa u organización. Al crear cuentas y grupos de cuentas, planifique un esquema coherente de la forma en que la empresa utiliza las capas empresariales siguientes:
- Grupos de recursos y organizaciones y espacios de Cloud Foundry dentro de una cuenta
- Cuentas dentro de un grupo de cuentas
- Grupos de cuentas dentro de la empresa

Por ejemplo, su empresa puede crear cuentas para cada equipo, con grupos de recursos u organizaciones de Cloud Foundry dentro de la cuenta para entornos de desarrollo, pruebas y producción. Otra empresa puede tener cuentas distintas para cada entorno, que se agrupen en grupos de cuentas para cada equipo.

No importa la forma en que estructure la empresa, pero se recomienda ser lo más coherente posible para simplificar la gestión de la empresa. Debido a que es fácil crear y realizar el seguimiento de nuevas cuentas, puede haber la tentación de crear muchas cuentas distintas a medida que los usuarios las soliciten. Sin embargo, cada cuenta introduce una sobrecarga de gestión adicional. Al planificar cómo estructurar la empresa, tenga en cuenta los puntos siguientes:
- Para cada cuenta que cree, se debe invitar a los usuarios y su acceso debe gestionarse por separado.
- Una estructura incoherente puede hacer más difícil determinar a quién dar acceso dentro de cada cuenta y saber qué equipos utilizan recursos.
- Los usuarios pueden colaborar en recursos y servicios sólo dentro de una cuenta individual. Los recursos no se pueden pasar de una cuenta a la otra.

## Configuración de políticas de acceso en una empresa
{: #access-enterprise}

Como siempre, siga las prácticas recomendada para asignar el número mínimo de políticas de acceso y niveles de acceso. Esto le permite dedicar menos tiempo a asignar acceso a los usuarios y dedicar más tiempo al desarrollo en {{site.data.keyword.cloud_notm}}, y a la vez asegurarse de no proporcionar demasiado acceso a los usuarios que no lo necesitan.

Los grupos de acceso son una herramienta útil para asignar acceso a un grupo de usuarios e ID de servicio que necesitan el mismo acceso. Utilizando grupos de acceso, puede racionalizar la gestión de acceso asignando el mínimo número de políticas de acceso a los grupos de usuarios. A modo de ejemplo, si tiene cinco usuarios que desea que puedan gestionar todas las tareas relacionadas con la facturación y la gestión de cuentas para la empresa, puede añadirlos a un grupo de acceso denominado `Administrators`. En ese grupo de acceso, puede asignar dos políticas: una con el rol de administrador en el servicio de gestión de cuentas de facturación y una con el rol de administrador en todos los servicios de gestión de cuentas de la cuenta. A medida que los usuarios cambian de responsabilidades laborales o de equipo, puede añadir o eliminar usuarios del grupo de acceso en lugar de añadir o eliminar las políticas de los usuarios individuales. Consulte el apartado [Asignación de acceso de empresa](/docs/iam?topic=iam-assign-access-enterprise) para obtener más información.

## Cómo trabajar con recursos en una empresa
{: #child-resources-enterprise}

Cree los recursos sólo en las cuentas secundarias que importe o cree dentro de la empresa. Aunque es posible crear recursos dentro de la cuenta de empresa, no es recomendable por los siguientes motivos:
 - La cuenta de empresa es siempre hija directa de la empresa y no se puede mover, por lo que no tendrá la flexibilidad necesaria para cambiar el modo en que se informa sobre el uso de los recursos.
 - La cuenta de empresa contiene los usuarios y el acceso para la gestión de la empresa y su facturación, por lo que sólo deben añadirse a esta cuenta los usuarios con estas responsabilidades.

Los usuarios dentro de cada cuenta de la empresa pueden crear, utilizar y colaborar en los recursos de la misma forma que en una cuenta autónoma. Para obtener detalles, consulte [Cómo trabajar con recursos y servicios](/docs/resources?topic=resources-resource). Los usuarios de empresa no pueden trabajar directamente con recursos dentro de cuentas secundarias, pero pueden supervisar los tipos de recursos y los planes que se utilizan en cada cuenta mediante la visualización de su uso. Para obtener más información, consulte [Visualización del uso en una empresa](/docs/billing-usage?topic=billing-usage-enterprise-usage).


