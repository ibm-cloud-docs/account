---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise account, multiple accounts, organization, hierarchy

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# ¿Qué es una empresa?
{: #enterprise}

Las empresas de {{site.data.keyword.Bluemix}} proporcionan una forma de gestionar de forma centralizada la facturación y el uso de recursos en varias cuentas. Dentro de una empresa, puede crear una jerarquía multinivel de cuentas, con facturación y pagos para todas las cuentas gestionadas a nivel de empresa.
{:shortdesc}

En comparación con el uso de varias cuentas autónomas, las empresas ofrecen las siguientes ventajas clave:
- Gestión centralizada de cuentas: Ver toda la jerarquía de la empresa de un vistazo, sin necesidad de cambiar de cuenta. Puede añadir cuentas existentes o crear nuevas cuentas directamente dentro de la empresa.
- Facturación consolidada de la suscripción: Realice un seguimiento de las suscripciones y del gasto de crédito para todas las cuentas desde una sola vista. Su crédito de suscripción se agrupa y se comparte entre las cuentas de la empresa.
- Informes de uso de arriba abajo: desde la cuenta de empresa, puede ver el uso de todas las cuentas de la empresa, organizadas por grupos de cuentas.

## Jerarquía de la empresa
{: #enterprise-hierarchy}

En su núcleo, una empresa se compone de tres bloques de construcción principales:
- La cuenta de empresa, que sirve como cuenta padre de todas las demás cuentas de la empresa. La cuenta de empresa gestiona la facturación de toda la empresa, con los costes de uso de todas las cuentas que se están desplegando y pagando desde la cuenta de empresa.
- Grupos de cuentas, que puede utilizar para organizar las cuentas relacionadas. Los grupos de cuentas no pueden contener recursos propios, pero puede ver los costes del uso de recursos desde las cuentas que contienen.
- Cuentas, que son como las cuentas autónomas de {{site.data.keyword.Bluemix_notm}} en tanto que contienen recursos y grupos de recursos, organizaciones de Cloud Foundry y espacios y permisos de acceso independientes. No obstante, una diferencia importante es que cada cuenta de una empresa no gestiona su propia facturación ni sus pagos, ya que éstos se gestionan en el nivel de cuentas de la empresa.

Puede crear niveles en la empresa anidando un grupo de cuentas dentro de otro grupo de cuentas.
![Un diagrama que muestra cuatro niveles de empresa. El nivel superior es la empresa, que contiene dos niveles de grupos de cuentas. Después, el grupo de cuentas contiene cuentas.](images/enterprise-hierarchy.svg "Los niveles de empresa se crean añadiendo grupos de cuentas.")

Una empresa puede contener hasta 10 niveles de cuentas y grupos de cuentas. En su forma más básica, una empresa tiene dos niveles: la cuenta de empresa y una sola cuenta secundaria.

Su estructura empresarial es flexible y puede crecer y cambiar según sus necesidades. Puede añadir y eliminar grupos de cuentas y mover cuentas de un grupo de cuentas a otro. Si el propósito de un grupo de cuentas cambia, puede cambiarle el nombre para que refleje mejor las cuentas que contiene.

## Facturación consolidada
{: #enterprise-billing}

En una empresa, toda la facturación se gestiona a través de la cuenta de empresa de nivel superior. Las empresas requieren una [facturación de suscripción](/docs/account?topic=account-accounts#subscription-account), lo que significa que se compra una suscripción para una cantidad de crédito que se debe gastar durante el período de suscripción, y el uso se deduce del crédito de suscripción a una tasa de descuento. El crédito de suscripción, así como el crédito de cualquier promoción, se añade a la agrupación de crédito de la empresa, que se comparte entre todas las cuentas de la empresa. A medida que las cuentas utilizan recursos, se gasta el crédito de la agrupación de crédito.

![Un diagrama que muestra que el crédito de las cuentas se añade a la agrupación de crédito de empresa, que gestiona el administrador de facturación en la cuenta de empresa.](images/enterprise-billing.svg "La facturación de todas las cuentas la gestiona el administrador de facturación de la cuenta de empresa.")

Dado que la facturación es consolidada, las empresas gestionan la facturación y los pagos de varias cuentas más fácilmente con estas ventajas clave:
* Una agrupación de crédito de suscripciones que abarca varias cuentas, de forma que puede cambiar el tamaño de las suscripciones para todo el uso en lugar de para el uso por cuenta
* Una sola factura para todo el uso dentro de la empresa, por lo que resulta más fácil identificar los costes
* Un solo lugar para gestionar los métodos de pago, de modo que puede actualizar una vez para todas las cuentas

Puede obtener más información en [Gestión centralizada de la facturación y el uso con las empresas](/docs/billing-usage?topic=billing-usage-enterprise).

## Gestión de recursos
{: #enterprise-resources}

Los recursos y servicios dentro de una empresa funcionan de la misma forma que en las cuentas autónomas. Cada cuenta de una empresa puede contener recursos en grupos de recursos y servicios en organizaciones y espacios de Cloud Foundry. Los grupos de cuentas no pueden contener recursos. Para obtener más información, consulte [Cómo trabajar con recursos y servicios](/docs/resources?topic=resources-resource).

![Un diagrama que muestra que los recursos están contenidos en las cuentas de la empresa.](images/enterprise-resources.svg "Los recursos están ligados a la cuenta en la empresa, igual que a una cuenta autónoma.")

Al igual que con todas las cuentas, los recursos están ligados al grupo de recursos y la cuenta donde se crean, por lo que no se pueden mover entre las distintas cuentas de una empresa. No obstante, gracias la flexible estructura de cuentas de la empresa, puede mover recursos dentro de la empresa moviendo las cuentas que los contienen.

## Informe completo de uso
{: #enterprise-usage}

Desde la cuenta de empresa, puede ver el uso de recursos de todas las cuentas de la empresa. Partiendo del nivel de empresa, puede ver los costes de uso estimados desglosados por cuenta y grupos de cuentas. Puede descender en la estructura de la empresa para ver los costes en cada nivel. En el nivel de cuentas, los usuarios de empresa pueden ver los costes de cada tipo de recurso o servicio de la cuenta.

Dado que el acceso a la empresa es independiente del acceso a cada cuenta, los usuarios de empresa no pueden crear ni gestionar automáticamente recursos dentro de las cuentas secundarias. De forma similar, los usuarios de cada cuenta pueden seguir viendo su uso pasado y actual desde la página de Uso independientemente de si tienen acceso de empresa.

Para obtener más información, consulte [Visualización del uso en una empresa](/docs/billing-usage?topic=billing-usage-enterprise-usage).

## Gestión de usuarios y de acceso aislada
{: #enterprise-access}

Las empresas mantienen aislada la gestión de usuarios y de acceso entre la empresa y sus cuentas secundarias para ofrecer una mayor seguridad de los datos de las cuentas. Los usuarios y su acceso asignado en la cuenta de empresa están completamente separados de los de las cuentas secundarias, y no se hereda automáticamente el acceso entre los dos tipos de cuentas.

Las listas de usuarios de cada cuenta sólo son visibles para los usuarios invitados a esa cuenta. Sólo por que se invite a un usuario y se le dé acceso para gestionar toda la empresa, no significa que pueda ver los usuarios invitados en cada cuenta secundaria. La gestión de usuarios en cada empresa y cada cuenta es totalmente independiente y debe ser gestionada por el propietario de la cuenta o por un usuario con el rol de administrador en el servicio de gestión de cuentas de gestión de usuarios de la cuenta específica.

Igual que la gestión de usuarios está completamente separada en cada cuenta y en la empresa propiamente dicha, lo mismo ocurre con la gestión de acceso. Esta separación significa que los usuarios que gestionan la empresa no pueden acceder a los recursos de cuenta dentro de las cuentas secundarias a menos que se les permita específicamente hacerlo. Por ejemplo, el responsable financiero puede tener el rol de administrador en el servicio de gestión de cuentas de facturación dentro de la cuenta de empresa, lo que le proporciona acceso a la información de facturación y de pago y a los datos de uso hasta el tipo de recurso. Pero, a menos que se le invite a una cuenta secundaria y tenga acceso al servicio de gestión de cuentas de facturación de esa cuenta, no puede ver las ofertas ni actualizar los límites de gasto de la cuenta secundaria.

Para obtener más información, consulte [Gestión de usuarios para empresas](/docs/iam?topic=iam-enterprise-access).

## ¿Cómo puedo utilizar una empresa?
{: #enterprise-use-cases}

Las empresas pueden ayudar a simplificar la gestión de cuentas y de facturación en casos que, si no, serían muy complejos. Las empresas pueden ser beneficiosas para la gestión de cualquier organización grande, pero dos ejemplos en los que posiblemente que desee crear una son las grandes empresas y las instituciones educativas.

La forma en que estructure su empresa depende de cómo desea analizar el uso y los costes, como por ejemplo para reembolsar el uso a un grupo en particular. Organice su empresa según cómo desee realizar el seguimiento y gestionar la facturación y el uso.
{:tip}

### Grandes empresas u organizaciones
{: #enterprise-orgs}

Las empresas pueden ser útiles para las grandes organizaciones que, de lo contrario, requieren varias cuentas separadas para sus departamentos o equipos. Utilizando grupos de cuentas, puede modelar la jerarquía de la empresa según la estructura de la organización.

#### Organizar por departamento
{: #enterprise-by-dept}

Si su organización tiene equipos globales que comparten un presupuesto, puede modelar la estructura de la empresa en base a sus departamentos. Con esta estructura, puede ver los costes de uso agregados en cada departamento.

![Una empresa de cuatro niveles que agrupa las cuentas según los departamentos de la organización. Por ejemplo, los grupos de cuentas se denominan Marketing, Development y Sales. Los grupos de cuentas contienen cuentas para los equipos dentro de esos departamentos. Por ejemplo, el grupo de cuentas de ventas contiene las cuentas Direct, Online y Enablement.](images/enterprise-by-dept.svg "Una empresa que organiza las cuentas según los departamentos de la organización.")

#### Organizar por geografía
{: #enterprise-by-geo}

O bien, si su organización tiene presupuestos separados según la ubicación geográfica, puede estructurar su empresa para agrupar los costes para cada entidad geográfica.

![Una empresa de cuatro niveles que agrupa las cuentas según la geografía. Por ejemplo, los grupos de cuentas se denominan Americas, Europe y Asia-Pacific. Los grupos de cuentas contienen cuentas para países dentro de esas ubicaciones. Por ejemplo, el grupo de cuentas Asia-Pacific contiene China, Japan e India.](images/enterprise-by-geo.svg "Una empresa que organiza las cuentas por geografía.")

### Instituciones educativas
{: #enterprise-edu}

Es posible que las instituciones educativas deseen proporcionar cuentas de {{site.data.keyword.Bluemix_notm}} a sus alumnos de forma que puedan adquirir conocimientos útiles a través de proyectos prácticos que utilizan servicios de {{site.data.keyword.Bluemix_notm}}. Para estas instituciones, como por ejemplo las universidades tradicionales o las plataformas de aprendizaje en línea, puede agrupar cuentas por departamento o área temática y, a continuación, crear cuentas para cada curso.

Dentro de cada cuenta, los estudiantes pueden crear recursos para construir sus proyectos y colaborar con otros estudiantes de la cuenta. La universidad tiene una visión completa de los costes de cada departamento y curso.

![Una empresa de tres niveles que modela la forma en que una universidad puede organizar sus cuentas. Por ejemplo, los grupos de cuenta se denominan según el departamento: Data Science, Computer Science y Computer Engineering. Cada grupo de cuentas contiene cuentas individuales para cada clase, como por ejemplo DS101 y DS102.](images/enterprise-edu.svg "Una empresa para una universidad que tiene grupos de cuenta para cada departamento, y cuentas individuales para cada clase.")
