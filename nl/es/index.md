---

copyright:
  years: 2015, 2019
lastupdated: "2019-06-03"

keywords: account types, Lite, free account, paid account, buy account, account difference, compare account, subscription, service bundle

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}
{:row-headers: .row-headers}

# Tipos de cuentas
{: #accounts}

{{site.data.keyword.Bluemix_notm}} tiene tres tipos de cuentas: Lite, Pago según uso y Suscripción. En cuanto se registra, obtiene una cuenta Lite gratuita. Las cuentas de Pago según uso y Suscripción son nuestras opciones de pago y cada una ofrece distintas características. Compare cada cuenta y elija la que mejor se adapte a sus necesidades.
{:shortdesc}

## Comparación de cuentas
{: #compare}

La siguiente tabla proporciona una comparación de las cuentas Lite, Pago según uso y Suscripción. Para obtener más detalles acerca de cada cuenta, consulte las siguientes secciones.

|                                         | Lite               | Pago según uso      | Suscripción       |
|-----------------------------------------|--------------------|--------------------|--------------------|
| **Acceso a memoria de Cloud Foundry gratuita** | 256 MB             | 512 MB             | 512 MB             |
| **Acceso a [planes de servicio Lite ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://{DomainName}/catalog/?search=label:lite){: new_window}** | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
| **Acceso a todos los planes gratuitos**            |                    | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
| **Acceso al catálogo completo de {{site.data.keyword.Bluemix_notm}}** |  | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
| **Acceso a varias regiones de Cloud Foundry** |               | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
| **Sin restricciones de tiempo** | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
| **Coste cero garantizado**                | ![Característica disponible](../icons/icon_enabled.svg) |  |         |
| **Descuentos en los precios**                  |                    |                    | ![Característica disponible](../icons/icon_enabled.svg) |
| **Adecuado para aprender o crear pruebas de conceptos** | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |  |
| **Ajuste para casos de uso de producción**        |                    | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
{: row-headers}
{: class="comparison-table"}
{: caption="Tabla 1. Comparación de cuentas de {{site.data.keyword.Bluemix_notm}}" caption-side="top"}
{: summary="This table has row and column headers. The row headers identify the feature. The column headers identify the account type. To understand which features apply to the account types, navigate to the row, and find the feature that you're interested in."}

## Cuenta Lite
{: #liteaccount}

Regístrese para una cuenta Lite para empezar a crear sus apps y explorar servicios con planes Lite gratuitos seleccionados, que se muestran con una etiqueta Lite ![etiqueta Lite](../icons/Lite.svg) en la consola de {{site.data.keyword.Bluemix_notm}}. Su cuenta Lite no caduca y la tarjeta de crédito no es necesaria.

Tiene acceso a un único grupo de recursos creado para usted y llamado `Default`. Todas las instancias de su servicio gestionadas por {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) se añaden automáticamente a este grupo de recursos. Puede actualizar en nombre de este grupo de recursos en cualquier momento. Consulte [Cómo renombrar un grupo de recursos](/docs/resources?topic=resources-rgs#rename_rgs) para obtener los pasos detallados.

Cada grupo de recursos es gratuito. Cuando crea una conexión entre un servicio gestionado por IAM y una app de Cloud Foundry, crea un alias, que es una instancia de servicio que cuenta en el cálculo de su cuota. Consulte [Gestión de conexiones](/docs/resources?topic=resources-connect_app).
{: tip}

### ¿Qué hay disponible?
{: #lite-account-features}

Consulte la siguiente lista con las características principales que están disponibles en una cuenta Lite:

   * La cuenta es gratuita. No necesita tarjeta de crédito.
   * La cuenta no caduca nunca.
   * Puede utilizar una organización en una región de {{site.data.keyword.Bluemix_notm}}.
   * Soporte básico de {{site.data.keyword.Bluemix_notm}} de forma gratuita. El soporte básico se proporciona para entornos de no producción o cargas de trabajo donde las gravedades tradicionales no se utilizan y los tiempos de respuesta específicos no están estipulados.
   * Recibirá notificaciones de correo electrónico sobre el estado de la cuenta y los límites de la cuota.
   * Sus apps de Cloud Foundry pueden acceder hasta un máximo de 256 MB de memoria de tiempo de ejecución gratuita e instantánea al mes.
   * Puede suministrar una instancia de cualquier servicio en el [catálogo de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} que tiene el plan Lite.
   * Después de 10 días de inactividad de desarrollo, sus apps entrarán en suspensión. Puede activar sus apps si continúa trabajando con las mismas.
   * Después de 30 días de inactividad de desarrollo, se suprimirán las instancias de servicio con planes Lite.

## Cuenta de Pago según uso
{: #paygo}

Con una cuenta de pago según uso, puede acceder a todo el catálogo de {{site.data.keyword.Bluemix_notm}}, incluidos todos los planes gratuitos, y obtiene el doble de memoria de tiempo de ejecución gratuita a 512 MB al mes. Solo pagará los servicios facturables que utilice, sin contratos ni compromisos a largo plazo.

Puede crear varios grupos de recursos para gestionar fácilmente la cuota y ver el uso de facturación de un conjunto de recursos. Los cargos son en función del uso del cálculo y los servicios de {{site.data.keyword.Bluemix_notm}}. Si utiliza más de un tiempo de ejecución gratuito y concesiones de servicio, recibirá una factura mensual con detalles sobre los cargos de recursos.

Además, con una cuenta de pago según uso, puede solicitar planes de soporte premium o avanzados para obtener más ayuda con las cargas de trabajo de producción. Encontrará más información en el apartado sobre [Planes de soporte](/docs/get-support?topic=get-support-support-plans).

## Cuenta de Suscripción
{: #subscription-account}

Con una cuenta de Suscripción, puede crear varios grupos de recursos para gestionar fácilmente la cuota y ver el uso de facturación de un conjunto de recursos. Se compromete a una cantidad de gasto mínimo al mes y recibirá un descuento por suscripción que se aplicará a dicho cargo mínimo.

Por ejemplo, si se compromete a gastar 100 $ al mes durante 6 meses, puede obtener un descuento del 10 %. Mientras dure la suscripción, obtiene 600 $ de uso pero solo paga 540 $. Cuando más largo sea el periodo de la suscripción, mayor es el descuento.

El uso se resta del importe total de la suscripción. Aunque el uso varíe de mes a mes, la factura siempre es previsible y coherente. Si su uso supera la cantidad total de la suscripción, se le cargará una tasa sin descuento por la parte excedente.

Al igual que sucede con las cuentas de pago según uso, la cuenta de suscripción le permite solicitar planes de soporte avanzados o premium para obtener más ayuda si la necesita. Encontrará más información en el apartado sobre [Planes de soporte](/docs/get-support?topic=get-support-support-plans).

Si tiene una cuenta de suscripción, puede crear la mayoría de los servicios que están disponibles en el [catálogo de {{site.data.keyword.Bluemix_notm}}](https://{DomainName}/catalog){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo"). Sin embargo, algunos servicios utilizan un plan de precios específicos que requiere que se adquieran por separado.

### Suscripciones de paquetes de servicios
{: #service-subscriptions}

Las suscripciones a paquetes de servicios le ofrecen acceso y crédito sobre un conjunto de servicios dentro de un determinado dominio, pensados para usos comunes. Puede elegir entre paquetes de servicios que incluyen IA, analítica, {{site.data.keyword.blockchainfull_notm}}, Internet de las cosas (IoT) y servicios nativos de la nube. Si sus necesidades abarcan diversos dominios, puede adquirir varias suscripciones de paquetes de servicios.

Puede añadir paquetes de servicios a cualquier tipo de cuenta existente, incluidas las cuentas Lite. Durante los 90 primeros días, estará limitado a utilizar los servicios del paquete. Transcurridos estos primeros 90 días, podrá acceder a todo el catálogo. Las suscripciones a paquetes de servicios están sujetas a las condiciones de la [Descripción de servicios de {{site.data.keyword.Bluemix_notm}}](/docs/overview/terms-of-use?topic=overview-terms).

Las suscripciones a paquetes de servicios no están disponibles a través de la consola de {{site.data.keyword.Bluemix_notm}}. Para obtener más información y para adquirir un paquete de servicios, póngase en contacto con el [equipo de ventas de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window}.
{:tip}

Después de adquirir una suscripción a un paquete de servicios, recibirá un correo electrónico con el código de característica que debe aplicar para añadir el paquete a su cuenta. Para obtener más información sobre cómo aplicar códigos de característica, consulte el apartado sobre [Aplicación de códigos de característica](/docs/account?topic=account-codes). Cuando caduque el paquete de servicios o cuando agote todo el crédito, puede seguir utilizando cualquiera de los servicios y el uso se cargará a la tasa de pago según uso.

## Actualización de la cuenta
{: #upgrade-lite-account}

Cuando esté preparado para elevar su cuenta al siguiente nivel, puede [actualizar su cuenta Lite](/docs/account?topic=account-upgrading-account) a una cuenta de pago según uso o a una cuenta de suscripción. La actualización de la cuenta le permite explorar todo el catálogo de {{site.data.keyword.Bluemix_notm}}, le ofrece recursos gratuitos adicionales y más.

Después de actualizar su cuenta Lite a una cuenta de pago según uso, obtendrá un crédito promocional de 200 $ que se aplica automáticamente a su cuenta. El crédito de 200 dólares es válido durante 30 días y el uso de resta automáticamente del importe del crédito. El crédito no puede utilizarse con ofertas de terceros y es posible que no esté disponible para todas las cuentas.

Si ya tiene una cuenta de pago según uso o de suscripción, también puede convertir su cuenta en una de otro tipo. Para obtener más información, consulte [Actualización de la cuenta](/docs/account?topic=account-upgrading-account).
