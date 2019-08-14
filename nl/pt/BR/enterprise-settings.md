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

# Gerenciando sua empresa
{: #enterprise-settings}

No painel de sua empresa do {{site.data.keyword.Bluemix}}, é possível visualizar detalhes corporativos, executar ações comuns, como incluir contas, convidar usuários e visualizar informações de faturamento. Também é possível renomear sua empresa no painel ou usar a CLI ou a API.
{:shortdesc}

Para gerenciar as configurações corporativas, é necessária a função de Administrador ou de Editor no Serviço corporativo na conta corporativa.
{: tip}

## Gerenciando sua empresa no console
{: #enterprise-manage}

Para visualizar o painel corporativo, acesse **Gerenciar > Empresa**. O painel fornece uma visão geral de contas, usuários e crédito de assinatura em sua empresa. O painel tem links rápidos para que seja possível executar as ações comuns a seguir:
   * [Incluir contas novas ou existentes em sua empresa](/docs/account?topic=account-enterprise-add)
   * [Convidar usuários para a conta corporativa](/docs/iam?topic=iam-iamuserinv)
   * [Visualizar e gerenciar crédito de assinatura](/docs/billing-usage?topic=billing-usage-subscriptions)

Além disso, é possível renomear sua empresa clicando em **Renomear** na seção Detalhes corporativos.

## Gerenciando sua empresa por meio da CLI
{: #enterprise-manage-cli}

* Visualize informações corporativas, como o nome, o domínio, o proprietário e as datas de criação e atualização.

  ```
  ibmcloud enterprise show
  ```
  {: codeblock}
* Renomeie a empresa ao especificar o novo nome na opção `-n` no comando a seguir.

   ```
   ibmcloud enterprise update -n NEW_NAME
   ```
   {:codeblock}

## Gerenciando sua empresa usando a API
{: #enterprise-manage-api}

É possível atualizar programaticamente uma empresa chamando a API de gerenciamento corporativo, conforme mostrado na solicitação de amostra a seguir. É possível atualizar o nome da empresa ou o domínio, transmitindo os novos valores na chamada da API. Para obter informações detalhadas sobre a API, consulte a [documentação da API de gerenciamento corporativo](https://{DomainName}/apidocs/enterprise-apis/enterprise#update-an-enterprise){: external}.

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
