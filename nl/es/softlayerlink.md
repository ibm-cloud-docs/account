---

copyright:

  years: 2016, 2018

lastupdated: "2018-11-17"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:important: .important}
{:new_window: target="_blank"}

# Cómo cambiar a IBMid y enlazar cuentas
{: #unifyingaccounts}

Un IBMid es un ID único que utiliza para iniciar sesión en la cuenta de {{site.data.keyword.Bluemix}} para acceder a las características de infraestructura, servicios y aplicaciones, y adquirirlas. Todas las nuevas cuentas automáticamente recibirán un IBMid y las cuentas existentes de SoftLayer, excepto las cuentas federadas SAML, estarán habilitadas para conmutar a la autenticación de IBMid.
{:shortdesc}

## Cambio a IBMid
{: #switchtoIBMid}

Cuando empiece el proceso de cambiar a un IBMid, siempre podrá cancelar el proceso de cambio antes de finalizarlo. Sin embargo, cada vez que inicie una sesión, se mostrará el indicador para cambiar a un IBMid. Cada cuenta de SoftLayer que tenga previsto enlazar a una cuenta de {{site.data.keyword.Bluemix_notm}} debe ser propiedad de un IBMid único con una dirección de correo electrónico exclusiva.

Para cambiar desde su cuenta de SoftLayer existente a un IBMid, cree un IBMid y utilice el código de registro para confirmarlo.

### Solicitud de un IBMid y un código de registro
{: #reqIBMidandregcode}

1. Inicie una sesión en su cuenta de SoftLayer y pulse **Aceptar** cuando se visualice una solicitud para cambiar a un IBMid.

   Si es un usuario maestro y no ve un indicador para cambiar a un IBMid en el portal de clientes póngase en contacto con el equipo de soporte de IBM para obtener ayuda. Consulte [Obtener soporte](/docs/get-support/howtogetsupport.html#getting-customer-support) para obtener información de contacto.

   Si con anterioridad inició una sesión y pulso **Más tarde** en la solicitud, y desea cambiar a la autenticación de IBMid en la sesión actual, vaya a la página Editar perfil de usuario y pulse **Cambiar a IBMid**.

2. Siga las indicaciones del asistente para crear el IBMid.

   Especifique una dirección de correo electrónico que no utilice actualmente ningún otro IBMid. Esta dirección de correo electrónico sirve como el nombre de usuario para el nuevo IBMid, y es adónde se envía su código de registro después de que se cree su IBMid. Más tarde podrá actualizar la dirección de correo electrónico asociada al IBMid, pero no podrá cambiar el nombre de usuario.

### Confirmación del IBMid con el código de registro
{: #confIBMiduseregcode}

1. Cuando reciba el código de registro, pulse en el enlace en el correo electrónico o copie el URL en un navegador y especifique su código de registro. El código de registro es válido durante 7 días y solo se puede utilizar una vez.

2. Después de enviar su código de registro, utilice el IBMid para iniciar una sesión en el portal de clientes.

   En el indicador de inicio de sesión de la cuenta, vaya a la sección **Inicio de sesión de cuenta de IBMid** y pulse **Iniciar sesión con IBMid**. No utilice los campos el **Nombre de usuario** y **Contraseña** que ha utilizado previamente con su ID de SoftLayer.

Si es un nuevo cliente, se le solicitará su IBMid existente o que cree un nuevo IBMid al crear su pedido.
  * Para utilizar un IBMid existente, escriba el nombre de usuario o la dirección de correo electrónico del IBMid si no se comparte con varios IBMid.
  * Para crear un nuevo IBMid, escriba una dirección de correo electrónico que no utilice actualmente ningún otro IBMid. Esta dirección de correo electrónico es el nombre de usuario para el IBMid, y es adónde se enviará su código de registro después de que se cree su IBMid. Más tarde podrá actualizar la dirección de correo electrónico asociada al IBMid, pero no podrá cambiar el nombre de usuario.

Para resolver cualquier problema de inicio de sesión con su IBMid, consulte [Resolución de problemas para acceder a {{site.data.keyword.Bluemix_notm}}](/docs/account/ts_accessing.html#accessing).


## Enlace de cuentas de IBMid
{: #link_accounts}

Cuando las cuentas se hayan cambiado a cuentas de IBMid, podrá enlazar cuentas de SoftLayer y {{site.data.keyword.Bluemix_notm}} para un uso combinado de los recursos de la infraestructura como servicio (IaaS) y de la plataforma como servicio (PaaS). A continuación, podrá acceder a recursos IaaS y PaaS desde un inicio de sesión único. Enlazar sus cuentas también supondrá una única factura para todos los recursos IaaS y PaaS que utilice. Puede enlazar su propia cuenta o, si es un usuario maestro, puede enlazar sus cuentas de usuario.

### Enlace de su cuenta de IBMid
{: #link_user_account}

Si es un cliente de la infraestructura y también dispone de cuentas PaaS en {{site.data.keyword.Bluemix_notm}} o las crea, puede enlazar IaaS y PaaS para obtener una vista única de sus cuentas. Para enlazar las cuentas, siga estos pasos:
1. Inicie sesión en su cuenta de SoftLayer.
2. En la página Resumen de la cuenta, pulse **Nuevo. Enlazar una cuenta de Bluemix**.
3. Revise las condiciones de uso y pulse para aceptarlas.
4. Complete uno de los pasos finales siguientes, en función de cómo está configurada su cuenta:
  * Si tiene una cuenta de {{site.data.keyword.Bluemix_notm}} asociada a su IBMid, se le direccionará a una página de autorización, y luego al paso de confirmación final.
  * Si no tiene una cuenta de {{site.data.keyword.Bluemix_notm}} asociada, se le solicitará que cree una nueva.

Para ver preguntas y respuestas comunes acerca de su cuenta, consulte [Preguntas frecuentes](/docs/account/account_faq.html#al_login).

### Cómo enlazar cuentas de usuario de IBMid
{: #link_customer_accounts}

Cuando sus cuentas de usuario se hayan cambiado a la autenticación de IBMid, los concesionarios y distribuidores podrán enlazar sus cuentas de usuario. Para enlazar cuentas de usuario debe ser un usuario maestro de SoftLayer. El IBMid que es el usuario maestro de la cuenta debe ser el propietario de la cuenta de la plataforma {{site.data.keyword.Bluemix_notm}} a la que se va a enlazar. 

Después de enlazar sus cuentas, no podrá desenlazarlas.
{: note}

Asegúrese de revisar las siguientes notas importantes para enlazar cuentas:

  * El usuario maestro de la cuenta de SoftLayer a la que se está enlazando debe tener un IBMid.
  * Cada cuenta de usuario que enlace con una cuenta de {{site.data.keyword.Bluemix_notm}} debe ser propiedad de un IBMid exclusivo con una dirección de correo electrónico exclusiva. A pesar de que un único IBMid puede poseer varias cuentas de SoftLayer, debe cambiar el usuario maestro para que sea un IBMid exclusivo para cada cuenta. Póngase en contacto con el equipo de soporte para cambiar el usuario maestro de una cuenta de SoftLayer. Consulte [Obtención de soporte para la infraestructura de {{site.data.keyword.Bluemix_notm}}](/docs/customer-portal/cpsupport.html) para obtener más información.
  * Cuando añada nuevos usuarios a una cuenta enlazada, debe añadirlos tanto a la cuenta de SoftLayer como a la cuenta de {{site.data.keyword.Bluemix_notm}} de forma que puedan acceder a todas las funcionalidades de la consola unificada.
  * Si tiene una cuenta derivada, utilice BAP (Brand Agent Portal). Necesitará soporte al enlazar su cuenta, póngase en contacto con el equipo de Revenue Services enviando un correo electrónico a softlayer_revenue_services_team@wwpdl.vnet.ibm.com.

Siga estos pasos para enlazar cada cuenta de SoftLayer con una cuenta de plataforma de {{site.data.keyword.Bluemix_notm}} existente o para crear una nueva:

   1. Inicie sesión en el portal de clientes con su IBMid de cuenta de usuario maestro.
   2. Desde el portal de clientes, haga clic en **Enlazar a una cuenta Bluemix**.
   3. Lea y acepte las condiciones para enlazar cuentas de SoftLayer y {{site.data.keyword.Bluemix_notm}}.
   4. Siga las indicaciones del asistente, incluida la adición de los usuarios de la cuenta de SoftLayer a la cuenta de {{site.data.keyword.Bluemix_notm}}.
   5. Cuando se le solicite, realice una de las siguientes acciones:
     * Si ya tiene una cuenta de {{site.data.keyword.Bluemix_notm}}, proporcione la dirección de correo electrónico asociada a la cuenta para enlazar las cuentas.
     * Si no tiene una cuenta de {{site.data.keyword.Bluemix_notm}}, especifique la dirección de correo electrónico que desea utilizar y siga las instrucciones para ser invitado a {{site.data.keyword.Bluemix_notm}} y cree una cuenta.
   6. Después de que haya enlazado la cuenta, informe al usuario final de cada cuenta para que migre a un IBMid siguiendo el procedimiento que se ha descrito en la sección anterior de [Cambio a IBMid](/docs/account/softlayerlink.html#switchtoIBMid).

      Migre únicamente cuentas de usuario final a IBMid. No migre cuentas derivadas, que son cuentas padre de cuentas de usuario final y no contienen recursos. Los usuarios de cuentas derivadas que migren a un IBMid pierden la posibilidad de iniciar una sesión en el Brand Agent Portal (BAP).
      {: important}

Tenga en cuenta los cambios siguientes una vez que se enlacen las cuentas:
  
  * Ahora inicie sesión en la consola de [{{site.data.keyword.Bluemix}} ![Icono de enlace externo](../icons/launch-glyph.svg)](https://cloud.ibm.com){: new_window}.
  * Debe utilizar las credenciales de IBMid para acceder a sus cuentas tanto de SoftLayer como de {{site.data.keyword.Bluemix_notm}}.
  * Cualquier descuento existente de SoftLayer se aplicará en cargos de {{site.data.keyword.Bluemix_notm}}.
  * Recibirá una factura en dólares de Estados Unidos (USD). Si tiene una cuenta de {{site.data.keyword.Bluemix_notm}}, la facturación a través de {{site.data.keyword.Bluemix_notm}} para los recursos de infraestructura será efectiva para el nuevo ciclo de facturación que empieza una vez que se hayan enlazado las cuentas. Para obtener más información, consulte [Facturación consolidada para cuentas enlazadas](/docs/customer-portal/linking_accounts.html).
  * Puede supervisar el uso de los recursos de infraestructura clásica en la consola de {{site.data.keyword.Bluemix_notm}}.

## Uso de la autenticación de multifactores en cuentas enlazadas
{: #2fa}

Si tiene una cuenta enlazada, puede utilizar la página **Valores** de IAM de {{site.data.keyword.Bluemix_notm}} para habilitar la autenticación de multifactores (MFA) para su cuenta. Se trata de la autenticación de dos factores (2FA) donde se añade una capa de seguridad para acceder a su cuenta más allá del IBMid y de la contraseña necesarios estándares. La autenticación de multifactores (MFA) para su cuenta se aplica a todos los recursos de la cuenta de {{site.data.keyword.Bluemix_notm}} enlazada. Cuando se habilita para su cuenta, también se aplicará a todos los usuarios que se hayan añadido a su cuenta.

Otros métodos de autenticación de multifactores no son por IBMid. Son por cuenta. Cuando un IBMid está asociado con varias cuentas, y cambia entre ellas, debe confirmar su identidad cada vez que cambie a una cuenta distinta que requiera la autenticación de dos factores. Esto es cierto incluso si la cuenta anterior y la cuenta nueva están configuradas con el mismo mecanismo de autenticación de dos factores.

Si anteriormente ha habilitado la [2FA en el portal de clientes](/docs/customer-portal/cpenable2fa.html#customerportal_2fa) para sus recursos de infraestructura clásica y habilita el valor MFA de la cuenta de {{site.data.keyword.Bluemix_notm}}, el valor de la cuenta de MFA sustituye la 2FA que ha configurado en el portal de customer. Esto significa que puede inhabilitar la 2FA que ha adquirido en el portal de clientes en favor del valor MFA de la cuenta. 
