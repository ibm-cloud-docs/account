---

copyright:

  years: 2015, 2019
lastupdated: "2019-02-13"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

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
{: caption="Tabla 1. Comparación de cuentas de {{site.data.keyword.Bluemix_notm}}" caption-side="top"}


## Cuenta Lite
{: #liteaccount}

Regístrese para una cuenta Lite para empezar a crear sus apps y explorar servicios con planes Lite gratuitos seleccionados, que se muestran con una etiqueta Lite ![etiqueta Lite](../icons/Lite.svg) en la consola de {{site.data.keyword.Bluemix_notm}}. Su cuenta Lite no caduca y la tarjeta de crédito no es necesaria.

Tiene acceso a un único grupo de recursos creado para usted y llamado `Default`. Todas las instancias de su servicio gestionadas por la Gestión de identidad y acceso de {{site.data.keyword.Bluemix_notm}} (IAM) se añaden automáticamente a este grupo de recursos. Puede actualizar en nombre de este grupo de recursos en cualquier momento. Consulte [Cómo renombrar un grupo de recursos](/docs/resources?topic=resources-rgs#rename_rgs) para obtener los pasos detallados.

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
   * Sus apps de Cloud Foundry pueden acceder hasta un máximo de 256 MB de memoria de tiempo de ejecución gratuita e instantánea.
   * Puede suministrar una instancia de cualquier servicio en el [catálogo de {{site.data.keyword.Bluemix_notm}} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://cloud.ibm.com/catalog/?search=label:lite%20lite){: new_window} que tiene el plan Lite.
   * Después de 10 días de inactividad de desarrollo, sus apps entrarán en suspensión. Puede activar sus apps si continúa trabajando con las mismas.
   * Después de 30 días de inactividad de desarrollo, se suprimirán las instancias de servicio con planes Lite.

### Actualización de la cuenta Lite
{: #upgrade-lite-account}

Puede actualizar a una cuenta de Pago según uso o Suscripción. Para obtener más información, consulte [¿Cómo puedo actualizar o convertir mi tipo de cuenta?](/docs/account?topic=account-changeacct).

Obtendrá un crédito promocional de 200 dólares después de actualizar una cuenta de Pago según uso y el crédito se aplica automáticamente a su cuenta. Su crédito de 200 dólares es válido durante 30 días y se aplica automáticamente a su factura. El crédito no puede utilizarse con ofertas de terceros.

## Cuenta de Pago según uso
{: #paygo}

Con una cuenta de Pago según uso, puede crear varios grupos de recursos para gestionar fácilmente la cuota y ver el uso de facturación de un conjunto de recursos. Los cargos son en función del uso del cálculo y los servicios de {{site.data.keyword.Bluemix_notm}}. Puede optar a concesiones de tiempo de ejecución y de servicio gratuitas. Si utiliza más que la concesión gratuita, recibirá una factura mensual de {{site.data.keyword.Bluemix_notm}}. La factura está en dólares de Estados Unidos (USD) y proporciona detalles sobre los cargos de recursos.

Además, con una cuenta de Pago según uso puede pedir elementos opcionales como, por ejemplo, opciones de soporte avanzadas o premium. Póngase en contacto con el [equipo de ventas de {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg) para obtener más información.


### Actualización de la cuenta Pago según uso
{: #upgrade-to-subscription}

Para actualizar su cuenta de Pago según uso a una cuenta de Suscripción, póngase en contacto con el [equipo de ventas de {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo").

## Cuenta de Suscripción
{: #subscription-account}

Con una cuenta de Suscripción, puede crear varios grupos de recursos para gestionar fácilmente la cuota y ver el uso de facturación de un conjunto de recursos. Se compromete a una cantidad de gasto mínimo combinada al mes y recibirá un descuento de suscripción que se aplicará a dicho cargo mínimo. Se le cobrará la tarifa sin descuento para cualquier uso que supere la cantidad total de Suscripción. Para ver su suscripción, vaya a **Gestionar > Facturación y uso** y seleccione **Suscripciones**.

Si tiene una cuenta de suscripción, puede crear la mayoría de los servicios que están disponibles en el [catálogo de {{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com/catalog/){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo"). Sin embargo, algunos servicios utilizan un plan de precios específicos que requiere que se adquieran por separado.

### {{site.data.keyword.Bluemix_dedicated_notm}} account
Con {{site.data.keyword.Bluemix_dedicated_notm}}, debe registrarse para un plazo mínimo de un año que incluye:

   * Conectividad VPN para volver a su infraestructura
   * Entorno completo y redundante en un centro de datos de {{site.data.keyword.BluSoftlayer_notm}}
   * Todos los tiempos de ejecución soportados ({{site.data.keyword.runtime_liberty_short}}, {{site.data.keyword.runtime_nodejs_short}} y ejecuciones de código abierto)
   * Todos los servicios dedicados que ha seleccionado y todos los servicios públicos de {{site.data.keyword.Bluemix_notm}}
   * Soporte de {{site.data.keyword.Bluemix_notm}} estándar

También puede pedir elementos opcionales como {{site.data.keyword.BluDirectLink}} u opciones de soporte avanzado o premium. Póngase en contacto con el [equipo de ventas de {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg) para obtener más información.

Lo que deberá abonar cada mes durante dicho plazo dependerá de los servicios dedicados que desee, más una cuenta de suscripción que le ofrece acceso a todos los servicios públicos. Los cargos por uso de los servicios de {{site.data.keyword.Bluemix_notm}} público se calculan en función del acuerdo de la cuenta de suscripción. Recibirá una factura correspondiente a los servicios que utilice por encima del acuerdo de suscripción. Póngase en contacto con su representante de cuenta designado de IBM o con el [equipo de ventas de {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg) para empezar a trabajar en su acuerdo.
