---

copyright:
  years: 2019
lastupdated: "2019-07-29"

keywords: enterprise, enterprise account, create enterprise, set up enterprise, multiple account

subcollection: account

---

{:shortdesc: .shortdesc}
{:external: target="_blank" .external}
{:codeblock: .codeblock}
{:important: .important}
{:tip: .tip}
{:note: .note}

# Creación de una empresa
{: #create-enterprise}

Una empresa de {{site.data.keyword.Bluemix}} se crea a partir de una cuenta de suscripción. La cuenta que se utiliza para crear la empresa se añade permanentemente a la empresa.
{:shortdesc}

## Antes de empezar
{: #create-prereqs}

Para crear una [empresa de {{site.data.keyword.Bluemix_notm}}](/docs/account?topic=account-enterprise), debe ser el propietario de la cuenta o tener el rol de Administrador en el servicio de Gestión de cuentas de facturación en una cuenta de Suscripción.

La cuenta de Suscripción que se utiliza para crear la empresa se mueve permanentemente a la empresa. Mover la cuenta a la empresa tiene los siguientes impactos:
* La facturación de las transiciones de la cuenta pasa a ser [gestionada por la empresa.](/docs/billing-usage?topic=billing-usage-enterprise). Después de la transición, los usuarios de la cuenta no pueden acceder a la información de facturación ni de pago, como por ejemplo facturas, pagos o suscripciones, de los periodos de facturación futuros. Para ver o gestionar la facturación, los usuarios deben ser invitados a la cuenta de empresa y se les debe dar acceso al servicio de Facturación en dicha cuenta.
* Los usuarios y los permisos de acceso dentro de la cuenta no se cambian. El acceso dentro de la cuenta es independiente de la empresa y los usuarios no obtienen automáticamente acceso dentro de la empresa cuando se añade la cuenta. Sin embargo, como se ha mencionado anteriormente, la información de facturación ya no está disponible dentro de la cuenta independientemente de los permisos de acceso.
* Los recursos dentro de la cuenta no se cambian. Los usuarios con los permisos de acceso correctos pueden seguir visualizando la información de uso de los recursos de la cuenta.

Si no tiene una cuenta de Suscripción, puede actualizar su cuenta como se describe en [Actualización de la cuenta](/docs/account?topic=account-upgrading-account).

## Creación de una empresa en la consola
{: #create-console}

1. Vaya a **Gestionar > Empresa** y pulse **Crear**.
1. Especifique un nombre exclusivo para identificar la empresa. Por lo general, el nombre refleja la empresa u organización, por ejemplo, `My organization's enterprise`. Puede editar el nombre de empresa más adelante si es necesario.
1. Si su empresa u organización tiene un nombre de dominio asociado, especifíquelo en el campo **Dominio**. Puede especificar cualquier formato de dominio o subdominio, como por ejemplo `example.com` o `my.example.com`.
1. Revise la información sobre el impacto en la cuenta, y seleccione **Entiendo el impacto en mi cuenta**. A continuación, pulse **Crear**.

   Una vez que la cuenta se ha añadido a la empresa, no se puede eliminar. Asegúrese de que realmente desea mover permanentemente la cuenta a una empresa.
   {: important}

Al cabo de unos momentos, se crea la empresa y puede ver el panel de control de la empresa. Su IBMid aparece listado como contacto. El contacto sirve como punto focal para cualquier asunto de la empresa, como por ejemplo preguntas sobre facturación o uso. También se le asigna como propietario de cuenta de empresa, de forma que puede invitar a usuarios adicionales a gestionar la empresa.

Pulse en **Cuentas** para ver la jerarquía de la empresa, que contiene dos cuentas.

* La cuenta de empresa, que es dónde invita a usuarios y otorga acceso para gestionar la empresa.
* La cuenta que ha utilizado para crear la empresa. Sus usuarios y recursos siguen siendo los mismos, pero la facturación ahora está gestionada por la empresa.

## Creación de una empresa utilizando la CLI
{: #create-cli}

1. Inicie sesión y seleccione la cuenta.

   ```
   ibmcloud login
   ```
   {:codeblock}
1. Cree la empresa ejecutando el mandato siguiente, donde `NAME` es un nombre exclusivo para identificar la empresa.

   ```
   ibmcloud enterprise create NAME [-d, --domain DOMAIN_NAME] [--primary-contact-id PRIMARY_CONTACT_USER_ID]
   ```
   {:codeblock}

   Por ejemplo, el mandato siguiente crea una empresa llamada `Example Corp Enterprise` con el dominio `examplecorp.com`.

   ```
   ibmcloud enterprise create "Example Corp Enterprise" -d examplecorp.com
   ```
   {:codeblock}

   De forma predeterminada, la empresa se crea con el usuario conectado actualmente con los roles siguientes:
      * El contacto de la empresa, que identifica a una persona focal a la que notificar los problemas relacionados con la empresa
      * El propietario de la cuenta de empresa, que tiene acceso completo a la gestión de la cuenta de empresa

   Puede especificar el IBMid de otro usuario distinto en la opción `--primary-contact-id`. Los dos roles se asignan al mismo usuario.
1. Revise el impacto en la cuenta, y confirme que desea continuar escribiendo `y`.
   ```
   Account abcde12345fghij67890 will be incorporated into enterprise My new enterprise
   (which cannot be undone). Do you want to proceed? [y/N]> y
   ```

Una vez creada la empresa, se visualizan dos nuevos ID. El primer ID está asociado a la empresa, y el segundo ID identifica la cuenta de empresa, que se utiliza para gestionar la empresa.

```
ID:                      09876jihgf54321edcba   
Enterprise Account ID:   edcba12345jihgf67890
```

La cuenta que ha utilizado para crear la empresa forma ahora parte de la empresa. Ejecute el mandato [`ibmcloud enterprise accounts`](/docs/cli?topic=cloud-cli-ibmcloud_enterprise#ibmcloud_enterprise_accounts) para ver las dos cuentas de la empresa: la cuenta de empresa y la cuenta que ha utilizado para crear la empresa.

## Creación de una empresa utilizando la API
{: #create-api}

Puede crear una empresa mediante programación llamando a la API de gestión de empresa tal como se muestra en la siguiente solicitud de ejemplo. <!-- For detailed information about the API, see [Enterprise Management API](https://{DomainName}/apidocs/enterprise-apis/enterprise#create-an-enterprise){: external}.-->

```
curl -X POST \
"https://enterprise.cloud.ibm.com/v1/enterprises \
-H "Authorization: Bearer <Token>" \
-H 'Content-Type: application/json' \
-d '{
  "source_account_id": "a1b2c32a5ea94809a9840f5e23c362d",
  "name": "Sample Enterprise",
  "domain": "example.com",
  "primary_contact_iam_id": "IBMid-0123ABC"
}'
```
{: codeblock}

## Pasos siguientes
{: #create-next-steps}

Cree la estructura de la empresa añadiendo más cuentas existentes o creando nuevas cuentas dentro de la empresa. Para obtener más información, consulte [Adición de cuentas en la empresa](/docs/account?topic=account-enterprise-add).

También puede invitar a usuarios adicionales a la cuenta de empresa para que puedan ayudarle a gestionar la empresa. Por ejemplo, es posible que desee invitar a un responsable de finanzas para gestionar la facturación y hacer el seguimiento de los costes de uso, e invitar a los jefes de departamento para que administren las cuentas. Consulte [Invitación a usuarios](/docs/iam?topic=iam-iamuserinv) para obtener más información sobre cómo invitar a usuarios.
