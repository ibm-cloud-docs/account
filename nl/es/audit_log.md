---

copyright:
  years: 2018, 2019
lastupdated: "2019-02-05"

keywords: audit log, user access, account log

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:tip: .tip}
{:screen: .screen}
{:new_window: target="_blank"}


# Supervisión de sucesos del sistema con un registro de auditoría
{: #audit-log}

Si tiene una cuenta de infraestructura clásica, puede gestionar sucesos de réplica de almacenamiento visualizando registros de auditoría. Los registros de auditoría realizan un seguimiento de interacciones de cada usuario, como los intentos de inicio de sesión, las actualizaciones de la velocidad de puerto y las interacciones realizadas por el personal de soporte de la infraestructura de {{site.data.keyword.BluSoftlayer_notm}}.
{:shortdesc}


## Visualización del registro de auditoría
{: #view-audit-log}

Para ver el registro de auditoría, vaya a **Gestionar > Cuenta** y seleccione **Registro de auditoría**. El registro de auditoría muestra inicialmente las últimas 25 interacciones realizadas por los usuarios en la cuenta. Puede ver hasta 200 interacciones en cualquier momento. Expanda los artículos por menú de página para ver más resultados.

### Visualización de registros de acceso de un usuario
{: #view-access-logs}

Desde la página del registro de auditoría también puede ver los datos de cada intento de acceso que realiza un usuario específico. Los registros muestran una indicación de fecha y hora y la dirección IP por cada intento de acceso. Utilice los pasos siguientes para ver los Registros de acceso de un usuario.

1. Vaya a **Gestionar > Cuenta** y seleccione **Registro de auditoría**.
2. A continuación, **filtre** en el usuario, seleccione el período de tiempo que desea visualizar y elija el tipo de objeto.  

El registro de acceso para cada usuario muestra los intentos de acceso realizados por dicho usuario por fecha, junto con la dirección IP desde la que se ha realizado el intento de acceso. La información del registro de acceso es de solo lectura.
