---



copyright:

  years: 2017, 2018
lastupdated: "2018-07-17"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}

# Como cambiar su plan
{: #changing}

Puede cambiar su plan de servicios en {{site.data.keyword.Bluemix}} en el panel de control de la instancia de servicio si los cambios de plan están habilitados para dicho servicio.
{: shortdesc}

Consulte [¿Cómo puedo actualizar o cambiar mi tipo de cuenta?](/docs/account/account_faq.html#changeacct) si desea ver información sobre cómo actualizar su tipo de cuenta.
{: tip}

Sólo determinados servicios le proporcionan la capacidad de cambiar el plan de servicios. Si los cambios de plan están habilitados para el servicio, el panel de control de la instancia de servicio muestra una opción **Plan** en la navegación. Cada servicio tiene un conjunto distinto de pasos siguientes a seguir
si cambia su plan.

1. Para cambiar el plan, pulse **Plan** en el panel de control de la instancia de servicio. Por lo general, puede actualizar su plan o reducirlo.
2. Tras cambiar su plan, debe completar un conjunto de pasos a seguir. Los pasos varían según el tipo de cambio
de plan y del servicio. Por ejemplo, si ha reducido su plan, es posible que tenga que volver a transferir su
app. O, si ha actualizado su plan, es posible que deba volver a transferir su app y realizar otras acciones.<br/><br/>Para volver a transferir la app, vaya al panel de control de {{site.data.keyword.Bluemix_notm}} y busque la app a la que está vinculado el servicio. En el menú de la app, seleccione **Reiniciar app**.<br/><br/>Otros pasos siguientes dependen del servicio. Para acciones específicas, consulte la tabla siguiente.

|Servicio |	Información|
|--------|-------------|
|Presence Insights 	|Si tiene un plan Lite y supera el permitido gratis, se mostrará un mensaje 403 o se registra para indicar que ya no tiene autorización, y su instancia de servicio se inhabilita. Además, las llamadas POST
REST API se rechazan con la respuesta 403.<br/><br/>Si su servicio está inhabilitado porque ha excedido el periodo de permiso gratuito, puede actualizar de un plan Lite a un plan de pago. Su servicio se vuelve a habilitar en 2 horas.<br/><br/>Si tiene un plan de pago, puede reducirlo al plan Lite, siempre que su uso permanezca dentro de lo permitido en el
plan Lite para sucesos y almacenamiento total.<br/><br/>Cuando actualiza o reduce su plan, no necesita volver a transferir o reiniciar sus apps.|
{:caption="Tabla 1. Pasos siguientes para cambiar su plan" caption-side="top"}

## Cambiar su plan por medio de la interfaz de línea de mandatos
{: #changing_command_line}

Si lo prefiere, puede cambiar su plan de servicio por medio de la interfaz de línea de mandatos indicando el mandato siguiente:
```
cf update-service <nombre_servicio> [-p <plan_nuevo>]
```
