---

copyright:
  years: 2019
lastupdated: "2019-07-26"

keywords: enterprise, add account, import account, create account

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Adición de cuentas a una empresa
{: #enterprise-add}

Puede crear su empresa añadiendo más cuentas de {{site.data.keyword.Bluemix}} a la misma. Para añadir cuentas, puede importar cuentas existentes que no estén en otra empresa, o puede crear nuevas cuentas dentro de la empresa.
{:shortdesc}

Cuando la empresa tenga varias cuentas, puede organizar cuentas relacionadas utilizando grupos de cuentas. Para obtener más información, consulte el apartado [Organización de cuentas en una empresa](/docs/account?topic=account-enterprise-organize).

## Importación de cuentas existentes
{: #add-accounts}

Puede importar cuentas existentes en una empresa. Tras importar una cuenta, ésta no se puede eliminar, y una cuenta sólo puede formar parte de una empresa. Si importa una cuenta Lite o de prueba, se actualiza automáticamente a una [cuenta de Pago según uso](/docs/account?topic=account-accounts).

La importación de una cuenta a la empresa tiene los siguientes impactos:
* La facturación de las transiciones de la cuenta pasa a ser gestionada por la empresa. Después de la transición, los usuarios de la cuenta no pueden acceder a la información de facturación ni de pago, como por ejemplo facturas, pagos o suscripciones, de los periodos de facturación futuros. Para ver o gestionar la facturación, los usuarios deben ser invitados a la cuenta de empresa y se les debe dar acceso al servicio de Facturación en dicha cuenta. Consulte [Gestión centralizada de la facturación y el uso con las empresas](/docs/billing-usage?topic=billing-usage-enterprise) para obtener más información.
* Los usuarios y los permisos de acceso dentro de la cuenta no se cambian. El acceso dentro de la cuenta es independiente de la empresa y los usuarios no obtienen automáticamente acceso dentro de la empresa cuando se importa la cuenta.
* Los recursos dentro de la cuenta no se cambian. Los usuarios con los permisos de acceso correctos pueden seguir visualizando la información de uso de los recursos de la cuenta.

Para importar cuentas existentes en una empresa, es necesario el acceso siguiente:

   * Dentro de la cuenta a importar, debe ser el propietario de la cuenta o tener el rol de Administrador en el servicio de facturación de la cuenta.
   * Dentro de la cuenta de empresa, necesita el rol Editor o Administrador en el servicio de Empresa y el rol de Administrador en el servicio de Facturación.

Para importar una cuenta existente, complete los pasos siguientes:

1. Inicie sesión en la cuenta de empresa y vaya a **Gestión > Empresa**.
1. Pulse **Cuentas** para ver las cuentas y los grupos de cuentas de la empresa. En la sección Cuentas, seleccione **Añadir > Importar cuenta**.
1. Seleccione la cuenta que desea importar.

   Si no se muestran cuentas, probablemente no tiene el acceso adecuado en ninguna de las cuentas existentes.
   {: tip}
1. Si desea añadir la cuenta a un grupo de cuentas, seleccione el grupo de cuentas al que desea añadirla. El grupo que seleccione determina dónde se encuentra la cuenta en la jerarquía de empresa.
1. Revise la información sobre los impactos en la cuenta, y seleccione **Entiendo el impacto en mi cuenta**. A continuación, pulse **Importar**.

   Una vez que la cuenta se ha importado en la empresa, no se puede eliminar. Asegúrese de que realmente desea mover permanentemente la cuenta a la empresa.
   {: important}

### Importación de cuentas utilizando la CLI
{: #add-account-cli}

1. Busque el ID de la cuenta que desea importar a la empresa.

   ```
   ibmcloud account list
   ```
   {: codeblock}
1. Si desea añadir la cuenta a un grupo de cuentas, busque los nombres y los ID de los grupos de cuentas existentes en la empresa.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. Importe la cuenta en la empresa, especificando el ID de cuenta en el parámetro `--account ID`. Si no especifica un grupo de cuentas padre, la cuenta se añade directamente bajo la empresa.

   ```
   ibmcloud enterprise account-import --account-id ID
   [--parent-account-group ACCOUNT_GROUP_NAME | --parent-account-group-id ACCOUNT_GROUP_ID]
   ```
   {: codeblock}

### Importación de cuentas utilizando la API
{: #add-account-api}

Para importar una cuenta existente a la empresa, llame a la [API de gestión de empresa](https://{DomainName}/apidocs/enterprise-apis/enterprise#import-an-account-into-an-enterprise){: external}, como se muestra en la siguiente solicitud de ejemplo. Sustituya las variables de ID y señal de IAM (Identity and Access Management) de {{site.data.keyword.Bluemix_notm}} por los valores de la empresa.

```
curl -X PUT \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID/import/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" -H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID"
}'
```
{: codeblock}

## Creación de cuentas nuevas
{: #create-accounts}

Puede crear nuevas cuentas dentro de la empresa. Las cuentas se crean como cuentas de Pago según uso, y el uso se factura a la empresa. Para crear una cuenta, necesita una política de acceso con el rol Editor o Administrador en el servicio de Empresa.

1. En el panel de control de la Empresa, pulse **Cuentas** para ver las cuentas y los grupos de cuentas de la empresa.
1. En la sección Cuentas, seleccione **Añadir > Crear cuenta**.
1. Especifique un nombre para la cuenta que sea exclusivo dentro de la empresa. Debido a que es una de las muchas cuentas, un nombre exclusivo y descriptivo le ayuda a entender el propósito de la cuenta a simple vista.
1. Si desea asignar un usuario diferente como propietario de la cuenta, especifique su IBMid en el campo **Propietario**. El propietario de la cuenta tiene acceso completo para gestionar la cuenta.
1. Si desea añadir la cuenta a un grupo de cuentas, seleccione el grupo de cuentas al que desea añadirla. El grupo que elija determina dónde se encuentra la cuenta en la jerarquía de empresa.
1. Pulse **Crear**.

Una vez creada la cuenta, el propietario de la cuenta puede iniciar la sesión en la cuenta para invitar a otros usuarios y gestionar su acceso.

### Creación de cuentas utilizando la CLI
{: #create-accounts-cli}

1. Si desea añadir la cuenta a un grupo de cuentas, busque los nombres y los ID de los grupos de cuentas existentes.

   ```
   ibmcloud enterprise account-groups --recursive
   ```
   {: codeblock}
1. Cree la cuenta ejecutando el mandato siguiente. Si no especifica un grupo de cuentas padre, la cuenta se añade directamente bajo la empresa. Para hacer que el propietario de la cuenta sea otro usuario, especifique el IBMid del mismo en la opción `--owner`.

   ```
   ibmcloud enterprise account-create NAME
   [--parent-account-group ACCOUNT_GROUP_NAME] [--owner USER_ID]
   ```
   {: codeblock}

### Creación de cuentas utilizando la API
{: #create-account-api}

Para crear una nueva cuenta en la empresa, llame a la API de Gestión de empresa, tal como se muestra en la siguiente solicitud de ejemplo, sustituyendo las variables de ID y señal de IAM por los valores de la empresa. Para obtener información detallada sobre la API, consulte [API de Gestión de empresa](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-a-new-account-in-an-enterprise){: external}.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/accounts \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID",
  "name": "Sample Account",
  "owner_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}
