---

copyright:

  years: 2017, 2018
lastupdated: "2018-11-28"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:note: .note}


# Cómo ocultar un recurso público a usuarios
{: #exclude}

Como administrador de su cuenta de {{site.data.keyword.Bluemix}}, puede ocultar un recurso público a los usuarios que tengan acceso a la cuenta. Puede ocultar los recursos para mantener la información confidencial oculta de los usuarios no autorizados o es posible que solo un número determinado de personas necesite acceder a parte de la información.
{:shortdesc}

Ocultar un recurso en el catálogo no lo eliminará de la interfaz de línea de mandatos (CLI) de Cloud Foundry o de la lista de suministro de servicios disponible en la navegación de la consola de {{site.data.keyword.Bluemix_notm}}, como Finanzas, Móvil, Watson y Apps web.
{: note}

Puede utilizar la [interfaz de línea de mandatos (CLI)](/docs/cli/reference/ibmcloud/bx_cli.html#bluemix_catalog_entry_visibility_set) o consola de {{site.data.keyword.Bluemix}} para determinar si tiene acceso para permitir a los usuarios ver un recurso privado que se añadió a la cuenta. Si es propietario de la cuenta, puede dar acceso a un usuario a su cuenta desde la consola asignando una política de acceso. Para obtener más información, consulte [Gestión del acceso a su cuenta](access.html).

## Búsqueda de recursos
{: #find-resource}

Ejecute el mandato `ibmcloud catalog search <service-id or service-name>` para buscar un recurso. Sustituya las variables service-id o service-name con el nombre de recurso o ID. Utilice la información que se devuelve para buscar el ID o nombre del servicio que desea ocultar.

## Obtención de los detalles del recurso

Ejecute el mandato `ibmcloud catalog service <service-id or service-name>`. Con la información que se devuelve de la ejecución del mandato anterior, utilice el mandato para obtener más detalles del recurso. Con la información que se devuelve, puede visualizar la jerarquía, que muestra los recursos hijo de los elementos del recurso.

## Cómo ocultar el recurso
{: #vis-exc}

Ejecute el mandato siguiente para evitar que los usuarios de su cuenta visualicen un recurso público.

`ibmcloud catalog entry-visibility-set <resource-id> —-excludes-add <account-id or account-email>`

Puede añadir una lista separada por comas de correos electrónicos o un ID de cuenta asociado con las cuentas después del indicador de exclusión.

Después de ejecutar el mandato, el proceso para ocultar el recurso tarda aproximadamente 30 minutos. Después de 30 minutos, cierre la sesión y vuelva a iniciarla en su cuenta para ver el recurso oculto.

Las entradas que oculta no están disponibles en la consola o CLI. Los administradores de la cuenta excluida aún pueden ver el recurso.
{: note}

## Cómo eliminar una cuenta de una lista de exclusión
{: #remove-exclude}

Ejecute el mandato siguiente para eliminar un ID de cuenta o un correo electrónico de la lista de exclusión.

`ibmcloud catalog entry-visibility-set <service-id> —-excludes-remove <account-id or account-email>`


## Ejemplo: Gestión de la visibilidad de objetos hijo
{: #child}

Puede gestionar la visibilidad de todos los recursos. Cada recurso hijo tiene sus características visibilidad individuales. En este ejemplo se muestra cómo puede excluir una cuenta del servicio Cloudant público.

Ejecute el mandato `ibmcloud catalog service cloudant` para ver todos los hijos del recurso.

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

Busque el ID de un objeto y excluya una cuenta ejecutando el mandato `ibmcloud catalog entry-visibility-set <resource-id> --excludes-add <account-id or account-email>`.

Para obtener más información sobre cómo funciona la visibilidad, consulte los [documentos de API de catálogo](https://{DomainName}/apidocs/globalcatalog).
