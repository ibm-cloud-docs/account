---

copyright:

  years: 2015, 2018
lastupdated: "2018-05-08"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Tipos de cuentas
{: #accounts}

Puede empezar a crear en {{site.data.keyword.Bluemix}} gratis. Tenemos tres tipos de cuenta diferentes entre los que puede elegir: Lite, Pago según uso y Suscripción. Puede utilizar cualquier tipo de cuenta para empezar en {{site.data.keyword.Bluemix_notm}}, elija aquel que se adapte mejor a sus necesidades.
{:shortdesc}

## Comparación de cuentas
{: #compare}

La siguiente tabla proporciona una comparación de las cuentas Lite, Pago según uso y Suscripción. Para obtener más detalles acerca de cada cuenta, consulte las siguientes secciones.

|  | Lite  | Pago según uso | Suscripción |
|--------------------|--------------------|--------------------|--------------------|
| **Acceso a memoria de Cloud Foundry gratuita** | 256 MB | 512 MB | 512 MB |
| **Acceso a [planes de servicio Lite ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/catalog/?search=label:lite){: new_window}** | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
| **Acceso a todos los planes gratuitos** |  | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
| **Acceso al catálogo completo** |  | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
| **Acceso a varias regiones de Cloud Foundry** |  | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
| **Sin restricciones de tiempo** | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
| **Coste cero garantizado** | ![Característica disponible](../icons/icon_enabled.svg) |  |  |
| **Descuentos en los precios** |  |  | ![Característica disponible](../icons/icon_enabled.svg) |
| **Adecuado para aprender o crear pruebas de conceptos** | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |  |
| **Ajuste para casos de uso de producción** |  | ![Característica disponible](../icons/icon_enabled.svg) | ![Característica disponible](../icons/icon_enabled.svg) |
{: caption="Tabla 1. Comparación de cuentas de {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Cuenta Lite
{: #liteaccount}

Registrarse para una cuenta Lite gratuita para crear apps y explorar servicios con planes gratuitos seleccionados llamados Lite y que se muestran con la etiqueta Lite ![Etiqueta Lite](../icons/Lite.svg) en la consola de {{site.data.keyword.Bluemix_notm}}. Su cuenta Lite no caduca y la tarjeta de crédito no es necesaria.

Tiene acceso a un único grupo de recursos creado para usted y llamado `Default`. Todas sus instancias de servicio gestionadas por la Gestión de identidad y acceso de {{site.data.keyword.Bluemix_notm}} (IAM) se añaden automáticamente a este grupo de recursos. Puede actualizar en nombre de este grupo de recursos en cualquier momento. Consulte [Cómo renombrar un grupo de recursos](/docs/account/resourcegroups.html#renaming-a-resource-group) para obtener los pasos detallados.

Cada grupo de recursos es gratuito. Cuando crea una conexión entre un servicio gestionado por IAM y una app de Cloud Foundry, crea un alias, que es una instancia de servicio que cuenta en el cálculo de su cuota. Consulte [¿Qué es un alias?](/docs/cfapps/connecting_apps.html#what_is_alias)
{: tip}

### ¿Qué hay disponible?

Se estará preguntando qué se ofrece en una cuenta Lite. Consulte la siguiente lista con las características principales:

   * La cuenta es gratuita. No necesita tarjeta de crédito.
   * La cuenta no caduca nunca.
   * Puede utilizar una organización en una región de {{site.data.keyword.Bluemix_notm}}.
   * Soporte básico de {{site.data.keyword.Bluemix_notm}} de forma gratuita. El soporte básico se proporciona para entornos de no producción o cargas de trabajo donde las gravedades tradicionales no se utilizan y los tiempos de respuesta específicos no están estipulados.
   * Recibirá notificaciones de correo electrónico sobre el estado de la cuenta y los límites de la cuota.
   * Sus apps de Cloud Foundry pueden acceder hasta un máximo de 256 MB de memoria de tiempo de ejecución gratuita e instantánea.
   * Puede suministrar una instancia de cualquier servicio en el [catálogo de {{site.data.keyword.Bluemix_notm}}![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window} que tenga un plan Lite.
   * Después de 10 días de inactividad de desarrollo, sus apps entrarán en suspensión. Puede empezar a trabajar en apps nuevas sin tener que preocuparse por llegar a los límites de cuota de memoria.
   * Después de 30 días de inactividad de desarrollo, se suprimirán las instancias de servicio con planes Lite. De esta forma, no tiene que preocuparse de la supresión de instancias inactivas antes de crear nuevas.

### Actualización de la cuenta

Cuando esté preparado para crecer, actualice a una cuenta de pago según uso y pague sólo por lo que utilice más allá de las concesiones gratuitas. Después de la actualización, puede continuar utilizando las instancias que ha creado con su cuenta Lite. Vaya a **Gestionar** > **Facturación y utilización ** > **Facturación** en la consola y pulse **Añadir tarjeta de crédito**. 

## Cuentas facturables
{: #billableacts}

En la tabla siguiente se muestran los distintos tipos de cuentas y los métodos de cargos.

|Tipo de cuenta |	¿Cómo se me facturará? |
|------------------|-----------------------|
|Pago según uso |	Los cargos son en función del uso del cálculo y los servicios de {{site.data.keyword.Bluemix_notm}}. |
|Suscripción | Puede obtener un descuento mensual en función del compromiso de gasto mensual mínimo |
| {{site.data.keyword.Bluemix_dedicated_notm}} | Contrato anual |
|{{site.data.keyword.Bluemix_local_notm}} |	Contrato anual |
{:caption="Tabla 2. Cuentas facturables y cargos de {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

Si enlaza su cuenta facturable de {{site.data.keyword.Bluemix_notm}} con una cuenta de SoftLayer, a partir del día 1 del próximo mes, los cargos combinados están incluidos en su factura de {{site.data.keyword.Bluemix_notm}}. Para obtener más información, consulte [Visualización de cargos](/docs/billing-usage/viewing_usage.html#credits).
{: tip}

### Cuenta de Pago según uso

Con una cuenta de Pago según uso, puede crear varios grupos de recursos para gestionar fácilmente la cuota y ver el uso de facturación de un conjunto de recursos. Puede optar a concesiones de tiempo de ejecución y de servicio gratuitas. Si utiliza más que la concesión gratuita, recibirá una factura mensual de {{site.data.keyword.Bluemix_notm}}. La factura estará en dólares de Estados Unidos (USD) y detallará los cargos de recursos.

En muchos países y regiones, puede registrarse para una cuenta Pago según uso desde la consola de {{site.data.keyword.Bluemix_notm}}. Tras proporcionar la información de la tarjeta de crédito y la facturación, aceptar los términos y condiciones y enviar una solicitud de cuenta. A continuación, se validará su tarjeta de crédito. También recibirá un correo electrónico de confirmación sobre la información de la cuenta. Transcurridos algunos minutos tras la recepción del correo electrónico de confirmación, puede volver a la consola para continuar creando sus apps. 

Si no se puede procesar su solicitud en línea para su país o región, póngase en contacto con el equipo de [{{site.data.keyword.Bluemix_notm}} Soporte](https://ibm.biz/bluemixsupport){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg). Después de iniciar sesión en el portal de servicio de {{site.data.keyword.Bluemix_notm}}, pulse **Póngase en contacto con soporte** y seleccione la opción **Facturación, Cuenta o Iniciar sesión**.

Puede convertir la cuenta Pago según uso en una cuenta Suscripción en cualquier momento. Póngase en contacto con el [equipo de ventas de {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg) para obtener más detalles.
{: tip}

### Cuenta de Suscripción

Con una cuenta de Suscripción, puede crear varios grupos de recursos para gestionar fácilmente la cuota y ver el uso de facturación de un conjunto de recursos.

Se compromete a una cantidad de gasto mínimo al mes y recibirá un descuento de suscripción que se aplicará a dicho cargo mínimo. También puede pagar cualquier uso que exceda la cantidad de gasto mínimo.

Para registrarse con una cuenta de Suscripción, y para obtener más información sobre las tarifas y descuentos de la suscripción, póngase en contacto con [el equipo de ventas de {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg).

### Cuenta de {{site.data.keyword.Bluemix_dedicated_notm}}

Con {{site.data.keyword.Bluemix_dedicated_notm}}, debe registrarse para un plazo mínimo de un año que incluye:

   * Conectividad VPN para volver a su infraestructura
   * Entorno completo y redundante en un centro de datos de {{site.data.keyword.BluSoftLayer_notm}}
   * Todos los tiempos de ejecución soportados (IBM Java Liberty, Node.js y ejecuciones de código abierto)
   * Todos los servicios dedicados que ha seleccionado y todos los servicios públicos de {{site.data.keyword.Bluemix_notm}}
   * Soporte de {{site.data.keyword.Bluemix_notm}} estándar

También puede pedir elementos opcionales como
SoftLayer DirectLink u opciones de soporte premium. Póngase en contacto con el [equipo de ventas de {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg) para obtener más información.

Lo que deberá abonar cada mes durante dicho plazo dependerá de los servicios dedicados que desee, más una cuenta de suscripción que le ofrece acceso a todos los servicios públicos. Los cargos por uso de los servicios de {{site.data.keyword.Bluemix_notm}} público se calculan en función del acuerdo de la cuenta de suscripción. Recibirá una factura correspondiente a los servicios que utilice por encima del acuerdo de suscripción. Póngase en contacto con su representante de cuenta designado de IBM o con el [equipo de ventas de {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg) para empezar a trabajar en su acuerdo.

### Cuenta de {{site.data.keyword.Bluemix_local_notm}}

Con {{site.data.keyword.Bluemix_local_notm}}, debe registrarse para un plazo mínimo de un año que incluye:

   * Una función de entrega denominada retransmisión que permite a IBM conectarse a su despliegue local y entregar actualizaciones de forma automática y coherente.
   * Todos los tiempos de ejecución soportados (IBM Java Liberty, Node.js y ejecuciones de código abierto)
   * Todos los servicios locales que ha seleccionado y acceso a todos los servicios públicos de {{site.data.keyword.Bluemix_notm}}
   * Soporte de {{site.data.keyword.Bluemix_notm}} estándar

Lo que deberá abonar cada mes durante dicho plazo dependerá de los servicios locales que desee, más una cuenta de suscripción que le ofrece acceso a todos los servicios públicos. Los cargos por uso de los servicios de {{site.data.keyword.Bluemix_notm}} público se calculan en función del acuerdo de la cuenta de suscripción. Recibirá una factura correspondiente a los servicios que utilice por encima del acuerdo de suscripción. Póngase en contacto con su representante de cuenta designado de IBM o con el [equipo de ventas de {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg) para empezar a trabajar en su acuerdo.

## Cuenta de prueba
{: #trial}

Las cuentas de prueba están disponibles en todas las regiones. Con una prueba de 30 días, ya puede empezar a crear sus apps y a explorar los servicios de {{site.data.keyword.Bluemix_notm}}.

Al registrarse para una prueba gratuita con su ID de {{site.data.keyword.Bluemix_notm}}, se le proporciona una cuenta con los siguientes recursos gratuitos:

  * Un máximo de 2 GB de memoria
  * 10 servicios
  * 1 certificado SSL

También tiene acceso a un único grupo de recursos creado para usted y llamado `Default`. Todas sus instancias de servicio gestionadas por IAM se añaden automáticamente a este grupo de recursos. Puede actualizar en nombre de este grupo de recursos en cualquier momento. Consulte [Cómo renombrar un grupo de recursos](/docs/account/resourcegroups.html#renaming-a-resource-group) para obtener los pasos detallados.

Cada grupo de recursos es gratuito. Cuando crea una conexión entre un servicio gestionado por IAM y una app de Cloud Foundry, crea un alias, que es una instancia de servicio que cuenta en el cálculo de su cuota. Consulte [¿Qué es un alias?](/docs/cfapps/connecting_apps.html#what_is_alias)
{: tip}

### ¿Qué ocurre cuando mi prueba gratuita finaliza?
{: #trialend}

Cuando el período de prueba gratuito vence 30 días después de registrarse, las apps de su cuenta se detienen. No podrá registrarse para otra cuenta de {{site.data.keyword.Bluemix_notm}}, pero podrá seguir accediendo a su cuenta y a las cuentas en las que ha sido invitado.

Para reiniciar sus apps, convierta su cuenta en una cuenta facturable proporcionando la información de su tarjeta de crédito para una cuenta de pago según uso o creando una cuenta de Suscripción. Puede continuar utilizando concesiones y servicio gratuitos. Sólo pagará por el uso de servicios, contenedores y tiempos de ejecución que no están incluidos en la concesión mensual gratuita.

  * Para actualizar a una cuenta de Pago según uso, vaya a **Gestionar** > **Facturación y utilización ** > **Facturación** en la consola y pulse **Añadir tarjeta de crédito**.
  * Para registrarse con una cuenta de Suscripción, póngase en contacto con [el equipo de ventas de {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg).

Si no convierte su cuenta una vez haya vencido el período de prueba gratuita, sus apps y servicios se eliminarán después de 30 días. Sin embargo, la cuenta no se suprime y puede iniciar sesión y actualizar a una cuenta facturable en cualquier momento. También, recibirá notificaciones de correo electrónico para recordarle que debe crear una cuenta facturable y evitar perder los valores de su app y la configuración de los servicios. Si prefiere no recibir notificaciones de {{site.data.keyword.Bluemix_notm}}, puede anular la suscripción en cualquier momento.

Si convierte la cuenta, las concesiones gratuitas se verán limitadas a concesiones proporcionadas normalmente por cada servicio. Las concesiones ya no son concesiones de uso ilimitado que ofrecen muchos de los servicios de IBM durante el periodo de prueba gratuito.

