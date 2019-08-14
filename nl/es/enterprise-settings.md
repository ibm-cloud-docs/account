---

copyright:
  years: 2019
lastupdated: "2019-07-25"

keywords: enterprise, enterprise settings, manage enterprise, view enterprise, rename enterprise

subcollection: account

---

{:shortdesc: .shortdesc}
{:new_window: target="_blank"}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Gestión de la empresa
{: #enterprise-settings}

Desde el panel de control de la empresa de {{site.data.keyword.Bluemix}}, puede ver detalles de empresa, realizar acciones comunes, como añadir cuentas e invitar a usuarios, y ver información de facturación. También puede cambiar el nombre de la empresa en el panel de control o utilizando la CLI o la API.
{:shortdesc}

Para gestionar los valores de la empresa, necesita el rol de Administrador o de Editor del servicio de Empresa en la cuenta de empresa.
{: tip}

## Gestión de la empresa en la consola
{: #enterprise-manage}

Para ver el panel de control de la empresa, vaya a **Gestión > Empresa**. El panel de control ofrece una visión general de las cuentas, los usuarios y el crédito de suscripción en la empresa. El panel de control tiene enlaces rápidos para poder llevar a cabo las acciones comunes siguientes:
   * [Añadir cuentas nuevas o existentes a la empresa](/docs/account?topic=account-enterprise-add)
   * [Invitar a usuarios a la cuenta de empresa](/docs/iam?topic=iam-iamuserinv)
   * [Ver y gestionar el crédito de suscripción](/docs/billing-usage?topic=billing-usage-subscriptions)

Puede renombrar la empresa pulsando en **Renombrar** en la sección Detalles de la empresa.

## Gestión de la empresa desde la CLI
{: #enterprise-manage-cli}

* Ver información de la empresa como por ejemplo el nombre, el dominio, el propietario y las fechas de creación y actualización.

  ```
  ibmcloud enterprise show
  ```
  {: codeblock}
* Renombrar la empresa especificando el nuevo nombre en la opción `-n` en el mandato siguiente.

   ```
   ibmcloud enterprise update -n NEW_NAME
   ```
   {:codeblock}

## Gestión de la empresa utilizando la API
{: #enterprise-manage-api}

Puede actualizar una empresa mediante programación llamando a la API de gestión de empresa tal como se muestra en la siguiente solicitud de ejemplo. Puede actualizar el nombre de la empresa o el dominio pasando los nuevos valores en la llamada de API. Para obtener información detallada sobre la API, consulte la [documentación de la API de Gestión de empresa](https://{DomainName}/apidocs/enterprise-apis/enterprise#update-an-enterprise){: external}.

```
curl -X PATCH \
"https://enterprise.cloud.ibm.com/v1/enterprises/$ENTERPRISE_ID" \
-H "Authorization: $IAM_TOKEN" \
-H 'Content-Type: application/json' \
-d '{
  "name": "Brand New Sample Enterprise",
  "domain": "new.example.com"
}'
```
