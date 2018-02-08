---



copyright:

  years: 2015, 2018
lastupdated: "2018-01-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Enlace sus cuentas de {{site.data.keyword.Bluemix_notm}} y SoftLayer
{: #unifyingaccounts}

Puede enlazar las cuentas de {{site.data.keyword.Bluemix}} y SoftLayer para hacer uso de los recursos combinados. 
{: shortdesc}

Cuando enlace las cuentas de {{site.data.keyword.Bluemix_notm}} y Softlayer, recibirá una factura única de {{site.data.keyword.Bluemix_notm}}. Si tiene una cuenta de {{site.data.keyword.Bluemix_notm}}, la facturación a través de {{site.data.keyword.Bluemix_notm}} para los recursos de infraestructura será efectiva para el nuevo ciclo de facturación que empieza una vez que se hayan enlazado las cuentas.

Todas las cuentas vinculadas en {{site.data.keyword.Bluemix_notm}} deben ser cuentas de Pago según uso. Puede crear una nueva cuenta de Pago según uso, enlazar a una cuenta de Pago según uso existente o enlazar con una cuenta de prueba existente, que se actualizará a una cuenta de Pago según uso. No puede enlazar las cuentas de Suscripción.
{: tip}

Para enlazar cuentas debe ser un usuario maestro en la cuenta de Softlayer.

Cuando se enlacen sus cuentas:

* Debe utilizar las credenciales de ID de IBM para acceder a sus cuentas tanto de SoftLayer como de {{site.data.keyword.Bluemix_notm}}.
* Cualquier descuento existente de SoftLayer se aplicará en cargos de {{site.data.keyword.Bluemix_notm}}.
* Recibirá una factura en dólares de Estados Unidos (USD).
* Puede supervisar el uso de los recursos de infraestructura en la consola de {{site.data.keyword.Bluemix_notm}}.

Después de enlazar sus cuentas, no podrá desenlazarlas.  

Como usuario maestro, complete los siguientes pasos para enlazar sus cuentas de {{site.data.keyword.Bluemix_notm}} y SoftLayer:

 1. Desde el Portal de cliente de {{site.data.keyword.Bluemix_notm}}, pulse **Enlazar a una cuenta de {{site.data.keyword.Bluemix_notm}}**.
 2. Lea y acepte las condiciones para enlazar cuentas de SoftLayer y {{site.data.keyword.Bluemix_notm}}.
 3. Cuando se le solicite, proporcione la dirección de correo electrónico asociada con su cuenta de {{site.data.keyword.Bluemix_notm}}. Si no tiene cuenta de {{site.data.keyword.Bluemix_notm}}, especifique la dirección de correo electrónico que desea utilizar, siga las instrucciones para ser invitado a {{site.data.keyword.Bluemix_notm}} y cree una cuenta.

Después de enlazar sus cuentas, **Ir a {{site.data.keyword.Bluemix_notm}}** estará disponible en la barra de menús de la consola de SoftLayer. Al hacer clic en este enlace, accederá a la página de inicio de sesión de {{site.data.keyword.Bluemix_notm}}.

## Facturación para el uso de {{site.data.keyword.Bluemix_notm}} cuando las cuentas están enlazadas
{: #linkedbilling}

Una vez que haya enlazado sus cuentas de facturación de {{site.data.keyword.Bluemix_notm}} y SoftLayer, el siguiente ciclo de facturación se cargará en una única factura de {{site.data.keyword.Bluemix_notm}}.

El ciclo de uso de {{site.data.keyword.Bluemix_notm}} se basa en meses naturales, por lo que la cuenta se factura cada mes el día de facturación que se estableció para su acuerdo de cargo. Con SoftLayer, el ciclo de uso empieza al empezar a utilizar SoftLayer, por lo que la facturación es cada mes, el día en el que se registró para la cuenta de SoftLayer. 

Cuando las cuentas están enlazadas, el uso de {{site.data.keyword.Bluemix_notm}} seguirá midiéndose para el ciclo mensual actual y dicho uso se facturará en una factura de {{site.data.keyword.Bluemix_notm}}. A partir del día 1 del siguiente mes, los cargos de {{site.data.keyword.Bluemix_notm}} y SoftLayer se combinarán en la factura de {{site.data.keyword.Bluemix_notm}}.

Por ejemplo, si enlazó las cuentas el 16 de abril de 2017, recibirá una factura de {{site.data.keyword.Bluemix_notm}} para su uso de abril. Según cuándo haya enlazado las cuentas, podrá obtener una factura independiente para el uso de SoftLayer. A continuación, el uso combinado durante mayo se facturará mediante su cuenta de {{site.data.keyword.Bluemix_notm}}.

![Resumen del enlace de cuentas de IBM Cloud y SoftLayer](images/IBMCloudSoftLayerBill.svg)

Una vez que se enlacen las facturas, la factura de {{site.data.keyword.Bluemix_notm}} listará los distintos cargos para cada recurso que haya utilizado.

## Servicios de {{site.data.keyword.Bluemix_notm}} basados en API
{: #api-based-services}

En la siguiente lista encontrará los servicios que puede configurar para ejecutarlos con su código de aplicación. No todos los planes para estos servicios están disponibles para su utilización con cuentas enlazadas. Para utilizar con las cuentas enlazadas, solo están disponibles los planes habilitados para cuentas Pago según uso. Sin embargo, si tiene una cuenta de {{site.data.keyword.Bluemix_notm}} separada que también se factura de forma separada, puede utilizar cualquier plan para cualquiera de estos servicios.

* {{site.data.keyword.alchemyapishort}}
* {{site.data.keyword.alertnotificationshort}}
* {{site.data.keyword.sparks}}
* {{site.data.keyword.appseccloudshort}}
* {{site.data.keyword.blockchain}}
* {{site.data.keyword.cloudant}}
* {{site.data.keyword.conceptinsightsshort}}
* {{site.data.keyword.iotmapinsights_short}}
* {{site.data.keyword.dashdbshort}}
* {{site.data.keyword.dialogshort}}
* {{site.data.keyword.documentconversionshort}}
* {{site.data.keyword.twittershort}}
* {{site.data.keyword.weather_short}}
* {{site.data.keyword.iotdriverinsights_short}}
* {{site.data.keyword.geospatialshort_Geospatial}}
* {{site.data.keyword.graphshort}}
* {{site.data.keyword.iotelectronics}}
* {{site.data.keyword.languagetranslationshort}}
* {{site.data.keyword.messagehub}}
* {{site.data.keyword.mqa}}
* {{site.data.keyword.mobileappbuilder_short}}
* {{site.data.keyword.mql}}
* {{site.data.keyword.nlclassifiershort}}
* {{site.data.keyword.objectstorageshort}}
* {{site.data.keyword.personalityinsightsshort}}
* {{site.data.keyword.presenceinsightsshort}}
* {{site.data.keyword.relationshipextractionshort}}
* {{site.data.keyword.retrieveandrankshort}}
* {{site.data.keyword.servicediscoveryshort}}
* {{site.data.keyword.speechtotextshort}}
* {{site.data.keyword.sqldb}}
* {{site.data.keyword.streaminganalyticsshort}}
* {{site.data.keyword.texttospeechshort}}
* {{site.data.keyword.toneanalyzershort}}
* {{site.data.keyword.tradeoffanalyticsshort}}
* {{site.data.keyword.visualinsightsshort}}
* {{site.data.keyword.visualrecognitionshort}}
* {{site.data.keyword.workflow}}
* {{site.data.keyword.workloadscheduler}}

