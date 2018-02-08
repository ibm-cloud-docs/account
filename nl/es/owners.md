---

copyright:

  years: 2017, 2018
lastupdated: "2018-01-10"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}

# Cambio de la propiedad de recursos privados

Puede cambiar la propiedad de la cuenta con la interfaz de línea de mandatos. Una vez que haya creado y personalizado recursos privados en el catálogo, puede transferir la propiedad de dichos recursos a otra persona. Después de transferir la propiedad, no podrá ver el recurso desde su cuenta. El cambio de la propiedad de la cuenta no se puede deshacer, hágalo con cautela.
{:shortdesc: .shortdesc}

## Cómo cambiar el propietario de un recurso de catálogo

Para cambiar el propietario de un recurso, utilice el mandato siguiente con la [CLI](/docs/cli/reference/bluemix_cli/bx_cli.html#bx_commands_settings):

`bx catalog entry-visibility-set <service-id> --owner <account-id or account-email>`
