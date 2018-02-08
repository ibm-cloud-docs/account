---

copyright:

  years: 2017, 2018
lastupdated: "2017-12-06"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Adición de cuentas al recurso privado
{: #include}

Cualquier recurso privado que cree está restringido de forma predeterminada. Si es un administrador de la cuenta, puede decidir quién puede ver su recurso añadiéndolos a una lista de inclusión con la [interfaz de línea de mandatos](/docs/cli/reference/bluemix_cli/bx_cli.html#bluemix_catalog_entry_visibility_set) de `bx`.
{:shortdesc: .shortdesc}

## ¿Cómo sé si tengo acceso?
{: #find-access}

Puede utilizar la CLI o la interfaz de usuario de identidad y acceso para determinar si tiene acceso para permitir a los usuarios ver un recurso privado que se ha añadido a la cuenta. Si es propietario de la cuenta, puede dar acceso a un usuario a su cuenta a través de la interfaz de usuario de Identity and Access Management asignando una política de acceso. Para obtener más información, consulte [Gestión del acceso a su cuenta](access.html).

## Paso 1: Buscar el recurso
{: #find-resource}

Indique `bx catalog service <service-id or service-name>`. Sustituya service-id o service-name con el ID o nombre del recurso. Con la información que devuelve, puede ver la jerarquía, que muestra los recursos hijo de los elementos del recurso.

## Paso 2: Definir la visibilidad incluyendo una cuenta
{: #vis-inc}

Especifique el mandato siguiente para permitir que una cuenta vea el recurso privado.

`bx catalog entry-visibility-set <service-id> --includes-add <account-id or account-email>`

Detrás del distintivo includes-add, puede añadir una lista separada por comas de correos electrónicos o ID asociados con cuentas.

Después de ejecutar el mandato, el proceso para incluir el recurso tarda 30 minutos. Después de 30 minutos, cierre la sesión y vuelva a su cuenta para ver el recurso incluido.

## Eliminar una cuenta de la lista de inclusiones
{: #remove-exclude}

Especifique el mandato siguiente para eliminar una cuenta de la lista de inclusiones.

`bx catalog entry-visibility-set <service-id> --includes-remove <account-id or account-email>`

## Gestión de visibilidad de objetos hijo
{: #child-vis}

Puede gestionar la visibilidad del recurso o de sus hijos.

Una lista de inclusiones vacía significa que solo lo pueden ver los administradores de la cuenta. La cuenta debe estar en la lista de inclusiones para que todos los miembros de la cuenta puedan verlo.

Por ejemplo, si especifica `bx catalog service <your_service>`, puede ver los hijos del recurso.

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

Puede obtener el ID de recurso para el despliegue del hijo y luego incluir una cuenta utilizando el mandato siguiente. `bx catalog entry-visibility-set <service-id> —-includes-add <some-other-account>`.

Los hijos de un objeto pueden heredar la visibilidad de una forma compleja. Si el objeto hijo es privado, tiene su propia configuración de visibilidad. Sin embargo, si el objeto hijo se establece en público, hereda la visibilidad de su padre. Establecer la visibilidad en un objeto hijo privado puede restringirla más que en el padre.

Para obtener más información sobre cómo funciona la visibilidad, consulte los [Documentos de API](https://console.bluemix.net/apidocs/682).
