---

copyright:
  years: 2017, 2019
lastupdated: "2019-02-13"

keywords: change service, upgrade service, service plan

subcollection: account

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Cambio de planes de servicio
{: #changing}

Puede cambiar el plan de un servicio de {{site.data.keyword.Bluemix}} si los cambios de plan están habilitados para el servicio específico. Es posible que desee cambiar el plan, por ejemplo, para actualizarlo o reducirlo. Puede cambiar el plan desde el panel de control de la instancia de servicio.
{: shortdesc}

¿Desea ver información sobre cómo actualizar su tipo de cuenta? Consulte [Actualización de la cuenta](/docs/account?topic=account-upgrading-account) para obtener más información.
{: tip}

Solo puede cambiar los planes de servicio de determinados servicios. Si los cambios de plan están habilitados para el servicio, el panel de control de la instancia de servicio muestra una opción **Plan** en la navegación. Cada servicio tiene un conjunto distinto de pasos siguientes a seguir
si cambia su plan.

1. Pulse **Plan** en el panel de control de la instancia de servicio. Por lo general, puede actualizar su plan o reducirlo.
2. Después de cambiar el plan, debe completar unos pasos adicionales. Los pasos varían según el tipo de cambio
de plan y del servicio. Por ejemplo, si ha reducido su plan, es posible que tenga que volver a transferir su
app. O, si ha actualizado su plan, es posible que deba volver a transferir su app y realizar otras acciones.

   Para volver a transferir la app, vaya a la lista de recursos para buscar la app a la que está vinculado el servicio. Pulse en el icono de Menú ![icono de Menú](../icons/icon_hamburger.svg) **> Lista de recursos**. En el menú de la app, seleccione **Reiniciar app**.

  Para obtener más información sobre otras acciones necesarias, consulte la documentación del servicio.

## Cambio de un plan mediante la CLI
{: #changing_command_line}

Como alternativa a la consola, puede cambiar el plan de un servicio mediante la interfaz de línea de mandatos (CLI) de {{site.data.keyword.Bluemix_notm}}.

1. Compruebe si el servicio está habilitado con el controlador de recursos.

   ```
   ibmcloud catalog service <service_name>
   ```
   {:codeblock}

   Si el servicio está habilitado con el controlador de servicios (RC), aparecerá `RC Compatible true`. Anote el ID del plan al que quiere cambiar.

   ```
   RC Compatible      true
   RC Provisionable   true
   IAM Compatible     true
   Children   Name                      Kind         ID
              lite                      plan         4bcd3fgh-3cf2-47c0-93d4-d2f2289eac28
              standard                  plan         264d0450-996d-4bcd-894d-fc7018dacf1e
    ```

1. Cambie el plan de la instancia de servicio.

   - Si el servicio está habilitado para RC, cambie el plan con el [mandato `ibmcloud resource service-instance-update`](/docs/cli/reference/ibmcloud?topic=cloud-cli-ibmcloud_commands_resource).

     ```
     ibmcloud resource service-instance-update <service_instance_name> --service-plan-id <plan_id>
     ```
     {: codeblock}

   - Si el servicio no está habilitado para RC y, por tanto, se basa en Cloud Foundry, cambie el plan con el [mandato `ibmcloud cf update-service`](/docs/cli/reference/ibmcloud?topic=cloud-cli-cf#cf).

     ```
     ibmcloud cf update-service <service_instance_name> [-p <plan_name>]
     ```
     {:codeblock}
