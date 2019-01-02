---



copyright:

  years: 2017, 2018
lastupdated: "2018-11-19"

---

{:shortdesc: .shortdesc}
{:tip: .tip}
{:codeblock: .codeblock}
{:screen: .screen}
{:new_window: target="_blank"}


# Mudando seu plano
{: #changing}

Será possível mudar seu plano de serviço do {{site.data.keyword.Bluemix}} se as mudanças do plano estiverem ativadas para o serviço específico. Você pode desejar mudar seu plano, por exemplo, para fazer upgrade ou reduzir seu plano. É possível mudar seu plano por meio de seu painel da instância de serviço.
{: shortdesc}

Você está procurando detalhes sobre como fazer upgrade de seu tipo de conta? Veja [Como faço upgrade ou mudo o meu tipo de conta?](/docs/account/account_faq.html#changeacct) para obter mais informações. 
{: tip}

É possível mudar os planos de serviços somente para determinados serviços. Se mudanças de plano estiverem ativadas para o serviço, o painel da instância de serviço exibirá uma opção **Plano** na navegação. Cada serviço terá um conjunto diferente de etapas subsequentes se você mudar o seu plano.

1. Clique em **Plano** no painel da instância de serviço. Normalmente, é possível fazer upgrade do plano ou reduzi-lo.
2. Depois de mudar seu plano, deve-se concluir etapas extras. As etapas serão diferentes dependendo do tipo de mudança de plano e do serviço. Por exemplo, se
tiver reduzido o plano, talvez precise remontar seu app. Ou, caso tenha feito upgrade do
plano, talvez seja necessário remontar o app e tomar ações adicionais.

Para remontar seu app, acesse sua lista de recursos para localizar o app ao qual o serviço está ligado. Clique no ícone Menu ![Ícone Menu](../icons/icon_hamburger.svg) **> Lista de recursos**. No menu do app, selecione **Reiniciar app**.

Outras ações de etapa subsequente dependem do serviço. Veja as ações específicas na tabela a seguir.

|Serviço |	Informações|
|--------|-------------|
|Presence Insights 	|Se você tiver um plano Lite e exceder os abonos grátis, uma mensagem 403 será exibida ou registrada para indicar que você não está mais autorizado e que a sua instância de serviço está desativada. Além disso, as chamadas API de REST POST são rejeitadas com uma resposta 403.<br/><br/>Se o serviço estiver desativado porque o abono grátis foi excedido, será necessário fazer upgrade de um plano Lite para um plano Pago. Seu serviço será reativado dentro de 2 horas.<br/><br/>Se você tiver um plano Pago, será possível reduzi-lo para o plano Lite, embora seu uso permaneça dentro do abono do plano Lite para eventos e armazenamento total.<br/><br/>Ao fazer upgrade ou reduzir seu plano, não é necessário remontar ou reiniciar seus apps.|
{:caption="Tabela 1. Próximas etapas para mudar seu plano" caption-side="top"}


## Mudando seu plano por meio da interface da linha de comandos
{: #changing_command_line}

Opcionalmente, é possível mudar o seu plano de serviço por meio da interface da linha de comandos inserindo o comando a seguir:

```
cf update-service <service_name> [-p <new_plan>]
```
