---

copyright:

  years: 2017, 2018
lastupdated: "2018-08-02"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Cómo ocultar un recurso público a usuarios de su cuenta
{: #exclude}

Si es un administrador de la cuenta, puede ocultar un recurso público a todos los usuarios de la cuenta. Añada el recurso a una lista de exclusión con la [interfaz de línea de mandatos](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set) de `ibmcloud`.
{:shortdesc: .shortdesc}

**Nota:** Ocultar un recurso en el catálogo no lo eliminará de la CLI de Cloud Foundry ni de las listas de suministro de servicio disponibles a través de la navegación global, como Finanzas, Móvil, Watson y Apps web.

## ¿Cómo sé si tengo acceso?
{: #find-access}

Puede utilizar la CLI o la interfaz de usuario de identidad y acceso para determinar si tiene acceso para permitir a los usuarios ver un recurso privado que se añadió a la cuenta. Si es propietario de la cuenta, puede dar acceso a un usuario a su cuenta a través de la interfaz de usuario de Identity and Access Management asignando una política de acceso. Para obtener más información, consulte [Gestión del acceso a su cuenta](access.html).

## Paso 1: Buscar un recurso
{: #find-resource}

Indique `ibmcloud catalog search <service-id or service-name>` para buscar un recurso. Sustituya service-id o service-name con un ID o nombre de recurso. Busque el ID o el nombre del servicio que desea ocultar en la información que se devuelve.

## Paso 2: Obtener los detalles de ese servicio

Indique `ibmcloud catalog service <service-id or service-name>`. Con lo que ha encontrado en el mandato anterior, utilice este mandato para examinar más detalles del recurso. Con la información que devuelve, puede ver la jerarquía, que muestra los recursos hijo de los elementos del recurso.

## Paso 3: Ocultar el recurso
{: #vis-exc}

Especifique el mandato siguiente para evitar que su cuenta vea un recurso público.

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

Detrás del distintivo `excludes`, puede añadir una lista separada por comas de correos electrónicos o ID de cuenta asociados con cuentas.

Después de ejecutar el mandato, el proceso para ocultar el recurso tarda 30 minutos. Después de 30 minutos, cierre la sesión y vuelva a su cuenta para ver el recurso oculto.

**Nota:** Las entradas que oculta no están disponibles desde la interfaz de usuario ni la CLI de {{site.data.keyword.Bluemix}}. Las entradas ocultas todavía son visibles en el mercado de Cloud Foundry, pero no se puede suministrar un plan oculto desde Cloud Foundry. Los administradores de la cuenta excluida aún pueden ver el recurso.

## Eliminar una cuenta de la lista de exclusión
{: #remove-exclude}

Especifique el mandato siguiente para eliminar un ID de cuenta o un correo electrónico de la lista de exclusión.

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`

## Ejemplo de gestión de visibilidad de objetos hijo
{: #child}

Puede gestionar la visibilidad de todos los recursos. Cada recurso hijo tiene sus características visibilidad individuales.

En este ejemplo, puede excluir una cuenta del servicio Cloudant público.

Si indica `ibmcloud catalog service cloudant`, puede ver los hijos del recurso.

```
ID                 cloudant
Name               cloudantnosqldb
Kind               service
Provider           IBM
Tags               data_management, ibm_created, ibm_dedicated_public, lite
Active             true
Description        Cloudant NoSQL DB es una capa de datos totalmente gestionada diseñada para aplicaciones  móviles y web modernas que utilizan un esquema JSON flexible. Cloudant se basa en, y es compatible con, Apache CouchDB, y es accesible mediante una API HTTPS segura, que se escala a medida que la aplicación crece. Cloudant dispone de los certificados ISO27001 y SOC2 Tipo 1, y todos los datos se almacenan por triplicado en nodos físicos distintos de un clúster a fin de obtener alta disponibilidad y recuperación tras desastre en un centro de datos.
Bindable           true
RC Compatible      false
RC Provisionable   false
Children           Name                                          Kind         ID                                               Location
                   lite                                          plan         cloudant-lite
                   |__lite-eu-gb                             deployment   cloudant-lite:eu-gb                          eu-gb
                   |  |__lite-alias-eu-gb                    alias        cloudant-lite:alias:eu-gb                    eu-gb
                   |__lite-us-south                          deployment   cloudant-lite:us-south                       us-south
                      |__lite-alias-us-south                 alias        cloudant-lite:alias:us-south                 us-south
                   standard                                      plan         cloudant-standard
                   |__standard-eu-gb                         deployment   cloudant-standard:eu-gb                      eu-gb
                   |  |__standard-alias-eu-gb                alias        cloudant-standard:alias:eu-gb                eu-gb
                   |__standard-us-south                      deployment   cloudant-standard:us-south                   us-south
                      |__standard-alias-us-south             alias        cloudant-standard:alias:us-south             us-south
```

Busque el ID de un objeto y excluya una cuenta con `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

Para obtener más información sobre cómo funciona la visibilidad, consulte los [Documentos de API](https://console.bluemix.net/apidocs/globalcatalog).
