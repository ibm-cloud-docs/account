---

copyright:
  years: 2015, 2019
lastupdated: "2019-04-08"

keywords: create account, IBMid, sign up for account, sign up

subcollection: account

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Registro en {{site.data.keyword.Bluemix_notm}}
{: #signup}

Puede registrarse para obtener una cuenta de {{site.data.keyword.Bluemix}} utilizando un IBMid existente o creando un nuevo IBMid. Si la empresa está registrada para utilizar un ID federado para inicio de sesión único, regístrese con su ID federado.
{:shortdesc}

| ID de registro | Detalles |    
|-----------------|---------|
|IBMid existente   | Si ya tiene un IBMid, regístrese en {{site.data.keyword.Bluemix_notm}} con sus credenciales existentes que utilice para otros productos y servicios de IBM. |
|IBMid nuevo        | Si no aún no tiene un IBMid, creará uno cuando se registre. Con un IBMid puede utilizar un nombre de usuario para iniciar sesión en todos los productos y servicios de IBM que utilice, incluido {{site.data.keyword.Bluemix_notm}}. |
|ID federado     | Si la empresa ya ha solicitado registrar las credenciales de usuario desde el dominio de su empresa con IBM, puede registrarse en {{site.data.keyword.Bluemix_notm}} utilizando las credenciales que ya utilice para el inicio de sesión de su empresa. Debe especificar un número de teléfono al registrarse. |
{:caption="Tabla 1. Opciones de ID para registrarse para {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Registro con un IBMid nuevo o existente
{: #signup-ibmid}

Si no forma parte de una empresa que utiliza ID federados, se registrará para {{site.data.keyword.Bluemix_notm}} con un IBMid.

1. Vaya a la [página de inicio de sesión de {{site.data.keyword.Bluemix_notm}}](https://cloud.ibm.com/){: new_window} ![Icono de enlace externo](../icons/launch-glyph.svg "Icono de enlace externo") y pulse **Crear una cuenta de {{site.data.keyword.Bluemix_notm}}**.
1. Especifique su dirección de correo electrónico de IBMid. Si no tiene un IBMid existente, se crea un ID en función del correo electrónico que especifique.
1. Cumplimente los demás campos con su información y pulse **Crear cuenta**.


## Registro con un ID federado
{: #signup-federated}

Un ID federado es un ID dentro del dominio de una empresa que ha sido registrado con IBM, por lo que el dominio y las credenciales de usuario pueden utilizarse para acceder a aplicaciones web de IBM. Solo puede registrarse para {{site.data.keyword.Bluemix_notm}} con un ID federado si su empresa ya está registrada con IBM. El registro del dominio de una empresa con IBM permite que los usuarios puedan iniciar sesión en los productos y servicios de IBM utilizando sus credenciales de usuario de empresa existentes. La autenticación la gestiona el proveedor de identidades de la empresa mediante SSO.

IBM utiliza el Security Assertion Markup Language 2.0 (SAML 2.0) para esta federación de identidad. SAML 2.0 es una versión estándar para intercambiar datos de autenticación entre dominios de seguridad. Es un protocolo basado en XML que utiliza señales de seguridad que contienen aserciones para pasar información entre los "proveedores de identidad" de las organizaciones y el "IBM Rely Party (RP)" conocido como proveedor de servicios.

Para obtener información sobre cómo registrar su empresa para un ID federado, consulte la [Guía de adopción de federación empresarial de IBMid ![icono de enlace externo](../icons/launch-glyph.svg)](https://ibm.box.com/v/IBMid-Federation-Guide){: new_window}. Es necesario un patrocinador de IBM, como un abogado de ofertas o un abogado de cliente, al solicitar el registro de ID federados.

### Inicio de sesión con un ID federado
{: #login-federated}

Al iniciar sesión en la consola de
{{site.data.keyword.Bluemix_notm}} con un ID federado, se le solicita que inicie sesión a través de la página de inicio de sesión de su empresa. Si inicia la sesión a través de una CLI, tendrá que especificar parámetros adicionales para autenticarse. Para obtener más información, consulte [Inicio de sesión con un ID federado](/docs/iam?topic=iam-federated_id).
