---

copyright:
  years: 2015, 2019
lastupdated: "2019-07-18"

keywords: troubleshoot enterprise, enterprise problem, account problem, enterprise support, enterprise help, error message

subcollection: account
---

{:tsSymptoms: .tsSymptoms}
{:tsCauses: .tsCauses}
{:tsResolve: .tsResolve}
{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}
{:new_window: target="_blank"}
{:troubleshoot: data-hd-content-type='troubleshoot'}

# Resolución de problemas de una empresa
{: #enterprise_help}

Entre los problemas generales relacionados con la gestión de la empresa se pueden incluir problemas al intentar aplicar códigos de suscripción o de características, o al intentar añadir una cuenta a la empresa. En muchos de los casos, puede solucionar estos problemas siguiendo unos sencillos pasos.

## ¿Por qué no puedo ver toda la empresa?
{: #troubleshoot-view-enterprise}
{: troubleshoot}

Si no ve toda la empresa, es posible que tenga que comprobar el acceso que tiene asignado.

Puede ver algunas de las cuentas de la empresa, pero no la jerarquía completa de la empresa. La jerarquía de cuentas sólo muestra las cuentas a las que tiene acceso, no toda la cuenta de empresa.
{: tsSymptoms}

Sólo tiene asignado acceso a algunas cuentas de la empresa.
{: tsCauses}

Para comprobar el acceso que tiene asignado, siga estos pasos:
{: tsResolve}

1. Vaya a **Gestionar** &gt; **Acceso (IAM)** > **Usuarios**.
2. Seleccione su nombre.
2. Pulse el separador **Políticas de acceso**.

Póngase en contacto con el propietario de la empresa para solicitar el acceso correcto.

Si es el propietario de la empresa, complete los pasos siguientes para asignar a un usuario acceso a toda la empresa:
1. Vaya a **Gestionar** > **Acceso (IAM)** > **Usuarios**.
2. Seleccione el nombre del usuario. 
2. Pulse el separador **Políticas de acceso** > **Asignar acceso** > **Asignar acceso a servicios de gestión de cuentas**.
3. Seleccione **Empresa** como el servicio y seleccione el nombre de la empresa.
4. Seleccione la cuenta o el grupo de cuentas de la empresa al que desea otorgar acceso al usuario. Por ejemplo, si desea que un usuario tenga acceso para ver sólo una cuenta, seleccione la cuenta y asigne al usuario el rol de Visor o un rol superior. Si desea que un usuario tenga acceso para ver toda la empresa, deje en blanco los campos grupos de cuenta y cuenta y asigne el acceso.

## ¿Por qué no puedo añadir una cuenta existente a la empresa?
{: #troubleshoot-existing-enterprise}
{: troubleshoot}

Al intentar añadir una cuenta existente a la empresa, se produce uno de los siguientes problemas:
{: tsSymptoms}
* Al pulsar **Añadir una cuenta existente** en la sección Cuenta, la cuenta que desea añadir no aparece en la lista.
* No tiene la opción de pulsar **Añadir una cuenta existente**.

No se le ha asignado el acceso correcto.
{: tsCauses}

Si no puede ver la cuenta existente que en la lista de opciones, necesita el rol de Administrador en el servicio de facturación de la cuenta existente.
{: tsResolve}

Para añadir una cuenta existente a la empresa, necesita el rol de Administrador o de Editor en el servicio de facturación de la empresa y el rol de Administrador o Editor en el servicio de empresa para la empresa o el grupo de cuentas padre.

## ¿Por qué no puedo crear una cuenta nueva en la empresa?
{: #troubleshoot-add-enterprise}
{: troubleshoot}

No puede pulsar en **Añadir cuenta** en la sección Cuenta.
{: tsSymptoms}

No se le ha asignado el acceso correcto.
{: tsCauses}

Para crear una cuenta en la empresa, debe tener el acceso siguiente.
{: tsResolve}
1. Rol de Administrador en el servicio de facturación de la empresa.
2. Rol de Administrador o de Editor en el servicio de empresa para la empresa o el grupo de cuentas padre de destino.

## ¿Por qué no puedo ver las suscripciones de empresa?
{: #troubleshoot-viewsub-enterprise}
{: troubleshoot}

Al ir a la página Suscripciones de una cuenta secundaria, se muestra el siguiente mensaje:
{: tsSymptoms}

`Looks like you don't have permission to view subscription data for this account. Contact your account owner or administrator to request access.`

Se muestra el siguiente mensaje en la sección de Facturación del panel de control de la empresa:

`Looks like you don't have permission to view this information. Learn more about IAM access.`

El acceso a la información de facturación y pago para futuros periodos de facturación está limitado a los usuarios de la cuenta de empresa. Los usuarios de una cuenta secundaria no pueden acceder a la información de facturación y de pago, como por ejemplo suscripciones, aunque anteriormente tuvieran acceso a la cuenta.
{: tsCauses}

Para ver o gestionar la facturación, tiene que haber sido invitado a la cuenta de empresa y se le tiene que dar acceso al servicio de Facturación de esa cuenta. Póngase en contacto con el propietario de la cuenta para solicitar acceso.
{: tsResolve}

## ¿Por qué no puedo aplicar un código de suscripción a mi cuenta?  
{: #troubleshoot-promo-enterprise}
{: troubleshoot}

No puede agregar un código de suscripción a su cuenta porque no tiene el acceso correcto.  
{: tsSymptoms}

Debido a que es una cuenta secundaria de la empresa, no puede aplicar códigos de suscripción. Los códigos de suscripción se deben aplicar a nivel de empresa.
{: tsCauses}

Póngase en contacto con el propietario o con el administrador de la empresa para añadir el código de suscripción. Cuando se añade el código de suscripción, se aplica a todas las cuentas de la empresa. Para obtener más información, consulte [Gestión de suscripciones](/docs/billing-usage?topic=billing-usage-subscriptions).
{: tsResolve}
