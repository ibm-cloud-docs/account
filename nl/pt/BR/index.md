---

copyright:

  years: 2015, 2018
lastupdated: "2018-09-04"

---

{:shortdesc: .shortdesc}
{:codeblock: .codeblock}
{:screen: .screen}
{:tip: .tip}
{:new_window: target="_blank"}

# Tipos de Conta
{: #accounts}

É possível escolher entre três tipos de contas do {{site.data.keyword.Bluemix}}: Lite, Pré-paga e de Assinatura. É possível usar qualquer um dos tipos de contas para começar a usar o {{site.data.keyword.Bluemix_notm}} - escolha aquele que
melhor se adequar às suas necessidades.
{:shortdesc}

## Comparando contas
{: #compare}

A tabela a seguir fornece uma comparação das contas Lite, Pré-paga e de Assinatura. Para obter mais detalhes sobre cada conta, consulte as seções a seguir.

|  | Lite  | Pré-paga | Inscrição |
|--------------------|--------------------|--------------------|--------------------|
| **Acesso à memória do Cloud Foundry grátis** | 256 MB | 512 MB | 512 MB |
| **Acesso aos [Planos de serviço Lite ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/catalog/?search=label:lite){: new_window}** | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Acesso a todos os planos grátis** |  | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Acesso ao catálogo completo do {{site.data.keyword.Bluemix_notm}}** |  | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Acesso a múltiplas regiões do Cloud Foundry** |  | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Sem restrições de tempo** | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Custo zero garantido** | ![Recurso disponível](../icons/icon_enabled.svg) |  |  |
| **Precificação com desconto** |  |  | ![Recurso disponível](../icons/icon_enabled.svg) |
| **Melhor para provas de conceito de aprendizado ou construção** | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |  |
| **Adequado para casos de uso de produção** |  | ![Recurso disponível](../icons/icon_enabled.svg) | ![Recurso disponível](../icons/icon_enabled.svg) |
{: caption="Tabela 1. Comparação de contas do {{site.data.keyword.Bluemix_notm}}" caption-side="top"}

## Conta Lite
{: #liteaccount}

Inscreva-se para uma conta Lite para começar a construir seus apps e explorar serviços com planos Lite grátis selecionados, que são exibidos com uma tag Lite ![Tag Lite](../icons/Lite.svg) no console do {{site.data.keyword.Bluemix_notm}}. Sua conta Lite não expira e seu cartão de crédito não é necessário.

Você tem acesso a um único grupo de recursos que é criado e denominado `Default`. Todas as suas instâncias de serviços que são gerenciadas pelo {{site.data.keyword.Bluemix_notm}} Identity and Access Management (IAM) são incluídas automaticamente nesse grupo de recursos. É possível atualizar o nome desse grupo de recursos a qualquer momento. Consulte [Renomeando um grupo de recursos](/docs/resources/resourcegroups.html#renaming-a-resource-group) para obter as etapas detalhadas.

Cada grupo de recursos é livre. Ao criar uma conexão entre um serviço gerenciado pelo IAM e um app Cloud Foundry, você cria um alias, que é uma instância de serviço, que conta para sua cota. Consulte [O que é um alias?](/docs/resources/connecting_apps.html#what_is_alias).
{: tip}

### O que está disponível?

Confira a lista a seguir de recursos-chave que estão disponíveis em uma conta Lite:

   * A conta é grátis, nenhum cartão de crédito é necessário.
   * A conta nunca expira.
   * É possível usar uma organização em uma região do {{site.data.keyword.Bluemix_notm}}.
   * Suporte básico do {{site.data.keyword.Bluemix_notm}} de graça. O suporte básico é fornecido para ambientes de não produção ou cargas de trabalho em que severidades tradicionais não são usadas e tempos de resposta específicos não são estipulados.
   * Você recebe notificações por e-mail sobre o status da conta e limites de cota.
   * Seus apps Cloud Foundry podem acessar até 256 MB de memória instantânea de tempo execução grátis.
   * É possível provisionar uma instância de qualquer serviço no catálogo do [{{site.data.keyword.Bluemix_notm}} ![Ícone de link externo](../icons/launch-glyph.svg "Ícone de link externo")](https://console.bluemix.net/catalog/?search=label:lite%20lite){: new_window} que tenha um plano Lite.
   * Depois de 10 dias sem atividade de desenvolvimento, seus apps serão suspensos. É possível começar a trabalhar em novos apps sem ter que se preocupar com atingir os limites de cota de memória.
   * Depois de 30 dias sem atividade de desenvolvimento, suas instâncias de serviço com planos Lite serão excluídas. Dessa forma, você não precisa gerenciar a exclusão de instâncias inativas antes de criar novas.

### Fazendo upgrade de sua conta
{: #upgrade-to-paygo}

Quando estiver pronto para crescer, será possível fazer upgrade da sua conta Lite para uma conta pré-paga ou da
assinatura. 

  * Para fazer upgrade para uma conta pré-paga, acesse **Gerenciar** > **Faturamento e uso** > **Faturamento** no console e clique em **Incluir cartão de crédito**.
  * Para fazer upgrade para uma conta da assinatura, acesse **Gerenciar** > **Faturamento e
uso** > **Faturamento** no console e clique em **Saiba mais**.

## Conta pré-paga
{: #paygo}

Com uma conta pré-paga, é possível criar múltiplos grupos de recursos para gerenciar facilmente a cota e visualizar o uso de faturamento para um conjunto de recursos. Seus encargos se baseiam em seu uso de cálculos e serviços do {{site.data.keyword.Bluemix_notm}}. Você é elegível para abonos grátis de tempo de execução e serviço. Se você usar além do abono grátis, receberá uma fatura mensal do {{site.data.keyword.Bluemix_notm}}. A fatura será em dólares dos Estados Unidos (US$) e fornecerá detalhes sobre os encargos do recurso.

Se você vincular sua conta pré-paga a uma conta do SoftLayer, começando no primeiro dia do próximo mês, seus encargos combinados serão incluídos na fatura do {{site.data.keyword.Bluemix_notm}}.
{: tip}

É possível fazer upgrade para uma conta pré-paga por meio do console do {{site.data.keyword.Bluemix_notm}}. Depois de fornecer suas informações de faturamento e cartão de crédito, aceite os termos e condições e envie sua solicitação de conta. Em seguida, seu cartão de crédito será validado. Você também receberá um e-mail de confirmação sobre as informações da conta. Alguns minutos após o recebimento do e-mail de confirmação, é possível retornar ao console para continuar a construção de seus apps. Se a sua solicitação on-line não puder ser processada para seu país ou região, entre em contato com o [Suporte ao {{site.data.keyword.Bluemix_notm}}](/docs/get-support/howtogetsupport.html).

Você obterá um crédito promocional de US$ 200 após fazer upgrade para uma conta Pré-paga e o crédito será automaticamente aplicado à sua conta. Seu crédito de US$ 200 é válido por 30 dias e é automaticamente aplicado à sua fatura. O crédito não pode ser usado com ofertas de terceiros.

### Fazendo upgrade de sua conta
{: #upgrade-to-subscription}

Será possível fazer upgrade de sua conta pré-paga para uma conta de Assinatura a qualquer momento. Entre em contato com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg) para obter mais detalhes.

## Conta Assinatura

Com uma conta Assinatura, é possível criar múltiplos grupos de recursos para gerenciar facilmente a cota e visualizar o uso de faturamento para um conjunto de recursos. Você se compromete com um valor de gasto mínimo a cada mês e recebe um desconto de assinatura que é aplicado a esse encargo mínimo. Será cobrada uma taxa sem desconto por qualquer uso que exceda o seu valor total de assinatura.

Se você tiver uma conta de assinatura, será possível criar a maioria dos serviços que estão disponíveis no [Catálogo
do IBM Cloud](https://console.bluemix.net/catalog/), no entanto, poderá haver determinados serviços que usam um plano de precificação específico que requer que você o compre separadamente.

Se você vincular sua conta de Assinatura a uma conta do SoftLayer, começando no primeiro dia do próximo mês, seus encargos combinados serão incluídos na fatura do {{site.data.keyword.Bluemix_notm}}.
{: tip}

### Conta do {{site.data.keyword.Bluemix_dedicated_notm}}

Com o {{site.data.keyword.Bluemix_dedicated_notm}}, é necessário inscrever-se para um prazo mínimo de um ano que inclui:

   * Conectividade VPN de volta para a sua infraestrutura
   * Ambiente completamente redundante em um data center do {{site.data.keyword.BluSoftlayer_notm}}
   * Todos os tempos de execução suportados (IBM Java Liberty, Node.js e tempos de execução de software livre integrados)
   * Todos os serviços dedicados que você selecionou e todos os serviços públicos do {{site.data.keyword.Bluemix_notm}}
   * Suporte {{site.data.keyword.Bluemix_notm}} padrão

Também é possível pedir itens opcionais, tais como
o SoftLayer DirectLink ou opções de suporte premium. Entre em contato com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg) para obter informações adicionais.

O que é pago todos os meses durante esse prazo baseia-se nos serviços dedicados que você deseja, além de uma conta Assinatura que fornece acesso a todos os serviços públicos. Os encargos de uso dos serviços no {{site.data.keyword.Bluemix_notm}} Público são calculados com base no contrato da conta da assinatura. Você recebe
uma fatura para os serviços usados, além desse contrato de
assinatura. Entre em contato com o representante de conta designado da IBM ou com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg) para iniciar seu contrato.

### Conta do {{site.data.keyword.Bluemix_local_notm}}

Com o {{site.data.keyword.Bluemix_local_notm}}, deve-se inscrever por um prazo mínimo de um ano que inclui:

   * Uma capacidade de entrega denominada retransmissão que permite que a IBM se conecte à implementação local e
entregue atualizações de forma automática e consistente.
   * Todos os tempos de execução suportados (IBM Java Liberty, Node.js e tempos de execução de software livre integrados)
   * Todos os serviços locais selecionados e acesso a todos os serviços públicos do {{site.data.keyword.Bluemix_notm}}
   * Suporte {{site.data.keyword.Bluemix_notm}} padrão

O que é pago todos os meses durante esse prazo é baseado nos serviços locais que você deseja, além de uma conta Assinatura que fornece acesso a todos os serviços públicos. Os encargos de uso dos serviços no {{site.data.keyword.Bluemix_notm}} Público são calculados com base no contrato da conta da assinatura. Você recebe
uma fatura para os serviços usados, além desse contrato de
assinatura. Entre em contato com o representante de conta designado da IBM ou com [Vendas do {{site.data.keyword.Bluemix_notm}}](https://www.ibm.com/cloud-computing/bluemix/contact-us){: new_window} ![Ícone de link externo](../icons/launch-glyph.svg) para iniciar seu contrato.



