---

copyright:
  years: 2019
lastupdated: "2019-07-01"

keywords: VRF, virtual routing and forwarding, service endpoint, private network

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Habilitación de VRF y de puntos finales de servicio
{: #vrf-service-endpoint}

De forma predeterminada, se conecta a los recursos de la cuenta a través de la red pública de {{site.data.keyword.Bluemix}}. Puede habilitar el direccionamiento y el reenvío virtuales (VRF) para mover el direccionamiento de IP de la cuenta y de todos sus recursos a una tabla de direccionamiento independiente. Si VRF está habilitado, luego puede habilitar puntos finales de servicio de {{site.data.keyword.Bluemix_notm}} para conectarse directamente a los recursos sin utilizar la red pública.
{:shortdesc}

Para habilitar el direccionamiento y el reenvío virtuales y el punto final de servicio de {{site.data.keyword.Bluemix_notm}}, necesita una cuenta facturable.

## Habilitación de VRF
{: #vrf}

VRF permite que existan varias instancias de una tabla de direccionamiento en un direccionador y que funcionen simultáneamente. Cuando se habilita VRF, se crea una tabla de direccionamiento independiente para la cuenta, y las conexiones procedentes de los recursos de la cuenta y destinados al mismo se direccionan por separado en la red de {{site.data.keyword.Bluemix_notm}}. VRF se habilita a nivel de cuenta, de modo que todos los recursos se ven afectados por este cambio de red. Para obtener más información sobre la tecnología VRF y sobre cómo afecta el direccionamiento de red de su cuenta, consulte [Direccionamiento y reenvío virtuales en {{site.data.keyword.Bluemix_notm}}](/docs/resources?topic=direct-link-overview-of-virtual-routing-and-forwarding-vrf-on-ibm-cloud).

La habilitación de VRF altera de forma permanente la red de su cuenta. Asegúrese de comprender el impacto en la cuenta y en los recursos. Después de habilitar VRF, no se puede inhabilitar.
{: important}

Para habilitar VRF, cree un caso de soporte con su solicitud.

1. En la consola, vaya a **Soporte** y pulse **Crear un caso**.
1. Seleccione **Cuenta y acceso** como tipo de soporte.
1. En el campo **Asunto**, especifique `Pregunta de red privada`.
1. En el campo **Descripción**, especifique el mensaje siguiente y sustituya _especifique el número de cuenta_ por su número de cuenta de {{site.data.keyword.Bluemix_notm}}.

   `Solicitamos que la cuenta *especifique el número de cuenta* se mueva a su propio VRF. Comprendemos los riesgos y aprobamos el cambio. Responda con las ventanas de tiempo planificadas que las que se realizará este cambio para que podamos prepararnos para la migración.`

El equipo de ingeniería de red de {{site.data.keyword.Bluemix_notm}} se pondrá en contacto con el propietario del caso para planificar el periodo de tiempo en que la red de su cuenta se convertirá a VRF. Durante el proceso de conversión, las conexiones con los recursos de la cuenta podrían ser inestables debido a la pérdida de paquetes. La conversión tarda aproximadamente entre 15 y 30 minutos, dependiendo de la complejidad de su cuenta. Si su cuenta tiene conexiones {{site.data.keyword.BluDirectLink}} antiguas, podría tomar más tiempo.


## Habilitación de puntos finales de servicio
{: #service-endpoint}

Cuando los puntos finales de servicio de {{site.data.keyword.Bluemix_notm}} están habilitados en su cuenta, puede optar por exponer un punto final de red privado cuando cree un recurso. Luego puede conectarse directamente con este punto final a través de la red privada de {{site.data.keyword.Bluemix_notm}} en lugar de utilizar la red pública. Debido a que los recursos que utilizan puntos finales de red privada no tienen una dirección IP direccionable a Internet, las conexiones con estos recursos son más seguras. Para obtener más información, consulte [Puntos finales de servicio para conexiones de red privada](/docs/resources?topic=resources-service-endpoints).

Para poder habilitar los puntos finales de servicio, VRF debe estar habilitado en su cuenta.
{: note}

Para habilitar los puntos finales de servicio desde la CLI, necesita la versión 0.13 o posterior de la [CLI de {{site.data.keyword.Bluemix_notm}}](/docs/cli?topic=cloud-cli-getting-started).

1.  Compruebe si los puntos finales de servicio ya están habilitados en la cuenta.

    ```
    ibmcloud account show
    ```
    {: codeblock}

    Si el valor de `Service Endpoint Enabled` es `false`, tal como se muestra en el siguiente ejemplo, significa que los puntos finales de servicio no están habilitados.

    ```
    Retrieving account Mia Example's Account of m.example@example.com...
    OK

    Account ID:                   abc123d0bc2edefthyufffc9b5ca318   
    Currently Targeted Account:   true   
    Linked Softlayer Account:     0123456   
    Service Endpoint Enabled:     false  
    ```
    {: screen}
1. Habilite los puntos finales de servicio con el mandato siguiente.

   ```
   ibmcloud account update --service-endpoint-enable true
   ```
   {: codeblock}

   Este cambio puede tardar unos minutos en entrar en vigor. Una vez completado el mandato, puede volver a ejecutar el mandato `ibmcloud account show` para verificarlo.

    Si VRF no está habilitado para la cuenta, cuando ejecute este mandato se le solicitará que cree un caso para habilitarlo. Escriba `s` para crear el caso de soporte. Después de que se habilite VRF en la cuenta, vuelva a ejecutar el mandato para habilitar la conectividad de punto final de servicio en la cuenta.

    ```
    El punto final de servicio no está habilitado en la cuenta de Softlayer enlazada 1008967.
    Habilite primero VRF (Virtual Routing and Forwarding) para continuar.
    Aquí encontrará más información sobre VRF: https://cloud.ibm.com/docs/infrastructure/direct-link/vrf-on-ibm-cloud.html.

    ¿Desea abrir una incidencia para habilitarlo? [s/N]> s
    La incidencia 70729615 se ha abierto correctamente. Siga el enlace https://control.softlayer.com/support/tickets/70729876 para comprobar los detalles y realizar un seguimiento del estado de la incidencia. Tendrá que iniciar una sesión para ver esta incidencia.
    ID de cuenta:    1008967
    Incidencia:      Pregunta de red privada
    ```
    {: screen}


Después de que se habiliten los puntos finales de servicio, puede crear recursos que se conecten a través de la red privada de {{site.data.keyword.Bluemix_notm}}. Para obtener una lista de los servicios que dan soporte a puntos finales de servicio y más información, consulte [Configuración de puntos finales de red privada](/docs/resources?topic=resources-private-network-endpoints).
