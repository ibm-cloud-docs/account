---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, create account group, organize accounts, move accounts

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Organización de cuentas dentro de una empresa
{: #enterprise-organize}

Utilice los grupos de cuentas para organizar las cuentas que están relacionadas en su empresa de {{site.data.keyword.Bluemix}}. Puede crear una jerarquía de empresa de varios niveles anidando grupos de cuentas dentro de un grupo de cuentas. Si es necesario, puede reorganizarlo moviendo cuentas de un grupo de cuentas a otro.
{:shortdesc}

Por ejemplo, el diagrama siguiente muestra una empresa de cuatro niveles que puede configurar anidando grupos de cuentas. En primer lugar, debe crear dos grupos de cuentas que tengan la empresa como padre. A continuación, puede crear dos grupos de cuentas adicionales que tengan uno de estos grupos de cuenta como padre. Puede mover cuentas libremente dentro de los grupos de cuentas, sin importar a qué nivel se encuentran. No obstante, los grupos de cuentas no se pueden mover.

![Un diagrama que muestra cuatro niveles de empresa. El nivel superior es la empresa, que contiene dos niveles de grupos de cuentas. Después, el grupo de cuentas contiene cuentas.](images/enterprise-hierarchy.svg "Los niveles de empresa se crean añadiendo grupos de cuentas.")

Recuerde que el modo en que organiza la empresa afecta a cómo puede realizar el seguimiento de los costes de uso. Para obtener más información, consulte [Gestión centralizada de la facturación y el uso con las empresas](/docs/billing-usage?topic=billing-usage-enterprise).
{: tip}

## Creación de grupos de cuentas
{: #create-account-group}

Para crear un grupo de cuentas, necesita el rol de Administrador o de Editor del servicio de Empresa en la cuenta de empresa.

1. En el panel de control de la Empresa, pulse **Cuentas** para ver las cuentas y los grupos de cuentas de la empresa.
1. En la sección Grupos de cuentas, pulse **Crear**.
1. Especifique un nombre para la cuenta que refleje las cuentas que va a contener. Consulte [¿Cómo puedo utilizar una empresa?](/docs/account?topic=account-enterprise#enterprise-use-cases) para obtener ejemplos de cómo puede organizar las cuentas.
1. Si desea que el contacto principal para el grupo de cuentas sea otro usuario de empresa distinto del suyo, seleccione el IBMid de este usuario en el menú **Contacto**. Si un usuario que desea asignar como contacto no esta en la empresa, primero debe invitar al usuario a la cuenta de empresa. El contacto no se puede cambiar una vez creado el grupo de cuentas. Consulte [Invitación a usuarios](/docs/iam?topic=iam-iamuserinv) para obtener más información.

   El contacto es distinto de un propietario de cuenta en que no tiene ningún acceso adicional dentro del grupo de cuentas ni en las cuentas que contiene. El usuario que se seleccione como contacto actúa como punto focal para cualquier problema del grupo de cuentas. Por ejemplo, si un responsable de finanzas observa que los costes de uso del grupo de cuentas son inesperadamente altos, pueden notificárselo al contacto del grupo de cuentas.


1. Si desea que el grupo de cuentas esté en otra parte de la jerarquía de empresa, seleccione otro padre distinto.

  Los grupos de cuentas no se pueden suprimir ni mover de donde se crean.
  {: note}
1. Pulse **Crear**.

Para crear un nuevo nivel en la jerarquía de empresa, cree nuevos grupos de cuentas dentro del grupo de cuentas. Puede mover cuentas que ya están en la empresa al grupo de cuentas, o bien puede importar o crear cuentas dentro del mismo. Consulte [Adición de cuentas a una empresa](/docs/account?topic=account-enterprise-add) para obtener más información sobre cómo importar y crear cuentas.

### Creación de grupos de cuentas utilizando la CLI
{: #create-account-groups-cli}

Cree un grupo de cuentas ejecutando el mandato siguiente. Para anidar un grupo de cuentas dentro de otro grupo de cuentas, especifique el nombre del grupo de cuentas en la opción `--parent-account-group`. Si desea que otro usuario sea el contacto para el grupo de cuentas, especifique IBMid del mismo en la opción `--primary-contact-id`.

```
ibmcloud enterprise account-group-create NAME
[--parent-account-group ACCOUNT_GROUP_NAME] [--primary-contact-id USER_ID]
```
{: codeblock}

### Creación de grupos de cuentas utilizando la API
{: #create-account-groups-api}

Puede crear mediante programación un grupo de cuentas en la empresa llamando a la API de Gestión de empresa.

En la solicitud de ejemplo siguiente se crea un grupo de cuentas directamente bajo el nivel de empresa. En la llamada a la API, sustituya las variables de ID por los valores de la empresa. Para anidar el grupo de cuentas dentro de otro grupo de cuentas, especifique el ID del grupo de cuentas en el Nombre de recurso de nube (CRN) con el formato siguiente: `crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_ID`.

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/account-groups \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": "crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::enterprise:$ENTERPRISE_ID",
  "name": "Sample Account Group",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

Para obtener información detallada sobre la API, consulte [API de Gestión de empresa](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-account-group){: external}.

## Mover cuentas dentro de la empresa
{: #move-accounts}

Puede mover cuentas a cualquier lugar dentro de la empresa. Por ejemplo, puede mover una cuenta de un grupo de cuentas inferior a su grupo de cuentas padre, o puede ponerla directamente bajo la empresa. Las cuentas sólo se pueden mover dentro de la empresa. No se pueden mover a una empresa distinta ni se pueden eliminar de la empresa para convertirlas en una cuenta autónoma.

Para mover una cuenta, necesita el rol de Administrador en el servicio de Facturación en la cuenta de empresa y el rol de Editor o de Administrador en toda la empresa o en los grupos de cuenta actual y de destino.

1. En el panel de control de Empresa, pulse **Cuentas**.
1. En la sección Cuentas, pulse en el icono Acciones de la fila correspondiente a la cuenta y seleccione **Mover cuenta**.
1. Seleccione el nuevo padre de la cuenta y haga clic en **Guardar**.

### Mover una cuenta utilizando la CLI
{: #move-accounts-cli}

1. Busque el nombre y el ID de la cuenta listando todas las cuentas de la empresa.

   ```
   ibmcloud enterprise accounts --recursive
   ```
   {: codeblock}
1. Si va a mover la cuenta a un grupo de cuentas, busque el nombre y el ID del grupo de cuentas.

   ```
   ibmcloud enterprise account-groups
   ```
   {: codeblock}
1. Mueva la cuenta especificando el nuevo padre en la opción relacionada.

   Para mover la cuenta a un grupo de cuentas, especifique el nombre del grupo de cuentas en la opción `--parent-account-group`.

   ```
   ibmcloud enterprise account-move -n NAME --parent-account-group ACCOUNT_GROUP_NAME
   ```
   {: codeblock}

   Para mover la cuenta directamente bajo la empresa, especifique la opción `--parent-enterprise`.

   ```
   ibmcloud enterprise account-move -n NAME --parent-enterprise
   ```
   {: codeblock}

### Mover cuentas utilizando la API
{: #move-account-api}

Puede mover una cuenta llamando a la API de gestión de empresa tal como se muestra en la siguiente solicitud de ejemplo. Sustituya las variables de ID y señal de IAM por los valores de la empresa.

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/accounts/$ACCOUNT_ID" \
-H "Authorization: Bearer <IAM_Token>" \
-H 'Content-Type: application/json' \
-d '{
  "parent": crn:v1:bluemix:public:enterprise::a/$ENTERPRISE_ACCOUNT_ID::account-group:$ACCOUNT_GROUP_1"",
}'
```
{: codeblock}

Para obtener información detallada sobre la API, consulte [API de Gestión de empresa](https://{DomainName}/apidocs/enterprise-apis/enterprise#move-an-account-with-the-enterprise){: external}.
