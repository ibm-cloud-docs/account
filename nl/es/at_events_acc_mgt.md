---

copyright:
  years: 2016, 2018

lastupdated: "2018-10-31"

---

{:new_window: target="_blank"}
{:shortdesc: .shortdesc}
{:screen: .screen}
{:pre: .pre}
{:table: .aria-labeledby="caption"}
{:codeblock: .codeblock}
{:tip: .tip}
{:download: .download}


# Sucesos de {{site.data.keyword.cloudaccesstrailshort}}  
{: #at_events}

Como agente de seguridad, auditor o gestor, puede utilizar el servicio {{site.data.keyword.cloudaccesstrailfull}} para realizar un seguimiento de cómo interactúan los usuarios y las aplicaciones con la cuenta de {{site.data.keyword.Bluemix}}. 
{:shortdesc}

Por ejemplo, cuando un usuario o aplicación inicia sesión en
{{site.data.keyword.Bluemix_notm}} utilizando una contraseña, una clave de API y un código de autenticación o un código de acceso, se genera un suceso de {{site.data.keyword.cloudaccesstrailshort}} para cada intento. 

El servicio {{site.data.keyword.cloudaccesstrailfull_notm}} registra las actividades iniciadas por el usuario que cambian el estado de un servicio en {{site.data.keyword.Bluemix_notm}}. Para obtener más información, consulte [Acerca de {{site.data.keyword.cloudaccesstrailshort}}](/docs/services/cloud-activity-tracker/activity_tracker_ov.html#activity_tracker_ov ).

Para empezar a supervisar las acciones del usuario, consulte [{{site.data.keyword.cloudaccesstrailfull_notm}}](/docs/services/cloud-activity-tracker/index.html#getting-started-with-cla). 

## Sucesos para gestionar cuentas
{: #account}

En la tabla siguiente se muestran el método de API que genera un suceso cuando se le llama:

<table>
  <caption>Acciones que generan sucesos</caption>
  <tr>
    <th>Acción</th>
	  <th>Descripción</th>
  </tr>
  <tr>
    <td>billing.account.create</td>
	  <td>Se genera un suceso cuando suministra una cuenta y después de que se asigne el ID de cuenta a la cuenta.</td>
  </tr>
  <tr>
    <td>billing.account.update</td>
	  <td>Se genera un suceso cuando se actualiza la información sobre la cuenta.</td>
  </tr>
  <tr>
    <td>billing.account.active</td>
	  <td>Se genera un suceso cuando verifica la cuenta o cuando la cuenta pasa al estado activo.</td>
  </tr>
  <tr>
    <td>billing.account.subscription.create</td>
	  <td>Se genera un suceso cuando crea una <a href="/docs/account/index.html#subscription-account">cuenta de suscripción</a>.</td>
  </tr>
</table>



## Sucesos para gestionar usuarios
{: #users}

En la tabla siguiente se muestra el método de API que genera un suceso cuando se le llama:

<table>
  <caption>Acciones que generan sucesos</caption>
  <tr>
    <th>Acción</th>
	  <th>Descripción</th>
  </tr>
  <tr>
    <td>billing.account.user.create</td>
	  <td>Se genera un suceso cuando se envía una invitación a un usuario para que se una a una cuenta. </br>El propietario de la cuenta es el único usuario de la cuenta que puede realizar esta acción.</td>
  </tr>
  <tr>
    <td>billing.user.active</td>
	  <td>Se genera un suceso cuando se activa el usuario en la cuenta. </br>Cuando el usuario verifica su dirección de correo electrónico, se genera el suceso.</td>
  </tr>
  <tr>
    <td>billing.account.user.delete</td>
	  <td>Se genera un suceso cuando se elimina un usuario de la cuenta. </br>El propietario de la cuenta es el único usuario de la cuenta que puede realizar esta acción.</td>
  </tr>
</table>

## Sucesos para gestionar organizaciones
{: #org}

En la tabla siguiente se muestra el método de API que genera un suceso cuando se le llama:

<table>
  <caption>Acción que genera sucesos</caption>
  <tr>
    <th>Acción</th>
	  <th>Descripción</th>
  </tr>
  <tr>
    <td>billing.account.org.create</td>
	  <td>Se genera un suceso cuando se añade una organización a la cuenta.</td>
  </tr>
</table>

## Dónde buscar los sucesos
{: #ui}

Los sucesos de {{site.data.keyword.cloudaccesstrailshort}} están disponibles en el
**dominio de cuenta de Dallas** de {{site.data.keyword.cloudaccesstrailshort}} que está disponible en
{{site.data.keyword.Bluemix_notm}}. Para obtener más información, consulte [Visualización de sucesos de cuenta](/docs/services/cloud-activity-tracker/how-to/manage-events-ui/viewing_events.html#account_events).

Los sucesos de {{site.data.keyword.cloudaccesstrailshort}} se reenvían automáticamente al servicio {{site.data.keyword.cloudaccesstrailshort}} en la misma región en la que se produce la acción.
