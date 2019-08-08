---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, enterprise users, enterprise access, enterprise tutorial

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Cómo empezar con una empresa
{: #enterprise-tutorial}

Esta guía de aprendizaje le guiará en el proceso de configurar una empresa por departamentos de modo que pueda gestionar y realizar un seguimiento de los costes de uso de varias cuentas de {{site.data.keyword.Bluemix}}. Completando esta guía de aprendizaje, aprenderá a crear una empresa, a añadir cuentas y a organizarlas en grupos de cuentas, a invitar a usuarios y a explorar suscripciones.
{:shortdesc}

La guía de aprendizaje utiliza una empresa ficticia denominada *Example Corp* que desea crear una empresa con la estructura siguiente. A medida que complete la guía de aprendizaje, adapte cada paso para ajustarlo a las cuentas de la organización y la estructura deseada.

![Una empresa de cuatro niveles que agrupa las cuentas según los departamentos de la organización. Por ejemplo, los grupos de cuentas se denominan Marketing, Development y Sales. Los grupos de cuentas contienen cuentas para los equipos dentro de esos departamentos. Por ejemplo, el grupo de cuentas de ventas contiene las cuentas Direct, Online y Enablement.](images/enterprise-by-dept.svg "Una empresa que organiza las cuentas según los departamentos de la organización.")

## Antes de empezar
{: #setting-prereqs}

Lea [¿Qué es una empresa?](/docs/account?topic=account-enterprise) para conocer los principios básicos de cómo funciona la gestión de cuentas, la facturación, los recursos y la gestión de usuarios y de acceso a en una empresa.

Verifique que tiene el acceso necesario en una cuenta de suscripción, que sirve como la cuenta base desde la que se crea la empresa. Para crear una empresa, debe ser el propietario de la cuenta o tener el rol de Administrador en el servicio de gestión de cuentas de facturación.

La creación de una empresa a partir de una cuenta y la importación de cuentas existentes no se puede deshacer. Esta guía de aprendizaje se proporciona como un ejemplo de los pasos que puede seguir para configurar una empresa por departamento, pero debe planificar cuidadosamente la estructura empresarial en torno a las necesidades de su organización.
{:important}

## Paso 1. Crear la empresa
{: #create_enterprise_tutorial}

Las empresas se crean a partir de una cuenta de Suscripción existente. Cuando se crea la empresa, la cuenta se añade a la jerarquía de empresa. La facturación pasa a ser gestionada por la empresa, pero sus usuarios y recursos siguen igual y no se ven afectados en absoluto. Para obtener una descripción completa de los impactos en las cuentas, consulte [Creación de una empresa](/docs/account?topic=account-create-enterprise).

1. Vaya a **Gestionar** > **Empresa** y pulse **Crear**.
2. Especifique el nombre de la empresa, como por ejemplo 'Example Corp', para identificar la empresa.
3. Especifique el dominio de su empresa, como por ejemplo `examplecorp.com`.
4. Revise la información sobre el impacto en la cuenta, y seleccione **Entiendo el impacto en mi cuenta**. A continuación, pulse **Crear**. Ahora la cuenta forma parte de la empresa de forma permanente y no se puede eliminar.

Una vez que se crea la empresa, se le redirige al panel de control de la empresa. Desde aquí, puede ver los detalles de la empresa, las cuentas, los usuarios y la información de facturación. Vaya a la página **Cuentas** para ver la estructura de la empresa, donde verá las cuentas siguientes:
  * Una cuenta de empresa con el mismo nombre que la empresa. Esta cuenta se utiliza para la gestión de la empresa.
  * La cuenta desde la que ha creado la empresa. Los usuarios pueden seguir trabajando con los recursos de la cuenta no afectados.

## Paso 2. Crear una estructura de empresa con grupos de cuentas
{: #account_groups_tutorial}

Utilice los grupos de cuentas para organizar las cuentas que están relacionadas. El segundo y tercer nivel de la jerarquía de la empresa Example Corp. contiene los grupos de cuentas Marketing, Development, Sales, Design y Engineering. Complete los pasos siguientes para crear los grupos de cuentas:

1. En el panel de control de la empresa, pulse **Cuentas** para ver las cuentas y los grupos de cuentas de la empresa.
2. En la sección grupo de cuentas, pulse **Crear**.
3. Especifique el nombre del grupo de cuentas, como por ejemplo `Marketing`.
4. En el campo de contacto, especifique el IBMid del usuario que desea que sea el contacto principal del grupo de cuentas. Dado que un grupo de cuentas no puede contener ningún recurso, no tiene un propietario como una cuenta.
5. Seleccione **Example Corp** como la cuenta padre.
6. Pulse **Crear**.

Repita estos pasos para crear los grupos de cuentas Sales, Development, Design y Engineering. Cuando cree los grupos de cuentas Design y Engineering, asegúrese de añadir el Development como el grupo de cuentas padre.

## Paso 3. Importar cuentas existentes
{: #existing_accounts_tutorial}

Ahora que ya ha creado una estructura de empresa, puede importar una cuenta existente a la empresa. Cuando se importa una cuenta, se añade de forma permanente a la empresa. Igual que cuando se crea una empresa, la facturación de las cuentas importadas pasa a ser gestionada por la empresa, pero sus usuarios y recursos permanecen igual. Para obtener detalles, consulte [Importación de cuentas existentes](/docs/account?topic=account-enterprise-add#add-accounts).

Para importar una cuenta existente, es necesario el acceso siguiente:

* Dentro de la cuenta a importar, debe ser el propietario de la cuenta o tener el rol de administrador en los servicios de gestión de cuentas de Empresa y Facturación dentro de la cuenta.
* Dentro de la cuenta de empresa, necesita el rol Editor o Administrador en el servicio de Empresa y el rol de administrador en el servicio de Facturación.

Complete los pasos siguientes para importar la cuenta de UX-UI de ejemplo al grupo de cuentas Design:
1. En el panel de control de la empresa, pulse **Cuentas** para ver las cuentas y los grupos de cuentas de la empresa.
2. En la sección Cuentas, pulse **Añadir** > **Importar cuenta**.
3. Seleccione **UX-UI** en la lista de **Cuentas**.

  Si no se muestran cuentas, probablemente no tiene el acceso adecuado en ninguna de las cuentas existentes.
  {: tip}

4. Seleccione **Design** como padre de la cuenta UX-UI. Esto determina dónde se encuentra la cuenta en la jerarquía de empresa.
5. Revise la información sobre los impactos en la cuenta, y seleccione **Entiendo el impacto en mi cuenta**. A continuación, pulse **Importar**.

Repita los pasos para importar más cuentas.

## Paso 4. Crear cuentas nuevas
{: #create-accounts_tutorial}

Puede crear nuevas cuentas dentro de la empresa. Las cuentas se crean como cuentas de Pago según uso, y el uso se factura a la empresa. Para crear una cuenta, necesita una política de acceso con el rol Editor o Administrador en el servicio de Empresa.

Complete los pasos siguientes para crear la cuenta de ejemplo Web en la empresa:

1. En el panel de control de la Empresa, pulse **Cuentas** para ver las cuentas y los grupos de cuentas de la empresa.
1. En la sección Cuentas, seleccione **Añadir** > **Crear cuenta**.
1. Especifique `Web` como nombre de la cuenta.
1. Si desea asignar un usuario diferente como propietario de la cuenta, especifique su IBMid en el campo **Propietario**. El propietario de la cuenta tiene acceso completo para gestionar la cuenta.
1. Seleccione **Marketing** como padre de esta cuenta.
1. Pulse **Crear**.

Una vez creada la cuenta, el propietario de la cuenta puede iniciar la sesión en la cuenta para invitar a otros usuarios y gestionar su acceso.

Repita los pasos para crear más cuentas. A modo de ejemplo, la empresa Example Corp tiene la siguiente jerarquía de grupos de cuentas hijo y cuentas padre.

| Hijo | Padre |
| ----- | -------|
| Print | Marketing |
| Frontend | Engineering |
| Backend | Engineering |
| Direct | Sales |
| Online | Sales |
| Enablement | Sales |
{:caption="Tabla 1. Jerarquía de grupos de cuentas hijo y padre" caption-side="top"}

## Paso 5. Explorar suscripciones
{: #explore-sub_tutorial}

Puede explorar suscripciones en la empresa desde el panel de control de la empresa. Cualquier suscripción existente de las cuentas importadas en la empresa se traslada a la cuenta de empresa y se añade a la [agrupación de crédito](/docs/billing-usage?topic=billing-usage-enterprise#credit-pool) de la empresa.

1. Vuelva al panel de control de la Empresa pulsando **Panel de control**. En la sección Facturación, puede ver el crédito disponible, el crédito restante y las fechas de caducidad de las suscripciones.
1. Para ver información detallada de todas las suscripciones de la empresa, pulse **Ver suscripciones**.

   En la sección Suscripción de plataforma, puede ver la fecha de inicio de la suscripción, la fecha de finalización, el crédito de inicio y el crédito disponible. Para agregar más crédito, puede comprar suscripciones adicionales y aplicar el código de suscripción.

## Paso 6. Asignar a los usuarios de las cuentas hijo acceso para crear recursos
{: #users_create_resources}

Antes de empezar, asegúrese de cambiar a la cuenta en la que desea crear el recurso. En este caso cambie a la cuenta *Print*. Si desea que los usuarios de la cuenta creen recursos desde el catálogo y los asignen a un grupo de recursos, debe asignar dos tipos de políticas de acceso.
* Asigne una política de acceso con el rol de Visor o superior sobre el grupo de recursos.
* Asigne una política de acceso con el rol Editor o Administrador sobre el servicio.

Complete los pasos siguientes para asignar el acceso necesario:

1. Vaya a **Gestionar** > **Acceso (IAM)** y seleccione **Usuarios**.
2. Seleccione un nombre de usuario de la lista.
3. Pulse el separador **Políticas de acceso** > **Asignar acceso**.
4. Pulse **Asignar acceso dentro de un grupo de recursos**.
5. Seleccione el grupo de recursos al que desea asignar acceso al usuario.
6. Seleccione el rol de Visor o superior en el grupo de recursos.
7. Seleccione el servicio al que desea asignar acceso al usuario.
  * Si desea que el usuario pueda suministrar cualquier servicio, seleccione **Todos los servicios**.
  * Si desea asignar al usuario un acceso específico, seleccione un servicio de la lista. El usuario sólo tiene acceso al servicio seleccionado.
8. Seleccione el rol Editor o Administrador.
9. Pulse **Asignar**.

## Paso 7. Ver el uso de todas las cuentas
{: #usage_tutorial}

1. Inicie la sesión en la cuenta de empresa de Example Corp.
2. Vaya a **Gestionar > Facturación y uso** y seleccione **Uso**.

   La página Uso muestra los costes de todo el uso de la empresa, desglosado por cuenta y grupo de cuentas. No se incluye la información de uso de los servicios de infraestructura clásica para el periodo de facturación actual. Para obtener más información, consulte [Visualización del uso de recursos de la infraestructura clásica](/docs/billing-usage?topic=billing-usage-infra-usage).
3. Pulse en **Marketing** en la tabla para ver el uso dentro del grupo de cuentas. De forma similar al nivel de empresa, el uso se desglosa por cuenta y grupo de cuentas.
4. Para ver el uso por recurso, vaya al nivel de cuenta pulsando en los grupos de cuentas de la tabla o seleccionando la cuenta desde el menú **Empresa**. Se muestran los costes de cada tipo de recurso que se ha utilizado durante el período de tiempo.

Repita estos pasos para ver el uso de los grupos de cuentas Development, Sales, Design y Engineering.

   Desde la cuenta de empresa, no se pueden ver los datos de uso del plan de recursos ni de la instancia porque se requiere acceso dentro de la cuenta. Pulse **Cambiar a la cuenta** para ver los datos de la cuenta. Necesita acceso de facturación a los recursos y servicios de la cuenta. Consulte [Visualización del uso](/docs/billing-usage?topic=billing-usage-viewingusage) para obtener más información.

En la cuenta de empresa sólo se muestran los datos del uso que han realizado las cuentas de la empresa. Para ver el uso desde antes de añadir una cuenta a la empresa, inicie sesión en dicha cuenta y seleccione el intervalo de tiempo correspondiente.
{: note}
